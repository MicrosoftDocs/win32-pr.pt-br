---
description: Ocorre quando um gesto do sistema é reconhecido.
ms.assetid: 11071d6f-8aa3-4902-94fd-89ad0cf17729
title: InkCollector.Sysevento temGesture (Msinkaut. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 282f28e5ef1bc3a86f51b6d345be6e00d78c8213
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104501620"
---
# <a name="inkcollectorsystemgesture-event"></a><span data-ttu-id="41799-103">InkCollector.Sysevento temGesture</span><span class="sxs-lookup"><span data-stu-id="41799-103">InkCollector.SystemGesture event</span></span>

<span data-ttu-id="41799-104">Ocorre quando um gesto do sistema é reconhecido.</span><span class="sxs-lookup"><span data-stu-id="41799-104">Occurs when a system gesture is recognized.</span></span>

## <a name="syntax"></a><span data-ttu-id="41799-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="41799-105">Syntax</span></span>


```C++
void SystemGesture(
  [in] IInkCursor       *Cursor,
  [in] InkSystemGesture Id,
  [in] long             X,
  [in] long             Y,
  [in] long             Modifier,
  [in] BSTR             Character,
  [in] long             CursorMode
);
```



## <a name="parameters"></a><span data-ttu-id="41799-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="41799-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="41799-107">*Cursor* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="41799-107">*Cursor* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="41799-108">O objeto [**IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) que gerou o evento **SystemGesture** .</span><span class="sxs-lookup"><span data-stu-id="41799-108">The [**IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) object that generated the **SystemGesture** event.</span></span>

</dd> <dt>

<span data-ttu-id="41799-109">*ID* \[ em\]</span><span class="sxs-lookup"><span data-stu-id="41799-109">*Id* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="41799-110">O valor do gesto do sistema.</span><span class="sxs-lookup"><span data-stu-id="41799-110">The value of the system gesture.</span></span>

</dd> <dt>

<span data-ttu-id="41799-111">*X* \[ em\]</span><span class="sxs-lookup"><span data-stu-id="41799-111">*X* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="41799-112">A coordenada x da localização do gesto.</span><span class="sxs-lookup"><span data-stu-id="41799-112">The x-coordinate of the location of the gesture.</span></span>

</dd> <dt>

<span data-ttu-id="41799-113">*Y* \[ em\]</span><span class="sxs-lookup"><span data-stu-id="41799-113">*Y* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="41799-114">A coordenada y do local do gesto.</span><span class="sxs-lookup"><span data-stu-id="41799-114">The y-coordinate of the location of the gesture.</span></span>

</dd> <dt>

<span data-ttu-id="41799-115">*Modificador* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="41799-115">*Modifier* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="41799-116">Reservado.</span><span class="sxs-lookup"><span data-stu-id="41799-116">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="41799-117">*Caractere* \[ de no\]</span><span class="sxs-lookup"><span data-stu-id="41799-117">*Character* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="41799-118">Reservado.</span><span class="sxs-lookup"><span data-stu-id="41799-118">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="41799-119">*CursorMode* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="41799-119">*CursorMode* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="41799-120">Um valor que indica se o objeto [**IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) está no modo normal ou borracha.</span><span class="sxs-lookup"><span data-stu-id="41799-120">A value that indicates whether the [**IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) object is in normal mode or eraser mode.</span></span> <span data-ttu-id="41799-121">1 é para o modo normal e 2 são para o modo de borracha.</span><span class="sxs-lookup"><span data-stu-id="41799-121">1 is for normal mode and 2 are for eraser mode.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="41799-122">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="41799-122">Return value</span></span>

<span data-ttu-id="41799-123">Esse evento não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="41799-123">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="41799-124">Comentários</span><span class="sxs-lookup"><span data-stu-id="41799-124">Remarks</span></span>

<span data-ttu-id="41799-125">Os gestos do sistema são úteis porque fornecem informações sobre o objeto [**IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) que está sendo usado para criar o gesto.</span><span class="sxs-lookup"><span data-stu-id="41799-125">System gestures are useful because they give information about the [**IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) object that is being used to create the gesture.</span></span> <span data-ttu-id="41799-126">Eles também fornecem atalhos para combinações de eventos de mouse e são maneiras "mais baratas" de detectar eventos de mouse.</span><span class="sxs-lookup"><span data-stu-id="41799-126">They also provide shortcuts to combinations of mouse events and are "cheaper" ways to detect mouse events.</span></span>

<span data-ttu-id="41799-127">Por exemplo, em vez de procurar por [**um**](inkcollector-mouseup.md)  /  par de eventos [**evento MouseDown**](inkcollector-mousedown.md) evento do MouseUp sem outros eventos de mouse ocorrendo no, você pode procurar os gestos do sistema [**Tap**](/windows/desktop/api/msinkaut/ne-msinkaut-inksystemgesture) ou **RightTap** .</span><span class="sxs-lookup"><span data-stu-id="41799-127">For example, instead of looking for a [**MouseUp Event**](inkcollector-mouseup.md) / [**MouseDown Event**](inkcollector-mousedown.md) pair of events with no other mouse events occurring in between, you can look for the [**Tap**](/windows/desktop/api/msinkaut/ne-msinkaut-inksystemgesture) or **RightTap** system gestures.</span></span>

<span data-ttu-id="41799-128">Como outro exemplo, em vez de escutar eventos de evento MouseMove do [**evento MouseDown**](inkcollector-mousedown.md)  /  [](inkcollector-mousemove.md) e obter inúmeras mensagens de **evento MouseMove** , você pode observar os gestos do sistema de [**arrastar**](/windows/desktop/api/msinkaut/ne-msinkaut-inksystemgesture) ou **RightDrag** , contanto que não esteja interessado nas coordenadas (x, y) de cada posição do mouse.</span><span class="sxs-lookup"><span data-stu-id="41799-128">As another example, instead of listening for [**MouseDown Event**](inkcollector-mousedown.md) / [**MouseMove Event**](inkcollector-mousemove.md) events and getting numerous **MouseMove Event** messages, you can watch for the [**Drag**](/windows/desktop/api/msinkaut/ne-msinkaut-inksystemgesture) or **RightDrag** system gestures as long as you're not interested in the (x, y) coordinates of every position of the mouse.</span></span> <span data-ttu-id="41799-129">Isso permite que você receba apenas uma mensagem em vez de várias mensagens de **evento MouseMove** .</span><span class="sxs-lookup"><span data-stu-id="41799-129">This allows you to receive only one message instead of numerous **MouseMove Event** messages.</span></span>

<span data-ttu-id="41799-130">Para obter uma lista de gestos do sistema específicos, consulte o tipo de enumeração [**InkSystemGesture**](/windows/desktop/api/msinkaut/ne-msinkaut-inksystemgesture) .</span><span class="sxs-lookup"><span data-stu-id="41799-130">For a list of specific system gestures, see the [**InkSystemGesture**](/windows/desktop/api/msinkaut/ne-msinkaut-inksystemgesture) enumeration type.</span></span> <span data-ttu-id="41799-131">Para obter mais informações sobre gestos do sistema, consulte [usando gestos](using-gestures.md) e [entrada de comando no Tablet PC](/previous-versions//dd314533(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="41799-131">For more information about system gestures, see [Using Gestures](using-gestures.md) and [Command Input on the Tablet PC](/previous-versions//dd314533(v=vs.85)).</span></span>

<span data-ttu-id="41799-132">Esse método de evento é definido nas \_ \_ interfaces somente de expedição IInkCollectorEvents, IInkOverlayEvents e \_ IInkPictureEvents (dispinterfaces) com uma ID de ICESystemGesture de DISPID \_ .</span><span class="sxs-lookup"><span data-stu-id="41799-132">This event method is defined in the \_IInkCollectorEvents, \_IInkOverlayEvents, and \_IInkPictureEvents dispatch-only interfaces (dispinterfaces) with an ID of DISPID\_ICESystemGesture.</span></span>

## <a name="requirements"></a><span data-ttu-id="41799-133">Requisitos</span><span class="sxs-lookup"><span data-stu-id="41799-133">Requirements</span></span>



| <span data-ttu-id="41799-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="41799-134">Requirement</span></span> | <span data-ttu-id="41799-135">Valor</span><span class="sxs-lookup"><span data-stu-id="41799-135">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="41799-136">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="41799-136">Minimum supported client</span></span><br/> | <span data-ttu-id="41799-137">Somente aplicativos de área de trabalho do Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="41799-137">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="41799-138">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="41799-138">Minimum supported server</span></span><br/> | <span data-ttu-id="41799-139">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="41799-139">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="41799-140">parâmetro</span><span class="sxs-lookup"><span data-stu-id="41799-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="41799-141"><dt>Msinkaut. h (também requer Msinkaut \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="41799-141"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="41799-142">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="41799-142">Library</span></span><br/>                  | <dl> <span data-ttu-id="41799-143"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="41799-143"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="41799-144">Confira também</span><span class="sxs-lookup"><span data-stu-id="41799-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="41799-145">**Classe InkCollector**</span><span class="sxs-lookup"><span data-stu-id="41799-145">**InkCollector Class**</span></span>](inkcollector-class.md)
</dt> <dt>

[<span data-ttu-id="41799-146">**Enumeração InkSystemGesture**</span><span class="sxs-lookup"><span data-stu-id="41799-146">**InkSystemGesture Enumeration**</span></span>](/windows/desktop/api/msinkaut/ne-msinkaut-inksystemgesture)
</dt> <dt>

[<span data-ttu-id="41799-147">**Interface IInkCursor**</span><span class="sxs-lookup"><span data-stu-id="41799-147">**IInkCursor Interface**</span></span>](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor)
</dt> <dt>

[<span data-ttu-id="41799-148">Usando gestos</span><span class="sxs-lookup"><span data-stu-id="41799-148">Using Gestures</span></span>](using-gestures.md)
</dt> <dt>

[<span data-ttu-id="41799-149">Entrada, tinta e reconhecimento de caneta</span><span class="sxs-lookup"><span data-stu-id="41799-149">Pen Input, Ink, and Recognition</span></span>](pen-input--ink--and-recognition.md)
</dt> <dt>

<span data-ttu-id="41799-150">[Entrada de comando no Tablet PC](/previous-versions//dd314533(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="41799-150">[Command Input on the Tablet PC](/previous-versions//dd314533(v=vs.85))</span></span>
</dt> </dl>

 

