---
title: Mensagem de MM_JOY1ZMOVE (mmsystem. h)
description: A \_ mensagem mm JOY1ZMOVE notifica a janela que capturou o joystick JOYSTICKID1 que a posição do joystick no eixo z foi alterada.
ms.assetid: 25d98963-03e6-4276-a132-256e8bbfa73b
keywords:
- Multimídia do Windows de mensagem MM_JOY1ZMOVE
topic_type:
- apiref
api_name:
- MM_JOY1ZMOVE
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d7d4db3db8c1817f0502ce14cc5328ad666b32c9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104456035"
---
# <a name="mm_joy1zmove-message"></a><span data-ttu-id="3f120-104">\_Mensagem mm JOY1ZMOVE</span><span class="sxs-lookup"><span data-stu-id="3f120-104">MM\_JOY1ZMOVE message</span></span>

<span data-ttu-id="3f120-105">A mensagem **mm \_ JOY1ZMOVE** notifica a janela que CAPTUROU o joystick JOYSTICKID1 que a posição do joystick no eixo z foi alterada.</span><span class="sxs-lookup"><span data-stu-id="3f120-105">The **MM\_JOY1ZMOVE** message notifies the window that has captured joystick JOYSTICKID1 that the joystick position on the z-axis has changed.</span></span>


```C++
MM_JOY1ZMOVE 
fwButtons = wParam; 
zPos = LOWORD(lParam); 
```



## <a name="parameters"></a><span data-ttu-id="3f120-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="3f120-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3f120-107"><span id="fwButtons"></span><span id="fwbuttons"></span><span id="FWBUTTONS"></span>*fwButtons*</span><span class="sxs-lookup"><span data-stu-id="3f120-107"><span id="fwButtons"></span><span id="fwbuttons"></span><span id="FWBUTTONS"></span>*fwButtons*</span></span>
</dt> <dd>

<span data-ttu-id="3f120-108">Identifica os botões que são pressionados.</span><span class="sxs-lookup"><span data-stu-id="3f120-108">Identifies the buttons that are pressed.</span></span> <span data-ttu-id="3f120-109">Pode ser um ou mais dos seguintes valores:</span><span class="sxs-lookup"><span data-stu-id="3f120-109">It can be one or more of the following values:</span></span>



| <span data-ttu-id="3f120-110">Requisito</span><span class="sxs-lookup"><span data-stu-id="3f120-110">Requirement</span></span> | <span data-ttu-id="3f120-111">Valor</span><span class="sxs-lookup"><span data-stu-id="3f120-111">Value</span></span> |
|--------------|------------------------------------|
| <span data-ttu-id="3f120-112">JOY \_ Button1</span><span class="sxs-lookup"><span data-stu-id="3f120-112">JOY\_BUTTON1</span></span> | <span data-ttu-id="3f120-113">O primeiro botão de joystick é pressionado.</span><span class="sxs-lookup"><span data-stu-id="3f120-113">First joystick button is pressed.</span></span>  |
| <span data-ttu-id="3f120-114">JOY \_ Button1</span><span class="sxs-lookup"><span data-stu-id="3f120-114">JOY\_BUTTON2</span></span> | <span data-ttu-id="3f120-115">O segundo botão de joystick é pressionado.</span><span class="sxs-lookup"><span data-stu-id="3f120-115">Second joystick button is pressed.</span></span> |
| <span data-ttu-id="3f120-116">BUTTON3 de alegria \_</span><span class="sxs-lookup"><span data-stu-id="3f120-116">JOY\_BUTTON3</span></span> | <span data-ttu-id="3f120-117">O terceiro botão de joystick é pressionado.</span><span class="sxs-lookup"><span data-stu-id="3f120-117">Third joystick button is pressed.</span></span>  |
| <span data-ttu-id="3f120-118">BUTTON4 de alegria \_</span><span class="sxs-lookup"><span data-stu-id="3f120-118">JOY\_BUTTON4</span></span> | <span data-ttu-id="3f120-119">O quarto botão de joystick é pressionado.</span><span class="sxs-lookup"><span data-stu-id="3f120-119">Fourth joystick button is pressed.</span></span> |



 

</dd> <dt>

<span data-ttu-id="3f120-120"><span id="zPos"></span><span id="zpos"></span><span id="ZPOS"></span>*zPos*</span><span class="sxs-lookup"><span data-stu-id="3f120-120"><span id="zPos"></span><span id="zpos"></span><span id="ZPOS"></span>*zPos*</span></span>
</dt> <dd>

<span data-ttu-id="3f120-121">A coordenada z do joystick.</span><span class="sxs-lookup"><span data-stu-id="3f120-121">The z-coordinate of the joystick.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="3f120-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3f120-122">Requirements</span></span>



| <span data-ttu-id="3f120-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="3f120-123">Requirement</span></span> | <span data-ttu-id="3f120-124">Valor</span><span class="sxs-lookup"><span data-stu-id="3f120-124">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3f120-125">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3f120-125">Minimum supported client</span></span><br/> | <span data-ttu-id="3f120-126">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="3f120-126">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="3f120-127">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3f120-127">Minimum supported server</span></span><br/> | <span data-ttu-id="3f120-128">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="3f120-128">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="3f120-129">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="3f120-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="3f120-130"><dt>Mmsystem. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="3f120-130"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3f120-131">Confira também</span><span class="sxs-lookup"><span data-stu-id="3f120-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3f120-132">Joysticks</span><span class="sxs-lookup"><span data-stu-id="3f120-132">Joysticks</span></span>](joysticks.md)
</dt> <dt>

[<span data-ttu-id="3f120-133">Mensagens do joystick de multimídia</span><span class="sxs-lookup"><span data-stu-id="3f120-133">Multimedia Joystick Messages</span></span>](multimedia-joystick-messages.md)
</dt> </dl>

 

 





