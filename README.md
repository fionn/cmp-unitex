# cmp-UniTeX

## Overview

[nvim-cmp](https://github.com/hrsh7th/nvim-cmp) completion source to insert Unicode symbols by their $\mathrm{\TeX}$ command.

Unicode ↔ $\mathrm{\TeX}$ correspondence is from [_Unicode symbols and corresponding LaTeX math mode commands_](https://milde.users.sourceforge.net/LUCR/Math/), [parsed](https://gist.github.com/fionn/7a8675aa8a6d69142cc50124acfac0a1) and then heavily reduced by hand.

This is similar to [kdheepak/cmp-latex-symbols](https://github.com/kdheepak/cmp-latex-symbols), but I found it to be too slow due to the large number of symbols provided.

## Usage

The ``\`` character triggers completion, which is available for all file types except $\mathrm{\TeX}$ (where we don't want to insert Unicode and want the literal command instead).

## Configuration

Add `unitex` as a completion source.

```lua
cmp.setup {
    sources = cmp.config.sources {
        {name = "unitex"}
    }
}
```
