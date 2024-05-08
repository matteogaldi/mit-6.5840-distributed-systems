# Lecture 2
- `sync.WaitGroup` is used to define a waitGroup trivially. It's a counter, before launching a go routine we can add 1 to the counter, when the goroutine ends it decrements the value. When the value is 0 the caller continues

- In case of function failure is better to add `defer` before `Done()` so that even if the goroutine dies, it call the Done method

- `go run -race program` checks for race conditions **in that run** (no static analysis)
