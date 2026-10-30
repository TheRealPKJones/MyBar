# MyBar 2.3 development checklist

Status: development branch only; not published to the live website.

## Release scope
- [ ] Audit built-in and imported recipes; detect duplicates by normalized drink name and variation.
- [ ] Verify 150–200 classic and modern cocktail entries against reputable references, with source links and original directions. Do not copy website prose or unlicensed photos.
- [ ] Add missing classics (including Long Island Iced Tea); review existing Negroni, Old Fashioned, Manhattan and Whiskey Sour before adding duplicates.
- [ ] Support multiple labeled, sourced variations per drink; Bartender Mode follows selected variation.
- [ ] Premium cigar-lounge visual system: warm charcoal, espresso, muted gold, restrained typography, consistent cocktail imagery.
- [ ] Simplify home with featured cocktail and swipeable/arrow-navigable catalog; keyboard and touch support.
- [ ] Accessible three-line navigation with clear back/close behavior and visible current section.
- [ ] Browse by Spirit; My Mood; My Bar/ingredient builder; What I Can Make; search by cocktail name including variations. No Cocktail Families menu.
- [ ] Combine browse filters and add Surprise Me / Surprise Me Again.
- [ ] Random Cocktail of the Week changes every Friday, avoids recent repeats, uses local-time-independent deterministic week selection where possible.
- [ ] Suggest a Cocktail without requiring accounts, with abuse prevention and human verification before publication.
- [ ] Improve shopping list, ingredient management, responsive layouts, and consistent version labels.
- [ ] Keep accounts, cloud sync, paid tiers and public launch out of 2.3.

## Quality gates
- [ ] Confirm existing recipe storage schema and persistence; migrate without data loss.
- [ ] Validate quantities, units, ingredient matching, variations, and missing-ingredient calculations.
- [ ] Test navigation, filters, randomization, weekly rotation, search, bartender steps and suggestions.
- [ ] Test on desktop/mobile, keyboard and touch, including empty states.
- [ ] Review external recipe/data/photo licenses and attribution.
- [ ] Set up an isolated preview URL or local preview and verify it is not the production deployment.
- [ ] Obtain owner approval before merging to main or deploying to production.

## Initial audit findings
Built-in index.html contains Negroni, Old Fashioned, Manhattan and Whiskey Sour. No Long Island Iced Tea string was found in that file. The imported catalog still needs schema and contents validation; an earlier fetch did not yield a usable recipe list.
