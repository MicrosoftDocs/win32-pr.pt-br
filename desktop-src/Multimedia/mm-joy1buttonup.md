---
title: Mensagem de MM_JOY1BUTTONUP (mmsystem. h)
description: A \_ mensagem mm JOY1BUTTONUP notifica a janela que capturou o joystick JOYSTICKID1 de que um botão foi liberado.
ms.assetid: 37f0f87a-4805-4cec-9c0c-9d6b36a3ff0d
keywords:
- Multimídia do Windows de mensagem MM_JOY1BUTTONUP
topic_type:
- apiref
api_name:
- MM_JOY1BUTTONUP
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 007a5d954b9b879f87c5e8ffe2d0774d0d1d85a3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104086504"
---
# <a name="mm_joy1buttonup-message"></a><span data-ttu-id="d520a-104">\_Mensagem mm JOY1BUTTONUP</span><span class="sxs-lookup"><span data-stu-id="d520a-104">MM\_JOY1BUTTONUP message</span></span>

<span data-ttu-id="d520a-105">A mensagem **mm \_ JOY1BUTTONUP** notifica a janela que CAPTUROU o joystick JOYSTICKID1 de que um botão foi liberado.</span><span class="sxs-lookup"><span data-stu-id="d520a-105">The **MM\_JOY1BUTTONUP** message notifies the window that has captured joystick JOYSTICKID1 that a button has been released.</span></span>


```C++
MM_JOY1BUTTONUP 
fwButtons = wParam; 
xPos = LOWORD(lParam); 
yPos = HIWORD(lParam); 
```



## <a name="parameters"></a><span data-ttu-id="d520a-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="d520a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d520a-107"><span id="fwButtons"></span><span id="fwbuttons"></span><span id="FWBUTTONS"></span>*fwButtons*</span><span class="sxs-lookup"><span data-stu-id="d520a-107"><span id="fwButtons"></span><span id="fwbuttons"></span><span id="FWBUTTONS"></span>*fwButtons*</span></span>
</dt> <dd>

<span data-ttu-id="d520a-108">Identifica o botão que alterou o estado e os botões que são pressionados.</span><span class="sxs-lookup"><span data-stu-id="d520a-108">Identifies the button that has changed state and the buttons that are pressed.</span></span> <span data-ttu-id="d520a-109">Pode ser um dos seguintes:</span><span class="sxs-lookup"><span data-stu-id="d520a-109">It can be one of the following:</span></span>



| <span data-ttu-id="d520a-110">Requisito</span><span class="sxs-lookup"><span data-stu-id="d520a-110">Requirement</span></span> | <span data-ttu-id="d520a-111">Valor</span><span class="sxs-lookup"><span data-stu-id="d520a-111">Value</span></span> |
|-----------------|-------------------------------------------|
| <span data-ttu-id="d520a-112">BUTTON1CHG de alegria \_</span><span class="sxs-lookup"><span data-stu-id="d520a-112">JOY\_BUTTON1CHG</span></span> | <span data-ttu-id="d520a-113">O primeiro botão de joystick alterou o estado.</span><span class="sxs-lookup"><span data-stu-id="d520a-113">First joystick button has changed state.</span></span>  |
| <span data-ttu-id="d520a-114">BUTTON2CHG de alegria \_</span><span class="sxs-lookup"><span data-stu-id="d520a-114">JOY\_BUTTON2CHG</span></span> | <span data-ttu-id="d520a-115">O segundo botão de joystick alterou o estado.</span><span class="sxs-lookup"><span data-stu-id="d520a-115">Second joystick button has changed state.</span></span> |
| <span data-ttu-id="d520a-116">BUTTON3CHG de alegria \_</span><span class="sxs-lookup"><span data-stu-id="d520a-116">JOY\_BUTTON3CHG</span></span> | <span data-ttu-id="d520a-117">O terceiro botão de joystick alterou o estado.</span><span class="sxs-lookup"><span data-stu-id="d520a-117">Third joystick button has changed state.</span></span>  |
| <span data-ttu-id="d520a-118">BUTTON4CHG de alegria \_</span><span class="sxs-lookup"><span data-stu-id="d520a-118">JOY\_BUTTON4CHG</span></span> | <span data-ttu-id="d520a-119">O quarto botão de joystick alterou o estado.</span><span class="sxs-lookup"><span data-stu-id="d520a-119">Fourth joystick button has changed state.</span></span> |



 

