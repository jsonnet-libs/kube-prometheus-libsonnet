---
permalink: /0.8/monitoring/v1/prometheus/
---

# monitoring.v1.prometheus

Prometheus defines a Prometheus deployment.

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
  * [`fn withAllowOverlappingBlocks(allowOverlappingBlocks)`](#fn-specwithallowoverlappingblocks)
  * [`fn withBaseImage(baseImage)`](#fn-specwithbaseimage)
  * [`fn withConfigMaps(configMaps)`](#fn-specwithconfigmaps)
  * [`fn withConfigMapsMixin(configMaps)`](#fn-specwithconfigmapsmixin)
  * [`fn withContainers(containers)`](#fn-specwithcontainers)
  * [`fn withContainersMixin(containers)`](#fn-specwithcontainersmixin)
  * [`fn withDisableCompaction(disableCompaction)`](#fn-specwithdisablecompaction)
  * [`fn withEnableAdminAPI(enableAdminAPI)`](#fn-specwithenableadminapi)
  * [`fn withEnableFeatures(enableFeatures)`](#fn-specwithenablefeatures)
  * [`fn withEnableFeaturesMixin(enableFeatures)`](#fn-specwithenablefeaturesmixin)
  * [`fn withEnforcedNamespaceLabel(enforcedNamespaceLabel)`](#fn-specwithenforcednamespacelabel)
  * [`fn withEnforcedSampleLimit(enforcedSampleLimit)`](#fn-specwithenforcedsamplelimit)
  * [`fn withEnforcedTargetLimit(enforcedTargetLimit)`](#fn-specwithenforcedtargetlimit)
  * [`fn withEvaluationInterval(evaluationInterval)`](#fn-specwithevaluationinterval)
  * [`fn withExternalLabels(externalLabels)`](#fn-specwithexternallabels)
  * [`fn withExternalLabelsMixin(externalLabels)`](#fn-specwithexternallabelsmixin)
  * [`fn withExternalUrl(externalUrl)`](#fn-specwithexternalurl)
  * [`fn withIgnoreNamespaceSelectors(ignoreNamespaceSelectors)`](#fn-specwithignorenamespaceselectors)
  * [`fn withImage(image)`](#fn-specwithimage)
  * [`fn withImagePullSecrets(imagePullSecrets)`](#fn-specwithimagepullsecrets)
  * [`fn withImagePullSecretsMixin(imagePullSecrets)`](#fn-specwithimagepullsecretsmixin)
  * [`fn withInitContainers(initContainers)`](#fn-specwithinitcontainers)
  * [`fn withInitContainersMixin(initContainers)`](#fn-specwithinitcontainersmixin)
  * [`fn withListenLocal(listenLocal)`](#fn-specwithlistenlocal)
  * [`fn withLogFormat(logFormat)`](#fn-specwithlogformat)
  * [`fn withLogLevel(logLevel)`](#fn-specwithloglevel)
  * [`fn withNodeSelector(nodeSelector)`](#fn-specwithnodeselector)
  * [`fn withNodeSelectorMixin(nodeSelector)`](#fn-specwithnodeselectormixin)
  * [`fn withOverrideHonorLabels(overrideHonorLabels)`](#fn-specwithoverridehonorlabels)
  * [`fn withOverrideHonorTimestamps(overrideHonorTimestamps)`](#fn-specwithoverridehonortimestamps)
  * [`fn withPaused(paused)`](#fn-specwithpaused)
  * [`fn withPortName(portName)`](#fn-specwithportname)
  * [`fn withPriorityClassName(priorityClassName)`](#fn-specwithpriorityclassname)
  * [`fn withPrometheusExternalLabelName(prometheusExternalLabelName)`](#fn-specwithprometheusexternallabelname)
  * [`fn withPrometheusRulesExcludedFromEnforce(prometheusRulesExcludedFromEnforce)`](#fn-specwithprometheusrulesexcludedfromenforce)
  * [`fn withPrometheusRulesExcludedFromEnforceMixin(prometheusRulesExcludedFromEnforce)`](#fn-specwithprometheusrulesexcludedfromenforcemixin)
  * [`fn withQueryLogFile(queryLogFile)`](#fn-specwithquerylogfile)
  * [`fn withRemoteRead(remoteRead)`](#fn-specwithremoteread)
  * [`fn withRemoteReadMixin(remoteRead)`](#fn-specwithremotereadmixin)
  * [`fn withRemoteWrite(remoteWrite)`](#fn-specwithremotewrite)
  * [`fn withRemoteWriteMixin(remoteWrite)`](#fn-specwithremotewritemixin)
  * [`fn withReplicaExternalLabelName(replicaExternalLabelName)`](#fn-specwithreplicaexternallabelname)
  * [`fn withReplicas(replicas)`](#fn-specwithreplicas)
  * [`fn withRetention(retention)`](#fn-specwithretention)
  * [`fn withRetentionSize(retentionSize)`](#fn-specwithretentionsize)
  * [`fn withRoutePrefix(routePrefix)`](#fn-specwithrouteprefix)
  * [`fn withScrapeInterval(scrapeInterval)`](#fn-specwithscrapeinterval)
  * [`fn withScrapeTimeout(scrapeTimeout)`](#fn-specwithscrapetimeout)
  * [`fn withSecrets(secrets)`](#fn-specwithsecrets)
  * [`fn withSecretsMixin(secrets)`](#fn-specwithsecretsmixin)
  * [`fn withServiceAccountName(serviceAccountName)`](#fn-specwithserviceaccountname)
  * [`fn withSha(sha)`](#fn-specwithsha)
  * [`fn withShards(shards)`](#fn-specwithshards)
  * [`fn withTag(tag)`](#fn-specwithtag)
  * [`fn withTolerations(tolerations)`](#fn-specwithtolerations)
  * [`fn withTolerationsMixin(tolerations)`](#fn-specwithtolerationsmixin)
  * [`fn withTopologySpreadConstraints(topologySpreadConstraints)`](#fn-specwithtopologyspreadconstraints)
  * [`fn withTopologySpreadConstraintsMixin(topologySpreadConstraints)`](#fn-specwithtopologyspreadconstraintsmixin)
  * [`fn withVersion(version)`](#fn-specwithversion)
  * [`fn withVolumeMounts(volumeMounts)`](#fn-specwithvolumemounts)
  * [`fn withVolumeMountsMixin(volumeMounts)`](#fn-specwithvolumemountsmixin)
  * [`fn withVolumes(volumes)`](#fn-specwithvolumes)
  * [`fn withVolumesMixin(volumes)`](#fn-specwithvolumesmixin)
  * [`fn withWalCompression(walCompression)`](#fn-specwithwalcompression)
  * [`obj spec.additionalAlertManagerConfigs`](#obj-specadditionalalertmanagerconfigs)
    * [`fn withKey(key)`](#fn-specadditionalalertmanagerconfigswithkey)
    * [`fn withName(name)`](#fn-specadditionalalertmanagerconfigswithname)
    * [`fn withOptional(optional)`](#fn-specadditionalalertmanagerconfigswithoptional)
  * [`obj spec.additionalAlertRelabelConfigs`](#obj-specadditionalalertrelabelconfigs)
    * [`fn withKey(key)`](#fn-specadditionalalertrelabelconfigswithkey)
    * [`fn withName(name)`](#fn-specadditionalalertrelabelconfigswithname)
    * [`fn withOptional(optional)`](#fn-specadditionalalertrelabelconfigswithoptional)
  * [`obj spec.additionalScrapeConfigs`](#obj-specadditionalscrapeconfigs)
    * [`fn withKey(key)`](#fn-specadditionalscrapeconfigswithkey)
    * [`fn withName(name)`](#fn-specadditionalscrapeconfigswithname)
    * [`fn withOptional(optional)`](#fn-specadditionalscrapeconfigswithoptional)
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
  * [`obj spec.alerting`](#obj-specalerting)
    * [`fn withAlertmanagers(alertmanagers)`](#fn-specalertingwithalertmanagers)
    * [`fn withAlertmanagersMixin(alertmanagers)`](#fn-specalertingwithalertmanagersmixin)
  * [`obj spec.apiserverConfig`](#obj-specapiserverconfig)
    * [`fn withBearerToken(bearerToken)`](#fn-specapiserverconfigwithbearertoken)
    * [`fn withBearerTokenFile(bearerTokenFile)`](#fn-specapiserverconfigwithbearertokenfile)
    * [`fn withHost(host)`](#fn-specapiserverconfigwithhost)
    * [`obj spec.apiserverConfig.basicAuth`](#obj-specapiserverconfigbasicauth)
      * [`obj spec.apiserverConfig.basicAuth.password`](#obj-specapiserverconfigbasicauthpassword)
        * [`fn withKey(key)`](#fn-specapiserverconfigbasicauthpasswordwithkey)
        * [`fn withName(name)`](#fn-specapiserverconfigbasicauthpasswordwithname)
        * [`fn withOptional(optional)`](#fn-specapiserverconfigbasicauthpasswordwithoptional)
      * [`obj spec.apiserverConfig.basicAuth.username`](#obj-specapiserverconfigbasicauthusername)
        * [`fn withKey(key)`](#fn-specapiserverconfigbasicauthusernamewithkey)
        * [`fn withName(name)`](#fn-specapiserverconfigbasicauthusernamewithname)
        * [`fn withOptional(optional)`](#fn-specapiserverconfigbasicauthusernamewithoptional)
    * [`obj spec.apiserverConfig.tlsConfig`](#obj-specapiserverconfigtlsconfig)
      * [`fn withCaFile(caFile)`](#fn-specapiserverconfigtlsconfigwithcafile)
      * [`fn withCertFile(certFile)`](#fn-specapiserverconfigtlsconfigwithcertfile)
      * [`fn withInsecureSkipVerify(insecureSkipVerify)`](#fn-specapiserverconfigtlsconfigwithinsecureskipverify)
      * [`fn withKeyFile(keyFile)`](#fn-specapiserverconfigtlsconfigwithkeyfile)
      * [`fn withServerName(serverName)`](#fn-specapiserverconfigtlsconfigwithservername)
      * [`obj spec.apiserverConfig.tlsConfig.ca`](#obj-specapiserverconfigtlsconfigca)
        * [`obj spec.apiserverConfig.tlsConfig.ca.configMap`](#obj-specapiserverconfigtlsconfigcaconfigmap)
          * [`fn withKey(key)`](#fn-specapiserverconfigtlsconfigcaconfigmapwithkey)
          * [`fn withName(name)`](#fn-specapiserverconfigtlsconfigcaconfigmapwithname)
          * [`fn withOptional(optional)`](#fn-specapiserverconfigtlsconfigcaconfigmapwithoptional)
        * [`obj spec.apiserverConfig.tlsConfig.ca.secret`](#obj-specapiserverconfigtlsconfigcasecret)
          * [`fn withKey(key)`](#fn-specapiserverconfigtlsconfigcasecretwithkey)
          * [`fn withName(name)`](#fn-specapiserverconfigtlsconfigcasecretwithname)
          * [`fn withOptional(optional)`](#fn-specapiserverconfigtlsconfigcasecretwithoptional)
      * [`obj spec.apiserverConfig.tlsConfig.cert`](#obj-specapiserverconfigtlsconfigcert)
        * [`obj spec.apiserverConfig.tlsConfig.cert.configMap`](#obj-specapiserverconfigtlsconfigcertconfigmap)
          * [`fn withKey(key)`](#fn-specapiserverconfigtlsconfigcertconfigmapwithkey)
          * [`fn withName(name)`](#fn-specapiserverconfigtlsconfigcertconfigmapwithname)
          * [`fn withOptional(optional)`](#fn-specapiserverconfigtlsconfigcertconfigmapwithoptional)
        * [`obj spec.apiserverConfig.tlsConfig.cert.secret`](#obj-specapiserverconfigtlsconfigcertsecret)
          * [`fn withKey(key)`](#fn-specapiserverconfigtlsconfigcertsecretwithkey)
          * [`fn withName(name)`](#fn-specapiserverconfigtlsconfigcertsecretwithname)
          * [`fn withOptional(optional)`](#fn-specapiserverconfigtlsconfigcertsecretwithoptional)
      * [`obj spec.apiserverConfig.tlsConfig.keySecret`](#obj-specapiserverconfigtlsconfigkeysecret)
        * [`fn withKey(key)`](#fn-specapiserverconfigtlsconfigkeysecretwithkey)
        * [`fn withName(name)`](#fn-specapiserverconfigtlsconfigkeysecretwithname)
        * [`fn withOptional(optional)`](#fn-specapiserverconfigtlsconfigkeysecretwithoptional)
  * [`obj spec.arbitraryFSAccessThroughSMs`](#obj-specarbitraryfsaccessthroughsms)
    * [`fn withDeny(deny)`](#fn-specarbitraryfsaccessthroughsmswithdeny)
  * [`obj spec.podMetadata`](#obj-specpodmetadata)
    * [`fn withAnnotations(annotations)`](#fn-specpodmetadatawithannotations)
    * [`fn withAnnotationsMixin(annotations)`](#fn-specpodmetadatawithannotationsmixin)
    * [`fn withLabels(labels)`](#fn-specpodmetadatawithlabels)
    * [`fn withLabelsMixin(labels)`](#fn-specpodmetadatawithlabelsmixin)
    * [`fn withName(name)`](#fn-specpodmetadatawithname)
  * [`obj spec.podMonitorNamespaceSelector`](#obj-specpodmonitornamespaceselector)
    * [`fn withMatchExpressions(matchExpressions)`](#fn-specpodmonitornamespaceselectorwithmatchexpressions)
    * [`fn withMatchExpressionsMixin(matchExpressions)`](#fn-specpodmonitornamespaceselectorwithmatchexpressionsmixin)
    * [`fn withMatchLabels(matchLabels)`](#fn-specpodmonitornamespaceselectorwithmatchlabels)
    * [`fn withMatchLabelsMixin(matchLabels)`](#fn-specpodmonitornamespaceselectorwithmatchlabelsmixin)
  * [`obj spec.podMonitorSelector`](#obj-specpodmonitorselector)
    * [`fn withMatchExpressions(matchExpressions)`](#fn-specpodmonitorselectorwithmatchexpressions)
    * [`fn withMatchExpressionsMixin(matchExpressions)`](#fn-specpodmonitorselectorwithmatchexpressionsmixin)
    * [`fn withMatchLabels(matchLabels)`](#fn-specpodmonitorselectorwithmatchlabels)
    * [`fn withMatchLabelsMixin(matchLabels)`](#fn-specpodmonitorselectorwithmatchlabelsmixin)
  * [`obj spec.probeNamespaceSelector`](#obj-specprobenamespaceselector)
    * [`fn withMatchExpressions(matchExpressions)`](#fn-specprobenamespaceselectorwithmatchexpressions)
    * [`fn withMatchExpressionsMixin(matchExpressions)`](#fn-specprobenamespaceselectorwithmatchexpressionsmixin)
    * [`fn withMatchLabels(matchLabels)`](#fn-specprobenamespaceselectorwithmatchlabels)
    * [`fn withMatchLabelsMixin(matchLabels)`](#fn-specprobenamespaceselectorwithmatchlabelsmixin)
  * [`obj spec.probeSelector`](#obj-specprobeselector)
    * [`fn withMatchExpressions(matchExpressions)`](#fn-specprobeselectorwithmatchexpressions)
    * [`fn withMatchExpressionsMixin(matchExpressions)`](#fn-specprobeselectorwithmatchexpressionsmixin)
    * [`fn withMatchLabels(matchLabels)`](#fn-specprobeselectorwithmatchlabels)
    * [`fn withMatchLabelsMixin(matchLabels)`](#fn-specprobeselectorwithmatchlabelsmixin)
  * [`obj spec.query`](#obj-specquery)
    * [`fn withLookbackDelta(lookbackDelta)`](#fn-specquerywithlookbackdelta)
    * [`fn withMaxConcurrency(maxConcurrency)`](#fn-specquerywithmaxconcurrency)
    * [`fn withMaxSamples(maxSamples)`](#fn-specquerywithmaxsamples)
    * [`fn withTimeout(timeout)`](#fn-specquerywithtimeout)
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
  * [`obj spec.rules`](#obj-specrules)
    * [`obj spec.rules.alert`](#obj-specrulesalert)
      * [`fn withForGracePeriod(forGracePeriod)`](#fn-specrulesalertwithforgraceperiod)
      * [`fn withForOutageTolerance(forOutageTolerance)`](#fn-specrulesalertwithforoutagetolerance)
      * [`fn withResendDelay(resendDelay)`](#fn-specrulesalertwithresenddelay)
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
  * [`obj spec.serviceMonitorNamespaceSelector`](#obj-specservicemonitornamespaceselector)
    * [`fn withMatchExpressions(matchExpressions)`](#fn-specservicemonitornamespaceselectorwithmatchexpressions)
    * [`fn withMatchExpressionsMixin(matchExpressions)`](#fn-specservicemonitornamespaceselectorwithmatchexpressionsmixin)
    * [`fn withMatchLabels(matchLabels)`](#fn-specservicemonitornamespaceselectorwithmatchlabels)
    * [`fn withMatchLabelsMixin(matchLabels)`](#fn-specservicemonitornamespaceselectorwithmatchlabelsmixin)
  * [`obj spec.serviceMonitorSelector`](#obj-specservicemonitorselector)
    * [`fn withMatchExpressions(matchExpressions)`](#fn-specservicemonitorselectorwithmatchexpressions)
    * [`fn withMatchExpressionsMixin(matchExpressions)`](#fn-specservicemonitorselectorwithmatchexpressionsmixin)
    * [`fn withMatchLabels(matchLabels)`](#fn-specservicemonitorselectorwithmatchlabels)
    * [`fn withMatchLabelsMixin(matchLabels)`](#fn-specservicemonitorselectorwithmatchlabelsmixin)
  * [`obj spec.storage`](#obj-specstorage)
    * [`fn withDisableMountSubPath(disableMountSubPath)`](#fn-specstoragewithdisablemountsubpath)
    * [`obj spec.storage.emptyDir`](#obj-specstorageemptydir)
      * [`fn withMedium(medium)`](#fn-specstorageemptydirwithmedium)
      * [`fn withSizeLimit(sizeLimit)`](#fn-specstorageemptydirwithsizelimit)
    * [`obj spec.storage.volumeClaimTemplate`](#obj-specstoragevolumeclaimtemplate)
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
  * [`obj spec.thanos`](#obj-specthanos)
    * [`fn withBaseImage(baseImage)`](#fn-specthanoswithbaseimage)
    * [`fn withImage(image)`](#fn-specthanoswithimage)
    * [`fn withListenLocal(listenLocal)`](#fn-specthanoswithlistenlocal)
    * [`fn withLogFormat(logFormat)`](#fn-specthanoswithlogformat)
    * [`fn withLogLevel(logLevel)`](#fn-specthanoswithloglevel)
    * [`fn withMinTime(minTime)`](#fn-specthanoswithmintime)
    * [`fn withObjectStorageConfigFile(objectStorageConfigFile)`](#fn-specthanoswithobjectstorageconfigfile)
    * [`fn withSha(sha)`](#fn-specthanoswithsha)
    * [`fn withTag(tag)`](#fn-specthanoswithtag)
    * [`fn withTracingConfigFile(tracingConfigFile)`](#fn-specthanoswithtracingconfigfile)
    * [`fn withVersion(version)`](#fn-specthanoswithversion)
    * [`obj spec.thanos.grpcServerTlsConfig`](#obj-specthanosgrpcservertlsconfig)
      * [`fn withCaFile(caFile)`](#fn-specthanosgrpcservertlsconfigwithcafile)
      * [`fn withCertFile(certFile)`](#fn-specthanosgrpcservertlsconfigwithcertfile)
      * [`fn withInsecureSkipVerify(insecureSkipVerify)`](#fn-specthanosgrpcservertlsconfigwithinsecureskipverify)
      * [`fn withKeyFile(keyFile)`](#fn-specthanosgrpcservertlsconfigwithkeyfile)
      * [`fn withServerName(serverName)`](#fn-specthanosgrpcservertlsconfigwithservername)
      * [`obj spec.thanos.grpcServerTlsConfig.ca`](#obj-specthanosgrpcservertlsconfigca)
        * [`obj spec.thanos.grpcServerTlsConfig.ca.configMap`](#obj-specthanosgrpcservertlsconfigcaconfigmap)
          * [`fn withKey(key)`](#fn-specthanosgrpcservertlsconfigcaconfigmapwithkey)
          * [`fn withName(name)`](#fn-specthanosgrpcservertlsconfigcaconfigmapwithname)
          * [`fn withOptional(optional)`](#fn-specthanosgrpcservertlsconfigcaconfigmapwithoptional)
        * [`obj spec.thanos.grpcServerTlsConfig.ca.secret`](#obj-specthanosgrpcservertlsconfigcasecret)
          * [`fn withKey(key)`](#fn-specthanosgrpcservertlsconfigcasecretwithkey)
          * [`fn withName(name)`](#fn-specthanosgrpcservertlsconfigcasecretwithname)
          * [`fn withOptional(optional)`](#fn-specthanosgrpcservertlsconfigcasecretwithoptional)
      * [`obj spec.thanos.grpcServerTlsConfig.cert`](#obj-specthanosgrpcservertlsconfigcert)
        * [`obj spec.thanos.grpcServerTlsConfig.cert.configMap`](#obj-specthanosgrpcservertlsconfigcertconfigmap)
          * [`fn withKey(key)`](#fn-specthanosgrpcservertlsconfigcertconfigmapwithkey)
          * [`fn withName(name)`](#fn-specthanosgrpcservertlsconfigcertconfigmapwithname)
          * [`fn withOptional(optional)`](#fn-specthanosgrpcservertlsconfigcertconfigmapwithoptional)
        * [`obj spec.thanos.grpcServerTlsConfig.cert.secret`](#obj-specthanosgrpcservertlsconfigcertsecret)
          * [`fn withKey(key)`](#fn-specthanosgrpcservertlsconfigcertsecretwithkey)
          * [`fn withName(name)`](#fn-specthanosgrpcservertlsconfigcertsecretwithname)
          * [`fn withOptional(optional)`](#fn-specthanosgrpcservertlsconfigcertsecretwithoptional)
      * [`obj spec.thanos.grpcServerTlsConfig.keySecret`](#obj-specthanosgrpcservertlsconfigkeysecret)
        * [`fn withKey(key)`](#fn-specthanosgrpcservertlsconfigkeysecretwithkey)
        * [`fn withName(name)`](#fn-specthanosgrpcservertlsconfigkeysecretwithname)
        * [`fn withOptional(optional)`](#fn-specthanosgrpcservertlsconfigkeysecretwithoptional)
    * [`obj spec.thanos.objectStorageConfig`](#obj-specthanosobjectstorageconfig)
      * [`fn withKey(key)`](#fn-specthanosobjectstorageconfigwithkey)
      * [`fn withName(name)`](#fn-specthanosobjectstorageconfigwithname)
      * [`fn withOptional(optional)`](#fn-specthanosobjectstorageconfigwithoptional)
    * [`obj spec.thanos.resources`](#obj-specthanosresources)
      * [`fn withLimits(limits)`](#fn-specthanosresourceswithlimits)
      * [`fn withLimitsMixin(limits)`](#fn-specthanosresourceswithlimitsmixin)
      * [`fn withRequests(requests)`](#fn-specthanosresourceswithrequests)
      * [`fn withRequestsMixin(requests)`](#fn-specthanosresourceswithrequestsmixin)
    * [`obj spec.thanos.tracingConfig`](#obj-specthanostracingconfig)
      * [`fn withKey(key)`](#fn-specthanostracingconfigwithkey)
      * [`fn withName(name)`](#fn-specthanostracingconfigwithname)
      * [`fn withOptional(optional)`](#fn-specthanostracingconfigwithoptional)
  * [`obj spec.web`](#obj-specweb)
    * [`fn withPageTitle(pageTitle)`](#fn-specwebwithpagetitle)

## Fields

### fn new

```ts
new(name)
```

new returns an instance of Prometheus

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

Specification of the desired behavior of the Prometheus cluster. More info: https://github.com/kubernetes/community/blob/master/contributors/devel/sig-architecture/api-conventions.md#spec-and-status

### fn spec.withAllowOverlappingBlocks

```ts
withAllowOverlappingBlocks(allowOverlappingBlocks)
```

AllowOverlappingBlocks enables vertical compaction and vertical query merge in Prometheus. This is still experimental in Prometheus so it may change in any upcoming release.

### fn spec.withBaseImage

```ts
withBaseImage(baseImage)
```

Base image to use for a Prometheus deployment. Deprecated: use 'image' instead

### fn spec.withConfigMaps

```ts
withConfigMaps(configMaps)
```

ConfigMaps is a list of ConfigMaps in the same namespace as the Prometheus object, which shall be mounted into the Prometheus Pods. The ConfigMaps are mounted into /etc/prometheus/configmaps/<configmap-name>.

### fn spec.withConfigMapsMixin

```ts
withConfigMapsMixin(configMaps)
```

ConfigMaps is a list of ConfigMaps in the same namespace as the Prometheus object, which shall be mounted into the Prometheus Pods. The ConfigMaps are mounted into /etc/prometheus/configmaps/<configmap-name>.

**Note:** This function appends passed data to existing values

### fn spec.withContainers

```ts
withContainers(containers)
```

Containers allows injecting additional containers or modifying operator generated containers. This can be used to allow adding an authentication proxy to a Prometheus pod or to change the behavior of an operator generated container. Containers described here modify an operator generated container if they share the same name and modifications are done via a strategic merge patch. The current container names are: `prometheus`, `config-reloader`, and `thanos-sidecar`. Overriding containers is entirely outside the scope of what the maintainers will support and by doing so, you accept that this behaviour may break at any time without notice.

### fn spec.withContainersMixin

```ts
withContainersMixin(containers)
```

Containers allows injecting additional containers or modifying operator generated containers. This can be used to allow adding an authentication proxy to a Prometheus pod or to change the behavior of an operator generated container. Containers described here modify an operator generated container if they share the same name and modifications are done via a strategic merge patch. The current container names are: `prometheus`, `config-reloader`, and `thanos-sidecar`. Overriding containers is entirely outside the scope of what the maintainers will support and by doing so, you accept that this behaviour may break at any time without notice.

**Note:** This function appends passed data to existing values

### fn spec.withDisableCompaction

```ts
withDisableCompaction(disableCompaction)
```

Disable prometheus compaction.

### fn spec.withEnableAdminAPI

```ts
withEnableAdminAPI(enableAdminAPI)
```

Enable access to prometheus web admin API. Defaults to the value of `false`. WARNING: Enabling the admin APIs enables mutating endpoints, to delete data, shutdown Prometheus, and more. Enabling this should be done with care and the user is advised to add additional authentication authorization via a proxy to ensure only clients authorized to perform these actions can do so. For more information see https://prometheus.io/docs/prometheus/latest/querying/api/#tsdb-admin-apis

### fn spec.withEnableFeatures

```ts
withEnableFeatures(enableFeatures)
```

Enable access to Prometheus disabled features. By default, no features are enabled. Enabling disabled features is entirely outside the scope of what the maintainers will support and by doing so, you accept that this behaviour may break at any time without notice. For more information see https://prometheus.io/docs/prometheus/latest/disabled_features/

### fn spec.withEnableFeaturesMixin

```ts
withEnableFeaturesMixin(enableFeatures)
```

Enable access to Prometheus disabled features. By default, no features are enabled. Enabling disabled features is entirely outside the scope of what the maintainers will support and by doing so, you accept that this behaviour may break at any time without notice. For more information see https://prometheus.io/docs/prometheus/latest/disabled_features/

**Note:** This function appends passed data to existing values

### fn spec.withEnforcedNamespaceLabel

```ts
withEnforcedNamespaceLabel(enforcedNamespaceLabel)
```

EnforcedNamespaceLabel enforces adding a namespace label of origin for each alert and metric that is user created. The label value will always be the namespace of the object that is being created.

### fn spec.withEnforcedSampleLimit

```ts
withEnforcedSampleLimit(enforcedSampleLimit)
```

EnforcedSampleLimit defines global limit on number of scraped samples that will be accepted. This overrides any SampleLimit set per ServiceMonitor or/and PodMonitor. It is meant to be used by admins to enforce the SampleLimit to keep overall number of samples/series under the desired limit. Note that if SampleLimit is lower that value will be taken instead.

### fn spec.withEnforcedTargetLimit

```ts
withEnforcedTargetLimit(enforcedTargetLimit)
```

EnforcedTargetLimit defines a global limit on the number of scraped targets. This overrides any TargetLimit set per ServiceMonitor or/and PodMonitor. It is meant to be used by admins to enforce the TargetLimit to keep overall number of targets under the desired limit. Note that if TargetLimit is higher that value will be taken instead.

### fn spec.withEvaluationInterval

```ts
withEvaluationInterval(evaluationInterval)
```

Interval between consecutive evaluations.

### fn spec.withExternalLabels

```ts
withExternalLabels(externalLabels)
```

The labels to add to any time series or alerts when communicating with external systems (federation, remote storage, Alertmanager).

### fn spec.withExternalLabelsMixin

```ts
withExternalLabelsMixin(externalLabels)
```

The labels to add to any time series or alerts when communicating with external systems (federation, remote storage, Alertmanager).

**Note:** This function appends passed data to existing values

### fn spec.withExternalUrl

```ts
withExternalUrl(externalUrl)
```

The external URL the Prometheus instances will be available under. This is necessary to generate correct URLs. This is necessary if Prometheus is not served from root of a DNS name.

### fn spec.withIgnoreNamespaceSelectors

```ts
withIgnoreNamespaceSelectors(ignoreNamespaceSelectors)
```

IgnoreNamespaceSelectors if set to true will ignore NamespaceSelector settings from the podmonitor and servicemonitor configs, and they will only discover endpoints within their current namespace.  Defaults to false.

### fn spec.withImage

```ts
withImage(image)
```

Image if specified has precedence over baseImage, tag and sha combinations. Specifying the version is still necessary to ensure the Prometheus Operator knows what version of Prometheus is being configured.

### fn spec.withImagePullSecrets

```ts
withImagePullSecrets(imagePullSecrets)
```

An optional list of references to secrets in the same namespace to use for pulling prometheus and alertmanager images from registries see http://kubernetes.io/docs/user-guide/images#specifying-imagepullsecrets-on-a-pod

### fn spec.withImagePullSecretsMixin

```ts
withImagePullSecretsMixin(imagePullSecrets)
```

An optional list of references to secrets in the same namespace to use for pulling prometheus and alertmanager images from registries see http://kubernetes.io/docs/user-guide/images#specifying-imagepullsecrets-on-a-pod

**Note:** This function appends passed data to existing values

### fn spec.withInitContainers

```ts
withInitContainers(initContainers)
```

InitContainers allows adding initContainers to the pod definition. Those can be used to e.g. fetch secrets for injection into the Prometheus configuration from external sources. Any errors during the execution of an initContainer will lead to a restart of the Pod. More info: https://kubernetes.io/docs/concepts/workloads/pods/init-containers/ Using initContainers for any use case other then secret fetching is entirely outside the scope of what the maintainers will support and by doing so, you accept that this behaviour may break at any time without notice.

### fn spec.withInitContainersMixin

```ts
withInitContainersMixin(initContainers)
```

InitContainers allows adding initContainers to the pod definition. Those can be used to e.g. fetch secrets for injection into the Prometheus configuration from external sources. Any errors during the execution of an initContainer will lead to a restart of the Pod. More info: https://kubernetes.io/docs/concepts/workloads/pods/init-containers/ Using initContainers for any use case other then secret fetching is entirely outside the scope of what the maintainers will support and by doing so, you accept that this behaviour may break at any time without notice.

**Note:** This function appends passed data to existing values

### fn spec.withListenLocal

```ts
withListenLocal(listenLocal)
```

ListenLocal makes the Prometheus server listen on loopback, so that it does not bind against the Pod IP.

### fn spec.withLogFormat

```ts
withLogFormat(logFormat)
```

Log format for Prometheus to be configured with.

### fn spec.withLogLevel

```ts
withLogLevel(logLevel)
```

Log level for Prometheus to be configured with.

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

### fn spec.withOverrideHonorLabels

```ts
withOverrideHonorLabels(overrideHonorLabels)
```

OverrideHonorLabels if set to true overrides all user configured honor_labels. If HonorLabels is set in ServiceMonitor or PodMonitor to true, this overrides honor_labels to false.

### fn spec.withOverrideHonorTimestamps

```ts
withOverrideHonorTimestamps(overrideHonorTimestamps)
```

OverrideHonorTimestamps allows to globally enforce honoring timestamps in all scrape configs.

### fn spec.withPaused

```ts
withPaused(paused)
```

When a Prometheus deployment is paused, no actions except for deletion will be performed on the underlying objects.

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

### fn spec.withPrometheusExternalLabelName

```ts
withPrometheusExternalLabelName(prometheusExternalLabelName)
```

Name of Prometheus external label used to denote Prometheus instance name. Defaults to the value of `prometheus`. External label will _not_ be added when value is set to empty string (`""`).

### fn spec.withPrometheusRulesExcludedFromEnforce

```ts
withPrometheusRulesExcludedFromEnforce(prometheusRulesExcludedFromEnforce)
```

PrometheusRulesExcludedFromEnforce - list of prometheus rules to be excluded from enforcing of adding namespace labels. Works only if enforcedNamespaceLabel set to true. Make sure both ruleNamespace and ruleName are set for each pair

### fn spec.withPrometheusRulesExcludedFromEnforceMixin

```ts
withPrometheusRulesExcludedFromEnforceMixin(prometheusRulesExcludedFromEnforce)
```

PrometheusRulesExcludedFromEnforce - list of prometheus rules to be excluded from enforcing of adding namespace labels. Works only if enforcedNamespaceLabel set to true. Make sure both ruleNamespace and ruleName are set for each pair

**Note:** This function appends passed data to existing values

### fn spec.withQueryLogFile

```ts
withQueryLogFile(queryLogFile)
```

QueryLogFile specifies the file to which PromQL queries are logged. Note that this location must be writable, and can be persisted using an attached volume. Alternatively, the location can be set to a stdout location such as `/dev/stdout` to log querie information to the default Prometheus log stream. This is only available in versions of Prometheus >= 2.16.0. For more details, see the Prometheus docs (https://prometheus.io/docs/guides/query-log/)

### fn spec.withRemoteRead

```ts
withRemoteRead(remoteRead)
```

If specified, the remote_read spec. This is an experimental feature, it may change in any upcoming release in a breaking way.

### fn spec.withRemoteReadMixin

```ts
withRemoteReadMixin(remoteRead)
```

If specified, the remote_read spec. This is an experimental feature, it may change in any upcoming release in a breaking way.

**Note:** This function appends passed data to existing values

### fn spec.withRemoteWrite

```ts
withRemoteWrite(remoteWrite)
```

If specified, the remote_write spec. This is an experimental feature, it may change in any upcoming release in a breaking way.

### fn spec.withRemoteWriteMixin

```ts
withRemoteWriteMixin(remoteWrite)
```

If specified, the remote_write spec. This is an experimental feature, it may change in any upcoming release in a breaking way.

**Note:** This function appends passed data to existing values

### fn spec.withReplicaExternalLabelName

```ts
withReplicaExternalLabelName(replicaExternalLabelName)
```

Name of Prometheus external label used to denote replica name. Defaults to the value of `prometheus_replica`. External label will _not_ be added when value is set to empty string (`""`).

### fn spec.withReplicas

```ts
withReplicas(replicas)
```

Number of replicas of each shard to deploy for a Prometheus deployment. Number of replicas multiplied by shards is the total number of Pods created.

### fn spec.withRetention

```ts
withRetention(retention)
```

Time duration Prometheus shall retain data for. Default is '24h', and must match the regular expression `[0-9]+(ms|s|m|h|d|w|y)` (milliseconds seconds minutes hours days weeks years).

### fn spec.withRetentionSize

```ts
withRetentionSize(retentionSize)
```

Maximum amount of disk space used by blocks. Supported units: B, KB, MB, GB, TB, PB, EB. Ex: `512MB`.

### fn spec.withRoutePrefix

```ts
withRoutePrefix(routePrefix)
```

The route prefix Prometheus registers HTTP handlers for. This is useful, if using ExternalURL and a proxy is rewriting HTTP routes of a request, and the actual ExternalURL is still true, but the server serves requests under a different route prefix. For example for use with `kubectl proxy`.

### fn spec.withScrapeInterval

```ts
withScrapeInterval(scrapeInterval)
```

Interval between consecutive scrapes.

### fn spec.withScrapeTimeout

```ts
withScrapeTimeout(scrapeTimeout)
```

Number of seconds to wait for target to respond before erroring.

### fn spec.withSecrets

```ts
withSecrets(secrets)
```

Secrets is a list of Secrets in the same namespace as the Prometheus object, which shall be mounted into the Prometheus Pods. The Secrets are mounted into /etc/prometheus/secrets/<secret-name>.

### fn spec.withSecretsMixin

```ts
withSecretsMixin(secrets)
```

Secrets is a list of Secrets in the same namespace as the Prometheus object, which shall be mounted into the Prometheus Pods. The Secrets are mounted into /etc/prometheus/secrets/<secret-name>.

**Note:** This function appends passed data to existing values

### fn spec.withServiceAccountName

```ts
withServiceAccountName(serviceAccountName)
```

ServiceAccountName is the name of the ServiceAccount to use to run the Prometheus Pods.

### fn spec.withSha

```ts
withSha(sha)
```

SHA of Prometheus container image to be deployed. Defaults to the value of `version`. Similar to a tag, but the SHA explicitly deploys an immutable container image. Version and Tag are ignored if SHA is set. Deprecated: use 'image' instead.  The image digest can be specified as part of the image URL.

### fn spec.withShards

```ts
withShards(shards)
```

EXPERIMENTAL: Number of shards to distribute targets onto. Number of replicas multiplied by shards is the total number of Pods created. Note that scaling down shards will not reshard data onto remaining instances, it must be manually moved. Increasing shards will not reshard data either but it will continue to be available from the same instances. To query globally use Thanos sidecar and Thanos querier or remote write data to a central location. Sharding is done on the content of the `__address__` target meta-label.

### fn spec.withTag

```ts
withTag(tag)
```

Tag of Prometheus container image to be deployed. Defaults to the value of `version`. Version is ignored if Tag is set. Deprecated: use 'image' instead.  The image tag can be specified as part of the image URL.

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

### fn spec.withVersion

```ts
withVersion(version)
```

Version of Prometheus to be deployed.

### fn spec.withVolumeMounts

```ts
withVolumeMounts(volumeMounts)
```

VolumeMounts allows configuration of additional VolumeMounts on the output StatefulSet definition. VolumeMounts specified will be appended to other VolumeMounts in the prometheus container, that are generated as a result of StorageSpec objects.

### fn spec.withVolumeMountsMixin

```ts
withVolumeMountsMixin(volumeMounts)
```

VolumeMounts allows configuration of additional VolumeMounts on the output StatefulSet definition. VolumeMounts specified will be appended to other VolumeMounts in the prometheus container, that are generated as a result of StorageSpec objects.

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

### fn spec.withWalCompression

```ts
withWalCompression(walCompression)
```

Enable compression of the write-ahead log using Snappy. This flag is only available in versions of Prometheus >= 2.11.0.

## obj spec.additionalAlertManagerConfigs

AdditionalAlertManagerConfigs allows specifying a key of a Secret containing additional Prometheus AlertManager configurations. AlertManager configurations specified are appended to the configurations generated by the Prometheus Operator. Job configurations specified must have the form as specified in the official Prometheus documentation: https://prometheus.io/docs/prometheus/latest/configuration/configuration/#alertmanager_config. As AlertManager configs are appended, the user is responsible to make sure it is valid. Note that using this feature may expose the possibility to break upgrades of Prometheus. It is advised to review Prometheus release notes to ensure that no incompatible AlertManager configs are going to break Prometheus after the upgrade.

### fn spec.additionalAlertManagerConfigs.withKey

```ts
withKey(key)
```

The key of the secret to select from.  Must be a valid secret key.

### fn spec.additionalAlertManagerConfigs.withName

```ts
withName(name)
```

Name of the referent. More info: https://kubernetes.io/docs/concepts/overview/working-with-objects/names/#names TODO: Add other useful fields. apiVersion, kind, uid?

### fn spec.additionalAlertManagerConfigs.withOptional

```ts
withOptional(optional)
```

Specify whether the Secret or its key must be defined

## obj spec.additionalAlertRelabelConfigs

AdditionalAlertRelabelConfigs allows specifying a key of a Secret containing additional Prometheus alert relabel configurations. Alert relabel configurations specified are appended to the configurations generated by the Prometheus Operator. Alert relabel configurations specified must have the form as specified in the official Prometheus documentation: https://prometheus.io/docs/prometheus/latest/configuration/configuration/#alert_relabel_configs. As alert relabel configs are appended, the user is responsible to make sure it is valid. Note that using this feature may expose the possibility to break upgrades of Prometheus. It is advised to review Prometheus release notes to ensure that no incompatible alert relabel configs are going to break Prometheus after the upgrade.

### fn spec.additionalAlertRelabelConfigs.withKey

```ts
withKey(key)
```

The key of the secret to select from.  Must be a valid secret key.

### fn spec.additionalAlertRelabelConfigs.withName

```ts
withName(name)
```

Name of the referent. More info: https://kubernetes.io/docs/concepts/overview/working-with-objects/names/#names TODO: Add other useful fields. apiVersion, kind, uid?

### fn spec.additionalAlertRelabelConfigs.withOptional

```ts
withOptional(optional)
```

Specify whether the Secret or its key must be defined

## obj spec.additionalScrapeConfigs

AdditionalScrapeConfigs allows specifying a key of a Secret containing additional Prometheus scrape configurations. Scrape configurations specified are appended to the configurations generated by the Prometheus Operator. Job configurations specified must have the form as specified in the official Prometheus documentation: https://prometheus.io/docs/prometheus/latest/configuration/configuration/#scrape_config. As scrape configs are appended, the user is responsible to make sure it is valid. Note that using this feature may expose the possibility to break upgrades of Prometheus. It is advised to review Prometheus release notes to ensure that no incompatible scrape configs are going to break Prometheus after the upgrade.

### fn spec.additionalScrapeConfigs.withKey

```ts
withKey(key)
```

The key of the secret to select from.  Must be a valid secret key.

### fn spec.additionalScrapeConfigs.withName

```ts
withName(name)
```

Name of the referent. More info: https://kubernetes.io/docs/concepts/overview/working-with-objects/names/#names TODO: Add other useful fields. apiVersion, kind, uid?

### fn spec.additionalScrapeConfigs.withOptional

```ts
withOptional(optional)
```

Specify whether the Secret or its key must be defined

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

## obj spec.alerting

Define details regarding alerting.

### fn spec.alerting.withAlertmanagers

```ts
withAlertmanagers(alertmanagers)
```

AlertmanagerEndpoints Prometheus should fire alerts against.

### fn spec.alerting.withAlertmanagersMixin

```ts
withAlertmanagersMixin(alertmanagers)
```

AlertmanagerEndpoints Prometheus should fire alerts against.

**Note:** This function appends passed data to existing values

## obj spec.apiserverConfig

APIServerConfig allows specifying a host and auth methods to access apiserver. If left empty, Prometheus is assumed to run inside of the cluster and will discover API servers automatically and use the pod's CA certificate and bearer token file at /var/run/secrets/kubernetes.io/serviceaccount/.

### fn spec.apiserverConfig.withBearerToken

```ts
withBearerToken(bearerToken)
```

Bearer token for accessing apiserver.

### fn spec.apiserverConfig.withBearerTokenFile

```ts
withBearerTokenFile(bearerTokenFile)
```

File to read bearer token for accessing apiserver.

### fn spec.apiserverConfig.withHost

```ts
withHost(host)
```

Host of apiserver. A valid string consisting of a hostname or IP followed by an optional port number

## obj spec.apiserverConfig.basicAuth

BasicAuth allow an endpoint to authenticate over basic authentication

## obj spec.apiserverConfig.basicAuth.password

The secret in the service monitor namespace that contains the password for authentication.

### fn spec.apiserverConfig.basicAuth.password.withKey

```ts
withKey(key)
```

The key of the secret to select from.  Must be a valid secret key.

### fn spec.apiserverConfig.basicAuth.password.withName

```ts
withName(name)
```

Name of the referent. More info: https://kubernetes.io/docs/concepts/overview/working-with-objects/names/#names TODO: Add other useful fields. apiVersion, kind, uid?

### fn spec.apiserverConfig.basicAuth.password.withOptional

```ts
withOptional(optional)
```

Specify whether the Secret or its key must be defined

## obj spec.apiserverConfig.basicAuth.username

The secret in the service monitor namespace that contains the username for authentication.

### fn spec.apiserverConfig.basicAuth.username.withKey

```ts
withKey(key)
```

The key of the secret to select from.  Must be a valid secret key.

### fn spec.apiserverConfig.basicAuth.username.withName

```ts
withName(name)
```

Name of the referent. More info: https://kubernetes.io/docs/concepts/overview/working-with-objects/names/#names TODO: Add other useful fields. apiVersion, kind, uid?

### fn spec.apiserverConfig.basicAuth.username.withOptional

```ts
withOptional(optional)
```

Specify whether the Secret or its key must be defined

## obj spec.apiserverConfig.tlsConfig

TLS Config to use for accessing apiserver.

### fn spec.apiserverConfig.tlsConfig.withCaFile

```ts
withCaFile(caFile)
```

Path to the CA cert in the Prometheus container to use for the targets.

### fn spec.apiserverConfig.tlsConfig.withCertFile

```ts
withCertFile(certFile)
```

Path to the client cert file in the Prometheus container for the targets.

### fn spec.apiserverConfig.tlsConfig.withInsecureSkipVerify

```ts
withInsecureSkipVerify(insecureSkipVerify)
```

Disable target certificate validation.

### fn spec.apiserverConfig.tlsConfig.withKeyFile

```ts
withKeyFile(keyFile)
```

Path to the client key file in the Prometheus container for the targets.

### fn spec.apiserverConfig.tlsConfig.withServerName

```ts
withServerName(serverName)
```

Used to verify the hostname for the targets.

## obj spec.apiserverConfig.tlsConfig.ca

Struct containing the CA cert to use for the targets.

## obj spec.apiserverConfig.tlsConfig.ca.configMap

ConfigMap containing data to use for the targets.

### fn spec.apiserverConfig.tlsConfig.ca.configMap.withKey

```ts
withKey(key)
```

The key to select.

### fn spec.apiserverConfig.tlsConfig.ca.configMap.withName

```ts
withName(name)
```

Name of the referent. More info: https://kubernetes.io/docs/concepts/overview/working-with-objects/names/#names TODO: Add other useful fields. apiVersion, kind, uid?

### fn spec.apiserverConfig.tlsConfig.ca.configMap.withOptional

```ts
withOptional(optional)
```

Specify whether the ConfigMap or its key must be defined

## obj spec.apiserverConfig.tlsConfig.ca.secret

Secret containing data to use for the targets.

### fn spec.apiserverConfig.tlsConfig.ca.secret.withKey

```ts
withKey(key)
```

The key of the secret to select from.  Must be a valid secret key.

### fn spec.apiserverConfig.tlsConfig.ca.secret.withName

```ts
withName(name)
```

Name of the referent. More info: https://kubernetes.io/docs/concepts/overview/working-with-objects/names/#names TODO: Add other useful fields. apiVersion, kind, uid?

### fn spec.apiserverConfig.tlsConfig.ca.secret.withOptional

```ts
withOptional(optional)
```

Specify whether the Secret or its key must be defined

## obj spec.apiserverConfig.tlsConfig.cert

Struct containing the client cert file for the targets.

## obj spec.apiserverConfig.tlsConfig.cert.configMap

ConfigMap containing data to use for the targets.

### fn spec.apiserverConfig.tlsConfig.cert.configMap.withKey

```ts
withKey(key)
```

The key to select.

### fn spec.apiserverConfig.tlsConfig.cert.configMap.withName

```ts
withName(name)
```

Name of the referent. More info: https://kubernetes.io/docs/concepts/overview/working-with-objects/names/#names TODO: Add other useful fields. apiVersion, kind, uid?

### fn spec.apiserverConfig.tlsConfig.cert.configMap.withOptional

```ts
withOptional(optional)
```

Specify whether the ConfigMap or its key must be defined

## obj spec.apiserverConfig.tlsConfig.cert.secret

Secret containing data to use for the targets.

### fn spec.apiserverConfig.tlsConfig.cert.secret.withKey

```ts
withKey(key)
```

The key of the secret to select from.  Must be a valid secret key.

### fn spec.apiserverConfig.tlsConfig.cert.secret.withName

```ts
withName(name)
```

Name of the referent. More info: https://kubernetes.io/docs/concepts/overview/working-with-objects/names/#names TODO: Add other useful fields. apiVersion, kind, uid?

### fn spec.apiserverConfig.tlsConfig.cert.secret.withOptional

```ts
withOptional(optional)
```

Specify whether the Secret or its key must be defined

## obj spec.apiserverConfig.tlsConfig.keySecret

Secret containing the client key file for the targets.

### fn spec.apiserverConfig.tlsConfig.keySecret.withKey

```ts
withKey(key)
```

The key of the secret to select from.  Must be a valid secret key.

### fn spec.apiserverConfig.tlsConfig.keySecret.withName

```ts
withName(name)
```

Name of the referent. More info: https://kubernetes.io/docs/concepts/overview/working-with-objects/names/#names TODO: Add other useful fields. apiVersion, kind, uid?

### fn spec.apiserverConfig.tlsConfig.keySecret.withOptional

```ts
withOptional(optional)
```

Specify whether the Secret or its key must be defined

## obj spec.arbitraryFSAccessThroughSMs

ArbitraryFSAccessThroughSMs configures whether configuration based on a service monitor can access arbitrary files on the file system of the Prometheus container e.g. bearer token files.

### fn spec.arbitraryFSAccessThroughSMs.withDeny

```ts
withDeny(deny)
```



## obj spec.podMetadata

PodMetadata configures Labels and Annotations which are propagated to the prometheus pods.

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

## obj spec.podMonitorNamespaceSelector

Namespace's labels to match for PodMonitor discovery. If nil, only check own namespace.

### fn spec.podMonitorNamespaceSelector.withMatchExpressions

```ts
withMatchExpressions(matchExpressions)
```

matchExpressions is a list of label selector requirements. The requirements are ANDed.

### fn spec.podMonitorNamespaceSelector.withMatchExpressionsMixin

```ts
withMatchExpressionsMixin(matchExpressions)
```

matchExpressions is a list of label selector requirements. The requirements are ANDed.

**Note:** This function appends passed data to existing values

### fn spec.podMonitorNamespaceSelector.withMatchLabels

```ts
withMatchLabels(matchLabels)
```

matchLabels is a map of {key,value} pairs. A single {key,value} in the matchLabels map is equivalent to an element of matchExpressions, whose key field is "key", the operator is "In", and the values array contains only "value". The requirements are ANDed.

### fn spec.podMonitorNamespaceSelector.withMatchLabelsMixin

```ts
withMatchLabelsMixin(matchLabels)
```

matchLabels is a map of {key,value} pairs. A single {key,value} in the matchLabels map is equivalent to an element of matchExpressions, whose key field is "key", the operator is "In", and the values array contains only "value". The requirements are ANDed.

**Note:** This function appends passed data to existing values

## obj spec.podMonitorSelector

*Experimental* PodMonitors to be selected for target discovery. *Deprecated:* if neither this nor serviceMonitorSelector are specified, configuration is unmanaged.

### fn spec.podMonitorSelector.withMatchExpressions

```ts
withMatchExpressions(matchExpressions)
```

matchExpressions is a list of label selector requirements. The requirements are ANDed.

### fn spec.podMonitorSelector.withMatchExpressionsMixin

```ts
withMatchExpressionsMixin(matchExpressions)
```

matchExpressions is a list of label selector requirements. The requirements are ANDed.

**Note:** This function appends passed data to existing values

### fn spec.podMonitorSelector.withMatchLabels

```ts
withMatchLabels(matchLabels)
```

matchLabels is a map of {key,value} pairs. A single {key,value} in the matchLabels map is equivalent to an element of matchExpressions, whose key field is "key", the operator is "In", and the values array contains only "value". The requirements are ANDed.

### fn spec.podMonitorSelector.withMatchLabelsMixin

```ts
withMatchLabelsMixin(matchLabels)
```

matchLabels is a map of {key,value} pairs. A single {key,value} in the matchLabels map is equivalent to an element of matchExpressions, whose key field is "key", the operator is "In", and the values array contains only "value". The requirements are ANDed.

**Note:** This function appends passed data to existing values

## obj spec.probeNamespaceSelector

*Experimental* Namespaces to be selected for Probe discovery. If nil, only check own namespace.

### fn spec.probeNamespaceSelector.withMatchExpressions

```ts
withMatchExpressions(matchExpressions)
```

matchExpressions is a list of label selector requirements. The requirements are ANDed.

### fn spec.probeNamespaceSelector.withMatchExpressionsMixin

```ts
withMatchExpressionsMixin(matchExpressions)
```

matchExpressions is a list of label selector requirements. The requirements are ANDed.

**Note:** This function appends passed data to existing values

### fn spec.probeNamespaceSelector.withMatchLabels

```ts
withMatchLabels(matchLabels)
```

matchLabels is a map of {key,value} pairs. A single {key,value} in the matchLabels map is equivalent to an element of matchExpressions, whose key field is "key", the operator is "In", and the values array contains only "value". The requirements are ANDed.

### fn spec.probeNamespaceSelector.withMatchLabelsMixin

```ts
withMatchLabelsMixin(matchLabels)
```

matchLabels is a map of {key,value} pairs. A single {key,value} in the matchLabels map is equivalent to an element of matchExpressions, whose key field is "key", the operator is "In", and the values array contains only "value". The requirements are ANDed.

**Note:** This function appends passed data to existing values

## obj spec.probeSelector

*Experimental* Probes to be selected for target discovery.

### fn spec.probeSelector.withMatchExpressions

```ts
withMatchExpressions(matchExpressions)
```

matchExpressions is a list of label selector requirements. The requirements are ANDed.

### fn spec.probeSelector.withMatchExpressionsMixin

```ts
withMatchExpressionsMixin(matchExpressions)
```

matchExpressions is a list of label selector requirements. The requirements are ANDed.

**Note:** This function appends passed data to existing values

### fn spec.probeSelector.withMatchLabels

```ts
withMatchLabels(matchLabels)
```

matchLabels is a map of {key,value} pairs. A single {key,value} in the matchLabels map is equivalent to an element of matchExpressions, whose key field is "key", the operator is "In", and the values array contains only "value". The requirements are ANDed.

### fn spec.probeSelector.withMatchLabelsMixin

```ts
withMatchLabelsMixin(matchLabels)
```

matchLabels is a map of {key,value} pairs. A single {key,value} in the matchLabels map is equivalent to an element of matchExpressions, whose key field is "key", the operator is "In", and the values array contains only "value". The requirements are ANDed.

**Note:** This function appends passed data to existing values

## obj spec.query

QuerySpec defines the query command line flags when starting Prometheus.

### fn spec.query.withLookbackDelta

```ts
withLookbackDelta(lookbackDelta)
```

The delta difference allowed for retrieving metrics during expression evaluations.

### fn spec.query.withMaxConcurrency

```ts
withMaxConcurrency(maxConcurrency)
```

Number of concurrent queries that can be run at once.

### fn spec.query.withMaxSamples

```ts
withMaxSamples(maxSamples)
```

Maximum number of samples a single query can load into memory. Note that queries will fail if they would load more samples than this into memory, so this also limits the number of samples a query can return.

### fn spec.query.withTimeout

```ts
withTimeout(timeout)
```

Maximum time a query may take before being aborted.

## obj spec.resources

Define resources requests and limits for single Pods.

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

Namespaces to be selected for PrometheusRules discovery. If unspecified, only the same namespace as the Prometheus object is in is used.

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

A selector to select which PrometheusRules to mount for loading alerting/recording rules from. Until (excluding) Prometheus Operator v0.24.0 Prometheus Operator will migrate any legacy rule ConfigMaps to PrometheusRule custom resources selected by RuleSelector. Make sure it does not match any config maps that you do not want to be migrated.

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

## obj spec.rules

/--rules.*/ command-line arguments.

## obj spec.rules.alert

/--rules.alert.*/ command-line arguments

### fn spec.rules.alert.withForGracePeriod

```ts
withForGracePeriod(forGracePeriod)
```

Minimum duration between alert and restored 'for' state. This is maintained only for alerts with configured 'for' time greater than grace period.

### fn spec.rules.alert.withForOutageTolerance

```ts
withForOutageTolerance(forOutageTolerance)
```

Max time to tolerate prometheus outage for restoring 'for' state of alert.

### fn spec.rules.alert.withResendDelay

```ts
withResendDelay(resendDelay)
```

Minimum amount of time to wait before resending an alert to Alertmanager.

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

## obj spec.serviceMonitorNamespaceSelector

Namespace's labels to match for ServiceMonitor discovery. If nil, only check own namespace.

### fn spec.serviceMonitorNamespaceSelector.withMatchExpressions

```ts
withMatchExpressions(matchExpressions)
```

matchExpressions is a list of label selector requirements. The requirements are ANDed.

### fn spec.serviceMonitorNamespaceSelector.withMatchExpressionsMixin

```ts
withMatchExpressionsMixin(matchExpressions)
```

matchExpressions is a list of label selector requirements. The requirements are ANDed.

**Note:** This function appends passed data to existing values

### fn spec.serviceMonitorNamespaceSelector.withMatchLabels

```ts
withMatchLabels(matchLabels)
```

matchLabels is a map of {key,value} pairs. A single {key,value} in the matchLabels map is equivalent to an element of matchExpressions, whose key field is "key", the operator is "In", and the values array contains only "value". The requirements are ANDed.

### fn spec.serviceMonitorNamespaceSelector.withMatchLabelsMixin

```ts
withMatchLabelsMixin(matchLabels)
```

matchLabels is a map of {key,value} pairs. A single {key,value} in the matchLabels map is equivalent to an element of matchExpressions, whose key field is "key", the operator is "In", and the values array contains only "value". The requirements are ANDed.

**Note:** This function appends passed data to existing values

## obj spec.serviceMonitorSelector

ServiceMonitors to be selected for target discovery. *Deprecated:* if neither this nor podMonitorSelector are specified, configuration is unmanaged.

### fn spec.serviceMonitorSelector.withMatchExpressions

```ts
withMatchExpressions(matchExpressions)
```

matchExpressions is a list of label selector requirements. The requirements are ANDed.

### fn spec.serviceMonitorSelector.withMatchExpressionsMixin

```ts
withMatchExpressionsMixin(matchExpressions)
```

matchExpressions is a list of label selector requirements. The requirements are ANDed.

**Note:** This function appends passed data to existing values

### fn spec.serviceMonitorSelector.withMatchLabels

```ts
withMatchLabels(matchLabels)
```

matchLabels is a map of {key,value} pairs. A single {key,value} in the matchLabels map is equivalent to an element of matchExpressions, whose key field is "key", the operator is "In", and the values array contains only "value". The requirements are ANDed.

### fn spec.serviceMonitorSelector.withMatchLabelsMixin

```ts
withMatchLabelsMixin(matchLabels)
```

matchLabels is a map of {key,value} pairs. A single {key,value} in the matchLabels map is equivalent to an element of matchExpressions, whose key field is "key", the operator is "In", and the values array contains only "value". The requirements are ANDed.

**Note:** This function appends passed data to existing values

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

## obj spec.thanos

Thanos configuration allows configuring various aspects of a Prometheus server in a Thanos environment. 
 This section is experimental, it may change significantly without deprecation notice in any release. 
 This is experimental and may change significantly without backward compatibility in any release.

### fn spec.thanos.withBaseImage

```ts
withBaseImage(baseImage)
```

Thanos base image if other than default. Deprecated: use 'image' instead

### fn spec.thanos.withImage

```ts
withImage(image)
```

Image if specified has precedence over baseImage, tag and sha combinations. Specifying the version is still necessary to ensure the Prometheus Operator knows what version of Thanos is being configured.

### fn spec.thanos.withListenLocal

```ts
withListenLocal(listenLocal)
```

ListenLocal makes the Thanos sidecar listen on loopback, so that it does not bind against the Pod IP.

### fn spec.thanos.withLogFormat

```ts
withLogFormat(logFormat)
```

LogFormat for Thanos sidecar to be configured with.

### fn spec.thanos.withLogLevel

```ts
withLogLevel(logLevel)
```

LogLevel for Thanos sidecar to be configured with.

### fn spec.thanos.withMinTime

```ts
withMinTime(minTime)
```

MinTime for Thanos sidecar to be configured with. Option can be a constant time in RFC3339 format or time duration relative to current time, such as -1d or 2h45m. Valid duration units are ms, s, m, h, d, w, y.

### fn spec.thanos.withObjectStorageConfigFile

```ts
withObjectStorageConfigFile(objectStorageConfigFile)
```

ObjectStorageConfigFile specifies the path of the object storage configuration file. When used alongside with ObjectStorageConfig, ObjectStorageConfigFile takes precedence.

### fn spec.thanos.withSha

```ts
withSha(sha)
```

SHA of Thanos container image to be deployed. Defaults to the value of `version`. Similar to a tag, but the SHA explicitly deploys an immutable container image. Version and Tag are ignored if SHA is set. Deprecated: use 'image' instead.  The image digest can be specified as part of the image URL.

### fn spec.thanos.withTag

```ts
withTag(tag)
```

Tag of Thanos sidecar container image to be deployed. Defaults to the value of `version`. Version is ignored if Tag is set. Deprecated: use 'image' instead.  The image tag can be specified as part of the image URL.

### fn spec.thanos.withTracingConfigFile

```ts
withTracingConfigFile(tracingConfigFile)
```

TracingConfig specifies the path of the tracing configuration file. When used alongside with TracingConfig, TracingConfigFile takes precedence.

### fn spec.thanos.withVersion

```ts
withVersion(version)
```

Version describes the version of Thanos to use.

## obj spec.thanos.grpcServerTlsConfig

GRPCServerTLSConfig configures the gRPC server from which Thanos Querier reads recorded rule data. Note: Currently only the CAFile, CertFile, and KeyFile fields are supported. Maps to the '--grpc-server-tls-*' CLI args.

### fn spec.thanos.grpcServerTlsConfig.withCaFile

```ts
withCaFile(caFile)
```

Path to the CA cert in the Prometheus container to use for the targets.

### fn spec.thanos.grpcServerTlsConfig.withCertFile

```ts
withCertFile(certFile)
```

Path to the client cert file in the Prometheus container for the targets.

### fn spec.thanos.grpcServerTlsConfig.withInsecureSkipVerify

```ts
withInsecureSkipVerify(insecureSkipVerify)
```

Disable target certificate validation.

### fn spec.thanos.grpcServerTlsConfig.withKeyFile

```ts
withKeyFile(keyFile)
```

Path to the client key file in the Prometheus container for the targets.

### fn spec.thanos.grpcServerTlsConfig.withServerName

```ts
withServerName(serverName)
```

Used to verify the hostname for the targets.

## obj spec.thanos.grpcServerTlsConfig.ca

Struct containing the CA cert to use for the targets.

## obj spec.thanos.grpcServerTlsConfig.ca.configMap

ConfigMap containing data to use for the targets.

### fn spec.thanos.grpcServerTlsConfig.ca.configMap.withKey

```ts
withKey(key)
```

The key to select.

### fn spec.thanos.grpcServerTlsConfig.ca.configMap.withName

```ts
withName(name)
```

Name of the referent. More info: https://kubernetes.io/docs/concepts/overview/working-with-objects/names/#names TODO: Add other useful fields. apiVersion, kind, uid?

### fn spec.thanos.grpcServerTlsConfig.ca.configMap.withOptional

```ts
withOptional(optional)
```

Specify whether the ConfigMap or its key must be defined

## obj spec.thanos.grpcServerTlsConfig.ca.secret

Secret containing data to use for the targets.

### fn spec.thanos.grpcServerTlsConfig.ca.secret.withKey

```ts
withKey(key)
```

The key of the secret to select from.  Must be a valid secret key.

### fn spec.thanos.grpcServerTlsConfig.ca.secret.withName

```ts
withName(name)
```

Name of the referent. More info: https://kubernetes.io/docs/concepts/overview/working-with-objects/names/#names TODO: Add other useful fields. apiVersion, kind, uid?

### fn spec.thanos.grpcServerTlsConfig.ca.secret.withOptional

```ts
withOptional(optional)
```

Specify whether the Secret or its key must be defined

## obj spec.thanos.grpcServerTlsConfig.cert

Struct containing the client cert file for the targets.

## obj spec.thanos.grpcServerTlsConfig.cert.configMap

ConfigMap containing data to use for the targets.

### fn spec.thanos.grpcServerTlsConfig.cert.configMap.withKey

```ts
withKey(key)
```

The key to select.

### fn spec.thanos.grpcServerTlsConfig.cert.configMap.withName

```ts
withName(name)
```

Name of the referent. More info: https://kubernetes.io/docs/concepts/overview/working-with-objects/names/#names TODO: Add other useful fields. apiVersion, kind, uid?

### fn spec.thanos.grpcServerTlsConfig.cert.configMap.withOptional

```ts
withOptional(optional)
```

Specify whether the ConfigMap or its key must be defined

## obj spec.thanos.grpcServerTlsConfig.cert.secret

Secret containing data to use for the targets.

### fn spec.thanos.grpcServerTlsConfig.cert.secret.withKey

```ts
withKey(key)
```

The key of the secret to select from.  Must be a valid secret key.

### fn spec.thanos.grpcServerTlsConfig.cert.secret.withName

```ts
withName(name)
```

Name of the referent. More info: https://kubernetes.io/docs/concepts/overview/working-with-objects/names/#names TODO: Add other useful fields. apiVersion, kind, uid?

### fn spec.thanos.grpcServerTlsConfig.cert.secret.withOptional

```ts
withOptional(optional)
```

Specify whether the Secret or its key must be defined

## obj spec.thanos.grpcServerTlsConfig.keySecret

Secret containing the client key file for the targets.

### fn spec.thanos.grpcServerTlsConfig.keySecret.withKey

```ts
withKey(key)
```

The key of the secret to select from.  Must be a valid secret key.

### fn spec.thanos.grpcServerTlsConfig.keySecret.withName

```ts
withName(name)
```

Name of the referent. More info: https://kubernetes.io/docs/concepts/overview/working-with-objects/names/#names TODO: Add other useful fields. apiVersion, kind, uid?

### fn spec.thanos.grpcServerTlsConfig.keySecret.withOptional

```ts
withOptional(optional)
```

Specify whether the Secret or its key must be defined

## obj spec.thanos.objectStorageConfig

ObjectStorageConfig configures object storage in Thanos. Alternative to ObjectStorageConfigFile, and lower order priority.

### fn spec.thanos.objectStorageConfig.withKey

```ts
withKey(key)
```

The key of the secret to select from.  Must be a valid secret key.

### fn spec.thanos.objectStorageConfig.withName

```ts
withName(name)
```

Name of the referent. More info: https://kubernetes.io/docs/concepts/overview/working-with-objects/names/#names TODO: Add other useful fields. apiVersion, kind, uid?

### fn spec.thanos.objectStorageConfig.withOptional

```ts
withOptional(optional)
```

Specify whether the Secret or its key must be defined

## obj spec.thanos.resources

Resources defines the resource requirements for the Thanos sidecar. If not provided, no requests/limits will be set

### fn spec.thanos.resources.withLimits

```ts
withLimits(limits)
```

Limits describes the maximum amount of compute resources allowed. More info: https://kubernetes.io/docs/concepts/configuration/manage-compute-resources-container/

### fn spec.thanos.resources.withLimitsMixin

```ts
withLimitsMixin(limits)
```

Limits describes the maximum amount of compute resources allowed. More info: https://kubernetes.io/docs/concepts/configuration/manage-compute-resources-container/

**Note:** This function appends passed data to existing values

### fn spec.thanos.resources.withRequests

```ts
withRequests(requests)
```

Requests describes the minimum amount of compute resources required. If Requests is omitted for a container, it defaults to Limits if that is explicitly specified, otherwise to an implementation-defined value. More info: https://kubernetes.io/docs/concepts/configuration/manage-compute-resources-container/

### fn spec.thanos.resources.withRequestsMixin

```ts
withRequestsMixin(requests)
```

Requests describes the minimum amount of compute resources required. If Requests is omitted for a container, it defaults to Limits if that is explicitly specified, otherwise to an implementation-defined value. More info: https://kubernetes.io/docs/concepts/configuration/manage-compute-resources-container/

**Note:** This function appends passed data to existing values

## obj spec.thanos.tracingConfig

TracingConfig configures tracing in Thanos. This is an experimental feature, it may change in any upcoming release in a breaking way.

### fn spec.thanos.tracingConfig.withKey

```ts
withKey(key)
```

The key of the secret to select from.  Must be a valid secret key.

### fn spec.thanos.tracingConfig.withName

```ts
withName(name)
```

Name of the referent. More info: https://kubernetes.io/docs/concepts/overview/working-with-objects/names/#names TODO: Add other useful fields. apiVersion, kind, uid?

### fn spec.thanos.tracingConfig.withOptional

```ts
withOptional(optional)
```

Specify whether the Secret or its key must be defined

## obj spec.web

WebSpec defines the web command line flags when starting Prometheus.

### fn spec.web.withPageTitle

```ts
withPageTitle(pageTitle)
```

The prometheus web page title