These links contain examples and sources on creating flatpaks from manifests.

https://docs.flatpak.org/en/latest/conventions.html?highlight=launcher#application-icons

https://github.com/flathub

https://docs.flatpak.org/en/latest/first-build.html

If you run `flatpak-build --install --user <build-directory> net.veloren.airshipper` it will build and install the airshipper flatpak project onto your machine with the correct minimal permissions, but I couldn't get an application launcher or desktop icon to work. Do whatever you want with it, but as it is I can run Veloren on the latest GitLab version inside the lightweight sandboxing of Flatpak.

Flatpak needs to offer better sandboxing for exposed sockets like network and X11, and docker should have a finer-grained system available to prevent sandbox escapes.