<span data-ttu-id="d520a-120">e um ou mais dos seguintes:</span><span class="sxs-lookup"><span data-stu-id="d520a-120">and one or more of the following:</span></span>



| <span data-ttu-id="d520a-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="d520a-121">Requirement</span></span> | <span data-ttu-id="d520a-122">Valor</span><span class="sxs-lookup"><span data-stu-id="d520a-122">Value</span></span> |
|--------------|------------------------------------|
| <span data-ttu-id="d520a-123">JOY \_ Button1</span><span class="sxs-lookup"><span data-stu-id="d520a-123">JOY\_BUTTON1</span></span> | <span data-ttu-id="d520a-124">O primeiro botão de joystick é pressionado.</span><span class="sxs-lookup"><span data-stu-id="d520a-124">First joystick button is pressed.</span></span>  |
| <span data-ttu-id="d520a-125">JOY \_ Button1</span><span class="sxs-lookup"><span data-stu-id="d520a-125">JOY\_BUTTON2</span></span> | <span data-ttu-id="d520a-126">O segundo botão de joystick é pressionado.</span><span class="sxs-lookup"><span data-stu-id="d520a-126">Second joystick button is pressed.</span></span> |
| <span data-ttu-id="d520a-127">BUTTON3 de alegria \_</span><span class="sxs-lookup"><span data-stu-id="d520a-127">JOY\_BUTTON3</span></span> | <span data-ttu-id="d520a-128">O terceiro botão de joystick é pressionado.</span><span class="sxs-lookup"><span data-stu-id="d520a-128">Third joystick button is pressed.</span></span>  |
| <span data-ttu-id="d520a-129">BUTTON4 de alegria \_</span><span class="sxs-lookup"><span data-stu-id="d520a-129">JOY\_BUTTON4</span></span> | <span data-ttu-id="d520a-130">O quarto botão de joystick é pressionado.</span><span class="sxs-lookup"><span data-stu-id="d520a-130">Fourth joystick button is pressed.</span></span> |



 

</dd> <dt>

<span data-ttu-id="d520a-131"><span id="xPos"></span><span id="xpos"></span><span id="XPOS"></span>*xPos*</span><span class="sxs-lookup"><span data-stu-id="d520a-131"><span id="xPos"></span><span id="xpos"></span><span id="XPOS"></span>*xPos*</span></span>
</dt> <dd>

<span data-ttu-id="d520a-132">As coordenadas x do joystick em relação ao canto superior esquerdo da área do cliente.</span><span class="sxs-lookup"><span data-stu-id="d520a-132">The x-coordinates of the joystick relative to the upper left corner of the client area.</span></span>

</dd> <dt>

<span data-ttu-id="d520a-133"><span id="yPos"></span><span id="ypos"></span><span id="YPOS"></span>*yPos*</span><span class="sxs-lookup"><span data-stu-id="d520a-133"><span id="yPos"></span><span id="ypos"></span><span id="YPOS"></span>*yPos*</span></span>
</dt> <dd>

<span data-ttu-id="d520a-134">A coordenada y do joystick em relação ao canto superior esquerdo da área do cliente.</span><span class="sxs-lookup"><span data-stu-id="d520a-134">The y-coordinate of the joystick relative to the upper left corner of the client area.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="d520a-135">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d520a-135">Requirements</span></span>



| <span data-ttu-id="d520a-136">Requisito</span><span class="sxs-lookup"><span data-stu-id="d520a-136">Requirement</span></span> | <span data-ttu-id="d520a-137">Valor</span><span class="sxs-lookup"><span data-stu-id="d520a-137">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d520a-138">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d520a-138">Minimum supported client</span></span><br/> | <span data-ttu-id="d520a-139">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="d520a-139">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="d520a-140">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d520a-140">Minimum supported server</span></span><br/> | <span data-ttu-id="d520a-141">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="d520a-141">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="d520a-142">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="d520a-142">Header</span></span><br/>                   | <dl> <span data-ttu-id="d520a-143"><dt>Mmsystem. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="d520a-143"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d520a-144">Confira também</span><span class="sxs-lookup"><span data-stu-id="d520a-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d520a-145">Joysticks</span><span class="sxs-lookup"><span data-stu-id="d520a-145">Joysticks</span></span>](joysticks.md)
</dt> <dt>

[<span data-ttu-id="d520a-146">Mensagens do joystick de multimídia</span><span class="sxs-lookup"><span data-stu-id="d520a-146">Multimedia Joystick Messages</span></span>](multimedia-joystick-messages.md)
</dt> </dl>

 

 





