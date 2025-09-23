
---

## 🎯 Learning Objectives

By the end of this project, you should be able to:
- Draw diagrams of web infrastructures.
- Explain the role of each component in a web stack.
- Understand system redundancy and high availability.
- Identify Single Points of Failure (SPOF).
- Explain the difference between active-active and active-passive setups.
- Understand the basics of HTTPS, firewalls, and monitoring.

---

## 📚 Resources

**Read or watch:**
- [Network basics concept page](https://intranet.hbtn.io/concepts/33)
- [Server concept page](https://intranet.hbtn.io/concepts/67)
- [Web server concept page](https://intranet.hbtn.io/concepts/17)
- [DNS concept page](https://intranet.hbtn.io/concepts/12)
- [Load balancer concept page](https://intranet.hbtn.io/concepts/46)
- [Monitoring concept page](https://intranet.hbtn.io/concepts/13)
- [What is a database](https://www.oracle.com/database/what-is-database/)
- [What’s the difference between a web server and an app server?](https://wwwnginx.com/resources/glossary/web-server-vs-application-server/)
- [DNS record types](https://ns1.com/resources/dns-record-types)
- [Single point of failure](https://en.wikipedia.org/wiki/Single_point_of_failure)
- [How to avoid downtime when deploying new code](https://www.atlassian.com/continuous-delivery/principles/continuous-integration-and-deployment)
- [High availability cluster](https://en.wikipedia.org/wiki/High-availability_cluster)
- [What is HTTPS](https://www.cloudflare.com/learning/ssl/what-is-https/)
- [What is a firewall](https://www.cisco.com/c/en/us/products/security/firewalls/what-is-a-firewall.html)

---

## 📋 Requirements

- Each task includes a **diagram** (drawn on a whiteboard, paper, or software).
- Each task is documented in a **Markdown file** with explanations.
- All explanations are written in **English**.
- Screenshots of diagrams are uploaded to an image hosting service (e.g., Imgur) and linked in the answer files.
- Be concise and focus on what is asked. Avoid unnecessary details.

---

## 📌 Tasks

### **0. Simple Web Stack**
**Objective:** Design a one-server web infrastructure for `www.foobar.com`.

**Components:**
- 1 server with IP `8.8.8.8`.
- 1 web server (Nginx).
- 1 application server.
- 1 set of application files.
- 1 database (MySQL).
- 1 domain name `foobar.com` with a `www` record pointing to `8.8.8.8`.

**Explanations:**
- What is a server?
- Role of the domain name.
- Type of DNS record for `www.foobar.com`.
- Role of the web server (Nginx).
- Role of the application server.
- Role of the database.
- Communication protocol between the server and user.
- Issues with this infrastructure:
  - Single Point of Failure (SPOF).
  - Downtime during maintenance.
  - Scalability limitations.

**Files:**
- [0-simple_web_stack/0-simple_web_stack.md](0-simple_web_stack/0-simple_web_stack.md)
- Diagram: ![Simple Web Stack Diagram](0-simple_web_stack/diagram.png)

---

### **1. Distributed Web Infrastructure**
**Objective:** Design a three-server web infrastructure for `www.foobar.com`.

**Components:**
- 1 load balancer (HAproxy).
- 2 servers (each with Nginx, application server, application files, and MySQL).
- Primary-Replica (Master-Slave) database cluster.

**Explanations:**
- Why add a load balancer?
- Load balancer distribution algorithm.
- Active-Active vs. Active-Passive setup.
- How a Primary-Replica database cluster works.
- Issues with this infrastructure:
  - SPOF.
  - Security issues (no firewall, no HTTPS).
  - No monitoring.

**Files:**
- [1-distributed_web_infrastructure/1-distributed_web_infrastructure.md](1-distributed_web_infrastructure/1-distributed_web_infrastructure.md)
- Diagram: ![Distributed Web Infrastructure Diagram](1-distributed_web_infrastructure/diagram.png)

---

### **2. Secured and Monitored Web Infrastructure**
**Objective:** Design a three-server web infrastructure for `www.foobar.com` that is secured, serves encrypted traffic, and is monitored.

**Components:**
- 3 firewalls.
- 1 SSL certificate for HTTPS.
- 3 monitoring clients (e.g., Sumologic).

**Explanations:**
- Why add firewalls?
- Why serve traffic over HTTPS?
- Purpose of monitoring.
- How monitoring tools collect data.
- Issues with this infrastructure:
  - Terminating SSL at the load balancer.
  - Single MySQL server for writes.
  - Servers with identical components.

**Files:**
- [2-secured_and_monitored_web_infrastructure/2-secured_and_monitored_web_infrastructure.md](2-secured_and_monitored_web_infrastructure/2-secured_and_monitored_web_infrastructure.md)
- Diagram: ![Secured and Monitored Web Infrastructure Diagram](2-secured_and_monitored_web_infrastructure/diagram.png)

---

### **3. Scale Up**
**Objective:** Improve the infrastructure by scaling up.

**Components:**
- 1 additional server.
- Load balancer configured as a cluster.
- Separate components (web server, application server, database) on their own servers.

**Explanations:**
- Why add an additional server?
- Why configure the load balancer as a cluster?

**Files:**
- [3-scale_up/3-scale_up.md](3-scale_up/3-scale_up.md)
- Diagram: ![Scale Up Diagram](3-scale_up/diagram.png)

---

