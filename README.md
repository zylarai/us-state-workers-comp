# US state workers' compensation requirements for small businesses (50 states and DC, 2026)

When does a small business have to carry workers' compensation insurance? This dataset covers every US state and the District of Columbia. For each one it records:

- the employee count that triggers coverage, as the state words it;
- any separate rule for construction and for farm work;
- whether corporate officers and LLC members count;
- whether a sole proprietor with no employees needs coverage;
- the owner exemption or election form;
- how insurance is bought (private insurers, a state fund, or a monopolistic state fund);
- whether a private employer may opt out;
- the penalty for going without coverage;
- links to the state's coverage lookup and employer guide;
- the first-hire registration pages for unemployment insurance, income tax withholding and new hire reporting.

Every value comes from an official state page: the workers' compensation agency, labor department, statute or administrative code. The pages were opened on November 24 and 25, 2026, and each row lists its sources. Where a value was not stated on an official page we could open, the cell is empty and the reason is in `to_confirm`. Nothing is guessed or inferred.

> **General information, not legal or insurance advice.** Coverage rules have exceptions (industries, job types, out-of-state work). Check the state agency or a licensed professional before you decide.

Published by [Zylar](https://zylarai.com/?utm_source=github&utm_medium=referral&utm_campaign=dataset_workers_comp&utm_content=readme) under [CC BY 4.0](https://creativecommons.org/licenses/by/4.0/). You may use, share and adapt it, including commercially, if you credit Zylar and link to the source.

Archived on Zenodo: DOI [10.5281/zenodo.24531495](https://doi.org/10.5281/zenodo.24531495).

Companion datasets:
- [US state LLC formation and yearly fees](https://github.com/zylarai/us-state-llc-fees) (DOI [10.5281/zenodo.24404984](https://doi.org/10.5281/zenodo.24404984))
- [US state seller's permits and business licenses](https://github.com/zylarai/us-state-selling-permits) (DOI [10.5281/zenodo.24483920](https://doi.org/10.5281/zenodo.24483920))
- [US state required workplace posters](https://github.com/zylarai/us-state-workplace-posters) (DOI [10.5281/zenodo.24531513](https://doi.org/10.5281/zenodo.24531513))

## What the official pages say

- **Coverage from the first employee** in 20 jurisdictions: AK, AZ, CA, DC, DE, HI, ID, IL, MA, ME, MN, MT, ND, NH, NJ, NY, OR, PA, UT and VT.
- **Higher thresholds:**
  - 3 employees in AR, GA, MI, NC, NM, VA and WI.
  - 4 in Florida (non-construction; construction starts at 1) and South Carolina.
  - 5 in Alabama and Missouri.
  - In the other 20 states the employee count was not stated in a form we could confirm, so the cell is empty. See `threshold_note` and `to_confirm`.
- **Monopolistic state funds** (no private insurers): North Dakota, Ohio, Washington and Wyoming.
- **Private opt-out:** of the states with a confirmed answer in this dataset, only Texas lets a private employer choose not to carry coverage (a "non-subscriber"), under Texas Labor Code 406.002.
- **Sole proprietors with no employees:**
  - Not required to carry coverage, per the official page, in 18 states.
  - In 8 states they may elect coverage.
  - Elsewhere the page does not say, so the cell is empty.

## Files

| File | What it holds |
|---|---|
| `us-state-workers-comp-requirements.csv` | One row per state. Lists inside a cell are separated by spaces (URLs) or semicolons (notes). |
| `us-state-workers-comp-requirements.json` | The same records as JSON, keyed by state code. |
| `LICENSE` | CC BY 4.0 legal text. |

## Columns

| Column | Meaning |
|---|---|
| `state`, `code` | State name and postal code |
| `agency` | State workers' compensation agency |
| `required_threshold_employees` | Employee count at which a typical private employer must carry coverage; empty if not confirmed |
| `threshold_note` | The official wording |
| `construction_rule`, `agriculture_rule` | Different rules for construction and farm labor, where stated |
| `counts_owners` | Whether corporate officers and LLC members count, and whether they can opt out |
| `sole_prop_no_employees` | `not_required`, `required` or `optional` for an owner with no employees, where stated |
| `owner_exemption_form`, `exemption_form_url` | Exemption or election form for owners, with fee and validity where stated |
| `insurance_market` | `private_only`, `private_or_state_fund`, `private_or_self_insure` or `monopolistic_state_fund` |
| `private_opt_out` | `yes` if a private employer may legally choose not to carry coverage |
| `penalty_summary` | Penalty for not carrying required coverage, as stated officially |
| `coverage_verification_url`, `employer_guide_url`, `spanish_info_url` | Official lookup, employer guide and Spanish page |
| `ui_registration_url`, `withholding_registration_url`, `withholding_note`, `new_hire_reporting_url` | First-hire registration pages |
| `statute_citation` | Main statute for the coverage rule |
| `official_sources`, `to_confirm`, `checked_on` | Sources used, open points with reasons, date checked |

## Limits

- Several state sites refuse automated or out-of-country reading (for example Colorado, Kentucky, Louisiana, Mississippi, Nebraska, Nevada, Oklahoma and Tennessee). Their rows are thin. Each empty cell is explained in `to_confirm`.
- Some registration links point to the agency page the IRS state directory links to, not to the registration form itself. This is noted per row.
- Rules change. Check the official source before relying on a value.
- Found an error or a newer official page? Open an issue. We recheck the data regularly.

## How to cite

Zylar (2026). *US state workers' compensation requirements for small businesses (50 states and DC, 2026)* (Version v2026.11) [Data set]. Zenodo. https://doi.org/10.5281/zenodo.24531495

## About Zylar

Zylar checks a business or startup idea before you build it. It looks at what the market says, who else does it, whether you can deliver it and what could go wrong, and gives a scored verdict in a few minutes. It is in early alpha and free to try: [sign up here](https://zylarai.com/?utm_source=github&utm_medium=referral&utm_campaign=dataset_workers_comp&utm_content=readme_about). Advisory only. You decide.
