---
aliases:
  - NF
---

The *Novan Firewall* (NF) is a passive defense mechanism integrated into all Novan androids and protects them against external hacking. The system works by using a large cryptographic device inside the [[Novan Heart]] that is heavily insulated to obscure the parameters against external scanning, and delivers a new cryptographic key for all components to use to decrypt the instructions on a short interval, typically a second.

The fast key refresh rate forces Novan androids to come up with powerful cryptographic devices to minimise the time validating the requests as well as 

## Hacking
Hacking the average Novan android requires a computing power of 1 *Novan Firewall*, which is an unit that updates as the average changes. The counterpart is the *Firewall Factor* (FF) which is how many *Novan Firewalls* are needed to hack. Most androids fall under the following categories:

|         Category          | Novan Firewall | Firewall Factor | Key Refresh Speed | Key Refresh Interval |
| :-----------------------: | -------------: | --------------: | ----------------: | -------------------: |
|          Average          |           0.03 |               1 |            850 μs |                  1 s |
|        Elite (avg)        |           0.04 |             1.6 |            750 μs |               0.95 s |
| [[Six Deadly Units\|SDU]] |           0.04 |             3.4 |            750 μs |               0.92 s |
|       [[Archivist]]       |           0.11 |             4.1 |            1.2 ms |                1.5 s |
|       [[Operator]]        |            2.4 |             3.2 |            120 μs |                  1 s |
|    [[ArchId Operator]]    |             64 |           114.7 |             25 μs |               0.18 s |
> [!IMPORTANT]
> The Key Refresh Interval (KRI) can be changed at the android's will, with no upper limit (very vulnerable but very reactive) but with a lower limit bound to the Key Refresh Speed (KRS) (less vulnerable but less reactive).
> 
> The system generates a new key before the interval, taking the KRS into account, however, the key synchronization is asynchronous and causes a minor downtime between actions, lasting as long as the Key Propagation Speed (KPS, typically  ~15 μs).

**Notable exceptions:**
- [[Aelia]] is part of the [[Six Deadly Units|SDU]] group, but has 0.74 NF and 3.8 FF.
- [[Iriss]] is part of the [[ArchId Operator]] group but has 271 NF, 3114 FF, a KRS of 150 ns, and a KPS of 5 ns. Her NF and FF increase when linked to [[ArchId Ring]].

Novan androids can counteract hacking by two means:
- Decreasing the Key Refresh Interval, as the FF is inversely proportional to it (half the KRI, double the FF).
- Forming a hive network with other androids. This works by requiring keys from everyone at once, increasing the FF proportionally with the number of androids, however, this has two drawbacks:
	- If one android is too far from the rest, the connection wouldn't be fast enough for the keys to be updated and thus their hive link will be broken.
	- All androids in the hive network must run at the same KRI for optimal results, as the desynchronization would cause higher downtime.