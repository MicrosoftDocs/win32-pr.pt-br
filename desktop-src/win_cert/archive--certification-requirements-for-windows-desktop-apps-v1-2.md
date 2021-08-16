---
title: Requisitos de certificação de arquivo Windows Aplicativos da Área de Trabalho v1.2
description: Document version 1.2Document date 31 de maio de 2012 Este documento contém os requisitos técnicos e as qualificações de qualificação que um aplicativo da área de trabalho deve atender para participar do Programa de Certificação de Aplicativos da Área de Trabalho Windows 8.
ms.assetid: A65D7FE9-554B-4D59-91B7-E1582F7C6C87
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: c8ae995dcc9398ec0ee650388af761399f752a02bba4c365cf5d39f35a03973f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118203785"
---
# <a name="archive-certification-requirements-for-windows-desktop-apps-v12"></a>Arquivo morto: requisitos de certificação Windows Aplicativos da Área de Trabalho v1.2

**Versão do documento:** 1.2

**Data do documento:** 31 de maio de 2012

Este documento contém os requisitos técnicos e as qualificações de qualificação que um aplicativo da área de trabalho deve atender para participar do programa Windows 8 de Certificação de Aplicativos da Área de Trabalho. Por Windows 7, esse programa era conhecido como Programa de Logotipo Windows Software.

## <a name="welcome"></a>Seja bem-vindo!

A Windows plataforma dá suporte a um amplo ecossistema de produtos e parceiros. Exibir o logotipo Windows em seu produto representa uma relação e um compromisso compartilhado com a qualidade entre a Microsoft e sua empresa. Os clientes confiam na Windows em seu produto porque ele garante que ele atenda aos padrões de compatibilidade e seja bem-Windows plataforma. Passar com êxito Windows certificação de aplicativo permite que seu aplicativo seja apresentado no Centro de Compatibilidade do Windows e também é uma etapa necessária para listar uma referência de aplicativo da área de trabalho na Windows Store.

O Windows de Certificação de Aplicativos do Windows é feito de requisitos técnicos e de programa para ajudar a garantir que aplicativos de terceiros que carregam a marca Windows sejam fáceis de instalar e confiáveis em PCs que executam Windows. Os clientes dão valor à estabilidade, à compatibilidade, à confiabilidade, ao desempenho e à qualidade nos sistemas que compram. A Microsoft concentra seus investimentos para atender a esses requisitos para aplicativos de software projetados para executar na plataforma Windows para PCs. Esses esforços incluem testes de compatibilidade para consistência de experiência, melhor desempenho e segurança aprimorada em PCs que executam Windows software. Os testes de compatibilidade da Microsoft foram projetados em colaboração com parceiros do setor e são continuamente aprimorados em resposta aos desenvolvimentos do setor e à demanda do consumidor.

O Windows kit de certificação de aplicativo é usado para validar a conformidade com esses requisitos e substitui o WSLK usado para validação no programa de logotipo de software Windows 7. O Windows kit de certificação de aplicativos é um dos componentes incluídos no SDK (Software Development Kit) do Windows.

## <a name="app-eligibility"></a>Qualificação do aplicativo

Para que um aplicativo seja qualificado para Windows 8 de Aplicativo da Área de Trabalho, ele deve atender aos critérios a seguir e a todos os requisitos técnicos listados neste documento.

-   Ele deve ser um aplicativo autônomo
-   Ele deve ser executado em um computador Windows 8.1 local
-   Pode ser um componente cliente de um aplicativo Windows Server certificado
-   Ele deve ser o código e o recurso concluídos

## <a name="1-apps-are-compatible-and-resilient"></a>1. Os aplicativos são compatíveis e resilientes

Os momentos em que um aplicativo falha ou para de responder causam muita frustração do usuário. Espera-se que os aplicativos sejam resilientes e estáveis e eliminar essas falhas ajuda a garantir que o software seja mais previsível, mantenível, com desempenho e confiável.<dl> 1.1 Seu aplicativo não deve assumir uma dependência Windows modos de compatibilidade, mensagem AppHelp e outras correções de compatibilidade  
1.2 Seu aplicativo não deve ter uma dependência no runtime VB6  
1.3 Seu aplicativo não deve carregar DLLs arbitrárias para interceptar chamadas à API win32 usando dlls do Software HKLM \\ \\ microsoft Windows NT \\ \\ CurrentVersion Windows \\ AppInit. \_  
</dl>

