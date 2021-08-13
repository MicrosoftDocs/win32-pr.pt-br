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

<span id="Requirement"></span><span id="requirement"></span><span id="REQUIREMENT"></span>**Exigência**
</dt> <dd>

O jogo deve estar visível no Games Explorer (a **pasta Jogos)** no Windows Vista e Windows 7. Quando selecionado, o jogo também deve exibir metadados corretos, que incluem publicador, desenvolvedor, data de lançamento, versão, pontuações Windows Índice de Experiência, classificação (se aplicável) e hiperlinks associados.

Se o jogo for distribuído digitalmente por meio de um serviço de jogo online, o provedor de serviços também deverá aparecer no Games Explorer. Para garantir o tratamento adequado do provedor e habilitar o uso de feeds RSS, a versão 2 do esquema para GDFs (arquivos de definição de jogo) deve ser usada. (Para obter mais informações sobre GDFs, consulte Informações adicionais.)

Além disso, os instaladores de jogos devem observar as seguintes regras quando são executados no Windows Vista e Windows 7:

-   A instalação não deve criar um atalho para iniciar o jogo na área de trabalho, no menu Iniciar ou em qualquer outro local.
-   Tarefas e atalhos para remoção não devem ser criados.
-   Os usuários devem ser capazes de remover o jogo usando Programas e Recursos no Painel de Controle no Windows Vista e Windows 7 ou Adicionar ou Remover Programas no Painel de Controle no Windows XP.

No Windows XP e nas versões anteriores do Windows, o instalador do jogo é gratuito para criar grupos de programas, ícones de área de trabalho ou atalhos, conforme necessário.

</dd> <dt>

<span id="Rationale"></span><span id="rationale"></span><span id="RATIONALE"></span>**Lógica**
</dt> <dd>

Windows O Games Explorer é semelhante no conceito às pastas Windows XP **Meus Documentos** ou **Minhas Imagens**. A ideia é centralizar conteúdo semelhante em um só lugar e permitir atividades mais fáceis de organização e contextitivas. O Games Explorer estende o **conceito Meus Documentos** ou **Minhas Imagens,** permitindo uma organização mais rica e controle sobre jogos. O Games Explorer permite que os jogadores vejam, organizem e interajam com todos os jogos instalados em seus sistemas. Ele também permite que os editores de jogos comuniquem informações importantes do jogo com mais eficiência. O sistema é orientado por dados, facilitando para um editor de jogos atualizar informações do jogo ao longo da vida útil do produto.

</dd> <dt>

<span id="Additional_Information"></span><span id="additional_information"></span><span id="ADDITIONAL_INFORMATION"></span>**Informações adicionais**
</dt> <dd>

A integração com o Games Explorer exige que você autore um GDF (arquivo de definição de jogo), que é um arquivo de texto XML inserido em um arquivo binário (um arquivo executável ou uma DLL) como um recurso, juntamente com um ícone de Windows. Em seguida, o jogo deve ser registrado com o Games Explorer. O GDF também permite a exposição de informações fornecidas, como título do jogo, editor, desenvolvedor, links para sites e tarefas opcionais. Observe que as tarefas de suporte podem ser apenas links para sites, mas tarefas de reprodução também podem ser usadas para tarefas de suporte opcionais.

O Games Explorer pode usar uma imagem de bitmap em miniatura, mas é recomendável que, em vez disso, você forneça um recurso de ícone de Windows com ícones grandes (256 256). O recurso de ícone deve incluir tamanhos de imagem de 256 256 48 48, 32 32 e 16 16 em profundidades de cor de 24 bits (Cor Verdadeira) e 8 bits (256). O editor de ícones fornecido no Visual Studio 2008 e 2010 dá suporte a esses formatos de ícone grandes, assim como o IconWorkshop Lite.

Detalhes sobre a integração **com Windows Games Explorer** são fornecidos no SDK do DirectX. O SDK do DirectX inclui um editor de GDF (arquivo de definição de jogo), bem como um exemplo de GDF incluído em GDFExampleBinary, um exemplo. Outro exemplo, GameUxInstallHelper, fornece rotinas para integrar a funcionalidade necessária aos sistemas de instalação existentes. O validador de arquivo de definição de gdftrace.exe de jogos fornece suporte de depuração para avaliar uma GDF. Consulte também "Windows Integração do Games Explorer" na Documentação do SDK do DirectX para C++.

Windows 7 introduz suporte para a segunda versão de um esquema para arquivos GDF. A nova versão inclui um método simplificado para criar tarefas de reprodução e suporte para notificações de atualização, provedores de serviços de jogos, estatísticas de jogo e RSS feeds para provedores de serviços de jogos. A versão mais recente do GameUxInstallHelper lida com todo o registro e o suporte herdado necessários para usar um arquivo GDF versão 2 com Windows Vista. Use as ferramentas e o código de exemplo do SDK do DirectX de agosto de 2009 ou posterior. É recomendável usar um arquivo GDF versão 2 para habilitar o suporte para feeds RSS, estatísticas de jogo e notificações de atualização. Além disso, consulte os exemplos ProviderGDFExampleBinary e GameStatisticsExample.

No Windows Vista Business Edition, Windows 7 Professional Edition e Edição Enterprise do Windows Vista e Windows 7, o link Jogos no menu Iniciar fica oculto. O Games Explorer ainda está disponível no menu Iniciar **clicando** em Todos os Programas e, em seguida, clicando em **Jogos**.

