---
title: Mensagem de MM_JOY2BUTTONDOWN (mmsystem. h)
description: A \_ mensagem mm JOY2BUTTONDOWN notifica a janela que capturou o joystick JOYSTICKID2 de que um botão foi pressionado.
ms.assetid: b4cd48ea-91ad-48e9-b0ae-58d8ee124171
keywords:
- Multimídia do Windows de mensagem MM_JOY2BUTTONDOWN
topic_type:
- apiref
api_name:
- MM_JOY2BUTTONDOWN
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f155fcdc21247e01fd5d730f3f7d4daaba705e65
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105759199"
---
# <a name="mm_joy2buttondown-message"></a><span data-ttu-id="82655-104">\_Mensagem mm JOY2BUTTONDOWN</span><span class="sxs-lookup"><span data-stu-id="82655-104">MM\_JOY2BUTTONDOWN message</span></span>

<span data-ttu-id="82655-105">A mensagem **mm \_ JOY2BUTTONDOWN** notifica a janela que CAPTUROU o joystick JOYSTICKID2 de que um botão foi pressionado.</span><span class="sxs-lookup"><span data-stu-id="82655-105">The **MM\_JOY2BUTTONDOWN** message notifies the window that has captured joystick JOYSTICKID2 that a button has been pressed.</span></span>


```C++
MM_JOY2BUTTONDOWN 
fwButtons = wParam; 
xPos = LOWORD(lParam); 
yPos = HIWORD(lParam); 
```



## <a name="parameters"></a><span data-ttu-id="82655-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="82655-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="82655-107"><span id="fwButtons"></span><span id="fwbuttons"></span><span id="FWBUTTONS"></span>*fwButtons*</span><span class="sxs-lookup"><span data-stu-id="82655-107"><span id="fwButtons"></span><span id="fwbuttons"></span><span id="FWBUTTONS"></span>*fwButtons*</span></span>
</dt> <dd>

<span data-ttu-id="82655-108">Identifica o botão que alterou o estado e os botões que são pressionados.</span><span class="sxs-lookup"><span data-stu-id="82655-108">Identifies the button that has changed state and the buttons that are pressed.</span></span> <span data-ttu-id="82655-109">Pode ser um dos seguintes:</span><span class="sxs-lookup"><span data-stu-id="82655-109">It can be one of the following:</span></span>



| <span data-ttu-id="82655-110">Requisito</span><span class="sxs-lookup"><span data-stu-id="82655-110">Requirement</span></span> | <span data-ttu-id="82655-111">Valor</span><span class="sxs-lookup"><span data-stu-id="82655-111">Value</span></span> |
|-----------------|-------------------------------------------|
| <span data-ttu-id="82655-112">BUTTON1CHG de alegria \_</span><span class="sxs-lookup"><span data-stu-id="82655-112">JOY\_BUTTON1CHG</span></span> | <span data-ttu-id="82655-113">O primeiro botão de joystick alterou o estado.</span><span class="sxs-lookup"><span data-stu-id="82655-113">First joystick button has changed state.</span></span>  |
| <span data-ttu-id="82655-114">BUTTON2CHG de alegria \_</span><span class="sxs-lookup"><span data-stu-id="82655-114">JOY\_BUTTON2CHG</span></span> | <span data-ttu-id="82655-115">O segundo botão de joystick alterou o estado.</span><span class="sxs-lookup"><span data-stu-id="82655-115">Second joystick button has changed state.</span></span> |
| <span data-ttu-id="82655-116">BUTTON3CHG de alegria \_</span><span class="sxs-lookup"><span data-stu-id="82655-116">JOY\_BUTTON3CHG</span></span> | <span data-ttu-id="82655-117">O terceiro botão de joystick alterou o estado.</span><span class="sxs-lookup"><span data-stu-id="82655-117">Third joystick button has changed state.</span></span>  |
| <span data-ttu-id="82655-118">BUTTON4CHG de alegria \_</span><span class="sxs-lookup"><span data-stu-id="82655-118">JOY\_BUTTON4CHG</span></span> | <span data-ttu-id="82655-119">O quarto botão de joystick alterou o estado.</span><span class="sxs-lookup"><span data-stu-id="82655-119">Fourth joystick button has changed state.</span></span> |



 

<span data-ttu-id="82655-120">e um ou mais dos seguintes:</span><span class="sxs-lookup"><span data-stu-id="82655-120">and one or more of the following:</span></span>



