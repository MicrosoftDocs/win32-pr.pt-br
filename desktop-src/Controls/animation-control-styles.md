---
title: Estilos de controle de animação (CommCtrl. h)
description: Esta seção lista os estilos de janela usados com controles de animação.
ms.assetid: ad4fc4fd-166d-4871-9f60-5133a48681aa
topic_type:
- apiref
api_name:
- ACS_AUTOPLAY
- ACS_CENTER
- ACS_TIMER
- ACS_TRANSPARENT
api_location:
- CommCtrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d779b92c51420bc6bd9ad238bcff538dbc85841f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105753970"
---
# <a name="animation-control-styles"></a><span data-ttu-id="dac70-103">Estilos de controle de animação</span><span class="sxs-lookup"><span data-stu-id="dac70-103">Animation Control Styles</span></span>

<span data-ttu-id="dac70-104">Esta seção lista os estilos de janela usados com controles de animação.</span><span class="sxs-lookup"><span data-stu-id="dac70-104">This section lists the window styles used with animation controls.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th style="text-align: left;"><span data-ttu-id="dac70-105">Constante</span><span class="sxs-lookup"><span data-stu-id="dac70-105">Constant</span></span></th>
<th style="text-align: left;"><span data-ttu-id="dac70-106">Descrição</span><span class="sxs-lookup"><span data-stu-id="dac70-106">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;"><span id="ACS_AUTOPLAY"></span><span id="acs_autoplay"></span><dl> <span data-ttu-id="dac70-107"><dt><strong>ACS_AUTOPLAY</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="dac70-107"><dt><strong>ACS_AUTOPLAY</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="dac70-108">Começa a reproduzir a animação assim que o clipe AVI é aberto.</span><span class="sxs-lookup"><span data-stu-id="dac70-108">Starts playing the animation as soon as the AVI clip is opened.</span></span> <br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="ACS_CENTER"></span><span id="acs_center"></span><dl> <span data-ttu-id="dac70-109"><dt><strong>ACS_CENTER</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="dac70-109"><dt><strong>ACS_CENTER</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="dac70-110">Centraliza a animação na janela do controle de animação.</span><span class="sxs-lookup"><span data-stu-id="dac70-110">Centers the animation in the animation control's window.</span></span> <br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="ACS_TIMER"></span><span id="acs_timer"></span><dl> <span data-ttu-id="dac70-111"><dt><strong>ACS_TIMER</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="dac70-111"><dt><strong>ACS_TIMER</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="dac70-112">Por padrão, o controle cria um thread para reproduzir o clipe AVI.</span><span class="sxs-lookup"><span data-stu-id="dac70-112">By default, the control creates a thread to play the AVI clip.</span></span> <span data-ttu-id="dac70-113">Se você definir esse sinalizador, o controle reproduzirá o clipe sem criar um thread; internamente, o controle usa um temporizador do Win32 para sincronizar a reprodução.</span><span class="sxs-lookup"><span data-stu-id="dac70-113">If you set this flag, the control plays the clip without creating a thread; internally the control uses a Win32 timer to synchronize playback.</span></span> <br/> <span data-ttu-id="dac70-114"><strong>Comctl32.dll versão 6 e posterior:</strong> Não há suporte para esse estilo.</span><span class="sxs-lookup"><span data-stu-id="dac70-114"><strong>Comctl32.dll version 6 and later:</strong> This style is not supported.</span></span> <span data-ttu-id="dac70-115">Por padrão, o controle reproduz o clipe AVI sem criar um thread.</span><span class="sxs-lookup"><span data-stu-id="dac70-115">By default, the control plays the AVI clip without creating a thread.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="dac70-116">Comctl32.dll versão 6 não é redistribuível.</span><span class="sxs-lookup"><span data-stu-id="dac70-116">Comctl32.dll version 6 is not redistributable.</span></span> <span data-ttu-id="dac70-117">Para usar Comctl32.dll versão 6, especifique-o em um manifesto.</span><span class="sxs-lookup"><span data-stu-id="dac70-117">To use Comctl32.dll version 6, specify it in a manifest.</span></span> <span data-ttu-id="dac70-118">Para obter mais informações sobre manifestos, consulte <a href="cookbook-overview.md">habilitando estilos visuais</a>.</span><span class="sxs-lookup"><span data-stu-id="dac70-118">For more information on manifests, see <a href="cookbook-overview.md">Enabling Visual Styles</a>.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="ACS_TRANSPARENT"></span><span id="acs_transparent"></span><dl> <span data-ttu-id="dac70-119"><dt><strong>ACS_TRANSPARENT</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="dac70-119"><dt><strong>ACS_TRANSPARENT</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="dac70-120">Permite que você coincida a cor do plano de fundo de uma animação com a da janela subjacente, criando um &quot; &quot; plano de fundo transparente.</span><span class="sxs-lookup"><span data-stu-id="dac70-120">Allows you to match an animation's background color to that of the underlying window, creating a &quot;transparent&quot; background.</span></span> <span data-ttu-id="dac70-121">O pai do controle de animação não deve ter o estilo de WS_CLIPCHILDREN (consulte <a href="/windows/desktop/winmsg/window-styles">estilos de janela</a>).</span><span class="sxs-lookup"><span data-stu-id="dac70-121">The parent of the animation control must not have the WS_CLIPCHILDREN style (see <a href="/windows/desktop/winmsg/window-styles">Window Styles</a>).</span></span> <span data-ttu-id="dac70-122">O controle envia uma mensagem de <a href="wm-ctlcolorstatic.md"><strong>WM_CTLCOLORSTATIC</strong></a> para seu pai.</span><span class="sxs-lookup"><span data-stu-id="dac70-122">The control sends a <a href="wm-ctlcolorstatic.md"><strong>WM_CTLCOLORSTATIC</strong></a> message to its parent.</span></span> <span data-ttu-id="dac70-123">Use <a href="/windows/desktop/api/wingdi/nf-wingdi-setbkcolor"><strong>SetBkColor</strong></a> para definir a cor do plano de fundo para o contexto do dispositivo como um valor apropriado.</span><span class="sxs-lookup"><span data-stu-id="dac70-123">Use <a href="/windows/desktop/api/wingdi/nf-wingdi-setbkcolor"><strong>SetBkColor</strong></a> to set the background color for the device context to an appropriate value.</span></span> <span data-ttu-id="dac70-124">O controle interpreta o pixel superior esquerdo do primeiro quadro como a cor de fundo padrão da animação.</span><span class="sxs-lookup"><span data-stu-id="dac70-124">The control interprets the upper-left pixel of the first frame as the animation's default background color.</span></span> <span data-ttu-id="dac70-125">Ele remapeará todos os pixels com essa cor para o valor que você forneceu em resposta a WM_CTLCOLORSTATIC.</span><span class="sxs-lookup"><span data-stu-id="dac70-125">It will remap all pixels with that color to the value you supplied in response to WM_CTLCOLORSTATIC.</span></span> <br/></td>
</tr>
</tbody>
</table>



## <a name="requirements"></a><span data-ttu-id="dac70-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="dac70-126">Requirements</span></span>



| <span data-ttu-id="dac70-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="dac70-127">Requirement</span></span> | <span data-ttu-id="dac70-128">Valor</span><span class="sxs-lookup"><span data-stu-id="dac70-128">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="dac70-129">parâmetro</span><span class="sxs-lookup"><span data-stu-id="dac70-129">Header</span></span><br/> | <dl> <span data-ttu-id="dac70-130"><dt>CommCtrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="dac70-130"><dt>CommCtrl.h</dt></span></span> </dl> |



