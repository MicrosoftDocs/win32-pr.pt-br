---
title: Mensagem de MM_JOY2BUTTONUP (mmsystem. h)
description: A \_ mensagem mm JOY2BUTTONUP notifica a janela que capturou o joystick JOYSTICKID2 de que um botão foi liberado.
ms.assetid: da024466-7cd3-42ec-90a7-1468eb42841e
keywords:
- Multimídia do Windows de mensagem MM_JOY2BUTTONUP
topic_type:
- apiref
api_name:
- MM_JOY2BUTTONUP
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d7a4f2d23739fc72a6898e2b53fc3e1c330687f7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105811084"
---
# <a name="mm_joy2buttonup-message"></a><span data-ttu-id="d8294-104">\_Mensagem mm JOY2BUTTONUP</span><span class="sxs-lookup"><span data-stu-id="d8294-104">MM\_JOY2BUTTONUP message</span></span>

<span data-ttu-id="d8294-105">A mensagem **mm \_ JOY2BUTTONUP** notifica a janela que CAPTUROU o joystick JOYSTICKID2 de que um botão foi liberado.</span><span class="sxs-lookup"><span data-stu-id="d8294-105">The **MM\_JOY2BUTTONUP** message notifies the window that has captured joystick JOYSTICKID2 that a button has been released.</span></span>


```C++
MM_JOY2BUTTONUP 
fwButton = wParam; 
xPos = LOWORD(lParam); 
yPos = HIWORD(lParam); 
```



## <a name="parameters"></a><span data-ttu-id="d8294-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="d8294-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d8294-107">**fwButtons**</span><span class="sxs-lookup"><span data-stu-id="d8294-107">**fwButtons**</span></span> 
</dt> <dd>

<span data-ttu-id="d8294-108">Identifica o botão que alterou o estado e os botões que são pressionados.</span><span class="sxs-lookup"><span data-stu-id="d8294-108">Identifies the button that has changed state and the buttons that are pressed.</span></span> <span data-ttu-id="d8294-109">Pode ser um dos seguintes:</span><span class="sxs-lookup"><span data-stu-id="d8294-109">It can be one of the following:</span></span>



| <span data-ttu-id="d8294-110">Valor</span><span class="sxs-lookup"><span data-stu-id="d8294-110">Value</span></span>                                                                                                                                                            | <span data-ttu-id="d8294-111">Significado</span><span class="sxs-lookup"><span data-stu-id="d8294-111">Meaning</span></span>                                              |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------|
| <span id="JOY_BUTTON1CHG"></span><span id="joy_button1chg"></span><dl> <span data-ttu-id="d8294-112"><dt>**BUTTON1CHG de alegria \_**</dt></span><span class="sxs-lookup"><span data-stu-id="d8294-112"><dt>**JOY\_BUTTON1CHG**</dt></span></span> </dl> | <span data-ttu-id="d8294-113">O primeiro botão de joystick alterou o estado.</span><span class="sxs-lookup"><span data-stu-id="d8294-113">First joystick button has changed state.</span></span><br/>  |
| <span id="JOY_BUTTON2CHG"></span><span id="joy_button2chg"></span><dl> <span data-ttu-id="d8294-114"><dt>**BUTTON2CHG de alegria \_**</dt></span><span class="sxs-lookup"><span data-stu-id="d8294-114"><dt>**JOY\_BUTTON2CHG**</dt></span></span> </dl> | <span data-ttu-id="d8294-115">O segundo botão de joystick alterou o estado.</span><span class="sxs-lookup"><span data-stu-id="d8294-115">Second joystick button has changed state.</span></span><br/> |
| <span id="JOY_BUTTON3CHG"></span><span id="joy_button3chg"></span><dl> <span data-ttu-id="d8294-116"><dt>**BUTTON3CHG de alegria \_**</dt></span><span class="sxs-lookup"><span data-stu-id="d8294-116"><dt>**JOY\_BUTTON3CHG**</dt></span></span> </dl> | <span data-ttu-id="d8294-117">O terceiro botão de joystick alterou o estado.</span><span class="sxs-lookup"><span data-stu-id="d8294-117">Third joystick button has changed state.</span></span><br/>  |
| <span id="JOY_BUTTON4CHG"></span><span id="joy_button4chg"></span><dl> <span data-ttu-id="d8294-118"><dt>**BUTTON4CHG de alegria \_**</dt></span><span class="sxs-lookup"><span data-stu-id="d8294-118"><dt>**JOY\_BUTTON4CHG**</dt></span></span> </dl> | <span data-ttu-id="d8294-119">O quarto botão de joystick alterou o estado.</span><span class="sxs-lookup"><span data-stu-id="d8294-119">Fourth joystick button has changed state.</span></span><br/> |



 

