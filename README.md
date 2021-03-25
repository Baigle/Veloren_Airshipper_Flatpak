These links contain examples and sources on creating flatpaks from manifests.

https://docs.flatpak.org/en/latest/conventions.html?highlight=launcher#application-icons

https://github.com/flathub

https://docs.flatpak.org/en/latest/first-build.html

These repo files go in /home/<user>/.var/app/net.veloren.airshipper/.

From there, if you run `flatpak-build --install --user <build-directory> net.veloren.airshipper` it will build and install the airshipper flatpak project onto your machine with the correct minimal permissions, but I couldn't get an application launcher or desktop icon to work. Do whatever you want with it, but as it is I can run Veloren on the latest GitLab version inside the lightweight sandboxing of Flatpak.

To run this after flatpak-build'ing, you might be able to run `flatpak run net.veloren.airshipper` from an unprivileged commandline, or simply use the command `airshipper` if the installation registered the command. Whichever way you do it, it will launch the graphical airshipper interface from the terminal, and from there Veloren runs normally. Permissions can be adjusted with Flatseal for all your installed flatpak apps.

Notes on security: Flatpak needs to offer better sandboxing for exposed sockets like network and X11, and docker should have a finer-grained system available to prevent sandbox escapes. This may be partly due to the limited provided mechanisms through the linux kernel.
