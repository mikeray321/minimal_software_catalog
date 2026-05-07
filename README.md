# minimal_software_catalog
minimal software catalog

```
cookiecutter-inventory-item/
├── cookiecutter.json          # The configuration file for user input
└── {{cookiecutter.service_id}}/ # The template directory
    └── catalog-info.yaml      # The generated file
```


```
cookiecutter.json
{
  "service_id": "payment-gateway",
  "display_name": "Payment Gateway API",
  "description": "Handles all incoming Stripe and PayPal transactions.",
  "owner_team": "fintech-core",
  "slack_contact": "#team-payments-slack",
  "repo_url": "https://github.com/org/payment-gateway",
  "runbook_url": "https://wiki.internal/runbooks/payments"
}
```



```
catalog-info.yaml
# Simple Inventory Schema
service_id: "{{ cookiecutter.service_id }}"
display_name: "{{ cookiecutter.display_name }}"
description: "{{ cookiecutter.description }}"

# The "Who"
owner:
  team: "{{ cookiecutter.owner_team }}"
  contact: "{{ cookiecutter.slack_contact }}"

# The "Where"
links:
  repository: "{{ cookiecutter.repo_url }}"
  runbook: "{{ cookiecutter.runbook_url }}"
```

RUN IT
cookiecutter https://github.com/your-username/cookiecutter-inventory-item

