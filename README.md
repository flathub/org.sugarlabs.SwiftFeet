# Swift Feet Flatpak

A high energy and up-beat action program, Swift Feet encourages children to be active. 20 different exercises and 10 different dances set to music take users through high, moderate and low impact movements. This activity was designed for OLPC Canada in collaboration with ParticipACTION Canada and Ophea.

To know more refer: https://github.com/sugarlabs/swiftfeet-activity

## How To Build

```
git clone https://github.com/flathub/org.sugarlabs.SwiftFeet.git
cd org.sugarlabs.SwiftFeet
flatpak -y --user install flathub org.gnome.{Platform,Sdk}//46
flatpak -y --user install org.sugarlabs.BaseApp//24.04
flatpak-builder --user --force-clean --install build org.sugarlabs.SwiftFeet.json
```

## Check For Updates

Install the flatpak external data checker
```
flatpak --user install org.flathub.flatpak-external-data-checker
```

Now to update every single module to the latest stable version use
```
cd org.sugarlabs.SwiftFeet
flatpak run --filesystem=$PWD org.flathub.flatpak-external-data-checker org.sugarlabs.SwiftFeet.json
```