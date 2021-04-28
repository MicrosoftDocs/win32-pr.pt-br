---
description: ChooseFont () caixa de diálogo comum do Win32
ms.assetid: ee1df9f2-585f-4208-ad49-a0f6ba76f53a
title: ChooseFont () caixa de diálogo comum do Win32
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a4dd8eb6ec226f8dbf5220f5a90dac802cf149dd
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108088604"
---
# <a name="choosefont-win32-common-dialog"></a><span data-ttu-id="d68ff-103">ChooseFont () caixa de diálogo comum do Win32</span><span class="sxs-lookup"><span data-stu-id="d68ff-103">ChooseFont() Win32 Common Dialog</span></span>

## <a name="affected-platforms"></a><span data-ttu-id="d68ff-104">Plataformas afetadas</span><span class="sxs-lookup"><span data-stu-id="d68ff-104">Affected Platforms</span></span>

<span data-ttu-id="d68ff-105">**Clientes** -Windows 7</span><span class="sxs-lookup"><span data-stu-id="d68ff-105">**Clients** - Windows 7</span></span>  
<span data-ttu-id="d68ff-106">**Servidores** -Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="d68ff-106">**Servers** - Windows Server 2008 R2</span></span>  









## <a name="feature-impact"></a><span data-ttu-id="d68ff-107">Impacto do recurso</span><span class="sxs-lookup"><span data-stu-id="d68ff-107">Feature Impact</span></span>

<span data-ttu-id="d68ff-108">**Severidade** -baixa</span><span class="sxs-lookup"><span data-stu-id="d68ff-108">**Severity** - Low</span></span>  
<span data-ttu-id="d68ff-109">**Frequência** -média</span><span class="sxs-lookup"><span data-stu-id="d68ff-109">**Frequency** - Medium</span></span>  




## <a name="description"></a><span data-ttu-id="d68ff-110">Descrição</span><span class="sxs-lookup"><span data-stu-id="d68ff-110">Description</span></span>

<span data-ttu-id="d68ff-111">O Windows 7 inclui várias atualizações para a caixa de diálogo comum do Win32 ChooseFont ().</span><span class="sxs-lookup"><span data-stu-id="d68ff-111">Windows 7 includes several updates to the ChooseFont() Win32 common dialog.</span></span> <span data-ttu-id="d68ff-112">Elas se enquadram em duas categorias:</span><span class="sxs-lookup"><span data-stu-id="d68ff-112">These fall into two categories:</span></span>

-   <span data-ttu-id="d68ff-113">Atualização Visual da caixa de diálogo</span><span class="sxs-lookup"><span data-stu-id="d68ff-113">Visual refresh of the dialog</span></span>
-   <span data-ttu-id="d68ff-114">Suporte para novo recurso mostrar/ocultar fontes</span><span class="sxs-lookup"><span data-stu-id="d68ff-114">Support for new show/hide fonts feature</span></span>

<span data-ttu-id="d68ff-115">A **atualização da caixa de diálogo** atualiza o modelo padrão para colocar a caixa de diálogo mais em linha com outros layouts de caixa de diálogo no Windows.</span><span class="sxs-lookup"><span data-stu-id="d68ff-115">The **dialog refresh** updates the standard template to bring the dialog more in line with other dialog layouts in Windows.</span></span> <span data-ttu-id="d68ff-116">Ele apresenta WYSIWYG às listas de exibição de fontes para ajudar os usuários a escolher as fontes.</span><span class="sxs-lookup"><span data-stu-id="d68ff-116">It introduces WYSIWYG to the font display lists to help users choose fonts.</span></span> <span data-ttu-id="d68ff-117">Ele também inclui um link para o CPL Fonts para fornecer acesso fácil para os usuários que desejam personalizar suas listas de fontes.</span><span class="sxs-lookup"><span data-stu-id="d68ff-117">It also includes a link to the Fonts CPL to provide easy access for users wishing to customize their font lists.</span></span>

<span data-ttu-id="d68ff-118">**Mostrar/ocultar fontes** é um novo recurso de plataforma do Windows 7 no qual as fontes não apropriadas para as configurações de idioma do usuário atual (métodos de entrada) não são apresentadas por padrão nas listas de seleção de fontes.</span><span class="sxs-lookup"><span data-stu-id="d68ff-118">**Show/hide fonts** is a new Windows 7 platform feature whereby fonts not appropriate for the current user's language settings (input methods) are not presented by default in font selection lists.</span></span> <span data-ttu-id="d68ff-119">Os usuários podem personalizar as fontes que desejam aparecer no CPL de fontes ou podem desabilitar esse recurso.</span><span class="sxs-lookup"><span data-stu-id="d68ff-119">Users may customize the fonts that they wish to appear in the Fonts CPL or may disable this feature.</span></span>

