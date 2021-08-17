---
title: Melhores práticas dos requisitos técnicos de jogos para Windows no Windows XP, Windows Vista, Windows 7 e Windows 8
description: Este artigo fornece requisitos técnicos e práticas recomendadas para jogos que são executados em Windows.
ms.assetid: 8b816e9f-de68-cf84-1501-a9c36c6b75d8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 24ce541a1bd8b416bdd22431b59a2ca9490f331b693fe54d45397865d9c23e3f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118649364"
---
# <a name="games-for-windows-technical-requirements-best-practices-for-games-on-windows-xp-windows-vista-windows-7-and-windows-8"></a>jogos para Windows requisitos técnicos: práticas recomendadas para jogos no Windows XP, Windows Vista, Windows 7 e Windows 8

Este artigo fornece requisitos técnicos e práticas recomendadas para jogos que são executados em Windows. nós escrevemos esses requisitos técnicos e as práticas recomendadas principalmente para abranger Windows Vista e Windows 7, bem como o sistema operacional herdado do Windows XP. Essas práticas recomendadas também se aplicam a jogos de desktop Win32 em Windows 8.

Este artigo contém estas seções:

-   [Diferenças para Windows 8](#differences-for-windows-8)
    -   [Informações adicionais](#additional-information)
-   [Jogos para Windows](#games-for-windows-technical-requirements-best-practices-for-games-on-windows-xp-windows-vista-windows-7-and-windows-8)
    -   [Integração do explorador de jogos 1,1](#11-games-explorer-integration)
    -   [1,2 controles de segurança/pais da família de suporte](/windows)
    -   [1,3 suporte a jogos salvos avançados](#13-support-rich-saved-games)
    -   [1,4 suporte ao controlador comum do Xbox 360 para Windows \[ requisito condicional\]](#14-support-the-xbox-360-common-controller-for-windows-conditional-requirement)
    -   [1,5 suporte a várias taxas de proporção e resoluções](#15-support-multiple-aspect-ratios-and-resolutions)
    -   [lançamento do suporte do 1,6 do Windows Media Center](#16-support-launch-from-windows-media-center)
    -   [Suporte do Direct3D 1,7](#17-direct3d-support)
    -   [1,8 habilitar reconhecimento de DPI alto](#18-enable-high-dpi-aware)
-   [Segurança e compatibilidade](#security-and-compatibility)
    -   [2,1 seguir as diretrizes de controle de conta de usuário](#21-follow-user-account-control-guidelines)
    -   [suporte a 2,2 Windows versões x64](#22-support-windows-x64-versions)
    -   [2,3 assinar arquivos](#23-sign-files)
    -   [Drivers de assinatura 2,4](#24-sign-drivers)
    -   [2,5 executar a verificação de versão apropriada](#25-perform-proper-version-checking)
    -   [2,6 suporte a sessões de usuário simultâneas](#26-support-concurrent-user-sessions)
    -   [2,7 nomes longos de suporte](#27-support-long-names)
-   [Instalação](#32-support-user-account-control-for-installation)
    -   [3,1 suporte à instalação fácil](#31-support-easy-installation)
    -   [3,2 controle de conta de usuário de suporte para instalação](#32-support-user-account-control-for-installation)
    -   [3,3 instalar em pastas corretas](#33-install-to-correct-folders)
    -   [3,4 instalar Windows recursos corretamente](#34-install-windows-resources-properly)
    -   [3,5 evitar reinicializações durante a instalação](#35-avoid-reboots-during-installation)
    -   [3,6 usar o controle de versão de arquivo corretamente](#36-use-file-versioning-correctly)
    -   [3,7 suporte a \[ requisito condicional de Autorun\]](#37-support-autorun-conditional-requirement)
-   [Confiabilidade](#reliability)
    -   [4,1 eliminar reinicializações desnecessárias](#41-eliminate-unnecessary-reboots)
    -   [4,2 eliminar falhas de Application Verifier](#42-eliminate-application-verifier-failures)
    -   [4,3 Relatório de Erros do Windows de suporte e informações de versão do arquivo](#43-support-windows-error-reporting-and-file-version-information)
-   [controlador comum do Xbox 360 para terminologia Windows](#xbox-360-common-controller-for-windows-terminology)
-   [Diretrizes para produtos de middleware de jogos](#guidelines-for-game-middleware-products)
    -   [Introdução](#introduction)
    -   [Recomendações adicionais](#additional-recommendations)
    -   [jogos para Windows de casos](#games-for-windows-showcases)
-   [Recursos](#resources)

## <a name="differences-for-windows-8"></a>Diferenças para Windows 8

Aqui está um resumo das principais diferenças ao aplicar esses requisitos técnicos e práticas recomendadas para Windows 8.

<dl> <dt>

<span id="The_Games_Explorer_UI_is_not_visible"></span><span id="the_games_explorer_ui_is_not_visible"></span><span id="THE_GAMES_EXPLORER_UI_IS_NOT_VISIBLE"></span>**A interface do usuário do explorador de jogos não está visível**
</dt> <dd>

todos os jogos que você registra com o [explorador de jogos](/previous-versions/windows/desktop/legacy/hh437965(v=vs.85)) são exibidos como blocos em novas Windows interface do usuário, mas grande parte dos metadados associados ao título não é mais visível. você ainda usa a ferramenta criador de arquivos de definição de jogos (GDFMAKER.EXE), que agora está disponível no SDK (Software Development Kit) do Windows, para criar os metadados. Você também usa os mecanismos existentes para implantar os metadados. Continue testando o registro do explorador de jogos usando o Windows 7 e verifique se o novo bloco da interface do usuário do Windows aparece quando você o instala em Windows 8 (consulte a [integração do explorador de 1,1 jogos](#11-games-explorer-integration)).

para baixar o SDK do Windows 8, consulte [Downloads para desenvolver aplicativos da área de trabalho](https://msdn.microsoft.com/windows/desktop/aa904949).

</dd> <dt>

<span id="Registration_with_the_Game_Explorer_APIs_continues_to_be_the_mechanism_for_registering_your_game_with_Windows_Parental_Controls"></span><span id="registration_with_the_game_explorer_apis_continues_to_be_the_mechanism_for_registering_your_game_with_windows_parental_controls"></span><span id="REGISTRATION_WITH_THE_GAME_EXPLORER_APIS_CONTINUES_TO_BE_THE_MECHANISM_FOR_REGISTERING_YOUR_GAME_WITH_WINDOWS_PARENTAL_CONTROLS"></span>**o registro com as APIs do gerenciador de jogos continua sendo o mecanismo para registrar seu jogo com Windows controles dos pais**
</dt> <dd>

recomendamos que você execute a versão SDK do Windows do GDFMAKER na versão lançada do Windows 8 para garantir que ele possa preencher todos os sistemas de classificação com suporte no momento.

> [!Note]  
> Esta versão do GDFMAKER requer o .NET 4,0.

 

Consulte [segurança/controles dos pais da família de suporte do 1,2](/windows).

</dd> <dt>

<span id="There_are_now_three_choices_for_using_the_XINPUT_API_depending_on_your_requirements"></span><span id="there_are_now_three_choices_for_using_the_xinput_api_depending_on_your_requirements"></span><span id="THERE_ARE_NOW_THREE_CHOICES_FOR_USING_THE_XINPUT_API_DEPENDING_ON_YOUR_REQUIREMENTS"></span>**Agora há três opções para usar a API XINPUT dependendo de seus requisitos**
</dt> <dd>

O XINPUT 1,4 é integrado ao Windows 8. os aplicativos da Windows store e os aplicativos Win32 da área de trabalho podem usar o XINPUT 1,4. todas as versões do Windows podem usar XINPUT 9.1.0 para controladores comuns simplificados, mas não há nenhum pacote de redistribuição com XINPUT 9.1.0. todas as versões do Windows também podem usar o SDK do DirectX existente versão XINPUT 1,3, que requer a implantação do DirectSetup.

Consulte [1,4 suporte ao controlador comum do Xbox 360 para Windows](#14-support-the-xbox-360-common-controller-for-windows-conditional-requirement).

</dd> <dt>

<span id="Only_a_limited_set_of_desktop_Win32_apps_are_supported_on_"></span><span id="only_a_limited_set_of_desktop_win32_apps_are_supported_on_"></span><span id="ONLY_A_LIMITED_SET_OF_DESKTOP_WIN32_APPS_ARE_SUPPORTED_ON_"></span>**Há suporte apenas para um conjunto limitado de aplicativos Win32 da área de trabalho no Windows RT**
</dt> <dd>

os jogos executados no Windows 7 podem e devem ser executados corretamente em plataformas Windows 8 x86 e x64.

consulte [suporte do 2,2 Windows versões x64](#22-support-windows-x64-versions).

</dd> <dt>

<span id="Ensure_any_OS_checks_are_done_correctly"></span><span id="ensure_any_os_checks_are_done_correctly"></span><span id="ENSURE_ANY_OS_CHECKS_ARE_DONE_CORRECTLY"></span>**Certifique-se de que todas as verificações do sistema operacional sejam feitas corretamente**
</dt> <dd>

a versão do sistema operacional Windows 8 é 6,2. Windows 8 passa os testes de barra mínimos atuais que recomendamos para a implantação do jogo.

</dd> <dt>

<span id="The__DirectX_End-User_Redistribution__package_runs_successfully_on_Windows_8__as_it_does_on_Windows_7__to_deploy_D3DX9__D3DX10__D3DX11__XINPUT_1.3__XAUDIO_2.7__XACTEngine__and_so_on"></span><span id="the__directx_end-user_redistribution__package_runs_successfully_on_windows_8__as_it_does_on_windows_7__to_deploy_d3dx9__d3dx10__d3dx11__xinput_1.3__xaudio_2.7__xactengine__and_so_on"></span><span id="THE__DIRECTX_END-USER_REDISTRIBUTION__PACKAGE_RUNS_SUCCESSFULLY_ON_WINDOWS_8__AS_IT_DOES_ON_WINDOWS_7__TO_DEPLOY_D3DX9__D3DX10__D3DX11__XINPUT_1.3__XAUDIO_2.7__XACTENGINE__AND_SO_ON"></span>**o pacote de redistribuição do DirectX End-User é executado com êxito em Windows 8, como faz no Windows 7, para implantar D3DX9, D3DX10, D3DX11, XINPUT 1,3, XAUDIO 2,7, XACTEngine e assim por diante**
</dt> <dd>

Mas existe um problema conhecido com o DirectSetup em sistemas com apenas o .NET 4,0 instalado devido à manipulação de implantação dos assemblies DirectX 1,1 gerenciados herdados. esse problema se aplica a ambos os Windows 8, que vem com o .net 4,5 por padrão, e os computadores com Windows XP atualizados com o tempo de execução do .net 4,0 instalado. Mas esse problema não se aplica a nenhuma versão do .NET anterior ao .NET 4,0. embora Windows 8 tenha um comportamento de compatibilidade de aplicativo para resolver esse problema automaticamente (o que exige acesso à rede), recomendamos que os jogos que continuam a implantar a atualização do DirectSetup na versão atualizada do SDK do DirectX (junho de 2010) dos arquivos redist. Como sempre, se você usar DirectSetup para seu título, corte o título para baixo até o conjunto mínimo necessário de CABs.

consulte [3,4 instalar Windows recursos corretamente](#34-install-windows-resources-properly).

</dd> <dt>

<span id="Games_that_require_the_.NET__2.0__compatible_runtime__2.0__3.0__3.5__continue_to_use_existing_deployment_mechanisms"></span><span id="games_that_require_the_.net__2.0__compatible_runtime__2.0__3.0__3.5__continue_to_use_existing_deployment_mechanisms"></span><span id="GAMES_THAT_REQUIRE_THE_.NET__2.0__COMPATIBLE_RUNTIME__2.0__3.0__3.5__CONTINUE_TO_USE_EXISTING_DEPLOYMENT_MECHANISMS"></span>**Jogos que exigem o tempo de execução compatível com o .NET 2,0 (2,0, 3,0, 3,5) continuam a usar mecanismos de implantação existentes**
</dt> <dd>

esses jogos disparam um comportamento de compatibilidade de aplicativos no Windows 8 para habilitar o tempo de execução do .net 3,5 automaticamente (o que requer acesso à rede). Mas, recomendamos que os desenvolvedores do .NET se movam para o tempo de execução do .NET 4,0.

> [!Note]  
> Os assemblies do DirectX 1,1 gerenciados herdados não são compatíveis com o tempo de execução do .NET 4. x.

 

consulte [3,4 instalar Windows recursos corretamente](#34-install-windows-resources-properly).

</dd> <dt>

<span id="Use_of_an__autorunner__or_other_pre-install_technology_that_relies_on_.NET_is_not_recommended"></span><span id="use_of_an__autorunner__or_other_pre-install_technology_that_relies_on_.net_is_not_recommended"></span><span id="USE_OF_AN__AUTORUNNER__OR_OTHER_PRE-INSTALL_TECHNOLOGY_THAT_RELIES_ON_.NET_IS_NOT_RECOMMENDED"></span>**O uso de um autorunner ou de outra tecnologia de pré-instalação que se baseia no .NET não é recomendado**
</dt> <dd>

você pode assumir que somente os tempos de execução compatíveis com .net 2,0 (2,0, 3,0, 3,5) estão presentes no Windows Vista e Windows 7. somente o tempo de execução compatível com o .net 4,0 está presente no Windows 8 por padrão.

Consulte [suporte para autorun do 3,7](#37-support-autorun-conditional-requirement).

</dd> <dt>

<span id="There_is_an_updated_Application_Verifier_for_Windows_8"></span><span id="there_is_an_updated_application_verifier_for_windows_8"></span><span id="THERE_IS_AN_UPDATED_APPLICATION_VERIFIER_FOR_WINDOWS_8"></span>**Há uma Application Verifier atualizada para Windows 8**
</dt> <dd>

o SDK do Windows 8 inclui esse Application Verifier atualizado.

Consulte [4,2 eliminar falhas de Application Verifier](#42-eliminate-application-verifier-failures).

</dd> </dl>

### <a name="additional-information"></a>Informações adicionais

<dl>

[guia de compatibilidade de Windows 8 e Windows Server 2012](/windows/desktop/w8cookbook/windows-8-and-windows-server-8-compatibility-cookbook-portal)  
[Onde está o SDK do DirectX?](/windows/desktop/directx-sdk--august-2009-)  
</dl>

## <a name="games-for-windows"></a>Jogos para Windows

**Resumo dos requisitos de jogos**

**Benefícios do cliente**

jogos de computador são uma experiência de entretenimento importante em Windows, mas preocupações com a facilidade de uso causaram a frustração do cliente ao longo dos anos. Tradicionalmente, os jogos são instalados como aplicativos, mas são utilizados mais como mídia de entretenimento (filmes ou músicas, por exemplo). Inovações, como o explorador de jogos, expõem jogos de maneira consistente que é diferente dos aplicativos padrão. essas inovações também dão aos jogos o status do cidadão de primeira classe no Windows, junto com música e imagens. os requisitos a seguir ajudam a garantir que o Windows Vista e o Windows 7 forneçam uma experiência de jogos aprimorada, mais acessível e unificada. ao mesmo tempo, eles garantem a compatibilidade com o Windows XP.

### <a name="11-games-explorer-integration"></a>Integração do explorador de jogos 1,1

<dl> <dt>

<span id="Requirement"></span><span id="requirement"></span><span id="REQUIREMENT"></span>**Obrigatoriedade**
</dt> <dd>

o jogo deve estar visível no explorador de jogos (a pasta **jogos** ) no Windows Vista e Windows 7. quando selecionado, o jogo também deve exibir metadados corretos, o que inclui publicador, desenvolvedor, data de lançamento, versão, Windows pontuações de índice de experiência, classificação (se aplicável) e hiperlinks associados.

Se o jogo for distribuído digitalmente por meio de um serviço de jogo online, o provedor de serviços também deverá aparecer no explorador de jogos. Para garantir o tratamento adequado do provedor e habilitar o uso de RSS feeds, a versão 2 do esquema para GDFs (arquivos de definição de jogo) deve ser usada. (Para obter mais informações sobre GDFs, consulte informações adicionais.)

além disso, os instaladores de jogos devem observar as seguintes regras quando são executados no Windows Vista e Windows 7:

-   a instalação não deve criar um atalho para iniciar o jogo na área de trabalho, na menu Iniciar ou em qualquer outro local.
-   Tarefas e atalhos para remoção não devem ser criados.
-   os usuários devem ser capazes de remover o jogo usando programas e recursos no painel de controle no Windows Vista e no Windows 7, ou adicionar ou remover programas no painel de controle no Windows XP.

no Windows XP e nas versões anteriores do Windows, o instalador do jogo é gratuito para criar grupos de programas, ícones da área de trabalho ou atalhos, conforme necessário.

</dd> <dt>

<span id="Rationale"></span><span id="rationale"></span><span id="RATIONALE"></span>**Lógica**
</dt> <dd>

Windows o explorador de jogos é semelhante em conceito às pastas Windows XP **meus documentos** ou **minhas imagens**. A ideia é centralizar o conteúdo semelhante em um único local e permitir atividades mais fáceis e sensíveis ao contexto. O explorador de jogos estende o conceito **meus documentos** ou **minhas imagens** , permitindo uma organização mais rica e controle sobre jogos. O explorador de jogos permite que os jogadores exibam, organizem e interajam com todos os jogos instalados em seus sistemas. Ele também permite que os editores de jogos comuniquem informações importantes do jogo com mais eficiência. O sistema é controlado por dados, facilitando para um editor de jogos atualizar as informações do jogo durante a vida útil do produto.

</dd> <dt>

<span id="Additional_Information"></span><span id="additional_information"></span><span id="ADDITIONAL_INFORMATION"></span>**Informações adicionais**
</dt> <dd>

a integração com o explorador de jogos exige que você crie um arquivo de definição de jogo (GDF), que é um arquivo de texto XML que é inserido em um arquivo binário (um arquivo executável ou uma DLL) como um recurso, juntamente com um ícone de Windows. O jogo deve então ser registrado com o explorador de jogos. O GDF também permite a exposição de informações fornecidas, como o título do jogo, o editor, o desenvolvedor, links para sites e tarefas opcionais. Observe que as tarefas de suporte podem ser apenas links para sites da Web, mas as tarefas de reprodução também podem ser usadas para tarefas opcionais de suporte.

o explorador de jogos pode fazer uso de uma imagem de bitmap em miniatura, mas é recomendável que, em vez disso, você forneça um recurso de ícone de Windows com ícones grandes (256 256). O recurso de ícone deve incluir tamanhos de imagem de 256 256 48 48, 32 32 e 16 16 nas profundidades de cores de 24 bits (true color) e de 8 bits (256). o editor de ícone fornecido no Visual Studio 2008 e 2010 dá suporte a esses formatos de ícones grandes, assim como o IconWorkshop Lite.

detalhes sobre a integração com o **Windows Games Explorer** são fornecidos no SDK do DirectX. O SDK do DirectX inclui um editor de GDF (arquivo de definição de jogo), bem como um GDF de exemplo que é incluído no GDFExampleBinary, um exemplo. Outro exemplo, GameUxInstallHelper, fornece rotinas para integrar a funcionalidade necessária aos sistemas de instalação existentes. O validador de arquivo de definição de jogo (gdftrace.exe) fornece suporte de depuração para avaliar um GDF. consulte também "integração do gerenciador de jogos de Windows" na documentação do SDK do DirectX para C++.

o Windows 7 apresenta suporte para a segunda versão de um esquema para arquivos GDF. A nova versão inclui um método simplificado para criar tarefas de reprodução e suporte para notificações de atualização, provedores de serviço de jogos, estatísticas de jogos e RSS feeds para provedores de serviço de jogos. a versão mais recente do GameUxInstallHelper manipula todo o registro e o suporte herdado necessários para usar um arquivo GDF da versão 2 com o Windows Vista. Use as ferramentas e o código de exemplo do SDK do DirectX de agosto de 2009 ou posterior. É recomendável usar um arquivo GDF de versão 2 para habilitar o suporte para RSS feeds, estatísticas de jogos e notificações de atualização. Além disso, consulte os exemplos ProviderGDFExampleBinary e GameStatisticsExample.

no Windows vista Business edition, Windows 7 Professional edition e Edição Enterprise do Windows vista e do Windows 7, o link jogos na menu Iniciar está oculto. o explorador de jogos ainda está disponível no menu Iniciar clicando em **todos os programas** e, em seguida, clicando em **jogos**.

para aplicativos associados que são instalados com seu jogo, mas não em jogos, você tem a liberdade de criar menu Iniciar grupos de programas, atalhos e ícones de área de trabalho em todas as versões do Windows, incluindo Windows Vista e Windows 7. esses aplicativos associados devem passar em jogos aplicáveis para requisitos de Windows; para obter detalhes, consulte [diretrizes para produtos de middleware de jogos](#guidelines-for-game-middleware-products). os serviços de jogos são incentivados a se registrarem no explorador de jogos como um provedor de jogos para o Windows 7. 1

</dd> </dl>

### <a name="12-support-family-safety--parental-controls"></a>1,2 controles de segurança/pais da família de suporte

<dl> <dt>

<span id="Requirement"></span><span id="requirement"></span><span id="REQUIREMENT"></span>**Obrigatoriedade**
</dt> <dd>

os jogos devem dar suporte total à segurança da família Windows de acordo com as seguintes regras:

-   Os jogos não devem exigir que o usuário tenha credenciais administrativas para reproduzir. A instalação, a aplicação de patches e a remoção podem exigir credenciais administrativas, sujeitas aos requisitos da seção 3. (Relacionado a isso é requisito 2,1, siga as diretrizes de controle de conta de usuário.)
-   os jogos classificados por Windows placas de classificação com suporte, como ESRB e PEGI, devem incluir suas informações de classificações atribuídas em seu GDF (arquivo de definição de jogo). Todos os dados de classificação disponíveis devem ser incluídos em todas as versões localizadas do GDF, bem como na versão neutra da linguagem.
-   Os jogos devem listar seus executáveis no GDF para fornecer uma boa experiência de usuário para restrições gerais de aplicativos, a menos que o jogo use uma tecnologia antipirataria que cria executáveis aleatoriamente nomeados em tempo de execução.
-   Os jogos devem chamar o método **VerifyAccess** da interface do explorador de jogos durante a inicialização, se disponível, e sair se retornar \* pfHasAccess como falso.

</dd> <dt>

<span id="Rationale"></span><span id="rationale"></span><span id="RATIONALE"></span>**Lógica**
</dt> <dd>

todos os jogos devem ser executados dentro do contexto de uma conta de usuário padrão para permitir contas controladas por Windows controles dos pais para executar o jogo. Os pais desejam a capacidade de monitorar e controlar o acesso de seus filhos aos jogos. Além disso, vários grupos do setor, do governo e do advocacy desejam maneiras melhores de permitir que os pais monitorem e controlem os jogos nos quais seus filhos são expostos. em conjunto com a arquitetura oferecida pelo explorador de jogos, a Microsoft fornece aos pais essa capacidade por meio de Windows controles dos pais.

Mesmo para jogos que não participam de um programa de tabuleiro de classificação, exigir privilégios elevados cria uma experiência de reprodução ruim para a maioria das contas de usuário. Isso é particularmente o caso se os controles dos pais estiverem habilitados, o que exigiria que o pai entrasse na senha de administrador sempre que o jogo for iniciado.

o sistema de controles dos pais Windows permite que os pais selecionem as classificações que eles acreditam que são apropriadas para seus filhos. Os controles dos pais dão suporte a muitos dos sistemas de classificação mundiais. Os controles dos pais também permitem que os pais restrinjam o acesso a jogos com base em descritores de conteúdo (se o sistema de classificação aplicável oferecer suporte a eles) e para permitir ou impedir o acesso a jogos individuais.

a opção padrão de sistema de classificação para Windows controles dos pais é baseada na configuração de localidade do sistema, mas pode ser modificada pelo usuário em **opções regionais e de idioma** no **painel de controle**. Portanto, cada idioma com suporte deve fornecer todos os dados de classificação disponíveis para que o usuário tenha a liberdade de selecionar qualquer quadro de classificação desejado.

</dd> <dt>

<span id="Additional_Information"></span><span id="additional_information"></span><span id="ADDITIONAL_INFORMATION"></span>**Informações adicionais**
</dt> <dd>

Os jogos sem uma classificação ainda devem atender aos requisitos para dar suporte à reprodução como usuário padrão e chamar **VerifyAccess**. Esses jogos assumem como padrão a categoria não classificada, exibem o texto "nenhuma classificação fornecida" no explorador de jogos e estão sujeitos à configuração de **restrições do jogo** nos **controles dos pais** para jogos sem classificação. A configuração de **restrições** padrão é permitir.

As informações de classificação no GDF serão ignoradas se o binário que o contém não for corretamente assinado por Authenticode. Consulte o requisito 2,3.

O editor de arquivo de definição de jogo no SDK do DirectX inclui todos os sistemas de classificação com suporte e replicará corretamente essas informações para todas as versões localizadas do GDF, bem como uma versão neutra de idioma. A ferramenta GDFTrace decodificará e verificará todas as informações de classificação presentes. Use a versão de agosto de 2009 ou posterior dessas ferramentas.

O GDF para um provedor de jogos normalmente não contém informações de classificação e está sujeito às configurações de conteúdo sem classificação.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Sistema operacional</th>
<th>Sistemas de classificação com suporte</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Windows Vista</td>
<td><ul>
<li>CERO (Japão)</li>
<li>ESRB (EUA)</li>
<li>OFLC (Austrália)</li>
<li>PEGI (Europa)</li>
<li>PEGI Finlândia (preterido)</li>
<li>PEGI Portugal</li>
<li>PEGI/BBFC (Reino Unido)</li>
<li>USK (Alemanha)</li>
</ul></td>
</tr>
<tr class="even">
<td>Windows Vista com um service pack</td>
<td>os Service packs do Windows Vista adicionam suporte para o seguinte:<br/>
<ul>
<li>GRB (Coreia do Sul)</li>
<li>&quot;Descritores de conteúdo de variante leve do ESRB &quot;</li>
</ul></td>
</tr>
<tr class="odd">
<td>Windows 7</td>
<td>o Windows 7 dá suporte aos sistemas de classificação com suporte do Windows Vista e adiciona suporte para o seguinte: <br/>
<ul>
<li>CSRR (Taiwan)</li>
</ul></td>
</tr>
<tr class="even">
<td>Windows 8</td>
<td>o Windows 8 dá suporte aos sistemas de classificação anteriores e adiciona ao seguinte:<br/>
<ul>
<li>COB-AU (Austrália)</li>
<li>DJCTQ (Brasil)</li>
<li>PFB (África do Sul)</li>
<li>OFLC-NZ (Nova Zelândia)</li>
</ul>
Windows 8 o rearo dá suporte para os seguintes sistemas preteridos agora:<br/>
<ul>
<li>FINI-FI (Finlândia)</li>
<li>OFLC (Austrália)</li>
</ul></td>
</tr>
</tbody>
</table>



 

> [!Note]  
> Qualquer título que inclua novos descritores de conteúdo do ESRB Windows Vista Service Pack 1 (SP1) será show as Unrated on Windows Vista without a service pack.

 

Os dados de classificações mais recentes são ignorados em versões de sistemas operacionais sem suporte para eles. Agora, a variante DOEI (Finlândia) foi preterida em favor do sistema de classificação PADRÃO DAL (Europa). O sistema OFLC agora foi preterido em favor do COB-AU para a Austrália.

Para obter mais informações sobre como tornar um jogo compatível com privilégios de usuário padrão, consulte o artigo Controle de conta de usuário do DirectX [para desenvolvedores de jogos](/windows/desktop/DxTechArts/user-account-control-for-game-developers).

Consulte o requisito 1.1 para obter mais detalhes sobre o GDF (arquivo de definição de jogo).

</dd> </dl>

### <a name="13-support-rich-saved-games"></a>1.3 Suporte a jogos salvos com rich

\[Esse requisito foi retirado\]

### <a name="14-support-the-xbox-360-common-controller-for-windows-conditional-requirement"></a>1.4 Dar suporte ao Xbox 360 Common Controller para Windows \[ requisito condicional\]

<dl> <dt>

<span id="Requirement"></span><span id="requirement"></span><span id="REQUIREMENT"></span>**Exigência**
</dt> <dd>

Os jogos que suportam controladores de gamepad devem dar suporte ao Controle Xbox 360 para Windows usando a API [XInput.](/windows/desktop/xinput/xinput-game-controller-apis-portal) Se também há suporte para periféricos directInput, o DirectInput também pode ser usado. No entanto, o XInput deverá ser a API padrão se um Xbox 360 compatível for usado.

Todas as referências a gatilhos e botões de controlador comuns devem usar os nomes Xbox 360 dados. Consulte a [Xbox 360 Common Controller para obter Windows terminologia](#xbox-360-common-controller-for-windows-terminology) para obter detalhes.

A vibração do controlador deve ser desligada quando o jogo está em um estado em pausa ou suspenso.

O controle de mouse/teclado não pode ser totalmente desabilitado a qualquer momento. No mínimo, uma opção para retornar aos menus do jogo deve estar disponível.

</dd> <dt>

<span id="Rationale"></span><span id="rationale"></span><span id="RATIONALE"></span>**Lógica**
</dt> <dd>

Esse requisito dá aos jogadores a liberdade de escolha de usar o controlador Xbox 360 ou o teclado e o mouse, dependendo de qual método de entrada é uma interface mais natural e intuitiva.

</dd> <dt>

<span id="Additional_Information"></span><span id="additional_information"></span><span id="ADDITIONAL_INFORMATION"></span>**Informações adicionais**
</dt> <dd>

Esse requisito não se aplica a jogos que usam apenas o mouse e/ou o teclado.

Recomendamos que a navegação de menu seja implementada para usar os botões de controlador padrão amplamente aceitos:

-   A - Aceitar
-   B – Cancelar
-   Iniciar – Aceitar ou pausar
-   Voltar – Cancelar, voltar uma tela ou um nível de menu acima

Para obter mais informações, consulte [XInput](/windows/desktop/xinput/xinput-game-controller-apis-portal).

O tópico [XInput e DirectInput](/windows/desktop/xinput/xinput-and-directinput) aborda problemas com o uso de ambas as APIs ao mesmo tempo.

É recomendável que o DirectInput não seja usado para implementar controles de teclado ou mouse. Os controles de teclado e mouse só devem ser implementados usando Windows e APIs do Win32. Para obter detalhes sobre como obter informações de movimentação do mouse de alta resolução sem usar o DirectInput, consulte Aproveitando a High-Definition [do mouse.](/windows/desktop/DxTechArts/taking-advantage-of-high-dpi-mouse-movement)

</dd> </dl>

### <a name="15-support-multiple-aspect-ratios-and-resolutions"></a>1.5 Dar suporte a várias taxas de proporção e resoluções

<dl> <dt>

<span id="Requirement"></span><span id="requirement"></span><span id="REQUIREMENT"></span>**Exigência**
</dt> <dd>

O jogo deve dar suporte a pelo menos as seguintes taxas de proporção e resoluções de tela associadas:

-   4:3 normal (800 600 ou 1024 768)
-   16:9 widescreen (1280 720)
-   16:10 widescreen (1152 720 ou 1680 1050 ou 800 480)

Para configuração e detecção de resolução de tela, o jogo deve seguir as seguintes regras:

-   O jogo usa a resolução da área de trabalho do dispositivo de exibição por padrão se for uma resolução com suporte. A taxa de proporção da área de trabalho deve ser usada como um critério de pesquisa se o jogo escolher uma resolução padrão diferente.
-   O jogo deve solicitar que o usuário confirme novas configurações de exibição quando uma alteração for feita. Se o usuário não aceitar dentro de 15 segundos, a exibição deverá ser revertida para a configuração anterior.
-   O jogo não deve alongar pixels nem centralizar uma janela de renderização 4:3 para dar suporte a taxas de proporção de widescreen. No entanto, o letterboxing é aceitável.

</dd> <dt>

<span id="Rationale"></span><span id="rationale"></span><span id="RATIONALE"></span>**Lógica**
</dt> <dd>

Com o Windows desktop 3D, uma taxa de proporção ou resolução específica não pode ser assumida, devido aos seguintes fatores:

-   Suporte para exibições de alto detalhe.
-   Maior participação no mercado de monitores de tela larga.
-   Implantações de HDTV para Windows Media Center.
-   Requisitos de acessibilidade.

</dd> <dt>

<span id="Additional_Information"></span><span id="additional_information"></span><span id="ADDITIONAL_INFORMATION"></span>**Informações adicionais**
</dt> <dd>

O ideal é que o jogo padrão seja a taxa de proporção nativa da exibição. No entanto, obter essas informações de forma confiável pode ser um desafio, portanto, como uma solução mais geral, o jogo pode assumir que a área de trabalho está em execução na taxa de proporção nativa. A resolução da área de trabalho pode ser obtida chamando [**EnumDisplaySettings com**](/windows/desktop/api/winuser/nf-winuser-enumdisplaysettingsa) CONFIGURAÇÕES DE REGISTRO \_ \_ ENUM.

Para obter mais detalhes, consulte as seções Taxa de Proporção e Widescreen do artigo Do DirectX Introdução à experiência de 10 pés para [desenvolvedores Windows jogos.](/windows/desktop/DxTechArts/introduction-to-the-10-foot-experience-for-windows-game-developers)

</dd> </dl>

### <a name="16-support-launch-from-windows-media-center"></a>1.6 Lançamento de suporte do Windows Media Center

\[Esse requisito foi retirado.\]

### <a name="17-direct3d-support"></a>1.7 Suporte direct3D

<dl> <dt>

<span id="Requirement"></span><span id="requirement"></span><span id="REQUIREMENT"></span>**Exigência**
</dt> <dd>

Se o jogo usar Direct3D, a versão mínima com suporte deverá ser Direct3D 9 e Direct3D deverá ser o renderador padrão selecionado.

</dd> <dt>

<span id="Rationale"></span><span id="rationale"></span><span id="RATIONALE"></span>**Lógica**
</dt> <dd>

A Windows vista e a Windows elementos gráficos principais 7 são projetadas em torno do Direct3D. O Direct3D 8 e versões anteriores têm suporte remapeando interfaces herdadas.

É fortemente incentivado o uso de versões do Direct3D mais recentes do que o Direct3D 9. Consulte Os Jogos para Windows Demonstração S.1. Exigir Direct3D 10 ou Direct3D 11 é totalmente compatível com o requisito 1.7.

</dd> </dl>

### <a name="18-enable-high-dpi-aware"></a>1.8 Habilitar alto nível de DPI

<dl> <dt>

<span id="Requirement"></span><span id="requirement"></span><span id="REQUIREMENT"></span>**Exigência**
</dt> <dd>

Os jogos e seus instaladores devem ser executados corretamente sem problemas visuais quando o dimensionamento DPI (pontos por polegada) está habilitado (testado com 144 DPI para 150% de dimensionamento na resolução de exibição de 1600 1200) no Windows Vista e Windows 7.

Normalmente, isso requer que o executável do jogo declare estar ciente de DPI. Isso é feito pela incorporação de um elemento de manifesto: <dpiAware> <dpiAware> true.

</dd> <dt>

<span id="Rationale"></span><span id="rationale"></span><span id="RATIONALE"></span>**Lógica**
</dt> <dd>

Monitores DE MONITORES de alta qualidade são comuns à medida que o computador é exibido e têm uma melhor aparência quando orientados em suas resoluções nativas (normalmente 1280 1024, 1600 1200 e assim por diante). Os clientes que têm dificuldade para ler texto e ver imagens nessa resolução geralmente configuram suas áreas de trabalho de computador para uma resolução mais baixa e sofrem artefatos visuais do dimensionamento do LCD. Em vez disso, os clientes podem deixar a resolução no tamanho nativo e alterar o DPI da exibição Windows, tornando a aparência de item e texto maior sem sacrificar a qualidade da imagem.

Embora esse recurso tenha sido disponibilizado em alguma forma desde o Windows XP, ele raramente é habilitado por clientes ou por OEMs. Mais da metade de todas as exibições de computador hoje são definidas como uma resolução menor do que a resolução nativa do monitor, com base nos comentários dos clientes. Windows 7 torna esse recurso muito mais visível para os clientes durante a configuração inicial e ao alterar as configurações de exibição, incentivando-os a usar o dimensionamento de DPI em vez de alterar a resolução da área de trabalho.

</dd> <dt>

<span id="Additional_Information"></span><span id="additional_information"></span><span id="ADDITIONAL_INFORMATION"></span>**Informações adicionais**
</dt> <dd>

A [**função SetProcessDPIAware**](/windows/desktop/api/winuser/nf-winuser-setprocessdpiaware) pode ser usada, se chamada no início do código de inicialização do processo. É preferível adicionar ao manifesto, para garantir que não haja condições de corrida com elementos de software (como DLLs) que possam ser inicializados antes que o ponto de entrada principal seja chamado. Observe que **SetProcessDPIAware** está presente apenas no Windows Vista e Windows 7.

Adicionar o elemento de manifesto é fácil de fazer com Visual Studio 2005 e 2008; crie um arquivo chamado dpiaware.manifest que contém o seguinte texto:

``` syntax
            <assembly xmlns="urn:schemas-microsoft-com:asm.v1" manifestVersion="1.0" xmlns:asmv3="urn:schemas-microsoft-com:asm.v3">
            <asmv3:application>
            <asmv3:windowsSettings xmlns="http://schemas.microsoft.com/SMI/2005/WindowsSettings">
            <dpiAware>true</dpiAware>
            </asmv3:windowsSettings>
            </asmv3:application>
            </assembly>
```

Em seguida, Visual Studio, adicione dpiware.manifest ao projeto. Verifique se **Inserir Manifesto** está definido como **Sim** nas propriedades do projeto. Observe que versões mais antigas da Ferramenta de Manifesto (Mt.exe) gerarão um aviso ilídio com os elementos de manifesto com conhecimento de DPI. Para resolver isso, atualize Mt.exe para a versão mais recente do SDK do Windows.

Visual Studio 2010 inclui uma configuração nas propriedades do projeto, chamada Habilitar Reconhecimento **de DPI,** que elimina a necessidade de um arquivo como dpiaware.manifest. Encontre **Habilitar Reconhecimento de DPI** expandindo Propriedades de **Configuração** e **Ferramenta** de Manifesto e, em seguida, selecionando **Entrada & Saída**.

No Windows, o modo de exibição tradicional assume como padrão 96 DPI, o que era comum para monitores CRT.

Embora os aplicativos de tela inteira alterem a resolução de exibição, eles geralmente usam mensagens de janela e métricas ao configurar buffers e exibir retângulos. A virtualização de DPI faz com que esses modos de exibição de tela inteira apareçam cortados e a declaração com conhecimento de DPI impedirá esses problemas. Para obter mais informações, consulte [Escrevendo DPI-Aware aplicativos Win32](../hidpi/high-dpi-desktop-application-development-on-windows.md).

</dd> </dl>

## <a name="security-and-compatibility"></a>Segurança e compatibilidade

**Resumo dos requisitos de segurança e compatibilidade**

**Benefícios do cliente**

Os requisitos a seguir melhoram a segurança geral dos jogos e ajudam a garantir que eles trabalhem com Windows diferentes arquiteturas, em configurações diferentes e em modos diferentes.

### <a name="21-follow-user-account-control-guidelines"></a>2.1 Seguir as diretrizes de controle de conta de usuário

<dl> <dt>

<span id="Requirement"></span><span id="requirement"></span><span id="REQUIREMENT"></span>**Exigência**
</dt> <dd>

Cada arquivo executável (ou seja, cada arquivo que tem uma extensão .exe) deve conter um manifesto inserido que define seu nível de execução incluindo a seguinte marca:

``` syntax
            <requestedExecutionLevel>
```

De acordo com o requisito 1.2, o jogo principal e o executável de execução automática devem ter o nível de execução do asInvoker para dar suporte a contextos de Usuário Padrão.

Os arquivos de dados do usuário que têm associações de arquivos registradas com **Explorador de Arquivos** devem ser colocados em uma subpasta da pasta especificada pelo CSIDL PERSONAL (também chamado de Documentos \_ ou **Meus Documentos**).  Todos os outros arquivos de dados de usuário devem ser armazenados em uma subpasta das pastas especificadas por CSIDL \_ LOCAL \_ APPDATA ou CSIDL \_ COMMON \_ APPDATA. (Esses diretórios são ocultos por padrão para usuários individuais e para todos os usuários.)

</dd> <dt>

<span id="Rationale"></span><span id="rationale"></span><span id="RATIONALE"></span>**Lógica**
</dt> <dd>

A experiência de Windows usuário é mais segura se os aplicativos são executados somente com as permissões necessárias.

</dd> <dt>

<span id="Additional_Information"></span><span id="additional_information"></span><span id="ADDITIONAL_INFORMATION"></span>**Informações adicionais**
</dt> <dd>

Se apenas alguns recursos em um aplicativo exigirem privilégios administrativos (por exemplo, um aplicativo que precisa configurar um firewall), o processo principal do aplicativo ainda deverá ser executado usando privilégios de usuário padrão. Os recursos que exigem privilégios administrativos devem ser movidos para um processo separado, como um instalador ou utilitário de configuração.

Se os privilégios administrativos não são necessários, o XML do manifesto inserido deve incluir o seguinte:

``` syntax
            <?xml version="1.0" encoding="UTF-8" standalone="yes"?>
            <assembly xmlns="urn:schemas-microsoft-com:asm.v1" manifestVersion="1.0">
            <ms_asmv2:trustInfo xmlns:ms_asmv2="urn:schemas-microsoft-com:asm.v2">
            <ms_asmv2:security>
            <ms_asmv2:requestedPrivileges>
            <ms_asmv2:requestedExecutionLevel level="asInvoker" uiAccess="false" />
            </ms_asmv2:requestedPrivileges>
            </ms_asmv2:security>
            </ms_asmv2:trustInfo>
            </assembly>
```

Se os privilégios administrativos são necessários, o XML do manifesto inserido deve incluir o seguinte:

``` syntax
            <?xml version="1.0" encoding="UTF-8" standalone="yes"?>
            <assembly xmlns="urn:schemas-microsoft-com:asm.v1" manifestVersion="1.0">
            <ms_asmv2:trustInfo xmlns:ms_asmv2="urn:schemas-microsoft-com:asm.v2">
            <ms_asmv2:security>
            <ms_asmv2:requestedPrivileges>
            <ms_asmv2:requestedExecutionLevel level="requireAdministrator" uiAccess="false" />
            </ms_asmv2:requestedPrivileges>
            </ms_asmv2:security>
            </ms_asmv2:trustInfo>
            </assembly>
```

Com o Visual Studio 2005, isso é facilmente inserido apenas adicionando um arquivo de manifesto (.manifest) que contém um dos blocos anteriores ao projeto e garantindo que **Inserir** Manifesto seja definido como **Sim** nas propriedades do projeto para a Ferramenta de Manifesto. Por Visual Studio 2008 e 2010, as propriedades UAC podem ser definidas diretamente nas propriedades do projeto para o vinculador na página Arquivo **de** Manifesto. Observe que as versões mais antigas da Ferramenta de Manifesto (Mt.exe) geram um aviso imputioso com os elementos de manifesto UAC. Para resolver isso, atualize Mt.exe para a versão mais recente do SDK do Windows.

Consulte o requisito 3.1 para obter detalhes sobre os casos especiais de instalação, a patch e a remoção.

DLLs (Bibliotecas de Vínculo Dinâmico) não exigem esses manifestos.

Para obter mais informações sobre o Controle de Conta de Usuário, consulte [Controle de conta de usuário para desenvolvedores de jogos](/windows/desktop/DxTechArts/user-account-control-for-game-developers).

</dd> </dl>

### <a name="22-support-windows-x64-versions"></a>2.2 Suporte a Windows versões x64

<dl> <dt>

<span id="Requirement"></span><span id="requirement"></span><span id="REQUIREMENT"></span>**Exigência**
</dt> <dd>

Para manter a compatibilidade com as edições de 64 bits Windows, os jogos devem atender aos requisitos a seguir.

-   Os títulos e instaladores de título não devem conter nenhum código de 16 bits nem depender de nenhum componente de 16 bits.
-   Se o jogo for dependente de drivers de modo kernel para operação, as versões x64 desses drivers deverão estar disponíveis. A configuração do jogo deve detectar e instalar os drivers e componentes adequados para as edições de 64 bits Windows.

</dd> <dt>

<span id="Rationale"></span><span id="rationale"></span><span id="RATIONALE"></span>**Lógica**
</dt> <dd>

Muitos usuários Windows Vista e Windows 7 executarão edições de 64 bits do sistema operacional ao longo da vida útil do produto, portanto, é crucial que os aplicativos sejam compatíveis com esse sistema operacional.

</dd> <dt>

<span id="Additional_Information"></span><span id="additional_information"></span><span id="ADDITIONAL_INFORMATION"></span>**Informações adicionais**
</dt> <dd>

Windows no Windows 64 (WOW64) permite que o código de 32 bits seja executado em edições de 64 bits do Windows, portanto, não é necessário que o aplicativo seja um código nativo de 64 bits em edições de 64 bits do Windows. O código de 16 bits não é executado em edições de 64 bits do Windows.

Manter a compatibilidade com Windows XP Professional x64 Edition não é necessário, mas é fortemente incentivado.

Para obter detalhes, consulte [Programação de 64 bits para desenvolvedores de jogos.](/windows/desktop/DxTechArts/sixty-four-bit-programming-for-game-developers)

</dd> </dl>

### <a name="23-sign-files"></a>2.3 Assinar arquivos

<dl> <dt>

<span id="Requirement"></span><span id="requirement"></span><span id="REQUIREMENT"></span>**Exigência**
</dt> <dd>

Todos os arquivos de código executáveis (normalmente, arquivos com a extensão .exe ou .dll) devem ser assinados com um certificado Authenticode válido publicamente e devem ter uma URL de servidor de data/hora válida para assinatura de produção.

Se o seu jogo usar Windows Instalador, os arquivos de pacote do instalador (arquivos .msi) deverão ser assinados.

</dd> <dt>

<span id="Rationale"></span><span id="rationale"></span><span id="RATIONALE"></span>**Lógica**
</dt> <dd>

A assinatura de um arquivo ajuda os usuários a decidir se confiam em um aplicativo e garante que os arquivos não foram adulterados. Ele também permite que os aplicativos executem corretamente em ambientes bloqueados.

</dd> <dt>

<span id="Additional_Information"></span><span id="additional_information"></span><span id="ADDITIONAL_INFORMATION"></span>**Informações adicionais**
</dt> <dd>

Para obter detalhes, consulte [Autenticação authenticode para desenvolvedores de jogos.](/windows/desktop/DxTechArts/authenticode-signing-for-game-developers)

Se seu jogo usar Windows Instalador, recomendamos que você habilita a adoção de patch UAC/LUA, incluindo uma tabela MsiPatchCertificate. Para obter mais informações, consulte [UAC (Controle de Conta de Usuário).](/windows/desktop/Msi/user-account-control--uac--patching)

Não recomendamos assinar arquivos de gabinete (.cab), a menos que sejam relativamente pequenos (menos de 100 MB).

</dd> </dl>

### <a name="24-sign-drivers"></a>2.4 Assinar Drivers

<dl> <dt>

<span id="Requirement"></span><span id="requirement"></span><span id="REQUIREMENT"></span>**Exigência**
</dt> <dd>

Qualquer driver de modo kernel instalado pelo jogo deve ser assinado com um certificado Authenticode válido publicamente.

Qualquer driver de dispositivo de hardware no modo kernel instalado pelo jogo deve ter uma assinatura da Microsoft, que pode ser obtida do WHQL (Hardware Quality Labs) do Windows ou do programa DRS (Assinatura de Confiabilidade do Driver).

</dd> <dt>

<span id="Rationale"></span><span id="rationale"></span><span id="RATIONALE"></span>**Lógica**
</dt> <dd>

Drivers mal escritos ou malware podem afetar gravemente a estabilidade e a segurança de um sistema. Em edições de 64 bits do Windows Vista e Windows 7, os drivers não assinados não são carregados. Essa política também pode ser habilitada para edições de 32 bits do Windows Vista e Windows 7.

</dd> <dt>

<span id="Additional_Information"></span><span id="additional_information"></span><span id="ADDITIONAL_INFORMATION"></span>**Informações adicionais**
</dt> <dd>

As versões nativas de 32 e 64 bits de todos os drivers de modo kernel são necessárias de acordo com o requisito 2.2.

Mais informações sobre programas de assinatura de driver da Microsoft podem ser encontradas [no portal Windows Desenvolvedor de Hardware](https://www.microsoft.com/whdc/winlogo/hwrequirements.mspx).

</dd> </dl>

### <a name="25-perform-proper-version-checking"></a>2.5 Executar verificação de versão adequada

<dl> <dt>

<span id="Requirement"></span><span id="requirement"></span><span id="REQUIREMENT"></span>**Exigência**
</dt> <dd>

Os jogos não devem falhar ao ser executados em sistemas operacionais futuros, conforme indicado pelas alterações no número de versão Windows, a menos que o Contrato de Licença do Usuário Final proíbe o uso em sistemas operacionais futuros. Se o jogo tiver que falhar, ele deverá fazer isso normalmente exibindo uma mensagem apropriada para o usuário.

Se Windows de versão for feita, as APIs de verificação de versão ([**GetVersionEx**](/windows/desktop/api/sysinfoapi/nf-sysinfoapi-getversionexa) ou [**VerifyVersionInfo**](/windows/desktop/api/winbase/nf-winbase-verifyversioninfoa)) deverão ser usadas para verificar a versão do sistema operacional. As chaves do Registro não devem ser lidas para determinar a versão.

Verificações explícitas de versão para o runtime do DirectX não devem estar presentes no jogo. Essas verificações de versão não devem estar presentes na instalação que inicia a instalação do runtime do DirectX (DirectSetup).

</dd> <dt>

<span id="Rationale"></span><span id="rationale"></span><span id="RATIONALE"></span>**Lógica**
</dt> <dd>

Quando Windows os usuários atualizem seus sistemas operacionais, eles não devem ser impedidos de jogar jogos atuais simplesmente porque o Windows de versão aumentou. Os verificadores de versão mal escritos continuam a criar problemas para softwares que, caso contrário, funcionam bem em versões mais recentes do Windows ou simplesmente com a adição de um Windows service pack.

A lógica de comparação de verificação de versão frágil para o runtime do DirectX criou várias instalações com falha quando é executado em diferentes versões do Windows. O número de versão do DirectX se aplica somente aos componentes principais do sistema operacional. Ele não se aplica aos componentes do SDK do DirectX lado a lado que são usados por muitos jogos.

</dd> <dt>

<span id="Additional_Information"></span><span id="additional_information"></span><span id="ADDITIONAL_INFORMATION"></span>**Informações adicionais**
</dt> <dd>

É muito comum ver os instaladores verificarem se há uma versão mínima do sistema operacional. Essa verificação, no entanto, precisa ser feita com cuidado para garantir que ela teste para maior ou igual a, em vez de igualdade simples, assim, bloquear para uma versão específica do sistema operacional. Usar Application Verifier teste **HighVersionLie** é uma maneira rápida e fácil de determinar como o instalador reagirá a uma alteração significativa no número de versão do sistema operacional.

O uso adequado do pacote de redistribuição de runtime do DirectX (Instalação do DirectX) envolve sempre inove-o durante a instalação, preferencialmente no modo silencioso. Isso permite que o código fornecido pela Microsoft execute as atualizações de versão necessárias. Ele também permite a instalação de quaisquer componentes opcionais do SDK do DirectX lado a lado, como D3DX, XACT, MDX ou XInput.

Para ver as práticas recomendadas para implantar o runtime do DirectX, consulte [Instalação do DirectX para desenvolvedores de jogos.](/windows/desktop/DxTechArts/directx-setup-for-game-developers)

É recomendável que os jogos que dão suporte ao Windows XP verifiquem se há um nível de service pack 2 ou superior, pois o Service Pack 2 (SP2) e o Service Pack 3 (SP3) fornecem melhorias significativas de segurança, um requisito simplificado de Redistribuição do DirectX Runtime e uma implantação extremamente ampla. A maioria das tecnologias modernas da Microsoft que Windows o XP exige SP2 ou SP3 (XAudio2, Jogos para Windows – LIVE e assim por diante).

</dd> </dl>

### <a name="26-support-concurrent-user-sessions"></a>2.6 Suporte a sessões de usuário simultâneas

<dl> <dt>

<span id="Requirement"></span><span id="requirement"></span><span id="REQUIREMENT"></span>**Exigência**
</dt> <dd>

Os jogos que dependem de gráficos 3D não precisam funcionar em uma conexão de área de trabalho remota, mas o usuário deve ser alertado quando o jogo falhar.

Os jogos devem dar suporte Windows cenários de multitarefa padrão, aderindo às seguintes regras:

-   Os jogos não devem bloquear o uso de sessões de usuário simultâneas.
-   Um jogo deve ser executado em uma nova sessão de usuário quando ele já estiver em execução em outra sessão.
-   O som do jogo em uma sessão de usuário não deve ser ouvido quando outro usuário está ativo em uma sessão diferente.
-   Os jogos devem dar suporte à Troca Rápida de Usuários.
-   Os jogos não devem tentar desabilitar a alternação de tarefas padrão. Os jogos não devem desabilitar o atalho de teclado ALT+TAB. Os jogos têm permissão para desabilitar atalhos de teclado de acessibilidade, conforme descrito em [Desabilitando teclas de atalho em Jogos](/windows/desktop/DxTechArts/disabling-shortcut-keys-in-games).

</dd> <dt>

<span id="Rationale"></span><span id="rationale"></span><span id="RATIONALE"></span>**Lógica**
</dt> <dd>

Windows os usuários devem ser capazes de executar sessões simultâneas sem conflitos ou interrupções. Esse é um cenário comum para um computador Windows que é compartilhado por uma família, desamidados ou outros.

</dd> <dt>

<span id="Additional_Information"></span><span id="additional_information"></span><span id="ADDITIONAL_INFORMATION"></span>**Informações adicionais**
</dt> <dd>

Para testar se o jogo é lançado em uma sessão remota, chame [**GetSystemMetrics**](/windows/desktop/api/winuser/nf-winuser-getsystemmetrics)(SM \_ REMOTESESSION). Um valor não zero indica que a sessão é remota.

Para obter mais informações, consulte [Troca rápida de usuário.](/windows-hardware/drivers/display/fast-user-switching) Observe que a Opção Rápida de Usuário ocorrerá se as restrições de tempo dos Controles Dos Pais estão habilitadas quando o tempo do usuário está acima. Consulte o requisito 1,2 para obter mais detalhes.

</dd> </dl>

### <a name="27-support-long-names"></a>2,7 nomes longos de suporte

<dl> <dt>

<span id="Requirement"></span><span id="requirement"></span><span id="REQUIREMENT"></span>**Obrigatoriedade**
</dt> <dd>

Se um jogo oferecer suporte para salvar arquivos, ele deverá ser capaz de salvar arquivos que têm nomes e caminhos longos. O jogo deve lidar corretamente com caracteres especiais do sistema de arquivos, como \\ /: \* ? " < >, em qualquer campo de entrada do usuário que é usado para criar nomes de arquivo ou caminhos.

Os jogos devem funcionar corretamente quando um usuário tem um nome de usuário longo.

</dd> <dt>

<span id="Rationale"></span><span id="rationale"></span><span id="RATIONALE"></span>**Lógica**
</dt> <dd>

Os jogadores estão acostumados a usar nomes longos em caminhos profundos que são suportados pelo sistema operacional subjacente.

</dd> <dt>

<span id="Additional_Information"></span><span id="additional_information"></span><span id="ADDITIONAL_INFORMATION"></span>**Informações adicionais**
</dt> <dd>

nomes longos são definidos como aqueles que contêm os valores máximos definidos no SDK do Windows.

</dd> </dl>

## <a name="installation"></a>Instalação

**Resumo dos requisitos de segurança e compatibilidade**

**Benefícios do cliente**

os clientes podem ter certeza de que os aplicativos serão instalados em Windows sem degradar o sistema operacional ou outros aplicativos se os aplicativos usarem métodos oficiais de distribuição de componentes do sistema. Uma experiência de instalação simplificada fornece uma experiência pronta para uso mais acessível e sem problemas para jogos.

### <a name="31-support-easy-installation"></a>3,1 suporte à instalação fácil

<dl> <dt>

<span id="Requirement"></span><span id="requirement"></span><span id="REQUIREMENT"></span>**Obrigatoriedade**
</dt> <dd>

Os jogos devem fornecer um caminho simplificado na interface do usuário de instalação implementando o seguinte:

-   Exibir um máximo de um prompt de EULA.
-   O caminho de instalação padrão deve ignorar todas as seleções para a instalação (como a pasta de instalação ou seleções de componentes), assumir as seleções padrão e, em seguida, executar o jogo ou o iniciador após a instalação bem-sucedida, sem prompts adicionais. Se desejar, uma opção de instalação personalizada pode ser fornecida para opções de configuração avançadas.
-   Instale todos os componentes necessários do sistema operacional (como os tempos de execução do DirectX e do Visual C) usando os pacotes de redistribuição da Microsoft corretos. A instalação deve ser executada silenciosamente, sem avisar e sem ser protegida por verificações de versão de componente.
-   Forneça a remoção por meio de **programas e recursos** no **painel de controle** para o aplicativo do jogo e os arquivos de trabalho gerados. É recomendável uma opção para excluir qualquer arquivo de dados criado pelo usuário. O processo de remoção deve garantir que todos os arquivos instalados sejam removidos e todas as configurações (por exemplo, entradas da lista de exceção do firewall e chaves do registro) sejam limpas. Os componentes redistribuídos do sistema operacional não devem ser removidos.
-   se o jogo exigir exceções a serem adicionadas ao Windows Firewall, o processo de instalação poderá solicitar que o informe os usuários de que essa alteração é necessária. Esse prompt deve aparecer antes do início da instalação.

A instalação e a remoção podem exigir direitos administrativos. A aplicação de patch pode exigir a solicitação de credenciais administrativas, dependendo da frequência de atualização. A reprodução normal do jogo não deve exigir direitos administrativos, por requisito 2,1 Siga as diretrizes de controle de conta de usuário.

</dd> <dt>

<span id="Rationale"></span><span id="rationale"></span><span id="RATIONALE"></span>**Lógica**
</dt> <dd>

a fácil instalação é uma filosofia de desenvolvimento de jogos centrada em Windows que foi projetada para simplificar e simplificar o processo, às vezes, entediante e confuso de instalar jogos em computadores que executam Windows sistemas operacionais. a instalação fácil é habilitada utilizando um conjunto de tecnologias e práticas recomendadas que reduzem a complexidade desnecessária e o risco percebido de instalar jogos em computadores Windows.

Os principais objetivos são:

-   Reduza a quantidade de tempo para entrar no jogo e começar a jogar.
-   Reduza o número de caixas de diálogo e opções a muito poucos, ou nenhum, para simplificar a experiência de instalação do jogo.

Algumas instalações tradicionais têm prompts que permitem instalações não funcionais, embora o aplicativo pareça estar instalado com êxito. Por exemplo, um jogo pode exigir que um usuário aceite um EULA. O jogo é instalado e, em seguida, o EULA do DirectX é exibido. Esse EULA permite que os usuários recusem e, portanto, ignoram a instalação do tempo de execução do DirectX. Esse cenário pode resultar em um jogo que não é executado devido a componentes ausentes.

</dd> <dt>

<span id="Additional_Information"></span><span id="additional_information"></span><span id="ADDITIONAL_INFORMATION"></span>**Informações adicionais**
</dt> <dd>

Para obter mais informações sobre instalação de jogos, técnicas de instalação de jogos não tradicionais, soluções de aplicação de patches compatíveis com o UAC e manipulação de patches frequentes, consulte os seguintes artigos do DirectX:

-   [Simplificando a instalação do jogo](/windows/desktop/DxTechArts/simplifying-game-installation)
-   [Instale-sob demanda para jogos](/windows/desktop/DxTechArts/install-on-demand-for-games)
-   [aplicação de patch no Software de jogos no Windows XP, Windows Vista e Windows 7](/windows/desktop/DxTechArts/patching-methods-in-windows-xp-and-vista)
-   [Práticas recomendadas de instalação para jogos online com vários participantes](/windows/desktop/DxTechArts/mmo-installation-best-practices)

> [!Note]  
> A remoção de arquivos de dados gerados específicos do usuário deve ser executada somente para o usuário atual e para locais de usuário compartilhados comuns. Não há uma maneira robusta de verificar o sistema para remover arquivos específicos do usuário para outros usuários, mesmo que a remoção exija credenciais administrativas.

 

</dd> </dl>

### <a name="32-support-user-account-control-for-installation"></a>3,2 controle de conta de usuário de suporte para instalação

<dl> <dt>

<span id="Requirement"></span><span id="requirement"></span><span id="REQUIREMENT"></span>**Obrigatoriedade**
</dt> <dd>

O instalador de jogos não deve pressupor que esteja em execução no mesmo contexto que o usuário. Os locais específicos do usuário serão diferentes do instalador e do Player até mesmo para sistemas de usuário único devido à elevação de credenciais do administrador. Portanto, quando um jogo é executado pela primeira vez, ele deve executar tarefas específicas do usuário, separadamente do processo de instalação.

a caixa de diálogo Windows exceção de Firewall não deve aparecer quando um usuário hospeda ou ingressa em um jogo com vários participantes. Qualquer configuração necessária deve ser feita no momento da instalação. As instruções de instalação devem informar ao usuário que essa operação ocorrerá como parte da configuração.

O instalador do jogo deve fornecer um manifesto incorporado que designa o nível de execução necessário, por requisito 2,1 Siga as diretrizes de controle de conta de usuário.

Se o jogo for iniciado pelo instalador após a conclusão da instalação, ele deverá ser iniciado no contexto do usuário original.

</dd> <dt>

<span id="Rationale"></span><span id="rationale"></span><span id="RATIONALE"></span>**Lógica**
</dt> <dd>

uma das maiores alterações no sistema operacional Windows no Windows Vista é a adição do UAC (controle de conta de usuário), que executa aplicativos com privilégios reduzidos por padrão. Como resultado, os instaladores precisam gerenciar níveis de privilégio de acordo. Windows 7 também faz uso extensivo do UAC. embora Windows 7 aprimore a experiência do usuário do UAC, os instaladores ainda devem atender aos mesmos requisitos que o Windows Vista para funcionar corretamente, sem depender do comportamento potencialmente confuso de virtualização.

o UAC está ativo por padrão no Windows Vista e no Windows 7, e a grande maioria dos clientes (88% ou mais, com base nos comentários) deixa esse recurso habilitado.

</dd> <dt>

<span id="Additional_Information"></span><span id="additional_information"></span><span id="ADDITIONAL_INFORMATION"></span>**Informações adicionais**
</dt> <dd>

para obter mais detalhes sobre como configurar o firewall do Windows, consulte o artigo sobre o DirectX [Windows firewall para desenvolvedores de jogos](/windows/desktop/DxTechArts/games-and-firewalls) e o exemplo FirewallInstallHelper.

A inicialização padrão do jogo no final do processo de instalação falhará em atender ao último aspecto desse requisito se a instalação for iniciada por um usuário padrão e se o processo de instalação exigir privilégios administrativos (ou seja, solicitar credenciais de administrador). Ele também herda privilégios administrativos, o que é um risco de segurança potencial. Em vez disso, um carregador de inicialização da instalação deve iniciar o jogo depois de retornar de uma invocação bem-sucedida do instalador. para obter mais informações, consulte o artigo da MSDN Magazine [ensinar seus aplicativos a brincar com o Windows o controle de conta de usuário Vista](/archive/msdn-magazine/2007/january/teach-your-apps-to-work-with-windows-vista-user-account-control).

</dd> </dl>

### <a name="33-install-to-correct-folders"></a>3,3 instalar em pastas corretas

<dl> <dt>

<span id="Requirement"></span><span id="requirement"></span><span id="REQUIREMENT"></span>**Obrigatoriedade**
</dt> <dd>

Os jogos instalados para todos os usuários devem ser instalados na pasta arquivos de programas por padrão. Os dados do usuário devem ser gravados quando o jogo é executado pela primeira vez, não durante a instalação.

</dd> <dt>

<span id="Rationale"></span><span id="rationale"></span><span id="RATIONALE"></span>**Lógica**
</dt> <dd>

Os usuários devem ter a flexibilidade de instalar aplicativos onde precisam deles. Eles também devem ter uma experiência consistente e segura com o local padrão dos arquivos.

</dd> <dt>

<span id="Additional_Information"></span><span id="additional_information"></span><span id="ADDITIONAL_INFORMATION"></span>**Informações adicionais**
</dt> <dd>

Os jogos podem fazer uso de vários locais de pasta conhecidos (como aqueles especificados por CSIDl \_ local de \_ AppData e CSIDL \_ comuns \_ de AppData) para armazenar quantidades significativas de dados de jogos e dar suporte a arquivos executáveis para implementar cenários avançados de instalação sob demanda e aplicação de patches.

Como a instalação pode exigir a elevação para uma conta de usuário diferente durante o processo de instalação de todos os usuários, não há nenhum local de usuário correto no qual armazenar dados no momento da instalação. Além disso, se a criptografia de arquivo estiver habilitada, os arquivos criptografados só poderão ser acessados pela conta de usuário que os criou.

</dd> </dl>

### <a name="34-install-windows-resources-properly"></a>3,4 instalar Windows recursos corretamente

<dl> <dt>

<span id="Requirement"></span><span id="requirement"></span><span id="REQUIREMENT"></span>**Obrigatoriedade**
</dt> <dd>

os aplicativos não devem tentar instalar arquivos ou chaves do registro protegidos por Proteção de Recursos do Windows (WRP). Se o aplicativo exigir versões mais recentes dos componentes do sistema, ele deverá atualizar esses componentes usando um Microsoft Service Pack ou um pacote de instalação aprovado pela Microsoft que contenha o componente do sistema. Os componentes do sistema nunca devem ser reempacotados.

</dd> <dt>

<span id="Rationale"></span><span id="rationale"></span><span id="RATIONALE"></span>**Lógica**
</dt> <dd>

Windows A WRP (proteção de recursos) foi projetada para garantir que os recursos protegidos do sistema sejam atualizados somente usando os mecanismos de instalação ou atualização aprovados pela Microsoft. A WRP melhora a confiabilidade do sistema, garantindo que os resultados de uma instalação sejam previsíveis.

</dd> <dt>

<span id="Additional_Information"></span><span id="additional_information"></span><span id="ADDITIONAL_INFORMATION"></span>**Informações adicionais**
</dt> <dd>

a WRP é o sucessor de Windows proteção de arquivo, que protege a maioria dos componentes do sistema instalados na pasta Windows. A WRP protege a maioria das chaves do registro que armazenam configurações para a criação de objetos COM. Ele também reserva certas pastas para uso exclusivo pelo sistema operacional. As tentativas de acessar recursos protegidos normalmente resultam em um erro de negação de acesso.

Para obter detalhes de práticas recomendadas quando o tempo de execução do DirectX é implantado com um jogo, consulte o artigo DirectX [instalação do DirectX para desenvolvedores de jogos](/windows/desktop/DxTechArts/directx-setup-for-game-developers).

</dd> </dl>

### <a name="35-avoid-reboots-during-installation"></a>3,5 evitar reinicializações durante a instalação

<dl> <dt>

<span id="Requirement"></span><span id="requirement"></span><span id="REQUIREMENT"></span>**Obrigatoriedade**
</dt> <dd>

o instalador de jogos não deve supor que a instalação de componentes Windows de pacotes de redistribuição exige uma reinicialização, a menos que a reinicialização seja indicada por um resultado de retorno ou pela documentação da Microsoft.

Se o instalador do jogo sempre forçar uma reinicialização, isso deve ser aprovado pela Microsoft.

as caixas de diálogo arquivos em uso que estão incluídas em pacotes Windows Installer devem conter uma opção para fechar os aplicativos automaticamente e tentar reiniciá-los após a conclusão da instalação.

</dd> <dt>

<span id="Rationale"></span><span id="rationale"></span><span id="RATIONALE"></span>**Lógica**
</dt> <dd>

A reinicialização do sistema após a instalação é uma interrupção inconveniente para os usuários e normalmente é desnecessária.

</dd> <dt>

<span id="Additional_Information"></span><span id="additional_information"></span><span id="ADDITIONAL_INFORMATION"></span>**Informações adicionais**
</dt> <dd>

para obter mais informações, consulte [usando Windows Installer com o gerenciador de reinicialização](/windows/desktop/Msi/using-windows-installer-with-restart-manager).

</dd> </dl>

### <a name="36-use-file-versioning-correctly"></a>3,6 usar o controle de versão de arquivo corretamente

<dl> <dt>

<span id="Requirement"></span><span id="requirement"></span><span id="REQUIREMENT"></span>**Obrigatoriedade**
</dt> <dd>

O programa de instalação de jogos deve verificar corretamente se as versões de arquivo mais recentes estão instaladas. Instalar um jogo nunca deve retornar nenhum arquivo que você não produz ou que são compartilhados por aplicativos que você não produz.

</dd> <dt>

<span id="Rationale"></span><span id="rationale"></span><span id="RATIONALE"></span>**Lógica**
</dt> <dd>

Componentes compartilhados e componentes do sistema geralmente são atualizados para correções de segurança e funcionalidade expandida. Uma instalação que inclui uma versão mais antiga dos componentes atualizados não deve resultar na perda de atualizações e correções que já foram aplicadas.

</dd> </dl>

### <a name="37-support-autorun-conditional-requirement"></a>3,7 suporte a \[ requisito condicional de Autorun\]

<dl> <dt>

<span id="Requirement"></span><span id="requirement"></span><span id="REQUIREMENT"></span>**Obrigatoriedade**
</dt> <dd>

Para jogos distribuídos em CD, DVD ou outras mídias removíveis que oferecem suporte a autorun, quando o disco é inserido pela primeira vez, o aplicativo deve executar automaticamente ou solicitar que o usuário instale o jogo, a menos que o usuário tenha desabilitado o recurso AutoRun.

Depois que o aplicativo for instalado com êxito, a reinserção do disco na unidade não deverá fazer com que a instalação inicie automaticamente de novo. É aceitável perguntar aos usuários se eles desejam atualizar ou alterar suas opções de instalação.

O aplicativo autorun não deve solicitar elevação (ou seja, deve ter asInvoker no manifesto, por requisito 2,1, embora possa iniciar o programa de instalação ou outro utilitário que exija direitos administrativos. A elevação deve ocorrer somente se o jogo não estiver instalado ou se o usuário o selecionar especificamente.

</dd> <dt>

<span id="Rationale"></span><span id="rationale"></span><span id="RATIONALE"></span>**Lógica**
</dt> <dd>

O autorun simplifica a experiência de usar aplicativos distribuídos em mídia, como jogos que normalmente exigem que o disco esteja presente na unidade para jogar o jogo.

</dd> <dt>

<span id="Additional_Information"></span><span id="additional_information"></span><span id="ADDITIONAL_INFORMATION"></span>**Informações adicionais**
</dt> <dd>

Não é aceitável exigir que o usuário navegue no explorador de arquivos para iniciar a instalação a partir do CD ou DVD.

Para jogos que são distribuídos em vários discos, os discos subsequentes devem, idealmente, usar o recurso AutoRun ou continuar a instalação sem solicitar que o usuário pressione uma tecla ou execute outra ação.

Ao criar um programa de autorun, verifique se todos os componentes necessários estão presentes nas novas instalações do Windows. Aplicativos típicos dependem de tecnologias instaladas pela instalação, mas o autorun em si é executado antes que qualquer configuração ocorra. um exemplo comum é a falha dos programas Autorun porque as DLLs de tempo de execução do Visual C não foram incluídas como parte da configuração do Windows. O programa autorun, portanto, deve usar a implantação de CRT local do aplicativo ou deve vincular estaticamente o CRT.

programas de execução automática escritos para uso em versões do Windows antes de Windows Vista não devem usar o tempo de execução do .net porque essa tecnologia não está incluída no Windows XP ou em versões anteriores do Windows. Windows o Server 2003 e o Windows Vista são as primeiras versões do Windows para incluir o tempo de execução do .net como parte de seu sistema operacional.

Por motivos semelhantes, os programas autorun não podem exigir a presença de componentes lado a lado opcionais do SDK do DirectX, como D3DX9, D3DX10, D3DX11, XAudio2, X3DAudio, transação, XINPUT e MDX 1,1.

Para obter um exemplo de como usar o autorun, consulte exemplo de AutoRun.

</dd> </dl>

## <a name="reliability"></a>Confiabilidade

**Resumo dos requisitos de segurança e compatibilidade**

**Benefícios do cliente**

Esses requisitos tornam um aplicativo mais confiável, minimizando o número de falhas, travamentos e reinicializações. Os requisitos de confiabilidade podem ajudar a garantir que o software seja mais previsível, sustentável, resiliente e recuperável.

### <a name="41-eliminate-unnecessary-reboots"></a>4,1 eliminar reinicializações desnecessárias

<dl> <dt>

<span id="Requirement"></span><span id="requirement"></span><span id="REQUIREMENT"></span>**Obrigatoriedade**
</dt> <dd>

Todos os instaladores de aplicativo devem aproveitar as APIs do Gerenciador de reinicialização para evitar reinicializações do sistema (consulte o requisito 3,5).

Os jogos não devem bloquear o desligamento.

Todos os aplicativos devem responder ao Gerenciador de reinicialização ouvindo e respondendo às seguintes mensagens de desligamento:

<dl> <dt>

<span id="WM_QUERYENDSESSION_with_LPARAM___ENDSESSION_CLOSEAPP__0x1___"></span><span id="wm_queryendsession_with_lparam___endsession_closeapp__0x1___"></span><span id="WM_QUERYENDSESSION_WITH_LPARAM___ENDSESSION_CLOSEAPP__0X1___"></span>WM \_ QUERYENDSESSION com lParam = EndSession \_ CLOSEAPP (0x1) 
</dt> <dd>

Os aplicativos de GUI devem responder (TRUE) imediatamente na preparação para uma reinicialização.

</dd> <dt>

<span id="WM_ENDSESSION_with_LPARAM___ENDSESSION_CLOSEAPP__0x1___"></span><span id="wm_endsession_with_lparam___endsession_closeapp__0x1___"></span><span id="WM_ENDSESSION_WITH_LPARAM___ENDSESSION_CLOSEAPP__0X1___"></span>\_EndSession do WM com lParam = EndSession \_ CLOSEAPP (0x1) 
</dt> <dd>

Os aplicativos devem retornar um valor 0 em 5 segundos e, em seguida, fechar.

</dd> <dt>

<span id="CTRL_C__"></span><span id="ctrl_c__"></span>CTRL + C 
</dt> <dd>

Os aplicativos de console que recebem essa mensagem devem ser fechados imediatamente.

</dd> </dl> </dd> <dt>

<span id="Rationale"></span><span id="rationale"></span><span id="RATIONALE"></span>**Lógica**
</dt> <dd>

As reinicializações do sistema são uma grande interrupção. Eles levam a uma experiência de usuário inadequada e devem ser minimizados. Algumas operações, como atualizações críticas do sistema, podem exigir reinicializações. Ao escutar mensagens de desligamento, o jogo e outros aplicativos podem reagir imediatamente às solicitações do Gerenciador de reinicialização. Dessa forma, eles podem evitar atrasos desnecessariamente em solicitações de reinicialização válidas.

</dd> <dt>

<span id="Additional_Information"></span><span id="additional_information"></span><span id="ADDITIONAL_INFORMATION"></span>**Informações adicionais**
</dt> <dd>

se um instalador de jogo usar a tecnologia de Windows Installer (MSI) sem nenhuma ação personalizada, essa funcionalidade será fornecida automaticamente. Os pacotes de redistribuição da Microsoft também dão suporte ao Gerenciador de reinicialização.

Para obter mais informações sobre o Gerenciador de reinicialização, consulte o artigo do MSDN [sobre o Restart Manager](/windows/desktop/RstMgr/about-restart-manager).

</dd> </dl>

### <a name="42-eliminate-application-verifier-failures"></a>4,2 eliminar falhas de Application Verifier

<dl> <dt>

<span id="Requirement"></span><span id="requirement"></span><span id="REQUIREMENT"></span>**Obrigatoriedade**
</dt> <dd>

O jogo deve gerar nenhuma falha em execução no Microsoft Application Verifier (AppVerifier), versão 4,0 ou posterior, nos seguintes testes:

-   Noções básicas: identificadores, heaps, bloqueios, memória, TLS
-   Diversos: DangerousAPIs, DirtyStacks

</dd> <dt>

<span id="Rationale"></span><span id="rationale"></span><span id="RATIONALE"></span>**Lógica**
</dt> <dd>

o AppVerifier testa vários problemas conhecidos que causam falhas e trava em Windows aplicativos, bem como vulnerabilidades de segurança conhecidas.

</dd> <dt>

<span id="Additional_Information"></span><span id="additional_information"></span><span id="ADDITIONAL_INFORMATION"></span>**Informações adicionais**
</dt> <dd>

Para obter mais informações sobre Application Verifier, consulte [Application Verifier](/previous-versions/ms220948(v=vs.80)) e [usando Application Verifier em seu ciclo de vida de desenvolvimento de software](/previous-versions/aa480483(v=msdn.10)) no msdn. Você pode baixar Application Verifier de [detalhes de download: Application Verifier](https://www.microsoft.com/downloads/details.aspx?familyid=c4a25ab9-649d-4a1b-b4a7-c9d8b095df18) no centro de download da Microsoft.

Esse requisito não se aplica a aplicativos gerenciados puros sem interoperabilidade nativa.

Esses testes devem ser executados em uma compilação de versão. A depuração de compilações pode gerar falhas falsas. Algumas tecnologias antipirataria e antifalsificação podem interferir na execução do AppVerifier. Portanto, esses testes devem ser executados sem as tecnologias antipiratade e antifalsificação habilitadas.

Pode ser necessário definir a propriedade completa do Basic: heaps Test como FALSE, pois o PageHeap completo aumenta muito a pressão de memória do aplicativo em execução. As falhas ainda serão detectadas, mas podem ser mais difíceis de rastrear se você usar apenas PageHeap parciais.

Se você usar os testes relacionados ao UAC/LUA em Application Verifier para atender aos requisitos de controle de conta de usuário 2,1 e 3,2, deverá usar o [Standard User Analyzer](/windows/desktop/Win7AppQual/standard-user-analyzer--sua--tool-and-standard-user-analyzer-wizard--sua-wizard-) para examinar os resultados. Também há vários outros testes úteis fornecidos por Application Verifier que você é altamente incentivado a usar no desenvolvimento e no teste para garantir um alto nível de compatibilidade com versões atuais e futuras do Windows. O teste **HighVersionLie** é usado para verificar a conformidade com o requisito 2,5.

Visual Studio O Team System inclui um subconjunto da funcionalidade de AppVerifier que é integrada ao ambiente de depuração. Isso pode ser útil para rastrear e resolver problemas com noções básicas: heaps, identificadores e testes de bloqueios.

</dd> </dl>

### <a name="43-support-windows-error-reporting-and-file-version-information"></a>4,3 Relatório de Erros do Windows de suporte e informações de versão do arquivo

<dl> <dt>

<span id="Requirement"></span><span id="requirement"></span><span id="REQUIREMENT"></span>**Obrigatoriedade**
</dt> <dd>

para habilitar o suporte do Relatório de Erros do Windows, os jogos devem atender aos seguintes requisitos:

-   Os jogos devem tratar apenas as exceções conhecidas e esperadas. Relatório de Erros do Windows não deve ser desabilitado. se uma falha, como uma violação de acesso, aparecer em um jogo, ela deverá permitir que Relatório de Erros do Windows relate a falha.
-   Todos os arquivos executáveis (por exemplo, arquivos de .exe ou DLLs) devem conter um nome de produto preciso, nome da empresa e versão do arquivo.
-   A saída normal do jogo não deve resultar em uma falha de exceção desconhecida.

</dd> <dt>

<span id="Rationale"></span><span id="rationale"></span><span id="RATIONALE"></span>**Lógica**
</dt> <dd>

as APIs de Relatório de Erros do Windows fornecem comentários vitais à Microsoft para detectar falhas e travas generalizadas em aplicativos. Isso permite que a Microsoft e seus parceiros detectem e resolvam rapidamente problemas de sistema e driver que levam a falhas de aplicativos rapidamente.

</dd> <dt>

<span id="Additional_Information"></span><span id="additional_information"></span><span id="ADDITIONAL_INFORMATION"></span>**Informações adicionais**
</dt> <dd>

Os jogos podem incluir manipuladores de exceção sem tratamento personalizados para executar a funcionalidade personalizada de suporte e relatórios, mas eles devem passar qualquer erro para as funções **ReportFault** ou **WerReportSubmit** .

as informações adequadas de versão do arquivo podem ser verificadas exibindo as propriedades do arquivo na interface do usuário do Windows desktop e verificando a página de propriedades da versão.

para obter mais informações sobre as APIs de Relatório de Erros do Windows e como analisar os despejos de memória gerados quando você usa esse serviço, consulte o artigo do DirectX [análise de despejo](/windows/desktop/DxTechArts/crash-dump-analysis)de memória.

</dd> </dl>

## <a name="xbox-360-common-controller-for-windows-terminology"></a>controlador comum do Xbox 360 para terminologia Windows



| Nome                                          | Descrição                                                                                                 |
|------------------------------------------|--------------------------------------------------------------------------------------------------|
| Um                                        | O botão a.                                                                                     |
| B                                        | O botão B.                                                                                     |
| BACK                                     | O botão Voltar.                                                                                  |
| amortecedor (direita/esquerda)                      | O botão na parte superior direita e na borda esquerda do controlador. Equivalente a um botão de ressalto.    |
| painel direcional                          | O painel direcional do controlador.                                                                   |
| Painel D                                    | Abreviação aceita de pad direcional.                                                         |
| DP                                       | Abreviação de pad direcional e rótulo de controlador.                                                |
| RB, LB                                   | Abreviações e rótulos de controlador de subtapares à direita e à esquerda.                                        |
| RS, LS                                   | Abreviações e rótulos do controlador da direita e esquerda.                                         |
| RT, LT                                   | As abreviações e os rótulos do controlador do gatilho à direita e à esquerda.                                       |
| RSB, LSB                                 | Abreviações e rótulos do controlador da direita e esquerda.                                         |
| START                                    | O botão Iniciar.                                                                                 |
| (direita/esquerda) pente                       | O controlador do pente. Anteriormente Thumbstick.                                                       |
| botão de aderência (direita/esquerda)                | O botão do controlador. Antigo botão Thumbstick.                                         |
| gatilho (direita/esquerda)                     | O gatilho do controlador.                                                                          |
| Vibração                                | Comentários em jogo produzidos pelo motor do controlador. Não use Rumble.                           |
| X                                        | O botão X.                                                                                     |
| Y                                        | O botão Y.                                                                                     |
| Controle Xbox 360 para Windows          | o gamepad do Xbox 360 vendeu como um SKU de hardware de PC, incluindo um disco de driver de dispositivo Windows.          |
| Controle sem Fio Xbox 360 para Windows | o gamepad sem fio do Xbox 360 vendeu como um SKU de hardware de PC, incluindo um disco de driver de dispositivo Windows. |



 

## <a name="guidelines-for-game-middleware-products"></a>Diretrizes para produtos de middleware de jogos

### <a name="introduction"></a>Introdução

para que os jogos se qualifiquem para os jogos para Windows programa, eles devem atender a uma lista de requisitos técnicos. Todos os componentes de terceiros fornecidos com um título (arquivos executáveis, DLLs, drivers e assim por diante) também devem atender a esses requisitos para que o jogo se qualifique. Este documento destaca os requisitos mais comuns que também devem ser atendidos pelos componentes de terceiros para que o jogo passe os testes de conformidade. os instaladores e os pacotes de produção/mecanismo de jogos completos devem examinar o documento de requisitos técnicos do Windows Games, pois muitos desses requisitos são afetados por essas ferramentas.

### <a name="additional-recommendations"></a>Recomendações adicionais

além de garantir que o componente dê suporte à criação de títulos compatíveis com os requisitos para jogos para Windows, há várias outras considerações que você deve levar em conta ao projetar e implantar um utilitário de biblioteca ou suporte para um jogo de Windows.

-   Para dar suporte a desenvolvedores que trabalham em aplicativos x64 nativos de 64 bits, forneça versões nativas de 32 bits e de 64 bits de suas bibliotecas. A versão de 32 bits deve ser compatível com 64 bits por 2,2. Bibliotecas de aplicativos de 32 bits não devem assumir que o alto bit de qualquer endereço de 32 bits não é usado para dar suporte ao uso em aplicativos LARGEADDRESSAWARE x86.
-   Se você fornecer cabeçalhos de código nativo (C/C++), use a sintaxe de atributo SAL (linguagem de anotação padrão) para decorar suas rotinas de API pública. isso permitirá que os usuários da sua biblioteca obtenham o máximo benefício de usar o Code Analysis estático (/analyze), que faz parte do Visual Studio team system 2005, Visual Studio team system 2008, Visual Studio 2010 Premium e Visual Studio 2010 Ultimate, bem como as ferramentas de compilador SDK do Windows disponíveis publicamente.
-   Se seu produto criar threads dentro do processo do usuário, certifique-se de nomear cada thread para que as ferramentas de depuração possam anotar corretamente os threads em execução.
-   Se você escrever rotinas que devem ser chamadas dentro do loop principal de um jogo, use as rotinas de D3DX D3DPERF \_ BeginEvent/endEvent e D3DPERF \_ setmarc para anotar operações de alto nível para facilitar a identificação dos afunilamentos usando o PIX para Windows.
    > [!Note]  
    > para a funcionalidade de diagnóstico de gráficos Visual Studio 2012, essas rotinas D3DX e PIX são substituídas pela interface [**ID3DUserDefinedAnnotation**](/windows/desktop/api/d3d11_1/nn-d3d11_1-id3duserdefinedannotation) .

     

-   para bibliotecas de rede, forneça implementações com neutralidade de IP e evite rotinas somente IPv4 preteridas para dar suporte às tecnologias IPv6 e Teredo no Windows XP com Service Pack 2, Windows Vista e Windows 7.
-   Os provedores de serviço de jogos devem se registrar com o explorador de jogos usando a versão 2 do esquema GDF e usam o recurso RSS para fornecer notícias relacionadas ao serviço.

### <a name="games-for-windows-showcases"></a>jogos para Windows de casos

### <a name="introduction"></a>Introdução

jogos para Windows demonstrações vão além de fornecer uma experiência de jogos sólida em PCs Windows. ao implementar esses recursos, os jogos podem adicionar mais entusiasmo à experiência do usuário nas plataformas de Windows mais recentes.

os jogos para títulos de Windows devem atender a todos os requisitos técnicos listados neste artigo, mas os recursos de demonstração são opcionais. Esses títulos são gratuitos para implementar alguns, nenhum ou todos esses casos.

### <a name="s1-exploit-direct3d-11"></a>S. 1 explorar o Direct3D 11

<dl> <dt>

<span id="Requirement"></span><span id="requirement"></span><span id="REQUIREMENT"></span>**Obrigatoriedade**
</dt> <dd>

o Direct3D 11 é a API de renderização da próxima geração para o Windows Vista e o Windows 7. Jogos que exploram o Direct3D 11 usam conteúdo otimizado, técnicas de renderização avançadas e novos recursos de hardware para criar uma experiência atraente em hardware que dá suporte a 10, 10,1 e 11.

Se o jogo também implementar o Direct3D 9, uma comparação lado a lado deve demonstrar uma melhoria perceptível na qualidade do conteúdo, fidelidade visual, desempenho, complexidade da cena e outras áreas de fidelidade de gráficos para o Direct3D 11. esse suporte está sujeito aos jogos para Windows requisito técnico 1,7.

a tecnologia direct3d 10level9 pode ser usada para dar suporte ao hardware de vídeo do Shader modelo 2.0/3.0 Direct3D 9 em Windows Vista e Windows 7, em vez de usar uma implementação lado a lado do direct3d 9 para obter amplo suporte a hardware. No entanto, isso não é suficiente para demonstrar esta demonstração.

em computadores que executam o Windows Vista ou Windows 7 com o Direct3D 11 instalado, o jogo deve usar o direct3d 11 como padrão.

</dd> <dt>

<span id="Rationale"></span><span id="rationale"></span><span id="RATIONALE"></span>**Lógica**
</dt> <dd>

a API do direct3d 11 baseia-se no Windows o WDDM (modelo de Driver de vídeo) e na infraestrutura do direct3d 10,1 para dar suporte a novos recursos: mosaico de hardware, sombreadores de computação, processamento multithread e criação de recursos, novos formatos de compactação de textura e uma linguagem de sombreador mais flexível. O Direct3D 11 fornece suporte de hardware unificado para placas de vídeo modernas, incluindo a última geração de peças do Direct3D 11, todas as placas de vídeo do Direct3D 10 e 10,1 e muitos cartões de vídeo do sombreador 2.0/3.0 Direct3D 9, que é o hardware de vídeo mínimo necessário para a área de trabalho 3D do Aero.

</dd> <dt>

<span id="Additional_Information"></span><span id="additional_information"></span><span id="ADDITIONAL_INFORMATION"></span>**Informações adicionais**
</dt> <dd>

A migração de um mecanismo de renderização do Direct3D 9 para usar a nova interface do Direct3D 11 é uma tarefa bem definida:

-   Elimine todas as operações de função fixa em favor de sombreadores programáveis.
-   Atualize todos os sombreadores existentes para a nova sintaxe do Shader Model 4. x/5.
-   Atualize o gerenciamento de recursos para dar suporte ao novo modelo de exibição.
-   Converta todos os ativos para usar uma nova lista de formatos disponíveis.
-   Atualize o tratamento do estado de renderização para usar os blocos de estado imutável e retrabalhe as constantes do sombreador em buffers de constantes.

Essa conversão é essencial para habilitar a demonstração do Direct3D 11, embora o resultado não atenda ao requisito de demonstração de exploração da nova API.

A nova API e o modelo de programação HLSL associado oferecem muitas oportunidades de conteúdo aprimorado:

-   Aproveitando os recursos de hardware existentes do Direct3D 10, como o sombreador Geometry, fluxos de saída, matrizes de textura e os formatos de textura compactados BC4/BC5.
-   Aproveitando os recursos existentes de hardware do Direct3D 10,1, como modos de mesclagem de destino por renderização independentes, leitura de profundidade de MSAA, acesso de sombreador por exemplo de MSAA, matrizes de mapa de cubos e renderização para formatos de BC (em bloco) compactados.
-   Implementar algoritmos avançados de GPU usando o sombreador de computação com o CS4. x em placas de vídeo do Direct3D 10/10.1 existentes (habilitadas por drivers de vídeo atualizados) ou CS 5,0 na próxima geração de placas de vídeo do Direct3D 11.
-   Renderização em vários threads usando a criação de recursos com threads livres e vários contextos de dispositivo para melhorar o desempenho em sistemas multicore (com drivers de vídeo atualizados). para obter mais informações, consulte os jogos para Windows Showcase S. 3.
-   Utilizando novos recursos do hardware de vídeo de classe Direct3D 11, como o mosaico de hardware com envoltória e sombreadores de domínio, os recursos de hardware do sombreador 5,0 HLSL Shader BC6HBC7 formatos de textura compactados e o vínculo de sombreador dinâmico.

As técnicas que podem ser implementadas com o Direct3D 9 (amplamente por meio de alto custo de CPU) podem ser descarregadas para a GPU de maneira eficiente, liberando, assim, os recursos da CPU para dar suporte a outras demandas de jogos.

As APIs do Direct3D 11, as ferramentas de suporte e os exemplos estão disponíveis no SDK do DirectX. Consulte também APIs de gráficos no Windows.

</dd> </dl>

### <a name="s2-exploit-x64-native"></a>S. 2 exploração x64 nativa

<dl> <dt>

<span id="Requirement"></span><span id="requirement"></span><span id="REQUIREMENT"></span>**Obrigatoriedade**
</dt> <dd>

o jogo inclui um executável nativo de 64 bits que fornece uma nova experiência atraente habilitada pelas edições x64 do Windows em execução em hardware compatível com x64. Uma comparação lado a lado com a versão de 32 bits do jogo deve mostrar um aperfeiçoamento perceptível na complexidade do conteúdo, tempos de carregamento geral reduzidos e desempenho.

nas edições de 64 bits do Windows, a instalação deve sempre configurar a versão nativa de 64 bits do jogo como o padrão para atalhos no explorador de jogos e Windows XP Professional x64 Edition. se a instalação dupla for desejada, uma tarefa de reprodução adicional poderá ser especificada para o explorador de jogos no Windows Vista e Windows 7 que aponte para a versão de 32 bits, mas o padrão deverá permanecer a versão nativa de 64 bits.

observe que o jogo deve dar suporte às edições de 64 bits do Windows Vista e Windows 7 para atender a essa recomendação de demonstração. o suporte para Windows XP Professional x64 Edition é incentivado, mas não é necessário.

</dd> <dt>

<span id="Rationale"></span><span id="rationale"></span><span id="RATIONALE"></span>**Lógica**
</dt> <dd>

a tecnologia x64 fornece recursos de endereçamento de 64 bits para os mercados de consumidor e servidor que incluem dos de velocidade completa de 32 bits para aplicativos existentes. o x64 é uma parte fundamental do roteiro para AMD (AMD64) e Intel (EMT64) e, com exceção de CPUs Ultra-móveis, dá suporte à tecnologia para todos os processadores de geração atuais e futuros.

Windows o XP Professional x64 Edition foi o primeiro sistema operacional de Windows orientado ao consumidor para oferecer suporte à tecnologia x64, e o Windows Vista e o Windows 7 ampliam muito a disponibilidade da habilitação do so para a computação do consumidor de 64 bits. Com 2 GB de RAM como padrão em muitos computadores novos, aprimoramentos adicionais no dimensionamento de memória não beneficiarão os aplicativos individuais de 32 bits que não podem resolver mais de 2 GB de RAM física. Hoje em dia, muitos jogos estão enfrentando desafios que ajustam todo o conteúdo disponível nas restrições de 2 GB de espaço de endereço virtual, especialmente quando combinados com as memórias de vídeo grandes disponíveis em GPUs de alta tecnologia, e a mudança para as tecnologias x64 aumenta muito os níveis de detalhes com suporte.

a compatibilidade com x64 para jogos de 32 bits é um dos jogos para Windows requisito técnico (2,2), mas aproveitar ao máximo as novas tecnologias requer uma implementação nativa de 64 bits.

</dd> <dt>

<span id="Additional_Information"></span><span id="additional_information"></span><span id="ADDITIONAL_INFORMATION"></span>**Informações adicionais**
</dt> <dd>

O principal benefício do endereçamento de 64 bits é a capacidade de acessar diretamente mais de 2 GB de memória física e virtual. O espaço de endereço de memória virtual grande permite o uso extensivo de e/s mapeada por memória sem preocupação com problemas de esgotamento de espaço de endereço de VM predominantes na programação de 32 bits. Os jogos podem aproveitar o novo espaço para melhorar muito os tempos de carregamento ou, em algumas instâncias, para eliminar pausas para carregar conteúdo.

Os aplicativos de 32 bits existentes podem se beneficiar de edições x64 com a capacidade de processar endereços com dados completos de 32 bits quando criados com a opção de vinculador de **/LARGEADDRESSAWARE**(habilitar endereços grandes). nas versões de 32 bits do Windows XP, os modos de inicialização especiais permitiam que esses aplicativos tratassem de até 3 gb de ram e as edições x64 fornecem acesso a até 4 gb de ram para aplicativos de reconhecimento de endereço grande (LAA). embora o uso de LAA em um aplicativo de 32 bits não atenda a esse requisito de demonstração, essa tecnologia de ponte é uma maneira extremamente útil de fornecer benefícios de dimensionamento adicionais em versões x64 do Windows para aqueles que não implementam totalmente esse requisito de demonstração.

Para obter mais informações, consulte [programação de 64 bits para desenvolvedores de jogos](/windows/desktop/DxTechArts/sixty-four-bit-programming-for-game-developers) e [RAM, VRAM e mais RAM: jogos de 64 bits estão aqui](https://www.gamasutra.com/view/feature/3602/sponsored_feature_ram_vram_and_.php) no Gamasutra.

> [!Note]  
> Um desafio importante para essa demonstração é garantir que as bibliotecas ou componentes de terceiros dos quais seu jogo se baseia estejam disponíveis para o desenvolvimento nativo de 64 bits. Muitas APIs herdadas da Microsoft também foram eliminadas do ambiente nativo de 64 bits, que pode provar um desafio para as bases de código do mecanismo que contêm implementações mais antigas dos principais sistemas.

 

</dd> </dl>

### <a name="s3-exploit-many-core-processors"></a>S. 3 explorar Many-Core processadores

<dl> <dt>

<span id="Requirement"></span><span id="requirement"></span><span id="REQUIREMENT"></span>**Obrigatoriedade**
</dt> <dd>

O jogo implementa recursos que aproveitam os processadores de vários núcleos, dimensionando para 3, 4 ou mais núcleos, quando disponíveis.

Se o jogo oferecer suporte a sistemas de núcleo único ou Dual-Core, uma comparação lado a lado com um sistema quad-core deve demonstrar novos recursos, efeitos interessantes adicionais, melhoria na qualidade do conteúdo e/ou melhor desempenho.

Como o dimensionamento de dois núcleos já é amplamente suportado por jogos, bem como automaticamente utilizado por vários aprimoramentos de driver de Direct3D, o dimensionamento dual-core não é suficiente para demonstrar essa demonstração.

</dd> <dt>

<span id="Rationale"></span><span id="rationale"></span><span id="RATIONALE"></span>**Lógica**
</dt> <dd>

O crescimento contínuo no desempenho de CPUs mudou de melhorias na taxa de clock para a adição de núcleos computacionais. Os roteiros AMD e Intel são baseados em designs de vários núcleos escalonáveis. Todas as plataformas de jogos de última geração têm CPUs com vários núcleos devido a essa mudança fundamental na evolução dos processadores. Aplicativos de thread único não verão mais ganhos significativos de CPUs de última geração. O multithreading simples também falhará ao dimensionar, pois o número de núcleos de CPU em uso comum cresce para três ou mais.

</dd> <dt>

<span id="Additional_Information"></span><span id="additional_information"></span><span id="ADDITIONAL_INFORMATION"></span>**Informações adicionais**
</dt> <dd>

Observe que as contagens principais não precisam ser uma potência de dois, portanto, os jogos devem ser dimensionados linearmente e lidar com contagens de núcleos de 3, 4, 5, 6, 7, 8 e assim por diante.

O dimensionamento aumentando o número de threads em um aplicativo só fornecerá um retorno se o custo de comunicação e a sincronização de threads forem mantidos na verificação. O dimensionamento baseado em recursos pode provar uma solução mais fácil em curto prazo, permitindo que o jogo opere normalmente sem os threads adicionais em sistemas de núcleo único e habilitá-los quando a capacidade adicional da CPU estiver disponível.

para obter mais informações, consulte [codificação para vários núcleos no xbox 360 e microsoft Windows](/windows/desktop/DxTechArts/coding-for-multiple-cores) e [considerações de programação de bloqueio para o xbox 360 e o microsoft Windows](/windows/desktop/DxTechArts/lockless-programming) nos artigos do DirectX, bem como o utilitário DXUTLockFreePipe e o exemplo CoreDetection.

O uso da criação de recursos com thread livre do Direct3D 11 e contextos de dispositivo é útil na obtenção de escalabilidade de muitos núcleos na renderização e no carregamento de recursos gráficos. confira jogos para Windows Showcase S. 1.

observe que usar o rdtsc de instruções de CPU diretamente, em vez de usar Windows APIs para calcular o tempo em sistemas de vários núcleos, pode causar problemas em algumas configurações de hardware e de sistema operacional; consulte os [processadores de tempo de jogo e vários núcleos](/windows/desktop/DxTechArts/game-timing-and-multicore-processors) nos artigos do DirectX.

</dd> </dl>

### <a name="s4-support-games-for-windows---live"></a>S. 4 suporte a jogos para Windows-LIVE

os jogos para Windows-LIVE não são mais suportados pela Microsoft.

### <a name="s5-support-windows-touch"></a>S. 5 suporte a Windows Touch

<dl> <dt>

<span id="Requirement"></span><span id="requirement"></span><span id="REQUIREMENT"></span>**Obrigatoriedade**
</dt> <dd>

Windows jogos com capacidade de toque são reproduzidos usando toque e/ou gestos em computadores que executam o Windows 7 com uma tela de toque. A entrada de teclado também pode ser usada, mas a interface de execução primária deve ser baseada em toque.

Habilitar o Touch não deve impedir o uso do mouse ou do controlador comum, sujeito ao requisito técnico 1,4.

o instalador do jogo não deve dar suporte à funcionalidade de toque Windows.

</dd> <dt>

<span id="Rationale"></span><span id="rationale"></span><span id="RATIONALE"></span>**Lógica**
</dt> <dd>

os monitores compatíveis com vários toques para computadores estão disponíveis para laptops e desktops, e representam um recurso de hardware importante que está sendo promovido com o lançamento do Windows 7. o Windows 7 dá suporte a Windows toque em todas as interfaces de área de trabalho e controles comuns.

</dd> <dt>

<span id="Additional_Information"></span><span id="additional_information"></span><span id="ADDITIONAL_INFORMATION"></span>**Informações adicionais**
</dt> <dd>

Os aplicativos de código nativo podem acessar o multitoque por meio das mensagens do WM \_ Touch, em combinação com a função [**RegisterTouchWindow**](/windows/desktop/api/winuser/nf-winuser-registertouchwindow) . Veja também as manipulações e a API inércia.

o Windows Presentation Foundation (WPF) 4,0 fornece uma solução gerenciada para interfaces multitoque.

para obter mais informações, consulte o SDK do Windows Touch.

</dd> </dl>

### <a name="s6-support-high-color"></a>S. 6 suporte para alta cor

<dl> <dt>

<span id="Requirement"></span><span id="requirement"></span><span id="REQUIREMENT"></span>**Obrigatoriedade**
</dt> <dd>

Os jogos que suportam alta cor usam um formato 10:10:10:2 (DXGI \_ \_ R10G10B10A2, D3DFMT \_ A2B10G10R10) ou 16:16:16:16 ( \_ formato dxgi \_ R16G16B16A16, D3DFMT \_ A16B16G16R16) para o modo de exibição de buffer de fundo e de tela inteira.

Usando um destino de renderização de alta cor, o conteúdo do intervalo de High-Dynamic (HDR) pode ser renderizado com uma gama estendida ou larga ao executar o mapeamento de Tom para um intervalo de 10 ou 16 bits.

</dd> <dt>

<span id="Rationale"></span><span id="rationale"></span><span id="RATIONALE"></span>**Lógica**
</dt> <dd>

Os monitores têm sido capazes de exibir mais de 256 níveis de cor por canal por muitos anos, mesmo quando os monitores CRT eram predominantes. O hardware de digitalização em placas de vídeo tem sido o fator limitante. As GPUs modernas, incluindo a maioria dos hardwares de classe Direct3D 9 e todos os hardwares de classe Direct3D 10 e melhores, têm hardware de varredura com capacidade de pelo menos 10 bits por canal, e a capacidade de hardware é definida para aumentar para 16 bits por canal de cor no futuro. Os sistemas de interconexão de TV de HD (HDMI, DisplayPort) foram projetados para lidar com mais de 8 bits por canal também, e o VGA analógico já terá esses sinais.

</dd> <dt>

<span id="Additional_Information"></span><span id="additional_information"></span><span id="ADDITIONAL_INFORMATION"></span>**Informações adicionais**
</dt> <dd>

Observe que High Color ou Hi Color, historicamente refere-se à mudança de cores de 256 (8 bits) para monitores de cores de 15 ou 16 bits. A maioria dos sistemas de vídeo tem tempo desde que foi movida para uma cor verdadeira, que é de 24 bits ou 8 bits por canal de cor para vermelho, verde e azul. Por alta cor aqui, queremos dizer uma nova geração de sistemas de exibição que podem operar com mais de 8 bits por canal de cor individual. O também é conhecido como cor profunda.

</dd> </dl>

### <a name="recommended-best-practices"></a>Práticas recomendadas

### <a name="introduction"></a>Introdução

além de atender aos requisitos técnicos e adotar um ou mais casos no seu título, há uma série de práticas recomendadas que devem ser seguidas para todos os jogos de Windows. embora essas recomendações fiquem fora do escopo dos principais requisitos técnicos, você é altamente incentivado a empregar para todos os jogos de Windows títulos.

### <a name="additional-recommendations"></a>Recomendações adicionais

-   Use o compilador de Visual Studio mais recente e o tempo de execução. As versões mais recentes do compilador implementam melhorias significativas para a qualidade do código gerado e para problemas de segurança e empregam estratégias de otimização do processador modernas. Atualizar o compilador e usar o tempo de execução C mais recente é uma maneira fácil de migrar para as práticas de codificação modernas.
-   Use a versão da DLL (biblioteca de vínculo dinâmico) do tempo de execução C, em vez da vinculação estática, e faça uso do CRT seguro. (As exceções podem ser feitas em casos de pré-instalação especiais, como para um programa de execução automática ou para o próprio instalador).
-   Para áudio de jogos, use XAudio2, X3DAudio e/ou transação, em vez de DirectSound. para mecanismos de áudio que fazem toda a combinação e conversão de taxa de origem e precisam apenas de uma solução de baixa latência para saída de áudio, use o DirectSound no Windows XP (somente) e WASAPI no Windows Vista e no Windows 7.
-   Evite usar APIs herdadas e preteridas: DirectDraw, DirectSound, DirectPlay, camada de desempenho do DirectMusic, o DirectPlay Voice e o modo retido do Direct3D. observe que o modo retidos de voz e Direct3D do DirectPlay não estão disponíveis no Windows Vista ou Windows 7. A camada de desempenho do DirectPlay e do DirectMusic não está disponível para aplicativos nativos x64.
-   Otimizar usando conjuntos de instruções SSE/SSE2 SIMD. consulte a API do [DirectXMath](/windows/desktop/dxmath/directxmath-portal) no SDK do Windows como uma solução de plataforma cruzada para operações matemáticas com otimização de SIMD.
-   Use as práticas recomendadas modernas para Windows segurança (incluindo opções de compilador e vinculador, como **/NXCOMPAT**, **/gs**, **/SAFESEH**, **/DYNAMICBASE**, **/SDL** e assim por diante). Para obter mais informações, consulte [práticas recomendadas de segurança no desenvolvimento de jogos](/windows/desktop/DxTechArts/best-security-practices-in-game-development).
-   Use os componentes e as bibliotecas mais recentes do SDK do Windows. Remova dependências do DirectSetup herdado implantado componentes fora de banda, como D3DX9, D3DX10 e D3DX11. Considere o uso de [DirectXTex](https://github.com/Microsoft/DirectXTex) ou [DirectXTK](https://github.com/Microsoft/DirectXTK) ou ambos.
-   Evite usar o compilador HLSL mais antigo e, em vez disso, use o compilador moderno do HLSL. Se o suporte para o sombreador de pixel 1. x for exigido pelo seu aplicativo, use o assembly de sombreador em vez de HLSL ou limite o uso do compilador mais antigo apenas para esses cenários.

## <a name="resources"></a>Recursos



| Termo                                                                                                                                                                                                                         | Descrição                                                                                                                                                   |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="Games_for_Windows__Test_Cases__"></span><span id="games_for_windows__test_cases__"></span><span id="GAMES_FOR_WINDOWS__TEST_CASES__"></span>Jogos para Windows: Casos de Teste <br/>                              | Práticas recomendadas para jogos Windows XP, Windows Vista e Windows 7<br/>                                                                               |
| <span id="Windows_SDK__"></span><span id="windows_sdk__"></span><span id="WINDOWS_SDK__"></span>Windows Sdk <br/>                                                                                                      | [Windows Sdks](https://msdn.microsoft.com/bb980924.aspx)<br/>                                                                                      |
| <span id="User_Account_Control_Guidelines__"></span><span id="user_account_control_guidelines__"></span><span id="USER_ACCOUNT_CONTROL_GUIDELINES__"></span>Diretrizes de controle de conta de usuário <br/>                      | [Windows Requisitos de desenvolvimento de aplicativo vista para compatibilidade de controle de conta de usuário](/previous-versions/dotnet/articles/bb530410(v=msdn.10))<br/> |
| <span id="WinQual_Developer_Portal__"></span><span id="winqual_developer_portal__"></span><span id="WINQUAL_DEVELOPER_PORTAL__"></span>WinQual Portal do Desenvolvedor <br/>                                                  | [Windows Quality Online Services (Winqual)](/windows-hardware/drivers/dashboard/winqual-submission-tool--winqualexe-)<br/>                                                                         |
| <span id="DirectX_Developer_Portal__"></span><span id="directx_developer_portal__"></span><span id="DIRECTX_DEVELOPER_PORTAL__"></span>DirectX Portal do Desenvolvedor <br/>                                                  | [Central de Desenvolvedores do Directx](/previous-versions/windows/apps/hh452744(v=win.10))<br/>                                                                               |
| <span id="Games_for_Windows_and_DirectX_SDK_Blog"></span><span id="games_for_windows_and_directx_sdk_blog"></span><span id="GAMES_FOR_WINDOWS_AND_DIRECTX_SDK_BLOG"></span>Blog de jogos Windows sDK do DirectX e do Windows DirectX<br/> | [Jogos para Windows e SDK do DirectX](https://walbourn.github.io/)<br/>                                                                           |
| <span id="Additional_DirectX_Articles"></span><span id="additional_directx_articles"></span><span id="ADDITIONAL_DIRECTX_ARTICLES"></span>Artigos adicionais do DirectX<br/>                                             | [Artigos técnicos do DirectX](/windows/desktop/DxTechArts/dx9-technical-articles)<br/>                                                                                    |



 

 

