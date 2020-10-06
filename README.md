# Techniques

Adds fields to the tender and lot objects to describe the use of techniques, such as framework agreements, dynamic purchasing systems and electronic auctions.

## Legal context

In the European Union, this extension's fields correspond to [eForms BG-706 (Techniques)](https://github.com/eForms/eForms). See [OCDS for the European Union](http://standard.open-contracting.org/profiles/eu/master/en/) for the correspondences to Tenders Electronic Daily (TED).

## Examples

### Framework agreement

```json
{
  "tender": {
    "lots": [
      {
        "id": "1",
        "techniques": {
          "hasFrameworkAgreement": true,
          "frameworkAgreement": {
            "minimumParticipants": 2,
            "maximumParticipants": 100,
            "method": "withoutReopeningCompetition",
            "periodRationale": "<A good justification>",
            "buyerCategories": "all hospitals in the Tuscany region",
            "value": {
              "amount": 240000,
              "currency": "EUR"
            },
            "period": {
              "durationInDays": 730
            },
            "description": "Call offs are estimated to be organized every 3 months, with an average value of 60,000 euros per contract."
          }
        }
      }
    ]
  }
}
```

### Dynamic purchasing system

```json
{
  "tender": {
    "lots": [
      {
        "id": "1",
        "techniques": {
          "hasDynamicPurchasingSystem": true,
          "dynamicPurchasingSystem": {
            "type": "closed",
            "status": "active"
          }
        }
      }
    ]
  }
}
```

### Electronic auction

```json
{
  "tender": {
    "lots": [
      {
        "id": "1",
        "techniques": {
          "hasElectronicAuction": true,
          "electronicAuction": {
            "url": "https://example.com/auction/1",
            "description": "<Any relevant details>"
          }
        }
      }
    ]
  }
}
```

## Issues

Report issues for this extension in the [ocds-extensions repository](https://github.com/open-contracting/ocds-extensions/issues), putting the extension's name in the issue's title.

## Changelog

### 2020-10-05

* Add `minimumParticipants`, `value` fields to `frameworkAgreement`

### 2020-04-24

* Add `minProperties`, `minItems` and/or `minLength` properties.

This extension was originally discussed as part of the [OCDS for EU profile](https://github.com/open-contracting-extensions/european-union/issues), in [pull requests](https://github.com/open-contracting-extensions/ocds_techniques_extension/pulls?q=is%3Apr+is%3Aclosed) and in <https://github.com/open-contracting/standard/issues/695>.
