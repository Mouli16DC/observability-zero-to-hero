**🔥 Core SRE Metrics (a.k.a. The Four Golden Signals)**
**1. Latency**

**Meaning:** Request-ku response vara eduthukura time.

**Example:** REST API /login ku 200ms average latency.

**Tanglish Notes:** User button click pannadhum, server response vara time measure pannum.

**Why Important:** Latency adhiga irundha → user frustration + revenue loss.

**2. Traffic**

Meaning: System handle panra total demand (requests/sec, QPS, TPS).

Example: Website-ku peak time 20k requests/sec.

Tanglish Notes: App-ku ethana user simultaneous ha use panraanga-nu traffic kandupidikkum.

Why Important: Scaling decisions traffic pattern base la pannuvom.

**3. Errors**

Meaning: Failure rate (HTTP 5xx, timeouts, validation fails).

Example: 2% requests timeout aagiradhu.

Tanglish Notes: App la bug irundha, illa DB down aana, error count spike aagum.

Why Important: Reliability ku direct impact. SLA/SLO measure errors la base panidum.

**4. Saturation**

Meaning: Resource utilization (CPU, memory, DB connections, thread pools).

Example: DB connections pool 95% usage.

Tanglish Notes: Car la full seat occupied madhiri, infra la full load aana performance drop.

Why Important: Saturation → latency & errors increase. Scaling ku trigger aagum.

**🔑 Additional SRE Metrics**
✅ Availability

% of successful requests (uptime).

Example: 99.95% SLA.

Tanglish Notes: Site user ku ethana percentage time available nu solludhu.

✅ Durability

Data integrity over time.

Example: S3 la “11 9’s durability”.

Tanglish Notes: Data enna nadandhaalum lose aakakoodadhu.

✅ SLI, SLO, SLA

SLI: Actual metric measure (e.g., 99.9% requests < 250ms).

SLO: Target goal (e.g., 99.95% uptime).

SLA: Business contract, break pannaa penalty.

Tanglish Notes: SLI = thermometer reading, SLO = target temperature, SLA = doctor guarantee.

✅ Error Budget

Allowed failure quota (100% - SLO).

Example: SLO 99.9% → 0.1% failure allowed.

Tanglish Notes: Kudukkura budget madhiri, adhula tha mistake panlaam.

**⚡ Deep Infra Metrics**

CPU Utilization → system busy ah iruka?

Memory Usage → leaks / cache overflow?

Disk IOPS & latency → storage bottleneck?

Network throughput → packets/sec, bandwidth.

Queue depth → background jobs pending count.

GC Pause (JVM apps) → latency spikes.

🎯 SRE Mindset

Only collect actionable metrics (noise avoid).

Metrics → Alerts → Incident response → Postmortem → Reliability improve.

Observability triangle = Metrics + Logs + Traces → Full picture.
