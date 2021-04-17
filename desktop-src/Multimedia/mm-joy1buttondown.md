---
title: Mensagem de MM_JOY1BUTTONDOWN (mmsystem. h)
description: A \_ mensagem mm JOY1BUTTONDOWN notifica a janela que capturou o joystick JOYSTICKID1 de que um botão foi pressionado.
ms.assetid: 764f4bb4-134d-46b8-badb-3fb06af31e13
keywords:
- Multimídia do Windows de mensagem MM_JOY1BUTTONDOWN
topic_type:
- apiref
api_name:
- MM_JOY1BUTTONDOWN
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cefb70e5dd47fc14b39dcdeb59043b6827e7b89b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104454742"
---
# <a name="mm_joy1buttondown-message"></a><span data-ttu-id="d7a19-104">\_Mensagem mm JOY1BUTTONDOWN</span><span class="sxs-lookup"><span data-stu-id="d7a19-104">MM\_JOY1BUTTONDOWN message</span></span>

<span data-ttu-id="d7a19-105">A mensagem **mm \_ JOY1BUTTONDOWN** notifica a janela que CAPTUROU o joystick JOYSTICKID1 de que um botão foi pressionado.</span><span class="sxs-lookup"><span data-stu-id="d7a19-105">The **MM\_JOY1BUTTONDOWN** message notifies the window that has captured joystick JOYSTICKID1 that a button has been pressed.</span></span>


```C++
MM_JOY1BUTTONDOWN 
fwButtons = wParam; 
xPos = LOWORD(lParam); 
yPos = HIWORD(lParam); 
```



## <a name="parameters"></a><span data-ttu-id="d7a19-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="d7a19-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d7a19-107"><span id="fwButtons"></span><span id="fwbuttons"></span><span id="FWBUTTONS"></span>*fwButtons*</span><span class="sxs-lookup"><span data-stu-id="d7a19-107"><span id="fwButtons"></span><span id="fwbuttons"></span><span id="FWBUTTONS"></span>*fwButtons*</span></span>
</dt> <dd>

<span data-ttu-id="d7a19-108">Identifica o botão que alterou o estado e os botões que são pressionados.</span><span class="sxs-lookup"><span data-stu-id="d7a19-108">Identifies the button that has changed state and the buttons that are pressed.</span></span> <span data-ttu-id="d7a19-109">Pode ser um dos seguintes:</span><span class="sxs-lookup"><span data-stu-id="d7a19-109">It can be one of the following:</span></span>



| <span data-ttu-id="d7a19-110">Requisito</span><span class="sxs-lookup"><span data-stu-id="d7a19-110">Requirement</span></span> | <span data-ttu-id="d7a19-111">Valor</span><span class="sxs-lookup"><span data-stu-id="d7a19-111">Value</span></span> |
|-----------------|-------------------------------------------|
| <span data-ttu-id="d7a19-112">BUTTON1CHG de alegria \_</span><span class="sxs-lookup"><span data-stu-id="d7a19-112">JOY\_BUTTON1CHG</span></span> | <span data-ttu-id="d7a19-113">O primeiro botão de joystick alterou o estado.</span><span class="sxs-lookup"><span data-stu-id="d7a19-113">First joystick button has changed state.</span></span>  |
| <span data-ttu-id="d7a19-114">BUTTON2CHG de alegria \_</span><span class="sxs-lookup"><span data-stu-id="d7a19-114">JOY\_BUTTON2CHG</span></span> | <span data-ttu-id="d7a19-115">O segundo botão de joystick alterou o estado.</span><span class="sxs-lookup"><span data-stu-id="d7a19-115">Second joystick button has changed state.</span></span> |
| <span data-ttu-id="d7a19-116">BUTTON3CHG de alegria \_</span><span class="sxs-lookup"><span data-stu-id="d7a19-116">JOY\_BUTTON3CHG</span></span> | <span data-ttu-id="d7a19-117">O terceiro botão de joystick alterou o estado.</span><span class="sxs-lookup"><span data-stu-id="d7a19-117">Third joystick button has changed state.</span></span>  |
| <span data-ttu-id="d7a19-118">BUTTON4CHG de alegria \_</span><span class="sxs-lookup"><span data-stu-id="d7a19-118">JOY\_BUTTON4CHG</span></span> | <span data-ttu-id="d7a19-119">O quarto botão de joystick alterou o estado.</span><span class="sxs-lookup"><span data-stu-id="d7a19-119">Fourth joystick button has changed state.</span></span> |



 

<span data-ttu-id="d7a19-120">e um ou mais dos seguintes:</span><span class="sxs-lookup"><span data-stu-id="d7a19-120">and one or more of the following:</span></span>