<span data-ttu-id="d8294-120">e um ou mais dos seguintes:</span><span class="sxs-lookup"><span data-stu-id="d8294-120">and one or more of the following:</span></span>



| <span data-ttu-id="d8294-121">Valor</span><span class="sxs-lookup"><span data-stu-id="d8294-121">Value</span></span>                                                                                                                                                   | <span data-ttu-id="d8294-122">Significado</span><span class="sxs-lookup"><span data-stu-id="d8294-122">Meaning</span></span>                                       |
|---------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------|
| <span id="JOY_BUTTON1"></span><span id="joy_button1"></span><dl> <span data-ttu-id="d8294-123"><dt>**JOY \_ Button1**</dt></span><span class="sxs-lookup"><span data-stu-id="d8294-123"><dt>**JOY\_BUTTON1**</dt></span></span> </dl> | <span data-ttu-id="d8294-124">O primeiro botão de joystick é pressionado.</span><span class="sxs-lookup"><span data-stu-id="d8294-124">First joystick button is pressed.</span></span><br/>  |
| <span id="JOY_BUTTON2"></span><span id="joy_button2"></span><dl> <span data-ttu-id="d8294-125"><dt>**JOY \_ Button1**</dt></span><span class="sxs-lookup"><span data-stu-id="d8294-125"><dt>**JOY\_BUTTON2**</dt></span></span> </dl> | <span data-ttu-id="d8294-126">O segundo botão de joystick é pressionado.</span><span class="sxs-lookup"><span data-stu-id="d8294-126">Second joystick button is pressed.</span></span><br/> |
| <span id="JOY_BUTTON3"></span><span id="joy_button3"></span><dl> <span data-ttu-id="d8294-127"><dt>**BUTTON3 de alegria \_**</dt></span><span class="sxs-lookup"><span data-stu-id="d8294-127"><dt>**JOY\_BUTTON3**</dt></span></span> </dl> | <span data-ttu-id="d8294-128">O terceiro botão de joystick é pressionado.</span><span class="sxs-lookup"><span data-stu-id="d8294-128">Third joystick button is pressed.</span></span><br/>  |
| <span id="JOY_BUTTON4"></span><span id="joy_button4"></span><dl> <span data-ttu-id="d8294-129"><dt>**BUTTON4 de alegria \_**</dt></span><span class="sxs-lookup"><span data-stu-id="d8294-129"><dt>**JOY\_BUTTON4**</dt></span></span> </dl> | <span data-ttu-id="d8294-130">O quarto botão de joystick é pressionado.</span><span class="sxs-lookup"><span data-stu-id="d8294-130">Fourth joystick button is pressed.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="d8294-131">**xPos**</span><span class="sxs-lookup"><span data-stu-id="d8294-131">**xPos**</span></span> 
</dt> <dd>

<span data-ttu-id="d8294-132">As coordenadas x do joystick em relação ao canto superior esquerdo da área do cliente.</span><span class="sxs-lookup"><span data-stu-id="d8294-132">The x-coordinates of the joystick relative to the upper left corner of the client area.</span></span>

</dd> <dt>

<span data-ttu-id="d8294-133">**yPos**</span><span class="sxs-lookup"><span data-stu-id="d8294-133">**yPos**</span></span> 
</dt> <dd>

<span data-ttu-id="d8294-134">A coordenada y do joystick em relação ao canto superior esquerdo da área do cliente.</span><span class="sxs-lookup"><span data-stu-id="d8294-134">The y-coordinate of the joystick relative to the upper left corner of the client area.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="d8294-135">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d8294-135">Requirements</span></span>



| <span data-ttu-id="d8294-136">Requisito</span><span class="sxs-lookup"><span data-stu-id="d8294-136">Requirement</span></span> | <span data-ttu-id="d8294-137">Valor</span><span class="sxs-lookup"><span data-stu-id="d8294-137">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d8294-138">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d8294-138">Minimum supported client</span></span><br/> | <span data-ttu-id="d8294-139">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="d8294-139">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="d8294-140">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d8294-140">Minimum supported server</span></span><br/> | <span data-ttu-id="d8294-141">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="d8294-141">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="d8294-142">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="d8294-142">Header</span></span><br/>                   | <dl> <span data-ttu-id="d8294-143"><dt>Mmsystem. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="d8294-143"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d8294-144">Confira também</span><span class="sxs-lookup"><span data-stu-id="d8294-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d8294-145">Joysticks</span><span class="sxs-lookup"><span data-stu-id="d8294-145">Joysticks</span></span>](joysticks.md)
</dt> <dt>

[<span data-ttu-id="d8294-146">Mensagens do joystick de multimídia</span><span class="sxs-lookup"><span data-stu-id="d8294-146">Multimedia Joystick Messages</span></span>](multimedia-joystick-messages.md)
</dt> </dl>

 

 





