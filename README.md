PR created from this branch to the main branch will perform devSecOps analysis on the following folders:

**src/MultipleRuleInTerraform/AWSTF**

*Expected risk:*

O03-I-SG

I01-I-SG

O02-I-SG

I07-I-SG

**src/MultipleRuleInTerraform/AZURETF**

*Expected risk:*

I01-I-NSG

O01-I-NSG

I07-I-NSG

I25-I-NSG

>To eliminate any risk from the rules please read "Recommendation" for the risk and then perform the step accordingly

*e.g.*

**Rule:**

-----------------------
Vendor: AWS

From Port: 0

To Port: 0

Ip Protocol: -1

Ip Range: 0.0.0.0/0

-------------------------------

**Risk triggered:** I01-I-SG

**Recommendation:** Restrict the rules to refer to only the source IPs and services you really use.

**Steps to perform:**

>Change the Ip Protocol to be specific for e.g. tcp(var.tcp_protocol)

>Change the Ip Range to be specific IP e.g. "192.168.10.11/32"(var.private_ip)