## <a name="2-apps-must-adhere-to-windows-security-best-practices"></a>2. Os aplicativos devem seguir as Windows práticas recomendadas de segurança

Usar Windows práticas recomendadas de segurança ajudará a evitar a criação de exposição Windows superfícies de ataque. Superfícies de ataque são os pontos de entrada que um invasor mal-intencionado pode usar para explorar o sistema operacional aproveitando as vulnerabilidades no software de destino. Uma das piores vulnerabilidades de segurança é a elevação de privilégio.

<dl> 2.1 Seu aplicativo deve usar <a href="/windows/desktop/SecAuthZ/access-control-lists">ACLs</a> fortes e apropriadas para proteger arquivos executáveis  
2.2 Seu aplicativo deve usar <a href="/windows/desktop/SecAuthZ/access-control-lists">ACLs</a> fortes e apropriadas para proteger diretórios  
2.3 Seu aplicativo deve usar <a href="/windows/desktop/SecAuthZ/access-control-lists">ACLs</a> fortes e apropriadas para proteger chaves do Registro  
2.4 Seu aplicativo deve usar <a href="/windows/desktop/SecAuthZ/access-control-lists">ACLs</a> fortes e apropriadas para proteger diretórios que contêm objetos  
2.5 Seu aplicativo deve reduzir o acesso não administrador a serviços vulneráveis a adulterações  
2.6 Seu aplicativo deve impedir que serviços com reinicializações rápidas reiniciem mais de duas vezes a cada 24 horas
</dl>**Observação: o acesso só deve ser concedido às entidades que o exigem.**

O Windows de Certificação de Aplicativos do Windows verificará se as superfícies de ataque do Windows não são expostas verificando se as ACLs e os Serviços são implementados de uma maneira que não coloque o sistema Windows em risco.

## <a name="3-apps-support-windows-security-features"></a>3. Os aplicativos são Windows recursos de segurança

O Windows sistema operacional tem muitos recursos que suportam segurança e privacidade do sistema. Os aplicativos devem dar suporte a esses recursos para manter a integridade do sistema operacional. Aplicativos compilados incorretamente podem causar estouros de buffer que, por sua vez, podem causar negação de serviço ou permitir a execução de código mal-intencionado. <dl> 3.1 Seu aplicativo não deve usar AllowPartiallyTrustedCallersAttribute (APTCA) para garantir o acesso seguro a assemblies de nome forte  
3.2 Seu aplicativo deve ser compilado usando o sinalizador /SafeSEH para garantir o tratamento seguro de exceções  
3.3 Seu aplicativo deve ser compilado usando o sinalizador /NXCOMPAT para impedir a execução de dados  
3.4 Seu aplicativo deve ser compilado usando o sinalizador /DYNAMICBASE para randomização de layout de espaço de endereço (ASLR)  
3.5 Seu aplicativo não deve ler/gravar as seções pe compartilhadas  
</dl>

## <a name="4-apps-must-adhere-to-system-restart-manager-messages"></a>4. Os aplicativos devem aderir às mensagens do gerenciador de reinicialização do sistema

Quando os usuários iniciam o desligamento, eles geralmente têm um forte desejo de ver o desligamento bem-sucedido; eles podem estar com uma vontade de sair do escritório e apenas querem que seus computadores desliguem. Os aplicativos devem respeitar esse desejo sem bloquear o desligamento. Embora, na maioria dos casos, um desligamento possa não ser crítico, os aplicativos devem estar preparados para a possibilidade de um desligamento crítico.<dl> 4.1 Seu aplicativo deve lidar com desligamentos críticos adequadamente <dl> Em um desligamento crítico, os aplicativos que retornam FALSE para WM QUERYENDSESSION serão enviados WM ENDSESSION e fechados, enquanto aqueles que se desempenham em resposta a \_ \_ WM \_ QUERYENDSESSION serão encerrados.  
</dl> </dd> 4.2 A GUI app must return TRUE immediately in preparation for a restart <dl> WM \_ QUERYENDSESSION com LPARAM = ENDSESSION \_ CLOSEAPP(0x1).  
Os aplicativos de console podem chamar SetConsoleCtrlHandler para especificar a função que manipulará notificações de desligamento. Os aplicativos de serviço podem chamar RegisterServiceCtrlHandlerEx para especificar a função que receberá notificações de desligamento.  
</dl> </dd> 4.3 Your app must return 0 within 30 seconds and shut down <dl> WM \_ ENDSESSION com LPARAM = ENDSESSION \_ CLOSEAPP(0x1).  
No mínimo, o aplicativo deve se preparar salvando todos os dados do usuário e informando as informações necessárias após uma reinicialização.  
</dl> </dd> 4.4 Console apps that receive the CTRL\_C\_EVENT notification should shut down immediately  
4.5 Drivers must not veto a system shutdown event  
</dl>**Note: Apps that must block shutdown because of an operation that cannot be interrupted should explain the reason to the user.** Use ShutdownBlockReasonCreate to register a string that explains the reason to the user. When the operation has completed, the app should call ShutdownBlockReasonDestroy to indicate that the system can be shut down.

