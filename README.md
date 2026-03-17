<p align="center">
  <img src="https://img.shields.io/badge/Orbital-Design_System-b6f09c?style=for-the-badge&labelColor=0d0f10" alt="Orbital Design System" />
</p>

<h1 align="center">Orbital Design System</h1>

<p align="center">
  A token-driven design system with accessible components and flexible theming.<br/>
  Designed for scalable products. Open source.
</p>

<p align="center">
  <img src="https://img.shields.io/badge/tokens-DTCG_format-9ad37f?style=flat-square&labelColor=131619" />
  <img src="https://img.shields.io/badge/theme-dark-686b6e?style=flat-square&labelColor=0d0f10" />
  <img src="https://img.shields.io/badge/font-Plus_Jakarta_Sans-cdcecf?style=flat-square&labelColor=131619" />
  <img src="https://img.shields.io/badge/mono-Geist_Mono-cdcecf?style=flat-square&labelColor=131619" />
  <img src="https://img.shields.io/badge/license-MIT-9ad37f?style=flat-square&labelColor=131619" />
</p>

---

## Token Architecture

Orbital uses a **three-tier token architecture** that separates raw values from meaning from usage:

```
Core (primitives)          Semantic (theme)              Component (usage)
───────────────────        ─────────────────────         ─────────────────────
Color.SpaceGray.800   -->  General.Color.Background.base
Color.StemGreen.600   -->  General.Color.Accent.base     -->  Button.Primary.Default.backgroundColor
Color.Red.500         -->  General.Color.Destructive.base -->  Button.Destructive.Default.backgroundColor
Spacing.x2            -->  General.Spacing.Padding.md    -->  Button.Common.paddingY.medium
BorderRadius.xs       -->  General.BorderRadius.sm        -->  Button.Common.borderRadius
```

| Layer | File | Purpose |
|-------|------|---------|
| **Core** | `tokens/Core.json` | Raw values: colors, spacing, sizing, typography primitives, border radii, opacity |
| **Semantic** | `tokens/Orbital_Dark.json` | Theme mapping: backgrounds, text, borders, accent, status colors, typography scales |
| **Component** | `tokens/Orbital_Dark.json` | Component-specific tokens: buttons, cards, inputs, modals, badges, tags |

## Color Palette

### Brand Colors

