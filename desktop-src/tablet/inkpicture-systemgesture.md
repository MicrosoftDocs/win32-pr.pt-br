---
description: Ocorre quando um gesto do sistema é reconhecido.
ms.assetid: 36e2ac5a-dc91-47c2-a8e5-e555437c0a5d
title: InkPicture.Sysevento temGesture (Msinkaut. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 918198e4d18a854bb4238ce9d878dc70ab1f2f82
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105812038"
---
# <a name="inkpicturesystemgesture-event"></a><span data-ttu-id="0cb57-103">InkPicture.Sysevento temGesture</span><span class="sxs-lookup"><span data-stu-id="0cb57-103">InkPicture.SystemGesture event</span></span>

<span data-ttu-id="0cb57-104">Ocorre quando um gesto do sistema é reconhecido.</span><span class="sxs-lookup"><span data-stu-id="0cb57-104">Occurs when a system gesture is recognized.</span></span>

## <a name="syntax"></a><span data-ttu-id="0cb57-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="0cb57-105">Syntax</span></span>


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



## <a name="parameters"></a><span data-ttu-id="0cb57-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="0cb57-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0cb57-107">*Cursor* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="0cb57-107">*Cursor* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0cb57-108">O objeto [**IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) que gerou o evento **SystemGesture** .</span><span class="sxs-lookup"><span data-stu-id="0cb57-108">The [**IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) object that generated the **SystemGesture** event.</span></span>

</dd> <dt>

<span data-ttu-id="0cb57-109">*ID* \[ em\]</span><span class="sxs-lookup"><span data-stu-id="0cb57-109">*Id* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0cb57-110">O valor do gesto do sistema.</span><span class="sxs-lookup"><span data-stu-id="0cb57-110">The value of the system gesture.</span></span>

</dd> <dt>

<span data-ttu-id="0cb57-111">*X* \[ em\]</span><span class="sxs-lookup"><span data-stu-id="0cb57-111">*X* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0cb57-112">A coordenada x da localização do gesto.</span><span class="sxs-lookup"><span data-stu-id="0cb57-112">The x-coordinate of the location of the gesture.</span></span>

</dd> <dt>

<span data-ttu-id="0cb57-113">*Y* \[ em\]</span><span class="sxs-lookup"><span data-stu-id="0cb57-113">*Y* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0cb57-114">A coordenada y do local do gesto.</span><span class="sxs-lookup"><span data-stu-id="0cb57-114">The y-coordinate of the location of the gesture.</span></span>

</dd> <dt>

<span data-ttu-id="0cb57-115">*Modificador* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="0cb57-115">*Modifier* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0cb57-116">Reservado.</span><span class="sxs-lookup"><span data-stu-id="0cb57-116">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="0cb57-117">*Caractere* \[ de no\]</span><span class="sxs-lookup"><span data-stu-id="0cb57-117">*Character* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0cb57-118">Reservado.</span><span class="sxs-lookup"><span data-stu-id="0cb57-118">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="0cb57-119">*CursorMode* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="0cb57-119">*CursorMode* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0cb57-120">Um valor que indica se o objeto [**IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) está no modo normal ou borracha.</span><span class="sxs-lookup"><span data-stu-id="0cb57-120">A value that indicates whether the [**IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) object is in normal mode or eraser mode.</span></span> <span data-ttu-id="0cb57-121">1 é para o modo normal e 2 são para o modo de borracha.</span><span class="sxs-lookup"><span data-stu-id="0cb57-121">1 is for normal mode and 2 are for eraser mode.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0cb57-122">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="0cb57-122">Return value</span></span>

<span data-ttu-id="0cb57-123">Esse evento não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="0cb57-123">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="0cb57-124">Comentários</span><span class="sxs-lookup"><span data-stu-id="0cb57-124">Remarks</span></span>

<span data-ttu-id="0cb57-125">Os gestos do sistema fornecem informações sobre o objeto [**IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) que está sendo usado para criar o gesto.</span><span class="sxs-lookup"><span data-stu-id="0cb57-125">System gestures give information about the [**IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) object that is being used to create the gesture.</span></span> <span data-ttu-id="0cb57-126">Eles também fornecem atalhos para combinações de eventos de mouse e são maneiras de detectar eventos de mouse com menos impacto no desempenho.</span><span class="sxs-lookup"><span data-stu-id="0cb57-126">They also provide shortcuts to combinations of mouse events and are ways to detect mouse events with less impact on performance.</span></span>

<span data-ttu-id="0cb57-127">Por exemplo, em vez de procurar por um evento [**MouseUp \[ \]**](inkpicture-mouseup.md)controle InkPicture / [**de \[ \] evento**](inkpicture-mousedown.md) de controle de eventos MouseDown com nenhum outro evento de mouse ocorrendo no, você pode procurar os gestos do sistema Tap ou RightTap.</span><span class="sxs-lookup"><span data-stu-id="0cb57-127">For example, instead of looking for a [**MouseUp Event \[InkPicture Control\]**](inkpicture-mouseup.md)/[**MouseDown Event \[InkPicture Control\]**](inkpicture-mousedown.md) pair of events with no other mouse events occurring in between, you can look for the Tap or RightTap system gestures.</span></span>

<span data-ttu-id="0cb57-128">Como outro exemplo, em vez de escutar eventos de controle de InkPicture de [**evento de controle de eventos de \[ \]**](inkpicture-mousedown.md)evento / [**MouseMove \[ \]**](inkpicture-mousemove.md) e obter inúmeras mensagens de **\[ controle \] de InkPicture** de evento MouseMove, você pode observar os gestos do sistema de arrastar ou RightDrag, contanto que não esteja interessado nas coordenadas (x, y) de cada posição do mouse.</span><span class="sxs-lookup"><span data-stu-id="0cb57-128">As another example, instead of listening for [**MouseDown Event \[InkPicture Control\]**](inkpicture-mousedown.md)/[**MouseMove Event \[InkPicture Control\]**](inkpicture-mousemove.md) events and getting numerous **MouseMove Event \[InkPicture Control\]** messages, you can watch for the Drag or RightDrag system gestures as long as you're not interested in the (x, y) coordinates of every position of the mouse.</span></span> <span data-ttu-id="0cb57-129">Isso permite que você receba apenas uma mensagem em vez de várias mensagens de **\[ controle \] de InkPicture de evento MouseMove** .</span><span class="sxs-lookup"><span data-stu-id="0cb57-129">This allows you to receive only one message instead of numerous **MouseMove Event \[InkPicture Control\]** messages.</span></span>

<span data-ttu-id="0cb57-130">Para obter uma lista de gestos do sistema específicos, consulte o tipo de enumeração [**InkSystemGesture**](/windows/desktop/api/msinkaut/ne-msinkaut-inksystemgesture) .</span><span class="sxs-lookup"><span data-stu-id="0cb57-130">For a list of specific system gestures, see the [**InkSystemGesture**](/windows/desktop/api/msinkaut/ne-msinkaut-inksystemgesture) enumeration type.</span></span> <span data-ttu-id="0cb57-131">Para obter mais informações sobre gestos do sistema, consulte [usando gestos](using-gestures.md) e [entrada de comando no Tablet PC](/previous-versions//dd314533(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="0cb57-131">For more information about system gestures, see [Using Gestures](using-gestures.md) and [Command Input on the Tablet PC](/previous-versions//dd314533(v=vs.85)).</span></span>

<span data-ttu-id="0cb57-132">Esse método de evento é definido nas interfaces somente de expedição **\_ IInkCollectorEvents**, **\_ IInkOverlayEvents** e **\_ IInkPictureEvents** (dispinterfaces) com uma ID de ICESystemGesture de DISPID \_ .</span><span class="sxs-lookup"><span data-stu-id="0cb57-132">This event method is defined in the **\_IInkCollectorEvents**, **\_IInkOverlayEvents**, and **\_IInkPictureEvents** dispatch-only interfaces (dispinterfaces) with an ID of DISPID\_ICESystemGesture.</span></span>

## <a name="requirements"></a><span data-ttu-id="0cb57-133">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0cb57-133">Requirements</span></span>



| <span data-ttu-id="0cb57-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="0cb57-134">Requirement</span></span> | <span data-ttu-id="0cb57-135">Valor</span><span class="sxs-lookup"><span data-stu-id="0cb57-135">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0cb57-136">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="0cb57-136">Minimum supported client</span></span><br/> | <span data-ttu-id="0cb57-137">Somente aplicativos de área de trabalho do Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="0cb57-137">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="0cb57-138">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="0cb57-138">Minimum supported server</span></span><br/> | <span data-ttu-id="0cb57-139">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="0cb57-139">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="0cb57-140">parâmetro</span><span class="sxs-lookup"><span data-stu-id="0cb57-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="0cb57-141"><dt>Msinkaut. h (também requer Msinkaut \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="0cb57-141"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="0cb57-142">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="0cb57-142">Library</span></span><br/>                  | <dl> <span data-ttu-id="0cb57-143"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0cb57-143"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="0cb57-144">Confira também</span><span class="sxs-lookup"><span data-stu-id="0cb57-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0cb57-145">InkPicture</span><span class="sxs-lookup"><span data-stu-id="0cb57-145">InkPicture</span></span>](inkpicture-control-reference.md)
</dt> <dt>

[<span data-ttu-id="0cb57-146">**Enumeração InkSystemGesture**</span><span class="sxs-lookup"><span data-stu-id="0cb57-146">**InkSystemGesture Enumeration**</span></span>](/windows/desktop/api/msinkaut/ne-msinkaut-inksystemgesture)
</dt> <dt>

[<span data-ttu-id="0cb57-147">Usando gestos</span><span class="sxs-lookup"><span data-stu-id="0cb57-147">Using Gestures</span></span>](using-gestures.md)
</dt> </dl>

 

