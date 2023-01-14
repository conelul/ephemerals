# Ephemerals

This is a basic program for "ephemeral" URL research. It is still in early development so you probably **shouldn't** run it. It basically runs through a list of websites and stores their requests.

## Dependencies

- [Go](https://go.dev/doc/install)
- [Playwright](https://playwright.dev/docs/intro) version of Chromium.
- [MongoDB](https://www.mongodb.com/try/download/community)

## Configuration

Configuration is done using the `const` fields in [`main.go`](main.go)

## Running

To run the script:

```sh
go run main.go
```

## TODO

- Add TTL data gathering