## <a name="5-apps-must-support-a-clean-reversible-installation"></a>5. Os aplicativos devem dar suporte a uma instalação limpa e reversível

Uma instalação limpa e reversível permite que os usuários gerenciem (implantem e removam) aplicativos em seus sistemas com êxito.<dl> 5.1 Seu aplicativo deve implementar corretamente uma instalação limpa e reversível <dl> Se a instalação falhar, o aplicativo deverá ser capaz de reverter e restaurar o computador para seu estado anterior.  
</dl> </dd> 5.2 Your app must never force the user to restart the computer immediately <dl> Reiniciar o computador nunca deve ser a única opção no final de uma instalação ou atualização. Os usuários devem ter a oportunidade de reiniciar mais tarde.  
</dl> </dd> 5.3 Your app must never be dependent on 8.3 short file names (SFN)  
5.4 Your app must never block silent install/uninstall  
5.5 Your app installer must create the correct registry entries to allow successful detection and uninstalls <dl> Windows ferramentas de inventário e ferramentas de telemetria exigem informações completas sobre aplicativos instalados. Se você estiver usando um instalador baseado em MSI, o MSI criará automaticamente as entradas do Registro abaixo. Se você não estiver usando um instalador MSI, o módulo de instalação deverá criar as seguintes entradas do Registro durante a instalação:  
</dl>

-   DisplayName
-   InstallLocation
-   Publisher
-   UninstallString
-   VersionMajor ou MajorVersion
-   VersionMinor ou MinorVersion

</dd> </dl>

## <a name="6-apps-must-digitally-sign-files-and-drivers"></a>6. Os aplicativos devem assinar arquivos e drivers digitalmente

Uma assinatura digital Authenticode permite que os usuários certifiquem-se de que o software é original. Ele também permite detectar se um arquivo foi adulterado, como se ele foi infectado por um vírus. A imposição de assinatura de código no modo kernel é um recurso de Windows conhecido como CI (integridade de código), que melhora a segurança do sistema operacional verificando a integridade de um arquivo sempre que a imagem do arquivo é carregada na memória. A CI detecta se o código mal-intencionado modificou um arquivo binário do sistema. Também gera um evento de log de diagnóstico e auditoria do sistema quando a assinatura de um módulo de kernel falha ao verificar corretamente. <dl> 6.1 Todos os arquivos executáveis (.exe, .dll, .ocx, .sys, .cpl, .drv, .scr) devem ser assinados com um certificado Authenticode  
6.2 Todos os drivers de modo kernel instalados pelo aplicativo devem ter uma assinatura da Microsoft obtida por meio do programa Windows certificação de hardware. Todos os drivers de filtro do Sistema de Arquivos devem ser assinados pela Microsoft.  
6.3 Exceções e exceções <dl> As isenções serão consideradas somente para redistribuíveis de terceiros não assinados, exceto drivers. Uma prova de comunicação solicitando uma versão assinada dos redistribuíveis é necessária para que essa isenção seja concedida.  
</dl> </dd> </dl>

## <a name="7-apps-don-t-block-installation-or-app-launch-based-on-an-operating-system-version-check"></a>7. Os aplicativos não bloqueiam a instalação ou a iniciação do aplicativo com base em uma verificação de versão do sistema operacional

