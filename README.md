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
