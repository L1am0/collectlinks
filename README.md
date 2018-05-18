Package collectlinks is useful for only one task:

Given a response from `http.Get` it will use parse the page and
return to you a slice of all the href links and img src found.

Usage:

    package main
    import (
      "https://github.com/L1am0/collectlinks"
      "net/http"
      "fmt"
    )

    func main() {
      resp, _ := http.Get("http://motherfuckingwebsite.com")
      links := collectlinks.All(resp.Body)
      fmt.Println(links)
    }


Running that will output:

   [http://twitter.com/thebarrytone http://txti.es]
