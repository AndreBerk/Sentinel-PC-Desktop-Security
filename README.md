Sentinel-PC (Desktop Security Watchdog)

Descrição Curta: Um porteiro digital automatizado para Windows. O Sentinel-PC monitora sua máquina em segundo plano, analisando usuários fantasmas, processos suspeitos e conexões de rede em tempo real, integrando-se à API do VirusTotal para bloquear ameaças antes que elas se instalem.

📌 Sobre o Projeto

O Sentinel-PC nasceu da necessidade de automatizar auditorias de segurança que normalmente são feitas manualmente. Em vez de o usuário precisar abrir o terminal (cmd), usar comandos como netstat ou vasculhar o Gerenciador de Tarefas diariamente, o Sentinel-PC faz isso de forma invisível e inteligente.

Ele atua como um "Vigia", rodando silenciosamente na bandeja do sistema (System Tray) e notificando o usuário imediatamente caso atividades anômalas (como a criação de um backdoor ou comunicação com IPs maliciosos) sejam detectadas.

🚀 Principais Funcionalidades

👤 Caçador de Usuários Fantasmas: Monitora constantemente o registro do Windows e o comando netplwiz para alertar sobre a criação de novas contas de Administrador não autorizadas.

🕵️ Verificador de Processos e Inicialização: Vasculha a inicialização do sistema em busca de executáveis ocultos, nomes aleatórios ou parasitas sem assinatura digital (ex: win_driver.exe rodando em plano de fundo).

🌐 Network Shield (Análise de Tráfego): Intercepta e analisa conexões TCP/UDP. Se sua máquina se comunicar com um IP desconhecido (especialmente com navegadores fechados), o IP é enviado automaticamente para análise.

🦠 Integração com VirusTotal: Checagem em tempo real da reputação de IPs estrangeiros usando a API do VirusTotal.

🔔 Alertas Nativos: Notificações instantâneas e um painel de acesso rápido (Dark Mode) na bandeja do sistema.

🛠️ Tecnologias Utilizadas

(Nota: Ajuste esta seção conforme a stack final escolhida)

Backend (Core/Serviço): Rust (Tauri) / C# (.NET) - Garante baixo consumo de RAM em background e acesso profundo às APIs do Windows.

Frontend (Interface): HTML5, Tailwind CSS, Vue.js / React - Para um Dashboard moderno, fluido e com gráficos dinâmicos.

Banco de Dados: SQLite - Armazenamento local e leve para logs e histórico de ameaças.

APIs Externas: VirusTotal API.

🖥️ Escopo das Telas (UI/UX)

Dashboard Principal: Resumo de integridade do sistema, gráficos de conexões e log contínuo de verificações.

Network (Rede): Tabela de IPs conectados no momento e seus respectivos Scores de Segurança. Opção para "Derrubar Conexão".

Startup & Processos: Lista detalhada do que inicia com seu PC, com indicativos visuais (verde/vermelho) para assinaturas digitais validadas.

Configurações: Inserção de chave de API, controle de tempo de varredura (ex: a cada 15 min) e preferências de notificação.


🤝 Como Contribuir

Contribuições são sempre bem-vindas! Se você tem ideias para novas regras de detecção ou melhorias na interface, siga os passos abaixo:

Faça um Fork do projeto.

Crie uma Branch para sua Feature (git checkout -b feature/IncrivelRecurso).

Adicione suas mudanças (git commit -m 'Adicionando um Incrível Recurso').

Faça o Push para a Branch (git push origin feature/IncrivelRecurso).

Abra um Pull Request.


Desenvolvido com 💻 e 🔒 para manter o seu PC seguro.
