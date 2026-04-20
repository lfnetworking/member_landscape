[![Build Landscape from LFX](https://github.com/lfnetworking/member_landscape/actions/workflows/build.yml/badge.svg)](https://github.com/lfnetworking/member_landscape/actions/workflows/build.yml)

# LF Networking Landscape

![LF Networking Landscape Logo](images/left-logo.svg)

-   [About]
-   [How It Works]
-   [Updating Your Organization's Information]
-   [Getting Listed]
-   [Logo Requirements]
-   [License]

## About

The LF Networking Landscape is a map of the member organizations and projects -- including [LFN Super Blueprints](https://blueprints.lfnetworking.org/), [ONAP](https://www.onap.org/), [OpenDaylight](https://www.opendaylight.org/), and others -- in the LF Networking community. You can explore it at **[landscape.lfnetworking.org](https://landscape.lfnetworking.org/)**.

It is generated using the [Landscape2](https://github.com/cncf/landscape2) tool.

## How It Works

The landscape is rebuilt nightly from the data in this repository. Member organization data (name, logo, description, and homepage) is pulled automatically from LFX each night, so most organizations never need to touch this repository directly.

## Updating Your Organization's Information

**LF Networking member organizations** should update their name, logo, description, or homepage via their organization's LFX dashboard at [https://myorg.lfx.dev](https://myorg.lfx.dev). Updates will be reflected in the landscape automatically on the next nightly build -- no pull request needed.

The [Landscape2 data schema][schema] supports additional optional fields beyond what LFX provides -- such as `joined`, `twitter`, `enduser`, and a range of `extra` fields including `blog_url`, `linkedin_url`, and `artwork_url`. To add any of these to your entry, please open a pull request with edits to [landscape.yml], or email [support@lfnetworking.org](mailto:support@lfnetworking.org) if you are not familiar with GitHub.

## Getting Listed

LF Networking member organizations are added to the landscape automatically via LFX. If your organization is not yet listed and you believe it should be, please open a pull request with edits to [landscape.yml] or email [support@lfnetworking.org](mailto:support@lfnetworking.org).

Include an SVG logo in the `hosted_logos/` directory and reference it by filename only (no path) in the `logo` field.

### Required Fields

```yaml
- item:
  name: <organization name>
  homepage_url: <website>
  logo: <filename of .svg in the hosted_logos folder>
```

## Logo Requirements

Logos must be in **SVG format** (PNG and JPG are not accepted) and placed in the `hosted_logos/` directory. Use a filename that clearly identifies your organization (e.g., `mycompany.svg`) and reference it by filename only (no path) in the `logo` field of `landscape.yml`.

SVG files must not contain embedded text elements -- any text in your logo (such as your company name or tagline) must be converted to paths/outlines before saving. If this step is skipped, the build will fail. Most vector graphics tools handle this with a simple menu option:

-   **Inkscape:** Path > Object to Path
-   **Adobe Illustrator:** Type > Create Outlines
-   **Sketch/Figma:** Use "Outline Stroke" or export as "Flatten" SVG

## License

Everything in this repository is under the Apache License, Version 2.0, except for project and product logos, which are generally copyrighted by the company that created them, and are simply cached here for reliability. The [landscape.yml] file is alternatively available under the [Creative Commons Attribution 4.0 license].

[About]: #about
[How It Works]: #how-it-works
[Updating Your Organization's Information]: #updating-your-organizations-information
[Getting Listed]: #getting-listed
[Logo Requirements]: #logo-requirements
[License]: #license
[landscape.yml]: landscape.yml
[schema]: https://raw.githubusercontent.com/cncf/landscape2/refs/heads/main/docs/config/schema/data.schema.json
[Creative Commons Attribution 4.0 license]: https://creativecommons.org/licenses/by/4.0/
