---
title: Instalação do DirectX para desenvolvedores de jogos
description: Este artigo destina-se a abordar algumas das perguntas mais comuns sobre o tempo de execução do DirectX e o uso do DirectSetup para instalar o DirectX.
ms.assetid: 2ab439be-8d99-bcf8-89af-d4274e044c88
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a9c0faf346bd8793e61a89128ce573e29b7a8267
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104008026"
---
# <a name="directx-installation-for-game-developers"></a>Instalação do DirectX para desenvolvedores de jogos

Este artigo destina-se a abordar algumas das perguntas mais comuns sobre o tempo de execução do DirectX e o uso do DirectSetup para instalar o DirectX.

-   [Tempo de execução do DirectX](#directx-runtime)
-   [Número de versão do DirectX](#directx-version-number)
-   [Bibliotecas do DirectX](#directx-libraries)
-   [Instalação do DirectX pelo instalador do jogo](#installation-of-directx-by-the-games-installer)
-   [Pacotes de instalação pequenos](#small-installation-packages)
-   [Implantação interna do tempo de execução de depuração DirectX](#internal-deployment-of-the-debug-directx-runtime)

> [!IMPORTANT]
> O SDK do DirectX herdado está no fim da vida útil, mas ainda está disponível para dar suporte a jogos, tutoriais e projetos antigos. Novos projetos não devem usá-lo. O uso do SDK do DirectX herdado requer o uso do DirectSetup preterido para componentes como D3DX9, D3DX10, D3DX11, XAudio 2,7, XInput 1,3 e transação. Para obter mais detalhes sobre o estado atual do SDK do DirectX, consulte [onde está o SDK do DirectX?](../directx-sdk--august-2009-.md)e a postagem do blog [não tão direcionada para a instalação direta](https://walbourn.github.io/not-so-direct-setup/).

## <a name="directx-runtime"></a>Tempo de execução do DirectX

O tempo de execução do DirectX consiste em componentes principais e componentes opcionais.

Os componentes principais, como Direct3D e DirectInput, são considerados parte do sistema operacional. Os componentes principais do DirectX 9.0 c não foram alterados desde a atualização 2004 do SDK do DirectX, e eles correspondem ao que foi lançado com o Microsoft Windows XP SP2, Windows XP pro x64 Edition e Windows Server 2003 SP1. O Windows Vista inclui o DirectX 10, que dá suporte ao Windows Display Driver Model (WDDM) e ao Direct3D 10. x. O Windows 7 e o Windows Vista (consulte [KB971644](https://support.microsoft.com/kb/971644)) dão suporte ao DirectX 11, que dá suporte ao Direct3D 11, Direct2D, DirectWrite, ao dispositivo de renderização de software WARP10 e aos níveis de recursos do 10level9. Consulte [APIs de gráficos no Windows](/windows/desktop/direct3darticles/graphics-apis-in-windows-vista) para obter mais detalhes.

Os componentes opcionais são liberados nas atualizações do SDK do DirectX e incluem D3DX, transação, XAudio2, XINPUT, DirectX gerenciado e outros componentes desse tipo. Muitos dos componentes opcionais são atualizados regularmente para integrar os comentários dos clientes e expor novos recursos.

## <a name="directx-version-number"></a>Número de versão do DirectX

O número de versão do DirectX, como 9.0 c, refere-se apenas à versão dos componentes principais, como Direct3D, DirectInput ou DirectSound. Esse número não abrange as versões dos vários componentes opcionais que são lançados no SDK do DirectX, como D3DX, transação, XINPUT e assim por diante.

Em termos gerais, o número de versão do DirectX não é significativo, exceto como referência rápida para os bits principais de tempo de execução. Esse número não deve ser usado para verificar se o tempo de execução correto do DirectX já está instalado, pois ele não leva em conta os componentes opcionais do DirectX.

## <a name="directx-libraries"></a>Bibliotecas do DirectX

No passado, os componentes opcionais do SDK do DirectX, incluindo D3DX, foram lançados como bibliotecas estáticas. No entanto, agora eles são lançados como bibliotecas de forma dinâmica (DLL) devido à maior demanda para melhores práticas de segurança. DLLs permitem a manutenção de código lançado anteriormente. Se esses componentes foram implantados como bibliotecas estáticas, não haveria como a Microsoft abordar os problemas de segurança encontrados após o lançamento.

À medida que os recursos são adicionados ou alterados para os componentes opcionais, os nomes das DLLs correspondentes também são alterados para garantir que nenhuma regressão seja causada a jogos existentes que estejam usando componentes liberados. As DLLs de cada componente residem lado a lado, e os desenvolvedores de jogos podem escolher exatamente qual versão de DLL o jogo usa Vinculando-se à biblioteca de importação correspondente.

Embora a garantia de que as DLLs estejam instaladas em um sistema não seja tão fácil quanto simplesmente vincular a bibliotecas estáticas, algumas alterações foram feitas no SDK do DirectX para resolver o problema do modelo de DLL:

-   O DirectX redistribuível pode ser configurado para conter apenas os componentes que seu aplicativo precisa para minimizar os tamanhos de mídia e distribuição.
-   A pasta redistribuível, arquivos de programa \\ \\ Redist SDK \\ do DirectX, agora contém um arquivo de gabinete (. cab) para cada componente opcional possível, para que você não precise procurar um SDK mais antigo para encontrá-los.
-   Instalar o próprio SDK instala todos os componentes opcionais possíveis.
-   Um DirectX redistribuível que contém todos os componentes opcionais está disponível como um instalador baseado na Web e como um pacote que pode ser baixado; consulte o DirectX Developer Center ([DirectX](/previous-versions/windows/apps/hh452744(v=win.10))) para obter mais informações.

## <a name="installation-of-directx-by-the-games-installer"></a>Instalação do DirectX pelo instalador do jogo

> [!Note]  
> Consulte [implantação do Direct3D 11 para desenvolvedores de jogos](/windows/desktop/direct3darticles/direct3d11-deployment).

 

Veja a seguir as práticas recomendadas para adicionar a instalação do DirectX ao instalador de um jogo:



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Termo</th>
<th>Descrição</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span id="Install_the_redistributable_components_every_time.__"></span><span id="install_the_redistributable_components_every_time.__"></span><span id="INSTALL_THE_REDISTRIBUTABLE_COMPONENTS_EVERY_TIME.__"></span>Instale os componentes redistribuíveis a cada vez. <br/></td>
<td>O processo de instalação de um jogo deve instalar os componentes redistribuíveis do DirectX durante cada instalação única, sem permitir que os usuários o recusem. Se você permitir a recusa, alguns usuários descobrirão que eles não precisam e, se realmente fizerem, o jogo não será executado. <br/></td>
</tr>
<tr class="even">
<td><span id="Let_the_DirectX_installer_check_for_optional_components.__"></span><span id="let_the_directx_installer_check_for_optional_components.__"></span><span id="LET_THE_DIRECTX_INSTALLER_CHECK_FOR_OPTIONAL_COMPONENTS.__"></span>Deixe que o instalador do DirectX Verifique se há componentes opcionais. <br/></td>
<td>Não presuma que os componentes opcionais mais recentes já estejam instalados em um sistema, porque Windows Update e service packs não fornecem nenhum dos componentes opcionais do DirectX. Você deve instalar o tempo de execução do DirectX executando dxsetup.exe diretamente ou chamando DirectSetup. <br/></td>
</tr>
<tr class="odd">
<td><span id="Set_up_silently.__"></span><span id="set_up_silently.__"></span><span id="SET_UP_SILENTLY.__"></span>Configurar silenciosamente. <br/></td>
<td>Inicie a instalação no modo silencioso para que os usuários não ignorem a atualização do tempo de execução do DirectX acidentalmente. Você pode fazer isso iniciando dxsetup.exe com o seguinte comando: <br/>
<pre class="syntax" data-space="preserve"><code>   path-to-redistributable\dxsetup.exe /silent</code></pre>
ou chamando DirectSetup e não mostrando nenhuma interface do usuário. <br/></td>
</tr>
<tr class="even">
<td><span id="Combine_EULA_acceptances.__"></span><span id="combine_eula_acceptances.__"></span><span id="COMBINE_EULA_ACCEPTANCES.__"></span>Combine as aceitações de EULA. <br/></td>
<td>Se você solicitar que o usuário aceite um EULA, combine-o com a solicitação de aceitação do EULA do DirectX ao instalar no modo silencioso para que a solicitação de aceitação de EULAs ocorra apenas uma vez. A solicitação deve ocorrer antes de você instalar qualquer coisa para que, se o usuário não aceitar, você não acabe com uma instalação parcial e com falha. <br/></td>
</tr>
<tr class="odd">
<td><span id="Just_run_dxsetup_or_call_DirectSetup.__"></span><span id="just_run_dxsetup_or_call_directsetup.__"></span><span id="JUST_RUN_DXSETUP_OR_CALL_DIRECTSETUP.__"></span>Basta executar DxSetup ou chamar DirectSetup. <br/></td>
<td>Como o número de versão do DirectX não se refere a nada, exceto os principais componentes do DirectX, não verifique uma versão instalada antes de executar dxsetup.exe ou chamar DirectSetup. Além disso, não verifique a existência de um arquivo para testar se um componente opcional já está instalado, pois isso geralmente não determinará corretamente quando um componente existe, mas precisa ser atualizado. No entanto, o pacote de instalação do DirectX determinará isso rapidamente e executará a ação certa. <br/></td>
</tr>
</tbody>
</table>



 

## <a name="small-installation-packages"></a>Pacotes de instalação pequenos

Você pode criar pacotes de instalação menores para o DirectX removendo o conteúdo da pasta redistribuível do DirectX para o conjunto mínimo de arquivos necessários para fazer o instalador funcionar e reter quaisquer componentes adicionais usados por seu jogo.

Dependendo de suas especificações mínimas, talvez nem seja necessário incluir os arquivos de gabinete do DirectX 9.0 c básico na pasta redistribuível da mídia de instalação. Uma grande maioria das instalações do Windows XP tem o Service Pack 2, que inclui os componentes principais do DirectX 9.0 c, portanto, a operação de instalação do DirectX será muito rápida e não exigirá uma reinicialização. O menor pacote que pode ser criado é de cerca de 3 MB e pode ser compactado para cerca de metade desse tamanho. Um pacote como este contém uma versão da DLL D3DX e requer que o DirectX 9.0 c já esteja presente.

O conjunto mínimo de arquivos que são necessários para criar um pacote redistribuível são os seguintes arquivos, localizados na pasta redist do SDK do DirectX (arquivos de programa \\ Redist SDK do DirectX \\ \) :

-   dxsetup.exe
-   dsetup32.dll
-   dsetup.dll
-   dxupdate.cab

Adicione a esses arquivos de gabinete para os componentes que você deseja instalar. Se você precisar que os usuários do seu aplicativo já tenham o DirectX 9.0 c, não precisará incluir DirectX.cab ou dxnt.cab, que constituem a maior parte do requisito de espaço. O DirectX.cab só é necessário para o Windows 98 e o Windows ME; O dxnt.cab só é necessário para o Windows 2000, o Windows XP e o Windows XP SP1; e o dxdllreg \_x86.cab só é necessário para o windows 2000, Windows XP RTM, Windows XP SP1 e Windows Server 2003 RTM. Além disso, se você não usar o DirectShow ou se presumir que ele já está instalado, poderá omitir BDA.cab, BDANT.cab e BDAXP.cab.

> [!Note]  
> Você pode assumir que os usuários do seu aplicativo já têm o DirectX 9.0 c se ele foi instalado por uma versão anterior do seu aplicativo, você força os usuários a atualizar manualmente por meio do instalador da Web ou supõe que eles têm o Windows XP SP2 ou posterior.

 

Continuando com este exemplo, se você estiver usando apenas a versão de 32 bits do D3DX para abril de 2006, você poderá adicionar Apr2006 \_ d3dx9 \_ 30 \_x86.cab. Se você estiver usando a versão de 32 de agosto de 2006 32 bits do XINPUT, adicione Aug2006 \_ XINPUT \_x86.cab.

Se você tiver um aplicativo nativo de 64 bits, precisará adicionar as \_ versões x64. No entanto, se você tiver um aplicativo de 32 bits em execução em um sistema operacional de 64 bits, as versões de 32 bits das DLLs funcionarão.

Em seguida, você pode distribuir esse pacote de arquivos e iniciar o DirectSetup no modo silencioso ou executar dxsetup.exe no Shell de comando no modo silencioso. Lembre-se de não proteger esse pacote por qualquer verificação de versão dos arquivos e certifique-se de que os usuários não possam optar por executar a instalação do DirectX. Qualquer um desses eventos cria um processo de instalação do falível.

## <a name="internal-deployment-of-the-debug-directx-runtime"></a>Implantação interna do tempo de execução de depuração DirectX

Os tempos de execução de depuração dos componentes do DirectX são instalados quando o SDK do DirectX é instalado, mas instalar o SDK em cada computador de teste pode ser trabalhoso. Você precisa projetar seu processo de instalação para copiar as DLLs de tempo de execução de depuração de arquivos de programas \\ Microsoft DirectX SDK \\ Developer Runtime \\ Architecture \\ para Windows \\ System32 \\ ou para a pasta do jogo.

No entanto, é altamente recomendável que você não simplesmente copie as DLLs de tempo de execução liberadas porque é fácil esquecer de removê-las para o produto final. Em vez disso, coloque os arquivos de instalação do DirectX em uma pasta compartilhada e execute a instalação silenciosamente da pasta compartilhada.

## <a name="desktop-bridge-applications"></a>Aplicativos de ponte de desktop 

Os aplicativos de ponte de desktop que usam D3DX9, D3DX10, D3DX11, XAudio 2,7, XInput 1,3 ou transação devem baixar o [Microsoft. DirectX. x86](https://download.microsoft.com/download/c/c/2/cc291a37-2ebd-4ac2-ba5f-4c9124733bf1/UAPSignedBinary_Microsoft.DirectX.x86.appx) ou a estrutura [Microsoft. DirectX. x64](https://download.microsoft.com/download/c/c/2/cc291a37-2ebd-4ac2-ba5f-4c9124733bf1/UAPSignedBinary_Microsoft.DirectX.x64.appx) para implantar esses componentes herdados do SDK do DirectX. Como alternativa, você pode remover todas essas dependências &mdash; (consulte o [Guia do desenvolvedor para a versão redistribuível do XAudio 2,9](../xaudio2/xaudio2-redistributable.md)e as postagens de blog em [vida sem D3DX](https://walbourn.github.io/living-without-d3dx/) e [XInput e Windows 8](https://walbourn.github.io/xinput-and-windows-8/)).