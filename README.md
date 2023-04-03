[Project homepage](https://commits.top/)

# Most Active GitHub Users Counter

This CLI tool queries the GitHub GraphQL API for users and ranks them according to number of contributions. Several preset locations are provided (refer to `presets.go`).

**Requirements:**
- [Golang](https://golang.org/)

**Example usage (dev environment):**

```
go run *.go \
   --token y0urt0k3n \
   --preset worldwide \
   --amount 500 \
   --consider 1000 \
   --output csv \
   --file ./output.csv
```
| Flag | Description | Default |
| --- | --- | --- |
| `token` | In order to make requests against the GitHub API one needs an access token, which can be created [here](https://github.com/settings/tokens). The token needs `read:org` and `read:user` permissions. | _empty string_ |
| `preset` | The preset location to be included in query. Refer to `presets.go` | _empty string_ |
| `amount` | The amount of users to be shown. This flag wil only take effect in `yaml` format to choose top `amount` account from top `consider` account by several categories. | `256` |
| `consider` | The amount of users to consider from the query. | `1000` |
| `output` | The output format. Choices between `plain`, `csv`, & `yaml` | `plain` |
| `file` | The output file. | **stdout** |

**Acknowledgement:**
- [Origin Project homepage](https://commits.top/)
- [Origin Project github](https://github.com/lauripiispanen/most-active-github-users-counter)
- [Origin Project Creator](https://github.com/lauripiispanen)
