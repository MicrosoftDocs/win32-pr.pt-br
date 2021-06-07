---
title: Requisitos de certificação de arquivamento para aplicativos da área de trabalho do Windows v 1.2
description: Documento versão 1.2 data do documento 31 de maio de 2012This documento contém os requisitos técnicos e as qualificações de qualificação que um aplicativo de desktop deve atender para participar do programa de certificação de aplicativos para desktop do Windows 8.
ms.assetid: A65D7FE9-554B-4D59-91B7-E1582F7C6C87
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: dd84d5586d682b22947b182bd7d5a11625fcf537
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/04/2021
ms.locfileid: "111444227"
---
# <a name="archive-certification-requirements-for-windows-desktop-apps-v12"></a>Arquivo: requisitos de certificação para aplicativos da área de trabalho do Windows v 1.2

**Versão do documento:** 1,2

**Data do documento:** 31 de maio de 2012

Este documento contém os requisitos técnicos e as qualificações de qualificação que um aplicativo de desktop deve atender para participar do programa de certificação de aplicativos para desktop do Windows 8. Para o Windows 7, esse programa era conhecido como o programa de logotipo de software do Windows.

## <a name="welcome"></a>Seja bem-vindo!

A plataforma Windows dá suporte a um amplo ecossistema de produtos e parceiros. A exibição do logotipo do Windows em seu produto representa uma relação e um compromisso compartilhado com a qualidade entre a Microsoft e a sua empresa. Os clientes confiam na marca do Windows em seu produto, pois garantem que ele atenda aos padrões de compatibilidade e que funcione bem na plataforma Windows. A passagem bem-sucedida da certificação de aplicativos para Windows permite que seu aplicativo seja demonstrado no centro de compatibilidade do Windows e também uma etapa necessária para listar uma referência de aplicativo de desktop na Windows Store.

O programa de certificação de aplicativos para Windows é composto por requisitos de programa e técnicos para ajudar a garantir que aplicativos de terceiros que tenham a marca do Windows sejam fáceis de instalar e confiáveis em computadores que executam o Windows. Os clientes precisam de estabilidade, compatibilidade, confiabilidade, desempenho e qualidade nos sistemas comprados. A Microsoft concentra seus investimentos para atender a esses requisitos para aplicativos de software projetados para serem executados na plataforma Windows para PCs. Esses esforços incluem testes de compatibilidade de consistência de experiência, desempenho aprimorado e segurança aprimorada em computadores que executam o software Windows. Os testes de compatibilidade da Microsoft foram projetados em colaboração com parceiros do setor e são aprimorados continuamente em resposta aos desenvolvimentos do setor e à demanda do consumidor.

O kit de certificação de aplicativos para Windows é usado para validar a conformidade com esses requisitos e substitui o WSLK usado para validação no programa de logotipo de software do Windows 7. O kit de certificação de aplicativos para Windows é um dos componentes incluídos no SDK (Software Development Kit) do Windows.

## <a name="app-eligibility"></a>Qualificação do aplicativo

Para que um aplicativo se qualifique para a certificação de aplicativos de área de trabalho do Windows 8, ele deve atender aos critérios a seguir e a todos os requisitos técnicos listados neste documento.

-   Ele deve ser um aplicativo autônomo
-   Ele deve ser executado em um computador Windows 8.1 local
-   Pode ser um componente de cliente de um aplicativo do Windows Server certificado
-   Ele deve ser o código e o recurso concluídos

## <a name="1-apps-are-compatible-and-resilient"></a>1. os aplicativos são compatíveis e resilientes

Os horários em que um aplicativo falha ou param de responder causam grande frustração do usuário. Os aplicativos devem ser resilientes e estáveis e a eliminação dessas falhas ajuda a garantir que o software seja mais previsível, passível de manutenção, de alto desempenho e confiável.<dl> 1,1 seu aplicativo não deve assumir uma dependência dos modos de compatibilidade do Windows, mensagem AppHelp e ou quaisquer outras correções de compatibilidade  
1,2 seu aplicativo não deve assumir uma dependência do tempo de execução do VB6  
1,3 seu aplicativo não deve carregar DLLs arbitrárias para interceptar chamadas à API do Win32 usando HKLM \\ software \\ Microsoft \\ Windows NT \\ CurrentVersion \\ Windows AppInit \_ DLLs.  
</dl>

## <a name="2-apps-must-adhere-to-windows-security-best-practices"></a>2. os aplicativos devem aderir às práticas recomendadas de segurança do Windows

