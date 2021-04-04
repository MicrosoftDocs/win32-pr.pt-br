---
title: Mensagem de MM_JOY2MOVE (mmsystem. h)
description: A \_ mensagem mm JOY2MOVE notifica a janela que capturou o joystick JOYSTICKID2 de que a posição do joystick foi alterada.
ms.assetid: 8dc1c092-3947-43d5-8504-a4e4e121fbcb
keywords:
- Multimídia do Windows de mensagem MM_JOY2MOVE
topic_type:
- apiref
api_name:
- MM_JOY2MOVE
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ec8921f0ae76d05c429d6750944a26662c1276af
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104085241"
---
# <a name="mm_joy2move-message"></a><span data-ttu-id="5a028-104">\_Mensagem mm JOY2MOVE</span><span class="sxs-lookup"><span data-stu-id="5a028-104">MM\_JOY2MOVE message</span></span>

<span data-ttu-id="5a028-105">A mensagem **mm \_ JOY2MOVE** notifica a janela que CAPTUROU o joystick JOYSTICKID2 de que a posição do joystick foi alterada.</span><span class="sxs-lookup"><span data-stu-id="5a028-105">The **MM\_JOY2MOVE** message notifies the window that has captured joystick JOYSTICKID2 that the joystick position has changed.</span></span>


```C++
MM_JOY2MOVE 
fwButtons = wParam; 
xPos = LOWORD(lParam); 
yPos = HIWORD(lParam); 
```



## <a name="parameters"></a><span data-ttu-id="5a028-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="5a028-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5a028-107"><span id="fwButtons"></span><span id="fwbuttons"></span><span id="FWBUTTONS"></span>*fwButtons*</span><span class="sxs-lookup"><span data-stu-id="5a028-107"><span id="fwButtons"></span><span id="fwbuttons"></span><span id="FWBUTTONS"></span>*fwButtons*</span></span>
</dt> <dd>

<span data-ttu-id="5a028-108">Identifica os botões que são pressionados.</span><span class="sxs-lookup"><span data-stu-id="5a028-108">Identifies the buttons that are pressed.</span></span> <span data-ttu-id="5a028-109">Pode ser um ou mais dos seguintes valores:</span><span class="sxs-lookup"><span data-stu-id="5a028-109">It can be one or more of the following values:</span></span>



| <span data-ttu-id="5a028-110">Requisito</span><span class="sxs-lookup"><span data-stu-id="5a028-110">Requirement</span></span> | <span data-ttu-id="5a028-111">Valor</span><span class="sxs-lookup"><span data-stu-id="5a028-111">Value</span></span> |
|--------------|------------------------------------|
| <span data-ttu-id="5a028-112">JOY \_ Button1</span><span class="sxs-lookup"><span data-stu-id="5a028-112">JOY\_BUTTON1</span></span> | <span data-ttu-id="5a028-113">O primeiro botão de joystick é pressionado.</span><span class="sxs-lookup"><span data-stu-id="5a028-113">First joystick button is pressed.</span></span>  |
| <span data-ttu-id="5a028-114">JOY \_ Button1</span><span class="sxs-lookup"><span data-stu-id="5a028-114">JOY\_BUTTON2</span></span> | <span data-ttu-id="5a028-115">O segundo botão de joystick é pressionado.</span><span class="sxs-lookup"><span data-stu-id="5a028-115">Second joystick button is pressed.</span></span> |
| <span data-ttu-id="5a028-116">BUTTON3 de alegria \_</span><span class="sxs-lookup"><span data-stu-id="5a028-116">JOY\_BUTTON3</span></span> | <span data-ttu-id="5a028-117">O terceiro botão de joystick é pressionado.</span><span class="sxs-lookup"><span data-stu-id="5a028-117">Third joystick button is pressed.</span></span>  |
| <span data-ttu-id="5a028-118">BUTTON4 de alegria \_</span><span class="sxs-lookup"><span data-stu-id="5a028-118">JOY\_BUTTON4</span></span> | <span data-ttu-id="5a028-119">O quarto botão de joystick é pressionado.</span><span class="sxs-lookup"><span data-stu-id="5a028-119">Fourth joystick button is pressed.</span></span> |



 

</dd> <dt>

<span data-ttu-id="5a028-120"><span id="xPos"></span><span id="xpos"></span><span id="XPOS"></span>*xPos*</span><span class="sxs-lookup"><span data-stu-id="5a028-120"><span id="xPos"></span><span id="xpos"></span><span id="XPOS"></span>*xPos*</span></span>
</dt> <dd>

<span data-ttu-id="5a028-121">As coordenadas x do joystick em relação ao canto superior esquerdo da área do cliente.</span><span class="sxs-lookup"><span data-stu-id="5a028-121">The x-coordinates of the joystick relative to the upper left corner of the client area.</span></span>

</dd> <dt>

<span data-ttu-id="5a028-122"><span id="yPos"></span><span id="ypos"></span><span id="YPOS"></span>*yPos*</span><span class="sxs-lookup"><span data-stu-id="5a028-122"><span id="yPos"></span><span id="ypos"></span><span id="YPOS"></span>*yPos*</span></span>
</dt> <dd>

<span data-ttu-id="5a028-123">A coordenada y do joystick em relação ao canto superior esquerdo da área do cliente.</span><span class="sxs-lookup"><span data-stu-id="5a028-123">The y-coordinate of the joystick relative to the upper left corner of the client area.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="5a028-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5a028-124">Requirements</span></span>



| <span data-ttu-id="5a028-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="5a028-125">Requirement</span></span> | <span data-ttu-id="5a028-126">Valor</span><span class="sxs-lookup"><span data-stu-id="5a028-126">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5a028-127">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="5a028-127">Minimum supported client</span></span><br/> | <span data-ttu-id="5a028-128">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="5a028-128">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="5a028-129">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="5a028-129">Minimum supported server</span></span><br/> | <span data-ttu-id="5a028-130">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="5a028-130">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="5a028-131">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="5a028-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="5a028-132"><dt>Mmsystem. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="5a028-132"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5a028-133">Confira também</span><span class="sxs-lookup"><span data-stu-id="5a028-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5a028-134">Joysticks</span><span class="sxs-lookup"><span data-stu-id="5a028-134">Joysticks</span></span>](joysticks.md)
</dt> <dt>

[<span data-ttu-id="5a028-135">Mensagens do joystick de multimídia</span><span class="sxs-lookup"><span data-stu-id="5a028-135">Multimedia Joystick Messages</span></span>](multimedia-joystick-messages.md)
</dt> </dl>

 

 