## <a name="manifestation-of-impact"></a><span data-ttu-id="d68ff-120">Manifestação do impacto</span><span class="sxs-lookup"><span data-stu-id="d68ff-120">Manifestation of Impact</span></span>

<span data-ttu-id="d68ff-121">**Atualização Visual do diálogo**</span><span class="sxs-lookup"><span data-stu-id="d68ff-121">**Dialog visual refresh**</span></span>

<span data-ttu-id="d68ff-122">Apresentamos dois novos modelos no Windows 7 (um para aplicativos que carregam a versão 6 ou posterior de comctl32.dll e outro para aplicativos que carregam versões anteriores).</span><span class="sxs-lookup"><span data-stu-id="d68ff-122">We have introduced two new templates in Windows 7 (one for applications that load version 6 or later of comctl32.dll and another for applications loading earlier versions).</span></span>

-   <span data-ttu-id="d68ff-123">Por motivos de compatibilidade de aplicativos, esses novos modelos serão carregados somente para aplicativos que não conectam a fila de mensagens do ChooseFont.</span><span class="sxs-lookup"><span data-stu-id="d68ff-123">For application compatibility reasons, these new templates will only be loaded for applications that do not hook the ChooseFont message queue.</span></span> <span data-ttu-id="d68ff-124">Os aplicativos que conectam a fila de mensagens continuarão a ver o layout de caixa de diálogo antigo.</span><span class="sxs-lookup"><span data-stu-id="d68ff-124">Applications that hook the message queue will continue to see the old dialog layout.</span></span>
-   <span data-ttu-id="d68ff-125">Os aplicativos que fornecem seus próprios modelos continuarão a ser capazes de usá-los.</span><span class="sxs-lookup"><span data-stu-id="d68ff-125">Applications that provide their own templates will continue to be able to use them.</span></span>

<span data-ttu-id="d68ff-126">Os aplicativos que não obtiverem os novos modelos não verão nenhuma alteração de layout de caixa de diálogo do vista.</span><span class="sxs-lookup"><span data-stu-id="d68ff-126">Applications that do not get the new templates will see no dialog layout changes from Vista.</span></span> <span data-ttu-id="d68ff-127">No entanto, eles ainda devem obter a nova visualização de fonte WYSIWYG.</span><span class="sxs-lookup"><span data-stu-id="d68ff-127">They should however still get the new WYSIWYG font preview.</span></span>

<span data-ttu-id="d68ff-128">**Mostrar/ocultar fontes**</span><span class="sxs-lookup"><span data-stu-id="d68ff-128">**Show/hide fonts**</span></span>

<span data-ttu-id="d68ff-129">Para todas as versões do ChooseFont, a caixa de diálogo usará as configurações de fonte de mostrar/ocultar do usuário atual para determinar a lista de fontes a ser exibida.</span><span class="sxs-lookup"><span data-stu-id="d68ff-129">For all versions of ChooseFont, the dialog will use the current user's show/hide font settings to determine the font list to display.</span></span> <span data-ttu-id="d68ff-130">Isso resultará na exibição de menos listas de fontes na maioria das instâncias.</span><span class="sxs-lookup"><span data-stu-id="d68ff-130">This will result in the display of fewer font lists in most instances.</span></span>

## <a name="end-user-mitigation"></a><span data-ttu-id="d68ff-131">Mitigação do usuário final</span><span class="sxs-lookup"><span data-stu-id="d68ff-131">End-user Mitigation</span></span>

<span data-ttu-id="d68ff-132">**Mostrar/ocultar fontes:** Para desabilitar a ocultação de fontes, os usuários devem ir para a página de configurações de fonte no CPL de fontes e desmarcar a seleção de '</span><span class="sxs-lookup"><span data-stu-id="d68ff-132">**Show/Hide Fonts:** To disable font hiding, users should go to the Font Settings page in the Fonts CPL and deselect the '</span></span>

<span data-ttu-id="d68ff-133">Caixa de seleção "ocultar fontes com base nas configurações de idioma"</span><span class="sxs-lookup"><span data-stu-id="d68ff-133">"Hide fonts based on language settings" checkbox</span></span>

## <a name="developer-mitigation"></a><span data-ttu-id="d68ff-134">Mitigação do desenvolvedor</span><span class="sxs-lookup"><span data-stu-id="d68ff-134">Developer Mitigation</span></span>

