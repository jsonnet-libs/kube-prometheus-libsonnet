---
permalink: /0.8/monitoring/v1alpha1/endpoint/
---

# monitoring.v1alpha1.endpoint

Endpoint is a helper to create endpoint configurations in ServiceMonitors. An endpoint defines a scrapeable endpoint serving Prometheus metrics.

## Index

* [`fn withBearerTokenFile(path)`](#fn-withbearertokenfile)
* [`fn withHonorLabels(honor_labels)`](#fn-withhonorlabels)
* [`fn withHonorTimestamps(honor_timestamps)`](#fn-withhonortimestamps)
* [`fn withInterval(interval)`](#fn-withinterval)
* [`fn withMetricRelabelings(relabelings)`](#fn-withmetricrelabelings)
* [`fn withParams(params)`](#fn-withparams)
* [`fn withPath(path)`](#fn-withpath)
* [`fn withPort(port)`](#fn-withport)
* [`fn withProxyUrl(url)`](#fn-withproxyurl)
* [`fn withRelabelings(relabelings)`](#fn-withrelabelings)
* [`fn withScheme(scheme)`](#fn-withscheme)
* [`fn withScrapeTimeout(timeout)`](#fn-withscrapetimeout)
* [`fn withTargetPort(port)`](#fn-withtargetport)
* [`obj authorization`](#obj-authorization)
  * [`fn withType(type)`](#fn-authorizationwithtype)
  * [`obj authorization.credentials`](#obj-authorizationcredentials)
    * [`fn withKey(key)`](#fn-authorizationcredentialswithkey)
    * [`fn withName(name)`](#fn-authorizationcredentialswithname)
    * [`fn withOptional(is_optional)`](#fn-authorizationcredentialswithoptional)
* [`obj basicAuth`](#obj-basicauth)
  * [`obj basicAuth.password`](#obj-basicauthpassword)
    * [`fn withKey(key)`](#fn-basicauthpasswordwithkey)
    * [`fn withName(name)`](#fn-basicauthpasswordwithname)
    * [`fn withOptional(is_optional)`](#fn-basicauthpasswordwithoptional)
  * [`obj basicAuth.username`](#obj-basicauthusername)
    * [`fn withKey(key)`](#fn-basicauthusernamewithkey)
    * [`fn withName(name)`](#fn-basicauthusernamewithname)
    * [`fn withOptional(is_optional)`](#fn-basicauthusernamewithoptional)
* [`obj bearerTokenSecret`](#obj-bearertokensecret)
  * [`fn withKey(key)`](#fn-bearertokensecretwithkey)
  * [`fn withName(name)`](#fn-bearertokensecretwithname)
  * [`fn withOptional(is_optional)`](#fn-bearertokensecretwithoptional)
* [`obj oauth2`](#obj-oauth2)
  * [`fn withEndpointParams(params)`](#fn-oauth2withendpointparams)
  * [`fn withScopes(scopes)`](#fn-oauth2withscopes)
  * [`fn withTokenUrl(url)`](#fn-oauth2withtokenurl)
  * [`obj oauth2.clientId`](#obj-oauth2clientid)
    * [`obj oauth2.clientId.configMap`](#obj-oauth2clientidconfigmap)
      * [`fn withKey(key)`](#fn-oauth2clientidconfigmapwithkey)
      * [`fn withName(name)`](#fn-oauth2clientidconfigmapwithname)
      * [`fn withOptional(is_optional)`](#fn-oauth2clientidconfigmapwithoptional)
    * [`obj oauth2.clientId.secret`](#obj-oauth2clientidsecret)
      * [`fn withKey(key)`](#fn-oauth2clientidsecretwithkey)
      * [`fn withName(name)`](#fn-oauth2clientidsecretwithname)
      * [`fn withOptional(is_optional)`](#fn-oauth2clientidsecretwithoptional)
  * [`obj oauth2.clientSecret`](#obj-oauth2clientsecret)
    * [`fn withKey(key)`](#fn-oauth2clientsecretwithkey)
    * [`fn withName(name)`](#fn-oauth2clientsecretwithname)
    * [`fn withOptional(is_optional)`](#fn-oauth2clientsecretwithoptional)
* [`obj tlsConfig`](#obj-tlsconfig)
  * [`fn withCaFile(path)`](#fn-tlsconfigwithcafile)
  * [`fn withCertFile(path)`](#fn-tlsconfigwithcertfile)
  * [`fn withInsecureSkipVerify(skip_verify)`](#fn-tlsconfigwithinsecureskipverify)
  * [`fn withKeyFile(path)`](#fn-tlsconfigwithkeyfile)
  * [`fn withServerName(name)`](#fn-tlsconfigwithservername)
  * [`obj tlsConfig.ca`](#obj-tlsconfigca)
    * [`obj tlsConfig.ca.configMap`](#obj-tlsconfigcaconfigmap)
      * [`fn withKey(key)`](#fn-tlsconfigcaconfigmapwithkey)
      * [`fn withName(name)`](#fn-tlsconfigcaconfigmapwithname)
      * [`fn withOptional(is_optional)`](#fn-tlsconfigcaconfigmapwithoptional)
    * [`obj tlsConfig.ca.secret`](#obj-tlsconfigcasecret)
      * [`fn withKey(key)`](#fn-tlsconfigcasecretwithkey)
      * [`fn withName(name)`](#fn-tlsconfigcasecretwithname)
      * [`fn withOptional(is_optional)`](#fn-tlsconfigcasecretwithoptional)
  * [`obj tlsConfig.cert`](#obj-tlsconfigcert)
    * [`obj tlsConfig.cert.configMap`](#obj-tlsconfigcertconfigmap)
      * [`fn withKey(key)`](#fn-tlsconfigcertconfigmapwithkey)
      * [`fn withName(name)`](#fn-tlsconfigcertconfigmapwithname)
      * [`fn withOptional(is_optional)`](#fn-tlsconfigcertconfigmapwithoptional)
    * [`obj tlsConfig.cert.secret`](#obj-tlsconfigcertsecret)
      * [`fn withKey(key)`](#fn-tlsconfigcertsecretwithkey)
      * [`fn withName(name)`](#fn-tlsconfigcertsecretwithname)
      * [`fn withOptional(is_optional)`](#fn-tlsconfigcertsecretwithoptional)
  * [`obj tlsConfig.keySecret`](#obj-tlsconfigkeysecret)
    * [`fn withKey(key)`](#fn-tlsconfigkeysecretwithkey)
    * [`fn withName(name)`](#fn-tlsconfigkeysecretwithname)
    * [`fn withOptional(is_optional)`](#fn-tlsconfigkeysecretwithoptional)

## Fields

### fn withBearerTokenFile

```ts
withBearerTokenFile(path)
```

File to read bearer token for scraping targets.

### fn withHonorLabels

```ts
withHonorLabels(honor_labels)
```

HonorLabels chooses the metric’s labels on collisions with target labels.

### fn withHonorTimestamps

```ts
withHonorTimestamps(honor_timestamps)
```

HonorTimestamps controls whether Prometheus respects the timestamps present in scraped data.

### fn withInterval

```ts
withInterval(interval)
```

Interval at which metrics should be scraped.

### fn withMetricRelabelings

```ts
withMetricRelabelings(relabelings)
```

MetricRelabelConfigs to apply to samples before ingestion.

### fn withParams

```ts
withParams(params)
```

Optional HTTP URL parameters.

### fn withPath

```ts
withPath(path)
```

HTTP path to scrape for metrics.

### fn withPort

```ts
withPort(port)
```

Name of the service port this endpoint refers to. Mutually exclusive with withTargetPort.

### fn withProxyUrl

```ts
withProxyUrl(url)
```

ProxyURL eg http://proxyserver:2195 Directs scrapes to proxy through this endpoint.

### fn withRelabelings

```ts
withRelabelings(relabelings)
```

RelabelConfigs to apply to samples before scraping. Prometheus Operator automatically adds relabelings for a few standard Kubernetes fields and replaces original scrape job name with __tmp_prometheus_job_name. More info: https://prometheus.io/docs/prometheus/latest/configuration/configuration/#relabel_config

### fn withScheme

```ts
withScheme(scheme)
```

HTTP scheme to use for scraping.

### fn withScrapeTimeout

```ts
withScrapeTimeout(timeout)
```

Timeout after which the scrape is ended.

### fn withTargetPort

```ts
withTargetPort(port)
```

Name or number of the target port of the Pod behind the Service, the port must be specified with container port property. Mutually exclusive with withPort.

## obj authorization

Authorization section for this endpoint

### fn authorization.withType

```ts
withType(type)
```

Set the authentication type. Defaults to Bearer, Basic will cause an error

## obj authorization.credentials

The secret's key that contains the credentials of the request

### fn authorization.credentials.withKey

```ts
withKey(key)
```

The key of the secret to select from.  Must be a valid secret key.

### fn authorization.credentials.withName

```ts
withName(name)
```

Name of the referent. More info: https://kubernetes.io/docs/concepts/overview/working-with-objects/names/#names

### fn authorization.credentials.withOptional

```ts
withOptional(is_optional)
```

Specify whether the Secret or its key must be defined

## obj basicAuth

BasicAuth allow an endpoint to authenticate over basic authentication More info: https://prometheus.io/docs/operating/configuration/#endpoints

## obj basicAuth.password

The secret in the service monitor namespace that contains the password for authentication.

### fn basicAuth.password.withKey

```ts
withKey(key)
```

The key of the secret to select from.  Must be a valid secret key.

### fn basicAuth.password.withName

```ts
withName(name)
```

Name of the referent. More info: https://kubernetes.io/docs/concepts/overview/working-with-objects/names/#names

### fn basicAuth.password.withOptional

```ts
withOptional(is_optional)
```

Specify whether the Secret or its key must be defined

## obj basicAuth.username

The secret in the service monitor namespace that contains the username for authentication.

### fn basicAuth.username.withKey

```ts
withKey(key)
```

The key of the secret to select from.  Must be a valid secret key.

### fn basicAuth.username.withName

```ts
withName(name)
```

Name of the referent. More info: https://kubernetes.io/docs/concepts/overview/working-with-objects/names/#names

### fn basicAuth.username.withOptional

```ts
withOptional(is_optional)
```

Specify whether the Secret or its key must be defined

## obj bearerTokenSecret

Secret to mount to read bearer token for scraping targets. The secret needs to be in the same namespace as the service monitor and accessible by the Prometheus Operator.

### fn bearerTokenSecret.withKey

```ts
withKey(key)
```

The key of the secret to select from.  Must be a valid secret key.

### fn bearerTokenSecret.withName

```ts
withName(name)
```

Name of the referent. More info: https://kubernetes.io/docs/concepts/overview/working-with-objects/names/#names

### fn bearerTokenSecret.withOptional

```ts
withOptional(is_optional)
```

Specify whether the Secret or its key must be defined

## obj oauth2

OAuth2 for the URL. Only valid in Prometheus versions 2.27.0 and newer.

### fn oauth2.withEndpointParams

```ts
withEndpointParams(params)
```

Parameters to append to the token URL

### fn oauth2.withScopes

```ts
withScopes(scopes)
```

OAuth2 scopes used for the token request.

### fn oauth2.withTokenUrl

```ts
withTokenUrl(url)
```

The URL to fetch the token from.

## obj oauth2.clientId

The secret or configmap containing the OAuth2 client id.

## obj oauth2.clientId.configMap

ConfigMap containing data to use for the targets. Mutually exclusive with secret.

### fn oauth2.clientId.configMap.withKey

```ts
withKey(key)
```

The key to select.

### fn oauth2.clientId.configMap.withName

```ts
withName(name)
```

Name of the referent. More info: https://kubernetes.io/docs/concepts/overview/working-with-objects/names/#names

### fn oauth2.clientId.configMap.withOptional

```ts
withOptional(is_optional)
```

Specify whether the ConfigMap or its key must be defined.

## obj oauth2.clientId.secret

Secret containing data to use for the targets. Mutually exclusive with configMap.

### fn oauth2.clientId.secret.withKey

```ts
withKey(key)
```

The key of the secret to select from.  Must be a valid secret key.

### fn oauth2.clientId.secret.withName

```ts
withName(name)
```

Name of the referent. More info: https://kubernetes.io/docs/concepts/overview/working-with-objects/names/#names

### fn oauth2.clientId.secret.withOptional

```ts
withOptional(is_optional)
```

Specify whether the Secret or its key must be defined

## obj oauth2.clientSecret

The secret containing the OAuth2 client secret.

### fn oauth2.clientSecret.withKey

```ts
withKey(key)
```

The key of the secret to select from.  Must be a valid secret key.

### fn oauth2.clientSecret.withName

```ts
withName(name)
```

Name of the referent. More info: https://kubernetes.io/docs/concepts/overview/working-with-objects/names/#names

### fn oauth2.clientSecret.withOptional

```ts
withOptional(is_optional)
```

Specify whether the Secret or its key must be defined

## obj tlsConfig

TLS configuration to use when scraping the endpoint

### fn tlsConfig.withCaFile

```ts
withCaFile(path)
```

Path to the CA cert in the Prometheus container to use for the targets.

### fn tlsConfig.withCertFile

```ts
withCertFile(path)
```

Path to the client cert file in the Prometheus container for the targets.

### fn tlsConfig.withInsecureSkipVerify

```ts
withInsecureSkipVerify(skip_verify)
```

Disable target certificate validation.

### fn tlsConfig.withKeyFile

```ts
withKeyFile(path)
```

Path to the client key file in the Prometheus container for the targets.

### fn tlsConfig.withServerName

```ts
withServerName(name)
```

Used to verify the hostname for the targets.

## obj tlsConfig.ca

Struct containing the CA cert to use for the targets.

## obj tlsConfig.ca.configMap

ConfigMap containing data to use for the targets. Mutually exclusive with secret.

### fn tlsConfig.ca.configMap.withKey

```ts
withKey(key)
```

The key to select.

### fn tlsConfig.ca.configMap.withName

```ts
withName(name)
```

Name of the referent. More info: https://kubernetes.io/docs/concepts/overview/working-with-objects/names/#names

### fn tlsConfig.ca.configMap.withOptional

```ts
withOptional(is_optional)
```

Specify whether the ConfigMap or its key must be defined.

## obj tlsConfig.ca.secret

Secret containing data to use for the targets. Mutually exclusive with configMap.

### fn tlsConfig.ca.secret.withKey

```ts
withKey(key)
```

The key of the secret to select from.  Must be a valid secret key.

### fn tlsConfig.ca.secret.withName

```ts
withName(name)
```

Name of the referent. More info: https://kubernetes.io/docs/concepts/overview/working-with-objects/names/#names

### fn tlsConfig.ca.secret.withOptional

```ts
withOptional(is_optional)
```

Specify whether the Secret or its key must be defined

## obj tlsConfig.cert

Struct containing the client cert file for the targets.

## obj tlsConfig.cert.configMap

ConfigMap containing data to use for the targets. Mutually exclusive with secret.

### fn tlsConfig.cert.configMap.withKey

```ts
withKey(key)
```

The key to select.

### fn tlsConfig.cert.configMap.withName

```ts
withName(name)
```

Name of the referent. More info: https://kubernetes.io/docs/concepts/overview/working-with-objects/names/#names

### fn tlsConfig.cert.configMap.withOptional

```ts
withOptional(is_optional)
```

Specify whether the ConfigMap or its key must be defined.

## obj tlsConfig.cert.secret

Secret containing data to use for the targets. Mutually exclusive with configMap.

### fn tlsConfig.cert.secret.withKey

```ts
withKey(key)
```

The key of the secret to select from.  Must be a valid secret key.

### fn tlsConfig.cert.secret.withName

```ts
withName(name)
```

Name of the referent. More info: https://kubernetes.io/docs/concepts/overview/working-with-objects/names/#names

### fn tlsConfig.cert.secret.withOptional

```ts
withOptional(is_optional)
```

Specify whether the Secret or its key must be defined

## obj tlsConfig.keySecret

Secret containing the client key file for the targets.

### fn tlsConfig.keySecret.withKey

```ts
withKey(key)
```

The key of the secret to select from.  Must be a valid secret key.

### fn tlsConfig.keySecret.withName

```ts
withName(name)
```

Name of the referent. More info: https://kubernetes.io/docs/concepts/overview/working-with-objects/names/#names

### fn tlsConfig.keySecret.withOptional

```ts
withOptional(is_optional)
```

Specify whether the Secret or its key must be defined