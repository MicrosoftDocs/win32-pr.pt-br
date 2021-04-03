---
description: Ocorre quando o usuário pressiona uma tecla enquanto o controle InkEdit tem foco.
ms.assetid: 14b05b72-ae5d-416a-8ea5-9d9716c0967f
title: Evento InkEdit. KeyDown (Inked. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 07cee260d4c902534b9b234e0e30d0b60645c579
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103922653"
---
# <a name="inkeditkeydown-event"></a><span data-ttu-id="555b0-103">Evento InkEdit. KeyDown</span><span class="sxs-lookup"><span data-stu-id="555b0-103">InkEdit.KeyDown event</span></span>

<span data-ttu-id="555b0-104">Ocorre quando o usuário pressiona uma tecla enquanto o controle [InkEdit](inkedit-control-reference.md) tem foco.</span><span class="sxs-lookup"><span data-stu-id="555b0-104">Occurs when the user presses a key while the [InkEdit](inkedit-control-reference.md) control has focus.</span></span>

## <a name="syntax"></a><span data-ttu-id="555b0-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="555b0-105">Syntax</span></span>


```C++
HRESULT KeyDown(
   Long  *pKey,
   short ShiftKey
);
```



## <a name="parameters"></a><span data-ttu-id="555b0-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="555b0-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="555b0-107">*pKey*</span><span class="sxs-lookup"><span data-stu-id="555b0-107">*pKey*</span></span> 
</dt> <dd>

<span data-ttu-id="555b0-108">O código de chave virtual da chave pressionada pelo usuário.</span><span class="sxs-lookup"><span data-stu-id="555b0-108">The virtual-key code of the key pressed by the user.</span></span>

</dd> <dt>

<span data-ttu-id="555b0-109">*ShiftKey*</span><span class="sxs-lookup"><span data-stu-id="555b0-109">*ShiftKey*</span></span> 
</dt> <dd>

<span data-ttu-id="555b0-110">Um membro da enumeração [**InkShiftKeyModifierFlags**](/windows/desktop/api/msinkaut/ne-msinkaut-inkshiftkeymodifierflags) , que indica quais teclas modificadoras são pressionadas no momento do evento.</span><span class="sxs-lookup"><span data-stu-id="555b0-110">A member of the [**InkShiftKeyModifierFlags**](/windows/desktop/api/msinkaut/ne-msinkaut-inkshiftkeymodifierflags) enumeration, that indicates which modifier keys are depressed at the time of the event.</span></span>



| <span data-ttu-id="555b0-111">Valor</span><span class="sxs-lookup"><span data-stu-id="555b0-111">Value</span></span>                                                                                                                                                                                     | <span data-ttu-id="555b0-112">Significado</span><span class="sxs-lookup"><span data-stu-id="555b0-112">Meaning</span></span>                                                          |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------|
| <span id="IKM_Shift"></span><span id="ikm_shift"></span><span id="IKM_SHIFT"></span><dl> <span data-ttu-id="555b0-113"><dt>**IKM \_ Shift**</dt></span><span class="sxs-lookup"><span data-stu-id="555b0-113"><dt>**IKM\_Shift**</dt></span></span> </dl>             | <span data-ttu-id="555b0-114">Especifica que a tecla SHIFT foi usada como um modificador.</span><span class="sxs-lookup"><span data-stu-id="555b0-114">Specifies that the SHIFT key was used as a modifier.</span></span> <br/> |
| <span id="IKM_Control_"></span><span id="ikm_control_"></span><span id="IKM_CONTROL_"></span><dl> <span data-ttu-id="555b0-115"><dt>**IKM \_ Controle** do</dt></span><span class="sxs-lookup"><span data-stu-id="555b0-115"><dt>**IKM\_Control** </dt></span></span> </dl> | <span data-ttu-id="555b0-116">Especifica que a tecla CTRL foi usada como um modificador.</span><span class="sxs-lookup"><span data-stu-id="555b0-116">Specifies that the CTRL key was used as a modifier.</span></span> <br/>  |
| <span id="IKM_Alt_"></span><span id="ikm_alt_"></span><span id="IKM_ALT_"></span><dl> <span data-ttu-id="555b0-117"><dt>**IKM \_ Alt**</dt></span><span class="sxs-lookup"><span data-stu-id="555b0-117"><dt>**IKM\_Alt** </dt></span></span> </dl>                 | <span data-ttu-id="555b0-118">Especifica que a tecla ALT foi usada como um modificador.</span><span class="sxs-lookup"><span data-stu-id="555b0-118">Specifies that the ALT key was used as a modifier.</span></span> <br/>   |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="555b0-119">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="555b0-119">Return value</span></span>

<span data-ttu-id="555b0-120">Se esse evento for bem sucedido, ele retornará **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="555b0-120">If this event succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="555b0-121">Caso contrário, ele retorna um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="555b0-121">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="555b0-122">Comentários</span><span class="sxs-lookup"><span data-stu-id="555b0-122">Remarks</span></span>

<span data-ttu-id="555b0-123">Esse método de evento é definido na interface **\_ IInkEditEvents** .</span><span class="sxs-lookup"><span data-stu-id="555b0-123">This event method is defined in the **\_IInkEditEvents** interface.</span></span> <span data-ttu-id="555b0-124">A interface **\_ IInkEditEvents** implementa a interface [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) com um identificador de \_ IeeKeyDown DISPID.</span><span class="sxs-lookup"><span data-stu-id="555b0-124">The **\_IInkEditEvents** interface implements the [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interface with an identifier of DISPID\_IeeKeyDown.</span></span>

## <a name="requirements"></a><span data-ttu-id="555b0-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="555b0-125">Requirements</span></span>



| <span data-ttu-id="555b0-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="555b0-126">Requirement</span></span> | <span data-ttu-id="555b0-127">Valor</span><span class="sxs-lookup"><span data-stu-id="555b0-127">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="555b0-128">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="555b0-128">Minimum supported client</span></span><br/> | <span data-ttu-id="555b0-129">Somente aplicativos de área de trabalho do Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="555b0-129">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="555b0-130">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="555b0-130">Minimum supported server</span></span><br/> | <span data-ttu-id="555b0-131">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="555b0-131">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="555b0-132">parâmetro</span><span class="sxs-lookup"><span data-stu-id="555b0-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="555b0-133"><dt>Inked. h (também requer Inked \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="555b0-133"><dt>Inked.h (also requires inked\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="555b0-134">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="555b0-134">Library</span></span><br/>                  | <dl> <span data-ttu-id="555b0-135"><dt>InkEd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="555b0-135"><dt>InkEd.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="555b0-136">Confira também</span><span class="sxs-lookup"><span data-stu-id="555b0-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="555b0-137">InkEdit</span><span class="sxs-lookup"><span data-stu-id="555b0-137">InkEdit</span></span>](inkedit-control-reference.md)
</dt> <dt>

[<span data-ttu-id="555b0-138">**Enumeração InkShiftKeyModifierFlags**</span><span class="sxs-lookup"><span data-stu-id="555b0-138">**InkShiftKeyModifierFlags Enumeration**</span></span>](/windows/desktop/api/msinkaut/ne-msinkaut-inkshiftkeymodifierflags)
</dt> <dt>

<span data-ttu-id="555b0-139">[**Controle de evento InkEdit de KeyPress \[\]**](inkedit-keypress.md)</span><span class="sxs-lookup"><span data-stu-id="555b0-139">[**KeyPress Event \[InkEdit Control\]**](inkedit-keypress.md)</span></span>
</dt> <dt>

<span data-ttu-id="555b0-140">[**Controle de evento InkEdit de KeyUp \[\]**](inkedit-keyup.md)</span><span class="sxs-lookup"><span data-stu-id="555b0-140">[**KeyUp Event \[InkEdit Control\]**](inkedit-keyup.md)</span></span>
</dt> </dl>

 

