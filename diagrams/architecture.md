# Lab architecture

This conceptual diagram represents **NSG configuration**, not a live internet-reachable RDP service.

```mermaid
flowchart TB
    Untrusted["Untrusted IPv4 sources (conceptual)"]
    subgraph Azure["Azure for Students — East Asia"]
      subgraph VNet["vnet-security-lab | 10.10.0.0/16"]
        subgraph Subnet["snet-assessment | 10.10.1.0/24"]
          NSG["nsg-security-lab | associated NSG"]
          Empty["No VM, NIC, or public IP"]
        end
      end
    end
    Untrusted -. "Temporary allow TCP/3389 rule (deleted)" .-> NSG
    NSG -. "No workload or traffic test" .-> Empty
```

**Before:** A temporary inbound NSG rule allowed TCP/3389 from `0.0.0.0/0` at priority 100.

**After:** The test rule was deleted and zero custom inbound rules remained.

**Limit:** An NSG rule does not by itself make a VM or port reachable from the internet.
