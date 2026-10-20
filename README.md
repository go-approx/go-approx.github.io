# go-approx.github.io

The go-approx landing page (Hugo), served at <https://go-approx.github.io/>.

The layout is the go-* family template, imported as the Hugo module
`github.com/go-fleettools/landingkit` (pinned in `go.mod`; `kit.go` keeps
`go mod tidy` from dropping the requirement). `layouts/index.html` is this
organisation's own, and `[params.brand]` in `hugo.toml` is generated from the
logo's gradient with `landingkit brand static/img/logo.svg`.

The libraries on the page (`[[params.repos]]`) say "released vX.Y.Z" only when
the repository has a tag. The documentation is at
<https://go-approx.github.io/docs/>; the logo kit is in
[go-approx/brand](https://github.com/go-approx/brand).

```sh
hugo server
```

| Workflow | What |
| --- | --- |
| `hugo.yml` | builds on pull requests; builds and deploys to Pages on `main` |
| `ci.yml` | the site builds and names every repository |
| `links.yml` | every link and image of the built site resolves |

BSD-3-Clause.
