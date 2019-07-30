# Techniques

Adds fields to the tender object to describe the use of techniques, such as framework agreements without reopening of competition, framework agreements with reopening of competition, dynamic purchasing systems and electronic auctions.

## Legal context

In the European Union, this extension's fields correspond to [eForms BG-706 (Techniques)](https://github.com/eForms/eForms). See [OCDS for the European Union](http://standard.open-contracting.org/profiles/eu/master/en/) for the correspondences to Tenders Electronic Daily (TED).

## Examples

### Framework agreement

```json
{
  "tender": {
    "hasFrameworkAgreement": true,
    "frameworkAgreement": {
      "maximumNumberParticipants": 100,
      "method": "withoutReopeningCompetition",
      "durationRationale": "<A good justification>",
      "buyerCategories": "all hospitals in the Tuscany region"
    }
  }
}
```

### Dynamic purchasing system

```json
{
  "tender": {
    "hasDynamicPurchasingSystem": true,
    "dynamicPurchasingSystem": {
      "type": "closed"
    }
  }
}
```

### Electronic auction

```json
{
  "tender": {
    "hasElectronicAuction": true,
    "electronicAuction": {
      "url": "https://example.com/auction/1",
      "description": "<Any relevant details>"
    }
  }
}
```

## Issues

Report issues for this extension in the [ocds-extensions repository](https://github.com/open-contracting/ocds-extensions/issues), putting the extension's name in the issue's title.