Usar as práticas recomendadas de segurança do Windows ajudará a evitar a criação de exposição a superfícies de ataque do Windows. As superfícies de ataque são os pontos de entrada que um invasor mal-intencionado poderia usar para explorar o sistema operacional aproveitando as vulnerabilidades no software de destino. Uma das piores vulnerabilidades de segurança é a elevação de privilégio.

<dl> 2,1 seu aplicativo deve usar <a href="/windows/desktop/SecAuthZ/access-control-lists">ACLs</a> fortes e apropriadas para proteger arquivos executáveis  
2,2 seu aplicativo deve usar <a href="/windows/desktop/SecAuthZ/access-control-lists">ACLs</a> fortes e apropriadas para proteger diretórios  
2,3 seu aplicativo deve usar <a href="/windows/desktop/SecAuthZ/access-control-lists">ACLs</a> fortes e apropriadas para proteger chaves do registro  
2,4 seu aplicativo deve usar <a href="/windows/desktop/SecAuthZ/access-control-lists">ACLs</a> fortes e apropriadas para proteger diretórios que contêm objetos  
2,5 seu aplicativo deve reduzir o acesso de não administrador aos serviços que estão vulneráveis à violação  
2,6 seu aplicativo deve impedir que os serviços com reinicializações rápidas reiniciem mais de duas vezes a cada 24 horas
</dl>**Observação: o acesso só deve ser concedido às entidades que o exigem.**

O programa de certificação de aplicativos para Windows verificará se as superfícies de ataque do Windows não são expostas verificando se as ACLs e os serviços são implementados de uma maneira que não coloca o sistema Windows em risco.

## <a name="3-apps-support-windows-security-features"></a>3. os aplicativos dão suporte aos recursos de segurança do Windows

O sistema operacional Windows tem muitos recursos que dão suporte à segurança e privacidade do sistema. Os aplicativos devem dar suporte a esses recursos para manter a integridade do sistema operacional. Aplicativos compilados incorretamente poderiam causar estouros de buffer que podem, por sua vez, causar negação de serviço ou permitir a execução de código mal-intencionado. <dl> 3,1 seu aplicativo não deve usar AllowPartiallyTrustedCallersAttribute (APTCA) para garantir o acesso seguro a assemblies de nome forte  
3,2 seu aplicativo deve ser compilado usando o sinalizador/SafeSEH para garantir a manipulação de exceções seguras  
3,3 seu aplicativo deve ser compilado usando o sinalizador/NXCOMPAT para impedir a execução de dados  
3,4 seu aplicativo deve ser compilado usando o sinalizador/DYNAMICBASE para o ASLR (Address Space layout Randomization)  
3,5 seu aplicativo não deve ler/gravar as seções do PE compartilhadas  
</dl>

## <a name="4-apps-must-adhere-to-system-restart-manager-messages"></a>4. os aplicativos devem aderir às mensagens do Gerenciador de reinicialização do sistema

Quando os usuários iniciam o desligamento, eles geralmente têm um desejo forte de ver o desligamento com sucesso; Eles podem estar com pressa para sair do escritório e apenas querem que seus computadores sejam desligados. Os aplicativos devem respeitar esse desejo não bloqueando o desligamento. Na maioria dos casos, um desligamento pode não ser crítico, os aplicativos devem estar preparados para a possibilidade de um desligamento crítico.<dl> 4,1 seu aplicativo deve lidar com desligamentos críticos adequadamente <dl> Em um desligamento crítico, os aplicativos que retornam FALSE para o WM \_ QUERYENDSESSION serão enviados ao WM \_ EndSession e fechados, enquanto aqueles que atingirem o tempo limite em resposta ao WM \_ QUERYENDSESSION serão encerrados.  
</dl> </dd> 4.2 A GUI app must return TRUE immediately in preparation for a restart <dl> WM \_ QUERYENDSESSION com lParam = EndSession \_ CLOSEAPP (0x1).  
Os aplicativos de console podem chamar SetConsoleCtrlHandler para especificar a função que tratará as notificações de desligamento. Os aplicativos de serviço podem chamar RegisterServiceCtrlHandlerEx para especificar a função que receberá notificações de desligamento.  
</dl> </dd> 4.3 Your app must return 0 within 30 seconds and shut down <dl> \_EndSession do WM com lParam = EndSession \_ CLOSEAPP (0x1).  
No mínimo, o aplicativo deve se preparar salvando os dados do usuário e estado as informações necessárias após uma reinicialização.  
</dl> </dd> 4.4 Console apps that receive the CTRL\_C\_EVENT notification should shut down immediately  
4.5 Drivers must not veto a system shutdown event  
</dl>**Note: Apps that must block shutdown because of an operation that cannot be interrupted should explain the reason to the user.** Use ShutdownBlockReasonCreate to register a string that explains the reason to the user. When the operation has completed, the app should call ShutdownBlockReasonDestroy to indicate that the system can be shut down.

