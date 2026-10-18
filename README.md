# CyberFortress - Projeto Integrador (SENAC)
> **Segurança em Camadas e Proteção Contra Ransomware para Clínica Médica**

![pfSense](https://img.shields.io/badge/pfSense-212B35?style=for-the-badge&logo=pfsense&logoColor=white)
![Windows Server](https://img.shields.io/badge/Windows_Server-0078D6?style=for-the-badge&logo=windows-server&logoColor=white)
![Debian](https://img.shields.io/badge/Debian_13-A80030?style=for-the-badge&logo=debian&logoColor=white)
![Zabbix](https://img.shields.io/badge/Zabbix-D21920?style=for-the-badge&logo=zabbix&logoColor=white)
![Grafana](https://img.shields.io/badge/Grafana-F46800?style=for-the-badge&logo=grafana&logoColor=white)
![TrueNAS](https://img.shields.io/badge/TrueNAS-0095D5?style=for-the-badge&logo=truenas&logoColor=white)

---

### Sobre o Projeto
A empresa fictícia "**CyberFortress**", foi desenvolvida no curso **Técnico em Segurança Cibernética no SENAC**. 

Criamos uma estrutura completa de segurança para uma **clínica médica**, protegendo o ambiente contra o vírus **Ransomware**, vazamento de dados e garantindo total adequação à **LGPD**.

---

### Situação Problema
- **Ameaça:** Invasão por vírus (Ransomware) após um funcionário abrir um e-mail falso (Phishing).
- **Impacto:** Perda de dados e arquivos bloqueados por falta de backups isolados.

---

### Soluções Práticas Implementadas

1. **Proteção de Borda & Rede (pfSense):**
   - **Dupla de Firewalls:** Se o firewall principal falhar, o secundário assume na hora sem derrubar a rede.
   - **Filtro de Tráfego:** Bloqueio automático de portas vulneráveis e sites/links maliciosos.
   - **Segurança de Conexão:** Bloqueio de roteadores não autorizados na rede interna.

2. **Monitoramento em Tempo Real (Zabbix + Grafana):**
   - Painel visual para acompanhar a saúde dos servidores, uso de memória e tráfego de rede.
   - Alertas rápidos caso algum computador ou servidor apresente problemas.

3. **Bloqueios & Permissões nos Computadores (Windows Server):**
   - Bloqueio total de pen drives (USB) para evitar entrada de vírus.
   - Desativação de funções antigas e vulneráveis do Windows.
   - Prontuários protegidos: apenas a equipe médica tem acesso aos arquivos dos pacientes.

4. **Recuperação de Dados & LGPD:**
   - **Cópia de Segurança Segura (Backup 3-2-1):** Cópias salvas em um servidor separado que o vírus não consegue alterar ou apagar.
   - Proteção rigorosa de dados sensíveis de saúde conforme exige a LGPD.

---

### 📐 Estrutura de Rede (IPs)
- **Rede Principal:** `192.168.1.0/24`
- **Firewall (pfSense):** `192.168.1.1`
- **Servidor do Domínio (Windows Server):** `192.168.1.10`
- **Servidor de Monitoramento (Zabbix / Grafana):** `192.168.1.20`
- **Recepção (VLAN 10):** Computadores limitados (USB e acessos remotos bloqueados).
- **Área Médica e Servidores (VLAN 20):** Acesso restrito aos prontuários e servidores.

---

### 👥 Equipe
- Giu Lacerda
- Isabely Pereira
- **Júlia Coelho**
- Luca Navarro
- Maria Vitória

---

### 🔗 Links
- 📄 **[Baixar o PDF da Apresentação (`cyberfortress (p.i).pdf`)](./cyberfortress%20(p.i).pdf)**
