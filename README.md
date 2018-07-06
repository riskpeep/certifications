# certifications
Certification control selections in OpenControl formats.

To import these data into a OpenControl project add the follow code to your opencontrol.yaml file.
```yaml
dependencies:
  certifications:
    - url: https://github.com/riskpeep/certifications
      revision: master
```

Once imported into your OpenControl content, [Compliance Masonry](https://github.com/opencontrol/compliance-masonry) and [FedRAMP Templater](https://github.com/opencontrol/fedramp-templater) can be used to generate template System Security Plans (SSPs):
```
compliance-masonry get
compliance-masonry docs gitbook fedramp-high
fedramp-templater fill opencontrols/ ./path_to_fedramp_templates/FedRAMP-System-Security-Plan-Template-v2.1.docx exports/FedRAMP-filled.docx
```

For more information on the opencontrol.yaml visit the [Compliance Masonry CLI](https://github.com/opencontrol/compliance-masonry#creating-an-opencontrol-project).

## Why this Fork
This fork is created to add in additional certifications that we're aiming for (e.g. 48 CFR 52.204-21, NIST 800-171) in addition to the existing ones

## About the 48 CFR 52.204-21
This repository includes a definition of 48 CFR 52.204-21: Basic Safeguarding of Covered Contractor Information Systems as amended July 14, 2016.

48cfr-52.204-21.yaml is an OpenControl certifications file that selects all of 48 CFR 52.204-21 controls.

