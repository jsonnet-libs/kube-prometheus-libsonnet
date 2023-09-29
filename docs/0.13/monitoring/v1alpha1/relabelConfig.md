---
permalink: /0.13/monitoring/v1alpha1/relabelConfig/
---

# monitoring.v1alpha1.relabelConfig

RelabelConfig is a help to build RelabelConfig objects for ServiceMonitors and PodMonitors

## Index

* [`fn withAction(separator)`](#fn-withaction)
* [`fn withModulus(modulus)`](#fn-withmodulus)
* [`fn withRegex(separator)`](#fn-withregex)
* [`fn withReplacement(separator)`](#fn-withreplacement)
* [`fn withSeparator(separator)`](#fn-withseparator)
* [`fn withSourceLabels(labels)`](#fn-withsourcelabels)
* [`fn withTargetLabel(separator)`](#fn-withtargetlabel)

## Fields

### fn withAction

```ts
withAction(separator)
```

Action to perform based on regex matching. Default is ‘replace’

### fn withModulus

```ts
withModulus(modulus)
```

Modulus to take of the hash of the source label values.

### fn withRegex

```ts
withRegex(separator)
```

Regular expression against which the extracted value is matched. Default is ‘(.*)’

### fn withReplacement

```ts
withReplacement(separator)
```

Replacement value against which a regex replace is performed if the regular expression matches. Regex capture groups are available. Default is ‘$1’

### fn withSeparator

```ts
withSeparator(separator)
```

Separator placed between concatenated source label values. default is ‘;’.

### fn withSourceLabels

```ts
withSourceLabels(labels)
```

The source labels select values from existing labels. Their content is concatenated using the configured separator and matched against the configured regular expression for the replace, keep, and drop actions.

### fn withTargetLabel

```ts
withTargetLabel(separator)
```

Label to which the resulting value is written in a replace action. It is mandatory for replace actions. Regex capture groups are available.