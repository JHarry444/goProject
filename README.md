# goProject

Main.go:
package main -> denotes package is going to be run.
import ("net/http") -> imports the net and http libraries.
func main() { -> function is called when application starts.
http.Handle("/", http.FileServer(http.Dir("./static/"))) -> sets the contents of /static to the http handler.
if err := http.ListenAndServe(":8080", nil); err != nil {panic(err)} -> listens on port 8080 and serves contents of handler when it is visited.
