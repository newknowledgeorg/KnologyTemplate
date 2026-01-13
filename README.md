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
devtools::install_github("newknowledgeorg/KnologyTemplate", force = TRUE)
```

## Usage

After installing the package, create a new R Markdown document in RStudio:

1. **File → New File → R Markdown...**
2. Click **"From Template"**
3. Select **"Knology Report"**
4. Click **OK**

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

