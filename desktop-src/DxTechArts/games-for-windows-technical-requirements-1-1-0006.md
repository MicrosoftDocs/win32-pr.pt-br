---
title: Melhores práticas dos requisitos técnicos de jogos para Windows no Windows XP, Windows Vista, Windows 7 e Windows 8
description: Este artigo fornece requisitos técnicos e práticas recomendadas para jogos que são executados no Windows.
ms.assetid: 8b816e9f-de68-cf84-1501-a9c36c6b75d8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 60c7a0f52685b0b99247ebfd86af3727d834ca63
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/30/2021
ms.locfileid: "113120301"
---
# <a name="games-for-windows-technical-requirements-best-practices-for-games-on-windows-xp-windows-vista-windows-7-and-windows-8"></a>Jogos para requisitos técnicos do Windows: práticas recomendadas para jogos no Windows XP, Windows Vista, Windows 7 e Windows 8

Este artigo fornece requisitos técnicos e práticas recomendadas para jogos que são executados no Windows. Nós escrevemos esses requisitos técnicos e as práticas recomendadas principalmente para abranger o Windows Vista e o Windows 7, bem como o sistema operacional herdado do Windows XP. Essas práticas recomendadas também se aplicam a jogos de desktop Win32 no Windows 8.

Este artigo contém estas seções:

