# server-columns

lightweight discord css addon that displays server icons in multiple columns instead of a single vertical list.

designed for custom discord clients that support css themes, such as vencord and betterdiscord.

## features

- multiple server icon columns
- adjustable server icon size
- adjustable spacing between servers
- optional dm alignment
- badge scaling
- folder support
- serverfolders compatibility
- works on macos, windows, and linux

## installation

download:

`servercolumns.css`

then either add it directly to your theme setup or import it into another css theme.

example:

```css
@import url('your-raw-github-link/servercolumns.css');
```

## customization

the main settings are at the top of `servercolumns.css`:

```css
:root {
    --columns: 3;
    --guildsize: 50;
    --guildgap: 3;
    --badgescale: 1;
    --aligndms: 1;
}
```

### columns

controls how many server columns are displayed.

```css
--columns: 3;
```

example:

```css
--columns: 4;
```

### server icon size

controls the size of server icons.

```css
--guildsize: 50;
```

the default is:

```css
--guildsize: 50;
```

### server spacing

controls the spacing between server icons.

```css
--guildgap: 3;
```

increase the number for more space between servers.

### badge scale

controls the size of notification and mention badges.

```css
--badgescale: 1;
```

for example:

```css
--badgescale: 0.8;
```

will make badges slightly smaller.

### dm alignment

controls the alignment of direct message icons.

```css
--aligndms: 1;
```

use:

```css
--aligndms: 1;
```

for aligned dms.

use:

```css
--aligndms: 0;
```

for centered dms.

## using server columns in another theme

you can import this addon into another discord theme and override the settings there.

example:

```css
@import url('your-raw-github-link/servercolumns.css');

:root {
    --columns: 3;
    --guildsize: 50;
    --guildgap: 3;
    --badgescale: 1;
    --aligndms: 0;
}
```

this lets you keep `servercolumns.css` separate while changing its settings from your main theme.

## compatibility

server columns is intended for discord's current visual refresh interface.

includes support for:

- normal server icons
- direct messages
- server folders
- notification badges
- server search
- macos title bar positioning
- serverfolders layouts

macos-specific rules are included where necessary, but the addon is not macos-only. those rules are simply ignored on windows and linux.

## notes

discord frequently changes internal class names.

because of this, some discord updates may temporarily break parts of the layout until the css is updated.

## credits

based on the original ServerColumns theme by [mwittrien](https://github.com/mwittrien).

maintained and adapted by finney.
