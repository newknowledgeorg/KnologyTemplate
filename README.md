# Knology R Markdown Template

This package provides R Markdown templates for researchers at Knology.

## Features

- **Knology Color Palette**: Pre-defined color variables for all Knology brand colors
- **Custom Fonts**: Ubuntu for headers, Open Sans for body text
- **ggplot2 Theme**: Custom `graphStyle` theme for consistent visualizations
- **HTML & Word Output**: Professional styling for both formats
- **Auto-formatted**: Tables, figures, and code blocks styled consistently

## Installation

Install from GitHub:

```r
devtools::install_github("knology/KnologyTemplate")
```

Or install from a local copy:

```r
devtools::install_local("~/path/to/KnologyTemplate/")
```

## Usage

After installing the package, create a new R Markdown document in RStudio:

1. **File → New File → R Markdown...**
2. Click **"From Template"**
3. Select **"Knology Report"**
4. Click **OK**

## Knology Color Palette

The template includes all Knology brand colors:

| Variable | Color Name | Hex Code |
|----------|-----------|----------|
| `kBlue` | Trusted Blue | #266093 |
| `kSky` | Horizon Blue | #7D9BC0 |
| `kYellow` | Optimistic Citrine | #D8C827 |
| `kOrange` | Radiant Coral | #F36C3E |
| `kGreen` | New Leaf | #6CA443 |
| `kAqua` | Ocean | #00A2AE |
| `kPurple` | Passion | #943A80 |
| `kText` | Dark Blue Text | #002F6C |
| `kBlack` | Black | #101820 |

## Example Usage

```r
library(ggplot2)

# Create a plot with Knology styling
ggplot(mtcars, aes(x = wt, y = mpg)) +
  geom_point(color = kBlue, size = 3) +
  geom_smooth(method = "lm", color = kOrange) +
  labs(
    title = "Car Weight vs MPG",
    x = "Weight (1000 lbs)",
    y = "Miles per Gallon"
  ) +
  graphStyle
```

## Package Structure

```
KnologyTemplate/
├── DESCRIPTION
├── LICENSE
├── README.md
├── NAMESPACE
└── inst/
    └── rmarkdown/
        └── templates/
            └── knology_report/
                ├── template.yaml
                └── skeleton/
                    ├── skeleton.Rmd
                    └── styles.css
```

## Building from Source

If you're modifying the package:

```r
# Document the package
devtools::document()

# Build the package
devtools::build()

# Install locally
devtools::install()

# Or do all at once
devtools::install()
```

## Contributing

We welcome comments and suggestions from other researchers. Please open an issue or submit a pull request.

## License

MIT License - see LICENSE file for details.