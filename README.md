# Colory for PHP.

> Simple colors helper for PHP.

Generating random RGB & HEX colors with alpha capability,
Inverting RGB and HEX colors, converting between RGB and HEX colors &
perhaps more features in the future.

## 🫡 Usage

### 🚀 Installation

You can install the package via composer:

```bash
composer require nabeghe/colory
```

#### Example:

```php
use Nabeghe\Colory\Colory;

echo "[[ Random RBG ]]\n";
echo "> Random RBG => ".json_encode(Colory::randomRgb())."\n";
echo "> Random RGBA => ".json_encode(Colory::randomRgb(true))."\n";
echo '> Random RGB for CSS => '.json_encode(Colory::randomRgbCss())."\n";
echo '> Random RGBA for CSS => '.json_encode(Colory::randomRgbCss(true))."\n";
echo "\n";

echo "[[ Random Hex ]]\n";
echo '> Random Hex => '.json_encode(Colory::randomHex())."\n";
echo '> Random Hex With Alpha => '.json_encode(Colory::randomHex(true))."\n";
echo "\n";

echo "[[ Invert RGB ]]\n";
$random_rgb = Colory::randomRgb();
echo "> Invert RGB ($random_rgb[r], $random_rgb[g], $random_rgb[b]) => ".json_encode(Colory::invertRgb($random_rgb))."\n";
$random_rgba = Colory::randomRgb(true);
echo "> Invert RGBA ($random_rgba[r], $random_rgba[g], $random_rgba[b], $random_rgba[a]) => ".json_encode(Colory::invertRgb($random_rgba))."\n";
echo "> Invert RGBA (nabeghe/colory) => ".json_encode(Colory::invertRgb('nabeghe/colory'))."\n";
echo "\n";

echo "[[ Invert HEX ]]\n";
$random_hex = Colory::randomHex();
echo "> Invert HEX ($random_hex) => ".json_encode(Colory::invertHex($random_hex))."\n";
$random_hexa = Colory::randomHex(true);
echo "> Invert HEX ($random_hexa) => ".json_encode(Colory::invertHex($random_hexa))."\n";
echo '> Invert HEX (#EEE) => '.json_encode(Colory::invertHex('#EEE'))."\n";
echo '> Invert HEX (#eee) => '.json_encode(Colory::invertHex('#eee'))."\n";
echo '> Invert HEX (#FFF) => '.json_encode(Colory::invertHex('#FFF'))."\n";
echo '> Invert HEX (#fff) => '.json_encode(Colory::invertHex('#fff'))."\n";
echo '> Invert HEX (#ff573380) => '.json_encode(Colory::invertHex('#ff573380'))."\n";
echo '> Invert HEX (nabeghe/colory) => '.json_encode(Colory::invertHex('nabeghe/colory'))."\n"; // null
echo "\n";

echo "[[ RGB To HEX ]]\n";
$random_rgb = Colory::randomRgb();
echo "> RGB To HEX ($random_rgb[r], $random_rgb[g], $random_rgb[b]) => ".Colory::rgbToHex($random_rgb)."\n";
$random_rgba = Colory::randomRgb(true);
echo "> RGB To HEX ($random_rgba[r], $random_rgba[g], $random_rgba[b], $random_rgba[a]) => ".json_encode(Colory::rgbToHex($random_rgba))."\n";
echo "> RGB To HEX (nabeghe/colory) => ".json_encode(Colory::rgbToHex('nabeghe/colory'))."\n";
echo "\n";

echo "[[ HEX To RGB ]]\n";
$random_hex = Colory::randomHex();
echo "> HEX To RGB ($random_hex) => ".json_encode(Colory::hexToRgb($random_hex))."\n";
$random_hexa = Colory::randomHex(true);
echo "> HEX To RGB ($random_hexa) => ".json_encode(Colory::hexToRgb($random_hexa))."\n";
echo "> HEX To RGB (nabeghe/colory) => ".json_encode(Colory::hexToRgb('nabeghe/colory'))."\n";
echo "\n";
```

## 📖 License

Licensed under the MIT license, see [LICENSE.md](LICENSE.md) for details.