## <a name="5-apps-must-support-a-clean-reversible-installation"></a>5. os aplicativos devem oferecer suporte a uma instalação limpa e reversível

Uma instalação limpa e reversível permite que os usuários gerenciem com êxito (implante e removam) aplicativos em seus sistemas.<dl> 5,1 seu aplicativo deve implementar corretamente uma instalação limpa e reversível <dl> Se a instalação falhar, o aplicativo deverá ser capaz de reverter e restaurar o computador para seu estado anterior.  
</dl> </dd> 5.2 Your app must never force the user to restart the computer immediately <dl> Reiniciar o computador nunca deve ser a única opção no final de uma instalação ou atualização. Os usuários devem ter a oportunidade de reiniciar mais tarde.  
</dl> </dd> 5.3 Your app must never be dependent on 8.3 short file names (SFN)  
5.4 Your app must never block silent install/uninstall  
5.5 Your app installer must create the correct registry entries to allow successful detection and uninstalls <dl> As ferramentas de inventário do Windows e as ferramentas de telemetria exigem informações completas sobre os aplicativos instalados. Se você estiver usando um instalador baseado em MSI, o MSI criará automaticamente as entradas de registro abaixo. Se você não estiver usando um instalador MSI, o módulo de instalação deverá criar as seguintes entradas de registro durante a instalação:  
</dl>

-   DisplayName
-   InstallLocation
-   Publicador
-   UninstallString
-   Propriedade VersionMajor ou MajorVersion
-   VersionMinor ou MinorVersion

</dd> </dl>

## <a name="6-apps-must-digitally-sign-files-and-drivers"></a>6. os aplicativos devem assinar digitalmente arquivos e drivers

Uma assinatura digital Authenticode permite que os usuários tenham certeza de que o software é autêntico. Ele também permite detectar se um arquivo foi violado, como se ele foi infectado por um vírus. A imposição de assinatura de código no modo kernel é um recurso do Windows conhecido como integridade de código (CI), que melhora a segurança do sistema operacional, verificando a integridade de um arquivo cada vez que a imagem do arquivo é carregada na memória. O CI detecta se o código mal-intencionado modificou um arquivo binário do sistema. Também gera um evento de log de diagnóstico e auditoria do sistema quando a assinatura de um módulo kernel não é verificada corretamente. <dl> 6,1 todos os arquivos executáveis (.exe, .dll,. ocx, .sys, .cpl,. drv,. SCR) devem ser assinados com um certificado Authenticode  
6,2 todos os drivers de modo kernel instalados pelo aplicativo devem ter uma assinatura da Microsoft obtida por meio do programa de certificação de hardware do Windows. Todos os drivers de filtro do sistema de arquivos devem ser assinados pela Microsoft.  
6,3 exceções e renúncias <dl> As renúncias serão consideradas apenas para redistribuíveis de terceiros não assinados, excluindo drivers. Uma prova de comunicação solicitando uma versão assinada dos redistribuíveis (s) é necessária para que essa renúncia seja concedida.  
</dl> </dd> </dl>

## <a name="7-apps-don-t-block-installation-or-app-launch-based-on-an-operating-system-version-check"></a>7. aplicativos Don t bloquear instalação ou inicialização de aplicativo com base em uma verificação de versão do sistema operacional

É importante que os clientes não sejam artificialmente impedidos de instalar ou executar seu aplicativo quando não houver nenhuma limitação técnica. Em geral, se os aplicativos foram escritos para o Windows Vista ou versões posteriores do Windows, eles não devem verificar a versão do sistema operacional.<dl> 7,1 seu aplicativo não deve executar verificações de versão para igualdade <dl> Se você precisar de um recurso específico, verifique se o recurso em si está disponível. Se você precisar do Windows XP, verifique o Windows XP ou posterior (>= 5,1). Dessa forma, o código de detecção continuará a funcionar em versões futuras do Windows. Instaladores de driver e módulos de desinstalação nunca devem verificar a versão do sistema operacional.  
</dl> </dd> 7.2 Exceptions and Waivers will be considered for apps meeting the criteria below:

-   Aplicativos que são entregues como um pacote que também são executados no Windows XP, no Windows Vista e no Windows 7, e precisam verificar a versão do sistema operacional para determinar quais componentes devem ser instalados em um determinado sistema operacional.
-   Aplicativos que verificam apenas a versão mínima do sistema operacional (durante a instalação apenas, não em tempo de execução) usando apenas as chamadas à API aprovadas e que listam corretamente o requisito mínimo de versão no manifesto do aplicativo.
-   Aplicativos de segurança (antivírus, firewall etc.), utilitários do sistema (por exemplo, desfragmentação, backups e ferramentas de diagnóstico) que verificam a versão do sistema operacional usando apenas as chamadas à API aprovadas.

  
</dl>

## <a name="8-apps-don-t-load-services-or-drivers-in-safe-mode"></a>8. Os aplicativos não carregam serviços ou drivers no modo de segurança

O modo de segurança permite aos usuários diagnosticar e solucionar problemas do Windows. Drivers e serviços não devem ser definidos para serem carregados no modo de segurança, a menos que sejam necessários para operações básicas do sistema, como drivers de dispositivo de armazenamento ou para fins de diagnóstico e recuperação, como scanners antivírus, . Por padrão, quando o Windows está no modo de segurança, ele inicia apenas os drivers e serviços que foram pré-instalados com o Windows.

-   8.1 Exceções e exceções <dl> Drivers e serviços que devem ser iniciados no modo de segurança exigem uma isenção. A solicitação de isenção deve incluir cada driver ou serviço aplicável que escreve nas chaves do Registro SafeBoot e descrever os motivos técnicos pelos quais o aplicativo ou serviço deve ser executado no modo de segurança. O instalador do aplicativo deve registrar todos esses drivers e serviços usando estas chaves do Registro:  
    </dl>
    -   HKLM/System/CurrentControlSet/Control/SafeBoot/Minimal
    -   HKLM/System/CurrentControlSet/Control/SafeBoot/Network

**Observação:** Você deve testar esses drivers e serviços para garantir que eles funcionem no modo de segurança sem erros.

## <a name="9-apps-must-follow-user-account-control-guidelines"></a>9. Os aplicativos devem seguir as diretrizes de Controle de Conta de Usuário

Alguns aplicativos do Windows são executados no contexto de segurança de uma conta de administrador e os aplicativos geralmente solicitam direitos de usuário excessivos e privilégios do Windows. Controlar o acesso a recursos permite que os usuários controlem seus sistemas e protejam-nos contra alterações indesejadas. Uma alteração indesejada pode ser mal-intencionada, como um rootkit assumindo o controle do computador ou ser o resultado de uma ação feita por pessoas que têm privilégios limitados.. A regra mais importante para controlar o acesso aos recursos é fornecer a menor quantidade de contexto de usuário padrão de acesso necessária para que um usuário execute suas tarefas necessárias. As diretrizes de UAC (controle de conta de usuário) a seguir fornece ao aplicativo as permissões necessárias quando elas são necessárias para o aplicativo, sem deixar o sistema constantemente exposto a riscos de segurança. A maioria dos aplicativos não exige privilégios de administrador em tempo de execução e deve estar funcionando bem como um usuário padrão.<dl> 9.1 Seu aplicativo deve ter um manifesto que define os níveis de execução e informa ao sistema operacional quais privilégios o aplicativo requer para ser executado <dl> A marcação do manifesto do aplicativo se aplica somente a EXEs, não DLLs. Isso acontece porque o UAC não inspeciona DLLs durante a criação do processo. Também vale a pena notar que as regras de UAC não se aplicam aos Serviços do Windows. O manifesto pode ser inserido ou externo.  
Para criar um manifesto, crie um arquivo com o nome <nome do aplicativo>.exe.manifest e armazene-o \_ no mesmo diretório que EXE. Observe que qualquer manifesto externo será ignorado se o aplicativo tiver um manifesto interno. Por exemplo:  
<requestedExecutionLevel level=""asInvoker \| highestAvailable \| requireAdministrator"" uiAccess="true \| false""/>  
</dl> </dd> 9.2 Your app s main process must be run as a standard user (asInvoker). <dl> Todos os recursos administrativos devem ser movidos para um processo separado que é executado com privilégios administrativos. Aplicativos voltados para o usuário, como aqueles acessíveis por meio do grupo de programas no Menu Inicial, e que exigem elevação devem ser assinados pelo Authenticode.  
</dl> </dd> 9.3 Exceptions and Waivers <dl> Uma isenção é necessária para aplicativos que executem seu processo principal com privilégios elevados (requireAdministrator ou highestAvailable). O processo principal é identificado como o ponto de entrada do usuário para o aplicativo. As isenções serão consideradas para os seguintes cenários:

-   Ferramentas administrativas ou do sistema com nível de execução definido como highestAvailable e/ou requireAdministrator
-   Somente o aplicativo de estrutura de automação de acessibilidade ou interface do usuário define o sinalizador uiAccess como true para ignorar o UIPI (isolamento de privilégio de interface do usuário). Para iniciar corretamente a utilização do aplicativo, esse sinalizador deve ser assinado por Authenticode e deve residir em um local protegido no sistema de arquivos, ou seja, Arquivos de Programas.

  
</dl> </dd> </dl>

## <a name="10-apps-must-install-to-the-correct-folders-by-default"></a>10. Os aplicativos devem ser instalados nas pastas corretas por padrão

Os usuários devem ter uma experiência consistente e segura com o local de instalação padrão dos arquivos, mantendo a opção de instalar um aplicativo no local de sua escolha. Também é necessário armazenar dados do aplicativo no local correto para permitir que várias pessoas usem o mesmo computador sem corromper ou sobrescrever os dados e as configurações umas das outras. O Windows fornece locais específicos no sistema de arquivos para armazenar programas e componentes de software, dados de aplicativo compartilhados e dados de aplicativo específicos para um usuário<dl> 10.1 Seu aplicativo deve ser instalado na pasta Arquivos de Programas por padrão <dl> Para aplicativos nativos de 32 bits e 64 bits em %ProgramFiles%, e %ProgramFiles(x86)% para aplicativos de 32 bits em execução no x64. Os dados do usuário ou os dados do aplicativo nunca devem ser armazenados nesse local devido às permissões de segurança configuradas para essa pasta.  
</dl> </dd> 10.2 Your app must avoid starting automatically on startup <dl> Por exemplo, seu aplicativo não deve definir nenhum dos seguintes;  
</dl>

-   Chaves de run do Registro HKLM e ou HKCU em Software \\ Microsoft \\ Windows \\ CurrentVersion
-   Chaves de run do Registro HKLM e ou HKCU em Software \\ Wow6432Nãode \\ Microsoft \\ windows \\ CurrentVersion
-   Iniciar Menu TodosProgramas > INICIALIZAÇÃO

</dd> 10.3 Your app data, which must be shared among users on the computer, should be stored within ProgramData  
10.4 Your app s data that is exclusive to a specific user and that is not to be shared with other users of the computer, must be stored in Users\\<username>\\Appdata  
10.5 Seu aplicativo nunca deve gravar diretamente no diretório "Windows" e ou subdireções <dl> Use os métodos corretos para instalar arquivos, como fontes ou drivers.  
</dl> </dd> 10.6 Your app must write user data at first run and not during the installation in  per-machine  installations <dl> Quando o aplicativo é instalado, não há nenhum local de usuário correto no qual armazenar dados. As tentativas de um aplicativo de modificar comportamentos de associação padrão em um nível de computador após a instalação não serão bem-sucedidas. Em vez disso, os padrões devem ser reivindicados em um nível por usuário, o que impede que vários usuários sobrescrevam os padrões uns dos outros.  
</dl> </dd> 10.7 Exceptions and Waivers <dl> Uma isenção é necessária para aplicativos que escrevem no GAC (cache de assembly global) . Os aplicativos .NET devem manter as dependências de assembly privadas e armazená-los no diretório do aplicativo, a menos que o compartilhamento de um assembly seja explicitamente necessário.  
</dl> </dd> </dl>

## <a name="11-apps-must-support-multi-user-sessions"></a>11. Os aplicativos devem dar suporte a sessões de vários usuários