Para aplicativos associados instalados com seu jogo, mas não os próprios jogos, você pode criar grupos de programas, atalhos e ícones de área de trabalho do menu Iniciar em todas as versões do Windows, incluindo Windows Vista e Windows 7. Esses aplicativos associados devem passar os Jogos aplicáveis para Windows requisitos; Para obter detalhes, consulte [Diretrizes para produtos de middleware de jogos.](#guidelines-for-game-middleware-products) Os serviços de jogos são incentivados a se registrar com o Games Explorer como um Provedor de Jogos Windows 7. 1

</dd> </dl>

### <a name="12-support-family-safety--parental-controls"></a>1.2 Dar suporte a controles de segurança de família/pais

<dl> <dt>

<span id="Requirement"></span><span id="requirement"></span><span id="REQUIREMENT"></span>**Exigência**
</dt> <dd>

Os jogos devem dar suporte completo Windows Segurança da Família, aderindo às seguintes regras:

-   Os jogos não devem exigir que o usuário tenha credenciais administrativas para jogar. A instalação, a adoção de patch e a remoção podem exigir credenciais administrativas, sujeitos aos requisitos na seção 3. (Relacionado a isso é o requisito 2.1, Siga as Diretrizes de Controle de Conta de Usuário.)
-   Os jogos classificados por Windows de classificações com suporte, como ESRB e DRAI, devem incluir suas informações de classificações atribuídas no GDF (arquivo de definição de jogo). Todos os dados de classificações disponíveis devem ser incluídos em todas as versões localizadas do GDF, bem como na versão neutra para idioma.
-   Os jogos devem listar seus executáveis no GDF para fornecer uma boa experiência do usuário para Restrições Gerais de Aplicativo, a menos que o jogo use uma tecnologia antileição que cria executáveis nomeados aleatoriamente em runtime.
-   Os jogos devem chamar o **método VerifyAccess** da interface do Games Explorer durante a inicialização, se disponível, e sair se ele retornar \* pfHasAccess como FALSE.

</dd> <dt>

<span id="Rationale"></span><span id="rationale"></span><span id="RATIONALE"></span>**Lógica**
</dt> <dd>

Todos os jogos devem ser executados dentro do contexto de uma conta de usuário padrão para permitir que as contas controladas Windows controles dos pais executem o jogo. Os pais querem a capacidade de monitorar e controlar o acesso dos filhos aos jogos. Além disso, vários grupos do setor, governo e advocacy desejam maneiras melhores de permitir que os pais monitorem e controlem os jogos aos quais seus filhos são expostos. Em conjunto com a arquitetura oferecida pelo Games Explorer, a Microsoft fornece aos pais essa capacidade por meio Windows de pais.

Mesmo para jogos que não participam de um programa de quadro de classificações, exigir privilégios elevados cria uma experiência de jogo ruim para a maioria das contas de usuário. Esse é particularmente o caso se os Controles Dos Pais estão habilitados, o que exigiria que o pai insira a senha de administrador sempre que o jogo for lançado.

O Windows controles dos pais permite que os pais selecionem as classificações que eles acredita que são apropriadas para seus filhos. Os Controles Dos Pais são suportados por muitos dos sistemas de classificações em todo o mundo. Os Controles dos Pais também permitem que os pais restrinjam o acesso a jogos com base em Descritores de Conteúdo (se o sistema de classificação aplicável dá suporte a eles) e para permitir ou não permitir o acesso a jogos individuais.

A opção padrão do sistema de classificação para Windows Controles Dos Pais é baseada na configuração de localidade do sistema, mas pode ser modificada pelo usuário em **Opções** Regionais e **de Idioma no Painel de Controle**. Portanto, cada idioma com suporte deve fornecer todos os dados de classificações disponíveis para que o usuário tenha a liberdade de selecionar qualquer quadro de classificações desejado.

</dd> <dt>

<span id="Additional_Information"></span><span id="additional_information"></span><span id="ADDITIONAL_INFORMATION"></span>**Informações adicionais**
</dt> <dd>

Os jogos sem uma classificação ainda devem atender aos requisitos para dar suporte ao jogo como um Usuário Padrão e chamar **VerifyAccess**. Esses jogos são padrão para a categoria Não rateado, exibem o texto  "Sem Classificação Fornecida" no Games Explorer e estão sujeitos à configuração Restrições de Jogo em Controles Dos **Pais** para jogos não rateados. A **configuração padrão Restrições** é Permitir.

As informações de classificação na GDF serão ignoradas se o binário que contém não estiver assinado corretamente pelo Authenticode. Consulte o requisito 2.3.

O Editor de Arquivos de Definição de Jogo no SDK do DirectX inclui todos os sistemas de classificações com suporte e replicará corretamente essas informações para todas as versões localizadas do GDF, bem como uma versão neutra de idioma. A ferramenta GDFTrace decodificará e verificará todas as informações de classificações presentes. Use a versão de agosto de 2009 ou posterior dessas ferramentas.

O GDF para um provedor de jogos normalmente não contém informações de classificação e está sujeito às configurações de conteúdo não rateado.



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
<li>DRAI (Europa)</li>
<li>FINLÂNDIA (preterido)</li>
<li>PORTUGALI Portugal</li>
<li>DRAI/BBFC (Reino Unido)</li>
<li>USK (Alemanha)</li>
</ul></td>
</tr>
<tr class="even">
<td>Windows Vista com um service pack</td>
<td>Os service packs para Windows Vista adicionam suporte para o seguinte:<br/>
<ul>
<li>GRB (Coreia do Sul)</li>
<li>Descritores de conteúdo variantes do ESRB &quot; Variant &quot;</li>
</ul></td>
</tr>
<tr class="odd">
<td>Windows 7</td>
<td>Windows 7 dá suporte aos sistemas de classificações com suporte do Windows Vista e adiciona suporte para o seguinte: <br/>
<ul>
<li>CSRR (Taiwan)</li>
</ul></td>
</tr>
<tr class="even">
<td>Windows 8</td>
<td>Windows 8 dá suporte aos sistemas de classificações anteriores e adiciona suporte para o seguinte:<br/>
<ul>
<li>COB-AU (Austrália)</li>
<li>DJCTQ (Brasil)</li>
<li>PFB (África do Sul)</li>
<li>OFLC-NZ (Nova Zelândia)</li>
</ul>
Windows 8 o suporte para os seguintes sistemas preterido agora:<br/>
<ul>
<li>PEGI-FI (Finlândia)</li>
<li>OFLC (Austrália)</li>
</ul></td>
</tr>
</tbody>
</table>



 

> [!Note]  
> qualquer título que inclua os novos descritores de conteúdo do ESRB Windows Vista Service Pack 1 (SP1) mostrará como sem classificação no Windows Vista que não seja um service pack.

 

Os dados de classificação mais recentes são ignorados em versões de sistemas operacionais sem suporte para eles. A variante PEGI (Finlândia) agora foi preterida em favor do sistema de classificação padrão PEGI (Europa). O sistema OFLC agora foi preterido em favor de COB-AU para Austrália.

Para obter mais informações sobre como tornar um jogo compatível com privilégios de usuário padrão, consulte o artigo DirectX [controle de conta de usuário para desenvolvedores de jogos](/windows/desktop/DxTechArts/user-account-control-for-game-developers).

Consulte o requisito 1,1 para obter mais detalhes sobre o arquivo de definição de jogo (GDF).

</dd> </dl>

### <a name="13-support-rich-saved-games"></a>1,3 suporte a jogos salvos avançados

\[Este requisito foi desativado\]

### <a name="14-support-the-xbox-360-common-controller-for-windows-conditional-requirement"></a>1,4 suporte ao controlador comum do Xbox 360 para Windows \[ requisito condicional\]

<dl> <dt>

<span id="Requirement"></span><span id="requirement"></span><span id="REQUIREMENT"></span>**Obrigatoriedade**
</dt> <dd>

jogos que dão suporte a controladores de gamepad devem dar suporte ao Controle Xbox 360 para Windows usando a API [XInput](/windows/desktop/xinput/xinput-game-controller-apis-portal) . Se os periféricos do DirectInput também tiverem suporte, o DirectInput também poderá ser usado. No entanto, XInput deverá ser a API padrão se um dispositivo compatível com o Xbox 360 for usado.

Todas as referências a gatilhos e botões comuns do controlador devem usar os nomes do Xbox 360. consulte a lista de [terminologia do controlador comum do Xbox 360 para Windows](#xbox-360-common-controller-for-windows-terminology) para obter detalhes.

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

É recomendável que o DirectInput não seja usado para implementar controles de teclado ou mouse. os controles de teclado e mouse só devem ser implementados usando mensagens Windows e APIs do Win32. Para obter detalhes sobre como obter informações de movimentação de mouse de alta resolução sem usar o DirectInput, consulte [aproveitando High-Definition movimento do mouse](/windows/desktop/DxTechArts/taking-advantage-of-high-dpi-mouse-movement).

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

com o Windows área de trabalho 3d, uma taxa de proporção ou resolução específica não pode ser assumida, devido aos seguintes fatores:

-   Suporte para exibições de alto nível.
-   Maior participação no mercado de monitores widescreen.
-   implantações de HDTV para Windows Media Center.
-   Requisitos de acessibilidade.

</dd> <dt>

<span id="Additional_Information"></span><span id="additional_information"></span><span id="ADDITIONAL_INFORMATION"></span>**Informações adicionais**
</dt> <dd>

Idealmente, o jogo assume como padrão a taxa de proporção nativa da exibição. No entanto, a obtenção dessas informações de forma confiável pode ser um desafio, assim como uma solução mais geral, o jogo pode assumir que a área de trabalho está sendo executada na proporção de aspecto nativa. A resolução da área de trabalho pode ser obtida chamando [**EnumDisplaySettings**](/windows/desktop/api/winuser/nf-winuser-enumdisplaysettingsa) com \_ as configurações de enumeração do registro \_ .

para obter mais detalhes, consulte as seções taxa de proporção e Widescreen do artigo do DirectX [introdução à experiência de 10 pés para desenvolvedores de Windows jogos](/windows/desktop/DxTechArts/introduction-to-the-10-foot-experience-for-windows-game-developers).

</dd> </dl>

### <a name="16-support-launch-from-windows-media-center"></a>lançamento do suporte do 1,6 do Windows Media Center

\[Esse requisito foi desativado.\]

### <a name="17-direct3d-support"></a>Suporte do Direct3D 1,7

<dl> <dt>

<span id="Requirement"></span><span id="requirement"></span><span id="REQUIREMENT"></span>**Obrigatoriedade**
</dt> <dd>

Se o jogo usar o Direct3D, a versão mínima com suporte deverá ser o Direct3D 9 e o Direct3D deverá ser o renderizador padrão selecionado.

</dd> <dt>

<span id="Rationale"></span><span id="rationale"></span><span id="RATIONALE"></span>**Lógica**
</dt> <dd>

a arquitetura gráfica do Windows Vista e do Windows 7 core foi projetada em todo o Direct3D. O Direct3D 8 e versões anteriores têm suporte ao remapear interfaces herdadas.

O uso de versões do Direct3D mais recentes do que o Direct3D 9 é altamente incentivado. consulte os jogos para Windows Showcase S. 1. Exigir o Direct3D 10 ou o Direct3D 11 é totalmente compatível com o requisito 1,7.

</dd> </dl>

### <a name="18-enable-high-dpi-aware"></a>1,8 habilitar reconhecimento de DPI alto

<dl> <dt>

<span id="Requirement"></span><span id="requirement"></span><span id="REQUIREMENT"></span>**Obrigatoriedade**
</dt> <dd>

os jogos e seus instaladores devem ser executados corretamente sem problemas visuais quando o dimensionamento de pontos por polegada (DPI) estiver habilitado (testado com 144 DPI para 150% de dimensionamento na resolução de vídeo de 1600 1200) no Windows Vista e Windows 7.

Isso normalmente requer que o executável do jogo declare ser compatível com DPI. Isso é feito inserindo um elemento de manifesto: <dpiAware> true <dpiAware> .

</dd> <dt>

<span id="Rationale"></span><span id="rationale"></span><span id="RATIONALE"></span>**Lógica**
</dt> <dd>

Monitores LCD de alta qualidade são comuns à medida que o computador é exibido e eles parecem melhores quando controlados em suas resoluções nativas (geralmente 1280 1024, 1600 1200 e assim por diante). Os clientes que têm dificuldade de ler texto e ver as imagens nessa resolução geralmente definem suas áreas de trabalho de computador com uma resolução mais baixa e sofrem artefatos visuais do dimensionamento de LCD. em vez disso, os clientes podem deixar a resolução no tamanho nativo e alterar o DPI da exibição do Windows, tornando a aparência do item e do texto maior sem sacrificar a qualidade da imagem.

embora esse recurso esteja disponível em algum formato desde o Windows XP, raramente é habilitado por clientes ou por OEMs. Mais da metade de todas as exibições de computador hoje estão definidas para uma resolução mais baixa do que a resolução nativa do monitor, com base nos comentários do cliente. o Windows 7 torna esse recurso muito mais visível para os clientes durante a configuração inicial e ao alterar as configurações de exibição, incentivando-os a usar o dimensionamento de DPI em vez de alterar a resolução da área de trabalho.

</dd> <dt>

<span id="Additional_Information"></span><span id="additional_information"></span><span id="ADDITIONAL_INFORMATION"></span>**Informações adicionais**
</dt> <dd>

Em vez disso, a função [**SetProcessDPIAware**](/windows/desktop/api/winuser/nf-winuser-setprocessdpiaware) pode ser usada, se chamada antecipada no código de inicialização do processo. A adição ao manifesto é preferida, para garantir que não haja nenhuma condição de corrida com elementos de software (como DLLs) que possam ser inicializados antes do ponto de entrada principal ser chamado. observe que o **SetProcessDPIAware** está presente apenas no Windows Vista e Windows 7.

a adição do elemento manifest é fácil com Visual Studio 2005 e 2008; Crie um arquivo chamado dpiaware. manifest que contenha o seguinte texto:

``` syntax
            <assembly xmlns="urn:schemas-microsoft-com:asm.v1" manifestVersion="1.0" xmlns:asmv3="urn:schemas-microsoft-com:asm.v3">
            <asmv3:application>
            <asmv3:windowsSettings xmlns="http://schemas.microsoft.com/SMI/2005/WindowsSettings">
            <dpiAware>true</dpiAware>
            </asmv3:windowsSettings>
            </asmv3:application>
            </assembly>
```

em seguida, dentro de Visual Studio, adicione dpiware. manifest ao projeto. Verifique se **Inserir manifesto** está definido como **Sim** nas propriedades do projeto. Observe que as versões mais antigas da ferramenta de manifesto (Mt.exe) irão gerar um aviso falso com os elementos de manifesto com reconhecimento de DPI. para resolver isso, atualize Mt.exe para a versão mais recente do SDK do Windows.

Visual Studio 2010 inclui uma configuração nas propriedades do projeto, denominada **habilitar reconhecimento de DPI**, que elimina a necessidade de um arquivo como dpiaware. manifest. Localize **habilitar reconhecimento de DPI** expandindo **as propriedades de configuração** e a **ferramenta de manifesto** e, em seguida, selecionando **entrada & saída**.

em Windows, o modo de exibição tradicional usa como padrão 96 DPI, que era comum para monitores CRT.

Enquanto os aplicativos de tela inteira alteram a resolução de vídeo, geralmente usam as mensagens e métricas da janela ao configurar buffers e exibir retângulos. A virtualização de DPI faz com que esses modos de exibição de tela inteira pareçam cortados e a declaração de reconhecimento de DPI irá impedir esses problemas. Para obter mais informações, consulte [escrevendo DPI-Aware aplicativos Win32](../hidpi/high-dpi-desktop-application-development-on-windows.md).

</dd> </dl>

## <a name="security-and-compatibility"></a>Segurança e compatibilidade

**Resumo dos requisitos de segurança e compatibilidade**

**Benefícios do cliente**

os requisitos a seguir melhoram a segurança geral dos jogos e ajudam a garantir que eles trabalhem com Windows em diferentes arquiteturas, em configurações diferentes e em modos diferentes.

### <a name="21-follow-user-account-control-guidelines"></a>2,1 seguir as diretrizes de controle de conta de usuário

<dl> <dt>

<span id="Requirement"></span><span id="requirement"></span><span id="REQUIREMENT"></span>**Obrigatoriedade**
</dt> <dd>

Cada arquivo executável (ou seja, todos os arquivos que têm uma extensão .exe) deve conter um manifesto inserido que define seu nível de execução, incluindo a seguinte marca:

``` syntax
            <requestedExecutionLevel>
```

Por requisito 1,2, o jogo principal e o executável de Autorun devem ter o nível de execução de asInvoker para dar suporte a contextos de usuário padrão.

Os arquivos de dados do usuário que têm associações de arquivos registradas com o **Explorador de arquivos** devem ser colocados em uma subpasta da pasta especificada por CSIDL \_ pessoal (também chamada de **documentos** ou **meus documentos**). Todos os outros arquivos de dados de usuário devem ser armazenados em uma subpasta das pastas que são especificadas por CSIDl \_ local \_ AppData ou CSIDL \_ comum \_ AppData. (Esses diretórios ficam ocultos por padrão para usuários individuais e para todos os usuários.)

</dd> <dt>

<span id="Rationale"></span><span id="rationale"></span><span id="RATIONALE"></span>**Lógica**
</dt> <dd>

a experiência de Windows de um usuário será mais segura se os aplicativos forem executados somente com as permissões necessárias.

</dd> <dt>

<span id="Additional_Information"></span><span id="additional_information"></span><span id="ADDITIONAL_INFORMATION"></span>**Informações adicionais**
</dt> <dd>

Se apenas alguns recursos em um aplicativo exigirem privilégios administrativos (por exemplo, um aplicativo que precise configurar um firewall), o processo principal do aplicativo ainda deverá ser executado usando privilégios de usuário padrão. Recursos que exigem privilégios administrativos devem ser movidos para um processo separado, como um instalador ou utilitário de configuração.

Se privilégios administrativos não forem necessários, o XML do manifesto inserido deverá incluir o seguinte:

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

Se forem necessários privilégios administrativos, o XML do manifesto inserido deverá incluir o seguinte:

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

com o Visual Studio 2005, isso é facilmente inserido simplesmente adicionando um arquivo de manifesto (. manifest) que contém um dos blocos anteriores ao projeto e garantindo que o **manifesto de inserção** seja definido como **sim** na ferramenta de manifesto propriedades do projeto. para Visual Studio 2008 e 2010, as propriedades do UAC podem ser definidas diretamente nas propriedades do projeto para o vinculador na página do **arquivo de manifesto** . Observe que as versões mais antigas da ferramenta de manifesto (Mt.exe) geram um aviso falso com os elementos de manifesto do UAC. para resolver isso, atualize Mt.exe para a versão mais recente do SDK do Windows.

Consulte o requisito 3,1 para obter detalhes sobre os casos especiais de instalação, aplicação de patch e remoção.

As DLLs (bibliotecas de vínculo dinâmico) não exigem esses manifestos.

Para obter mais informações sobre o controle de conta de usuário, consulte [controle de conta de usuário para desenvolvedores de jogos](/windows/desktop/DxTechArts/user-account-control-for-game-developers).

</dd> </dl>

### <a name="22-support-windows-x64-versions"></a>suporte a 2,2 Windows versões x64

<dl> <dt>

<span id="Requirement"></span><span id="requirement"></span><span id="REQUIREMENT"></span>**Obrigatoriedade**
</dt> <dd>

para manter a compatibilidade com as edições de 64 bits do Windows, os jogos devem atender aos seguintes requisitos.

-   Os títulos e os instaladores de título não devem conter nenhum código de 16 bits nem contar com nenhum componente de 16 bits.
-   Se o jogo for dependente dos drivers do modo kernel para a operação, as versões x64 desses drivers deverão estar disponíveis. A instalação do jogo deve detectar e instalar os drivers e componentes adequados para as edições de 64 bits do Windows.

</dd> <dt>

<span id="Rationale"></span><span id="rationale"></span><span id="RATIONALE"></span>**Lógica**
</dt> <dd>

muitos usuários Windows Vista e Windows 7 executarão edições de 64 bits do sistema operacional durante a vida útil do produto, portanto, é crucial que os aplicativos sejam compatíveis com esse sistema operacional.

</dd> <dt>

<span id="Additional_Information"></span><span id="additional_information"></span><span id="ADDITIONAL_INFORMATION"></span>**Informações adicionais**
</dt> <dd>

Windows em Windows 64 (WOW64) permite que o código de 32 bits seja executado em edições de 64 bits do Windows, portanto, não é necessário que o aplicativo seja um código nativo de 64 bits em edições de 64 bits do Windows. O código de 16 bits não é executado em edições de 64 bits do Windows.

não é necessário manter a compatibilidade com o Windows XP Professional x64 Edition, mas é altamente recomendável.

Para obter detalhes, consulte [programação de 64 bits para desenvolvedores de jogos](/windows/desktop/DxTechArts/sixty-four-bit-programming-for-game-developers).

</dd> </dl>

### <a name="23-sign-files"></a>2,3 assinar arquivos

<dl> <dt>

<span id="Requirement"></span><span id="requirement"></span><span id="REQUIREMENT"></span>**Obrigatoriedade**
</dt> <dd>

Todos os arquivos de código executáveis (normalmente, arquivos com a extensão .exe ou .dll) devem ser assinados com um certificado Authenticode válido publicamente e devem ter uma URL de servidor de carimbo de data/hora válida para assinatura de produção.

se seu jogo usa Windows Installer, os arquivos do pacote do instalador (arquivos .msi) devem ser assinados.

</dd> <dt>

<span id="Rationale"></span><span id="rationale"></span><span id="RATIONALE"></span>**Lógica**
</dt> <dd>

Assinar um arquivo ajuda os usuários a decidir se devem confiar em um aplicativo e garante aos usuários que os arquivos não foram adulterados. Ele também permite que os aplicativos sejam executados corretamente em ambientes bloqueados.

</dd> <dt>

<span id="Additional_Information"></span><span id="additional_information"></span><span id="ADDITIONAL_INFORMATION"></span>**Informações adicionais**
</dt> <dd>

Para obter detalhes, consulte [assinatura Authenticode para desenvolvedores de jogos](/windows/desktop/DxTechArts/authenticode-signing-for-game-developers).

se seu jogo usa Windows Installer, recomendamos que você habilite o UAC/aplicação de patches de LUA, incluindo uma tabela MsiPatchCertificate. Para obter mais informações, consulte [aplicação de patch de UAC (controle de conta de usuário)](/windows/desktop/Msi/user-account-control--uac--patching).

Não recomendamos a assinatura de arquivos de gabinete (.cab), a menos que eles sejam relativamente pequenos (menos de 100 MB).

</dd> </dl>

### <a name="24-sign-drivers"></a>Drivers de assinatura 2,4

<dl> <dt>

<span id="Requirement"></span><span id="requirement"></span><span id="REQUIREMENT"></span>**Obrigatoriedade**
</dt> <dd>

Qualquer driver de modo kernel instalado pelo jogo deve ser assinado com um certificado de Authenticode válido publicamente.

qualquer driver de dispositivo de hardware de modo kernel instalado pelo jogo deve ter uma assinatura da Microsoft, que pode ser obtida do Windows WHQL (laboratórios de qualidade de hardware) ou do programa DRS (assinatura de confiabilidade do driver).

</dd> <dt>

<span id="Rationale"></span><span id="rationale"></span><span id="RATIONALE"></span>**Lógica**
</dt> <dd>

Mal gravados ou drivers de malware podem afetar seriamente a estabilidade e a segurança de um sistema. em edições de 64 bits do Windows Vista e Windows 7, os drivers não assinados não são carregados. essa política também pode ser habilitada para edições de 32 bits do Windows Vista e Windows 7.

</dd> <dt>

<span id="Additional_Information"></span><span id="additional_information"></span><span id="ADDITIONAL_INFORMATION"></span>**Informações adicionais**
</dt> <dd>

As versões nativas de 32 bits e 64 bits de todos os drivers de modo kernel são necessárias por requisito 2,2.

mais informações sobre programas de assinatura de driver da Microsoft podem ser encontradas no [portal do desenvolvedor de Hardware Windows](https://www.microsoft.com/whdc/winlogo/hwrequirements.mspx).

</dd> </dl>

### <a name="25-perform-proper-version-checking"></a>2,5 executar a verificação de versão apropriada

<dl> <dt>

<span id="Requirement"></span><span id="requirement"></span><span id="REQUIREMENT"></span>**Obrigatoriedade**
</dt> <dd>

os jogos não devem falhar na execução em sistemas operacionais futuros, conforme indicado pelas alterações no número de versão Windows, a menos que o contrato de licença de usuário final proíba o uso em sistemas operacionais futuros. Se o jogo for supostamente reprovado, ele deverá fazer isso normalmente exibindo uma mensagem apropriada ao usuário.

se Windows verificações de versão forem feitas, as APIs de verificação de versão ([**GetVersionEx**](/windows/desktop/api/sysinfoapi/nf-sysinfoapi-getversionexa) ou [**VerifyVersionInfo**](/windows/desktop/api/winbase/nf-winbase-verifyversioninfoa)) deverão ser usadas para verificar a versão do sistema operacional. As chaves do registro não devem ser lidas para determinar a versão.

As verificações explícitas de versão do tempo de execução do DirectX não devem estar presentes no jogo. Essas verificações de versão não devem estar presentes na instalação que inicia a instalação do DirectX Runtime (DirectSetup).

</dd> <dt>

<span id="Rationale"></span><span id="rationale"></span><span id="RATIONALE"></span>**Lógica**
</dt> <dd>

quando Windows usuários atualizam seus sistemas operacionais, eles não devem ser impedidos de reproduzir jogos atuais simplesmente porque o número de versão do Windows aumentou. os verificadores de versão mal escritos continuam a criar problemas de software que, caso contrário, funciona bem em versões mais recentes do Windows ou simplesmente com a adição de um service pack de Windows.

A lógica de comparação de verificação de versão frágil para o tempo de execução do DirectX criou várias instalações com falha quando ele é executado em versões diferentes do Windows. O número de versão do DirectX aplica-se apenas aos principais componentes do sistema operacional. Ele não se aplica aos componentes do SDK do DirectX lado a lado que são usados por muitos jogos.

</dd> <dt>

<span id="Additional_Information"></span><span id="additional_information"></span><span id="ADDITIONAL_INFORMATION"></span>**Informações adicionais**
</dt> <dd>

É muito comum ver OS instaladores verificar se há uma versão mínima do so. No entanto, essa verificação precisa ser feita com cuidado para garantir que ela teste para maior ou igual a, em vez de igualdade simples, bloqueando assim para uma versão específica do sistema operacional. Usar o teste de **HighVersionLie** do Application Verifier é uma maneira rápida e fácil de determinar como o seu instalador reagirá a uma alteração significativa no número de versão do sistema operacional.

O uso adequado do pacote de redistribuição do DirectX Runtime (instalação do DirectX) envolve sempre iniciá-lo durante a instalação, preferencialmente no modo silencioso. Isso permite que o código fornecido pela Microsoft execute todas as atualizações de versão necessárias. Ele também permite a instalação de quaisquer componentes opcionais do SDK do DirectX lado a lado, como D3DX, transação, MDX ou XInput.

Para obter as práticas recomendadas para implantar o tempo de execução do DirectX, consulte [instalação do DirectX para desenvolvedores de jogos](/windows/desktop/DxTechArts/directx-setup-for-game-developers).

é recomendável que os jogos que dão suporte ao Windows XP verifiquem um nível de service pack 2 ou superior, pois o service pack 2 (SP2) e o service pack 3 (SP3) fornecem melhorias de segurança significativas, um requisito simplificado de redistribuição de tempo de execução do DirectX e uma implantação extremamente ampla. as tecnologias mais modernas da Microsoft que dão suporte ao Windows XP exigem SP2 ou SP3 (XAudio2, jogos para Windows-LIVE e assim por diante).

</dd> </dl>

### <a name="26-support-concurrent-user-sessions"></a>2,6 suporte a sessões de usuário simultâneas

<dl> <dt>

<span id="Requirement"></span><span id="requirement"></span><span id="REQUIREMENT"></span>**Obrigatoriedade**
</dt> <dd>

Não é necessário que os jogos que dependem de gráficos 3D funcionem em uma conexão de área de trabalho remota, mas o usuário deve ser alertado quando o jogo falhar.

os jogos devem oferecer suporte a cenários de Windows multitarefa padrão ao aderir às seguintes regras:

-   Os jogos não devem bloquear o uso de sessões de usuário simultâneas.
-   Um jogo deve ser executado em uma nova sessão de usuário quando ele já estiver em execução em outra sessão.
-   O som do jogo em uma sessão de usuário não deve ser ouvido quando outro usuário estiver ativo em uma sessão diferente.
-   Os jogos devem dar suporte à troca rápida de usuário.
-   Os jogos não devem tentar desabilitar a alternância de tarefas padrão. Os jogos não devem desabilitar o atalho de teclado ALT + TAB. Os jogos têm permissão para desabilitar atalhos de teclado de acessibilidade, conforme descrito em [desabilitando teclas de atalho em jogos](/windows/desktop/DxTechArts/disabling-shortcut-keys-in-games).

</dd> <dt>

<span id="Rationale"></span><span id="rationale"></span><span id="RATIONALE"></span>**Lógica**
</dt> <dd>

Windows os usuários devem ser capazes de executar sessões simultâneas sem conflitos ou interrupções. esse é um cenário comum para um computador Windows que é compartilhado por uma família, roommates ou outros.

</dd> <dt>

<span id="Additional_Information"></span><span id="additional_information"></span><span id="ADDITIONAL_INFORMATION"></span>**Informações adicionais**
</dt> <dd>

Para testar se o jogo é iniciado em uma sessão remota, chame [**GetSystemMetrics**](/windows/desktop/api/winuser/nf-winuser-getsystemmetrics)(SM \_ REMOTESESSION). Um valor diferente de zero indica que a sessão é remota.

Para obter mais informações, consulte [troca rápida de usuário](/windows-hardware/drivers/display/fast-user-switching). Observe que a troca rápida de usuário ocorre se as restrições de tempo dos controles pais estiverem habilitadas quando o tempo do usuário estiver ativo. Consulte o requisito 1.2 para obter mais detalhes.

</dd> </dl>

### <a name="27-support-long-names"></a>2.7 Suporte a nomes longos

<dl> <dt>

<span id="Requirement"></span><span id="requirement"></span><span id="REQUIREMENT"></span>**Exigência**
</dt> <dd>

Se um jogo dá suporte à salvação de arquivos, ele deve ser capaz de salvar arquivos que têm nomes e caminhos longos. O jogo deve lidar corretamente com caracteres especiais do sistema de arquivos, como \\ / : \* ? " < >, em qualquer campo de entrada do usuário usado para criar nomes de arquivo ou caminhos.

Os jogos devem funcionar corretamente quando um usuário tem um nome de usuário longo.

</dd> <dt>

<span id="Rationale"></span><span id="rationale"></span><span id="RATIONALE"></span>**Lógica**
</dt> <dd>

Os jogadores estão acostumados a usar nomes longos em caminhos profundos com suporte pelo sistema operacional subjacente.

</dd> <dt>

<span id="Additional_Information"></span><span id="additional_information"></span><span id="ADDITIONAL_INFORMATION"></span>**Informações adicionais**
</dt> <dd>

Nomes longos são definidos como aqueles que contêm os valores máximos definidos no SDK Windows dados.

</dd> </dl>

## <a name="installation"></a>Instalação

**Resumo dos requisitos de segurança e compatibilidade**

**Benefícios do cliente**

Os clientes podem ter certeza de que os aplicativos serão instalados no Windows sem degradar o sistema operacional ou outros aplicativos se os aplicativos usarem métodos oficiais de distribuição de componentes do sistema. Uma experiência de instalação simplificada fornece uma experiência mais acessível e sem problemas para jogos.

### <a name="31-support-easy-installation"></a>3.1 Dar suporte à instalação fácil

<dl> <dt>

<span id="Requirement"></span><span id="requirement"></span><span id="REQUIREMENT"></span>**Exigência**
</dt> <dd>

Os jogos devem fornecer um caminho simplificado na interface do usuário de instalação implementando o seguinte:

-   Exibir um máximo de um prompt de EULA.
-   O caminho de instalação padrão deve ignorar todas as seleções para a instalação (como seleções de componente ou pasta de instalação), assumir as seleções padrão e, em seguida, executar o jogo ou o launcher após a instalação bem-sucedida, sem prompts adicionais. Se desejado, uma opção de instalação personalizada pode ser fornecida para opções de configuração avançadas.
-   Instale os componentes necessários do sistema operacional (como os runtimes do DirectX e do Visual C) usando os pacotes de redistribuição corretos da Microsoft. A instalação deve ser executada silenciosamente, sem solicitar e sem ser protegido por verificações de versão do componente.
-   Forneça a remoção **por meio de Programas** e Recursos **Painel de Controle** para o aplicativo de jogos e arquivos de trabalho gerados. Uma opção para excluir todos os arquivos de dados criados pelo usuário é recomendada. O processo de remoção deve garantir que todos os arquivos instalados sejam removidos e que todas as configurações (por exemplo, entradas de lista de exceção de firewall e chaves do Registro) sejam limpas. Os componentes do sistema operacional redistribuídos não devem ser removidos.
-   Se o jogo exigir que exceções sejam adicionadas ao firewall Windows, o processo de instalação poderá solicitar que os usuários informem que essa alteração é necessária. Esse prompt deve aparecer antes do início da instalação.

A instalação e a remoção podem exigir direitos administrativos. A adoção de patch pode exigir a solicitação de credenciais administrativas, dependendo da frequência da atualização. O jogo normal não deve exigir direitos administrativos, de acordo com o requisito 2.1 Siga as Diretrizes de Controle de Conta de Usuário.

</dd> <dt>

<span id="Rationale"></span><span id="rationale"></span><span id="RATIONALE"></span>**Lógica**
</dt> <dd>

A instalação fácil é uma filosofia de desenvolvimento de jogos centrada em Windows que foi projetada para simplificar e simplificar o processo, às vezes, entediante e confuso de instalação de jogos em computadores que executam Windows operacionais. A instalação fácil é habilitada utilizando um conjunto de tecnologias e práticas recomendadas que reduzem a complexidade desnecessária e o risco percebido de instalação de jogos em Windows computadores.

As principais metas são:

-   Reduza a quantidade de tempo para entrar no jogo e começar a jogar.
-   Reduza o número de caixas de diálogo e opções para muito poucas ou nenhuma para simplificar a experiência de instalação do jogo.

Algumas instalações tradicionais têm prompts que permitem instalações não funcionais, mesmo que o aplicativo pareça ter sido instalado com êxito. Por exemplo, um jogo pode exigir que um usuário aceite um EULA. O jogo é instalado e, em seguida, o EULA do DirectX é exibido. Esse EULA permite que os usuários se recusam e, portanto, ignoram a instalação do runtime do DirectX. Esse cenário pode resultar em um jogo que não é executado devido a componentes ausentes.

</dd> <dt>

<span id="Additional_Information"></span><span id="additional_information"></span><span id="ADDITIONAL_INFORMATION"></span>**Informações adicionais**
</dt> <dd>

Para obter mais informações sobre a instalação de jogos, técnicas de instalação de jogos não tradicionais, soluções de a patch compatíveis com UAC e tratamento de a patch frequente, consulte os seguintes artigos do DirectX:

-   [Simplificando a instalação do jogo](/windows/desktop/DxTechArts/simplifying-game-installation)
-   [Instalação sob demanda para jogos](/windows/desktop/DxTechArts/install-on-demand-for-games)
-   [Patching Game Software no Windows XP, Windows Vista e Windows 7](/windows/desktop/DxTechArts/patching-methods-in-windows-xp-and-vista)
-   [Práticas recomendadas de instalação para jogos online de multijogador maciço](/windows/desktop/DxTechArts/mmo-installation-best-practices)

> [!Note]  
> A remoção de arquivos de dados gerados específicos do usuário deve ser executada somente para o usuário atual e para locais comuns de usuário compartilhado. Não há nenhuma maneira robusta de verificar o sistema para remover arquivos específicos do usuário para outros usuários, mesmo que a remoção exija credenciais administrativas.

 

</dd> </dl>

### <a name="32-support-user-account-control-for-installation"></a>3.2 Dar suporte ao controle de conta de usuário para instalação

<dl> <dt>

<span id="Requirement"></span><span id="requirement"></span><span id="REQUIREMENT"></span>**Exigência**
</dt> <dd>

O instalador do jogo não deve supor que ele está em execução no mesmo contexto que o usuário. Locais específicos do usuário serão diferentes do instalador e do player até mesmo para sistemas de usuário único devido à elevação de credenciais de administrador. Portanto, quando um jogo é executado pela primeira vez, ele deve executar tarefas específicas do usuário, separadamente do processo de instalação.

A Windows de diálogo Exceção do firewall não deve aparecer quando um usuário hospeda ou insinte um jogo multijogador. Qualquer configuração necessária deve ser feita no momento da instalação. As instruções de instalação devem informar o usuário de que essa operação ocorrerá como parte da instalação.

O instalador do jogo deve fornecer um manifesto inserido que designa o nível de execução necessário, de acordo com o requisito 2.1 Siga as Diretrizes de Controle de Conta de Usuário.

Se o jogo for lançado pelo instalador após a conclusão da instalação, ele deverá ser lançado no contexto do usuário original.

</dd> <dt>

<span id="Rationale"></span><span id="rationale"></span><span id="RATIONALE"></span>**Lógica**
</dt> <dd>

Uma das maiores alterações no sistema operacional Windows no Windows Vista é a adição do UAC (Controle de Conta de Usuário), que executa aplicativos com privilégios reduzidos por padrão. Como resultado, os instaladores precisam gerenciar níveis de privilégio de acordo. Windows 7 também faz uso extensivo do UAC. Embora Windows 7 aprimora a experiência do usuário do UAC, os instaladores ainda devem atender aos mesmos requisitos do Windows Vista para funcionar corretamente, sem depender do comportamento de virtualização potencialmente confuso.

O UAC está ativo por padrão no Windows Vista e Windows 7, e a grande maioria dos clientes (88% ou mais, com base nos comentários) deixa esse recurso habilitado.

</dd> <dt>

<span id="Additional_Information"></span><span id="additional_information"></span><span id="ADDITIONAL_INFORMATION"></span>**Informações adicionais**
</dt> <dd>

Para obter mais detalhes sobre como configurar o firewall Windows, consulte o artigo do DirectX [Windows Firewall para](/windows/desktop/DxTechArts/games-and-firewalls) Desenvolvedores de Jogos e o exemplo FirewallInstallHelper.

O lançamento padrão do jogo no final do processo de instalação não atenderá ao último aspecto desse requisito se a instalação for lançada por um usuário padrão e se o processo de instalação exigir privilégios administrativos (ou seja, solicitará credenciais de administrador). Ele também herda privilégios administrativos, que é um risco de segurança potencial. Em vez disso, um carregador de inicialização de instalação deve iniciar o jogo depois de retornar de uma invocação bem-sucedida do instalador. Para obter mais informações, consulte o artigo da MSDN Magazine Ensinar seus aplicativos a reproduzirem-se bem com Windows controle de conta de usuário [do Vista](/archive/msdn-magazine/2007/january/teach-your-apps-to-work-with-windows-vista-user-account-control).

</dd> </dl>

### <a name="33-install-to-correct-folders"></a>3.3 Instalar para corrigir pastas

<dl> <dt>

<span id="Requirement"></span><span id="requirement"></span><span id="REQUIREMENT"></span>**Exigência**
</dt> <dd>

Os jogos instalados para todos os usuários devem ser instalados na pasta Arquivos de Programas por padrão. Os dados do usuário devem ser gravados quando o jogo é executado pela primeira vez, não durante a instalação.

</dd> <dt>

<span id="Rationale"></span><span id="rationale"></span><span id="RATIONALE"></span>**Lógica**
</dt> <dd>

Os usuários devem ter a flexibilidade de instalar aplicativos onde eles precisam. Eles também devem ter uma experiência consistente e segura com o local padrão dos arquivos.

</dd> <dt>

<span id="Additional_Information"></span><span id="additional_information"></span><span id="ADDITIONAL_INFORMATION"></span>**Informações adicionais**
</dt> <dd>

Os jogos podem usar os vários locais de pastas conhecidos (como os especificados por CSIDL LOCAL APPDATA e \_ \_ CSIDL \_ COMMON APPDATA) para armazenar quantidades significativas de dados de jogos e dar suporte a arquivos executáveis para implementar cenários avançados de instalação sob demanda e aplicação de \_ patch.

Como a instalação pode exigir elevação para uma conta de usuário diferente durante o processo de instalação de todos os usuários, não há nenhum local de usuário correto no qual armazenar dados no momento da instalação. Além disso, se a criptografia de arquivos estiver habilitada, os arquivos criptografados só poderão ser acessados pela conta de usuário que os criou.

</dd> </dl>

### <a name="34-install-windows-resources-properly"></a>3.4 Instalar recursos Windows corretamente

<dl> <dt>

<span id="Requirement"></span><span id="requirement"></span><span id="REQUIREMENT"></span>**Exigência**
</dt> <dd>

Os aplicativos não devem tentar instalar arquivos ou chaves do Registro que são protegidos pelo WINDOWS Proteção de Recursos (WRP). Se o aplicativo exigir versões mais recentes dos componentes do sistema, ele deverá atualizar esses componentes usando um Microsoft Service Pack ou um pacote de instalação aprovado pela Microsoft que contém o componente do sistema. Os componentes do sistema nunca devem ser reempacodados.

</dd> <dt>

<span id="Rationale"></span><span id="rationale"></span><span id="RATIONALE"></span>**Lógica**
</dt> <dd>

Windows A WRP (Proteção de Recursos) foi projetada para garantir que os recursos protegidos do sistema sejam atualizados somente usando mecanismos de atualização ou instalação aprovados pela Microsoft. A WRP melhora a confiabilidade do sistema, garantindo que os resultados de uma instalação sejam previsíveis.

</dd> <dt>

<span id="Additional_Information"></span><span id="additional_information"></span><span id="ADDITIONAL_INFORMATION"></span>**Informações adicionais**
</dt> <dd>

A WRP é a sucessora Windows Proteção de Arquivos, que protege a maioria dos componentes do sistema instalados na pasta Windows. A WRP protege a maioria das chaves do Registro que armazenam configurações para criação de objeto COM. Ele também reserva determinadas pastas para uso exclusivo pelo sistema operacional. As tentativas de acessar recursos protegidos normalmente resultam em um erro de negação de acesso.

Para obter detalhes das práticas recomendadas quando o runtime do DirectX é implantado com um jogo, consulte o artigo Instalação do DirectX para [desenvolvedores de jogos](/windows/desktop/DxTechArts/directx-setup-for-game-developers).

</dd> </dl>

### <a name="35-avoid-reboots-during-installation"></a>3.5 Evitar reinicializações durante a instalação

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



| Name                                          | Descrição                                                                                                 |
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
| <span id="Games_for_Windows_and_DirectX_SDK_Blog"></span><span id="games_for_windows_and_directx_sdk_blog"></span><span id="GAMES_FOR_WINDOWS_AND_DIRECTX_SDK_BLOG"></span>Blog de jogos para Windows sdk do DirectX e do DirectX<br/> | [Jogos para Windows e SDK do DirectX](https://walbourn.github.io/)<br/>                                                                           |
| <span id="Additional_DirectX_Articles"></span><span id="additional_directx_articles"></span><span id="ADDITIONAL_DIRECTX_ARTICLES"></span>Artigos adicionais do DirectX<br/>                                             | [Artigos técnicos do DirectX](/windows/desktop/DxTechArts/dx9-technical-articles)<br/>                                                                                    |



 

 

