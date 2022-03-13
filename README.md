# Switch Games JSON

:warning: **NOTICE:** This repository has been archived an read-only because now there's a better method to get the Switch game screenshots with folder names. [Please refer to the Nintendo documentation](https://en-americas-support.nintendo.com/app/answers/detail/a_id/53664/~/how-to-transfer-screenshots-and-video-captures-to-a-computer-via-a-usb-cable) to learn more. The site for this repository will remain online but it wont be updated anymore.

---

This repository contains the code to parse and build a Nintendo Switch game list in JSON using the [Game List from switchbrew](https://switchbrew.org/w/index.php?title=Title_list/Games") and the Community Provided list from [RenanGreca/Switch-Screenshots repository](https://github.com/RenanGreca/Switch-Screenshots).

There are two resulting JSON files:
- `switch_games.json`: Will have all information from SwitchBrew with the merged information from RenanGreca's file.
- `switch_id_names.json`: Will only have a map of `encrypted game id: game name`.

## Where to obtain the list?

List is published in the github pages for this repository and access it can be downloaded at [https://fmartingr.github.io/switch-games-json/](https://fmartingr.github.io/switch-games-json/), just point to the file that more suites your use case.

List is updated weekly via Github actions.

## Schema

``` json
# switch_games.json
{
    "title_id": "0100000000010000",
    "type": "Application / Game",
    "description": "Super Mario Odyssey\u2122",
    "min_os": "3.0.1",
    "regions": [
        "CHN",
        "EUR",
        "JPN",
        "KOR",
        "USA"
    ],
    "distribution": [
        "Digital",
        "Cartridge"
    ],
    "versions": [
        "0",
        "0x10000",
        "0x20000",
        "0x30000",
        "0x40000"
    ],
    "cartdridge_description": "",
    "encrypted_game_id": "8AEDFF741E2D23FBED39474178692DAF"
}
```

``` json
# switch_id_names.json
{
    "title_normalized": "Super Mario Odyssey",
    "encrypted_game_id": "8AEDFF741E2D23FBED39474178692DAF"
}
```

## Acknoledgements

- [s1cp/nxshot](https://github.com/s1cp/nxshot): Original work on calculating the switch encrypted title IDs.
- [RenanGreca](https://githuub.com/RenanGreca/Switch-Screenshots): Community provided game IDs.
