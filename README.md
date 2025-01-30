# Go Map Nil Check Panic

This repository demonstrates a common error in Go: panics caused by accessing nil maps.  Go's maps do not have default behavior like some other languages (e.g., Python's dictionaries, which return `None` if a key doesn't exist).  Attempting to access a non-existent key in a `nil` map will result in a runtime panic.

The `bug.go` file shows this error in action. The `bugSolution.go` file demonstrates the correct way to handle this situation using a nil check.

## How to reproduce

1. Clone the repository
2. Run `go run bug.go` to see the panic
3. Run `go run bugSolution.go` to see the corrected behavior

## Solution
Always check for a `nil` map before accessing its elements.   This can be done using an `if` statement or a shorthand conditional.
