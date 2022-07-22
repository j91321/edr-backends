# EDR Backends


## Bitdefender GravityZone

**Backend:** MongoDB

**Reference:** [GravityZone virtual appliance](https://www.bitdefender.com/business/support/en/77212-87477-gravityzone-virtual-appliance.html)

## BlackBerry CylanceON-PREM

**Backend:** PostgreSQL

**Reference:** [CylanceON-PREM virtual appliance
](https://docs.blackberry.com/en/unified-endpoint-security/cylanceonprem/cylance-on-prem-administration-guide/Configure_CylanceON-PREM_Virtual_Appliance/External_Database_Overview)

## Crowdstrike

**Backend:** Splunk + Elasticsearch + Cassandra (possibly others)

**Reference:** [MITRE Evals Step Wizard Spider + Sandworm 7.A.4](https://attackevals.mitre-engenuity.org/enterprise/participants/crowdstrike?view=results&adversary=wizard-spider-sandworm&scenario=1&wizard-spider-sandwormdetection=7.A.4_0), [Reddit answer by Crowdstrike employee](https://www.reddit.com/r/Splunk/comments/b8oksl/what_dashboard_software_does_splunkcrowdstrike_use/)

## Elastic Security

**Backend:** Elasticsearch

**Reference:** Not needed 😀

## ESET Inspect

**Backend:** Microsoft SQL / MySQL

**Reference:** [ESET Inspect Software Requirements](https://help.eset.com/ei_deploy/1.7/en-US/index.html?database.html)

## Kaspersky Anti Targeted Attack Platform (KATA)

**Backend:** (Possibly) Elasticsearch

**Reference:** [MITRE Evaluations APT29 MSSP Steps](https://attackevals.mitre-engenuity.org/enterprise/participants/kaspersky?view=results&adversary=apt29&scenario=1&apt29detection=1.B.1_2), [KATA Distributed solution and multitenancy](https://support.kaspersky.com/KATA/4.1/en-US/194605.htm)

**Note:** Screenshots in MITRE Evals show that Kaspersky uses Elasticsearch for MSSP steps. This doesn't prove KATA itself uses Elasticsearch internaly. However KATA documentation mentions following: *The distributed solution is a two-tier hierarchy of servers with Central Node components installed. This structure sets apart a master control server known as the Primary Central Node (PCN) and slave servers known as Secondary Central Nodes (SCN). Interaction of servers requires connecting SCN to PCN.* This sound like Elasticsearch master and data nodes. 

## McAfee ePO (server for MVISION)

**Backend:** Microsoft SQL

**Reference:** [McAfee ePolicy Orchestrator 5.10.0 Product Guide](https://docs.trellix.com/bundle/epolicy-orchestrator-5.10.0-product-guide/page/GUID-5463D654-8EA6-473B-84A6-43A3F2C0187E.html)

**Note:** Old version reference, doesn't seem they still provide on-prem solution. So this may be outdated.

## Qualys Multi-Vector EDR 

**Backend:** Apache Lucene based (Possibly Elasticsearch/Solr or both) 

**References:** [Qualys Endpoint Detection and Response API](https://www.qualys.com/docs/qualys-edr-api-user-guide.pdf),  [Components of a QQL query](https://qualysguard.qg2.apps.qualys.com/portal-help/en/ud/qql_topics/components_of_a_qql_query.htm), [Investor Presentation](https://investor.qualys.com/static-files/76e233e8-bf59-4d24-99a8-49ccf609feee)

**Notes:** The query language used by Qualys is very similar to Lucene syntax, but with small quirks like backticks usage. Response examples in API manual also include field "score". The "Investor Presentation" mentions both Solr and Elasticsearch under *Analytics and Reporting Engines*.


## Sophos Intercept X

**Backend:** Trino.io (formerly PrestoSQL)

**Reference:** [Sophos schema viewer](https://docs.sophos.com/central/References/schemas/index.html)

**Note:** From Trino documentation: *Trino is a distributed SQL query engine designed to query large data sets distributed over one or more heterogeneous data sources.* The real database backend/backends can be anything that is supported by Trino and is hard to determine just from documentation. 

## Symantec Advanced Threat Protection: Endpoint

**Backend:** Elasticsearch 

**Reference:** [SYMANTEC EDR 4.6 HELP About the data migration process](https://techdocs.broadcom.com/us/en/symantec-security-software/endpoint-security-and-management/endpoint-detection-and-response/4-6/about-v96380626-d38e6/about-the-data-migration-process-v126294452-d38e12516.html)

## Trend Micro Endpoint Sensor server (older EDR)

**Backend:** Microsoft SQL

**Reference:** [Trend Micro Endpoint Sensor Update 6 Installation Guide](https://docs.trendmicro.com/all/ent/tmes/v1.6/en-us/tmes_1.6_update6_ig.pdf)

## Trend Micro One Vision

**Backend:** Apache Lucene based (Possible Elasticsearch or Solr)

**Reference:** [Trend Micro Vision One Search App](https://docs.trendmicro.com/en-us/enterprise/trend-micro-vision-one/common-apps/search-app.aspx)

**Note:** From the documentation: *The Search app provides different search methods, filters, and a Kibana-like query language to identify, categorize, and retrieve your search results.* By Kibana-like they mean Lucene as can be seen from syntax examples.

## VMware CarbonBlack EDR 

**Backend:** Apache Solr + Postgres + Redis + Hazelcast

**Reference:** [VMware Carbon Black EDR Server Technology Stack](https://docs.vmware.com/en/VMware-Carbon-Black-EDR/7.7/cb-edr-scm-guide/GUID-757AF3C1-516D-4D23-93CF-A8F8BCE07426.html)

**Notes:** Kudos to VMware for being the only vendor that provides clear view and diagrams of their technology stack.


## WithSecure Elements

**Backend:** Elasticsearch

**References:** [MITRE Evaluations Wizard Spider + Sandworm Step 11.A.4](https://attackevals.mitre-engenuity.org/enterprise/participants/withsecure?view=results&adversary=wizard-spider-sandworm&scenario=2&wizard-spider-sandwormdetection=11.A.4_0)


