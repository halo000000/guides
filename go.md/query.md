## query parameters in Go using the `net/http` package
To retrieve query parameters in Go using the `net/http` package, you can use the `URL.Query()` method of the `http.Request` object. This method returns a `url.Values` map, which allows you to easily access query parameters by their key.

Here’s an example:

```go
package main

import (
	"fmt"
	"net/http"
)

func handler(w http.ResponseWriter, r *http.Request) {
	// Parse query parameters
	queryParams := r.URL.Query()

	// Retrieve specific parameters
	param1 := queryParams.Get("param1") // Get a single value for the "param1" key
	param2 := queryParams.Get("param2")

	// Print them to the response
	fmt.Fprintf(w, "param1: %s\n", param1)
	fmt.Fprintf(w, "param2: %s\n", param2)

	// Optional: Iterate over all query parameters
	for key, values := range queryParams {
		for _, value := range values {
			fmt.Fprintf(w, "Key: %s, Value: %s\n", key, value)
		}
	}
}

func main() {
	http.HandleFunc("/", handler)

	fmt.Println("Server is running on http://localhost:8080")
	http.ListenAndServe(":8080", nil)
}
```

### Explanation:
1. **`r.URL.Query()`**:
   - Returns the query parameters as a `url.Values` map, where each key maps to a slice of strings (`map[string][]string`).

2. **`queryParams.Get("key")`**:
   - Fetches the first value associated with the given key.

3. **Iteration**:
   - If you want to handle multiple values for a single key, iterate over the slice.

### Example Query:
If the URL is `http://localhost:8080/?param1=value1&param2=value2&param1=value3`, the output will be:
```
param1: value1
param2: value2
Key: param1, Value: value1
Key: param1, Value: value3
Key: param2, Value: value2
```


---

##  path parameters in Go using the `net/http` package
you can get path parames with ```r.PathValue("param-name") ```

url example ```http://localhost:8080/{user}/{post}/{id}```

```go
package main

import (
	"fmt"
	"net/http"
)

func main() {
	http.HandleFunc("/users/{id}", handler)
	http.ListenAndServe(":8080", nil)
}

func handler(w http.ResponseWriter, r *http.Request) {
	// you can get path parames with r.PathValue("param-name")
	id := r.PathValue("id")
	fmt.Printf("User ID: %s\n", id)
	fmt.Fprintf(w, "User ID: %s\n", id)
}

```