---
description: As constantes a seguir são usadas por aplicativos ou estruturas de interface do usuário para identificar como os comentários da interface do usuário são processados quando um dos gestos de caneta listados é detectado.
ms.assetid: 434DC272-DC1C-4091-BB38-DDCB1A635D8D
title: Visualização de caneta (WinUser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6e9a09aa8892647315eccbb1e8b3ca443e01c1ec
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104505897"
---
# <a name="pen-visualization"></a><span data-ttu-id="3bb21-103">Visualização de caneta</span><span class="sxs-lookup"><span data-stu-id="3bb21-103">Pen Visualization</span></span>

<span data-ttu-id="3bb21-104">As constantes a seguir são usadas por aplicativos ou estruturas de interface do usuário para identificar como os comentários da interface do usuário são processados quando um dos gestos de caneta listados é detectado.</span><span class="sxs-lookup"><span data-stu-id="3bb21-104">The following constants are used by applications or UI frameworks to identify how UI feedback is processed when one of the listed pen gestures is detected.</span></span>

<span data-ttu-id="3bb21-105">Essas constantes são usadas com os parâmetros **SPI \_ GETPENVISUALIZATION** e **SPI \_ SETPENVISUALIZATION** e a função [**SystemParametersInfo**](/windows/win32/api/winuser/nf-winuser-systemparametersinfoa) .</span><span class="sxs-lookup"><span data-stu-id="3bb21-105">These constants are used with the **SPI\_GETPENVISUALIZATION** and **SPI\_SETPENVISUALIZATION** parameters and the [**SystemParametersInfo**](/windows/win32/api/winuser/nf-winuser-systemparametersinfoa) function.</span></span>

<dl> <dt>

<span data-ttu-id="3bb21-106"><span id="PENVISUALIZATION_OFF"></span><span id="penvisualization_off"></span>**PENVISUALIZATION \_ desativado**</span><span class="sxs-lookup"><span data-stu-id="3bb21-106"><span id="PENVISUALIZATION_OFF"></span><span id="penvisualization_off"></span>**PENVISUALIZATION\_OFF**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3bb21-107">0x0000</span><span class="sxs-lookup"><span data-stu-id="3bb21-107">0x0000</span></span>
</dt> <dt>



<span data-ttu-id="3bb21-108">Especifica que os comentários da interface do usuário para todos os gestos de caneta estão desativados.</span><span class="sxs-lookup"><span data-stu-id="3bb21-108">Specifies that UI feedback for all pen gestures is off.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3bb21-109"><span id="PENVISUALIZATION_ON"></span><span id="penvisualization_on"></span>**PENVISUALIZATION \_ em**</span><span class="sxs-lookup"><span data-stu-id="3bb21-109"><span id="PENVISUALIZATION_ON"></span><span id="penvisualization_on"></span>**PENVISUALIZATION\_ON**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3bb21-110">0x0023</span><span class="sxs-lookup"><span data-stu-id="3bb21-110">0x0023</span></span>
</dt> <dt>



<span data-ttu-id="3bb21-111">Especifica que os comentários da interface do usuário para todos os gestos de caneta estão ativados.</span><span class="sxs-lookup"><span data-stu-id="3bb21-111">Specifies that UI feedback for all pen gestures is on.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3bb21-112"><span id="PENVISUALIZATION_TAP"></span><span id="penvisualization_tap"></span>**\_toque PENVISUALIZATION**</span><span class="sxs-lookup"><span data-stu-id="3bb21-112"><span id="PENVISUALIZATION_TAP"></span><span id="penvisualization_tap"></span>**PENVISUALIZATION\_TAP**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3bb21-113">0x0001</span><span class="sxs-lookup"><span data-stu-id="3bb21-113">0x0001</span></span>
</dt> <dt>



<span data-ttu-id="3bb21-114">Especifica comentários da interface do usuário para um toque de caneta.</span><span class="sxs-lookup"><span data-stu-id="3bb21-114">Specifies UI feedback for a pen tap.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3bb21-115"><span id="PENVISUALIZATION_DOUBLETAP"></span><span id="penvisualization_doubletap"></span>**PENVISUALIZATION \_ DOUBLETAP**</span><span class="sxs-lookup"><span data-stu-id="3bb21-115"><span id="PENVISUALIZATION_DOUBLETAP"></span><span id="penvisualization_doubletap"></span>**PENVISUALIZATION\_DOUBLETAP**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3bb21-116">0x0002</span><span class="sxs-lookup"><span data-stu-id="3bb21-116">0x0002</span></span>
</dt> <dt>



<span data-ttu-id="3bb21-117">Especifica comentários da interface do usuário para um toque duplo de caneta.</span><span class="sxs-lookup"><span data-stu-id="3bb21-117">Specifies UI feedback for a pen double tap.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3bb21-118"><span id="PENVISUALIZATION_CURSOR"></span><span id="penvisualization_cursor"></span>**\_cursor PENVISUALIZATION**</span><span class="sxs-lookup"><span data-stu-id="3bb21-118"><span id="PENVISUALIZATION_CURSOR"></span><span id="penvisualization_cursor"></span>**PENVISUALIZATION\_CURSOR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3bb21-119">0x0020</span><span class="sxs-lookup"><span data-stu-id="3bb21-119">0x0020</span></span>
</dt> <dt>



<span data-ttu-id="3bb21-120">Especifica os comentários da interface do usuário para o cursor da caneta.</span><span class="sxs-lookup"><span data-stu-id="3bb21-120">Specifies UI feedback for the pen cursor.</span></span>


</dt> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="3bb21-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3bb21-121">Requirements</span></span>



| <span data-ttu-id="3bb21-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="3bb21-122">Requirement</span></span> | <span data-ttu-id="3bb21-123">Valor</span><span class="sxs-lookup"><span data-stu-id="3bb21-123">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="3bb21-124">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3bb21-124">Minimum supported client</span></span><br/> | <span data-ttu-id="3bb21-125">\[Somente aplicativos da área de trabalho do Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="3bb21-125">Windows 10 \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="3bb21-126">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3bb21-126">Minimum supported server</span></span><br/> | <span data-ttu-id="3bb21-127">\[Somente aplicativos da área de trabalho do Windows Server 2016\]</span><span class="sxs-lookup"><span data-stu-id="3bb21-127">Windows Server 2016 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="3bb21-128">parâmetro</span><span class="sxs-lookup"><span data-stu-id="3bb21-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="3bb21-129"><dt>WinUser. h</dt></span><span class="sxs-lookup"><span data-stu-id="3bb21-129"><dt>Winuser.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3bb21-130">Confira também</span><span class="sxs-lookup"><span data-stu-id="3bb21-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3bb21-131">Constantes de configuração</span><span class="sxs-lookup"><span data-stu-id="3bb21-131">Configuration Constants</span></span>](configuration-constants.md)
</dt> <dt>

[<span data-ttu-id="3bb21-132">**Visualização de contato**</span><span class="sxs-lookup"><span data-stu-id="3bb21-132">**Contact Visualization**</span></span>](contact-visualization.md)
</dt> <dt>

[<span data-ttu-id="3bb21-133">**SystemParametersInfo**</span><span class="sxs-lookup"><span data-stu-id="3bb21-133">**SystemParametersInfo**</span></span>](/windows/win32/api/winuser/nf-winuser-systemparametersinfoa)
</dt> <dt>

[<span data-ttu-id="3bb21-134">Configuração de comentários de entrada</span><span class="sxs-lookup"><span data-stu-id="3bb21-134">Input Feedback Configuration</span></span>](/previous-versions/windows/desktop/input_feedback/input-feedback-configuration-portal)
</dt> </dl>

 

