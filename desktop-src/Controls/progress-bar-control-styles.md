---
title: Estilos de controle da barra de progresso (CommCtrl. h)
description: Os seguintes estilos de controle têm suporte dos controles de barra de progresso
ms.assetid: bd89aa74-c15e-4745-8b2b-7cbd8b28c1c8
topic_type:
- apiref
api_name:
- PBS_MARQUEE
- PBS_SMOOTH
- PBS_SMOOTHREVERSE
- PBS_VERTICAL
api_location:
- CommCtrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d55ec928fb1ee2715576f3131dde0f661a91fcf8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105750938"
---
# <a name="progress-bar-control-styles"></a><span data-ttu-id="2a62c-103">Estilos de controle da barra de progresso</span><span class="sxs-lookup"><span data-stu-id="2a62c-103">Progress Bar Control Styles</span></span>

<span data-ttu-id="2a62c-104">Os seguintes estilos de controle têm suporte dos controles de [barra de progresso](progress-bar-control.md) :</span><span class="sxs-lookup"><span data-stu-id="2a62c-104">The following control styles are supported by [Progress Bar](progress-bar-control.md) controls:</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th style="text-align: left;"><span data-ttu-id="2a62c-105">Constante</span><span class="sxs-lookup"><span data-stu-id="2a62c-105">Constant</span></span></th>
<th style="text-align: left;"><span data-ttu-id="2a62c-106">Descrição</span><span class="sxs-lookup"><span data-stu-id="2a62c-106">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;"><span id="PBS_MARQUEE"></span><span id="pbs_marquee"></span><dl> <span data-ttu-id="2a62c-107"><dt><strong>PBS_MARQUEE</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="2a62c-107"><dt><strong>PBS_MARQUEE</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="2a62c-108"><a href="common-control-versions.md">Versão 6,0</a> ou posterior.</span><span class="sxs-lookup"><span data-stu-id="2a62c-108"><a href="common-control-versions.md">Version 6.0</a> or later.</span></span> <span data-ttu-id="2a62c-109">O indicador de progresso não aumenta em tamanho, mas, em vez disso, é movido repetidamente ao longo do comprimento da barra, indicando a atividade sem especificar a proporção do progresso concluída.</span><span class="sxs-lookup"><span data-stu-id="2a62c-109">The progress indicator does not grow in size but instead moves repeatedly along the length of the bar, indicating activity without specifying what proportion of the progress is complete.</span></span> <br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="2a62c-110">O Comctl32.dll versão 6 não é redistribuível, mas está incluído no Windows ou posterior.</span><span class="sxs-lookup"><span data-stu-id="2a62c-110">Comctl32.dll version 6 is not redistributable but it is included in Windows or later.</span></span> <span data-ttu-id="2a62c-111">Para usar Comctl32.dll versão 6, especifique-o em um manifesto.</span><span class="sxs-lookup"><span data-stu-id="2a62c-111">To use Comctl32.dll version 6, specify it in a manifest.</span></span> <span data-ttu-id="2a62c-112">Para obter mais informações sobre manifestos, consulte <a href="cookbook-overview.md">habilitando estilos visuais</a>.</span><span class="sxs-lookup"><span data-stu-id="2a62c-112">For more information on manifests, see <a href="cookbook-overview.md">Enabling Visual Styles</a>.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="PBS_SMOOTH"></span><span id="pbs_smooth"></span><dl> <span data-ttu-id="2a62c-113"><dt><strong>PBS_SMOOTH</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="2a62c-113"><dt><strong>PBS_SMOOTH</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="2a62c-114"><a href="common-control-versions.md">Versão 4,70</a> ou posterior.</span><span class="sxs-lookup"><span data-stu-id="2a62c-114"><a href="common-control-versions.md">Version 4.70</a> or later.</span></span> <span data-ttu-id="2a62c-115">A barra de progresso exibe o status de progresso em uma barra de rolagem suave em vez da barra segmentada padrão.</span><span class="sxs-lookup"><span data-stu-id="2a62c-115">The progress bar displays progress status in a smooth scrolling bar instead of the default segmented bar.</span></span> <br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="2a62c-116">Esse estilo só tem suporte no tema clássico do Windows.</span><span class="sxs-lookup"><span data-stu-id="2a62c-116">This style is supported only in the Windows Classic theme.</span></span> <span data-ttu-id="2a62c-117">Todos os outros temas substituem esse estilo.</span><span class="sxs-lookup"><span data-stu-id="2a62c-117">All other themes override this style.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="PBS_SMOOTHREVERSE"></span><span id="pbs_smoothreverse"></span><dl> <span data-ttu-id="2a62c-118"><dt><strong>PBS_SMOOTHREVERSE</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="2a62c-118"><dt><strong>PBS_SMOOTHREVERSE</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="2a62c-119"><a href="common-control-versions.md">Versão 6,0</a> ou posterior e <strong>Windows Vista.</strong></span><span class="sxs-lookup"><span data-stu-id="2a62c-119"><a href="common-control-versions.md">Version 6.0</a> or later and <strong>Windows Vista.</strong></span></span> <span data-ttu-id="2a62c-120">Determina o comportamento da animação que a barra de progresso deve usar ao mover para trás (de um valor mais alto para um valor mais baixo).</span><span class="sxs-lookup"><span data-stu-id="2a62c-120">Determines the animation behavior that the progress bar should use when moving backward (from a higher value to a lower value).</span></span> <span data-ttu-id="2a62c-121">Se estiver definido, uma &quot; &quot; transição suave ocorrerá, caso contrário, o controle &quot; saltará &quot; para o valor mais baixo.</span><span class="sxs-lookup"><span data-stu-id="2a62c-121">If this is set, then a &quot;smooth&quot; transition will occur, otherwise the control will &quot;jump&quot; to the lower value.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="PBS_VERTICAL"></span><span id="pbs_vertical"></span><dl> <span data-ttu-id="2a62c-122"><dt><strong>PBS_VERTICAL</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="2a62c-122"><dt><strong>PBS_VERTICAL</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="2a62c-123"><a href="common-control-versions.md">Versão 4,70</a> ou posterior.</span><span class="sxs-lookup"><span data-stu-id="2a62c-123"><a href="common-control-versions.md">Version 4.70</a> or later.</span></span> <span data-ttu-id="2a62c-124">A barra de progresso exibe o status de progresso verticalmente, de baixo para cima.</span><span class="sxs-lookup"><span data-stu-id="2a62c-124">The progress bar displays progress status vertically, from bottom to top.</span></span><br/></td>
</tr>
</tbody>
</table>