-   [Diferenças para o Windows 8](#differences-for-windows-8)
    -   [Informações adicionais](#additional-information)
-   [Jogos para Windows](#games-for-windows-technical-requirements-best-practices-for-games-on-windows-xp-windows-vista-windows-7-and-windows-8)
    -   [Integração do explorador de jogos 1,1](#11-games-explorer-integration)
    -   [1,2 controles de segurança/pais da família de suporte](/windows)
    -   [1,3 suporte a jogos salvos avançados](#13-support-rich-saved-games)
    -   [1,4 suporte ao requisito condicional do controlador comum do Xbox 360 para Windows \[\]](#14-support-the-xbox-360-common-controller-for-windows-conditional-requirement)
    -   [1,5 suporte a várias taxas de proporção e resoluções](#15-support-multiple-aspect-ratios-and-resolutions)
    -   [Lançamento do suporte do 1,6 do Windows Media Center](#16-support-launch-from-windows-media-center)
    -   [Suporte do Direct3D 1,7](#17-direct3d-support)
    -   [1,8 habilitar reconhecimento de DPI alto](#18-enable-high-dpi-aware)
-   [Segurança e compatibilidade](#security-and-compatibility)
    -   [2,1 seguir as diretrizes de controle de conta de usuário](#21-follow-user-account-control-guidelines)
    -   [2,2 suporte a versões x64 do Windows](#22-support-windows-x64-versions)
    -   [2,3 assinar arquivos](#23-sign-files)
    -   [Drivers de assinatura 2,4](#24-sign-drivers)
    -   [2,5 executar a verificação de versão apropriada](#25-perform-proper-version-checking)
    -   [2,6 suporte a sessões de usuário simultâneas](#26-support-concurrent-user-sessions)
    -   [2,7 nomes longos de suporte](#27-support-long-names)
-   [Instalação](#32-support-user-account-control-for-installation)
    -   [3,1 suporte à instalação fácil](#31-support-easy-installation)
    -   [3,2 controle de conta de usuário de suporte para instalação](#32-support-user-account-control-for-installation)
    -   [3,3 instalar em pastas corretas](#33-install-to-correct-folders)
    -   [3,4 instalar recursos do Windows corretamente](#34-install-windows-resources-properly)
    -   [3,5 evitar reinicializações durante a instalação](#35-avoid-reboots-during-installation)
    -   [3,6 usar o controle de versão de arquivo corretamente](#36-use-file-versioning-correctly)
    -   [3,7 suporte a \[ requisito condicional de Autorun\]](#37-support-autorun-conditional-requirement)
-   [Confiabilidade](#reliability)
    -   [4,1 eliminar reinicializações desnecessárias](#41-eliminate-unnecessary-reboots)
    -   [4,2 eliminar falhas de Application Verifier](#42-eliminate-application-verifier-failures)
    -   [4,3 Relatório de Erros do Windows de suporte e informações de versão do arquivo](#43-support-windows-error-reporting-and-file-version-information)
-   [Terminologia do controlador comum do Xbox 360 para Windows](#xbox-360-common-controller-for-windows-terminology)
-   [Diretrizes para produtos de middleware de jogos](#guidelines-for-game-middleware-products)
    -   [Introdução](#introduction)
    -   [Recomendações adicionais](#additional-recommendations)
    -   [Jogos para o Windows demonstrativos](#games-for-windows-showcases)
-   [Recursos](#resources)

## <a name="differences-for-windows-8"></a>Diferenças para o Windows 8

Aqui está um resumo das principais diferenças ao aplicar esses requisitos técnicos e práticas recomendadas ao Windows 8.

<dl> <dt>

<span id="The_Games_Explorer_UI_is_not_visible"></span><span id="the_games_explorer_ui_is_not_visible"></span><span id="THE_GAMES_EXPLORER_UI_IS_NOT_VISIBLE"></span>**A interface do usuário do explorador de jogos não está visível**
</dt> <dd>

Todos os jogos que você registra com o [Explorador de jogos](/previous-versions/windows/desktop/legacy/hh437965(v=vs.85)) são exibidos como blocos na nova interface do usuário do Windows, mas grande parte dos metadados associados ao título não é mais visível. Você ainda usa a ferramenta criador de arquivos de definição de jogos (GDFMAKER.EXE), que agora está disponível no SDK (Software Development Kit) do Windows para criar os metadados. Você também usa os mecanismos existentes para implantar os metadados. Continue testando o registro do explorador de jogos usando o Windows 7 e verifique se o novo bloco da interface do usuário do Windows aparece quando você o instala no Windows 8 (consulte a [integração do explorador de 1,1 jogos](#11-games-explorer-integration)).

Para baixar o SDK do Windows 8, consulte [downloads para desenvolvimento de aplicativos da área de trabalho](https://msdn.microsoft.com/windows/desktop/aa904949).

</dd> <dt>

<span id="Registration_with_the_Game_Explorer_APIs_continues_to_be_the_mechanism_for_registering_your_game_with_Windows_Parental_Controls"></span><span id="registration_with_the_game_explorer_apis_continues_to_be_the_mechanism_for_registering_your_game_with_windows_parental_controls"></span><span id="REGISTRATION_WITH_THE_GAME_EXPLORER_APIS_CONTINUES_TO_BE_THE_MECHANISM_FOR_REGISTERING_YOUR_GAME_WITH_WINDOWS_PARENTAL_CONTROLS"></span>**O registro com as APIs do Gerenciador de jogos continua sendo o mecanismo para registrar seu jogo com controles dos pais do Windows**
</dt> <dd>

Recomendamos que você execute a versão SDK do Windows do GDFMAKER na versão de lançamento do Windows 8 para garantir que ele possa preencher todos os sistemas de classificação com suporte no momento.

> [!Note]  
> Esta versão do GDFMAKER requer o .NET 4,0.

 

Consulte [segurança/controles dos pais da família de suporte do 1,2](/windows).

</dd> <dt>

<span id="There_are_now_three_choices_for_using_the_XINPUT_API_depending_on_your_requirements"></span><span id="there_are_now_three_choices_for_using_the_xinput_api_depending_on_your_requirements"></span><span id="THERE_ARE_NOW_THREE_CHOICES_FOR_USING_THE_XINPUT_API_DEPENDING_ON_YOUR_REQUIREMENTS"></span>**Agora há três opções para usar a API XINPUT dependendo de seus requisitos**
</dt> <dd>

O XINPUT 1,4 é integrado ao Windows 8. Os aplicativos da Windows Store e os aplicativos Win32 da área de trabalho podem usar o XINPUT 1,4. Todas as versões do Windows podem usar XINPUT 9.1.0 para controladores comuns simplificados, mas não há nenhum pacote de redistribuição com XINPUT 9.1.0. Todas as versões do Windows também podem usar o SDK do DirectX existente versão XINPUT 1,3, que exige que o DirectSetup seja implantado.

Consulte [1,4 suporte ao controlador comum do Xbox 360 para Windows](#14-support-the-xbox-360-common-controller-for-windows-conditional-requirement).

</dd> <dt>

<span id="Only_a_limited_set_of_desktop_Win32_apps_are_supported_on_"></span><span id="only_a_limited_set_of_desktop_win32_apps_are_supported_on_"></span><span id="ONLY_A_LIMITED_SET_OF_DESKTOP_WIN32_APPS_ARE_SUPPORTED_ON_"></span>**Há suporte apenas para um conjunto limitado de aplicativos Win32 da área de trabalho no Windows RT**
</dt> <dd>

Os jogos executados no Windows 7 podem e devem ser executados corretamente em plataformas Windows 8 x86 e x64.

Consulte [suporte a 2,2 versões do Windows x64](#22-support-windows-x64-versions).

</dd> <dt>

<span id="Ensure_any_OS_checks_are_done_correctly"></span><span id="ensure_any_os_checks_are_done_correctly"></span><span id="ENSURE_ANY_OS_CHECKS_ARE_DONE_CORRECTLY"></span>**Certifique-se de que todas as verificações do sistema operacional sejam feitas corretamente**
</dt> <dd>

A versão do sistema operacional Windows 8 é 6,2. O Windows 8 passa os testes de barra mínimos atuais que recomendamos para a implantação de jogos.

</dd> <dt>

<span id="The__DirectX_End-User_Redistribution__package_runs_successfully_on_Windows_8__as_it_does_on_Windows_7__to_deploy_D3DX9__D3DX10__D3DX11__XINPUT_1.3__XAUDIO_2.7__XACTEngine__and_so_on"></span><span id="the__directx_end-user_redistribution__package_runs_successfully_on_windows_8__as_it_does_on_windows_7__to_deploy_d3dx9__d3dx10__d3dx11__xinput_1.3__xaudio_2.7__xactengine__and_so_on"></span><span id="THE__DIRECTX_END-USER_REDISTRIBUTION__PACKAGE_RUNS_SUCCESSFULLY_ON_WINDOWS_8__AS_IT_DOES_ON_WINDOWS_7__TO_DEPLOY_D3DX9__D3DX10__D3DX11__XINPUT_1.3__XAUDIO_2.7__XACTENGINE__AND_SO_ON"></span>**O pacote de redistribuição do DirectX End-User é executado com êxito no Windows 8, como faz no Windows 7, para implantar D3DX9, D3DX10, D3DX11, XINPUT 1,3, XAUDIO 2,7, XACTEngine e assim por diante**
</dt> <dd>

Mas existe um problema conhecido com o DirectSetup em sistemas com apenas o .NET 4,0 instalado devido à manipulação de implantação dos assemblies DirectX 1,1 gerenciados herdados. Esse problema se aplica ao Windows 8, que vem com o .NET 4,5 por padrão, e os novos computadores com Windows XP com o tempo de execução do .NET 4,0 instalado. Mas esse problema não se aplica a nenhuma versão do .NET anterior ao .NET 4,0. Embora o Windows 8 tenha um comportamento de compatibilidade de aplicativos para resolver esse problema automaticamente (o que exige acesso à rede), recomendamos que os jogos que continuam a implantar a atualização do DirectSetup na versão atualizada do SDK do DirectX (junho de 2010) dos arquivos Redist. Como sempre, se você usar DirectSetup para seu título, corte o título para baixo até o conjunto mínimo necessário de CABs.

Consulte [3,4 instalar recursos do Windows corretamente](#34-install-windows-resources-properly).

</dd> <dt>

<span id="Games_that_require_the_.NET__2.0__compatible_runtime__2.0__3.0__3.5__continue_to_use_existing_deployment_mechanisms"></span><span id="games_that_require_the_.net__2.0__compatible_runtime__2.0__3.0__3.5__continue_to_use_existing_deployment_mechanisms"></span><span id="GAMES_THAT_REQUIRE_THE_.NET__2.0__COMPATIBLE_RUNTIME__2.0__3.0__3.5__CONTINUE_TO_USE_EXISTING_DEPLOYMENT_MECHANISMS"></span>**Jogos que exigem o tempo de execução compatível com o .NET 2,0 (2,0, 3,0, 3,5) continuam a usar mecanismos de implantação existentes**
</dt> <dd>

Esses jogos disparam um comportamento de compatibilidade de aplicativos no Windows 8 para habilitar o tempo de execução do .NET 3,5 automaticamente (o que requer acesso à rede). Mas, recomendamos que os desenvolvedores do .NET se movam para o tempo de execução do .NET 4,0.

> [!Note]  
> Os assemblies do DirectX 1,1 gerenciados herdados não são compatíveis com o tempo de execução do .NET 4. x.

 

Consulte [3,4 instalar recursos do Windows corretamente](#34-install-windows-resources-properly).

</dd> <dt>

<span id="Use_of_an__autorunner__or_other_pre-install_technology_that_relies_on_.NET_is_not_recommended"></span><span id="use_of_an__autorunner__or_other_pre-install_technology_that_relies_on_.net_is_not_recommended"></span><span id="USE_OF_AN__AUTORUNNER__OR_OTHER_PRE-INSTALL_TECHNOLOGY_THAT_RELIES_ON_.NET_IS_NOT_RECOMMENDED"></span>**O uso de um autorunner ou de outra tecnologia de pré-instalação que se baseia no .NET não é recomendado**
</dt> <dd>

Você pode pressupor que somente os tempos de execução compatíveis com .NET 2,0 (2,0, 3,0, 3,5) estão presentes no Windows Vista e no Windows 7. Somente o tempo de execução compatível com o .NET 4,0 está presente no Windows 8 por padrão.

Consulte [suporte para autorun do 3,7](#37-support-autorun-conditional-requirement).

</dd> <dt>

<span id="There_is_an_updated_Application_Verifier_for_Windows_8"></span><span id="there_is_an_updated_application_verifier_for_windows_8"></span><span id="THERE_IS_AN_UPDATED_APPLICATION_VERIFIER_FOR_WINDOWS_8"></span>**Há uma Application Verifier atualizada para o Windows 8**
</dt> <dd>

O SDK do Windows 8 inclui esse Application Verifier atualizado.

Consulte [4,2 eliminar falhas de Application Verifier](#42-eliminate-application-verifier-failures).

</dd> </dl>

### <a name="additional-information"></a>Informações adicionais

<dl>

[Manual de compatibilidade do Windows 8 e do Windows Server 2012](/windows/desktop/w8cookbook/windows-8-and-windows-server-8-compatibility-cookbook-portal)  
[Onde está o SDK do DirectX?](/windows/desktop/directx-sdk--august-2009-)  
</dl>

## <a name="games-for-windows"></a>Jogos para Windows

**Resumo dos requisitos de jogos**

**Benefícios do cliente**

Jogos de computador são uma experiência de entretenimento importante no Windows, mas preocupações com a facilidade de uso causaram a frustração do cliente ao longo dos anos. Tradicionalmente, os jogos são instalados como aplicativos, mas são utilizados mais como mídia de entretenimento (filmes ou músicas, por exemplo). Inovações, como o explorador de jogos, expõem jogos de maneira consistente que é diferente dos aplicativos padrão. Essas inovações também dão aos jogos o status do cidadão de primeira classe no Windows, junto com músicas e imagens. Os requisitos a seguir ajudam a garantir que o Windows Vista e o Windows 7 forneçam uma experiência de jogos melhorada, mais acessível e unificada. Ao mesmo tempo, eles garantem a compatibilidade com o Windows XP.

### <a name="11-games-explorer-integration"></a>Integração do explorador de jogos 1,1

<dl> <dt>

<span id="Requirement"></span><span id="requirement"></span><span id="REQUIREMENT"></span>**Obrigatoriedade**
</dt> <dd>

O jogo deve estar visível no explorador de jogos (a pasta **jogos** ) no Windows Vista e no Windows 7. Quando selecionado, o jogo também deve exibir metadados corretos, que incluem Publicador, desenvolvedor, data de lançamento, versão, pontuações do índice de experiência do Windows, classificação (se aplicável) e hiperlinks associados.

Se o jogo for distribuído digitalmente por meio de um serviço de jogo online, o provedor de serviços também deverá aparecer no explorador de jogos. Para garantir o tratamento adequado do provedor e habilitar o uso de RSS feeds, a versão 2 do esquema para GDFs (arquivos de definição de jogo) deve ser usada. (Para obter mais informações sobre GDFs, consulte informações adicionais.)

Além disso, os instaladores de jogos devem observar as seguintes regras ao serem executados no Windows Vista e no Windows 7:

-   A instalação não deve criar um atalho para iniciar o jogo na área de trabalho, no menu iniciar ou em qualquer outro local.
-   Tarefas e atalhos para remoção não devem ser criados.
-   Os usuários devem ser capazes de remover o jogo usando programas e recursos no painel de controle no Windows Vista e no Windows 7, ou adicionar ou remover programas no painel de controle no Windows XP.

No Windows XP e nas versões anteriores do Windows, o instalador de jogos é gratuito para criar grupos de programas, ícones da área de trabalho ou atalhos, conforme necessário.

</dd> <dt>

<span id="Rationale"></span><span id="rationale"></span><span id="RATIONALE"></span>**Lógica**
</dt> <dd>

O explorador de jogos do Windows é semelhante em conceito às pastas **meus documentos** do Windows XP ou **minhas imagens**. A ideia é centralizar o conteúdo semelhante em um único local e permitir atividades mais fáceis e sensíveis ao contexto. O explorador de jogos estende o conceito **meus documentos** ou **minhas imagens** , permitindo uma organização mais rica e controle sobre jogos. O explorador de jogos permite que os jogadores exibam, organizem e interajam com todos os jogos instalados em seus sistemas. Ele também permite que os editores de jogos comuniquem informações importantes do jogo com mais eficiência. O sistema é controlado por dados, facilitando para um editor de jogos atualizar as informações do jogo durante a vida útil do produto.

</dd> <dt>

<span id="Additional_Information"></span><span id="additional_information"></span><span id="ADDITIONAL_INFORMATION"></span>**Informações adicionais**
</dt> <dd>

A integração com o explorador de jogos exige que você crie um arquivo de definição de jogo (GDF), que é um arquivo de texto XML que é inserido em um arquivo binário (um arquivo executável ou uma DLL) como um recurso, juntamente com um ícone do Windows. O jogo deve então ser registrado com o explorador de jogos. O GDF também permite a exposição de informações fornecidas, como o título do jogo, o editor, o desenvolvedor, links para sites e tarefas opcionais. Observe que as tarefas de suporte podem ser apenas links para sites da Web, mas as tarefas de reprodução também podem ser usadas para tarefas opcionais de suporte.

O explorador de jogos pode fazer uso de uma imagem de bitmap em miniatura, mas é recomendável que, em vez disso, você forneça um recurso de ícone do Windows com ícones grandes (256 256). O recurso de ícone deve incluir tamanhos de imagem de 256 256 48 48, 32 32 e 16 16 nas profundidades de cores de 24 bits (true color) e de 8 bits (256). O editor de ícone fornecido no Visual Studio 2008 e 2010 dá suporte a esses formatos de ícones grandes, assim como o IconWorkshop Lite.

Os detalhes sobre a integração com o **Explorador de jogos do Windows** são fornecidos no SDK do DirectX. O SDK do DirectX inclui um editor de GDF (arquivo de definição de jogo), bem como um GDF de exemplo que é incluído no GDFExampleBinary, um exemplo. Outro exemplo, GameUxInstallHelper, fornece rotinas para integrar a funcionalidade necessária aos sistemas de instalação existentes. O validador de arquivo de definição de jogo (gdftrace.exe) fornece suporte de depuração para avaliar um GDF. Consulte também "integração do explorador de jogos do Windows" na documentação do SDK do DirectX para C++.

O Windows 7 apresenta suporte para a segunda versão de um esquema para arquivos GDF. A nova versão inclui um método simplificado para criar tarefas de reprodução e suporte para notificações de atualização, provedores de serviço de jogos, estatísticas de jogos e RSS feeds para provedores de serviço de jogos. A versão mais recente do GameUxInstallHelper manipula todo o registro e o suporte herdado necessários para usar um arquivo GDF da versão 2 com o Windows Vista. Use as ferramentas e o código de exemplo do SDK do DirectX de agosto de 2009 ou posterior. É recomendável usar um arquivo GDF de versão 2 para habilitar o suporte para RSS feeds, estatísticas de jogos e notificações de atualização. Além disso, consulte os exemplos ProviderGDFExampleBinary e GameStatisticsExample.

No Windows Vista Business Edition, no Windows 7 Professional Edition e no Enterprise Edition do Windows Vista e do Windows 7, o link jogos no menu iniciar é ocultado. O explorador de jogos ainda está disponível no menu iniciar clicando em **todos os programas** e, em seguida, clicando em **jogos**.

Para aplicativos associados que são instalados com seu jogo, mas não em jogos, você tem a liberdade de criar grupos de programas de menu Iniciar, atalhos e ícones da área de trabalho em todas as versões do Windows, incluindo o Windows Vista e o Windows 7. Esses aplicativos associados devem passar nos Jogos aplicáveis para os requisitos do Windows; para obter detalhes, consulte [diretrizes para produtos de middleware de jogos](#guidelines-for-game-middleware-products). Os serviços de jogos são incentivados a se registrarem no explorador de jogos como um provedor de jogos para o Windows 7. 1

</dd> </dl>

### <a name="12-support-family-safety--parental-controls"></a>1,2 controles de segurança/pais da família de suporte

<dl> <dt>

<span id="Requirement"></span><span id="requirement"></span><span id="REQUIREMENT"></span>**Obrigatoriedade**
</dt> <dd>

Os jogos devem dar suporte total à segurança da família Windows ao aderir às seguintes regras:

-   Os jogos não devem exigir que o usuário tenha credenciais administrativas para reproduzir. A instalação, a aplicação de patches e a remoção podem exigir credenciais administrativas, sujeitas aos requisitos da seção 3. (Relacionado a isso é requisito 2,1, siga as diretrizes de controle de conta de usuário.)
-   Os jogos classificados por placas de classificação com suporte do Windows, como ESRB e PEGI, devem incluir suas informações de classificações atribuídas em seu GDF (arquivo de definição de jogo). Todos os dados de classificação disponíveis devem ser incluídos em todas as versões localizadas do GDF, bem como na versão neutra da linguagem.
-   Os jogos devem listar seus executáveis no GDF para fornecer uma boa experiência de usuário para restrições gerais de aplicativos, a menos que o jogo use uma tecnologia antipirataria que cria executáveis aleatoriamente nomeados em tempo de execução.
-   Os jogos devem chamar o método **VerifyAccess** da interface do explorador de jogos durante a inicialização, se disponível, e sair se retornar \* pfHasAccess como falso.

</dd> <dt>

<span id="Rationale"></span><span id="rationale"></span><span id="RATIONALE"></span>**Lógica**
</dt> <dd>

Todos os jogos devem ser executados dentro do contexto de uma conta de usuário padrão para permitir que contas controladas pelos controles dos pais do Windows reproduzam o jogo. Os pais desejam a capacidade de monitorar e controlar o acesso de seus filhos aos jogos. Além disso, vários grupos do setor, do governo e do advocacy desejam maneiras melhores de permitir que os pais monitorem e controlem os jogos nos quais seus filhos são expostos. Em conjunto com a arquitetura oferecida pelo explorador de jogos, a Microsoft fornece aos pais essa capacidade por meio de controles dos pais do Windows.

Mesmo para jogos que não participam de um programa de tabuleiro de classificação, exigir privilégios elevados cria uma experiência de reprodução ruim para a maioria das contas de usuário. Isso é particularmente o caso se os controles dos pais estiverem habilitados, o que exigiria que o pai entrasse na senha de administrador sempre que o jogo for iniciado.

O sistema de controles dos pais do Windows permite que os pais selecionem as classificações que elas acreditam que são apropriadas para seus filhos. Os controles dos pais dão suporte a muitos dos sistemas de classificação mundiais. Os controles dos pais também permitem que os pais restrinjam o acesso a jogos com base em descritores de conteúdo (se o sistema de classificação aplicável oferecer suporte a eles) e para permitir ou impedir o acesso a jogos individuais.

A opção padrão de sistema de classificação para controles dos pais do Windows é baseada na configuração de localidade do sistema, mas pode ser modificada pelo usuário em **Opções regionais e de idioma** no **painel de controle**. Portanto, cada idioma com suporte deve fornecer todos os dados de classificação disponíveis para que o usuário tenha a liberdade de selecionar qualquer quadro de classificação desejado.

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
<td>Os Service Packs do Windows Vista adicionam suporte para o seguinte:<br/>
<ul>
<li>GRB (Coreia do Sul)</li>
<li>&quot;Descritores de conteúdo de variante leve do ESRB &quot;</li>
</ul></td>
</tr>
<tr class="odd">
<td>Windows 7</td>
<td>O Windows 7 dá suporte aos sistemas de classificação com suporte do Windows Vista e adiciona suporte para o seguinte: <br/>
<ul>
<li>CSRR (Taiwan)</li>
</ul></td>
</tr>
<tr class="even">
<td>Windows 8</td>
<td>O Windows 8 dá suporte aos sistemas de classificação anteriores e adiciona suporte para o seguinte:<br/>
<ul>
<li>COB-AU (Austrália)</li>
<li>DJCTQ (Brasil)</li>
<li>PFB (África do Sul)</li>
<li>OFLC-NZ (Nova Zelândia)</li>
</ul>
Os rearos do Windows 8 suportam os seguintes sistemas preteridos agora:<br/>
<ul>
<li>PEGI-FI (Finlândia)</li>
<li>OFLC (Austrália)</li>
</ul></td>
</tr>
</tbody>
</table>



 

> [!Note]  
> Qualquer título que inclua novos descritores de conteúdo de ESRB do Windows Vista Service Pack 1 (SP1) mostrará como sem classificação no Windows Vista com um service pack.

 

Os dados de classificação mais recentes são ignorados em versões de sistemas operacionais sem suporte para eles. A variante PEGI (Finlândia) agora foi preterida em favor do sistema de classificação padrão PEGI (Europa). O sistema OFLC agora foi preterido em favor de COB-AU para Austrália.

Para obter mais informações sobre como tornar um jogo compatível com privilégios de usuário padrão, consulte o artigo DirectX [controle de conta de usuário para desenvolvedores de jogos](/windows/desktop/DxTechArts/user-account-control-for-game-developers).

Consulte o requisito 1,1 para obter mais detalhes sobre o arquivo de definição de jogo (GDF).

</dd> </dl>

### <a name="13-support-rich-saved-games"></a>1,3 suporte a jogos salvos avançados

\[Este requisito foi desativado\]

### <a name="14-support-the-xbox-360-common-controller-for-windows-conditional-requirement"></a>1,4 suporte ao requisito condicional do controlador comum do Xbox 360 para Windows \[\]

<dl> <dt>

<span id="Requirement"></span><span id="requirement"></span><span id="REQUIREMENT"></span>**Obrigatoriedade**
</dt> <dd>

Jogos que dão suporte a controladores de gamepad devem dar suporte ao controlador Xbox 360 para Windows usando a API [XInput](/windows/desktop/xinput/xinput-game-controller-apis-portal) . Se os periféricos do DirectInput também tiverem suporte, o DirectInput também poderá ser usado. No entanto, XInput deverá ser a API padrão se um dispositivo compatível com o Xbox 360 for usado.

Todas as referências a gatilhos e botões comuns do controlador devem usar os nomes do Xbox 360. Consulte a lista de [terminologia do controlador comum do Xbox 360 para Windows](#xbox-360-common-controller-for-windows-terminology) para obter detalhes.

A vibração do controlador deve ser desativada quando o jogo estiver em um estado de pausa ou suspenso.

O controle de mouse/teclado não pode ser totalmente desabilitado a qualquer momento. No mínimo, uma opção para retornar aos menus do jogo deve estar disponível.

</dd> <dt>

<span id="Rationale"></span><span id="rationale"></span><span id="RATIONALE"></span>**Lógica**
</dt> <dd>

Esse requisito faz com que os jogadores tenham liberdade de escolha para usar o controlador Xbox 360 ou o teclado e o mouse, dependendo de qual método de entrada é uma interface mais natural e intuitiva.

</dd> <dt>

<span id="Additional_Information"></span><span id="additional_information"></span><span id="ADDITIONAL_INFORMATION"></span>**Informações adicionais**
</dt> <dd>

Esse requisito não se aplica a jogos que usam apenas o mouse e/ou o teclado.

Recomendamos que a navegação do menu seja implementada para usar os botões do controlador padrão amplamente aceitos:

-   A-aceitar
-   B-cancelar
-   Iniciar-aceitar ou pausar
-   Back-Cancel, voltar uma tela ou um nível de menu acima

Para obter mais informações, consulte [XInput](/windows/desktop/xinput/xinput-game-controller-apis-portal).

O tópico [XInput e DirectInput](/windows/desktop/xinput/xinput-and-directinput) discute problemas com o uso de ambas as APIs ao mesmo tempo.

É recomendável que o DirectInput não seja usado para implementar controles de teclado ou mouse. Os controles de teclado e mouse só devem ser implementados usando mensagens do Windows e APIs do Win32. Para obter detalhes sobre como obter informações de movimentação de mouse de alta resolução sem usar o DirectInput, consulte [aproveitando High-Definition movimento do mouse](/windows/desktop/DxTechArts/taking-advantage-of-high-dpi-mouse-movement).

</dd> </dl>

### <a name="15-support-multiple-aspect-ratios-and-resolutions"></a>1,5 suporte a várias taxas de proporção e resoluções

<dl> <dt>

<span id="Requirement"></span><span id="requirement"></span><span id="REQUIREMENT"></span>**Obrigatoriedade**
</dt> <dd>

O jogo deve dar suporte a pelo menos as seguintes taxas de proporção e resoluções de tela associadas:

-   4:3 normal (800 600 ou 1024 768)
-   16:9 widescreen (1280 720)
-   16:10 widescreen (1152 720 ou 1680 1050 ou 800 480)

Para configuração e detecção de resolução de tela, o jogo deve aderir às seguintes regras:

-   O jogo usa a resolução de desktop do dispositivo de vídeo por padrão se for uma resolução com suporte. A taxa de proporção da área de trabalho deve ser usada como critério de pesquisa se o jogo escolher uma resolução padrão diferente.
-   O jogo deve solicitar que o usuário confirme as novas configurações de exibição quando uma alteração é feita. Se o usuário não aceitar dentro de 15 segundos, a exibição deverá reverter para a configuração anterior.
-   O jogo não deve alongar os pixels ou centralizar uma janela de renderização 4:3 para dar suporte a taxas de proporção widescreen. No entanto, o formato Letterbox é aceitável.

</dd> <dt>

<span id="Rationale"></span><span id="rationale"></span><span id="RATIONALE"></span>**Lógica**
</dt> <dd>

Com a área de trabalho 3D do Windows, uma taxa de proporção ou resolução específica não pode ser assumida, devido aos seguintes fatores:

-   Suporte para exibições de alto nível.
-   Maior participação no mercado de monitores widescreen.
-   Implantações de HDTV para o Windows Media Center.
-   Requisitos de acessibilidade.

</dd> <dt>

<span id="Additional_Information"></span><span id="additional_information"></span><span id="ADDITIONAL_INFORMATION"></span>**Informações adicionais**
</dt> <dd>

Idealmente, o jogo assume como padrão a taxa de proporção nativa da exibição. No entanto, a obtenção dessas informações de forma confiável pode ser um desafio, assim como uma solução mais geral, o jogo pode assumir que a área de trabalho está sendo executada na proporção de aspecto nativa. A resolução da área de trabalho pode ser obtida chamando [**EnumDisplaySettings**](/windows/desktop/api/winuser/nf-winuser-enumdisplaysettingsa) com \_ as configurações de enumeração do registro \_ .

Para obter mais detalhes, consulte as seções taxa de proporção e widescreen do artigo do DirectX [introdução à experiência de 10 pés para desenvolvedores de jogos do Windows](/windows/desktop/DxTechArts/introduction-to-the-10-foot-experience-for-windows-game-developers).

</dd> </dl>

### <a name="16-support-launch-from-windows-media-center"></a>Lançamento do suporte do 1,6 do Windows Media Center

\[Esse requisito foi desativado.\]

### <a name="17-direct3d-support"></a>Suporte do Direct3D 1,7

<dl> <dt>

<span id="Requirement"></span><span id="requirement"></span><span id="REQUIREMENT"></span>**Obrigatoriedade**
</dt> <dd>

Se o jogo usar o Direct3D, a versão mínima com suporte deverá ser o Direct3D 9 e o Direct3D deverá ser o renderizador padrão selecionado.

</dd> <dt>

<span id="Rationale"></span><span id="rationale"></span><span id="RATIONALE"></span>**Lógica**
</dt> <dd>

A arquitetura gráfica do Windows Vista e do Windows 7 Core foi projetada em todo o Direct3D. O Direct3D 8 e versões anteriores têm suporte ao remapear interfaces herdadas.

O uso de versões do Direct3D mais recentes do que o Direct3D 9 é altamente incentivado. Consulte os jogos para Windows Showcase S. 1. Exigir o Direct3D 10 ou o Direct3D 11 é totalmente compatível com o requisito 1,7.

</dd> </dl>

### <a name="18-enable-high-dpi-aware"></a>1,8 habilitar reconhecimento de DPI alto

<dl> <dt>

<span id="Requirement"></span><span id="requirement"></span><span id="REQUIREMENT"></span>**Obrigatoriedade**
</dt> <dd>

Os jogos e seus instaladores devem ser executados corretamente sem problemas visuais quando o dimensionamento de pontos por polegada (DPI) estiver habilitado (testado com 144 DPI para 150% de dimensionamento na resolução de vídeo de 1600 1200) no Windows Vista e no Windows 7.

Isso normalmente requer que o executável do jogo declare ser compatível com DPI. Isso é feito inserindo um elemento de manifesto: <dpiAware> true <dpiAware> .

</dd> <dt>

<span id="Rationale"></span><span id="rationale"></span><span id="RATIONALE"></span>**Lógica**
</dt> <dd>

Monitores LCD de alta qualidade são comuns à medida que o computador é exibido e eles parecem melhores quando controlados em suas resoluções nativas (geralmente 1280 1024, 1600 1200 e assim por diante). Os clientes que têm dificuldade de ler texto e ver as imagens nessa resolução geralmente definem suas áreas de trabalho de computador com uma resolução mais baixa e sofrem artefatos visuais do dimensionamento de LCD. Em vez disso, os clientes podem deixar a resolução no tamanho nativo e alterar o DPI da tela do Windows, tornando a aparência do item e do texto maior sem sacrificar a qualidade da imagem.

Embora esse recurso esteja disponível em algum formato desde o Windows XP, raramente é habilitado por clientes ou por OEMs. Mais da metade de todas as exibições de computador hoje estão definidas para uma resolução mais baixa do que a resolução nativa do monitor, com base nos comentários do cliente. O Windows 7 torna esse recurso muito mais visível para os clientes durante a configuração inicial e ao alterar as configurações de exibição, incentivando-os a usar o dimensionamento de DPI em vez de alterar a resolução da área de trabalho.

</dd> <dt>

<span id="Additional_Information"></span><span id="additional_information"></span><span id="ADDITIONAL_INFORMATION"></span>**Informações adicionais**
</dt> <dd>

Em vez disso, a função [**SetProcessDPIAware**](/windows/desktop/api/winuser/nf-winuser-setprocessdpiaware) pode ser usada, se chamada antecipada no código de inicialização do processo. A adição ao manifesto é preferida, para garantir que não haja nenhuma condição de corrida com elementos de software (como DLLs) que possam ser inicializados antes do ponto de entrada principal ser chamado. Observe que o **SetProcessDPIAware** está presente apenas no Windows Vista e no Windows 7.

Adicionar o elemento manifest é fácil de fazer com o Visual Studio 2005 e 2008; Crie um arquivo chamado dpiaware. manifest que contenha o seguinte texto:

``` syntax
            <assembly xmlns="urn:schemas-microsoft-com:asm.v1" manifestVersion="1.0" xmlns:asmv3="urn:schemas-microsoft-com:asm.v3">
            <asmv3:application>
            <asmv3:windowsSettings xmlns="http://schemas.microsoft.com/SMI/2005/WindowsSettings">
            <dpiAware>true</dpiAware>
            </asmv3:windowsSettings>
            </asmv3:application>
            </assembly>
```

Em seguida, dentro do Visual Studio, adicione dpiware. manifest ao projeto. Verifique se **Inserir manifesto** está definido como **Sim** nas propriedades do projeto. Observe que as versões mais antigas da ferramenta de manifesto (Mt.exe) irão gerar um aviso falso com os elementos de manifesto com reconhecimento de DPI. Para resolver isso, atualize Mt.exe para a versão mais recente do SDK do Windows.

O Visual Studio 2010 inclui uma configuração nas propriedades do projeto, denominada **habilitar reconhecimento de DPI**, que elimina a necessidade de um arquivo como dpiaware. manifest. Localize **habilitar reconhecimento de DPI** expandindo **as propriedades de configuração** e a **ferramenta de manifesto** e, em seguida, selecionando **entrada & saída**.

No Windows, o modo de exibição tradicional usa como padrão 96 DPI, que era comum para monitores CRT.

Enquanto os aplicativos de tela inteira alteram a resolução de vídeo, geralmente usam as mensagens e métricas da janela ao configurar buffers e exibir retângulos. A virtualização de DPI faz com que esses modos de exibição de tela inteira pareçam cortados e a declaração de reconhecimento de DPI irá impedir esses problemas. Para obter mais informações, consulte [escrevendo DPI-Aware aplicativos Win32](../hidpi/high-dpi-desktop-application-development-on-windows.md).

</dd> </dl>

## <a name="security-and-compatibility"></a>Segurança e compatibilidade

**Resumo dos requisitos de segurança e compatibilidade**

**Benefícios do cliente**

Os requisitos a seguir melhoram a segurança geral dos jogos e ajudam a garantir que eles funcionem com o Windows em diferentes arquiteturas, em configurações diferentes e em modos diferentes.

### <a name="21-follow-user-account-control-guidelines"></a>2.1 Seguir as diretrizes de controle de conta de usuário

<dl> <dt>

<span id="Requirement"></span><span id="requirement"></span><span id="REQUIREMENT"></span>**Exigência**
</dt> <dd>

Cada arquivo executável (ou seja, cada arquivo que tem uma extensão .exe) deve conter um manifesto inserido que define seu nível de execução incluindo a seguinte marca:

``` syntax
            <requestedExecutionLevel>
```

De acordo com o requisito 1.2, o jogo principal e o executável de execução automática devem ter o nível de execução asInvoker para dar suporte a contextos de Usuário Padrão.

Os arquivos de dados do usuário que têm associações de arquivo registradas com **Explorador de Arquivos** devem ser colocados em uma subpasta da pasta especificada pelo CSIDL PERSONAL (também chamado de Documentos \_ ou **Meus Documentos**).  Todos os outros arquivos de dados de usuário devem ser armazenados em uma subpasta das pastas especificadas por CSIDL \_ LOCAL \_ APPDATA ou CSIDL \_ COMMON \_ APPDATA. (Esses diretórios são ocultos por padrão para usuários individuais e para todos os usuários.)

</dd> <dt>

<span id="Rationale"></span><span id="rationale"></span><span id="RATIONALE"></span>**Lógica**
</dt> <dd>

A experiência do Windows de um usuário é mais segura se os aplicativos são executados somente com as permissões necessárias.

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

### <a name="22-support-windows-x64-versions"></a>2.2 Suporte a versões do Windows x64

<dl> <dt>

<span id="Requirement"></span><span id="requirement"></span><span id="REQUIREMENT"></span>**Exigência**
</dt> <dd>

Para manter a compatibilidade com edições de 64 bits do Windows, os jogos devem atender aos requisitos a seguir.

-   Os títulos e instaladores de título não devem conter nenhum código de 16 bits nem depender de nenhum componente de 16 bits.
-   Se o jogo for dependente de drivers de modo kernel para operação, as versões x64 desses drivers deverão estar disponíveis. A configuração do jogo deve detectar e instalar os drivers e componentes adequados para as edições de 64 bits do Windows.

</dd> <dt>

<span id="Rationale"></span><span id="rationale"></span><span id="RATIONALE"></span>**Lógica**
</dt> <dd>

Muitos usuários do Windows Vista e do Windows 7 executarão edições de 64 bits do sistema operacional ao longo da vida útil do produto, portanto, é crucial que os aplicativos sejam compatíveis com esse sistema operacional.

</dd> <dt>

<span id="Additional_Information"></span><span id="additional_information"></span><span id="ADDITIONAL_INFORMATION"></span>**Informações adicionais**
</dt> <dd>

O Windows no Windows 64 (WOW64) permite que o código de 32 bits seja executado em edições de 64 bits do Windows, portanto, não é necessário que o aplicativo seja um código nativo de 64 bits em edições de 64 bits do Windows. O código de 16 bits não é executado em edições de 64 bits do Windows.

Manter a compatibilidade com o Windows XP Professional x64 Edition não é necessário, mas é fortemente incentivado.

Para obter detalhes, consulte [Programação de 64 bits para desenvolvedores de jogos.](/windows/desktop/DxTechArts/sixty-four-bit-programming-for-game-developers)

</dd> </dl>

### <a name="23-sign-files"></a>2.3 Assinar arquivos

<dl> <dt>

<span id="Requirement"></span><span id="requirement"></span><span id="REQUIREMENT"></span>**Exigência**
</dt> <dd>

Todos os arquivos de código executáveis (normalmente, arquivos com a extensão .exe ou .dll) devem ser assinados com um certificado Authenticode válido publicamente e devem ter uma URL de servidor de data/hora válida para assinatura de produção.

Se o jogo usar Windows Installer, os arquivos de pacote do instalador (arquivos .msi) deverão ser assinados.

</dd> <dt>

<span id="Rationale"></span><span id="rationale"></span><span id="RATIONALE"></span>**Lógica**
</dt> <dd>

A assinatura de um arquivo ajuda os usuários a decidir se confiam em um aplicativo e garante que os arquivos não foram adulterados. Ele também permite que os aplicativos executem corretamente em ambientes bloqueados.

</dd> <dt>

<span id="Additional_Information"></span><span id="additional_information"></span><span id="ADDITIONAL_INFORMATION"></span>**Informações adicionais**
</dt> <dd>

Para obter detalhes, consulte [Autenticação authenticode para desenvolvedores de jogos.](/windows/desktop/DxTechArts/authenticode-signing-for-game-developers)

Se o jogo usar Windows Installer, recomendamos que você habilita a adoção de patch UAC/LUA, incluindo uma tabela MsiPatchCertificate. Para obter mais informações, consulte [UAC (Controle de Conta de Usuário).](/windows/desktop/Msi/user-account-control--uac--patching)

Não recomendamos assinar arquivos de gabinete (.cab), a menos que sejam relativamente pequenos (menos de 100 MB).

</dd> </dl>

### <a name="24-sign-drivers"></a>2.4 Assinar Drivers

<dl> <dt>

<span id="Requirement"></span><span id="requirement"></span><span id="REQUIREMENT"></span>**Exigência**
</dt> <dd>

Qualquer driver de modo kernel instalado pelo jogo deve ser assinado com um certificado Authenticode válido publicamente.

Qualquer driver de dispositivo de hardware no modo kernel instalado pelo jogo deve ter uma assinatura da Microsoft, que pode ser obtida do WHQL (Windows Hardware Quality Labs) ou do programa DRS (Assinatura de Confiabilidade do Driver).

</dd> <dt>

<span id="Rationale"></span><span id="rationale"></span><span id="RATIONALE"></span>**Lógica**
</dt> <dd>

Drivers mal escritos ou malware podem afetar gravemente a estabilidade e a segurança de um sistema. Em edições de 64 bits do Windows Vista e do Windows 7, os drivers não assinados não são carregados. Essa política também pode ser habilitada para edições de 32 bits do Windows Vista e do Windows 7.

</dd> <dt>

<span id="Additional_Information"></span><span id="additional_information"></span><span id="ADDITIONAL_INFORMATION"></span>**Informações adicionais**
</dt> <dd>

As versões nativas de 32 e 64 bits de todos os drivers de modo kernel são necessárias de acordo com o requisito 2.2.

Mais informações sobre programas de assinatura de driver da Microsoft podem ser encontradas no [portal do Desenvolvedor de Hardware do Windows](https://www.microsoft.com/whdc/winlogo/hwrequirements.mspx).

</dd> </dl>

### <a name="25-perform-proper-version-checking"></a>2.5 Executar verificação de versão adequada

<dl> <dt>

<span id="Requirement"></span><span id="requirement"></span><span id="REQUIREMENT"></span>**Exigência**
</dt> <dd>

Os jogos não devem falhar ao ser executados em sistemas operacionais futuros, conforme indicado pelas alterações no número de versão do Windows, a menos que o Contrato de Licença do Usuário Final proíbe o uso em sistemas operacionais futuros. Se o jogo tiver que falhar, ele deverá fazer isso normalmente exibindo uma mensagem apropriada para o usuário.

Se as verificações de versão do Windows são feitas, as APIs de verificação de versão ([**GetVersionEx**](/windows/desktop/api/sysinfoapi/nf-sysinfoapi-getversionexa) ou [**VerifyVersionInfo**](/windows/desktop/api/winbase/nf-winbase-verifyversioninfoa)) devem ser usadas para verificar a versão do sistema operacional. As chaves do Registro não devem ser lidas para determinar a versão.

Verificações explícitas de versão para o runtime do DirectX não devem estar presentes no jogo. Essas verificações de versão não devem estar presentes na instalação que inicia a instalação do runtime do DirectX (DirectSetup).

</dd> <dt>

<span id="Rationale"></span><span id="rationale"></span><span id="RATIONALE"></span>**Lógica**
</dt> <dd>

Quando os usuários do Windows atualizam seus sistemas operacionais, eles não devem ser impedidos de jogar jogos atuais simplesmente porque o número de versão do Windows aumentou. Os verificadores de versão mal escritos continuam a criar problemas para softwares que, caso contrário, funcionam bem em versões mais recentes do Windows ou simplesmente com a adição de um windows service pack.

A lógica de comparação de verificação de versão frágil para o runtime do DirectX criou várias instalações com falha quando é executado em versões diferentes do Windows. O número de versão do DirectX se aplica somente aos componentes principais do sistema operacional. Ele não se aplica aos componentes do SDK do DirectX lado a lado que são usados por muitos jogos.

</dd> <dt>

<span id="Additional_Information"></span><span id="additional_information"></span><span id="ADDITIONAL_INFORMATION"></span>**Informações adicionais**
</dt> <dd>

É muito comum ver os instaladores verificarem se há uma versão mínima do sistema operacional. Essa verificação, no entanto, precisa ser feita com cuidado para garantir que ela teste para maior ou igual a, em vez de igualdade simples, assim, bloquear para uma versão específica do sistema operacional. Usar Application Verifier teste **HighVersionLie** é uma maneira rápida e fácil de determinar como o instalador reagirá a uma alteração significativa no número de versão do sistema operacional.

O uso adequado do pacote de redistribuição de runtime do DirectX (Instalação do DirectX) envolve sempre inove-o durante a instalação, preferencialmente no modo silencioso. Isso permite que o código fornecido pela Microsoft execute as atualizações de versão necessárias. Ele também permite a instalação de quaisquer componentes opcionais do SDK do DirectX lado a lado, como D3DX, XACT, MDX ou XInput.

Para ver as práticas recomendadas para implantar o runtime do DirectX, consulte [Instalação do DirectX para desenvolvedores de jogos.](/windows/desktop/DxTechArts/directx-setup-for-game-developers)

É recomendável que os jogos que dão suporte ao Windows XP verifiquem um nível de service pack de 2 ou superior, pois o Service Pack 2 (SP2) e o Service Pack 3 (SP3) fornecem melhorias significativas de segurança, um requisito simplificado de redistribuição do DirectX Runtime e uma implantação extremamente ampla. A maioria das tecnologias modernas da Microsoft que suportam o Windows XP exige SP2 ou SP3 (XAudio2, Jogos para Windows – LIVE e assim por diante).

</dd> </dl>

### <a name="26-support-concurrent-user-sessions"></a>2.6 Suporte a sessões de usuário simultâneas

<dl> <dt>

<span id="Requirement"></span><span id="requirement"></span><span id="REQUIREMENT"></span>**Exigência**
</dt> <dd>

Os jogos que dependem de gráficos 3D não precisam funcionar em uma conexão de área de trabalho remota, mas o usuário deve ser alertado quando o jogo falhar.

Os jogos devem dar suporte a cenários padrão de multitarefa do Windows aderindo às seguintes regras:

-   Os jogos não devem bloquear o uso de sessões de usuário simultâneas.
-   Um jogo deve ser executado em uma nova sessão de usuário quando ele já estiver em execução em outra sessão.
-   O som do jogo em uma sessão de usuário não deve ser ouvido quando outro usuário está ativo em uma sessão diferente.
-   Os jogos devem dar suporte à Troca Rápida de Usuários.
-   Os jogos não devem tentar desabilitar a alternação de tarefas padrão. Os jogos não devem desabilitar o atalho de teclado ALT+TAB. Os jogos têm permissão para desabilitar atalhos de teclado de acessibilidade, conforme descrito em [Desabilitando teclas de atalho em Jogos](/windows/desktop/DxTechArts/disabling-shortcut-keys-in-games).

</dd> <dt>

<span id="Rationale"></span><span id="rationale"></span><span id="RATIONALE"></span>**Lógica**
</dt> <dd>

Os usuários do Windows devem ser capazes de executar sessões simultâneas sem conflitos ou interrupções. Esse é um cenário comum para um computador Windows que é compartilhado por uma família, desamadas ou outras pessoas.

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

Nomes longos são definidos como aqueles que contêm os valores máximos definidos no SDK do Windows.

</dd> </dl>

## <a name="installation"></a>Instalação

**Resumo dos requisitos de segurança e compatibilidade**

**Benefícios do cliente**

Os clientes podem ter certeza de que os aplicativos serão instalados no Windows sem degradar o sistema operacional ou outros aplicativos se os aplicativos usarem métodos oficiais de distribuição de componentes do sistema. Uma experiência de instalação simplificada fornece uma experiência pronta para uso mais acessível e sem problemas para jogos.

### <a name="31-support-easy-installation"></a>3,1 suporte à instalação fácil

<dl> <dt>

<span id="Requirement"></span><span id="requirement"></span><span id="REQUIREMENT"></span>**Obrigatoriedade**
</dt> <dd>

Os jogos devem fornecer um caminho simplificado na interface do usuário de instalação implementando o seguinte:

-   Exibir um máximo de um prompt de EULA.
-   O caminho de instalação padrão deve ignorar todas as seleções para a instalação (como a pasta de instalação ou seleções de componentes), assumir as seleções padrão e, em seguida, executar o jogo ou o iniciador após a instalação bem-sucedida, sem prompts adicionais. Se desejar, uma opção de instalação personalizada pode ser fornecida para opções de configuração avançadas.
-   Instale todos os componentes necessários do sistema operacional (como os tempos de execução do DirectX e do Visual C) usando os pacotes de redistribuição da Microsoft corretos. A instalação deve ser executada silenciosamente, sem avisar e sem ser protegida por verificações de versão de componente.
-   Forneça a remoção por meio de **programas e recursos** no **painel de controle** para o aplicativo do jogo e os arquivos de trabalho gerados. É recomendável uma opção para excluir qualquer arquivo de dados criado pelo usuário. O processo de remoção deve garantir que todos os arquivos instalados sejam removidos e todas as configurações (por exemplo, entradas da lista de exceção do firewall e chaves do registro) sejam limpas. Os componentes redistribuídos do sistema operacional não devem ser removidos.
-   Se o jogo exigir exceções a serem adicionadas ao firewall do Windows, o processo de instalação poderá solicitar que o informe os usuários de que essa alteração é necessária. Esse prompt deve aparecer antes do início da instalação.

A instalação e a remoção podem exigir direitos administrativos. A aplicação de patch pode exigir a solicitação de credenciais administrativas, dependendo da frequência de atualização. A reprodução normal do jogo não deve exigir direitos administrativos, por requisito 2,1 Siga as diretrizes de controle de conta de usuário.

</dd> <dt>

<span id="Rationale"></span><span id="rationale"></span><span id="RATIONALE"></span>**Lógica**
</dt> <dd>

A fácil instalação é uma filosofia de desenvolvimento de jogos centrada no Windows projetada para simplificar e simplificar o processo, às vezes, entediante e confuso de instalar jogos em computadores que executam sistemas operacionais Windows. A instalação fácil é habilitada utilizando um conjunto de tecnologias e práticas recomendadas que reduzem a complexidade desnecessária e o risco percebido da instalação de jogos em computadores Windows.

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
-   [Aplicação de patch no software de jogos no Windows XP, no Windows Vista e no Windows 7](/windows/desktop/DxTechArts/patching-methods-in-windows-xp-and-vista)
-   [Práticas recomendadas de instalação para jogos online com vários participantes](/windows/desktop/DxTechArts/mmo-installation-best-practices)

> [!Note]  
> A remoção de arquivos de dados gerados específicos do usuário deve ser executada somente para o usuário atual e para locais de usuário compartilhados comuns. Não há uma maneira robusta de verificar o sistema para remover arquivos específicos do usuário para outros usuários, mesmo que a remoção exija credenciais administrativas.

 

</dd> </dl>

### <a name="32-support-user-account-control-for-installation"></a>3,2 controle de conta de usuário de suporte para instalação

<dl> <dt>

<span id="Requirement"></span><span id="requirement"></span><span id="REQUIREMENT"></span>**Obrigatoriedade**
</dt> <dd>

O instalador de jogos não deve pressupor que esteja em execução no mesmo contexto que o usuário. Os locais específicos do usuário serão diferentes do instalador e do Player até mesmo para sistemas de usuário único devido à elevação de credenciais do administrador. Portanto, quando um jogo é executado pela primeira vez, ele deve executar tarefas específicas do usuário, separadamente do processo de instalação.

A caixa de diálogo exceção do firewall do Windows não deve aparecer quando um usuário hospeda ou ingressa em um jogo com vários participantes. Qualquer configuração necessária deve ser feita no momento da instalação. As instruções de instalação devem informar ao usuário que essa operação ocorrerá como parte da configuração.

O instalador do jogo deve fornecer um manifesto incorporado que designa o nível de execução necessário, por requisito 2,1 Siga as diretrizes de controle de conta de usuário.

Se o jogo for iniciado pelo instalador após a conclusão da instalação, ele deverá ser iniciado no contexto do usuário original.

</dd> <dt>

<span id="Rationale"></span><span id="rationale"></span><span id="RATIONALE"></span>**Lógica**
</dt> <dd>

Uma das maiores alterações no sistema operacional Windows no Windows Vista é a adição do UAC (controle de conta de usuário), que executa aplicativos com privilégios reduzidos por padrão. Como resultado, os instaladores precisam gerenciar níveis de privilégio de acordo. O Windows 7 também faz uso extensivo do UAC. Embora o Windows 7 aprimore a experiência do usuário do UAC, os instaladores ainda devem atender aos mesmos requisitos do Windows Vista para funcionar corretamente, sem depender do comportamento potencialmente confuso de virtualização.

O UAC está ativo por padrão no Windows Vista e no Windows 7, e a grande maioria dos clientes (88% ou mais, com base nos comentários) deixa esse recurso habilitado.

</dd> <dt>

<span id="Additional_Information"></span><span id="additional_information"></span><span id="ADDITIONAL_INFORMATION"></span>**Informações adicionais**
</dt> <dd>

Para obter mais detalhes sobre como configurar o Firewall do Windows, consulte o artigo sobre o DirectX [Firewall do Windows para desenvolvedores de jogos](/windows/desktop/DxTechArts/games-and-firewalls) e o exemplo FirewallInstallHelper.

A inicialização padrão do jogo no final do processo de instalação falhará em atender ao último aspecto desse requisito se a instalação for iniciada por um usuário padrão e se o processo de instalação exigir privilégios administrativos (ou seja, solicitar credenciais de administrador). Ele também herda privilégios administrativos, o que é um risco de segurança potencial. Em vez disso, um carregador de inicialização da instalação deve iniciar o jogo depois de retornar de uma invocação bem-sucedida do instalador. Para obter mais informações, consulte o artigo da MSDN Magazine [ensinar seus aplicativos a brincar com o controle de conta de usuário do Windows Vista](/archive/msdn-magazine/2007/january/teach-your-apps-to-work-with-windows-vista-user-account-control).

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

### <a name="34-install-windows-resources-properly"></a>3,4 instalar recursos do Windows corretamente

<dl> <dt>

<span id="Requirement"></span><span id="requirement"></span><span id="REQUIREMENT"></span>**Obrigatoriedade**
</dt> <dd>

Os aplicativos não devem tentar instalar arquivos ou chaves do registro protegidos por Proteção de Recursos do Windows (WRP). Se o aplicativo exigir versões mais recentes dos componentes do sistema, ele deverá atualizar esses componentes usando um Microsoft Service Pack ou um pacote de instalação aprovado pela Microsoft que contenha o componente do sistema. Os componentes do sistema nunca devem ser reempacotados.

</dd> <dt>

<span id="Rationale"></span><span id="rationale"></span><span id="RATIONALE"></span>**Lógica**
</dt> <dd>

O Proteção de Recursos do Windows (WRP) foi projetado para garantir que os recursos protegidos do sistema sejam atualizados somente usando os mecanismos de instalação ou atualização aprovados pela Microsoft. A WRP melhora a confiabilidade do sistema, garantindo que os resultados de uma instalação sejam previsíveis.

</dd> <dt>

<span id="Additional_Information"></span><span id="additional_information"></span><span id="ADDITIONAL_INFORMATION"></span>**Informações adicionais**
</dt> <dd>

A WRP é a sucessora da proteção de arquivos do Windows, que protege a maioria dos componentes do sistema instalados na pasta do Windows. A WRP protege a maioria das chaves do registro que armazenam configurações para a criação de objetos COM. Ele também reserva certas pastas para uso exclusivo pelo sistema operacional. As tentativas de acessar recursos protegidos normalmente resultam em um erro de negação de acesso.

Para obter detalhes de práticas recomendadas quando o tempo de execução do DirectX é implantado com um jogo, consulte o artigo DirectX [instalação do DirectX para desenvolvedores de jogos](/windows/desktop/DxTechArts/directx-setup-for-game-developers).

</dd> </dl>

### <a name="35-avoid-reboots-during-installation"></a>3,5 evitar reinicializações durante a instalação

<dl> <dt>

<span id="Requirement"></span><span id="requirement"></span><span id="REQUIREMENT"></span>**Exigência**
</dt> <dd>

O instalador do jogo não deve supor que a instalação de componentes do Windows de pacotes de redistribuição exija uma reinicialização, a menos que a reinicialização seja indicada por um resultado de retorno ou pela documentação da Microsoft.

Se o instalador do jogo sempre força uma reinicialização, isso deve ser aprovado pela Microsoft.

As caixas de diálogo de arquivos em uso incluídas Windows Installer pacotes devem conter uma opção para fechar automaticamente os aplicativos e tentar reiniciá-los após a conclusão da instalação.

</dd> <dt>

<span id="Rationale"></span><span id="rationale"></span><span id="RATIONALE"></span>**Lógica**
</dt> <dd>

Reinicializar o sistema após uma instalação é uma interrupção inconveniente para os usuários e geralmente é desnecessário.

</dd> <dt>

<span id="Additional_Information"></span><span id="additional_information"></span><span id="ADDITIONAL_INFORMATION"></span>**Informações adicionais**
</dt> <dd>

Para obter mais informações, consulte [Using Windows Installer with Restart Manager](/windows/desktop/Msi/using-windows-installer-with-restart-manager).

</dd> </dl>

### <a name="36-use-file-versioning-correctly"></a>3.6 Usar o versionamento de arquivo corretamente

<dl> <dt>

<span id="Requirement"></span><span id="requirement"></span><span id="REQUIREMENT"></span>**Exigência**
</dt> <dd>

O programa de instalação do jogo deve verificar corretamente para garantir que as versões mais recentes do arquivo sejam instaladas. A instalação de um jogo nunca deve regredir os arquivos que você não produz ou que são compartilhados por aplicativos que você não produz.

</dd> <dt>

<span id="Rationale"></span><span id="rationale"></span><span id="RATIONALE"></span>**Lógica**
</dt> <dd>

Componentes compartilhados e componentes do sistema geralmente são atualizados para correções de segurança e funcionalidade expandida. Uma instalação que inclui uma versão mais antiga dos componentes atualizados não deve resultar na perda de atualizações e correções que já foram aplicadas.

</dd> </dl>

### <a name="37-support-autorun-conditional-requirement"></a>3.7 Dar suporte ao requisito condicional de autorun \[\]

<dl> <dt>

<span id="Requirement"></span><span id="requirement"></span><span id="REQUIREMENT"></span>**Exigência**
</dt> <dd>

Para jogos distribuídos em CD, DVD ou outras mídias removíveis que suportam a Autorun, quando o disco é inserido pela primeira vez, o aplicativo deve ser executado automaticamente ou solicitar que o usuário instale o jogo, a menos que o usuário tenha desabilitado o recurso Executar automaticamente.

Depois que o aplicativo for instalado com êxito, a inserção novamente do disco na unidade não deverá fazer com que a instalação seja iniciada automaticamente novamente. É aceitável perguntar aos usuários se eles querem atualizar ou alterar suas opções de instalação.

O aplicativo de autorun não deve solicitar elevação (ou seja, ele deve ter asInvoker no manifesto, de acordo com o requisito 2.1), embora possa iniciar o programa de instalação ou outro utilitário que exija direitos administrativos. A elevação deverá ocorrer somente se o jogo não estiver instalado ou se o usuário o selecionar especificamente.

</dd> <dt>

<span id="Rationale"></span><span id="rationale"></span><span id="RATIONALE"></span>**Lógica**
</dt> <dd>

A autorun simplifica a experiência de usar aplicativos distribuídos por mídia, como jogos que normalmente exigem que o disco está presente na unidade para jogar o jogo.

</dd> <dt>

<span id="Additional_Information"></span><span id="additional_information"></span><span id="ADDITIONAL_INFORMATION"></span>**Informações adicionais**
</dt> <dd>

Não é aceitável exigir que o usuário navegue no Explorador de Arquivos para iniciar a instalação do CD ou DVD.

Para jogos distribuídos em vários discos, o ideal é que os discos subsequentes usem o recurso de Autorun ou continuem a instalação sem solicitar que o usuário pressione uma tecla ou tome outra ação.

Ao autorizar um programa de Autorun, verifique se todos os componentes necessários estão presentes em novas instalações do Windows. Os aplicativos típicos dependem de tecnologias instaladas pela instalação, mas a execução automática em si é executada antes que qualquer configuração desse tipo ocorra. Um exemplo comum é a falha de programas de Execução automática porque as DLLs do Runtime do Visual C não foram incluídas como parte da configuração do Windows. O programa de autorun, portanto, deve usar a implantação do CRT local do aplicativo ou vincular estaticamente o CRT.

Os programas de execução automática escritos para uso em versões do Windows antes do Windows Vista não devem usar o runtime do .NET porque essa tecnologia não está incluída no Windows XP ou em versões mais antigas do Windows. O Windows Server 2003 e o Windows Vista são as primeiras versões do Windows a incluir o runtime do .NET como parte de seu sistema operacional.

Por motivos semelhantes, os programas de Autorun não podem exigir a presença de componentes opcionais lado a lado do SDK do DirectX, como D3DX9, D3DX10, D3DX11, XAudio2, X3DAudio, XACT, XINPUT e MDX 1.1.

Para ver um exemplo de como usar a Autorun, consulte Exemplo de AutoRun.

</dd> </dl>

## <a name="reliability"></a>Confiabilidade

**Resumo dos requisitos de segurança e compatibilidade**

**Benefícios do cliente**

Esses requisitos torna um aplicativo mais confiável minimizando o número de falhas, travamentos e reinicializações. Os requisitos de confiabilidade podem ajudar a garantir que o software seja mais previsível, mantenível, resiliente e recuperável.

### <a name="41-eliminate-unnecessary-reboots"></a>4.1 Eliminar reinicializações desnecessárias

<dl> <dt>

<span id="Requirement"></span><span id="requirement"></span><span id="REQUIREMENT"></span>**Exigência**
</dt> <dd>

Todos os instaladores de aplicativos devem aproveitar as APIs do gerenciador de reinicialização para evitar reinicializações do sistema (consulte o requisito 3.5).

Os jogos não devem bloquear o desligamento.

Todos os aplicativos devem responder ao gerenciador de reinicialização escutando e respondendo às seguintes mensagens de desligamento:

<dl> <dt>

<span id="WM_QUERYENDSESSION_with_LPARAM___ENDSESSION_CLOSEAPP__0x1___"></span><span id="wm_queryendsession_with_lparam___endsession_closeapp__0x1___"></span><span id="WM_QUERYENDSESSION_WITH_LPARAM___ENDSESSION_CLOSEAPP__0X1___"></span>WM \_ QUERYENDSESSION com LPARAM = ENDSESSION \_ CLOSEAPP (0x1) 
</dt> <dd>

Os aplicativos de GUI devem responder (TRUE) imediatamente em preparação para uma reinicialização.

</dd> <dt>

<span id="WM_ENDSESSION_with_LPARAM___ENDSESSION_CLOSEAPP__0x1___"></span><span id="wm_endsession_with_lparam___endsession_closeapp__0x1___"></span><span id="WM_ENDSESSION_WITH_LPARAM___ENDSESSION_CLOSEAPP__0X1___"></span>WM \_ ENDSESSION com LPARAM = ENDSESSION \_ CLOSEAPP (0x1) 
</dt> <dd>

Os aplicativos devem retornar um valor 0 dentro de 5 segundos e, em seguida, fechar.

</dd> <dt>

<span id="CTRL_C__"></span><span id="ctrl_c__"></span>CTRL+C 
</dt> <dd>

Os aplicativos de console que recebem essa mensagem devem ser fechado imediatamente.

</dd> </dl> </dd> <dt>

<span id="Rationale"></span><span id="rationale"></span><span id="RATIONALE"></span>**Lógica**
</dt> <dd>

As reinicializações do sistema são uma interrupção importante. Eles levam a uma experiência de usuário ruim e devem ser minimizados. Algumas operações, como atualizações críticas do sistema, podem exigir reinicializações. Ao escutar mensagens de desligamento, o jogo e outros aplicativos podem reagir imediatamente às solicitações do gerenciador de reinicialização. Dessa forma, eles podem evitar atrasos desnecessários em solicitações de reinicialização válidas.

</dd> <dt>

<span id="Additional_Information"></span><span id="additional_information"></span><span id="ADDITIONAL_INFORMATION"></span>**Informações adicionais**
</dt> <dd>

Se um instalador de jogos usar Windows Installer (MSI) sem nenhuma ação personalizada, essa funcionalidade será fornecida automaticamente. Os pacotes de redistribuição da Microsoft também são suportados pelo Gerenciador de Reinicialização.

Para obter mais informações sobre o Gerenciador de Reinicialização, consulte o artigo do MSDN [Sobre o Restart Manager.](/windows/desktop/RstMgr/about-restart-manager)

</dd> </dl>

### <a name="42-eliminate-application-verifier-failures"></a>4.2 Eliminar Application Verifier falhas

<dl> <dt>

<span id="Requirement"></span><span id="requirement"></span><span id="REQUIREMENT"></span>**Exigência**
</dt> <dd>

O jogo não deve gerar falhas em execução no Microsoft Application Verifier (AppVerifier), versão 4.0 ou posterior, nos seguintes testes:

-   Noções básicas: Handles, Heaps, Locks, Memory, TLS
-   Diversos: DangerousAPIs, DirtyStacks

</dd> <dt>

<span id="Rationale"></span><span id="rationale"></span><span id="RATIONALE"></span>**Lógica**
</dt> <dd>

O AppVerifier testa muitos problemas conhecidos que causam falhas e travamentos em aplicativos do Windows, bem como vulnerabilidades de segurança conhecidas.

</dd> <dt>

<span id="Additional_Information"></span><span id="additional_information"></span><span id="ADDITIONAL_INFORMATION"></span>**Informações adicionais**
</dt> <dd>

Para obter mais informações sobre Application Verifier, consulte [Application Verifier](/previous-versions/ms220948(v=vs.80)) [e Usando Application Verifier em](/previous-versions/aa480483(v=msdn.10)) seu ciclo de vida de desenvolvimento de software no MSDN. Você pode baixar Application Verifier em [Detalhes do download: Application Verifier](https://www.microsoft.com/downloads/details.aspx?familyid=c4a25ab9-649d-4a1b-b4a7-c9d8b095df18) no Centro de Download da Microsoft.

Esse requisito não se aplica a aplicativos gerenciados puros sem interop nativa.

Esses testes devem ser executados em um build de versão. A depuração de builds pode gerar falhas falsas. Algumas tecnologias antissegmentar e antissegência podem interferir na execução de AppVerifier. Portanto, esses testes devem ser executados sem tecnologias antiesvaxa e anti-fraude habilitadas.

Pode ser necessário definir a propriedade Full do teste Basics:Heaps como FALSE, pois a PageHeap completa aumenta muito a pressão de memória do aplicativo em execução. As falhas ainda serão detectadas, mas podem ser mais difíceis de rastrear se você usar apenas PageHeap parcial.

Se você usar os testes relacionados ao UAC/LUA no Application Verifier para atender aos requisitos de Controle de Conta de Usuário 2.1 e 3.2, use o [Standard User Analyzer](/windows/desktop/Win7AppQual/standard-user-analyzer--sua--tool-and-standard-user-analyzer-wizard--sua-wizard-) para revisar os resultados. Também há vários outros testes úteis fornecidos pelo Application Verifier que você é incentivado a usar no desenvolvimento e no teste para garantir um alto nível de compatibilidade com versões atuais e futuras do Windows. O **teste HighVersionLie** é usado para verificar a conformidade com o requisito 2.5.

Visual Studio Team System inclui um subconjunto da funcionalidade AppVerifier integrado ao ambiente de depuração. Isso pode ser útil para rastrear e resolver problemas com os testes básicos: heaps, handles e locks.

</dd> </dl>

### <a name="43-support-windows-error-reporting-and-file-version-information"></a>4.3 Suporte a Relatório de Erros do Windows e informações de versão do arquivo

<dl> <dt>

<span id="Requirement"></span><span id="requirement"></span><span id="REQUIREMENT"></span>**Exigência**
</dt> <dd>

Para habilitar o suporte Relatório de Erros do Windows, os jogos devem atender aos seguintes requisitos:

-   Os jogos devem lidar apenas com exceções conhecidas e esperadas. Relatório de Erros do Windows não deve ser desabilitado. Se uma falha como uma Violação de Acesso aparecer em um jogo, ela deverá permitir Relatório de Erros do Windows relatar a falha.
-   Todos os arquivos executáveis (por exemplo, .exe arquivos ou DLLs) devem conter um nome de produto preciso, o nome da empresa e a versão do arquivo.
-   A saída normal do jogo não deve resultar em uma falha de exceção desconhecida.

</dd> <dt>

<span id="Rationale"></span><span id="rationale"></span><span id="RATIONALE"></span>**Lógica**
</dt> <dd>

As APIs Relatório de Erros do Windows fornecem comentários vitais à Microsoft para detectar falhas generalizadas e travamentos em aplicativos. Isso permite que a Microsoft e seus parceiros detectem e resolvam rapidamente problemas de sistema e driver que levam a falhas de aplicativo rapidamente.

</dd> <dt>

<span id="Additional_Information"></span><span id="additional_information"></span><span id="ADDITIONAL_INFORMATION"></span>**Informações adicionais**
</dt> <dd>

Os jogos podem incluir manipuladores de exceção sem ajuda personalizados para executar o suporte personalizado e a funcionalidade de relatório, mas eles devem passar qualquer erro para as funções **ReportFault** ou **WerReportSubmit.**

As informações de versão adequadas do arquivo podem ser verificadas exibindo as propriedades do arquivo na interface do usuário da área de trabalho do Windows e verificando a página de propriedades Versão.

Para obter mais informações sobre as APIs Relatório de Erros do Windows e como analisar os despejos de falha gerados quando você usa esse serviço, consulte o artigo DirectX Análise de Despejo [de Falha](/windows/desktop/DxTechArts/crash-dump-analysis).

</dd> </dl>

## <a name="xbox-360-common-controller-for-windows-terminology"></a>Xbox 360 Common Controller para Terminologia do Windows



| Nome                                          | Descrição                                                                                                 |
|------------------------------------------|--------------------------------------------------------------------------------------------------|
| Um                                        | O botão A.                                                                                     |
| B                                        | O botão B.                                                                                     |
| BACK                                     | O botão Voltar.                                                                                  |
| (direita/esquerda)                      | O botão na borda superior direita e esquerda do controlador. Equivalente a um botão de altura.    |
| painel direcional                          | O painel direcional do controlador.                                                                   |
| Painel D                                    | Abreviação aceita do painel direcional.                                                         |
| DP                                       | Abreviação de painel direcional e rótulo do controlador.                                                |
| RB, LB                                   | Abreviações e rótulos de controlador da direita e da esquerda.                                        |
| RS, LS                                   | Abreviações de controle e abreviações de stick à direita e à esquerda.                                         |
| RT, LT                                   | Abreviações de gatilho à direita e à esquerda e rótulos do controlador.                                       |
| RSB, LSB                                 | Abreviações de controle e abreviações de stick à direita e à esquerda.                                         |
| START                                    | O botão Iniciar.                                                                                 |
| (direita/esquerda) stick                       | O stick do controlador. Anteriormente, o thumbstick.                                                       |
| Botão de stick (direita/esquerda)                | O botão de stick do controlador. Anteriormente, o botão de thumbstick.                                         |
| Gatilho (direita/esquerda)                     | O gatilho do controlador.                                                                          |
| Vibração                                | Comentários de jogo produzidos pelo motor do controlador. Não use o esbravejável.                           |
| X                                        | O botão X.                                                                                     |
| Y                                        | O botão Y.                                                                                     |
| Xbox 360 controlador para Windows          | O Xbox 360 gamepad vendido como um SKU de hardware de pc, incluindo um disco de driver de dispositivo Windows.          |
| Xbox 360 sem fio para Windows | O Xbox 360 gamepad sem fio vendido como um SKU de hardware de pc, incluindo um disco de driver de dispositivo Windows. |



 

## <a name="guidelines-for-game-middleware-products"></a>Diretrizes para produtos de middleware de jogos

### <a name="introduction"></a>Introdução

Para que os jogos se qualiem para o programa Jogos para Windows, eles devem atender a uma lista de requisitos técnicos. Todos os componentes de terceiros fornecidos com um título (arquivos executáveis, DLLs, drivers e assim por diante) também devem atender a esses requisitos para que o jogo seja qualificado. Este documento destaca os requisitos mais comuns que também devem ser atendidos pelos componentes de terceiros para que o jogo passe nos testes de conformidade. Os instaladores e pacotes completos de produção/mecanismo de jogos devem revisar o documento completo de requisitos técnicos de Jogos para Windows, pois muitos desses requisitos são afetados por essas ferramentas.

### <a name="additional-recommendations"></a>Recomendações adicionais

Além de garantir que seu componente dê suporte à criação de títulos que estão em conformidade com os requisitos para Jogos para Windows, há várias outras considerações que você deve levar em conta ao projetar e implantar uma biblioteca ou utilitário de suporte para um jogo do Windows.

-   Para dar suporte a desenvolvedores que trabalham em aplicativos x64 nativos de 64 bits, forneça versões nativas de 32 e 64 bits de suas bibliotecas. A versão de 32 bits deve ser compatível com 64 bits por 2,2. As bibliotecas para aplicativos de 32 bits não devem assumir que o alto bit de qualquer endereço de 32 bits não é usado para dar suporte ao uso em aplicativos LARGEADDRESSAWARE x86.
-   Se você fornecer os headers de código nativo (C/C++), use a sintaxe de atributo SAL (Linguagem de Anotação Padrão) para decorar suas rotinas de API públicas. Isso permitirá que os usuários de sua biblioteca recebam o benefício máximo de usar o Code Analysis estático (/analyze), que faz parte do Visual Studio Team System 2005, do Visual Studio Team System 2008, do Visual Studio 2010 Premium e do Visual Studio 2010 Ultimate, bem como das ferramentas do compilador SDK do Windows disponíveis publicamente.
-   Se seu produto criar threads dentro do processo do usuário, nomee cada thread para que as ferramentas de depuração possam anotar corretamente os threads em execução.
-   Se você escrever rotinas que devem ser chamadas dentro do loop principal de um jogo, use as rotinas D3DX D3DPERF \_ BeginEvent/EndEvent e D3DPERF SetMarker para anotar operações de alto nível para facilitar a identificação de gargalos usando \_ oNEC para Windows.
    > [!Note]  
    > Para a Visual Studio de diagnóstico de gráficos do Visual Studio 2012, essas rotinas D3DX e BLOOM são substituídas pela interface [**ID3DUserDefinedAnnotation.**](/windows/desktop/api/d3d11_1/nn-d3d11_1-id3duserdefinedannotation)

     

-   Para bibliotecas de rede, forneça implementações neutras de IP e evite rotinas IPv4 preteridas para dar suporte às tecnologias IPv6 e Teredo no Windows XP com Service Pack 2, Windows Vista e Windows 7.
-   Os provedores de serviços de jogos devem se registrar no Games Explorer usando a versão 2 do esquema GDF e usar o recurso RSS para fornecer notícias relacionadas ao serviço.

### <a name="games-for-windows-showcases"></a>Demonstrações de jogos para Windows

### <a name="introduction"></a>Introdução

As demonstrações de jogos para Windows vão além de fornecer uma experiência de jogos sólida em computadores Windows. Ao implementar esses recursos, os jogos podem adicionar mais animação à experiência do usuário nas plataformas mais recentes do Windows.

Os jogos para títulos do Windows devem atender a todos os requisitos técnicos listados neste artigo, mas os recursos de demonstração são opcionais. Esses títulos são gratuitos para implementar algumas, nenhuma ou todas essas demonstrações.

### <a name="s1-exploit-direct3d-11"></a>S.1 Exploit Direct3D 11

<dl> <dt>

<span id="Requirement"></span><span id="requirement"></span><span id="REQUIREMENT"></span>**Exigência**
</dt> <dd>

O Direct3D 11 é a API de renderização de última geração para Windows Vista e Windows 7. Os jogos que exploram o Direct3D 11 usam conteúdo otimizado, técnicas avançadas de renderização e novos recursos de hardware para criar uma experiência atraente no hardware que dá suporte a 10, 10.1 e 11.

Se o jogo também implementar o Direct3D 9, uma comparação lado a lado deverá demonstrar uma melhoria perceptível na qualidade do conteúdo, na fidelidade visual, no desempenho, na complexidade da cena e em outras áreas de fidelidade de gráficos para o Direct3D 11. Esse suporte está sujeito aos Jogos para Windows Technical Requirement 1.7.

A tecnologia Direct3D 10level9 pode ser usada para dar suporte ao hardware de vídeo de 9 classes Direct3D/2.0/3.0 do Modelo de Sombreador 2.0/3.0 no Windows Vista e Windows 7, em vez de usar uma implementação lado a lado do Direct3D 9 para amplo suporte a hardware. No entanto, isso não é suficiente para demonstrar essa demonstração.

Em computadores que executam o Windows Vista ou o Windows 7 com o Direct3D 11 instalado, o jogo deve usar o Direct3D 11 como padrão.

</dd> <dt>

<span id="Rationale"></span><span id="rationale"></span><span id="RATIONALE"></span>**Lógica**
</dt> <dd>

A API do Direct3D 11 se baseia na infraestrutura WDDM (Modelo de Driver de Exibição do Windows) e Direct3D 10.1 para dar suporte a novos recursos: mosaico de hardware, sombreadores de computação, renderização multithread e criação de recursos, novos formatos de compactação de textura e uma linguagem de sombreador mais flexível. O Direct3D 11 fornece suporte de hardware unificado para placas de vídeo modernas, incluindo as últimas partes de geração do Direct3D 11, todas as placas de vídeo Direct3D 10 e 10.1 e muitas placas de vídeo do Modelo de Sombreador 2.0/3.0 Direct3D 9, que é o hardware de vídeo mínimo necessário para a área de trabalho do Aero 3D.

</dd> <dt>

<span id="Additional_Information"></span><span id="additional_information"></span><span id="ADDITIONAL_INFORMATION"></span>**Informações adicionais**
</dt> <dd>

Migrar um mecanismo de renderização direct3D 9 para usar a nova interface direct3D 11 é uma tarefa bem definida:

-   Elimine todas as operações de função fixa em favor de sombreadores programáveis.
-   Atualize todos os sombreadores existentes para a nova sintaxe do Modelo de Sombreador 4.x/5.
-   Atualize o gerenciamento de recursos para dar suporte ao novo modelo de exibição.
-   Converta todos os ativos para usar uma nova lista de formatos disponíveis.
-   Atualize o tratamento de estado de renderização para usar blocos de estado imutáveis e retrabalho constantes de sombreador em buffers constantes.

Essa conversão é essencial para habilitar a demonstração do Direct3D 11, embora o resultado não atender ao requisito de demonstração de exploração da nova API.

A nova API e o modelo de programação HLSL associado oferecem muitas oportunidades para conteúdo aprimorado:

-   Aproveitando os recursos de hardware existentes do Direct3D 10, como Sombreador de Geometria, Stream Out, matrizes de textura e formatos de textura compactados BC4/BC5.
-   Aproveitando os recursos de hardware existentes do Direct3D 10.1, como modos de mesclagem independentes por destino de renderização, leitura de profundidade da MSAA, acesso de sombreador por exemplo da MSAA, matrizes de mapa de cubo e renderização para formatos BC (compactados em bloco).
-   Implementando algoritmos de GPU avançados usando o Sombreador de Computação com CS4.x em placas de vídeo direct3D 10/10.1 existentes (habilitadas por drivers de vídeo atualizados) ou CS 5.0 em placas de vídeo Direct3D 11 de última geração.
-   Renderização em vários threads usando a criação de recursos de thread livre e vários contextos de dispositivo para melhorar o desempenho em sistemas multicore (com drivers de vídeo atualizados). Para obter mais informações, consulte Jogos para Windows Showcase S.3.
-   A utilização de novos recursos do hardware de vídeo da classe Direct3D 11, como mosaico de hardware com sombreadores de área e domínio, hardware de sombreador HLSL do Modelo de Sombreador 5.0 apresenta formatos de textura compactados BC6HBC7 e Vinculação dinâmica do sombreador.

Técnicas que podem ser implementadas com o Direct3D 9 (em grande parte por meio do alto custo de CPU) podem ser carregadas para a GPU de maneira eficiente, liberando recursos de CPU para dar suporte a outras demandas de jogo.

APIs do Direct3D 11, ferramentas de suporte e exemplos estão disponíveis no SDK do DirectX. Consulte também APIs de gráficos no Windows.

</dd> </dl>

### <a name="s2-exploit-x64-native"></a>S.2 Exploit x64 Native

<dl> <dt>

<span id="Requirement"></span><span id="requirement"></span><span id="REQUIREMENT"></span>**Exigência**
</dt> <dd>

O jogo inclui um executável nativo de 64 bits que oferece uma nova experiência atraente habilitada pelas edições x64 do Windows em execução em hardware com capacidade para x64. Uma comparação lado a lado com a versão de 32 bits do jogo deve mostrar uma melhoria perceptível na complexidade do conteúdo, redução dos tempos de carregamento gerais e do desempenho.

Em edições de 64 bits do Windows, a instalação sempre deve configurar a versão nativa de 64 bits do jogo como o padrão para atalhos no Games Explorer e no Windows XP Professional x64 Edition. Se a instalação dupla for desejada, uma tarefa de reprodução adicional poderá ser especificada para o Games Explorer no Windows Vista e No Windows 7 que aponta para a versão de 32 bits, mas o padrão deve permanecer a versão nativa de 64 bits.

Observe que o jogo deve dar suporte às edições de 64 bits do Windows Vista e do Windows 7 para atender a essa recomendação de demonstração. O suporte para o Windows XP Professional x64 Edition é incentivado, mas não é necessário.

</dd> <dt>

<span id="Rationale"></span><span id="rationale"></span><span id="RATIONALE"></span>**Lógica**
</dt> <dd>

A tecnologia x64 fornece funcionalidades de endereçamento de 64 bits para os mercados de consumidor e servidor que incluem compatibilidade com velocidade total de 32 bits para aplicativos existentes. O x64 é uma parte importante do roteiro para AMD (AMD64) e Intel (EMT64) e, com exceção de CPUs ultra-móveis, dar suporte à tecnologia para todos os processadores de geração atuais e futuros.

O Windows XP Professional x64 Edition foi o primeiro sistema operacional Windows orientado ao consumidor para dar suporte à tecnologia x64 e o Windows Vista e o Windows 7 expandem muito a disponibilidade da habilitação do sistema operacional para computação do consumidor de 64 bits. Com 2 GB de RAM como padrão em muitos computadores novos, outras melhorias no dimensionamento de memória não beneficiarão aplicativos individuais de 32 bits que não conseguem lidar com mais de 2 GB de RAM física. Muitos jogos atualmente enfrentam desafios que se ajustam a todo o conteúdo disponível nas restrições de 2 GB de espaço de endereço virtual, especialmente quando combinados com as memórias de vídeo grandes disponíveis em GPUs de alto nível e a mudança para a tecnologia x64 aumenta muito os níveis de detalhes com suporte.

A compatibilidade com x64 para jogos de 32 bits é um requisito técnico dos Jogos para Windows (2.2), mas aproveitar ao máximo as novas tecnologias requer uma implementação nativa de 64 bits.

</dd> <dt>

<span id="Additional_Information"></span><span id="additional_information"></span><span id="ADDITIONAL_INFORMATION"></span>**Informações adicionais**
</dt> <dd>

O principal benefício do endereçamento de 64 bits é a capacidade de acessar diretamente mais de 2 GB de memória física e virtual. O espaço de endereço de memória virtual grande permite o uso extensivo de E/S mapeada em memória sem preocupação com problemas de esgotamento de espaço de endereço da VM predominantes na programação de 32 bits. Os jogos podem aproveitar o novo espaço para melhorar muito os tempos de carregamento ou, em algumas instâncias, eliminar pausas para carregar conteúdo.

Aplicativos de 32 bits existentes podem se beneficiar de edições x64, tendo a capacidade de processar endereços com dados completos de 32 bits quando criado com a opção de vinculador Habilitar Endereços Grandes (**/LARGEADDRESSAWARE**). Em versões de 32 bits do Windows XP, os modos de inicialização especiais permitiam que esses aplicativos abordam até 3 GB de RAM e as edições x64 fornecem acesso de até 4 GB de RAM para aplicativos LAA (Com Suporte a Endereços Grandes). Embora o uso da LAA em um aplicativo de 32 bits não atender a esse requisito de demonstração, essa tecnologia de ponte é uma maneira extremamente útil de fornecer benefícios adicionais de dimensionamento em versões x64 do Windows para aqueles que não implementam totalmente esse requisito de demonstração.

Para obter mais informações, consulte Programação de [64](/windows/desktop/DxTechArts/sixty-four-bit-programming-for-game-developers) bits para desenvolvedores de jogos e [RAM, VRAM](https://www.gamasutra.com/view/feature/3602/sponsored_feature_ram_vram_and_.php) e mais RAM: Jogos de 64 bits estão aqui no Gamas ltda.

> [!Note]  
> Um grande desafio para essa demonstração é garantir que todas as bibliotecas ou componentes de terceiros em que seu jogo depende estão disponíveis para desenvolvimento nativo de 64 bits. Muitas APIs herdados da Microsoft também foram eliminadas do ambiente nativo de 64 bits, o que pode provar um desafio para bases de código do mecanismo que contêm implementações mais antigas de sistemas principais.

 

</dd> </dl>

### <a name="s3-exploit-many-core-processors"></a>Processadores de Many-Core S.3

<dl> <dt>

<span id="Requirement"></span><span id="requirement"></span><span id="REQUIREMENT"></span>**Exigência**
</dt> <dd>

O jogo implementa recursos que aproveitam processadores multicore, dimensionando para 3, 4 ou mais núcleos, quando disponíveis.

Se o jogo dá suporte a sistemas de processador único ou de núcleo duplo, uma comparação lado a lado com um sistema quad-core deve demonstrar novos recursos perceptíveis, efeitos atraentes adicionais, melhoria na qualidade do conteúdo e/ou desempenho aprimorado.

Como o dimensionamento de núcleo duplo já é amplamente suportado por jogos, bem como utilizado automaticamente por vários aprimoramentos de driver Direct3D, o dimensionamento de núcleo duplo não é suficiente para demonstrar essa demonstração.

</dd> <dt>

<span id="Rationale"></span><span id="rationale"></span><span id="RATIONALE"></span>**Lógica**
</dt> <dd>

O crescimento contínuo no desempenho de CPUs mudou de melhorias de taxa de relógio para a adição de núcleos computacionais. Os roteiros AMD e Intel são baseados em designs escalonáveis e multicore. Todas as plataformas de jogos de última geração têm CPUs multicore devido a essa mudança fundamental na evolução dos processadores. Aplicativos de thread único não verão mais ganhos significativos das CPUs de última geração. Multithreading simples também falhará ao dimensionar à medida que o número de núcleos de CPU em uso comum aumenta para três ou mais.

</dd> <dt>

<span id="Additional_Information"></span><span id="additional_information"></span><span id="ADDITIONAL_INFORMATION"></span>**Informações adicionais**
</dt> <dd>

Observe que as contagens de núcleo não precisam ser uma potência de dois, portanto, os jogos devem ser escalados linearmente e lidar com contagens principais de 3, 4, 5, 6, 7, 8 e assim por diante.

O dimensionamento aumentando o número de threads em um aplicativo só fornece um retorno se o custo de comunicação e a sincronização de threads são mantidos em verificação. O dimensionamento baseado em recursos pode ser uma solução mais fácil em curto prazo, permitindo que o jogo opere normalmente sem os threads adicionais em sistemas de núcleo único e habilitando-os quando a potência adicional da CPU estiver disponível.

Para obter mais informações, consulte [Coding for Multiple Cores](/windows/desktop/DxTechArts/coding-for-multiple-cores) on Xbox 360 and Microsoft Windows and [Lockless Programming Considerations for Xbox 360](/windows/desktop/DxTechArts/lockless-programming) and Microsoft Windows nos artigos DirectX, bem como o utilitário DXUTLockFreePipe e o exemplo coreDetection.

Fazer uso da criação de recursos de thread livre do Direct3D 11 e dos contextos do dispositivo é útil para alcançar a escalabilidade de muitos núcleos na renderização e no carregamento de recursos gráficos. Confira Jogos para Windows Showcase S.1.

Observe que o uso da instrução de CPU rdtsc diretamente, em vez de usar APIs do Windows para calcular o tempo em sistemas multicore, pode levar a problemas em algumas configurações de hardware e sistema operacional; consulte [Game Timing and Multicore Processors](/windows/desktop/DxTechArts/game-timing-and-multicore-processors) nos artigos DirectX.

</dd> </dl>

### <a name="s4-support-games-for-windows---live"></a>Jogos de suporte do S.4 para Windows – LIVE

Não há mais suporte para jogos para Windows – LIVE da Microsoft.

### <a name="s5-support-windows-touch"></a>Suporte do S.5 Windows Touch

<dl> <dt>

<span id="Requirement"></span><span id="requirement"></span><span id="REQUIREMENT"></span>**Exigência**
</dt> <dd>

Os jogos com capacidade de toque do Windows são reproduzíveis usando toque e/ou gestos em computadores que executam o Windows 7 com uma exibição de toque. A entrada do teclado também pode ser usada, mas a interface de reprodução primária deve ser baseada em toque.

A habilitação do toque não deve impedir o uso do mouse ou do controlador comum, sujeito ao Requisito Técnico 1.4.

O instalador do jogo não deve dar suporte Windows Touch funcionalidade.

</dd> <dt>

<span id="Rationale"></span><span id="rationale"></span><span id="RATIONALE"></span>**Lógica**
</dt> <dd>

As exibições com capacidade para toque múltiplo para computadores estão disponíveis para laptops e áreas de trabalho e representam um recurso de hardware principal que está sendo promovido com o lançamento do Windows 7. O Windows 7 dá suporte Windows Touch em toda a área de trabalho e interfaces de controles comuns.

</dd> <dt>

<span id="Additional_Information"></span><span id="additional_information"></span><span id="ADDITIONAL_INFORMATION"></span>**Informações adicionais**
</dt> <dd>

Os aplicativos de código nativo podem acessar vários toques por meio das mensagens WM TOUCH, em combinação \_ com a [**função RegisterTouchWindow.**](/windows/desktop/api/winuser/nf-winuser-registertouchwindow) Consulte também a API de Manipulações e Inércia.

Windows Presentation Foundation (WPF) 4.0 fornece uma solução gerenciada para interfaces de vários toques.

Para obter mais informações, consulte Windows Touch SDK.

</dd> </dl>

### <a name="s6-support-high-color"></a>S.6 Suporte a cor alta

<dl> <dt>

<span id="Requirement"></span><span id="requirement"></span><span id="REQUIREMENT"></span>**Exigência**
</dt> <dd>

Os jogos que suportam Cor Alta usam um 10:10:10:2 (FORMATO DXGI \_ \_ R10G10B10A2, D3DFMT \_ A2B10G10R10) ou um formato 16:16:16:16 (FORMATO DXGI \_ \_ R16G16B16A16, D3DFMT \_ A16B16G16R16) para o modo de exibição de tela inteira e back-buffer de renderização.

Usando um destino de renderização de Alta Cor, o conteúdo do HDR (intervalo High-Dynamic) pode ser renderizado com uma gama estendida ou ampla ao executar o mapeamento de tom para um intervalo de 10 ou 16 bits.

</dd> <dt>

<span id="Rationale"></span><span id="rationale"></span><span id="RATIONALE"></span>**Lógica**
</dt> <dd>

Os monitores têm sido capazes de exibir mais de 256 níveis de cor por canal por muitos anos, mesmo quando as exibições CRT eram predominantes. O hardware de verificação em placas de vídeo foi o fator limitante. As GPUs modernas, incluindo a maioria dos hardwares de 9 classes direct3D e todos os hardwares de 10 e melhores do Direct3D, têm hardware de varredura capaz de pelo menos 10 bits por canal e a capacidade de hardware está definida para aumentar para 16 bits por canal de cores no futuro. Os sistemas de interconexão de TV HD (HDMI, DisplayPort) foram projetados para lidar com mais de 8 bits por canal, e a VGA análoga já carregará esses sinais.

</dd> <dt>

<span id="Additional_Information"></span><span id="additional_information"></span><span id="ADDITIONAL_INFORMATION"></span>**Informações adicionais**
</dt> <dd>

Observe que Cor Alta, ou Cor Alta, historicamente se refere à movimentação de exibições de cor de 256 (8 bits) para exibições de cor de 15 ou 16 bits. A maioria dos sistemas de exibição foi movida há muito tempo para a Cor Verdadeira, que é uma cor de 24 bits ou 8 bits por canal de cores para vermelho, verde e azul. Por Cor Alta aqui, queremos dizer uma nova geração de sistemas de exibição que podem operar com mais de 8 bits por canal de cores individual. O também é conhecido como Cor Profunda.

</dd> </dl>

### <a name="recommended-best-practices"></a>Práticas recomendadas

### <a name="introduction"></a>Introdução

Além de atender aos Requisitos Técnicos e adotar uma ou mais Demonstrações em seu título, há várias práticas recomendadas que devem ser seguidas para todos os jogos do Windows. Embora essas recomendações estejam fora do escopo dos Principais Requisitos Técnicos, você é incentivado a empresá-las para todos os títulos dos Jogos para Windows.

### <a name="additional-recommendations"></a>Recomendações adicionais

-   Use o compilador de Visual Studio e o runtime mais recentes. As versões mais recentes do compilador implementam melhorias significativas para a qualidade do código gerado e para problemas de segurança, e empregam estratégias modernas de otimização do processador. Atualizar o compilador e usar o runtime C mais recente é uma maneira fácil de migrar para práticas de codificação modernas.
-   Use a versão DLL (biblioteca de vínculo dinâmico) do Runtime C, em vez de vinculação estática, e use o Secure CRT. (Exceções podem ser feitas em casos especiais de pré-instalação, como para um programa de Autorun ou para o próprio instalador).
-   Para áudio do jogo, use XAudio2, X3DAudio e/ou XACT, em vez de DirectSound. Para mecanismos de áudio que fazem toda a combinação e conversão de taxa de origem e precisam apenas de uma solução de baixa latência para saída de áudio, use DirectSound no Windows XP (somente) e WASAPI no Windows Vista e Windows 7.
-   Evite usar APIs herdadas e preterida: DirectDraw, DirectSound, DirectPlay, camada de desempenho do DirectMusic, DirectPlay Voice e Modo Retido direct3D. Observe que o DirectPlay Voice e o Modo retido do Direct3D não estão disponíveis no Windows Vista ou no Windows 7. A camada de desempenho do DirectPlay e do DirectMusic não está disponível para aplicativos nativos x64.
-   Otimizar usando conjuntos de instruções SIMD SSE/SSE2. Consulte a API [directXMath](/windows/desktop/dxmath/directxmath-portal) no SDK do Windows como uma solução de plataforma cruzada para operações matemáticas otimizadas para SIMD.
-   Use práticas recomendadas modernas para segurança do Windows (incluindo opções de compilador e de vinculador, como **/NXCOMPAT,** **/GS,** **/SAFESEH,** **/DYNAMICBASE,** **/SDL** e assim por diante). Para obter mais informações, consulte [Práticas recomendadas de segurança no desenvolvimento de jogos.](/windows/desktop/DxTechArts/best-security-practices-in-game-development)
-   Use as bibliotecas e SDK do Windows mais recentes. Remova dependências do DirectSetup herdado implantados fora de banda, como D3DX9, D3DX10 e D3DX11. Considere usar [DirectXTex](https://github.com/Microsoft/DirectXTex) ou [DirectXTK](https://github.com/Microsoft/DirectXTK) ou ambos.
-   Evite usar o compilador HLSL mais antigo e, em vez disso, use o compilador HLSL moderno. Se o suporte para o Sombreador de Pixel 1.x for exigido pelo seu aplicativo, use o assembly do sombreador em vez de HLSL ou limite o uso do compilador mais antigo apenas para esses cenários.

## <a name="resources"></a>Recursos



| Termo                                                                                                                                                                                                                         | Descrição                                                                                                                                                   |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="Games_for_Windows__Test_Cases__"></span><span id="games_for_windows__test_cases__"></span><span id="GAMES_FOR_WINDOWS__TEST_CASES__"></span>Jogos para Windows: casos de teste <br/>                              | Práticas recomendadas para jogos no Windows XP, Windows Vista e Windows 7<br/>                                                                               |
| <span id="Windows_SDK__"></span><span id="windows_sdk__"></span><span id="WINDOWS_SDK__"></span>SDK do Windows <br/>                                                                                                      | [SDKs do Windows](https://msdn.microsoft.com/bb980924.aspx)<br/>                                                                                      |
| <span id="User_Account_Control_Guidelines__"></span><span id="user_account_control_guidelines__"></span><span id="USER_ACCOUNT_CONTROL_GUIDELINES__"></span>Diretrizes de controle de conta de usuário <br/>                      | [Requisitos de desenvolvimento de aplicativos do Windows Vista para compatibilidade de controle de conta de usuário](/previous-versions/dotnet/articles/bb530410(v=msdn.10))<br/> |
| <span id="WinQual_Developer_Portal__"></span><span id="winqual_developer_portal__"></span><span id="WINQUAL_DEVELOPER_PORTAL__"></span>Portal do desenvolvedor do WinQual <br/>                                                  | [Winqual (Windows Quality Online Services)](/windows-hardware/drivers/dashboard/winqual-submission-tool--winqualexe-)<br/>                                                                         |
| <span id="DirectX_Developer_Portal__"></span><span id="directx_developer_portal__"></span><span id="DIRECTX_DEVELOPER_PORTAL__"></span>Portal do desenvolvedor do DirectX <br/>                                                  | [Central de desenvolvedores do DirectX](/previous-versions/windows/apps/hh452744(v=win.10))<br/>                                                                               |
| <span id="Games_for_Windows_and_DirectX_SDK_Blog"></span><span id="games_for_windows_and_directx_sdk_blog"></span><span id="GAMES_FOR_WINDOWS_AND_DIRECTX_SDK_BLOG"></span>Blog de jogos para Windows e SDK do DirectX<br/> | [Jogos para Windows e SDK do DirectX](https://walbourn.github.io/)<br/>                                                                           |
| <span id="Additional_DirectX_Articles"></span><span id="additional_directx_articles"></span><span id="ADDITIONAL_DIRECTX_ARTICLES"></span>Artigos adicionais sobre o DirectX<br/>                                             | [Artigos técnicos sobre o DirectX](/windows/desktop/DxTechArts/dx9-technical-articles)<br/>                                                                                    |



 

 

