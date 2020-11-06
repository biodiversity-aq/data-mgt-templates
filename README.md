# Biodiversity data management templates

The biodiversity.aq team designed 2 types templates to help scientists manage their data in Antarctic field works. The terms used in the templates are as close to the [Darwin Core standard terms](http://rs.tdwg.org/dwc/terms.htm) as possible.

### 1. Field templates

The field templates serve to help scientists to further customise their templates to record data for a sampling event at a sampling station.

### 2. Data templates

The data templates serve to be the starting point for scientists to customise their own templates to aggregate data from multiple sampling stations (field templates).

Pull requests are welcome.

## Repo structure

The repository structure is described below.

```
.
├── README.md			: Description of this repository
├── LICENSE				: Repository license
├── slides				: Slides that explains the usage of templates
│   └── 2020-11-04_field-work-templates.pdf
└── templates
    ├── data-templates	: Templates to aggregate data from multiple field-templates
    │   ├── 2020-11_data_event.xlsx
    │   ├── ...
    └── field-templates	: Templates to record data in the field
        ├── 2020-11_field_event.xlsx
        └── ...
```

## Additional resources
* [Excel template generator](https://sios-svalbard.org/cgi-bin/darwinsheet/index.cgi?setup=darwin)
* [Darwin Core standard terms with definitions and examples](https://dwc.tdwg.org/terms/)


## Contributors

[List of contributors](https://github.com/data-biodiversity-aq/data-mgt-templates/graphs/contributors)

## Acknowledgement

We would like to acknowledge the scientists who contributed to the templates design: <br/>
Huw Griffiths, Anton Van de Putte, Fokje Schaafsma, Hauk Flores
