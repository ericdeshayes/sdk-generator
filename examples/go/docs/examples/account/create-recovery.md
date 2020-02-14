package main

import (
    "fmt"
    "github.com/appwrite/go-sdk"
)

func main() {
    var client := appwrite.Client{}

    var service := appwrite.Account{
        client: &client
    }

    var response, error := service.CreateRecovery("email@example.com", "https://example.com")

    if error != nil {
        panic(error)
    }

    fmt.Println(response)
}