Os usuários do Windows devem ser capazes de executar sessões simultâneas sem conflitos ou interrupções.<dl> 11.1 Seu aplicativo deve garantir que, ao executar em várias sessões local ou remotamente, a funcionalidade normal do aplicativo não seja afetada negativamente  
11.2 As configurações e os arquivos de dados do aplicativo não devem persistir entre os usuários  
11.3 A privacidade e as preferências de um usuário devem ser isoladas para a sessão do usuário  
11.4 As instâncias do aplicativo devem ser isoladas umas das outras <dl> Isso significa que os dados do usuário de uma instância não são visíveis para outra instância do aplicativo. O som em uma sessão de usuário inativo não deve ser ouvido em uma sessão de usuário ativa. Nos casos em que várias instâncias de aplicativo usam recursos compartilhados, o aplicativo deve garantir que não haja um conflito.  
</dl> </dd> 11.5 Apps that are installed for multiple users must store data in the correct folder(s) and registry locations <dl> Consulte os requisitos do UAC.  
</dl> </dd> 11.6 User apps must be able to run in multiple user sessions (Fast User Switching) for both local and remote access  
11.7 Your app must check other terminal service (TS) sessions for existing instances of the app  
</dl>**Note:** If an app does not support multiple user sessions or remote access, it must clearly state this when launched from this kind of session.

## <a name="12-apps-must-support-x64-versions-of-windows"></a>12. Os aplicativos devem dar suporte a versões x64 do Windows

À medida que o hardware de 64 bits se torna mais comum, os usuários esperam que os desenvolvedores de aplicativos aproveitem os benefícios da arquitetura de 64 bits migrando seus aplicativos para 64 bits ou que as versões de 32 bits do aplicativo são bem executados em versões de 64 bits do Windows.<dl> 12.1 Seu aplicativo deve dar suporte nativo a 64 bits ou, no mínimo, aplicativos baseados no Windows de 32 bits devem ser executados perfeitamente em sistemas de 64 bits para manter a compatibilidade com versões de 64 bits do Windows  
12.2 Seu aplicativo e seus instaladores não devem conter nenhum código de 16 bits nem depender de nenhum componente de 16 bits  
12.3 A instalação do aplicativo deve detectar e instalar os drivers e componentes adequados para a arquitetura de 64 bits  
12.4 Todos os plug-ins de shell devem ser executados em versões de 64 bits do Windows  
12.5 O aplicativo em execução no emulador WoW64 não deve tentar subverter ou ignorar mecanismos de virtualização wow64 <dl> Se houver cenários específicos em que os aplicativos precisam detectar se estão em execução no emulador WoW64, eles devem fazer isso chamando IsWow64Process.  
</dl> </dd> </dl>

## <a name="summary-of-the-tests-performed-on-desktop-apps"></a>Resumo dos testes executados em aplicativos da Área de Trabalho



|   Nome do teste                                                             |   Resultados possíveis do teste   |
|-------------------------------------------------------------------------|---------------------------|
| Aderir às mensagens do gerenciador de reinicialização do sistema                               | Passar/Falhar               |
| Limpar instalação reversível                                                | Pass/Fail/Warning     |
| Teste de & de resiliência                                         | Pass/Fail/Warning     |
| Teste de arquivo assinado digitalmente                                              | Pass/Fail/Warning     |
| Instalar para o teste de pastas correto                                     | Aviso                   |
| Teste de sessão multiusuário                                                  | Aviso                   |
| Teste de verificação de versão do sistema operacional                                                | Passar/Falhar               |
| Teste de modo de segurança                                                          | Passar/Falhar               |
| Suporte ao teste do Windows x64                                                | Passar/Falhar               |
| Testar alterações nos recursos de segurança do Windows (Analisador de Superfície de Ataque) | Pass/Fail/Warning     |
| Testar alterações nos recursos de segurança do Windows (Analisador Binário binScope) | Aviso                   |
| Teste de UAC (controle de conta de usuário)                                         | Pass/Fail/Warning     |



 

## <a name="conclusion"></a>Conclusão

À medida que esses requisitos evoluem, observaremos as alterações no histórico de revisão abaixo. Os requisitos estáveis são essenciais para fazer seu melhor trabalho, portanto, vamos garantir que as alterações feitas sejam sustentáveis e continuar a proteger e aprimorar seus aplicativos.

Obrigado novamente por ingressar em nosso compromisso de fornecer excelentes experiências do cliente.

## <a name="revision-history"></a>Histórico de revisão



| Data         | Versão | Descrição da revisão                                            | Link para o documento                                                             |
|--------------|---------|-----------------------------------------------------------------|------------------------------------------------------------------------------|
| 20 de dezembro de 2011 | 1.0     | Rascunho inicial do documento para visualização.                          |                                                                              |
| 26 de janeiro de 2012 | 1,1     | Atualize para a seção \# 2.                                          | [1.1](archive--certification-requirements-for-windows-desktop-apps-v1-1.md) |
| 31 de maio de 2012 | 1.2     | Resultados de teste de resumo adicionados<br/> Documento final<br/> | 1.2                                                                          |



 