É importante que os clientes não sejam impedidos artificialmente de instalar ou executar seu aplicativo quando não houver limitações técnicas. Em geral, se os aplicativos foram escritos para Windows Vista ou versões posteriores do Windows, eles não devem ter que verificar a versão do sistema operacional.<dl> 7.1 Seu aplicativo não deve executar verificações de versão em busca de igualdade <dl> Se você precisar de um recurso específico, verifique se o próprio recurso está disponível. Se você precisar Windows XP, verifique se há Windows XP ou posterior (>= 5,1). Dessa forma, seu código de detecção continuará a funcionar em versões futuras do Windows. Os instaladores de driver e os módulos de desinstalação nunca devem verificar a versão do sistema operacional.  
</dl> </dd> 7.2 Exceptions and Waivers will be considered for apps meeting the criteria below:

-   Aplicativos que são entregues como um pacote que também são executados no Windows XP, Windows Vista e Windows 7 e precisam verificar a versão do sistema operacional para determinar quais componentes instalar em um determinado sistema operacional.
-   Aplicativos que verificam apenas a versão mínima do sistema operacional (somente durante a instalação, não em runtime) usando apenas as chamadas à API aprovadas e que listam corretamente o requisito mínimo de versão no manifesto do aplicativo.
-   Aplicativos de segurança (antivírus, firewall etc.), utilitários do sistema (por exemplo, desfragmentação, backups e ferramentas de diagnóstico) que verificam a versão do sistema operacional usando apenas as chamadas à API aprovadas.

  
</dl>

## <a name="8-apps-don-t-load-services-or-drivers-in-safe-mode"></a>8. Os aplicativos não carregam serviços ou drivers no modo de segurança

Cofre modo permite que os usuários dia diagnosticem e solucionem problemas Windows. Drivers e serviços não devem ser definidos para serem carregados no modo de segurança, a menos que sejam necessários para operações básicas do sistema, como drivers de dispositivo de armazenamento ou para fins de diagnóstico e recuperação, como scanners antivírus, . Por padrão, quando Windows está no modo de segurança, ele inicia apenas os drivers e serviços que foram pré-instalados com Windows.

-   8.1 Exceções e exceções <dl> Drivers e serviços que devem ser iniciados no modo de segurança exigem uma isenção. A solicitação de isenção deve incluir cada driver ou serviço aplicável que escreve nas chaves do Registro SafeBoot e descrever os motivos técnicos pelos quais o aplicativo ou serviço deve ser executado no modo de segurança. O instalador do aplicativo deve registrar todos esses drivers e serviços usando estas chaves do Registro:  
    </dl>
    -   HKLM/System/CurrentControlSet/Control/SafeBoot/Minimal
    -   HKLM/System/CurrentControlSet/Control/SafeBoot/Network

**Observação:** Você deve testar esses drivers e serviços para garantir que eles funcionem no modo de segurança sem erros.

## <a name="9-apps-must-follow-user-account-control-guidelines"></a>9. Os aplicativos devem seguir as diretrizes de Controle de Conta de Usuário

Alguns Windows aplicativos executados no contexto de segurança de uma conta de administrador, e os aplicativos geralmente solicitam direitos de usuário excessivos e Windows privilégios. Controlar o acesso a recursos permite que os usuários controlem seus sistemas e protejam-nos contra alterações indesejadas. Uma alteração indesejada pode ser mal-intencionada, como um rootkit assumindo o controle do computador ou ser o resultado de uma ação feita por pessoas que têm privilégios limitados.. A regra mais importante para controlar o acesso aos recursos é fornecer a menor quantidade de contexto de usuário padrão de acesso necessária para que um usuário execute suas tarefas necessárias. As diretrizes de UAC (controle de conta de usuário) a seguir fornece ao aplicativo as permissões necessárias quando elas são necessárias para o aplicativo, sem deixar o sistema constantemente exposto a riscos de segurança. A maioria dos aplicativos não exige privilégios de administrador em tempo de execução e deve estar funcionando bem como um usuário padrão.<dl> 9.1 Seu aplicativo deve ter um manifesto que define os níveis de execução e informa ao sistema operacional quais privilégios o aplicativo requer para ser executado <dl> A marcação do manifesto do aplicativo se aplica somente a EXEs, não DLLs. Isso acontece porque o UAC não inspeciona DLLs durante a criação do processo. Também vale a pena notar que as regras de UAC não se aplicam aos Windows Serviços. O manifesto pode ser inserido ou externo.  
Para criar um manifesto, crie um arquivo com o nome <nome do aplicativo>.exe.manifest e armazene-o no mesmo diretório \_ que EXE. Observe que qualquer manifesto externo será ignorado se o aplicativo tiver um manifesto interno. Por exemplo:  
<requestedExecutionLevel level=""asInvoker \| highestAvailable \| requireAdministrator"" uiAccess="true \| false""/>  
</dl> </dd> 9.2 Your app s main process must be run as a standard user (asInvoker). <dl> Todos os recursos administrativos devem ser movidos para um processo separado que é executado com privilégios administrativos. Aplicativos voltados para o usuário, como aqueles acessíveis por meio do grupo de programas no Menu Inicial, e que exigem elevação devem ser assinados pelo Authenticode.  
</dl> </dd> 9.3 Exceptions and Waivers <dl> Uma isenção é necessária para aplicativos que executem seu processo principal com privilégios elevados (requireAdministrator ou highestAvailable). O processo principal é identificado como o ponto de entrada do usuário para o aplicativo. As isenções serão consideradas para os seguintes cenários:

