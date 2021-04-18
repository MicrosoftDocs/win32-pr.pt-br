---
title: Mensagem de MM_JOY2ZMOVE (mmsystem. h)
description: A \_ mensagem mm JOY2ZMOVE notifica a janela que capturou o joystick JOYSTICKID2 que a posição do joystick no eixo z foi alterada.
ms.assetid: f09a1a11-8c97-4a03-a388-8bf9ab89a3db
keywords:
- Multimídia do Windows de mensagem MM_JOY2ZMOVE
topic_type:
- apiref
api_name:
- MM_JOY2ZMOVE
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0d899a4a1c93304075cb166ba805367ceed6ddd3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105788133"
---
# <a name="mm_joy2zmove-message"></a><span data-ttu-id="81cfc-104">\_Mensagem mm JOY2ZMOVE</span><span class="sxs-lookup"><span data-stu-id="81cfc-104">MM\_JOY2ZMOVE message</span></span>

<span data-ttu-id="81cfc-105">A mensagem **mm \_ JOY2ZMOVE** notifica a janela que CAPTUROU o joystick JOYSTICKID2 que a posição do joystick no eixo z foi alterada.</span><span class="sxs-lookup"><span data-stu-id="81cfc-105">The **MM\_JOY2ZMOVE** message notifies the window that has captured joystick JOYSTICKID2 that the joystick position on the z-axis has changed.</span></span>


```C++
MM_JOY2ZMOVE 
fwButtons = wParam; 
zPos = LOWORD(lParam); 
```



## <a name="parameters"></a><span data-ttu-id="81cfc-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="81cfc-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="81cfc-107"><span id="fwButtons"></span><span id="fwbuttons"></span><span id="FWBUTTONS"></span>*fwButtons*</span><span class="sxs-lookup"><span data-stu-id="81cfc-107"><span id="fwButtons"></span><span id="fwbuttons"></span><span id="FWBUTTONS"></span>*fwButtons*</span></span>
</dt> <dd>

<span data-ttu-id="81cfc-108">Identifica os botões que são pressionados.</span><span class="sxs-lookup"><span data-stu-id="81cfc-108">Identifies the buttons that are pressed.</span></span> <span data-ttu-id="81cfc-109">Pode ser um ou mais dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="81cfc-109">It can be one or more of the following values.</span></span>



| <span data-ttu-id="81cfc-110">Requisito</span><span class="sxs-lookup"><span data-stu-id="81cfc-110">Requirement</span></span> | <span data-ttu-id="81cfc-111">Valor</span><span class="sxs-lookup"><span data-stu-id="81cfc-111">Value</span></span> |
|--------------|------------------------------------|
| <span data-ttu-id="81cfc-112">JOY \_ Button1</span><span class="sxs-lookup"><span data-stu-id="81cfc-112">JOY\_BUTTON1</span></span> | <span data-ttu-id="81cfc-113">O primeiro botão de joystick é pressionado.</span><span class="sxs-lookup"><span data-stu-id="81cfc-113">First joystick button is pressed.</span></span>  |
| <span data-ttu-id="81cfc-114">JOY \_ Button1</span><span class="sxs-lookup"><span data-stu-id="81cfc-114">JOY\_BUTTON2</span></span> | <span data-ttu-id="81cfc-115">O segundo botão de joystick é pressionado.</span><span class="sxs-lookup"><span data-stu-id="81cfc-115">Second joystick button is pressed.</span></span> |
| <span data-ttu-id="81cfc-116">BUTTON3 de alegria \_</span><span class="sxs-lookup"><span data-stu-id="81cfc-116">JOY\_BUTTON3</span></span> | <span data-ttu-id="81cfc-117">O terceiro botão de joystick é pressionado.</span><span class="sxs-lookup"><span data-stu-id="81cfc-117">Third joystick button is pressed.</span></span>  |
| <span data-ttu-id="81cfc-118">BUTTON4 de alegria \_</span><span class="sxs-lookup"><span data-stu-id="81cfc-118">JOY\_BUTTON4</span></span> | <span data-ttu-id="81cfc-119">O quarto botão de joystick é pressionado.</span><span class="sxs-lookup"><span data-stu-id="81cfc-119">Fourth joystick button is pressed.</span></span> |



 

</dd> <dt>

<span data-ttu-id="81cfc-120"><span id="zPos"></span><span id="zpos"></span><span id="ZPOS"></span>*zPos*</span><span class="sxs-lookup"><span data-stu-id="81cfc-120"><span id="zPos"></span><span id="zpos"></span><span id="ZPOS"></span>*zPos*</span></span>
</dt> <dd>

<span data-ttu-id="81cfc-121">A coordenada z do joystick.</span><span class="sxs-lookup"><span data-stu-id="81cfc-121">The z-coordinate of the joystick.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="81cfc-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="81cfc-122">Requirements</span></span>



| <span data-ttu-id="81cfc-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="81cfc-123">Requirement</span></span> | <span data-ttu-id="81cfc-124">Valor</span><span class="sxs-lookup"><span data-stu-id="81cfc-124">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="81cfc-125">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="81cfc-125">Minimum supported client</span></span><br/> | <span data-ttu-id="81cfc-126">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="81cfc-126">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="81cfc-127">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="81cfc-127">Minimum supported server</span></span><br/> | <span data-ttu-id="81cfc-128">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="81cfc-128">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="81cfc-129">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="81cfc-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="81cfc-130"><dt>Mmsystem. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="81cfc-130"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="81cfc-131">Confira também</span><span class="sxs-lookup"><span data-stu-id="81cfc-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="81cfc-132">Joysticks</span><span class="sxs-lookup"><span data-stu-id="81cfc-132">Joysticks</span></span>](joysticks.md)
</dt> <dt>

[<span data-ttu-id="81cfc-133">Mensagens do joystick de multimídia</span><span class="sxs-lookup"><span data-stu-id="81cfc-133">Multimedia Joystick Messages</span></span>](multimedia-joystick-messages.md)
</dt> </dl>

 

 





