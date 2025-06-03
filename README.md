# Utilizando o Jenkins no Ambiente Local (Ubuntu)

## 🔧 O que é o Jenkins?
O Jenkins é uma ferramenta de automação open source, voltada para Integração Contínua (CI) e Entrega Contínua (CD). Ele permite automatizar processos de desenvolvimento de software, como build, testes, deploy e entregas, tornando o ciclo de desenvolvimento mais ágil, eficiente e confiável.

---

## 🎯 Para que serve o Jenkins?
O Jenkins é utilizado principalmente para:

🔹 Automatizar tarefas recorrentes de desenvolvimento.

🔹 Executar pipelines de Integração Contínua e Entrega Contínua.

🔹 Compilar códigos automaticamente após cada alteração.

🔹 Executar testes automatizados.

🔹 Fazer deploy automático em servidores, containers ou ambientes de produção.

🔹 Melhorar a qualidade do código e acelerar a entrega de software.

---
## 💻 Subindo o Jenkins Localmente no Ubuntu
O Jenkins está sendo executado de forma local, diretamente no Ubuntu, podendo ser acessado na rede local ou, se configurado, através do IP público da máquina.

## Passo a Passo para Instalar e Subir o Jenkins no Ubuntu:
1️⃣ Atualizar pacotes do sistema:
```bash
sudo apt update && sudo apt upgrade -y
```
## 2️⃣ Instalar o Java (requisito do Jenkins):
```bash
sudo apt update && sudo apt install openjdk-17-jdk -y
```
## 3️⃣ Adicionar a chave do Jenkins e instalar:
```bash
sudo wget -O /usr/share/keyrings/jenkins-keyring.asc \
  https://pkg.jenkins.io/debian-stable/jenkins.io-2023.key
```

## 4️⃣ Adicione o repositório do Jenkins à lista de fontes do apt:
```bash
echo "deb [signed-by=/usr/share/keyrings/jenkins-keyring.asc] https://pkg.jenkins.io/debian-stable binary/" | sudo tee /etc/apt/sources.list.d/jenkins.list > /dev/null
```

## 5️⃣ Atualize a lista de pacotes e instale o Jenkins:
```bash
sudo apt-get update && sudo apt-get install -y jenkins
```

## 6️⃣ Chave de Segurança
Para obter a senha inicial de administrador do Jenkins, execute o comando:
```bash
sudo cat /var/lib/jenkins/secrets/initialAdminPassword
```

## 7️⃣ Iniciar e habilitar o serviço Jenkins:

```bash
sudo systemctl start jenkins
sudo systemctl enable jenkins

```

## 🌐 Acessando o Jenkins Localmente
🔗 O Jenkins, por padrão, roda na porta 8080. Para acessar, você pode usar:

Se estiver na mesma máquina:
```bash
http://localhost:8080
```
ou se quiser  Descobrir o IP Público do servidor
```bash
curl -4 ifconfig.me
```
Descobrir o IP Local (na rede local)
```bash
ip a
```

 <img src="https://github.com/user-attachments/assets/48fa648f-b961-4c50-bb52-acc59109fe9b" alt="Descrição da imagem" style="max-width:100%; height:auto;">
 <img src="https://github.com/user-attachments/assets/7a40bde2-f2e1-4c0f-910d-ac142baeee57" alt="Imagem" />

---

# 📌 Observações 

## Liberar portas necessárias
Se não estava liberado, rodou:
```bash
sudo ufw allow 8080
sudo ufw allow 80
sudo ufw allow 443
sudo ufw reload
```
