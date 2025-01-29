# Dockerfile Best Practices: Base Image Selection

This example demonstrates a common error in Dockerfiles: using a large, unpinned base image. This leads to bloated image sizes and reproducibility problems.

**Problem:** The original `Dockerfile` uses `ubuntu:latest`. This image is large and its contents are not guaranteed to remain consistent across builds, leading to non-deterministic behaviour.

**Solution:** The improved `Dockerfile_solution` specifies a slimmer base image (`ubuntu:22.04`) and uses a specific version. This creates a much smaller, more reproducible image.

**Key improvements:**

*   **Smaller base image:** Using a slimmer image drastically reduces the image size.
*   **Version pinning:** Specifying the exact version of the base image guarantees reproducibility across builds.

By following these best practices, you can create efficient and reliable Docker images.