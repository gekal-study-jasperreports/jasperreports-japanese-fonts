# JasperReports Japanese Fonts

Japanese fonts extension for JasperReports. This project provides a simple way to include Japanese fonts (specifically IPAex fonts) in your JasperReports projects.

## Included Fonts

- **IPAexGothic**: A Japanese Gothic font.
- **IPAexMincho**: A Japanese Mincho font.
- **Comic Sans MS**: (Included for legacy support/examples)

## Usage

Add this library to your project's dependencies.

### Gradle

```gradle
repositories {
    mavenCentral()
}

dependencies {
    implementation 'cn.gekal:jasperreports-japanese-fonts:0.0.2'
}
```

### Maven

```xml
<dependency>
    <groupId>cn.gekal</groupId>
    <artifactId>jasperreports-japanese-fonts</artifactId>
    <version>0.0.2</version>
</dependency>
```

In your JasperReports JRXML file, you can then use these fonts by setting the `fontName` attribute:

```xml
<textElement>
    <font fontName="IPAexGothic"/>
</textElement>
```

## How to Release

This project uses GitHub Actions and JReleaser for automated releases to Maven Central.

1.  Update the version in `gradle.properties` (Optional, the workflow will do it automatically based on the tag).
2.  Create and push a new tag starting with `v` (e.g., `v1.0.0`).

    ```bash
    git tag v1.0.0
    git push origin v1.0.0
    ```

3.  The GitHub Actions workflow will:
    -   Extract the version from the tag.
    -   Update `gradle.properties` and push the change to the `main` branch.
    -   Build and publish the artifacts to Maven Central.
    -   Create a GitHub Release.

## License

This project is licensed under the [Apache License, Version 2.0](http://www.apache.org/licenses/LICENSE-2.0.txt).
The IPAex fonts are subject to the [IPA Font License Agreement v1.0](https://fonts.jp/ipaex_licenses/).