| Scale | 50 | 100 | 200 | 300 | 400 | 500 | 600 | 700 | 800 | 900 |
|-------|:--:|:---:|:---:|:---:|:---:|:---:|:---:|:---:|:---:|:---:|
| **SpaceGray** | ![#eeefef](https://img.shields.io/badge/-eeefef?style=flat-square&color=eeefef) | ![#e8e9e9](https://img.shields.io/badge/-e8e9e9?style=flat-square&color=e8e9e9) | ![#cdcecf](https://img.shields.io/badge/-cdcecf?style=flat-square&color=cdcecf) | ![#9b9c9e](https://img.shields.io/badge/-9b9c9e?style=flat-square&color=9b9c9e) | ![#686b6e](https://img.shields.io/badge/-686b6e?style=flat-square&color=686b6e) | ![#363a3d](https://img.shields.io/badge/-363a3d?style=flat-square&color=363a3d) | ![#1a1d21](https://img.shields.io/badge/-1a1d21?style=flat-square&color=1a1d21) | ![#131619](https://img.shields.io/badge/-131619?style=flat-square&color=131619) | ![#0d0f10](https://img.shields.io/badge/-0d0f10?style=flat-square&color=0d0f10) | ![#060708](https://img.shields.io/badge/-060708?style=flat-square&color=060708) |
| **StemGreen** | ![#FCFEFB](https://img.shields.io/badge/-FCFEFB?style=flat-square&color=FCFEFB) | ![#f7fdf4](https://img.shields.io/badge/-f7fdf4?style=flat-square&color=f7fdf4) | ![#edfbe6](https://img.shields.io/badge/-edfbe6?style=flat-square&color=edfbe6) | ![#dbf7cd](https://img.shields.io/badge/-dbf7cd?style=flat-square&color=dbf7cd) | ![#c8f4b4](https://img.shields.io/badge/-c8f4b4?style=flat-square&color=c8f4b4) | ![#b6f09c](https://img.shields.io/badge/-b6f09c?style=flat-square&color=b6f09c) | ![#9ad37f](https://img.shields.io/badge/-9ad37f?style=flat-square&color=9ad37f) | ![#739f5f](https://img.shields.io/badge/-739f5f?style=flat-square&color=739f5f) | ![#4d6a3f](https://img.shields.io/badge/-4d6a3f?style=flat-square&color=4d6a3f) | ![#263520](https://img.shields.io/badge/-263520?style=flat-square&color=263520) |

### Status Colors

| Scale | 50 | 100 | 200 | 300 | 400 | 500 | 600 | 700 | 800 | 900 |
|-------|:--:|:---:|:---:|:---:|:---:|:---:|:---:|:---:|:---:|:---:|
| **Red** | ![#FEF4F3](https://img.shields.io/badge/-FEF4F3?style=flat-square&color=FEF4F3) | ![#fee4e2](https://img.shields.io/badge/-fee4e2?style=flat-square&color=fee4e2) | ![#fecdca](https://img.shields.io/badge/-fecdca?style=flat-square&color=fecdca) | ![#fda29b](https://img.shields.io/badge/-fda29b?style=flat-square&color=fda29b) | ![#f97066](https://img.shields.io/badge/-f97066?style=flat-square&color=f97066) | ![#f04438](https://img.shields.io/badge/-f04438?style=flat-square&color=f04438) | ![#d92d20](https://img.shields.io/badge/-d92d20?style=flat-square&color=d92d20) | ![#b42318](https://img.shields.io/badge/-b42318?style=flat-square&color=b42318) | ![#912018](https://img.shields.io/badge/-912018?style=flat-square&color=912018) | ![#7a271a](https://img.shields.io/badge/-7a271a?style=flat-square&color=7a271a) |
| **Yellow** | ![#FFFDF5](https://img.shields.io/badge/-FFFDF5?style=flat-square&color=FFFDF5) | ![#fffaea](https://img.shields.io/badge/-fffaea?style=flat-square&color=fffaea) | ![#fff3d1](https://img.shields.io/badge/-fff3d1?style=flat-square&color=fff3d1) | ![#ffe8a3](https://img.shields.io/badge/-ffe8a3?style=flat-square&color=ffe8a3) | ![#ffdc75](https://img.shields.io/badge/-ffdc75?style=flat-square&color=ffdc75) | ![#ffd147](https://img.shields.io/badge/-ffd147?style=flat-square&color=ffd147) | ![#e2b42b](https://img.shields.io/badge/-e2b42b?style=flat-square&color=e2b42b) | ![#aa8720](https://img.shields.io/badge/-aa8720?style=flat-square&color=aa8720) | ![#715a15](https://img.shields.io/badge/-715a15?style=flat-square&color=715a15) | ![#392d0b](https://img.shields.io/badge/-392d0b?style=flat-square&color=392d0b) |
| **Green** | ![#F1FEF5](https://img.shields.io/badge/-F1FEF5?style=flat-square&color=F1FEF5) | ![#dcfae6](https://img.shields.io/badge/-dcfae6?style=flat-square&color=dcfae6) | ![#abefc6](https://img.shields.io/badge/-abefc6?style=flat-square&color=abefc6) | ![#75e0a7](https://img.shields.io/badge/-75e0a7?style=flat-square&color=75e0a7) | ![#47cd89](https://img.shields.io/badge/-47cd89?style=flat-square&color=47cd89) | ![#17b26a](https://img.shields.io/badge/-17b26a?style=flat-square&color=17b26a) | ![#079455](https://img.shields.io/badge/-079455?style=flat-square&color=079455) | ![#067647](https://img.shields.io/badge/-067647?style=flat-square&color=067647) | ![#085d3a](https://img.shields.io/badge/-085d3a?style=flat-square&color=085d3a) | ![#074d31](https://img.shields.io/badge/-074d31?style=flat-square&color=074d31) |
| **Blue** | ![#eff8ff](https://img.shields.io/badge/-eff8ff?style=flat-square&color=eff8ff) | ![#d1e9ff](https://img.shields.io/badge/-d1e9ff?style=flat-square&color=d1e9ff) | ![#b2ddff](https://img.shields.io/badge/-b2ddff?style=flat-square&color=b2ddff) | ![#84caff](https://img.shields.io/badge/-84caff?style=flat-square&color=84caff) | ![#53b1fd](https://img.shields.io/badge/-53b1fd?style=flat-square&color=53b1fd) | ![#2e90fa](https://img.shields.io/badge/-2e90fa?style=flat-square&color=2e90fa) | ![#1570ef](https://img.shields.io/badge/-1570ef?style=flat-square&color=1570ef) | ![#175cd3](https://img.shields.io/badge/-175cd3?style=flat-square&color=175cd3) | ![#1849a9](https://img.shields.io/badge/-1849a9?style=flat-square&color=1849a9) | ![#194185](https://img.shields.io/badge/-194185?style=flat-square&color=194185) |
| **Orange** | ![#FFF4ED](https://img.shields.io/badge/-FFF4ED?style=flat-square&color=FFF4ED) | ![#FFE6D5](https://img.shields.io/badge/-FFE6D5?style=flat-square&color=FFE6D5) | ![#FFD6AE](https://img.shields.io/badge/-FFD6AE?style=flat-square&color=FFD6AE) | ![#FF9C66](https://img.shields.io/badge/-FF9C66?style=flat-square&color=FF9C66) | ![#FF692E](https://img.shields.io/badge/-FF692E?style=flat-square&color=FF692E) | ![#FE5514](https://img.shields.io/badge/-FE5514?style=flat-square&color=FE5514) | ![#E84D0F](https://img.shields.io/badge/-E84D0F?style=flat-square&color=E84D0F) | ![#F04A00](https://img.shields.io/badge/-F04A00?style=flat-square&color=F04A00) | ![#BA160C](https://img.shields.io/badge/-BA160C?style=flat-square&color=BA160C) | ![#771A0D](https://img.shields.io/badge/-771A0D?style=flat-square&color=771A0D) |

### Semantic Color Mapping (Dark Theme)

```
Background.base         SpaceGray.800  #0d0f10   ████  Deep dark base
Background.intense      SpaceGray.700  #131619   ████  Elevated surfaces
Background.extraIntense SpaceGray.600  #1a1d21   ████  Cards, popovers
Background.muted        SpaceGray.900  #060708   ████  Recessed areas

Text.extraIntense       SpaceGray.50   #eeefef   ████  Primary headings
Text.intense            SpaceGray.100  #e8e9e9   ████  Emphasis text
Text.base               SpaceGray.200  #cdcecf   ████  Default body text
Text.muted              SpaceGray.300  #9b9c9e   ████  Secondary text
Text.extraMuted         SpaceGray.400  #686b6e   ████  Tertiary / hints

Accent.base             StemGreen.600  #9ad37f   ████  Primary actions
Accent.intense          StemGreen.300  #dbf7cd   ████  Hover / emphasis
Accent.muted            StemGreen.700  #739f5f   ████  Pressed states
```

## Typography

| Style | Font | Weight | Size | Line Height | Tracking |
|-------|------|--------|------|-------------|----------|
| **Display Large** | Plus Jakarta Sans | 700 | 48px | 120% | -0.04em |
| **Display Small** | Plus Jakarta Sans | 700 | 40px | 120% | -0.04em |
| **Heading H1** | Plus Jakarta Sans | 600 | 34px | 120% | -0.02em |
| **Heading H2** | Plus Jakarta Sans | 600 | 28px | 120% | -0.02em |
| **Heading H3** | Plus Jakarta Sans | 600 | 24px | 120% | -0.02em |
| **Heading H4** | Plus Jakarta Sans | 600 | 20px | 120% | 0em |
| **Heading H5** | Plus Jakarta Sans | 600 | 16px | 120% | 0em |
| **Heading H6** | Plus Jakarta Sans | 600 | 14px | 120% | 0.02em |
| **Body Large** | Plus Jakarta Sans | 400 | 20px | 140% | 0em |
| **Body Base** | Plus Jakarta Sans | 400 | 16px | 140% | 0em |
| **Body Small** | Plus Jakarta Sans | 400 | 14px | 140% | 0em |
| **Label Large** | Plus Jakarta Sans | 500 | 16px | 120% | 0em |
| **Label Base** | Plus Jakarta Sans | 500 | 14px | 120% | 0em |
| **Label Small** | Plus Jakarta Sans | 500 | 12px | 120% | 0.02em |
| **Caption** | Plus Jakarta Sans | 400 | 12px | 140% | 0.02em |
| **Overline** | Plus Jakarta Sans | 600 | 11px | 120% | 0.08em |
| **Code Base** | Geist Mono | 400 | 14px | 140% | 0em |
| **Code Small** | Geist Mono | 400 | 12px | 140% | 0em |

## Components

### Button Variants

Orbital ships with **7 button variants**, each with full state coverage:

| Variant | Default | Hover | Focused | Pressed | Active | Disabled | Pending |
|---------|---------|-------|---------|---------|--------|----------|---------|
| **Primary** | Accent bg, dark text | Lighter green | Focus ring | Muted green | Muted + light text | Faded | Intense + spinner |
| **Secondary** | Gray bg, light text | Lighter bg | Focus ring | Darker bg | Accent border | Faded | Lighter + muted |
| **Tertiary** | Base bg | Intense bg | Focus ring | Muted bg | Accent border | Faded | Lighter + muted |
| **Outline** | Transparent, border | Brighter border | Focus ring | Muted border | Accent border | Faded border | Muted border |
| **Ghost** | Transparent | Subtle hover bg | Focus ring | Muted text | Accent text | Faded | Muted text |
| **Link** | Transparent | Icon brightens | Focus ring | Muted text | Accent text | Hidden | Muted text |
| **Destructive** | Red bg, light text | Lighter red | Focus ring | Dark red | - | Faded red | - |

Each variant supports **3 sizes**: `small`, `medium`, `large` with corresponding padding, gap, and typography tokens.

### Other Components

| Component | Token Coverage |
|-----------|---------------|
| **Card** | Padding, gap, border radius, border width, heading/content/footer spacing |
| **Modal** | Background, border, max-width (sm/base/lg), padding, gap, alert variant |
| **Input Field** | Background, border, label, text, placeholder, help text, icon colors per state |
| **Badge** | Border radius |
| **Tag** | Pill border radius |
| **Checkbox** | Border radius |
| **Loading Spinner** | Light/color variants, 3 sizes |
| **Code Block** | Geist Mono font family |

## Spacing Scale

| Token | Value | | Token | Value |
|-------|------:|-|-------|------:|
| `x0` | 0px | | `x6` | 24px |
| `x0_5` | 2px | | `x8` | 32px |
| `x1` | 4px | | `x10` | 40px |
| `x1_5` | 6px | | `x20` | 80px |
| `x2` | 8px | | `x30` | 120px |
| `x2_5` | 10px | | `x40` | 160px |
| `x3` | 12px | | `x50` | 200px |
| `x4` | 16px | | `x60` | 240px |
| `x5` | 20px | | `x80` | 320px |

## Border Radius

| Token | Value | Use Case |
|-------|-------|----------|
| `none` | 0px | Sharp edges |
| `2xs` | 4px | Checkboxes |
| `xs` | 6px | Buttons (sm), badges |
| `sm` | 8px | Buttons (default), inputs |
| `md` | 12px | Cards, base radius |
| `lg` | 24px | Large containers |
| `xl` | 32px | Extra large |
| `pill` | 9999px | Tags, fully rounded |

## Elevation (Dark Theme)

| Level | Surface | Shadow |
|-------|---------|--------|
| **Base** | SpaceGray.800 `#0d0f10` | None |
| **Raised** | SpaceGray.600 `#1a1d21` | Subtle drop shadow |
| **Overlay** | Alpha White 24% | Heavy drop shadow with border ring |
| **Recessed** | SpaceGray.900 `#060708` | None (inset feel) |

## File Structure

```
orbital-design-system/
  tokens/
    Core.json            # Primitive values (colors, spacing, sizing, typography)
    Orbital_Dark.json    # Dark theme (semantic + component tokens)
```

## Token Format

Tokens follow the [Design Tokens Community Group (DTCG)](https://tr.designtokens.org/format/) specification:

```json
{
  "Color.StemGreen.500": {
    "$type": "color",
    "$value": "#b6f09c"
  }
}
```

Aliases use curly-brace references:

```json
{
  "General.Color.Accent.base": {
    "$type": "color",
    "$value": "{Color.StemGreen.600}"
  }
}
```

## Tooling Compatibility

These tokens are compatible with:
- [Tokens Studio](https://tokens.studio/) (Figma plugin)
- [Style Dictionary](https://amzn.github.io/style-dictionary/)
- [Token Transformer](https://github.com/tokens-studio/figma-plugin/tree/main/token-transformer)
- Any DTCG-compatible token pipeline

## License

MIT License - see [LICENSE](LICENSE) for details.

---

<p align="center">
  <sub>Built with precision. Themed for the cosmos.</sub>
</p>
