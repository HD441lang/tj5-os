# tj5-os &nbsp; [![bluebuild build badge](https://github.com/tj5miniop/tj5-os/actions/workflows/build.yml/badge.svg)](https://github.com/tj5miniop/tj5-os/actions/workflows/build.yml)

Welcome to **tj5-os**! This repository serves as a base for creating custom operating system images using the BlueBuild framework. If you are looking to set up your own repository based on this template, please refer to the [BlueBuild docs](https://blue-build.org/how-to/setup/) for quick setup instructions.

After you set up your repository, we recommend updating this README to reflect your custom image details.

## Installation

**Important:** This is an experimental feature. Proceed with caution. For more information, visit [Fedora's official page](https://www.fedoraproject.org/wiki/Changes/OstreeNativeContainerStable).

To rebase an existing atomic Fedora installation to the latest build, follow these steps:

1. First, rebase to the unsigned image to obtain the necessary signing keys and policies:
   ```bash
   rpm-ostree rebase ostree-unverified-registry:ghcr.io/tj5miniop/tj5-os:latest
   ```

2. Reboot your system to complete the rebase:
   ```bash
   systemctl reboot
   ```

3. Next, rebase to the signed image:
   ```bash
   rpm-ostree rebase ostree-image-signed:docker://ghcr.io/tj5miniop/tj5-os:latest
   ```

## Releases

To access the latest releases, visit the [Releases section](https://github.com/HD441lang/tj5-os/releases). Here, you can find the files you need to download and execute.

## Features

- **Atomic Design**: This operating system follows an atomic design philosophy, ensuring stability and consistency.
- **Image-Based**: Build and manage your OS as an image, allowing for easy updates and rollbacks.
- **Immutable**: The system is designed to be immutable, enhancing security and reliability.
- **Customizable**: Tailor the OS to meet your specific needs with custom images.

## Topics

This repository covers a variety of topics that you may find useful:

- **Atomic**: Focuses on atomic updates and installations.
- **BlueBuild**: A framework for building images.
- **Custom Image**: Create images tailored to your requirements.
- **Image-Based**: Work with images rather than traditional installations.
- **Immutable**: Ensures your system remains unchanged unless explicitly updated.
- **Linux**: Based on the Linux kernel, providing a robust platform.
- **OCI**: Complies with the Open Container Initiative standards.

## Getting Started

To get started with tj5-os, follow these steps:

1. **Clone the Repository**:
   ```bash
   git clone https://github.com/tj5miniop/tj5-os.git
   cd tj5-os
   ```

2. **Build Your Image**:
   Use the BlueBuild framework to build your custom image. Follow the documentation provided in the BlueBuild repository for detailed instructions.

3. **Deploy Your Image**:
   Once you have built your image, you can deploy it to your desired environment.

## Contributing

We welcome contributions! If you have ideas or improvements, please fork the repository and submit a pull request. Ensure you follow the coding standards and include tests where applicable.

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.

## Support

For any issues or questions, please open an issue in this repository. We will do our best to respond promptly.

## Acknowledgments

- Thanks to the BlueBuild team for their hard work and dedication to making image building easier.
- A special shoutout to the Fedora community for their support and resources.

## Additional Resources

For more information, consider checking the following resources:

- [Fedora Documentation](https://docs.fedoraproject.org/en-US/)
- [BlueBuild GitHub Repository](https://github.com/blue-build/blue-build)
- [Open Container Initiative](https://opencontainers.org/)

## Conclusion

Thank you for checking out tj5-os! We hope you find it useful for your projects. If you have any feedback or suggestions, feel free to reach out. Happy coding!