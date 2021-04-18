---
title: Mensagens do DWM
description: Esta seção contém informações sobre as mensagens de Gerenciador de Janelas da Área de Trabalho (DWM).
ms.assetid: FF251CDA-7D68-4dd0-A54B-50B07E11C7C1
keywords:
- Gerenciador de Janelas da Área de Trabalho (DWM), referência
- DWM (Gerenciador de Janelas da Área de Trabalho), referência
- Gerenciador de Janelas da Área de Trabalho (DWM), mensagens
- DWM (Gerenciador de Janelas da Área de Trabalho), mensagens
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 399db1399cfc7cb60d29f0fa554a2233dc75a279
ms.sourcegitcommit: 927b9c371f75f52b8011483edf3a4ba37d11ebe4
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/11/2020
ms.locfileid: "105771454"
---
# <a name="dwm-messages"></a><span data-ttu-id="7f5dc-107">Mensagens do DWM</span><span class="sxs-lookup"><span data-stu-id="7f5dc-107">DWM Messages</span></span>

<span data-ttu-id="7f5dc-108">Esta seção contém informações sobre as mensagens de Gerenciador de Janelas da Área de Trabalho (DWM).</span><span class="sxs-lookup"><span data-stu-id="7f5dc-108">This section contains information about the Desktop Window Manager (DWM) messages.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="7f5dc-109">Nesta seção</span><span class="sxs-lookup"><span data-stu-id="7f5dc-109">In this section</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="7f5dc-110">Tópico</span><span class="sxs-lookup"><span data-stu-id="7f5dc-110">Topic</span></span></th>
<th><span data-ttu-id="7f5dc-111">Descrição</span><span class="sxs-lookup"><span data-stu-id="7f5dc-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="7f5dc-112"><a href="wm-dwmcolorizationcolorchanged.md"><strong>WM_DWMCOLORIZATIONCOLORCHANGED</strong></a></span><span class="sxs-lookup"><span data-stu-id="7f5dc-112"><a href="wm-dwmcolorizationcolorchanged.md"><strong>WM_DWMCOLORIZATIONCOLORCHANGED</strong></a></span></span><br/></td>
<td><span data-ttu-id="7f5dc-113">Informa todas as janelas de nível superior que a cor de colorização alterou.</span><span class="sxs-lookup"><span data-stu-id="7f5dc-113">Informs all top-level windows that the colorization color has changed.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7f5dc-114"><a href="wm-dwmcompositionchanged.md"><strong>WM_DWMCOMPOSITIONCHANGED</strong></a></span><span class="sxs-lookup"><span data-stu-id="7f5dc-114"><a href="wm-dwmcompositionchanged.md"><strong>WM_DWMCOMPOSITIONCHANGED</strong></a></span></span><br/></td>
<td><span data-ttu-id="7f5dc-115">Informa todas as janelas de nível superior que a composição do DWM foi habilitada ou desabilitada.</span><span class="sxs-lookup"><span data-stu-id="7f5dc-115">Informs all top-level windows that DWM composition has been enabled or disabled.</span></span> <br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="7f5dc-116">A partir do Windows 8, a composição do DWM é sempre habilitada, portanto, essa mensagem não é enviada independentemente das alterações no modo de vídeo.</span><span class="sxs-lookup"><span data-stu-id="7f5dc-116">As of Windows 8, DWM composition is always enabled, so this message is not sent regardless of video mode changes.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7f5dc-117"><a href="wm-dwmncrenderingchanged.md"><strong>WM_DWMNCRENDERINGCHANGED</strong></a></span><span class="sxs-lookup"><span data-stu-id="7f5dc-117"><a href="wm-dwmncrenderingchanged.md"><strong>WM_DWMNCRENDERINGCHANGED</strong></a></span></span><br/></td>
<td><span data-ttu-id="7f5dc-118">Enviado quando a política de renderização de área não cliente é alterada.</span><span class="sxs-lookup"><span data-stu-id="7f5dc-118">Sent when the non-client area rendering policy has changed.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7f5dc-119"><a href="wm-dwmsendiconiclivepreviewbitmap.md"><strong>WM_DWMSENDICONICLIVEPREVIEWBITMAP</strong></a></span><span class="sxs-lookup"><span data-stu-id="7f5dc-119"><a href="wm-dwmsendiconiclivepreviewbitmap.md"><strong>WM_DWMSENDICONICLIVEPREVIEWBITMAP</strong></a></span></span><br/></td>
<td><span data-ttu-id="7f5dc-120">Instrui uma janela para fornecer um bitmap estático a ser usado como uma <em>Visualização dinâmica</em> (também conhecida como <em>visualização de inspeção</em>) dessa janela.</span><span class="sxs-lookup"><span data-stu-id="7f5dc-120">Instructs a window to provide a static bitmap to use as a <em>live preview</em> (also known as a <em>Peek preview</em>) of that window.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7f5dc-121"><a href="wm-dwmsendiconicthumbnail.md"><strong>WM_DWMSENDICONICTHUMBNAIL</strong></a></span><span class="sxs-lookup"><span data-stu-id="7f5dc-121"><a href="wm-dwmsendiconicthumbnail.md"><strong>WM_DWMSENDICONICTHUMBNAIL</strong></a></span></span><br/></td>
<td><span data-ttu-id="7f5dc-122">Instrui uma janela para fornecer um bitmap estático a ser usado como uma representação em miniatura dessa janela.</span><span class="sxs-lookup"><span data-stu-id="7f5dc-122">Instructs a window to provide a static bitmap to use as a thumbnail representation of that window.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7f5dc-123"><a href="wm-dwmwindowmaximizedchange.md"><strong>WM_DWMWINDOWMAXIMIZEDCHANGE</strong></a></span><span class="sxs-lookup"><span data-stu-id="7f5dc-123"><a href="wm-dwmwindowmaximizedchange.md"><strong>WM_DWMWINDOWMAXIMIZEDCHANGE</strong></a></span></span><br/></td>
<td><span data-ttu-id="7f5dc-124">Enviado quando uma janela composta por DWM é maximizada.</span><span class="sxs-lookup"><span data-stu-id="7f5dc-124">Sent when a DWM composed window is maximized.</span></span><br/></td>
</tr>
</tbody>
</table>



 

 

 