-   Ferramentas administrativas ou do sistema com nível de execução definido como highestAvailable e/ou requireAdministrator
-   Somente o aplicativo de estrutura de automação de acessibilidade ou interface do usuário define o sinalizador uiAccess como true para ignorar o UIPI (isolamento de privilégio de interface do usuário). Para iniciar corretamente a utilização do aplicativo, esse sinalizador deve ser assinado por Authenticode e deve residir em um local protegido no sistema de arquivos, ou seja, Arquivos de Programas.

  
</dl> </dd> </dl>

## <a name="10-apps-must-install-to-the-correct-folders-by-default"></a>10. Os aplicativos devem ser instalados nas pastas corretas por padrão

Os usuários devem ter uma experiência consistente e segura com o local de instalação padrão dos arquivos, mantendo a opção de instalar um aplicativo no local de sua escolha. Também é necessário armazenar dados do aplicativo no local correto para permitir que várias pessoas usem o mesmo computador sem corromper ou sobrescrever os dados e as configurações umas das outras. Windows fornece locais específicos no sistema de arquivos para armazenar programas e componentes de software, dados de aplicativo compartilhados e dados de aplicativo específicos para um usuário<dl> 10.1 Seu aplicativo deve ser instalado na pasta Arquivos de Programas por padrão <dl> Para aplicativos nativos de 32 bits e 64 bits em %ProgramFiles%, e %ProgramFiles(x86)% para aplicativos de 32 bits em execução no x64. Os dados do usuário ou os dados do aplicativo nunca devem ser armazenados nesse local devido às permissões de segurança configuradas para essa pasta.  
</dl> </dd> 10.2 Your app must avoid starting automatically on startup <dl> Por exemplo, seu aplicativo não deve definir nenhum dos seguintes;  
</dl>

-   Chaves de run do Registro HKLM e ou HKCU em Software \\ Microsoft \\ Windows \\ CurrentVersion
-   Chaves de run do Registro HKLM e ou HKCU em Software \\ Wow6432Nãode \\ Microsoft \\ windows \\ CurrentVersion
-   Iniciar Menu TodosProgramas > INICIALIZAÇÃO

</dd> 10.3 Your app data, which must be shared among users on the computer, should be stored within ProgramData  
10.4 Your app s data that is exclusive to a specific user and that is not to be shared with other users of the computer, must be stored in Users\\<username>\\Appdata  
10.5 Seu aplicativo nunca deve gravar diretamente no diretório "Windows" e ou subdirecional <dl> Use os métodos corretos para instalar arquivos, como fontes ou drivers.  
</dl> </dd> 10.6 Your app must write user data at first run and not during the installation in  per-machine  installations <dl> Quando o aplicativo é instalado, não há nenhum local de usuário correto no qual armazenar dados. As tentativas de um aplicativo de modificar comportamentos de associação padrão em um nível de computador após a instalação não serão bem-sucedidas. Em vez disso, os padrões devem ser reivindicados em um nível por usuário, o que impede que vários usuários sobrescrevam os padrões uns dos outros.  
</dl> </dd> 10.7 Exceptions and Waivers <dl> Uma isenção é necessária para aplicativos que escrevem no GAC (cache de assembly global) . Os aplicativos .NET devem manter as dependências de assembly privadas e armazená-los no diretório do aplicativo, a menos que o compartilhamento de um assembly seja explicitamente necessário.  
</dl> </dd> </dl>

