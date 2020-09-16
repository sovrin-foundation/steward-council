
# Metrics and Monitoring for Indy Networks

**Purpose of this document:**



*   Develop core metrics for Indy node and network operators against standards, policies, principles and contracts within the governance frameworks
*   Provide business and governance requirements to health workstream
*   Support process improvement of network operations 
    *   Fault Monitoring and alerting
    *   Steward Support Services
*   Support security - identify vulnerabilities, anomalies and alert for specific types of attack
*   Identify metrics to support development roadmap of a coherent and interoperable network of networks

**Background and Rationale **



*   The Sovrin Steward Council Health Workstream has been exploring data available via Indy Scan and Indy Node Monitor in order to measure individual node and network health and improve network operations.  
*   Many new Indy nodes and networks are under development with their own requirements to monitor nodes and their networks as a whole
*   Measuring in a consistent way helps network users at upper layers of ToIP stack choose the right networks to fit their business model, ecosystem or jurisdiction
*   Sovrin, Trust over IP and the Hyperledger communities have been working towards the development of SSI as a utility layer: an interoperable network of networks.
*   Measuring in a consistent way enables overall n/w of n/w’s monitoring and management

**Who are these metrics for?**

For this document we have only focused on the needs of Sovrin as a community of Stewards (Indy Node Operators) and as an Indy Network Operator and Governance Authority.  

However there are other other roles within the ecosystem that may use these metrics or may define their own metrics.  For example an Agency at layer 2 might select different networks based on specific networks for specific types of transactions.  Or an ecosystem might select a specific sub-set of the network of networks based on measures of decentralization or performance.  An ecosystem that is concerned with IoT for example will require very high throughput and capacity vs an ecosystem that is all about KYC for private banking will require lower capacity and performance but higher consensus and freshness.  Equally we may find other metrics that are useful in the future as we learn more from these data.

We have sub-divided the our uses of these metrics into 4 groups



1. **Node Operators.**  Focuses on node health and performance, fault monitoring, local security and conformance within the network
2. **Network Operations.**  This focuses on network health, fault monitoring, security, and technical roadmap
3. **Public Dashboard. ** It's important to demonstrate to network users, and others the health of the network and to be able to measure against performance of other SSI networks.  This builds confidence, trust and accountability
4. **Business. ** Whether a for profit of not for profit model, every network operator needs to be sustainable

**Categories of Metrics**

We have grouped the metrics into 4 Categories 