-   <span data-ttu-id="d68ff-135">**Atualização Visual:** Os desenvolvedores de aplicativos que fornecem seus próprios modelos podem querer atualizá-lo para estar em linha com o novo modelo do Windows 7 apropriado.</span><span class="sxs-lookup"><span data-stu-id="d68ff-135">**Visual refresh:** Applications developers who provide their own templates may want to refresh this to be in line with the appropriate new Windows 7 template.</span></span> <span data-ttu-id="d68ff-136">Os novos modelos estão disponíveis no arquivo de modelo Font. Dlg.</span><span class="sxs-lookup"><span data-stu-id="d68ff-136">The new templates are available in the Font.dlg template file.</span></span>

    <span data-ttu-id="d68ff-137">**Observação:** O novo modelo publicado contém um controle SysLink adicional que fornece um atalho que permite aos usuários iniciarem as fontes CPL para exibir mais fontes.</span><span class="sxs-lookup"><span data-stu-id="d68ff-137">**Note:** The new published template contains an additional SysLink control that provides a shortcut that allows users to launch the Fonts CPL to display more fonts.</span></span> <span data-ttu-id="d68ff-138">O controle de link requer a versão 6 da biblioteca de controle comum do Windows (comctl32.dll).</span><span class="sxs-lookup"><span data-stu-id="d68ff-138">The link control requires version 6 of the Windows common control library (comctl32.dll).</span></span> <span data-ttu-id="d68ff-139">Os desenvolvedores devem fornecer um manifesto ou diretiva que especifique o uso da versão 6 da DLL, se disponível.</span><span class="sxs-lookup"><span data-stu-id="d68ff-139">Developers should provide a manifest or directive that specifies the use of version 6 of the DLL if available.</span></span> <span data-ttu-id="d68ff-140">Em que um aplicativo usa uma versão anterior da biblioteca de controle comum, use o tipo de controle "botão de pressão".</span><span class="sxs-lookup"><span data-stu-id="d68ff-140">Where an application uses an earlier version of the common control library, use the "PUSHBUTTON" control type instead.</span></span>

-   <span data-ttu-id="d68ff-141">**Mostrar/ocultar fontes:** Os desenvolvedores podem desabilitar esse recurso fornecendo um sinalizador adicional (CF \_ INACTIVEFONTS) no membro flags da estrutura CHOOSEFONT.</span><span class="sxs-lookup"><span data-stu-id="d68ff-141">**Show/Hide Fonts:** Developers may disable this feature by providing an additional flag (CF\_INACTIVEFONTS) in the flags member of the CHOOSEFONT structure.</span></span> <span data-ttu-id="d68ff-142">Definir esse sinalizador faz com que todas as fontes instaladas sejam exibidas na lista de fontes.</span><span class="sxs-lookup"><span data-stu-id="d68ff-142">Setting this flag causes all installed fonts to display in the font list.</span></span>
-   <span data-ttu-id="d68ff-143">**Mostrar/ocultar fontes:** Os aplicativos que fornecem conteúdo de ajuda do ChooseFont podem desejar adicionar conteúdo para explicar por que a lista de fontes é reduzida e direcionar os usuários para as fontes CPL para personalizar suas listas de fontes.</span><span class="sxs-lookup"><span data-stu-id="d68ff-143">**Show/Hide Fonts:** Applications that provide ChooseFont help content may wish to add content to explain why the font list is reduced and direct users to the Fonts CPL to customize their font lists.</span></span>

## <a name="compatibility-performance-reliability-and-usability-testing"></a><span data-ttu-id="d68ff-144">Compatibilidade, desempenho, confiabilidade e teste de usabilidade</span><span class="sxs-lookup"><span data-stu-id="d68ff-144">Compatibility, Performance, Reliability, and Usability Testing</span></span>

<span data-ttu-id="d68ff-145">Os desenvolvedores cujos aplicativos conectam a fila de mensagens do ChooseFont para personalizar a caixa de diálogo devem verificar se seus aplicativos retêm todas as funcionalidades existentes.</span><span class="sxs-lookup"><span data-stu-id="d68ff-145">Developers whose applications hook the ChooseFont message queue to customize the dialog should verify that their applications retain all existing functionality.</span></span>

<span data-ttu-id="d68ff-146">Os aplicativos que reduzem bastante a lista de fontes usando sinalizadores devem garantir que a lista de fontes apresentada permaneça aceitável.</span><span class="sxs-lookup"><span data-stu-id="d68ff-146">Applications that heavily trim the font list using flags should ensure that the font list presented remains acceptable.</span></span>

 

 