## <a name="11-apps-must-support-multi-user-sessions"></a>11. Os aplicativos devem dar suporte a sessões de vários usuários

Windows os usuários devem ser capazes de executar sessões simultâneas sem conflitos ou interrupções.<dl> 11.1 Seu aplicativo deve garantir que, ao executar em várias sessões local ou remotamente, a funcionalidade normal do aplicativo não seja afetada negativamente  
11.2 As configurações e os arquivos de dados do aplicativo não devem persistir entre os usuários  
11.3 A privacidade e as preferências do usuário devem ser isoladas para a sessão do usuário  
11.4 As instâncias do aplicativo devem ser isoladas umas das outras <dl> Isso significa que os dados do usuário de uma instância não são visíveis para outra instância do aplicativo. O som em uma sessão de usuário inativo não deve ser ouvido em uma sessão de usuário ativa. Nos casos em que várias instâncias de aplicativo usam recursos compartilhados, o aplicativo deve garantir que não haja um conflito.  
</dl> </dd> 11.5 Apps that are installed for multiple users must store data in the correct folder(s) and registry locations <dl> Consulte os requisitos do UAC.  
</dl> </dd> 11.6 User apps must be able to run in multiple user sessions (Fast User Switching) for both local and remote access  
11.7 Your app must check other terminal service (TS) sessions for existing instances of the app  
</dl>**Note:** If an app does not support multiple user sessions or remote access, it must clearly state this when launched from this kind of session.

## <a name="12-apps-must-support-x64-versions-of-windows"></a>12. Os aplicativos devem dar suporte a versões x64 do Windows

À medida que o hardware de 64 bits se torna mais comum, os usuários esperam que os desenvolvedores de aplicativos aproveitem os benefícios da arquitetura de 64 bits migrando seus aplicativos para 64 bits ou que as versões de 32 bits do aplicativo são bem executados em versões de 64 bits do Windows.<dl> 12.1 Seu aplicativo deve dar suporte nativo a 64 bits ou, no mínimo, aplicativos baseados em Windows de 32 bits devem ser executados perfeitamente em sistemas de 64 bits para manter a compatibilidade com versões de 64 bits do Windows  
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
| Cofre modo de teste                                                          | Passar/Falhar               |
| Suporte ao teste de Windows x64                                                | Passar/Falhar               |
| Testar se há alterações nos Windows de segurança (Analisador de Superfície de Ataque) | Pass/Fail/Warning     |
| Testar se há alterações nos Windows de segurança (BinScope Binary Analyzer) | Aviso                   |
| Teste de UAC (controle de conta de usuário)                                         | Pass/Fail/Warning     |



 

## <a name="conclusion"></a>Conclusão

À medida que esses requisitos evoluem, observaremos as alterações no histórico de revisão abaixo. Os requisitos estáveis são essenciais para fazer seu melhor trabalho, portanto, vamos garantir que as alterações feitas sejam sustentáveis e continuar a proteger e aprimorar seus aplicativos.

Agradecemos novamente por participar de nosso compromisso de fornecer ótimas experiências de clientes.

## <a name="revision-history"></a>Histórico de revisão



| Data         | Versão | Descrição da revisão                                            | Link para o documento                                                             |
|--------------|---------|-----------------------------------------------------------------|------------------------------------------------------------------------------|
| 20 de dezembro de 2011 | 1.0     | Rascunho inicial do documento para Visualização.                          |                                                                              |
| 26 de janeiro de 2012 | 1,1     | Atualize para a \# seção 2.                                          | [1.1](archive--certification-requirements-for-windows-desktop-apps-v1-1.md) |
| 31 de maio de 2012 | 1.2     | Adicionados resultados de teste de resumo<br/> Documento final<br/> | 1.2                                                                          |



 

## <a name="learn-more-about-desktop-app-certification"></a>Saiba mais sobre a certificação de aplicativo da área de trabalho