1. **Network Health** including Availability, Performance and Quality. Four of these metrics build on the Work of the Hyperledger Performance & Scale Working Group’s [white paper on metrics](https://www.hyperledger.org/wp-content/uploads/2018/10/HL_Whitepaper_Metrics_PDFVersion.pdf) October 2018.
2. **Business **primarily focused on uptake and usage, this category of measures over time will enable us to build patterns of usage and behaviours which in turn will help inform security as well as measures for business performance in building market adoption
3. **Governance Framework Compliance** this measures essential components of SSI such as Diversity and Decentralization, they are relevant to the role of Governance Authorities and attempt to measure some of the qualities of SSI.  



**Table of proposed metrics**


<table>
  <tr>
   <td><strong>Category</strong>
   </td>
   <td><strong>Measure</strong>
   </td>
   <td><strong>Node Operators</strong>
   </td>
   <td><strong>Network Operations</strong>
   </td>
   <td><strong>Public Dashboard</strong>
   </td>
   <td><strong>Business</strong>
   </td>
   <td><strong>How? / Notes</strong>
   </td>
  </tr>
  <tr>
   <td>Network Health: Capacity
   </td>
   <td>Availability % Uptime
   </td>
   <td>1
   </td>
   <td>1
   </td>
   <td>1
   </td>
   <td>1
   </td>
   <td>Monitor availability across nodes
<p>
Alerting
<p>
Current status (dashboard)
<p>
Steward response time
<p>
Trends
<p>
Correlate with events - upgrades, etc.
   </td>
  </tr>
  <tr>
   <td>Network Health: Capacity
   </td>
   <td>Capacity % utilisation
   </td>
   <td>
   </td>
   <td>1
   </td>
   <td>
   </td>
   <td>1
   </td>
   <td>Needed to support security controls and enable minimum permissible pricing as well as dimensioning / planning
   </td>
  </tr>
  <tr>
   <td>Network Health: Performance
   </td>
   <td>Read Latency
   </td>
   <td>1
   </td>
   <td>1
   </td>
   <td>
   </td>
   <td>
   </td>
   <td>Hyperledger Metric: = Time when response received – submit time
   </td>
  </tr>
  <tr>
   <td>Network Health: Performance
   </td>
   <td>Read Throughput
   </td>
   <td>1
   </td>
   <td>1
   </td>
   <td>
   </td>
   <td>
   </td>
   <td>Hyperledger Metric: = Total read operations / total time in seconds
   </td>
  </tr>
  <tr>
   <td>Network Health: Performance
   </td>
   <td>Transaction Latency
   </td>
   <td>1
   </td>
   <td>1
   </td>
   <td>
   </td>
   <td>
   </td>
   <td>Hyperledger Metric: = (Confirmation time @ network threshold) – submit time
   </td>
  </tr>
  <tr>
   <td>Network Health: Performance
   </td>
   <td>Transaction Throughput
   </td>
   <td>1
   </td>
   <td>1
   </td>
   <td>1
   </td>
   <td>
   </td>
   <td>Hyperledger Metric = Total committed transactions / total time in seconds @ #committed nodes
   </td>
  </tr>
  <tr>
   <td>Network Health: Quality
   </td>
   <td>Consensus
   </td>
   <td>1
   </td>
   <td>1
   </td>
   <td>1
   </td>
   <td>
   </td>
   <td>Monitor consensus across nodes;
<p>
Possible - monitor view change events
   </td>
  </tr>
  <tr>
   <td>Network Health: Quality
   </td>
   <td>Freshness
   </td>
   <td>1
   </td>
   <td>1
   </td>
   <td>1
   </td>
   <td>
   </td>
   <td>Freshness timestamp reported by each validator node.
   </td>
  </tr>
  <tr>
   <td>Network Health: Quality
   </td>
   <td>Reputation
   </td>
   <td>
   </td>
   <td>1
   </td>
   <td>
   </td>
   <td>1
   </td>
   <td>Future: Score nodes and (when in n/w of n/w’s) score network using Open Reputation where the node is the entity.  Could also apply to transaction endorsers etc https://github.com/SmithSamuelM/Papers/blob/master/whitepapers/open-reputation-low-level-whitepaper.pdf
   </td>
  </tr>
  <tr>
   <td>Business
   </td>
   <td>Usage # Writes
   </td>
   <td>
   </td>
   <td>
   </td>
   <td>
   </td>
   <td>1
   </td>
   <td>Indy Monitor - Track writes across ledgers
   </td>
  </tr>
  <tr>
   <td>Business
   </td>
   <td>Usage # Transaction Authors & Endorsers
   </td>
   <td>
   </td>
   <td>
   </td>
   <td>
   </td>
   <td>1
   </td>
   <td>Track TA and TE DIDs
   </td>
  </tr>
  <tr>
   <td>Business
   </td>
   <td>Uptake: # new TAs & TEs
   </td>
   <td>
   </td>
   <td>
   </td>
   <td>
   </td>
   <td>1
   </td>
   <td>Track TA and TE DIDs
   </td>
  </tr>
  <tr>
   <td>Governance Framework Compliance
   </td>
   <td>Diversity: Geo-location of Stewards and Nodes
   </td>
   <td>
   </td>
   <td>
   </td>
   <td>1
   </td>
   <td>1
   </td>
   <td>Diversity can be measured <a href="https://link.springer.com/chapter/10.1007/978-3-642-45030-3_13">https://link.springer.com/chapter/10.1007/978-3-642-45030-3_13</a>,  but diversity is measured against attributes we therefore need to identify elements which must be diversified both at a technical and organizational level, assign attributes (claims) against them and then use these types of metrics to measure diversity, this can be set at different levels as the network grows
   </td>
  </tr>
  <tr>
   <td>Governance Framework Compliance
   </td>
   <td>Diversity: Server / host type for Nodes
   </td>
   <td>
   </td>
   <td>
   </td>
   <td>1
   </td>
   <td>1
   </td>
   <td>See above: Geo IP lookup
   </td>
  </tr>
  <tr>
   <td>Governance Framework Compliance
   </td>
   <td>Sustainability: % Churn rate of Stewards
   </td>
   <td>
   </td>
   <td>1
   </td>
   <td>
   </td>
   <td>1
   </td>
   <td>Monitor Steward lifecycle in HubSpot
   </td>
  </tr>
  <tr>
   <td>Governance Framework Compliance
   </td>
   <td>Sustainability: Av. Cost / year to run a node
   </td>
   <td>1
   </td>
   <td>1
   </td>
   <td>
   </td>
   <td>1
   </td>
   <td>Qualitative annual Survey
   </td>
  </tr>
  <tr>
   <td>Governance Framework Compliance
   </td>
   <td>Decentralization: level of hierarchy or influence
   </td>
   <td>
   </td>
   <td>
   </td>
   <td>1
   </td>
   <td>1
   </td>
   <td>Measure heirarchy in networks<a href="https://arxiv.org/abs/1202.0191"> https://arxiv.org/abs/1202.0191</a>
<p>
Level of influence (there is a clever mathematical formula that enables you to measure levels of influence in networks, and a good deal of research in this domain eg <a href="http://dss.in.tum.de/files/bichler-research/2008_kiss_identification_of_influencers.pd">http://dss.in.tum.de/files/bichler-research/2008_kiss_identification_of_influencers.pd</a> f .
   </td>
  </tr>
</table>


**Future metrics to consider:**

In future, several factors several factors suggest that further metrics may be required:



1. High volumes of usage on individual networks may require a % capacity metric.  This could also support networking within a network of networks, pricing and security measures.
2. Operation of a network of networks (or grid) to build a global public utility layer may require the application of many of the above metrics by a governance authority at the ‘grid’ level (horizontally at layer 1 in the ToIP Stack vs vertically slice from layer 4 down)