| <span data-ttu-id="82655-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="82655-121">Requirement</span></span> | <span data-ttu-id="82655-122">Valor</span><span class="sxs-lookup"><span data-stu-id="82655-122">Value</span></span> |
|--------------|------------------------------------|
| <span data-ttu-id="82655-123">JOY \_ Button1</span><span class="sxs-lookup"><span data-stu-id="82655-123">JOY\_BUTTON1</span></span> | <span data-ttu-id="82655-124">O primeiro botão de joystick é pressionado.</span><span class="sxs-lookup"><span data-stu-id="82655-124">First joystick button is pressed.</span></span>  |
| <span data-ttu-id="82655-125">JOY \_ Button1</span><span class="sxs-lookup"><span data-stu-id="82655-125">JOY\_BUTTON2</span></span> | <span data-ttu-id="82655-126">O segundo botão de joystick é pressionado.</span><span class="sxs-lookup"><span data-stu-id="82655-126">Second joystick button is pressed.</span></span> |
| <span data-ttu-id="82655-127">BUTTON3 de alegria \_</span><span class="sxs-lookup"><span data-stu-id="82655-127">JOY\_BUTTON3</span></span> | <span data-ttu-id="82655-128">O terceiro botão de joystick é pressionado.</span><span class="sxs-lookup"><span data-stu-id="82655-128">Third joystick button is pressed.</span></span>  |
| <span data-ttu-id="82655-129">BUTTON4 de alegria \_</span><span class="sxs-lookup"><span data-stu-id="82655-129">JOY\_BUTTON4</span></span> | <span data-ttu-id="82655-130">O quarto botão de joystick é pressionado.</span><span class="sxs-lookup"><span data-stu-id="82655-130">Fourth joystick button is pressed.</span></span> |



 

</dd> <dt>

<span data-ttu-id="82655-131"><span id="xPos"></span><span id="xpos"></span><span id="XPOS"></span>*xPos*</span><span class="sxs-lookup"><span data-stu-id="82655-131"><span id="xPos"></span><span id="xpos"></span><span id="XPOS"></span>*xPos*</span></span>
</dt> <dd>

<span data-ttu-id="82655-132">As coordenadas x do joystick em relação ao canto superior esquerdo da área do cliente.</span><span class="sxs-lookup"><span data-stu-id="82655-132">The x-coordinates of the joystick relative to the upper left corner of the client area.</span></span>

</dd> <dt>

<span data-ttu-id="82655-133"><span id="yPos"></span><span id="ypos"></span><span id="YPOS"></span>*yPos*</span><span class="sxs-lookup"><span data-stu-id="82655-133"><span id="yPos"></span><span id="ypos"></span><span id="YPOS"></span>*yPos*</span></span>
</dt> <dd>

<span data-ttu-id="82655-134">A coordenada y do joystick em relação ao canto superior esquerdo da área do cliente.</span><span class="sxs-lookup"><span data-stu-id="82655-134">The y-coordinate of the joystick relative to the upper left corner of the client area.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="82655-135">Requisitos</span><span class="sxs-lookup"><span data-stu-id="82655-135">Requirements</span></span>



| <span data-ttu-id="82655-136">Requisito</span><span class="sxs-lookup"><span data-stu-id="82655-136">Requirement</span></span> | <span data-ttu-id="82655-137">Valor</span><span class="sxs-lookup"><span data-stu-id="82655-137">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="82655-138">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="82655-138">Minimum supported client</span></span><br/> | <span data-ttu-id="82655-139">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="82655-139">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="82655-140">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="82655-140">Minimum supported server</span></span><br/> | <span data-ttu-id="82655-141">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="82655-141">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="82655-142">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="82655-142">Header</span></span><br/>                   | <dl> <span data-ttu-id="82655-143"><dt>Mmsystem. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="82655-143"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="82655-144">Confira também</span><span class="sxs-lookup"><span data-stu-id="82655-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="82655-145">Joysticks</span><span class="sxs-lookup"><span data-stu-id="82655-145">Joysticks</span></span>](joysticks.md)
</dt> <dt>

[<span data-ttu-id="82655-146">Mensagens do joystick de multimídia</span><span class="sxs-lookup"><span data-stu-id="82655-146">Multimedia Joystick Messages</span></span>](multimedia-joystick-messages.md)
</dt> </dl>

 

 





