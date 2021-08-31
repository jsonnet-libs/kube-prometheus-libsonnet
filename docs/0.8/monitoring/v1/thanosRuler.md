---
permalink: /0.8/monitoring/v1/thanosRuler/
---

# monitoring.v1.thanosRuler

ThanosRuler defines a ThanosRuler deployment.

## Index

* [`fn new(name)`](#fn-new)
* [`obj metadata`](#obj-metadata)
  * [`fn withAnnotations(annotations)`](#fn-metadatawithannotations)
  * [`fn withAnnotationsMixin(annotations)`](#fn-metadatawithannotationsmixin)
  * [`fn withClusterName(clusterName)`](#fn-metadatawithclustername)
  * [`fn withCreationTimestamp(creationTimestamp)`](#fn-metadatawithcreationtimestamp)
  * [`fn withDeletionGracePeriodSeconds(deletionGracePeriodSeconds)`](#fn-metadatawithdeletiongraceperiodseconds)
  * [`fn withDeletionTimestamp(deletionTimestamp)`](#fn-metadatawithdeletiontimestamp)
  * [`fn withFinalizers(finalizers)`](#fn-metadatawithfinalizers)
  * [`fn withFinalizersMixin(finalizers)`](#fn-metadatawithfinalizersmixin)
  * [`fn withGenerateName(generateName)`](#fn-metadatawithgeneratename)
  * [`fn withGeneration(generation)`](#fn-metadatawithgeneration)
  * [`fn withLabels(labels)`](#fn-metadatawithlabels)
  * [`fn withLabelsMixin(labels)`](#fn-metadatawithlabelsmixin)
  * [`fn withManagedFields(managedFields)`](#fn-metadatawithmanagedfields)
  * [`fn withManagedFieldsMixin(managedFields)`](#fn-metadatawithmanagedfieldsmixin)
  * [`fn withName(name)`](#fn-metadatawithname)
  * [`fn withNamespace(namespace)`](#fn-metadatawithnamespace)
  * [`fn withOwnerReferences(ownerReferences)`](#fn-metadatawithownerreferences)
  * [`fn withOwnerReferencesMixin(ownerReferences)`](#fn-metadatawithownerreferencesmixin)
  * [`fn withResourceVersion(resourceVersion)`](#fn-metadatawithresourceversion)
  * [`fn withSelfLink(selfLink)`](#fn-metadatawithselflink)
  * [`fn withUid(uid)`](#fn-metadatawithuid)
* [`obj spec`](#obj-spec)
  * [`fn withAlertDropLabels(alertDropLabels)`](#fn-specwithalertdroplabels)
  * [`fn withAlertDropLabelsMixin(alertDropLabels)`](#fn-specwithalertdroplabelsmixin)
  * [`fn withAlertQueryUrl(alertQueryUrl)`](#fn-specwithalertqueryurl)
  * [`fn withAlertmanagersUrl(alertmanagersUrl)`](#fn-specwithalertmanagersurl)
  * [`fn withAlertmanagersUrlMixin(alertmanagersUrl)`](#fn-specwithalertmanagersurlmixin)
  * [`fn withContainers(containers)`](#fn-specwithcontainers)
  * [`fn withContainersMixin(containers)`](#fn-specwithcontainersmixin)
  * [`fn withEnforcedNamespaceLabel(enforcedNamespaceLabel)`](#fn-specwithenforcednamespacelabel)
  * [`fn withEvaluationInterval(evaluationInterval)`](#fn-specwithevaluationinterval)
  * [`fn withExternalPrefix(externalPrefix)`](#fn-specwithexternalprefix)
  * [`fn withImage(image)`](#fn-specwithimage)
  * [`fn withImagePullSecrets(imagePullSecrets)`](#fn-specwithimagepullsecrets)
  * [`fn withImagePullSecretsMixin(imagePullSecrets)`](#fn-specwithimagepullsecretsmixin)
  * [`fn withInitContainers(initContainers)`](#fn-specwithinitcontainers)
  * [`fn withInitContainersMixin(initContainers)`](#fn-specwithinitcontainersmixin)
  * [`fn withLabels(labels)`](#fn-specwithlabels)
  * [`fn withLabelsMixin(labels)`](#fn-specwithlabelsmixin)
  * [`fn withListenLocal(listenLocal)`](#fn-specwithlistenlocal)
  * [`fn withLogFormat(logFormat)`](#fn-specwithlogformat)
  * [`fn withLogLevel(logLevel)`](#fn-specwithloglevel)
  * [`fn withNodeSelector(nodeSelector)`](#fn-specwithnodeselector)
  * [`fn withNodeSelectorMixin(nodeSelector)`](#fn-specwithnodeselectormixin)
  * [`fn withObjectStorageConfigFile(objectStorageConfigFile)`](#fn-specwithobjectstorageconfigfile)
  * [`fn withPaused(paused)`](#fn-specwithpaused)
  * [`fn withPortName(portName)`](#fn-specwithportname)
  * [`fn withPriorityClassName(priorityClassName)`](#fn-specwithpriorityclassname)
  * [`fn withPrometheusRulesExcludedFromEnforce(prometheusRulesExcludedFromEnforce)`](#fn-specwithprometheusrulesexcludedfromenforce)
  * [`fn withPrometheusRulesExcludedFromEnforceMixin(prometheusRulesExcludedFromEnforce)`](#fn-specwithprometheusrulesexcludedfromenforcemixin)
  * [`fn withQueryEndpoints(queryEndpoints)`](#fn-specwithqueryendpoints)
  * [`fn withQueryEndpointsMixin(queryEndpoints)`](#fn-specwithqueryendpointsmixin)
  * [`fn withReplicas(replicas)`](#fn-specwithreplicas)
  * [`fn withRetention(retention)`](#fn-specwithretention)
  * [`fn withRoutePrefix(routePrefix)`](#fn-specwithrouteprefix)
  * [`fn withServiceAccountName(serviceAccountName)`](#fn-specwithserviceaccountname)
  * [`fn withTolerations(tolerations)`](#fn-specwithtolerations)
  * [`fn withTolerationsMixin(tolerations)`](#fn-specwithtolerationsmixin)
  * [`fn withTopologySpreadConstraints(topologySpreadConstraints)`](#fn-specwithtopologyspreadconstraints)
  * [`fn withTopologySpreadConstraintsMixin(topologySpreadConstraints)`](#fn-specwithtopologyspreadconstraintsmixin)
  * [`fn withVolumes(volumes)`](#fn-specwithvolumes)
  * [`fn withVolumesMixin(volumes)`](#fn-specwithvolumesmixin)
  * [`obj spec.affinity`](#obj-specaffinity)
    * [`obj spec.affinity.nodeAffinity`](#obj-specaffinitynodeaffinity)
      * [`fn withPreferredDuringSchedulingIgnoredDuringExecution(preferredDuringSchedulingIgnoredDuringExecution)`](#fn-specaffinitynodeaffinitywithpreferredduringschedulingignoredduringexecution)
      * [`fn withPreferredDuringSchedulingIgnoredDuringExecutionMixin(preferredDuringSchedulingIgnoredDuringExecution)`](#fn-specaffinitynodeaffinitywithpreferredduringschedulingignoredduringexecutionmixin)
      * [`obj spec.affinity.nodeAffinity.requiredDuringSchedulingIgnoredDuringExecution`](#obj-specaffinitynodeaffinityrequiredduringschedulingignoredduringexecution)
        * [`fn withNodeSelectorTerms(nodeSelectorTerms)`](#fn-specaffinitynodeaffinityrequiredduringschedulingignoredduringexecutionwithnodeselectorterms)
        * [`fn withNodeSelectorTermsMixin(nodeSelectorTerms)`](#fn-specaffinitynodeaffinityrequiredduringschedulingignoredduringexecutionwithnodeselectortermsmixin)
    * [`obj spec.affinity.podAffinity`](#obj-specaffinitypodaffinity)
      * [`fn withPreferredDuringSchedulingIgnoredDuringExecution(preferredDuringSchedulingIgnoredDuringExecution)`](#fn-specaffinitypodaffinitywithpreferredduringschedulingignoredduringexecution)
      * [`fn withPreferredDuringSchedulingIgnoredDuringExecutionMixin(preferredDuringSchedulingIgnoredDuringExecution)`](#fn-specaffinitypodaffinitywithpreferredduringschedulingignoredduringexecutionmixin)
      * [`fn withRequiredDuringSchedulingIgnoredDuringExecution(requiredDuringSchedulingIgnoredDuringExecution)`](#fn-specaffinitypodaffinitywithrequiredduringschedulingignoredduringexecution)
      * [`fn withRequiredDuringSchedulingIgnoredDuringExecutionMixin(requiredDuringSchedulingIgnoredDuringExecution)`](#fn-specaffinitypodaffinitywithrequiredduringschedulingignoredduringexecutionmixin)
    * [`obj spec.affinity.podAntiAffinity`](#obj-specaffinitypodantiaffinity)
      * [`fn withPreferredDuringSchedulingIgnoredDuringExecution(preferredDuringSchedulingIgnoredDuringExecution)`](#fn-specaffinitypodantiaffinitywithpreferredduringschedulingignoredduringexecution)
      * [`fn withPreferredDuringSchedulingIgnoredDuringExecutionMixin(preferredDuringSchedulingIgnoredDuringExecution)`](#fn-specaffinitypodantiaffinitywithpreferredduringschedulingignoredduringexecutionmixin)
      * [`fn withRequiredDuringSchedulingIgnoredDuringExecution(requiredDuringSchedulingIgnoredDuringExecution)`](#fn-specaffinitypodantiaffinitywithrequiredduringschedulingignoredduringexecution)
      * [`fn withRequiredDuringSchedulingIgnoredDuringExecutionMixin(requiredDuringSchedulingIgnoredDuringExecution)`](#fn-specaffinitypodantiaffinitywithrequiredduringschedulingignoredduringexecutionmixin)
  * [`obj spec.alertmanagersConfig`](#obj-specalertmanagersconfig)
    * [`fn withKey(key)`](#fn-specalertmanagersconfigwithkey)
    * [`fn withName(name)`](#fn-specalertmanagersconfigwithname)
    * [`fn withOptional(optional)`](#fn-specalertmanagersconfigwithoptional)
  * [`obj spec.grpcServerTlsConfig`](#obj-specgrpcservertlsconfig)
    * [`fn withCaFile(caFile)`](#fn-specgrpcservertlsconfigwithcafile)
    * [`fn withCertFile(certFile)`](#fn-specgrpcservertlsconfigwithcertfile)
    * [`fn withInsecureSkipVerify(insecureSkipVerify)`](#fn-specgrpcservertlsconfigwithinsecureskipverify)
    * [`fn withKeyFile(keyFile)`](#fn-specgrpcservertlsconfigwithkeyfile)
    * [`fn withServerName(serverName)`](#fn-specgrpcservertlsconfigwithservername)
    * [`obj spec.grpcServerTlsConfig.ca`](#obj-specgrpcservertlsconfigca)
      * [`obj spec.grpcServerTlsConfig.ca.configMap`](#obj-specgrpcservertlsconfigcaconfigmap)
        * [`fn withKey(key)`](#fn-specgrpcservertlsconfigcaconfigmapwithkey)
        * [`fn withName(name)`](#fn-specgrpcservertlsconfigcaconfigmapwithname)
        * [`fn withOptional(optional)`](#fn-specgrpcservertlsconfigcaconfigmapwithoptional)
      * [`obj spec.grpcServerTlsConfig.ca.secret`](#obj-specgrpcservertlsconfigcasecret)
        * [`fn withKey(key)`](#fn-specgrpcservertlsconfigcasecretwithkey)
        * [`fn withName(name)`](#fn-specgrpcservertlsconfigcasecretwithname)
        * [`fn withOptional(optional)`](#fn-specgrpcservertlsconfigcasecretwithoptional)
    * [`obj spec.grpcServerTlsConfig.cert`](#obj-specgrpcservertlsconfigcert)
      * [`obj spec.grpcServerTlsConfig.cert.configMap`](#obj-specgrpcservertlsconfigcertconfigmap)
        * [`fn withKey(key)`](#fn-specgrpcservertlsconfigcertconfigmapwithkey)
        * [`fn withName(name)`](#fn-specgrpcservertlsconfigcertconfigmapwithname)
        * [`fn withOptional(optional)`](#fn-specgrpcservertlsconfigcertconfigmapwithoptional)
      * [`obj spec.grpcServerTlsConfig.cert.secret`](#obj-specgrpcservertlsconfigcertsecret)
        * [`fn withKey(key)`](#fn-specgrpcservertlsconfigcertsecretwithkey)
        * [`fn withName(name)`](#fn-specgrpcservertlsconfigcertsecretwithname)
        * [`fn withOptional(optional)`](#fn-specgrpcservertlsconfigcertsecretwithoptional)
    * [`obj spec.grpcServerTlsConfig.keySecret`](#obj-specgrpcservertlsconfigkeysecret)
      * [`fn withKey(key)`](#fn-specgrpcservertlsconfigkeysecretwithkey)
      * [`fn withName(name)`](#fn-specgrpcservertlsconfigkeysecretwithname)
      * [`fn withOptional(optional)`](#fn-specgrpcservertlsconfigkeysecretwithoptional)
  * [`obj spec.objectStorageConfig`](#obj-specobjectstorageconfig)
    * [`fn withKey(key)`](#fn-specobjectstorageconfigwithkey)
    * [`fn withName(name)`](#fn-specobjectstorageconfigwithname)
    * [`fn withOptional(optional)`](#fn-specobjectstorageconfigwithoptional)
  * [`obj spec.podMetadata`](#obj-specpodmetadata)
    * [`fn withAnnotations(annotations)`](#fn-specpodmetadatawithannotations)
    * [`fn withAnnotationsMixin(annotations)`](#fn-specpodmetadatawithannotationsmixin)
    * [`fn withLabels(labels)`](#fn-specpodmetadatawithlabels)
    * [`fn withLabelsMixin(labels)`](#fn-specpodmetadatawithlabelsmixin)
    * [`fn withName(name)`](#fn-specpodmetadatawithname)
  * [`obj spec.queryConfig`](#obj-specqueryconfig)
    * [`fn withKey(key)`](#fn-specqueryconfigwithkey)
    * [`fn withName(name)`](#fn-specqueryconfigwithname)
    * [`fn withOptional(optional)`](#fn-specqueryconfigwithoptional)
  * [`obj spec.resources`](#obj-specresources)
    * [`fn withLimits(limits)`](#fn-specresourceswithlimits)
    * [`fn withLimitsMixin(limits)`](#fn-specresourceswithlimitsmixin)
    * [`fn withRequests(requests)`](#fn-specresourceswithrequests)
    * [`fn withRequestsMixin(requests)`](#fn-specresourceswithrequestsmixin)
  * [`obj spec.ruleNamespaceSelector`](#obj-specrulenamespaceselector)
    * [`fn withMatchExpressions(matchExpressions)`](#fn-specrulenamespaceselectorwithmatchexpressions)
    * [`fn withMatchExpressionsMixin(matchExpressions)`](#fn-specrulenamespaceselectorwithmatchexpressionsmixin)
    * [`fn withMatchLabels(matchLabels)`](#fn-specrulenamespaceselectorwithmatchlabels)
    * [`fn withMatchLabelsMixin(matchLabels)`](#fn-specrulenamespaceselectorwithmatchlabelsmixin)
  * [`obj spec.ruleSelector`](#obj-specruleselector)
    * [`fn withMatchExpressions(matchExpressions)`](#fn-specruleselectorwithmatchexpressions)
    * [`fn withMatchExpressionsMixin(matchExpressions)`](#fn-specruleselectorwithmatchexpressionsmixin)
    * [`fn withMatchLabels(matchLabels)`](#fn-specruleselectorwithmatchlabels)
    * [`fn withMatchLabelsMixin(matchLabels)`](#fn-specruleselectorwithmatchlabelsmixin)
  * [`obj spec.securityContext`](#obj-specsecuritycontext)
    * [`fn withFsGroup(fsGroup)`](#fn-specsecuritycontextwithfsgroup)
    * [`fn withFsGroupChangePolicy(fsGroupChangePolicy)`](#fn-specsecuritycontextwithfsgroupchangepolicy)
    * [`fn withRunAsGroup(runAsGroup)`](#fn-specsecuritycontextwithrunasgroup)
    * [`fn withRunAsNonRoot(runAsNonRoot)`](#fn-specsecuritycontextwithrunasnonroot)
    * [`fn withRunAsUser(runAsUser)`](#fn-specsecuritycontextwithrunasuser)
    * [`fn withSupplementalGroups(supplementalGroups)`](#fn-specsecuritycontextwithsupplementalgroups)
    * [`fn withSupplementalGroupsMixin(supplementalGroups)`](#fn-specsecuritycontextwithsupplementalgroupsmixin)
    * [`fn withSysctls(sysctls)`](#fn-specsecuritycontextwithsysctls)
    * [`fn withSysctlsMixin(sysctls)`](#fn-specsecuritycontextwithsysctlsmixin)
    * [`obj spec.securityContext.seLinuxOptions`](#obj-specsecuritycontextselinuxoptions)
      * [`fn withLevel(level)`](#fn-specsecuritycontextselinuxoptionswithlevel)
      * [`fn withRole(role)`](#fn-specsecuritycontextselinuxoptionswithrole)
      * [`fn withType(type)`](#fn-specsecuritycontextselinuxoptionswithtype)
      * [`fn withUser(user)`](#fn-specsecuritycontextselinuxoptionswithuser)
    * [`obj spec.securityContext.windowsOptions`](#obj-specsecuritycontextwindowsoptions)
      * [`fn withGmsaCredentialSpec(gmsaCredentialSpec)`](#fn-specsecuritycontextwindowsoptionswithgmsacredentialspec)
      * [`fn withGmsaCredentialSpecName(gmsaCredentialSpecName)`](#fn-specsecuritycontextwindowsoptionswithgmsacredentialspecname)
      * [`fn withRunAsUserName(runAsUserName)`](#fn-specsecuritycontextwindowsoptionswithrunasusername)
  * [`obj spec.storage`](#obj-specstorage)
    * [`fn withDisableMountSubPath(disableMountSubPath)`](#fn-specstoragewithdisablemountsubpath)
    * [`obj spec.storage.emptyDir`](#obj-specstorageemptydir)
      * [`fn withMedium(medium)`](#fn-specstorageemptydirwithmedium)
      * [`fn withSizeLimit(sizeLimit)`](#fn-specstorageemptydirwithsizelimit)
    * [`obj spec.storage.volumeClaimTemplate`](#obj-specstoragevolumeclaimtemplate)
      * [`fn withApiVersion(apiVersion)`](#fn-specstoragevolumeclaimtemplatewithapiversion)
      * [`fn withKind(kind)`](#fn-specstoragevolumeclaimtemplatewithkind)
      * [`obj spec.storage.volumeClaimTemplate.metadata`](#obj-specstoragevolumeclaimtemplatemetadata)
        * [`fn withAnnotations(annotations)`](#fn-specstoragevolumeclaimtemplatemetadatawithannotations)
        * [`fn withAnnotationsMixin(annotations)`](#fn-specstoragevolumeclaimtemplatemetadatawithannotationsmixin)
        * [`fn withLabels(labels)`](#fn-specstoragevolumeclaimtemplatemetadatawithlabels)
        * [`fn withLabelsMixin(labels)`](#fn-specstoragevolumeclaimtemplatemetadatawithlabelsmixin)
        * [`fn withName(name)`](#fn-specstoragevolumeclaimtemplatemetadatawithname)
      * [`obj spec.storage.volumeClaimTemplate.spec`](#obj-specstoragevolumeclaimtemplatespec)
        * [`fn withAccessModes(accessModes)`](#fn-specstoragevolumeclaimtemplatespecwithaccessmodes)
        * [`fn withAccessModesMixin(accessModes)`](#fn-specstoragevolumeclaimtemplatespecwithaccessmodesmixin)
        * [`fn withStorageClassName(storageClassName)`](#fn-specstoragevolumeclaimtemplatespecwithstorageclassname)
        * [`fn withVolumeMode(volumeMode)`](#fn-specstoragevolumeclaimtemplatespecwithvolumemode)
        * [`fn withVolumeName(volumeName)`](#fn-specstoragevolumeclaimtemplatespecwithvolumename)
        * [`obj spec.storage.volumeClaimTemplate.spec.dataSource`](#obj-specstoragevolumeclaimtemplatespecdatasource)
          * [`fn withApiGroup(apiGroup)`](#fn-specstoragevolumeclaimtemplatespecdatasourcewithapigroup)
          * [`fn withKind(kind)`](#fn-specstoragevolumeclaimtemplatespecdatasourcewithkind)
          * [`fn withName(name)`](#fn-specstoragevolumeclaimtemplatespecdatasourcewithname)
        * [`obj spec.storage.volumeClaimTemplate.spec.resources`](#obj-specstoragevolumeclaimtemplatespecresources)
          * [`fn withLimits(limits)`](#fn-specstoragevolumeclaimtemplatespecresourceswithlimits)
          * [`fn withLimitsMixin(limits)`](#fn-specstoragevolumeclaimtemplatespecresourceswithlimitsmixin)
          * [`fn withRequests(requests)`](#fn-specstoragevolumeclaimtemplatespecresourceswithrequests)
          * [`fn withRequestsMixin(requests)`](#fn-specstoragevolumeclaimtemplatespecresourceswithrequestsmixin)
        * [`obj spec.storage.volumeClaimTemplate.spec.selector`](#obj-specstoragevolumeclaimtemplatespecselector)
          * [`fn withMatchExpressions(matchExpressions)`](#fn-specstoragevolumeclaimtemplatespecselectorwithmatchexpressions)
          * [`fn withMatchExpressionsMixin(matchExpressions)`](#fn-specstoragevolumeclaimtemplatespecselectorwithmatchexpressionsmixin)
          * [`fn withMatchLabels(matchLabels)`](#fn-specstoragevolumeclaimtemplatespecselectorwithmatchlabels)
          * [`fn withMatchLabelsMixin(matchLabels)`](#fn-specstoragevolumeclaimtemplatespecselectorwithmatchlabelsmixin)
  * [`obj spec.tracingConfig`](#obj-spectracingconfig)
    * [`fn withKey(key)`](#fn-spectracingconfigwithkey)
    * [`fn withName(name)`](#fn-spectracingconfigwithname)
    * [`fn withOptional(optional)`](#fn-spectracingconfigwithoptional)

## Fields

### fn new

```ts
new(name)
```

new returns an instance of Thanosruler

## obj metadata

ObjectMeta is metadata that all persisted resources must have, which includes all objects users must create.

### fn metadata.withAnnotations

```ts
withAnnotations(annotations)
```

Annotations is an unstructured key value map stored with a resource that may be set by external tools to store and retrieve arbitrary metadata. They are not queryable and should be preserved when modifying objects. More info: http://kubernetes.io/docs/user-guide/annotations

### fn metadata.withAnnotationsMixin

```ts
withAnnotationsMixin(annotations)
```

Annotations is an unstructured key value map stored with a resource that may be set by external tools to store and retrieve arbitrary metadata. They are not queryable and should be preserved when modifying objects. More info: http://kubernetes.io/docs/user-guide/annotations

**Note:** This function appends passed data to existing values

### fn metadata.withClusterName

```ts
withClusterName(clusterName)
```

The name of the cluster which the object belongs to. This is used to distinguish resources with same name and namespace in different clusters. This field is not set anywhere right now and apiserver is going to ignore it if set in create or update request.

### fn metadata.withCreationTimestamp

```ts
withCreationTimestamp(creationTimestamp)
```

Time is a wrapper around time.Time which supports correct marshaling to YAML and JSON.  Wrappers are provided for many of the factory methods that the time package offers.

### fn metadata.withDeletionGracePeriodSeconds

```ts
withDeletionGracePeriodSeconds(deletionGracePeriodSeconds)
```

Number of seconds allowed for this object to gracefully terminate before it will be removed from the system. Only set when deletionTimestamp is also set. May only be shortened. Read-only.

### fn metadata.withDeletionTimestamp

```ts
withDeletionTimestamp(deletionTimestamp)
```

Time is a wrapper around time.Time which supports correct marshaling to YAML and JSON.  Wrappers are provided for many of the factory methods that the time package offers.

### fn metadata.withFinalizers

```ts
withFinalizers(finalizers)
```

Must be empty before the object is deleted from the registry. Each entry is an identifier for the responsible component that will remove the entry from the list. If the deletionTimestamp of the object is non-nil, entries in this list can only be removed. Finalizers may be processed and removed in any order.  Order is NOT enforced because it introduces significant risk of stuck finalizers. finalizers is a shared field, any actor with permission can reorder it. If the finalizer list is processed in order, then this can lead to a situation in which the component responsible for the first finalizer in the list is waiting for a signal (field value, external system, or other) produced by a component responsible for a finalizer later in the list, resulting in a deadlock. Without enforced ordering finalizers are free to order amongst themselves and are not vulnerable to ordering changes in the list.

### fn metadata.withFinalizersMixin

```ts
withFinalizersMixin(finalizers)
```

Must be empty before the object is deleted from the registry. Each entry is an identifier for the responsible component that will remove the entry from the list. If the deletionTimestamp of the object is non-nil, entries in this list can only be removed. Finalizers may be processed and removed in any order.  Order is NOT enforced because it introduces significant risk of stuck finalizers. finalizers is a shared field, any actor with permission can reorder it. If the finalizer list is processed in order, then this can lead to a situation in which the component responsible for the first finalizer in the list is waiting for a signal (field value, external system, or other) produced by a component responsible for a finalizer later in the list, resulting in a deadlock. Without enforced ordering finalizers are free to order amongst themselves and are not vulnerable to ordering changes in the list.

**Note:** This function appends passed data to existing values

### fn metadata.withGenerateName

```ts
withGenerateName(generateName)
```

GenerateName is an optional prefix, used by the server, to generate a unique name ONLY IF the Name field has not been provided. If this field is used, the name returned to the client will be different than the name passed. This value will also be combined with a unique suffix. The provided value has the same validation rules as the Name field, and may be truncated by the length of the suffix required to make the value unique on the server.

If this field is specified and the generated name exists, the server will NOT return a 409 - instead, it will either return 201 Created or 500 with Reason ServerTimeout indicating a unique name could not be found in the time allotted, and the client should retry (optionally after the time indicated in the Retry-After header).

Applied only if Name is not specified. More info: https://git.k8s.io/community/contributors/devel/sig-architecture/api-conventions.md#idempotency

### fn metadata.withGeneration

```ts
withGeneration(generation)
```

A sequence number representing a specific generation of the desired state. Populated by the system. Read-only.

### fn metadata.withLabels

```ts
withLabels(labels)
```

Map of string keys and values that can be used to organize and categorize (scope and select) objects. May match selectors of replication controllers and services. More info: http://kubernetes.io/docs/user-guide/labels

### fn metadata.withLabelsMixin

```ts
withLabelsMixin(labels)
```

Map of string keys and values that can be used to organize and categorize (scope and select) objects. May match selectors of replication controllers and services. More info: http://kubernetes.io/docs/user-guide/labels

**Note:** This function appends passed data to existing values

### fn metadata.withManagedFields

```ts
withManagedFields(managedFields)
```

ManagedFields maps workflow-id and version to the set of fields that are managed by that workflow. This is mostly for internal housekeeping, and users typically shouldn't need to set or understand this field. A workflow can be the user's name, a controller's name, or the name of a specific apply path like 'ci-cd'. The set of fields is always in the version that the workflow used when modifying the object.

### fn metadata.withManagedFieldsMixin

```ts
withManagedFieldsMixin(managedFields)
```

ManagedFields maps workflow-id and version to the set of fields that are managed by that workflow. This is mostly for internal housekeeping, and users typically shouldn't need to set or understand this field. A workflow can be the user's name, a controller's name, or the name of a specific apply path like 'ci-cd'. The set of fields is always in the version that the workflow used when modifying the object.

**Note:** This function appends passed data to existing values

### fn metadata.withName

```ts
withName(name)
```

Name must be unique within a namespace. Is required when creating resources, although some resources may allow a client to request the generation of an appropriate name automatically. Name is primarily intended for creation idempotence and configuration definition. Cannot be updated. More info: http://kubernetes.io/docs/user-guide/identifiers#names

### fn metadata.withNamespace

```ts
withNamespace(namespace)
```

Namespace defines the space within which each name must be unique. An empty namespace is equivalent to the "default" namespace, but "default" is the canonical representation. Not all objects are required to be scoped to a namespace - the value of this field for those objects will be empty.

Must be a DNS_LABEL. Cannot be updated. More info: http://kubernetes.io/docs/user-guide/namespaces

### fn metadata.withOwnerReferences

```ts
withOwnerReferences(ownerReferences)
```

List of objects depended by this object. If ALL objects in the list have been deleted, this object will be garbage collected. If this object is managed by a controller, then an entry in this list will point to this controller, with the controller field set to true. There cannot be more than one managing controller.

### fn metadata.withOwnerReferencesMixin

```ts
withOwnerReferencesMixin(ownerReferences)
```

List of objects depended by this object. If ALL objects in the list have been deleted, this object will be garbage collected. If this object is managed by a controller, then an entry in this list will point to this controller, with the controller field set to true. There cannot be more than one managing controller.

**Note:** This function appends passed data to existing values

### fn metadata.withResourceVersion

```ts
withResourceVersion(resourceVersion)
```

An opaque value that represents the internal version of this object that can be used by clients to determine when objects have changed. May be used for optimistic concurrency, change detection, and the watch operation on a resource or set of resources. Clients must treat these values as opaque and passed unmodified back to the server. They may only be valid for a particular resource or set of resources.

Populated by the system. Read-only. Value must be treated as opaque by clients and . More info: https://git.k8s.io/community/contributors/devel/sig-architecture/api-conventions.md#concurrency-control-and-consistency

### fn metadata.withSelfLink

```ts
withSelfLink(selfLink)
```

SelfLink is a URL representing this object. Populated by the system. Read-only.

DEPRECATED Kubernetes will stop propagating this field in 1.20 release and the field is planned to be removed in 1.21 release.

### fn metadata.withUid

```ts
withUid(uid)
```

UID is the unique in time and space value for this object. It is typically generated by the server on successful creation of a resource and is not allowed to change on PUT operations.

Populated by the system. Read-only. More info: http://kubernetes.io/docs/user-guide/identifiers#uids

## obj spec

Specification of the desired behavior of the ThanosRuler cluster. More info: https://github.com/kubernetes/community/blob/master/contributors/devel/sig-architecture/api-conventions.md#spec-and-status

### fn spec.withAlertDropLabels

```ts
withAlertDropLabels(alertDropLabels)
```

AlertDropLabels configure the label names which should be dropped in ThanosRuler alerts. If `labels` field is not provided, `thanos_ruler_replica` will be dropped in alerts by default.

### fn spec.withAlertDropLabelsMixin

```ts
withAlertDropLabelsMixin(alertDropLabels)
```

AlertDropLabels configure the label names which should be dropped in ThanosRuler alerts. If `labels` field is not provided, `thanos_ruler_replica` will be dropped in alerts by default.

**Note:** This function appends passed data to existing values

### fn spec.withAlertQueryUrl

```ts
withAlertQueryUrl(alertQueryUrl)
```

The external Query URL the Thanos Ruler will set in the 'Source' field of all alerts. Maps to the '--alert.query-url' CLI arg.

### fn spec.withAlertmanagersUrl

```ts
withAlertmanagersUrl(alertmanagersUrl)
```

Define URLs to send alerts to Alertmanager.  For Thanos v0.10.0 and higher, AlertManagersConfig should be used instead.  Note: this field will be ignored if AlertManagersConfig is specified. Maps to the `alertmanagers.url` arg.

### fn spec.withAlertmanagersUrlMixin

```ts
withAlertmanagersUrlMixin(alertmanagersUrl)
```

Define URLs to send alerts to Alertmanager.  For Thanos v0.10.0 and higher, AlertManagersConfig should be used instead.  Note: this field will be ignored if AlertManagersConfig is specified. Maps to the `alertmanagers.url` arg.

**Note:** This function appends passed data to existing values

### fn spec.withContainers

```ts
withContainers(containers)
```

Containers allows injecting additional containers or modifying operator generated containers. This can be used to allow adding an authentication proxy to a ThanosRuler pod or to change the behavior of an operator generated container. Containers described here modify an operator generated container if they share the same name and modifications are done via a strategic merge patch. The current container names are: `thanos-ruler` and `config-reloader`. Overriding containers is entirely outside the scope of what the maintainers will support and by doing so, you accept that this behaviour may break at any time without notice.

### fn spec.withContainersMixin

```ts
withContainersMixin(containers)
```

Containers allows injecting additional containers or modifying operator generated containers. This can be used to allow adding an authentication proxy to a ThanosRuler pod or to change the behavior of an operator generated container. Containers described here modify an operator generated container if they share the same name and modifications are done via a strategic merge patch. The current container names are: `thanos-ruler` and `config-reloader`. Overriding containers is entirely outside the scope of what the maintainers will support and by doing so, you accept that this behaviour may break at any time without notice.

**Note:** This function appends passed data to existing values

### fn spec.withEnforcedNamespaceLabel

```ts
withEnforcedNamespaceLabel(enforcedNamespaceLabel)
```

EnforcedNamespaceLabel enforces adding a namespace label of origin for each alert and metric that is user created. The label value will always be the namespace of the object that is being created.

### fn spec.withEvaluationInterval

```ts
withEvaluationInterval(evaluationInterval)
```

Interval between consecutive evaluations.

### fn spec.withExternalPrefix

```ts
withExternalPrefix(externalPrefix)
```

The external URL the Thanos Ruler instances will be available under. This is necessary to generate correct URLs. This is necessary if Thanos Ruler is not served from root of a DNS name.

### fn spec.withImage

```ts
withImage(image)
```

Thanos container image URL.

### fn spec.withImagePullSecrets

```ts
withImagePullSecrets(imagePullSecrets)
```

An optional list of references to secrets in the same namespace to use for pulling thanos images from registries see http://kubernetes.io/docs/user-guide/images#specifying-imagepullsecrets-on-a-pod

### fn spec.withImagePullSecretsMixin

```ts
withImagePullSecretsMixin(imagePullSecrets)
```

An optional list of references to secrets in the same namespace to use for pulling thanos images from registries see http://kubernetes.io/docs/user-guide/images#specifying-imagepullsecrets-on-a-pod

**Note:** This function appends passed data to existing values

### fn spec.withInitContainers

```ts
withInitContainers(initContainers)
```

InitContainers allows adding initContainers to the pod definition. Those can be used to e.g. fetch secrets for injection into the ThanosRuler configuration from external sources. Any errors during the execution of an initContainer will lead to a restart of the Pod. More info: https://kubernetes.io/docs/concepts/workloads/pods/init-containers/ Using initContainers for any use case other then secret fetching is entirely outside the scope of what the maintainers will support and by doing so, you accept that this behaviour may break at any time without notice.

### fn spec.withInitContainersMixin

```ts
withInitContainersMixin(initContainers)
```

InitContainers allows adding initContainers to the pod definition. Those can be used to e.g. fetch secrets for injection into the ThanosRuler configuration from external sources. Any errors during the execution of an initContainer will lead to a restart of the Pod. More info: https://kubernetes.io/docs/concepts/workloads/pods/init-containers/ Using initContainers for any use case other then secret fetching is entirely outside the scope of what the maintainers will support and by doing so, you accept that this behaviour may break at any time without notice.

**Note:** This function appends passed data to existing values

### fn spec.withLabels

```ts
withLabels(labels)
```

Labels configure the external label pairs to ThanosRuler. If not provided, default replica label `thanos_ruler_replica` will be added as a label and be dropped in alerts.

### fn spec.withLabelsMixin

```ts
withLabelsMixin(labels)
```

Labels configure the external label pairs to ThanosRuler. If not provided, default replica label `thanos_ruler_replica` will be added as a label and be dropped in alerts.

**Note:** This function appends passed data to existing values

### fn spec.withListenLocal

```ts
withListenLocal(listenLocal)
```

ListenLocal makes the Thanos ruler listen on loopback, so that it does not bind against the Pod IP.

### fn spec.withLogFormat

```ts
withLogFormat(logFormat)
```

Log format for ThanosRuler to be configured with.

### fn spec.withLogLevel

```ts
withLogLevel(logLevel)
```

Log level for ThanosRuler to be configured with.

### fn spec.withNodeSelector

```ts
withNodeSelector(nodeSelector)
```

Define which Nodes the Pods are scheduled on.

### fn spec.withNodeSelectorMixin

```ts
withNodeSelectorMixin(nodeSelector)
```

Define which Nodes the Pods are scheduled on.

**Note:** This function appends passed data to existing values

### fn spec.withObjectStorageConfigFile

```ts
withObjectStorageConfigFile(objectStorageConfigFile)
```

ObjectStorageConfigFile specifies the path of the object storage configuration file. When used alongside with ObjectStorageConfig, ObjectStorageConfigFile takes precedence.

### fn spec.withPaused

```ts
withPaused(paused)
```

When a ThanosRuler deployment is paused, no actions except for deletion will be performed on the underlying objects.

### fn spec.withPortName

```ts
withPortName(portName)
```

Port name used for the pods and governing service. This defaults to web

### fn spec.withPriorityClassName

```ts
withPriorityClassName(priorityClassName)
```

Priority class assigned to the Pods

### fn spec.withPrometheusRulesExcludedFromEnforce

```ts
withPrometheusRulesExcludedFromEnforce(prometheusRulesExcludedFromEnforce)
```

PrometheusRulesExcludedFromEnforce - list of Prometheus rules to be excluded from enforcing of adding namespace labels. Works only if enforcedNamespaceLabel set to true. Make sure both ruleNamespace and ruleName are set for each pair

### fn spec.withPrometheusRulesExcludedFromEnforceMixin

```ts
withPrometheusRulesExcludedFromEnforceMixin(prometheusRulesExcludedFromEnforce)
```

PrometheusRulesExcludedFromEnforce - list of Prometheus rules to be excluded from enforcing of adding namespace labels. Works only if enforcedNamespaceLabel set to true. Make sure both ruleNamespace and ruleName are set for each pair

**Note:** This function appends passed data to existing values

### fn spec.withQueryEndpoints

```ts
withQueryEndpoints(queryEndpoints)
```

QueryEndpoints defines Thanos querier endpoints from which to query metrics. Maps to the --query flag of thanos ruler.

### fn spec.withQueryEndpointsMixin

```ts
withQueryEndpointsMixin(queryEndpoints)
```

QueryEndpoints defines Thanos querier endpoints from which to query metrics. Maps to the --query flag of thanos ruler.

**Note:** This function appends passed data to existing values

### fn spec.withReplicas

```ts
withReplicas(replicas)
```

Number of thanos ruler instances to deploy.

### fn spec.withRetention

```ts
withRetention(retention)
```

Time duration ThanosRuler shall retain data for. Default is '24h', and must match the regular expression `[0-9]+(ms|s|m|h|d|w|y)` (milliseconds seconds minutes hours days weeks years).

### fn spec.withRoutePrefix

```ts
withRoutePrefix(routePrefix)
```

The route prefix ThanosRuler registers HTTP handlers for. This allows thanos UI to be served on a sub-path.

### fn spec.withServiceAccountName

```ts
withServiceAccountName(serviceAccountName)
```

ServiceAccountName is the name of the ServiceAccount to use to run the Thanos Ruler Pods.

### fn spec.withTolerations

```ts
withTolerations(tolerations)
```

If specified, the pod's tolerations.

### fn spec.withTolerationsMixin

```ts
withTolerationsMixin(tolerations)
```

If specified, the pod's tolerations.

**Note:** This function appends passed data to existing values

### fn spec.withTopologySpreadConstraints

```ts
withTopologySpreadConstraints(topologySpreadConstraints)
```

If specified, the pod's topology spread constraints.

### fn spec.withTopologySpreadConstraintsMixin

```ts
withTopologySpreadConstraintsMixin(topologySpreadConstraints)
```

If specified, the pod's topology spread constraints.

**Note:** This function appends passed data to existing values

### fn spec.withVolumes

```ts
withVolumes(volumes)
```

Volumes allows configuration of additional volumes on the output StatefulSet definition. Volumes specified will be appended to other volumes that are generated as a result of StorageSpec objects.

### fn spec.withVolumesMixin

```ts
withVolumesMixin(volumes)
```

Volumes allows configuration of additional volumes on the output StatefulSet definition. Volumes specified will be appended to other volumes that are generated as a result of StorageSpec objects.

**Note:** This function appends passed data to existing values

## obj spec.affinity

If specified, the pod's scheduling constraints.

## obj spec.affinity.nodeAffinity

Describes node affinity scheduling rules for the pod.

### fn spec.affinity.nodeAffinity.withPreferredDuringSchedulingIgnoredDuringExecution

```ts
withPreferredDuringSchedulingIgnoredDuringExecution(preferredDuringSchedulingIgnoredDuringExecution)
```

The scheduler will prefer to schedule pods to nodes that satisfy the affinity expressions specified by this field, but it may choose a node that violates one or more of the expressions. The node that is most preferred is the one with the greatest sum of weights, i.e. for each node that meets all of the scheduling requirements (resource request, requiredDuringScheduling affinity expressions, etc.), compute a sum by iterating through the elements of this field and adding "weight" to the sum if the node matches the corresponding matchExpressions; the node(s) with the highest sum are the most preferred.

### fn spec.affinity.nodeAffinity.withPreferredDuringSchedulingIgnoredDuringExecutionMixin

```ts
withPreferredDuringSchedulingIgnoredDuringExecutionMixin(preferredDuringSchedulingIgnoredDuringExecution)
```

The scheduler will prefer to schedule pods to nodes that satisfy the affinity expressions specified by this field, but it may choose a node that violates one or more of the expressions. The node that is most preferred is the one with the greatest sum of weights, i.e. for each node that meets all of the scheduling requirements (resource request, requiredDuringScheduling affinity expressions, etc.), compute a sum by iterating through the elements of this field and adding "weight" to the sum if the node matches the corresponding matchExpressions; the node(s) with the highest sum are the most preferred.

**Note:** This function appends passed data to existing values

## obj spec.affinity.nodeAffinity.requiredDuringSchedulingIgnoredDuringExecution

If the affinity requirements specified by this field are not met at scheduling time, the pod will not be scheduled onto the node. If the affinity requirements specified by this field cease to be met at some point during pod execution (e.g. due to an update), the system may or may not try to eventually evict the pod from its node.

### fn spec.affinity.nodeAffinity.requiredDuringSchedulingIgnoredDuringExecution.withNodeSelectorTerms

```ts
withNodeSelectorTerms(nodeSelectorTerms)
```

Required. A list of node selector terms. The terms are ORed.

### fn spec.affinity.nodeAffinity.requiredDuringSchedulingIgnoredDuringExecution.withNodeSelectorTermsMixin

```ts
withNodeSelectorTermsMixin(nodeSelectorTerms)
```

Required. A list of node selector terms. The terms are ORed.

**Note:** This function appends passed data to existing values

## obj spec.affinity.podAffinity

Describes pod affinity scheduling rules (e.g. co-locate this pod in the same node, zone, etc. as some other pod(s)).

### fn spec.affinity.podAffinity.withPreferredDuringSchedulingIgnoredDuringExecution

```ts
withPreferredDuringSchedulingIgnoredDuringExecution(preferredDuringSchedulingIgnoredDuringExecution)
```

The scheduler will prefer to schedule pods to nodes that satisfy the affinity expressions specified by this field, but it may choose a node that violates one or more of the expressions. The node that is most preferred is the one with the greatest sum of weights, i.e. for each node that meets all of the scheduling requirements (resource request, requiredDuringScheduling affinity expressions, etc.), compute a sum by iterating through the elements of this field and adding "weight" to the sum if the node has pods which matches the corresponding podAffinityTerm; the node(s) with the highest sum are the most preferred.

### fn spec.affinity.podAffinity.withPreferredDuringSchedulingIgnoredDuringExecutionMixin

```ts
withPreferredDuringSchedulingIgnoredDuringExecutionMixin(preferredDuringSchedulingIgnoredDuringExecution)
```

The scheduler will prefer to schedule pods to nodes that satisfy the affinity expressions specified by this field, but it may choose a node that violates one or more of the expressions. The node that is most preferred is the one with the greatest sum of weights, i.e. for each node that meets all of the scheduling requirements (resource request, requiredDuringScheduling affinity expressions, etc.), compute a sum by iterating through the elements of this field and adding "weight" to the sum if the node has pods which matches the corresponding podAffinityTerm; the node(s) with the highest sum are the most preferred.

**Note:** This function appends passed data to existing values

### fn spec.affinity.podAffinity.withRequiredDuringSchedulingIgnoredDuringExecution

```ts
withRequiredDuringSchedulingIgnoredDuringExecution(requiredDuringSchedulingIgnoredDuringExecution)
```

If the affinity requirements specified by this field are not met at scheduling time, the pod will not be scheduled onto the node. If the affinity requirements specified by this field cease to be met at some point during pod execution (e.g. due to a pod label update), the system may or may not try to eventually evict the pod from its node. When there are multiple elements, the lists of nodes corresponding to each podAffinityTerm are intersected, i.e. all terms must be satisfied.

### fn spec.affinity.podAffinity.withRequiredDuringSchedulingIgnoredDuringExecutionMixin

```ts
withRequiredDuringSchedulingIgnoredDuringExecutionMixin(requiredDuringSchedulingIgnoredDuringExecution)
```

If the affinity requirements specified by this field are not met at scheduling time, the pod will not be scheduled onto the node. If the affinity requirements specified by this field cease to be met at some point during pod execution (e.g. due to a pod label update), the system may or may not try to eventually evict the pod from its node. When there are multiple elements, the lists of nodes corresponding to each podAffinityTerm are intersected, i.e. all terms must be satisfied.

**Note:** This function appends passed data to existing values

## obj spec.affinity.podAntiAffinity

Describes pod anti-affinity scheduling rules (e.g. avoid putting this pod in the same node, zone, etc. as some other pod(s)).

### fn spec.affinity.podAntiAffinity.withPreferredDuringSchedulingIgnoredDuringExecution

```ts
withPreferredDuringSchedulingIgnoredDuringExecution(preferredDuringSchedulingIgnoredDuringExecution)
```

The scheduler will prefer to schedule pods to nodes that satisfy the anti-affinity expressions specified by this field, but it may choose a node that violates one or more of the expressions. The node that is most preferred is the one with the greatest sum of weights, i.e. for each node that meets all of the scheduling requirements (resource request, requiredDuringScheduling anti-affinity expressions, etc.), compute a sum by iterating through the elements of this field and adding "weight" to the sum if the node has pods which matches the corresponding podAffinityTerm; the node(s) with the highest sum are the most preferred.

### fn spec.affinity.podAntiAffinity.withPreferredDuringSchedulingIgnoredDuringExecutionMixin

```ts
withPreferredDuringSchedulingIgnoredDuringExecutionMixin(preferredDuringSchedulingIgnoredDuringExecution)
```

The scheduler will prefer to schedule pods to nodes that satisfy the anti-affinity expressions specified by this field, but it may choose a node that violates one or more of the expressions. The node that is most preferred is the one with the greatest sum of weights, i.e. for each node that meets all of the scheduling requirements (resource request, requiredDuringScheduling anti-affinity expressions, etc.), compute a sum by iterating through the elements of this field and adding "weight" to the sum if the node has pods which matches the corresponding podAffinityTerm; the node(s) with the highest sum are the most preferred.

**Note:** This function appends passed data to existing values

### fn spec.affinity.podAntiAffinity.withRequiredDuringSchedulingIgnoredDuringExecution

```ts
withRequiredDuringSchedulingIgnoredDuringExecution(requiredDuringSchedulingIgnoredDuringExecution)
```

If the anti-affinity requirements specified by this field are not met at scheduling time, the pod will not be scheduled onto the node. If the anti-affinity requirements specified by this field cease to be met at some point during pod execution (e.g. due to a pod label update), the system may or may not try to eventually evict the pod from its node. When there are multiple elements, the lists of nodes corresponding to each podAffinityTerm are intersected, i.e. all terms must be satisfied.

### fn spec.affinity.podAntiAffinity.withRequiredDuringSchedulingIgnoredDuringExecutionMixin

```ts
withRequiredDuringSchedulingIgnoredDuringExecutionMixin(requiredDuringSchedulingIgnoredDuringExecution)
```

If the anti-affinity requirements specified by this field are not met at scheduling time, the pod will not be scheduled onto the node. If the anti-affinity requirements specified by this field cease to be met at some point during pod execution (e.g. due to a pod label update), the system may or may not try to eventually evict the pod from its node. When there are multiple elements, the lists of nodes corresponding to each podAffinityTerm are intersected, i.e. all terms must be satisfied.

**Note:** This function appends passed data to existing values

## obj spec.alertmanagersConfig

Define configuration for connecting to alertmanager.  Only available with thanos v0.10.0 and higher.  Maps to the `alertmanagers.config` arg.

### fn spec.alertmanagersConfig.withKey

```ts
withKey(key)
```

The key of the secret to select from.  Must be a valid secret key.

### fn spec.alertmanagersConfig.withName

```ts
withName(name)
```

Name of the referent. More info: https://kubernetes.io/docs/concepts/overview/working-with-objects/names/#names TODO: Add other useful fields. apiVersion, kind, uid?

### fn spec.alertmanagersConfig.withOptional

```ts
withOptional(optional)
```

Specify whether the Secret or its key must be defined

## obj spec.grpcServerTlsConfig

GRPCServerTLSConfig configures the gRPC server from which Thanos Querier reads recorded rule data. Note: Currently only the CAFile, CertFile, and KeyFile fields are supported. Maps to the '--grpc-server-tls-*' CLI args.

### fn spec.grpcServerTlsConfig.withCaFile

```ts
withCaFile(caFile)
```

Path to the CA cert in the Prometheus container to use for the targets.

### fn spec.grpcServerTlsConfig.withCertFile

```ts
withCertFile(certFile)
```

Path to the client cert file in the Prometheus container for the targets.

### fn spec.grpcServerTlsConfig.withInsecureSkipVerify

```ts
withInsecureSkipVerify(insecureSkipVerify)
```

Disable target certificate validation.

### fn spec.grpcServerTlsConfig.withKeyFile

```ts
withKeyFile(keyFile)
```

Path to the client key file in the Prometheus container for the targets.

### fn spec.grpcServerTlsConfig.withServerName

```ts
withServerName(serverName)
```

Used to verify the hostname for the targets.

## obj spec.grpcServerTlsConfig.ca

Struct containing the CA cert to use for the targets.

## obj spec.grpcServerTlsConfig.ca.configMap

ConfigMap containing data to use for the targets.

### fn spec.grpcServerTlsConfig.ca.configMap.withKey

```ts
withKey(key)
```

The key to select.

### fn spec.grpcServerTlsConfig.ca.configMap.withName

```ts
withName(name)
```

Name of the referent. More info: https://kubernetes.io/docs/concepts/overview/working-with-objects/names/#names TODO: Add other useful fields. apiVersion, kind, uid?

### fn spec.grpcServerTlsConfig.ca.configMap.withOptional

```ts
withOptional(optional)
```

Specify whether the ConfigMap or its key must be defined

## obj spec.grpcServerTlsConfig.ca.secret

Secret containing data to use for the targets.

### fn spec.grpcServerTlsConfig.ca.secret.withKey

```ts
withKey(key)
```

The key of the secret to select from.  Must be a valid secret key.

### fn spec.grpcServerTlsConfig.ca.secret.withName

```ts
withName(name)
```

Name of the referent. More info: https://kubernetes.io/docs/concepts/overview/working-with-objects/names/#names TODO: Add other useful fields. apiVersion, kind, uid?

### fn spec.grpcServerTlsConfig.ca.secret.withOptional

```ts
withOptional(optional)
```

Specify whether the Secret or its key must be defined

## obj spec.grpcServerTlsConfig.cert

Struct containing the client cert file for the targets.

## obj spec.grpcServerTlsConfig.cert.configMap

ConfigMap containing data to use for the targets.

### fn spec.grpcServerTlsConfig.cert.configMap.withKey

```ts
withKey(key)
```

The key to select.

### fn spec.grpcServerTlsConfig.cert.configMap.withName

```ts
withName(name)
```

Name of the referent. More info: https://kubernetes.io/docs/concepts/overview/working-with-objects/names/#names TODO: Add other useful fields. apiVersion, kind, uid?

### fn spec.grpcServerTlsConfig.cert.configMap.withOptional

```ts
withOptional(optional)
```

Specify whether the ConfigMap or its key must be defined

## obj spec.grpcServerTlsConfig.cert.secret

Secret containing data to use for the targets.

### fn spec.grpcServerTlsConfig.cert.secret.withKey

```ts
withKey(key)
```

The key of the secret to select from.  Must be a valid secret key.

### fn spec.grpcServerTlsConfig.cert.secret.withName

```ts
withName(name)
```

Name of the referent. More info: https://kubernetes.io/docs/concepts/overview/working-with-objects/names/#names TODO: Add other useful fields. apiVersion, kind, uid?

### fn spec.grpcServerTlsConfig.cert.secret.withOptional

```ts
withOptional(optional)
```

Specify whether the Secret or its key must be defined

## obj spec.grpcServerTlsConfig.keySecret

Secret containing the client key file for the targets.

### fn spec.grpcServerTlsConfig.keySecret.withKey

```ts
withKey(key)
```

The key of the secret to select from.  Must be a valid secret key.

### fn spec.grpcServerTlsConfig.keySecret.withName

```ts
withName(name)
```

Name of the referent. More info: https://kubernetes.io/docs/concepts/overview/working-with-objects/names/#names TODO: Add other useful fields. apiVersion, kind, uid?

### fn spec.grpcServerTlsConfig.keySecret.withOptional

```ts
withOptional(optional)
```

Specify whether the Secret or its key must be defined

## obj spec.objectStorageConfig

ObjectStorageConfig configures object storage in Thanos. Alternative to ObjectStorageConfigFile, and lower order priority.

### fn spec.objectStorageConfig.withKey

```ts
withKey(key)
```

The key of the secret to select from.  Must be a valid secret key.

### fn spec.objectStorageConfig.withName

```ts
withName(name)
```

Name of the referent. More info: https://kubernetes.io/docs/concepts/overview/working-with-objects/names/#names TODO: Add other useful fields. apiVersion, kind, uid?

### fn spec.objectStorageConfig.withOptional

```ts
withOptional(optional)
```

Specify whether the Secret or its key must be defined

## obj spec.podMetadata

PodMetadata contains Labels and Annotations gets propagated to the thanos ruler pods.

### fn spec.podMetadata.withAnnotations

```ts
withAnnotations(annotations)
```

Annotations is an unstructured key value map stored with a resource that may be set by external tools to store and retrieve arbitrary metadata. They are not queryable and should be preserved when modifying objects. More info: http://kubernetes.io/docs/user-guide/annotations

### fn spec.podMetadata.withAnnotationsMixin

```ts
withAnnotationsMixin(annotations)
```

Annotations is an unstructured key value map stored with a resource that may be set by external tools to store and retrieve arbitrary metadata. They are not queryable and should be preserved when modifying objects. More info: http://kubernetes.io/docs/user-guide/annotations

**Note:** This function appends passed data to existing values

### fn spec.podMetadata.withLabels

```ts
withLabels(labels)
```

Map of string keys and values that can be used to organize and categorize (scope and select) objects. May match selectors of replication controllers and services. More info: http://kubernetes.io/docs/user-guide/labels

### fn spec.podMetadata.withLabelsMixin

```ts
withLabelsMixin(labels)
```

Map of string keys and values that can be used to organize and categorize (scope and select) objects. May match selectors of replication controllers and services. More info: http://kubernetes.io/docs/user-guide/labels

**Note:** This function appends passed data to existing values

### fn spec.podMetadata.withName

```ts
withName(name)
```

Name must be unique within a namespace. Is required when creating resources, although some resources may allow a client to request the generation of an appropriate name automatically. Name is primarily intended for creation idempotence and configuration definition. Cannot be updated. More info: http://kubernetes.io/docs/user-guide/identifiers#names

## obj spec.queryConfig

Define configuration for connecting to thanos query instances. If this is defined, the QueryEndpoints field will be ignored. Maps to the `query.config` CLI argument. Only available with thanos v0.11.0 and higher.

### fn spec.queryConfig.withKey

```ts
withKey(key)
```

The key of the secret to select from.  Must be a valid secret key.

### fn spec.queryConfig.withName

```ts
withName(name)
```

Name of the referent. More info: https://kubernetes.io/docs/concepts/overview/working-with-objects/names/#names TODO: Add other useful fields. apiVersion, kind, uid?

### fn spec.queryConfig.withOptional

```ts
withOptional(optional)
```

Specify whether the Secret or its key must be defined

## obj spec.resources

Resources defines the resource requirements for single Pods. If not provided, no requests/limits will be set

### fn spec.resources.withLimits

```ts
withLimits(limits)
```

Limits describes the maximum amount of compute resources allowed. More info: https://kubernetes.io/docs/concepts/configuration/manage-compute-resources-container/

### fn spec.resources.withLimitsMixin

```ts
withLimitsMixin(limits)
```

Limits describes the maximum amount of compute resources allowed. More info: https://kubernetes.io/docs/concepts/configuration/manage-compute-resources-container/

**Note:** This function appends passed data to existing values

### fn spec.resources.withRequests

```ts
withRequests(requests)
```

Requests describes the minimum amount of compute resources required. If Requests is omitted for a container, it defaults to Limits if that is explicitly specified, otherwise to an implementation-defined value. More info: https://kubernetes.io/docs/concepts/configuration/manage-compute-resources-container/

### fn spec.resources.withRequestsMixin

```ts
withRequestsMixin(requests)
```

Requests describes the minimum amount of compute resources required. If Requests is omitted for a container, it defaults to Limits if that is explicitly specified, otherwise to an implementation-defined value. More info: https://kubernetes.io/docs/concepts/configuration/manage-compute-resources-container/

**Note:** This function appends passed data to existing values

## obj spec.ruleNamespaceSelector

Namespaces to be selected for Rules discovery. If unspecified, only the same namespace as the ThanosRuler object is in is used.

### fn spec.ruleNamespaceSelector.withMatchExpressions

```ts
withMatchExpressions(matchExpressions)
```

matchExpressions is a list of label selector requirements. The requirements are ANDed.

### fn spec.ruleNamespaceSelector.withMatchExpressionsMixin

```ts
withMatchExpressionsMixin(matchExpressions)
```

matchExpressions is a list of label selector requirements. The requirements are ANDed.

**Note:** This function appends passed data to existing values

### fn spec.ruleNamespaceSelector.withMatchLabels

```ts
withMatchLabels(matchLabels)
```

matchLabels is a map of {key,value} pairs. A single {key,value} in the matchLabels map is equivalent to an element of matchExpressions, whose key field is "key", the operator is "In", and the values array contains only "value". The requirements are ANDed.

### fn spec.ruleNamespaceSelector.withMatchLabelsMixin

```ts
withMatchLabelsMixin(matchLabels)
```

matchLabels is a map of {key,value} pairs. A single {key,value} in the matchLabels map is equivalent to an element of matchExpressions, whose key field is "key", the operator is "In", and the values array contains only "value". The requirements are ANDed.

**Note:** This function appends passed data to existing values

## obj spec.ruleSelector

A label selector to select which PrometheusRules to mount for alerting and recording.

### fn spec.ruleSelector.withMatchExpressions

```ts
withMatchExpressions(matchExpressions)
```

matchExpressions is a list of label selector requirements. The requirements are ANDed.

### fn spec.ruleSelector.withMatchExpressionsMixin

```ts
withMatchExpressionsMixin(matchExpressions)
```

matchExpressions is a list of label selector requirements. The requirements are ANDed.

**Note:** This function appends passed data to existing values

### fn spec.ruleSelector.withMatchLabels

```ts
withMatchLabels(matchLabels)
```

matchLabels is a map of {key,value} pairs. A single {key,value} in the matchLabels map is equivalent to an element of matchExpressions, whose key field is "key", the operator is "In", and the values array contains only "value". The requirements are ANDed.

### fn spec.ruleSelector.withMatchLabelsMixin

```ts
withMatchLabelsMixin(matchLabels)
```

matchLabels is a map of {key,value} pairs. A single {key,value} in the matchLabels map is equivalent to an element of matchExpressions, whose key field is "key", the operator is "In", and the values array contains only "value". The requirements are ANDed.

**Note:** This function appends passed data to existing values

## obj spec.securityContext

SecurityContext holds pod-level security attributes and common container settings. This defaults to the default PodSecurityContext.

### fn spec.securityContext.withFsGroup

```ts
withFsGroup(fsGroup)
```

A special supplemental group that applies to all containers in a pod. Some volume types allow the Kubelet to change the ownership of that volume to be owned by the pod: 
 1. The owning GID will be the FSGroup 2. The setgid bit is set (new files created in the volume will be owned by FSGroup) 3. The permission bits are OR'd with rw-rw---- 
 If unset, the Kubelet will not modify the ownership and permissions of any volume.

### fn spec.securityContext.withFsGroupChangePolicy

```ts
withFsGroupChangePolicy(fsGroupChangePolicy)
```

fsGroupChangePolicy defines behavior of changing ownership and permission of the volume before being exposed inside Pod. This field will only apply to volume types which support fsGroup based ownership(and permissions). It will have no effect on ephemeral volume types such as: secret, configmaps and emptydir. Valid values are "OnRootMismatch" and "Always". If not specified defaults to "Always".

### fn spec.securityContext.withRunAsGroup

```ts
withRunAsGroup(runAsGroup)
```

The GID to run the entrypoint of the container process. Uses runtime default if unset. May also be set in SecurityContext.  If set in both SecurityContext and PodSecurityContext, the value specified in SecurityContext takes precedence for that container.

### fn spec.securityContext.withRunAsNonRoot

```ts
withRunAsNonRoot(runAsNonRoot)
```

Indicates that the container must run as a non-root user. If true, the Kubelet will validate the image at runtime to ensure that it does not run as UID 0 (root) and fail to start the container if it does. If unset or false, no such validation will be performed. May also be set in SecurityContext.  If set in both SecurityContext and PodSecurityContext, the value specified in SecurityContext takes precedence.

### fn spec.securityContext.withRunAsUser

```ts
withRunAsUser(runAsUser)
```

The UID to run the entrypoint of the container process. Defaults to user specified in image metadata if unspecified. May also be set in SecurityContext.  If set in both SecurityContext and PodSecurityContext, the value specified in SecurityContext takes precedence for that container.

### fn spec.securityContext.withSupplementalGroups

```ts
withSupplementalGroups(supplementalGroups)
```

A list of groups applied to the first process run in each container, in addition to the container's primary GID.  If unspecified, no groups will be added to any container.

### fn spec.securityContext.withSupplementalGroupsMixin

```ts
withSupplementalGroupsMixin(supplementalGroups)
```

A list of groups applied to the first process run in each container, in addition to the container's primary GID.  If unspecified, no groups will be added to any container.

**Note:** This function appends passed data to existing values

### fn spec.securityContext.withSysctls

```ts
withSysctls(sysctls)
```

Sysctls hold a list of namespaced sysctls used for the pod. Pods with unsupported sysctls (by the container runtime) might fail to launch.

### fn spec.securityContext.withSysctlsMixin

```ts
withSysctlsMixin(sysctls)
```

Sysctls hold a list of namespaced sysctls used for the pod. Pods with unsupported sysctls (by the container runtime) might fail to launch.

**Note:** This function appends passed data to existing values

## obj spec.securityContext.seLinuxOptions

The SELinux context to be applied to all containers. If unspecified, the container runtime will allocate a random SELinux context for each container.  May also be set in SecurityContext.  If set in both SecurityContext and PodSecurityContext, the value specified in SecurityContext takes precedence for that container.

### fn spec.securityContext.seLinuxOptions.withLevel

```ts
withLevel(level)
```

Level is SELinux level label that applies to the container.

### fn spec.securityContext.seLinuxOptions.withRole

```ts
withRole(role)
```

Role is a SELinux role label that applies to the container.

### fn spec.securityContext.seLinuxOptions.withType

```ts
withType(type)
```

Type is a SELinux type label that applies to the container.

### fn spec.securityContext.seLinuxOptions.withUser

```ts
withUser(user)
```

User is a SELinux user label that applies to the container.

## obj spec.securityContext.windowsOptions

The Windows specific settings applied to all containers. If unspecified, the options within a container's SecurityContext will be used. If set in both SecurityContext and PodSecurityContext, the value specified in SecurityContext takes precedence.

### fn spec.securityContext.windowsOptions.withGmsaCredentialSpec

```ts
withGmsaCredentialSpec(gmsaCredentialSpec)
```

GMSACredentialSpec is where the GMSA admission webhook (https://github.com/kubernetes-sigs/windows-gmsa) inlines the contents of the GMSA credential spec named by the GMSACredentialSpecName field.

### fn spec.securityContext.windowsOptions.withGmsaCredentialSpecName

```ts
withGmsaCredentialSpecName(gmsaCredentialSpecName)
```

GMSACredentialSpecName is the name of the GMSA credential spec to use.

### fn spec.securityContext.windowsOptions.withRunAsUserName

```ts
withRunAsUserName(runAsUserName)
```

The UserName in Windows to run the entrypoint of the container process. Defaults to the user specified in image metadata if unspecified. May also be set in PodSecurityContext. If set in both SecurityContext and PodSecurityContext, the value specified in SecurityContext takes precedence.

## obj spec.storage

Storage spec to specify how storage shall be used.

### fn spec.storage.withDisableMountSubPath

```ts
withDisableMountSubPath(disableMountSubPath)
```

Deprecated: subPath usage will be disabled by default in a future release, this option will become unnecessary. DisableMountSubPath allows to remove any subPath usage in volume mounts.

## obj spec.storage.emptyDir

EmptyDirVolumeSource to be used by the Prometheus StatefulSets. If specified, used in place of any volumeClaimTemplate. More info: https://kubernetes.io/docs/concepts/storage/volumes/#emptydir

### fn spec.storage.emptyDir.withMedium

```ts
withMedium(medium)
```

What type of storage medium should back this directory. The default is '' which means to use the node's default medium. Must be an empty string (default) or Memory. More info: https://kubernetes.io/docs/concepts/storage/volumes#emptydir

### fn spec.storage.emptyDir.withSizeLimit

```ts
withSizeLimit(sizeLimit)
```

Total amount of local storage required for this EmptyDir volume. The size limit is also applicable for memory medium. The maximum usage on memory medium EmptyDir would be the minimum value between the SizeLimit specified here and the sum of memory limits of all containers in a pod. The default is nil which means that the limit is undefined. More info: http://kubernetes.io/docs/user-guide/volumes#emptydir

## obj spec.storage.volumeClaimTemplate

A PVC spec to be used by the Prometheus StatefulSets.

### fn spec.storage.volumeClaimTemplate.withApiVersion

```ts
withApiVersion(apiVersion)
```

APIVersion defines the versioned schema of this representation of an object. Servers should convert recognized schemas to the latest internal value, and may reject unrecognized values. More info: https://git.k8s.io/community/contributors/devel/sig-architecture/api-conventions.md#resources

### fn spec.storage.volumeClaimTemplate.withKind

```ts
withKind(kind)
```

Kind is a string value representing the REST resource this object represents. Servers may infer this from the endpoint the client submits requests to. Cannot be updated. In CamelCase. More info: https://git.k8s.io/community/contributors/devel/sig-architecture/api-conventions.md#types-kinds

## obj spec.storage.volumeClaimTemplate.metadata

EmbeddedMetadata contains metadata relevant to an EmbeddedResource.

### fn spec.storage.volumeClaimTemplate.metadata.withAnnotations

```ts
withAnnotations(annotations)
```

Annotations is an unstructured key value map stored with a resource that may be set by external tools to store and retrieve arbitrary metadata. They are not queryable and should be preserved when modifying objects. More info: http://kubernetes.io/docs/user-guide/annotations

### fn spec.storage.volumeClaimTemplate.metadata.withAnnotationsMixin

```ts
withAnnotationsMixin(annotations)
```

Annotations is an unstructured key value map stored with a resource that may be set by external tools to store and retrieve arbitrary metadata. They are not queryable and should be preserved when modifying objects. More info: http://kubernetes.io/docs/user-guide/annotations

**Note:** This function appends passed data to existing values

### fn spec.storage.volumeClaimTemplate.metadata.withLabels

```ts
withLabels(labels)
```

Map of string keys and values that can be used to organize and categorize (scope and select) objects. May match selectors of replication controllers and services. More info: http://kubernetes.io/docs/user-guide/labels

### fn spec.storage.volumeClaimTemplate.metadata.withLabelsMixin

```ts
withLabelsMixin(labels)
```

Map of string keys and values that can be used to organize and categorize (scope and select) objects. May match selectors of replication controllers and services. More info: http://kubernetes.io/docs/user-guide/labels

**Note:** This function appends passed data to existing values

### fn spec.storage.volumeClaimTemplate.metadata.withName

```ts
withName(name)
```

Name must be unique within a namespace. Is required when creating resources, although some resources may allow a client to request the generation of an appropriate name automatically. Name is primarily intended for creation idempotence and configuration definition. Cannot be updated. More info: http://kubernetes.io/docs/user-guide/identifiers#names

## obj spec.storage.volumeClaimTemplate.spec

Spec defines the desired characteristics of a volume requested by a pod author. More info: https://kubernetes.io/docs/concepts/storage/persistent-volumes#persistentvolumeclaims

### fn spec.storage.volumeClaimTemplate.spec.withAccessModes

```ts
withAccessModes(accessModes)
```

AccessModes contains the desired access modes the volume should have. More info: https://kubernetes.io/docs/concepts/storage/persistent-volumes#access-modes-1

### fn spec.storage.volumeClaimTemplate.spec.withAccessModesMixin

```ts
withAccessModesMixin(accessModes)
```

AccessModes contains the desired access modes the volume should have. More info: https://kubernetes.io/docs/concepts/storage/persistent-volumes#access-modes-1

**Note:** This function appends passed data to existing values

### fn spec.storage.volumeClaimTemplate.spec.withStorageClassName

```ts
withStorageClassName(storageClassName)
```

Name of the StorageClass required by the claim. More info: https://kubernetes.io/docs/concepts/storage/persistent-volumes#class-1

### fn spec.storage.volumeClaimTemplate.spec.withVolumeMode

```ts
withVolumeMode(volumeMode)
```

volumeMode defines what type of volume is required by the claim. Value of Filesystem is implied when not included in claim spec.

### fn spec.storage.volumeClaimTemplate.spec.withVolumeName

```ts
withVolumeName(volumeName)
```

VolumeName is the binding reference to the PersistentVolume backing this claim.

## obj spec.storage.volumeClaimTemplate.spec.dataSource

This field can be used to specify either: * An existing VolumeSnapshot object (snapshot.storage.k8s.io/VolumeSnapshot - Beta) * An existing PVC (PersistentVolumeClaim) * An existing custom resource/object that implements data population (Alpha) In order to use VolumeSnapshot object types, the appropriate feature gate must be enabled (VolumeSnapshotDataSource or AnyVolumeDataSource) If the provisioner or an external controller can support the specified data source, it will create a new volume based on the contents of the specified data source. If the specified data source is not supported, the volume will not be created and the failure will be reported as an event. In the future, we plan to support more data source types and the behavior of the provisioner may change.

### fn spec.storage.volumeClaimTemplate.spec.dataSource.withApiGroup

```ts
withApiGroup(apiGroup)
```

APIGroup is the group for the resource being referenced. If APIGroup is not specified, the specified Kind must be in the core API group. For any other third-party types, APIGroup is required.

### fn spec.storage.volumeClaimTemplate.spec.dataSource.withKind

```ts
withKind(kind)
```

Kind is the type of resource being referenced

### fn spec.storage.volumeClaimTemplate.spec.dataSource.withName

```ts
withName(name)
```

Name is the name of resource being referenced

## obj spec.storage.volumeClaimTemplate.spec.resources

Resources represents the minimum resources the volume should have. More info: https://kubernetes.io/docs/concepts/storage/persistent-volumes#resources

### fn spec.storage.volumeClaimTemplate.spec.resources.withLimits

```ts
withLimits(limits)
```

Limits describes the maximum amount of compute resources allowed. More info: https://kubernetes.io/docs/concepts/configuration/manage-compute-resources-container/

### fn spec.storage.volumeClaimTemplate.spec.resources.withLimitsMixin

```ts
withLimitsMixin(limits)
```

Limits describes the maximum amount of compute resources allowed. More info: https://kubernetes.io/docs/concepts/configuration/manage-compute-resources-container/

**Note:** This function appends passed data to existing values

### fn spec.storage.volumeClaimTemplate.spec.resources.withRequests

```ts
withRequests(requests)
```

Requests describes the minimum amount of compute resources required. If Requests is omitted for a container, it defaults to Limits if that is explicitly specified, otherwise to an implementation-defined value. More info: https://kubernetes.io/docs/concepts/configuration/manage-compute-resources-container/

### fn spec.storage.volumeClaimTemplate.spec.resources.withRequestsMixin

```ts
withRequestsMixin(requests)
```

Requests describes the minimum amount of compute resources required. If Requests is omitted for a container, it defaults to Limits if that is explicitly specified, otherwise to an implementation-defined value. More info: https://kubernetes.io/docs/concepts/configuration/manage-compute-resources-container/

**Note:** This function appends passed data to existing values

## obj spec.storage.volumeClaimTemplate.spec.selector

A label query over volumes to consider for binding.

### fn spec.storage.volumeClaimTemplate.spec.selector.withMatchExpressions

```ts
withMatchExpressions(matchExpressions)
```

matchExpressions is a list of label selector requirements. The requirements are ANDed.

### fn spec.storage.volumeClaimTemplate.spec.selector.withMatchExpressionsMixin

```ts
withMatchExpressionsMixin(matchExpressions)
```

matchExpressions is a list of label selector requirements. The requirements are ANDed.

**Note:** This function appends passed data to existing values

### fn spec.storage.volumeClaimTemplate.spec.selector.withMatchLabels

```ts
withMatchLabels(matchLabels)
```

matchLabels is a map of {key,value} pairs. A single {key,value} in the matchLabels map is equivalent to an element of matchExpressions, whose key field is "key", the operator is "In", and the values array contains only "value". The requirements are ANDed.

### fn spec.storage.volumeClaimTemplate.spec.selector.withMatchLabelsMixin

```ts
withMatchLabelsMixin(matchLabels)
```

matchLabels is a map of {key,value} pairs. A single {key,value} in the matchLabels map is equivalent to an element of matchExpressions, whose key field is "key", the operator is "In", and the values array contains only "value". The requirements are ANDed.

**Note:** This function appends passed data to existing values

## obj spec.tracingConfig

TracingConfig configures tracing in Thanos. This is an experimental feature, it may change in any upcoming release in a breaking way.

### fn spec.tracingConfig.withKey

```ts
withKey(key)
```

The key of the secret to select from.  Must be a valid secret key.

### fn spec.tracingConfig.withName

```ts
withName(name)
```

Name of the referent. More info: https://kubernetes.io/docs/concepts/overview/working-with-objects/names/#names TODO: Add other useful fields. apiVersion, kind, uid?

### fn spec.tracingConfig.withOptional

```ts
withOptional(optional)
```

Specify whether the Secret or its key must be defined