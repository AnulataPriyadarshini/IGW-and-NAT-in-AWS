# IGW-and-NAT-in-AWS
Secure Dual-Zone Remote Access System Using IGW and NAT in AWS
# 🛡️ Secure Dual-Zone Remote Access System (AWS VPC with NAT & IGW)

This project demonstrates how to securely access two Windows EC2 instances in AWS using a public and private subnet setup. One instance has internet access via an Internet Gateway (IGW), while the other accesses the internet via a NAT instance. This is useful in corporate environments to isolate internal systems while maintaining controlled internet access.

---

## 🚀 Objective

- Deploy a custom VPC with public and private subnets.
- Configure a **NAT Instance** to allow outbound traffic from a private Windows EC2 instance.
- Demonstrate secure **RDP access** to both instances.

---

## 🧱 Architecture

- **VPC**: `10.0.0.0/16`
- **Public Subnet**: `10.0.1.0/24` with IGW and NAT instance
- **Private Subnet**: `10.0.2.0/24` with Windows EC2 (Worker)
- **Public EC2**: Admin Windows machine (RDP enabled)
- **Private EC2**: Worker machine (RDP via Public EC2)

---

## 🛠️ Services Used

- Amazon VPC
- Amazon EC2 (Windows)
- NAT Instance (custom setup)
- Internet Gateway (IGW)
- Route Tables and Subnets
- Elastic IP
- Security Groups

---

## 🔧 Setup Steps

### 1. Create VPC and Subnets
```bash
VPC CIDR: 10.0.0.0/16
Public Subnet: 10.0.1.0/24
Private Subnet: 10.0.2.0/24