## <a name="remarks"></a><span data-ttu-id="2a62c-125">Comentários</span><span class="sxs-lookup"><span data-stu-id="2a62c-125">Remarks</span></span>

<span data-ttu-id="2a62c-126">Você pode definir estilos de barra de progresso, da mesma forma que outros controles comuns, com [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa), [**GetWindowLong**](/windows/desktop/api/winuser/nf-winuser-getwindowlonga)ou [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga).</span><span class="sxs-lookup"><span data-stu-id="2a62c-126">You can set progress bar styles, in the same way as other common controls, with [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa), [**GetWindowLong**](/windows/desktop/api/winuser/nf-winuser-getwindowlonga), or [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga).</span></span>

## <a name="requirements"></a><span data-ttu-id="2a62c-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2a62c-127">Requirements</span></span>



| <span data-ttu-id="2a62c-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="2a62c-128">Requirement</span></span> | <span data-ttu-id="2a62c-129">Valor</span><span class="sxs-lookup"><span data-stu-id="2a62c-129">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="2a62c-130">parâmetro</span><span class="sxs-lookup"><span data-stu-id="2a62c-130">Header</span></span><br/> | <dl> <span data-ttu-id="2a62c-131"><dt>CommCtrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="2a62c-131"><dt>CommCtrl.h</dt></span></span> </dl> |



 

