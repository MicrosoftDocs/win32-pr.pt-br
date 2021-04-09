---
description: Ocorre quando o usuário libera um botão do mouse enquanto o mouse está sobre o controle InkEdit.
ms.assetid: 3c9e0229-c7e2-4b5c-9532-18fbf8a3667d
title: Evento InkEdit. MouseUp (Inked. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c331ec5dd0dd6a39ec956eda6980ee02cddd298e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104171542"
---
# <a name="inkeditmouseup-event"></a><span data-ttu-id="f3f92-103">Evento InkEdit. MouseUp</span><span class="sxs-lookup"><span data-stu-id="f3f92-103">InkEdit.MouseUp event</span></span>

<span data-ttu-id="f3f92-104">Ocorre quando o usuário libera um botão do mouse enquanto o mouse está sobre o controle [InkEdit](inkedit-control-reference.md) .</span><span class="sxs-lookup"><span data-stu-id="f3f92-104">Occurs when the user releases a mouse button while the mouse is over the [InkEdit](inkedit-control-reference.md) control.</span></span>

## <a name="syntax"></a><span data-ttu-id="f3f92-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="f3f92-105">Syntax</span></span>


```C++
HRESULT MouseUp(
   short Button,
   short ShiftKey,
   long  xMouse,
   long  yMouse
);
```



## <a name="parameters"></a><span data-ttu-id="f3f92-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="f3f92-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f3f92-107">*Botão*</span><span class="sxs-lookup"><span data-stu-id="f3f92-107">*Button*</span></span> 
</dt> <dd>

<span data-ttu-id="f3f92-108">Um membro da enumeração [**MouseButton**](/windows/desktop/api/inked/ne-inked-mousebutton) que indica quais botões do mouse foram liberados.</span><span class="sxs-lookup"><span data-stu-id="f3f92-108">A member of the [**MouseButton**](/windows/desktop/api/inked/ne-inked-mousebutton) enumeration that indicates which mouse buttons were released.</span></span>



| <span data-ttu-id="f3f92-109">Valor</span><span class="sxs-lookup"><span data-stu-id="f3f92-109">Value</span></span>                                                                                                                                                            | <span data-ttu-id="f3f92-110">Significado</span><span class="sxs-lookup"><span data-stu-id="f3f92-110">Meaning</span></span>                                           |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------|
| <span id="NO_BUTTON_"></span><span id="no_button_"></span><dl> <span data-ttu-id="f3f92-111"><dt>**Não \_ BOTÃO**</dt></span><span class="sxs-lookup"><span data-stu-id="f3f92-111"><dt>**NO\_BUTTON** </dt></span></span> </dl>             | <span data-ttu-id="f3f92-112">Padrão.</span><span class="sxs-lookup"><span data-stu-id="f3f92-112">Default.</span></span> <span data-ttu-id="f3f92-113">Nenhum botão do mouse foi pressionado.</span><span class="sxs-lookup"><span data-stu-id="f3f92-113">No mouse button was pressed.</span></span> <br/> |
| <span id="LEFT_BUTTON_"></span><span id="left_button_"></span><dl> <span data-ttu-id="f3f92-114"><dt>**À esquerda \_ BOTÃO**</dt></span><span class="sxs-lookup"><span data-stu-id="f3f92-114"><dt>**LEFT\_BUTTON** </dt></span></span> </dl>       | <span data-ttu-id="f3f92-115">O botão esquerdo do mouse foi pressionado.</span><span class="sxs-lookup"><span data-stu-id="f3f92-115">The left mouse button was pressed.</span></span> <br/>    |
| <span id="RIGHT_BUTTON_"></span><span id="right_button_"></span><dl> <span data-ttu-id="f3f92-116"><dt>**À direita \_ BOTÃO**</dt></span><span class="sxs-lookup"><span data-stu-id="f3f92-116"><dt>**RIGHT\_BUTTON** </dt></span></span> </dl>    | <span data-ttu-id="f3f92-117">O botão direito do mouse foi pressionado.</span><span class="sxs-lookup"><span data-stu-id="f3f92-117">The right mouse button was pressed.</span></span> <br/>   |
| <span id="MIDDLE_BUTTON_"></span><span id="middle_button_"></span><dl> <span data-ttu-id="f3f92-118"><dt>**Meio \_ BOTÃO**</dt></span><span class="sxs-lookup"><span data-stu-id="f3f92-118"><dt>**MIDDLE\_BUTTON** </dt></span></span> </dl> | <span data-ttu-id="f3f92-119">O botão do meio do mouse foi pressionado.</span><span class="sxs-lookup"><span data-stu-id="f3f92-119">The middle mouse button was pressed.</span></span> <br/>  |



 

</dd> <dt>

<span data-ttu-id="f3f92-120">*ShiftKey*</span><span class="sxs-lookup"><span data-stu-id="f3f92-120">*ShiftKey*</span></span> 
</dt> <dd>

<span data-ttu-id="f3f92-121">Um membro da enumeração [**InkShiftKeyModifierFlags**](/windows/desktop/api/msinkaut/ne-msinkaut-inkshiftkeymodifierflags) que indica quais teclas modificadoras são pressionadas no momento do evento.</span><span class="sxs-lookup"><span data-stu-id="f3f92-121">A member of the [**InkShiftKeyModifierFlags**](/windows/desktop/api/msinkaut/ne-msinkaut-inkshiftkeymodifierflags) enumeration that indicates which modifier keys are depressed at the time of the event.</span></span>



| <span data-ttu-id="f3f92-122">Valor</span><span class="sxs-lookup"><span data-stu-id="f3f92-122">Value</span></span>                                                                                                                                                                                     | <span data-ttu-id="f3f92-123">Significado</span><span class="sxs-lookup"><span data-stu-id="f3f92-123">Meaning</span></span>                                                          |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------|
| <span id="IKM_Shift"></span><span id="ikm_shift"></span><span id="IKM_SHIFT"></span><dl> <span data-ttu-id="f3f92-124"><dt>**IKM \_ Shift**</dt></span><span class="sxs-lookup"><span data-stu-id="f3f92-124"><dt>**IKM\_Shift**</dt></span></span> </dl>             | <span data-ttu-id="f3f92-125">Especifica que a tecla SHIFT foi usada como um modificador.</span><span class="sxs-lookup"><span data-stu-id="f3f92-125">Specifies that the SHIFT key was used as a modifier.</span></span> <br/> |
| <span id="IKM_Control_"></span><span id="ikm_control_"></span><span id="IKM_CONTROL_"></span><dl> <span data-ttu-id="f3f92-126"><dt>**IKM \_ Controle** do</dt></span><span class="sxs-lookup"><span data-stu-id="f3f92-126"><dt>**IKM\_Control** </dt></span></span> </dl> | <span data-ttu-id="f3f92-127">Especifica que a tecla CTRL foi usada como um modificador.</span><span class="sxs-lookup"><span data-stu-id="f3f92-127">Specifies that the CTRL key was used as a modifier.</span></span> <br/>  |
| <span id="IKM_Alt_"></span><span id="ikm_alt_"></span><span id="IKM_ALT_"></span><dl> <span data-ttu-id="f3f92-128"><dt>**IKM \_ Alt**</dt></span><span class="sxs-lookup"><span data-stu-id="f3f92-128"><dt>**IKM\_Alt** </dt></span></span> </dl>                 | <span data-ttu-id="f3f92-129">Especifica que a tecla ALT foi usada como um modificador.</span><span class="sxs-lookup"><span data-stu-id="f3f92-129">Specifies that the ALT key was used as a modifier.</span></span> <br/>   |



 

</dd> <dt>

<span data-ttu-id="f3f92-130">*xMouse*</span><span class="sxs-lookup"><span data-stu-id="f3f92-130">*xMouse*</span></span> 
</dt> <dd>

<span data-ttu-id="f3f92-131">A coordenada x atual, em pixels, do ponteiro do mouse.</span><span class="sxs-lookup"><span data-stu-id="f3f92-131">The current x coordinate, in pixels, of the mouse pointer.</span></span>

</dd> <dt>

<span data-ttu-id="f3f92-132">*yMouse*</span><span class="sxs-lookup"><span data-stu-id="f3f92-132">*yMouse*</span></span> 
</dt> <dd>

<span data-ttu-id="f3f92-133">A coordenada y atual, em pixels, do ponteiro do mouse.</span><span class="sxs-lookup"><span data-stu-id="f3f92-133">The current y coordinate, in pixels, of the mouse pointer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f3f92-134">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="f3f92-134">Return value</span></span>

<span data-ttu-id="f3f92-135">Se esse evento for bem sucedido, ele retornará **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="f3f92-135">If this event succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="f3f92-136">Caso contrário, ele retorna um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="f3f92-136">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="f3f92-137">Comentários</span><span class="sxs-lookup"><span data-stu-id="f3f92-137">Remarks</span></span>

<span data-ttu-id="f3f92-138">Se um botão do mouse for pressionado enquanto o ponteiro estiver sobre um controle [InkEdit](inkedit-control-reference.md) , esse controle capturará o mouse e receberá todos os eventos do mouse até e incluindo o último evento **MouseUp** .</span><span class="sxs-lookup"><span data-stu-id="f3f92-138">If a mouse button is pressed while the pointer is over an [InkEdit](inkedit-control-reference.md) control, that control captures the mouse and receives all mouse events up to and including the last **MouseUp** event.</span></span> <span data-ttu-id="f3f92-139">Isso implica que as coordenadas do ponteiro do mouse (x, y) retornadas por um evento do mouse talvez nem sempre estejam na área interna do objeto que as recebe.</span><span class="sxs-lookup"><span data-stu-id="f3f92-139">This implies that the (x, y) mouse-pointer coordinates returned by a mouse event may not always be in the internal area of the object that receives them.</span></span>

<span data-ttu-id="f3f92-140">Se os botões do mouse forem pressionados sucessivamente, o objeto que captura o mouse após o primeiro pressionamento receberá todos os eventos do mouse até que todos os botões sejam liberados.</span><span class="sxs-lookup"><span data-stu-id="f3f92-140">If mouse buttons are pressed in succession, the object that captures the mouse after the first press receives all mouse events until all buttons are released.</span></span>

<span data-ttu-id="f3f92-141">Esse método de evento é definido na interface **\_ IInkEditEvents** .</span><span class="sxs-lookup"><span data-stu-id="f3f92-141">This event method is defined in the **\_IInkEditEvents** interface.</span></span> <span data-ttu-id="f3f92-142">A interface **\_ IInkEditEvents** implementa a interface [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) com um identificador de \_ IeeMouseUp DISPID.</span><span class="sxs-lookup"><span data-stu-id="f3f92-142">The **\_IInkEditEvents** interface implements the [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interface with an identifier of DISPID\_IeeMouseUp.</span></span>

## <a name="requirements"></a><span data-ttu-id="f3f92-143">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f3f92-143">Requirements</span></span>



| <span data-ttu-id="f3f92-144">Requisito</span><span class="sxs-lookup"><span data-stu-id="f3f92-144">Requirement</span></span> | <span data-ttu-id="f3f92-145">Valor</span><span class="sxs-lookup"><span data-stu-id="f3f92-145">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f3f92-146">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f3f92-146">Minimum supported client</span></span><br/> | <span data-ttu-id="f3f92-147">Somente aplicativos de área de trabalho do Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="f3f92-147">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="f3f92-148">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f3f92-148">Minimum supported server</span></span><br/> | <span data-ttu-id="f3f92-149">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="f3f92-149">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="f3f92-150">parâmetro</span><span class="sxs-lookup"><span data-stu-id="f3f92-150">Header</span></span><br/>                   | <dl> <span data-ttu-id="f3f92-151"><dt>Inked. h (também requer Inked \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="f3f92-151"><dt>Inked.h (also requires inked\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="f3f92-152">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="f3f92-152">Library</span></span><br/>                  | <dl> <span data-ttu-id="f3f92-153"><dt>InkEd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f3f92-153"><dt>InkEd.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="f3f92-154">Confira também</span><span class="sxs-lookup"><span data-stu-id="f3f92-154">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f3f92-155">InkEdit</span><span class="sxs-lookup"><span data-stu-id="f3f92-155">InkEdit</span></span>](inkedit-control-reference.md)
</dt> <dt>

[<span data-ttu-id="f3f92-156">**Enumeração InkMouseButton**</span><span class="sxs-lookup"><span data-stu-id="f3f92-156">**InkMouseButton Enumeration**</span></span>](/windows/desktop/api/msinkaut/ne-msinkaut-inkmousebutton)
</dt> <dt>

[<span data-ttu-id="f3f92-157">**Enumeração InkShiftKeyModifierFlags**</span><span class="sxs-lookup"><span data-stu-id="f3f92-157">**InkShiftKeyModifierFlags Enumeration**</span></span>](/windows/desktop/api/msinkaut/ne-msinkaut-inkshiftkeymodifierflags)
</dt> <dt>

<span data-ttu-id="f3f92-158">[**Controle de evento InkEdit do MouseDown \[\]**](inkedit-mousedown.md)</span><span class="sxs-lookup"><span data-stu-id="f3f92-158">[**MouseDown Event \[InkEdit Control\]**](inkedit-mousedown.md)</span></span>
</dt> <dt>

<span data-ttu-id="f3f92-159">[**Controle de evento \[ InkEdit MouseMove\]**](inkedit-mousemove.md)</span><span class="sxs-lookup"><span data-stu-id="f3f92-159">[**MouseMove Event \[InkEdit Control\]**](inkedit-mousemove.md)</span></span>
</dt> </dl>

 

