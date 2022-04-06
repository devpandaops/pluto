# pluto
Automação do Microsoft Windows com o Ansible

### Visão geral

Use o Ansible para gerenciar e executar as funções básicas em ambientes Windows, incluindo atualizações de segurança e gerenciamento remoto por meio do WinRM. O Ansible precisa ser executado no Linux®, mas os administradores do Windows podem usá-lo para gerenciar e automatizar sistemas mesmo sem ter experiência no uso do terminal Linux.

O Ansible inclui um suporte nativo ao Windows que usa o PowerShel remoto que permite gerenciá-lo de uma maneira mais parecida com a que os administradores Windows estão habituados. 

O Red Hat® Ansible® Automation Platform oferece ferramentas modernas para o gerenciamento e a automação dos ambientes Microsoft Windows. Essa solução irá ajudá-lo a automatizar o provisionamento, implantar aplicações e gerenciar configurações em um ambiente com múltiplos fornecedores.

Com o suporte ao Windows do Red Hat Ansible Automation Platform, você pode:

- Instalar e desinstalar MSIs
- Ativar e desativar funcionalidades do Windows
- Iniciar, interromper e gerenciar serviços do Windows
- Criar e gerenciar usuários e grupos locais
- Gerenciar os pacotes do Windows por meio do Chocolatey
- Gerenciar e instalar atualizações do Windows
- Buscar arquivos de locais remotos
- Extrair e executar scripts do PowerShell

Quando você usa o Ansible para gerenciar o Windows, uma boa parte da sintaxe e das regras dos hosts Linux ou Unix também é aplicada a ele. No entanto, ainda há algumas diferenças com relação a componentes como separadores de caminhos e tarefas específicas de sistema operacional.

É necessário configurar o WinRM para que os servidores ou clientes do Windows possam ser acessados por meio da máquina de controle do Ansible. 

O script do PowerShell ConfigureRemotingForAnsible ajuda você a dar os primeiros passos com o Ansible nos seus ambientes de desenvolvimento e teste no Windows. Esse script configura o WinRM em todos os servidores ou clientes do Windows compatíveis.

A maioria dos módulos do Ansible foi criada para serviços web aleatórios e máquinas Linux. Como os módulos são escritos em Python, grande parte deles acaba não funcionando no Windows.

Por isso, use os módulos dedicados para o Windows que foram escritos no PowerShell e são executados em hosts do Windows. 

Também é possível criar seus próprios módulos ou usar os Ansible Playbooks para automatizar os sistemas do Windows e orquestrar tarefas. Esses playbooks são arquivos formatados em YAML que incluem um conjunto de configurações e tarefas para alcançar um estado final em um host do Ansible, Windows ou Linux. 

## Formas de automatizar sistemas Windows
### PowerShell
Incluído no Windows, o PowerShell é uma linguagem de script e shell de linha de comando baseado em tarefas. 

Use o Red Hat Ansible Automation Platform para automatizar novos sistemas do Windows, incluindo todas as funções .NET e DSC, sem precisar instalar outra linguagem de script.

#### Gerenciamento remoto do Windows (WinRM)
O WinRM é a tecnologia de gerenciamento remoto integrada e baseada em HTTP do Windows. Como ele oferece uma experiência de login não interativa, é difícil realizar tarefas como autenticação de salto duplo e atualizações do Windows. 

Com o Red Hat Ansible Automation Platform, você pode codificar a autenticação para automatizar tarefas de gerenciamento remoto no Windows.

#### Instalação e gerenciamento de aplicações
O Windows não inclui um sistema de gerenciamento de pacotes. Na verdade, ele utiliza a Microsoft Store para a distribuição e manutenção de aplicações. O problema é que ela é complicada de automatizar. 

O Red Hat Ansible Automation Platform oferece um módulo para automatizar o gerenciamento de pacotes básicos no Windows. Ele também pode ser integrado ao Chocolatey do Windows para você automatizar o gerenciamento de softwares e pacotes de maneira idempotente.

### Atualizações do Windows
O gerenciamento de atualizações é uma tarefa contínua. O Windows Update oferece atualizações de software para sistemas do Windows que são gerenciadas por muitas equipes de TI por meio do Microsoft System Center Configuration Manager (SCCM). 

No entanto, o SCCM não é a melhor ferramenta para as atualizações automatizadas, principalmente quando elas incluem reinicialização. Assim, fica mais cumprir os prazos de manutenção. 

Com o Red Hat Ansible Automation Platform, você realiza atualizações síncronas básicas por meio do Windows Update, aumentando a confiabilidade das atualizações automatizadas. Também é possível usar essa solução para gerenciar automaticamente as reinicializações intermediárias obrigatórias. Dessa forma, com apenas uma tarefa do Ansible, você instala centenas de atualizações.

## Treinamento sobre automação do Windows
### Microsoft Windows Automation with Red Hat Ansible Automation Platform
Neste curso, você aprende a automatizar tarefas de administração no Windows Server para viabilizar fluxos de trabalho de DevOps usando o Red Hat Ansible Automation Platform. 

Você usará o Ansible para escrever playbooks de automação que executem tarefas comuns de administração de sistemas do Microsoft Windows de modo reproduzível e em escala. Você também aprenderá a usar o controlador de automação para gerenciar e executar com segurança os Ansible Playbooks usando uma interface de usuário web central.

