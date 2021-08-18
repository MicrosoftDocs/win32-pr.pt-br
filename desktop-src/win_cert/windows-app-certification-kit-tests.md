---
title: Testes do Kit de Certificação de Aplicativos Windows
description: Abaixo estão os detalhes do teste para certificar aplicativos dekstop.
ms.assetid: FA160F46-C266-4F89-B77F-166FEA9ED96B
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1b251104418e8eeff88d4d0188e34628b5ec1bf3b54015550084d4a0e9df567e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119086559"
---
# <a name="windows-app-certification-kit-tests"></a>Testes do Kit de Certificação de Aplicativos Windows

Abaixo estão os detalhes do teste para certificar aplicativos dekstop. Para obter informações, consulte [Using the Windows App Certification Kit](using-the-windows-app-certification-kit.md).

-   [Limpar instalação reversível](#clean-reversible-install)
-   [Instalar para o teste de pastas correto](#install-to-the-correct-folders-test)
-   [Teste de arquivo assinado digitalmente](#digitally-signed-file-test)
-   [Suporte ao teste de Windows x64](#support-x64-windows-test)
-   [Teste de verificação de versão do sistema operacional](#os-version-checking-test)
-   [Teste de UAC (controle de conta de usuário)](#user-account-control-uac-test)
-   [Aderir às mensagens do gerenciador de reinicialização do sistema](#adhere-to-system-restart-manager-messages)
-   [Cofre modo de teste](#safe-mode-test)
-   [Teste de sessão multiusuário](#multiuser-session-test)
-   [Teste de falhas e travamentos](#crashes-and-hangs-test)
-   [Teste de compatibilidade e resiliência](#compatibility-and-resiliency-test)
-   [Segurança do Windows melhores práticas de teste](#windows-security-best-practices-test)
-   [Teste dos recursos de segurança do Windows](#windows-security-features-test)
-   [Teste de DPI alto](#high-dpi-test)

## <a name="clean-reversible-install"></a>Limpar instalação reversível

Instala e desinstala o aplicativo e verifica se há arquivos residuais e entradas do Registro.

-   Segundo plano
    -   Uma instalação limpa e reversível permite que os usuários implantem e removam aplicativos. Para passar nesse teste, o aplicativo deve fazer o seguinte:
        -   O aplicativo não força o sistema a reiniciar imediatamente após a instalação ou desinstalação do aplicativo. *O processo de instalação ou desinstalação de um aplicativo nunca deve exigir uma reinicialização do sistema logo após a conclusão. Se isso exigir que o sistema seja reiniciado, os usuários deverão ser capazes de reiniciar o sistema em sua conveniência.*
        -   O aplicativo não depende de nomes de arquivo curtos (SFN) 8.3. *Os processos de instalação e desinstalação do aplicativo devem ser capazes de usar nomes de arquivo longos e caminhos de pasta.*
        -   O aplicativo não bloqueia a instalação/desinstalação silenciosa
        -   O aplicativo faz as entradas necessárias no registro do sistema. *Windows ferramentas de inventário e ferramentas de telemetria exigem informações completas sobre aplicativos instalados. Os instaladores de aplicativos devem criar as entradas corretas do Registro para permitir a detecção e desinstalações bem-sucedidas.*
    -   Se você estiver usando um instalador baseado em MSI, o MSI criará automaticamente as entradas do Registro abaixo. Se você não estiver usando um instalador MSI, o módulo de instalação deverá criar as seguintes entradas do Registro durante a instalação:
        -   DisplayName
        -   InstallLocation
        -   Publisher
        -   UninstallString
        -   VersionMajor ou MajorVersion
        -   VersionMinor ou MinorVersion
    -   O aplicativo deve remover todas as suas entradas em Adicionar/Remover Programas.
-   Detalhes do teste
    -   Esse teste verifica os processos de instalação e desinstalação do aplicativo quanto ao comportamento necessário.
-   Ação corretiva
    -   Revise o design e o comportamento do aplicativo em relação aos requisitos descritos acima.

## <a name="install-to-the-correct-folders-test"></a>Instalar para o teste de pastas correto

Verifica se o aplicativo grava seu programa e arquivos de dados nas pastas corretas.

-   Segundo plano
    -   Os aplicativos devem usar o sistema e as pastas por usuário corretamente para que possam acessar os dados e as configurações de que precisam enquanto protegem os dados e as configurações do usuário contra acesso não autorizado.
-   Pastas de Arquivos de Programas
    -   O aplicativo deve ser instalado na pasta Arquivos de Programas por padrão (%ProgramFiles% para aplicativos nativos de 32 bits e 64 bits e %ProgramFiles(x86)% para aplicativos de 32 bits em execução no x64).
    -   **Observação:** O aplicativo não deve armazenar dados do usuário ou dados do aplicativo em uma pasta Arquivos de Programas devido às permissões de segurança configuradas para essa pasta.
    -   As ACLs nas Windows do sistema permitem que somente contas de administrador leiam e escrevam neles. Como resultado, as contas de usuário padrão não terão acesso a essas pastas. A virtualização de arquivos, no entanto, permite que os aplicativos armazenem um arquivo, como um arquivo de configuração, em um local do sistema que normalmente pode ser escrito somente por administradores. A execução de programas como um usuário padrão nessa situação poderá resultar em falha se eles não puderem acessar um arquivo necessário.
    -   Os aplicativos [devem usar Pastas Conhecidas](/previous-versions/windows/desktop/legacy/bb776911(v=vs.85)) para garantir que eles poderão acessar seus dados.
    -   **Observação: Windows** virtualização de arquivos para melhorar a compatibilidade do aplicativo e eliminar problemas quando os aplicativos são executados como um usuário padrão no Windows. Seu aplicativo não deve contar com a virtualização presente em versões futuras do Windows.
-   Pastas de dados de aplicativo específicas do usuário
    -   Em instalações "por computador", o aplicativo não deve gravar dados específicos do usuário durante a instalação. Os dados de instalação específicos do usuário só devem ser gravados quando um usuário inicia o aplicativo pela primeira vez. Isso porque não há nenhum local de usuário correto no qual armazenar dados no momento da instalação. As tentativas de um aplicativo de modificar comportamentos de associação padrão em um nível de computador após a instalação não serão bem-sucedidas. Em vez disso, os padrões devem ser reivindicados em um nível por usuário, o que impede que vários usuários sobrescrevam os padrões uns dos outros.
    -   Todos os dados do aplicativo exclusivos para um usuário específico e não devem ser compartilhados com outros usuários do computador devem ser armazenados em Usuários \\ <username> \\ AppData.
    -   Todos os dados do aplicativo que devem ser compartilhados entre os usuários no computador devem ser armazenados em ProgramData.
-   Outras pastas do sistema e chaves do Registro
    -   O aplicativo nunca deve gravar diretamente no diretório Windows e ou subdireários. Use os métodos corretos para instalar arquivos, como fontes ou drivers, nesses diretórios.
    -   Os aplicativos não devem iniciar automaticamente na inicialização, por exemplo, adicionando uma entrada a um ou mais desses locais:
        -   Chaves de run do Registro HKLM e ou HKCU em Software \\ Microsoft \\ Windows \\ CurrentVersion
        -   Chaves de run do Registro HKLM e ou HKCU em Software \\ Wow6432Nãode \\ Microsoft \\ windows \\ CurrentVersion
        -   Iniciar Menu TodosProgramas > INICIALIZAÇÃO
-   Detalhes do teste
    -   Este teste verifica se o aplicativo usa os locais específicos no sistema de arquivos que o Windows fornece para armazenar programas e componentes de software, dados de aplicativo compartilhados e dados de aplicativo específicos para um usuário.
-   Ações corretivas
    -   Revise como o aplicativo usa as pastas do sistema e certifique-se de que ele as está usando corretamente.
-   Exceções e exceções
    -   Uma isenção é necessária para aplicativos da área de trabalho que escrevem no GAC (cache de assembly global) (os aplicativos .NET devem manter as dependências de assembly privadas e armazená-los no diretório do aplicativo, a menos que o compartilhamento de um assembly seja explicitamente necessário).
    -   A instalação na pasta Arquivos de Programas não é um requisito para que os pacotes SW da Área de Trabalho alcancem o Logotipo sw, somente na categoria Conceitos básicos da SW.

## <a name="digitally-signed-file-test"></a>Teste de arquivo assinado digitalmente

Testa arquivos executáveis e drivers de dispositivo para verificar se eles têm uma assinatura digital válida.

-   Segundo plano
    -   Arquivos assinados digitalmente possibilitam verificar se o arquivo é original e detectar se o arquivo foi adulterado.
    -   A imposição de assinatura de código no modo kernel é Windows recurso que também é conhecido como CI (integridade de código). A CI melhora a segurança do Windows verificando a integridade de um arquivo sempre que ele é carregado na memória. A CI detecta se o código mal-intencionado modificou um arquivo binário do sistema e gera um evento de log de diagnóstico e auditoria do sistema quando a assinatura de um módulo de kernel falha ao verificar corretamente.
    -   Se o aplicativo exigir permissões elevadas, o prompt de elevação exibirá informações contextuais sobre o arquivo executável que está solicitando acesso elevado. Dependendo se o aplicativo for assinado por Authenticode, o usuário poderá ver o prompt de consentimento ou o prompt de credencial.
    -   Nomes fortes impedem que terceirosofem seu código, desde que você mantenha a chave privada segura. O .NET Framework verifica a assinatura digital ao carregar o assembly ou instalá-lo no GAC. Sem acesso à chave privada, um usuário mal-intencionado não pode modificar seu código e assino-o novamente.
-   Detalhes do teste
    -   Todos os arquivos executáveis, como aqueles com extensões de arquivo do .exe, .dll, .ocx, .sys, .cpl, .drv e .scr, devem ser assinados com um certificado Authenticode.
    -   Todos os drivers de modo kernel instalados pelo aplicativo devem ter uma assinatura da Microsoft obtida por meio do programa WHQL ou DRS. Todos os drivers de filtro do sistema de arquivos devem ser assinados por WHQL.
-   Ação corretiva
    -   Assine os arquivos executáveis do aplicativo.
    -   Use makecert.exe para gerar um certificado ou obter uma chave de assinatura de código de uma das autoridades de certificação comerciais (CAs), como VeriSign, Thawte ou uma AC da Microsoft.
-   Exceções e exceções
    -   As isenções serão consideradas apenas para redistribuíveis de terceiros não assinados. Uma prova de comunicação solicitando uma versão assinada dos redistribuíveis é necessária para que essa isenção seja concedida.
    -   Os pacotes de software adicionados ao valor do dispositivo são isentos da certificação do driver de modo kernel, pois os drivers devem ser certificados no Windows de Hardware.

## <a name="support-x64-windows-test"></a>Suporte ao teste de Windows x64

Teste o aplicativo para garantir que o .exe seja criado para a arquitetura da plataforma na qual ele será instalado.

-   Segundo plano
    -   O arquivo executável deve ser criado para a arquitetura do processador na qual ele está instalado. Alguns arquivos executáveis podem ser executados em uma arquitetura de processador diferente, mas isso não é confiável.
    -   A compatibilidade de arquitetura é importante porque processos de 32 bits não podem carregar DLLs de 64 bits e processos de 64 bits não podem carregar DLLs de 32 bits. Da mesma forma, as versões de 64 bits do Windows não são suportadas para a execução de aplicativos baseados em Windows de 16 bits porque os alças têm 32 bits significativos em Windows de 64 bits, de modo que não possam ser passados para aplicativos de 16 bits. Portanto, tentar iniciar um aplicativo de 16 bits falhará em versões de 64 bits do Windows.
    -   Drivers de dispositivo de 32 bits não podem ser executados em versões de 64 bits do Windows e, portanto, eles devem ser portados para a arquitetura de 64 bits.
    -   Para aplicativos de modo de usuário, o Windows de 64 bits inclui o WOW64, que permite que aplicativos Windows de 32 bits executem em sistemas que executam Windows de 64 bits, embora com alguma perda de desempenho. Não existe nenhuma camada de conversão equivalente para drivers de dispositivo.
    -   Para manter a compatibilidade com versões de 64 bits do Windows, os aplicativos devem dar suporte nativo a 64 bits ou, no mínimo, aplicativos baseados em Windows de 32 bits devem ser executados perfeitamente em sistemas de 64 bits:
        -   Os aplicativos e seus instaladores não contêm nenhum código de 16 bits nem dependem de nenhum componente de 16 bits.
        -   A instalação do aplicativo deve detectar e instalar os drivers e componentes adequados em versões de 64 bits do Windows.
        -   Todos os plug-ins de shell devem ser executados em versões de 64 bits do Windows.
        -   Os aplicativos executados no emulador WoW64 não devem tentar ignorar mecanismos de virtualização Wow64. Se houver cenários específicos em que os aplicativos precisem detectar se estão em execução em um emulador WoW64, eles deverão fazer isso chamando [**IsWow64Process**](/windows/desktop/api/wow64apiset/nf-wow64apiset-iswow64process).
-   Detalhes do teste
    -   O aplicativo não deve instalar binários de 16 bits. O aplicativo não deve instalar um driver de modo kernel de 32 bits se ele deve ser executado em um computador de 64 bits.
-   Ações Corretivas
    -   Crie os arquivos executáveis e drivers para a arquitetura do processador para a qual você deseja instalá-los.

## <a name="os-version-checking-test"></a>Teste de verificação de versão do sistema operacional

Testa como o aplicativo verifica a versão do Windows na qual ele está em execução.

-   Segundo plano
    -   Os aplicativos verificam a versão do sistema operacional testando uma versão maior ou igual à versão necessária para garantir a compatibilidade com versões futuras do Windows.
-   Detalhes do teste
    -   Simula a execução do aplicativo em diferentes versões do Windows para ver como ele reage.
-   Ações corretivas
    -   Teste a versão correta do Windows testando se a versão atual é maior ou igual à versão de que seu aplicativo, serviço ou driver precisa.
    -   Os instaladores de driver e os módulos de desinstalação nunca devem verificar a versão do sistema operacional.
-   Exceções e exceções
    -   As isenções serão consideradas para aplicativos que atendem aos seguintes *critérios: (Aplica-se somente à certificação de aplicativo da área de trabalho)*
        -   Aplicativos que são entregues como um pacote executado no Windows XP, Windows Vista e Windows 7 e precisam verificar a versão do sistema operacional para determinar quais componentes instalar em um determinado sistema operacional.
        -   Aplicativos que verificam apenas a versão mínima do sistema operacional (somente durante a instalação, não em runtime) usando apenas as chamadas à API aprovadas e listam o requisito mínimo de versão no manifesto do aplicativo, conforme necessário.
        -   Aplicativos de segurança, como aplicativos antivírus e firewall, utilitários do sistema, como utilitários de desfragmentação e aplicativos de backup, e ferramentas de diagnóstico que verificam a versão do sistema operacional usando apenas as chamadas à API aprovadas.

## <a name="user-account-control-uac-test"></a>Teste de UAC (controle de conta de usuário)

Testa o aplicativo para verificar se ele não precisa de permissões elevadas desnecessariamente para ser executado.

-   Segundo plano
    -   Um aplicativo que opera ou instala somente quando o usuário é um administrador força os usuários a executar o aplicativo com permissões elevadas desnecessariamente, o que pode permitir que o malware entre no computador do usuário.
    -   Quando os usuários são sempre forçados a executar aplicativos com tokens de acesso elevados, o aplicativo pode ser servidor como um ponto de entrada para código ofensivo ou mal-intencionado. Esse malware pode modificar facilmente o sistema operacional ou, pior ainda, afetar outros usuários. É quase impossível controlar um usuário que tem acesso completo de administrador, pois os administradores podem instalar aplicativos e executar qualquer aplicativo ou script no computador. Os gerentes de IT estão sempre buscando maneiras de criar "áreas de trabalho padrão" em que os usuários fazem logoff como usuários padrão. As áreas de trabalho padrão reduzem consideravelmente os custos do suporte ajuda e reduzem a sobrecarga de IT.
    -   A maioria dos aplicativos não exige privilégios de administrador em tempo de executar. Uma conta de usuário padrão deve ser capaz de executar. Windows aplicativos devem ter um manifesto (inserido ou externo) para definir seu nível de execução que informa ao sistema operacional os privilégios necessários para executar o aplicativo. O manifesto do aplicativo se aplica somente a arquivos .exe, não .dll arquivos. O UAC (Controle de Conta de Usuário) não inspeciona DLLs durante a criação do processo. As regras de UAC não se aplicam a serviços Microsoft. O manifesto do aplicativo pode ser inserido ou externo.
    -   Para criar um manifesto, crie um arquivo com o nome <nome do aplicativo>.exe.manifest e armazene-o \_ no mesmo diretório que EXE. Observe que qualquer manifesto externo será ignorado se o aplicativo tiver um manifesto interno.
        -   Por exemplo, <requestedExecutionLevel level=""asInvoker \| highestAvailable \| requireAdministrator"" uiAccess="true \| false""/>
        -   O processo principal do aplicativo deve ser executado como um usuário padrão (**asInvoker**). Todos os recursos administrativos devem ser movidos para um processo separado que é executado com privilégios administrativos.
        -   Os aplicativos voltados para o usuário que exigem privilégios elevados devem ser assinados pelo Authenticode.
-   Detalhes do teste
    -   Todos os exes voltados para o usuário devem ser marcados com o atributo asInvoker. Se eles são marcados como highestAvailable ou requireAdministrator, eles devem ser autenticados corretamente. Qualquer aplicativo exe não deve ter o atributo uiAccess definido como true. Qualquer exe executado como um serviço é excluído dessa verificação específica.
-   Ações corretivas
    -   Revise o arquivo de manifesto do aplicativo para ver as entradas e os níveis de permissão corretos.
-   Exceções e exceções
    -   Uma isenção é necessária para aplicativos que executem seu processo principal com privilégios elevados **(requireAdministrator** ou **highestAvailable).** O processo principal é o processo que fornece o ponto de entrada do usuário para o aplicativo.
    -   As isenções serão consideradas para os seguintes cenários:
        -   Ferramentas administrativas ou do sistema com nível de execução definido como **highestAvailable**, **requireAdministrator** ou ambos.
        -   Somente o aplicativo de estrutura de automação de acessibilidade ou de automação de interface do usuário define o sinalizador uiAccess como TRUE para ignorar o UIPI (isolamento de privilégio de interface do usuário). Para iniciar corretamente a utilização do aplicativo, esse sinalizador deve ser assinado por Authenticode e deve residir em um local protegido no sistema de arquivos, como Arquivos de Programas.

## <a name="adhere-to-system-restart-manager-messages"></a>Aderir às mensagens do gerenciador de reinicialização do sistema

Testa como o aplicativo responde às mensagens de desligamento e reinicialização do sistema.

-   Segundo plano
    -   Os aplicativos devem sair o mais rápido possível quando são notificados de que o sistema está sendo desligado para fornecer uma experiência de desligamento responsivo ou de desligamento para o usuário.
    -   Em um desligamento crítico, os aplicativos que retornam FALSE para [**WM \_ QUERYENDSESSION**](/windows/desktop/Shutdown/wm-queryendsession) serão enviados **WM \_ ENDSESSION** e fechados, enquanto aqueles que se desempenham em resposta a WM QUERYENDSESSION serão encerrados à \_ força.
-   Detalhes do teste
    -   Examina como o aplicativo responde às mensagens de desligar e sair.
-   Ações corretivas
    -   Se o aplicativo falhar neste teste, revise como ele lida com essas Windows mensagens:
        -   [**WM \_ QUERYENDSESSION**](/windows/desktop/Shutdown/wm-queryendsession) com *LPARAM*  =  **ENDSESSION \_ CLOSEAPP**(0x1): os aplicativos da área de trabalho devem responder (TRUE) imediatamente na preparação para uma reinicialização. Os aplicativos de console [**podem chamar SetConsoleCtrlHandler para**](/windows/console/setconsolectrlhandler) receber notificação de desligamento. Os serviços podem [**chamar RegisterServiceCtrlHandlerEx para**](/windows/desktop/api/winsvc/nf-winsvc-registerservicectrlhandlerexa) receber notificações de desligamento em uma rotina de manipulador.
        -   [**WM \_ ENDSESSION**](/windows/desktop/Shutdown/wm-queryendsession) com *LPARAM*  =  **ENDSESSION \_ CLOSEAPP**(0x1): os aplicativos devem retornar um valor 0 dentro de 30 segundos e desligar. No mínimo, os aplicativos devem se preparar salvando todos os dados do usuário e informando as informações necessárias após uma reinicialização.
    -   Os aplicativos de console que recebem a **notificação DE \_ \_ EVENTO CTRL C** devem ser desligados imediatamente. Os drivers não devem vetar um evento de desligamento do sistema.
    -   **Observação:** Os aplicativos que devem bloquear o desligamento devido a uma operação que não pode ser interrompida devem usar [**ShutdownBlockReasonCreate**](/windows/desktop/api/winuser/nf-winuser-shutdownblockreasoncreate) para registrar uma cadeia de caracteres que explica o motivo para o usuário. Quando a operação for concluída, o aplicativo deverá chamar [**ShutdownBlockReasonDestroy**](/windows/desktop/api/winuser/nf-winuser-shutdownblockreasondestroy) para indicar que o sistema pode ser desligado.

## <a name="safe-mode-test"></a>Cofre modo de teste

Testa se o driver ou serviço está configurado para iniciar no modo de segurança.

-   Segundo plano
    -   Cofre modo permite aos usuários diagnosticar e solucionar problemas com Windows. Somente drivers e serviços necessários para a operação básica do sistema operacional ou fornecer serviços de diagnóstico e recuperação devem ser carregados no modo de segurança. Carregar outros arquivos no modo de segurança torna mais difícil solucionar problemas com o sistema operacional.
    -   Por padrão, somente os drivers e serviços que vêm pré-instalados com Windows iniciam no modo de segurança. Todos os outros drivers e serviços devem ser desabilitados, a menos que o sistema os exija para operações básicas ou para fins de diagnóstico e recuperação.
-   Detalhes do teste
    -   Os drivers instalados pelo aplicativo não devem ser marcados para carregamento no modo de segurança.
-   Ações corretivas
    -   Se o driver ou o serviço não deve iniciar no modo de segurança, remova as entradas do aplicativo das chaves do registro.
-   Exceções e renúncias
    -   Os drivers e serviços que devem iniciar no modo de segurança exigem que uma renúncia seja certificada. A solicitação de renúncia deve incluir cada driver e serviço para adicionar às chaves do registro de inicialização segura e descrever os motivos técnicos para o motivo de o driver ou serviço precisar ser executado no modo de segurança. O instalador do aplicativo deve registrar todos esses drivers e serviços nessas chaves do registro:
        -   HKLM/sistema/CurrentControlSet/Control/segura/mínima
        -   HKLM/sistema/CurrentControlSet/Control/adsegural/rede
-   **Observação:** Você deve testar os drivers e serviços que deseja iniciar no modo de segurança para garantir que eles funcionem no modo de segurança sem erros.

## <a name="multiuser-session-test"></a>Teste de sessão multiusuário

Teste como o aplicativo se comporta quando executado em várias sessões ao mesmo tempo.

-   Segundo plano
    -   Windows os usuários devem ser capazes de executar sessões simultâneas. Os aplicativos devem garantir que, quando executados em várias sessões, seja local ou remotamente, a funcionalidade normal do aplicativo não seja afetada negativamente. As configurações do aplicativo e os arquivos de dados devem ser específicos do usuário e a privacidade e as preferências do usuário devem ser restritas à sessão do usuário.
-   Detalhes do teste
    -   Executa várias instâncias simultâneas do aplicativo para testar o seguinte:
        -   Várias instâncias de um aplicativo em execução ao mesmo tempo são isoladas umas das outras.
    -   Isso significa que os dados do usuário de uma instância não são visíveis para outra instância. O som em uma sessão de usuário inativa não deve ser ouvido em uma sessão de usuário ativa. Nos casos em que várias instâncias de aplicativo usam recursos compartilhados, o aplicativo deve garantir que não haja um conflito.
        -   Se o aplicativo tiver sido instalado para vários usuários, ele armazenará dados nas pastas e locais de registro corretos.
        -   O aplicativo pode ser executado em várias sessões de usuário (troca rápida de usuário) tanto para acesso local quanto remoto.
    -   Para garantir isso, o aplicativo deve verificar outras sessões de TS (serviço de terminal) para instâncias existentes do aplicativo. Se o aplicativo não oferecer suporte a várias sessões de usuário ou acesso remoto, ele deverá dizer claramente isso ao usuário quando ele for iniciado a partir de uma sessão desse tipo.
-   Ação Corretiva
    -   Certifique-se de que o aplicativo não armazene arquivos de dados de todo o sistema ou configurações em armazenamentos de dados específicos do usuário, como perfil do usuário ou HKCU. Se isso ocorrer, essas informações não estarão disponíveis para outros usuários.
    -   Seu aplicativo deve instalar arquivos de configuração e de dados de todo o sistema durante a instalação e criar os arquivos e as configurações específicas do usuário após a instalação quando um usuário o executa.
    -   Certifique-se de que o aplicativo não bloqueie várias sessões simultâneas, seja localmente ou remotamente. O aplicativo não deve depender de mutexes globais ou outros objetos nomeados para verificar ou bloquear várias sessões simultâneas.
    -   Se o aplicativo não puder permitir várias sessões simultâneas por usuário, use namespaces por usuário ou por sessão para mutexes e outros objetos nomeados.

## <a name="crashes-and-hangs-test"></a>Teste de panes e travamentos

Monitora o aplicativo durante o teste de certificação para registrar quando ele falha ou trava.

-   Tela de fundo
    -   Falhas de aplicativo, como panes e suspensões, são uma grande interrupção para os usuários e causam frustração. A eliminação dessas falhas melhora a estabilidade e a confiabilidade do aplicativo e, em geral, oferece aos usuários uma experiência de aplicativo melhor. Aplicativos que param de responder ou travam podem provocar a perda de dados do usuário ou uma experiência insatisfatória.
-   Detalhes do teste
    -   Testamos a resiliência e a estabilidade do aplicativo por meio do teste de certificação.
    -   o Kit de certificação de aplicativo Windows chama [**IApplicationActivationManager:: ActivateApplication**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iapplicationactivationmanager-activateapplication) para iniciar Windows aplicativos da loja. Para que o **ActivateApplication** inicie um aplicativo, o UAC (Controle de Conta de Usuário) deve estar habilitado, e a resolução da tela deve ser de pelo menos 1024 x 768 ou 768 x 1024. Se nenhuma condição for atendida, o aplicativo falhará nesse teste.
-   Ações Corretivas
    -   Verifique se o UAC está habilitado no computador de teste.
    -   Verifique se você está executando o teste em um computador com uma tela grande o suficiente.
    -   Se o aplicativo falhar para iniciar e sua plataforma de teste satisfizer os pré-requisitos do [**ActivateApplication**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iapplicationactivationmanager-activateapplication), você poderá solucionar o problema analisando o log de eventos de ativação. Para encontrar essas entradas no log de eventos:
        1.  abra eventvwr.exe e navegue até o \\ nó de \\ aplicativo Windows Logs.
        2.  Filtre a exibição para mostrar as IDs de Evento: 5900-6000.
        3.  Analise as entradas do log para obter informações que possam explicar por que o aplicativo não foi iniciado.
    -   Identifique e solucione o problema com o arquivo. Compile e teste novamente o aplicativo.
-   Recursos adicionais
    -   [Usando Application Verifier em seu ciclo de vida de desenvolvimento de software](https://blogs.msdn.com/b/ntdebugging/archive/2014/01/13/debugging-a-windows-8-1-store-app-crash-dump.aspx)
    -   [Application Verifier]( https://go.microsoft.com/fwlink/p/?LinkId=708300)
    -   [Usando Application Verifier](https://www.microsoft.com/?ref=go)
    -   [AppInit DLLs](https://www.microsoft.com/?ref=go)
    -   [{1&amp;gt;{2&amp;gt;Minimizar o tempo de inicialização (aplicativos da Windows Store usando C#/VB/C++ e XAML)&amp;lt;2}&amp;lt;1}](/previous-versions/windows/apps/hh994639(v=win.10))

## <a name="compatibility-and-resiliency-test"></a>Teste de compatibilidade e resiliência

-   Segundo plano
    -   Essa verificação validará dois aspectos de um aplicativo, os principais executáveis do aplicativo, por exemplo, o ponto de entrada do aplicativo voltado para o usuário deve ser manifestado quanto à compatibilidade, bem como declarar o GUID correto. Para dar suporte a esse novo teste, o relatório terá um subnó em "compatibilidade & resiliência". O aplicativo falhará se uma ou ambas as condições estiverem ausentes.
-   Detalhes do teste
    -   **Compatibilidade:** os aplicativos devem ser totalmente funcionais sem usar Windows modos de compatibilidade, mensagens AppHelp ou outras correções de compatibilidade. um manifesto de compatibilidade permite que Windows forneça ao seu aplicativo o comportamento adequado de compatibilidade nas diferentes versões do sistema operacional
    -   **AppInit:** os aplicativos não devem listar DLLs para carregar na \_ \_ \\ chave do registro HKEY LOCAL MACHINE Software \\ Microsoft \\ Windows NT \\ CurrentVersion \\ Windows \\ AppInit \_ DLLs.
    -   **Switchback:** O aplicativo deve fornecer o manifesto Switchback. se o manifesto estiver ausente, Windows Kit de certificação de aplicativo fornecerá uma mensagem de aviso. Windows O kit de certificação de aplicativo também verificará se o manifesto contém um GUID de sistema operacional válido.
-   Ações corretivas
    -   Corrija o componente do aplicativo que usa a correção de compatibilidade.
    -   Certifique-se de que o aplicativo não dependa de correções de compatibilidade para sua funcionalidade.
    -   Verifique se seu aplicativo está manifestado e se a seção de compatibilidade inclui os valores apropriados
-   Informações adicionais
    -   Consulte [AppInit DLLs](/previous-versions/windows/apps/hh994639(v=win.10)) para obter mais informações.

## <a name="windows-security-best-practices-test"></a>teste de práticas recomendadas Segurança do Windows

-   Segundo plano
    -   um aplicativo não deve alterar as configurações de segurança de Windows padrão
-   Detalhes do teste
    -   Testa a segurança do aplicativo executando o analisador de superfície de ataque. A abordagem será adicionar categorias de falha em uma base por teste. Por exemplo, algumas categorias de teste de segurança podem incluir:
        -   Falha na inicialização
        -   Falha na arquitetura de segurança
        -   Possível falha de estouro de buffer
        -   Falha de pane
    -   Para obter detalhes, consulte [aqui](/previous-versions/windows/hh920280(v=win.10)).
-   Ações corretivas
    -   Solucionar problemas e corrigir o problema identificado pelos testes. Compile e teste novamente o aplicativo.

## <a name="windows-security-features-test"></a>teste de recursos de segurança do Windows

-   Segundo plano
    -   os aplicativos devem optar por Windows recursos de segurança. Alterar as proteções de segurança padrão do Windows pode colocar os clientes em risco elevado.
-   Detalhes do teste
    -   Testa a segurança do aplicativo executando o Analisador de Binários BinScope. Para obter detalhes, consulte [aqui](/previous-versions/windows/hh920280(v=win.10)).
-   Ações corretivas
    -   Solucione e corrige o problema identificado pelos testes. Compile e teste novamente o aplicativo.

## <a name="high-dpi-test"></a>Teste de DPI alto

É altamente recomendável que os aplicativos Win32 sejam cientes de DPI. É a chave para fazer com que a interface do usuário do aplicativo pareça consistentemente boa em uma ampla variedade de configurações de exibição de alto DPI. Um aplicativo sem conhecimento de DPI em execução em uma configuração de exibição de alto DPI pode ter problemas como dimensionamento incorreto de elementos de interface do usuário, texto recortado e imagens desfocados. Há duas maneiras de declarar que um aplicativo tem conhecimento de DPI. Uma delas é declarar o DPI.

-   Segundo plano
    -   Essa verificação validará dois aspectos de um aplicativo, os principais executáveis, por exemplo, os pontos de entrada do aplicativo voltados para o usuário devem ser manifestados para reconhecimento de ALTA DPI e que as APIs apropriadas estão sendo chamadas para dar suporte a HIGH-DPI. O aplicativo falhará se uma ou ambas as condições estão ausentes. Essa verificação apresentará uma nova seção no relatório da área de trabalho, consulte o exemplo abaixo.
-   Detalhes do teste
    -   O teste gerará um aviso quando detectarmos qualquer um dos seguintes:
        -   O EXE principal não declara o reconhecimento de DPI em seu manifesto e não chama a API SetProcessDPIAware. (Avisar o desenvolvedor se ele esquecer de adicionar o manifesto de reconhecimento de DPI).
        -   O EXE principal não declara o reconhecimento de DPI em seu manifesto, mas chama a API SetProcessDPIAware (avisar o desenvolvedor de que ele deve usar o manifesto para declarar o reconhecimento de DPI em vez de chamar a API).
        -   O mainEXE declara o reconhecimento de DPI em seu manifesto, mas também chama a API SetProcessDPIAware (avisar o desenvolvedor de que chamar essa API não é necessário).
        -   Para os binários que não são EXEs principais, se eles chamarem a API, dê um aviso (Chamar a API não é recomendado).
-   Ações corretivas
    -   O uso da função SetProcessDPIAware() não é desencorajado. Se uma DLL armazenar em cache as configurações de DPI durante sua inicialização, invocar SetProcessDPIAware() no aplicativo poderá gerar uma condição de corrida. Chamar a função SetProcessDPIAware() em uma DLL também não é uma boa prática.
-   Informações adicionais
    -   [Escrevendo aplicativos de Alto DPI](https://msdn.microsoft.com/library/windows/desktop/mt843498(v=vs.85).aspx(d=robot))

 

 