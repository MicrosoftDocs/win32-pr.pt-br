---
title: Funções do DWM
description: Esta seção contém informações sobre as funções de Gerenciador de Janelas da Área de Trabalho (DWM).
ms.assetid: 525807fe-c5d7-4997-87b9-a14d02c33cc3
keywords:
- Gerenciador de Janelas da Área de Trabalho (DWM), referência
- DWM (Gerenciador de Janelas da Área de Trabalho), referência
- Gerenciador de Janelas da Área de Trabalho (DWM), funções
- DWM (Gerenciador de Janelas da Área de Trabalho), funções
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 067f836e7fa8b5b84be02a402a3e0b3d0f78d1c1
ms.sourcegitcommit: ae73f4dd3cf5a3c6a1ea7d191ca32a5b01f6686b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/08/2020
ms.locfileid: "104294549"
---
# <a name="dwm-functions"></a><span data-ttu-id="72d3c-107">Funções do DWM</span><span class="sxs-lookup"><span data-stu-id="72d3c-107">DWM Functions</span></span>

<span data-ttu-id="72d3c-108">Esta seção contém informações sobre as funções de Gerenciador de Janelas da Área de Trabalho (DWM).</span><span class="sxs-lookup"><span data-stu-id="72d3c-108">This section contains information about the Desktop Window Manager (DWM) functions.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="72d3c-109">Nesta seção</span><span class="sxs-lookup"><span data-stu-id="72d3c-109">In this section</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="72d3c-110">Tópico</span><span class="sxs-lookup"><span data-stu-id="72d3c-110">Topic</span></span></th>
<th><span data-ttu-id="72d3c-111">Descrição</span><span class="sxs-lookup"><span data-stu-id="72d3c-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="72d3c-112"><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmattachmilcontent"><strong>DwmAttachMilContent</strong></a></span><span class="sxs-lookup"><span data-stu-id="72d3c-112"><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmattachmilcontent"><strong>DwmAttachMilContent</strong></a></span></span><br/></td>
<td><span data-ttu-id="72d3c-113">Esta função não está implementada.</span><span class="sxs-lookup"><span data-stu-id="72d3c-113">This function is not implemented.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="72d3c-114"><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmdefwindowproc"><strong>DwmDefWindowProc</strong></a></span><span class="sxs-lookup"><span data-stu-id="72d3c-114"><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmdefwindowproc"><strong>DwmDefWindowProc</strong></a></span></span><br/></td>
<td><span data-ttu-id="72d3c-115">Procedimento de janela padrão para teste de clique de DWM na área não cliente.</span><span class="sxs-lookup"><span data-stu-id="72d3c-115">Default window procedure for DWM hit testing within the non-client area.</span></span><br/> <span data-ttu-id="72d3c-116">Você também precisa garantir que <a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmdefwindowproc"><strong>DwmDefWindowProc</strong></a> seja chamado para a mensagem de <a href="/windows/desktop/inputdev/wm-ncmouseleave"><strong>WM_NCMOUSELEAVE</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="72d3c-116">You also need to ensure that <a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmdefwindowproc"><strong>DwmDefWindowProc</strong></a> is called for the <a href="/windows/desktop/inputdev/wm-ncmouseleave"><strong>WM_NCMOUSELEAVE</strong></a> message.</span></span> <span data-ttu-id="72d3c-117">Se <strong>DwmDefWindowProc</strong> não for chamado para a mensagem de <strong>WM_NCMOUSELEAVE</strong> , o DWM não removerá o realce dos botões <strong>maximizar</strong>, <strong>minimizar</strong>e <strong>fechar</strong> quando o cursor sair da janela.</span><span class="sxs-lookup"><span data-stu-id="72d3c-117">If <strong>DwmDefWindowProc</strong> is not called for the <strong>WM_NCMOUSELEAVE</strong> message, DWM does not remove the highlighting from the <strong>Maximize</strong>, <strong>Minimize</strong>, and <strong>Close</strong> buttons when the cursor leaves the window.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="72d3c-118"><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmdetachmilcontent"><strong>DwmDetachMilContent</strong></a></span><span class="sxs-lookup"><span data-stu-id="72d3c-118"><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmdetachmilcontent"><strong>DwmDetachMilContent</strong></a></span></span><br/></td>
<td><span data-ttu-id="72d3c-119">Esta função não está implementada.</span><span class="sxs-lookup"><span data-stu-id="72d3c-119">This function is not implemented.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="72d3c-120"><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmenableblurbehindwindow"><strong>DwmEnableBlurBehindWindow</strong></a></span><span class="sxs-lookup"><span data-stu-id="72d3c-120"><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmenableblurbehindwindow"><strong>DwmEnableBlurBehindWindow</strong></a></span></span><br/></td>
<td><span data-ttu-id="72d3c-121">Habilita o efeito de desfoque em uma janela especificada.</span><span class="sxs-lookup"><span data-stu-id="72d3c-121">Enables the blur effect on a specified window.</span></span><br/></td><span data-ttu-id="72d3c-122">
<b>Observação</b> A partir do Windows 8, chamar essa função não resulta no efeito de desfoque, devido a uma alteração de estilo na maneira como as janelas são renderizadas.</span><span class="sxs-lookup"><span data-stu-id="72d3c-122">
<b>Note</b> Beginning with Windows 8, calling this function doesn't result in the blur effect, due to a style change in the way windows are rendered.</span></span>
</tr>
<tr class="odd">
<td><span data-ttu-id="72d3c-123"><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmenablecomposition"><strong>DwmEnableComposition</strong></a></span><span class="sxs-lookup"><span data-stu-id="72d3c-123"><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmenablecomposition"><strong>DwmEnableComposition</strong></a></span></span><br/></td>
<td><span data-ttu-id="72d3c-124">Habilita ou desabilita a composição do DWM.</span><span class="sxs-lookup"><span data-stu-id="72d3c-124">Enables or disables DWM composition.</span></span> <br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="72d3c-125">Essa função foi preterida a partir do Windows 8.</span><span class="sxs-lookup"><span data-stu-id="72d3c-125">This function is deprecated as of Windows 8.</span></span> <span data-ttu-id="72d3c-126">O DWM não pode mais ser desabilitado por meio de programação.</span><span class="sxs-lookup"><span data-stu-id="72d3c-126">DWM can no longer be programmatically disabled.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="72d3c-127"><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmenablemmcss"><strong>DwmEnableMMCSS</strong></a></span><span class="sxs-lookup"><span data-stu-id="72d3c-127"><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmenablemmcss"><strong>DwmEnableMMCSS</strong></a></span></span><br/></td>
<td><span data-ttu-id="72d3c-128">Notifica o DWM para aceitar ou sair do agendamento do serviço de agendamento de classe de multimídia (MMCSS) enquanto o processo de chamada está ativo.</span><span class="sxs-lookup"><span data-stu-id="72d3c-128">Notifies the DWM to opt in to or out of Multimedia Class Schedule Service (MMCSS) scheduling while the calling process is alive.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="72d3c-129"><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmextendframeintoclientarea"><strong>DwmExtendFrameIntoClientArea</strong></a></span><span class="sxs-lookup"><span data-stu-id="72d3c-129"><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmextendframeintoclientarea"><strong>DwmExtendFrameIntoClientArea</strong></a></span></span><br/></td>
<td><span data-ttu-id="72d3c-130">Estende o quadro da janela para a área do cliente.</span><span class="sxs-lookup"><span data-stu-id="72d3c-130">Extends the window frame into the client area.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="72d3c-131"><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmflush"><strong>DwmFlush</strong></a></span><span class="sxs-lookup"><span data-stu-id="72d3c-131"><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmflush"><strong>DwmFlush</strong></a></span></span><br/></td>
<td><span data-ttu-id="72d3c-132">Emite uma chamada de liberação que bloqueia o chamador até o próximo momento, quando todas as atualizações da superfície do Microsoft DirectX que estão pendentes no momento foram feitas.</span><span class="sxs-lookup"><span data-stu-id="72d3c-132">Issues a flush call that blocks the caller until the next present, when all of the Microsoft DirectX surface updates that are currently outstanding have been made.</span></span> <span data-ttu-id="72d3c-133">Isso compensa cenas muito complexas ou processos de chamada com prioridade muito baixa.</span><span class="sxs-lookup"><span data-stu-id="72d3c-133">This compensates for very complex scenes or calling processes with very low priority.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="72d3c-134"><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmgetcolorizationcolor"><strong>DwmGetColorizationColor</strong></a></span><span class="sxs-lookup"><span data-stu-id="72d3c-134"><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmgetcolorizationcolor"><strong>DwmGetColorizationColor</strong></a></span></span><br/></td>
<td><span data-ttu-id="72d3c-135">Recupera a cor atual usada para composição do DWM Glass.</span><span class="sxs-lookup"><span data-stu-id="72d3c-135">Retrieves the current color used for DWM glass composition.</span></span> <span data-ttu-id="72d3c-136">Esse valor é baseado no esquema de cores atual e pode ser modificado pelo usuário.</span><span class="sxs-lookup"><span data-stu-id="72d3c-136">This value is based on the current color scheme and can be modified by the user.</span></span> <span data-ttu-id="72d3c-137">Os aplicativos podem escutar alterações de cores manipulando a notificação de <a href="wm-dwmcolorizationcolorchanged.md"><strong>WM_DWMCOLORIZATIONCOLORCHANGED</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="72d3c-137">Applications can listen for color changes by handling the <a href="wm-dwmcolorizationcolorchanged.md"><strong>WM_DWMCOLORIZATIONCOLORCHANGED</strong></a> notification.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="72d3c-138"><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmgetcompositiontiminginfo"><strong>DwmGetCompositionTimingInfo</strong></a></span><span class="sxs-lookup"><span data-stu-id="72d3c-138"><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmgetcompositiontiminginfo"><strong>DwmGetCompositionTimingInfo</strong></a></span></span><br/></td>
<td><span data-ttu-id="72d3c-139">Recupera as informações de tempo de composição atuais para uma janela especificada.</span><span class="sxs-lookup"><span data-stu-id="72d3c-139">Retrieves the current composition timing information for a specified window.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="72d3c-140"><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmgetgraphicsstreamclient"><strong>DwmGetGraphicsStreamClient</strong></a></span><span class="sxs-lookup"><span data-stu-id="72d3c-140"><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmgetgraphicsstreamclient"><strong>DwmGetGraphicsStreamClient</strong></a></span></span><br/></td>
<td><span data-ttu-id="72d3c-141">Esta função não está implementada.</span><span class="sxs-lookup"><span data-stu-id="72d3c-141">This function is not implemented.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="72d3c-142"><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmgetgraphicsstreamtransformhint"><strong>DwmGetGraphicsStreamTransformHint</strong></a></span><span class="sxs-lookup"><span data-stu-id="72d3c-142"><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmgetgraphicsstreamtransformhint"><strong>DwmGetGraphicsStreamTransformHint</strong></a></span></span><br/></td>
<td><span data-ttu-id="72d3c-143">Esta função não está implementada.</span><span class="sxs-lookup"><span data-stu-id="72d3c-143">This function is not implemented.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="72d3c-144"><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmgettransportattributes"><strong>DwmGetTransportAttributes</strong></a></span><span class="sxs-lookup"><span data-stu-id="72d3c-144"><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmgettransportattributes"><strong>DwmGetTransportAttributes</strong></a></span></span><br/></td>
<td><span data-ttu-id="72d3c-145">Recupera atributos de transporte.</span><span class="sxs-lookup"><span data-stu-id="72d3c-145">Retrieves transport attributes.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="72d3c-146"><a href="/windows/desktop/api/dwmapi/nf-dwmapi-dwmgetunmettabrequirements"><strong>DwmGetUnmetTabRequirements</strong></a></span><span class="sxs-lookup"><span data-stu-id="72d3c-146"><a href="/windows/desktop/api/dwmapi/nf-dwmapi-dwmgetunmettabrequirements"><strong>DwmGetUnmetTabRequirements</strong></a></span></span><br/></td>
<td><blockquote><span data-ttu-id="72d3c-147">
<strong>Observação</strong>  Essa função está disponível publicamente, mas não funcional, para o Windows 10, versão 1803.</span><span class="sxs-lookup"><span data-stu-id="72d3c-147">
<strong>Note</strong>  This function is publically available, but nonfunctional, for Windows 10, version 1803.</span></span>
</blockquote>
<span data-ttu-id="72d3c-148">Verifica os requisitos necessários para obter guias na barra de título do aplicativo para a janela especificada.</span><span class="sxs-lookup"><span data-stu-id="72d3c-148">Checks the requirements needed to get tabs in the application title bar for the specified window.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="72d3c-149"><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmgetwindowattribute"><strong>DwmGetWindowAttribute</strong></a></span><span class="sxs-lookup"><span data-stu-id="72d3c-149"><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmgetwindowattribute"><strong>DwmGetWindowAttribute</strong></a></span></span><br/></td>
<td><span data-ttu-id="72d3c-150">Recupera o valor atual de um atributo especificado aplicado a uma janela.</span><span class="sxs-lookup"><span data-stu-id="72d3c-150">Retrieves the current value of a specified attribute applied to a window.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="72d3c-151"><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwminvalidateiconicbitmaps"><strong>DwmInvalidateIconicBitmaps</strong></a></span><span class="sxs-lookup"><span data-stu-id="72d3c-151"><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwminvalidateiconicbitmaps"><strong>DwmInvalidateIconicBitmaps</strong></a></span></span><br/></td>
<td><span data-ttu-id="72d3c-152">Chamado por um aplicativo para indicar que todos os bitmaps icônico fornecidos anteriormente de uma janela, miniaturas e representações de inspeção, devem ser atualizados.</span><span class="sxs-lookup"><span data-stu-id="72d3c-152">Called by an application to indicate that all previously provided iconic bitmaps from a window, both thumbnails and peek representations, should be refreshed.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="72d3c-153"><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmiscompositionenabled"><strong>DwmIsCompositionEnabled</strong></a></span><span class="sxs-lookup"><span data-stu-id="72d3c-153"><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmiscompositionenabled"><strong>DwmIsCompositionEnabled</strong></a></span></span><br/></td>
<td><span data-ttu-id="72d3c-154">Obtém um valor que indica se a composição do DWM está habilitada.</span><span class="sxs-lookup"><span data-stu-id="72d3c-154">Obtains a value that indicates whether DWM composition is enabled.</span></span> <span data-ttu-id="72d3c-155">Os aplicativos em computadores que executam o Windows 7 ou anterior podem escutar alterações de estado de composição manipulando a notificação de <a href="wm-dwmcompositionchanged.md"><strong>WM_DWMCOMPOSITIONCHANGED</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="72d3c-155">Applications on machines running Windows 7 or earlier can listen for composition state changes by handling the <a href="wm-dwmcompositionchanged.md"><strong>WM_DWMCOMPOSITIONCHANGED</strong></a> notification.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="72d3c-156"><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmmodifypreviousdxframeduration"><strong>DwmModifyPreviousDxFrameDuration</strong></a></span><span class="sxs-lookup"><span data-stu-id="72d3c-156"><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmmodifypreviousdxframeduration"><strong>DwmModifyPreviousDxFrameDuration</strong></a></span></span><br/></td>
<td><span data-ttu-id="72d3c-157">Altera o número de atualizações do monitor por meio do qual o quadro anterior será exibido.</span><span class="sxs-lookup"><span data-stu-id="72d3c-157">Changes the number of monitor refreshes through which the previous frame will be displayed.</span></span> <br/> <span data-ttu-id="72d3c-158">Não há mais suporte para <a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmmodifypreviousdxframeduration"><strong>DwmModifyPreviousDxFrameDuration</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="72d3c-158"><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmmodifypreviousdxframeduration"><strong>DwmModifyPreviousDxFrameDuration</strong></a> is no longer supported.</span></span> <span data-ttu-id="72d3c-159">Começando com Windows 8.1, chamadas para <strong>DwmModifyPreviousDxFrameDuration</strong> sempre retornam E_NOTIMPL.</span><span class="sxs-lookup"><span data-stu-id="72d3c-159">Starting with Windows 8.1, calls to <strong>DwmModifyPreviousDxFrameDuration</strong> always return E_NOTIMPL.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="72d3c-160"><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmquerythumbnailsourcesize"><strong>DwmQueryThumbnailSourceSize</strong></a></span><span class="sxs-lookup"><span data-stu-id="72d3c-160"><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmquerythumbnailsourcesize"><strong>DwmQueryThumbnailSourceSize</strong></a></span></span><br/></td>
<td><span data-ttu-id="72d3c-161">Recupera o tamanho da origem da miniatura do DWM.</span><span class="sxs-lookup"><span data-stu-id="72d3c-161">Retrieves the source size of the DWM thumbnail.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="72d3c-162"><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmregisterthumbnail"><strong>DwmRegisterThumbnail</strong></a></span><span class="sxs-lookup"><span data-stu-id="72d3c-162"><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmregisterthumbnail"><strong>DwmRegisterThumbnail</strong></a></span></span><br/></td>
<td><span data-ttu-id="72d3c-163">Cria uma relação de miniatura do DWM entre as janelas de destino e de origem.</span><span class="sxs-lookup"><span data-stu-id="72d3c-163">Creates a DWM thumbnail relationship between the destination and source windows.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="72d3c-164"><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmrendergesture"><strong>DwmRenderGesture</strong></a></span><span class="sxs-lookup"><span data-stu-id="72d3c-164"><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmrendergesture"><strong>DwmRenderGesture</strong></a></span></span><br/></td>
<td><span data-ttu-id="72d3c-165">Notifica o DWM de que um contato de toque foi reconhecido como um gesto e que o DWM deve desenhar comentários para esse gesto.</span><span class="sxs-lookup"><span data-stu-id="72d3c-165">Notifies DWM that a touch contact has been recognized as a gesture, and that DWM should draw feedback for that gesture.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="72d3c-166"><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmsetdxframeduration"><strong>DwmSetDxFrameDuration</strong></a></span><span class="sxs-lookup"><span data-stu-id="72d3c-166"><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmsetdxframeduration"><strong>DwmSetDxFrameDuration</strong></a></span></span><br/></td>
<td><span data-ttu-id="72d3c-167">Define o número de atualizações do monitor por meio do qual exibir o quadro apresentado.</span><span class="sxs-lookup"><span data-stu-id="72d3c-167">Sets the number of monitor refreshes through which to display the presented frame.</span></span> <br/> <span data-ttu-id="72d3c-168">Não há mais suporte para <a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmsetdxframeduration"><strong>DwmSetDxFrameDuration</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="72d3c-168"><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmsetdxframeduration"><strong>DwmSetDxFrameDuration</strong></a> is no longer supported.</span></span> <span data-ttu-id="72d3c-169">Começando com Windows 8.1, chamadas para <strong>DwmSetDxFrameDuration</strong> sempre retornam E_NOTIMPL.</span><span class="sxs-lookup"><span data-stu-id="72d3c-169">Starting with Windows 8.1, calls to <strong>DwmSetDxFrameDuration</strong> always return E_NOTIMPL.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="72d3c-170"><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmseticoniclivepreviewbitmap"><strong>DwmSetIconicLivePreviewBitmap</strong></a></span><span class="sxs-lookup"><span data-stu-id="72d3c-170"><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmseticoniclivepreviewbitmap"><strong>DwmSetIconicLivePreviewBitmap</strong></a></span></span><br/></td>
<td><span data-ttu-id="72d3c-171">Define um bitmap estático icônico para exibir uma <em>Visualização dinâmica</em> (também conhecida como visualização de <em>inspeção</em>) de uma janela ou guia. A barra de tarefas pode usar esse bitmap para mostrar uma visualização de tamanho completo de uma janela ou guia.</span><span class="sxs-lookup"><span data-stu-id="72d3c-171">Sets a static, iconic bitmap to display a <em>live preview</em> (also known as a <em>Peek preview</em>) of a window or tab. The taskbar can use this bitmap to show a full-sized preview of a window or tab.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="72d3c-172"><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmseticonicthumbnail"><strong>DwmSetIconicThumbnail</strong></a></span><span class="sxs-lookup"><span data-stu-id="72d3c-172"><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmseticonicthumbnail"><strong>DwmSetIconicThumbnail</strong></a></span></span><br/></td>
<td><span data-ttu-id="72d3c-173">Define um bitmap estático icônico em uma janela ou guia para usar como uma representação em miniatura.</span><span class="sxs-lookup"><span data-stu-id="72d3c-173">Sets a static, iconic bitmap on a window or tab to use as a thumbnail representation.</span></span> <span data-ttu-id="72d3c-174">A barra de tarefas pode usar esse bitmap como um destino de alternância de miniatura para a janela ou guia.</span><span class="sxs-lookup"><span data-stu-id="72d3c-174">The taskbar can use this bitmap as a thumbnail switch target for the window or tab.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="72d3c-175"><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmsetpresentparameters"><strong>DwmSetPresentParameters</strong></a></span><span class="sxs-lookup"><span data-stu-id="72d3c-175"><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmsetpresentparameters"><strong>DwmSetPresentParameters</strong></a></span></span><br/></td>
<td><span data-ttu-id="72d3c-176">Define os parâmetros atuais para composição de quadros.</span><span class="sxs-lookup"><span data-stu-id="72d3c-176">Sets the present parameters for frame composition.</span></span> <br/> <span data-ttu-id="72d3c-177">Não há mais suporte para <a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmsetpresentparameters"><strong>DwmSetPresentParameters</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="72d3c-177"><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmsetpresentparameters"><strong>DwmSetPresentParameters</strong></a> is no longer supported.</span></span> <span data-ttu-id="72d3c-178">Começando com Windows 8.1, chamadas para <strong>DwmSetPresentParameters</strong> sempre retornam E_NOTIMPL.</span><span class="sxs-lookup"><span data-stu-id="72d3c-178">Starting with Windows 8.1, calls to <strong>DwmSetPresentParameters</strong> always return E_NOTIMPL.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="72d3c-179"><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmsetwindowattribute"><strong>DwmSetWindowAttribute</strong></a></span><span class="sxs-lookup"><span data-stu-id="72d3c-179"><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmsetwindowattribute"><strong>DwmSetWindowAttribute</strong></a></span></span><br/></td>
<td><span data-ttu-id="72d3c-180">Define o valor de atributos de renderização que não são de cliente para uma janela.</span><span class="sxs-lookup"><span data-stu-id="72d3c-180">Sets the value of non-client rendering attributes for a window.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="72d3c-181"><a href="/windows/desktop/api/dwmapi/nf-dwmapi-dwmshowcontact"><strong>DwmShowContact</strong></a></span><span class="sxs-lookup"><span data-stu-id="72d3c-181"><a href="/windows/desktop/api/dwmapi/nf-dwmapi-dwmshowcontact"><strong>DwmShowContact</strong></a></span></span><br/></td>
<td><span data-ttu-id="72d3c-182">Chamado por um aplicativo ou estrutura para especificar o tipo de comentário visual a ser desenhado em resposta a um contato de caneta ou toque específico.</span><span class="sxs-lookup"><span data-stu-id="72d3c-182">Called by an app or framework to specify the visual feedback type to draw in response to a particular touch or pen contact.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="72d3c-183"><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmtethercontact"><strong>DwmTetherContact</strong></a></span><span class="sxs-lookup"><span data-stu-id="72d3c-183"><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmtethercontact"><strong>DwmTetherContact</strong></a></span></span><br/></td>
<td><span data-ttu-id="72d3c-184">Habilita os comentários gráficos de toque e arrasta as interações para o usuário.</span><span class="sxs-lookup"><span data-stu-id="72d3c-184">Enables the graphical feedback of touch and drag interactions to the user.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="72d3c-185"><a href="/windows/desktop/api/dwmapi/nf-dwmapi-dwmtransitionownedwindow"><strong>DwmTransitionOwnedWindow</strong></a></span><span class="sxs-lookup"><span data-stu-id="72d3c-185"><a href="/windows/desktop/api/dwmapi/nf-dwmapi-dwmtransitionownedwindow"><strong>DwmTransitionOwnedWindow</strong></a></span></span><br/></td>
<td><span data-ttu-id="72d3c-186">Coordena as animações de janelas de ferramentas com o DWM.</span><span class="sxs-lookup"><span data-stu-id="72d3c-186">Coordinates the animations of tool windows with the DWM.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="72d3c-187"><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmunregisterthumbnail"><strong>DwmUnregisterThumbnail</strong></a></span><span class="sxs-lookup"><span data-stu-id="72d3c-187"><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmunregisterthumbnail"><strong>DwmUnregisterThumbnail</strong></a></span></span><br/></td>
<td><span data-ttu-id="72d3c-188">Remove uma relação de miniatura do DWM criada pela função <a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmregisterthumbnail"><strong>DwmRegisterThumbnail</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="72d3c-188">Removes a DWM thumbnail relationship created by the <a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmregisterthumbnail"><strong>DwmRegisterThumbnail</strong></a> function.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="72d3c-189"><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmupdatethumbnailproperties"><strong>DwmUpdateThumbnailProperties</strong></a></span><span class="sxs-lookup"><span data-stu-id="72d3c-189"><a href="/windows/desktop/api/Dwmapi/nf-dwmapi-dwmupdatethumbnailproperties"><strong>DwmUpdateThumbnailProperties</strong></a></span></span><br/></td>
<td><span data-ttu-id="72d3c-190">Atualiza as propriedades de uma miniatura do DWM.</span><span class="sxs-lookup"><span data-stu-id="72d3c-190">Updates the properties for a DWM thumbnail.</span></span><br/></td>
</tr>
</tbody>
</table>



 

 

