---
title: Instalação do DirectX para desenvolvedores de jogos
description: Este artigo destina-se a abordar algumas das perguntas comuns sobre o runtime do DirectX e usar o DirectSetup para instalar o DirectX.
ms.assetid: 2ab439be-8d99-bcf8-89af-d4274e044c88
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0509084232f1dcfe63a7d956516aa723f8cd724b
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122477282"
---
# <a name="directx-installation-for-game-developers"></a>Instalação do DirectX para desenvolvedores de jogos

Este artigo destina-se a abordar algumas das perguntas comuns sobre o runtime do DirectX e usar o DirectSetup para instalar o DirectX.

-   [DirectX Runtime](#directx-runtime)
-   [Número de versão do DirectX](#directx-version-number)
-   [Bibliotecas DirectX](#directx-libraries)
-   [Instalação do DirectX pelo Instalador do Jogo](#installation-of-directx-by-the-games-installer)
-   [Pacotes de instalação pequenos](#small-installation-packages)
-   [Implantação interna do Runtime do DirectX de depuração](#internal-deployment-of-the-debug-directx-runtime)

> [!IMPORTANT]
> O SDK do DirectX herdado está no fim da vida útil, mas ainda está disponível para dar suporte a jogos, tutoriais e projetos antigos. Novos projetos não devem usá-lo. Usar o SDK do DirectX herdado requer o uso do DirectSetup preterido para componentes como D3DX9, D3DX10, D3DX11, XAudio 2.7, XInput 1.3 e XACT. Para obter mais detalhes sobre o estado atual do SDK do DirectX, consulte Onde está o [SDK do DirectX?](../directx-sdk--august-2009-.md)e a postagem no blog [Configuração](https://walbourn.github.io/not-so-direct-setup/)Não Tão Direta .

## <a name="directx-runtime"></a>DirectX Runtime

O runtime do DirectX consiste em componentes principais e componentes opcionais.

Os componentes principais, como Direct3D e DirectInput, são considerados parte do sistema operacional. Os componentes principais do DirectX 9.0c não foram alterados desde a Atualização de Verão de 2004 do SDK do DirectX e eles corresponderam ao que foi lançado com o Microsoft Windows XP SP2, o Windows XP Pro x64 Edition e o Windows Server 2003 SP1. Windows O Vista inclui o DirectX 10, que dá suporte Windows WDDM (Modelo de Driver de Exibição) e Direct3D 10.x. Windows 7 e Windows Vista (consulte [KB971644](https://support.microsoft.com/kb/971644)) são compatíveis com o DirectX 11, que dá suporte ao Direct3D 11, Direct2D, DirectWrite, ao dispositivo de renderização de software WARP10 e aos níveis de recurso 10level9. Consulte [APIs de gráficos Windows](/windows/desktop/direct3darticles/graphics-apis-in-windows-vista) para obter mais detalhes.

Os componentes opcionais são lançados em atualizações do SDK do DirectX e incluem D3DX, XACT, XAudio2, XINPUT, Managed DirectX e outros componentes desse tipo. Muitos dos componentes opcionais são atualizados regularmente para integrar comentários do cliente e expor novos recursos.

## <a name="directx-version-number"></a>Número de versão do DirectX

O número de versão do DirectX, como 9.0c, refere-se apenas à versão dos componentes principais, como Direct3D, DirectInput ou DirectSound. Esse número não abrange as versões dos vários componentes opcionais lançados no SDK do DirectX, como D3DX, XACT, XINPUT e assim por diante.

Em termos gerais, o número de versão do DirectX não é significativo, exceto como uma referência rápida aos bits de tempo de run-time principais. Esse número não deve ser usado para verificar se o runtime do DirectX correto já está instalado, porque ele não leva em conta os componentes opcionais do DirectX.

## <a name="directx-libraries"></a>Bibliotecas DirectX

No passado, os componentes opcionais do SDK do DirectX, incluindo D3DX, eram lançados como bibliotecas estáticas. No entanto, agora eles são lançados como DLL (bibliotecas dinâmicas) devido ao aumento da demanda por melhores práticas de segurança. As DLLs permitem a manutenção do código lançado anteriormente. Se esses componentes foram implantados como bibliotecas estáticas, não haverá como a Microsoft resolver problemas de segurança encontrados após o lançamento.

À medida que os recursos são adicionados ou alterados para os componentes opcionais, os nomes das DLLs correspondentes também são alterados para garantir que nenhuma regressão seja causada a jogos existentes que estão usando componentes lançados. As DLLs para cada componente ao vivo lado a lado e os desenvolvedores de jogos podem escolher exatamente qual versão de DLL o jogo usa vinculando-se à biblioteca de importação correspondente.

Embora garantir que as DLLs sejam instaladas em um sistema não seja tão fácil quanto simplesmente vincular a bibliotecas estáticas, algumas alterações foram feitas no SDK do DirectX para resolver o problema do modelo de DLL:

-   Os redistribuíveis do DirectX podem ser configurados para conter somente os componentes que seu aplicativo requer para minimizar os tamanhos de mídia e distribuição.
-   A pasta redistribuível, o Redist do SDK do DirectX dos Arquivos de Programas, agora contém um arquivo de gabinete (.cab) para cada componente opcional possível, portanto, você não precisa pesquisar um SDK mais antigo para \\ \\ \\ encontrá-los.
-   Instalar o próprio SDK instala todos os componentes opcionais possíveis.
-   Um directX redistribuível que contém todos os componentes opcionais está disponível como um instalador baseado na Web e como um pacote baixável; consulte o DirectX Developer Center ([DirectX](/previous-versions/windows/apps/hh452744(v=win.10))) para obter mais informações.

## <a name="installation-of-directx-by-the-games-installer"></a>Instalação do DirectX pelo Instalador do Jogo

> [!Note]  
> Consulte [Implantação do Direct3D 11 para desenvolvedores de jogos.](/windows/desktop/direct3darticles/direct3d11-deployment)

 

Veja a seguir as práticas recomendadas para adicionar a instalação do DirectX ao instalador de um jogo:




| Termo | Descrição | 
|------|-------------|
| <span id="Install_the_redistributable_components_every_time.__"></span><span id="install_the_redistributable_components_every_time.__"></span><span id="INSTALL_THE_REDISTRIBUTABLE_COMPONENTS_EVERY_TIME.__"></span>Instale os componentes redistribuíveis toda vez. <br /> | O processo de instalação de um jogo deve instalar os componentes redistribuíveis do DirectX durante cada única instalação sem permitir que os usuários o optem. Se você permitir a aceitação, alguns usuários adivinharão que não precisam dela e, se realmente o fizerem, o jogo não será executado. <br /> | 
| <span id="Let_the_DirectX_installer_check_for_optional_components.__"></span><span id="let_the_directx_installer_check_for_optional_components.__"></span><span id="LET_THE_DIRECTX_INSTALLER_CHECK_FOR_OPTIONAL_COMPONENTS.__"></span>Deixe o instalador do DirectX verificar se há componentes opcionais. <br /> | Não suponha que os componentes opcionais mais recentes já estão instalados em um sistema, porque Windows Update e Service Packs não fornecem nenhum dos componentes opcionais do DirectX. Você deve instalar o runtime do DirectX executando o dxsetup.exe diretamente ou chamando DirectSetup. <br /> | 
| <span id="Set_up_silently.__"></span><span id="set_up_silently.__"></span><span id="SET_UP_SILENTLY.__"></span>Configurar silenciosamente. <br /> | Iniciar a instalação no modo silencioso para que os usuários não ignorem acidentalmente a atualização do runtime do DirectX. Você pode fazer isso iniciando dxsetup.exe com o seguinte comando: <br /><pre class="syntax" data-space="preserve"><code>   path-to-redistributable\dxsetup.exe /silent</code></pre>ou chamando DirectSetup e não mostrando nenhuma interface do usuário. <br /> | 
| <span id="Combine_EULA_acceptances.__"></span><span id="combine_eula_acceptances.__"></span><span id="COMBINE_EULA_ACCEPTANCES.__"></span>Combinar aceitaçãos de EULA. <br /> | Se você solicitar que o usuário aceite um EULA, combine-o com solicitando a aceitação do EULA do DirectX ao instalar no modo silencioso para que a solicitação de aceitação de EULAs ocorra apenas uma vez. A solicitação deve acontecer antes de você instalar qualquer coisa para que, se o usuário não aceitar, você não acabará com uma instalação parcial e com falha. <br /> | 
| <span id="Just_run_dxsetup_or_call_DirectSetup.__"></span><span id="just_run_dxsetup_or_call_directsetup.__"></span><span id="JUST_RUN_DXSETUP_OR_CALL_DIRECTSETUP.__"></span>Basta executar dxsetup ou chamar DirectSetup. <br /> | Como o número de versão do DirectX não se refere a nada, exceto os componentes principais do DirectX, não verifique uma versão instalada antes de executar dxsetup.exe ou chamar DirectSetup. Além disso, não verifique a existência de um arquivo para testar se um componente opcional já está instalado, pois isso geralmente não determinará corretamente quando um componente existe, mas precisa ser atualizado. No entanto, o pacote de instalação do DirectX determinará isso rapidamente e executará a ação correta. <br /> | 




 

## <a name="small-installation-packages"></a>Pacotes de instalação pequenos

Você pode criar pacotes de instalação menores para o DirectX remoção do conteúdo da pasta redistribuível do DirectX para o conjunto mínimo de arquivos necessários para fazer com que o instalador funcione e mantendo todos os componentes adicionais que seu jogo usa.

Dependendo de suas especificações mínimas, talvez você nem precise incluir os principais arquivos de gabinete do DirectX 9.0c na pasta redistribuível da mídia de instalação. Uma grande maioria das instalações do Windows XP tem o Service Pack 2, que inclui os componentes principais do DirectX 9.0c, portanto, a operação de instalação do DirectX será muito rápida e não exigirá uma reinicialização. O menor pacote que pode ser criado é de cerca de 3 MB e pode ser compactado para cerca de metade desse tamanho. Um pacote como este contém uma versão da DLL D3DX e requer que o DirectX 9.0c já está presente.

O conjunto mínimo de arquivos necessários para criar um pacote redistribuível são os seguintes arquivos, localizados na pasta Redist do SDK do DirectX (Program Files \\ DirectX SDK \\ \) Redist:

-   dxsetup.exe
-   dsetup32.dll
-   dsetup.dll
-   dxupdate.cab

Adicione a eles os arquivos de gabinete para os componentes que você deseja instalar. Se você precisar que os usuários do seu aplicativo já tenham o DirectX 9.0c, não será necessário incluir DirectX.cab ou dxnt.cab, que comem a maior parte do requisito de espaço. DirectX.cab é necessário apenas para Windows 98 e Windows ME; dxnt.cab é necessário apenas para Windows 2000, Windows XP e Windows XP SP1; e dxdllregx86.cab é necessário apenas para \_ o Windows 2000, o Windows XP RTM, o Windows XP SP1 e o Windows Server 2003 RTM. Além disso, se você não fizer uso do DirectShow ou assumir que ele já está instalado, poderá omitir BDA.cab, BDANT.cab e BDAXP.cab.

> [!Note]  
> Você pode supor que os usuários do seu aplicativo já tenham o DirectX 9.0c se ele tiver sido instalado por uma versão anterior do seu aplicativo, forçar os usuários a atualizar manualmente por meio do Web Installer ou pressupor que eles tenham Windows XP SP2 ou posterior.

 

Continuando com este exemplo, se você estiver usando apenas a versão de 32 bits do D3DX para abril de 2006, poderá adicionar Apr2006 \_ d3dx9 \_ 30 \_x86.cab. Se você estiver usando a versão de 32 bits de agosto de 2006 de 32 bits do XINPUT, adicione Aug2006 \_ xinput \_x86.cab.

Se você tiver um aplicativo nativo de 64 bits, precisará adicionar as \_ versões x64. No entanto, se você tiver um aplicativo de 32 bits em execução em um sistema operacional de 64 bits, as versões de 32 bits das DLLs funcionarão.

Em seguida, você pode distribuir esse pacote de arquivos e iniciar DirectSetup no modo silencioso ou executar dxsetup.exe no shell de comando no modo silencioso. Lembre-se de não proteger esse pacote por nenhuma verificação de versão de arquivos e certifique-se de que os usuários não podem optar por não executar a instalação do DirectX. Qualquer um desses eventos cria um processo de instalação fallible.

## <a name="internal-deployment-of-the-debug-directx-runtime"></a>Implantação interna do Runtime do DirectX de depuração

Os runtimes de depuração dos componentes do DirectX são instalados quando o SDK do DirectX é instalado, mas a instalação do SDK em cada computador de teste pode ser difícil. Você precisa projetar o processo de instalação para copiar as DLLs de runtime de depuração da arquitetura do Runtime do Desenvolvedor do SDK do Microsoft DirectX dos Arquivos de Programas para Windows \\ \\ \\ \\ \\ system32 ou para a pasta do \\ jogo.

No entanto, é recomendável que você não simplesmente copie as DLLs de tempo de run time lançadas porque é fácil esquecer de removê-las para o produto final. Em vez disso, coloque os arquivos de instalação do DirectX em uma pasta compartilhada e execute a instalação silenciosamente da pasta compartilhada.

## <a name="desktop-bridge-applications"></a>Ponte de Desktop aplicativos 

Ponte de Desktop aplicativos que usam D3DX9, D3DX10, D3DX11, XAudio 2.7, XInput 1.3 ou XACT devem baixar a estrutura [Microsoft.DirectX.x86](https://download.microsoft.com/download/c/c/2/cc291a37-2ebd-4ac2-ba5f-4c9124733bf1/UAPSignedBinary_Microsoft.DirectX.x86.appx) ou [Microsoft.DirectX.x64](https://download.microsoft.com/download/c/c/2/cc291a37-2ebd-4ac2-ba5f-4c9124733bf1/UAPSignedBinary_Microsoft.DirectX.x64.appx) para implantar esses componentes herdados do SDK do DirectX lado a lado. Como alternativa, você pode remover todas essas dependências (consulte Guia do desenvolvedor para a versão &mdash; [redistribuível do XAudio 2.9](../xaudio2/xaudio2-redistributable.md)e as postagens no blog [Living without D3DX,](https://walbourn.github.io/living-without-d3dx/) [XINPUT e Windows 8](https://walbourn.github.io/xinput-and-windows-8/)).
