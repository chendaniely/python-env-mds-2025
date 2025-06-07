## Conda Lock File Generation

I used [conda-lock](https://github.com/conda/conda-lock) to make sure everyone can get the exact same environment.

### Platform Issue

When I first ran `conda-lock`, it tried to make lock files for all platforms. But some packages we use (like `libcxx=17.0.6`) aren’t available on Windows, so it threw an error (see screenshot).
![](libcxx_image.png)

To still generate a lock file here, I need to tell `conda-lock` to only make lock files for Mac (Intel and Apple Silicon) and Linux:

```sh
conda-lock lock --platform osx-64 --platform osx-arm64 --platform linux-64
```

This way, it skips Windows and works fine for us.