---
description: Ocorre quando o usuário pressiona um botão do mouse enquanto o mouse está sobre o controle InkEdit.
ms.assetid: 8985fee5-7b63-46ab-b229-046e2f0ee004
title: Evento InkEdit. MouseDown (Inked. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 78e684fe2d75e5eaaf2b0064e8c7c78cbfe281a5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103837028"
---
# <a name="inkeditmousedown-event"></a><span data-ttu-id="ab3d8-103">Evento InkEdit. MouseDown</span><span class="sxs-lookup"><span data-stu-id="ab3d8-103">InkEdit.MouseDown event</span></span>

<span data-ttu-id="ab3d8-104">Ocorre quando o usuário pressiona um botão do mouse enquanto o mouse está sobre o controle [InkEdit](inkedit-control-reference.md) .</span><span class="sxs-lookup"><span data-stu-id="ab3d8-104">Occurs when the user presses a mouse button while the mouse is over the [InkEdit](inkedit-control-reference.md) control.</span></span>

## <a name="syntax"></a><span data-ttu-id="ab3d8-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="ab3d8-105">Syntax</span></span>


```C++
HRESULT MouseDown(
   short Button,
   short ShiftKey,
   long  xMouse,
   long  yMouse
);
```



## <a name="parameters"></a><span data-ttu-id="ab3d8-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="ab3d8-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ab3d8-107">*Botão*</span><span class="sxs-lookup"><span data-stu-id="ab3d8-107">*Button*</span></span> 
</dt> <dd>

<span data-ttu-id="ab3d8-108">Um membro da enumeração [**MouseButton**](/windows/desktop/api/inked/ne-inked-mousebutton) que indica quais botões do mouse foram pressionados.</span><span class="sxs-lookup"><span data-stu-id="ab3d8-108">A member of the [**MouseButton**](/windows/desktop/api/inked/ne-inked-mousebutton) enumeration that indicates which mouse buttons were pressed.</span></span>



| <span data-ttu-id="ab3d8-109">Valor</span><span class="sxs-lookup"><span data-stu-id="ab3d8-109">Value</span></span>                                                                                                                                                            | <span data-ttu-id="ab3d8-110">Significado</span><span class="sxs-lookup"><span data-stu-id="ab3d8-110">Meaning</span></span>                                           |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------|
| <span id="NO_BUTTON_"></span><span id="no_button_"></span><dl> <span data-ttu-id="ab3d8-111"><dt>**Não \_ BOTÃO**</dt></span><span class="sxs-lookup"><span data-stu-id="ab3d8-111"><dt>**NO\_BUTTON** </dt></span></span> </dl>             | <span data-ttu-id="ab3d8-112">Padrão.</span><span class="sxs-lookup"><span data-stu-id="ab3d8-112">Default.</span></span> <span data-ttu-id="ab3d8-113">Nenhum botão do mouse foi pressionado.</span><span class="sxs-lookup"><span data-stu-id="ab3d8-113">No mouse button was pressed.</span></span> <br/> |
| <span id="LEFT_BUTTON_"></span><span id="left_button_"></span><dl> <span data-ttu-id="ab3d8-114"><dt>**À esquerda \_ BOTÃO**</dt></span><span class="sxs-lookup"><span data-stu-id="ab3d8-114"><dt>**LEFT\_BUTTON** </dt></span></span> </dl>       | <span data-ttu-id="ab3d8-115">O botão esquerdo do mouse foi pressionado.</span><span class="sxs-lookup"><span data-stu-id="ab3d8-115">The left mouse button was pressed.</span></span> <br/>    |
| <span id="RIGHT_BUTTON_"></span><span id="right_button_"></span><dl> <span data-ttu-id="ab3d8-116"><dt>**À direita \_ BOTÃO**</dt></span><span class="sxs-lookup"><span data-stu-id="ab3d8-116"><dt>**RIGHT\_BUTTON** </dt></span></span> </dl>    | <span data-ttu-id="ab3d8-117">O botão direito do mouse foi pressionado.</span><span class="sxs-lookup"><span data-stu-id="ab3d8-117">The right mouse button was pressed.</span></span> <br/>   |
| <span id="MIDDLE_BUTTON_"></span><span id="middle_button_"></span><dl> <span data-ttu-id="ab3d8-118"><dt>**Meio \_ BOTÃO**</dt></span><span class="sxs-lookup"><span data-stu-id="ab3d8-118"><dt>**MIDDLE\_BUTTON** </dt></span></span> </dl> | <span data-ttu-id="ab3d8-119">O botão do meio do mouse foi pressionado.</span><span class="sxs-lookup"><span data-stu-id="ab3d8-119">The middle mouse button was pressed.</span></span> <br/>  |



 

</dd> <dt>

<span data-ttu-id="ab3d8-120">*ShiftKey*</span><span class="sxs-lookup"><span data-stu-id="ab3d8-120">*ShiftKey*</span></span> 
</dt> <dd>

<span data-ttu-id="ab3d8-121">Um membro da enumeração [**InkShiftKeyModifierFlags**](/windows/desktop/api/msinkaut/ne-msinkaut-inkshiftkeymodifierflags) que indica quais teclas modificadoras são pressionadas no momento do evento.</span><span class="sxs-lookup"><span data-stu-id="ab3d8-121">A member of the [**InkShiftKeyModifierFlags**](/windows/desktop/api/msinkaut/ne-msinkaut-inkshiftkeymodifierflags) enumeration that indicates which modifier keys are depressed at the time of the event.</span></span>



| <span data-ttu-id="ab3d8-122">Valor</span><span class="sxs-lookup"><span data-stu-id="ab3d8-122">Value</span></span>                                                                                                                                                                                     | <span data-ttu-id="ab3d8-123">Significado</span><span class="sxs-lookup"><span data-stu-id="ab3d8-123">Meaning</span></span>                                                          |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------|
| <span id="IKM_Shift"></span><span id="ikm_shift"></span><span id="IKM_SHIFT"></span><dl> <span data-ttu-id="ab3d8-124"><dt>**IKM \_ Shift**</dt></span><span class="sxs-lookup"><span data-stu-id="ab3d8-124"><dt>**IKM\_Shift**</dt></span></span> </dl>             | <span data-ttu-id="ab3d8-125">Especifica que a tecla SHIFT foi usada como um modificador.</span><span class="sxs-lookup"><span data-stu-id="ab3d8-125">Specifies that the SHIFT key was used as a modifier.</span></span> <br/> |
| <span id="IKM_Control_"></span><span id="ikm_control_"></span><span id="IKM_CONTROL_"></span><dl> <span data-ttu-id="ab3d8-126"><dt>**IKM \_ Controle** do</dt></span><span class="sxs-lookup"><span data-stu-id="ab3d8-126"><dt>**IKM\_Control** </dt></span></span> </dl> | <span data-ttu-id="ab3d8-127">Especifica que a tecla CTRL foi usada como um modificador.</span><span class="sxs-lookup"><span data-stu-id="ab3d8-127">Specifies that the CTRL key was used as a modifier.</span></span> <br/>  |
| <span id="IKM_Alt_"></span><span id="ikm_alt_"></span><span id="IKM_ALT_"></span><dl> <span data-ttu-id="ab3d8-128"><dt>**IKM \_ Alt**</dt></span><span class="sxs-lookup"><span data-stu-id="ab3d8-128"><dt>**IKM\_Alt** </dt></span></span> </dl>                 | <span data-ttu-id="ab3d8-129">Especifica que a tecla ALT foi usada como um modificador.</span><span class="sxs-lookup"><span data-stu-id="ab3d8-129">Specifies that the ALT key was used as a modifier.</span></span> <br/>   |



 

</dd> <dt>

<span data-ttu-id="ab3d8-130">*xMouse*</span><span class="sxs-lookup"><span data-stu-id="ab3d8-130">*xMouse*</span></span> 
</dt> <dd>

<span data-ttu-id="ab3d8-131">A coordenada x atual, em pixels, do ponteiro do mouse.</span><span class="sxs-lookup"><span data-stu-id="ab3d8-131">The current x coordinate, in pixels, of the mouse pointer.</span></span>

</dd> <dt>

<span data-ttu-id="ab3d8-132">*yMouse*</span><span class="sxs-lookup"><span data-stu-id="ab3d8-132">*yMouse*</span></span> 
</dt> <dd>

<span data-ttu-id="ab3d8-133">A coordenada y atual, em pixels, do ponteiro do mouse.</span><span class="sxs-lookup"><span data-stu-id="ab3d8-133">The current y coordinate, in pixels, of the mouse pointer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ab3d8-134">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="ab3d8-134">Return value</span></span>

<span data-ttu-id="ab3d8-135">Se esse evento for bem sucedido, ele retornará **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="ab3d8-135">If this event succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="ab3d8-136">Caso contrário, ele retorna um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="ab3d8-136">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="ab3d8-137">Comentários</span><span class="sxs-lookup"><span data-stu-id="ab3d8-137">Remarks</span></span>

<span data-ttu-id="ab3d8-138">Se um botão do mouse for pressionado enquanto o ponteiro estiver sobre um controle [InkEdit](inkedit-control-reference.md) , esse controle capturará o mouse e receberá todos os eventos do mouse até e incluindo o último evento [**MouseUp**](inkedit-mouseup.md) .</span><span class="sxs-lookup"><span data-stu-id="ab3d8-138">If a mouse button is pressed while the pointer is over an [InkEdit](inkedit-control-reference.md) control, that control captures the mouse and receives all mouse events up to and including the last [**MouseUp**](inkedit-mouseup.md) event.</span></span> <span data-ttu-id="ab3d8-139">Isso implica que as coordenadas do ponteiro do mouse (x, y) retornadas por um evento do mouse talvez nem sempre estejam na área interna do objeto que as recebe.</span><span class="sxs-lookup"><span data-stu-id="ab3d8-139">This implies that the (x, y) mouse-pointer coordinates returned by a mouse event may not always be in the internal area of the object that receives them.</span></span>

<span data-ttu-id="ab3d8-140">Se os botões do mouse forem pressionados sucessivamente, o objeto que captura o mouse após o primeiro pressionamento receberá todos os eventos do mouse até que todos os botões sejam liberados.</span><span class="sxs-lookup"><span data-stu-id="ab3d8-140">If mouse buttons are pressed in succession, the object that captures the mouse after the first press receives all mouse events until all buttons are released.</span></span>

<span data-ttu-id="ab3d8-141">Esse método de evento é definido na interface **\_ IInkEditEvents** .</span><span class="sxs-lookup"><span data-stu-id="ab3d8-141">This event method is defined in the **\_IInkEditEvents** interface.</span></span> <span data-ttu-id="ab3d8-142">A interface **\_ IInkEditEvents** implementa a interface [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) com um identificador de \_ IeeMouseDown DISPID.</span><span class="sxs-lookup"><span data-stu-id="ab3d8-142">The **\_IInkEditEvents** interface implements the [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interface with an identifier of DISPID\_IeeMouseDown.</span></span>

## <a name="requirements"></a><span data-ttu-id="ab3d8-143">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ab3d8-143">Requirements</span></span>



| <span data-ttu-id="ab3d8-144">Requisito</span><span class="sxs-lookup"><span data-stu-id="ab3d8-144">Requirement</span></span> | <span data-ttu-id="ab3d8-145">Valor</span><span class="sxs-lookup"><span data-stu-id="ab3d8-145">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ab3d8-146">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ab3d8-146">Minimum supported client</span></span><br/> | <span data-ttu-id="ab3d8-147">Somente aplicativos de área de trabalho do Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="ab3d8-147">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="ab3d8-148">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ab3d8-148">Minimum supported server</span></span><br/> | <span data-ttu-id="ab3d8-149">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="ab3d8-149">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="ab3d8-150">parâmetro</span><span class="sxs-lookup"><span data-stu-id="ab3d8-150">Header</span></span><br/>                   | <dl> <span data-ttu-id="ab3d8-151"><dt>Inked. h (também requer Inked \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="ab3d8-151"><dt>Inked.h (also requires inked\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="ab3d8-152">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="ab3d8-152">Library</span></span><br/>                  | <dl> <span data-ttu-id="ab3d8-153"><dt>InkEd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ab3d8-153"><dt>InkEd.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="ab3d8-154">Confira também</span><span class="sxs-lookup"><span data-stu-id="ab3d8-154">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ab3d8-155">InkEdit</span><span class="sxs-lookup"><span data-stu-id="ab3d8-155">InkEdit</span></span>](inkedit-control-reference.md)
</dt> <dt>

[<span data-ttu-id="ab3d8-156">**Enumeração InkMouseButton**</span><span class="sxs-lookup"><span data-stu-id="ab3d8-156">**InkMouseButton Enumeration**</span></span>](/windows/desktop/api/msinkaut/ne-msinkaut-inkmousebutton)
</dt> <dt>

[<span data-ttu-id="ab3d8-157">**Enumeração InkShiftKeyModifierFlags**</span><span class="sxs-lookup"><span data-stu-id="ab3d8-157">**InkShiftKeyModifierFlags Enumeration**</span></span>](/windows/desktop/api/msinkaut/ne-msinkaut-inkshiftkeymodifierflags)
</dt> <dt>

<span data-ttu-id="ab3d8-158">[**Controle de evento \[ InkEdit MouseMove\]**](inkedit-mousemove.md)</span><span class="sxs-lookup"><span data-stu-id="ab3d8-158">[**MouseMove Event \[InkEdit Control\]**](inkedit-mousemove.md)</span></span>
</dt> <dt>

<span data-ttu-id="ab3d8-159">[**Controle de evento InkEdit do MouseUp \[\]**](inkedit-mouseup.md)</span><span class="sxs-lookup"><span data-stu-id="ab3d8-159">[**MouseUp Event \[InkEdit Control\]**](inkedit-mouseup.md)</span></span>
</dt> </dl>

 