## <a name="learn-more-about-desktop-app-certification"></a>Saiba mais sobre a certificação de aplicativos de desktop



| Requisito                                                                     | Descrição                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  | Mais detalhes                                                                                                                                                                                                                                                                                |
|---------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Compatibilidade e resiliência                                                    | Falhas & travas são uma grande interrupção dos usuários e causam frustração. Os aplicativos devem ser resilientes e estáveis, eliminando essas falhas ajuda a garantir que o software seja mais previsível, passível de manutenção, com bom desempenho e confiável.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     | [Sistemas operacionais Windows Vista, Windows 7 e Windows 8](/previous-versions/windows/it-pro/windows-7/cc722305(v=ws.10))<br/> [Application Verifier](/previous-versions/aa480483(v=msdn.10))<br/> [AppInit DLLs](https://support.microsoft.com/kb/197571)<br/> |
| Siga as práticas recomendadas de segurança do Windows                                       | Usar as práticas recomendadas de segurança do Windows ajudará a evitar a criação de exposição a superfícies de ataque do Windows. As superfícies de ataque são os pontos de entrada que um invasor mal-intencionado poderia usar para explorar o sistema operacional aproveitando as vulnerabilidades no software de destino. Uma das piores vulnerabilidades de segurança é a elevação de privilégio.                                                                                                                                                                                                                                                                                                                                                                                                                                                                         | [Analisador de superfície de ataque](https://technet.microsoft.com/security/gg749821)<br/> [Listas de controle de acesso](/windows/desktop/SecAuthZ/access-control-lists)<br/>                                                                                                                                |
| Suporte a recursos de segurança do Windows                                               | O sistema operacional Windows implementou muitas medidas para dar suporte à segurança e privacidade do sistema. Os aplicativos devem dar suporte a essas medidas para manter a integridade do sistema operacional. Aplicativos compilados incorretamente poderiam causar estouros de buffer que, por sua vez, poderiam causar negação de serviço ou fazer com que um código mal-intencionado seja executado.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     | [Referência da ferramenta BinScope](https://blogs.microsoft.com/cybertrust/2012/08/15/microsofts-free-security-tools-binscope-binary-analyzer/)<br/>                                                                                                                                             |
| Aderir às mensagens do Gerenciador de reinicialização do sistema                                       | Quando os usuários iniciam o desligamento, na grande maioria dos casos, eles têm um desejo forte de ver o desligamento com sucesso; Eles podem estar com pressa para sair do escritório e "querem apenas" seus computadores para desligar. Os aplicativos devem respeitar esse desejo não bloqueando o desligamento. Na maioria dos casos, um desligamento pode não ser crítico, os aplicativos devem estar preparados para a possibilidade de um desligamento crítico.                                                                                                                                                                                                                                                                                                                                                                                                                                       | [Alterações de desligamento de aplicativo no Windows Vista](/previous-versions/windows/desktop/ms700677(v=vs.85))<br/> [Desenvolvimento do Gerenciador de reinicialização](/previous-versions/bb756958(v=msdn.10))<br/>                                                                              |
| Instalação reversível limpa                                                   | Uma instalação limpa e reversível permite que os usuários gerenciem com êxito (implante e removam) aplicativos em seus sistemas.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             | [Como instalar pré-requisitos com um aplicativo ClickOnce](/visualstudio/deployment/how-to-install-prerequisites-with-a-clickonce-application?view=vs-2015)<br/> [Instalação de aplicativos em sistemas de 64 bits](/windows/desktop/WinProg64/application-installation)<br/>                                                |
| Assinar digitalmente arquivos e drivers                                                | Uma assinatura digital Authenticode permite que os usuários tenham certeza de que o software é autêntico. Ele também permite detectar se um arquivo foi violado, por exemplo, se ele foi infectado por um vírus. A imposição de assinatura de código no modo kernel é um recurso do Windows conhecido como integridade de código (CI), que melhora a segurança do sistema operacional, verificando a integridade de um arquivo cada vez que a imagem do arquivo é carregada na memória. O CI detecta se o código mal-intencionado modificou um arquivo binário do sistema. Também gera um evento de log de diagnóstico e auditoria do sistema quando a assinatura de um módulo kernel não é verificada corretamente.                                                                                                                                                                            | [Assinaturas digitais para módulos de kernel no Windows](/previous-versions/windows/hardware/design/dn653559(v=vs.85))<br/>                                                                                                                                             |
| Não bloquear instalação ou inicialização de aplicativo com base na verificação de versão do sistema operacional | É importante que os clientes não sejam artificialmente impedidos de instalar ou executar seu aplicativo quando não houver nenhuma limitação técnica. Em geral, se os aplicativos foram escritos para o Windows Vista ou versões posteriores, eles não devem ter nenhum motivo para verificar a versão do sistema operacional.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            | [Controle de versão do sistema operacional](../win7appqual/operating-system-versioning.md)<br/>                                                                                                                                                                                           |
| Não carregar serviços e drivers no modo de segurança                                   | O modo de segurança permite que os usuários diagnostiquem e solucionem problemas no Windows. A menos que seja necessário para as operações básicas do sistema (por exemplo, drivers de dispositivo de armazenamento) ou para fins de diagnóstico e recuperação (por exemplo, scanners antivírus), os drivers e serviços não devem ser definidos para serem carregados no modo de segurança. Por padrão, o modo de segurança não inicia a maioria dos drivers e serviços que não vieram pré-instalados com o Windows. Eles devem permanecer desabilitados, a menos que o sistema os exija para operações básicas ou para fins de diagnóstico e recuperação.                                                                                                                                                                                                                                                                                         | [Determinando se o sistema operacional está sendo executado no modo de segurança](/windows-hardware/drivers/kernel/determining-whether-the-operating-system-is-running-in-safe-mode)<br/> [Como determinar se o sistema está sendo executado em modo de segurança de um driver de dispositivo](https://support.microsoft.com/kb/837643)<br/>       |
| Seguir as diretrizes de controle de conta de usuário (UAC)                                    | Alguns aplicativos do Windows são executados no contexto de segurança de uma conta de administrador, e muitos exigem direitos de usuário e privilégios do Windows excessivos. Controlar o acesso a recursos permite que os usuários estejam no controle de seus sistemas contra alterações indesejadas (uma alteração indesejada pode ser mal-intencionada, como um rootkit furtivamente assumir a máquina ou uma ação de pessoas que têm privilégios limitados, por exemplo, um funcionário instalando software proibido em um computador de trabalho). A regra mais importante para controlar o acesso a recursos é fornecer a menor quantidade de contexto de usuário padrão de acesso necessário para que um usuário execute suas tarefas necessárias. As diretrizes do UAC a seguir fornecem ao aplicativo as permissões necessárias, quando necessário, sem deixar o sistema constantemente exposto a riscos de segurança. | [Controle de conta de usuário](/windows/desktop/uxguide/winenv-uac)<br/> [UAC: diretrizes de atualização de aplicativo](/previous-versions/aa480152(v=msdn.10))<br/>                                                                       |
| Instalar nas pastas corretas por padrão                                       | Os usuários devem ter uma experiência consistente e segura com o local de instalação padrão dos arquivos, mantendo a opção de instalar um aplicativo no local escolhido. Também é necessário armazenar os dados do aplicativo no local correto para permitir que várias pessoas usem o mesmo computador sem corromper ou substituir os dados e as configurações uns dos outros.                                                                                                                                                                                                                                                                                                                                                                                                                                                          | [Resumo dos requisitos de instalação/desinstalação](/previous-versions/ms954376(v=msdn.10))<br/>                                                                                                                                                                                    |
| Suporte a sessões de vários usuários                                                     | Os usuários do Windows devem ser capazes de executar sessões simultâneas sem conflitos ou interrupções.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      | [Diretrizes de programação de Serviços de Área de Trabalho Remota](/windows/desktop/TermServ/terminal-services-programming-guidelines)<br/>                                                                                                                                                                      |
| Suporte a versões x64 do Windows                                                 | Como o hardware de 64 bits se torna mais predominante, os usuários esperam que os desenvolvedores de aplicativos aproveitem os benefícios da arquitetura de 64 bits migrando seus aplicativos para 64 bits ou que as versões de 32 bits do aplicativo sejam executadas bem em versões de 64 bits do Windows.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             | [Compatibilidade de aplicativos: Windows Vista 64-bit](/previous-versions/bb756962(v=msdn.10))<br/>                                                                                                                                                                              |



 

## <a name="see-also"></a>Confira também

-   [Programa de certificação de hardware do Windows](/previous-versions/windows/hardware/hck/jj124227(v=vs.85))
-   [Requisitos de certificação de aplicativos da Windows Store](/legal/windows/agreements/store-policies)

 