| Requisito                                                                     | Descrição                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  | Mais detalhes                                                                                                                                                                                                                                                                                |
|---------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Compatibilidade e resiliência                                                    | Falhas & travamentos são uma grande interrupção para os usuários e causam frustração. Espera-se que os aplicativos sejam resilientes e estáveis, eliminar essas falhas ajuda a garantir que o software seja mais previsível, mantenível, com desempenho e confiável.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     | [Windows Vista, Windows 7 e Windows 8 operacionais](/previous-versions/windows/it-pro/windows-7/cc722305(v=ws.10))<br/> [Application Verifier](/previous-versions/aa480483(v=msdn.10))<br/> [AppInit DLLs](https://support.microsoft.com/kb/197571)<br/> |
| Seguir as Segurança do Windows práticas recomendadas                                       | Usar Windows práticas recomendadas de segurança ajudará a evitar a criação de exposição Windows superfícies de ataque. Superfícies de ataque são os pontos de entrada que um invasor mal-intencionado pode usar para explorar o sistema operacional aproveitando as vulnerabilidades no software de destino. Uma das piores vulnerabilidades de segurança é a elevação de privilégio.                                                                                                                                                                                                                                                                                                                                                                                                                                                                         | [Analisador de superfície de ataque](https://technet.microsoft.com/security/gg749821)<br/> [Listas de controle de acesso](/windows/desktop/SecAuthZ/access-control-lists)<br/>                                                                                                                                |
| Suporte Segurança do Windows recursos                                               | O Windows sistema operacional implementou muitas medidas para dar suporte à segurança e à privacidade do sistema. Os aplicativos devem dar suporte a essas medidas para manter a integridade do sistema operacional. Aplicativos compilados incorretamente podem causar estouros de buffer que, por sua vez, podem causar negação de serviço ou fazer com que o código mal-intencionado seja executado.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     | [Referência da ferramenta BinScope](https://blogs.microsoft.com/cybertrust/2012/08/15/microsofts-free-security-tools-binscope-binary-analyzer/)<br/>                                                                                                                                             |
| Aderir às mensagens do System Restart Manager                                       | Quando os usuários iniciam o desligamento, na grande maioria dos casos, eles têm um forte desejo de ver o desligamento bem-sucedido; eles podem estar com uma vontade de sair do escritório e "apenas querem" que seus computadores desliguem. Os aplicativos devem respeitar esse desejo sem bloquear o desligamento. Embora, na maioria dos casos, um desligamento possa não ser crítico, os aplicativos devem estar preparados para a possibilidade de um desligamento crítico.                                                                                                                                                                                                                                                                                                                                                                                                                                       | [Alterações de desligamento do aplicativo no Windows Vista](/previous-versions/windows/desktop/ms700677(v=vs.85))<br/> [Reiniciar o desenvolvimento do Gerenciador](/previous-versions/bb756958(v=msdn.10))<br/>                                                                              |
| Limpar instalação reversível                                                   | Uma instalação limpa e reversível permite que os usuários gerenciem (implantem e removam) aplicativos em seus sistemas com êxito.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             | [Como instalar pré-requisitos com um aplicativo ClickOnce](/visualstudio/deployment/how-to-install-prerequisites-with-a-clickonce-application?view=vs-2015)<br/> [Instalação do aplicativo em sistemas de 64 bits](/windows/desktop/WinProg64/application-installation)<br/>                                                |
| Assinar arquivos e drivers digitalmente                                                | Uma assinatura digital Authenticode permite que os usuários certifiquem-se de que o software é original. Ele também permite detectar se um arquivo foi adulterado, por exemplo, se ele foi infectado por um vírus. A imposição de assinatura de código no modo kernel é um recurso de Windows conhecido como CI (integridade de código), que melhora a segurança do sistema operacional verificando a integridade de um arquivo sempre que a imagem do arquivo é carregada na memória. A CI detecta se o código mal-intencionado modificou um arquivo binário do sistema. Também gera um evento de log de diagnóstico e auditoria do sistema quando a assinatura de um módulo de kernel falha ao verificar corretamente.                                                                                                                                                                            | [Assinaturas digitais para módulos de kernel Windows](/previous-versions/windows/hardware/design/dn653559(v=vs.85))<br/>                                                                                                                                             |
| Não bloqueie a instalação ou a iniciação do aplicativo com base na verificação de versão do sistema operacional | É importante que os clientes não sejam impedidos artificialmente de instalar ou executar seu aplicativo quando não houver limitações técnicas. Em geral, se os aplicativos foram escritos para Windows Vista ou versões posteriores, eles não devem ter motivo para verificar a versão do sistema operacional.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            | [Versão do sistema operacional](../win7appqual/operating-system-versioning.md)<br/>                                                                                                                                                                                           |
| Não carregar serviços e drivers no modo Cofre serviço                                   | Cofre modo permite que os usuários dia diagnosticem e solucionem problemas Windows. A menos que seja necessário para operações básicas do sistema (por exemplo, drivers de dispositivo de armazenamento) ou para fins de diagnóstico e recuperação (por exemplo, scanners antivírus), os drivers e os serviços não devem ser definidos para serem carregados no modo de segurança. Por padrão, o modo de segurança não inicia a maioria dos drivers e serviços que não foram pré-instalados com Windows. Eles devem permanecer desabilitados, a menos que o sistema os exija para operações básicas ou para fins de diagnóstico e recuperação.                                                                                                                                                                                                                                                                                         | [Determinando se o sistema operacional está em execução no modo Cofre sistema](/windows-hardware/drivers/kernel/determining-whether-the-operating-system-is-running-in-safe-mode)<br/> [Como determinar se o sistema está em execução no modo Cofre de um driver de dispositivo](https://support.microsoft.com/kb/837643)<br/>       |
| Seguir as diretrizes do UAC (Controle de Conta de Usuário)                                    | Alguns Windows aplicativo são executados no contexto de segurança de uma conta de administrador e muitos exigem direitos de usuário excessivos e Windows privilégios. Controlar o acesso aos recursos permite que os usuários controlem seus sistemas contra alterações indesejadas (uma alteração indesejada pode ser mal-intencionada, como um rootkit assumindo o computador de forma furtiva ou uma ação de pessoas que têm privilégios limitados, por exemplo, um funcionário instalando software proibido em um computador de trabalho). A regra mais importante para controlar o acesso aos recursos é fornecer a menor quantidade de contexto de usuário padrão de acesso necessária para que um usuário execute suas tarefas necessárias. As diretrizes de UAC a seguir fornece ao aplicativo as permissões necessárias quando necessário, sem deixar o sistema constantemente exposto a riscos de segurança. | [Controle de conta de usuário](/windows/desktop/uxguide/winenv-uac)<br/> [UAC: Diretrizes de atualização de aplicativo](/previous-versions/aa480152(v=msdn.10))<br/>                                                                       |
| Instalar as pastas corretas por padrão                                       | Os usuários devem ter uma experiência consistente e segura com o local de instalação padrão dos arquivos, mantendo a opção de instalar um aplicativo no local escolhido. Também é necessário armazenar dados do aplicativo no local correto para permitir que várias pessoas usem o mesmo computador sem corromper ou sobrescrever os dados e as configurações umas das outras.                                                                                                                                                                                                                                                                                                                                                                                                                                                          | [Resumo dos requisitos de instalação/desinstalação](/previous-versions/ms954376(v=msdn.10))<br/>                                                                                                                                                                                    |
| Suporte a sessões de vários usuários                                                     | Windows os usuários devem ser capazes de executar sessões simultâneas sem conflitos ou interrupções.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      | [diretrizes Serviços de Área de Trabalho Remota programação de Serviços de Área de Trabalho Remota](/windows/desktop/TermServ/terminal-services-programming-guidelines)<br/>                                                                                                                                                                      |
| Suporte a versões x64 do Windows                                                 | À medida que o hardware de 64 bits se torna mais predominante, os usuários esperam que os desenvolvedores de aplicativos aproveitem os benefícios da arquitetura de 64 bits migrando seus aplicativos para 64 bits ou que as versões de 32 bits do aplicativo são bem executados em versões de 64 bits do Windows.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             | [Compatibilidade do aplicativo: Windows Vista de 64 bits](/previous-versions/bb756962(v=msdn.10))<br/>                                                                                                                                                                              |



 

## <a name="see-also"></a>Confira também

-   [Windows Programa de Certificação de Hardware](/previous-versions/windows/hardware/hck/jj124227(v=vs.85))
-   [Windows Requisitos de certificação de aplicativos da Store](/legal/windows/agreements/store-policies)

 

