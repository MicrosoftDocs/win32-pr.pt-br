---
description: Ocorre quando o usuário libera uma chave enquanto o controle InkEdit tem foco.
ms.assetid: 973d99f2-df09-4315-aaab-72877272100b
title: Evento InkEdit. KeyUp (Inked. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 590f5f6b2e81e1996bca973f4994c0eade7ead18
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104506191"
---
# <a name="inkeditkeyup-event"></a><span data-ttu-id="b7fe6-103">Evento InkEdit. KeyUp</span><span class="sxs-lookup"><span data-stu-id="b7fe6-103">InkEdit.KeyUp event</span></span>

<span data-ttu-id="b7fe6-104">Ocorre quando o usuário libera uma chave enquanto o controle [InkEdit](inkedit-control-reference.md) tem foco.</span><span class="sxs-lookup"><span data-stu-id="b7fe6-104">Occurs when the user releases a key while the [InkEdit](inkedit-control-reference.md) control has focus.</span></span>

## <a name="syntax"></a><span data-ttu-id="b7fe6-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="b7fe6-105">Syntax</span></span>


```C++
HRESULT KeyUp(
   Long  *pKey,
   short ShiftKey
);
```



## <a name="parameters"></a><span data-ttu-id="b7fe6-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="b7fe6-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b7fe6-107">*pKey*</span><span class="sxs-lookup"><span data-stu-id="b7fe6-107">*pKey*</span></span> 
</dt> <dd>

<span data-ttu-id="b7fe6-108">O código de chave virtual da chave pressionada pelo usuário.</span><span class="sxs-lookup"><span data-stu-id="b7fe6-108">The virtual-key code of the key pressed by the user.</span></span>

</dd> <dt>

<span data-ttu-id="b7fe6-109">*ShiftKey*</span><span class="sxs-lookup"><span data-stu-id="b7fe6-109">*ShiftKey*</span></span> 
</dt> <dd>

<span data-ttu-id="b7fe6-110">Um membro da enumeração [**InkShiftKeyModifierFlags**](/windows/desktop/api/msinkaut/ne-msinkaut-inkshiftkeymodifierflags) que indica quais teclas modificadoras são pressionadas no momento do evento.</span><span class="sxs-lookup"><span data-stu-id="b7fe6-110">A member of the [**InkShiftKeyModifierFlags**](/windows/desktop/api/msinkaut/ne-msinkaut-inkshiftkeymodifierflags) enumeration that indicates which modifier keys are depressed at the time of the event.</span></span>



| <span data-ttu-id="b7fe6-111">Valor</span><span class="sxs-lookup"><span data-stu-id="b7fe6-111">Value</span></span>                                                                                                                                                                                     | <span data-ttu-id="b7fe6-112">Significado</span><span class="sxs-lookup"><span data-stu-id="b7fe6-112">Meaning</span></span>                                                          |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------|
| <span id="IKM_Shift"></span><span id="ikm_shift"></span><span id="IKM_SHIFT"></span><dl> <span data-ttu-id="b7fe6-113"><dt>**IKM \_ Shift**</dt></span><span class="sxs-lookup"><span data-stu-id="b7fe6-113"><dt>**IKM\_Shift**</dt></span></span> </dl>             | <span data-ttu-id="b7fe6-114">Especifica que a tecla SHIFT foi usada como um modificador.</span><span class="sxs-lookup"><span data-stu-id="b7fe6-114">Specifies that the SHIFT key was used as a modifier.</span></span> <br/> |
| <span id="IKM_Control_"></span><span id="ikm_control_"></span><span id="IKM_CONTROL_"></span><dl> <span data-ttu-id="b7fe6-115"><dt>**IKM \_ Controle** do</dt></span><span class="sxs-lookup"><span data-stu-id="b7fe6-115"><dt>**IKM\_Control** </dt></span></span> </dl> | <span data-ttu-id="b7fe6-116">Especifica que a tecla CTRL foi usada como um modificador.</span><span class="sxs-lookup"><span data-stu-id="b7fe6-116">Specifies that the CTRL key was used as a modifier.</span></span> <br/>  |
| <span id="IKM_Alt_"></span><span id="ikm_alt_"></span><span id="IKM_ALT_"></span><dl> <span data-ttu-id="b7fe6-117"><dt>**IKM \_ Alt**</dt></span><span class="sxs-lookup"><span data-stu-id="b7fe6-117"><dt>**IKM\_Alt** </dt></span></span> </dl>                 | <span data-ttu-id="b7fe6-118">Especifica que a tecla ALT foi usada como um modificador.</span><span class="sxs-lookup"><span data-stu-id="b7fe6-118">Specifies that the ALT key was used as a modifier.</span></span> <br/>   |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b7fe6-119">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="b7fe6-119">Return value</span></span>

<span data-ttu-id="b7fe6-120">Se esse evento for bem sucedido, ele retornará **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="b7fe6-120">If this event succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="b7fe6-121">Caso contrário, ele retorna um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="b7fe6-121">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="b7fe6-122">Comentários</span><span class="sxs-lookup"><span data-stu-id="b7fe6-122">Remarks</span></span>

<span data-ttu-id="b7fe6-123">Esse método de evento é definido na interface **\_ IInkEditEvents** .</span><span class="sxs-lookup"><span data-stu-id="b7fe6-123">This event method is defined in the **\_IInkEditEvents** interface.</span></span> <span data-ttu-id="b7fe6-124">A interface **\_ IInkEditEvents** implementa a interface [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) com um identificador de \_ IeeKeyUp DISPID.</span><span class="sxs-lookup"><span data-stu-id="b7fe6-124">The **\_IInkEditEvents** interface implements the [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interface with an identifier of DISPID\_IeeKeyUp.</span></span>

## <a name="requirements"></a><span data-ttu-id="b7fe6-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b7fe6-125">Requirements</span></span>



| <span data-ttu-id="b7fe6-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="b7fe6-126">Requirement</span></span> | <span data-ttu-id="b7fe6-127">Valor</span><span class="sxs-lookup"><span data-stu-id="b7fe6-127">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b7fe6-128">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b7fe6-128">Minimum supported client</span></span><br/> | <span data-ttu-id="b7fe6-129">Somente aplicativos de área de trabalho do Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="b7fe6-129">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="b7fe6-130">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b7fe6-130">Minimum supported server</span></span><br/> | <span data-ttu-id="b7fe6-131">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="b7fe6-131">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="b7fe6-132">parâmetro</span><span class="sxs-lookup"><span data-stu-id="b7fe6-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="b7fe6-133"><dt>Inked. h (também requer Inked \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="b7fe6-133"><dt>Inked.h (also requires inked\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="b7fe6-134">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="b7fe6-134">Library</span></span><br/>                  | <dl> <span data-ttu-id="b7fe6-135"><dt>InkEd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b7fe6-135"><dt>InkEd.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="b7fe6-136">Confira também</span><span class="sxs-lookup"><span data-stu-id="b7fe6-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b7fe6-137">InkEdit</span><span class="sxs-lookup"><span data-stu-id="b7fe6-137">InkEdit</span></span>](inkedit-control-reference.md)
</dt> <dt>

[<span data-ttu-id="b7fe6-138">**Enumeração InkShiftKeyModifierFlags**</span><span class="sxs-lookup"><span data-stu-id="b7fe6-138">**InkShiftKeyModifierFlags Enumeration**</span></span>](/windows/desktop/api/msinkaut/ne-msinkaut-inkshiftkeymodifierflags)
</dt> <dt>

<span data-ttu-id="b7fe6-139">[**Controle de evento InkEdit de KeyDown \[\]**](inkedit-keydown.md)</span><span class="sxs-lookup"><span data-stu-id="b7fe6-139">[**KeyDown Event \[InkEdit Control\]**](inkedit-keydown.md)</span></span>
</dt> <dt>

<span data-ttu-id="b7fe6-140">[**Controle de evento InkEdit de KeyPress \[\]**](inkedit-keypress.md)</span><span class="sxs-lookup"><span data-stu-id="b7fe6-140">[**KeyPress Event \[InkEdit Control\]**](inkedit-keypress.md)</span></span>
</dt> </dl>

 

