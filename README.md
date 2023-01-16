# Ephemerals

This is a basic program for "ephemeral" URL research. It is still in early development so you probably **shouldn't** run it. It basically runs through a list of websites and stores their requests.

## Dependencies

- [Go](https://go.dev/doc/install)
- [Playwright](https://playwright.dev/docs/intro) version of Chromium.
- [MongoDB](https://www.mongodb.com/try/download/community)

## Configuration

Configuration is done using the `const` fields in [`main.go`](main.go)
- **NOTES**:
  - You must update the `BROWSER_PATH` variable as it is specific to me (but your path should look similar), use `go run github.com/playwright-community/playwright-go/cmd/playwright install` to install Playwright.
  - Additionally, the `SITES_FILE` must be in the following format:
    - ```json
      {"category": ["google.com", "duckduckgo.com"] }
      ```
    - Websites **must not** include `http[s]://` or the program will fail.

## Running

To run the script:

```sh
go run main.go
```

## TODO

- Don't revisit duplicate sites in differnet categories
- ~~Add TTL data gathering~~
- ~~Make data collection more efficient/parallel (streams vs chunks?)~~