| <span data-ttu-id="d7a19-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="d7a19-121">Requirement</span></span> | <span data-ttu-id="d7a19-122">Valor</span><span class="sxs-lookup"><span data-stu-id="d7a19-122">Value</span></span> |
|--------------|------------------------------------|
| <span data-ttu-id="d7a19-123">JOY \_ Button1</span><span class="sxs-lookup"><span data-stu-id="d7a19-123">JOY\_BUTTON1</span></span> | <span data-ttu-id="d7a19-124">O primeiro botão de joystick é pressionado.</span><span class="sxs-lookup"><span data-stu-id="d7a19-124">First joystick button is pressed.</span></span>  |
| <span data-ttu-id="d7a19-125">JOY \_ Button1</span><span class="sxs-lookup"><span data-stu-id="d7a19-125">JOY\_BUTTON2</span></span> | <span data-ttu-id="d7a19-126">O segundo botão de joystick é pressionado.</span><span class="sxs-lookup"><span data-stu-id="d7a19-126">Second joystick button is pressed.</span></span> |
| <span data-ttu-id="d7a19-127">BUTTON3 de alegria \_</span><span class="sxs-lookup"><span data-stu-id="d7a19-127">JOY\_BUTTON3</span></span> | <span data-ttu-id="d7a19-128">O terceiro botão de joystick é pressionado.</span><span class="sxs-lookup"><span data-stu-id="d7a19-128">Third joystick button is pressed.</span></span>  |
| <span data-ttu-id="d7a19-129">BUTTON4 de alegria \_</span><span class="sxs-lookup"><span data-stu-id="d7a19-129">JOY\_BUTTON4</span></span> | <span data-ttu-id="d7a19-130">O quarto botão de joystick é pressionado.</span><span class="sxs-lookup"><span data-stu-id="d7a19-130">Fourth joystick button is pressed.</span></span> |



 

</dd> <dt>

<span data-ttu-id="d7a19-131"><span id="xPos"></span><span id="xpos"></span><span id="XPOS"></span>*xPos*</span><span class="sxs-lookup"><span data-stu-id="d7a19-131"><span id="xPos"></span><span id="xpos"></span><span id="XPOS"></span>*xPos*</span></span>
</dt> <dd>

<span data-ttu-id="d7a19-132">A coordenada x do joystick em relação ao canto superior esquerdo da área do cliente.</span><span class="sxs-lookup"><span data-stu-id="d7a19-132">The x-coordinate of the joystick relative to the upper left corner of the client area.</span></span>

</dd> <dt>

<span data-ttu-id="d7a19-133"><span id="yPos"></span><span id="ypos"></span><span id="YPOS"></span>*yPos*</span><span class="sxs-lookup"><span data-stu-id="d7a19-133"><span id="yPos"></span><span id="ypos"></span><span id="YPOS"></span>*yPos*</span></span>
</dt> <dd>

<span data-ttu-id="d7a19-134">A coordenada y do joystick em relação ao canto superior esquerdo da área do cliente.</span><span class="sxs-lookup"><span data-stu-id="d7a19-134">The y-coordinate of the joystick relative to the upper left corner of the client area.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="d7a19-135">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d7a19-135">Requirements</span></span>



| <span data-ttu-id="d7a19-136">Requisito</span><span class="sxs-lookup"><span data-stu-id="d7a19-136">Requirement</span></span> | <span data-ttu-id="d7a19-137">Valor</span><span class="sxs-lookup"><span data-stu-id="d7a19-137">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d7a19-138">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d7a19-138">Minimum supported client</span></span><br/> | <span data-ttu-id="d7a19-139">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="d7a19-139">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="d7a19-140">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d7a19-140">Minimum supported server</span></span><br/> | <span data-ttu-id="d7a19-141">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="d7a19-141">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="d7a19-142">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="d7a19-142">Header</span></span><br/>                   | <dl> <span data-ttu-id="d7a19-143"><dt>Mmsystem. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="d7a19-143"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d7a19-144">Confira também</span><span class="sxs-lookup"><span data-stu-id="d7a19-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d7a19-145">Joysticks</span><span class="sxs-lookup"><span data-stu-id="d7a19-145">Joysticks</span></span>](joysticks.md)
</dt> <dt>

[<span data-ttu-id="d7a19-146">Mensagens do joystick de multimídia</span><span class="sxs-lookup"><span data-stu-id="d7a19-146">Multimedia Joystick Messages</span></span>](multimedia-joystick-messages.md)
</dt> </dl>

 

 





