# IntelliJ IDEA (Linux, tar.gz)


## Files

intelliJ-setup/
├── idea-2025.3.1.tar.gz (Download the latest version from jetbrains.com)
└── README.md

## Steps

    tar -xzf idea-2025.3.1.tar.gz
    sudo mv idea-IU-253.29346.138 /opt/
    /opt/idea-IU-253.29346.138/bin/idea.sh

    sudo nano /usr/share/applications/intellij-idea.desktop

    [Desktop Entry]
    Version=1.0
    Type=Application
    Name=IntelliJ IDEA
    Exec=/opt/idea-IU-253.29346.138/bin/idea
    Icon=/opt/idea-IU-253.29346.138/bin/idea.svg
    Terminal=false
    Categories=Development;IDE;
    StartupWMClass=jetbrains-idea

    sudo update-desktop-database
