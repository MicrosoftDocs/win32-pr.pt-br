---
title: Testes do Kit de Certificação de Aplicativos Windows
description: Abaixo estão os detalhes do teste para a certificação de aplicativos desktop.
ms.assetid: FA160F46-C266-4F89-B77F-166FEA9ED96B
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a353eef0cd73fecac275b750345b3dd97d05dc87
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "105812102"
---
# <a name="windows-app-certification-kit-tests"></a>Testes do Kit de Certificação de Aplicativos Windows

Abaixo estão os detalhes do teste para a certificação de aplicativos desktop. Para obter informações, consulte [usando o kit de certificação de aplicativos para Windows](using-the-windows-app-certification-kit.md).

-   [Instalação reversível limpa](#clean-reversible-install)
-   [Instalar no teste de pastas corretos](#install-to-the-correct-folders-test)
-   [Teste de arquivo assinado digitalmente](#digitally-signed-file-test)
-   [Suporte ao teste do Windows x64](#support-x64-windows-test)
-   [Teste de verificação de versão do so](#os-version-checking-test)
-   [Teste de controle de conta de usuário (UAC)](#user-account-control-uac-test)
-   [Aderir às mensagens do Gerenciador de reinicialização do sistema](#adhere-to-system-restart-manager-messages)
-   [Teste do modo de segurança](#safe-mode-test)
-   [Teste de sessão multiusuário](#multiuser-session-test)
-   [Teste de panes e travamentos](#crashes-and-hangs-test)
-   [Teste de compatibilidade e resiliência](#compatibility-and-resiliency-test)
-   [Teste de práticas recomendadas de segurança do Windows](#windows-security-best-practices-test)
-   [Teste dos recursos de segurança do Windows](#windows-security-features-test)
-   [Teste de DPI alto](#high-dpi-test)

## <a name="clean-reversible-install"></a>Instalação reversível limpa

Instala e desinstala o aplicativo e verifica se há arquivos residuais e entradas do registro.

-   Tela de fundo
    -   Uma instalação limpa e reversível permite que os usuários implantem e removam aplicativos. Para passar nesse teste, o aplicativo deve fazer o seguinte:
        -   O aplicativo não força o sistema a reiniciar imediatamente após a instalação ou desinstalação do aplicativo. *O processo de instalação ou desinstalação de um aplicativo nunca deve exigir uma reinicialização do sistema logo após a conclusão. Se isso exigir que o sistema seja reiniciado, os usuários deverão ser capazes de reiniciar o sistema de acordo com sua conveniência.*
        -   O aplicativo não depende de 8,3 SFN (nomes de arquivo curtos). *Os processos de instalação e desinstalação do aplicativo devem ser capazes de usar nomes de arquivo longos e caminhos de pasta.*
        -   O aplicativo não bloqueia a instalação/desinstalação silenciosa
        -   O aplicativo faz as entradas necessárias no registro do sistema. *As ferramentas de inventário do Windows e as ferramentas de telemetria exigem informações completas sobre os aplicativos instalados. Os instaladores de aplicativo devem criar as entradas de registro corretas para permitir a detecção e desinstalação bem-sucedidas.*
    -   Se você estiver usando um instalador baseado em MSI, o MSI criará automaticamente as entradas de registro abaixo. Se você não estiver usando um instalador MSI, o módulo de instalação deverá criar as seguintes entradas de registro durante a instalação:
        -   DisplayName
        -   InstallLocation
        -   Publicador
        -   UninstallString
        -   Propriedade VersionMajor ou MajorVersion
        -   VersionMinor ou MinorVersion
    -   O aplicativo deve remover todas as suas entradas em Adicionar ou remover programas.
-   Detalhes do teste
    -   Esse teste verifica os processos de instalação e desinstalação do aplicativo para o comportamento necessário.
-   Ação corretiva
    -   Examine o design e o comportamento do aplicativo em relação aos requisitos descritos acima.

## <a name="install-to-the-correct-folders-test"></a>Instalar no teste de pastas corretos

Verifica se o aplicativo grava seus arquivos de programa e de dados nas pastas corretas.

-   Tela de fundo
    -   Os aplicativos precisam de um sistema de usuário e de pastas por usuário corretamente para que ele possa acessar os dados e as configurações de que precisa ao mesmo tempo em que protege os dados e as configurações do usuário contra o acesso não autorizado.
-   Pastas de arquivos de programas
    -   O aplicativo deve ser instalado na pasta arquivos de programas por padrão (% ProgramFiles% para aplicativos nativos de 32 bits e 64 bits e% ProgramFiles (x86)% para aplicativos de 32 bits em execução em x64).
    -   **Observação:** O aplicativo não deve armazenar dados de usuário ou dados de aplicativo em uma pasta de arquivos de programas devido às permissões de segurança configuradas para essa pasta.
    -   As ACLs nas pastas de sistema do Windows permitem que somente contas de administrador leiam e gravem nelas. Como resultado, as contas de usuário padrão não terão acesso a essas pastas. No entanto, a virtualização de arquivos permite que os aplicativos armazenem um arquivo, como um arquivo de configuração, em um local do sistema que seja normalmente gravável somente por administradores. A execução de programas como usuário padrão nessa situação pode resultar em falha se não puderem acessar um arquivo necessário.
    -   Os aplicativos devem usar [pastas conhecidas](/previous-versions/windows/desktop/legacy/bb776911(v=vs.85)) para garantir que poderão acessar seus dados.
    -   **Observação:** O Windows fornece a virtualização de arquivos para melhorar a compatibilidade de aplicativos e eliminar problemas quando os aplicativos são executados como usuário padrão no Windows. Seu aplicativo não deve depender da virtualização que está presente em versões futuras do Windows.
-   Pastas de dados de aplicativo específicas do usuário
    -   Em instalações "por máquina", o aplicativo não deve gravar dados específicos do usuário durante a instalação. Os dados de instalação específicos do usuário só devem ser gravados quando um usuário inicia o aplicativo pela primeira vez. Isso ocorre porque não há nenhum local de usuário correto no qual armazenar dados no momento da instalação. As tentativas de um aplicativo para modificar os comportamentos de associação padrão em um nível de máquina após a instalação não serão bem-sucedidas. Em vez disso, os padrões devem ser reivindicados em um nível por usuário, o que impede que vários usuários substituam os padrões uns dos outros.
    -   Todos os dados de aplicativo exclusivos para um usuário específico e não para serem compartilhados com outros usuários do computador devem ser armazenados em usuários \\ <username> \\ AppData.
    -   Todos os dados de aplicativo que devem ser compartilhados entre os usuários no computador devem ser armazenados em ProgramData.
-   Outras pastas do sistema e chaves do registro
    -   O aplicativo nunca deve gravar diretamente no diretório e nos subdiretórios do Windows. Use os métodos corretos para instalar arquivos, como fontes ou drivers, nesses diretórios.
    -   Os aplicativos não devem iniciar automaticamente na inicialização, como ao adicionar uma entrada a um ou mais desses locais:
        -   Chaves de execução do Registro HKLM e, ou HKCU em software \\ Microsoft \\ Windows \\ CurrentVersion
        -   Chaves de execução do Registro HKLM, e ou HKCU em software \\ Wow6432Node \\ Microsoft \\ Windows \\ CurrentVersion
        -   Menu iniciar todos os programas > inicialização
-   Detalhes do teste
    -   Esse teste verifica se o aplicativo usa os locais específicos no sistema de arquivos que o Windows fornece para armazenar programas e componentes de software, dados de aplicativos compartilhados e dados de aplicativos que são específicos de um usuário.
-   Ações corretivas
    -   Examine como o aplicativo usa as pastas do sistema e verifique se ele está usando-as corretamente.
-   Exceções e renúncias
    -   Uma renúncia é necessária para aplicativos de desktop gravando no GAC (cache de assembly global) (os aplicativos .NET devem manter as dependências de assembly particulares e armazená-las no diretório do aplicativo, a menos que o compartilhamento de um assembly seja explicitamente necessário).
    -   A instalação na pasta arquivos de programas não é um requisito para que os pacotes de SW da área de trabalho obtenham o logotipo do SW, somente na categoria conceitos básicos do SW.

## <a name="digitally-signed-file-test"></a>Teste de arquivo assinado digitalmente

Testa arquivos executáveis e drivers de dispositivo para verificar se eles têm uma assinatura digital válida.

-   Tela de fundo
    -   Os arquivos assinados digitalmente possibilitam verificar se o arquivo é original e detectar se o arquivo foi violado.
    -   A imposição de assinatura de código no modo kernel é um recurso do Windows que também é conhecido como CI (integridade de código). O CI melhora a segurança do Windows, verificando a integridade de um arquivo cada vez que ele é carregado na memória. O CI detecta se o código mal-intencionado modificou um arquivo binário do sistema e gera um evento de log de diagnóstico e auditoria do sistema quando a assinatura de um módulo kernel não é verificada corretamente.
    -   Se o aplicativo exigir permissões elevadas, o prompt de elevação exibirá informações contextuais sobre o arquivo executável que está solicitando acesso elevado. Dependendo se o aplicativo é assinado por Authenticode, o usuário pode ver a solicitação de consentimento ou a solicitação de credencial.
    -   Nomes fortes impedem que terceiros falsifiquem seu código, contanto que você mantenha a chave privada segura. O .NET Framework verifica a assinatura digital quando carrega o assembly ou o instala no GAC. Sem acesso à chave privada, um usuário mal-intencionado não pode modificar seu código e inscreva-o novamente.
-   Detalhes do teste
    -   Todos os arquivos executáveis, como aqueles com extensões de arquivo. exe,. dll,. ocx,. sys,. cpl,. drv e. SCR, devem ser assinados com um certificado Authenticode.
    -   Todos os drivers de modo kernel instalados pelo aplicativo devem ter uma assinatura da Microsoft obtida por meio do programa WHQL ou DRS. Todos os drivers de filtro do sistema de arquivos devem ser assinados por WHQL.
-   Ação corretiva
    -   Assine os arquivos executáveis do aplicativo.
    -   Use makecert.exe para gerar um certificado ou obter uma chave de assinatura de código de uma das CAs (autoridades de certificação) comerciais, como VeriSign, Thawte ou uma AC da Microsoft.
-   Exceções e renúncias
    -   As renúncias serão consideradas apenas para os redistribuíveis de terceiros não assinados. Uma prova de comunicação solicitando uma versão assinada dos redistribuíveis (s) é necessária para que essa renúncia seja concedida.
    -   Os pacotes de software de valor agregado do dispositivo são isentos da certificação de driver de modo kernel, pois os drivers devem ser certificados pela certificação de hardware do Windows.

## <a name="support-x64-windows-test"></a>Suporte ao teste do Windows x64

Teste o aplicativo para certificar-se de que o. exe foi criado para a arquitetura da plataforma na qual ele será instalado.

-   Tela de fundo
    -   O arquivo executável deve ser criado para a arquitetura do processador na qual ele está instalado. Alguns arquivos executáveis podem ser executados em uma arquitetura de processador diferente, mas isso não é confiável.
    -   A compatibilidade de arquitetura é importante porque os processos de 32 bits não podem carregar DLLs de 64 bits e processos de 64 bits não podem carregar DLLs de 32 bits. Da mesma forma, as versões de 64 bits do Windows não oferecem suporte à execução de aplicativos baseados no Windows de 16 bits, pois os identificadores têm 32 bits significativos no Windows de 64 bits um para que não possam ser passados para aplicativos de 16 bits. Portanto, tentar iniciar um aplicativo de 16 bits falhará nas versões de 64 bits do Windows.
    -   os drivers de dispositivo de 32 bits não podem ser executados em versões de 64 bits do Windows e, portanto, devem ser portados para a arquitetura de 64 bits.
    -   Para aplicativos de modo de usuário, o Windows de 64 bits inclui o WOW64, que permite que aplicativos do Windows de 32 bits sejam executados em sistemas que executam o Windows de 64 bits, embora com alguma perda de desempenho. Não existe nenhuma camada de tradução equivalente para drivers de dispositivo.
    -   Para manter a compatibilidade com as versões de 64 bits do Windows, os aplicativos devem dar suporte nativo a 64 bits ou, no mínimo, aplicativos baseados no Windows de 32 bits devem ser executados diretamente em sistemas de 64 bits:
        -   Os aplicativos e seus instaladores não deve contêm qualquer código de 16 bits ou dependem de qualquer componente de 16 bits.
        -   A instalação do aplicativo deve detectar e instalar os drivers e componentes adequados nas versões de 64 bits do Windows.
        -   Os plug-ins de shell devem ser executados em versões de 64 bits do Windows.
        -   Os aplicativos executados no emulador WoW64 não devem tentar ignorar os mecanismos de virtualização do WOW64. Se houver cenários específicos em que os aplicativos precisam detectar se estão em execução em um emulador do WoW64, eles devem fazer isso chamando [**IsWow64Process**](/windows/desktop/api/wow64apiset/nf-wow64apiset-iswow64process).
-   Detalhes do teste
    -   O aplicativo não deve instalar nenhum binário de 16 bits. O aplicativo não deve instalar um driver de modo kernel de 32 bits se ele precisar ser executado em um computador de 64 bits.
-   Ações Corretivas
    -   Crie os arquivos executáveis e os drivers para a arquitetura do processador para o qual você deseja instalá-los.

## <a name="os-version-checking-test"></a>Teste de verificação de versão do so

Testa como o aplicativo verifica a versão do Windows na qual está sendo executado.

-   Tela de fundo
    -   Os aplicativos verificam a versão do sistema operacional testando uma versão que seja maior ou igual à versão necessária para garantir a compatibilidade com versões futuras do Windows.
-   Detalhes do teste
    -   Simula a execução do aplicativo em versões diferentes do Windows para ver como ele reage.
-   Ações corretivas
    -   Teste a versão correta do Windows testando se a versão atual é maior ou igual à versão de que seu aplicativo, serviço ou driver precisa.
    -   Instaladores de driver e módulos de desinstalação nunca devem verificar a versão do sistema operacional.
-   Exceções e renúncias
    -   As renúncias serão consideradas para aplicativos que atendam aos seguintes critérios: *(aplica-se somente à certificação de aplicativos da área de trabalho)*
        -   Aplicativos que são entregues como um pacote executado no Windows XP, no Windows Vista e no Windows 7 e precisam verificar a versão do sistema operacional para determinar quais componentes devem ser instalados em um determinado sistema de operação.
        -   Aplicativos que verificam apenas a versão mínima do sistema operacional (durante a instalação apenas, não em tempo de execução) usando apenas as chamadas à API aprovadas e listam o requisito mínimo de versão no manifesto do aplicativo, conforme necessário.
        -   Aplicativos de segurança como antivírus e aplicativos de firewall, utilitários de sistema como utilitários de desfragmentação e aplicativos de backup e ferramentas de diagnóstico que verificam a versão do sistema operacional usando apenas as chamadas de API aprovadas.

## <a name="user-account-control-uac-test"></a>Teste de controle de conta de usuário (UAC)

Testa o aplicativo para verificar se ele não precisa de permissões desnecessariamente elevadas para ser executado.

-   Tela de fundo
    -   Um aplicativo que opera ou instala somente quando o usuário é um administrador força os usuários a executarem o aplicativo com permissões desnecessariamente elevadas, que podem permitir que o malware Insira o computador do usuário.
    -   Quando os usuários são sempre forçados a executar aplicativos com tokens de acesso elevados, o aplicativo pode ser o servidor como um ponto de entrada para códigos enganosos ou mal-intencionados. Esse malware pode facilmente modificar o sistema operacional, ou pior, afetar outros usuários. É quase impossível controlar um usuário que tenha acesso de administrador total, pois os administradores podem instalar aplicativos e executar qualquer aplicativo ou script no computador. Os gerentes de ti sempre buscam maneiras de criar "áreas de trabalho padrão" em que os usuários fazem logon como usuários padrão. As áreas de trabalho padrão reduzem muito os custos de suporte técnico e reduzem a sobrecarga de ti.
    -   A maioria dos aplicativos não requer privilégios de administrador em tempo de execução. Uma conta de usuário padrão deve ser capaz de executá-las. Os aplicativos do Windows devem ter um manifesto (inserido ou externo) para definir seu nível de execução que informa ao sistema operacional os privilégios necessários para executar o aplicativo. O manifesto do aplicativo só se aplica a arquivos. exe, não a arquivos. dll. O UAC (controle de conta de usuário) não inspeciona DLLs durante a criação do processo. As regras de UAC não se aplicam aos serviços da Microsoft. O manifesto do aplicativo pode ser inserido ou externo.
    -   Para criar um manifesto, crie um arquivo com o nome <nome do aplicativo \_ # C1.exe. manifest e armazene-o no mesmo diretório que o exe. Observe que qualquer manifesto externo será ignorado se o aplicativo tiver um manifesto interno.
        -   Por exemplo, <requestedExecutionLevel Level = "" asInvoker \| highestAvailable \| requireAdministrator "" UIAccess = "" true \| false ""/>
        -   O processo principal do aplicativo deve ser executado como usuário padrão (**asInvoker**). Todos os recursos administrativos devem ser movidos para um processo separado que seja executado com privilégios administrativos.
        -   Os aplicativos voltados para o usuário que exigem privilégios elevados devem ser assinados por Authenticode.
-   Detalhes do teste
    -   Todos os EXEs voltados para o usuário devem ser marcados com o atributo asInvoker. Se eles estiverem marcados como highestAvailable ou requireAdministrator, eles deverão ser assinados com Authenticode corretamente. Qualquer executável de aplicativo não deve ter o atributo uiAccess definido como true. Qualquer exe que é executado como um serviço é excluído dessa verificação específica.
-   Ações corretivas
    -   Examine o arquivo de manifesto do aplicativo para obter as entradas e os níveis de permissão corretos.
-   Exceções e renúncias
    -   Uma renúncia é necessária para aplicativos que executam seu processo principal com privilégios elevados (**requireAdministrator** ou **highestAvailable**). O processo principal é o processo que fornece o ponto de entrada do usuário para o aplicativo.
    -   As renúncias serão consideradas para os seguintes cenários:
        -   Ferramentas administrativas ou do sistema com o nível de execução definido como **highestAvailable**, **requireAdministrator** ou ambos.
        -   Somente acessibilidade ou aplicativo de estrutura de automação de interface do usuário define o sinalizador uiAccess como TRUE para ignorar o UIPI (isolamento de privilégio de interface do usuário). Para iniciar corretamente a utilização do aplicativo, esse sinalizador deve ser assinado por Authenticode e deve residir em um local protegido no sistema de arquivos, como arquivos de programas.

## <a name="adhere-to-system-restart-manager-messages"></a>Aderir às mensagens do Gerenciador de reinicialização do sistema

Testa como o aplicativo responde às mensagens de desligamento e reinicialização do sistema.

-   Tela de fundo
    -   Os aplicativos devem sair o mais rápido possível quando são notificados de que o sistema está sendo desligado para fornecer um desligamento responsivo ou uma experiência de desativação para o usuário.
    -   Em um desligamento crítico, os aplicativos que retornam FALSE para o [**WM \_ QUERYENDSESSION**](/windows/desktop/Shutdown/wm-queryendsession) serão enviados ao **WM \_ EndSession** e fechados, enquanto aqueles que atingirem o tempo limite em resposta ao WM \_ QUERYENDSESSION serão encerrados de modo forçado.
-   Detalhes do teste
    -   Examina como o aplicativo responde às mensagens de encerramento e saída.
-   Ações corretivas
    -   Se o aplicativo falhar neste teste, examine como ele lida com essas mensagens do Windows:
        -   [**WM \_ QUERYENDSESSION**](/windows/desktop/Shutdown/wm-queryendsession) com o *lParam*  =  **EndSession \_ CLOSEAPP**(0x1): os aplicativos da área de trabalho devem responder (true) imediatamente na preparação para uma reinicialização. Os aplicativos de console podem chamar [**SetConsoleCtrlHandler**](/windows/console/setconsolectrlhandler) para receber a notificação de desligamento. Os serviços podem chamar [**RegisterServiceCtrlHandlerEx**](/windows/desktop/api/winsvc/nf-winsvc-registerservicectrlhandlerexa) para receber notificações de desligamento em uma rotina de manipulador.
        -   [**WM \_ EndSession**](/windows/desktop/Shutdown/wm-queryendsession) com *lParam*  =  **EndSession \_ CLOSEAPP**(0x1): os aplicativos devem retornar um valor 0 dentro de 30 segundos e desligar. No mínimo, os aplicativos devem se preparar salvando os dados do usuário e estado as informações necessárias após uma reinicialização.
    -   Os aplicativos de console que recebem a notificação de **\_ \_ evento CTRL C** devem ser desligados imediatamente. Os drivers não devem vetar um evento de desligamento do sistema.
    -   **Observação:** Aplicativos que devem bloquear o desligamento devido a uma operação que não pode ser interrompida devem usar [**ShutdownBlockReasonCreate**](/windows/desktop/api/winuser/nf-winuser-shutdownblockreasoncreate) para registrar uma cadeia de caracteres que explica o motivo do usuário. Quando a operação for concluída, o aplicativo deverá chamar [**ShutdownBlockReasonDestroy**](/windows/desktop/api/winuser/nf-winuser-shutdownblockreasondestroy) para indicar que o sistema pode ser desligado.

## <a name="safe-mode-test"></a>Teste do modo de segurança

Testa se o driver ou o serviço está configurado para iniciar no modo de segurança.

-   Tela de fundo
    -   O modo de segurança permite que os usuários diagnostiquem e solucionem problemas com o Windows. Somente os drivers e serviços que são necessários para a operação básica do sistema operacional ou fornecem serviços de diagnóstico e recuperação devem ser carregados no modo de segurança. Carregar outros arquivos no modo de segurança dificulta a solução de problemas com o sistema operacional.
    -   Por padrão, somente os drivers e serviços que vêm pré-instalados com o Windows são iniciados no modo de segurança. Todos os outros drivers e serviços devem ser desabilitados, a menos que o sistema os exija para operações básicas ou para fins de diagnóstico e recuperação.
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

-   Tela de fundo
    -   Os usuários do Windows devem ser capazes de executar sessões simultâneas. Os aplicativos devem garantir que, quando executados em várias sessões, seja local ou remotamente, a funcionalidade normal do aplicativo não seja afetada negativamente. As configurações do aplicativo e os arquivos de dados devem ser específicos do usuário e a privacidade e as preferências do usuário devem ser restritas à sessão do usuário.
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
    -   O kit de certificação de aplicativos para Windows chama [**IApplicationActivationManager:: ActivateApplication**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iapplicationactivationmanager-activateapplication) para iniciar aplicativos da Windows Store. Para que o **ActivateApplication** inicie um aplicativo, o UAC (Controle de Conta de Usuário) deve estar habilitado, e a resolução da tela deve ser de pelo menos 1024 x 768 ou 768 x 1024. Se nenhuma condição for atendida, o aplicativo falhará nesse teste.
-   Ações Corretivas
    -   Verifique se o UAC está habilitado no computador de teste.
    -   Verifique se você está executando o teste em um computador com uma tela grande o suficiente.
    -   Se o aplicativo falhar para iniciar e sua plataforma de teste satisfizer os pré-requisitos do [**ActivateApplication**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iapplicationactivationmanager-activateapplication), você poderá solucionar o problema analisando o log de eventos de ativação. Para encontrar essas entradas no log de eventos:
        1.  Abra eventvwr.exe e navegue até o \\ nó de aplicativo logs do Windows \\ .
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

-   Tela de fundo
    -   Essa verificação validará dois aspectos de um aplicativo, os principais executáveis do aplicativo, por exemplo, o ponto de entrada do aplicativo voltado para o usuário deve ser manifestado quanto à compatibilidade, bem como declarar o GUID correto. Para dar suporte a esse novo teste, o relatório terá um subnó em "compatibilidade & resiliência". O aplicativo falhará se uma ou ambas as condições estiverem ausentes.
-   Detalhes do teste
    -   **Compatibilidade:** Os aplicativos devem ser totalmente funcionais sem usar modos de compatibilidade do Windows, mensagens AppHelp ou outras correções de compatibilidade. Um manifesto de compatibilidade permite que o Windows forneça ao seu aplicativo o comportamento adequado de compatibilidade nas diferentes versões do sistema operacional
    -   **AppInit:** Os aplicativos não devem listar as DLLs a serem carregadas na \_ \_ \\ chave do registro hKey local Machine software \\ Microsoft \\ Windows NT \\ CurrentVersion \\ Windows \\ AppInit \_ DLLs.
    -   **Switchback:** O aplicativo deve fornecer o manifesto Switchback. Se o manifesto estiver ausente, o kit de certificação de aplicativos do Windows fornecerá uma mensagem de aviso. O kit de certificação de aplicativos para Windows também verificará se o manifesto contém um GUID de sistema operacional válido.
-   Ações corretivas
    -   Corrija o componente do aplicativo que usa a correção de compatibilidade.
    -   Certifique-se de que o aplicativo não dependa de correções de compatibilidade para sua funcionalidade.
    -   Verifique se seu aplicativo está manifestado e se a seção de compatibilidade inclui os valores apropriados
-   Informações adicionais
    -   Consulte [AppInit DLLs](/previous-versions/windows/apps/hh994639(v=win.10)) para obter mais informações.

## <a name="windows-security-best-practices-test"></a>Teste de práticas recomendadas de segurança do Windows

-   Tela de fundo
    -   Um aplicativo não deve alterar as configurações de segurança padrão do Windows
-   Detalhes do teste
    -   Testa a segurança do aplicativo executando o analisador de superfície de ataque. A abordagem será adicionar categorias de falha em uma base por teste. Por exemplo, algumas categorias de teste de segurança podem incluir:
        -   Falha na inicialização
        -   Falha na arquitetura de segurança
        -   Possível falha de estouro de buffer
        -   Falha de pane
    -   Para obter detalhes, consulte [aqui](/previous-versions/windows/hh920280(v=win.10)).
-   Ações corretivas
    -   Solucionar problemas e corrigir o problema identificado pelos testes. Compile e teste novamente o aplicativo.

## <a name="windows-security-features-test"></a>Teste de recursos de segurança do Windows

-   Tela de fundo
    -   Os aplicativos devem optar pelos recursos de segurança do Windows. Alterar as proteções de segurança padrão do Windows pode colocar os clientes em risco elevado.
-   Detalhes do teste
    -   Testa a segurança do aplicativo executando o Analisador de Binários BinScope. Para obter detalhes, consulte [aqui](/previous-versions/windows/hh920280(v=win.10)).
-   Ações corretivas
    -   Solucionar problemas e corrigir o problema identificado pelos testes. Compile e teste novamente o aplicativo.

## <a name="high-dpi-test"></a>Teste de DPI alto

É altamente recomendável que os aplicativos Win32 tenham reconhecimento de DPI. É a chave para fazer com que a interface do usuário do aplicativo pareça consistente em uma grande variedade de configurações de vídeo de alto DPI. Um aplicativo sem reconhecimento de DPI em execução em uma configuração de exibição de alto DPI pode ter problemas como o dimensionamento incorreto de elementos da interface do usuário, texto recortado e imagens borradas. Há duas maneiras de declarar um aplicativo com reconhecimento de DPI. Uma é declarar DPI.

-   Tela de fundo
    -   Essa verificação validará dois aspectos de um aplicativo, os principais executáveis, por exemplo, os pontos de entrada de aplicativo voltados para o usuário devem ser manifestados para reconhecimento de DPI alto e que as APIs apropriadas estejam sendo chamadas para dar suporte a DPI alto. O aplicativo falhará se uma ou ambas as condições estiverem ausentes. Essa verificação apresentará uma nova seção no relatório da área de trabalho, consulte o exemplo abaixo.
-   Detalhes do teste
    -   O teste irá gerar um aviso quando detectarmos qualquer um dos seguintes:
        -   O EXE principal não declara reconhecimento de DPI em seu manifesto e não chama a API SetProcessDPIAware. (Avise o desenvolvedor se ele esquecer de adicionar o manifesto de reconhecimento de DPI).
        -   O EXE principal não declara o reconhecimento de DPI em seu manifesto, mas chama a API SetProcessDPIAware (avise ao desenvolvedor que ele deve usar o manifesto para declarar o reconhecimento de DPI em vez de chamar a API).
        -   O mainEXE declara reconhecimento de DPI em seu manifesto, mas também chama a API SetProcessDPIAware (avisar o desenvolvedor que chama essa API não é necessário).
        -   Para os binários que não são os EXEs principais, se eles chamarem a API, dê um aviso (chamar a API não é recomendado).
-   Ações corretivas
    -   O uso da função SetProcessDPIAware () não é recomendado. Se uma DLL armazenar em cache as configurações de DPI durante sua inicialização, invocar SetProcessDPIAware () no aplicativo poderá gerar uma condição de corrida. Chamar a função SetProcessDPIAware () em uma DLL não é uma boa prática.
-   Informações adicionais
    -   [Escrevendo aplicativos de alto DPI](https://msdn.microsoft.com/library/windows/desktop/mt843498(v=vs.85).aspx(d=robot))

 

 