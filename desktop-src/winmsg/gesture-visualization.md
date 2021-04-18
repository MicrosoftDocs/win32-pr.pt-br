---
description: As constantes a seguir são usadas por aplicativos ou estruturas de interface do usuário para identificar como os comentários da interface do usuário são processados quando um dos gestos listados é detectado.
ms.assetid: 76D3DFF4-7BB2-49A9-8251-0B5D9376B649
title: Visualização do gesto (WinUser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 551934380e1d5ec0902818466f5840e1dc6718e9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105764080"
---
# <a name="gesture-visualization"></a><span data-ttu-id="11743-103">Visualização do gesto</span><span class="sxs-lookup"><span data-stu-id="11743-103">Gesture Visualization</span></span>

<span data-ttu-id="11743-104">As constantes a seguir são usadas por aplicativos ou estruturas de interface do usuário para identificar como os comentários da interface do usuário são processados quando um dos gestos listados é detectado.</span><span class="sxs-lookup"><span data-stu-id="11743-104">The following constants are used by applications or UI frameworks to identify how UI feedback is processed when one of the listed gestures is detected.</span></span>

<span data-ttu-id="11743-105">Essas constantes são usadas com os parâmetros **SPI \_ GETGESTUREVISUALIZATION** e **SPI \_ SETGESTUREVISUALIZATION** e a função [**SystemParametersInfo**](/windows/win32/api/winuser/nf-winuser-systemparametersinfoa) .</span><span class="sxs-lookup"><span data-stu-id="11743-105">These constants are used with the **SPI\_GETGESTUREVISUALIZATION** and **SPI\_SETGESTUREVISUALIZATION** parameters and the [**SystemParametersInfo**](/windows/win32/api/winuser/nf-winuser-systemparametersinfoa) function.</span></span>

<span data-ttu-id="11743-106">**Observação**</span><span class="sxs-lookup"><span data-stu-id="11743-106">**Note**</span></span>  

<span data-ttu-id="11743-107">Para recuperar ou definir informações de visualização da caneta, recomendamos que você use os parâmetros **SPI \_ GETPENVISUALIZATION** e **SPI \_ SETPENVISUALIZATION** e as constantes listadas na [**visualização de caneta**](pen-visualization.md).</span><span class="sxs-lookup"><span data-stu-id="11743-107">For retrieving or setting pen visualization info, we recommend that you use the **SPI\_GETPENVISUALIZATION** and **SPI\_SETPENVISUALIZATION** parameters and the constants listed in [**Pen Visualization**](pen-visualization.md).</span></span>

<dl> <dt>

<span data-ttu-id="11743-108"><span id="GESTUREVISUALIZATION_OFF"></span><span id="gesturevisualization_off"></span>**GESTUREVISUALIZATION \_ desativado**</span><span class="sxs-lookup"><span data-stu-id="11743-108"><span id="GESTUREVISUALIZATION_OFF"></span><span id="gesturevisualization_off"></span>**GESTUREVISUALIZATION\_OFF**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="11743-109">0x0000</span><span class="sxs-lookup"><span data-stu-id="11743-109">0x0000</span></span>
</dt> <dt>



<span data-ttu-id="11743-110">Especifica que os comentários da interface do usuário para todos os gestos estão desativados.</span><span class="sxs-lookup"><span data-stu-id="11743-110">Specifies that UI feedback for all gestures is off.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="11743-111"><span id="GESTUREVISUALIZATION_ON"></span><span id="gesturevisualization_on"></span>**GESTUREVISUALIZATION \_ em**</span><span class="sxs-lookup"><span data-stu-id="11743-111"><span id="GESTUREVISUALIZATION_ON"></span><span id="gesturevisualization_on"></span>**GESTUREVISUALIZATION\_ON**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="11743-112">0x001F</span><span class="sxs-lookup"><span data-stu-id="11743-112">0x001F</span></span>
</dt> <dt>



<span data-ttu-id="11743-113">Especifica que os comentários da interface do usuário para todos os gestos estão ativados.</span><span class="sxs-lookup"><span data-stu-id="11743-113">Specifies that UI feedback for all gestures is on.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="11743-114"><span id="GESTUREVISUALIZATION_TAP"></span><span id="gesturevisualization_tap"></span>**\_toque GESTUREVISUALIZATION**</span><span class="sxs-lookup"><span data-stu-id="11743-114"><span id="GESTUREVISUALIZATION_TAP"></span><span id="gesturevisualization_tap"></span>**GESTUREVISUALIZATION\_TAP**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="11743-115">0x0001</span><span class="sxs-lookup"><span data-stu-id="11743-115">0x0001</span></span>
</dt> <dt>



<span data-ttu-id="11743-116">Especifica comentários da interface do usuário para um toque.</span><span class="sxs-lookup"><span data-stu-id="11743-116">Specifies UI feedback for a tap.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="11743-117"><span id="GESTUREVISUALIZATION_DOUBLETAP"></span><span id="gesturevisualization_doubletap"></span>**GESTUREVISUALIZATION \_ DOUBLETAP**</span><span class="sxs-lookup"><span data-stu-id="11743-117"><span id="GESTUREVISUALIZATION_DOUBLETAP"></span><span id="gesturevisualization_doubletap"></span>**GESTUREVISUALIZATION\_DOUBLETAP**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="11743-118">0x0002</span><span class="sxs-lookup"><span data-stu-id="11743-118">0x0002</span></span>
</dt> <dt>



<span data-ttu-id="11743-119">Especifica comentários da interface do usuário para um toque duplo.</span><span class="sxs-lookup"><span data-stu-id="11743-119">Specifies UI feedback for a double tap.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="11743-120"><span id="GESTUREVISUALIZATION_PRESSANDTAP"></span><span id="gesturevisualization_pressandtap"></span>**GESTUREVISUALIZATION \_ PRESSANDTAP**</span><span class="sxs-lookup"><span data-stu-id="11743-120"><span id="GESTUREVISUALIZATION_PRESSANDTAP"></span><span id="gesturevisualization_pressandtap"></span>**GESTUREVISUALIZATION\_PRESSANDTAP**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="11743-121">0x0004</span><span class="sxs-lookup"><span data-stu-id="11743-121">0x0004</span></span>
</dt> <dt>



<span data-ttu-id="11743-122">Especifica comentários da interface do usuário para uma operação pressionar e tocar.</span><span class="sxs-lookup"><span data-stu-id="11743-122">Specifies UI feedback for a press and tap.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="11743-123"><span id="GESTUREVISUALIZATION_PRESSANDHOLD"></span><span id="gesturevisualization_pressandhold"></span>**GESTUREVISUALIZATION \_ PRESSANDHOLD**</span><span class="sxs-lookup"><span data-stu-id="11743-123"><span id="GESTUREVISUALIZATION_PRESSANDHOLD"></span><span id="gesturevisualization_pressandhold"></span>**GESTUREVISUALIZATION\_PRESSANDHOLD**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="11743-124">0x0008</span><span class="sxs-lookup"><span data-stu-id="11743-124">0x0008</span></span>
</dt> <dt>



<span data-ttu-id="11743-125">Especifica os comentários da interface do usuário para uma operação de pressionar e manter pressionado.</span><span class="sxs-lookup"><span data-stu-id="11743-125">Specifies UI feedback for a press and hold.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="11743-126"><span id="GESTUREVISUALIZATION_RIGHTTAP"></span><span id="gesturevisualization_righttap"></span>**GESTUREVISUALIZATION \_ RIGHTTAP**</span><span class="sxs-lookup"><span data-stu-id="11743-126"><span id="GESTUREVISUALIZATION_RIGHTTAP"></span><span id="gesturevisualization_righttap"></span>**GESTUREVISUALIZATION\_RIGHTTAP**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="11743-127">0x0010</span><span class="sxs-lookup"><span data-stu-id="11743-127">0x0010</span></span>
</dt> <dt>



<span data-ttu-id="11743-128">Especifica comentários da interface do usuário para um toque à direita.</span><span class="sxs-lookup"><span data-stu-id="11743-128">Specifies UI feedback for a right tap.</span></span>


</dt> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="11743-129">Requisitos</span><span class="sxs-lookup"><span data-stu-id="11743-129">Requirements</span></span>



| <span data-ttu-id="11743-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="11743-130">Requirement</span></span> | <span data-ttu-id="11743-131">Valor</span><span class="sxs-lookup"><span data-stu-id="11743-131">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="11743-132">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="11743-132">Minimum supported client</span></span><br/> | <span data-ttu-id="11743-133">\[Somente aplicativos de área de trabalho do Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="11743-133">Windows 8 \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="11743-134">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="11743-134">Minimum supported server</span></span><br/> | <span data-ttu-id="11743-135">\[Somente aplicativos da área de trabalho do Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="11743-135">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="11743-136">parâmetro</span><span class="sxs-lookup"><span data-stu-id="11743-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="11743-137"><dt>WinUser. h</dt></span><span class="sxs-lookup"><span data-stu-id="11743-137"><dt>Winuser.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="11743-138">Confira também</span><span class="sxs-lookup"><span data-stu-id="11743-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="11743-139">Constantes de configuração</span><span class="sxs-lookup"><span data-stu-id="11743-139">Configuration Constants</span></span>](configuration-constants.md)
</dt> <dt>

[<span data-ttu-id="11743-140">**Visualização de contato**</span><span class="sxs-lookup"><span data-stu-id="11743-140">**Contact Visualization**</span></span>](contact-visualization.md)
</dt> <dt>

[<span data-ttu-id="11743-141">**SystemParametersInfo**</span><span class="sxs-lookup"><span data-stu-id="11743-141">**SystemParametersInfo**</span></span>](/windows/win32/api/winuser/nf-winuser-systemparametersinfoa)
</dt> <dt>

[<span data-ttu-id="11743-142">Configuração de comentários de entrada</span><span class="sxs-lookup"><span data-stu-id="11743-142">Input Feedback Configuration</span></span>](/previous-versions/windows/desktop/input_feedback/input-feedback-configuration-portal)
</dt> </dl>

 

