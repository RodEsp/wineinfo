# `wineinfo`

A sample web application for Junction demos.

The app is a wine catalog that's built with a nextjs frontend and multiple
FastAPI services to handle traditional full-text search, LLM-based
vector search, and saving bottles to a collection. To make it easy to run
without being a Kubernetes whiz, it runs in a self-contained [`k3d`][k3d]
cluster.

## Installing

To run the wineinfo service, you'll need `docker` and `kubectl` installed. This
README won't cover installing them. Once you've gotten both `docker` and
`kubectl` set up, install `k3d` by running:

```bash
curl -s https://raw.githubusercontent.com/k3d-io/k3d/main/install.sh | bash
```

or check out the [official k3d installation instructions][k3d-install]

[k3d]: https://k3d.io/
[k3d-install]: https://k3d.io/v5.7.4/#install-script

Once you've installed `k3d` (check that it works by running `k3d version`) you
can start the demo:

```bash
./deploy/wineinfo.sh
```

## Begin the demo

Once you're done, point your browser at <http://localhost:8010>, and you should
see the working Wineinfo site. Once you click around the site,
head to [the first part of the demo](demo/01_intro.md).

## Uninstalling

If you're fully done, you can fully delete your k3d cluster with:

```bash
k3d cluster delete junction-wineinfo
```

![A screenshot of the demo UI](./demo/images/homepage.jpg)
