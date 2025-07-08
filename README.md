# 🚀 **Vprofile Project**

> **Vprofile** is a social media web application designed to demonstrate DevOps concepts and best practices.  
> **Automated provisioning** and **environment setup** are powered by Vagrant for Windows, enabling quick deployment and management of a full-stack environment.

---

## ✨ **Features**

- 🧑‍💻 **User Management:** Registration, login, and profile editing  
- 💬 **Social Interactions:** Posts, comments, likes, and tags  
- 🔐 **Role-Based Access:** Admin/user roles with Spring Security  
- ⚡ **Performance:** Memcached caching  
- 📩 **Messaging:** RabbitMQ for async communication  
- 🎨 **Modern UI:** Responsive with Bootstrap & Font Awesome  
- ⚙️ **Easy Setup:** Automated Vagrant provisioning (Windows)

---

## 🛠️ **Technology Stack**

| **Layer**        | **Technologies**                                                        |
|------------------|-------------------------------------------------------------------------|
| Backend          | Java (Spring MVC, Spring Security, Spring Data JPA)                     |
| Frontend         | JSP, HTML, CSS, Bootstrap, Font Awesome                                 |
| Database         | MySQL                                                                   |
| Caching          | Memcached                                                               |
| Messaging        | RabbitMQ                                                                |
| Web Server       | Tomcat, Nginx                                                           |
| Provisioning     | Vagrant, Shell scripts                                                  |
| Build Tool       | Maven                                                                   |

---

## ⚡ **Prerequisites**

- [Vagrant](https://www.vagrantup.com/downloads)
- [VirtualBox](https://www.virtualbox.org/wiki/Downloads)
- [Git for Windows](https://git-scm.com/download/win)

---

## 🚦 **Getting Started (Windows)**

### 1️⃣ **Clone the Repository**

```sh
git clone https://github.com/KIRANMORAB/vprofile-project.git

```

### 2️⃣ **Start the Vagrant Environment**

Navigate to the provisioning folder and run:

```sh
cd vagrant/Automated_provisioning_WinMacIntel
```
```sh
vagrant plugin install vagrant-hostmanager
```
```sh
vagrant up
```


### 3️⃣ **Access the Application**

- **Web App:** [http://192.168.56.11](http://192.168.56.11) or [http://web01](http://web01)

| VM Name | Private IP      | Service               | Access Location / Port                                   |
| ------- | --------------- | --------------------- | -------------------------------------------------------- |
| `web01` | `192.168.56.11` | Nginx (Reverse Proxy) | [http://192.168.56.11](http://192.168.56.11)             |
| `app01` | `192.168.56.12` | Tomcat Server         | [http://192.168.56.12:8080](http://192.168.56.12:8080)   |
| `db01`  | `192.168.56.15` | MariaDB               | `mysql -h 192.168.56.15 -P 3306`                         |
| `mc01`  | `192.168.56.14` | Memcached             | `telnet 192.168.56.14 11211`                             |
| `rmq01` | `192.168.56.16` | RabbitMQ UI           | [http://192.168.56.16:15672](http://192.168.56.16:15672) |

### 4️⃣ **Stop the Environment**

```sh
vagrant halt
```

---

## 📁 **Project Structure**

```text
src/main/java/                       # Java source code
src/main/resources/                  # Application configs & SQL scripts
src/main/webapp/WEB-INF/views/       # JSP views
src/main/webapp/resources/           # Static assets (CSS, JS, images)
vagrant/Automated_provisioning_WinMacIntel/  # Vagrantfile & provisioning scripts
```

---

## 🗄️ **Database**

- MySQL is provisioned automatically.
- Schema and sample data loaded from:  
    `src/main/resources/db_backup.sql`

---

## 📄 **License**

This project is licensed under the **MIT License**.

---

<p align="center"><b>Vprofile</b> — DevOps</p>
