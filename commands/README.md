# Commands

## build_runner


```
dart run build_runner watch --delete-conflicting-outputs

dart run build_runner build --delete-conflicting-outputs
```

## freezed

```
flutter pub add freezed_annotation
flutter pub add dev:build_runner
flutter pub add dev:freezed
# if using freezed to generate fromJson/toJson, also add:
flutter pub add json_annotation
flutter pub add dev:json_serializable
```

## easy_localization

Code generation supports only json files, for more information run in terminal flutter pub run easy_localization:generate -h

### Command line arguments 

| Arguments                     | Short | Default               | Description                                                                 |
|-------------------------------|-------|-----------------------|-----------------------------------------------------------------------------|
| --help                        | -h    |                       | Help info                                                                   |
| --source-dir                  | -S    | resources/langs       | Folder containing localization files                                        |
| --source-file                 | -s    | First file            | File to use for localization                                                |
| --output-dir                  | -O    | lib/generated         | Output folder for the generated file                                        |
| --output-file                 | -o    | codegen_loader.g.dart | Output file name                                                            |
| --format                      | -f    | json                  | Support json or keys formats                                                |
| --[no-]skip-unnecessary-keys  | -u    | false                 | Ignores keys defining nested object except for plural(), gender() keywords. |

```
dart run easy_localization:generate -S 'assets/translations' -O 'lib/presentation/core/translations'

dart run easy_localization:generate -f keys  -o locale_keys.g.dart -S 'assets/translations' -O 'lib/presentation/core/translations'
```