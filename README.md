# AirPrint Server (CUPS + Avahi)

Este projeto configura um servidor de impressão **AirPrint** utilizando Docker Compose. Permite transformar impressoras antigas ou partilhadas em impressoras compatíveis com AirPrint, tornando-as visíveis e utilizáveis por dispositivos iOS (iPhone, iPad) e macOS na tua rede local.

Baseado na imagem: `chuckcharlie/cups-avahi-airprint`.

---

## 🚀 Requisitos Prévios

* **Docker** e **Docker Compose** instalados (ex: Synology NAS, QNAP, Linux, etc.).
* **Modo de Rede Host:** O container utiliza `network_mode: host` para que o serviço Avahi (mDNS) consiga transmitir o sinal AirPrint corretamente para a tua rede local.

---

## 🛠️ Instalação e Configuração

### 1. Preparar as Variáveis de Ambiente
Cria um ficheiro `.env` na mesma pasta do teu `docker-compose.yml` para guardar as credenciais de administração do CUPS de forma segura.

Exemplo de conteúdo do ficheiro `.env`:
```env
CUPSADMIN=o_teu_utilizador
CUPSPASSWORD=a_tua_palavra_passe
