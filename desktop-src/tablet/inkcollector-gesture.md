---
description: Evento InkCollector. Gesture-ocorre quando um gesto específico do aplicativo é reconhecido.
ms.assetid: 5830f7f8-2870-4194-ab3e-b63b71e97063
title: Evento InkCollector. Gesture (Msinkaut. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0bfc2fea09060dbb206cd7681bcecfbedbc7a6b4
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108110184"
---
# <a name="inkcollectorgesture-event"></a><span data-ttu-id="3e1aa-103">Evento InkCollector. Gesture</span><span class="sxs-lookup"><span data-stu-id="3e1aa-103">InkCollector.Gesture event</span></span>

<span data-ttu-id="3e1aa-104">Ocorre quando um gesto específico do aplicativo é reconhecido.</span><span class="sxs-lookup"><span data-stu-id="3e1aa-104">Occurs when an application-specific gesture is recognized.</span></span>

## <a name="syntax"></a><span data-ttu-id="3e1aa-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="3e1aa-105">Syntax</span></span>


```C++
void Gesture(
  [in]      IInkCursor   *Cursor,
  [in]      IInkStrokes  *Strokes,
  [in]      VARIANT      Gestures,
  [in, out] VARIANT_BOOL *Cancel
);
```



## <a name="parameters"></a><span data-ttu-id="3e1aa-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="3e1aa-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3e1aa-107">*Cursor* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="3e1aa-107">*Cursor* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3e1aa-108">O objeto [**IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) que gerou o evento de **gesto** .</span><span class="sxs-lookup"><span data-stu-id="3e1aa-108">The [**IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) object that generated the **Gesture** event.</span></span>

</dd> <dt>

<span data-ttu-id="3e1aa-109">*Traços* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="3e1aa-109">*Strokes* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3e1aa-110">A coleção [IInkStrokes](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) que o reconhecedor retornou como gesto.</span><span class="sxs-lookup"><span data-stu-id="3e1aa-110">The [IInkStrokes](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) collection that the recognizer returned as the gesture.</span></span>

</dd> <dt>

<span data-ttu-id="3e1aa-111">*Gestos* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="3e1aa-111">*Gestures* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3e1aa-112">Uma matriz de objetos [**IInkGesture**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkgesture) , em ordem de confiança, do reconhecedor.</span><span class="sxs-lookup"><span data-stu-id="3e1aa-112">An array of [**IInkGesture**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkgesture) objects, in order of confidence, from the recognizer.</span></span>

<span data-ttu-id="3e1aa-113">Para obter mais informações sobre a estrutura de VARIAntes, consulte [usando a biblioteca com](using-the-com-library.md).</span><span class="sxs-lookup"><span data-stu-id="3e1aa-113">For more information about the VARIANT structure, see [Using the COM Library](using-the-com-library.md).</span></span>

</dd> <dt>

<span data-ttu-id="3e1aa-114">*Cancelar* \[ entrada, saída\]</span><span class="sxs-lookup"><span data-stu-id="3e1aa-114">*Cancel* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="3e1aa-115">**Variante \_ TRUE** se este gesto deve ser cancelado; caso contrário, **Variant \_ false**.</span><span class="sxs-lookup"><span data-stu-id="3e1aa-115">**VARIANT\_TRUE** if this gesture should be cancelled; otherwise, **VARIANT\_FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3e1aa-116">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="3e1aa-116">Return value</span></span>

<span data-ttu-id="3e1aa-117">Esse evento não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="3e1aa-117">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="3e1aa-118">Comentários</span><span class="sxs-lookup"><span data-stu-id="3e1aa-118">Remarks</span></span>

<span data-ttu-id="3e1aa-119">Esse método de evento é definido nas \_ \_ interfaces somente de expedição IInkCollectorEvents, IInkOverlayEvents e \_ IInkPictureEvents (dispinterfaces) com uma ID de ICEGesture de DISPID \_ .</span><span class="sxs-lookup"><span data-stu-id="3e1aa-119">This event method is defined in the \_IInkCollectorEvents, \_IInkOverlayEvents, and \_IInkPictureEvents dispatch-only interfaces (dispinterfaces) with an ID of DISPID\_ICEGesture.</span></span>

<span data-ttu-id="3e1aa-120">Quando a propriedade [**CollectionMode**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_collectionmode) é definida como [**GestureOnly**](/windows/desktop/api/msinkaut/ne-msinkaut-inkcollectionmode), o tempo limite entre quando um usuário adiciona um gesto e quando o evento de **gesto** ocorre é um valor fixo que você não pode alterar programaticamente.</span><span class="sxs-lookup"><span data-stu-id="3e1aa-120">When the [**CollectionMode**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_collectionmode) property is set to [**GestureOnly**](/windows/desktop/api/msinkaut/ne-msinkaut-inkcollectionmode), the timeout between when a user adds a gesture and when the **Gesture** event occurs is a fixed value that you cannot alter programmatically.</span></span> <span data-ttu-id="3e1aa-121">O reconhecimento de gestos é mais rápido no modo **InkAndGesture** .</span><span class="sxs-lookup"><span data-stu-id="3e1aa-121">Gesture recognition is faster in **InkAndGesture** mode.</span></span>

<span data-ttu-id="3e1aa-122">Para evitar a coleta de tinta no modo [**InkAndGesture**](/windows/desktop/api/msinkaut/ne-msinkaut-inkcollectionmode) :</span><span class="sxs-lookup"><span data-stu-id="3e1aa-122">To prevent the collection of ink while in [**InkAndGesture**](/windows/desktop/api/msinkaut/ne-msinkaut-inkcollectionmode) mode:</span></span>

-   <span data-ttu-id="3e1aa-123">Defina [**CollectionMode**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_collectionmode) como [**InkAndGesture**](/windows/desktop/api/msinkaut/ne-msinkaut-inkcollectionmode).</span><span class="sxs-lookup"><span data-stu-id="3e1aa-123">Set [**CollectionMode**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_collectionmode) to [**InkAndGesture**](/windows/desktop/api/msinkaut/ne-msinkaut-inkcollectionmode).</span></span>
-   <span data-ttu-id="3e1aa-124">Exclua o traço no evento de [**traço**](inkcollector-stroke.md) .</span><span class="sxs-lookup"><span data-stu-id="3e1aa-124">Delete the stroke in the [**Stroke**](inkcollector-stroke.md) event.</span></span>
-   <span data-ttu-id="3e1aa-125">Processe o gesto no evento de **gesto** .</span><span class="sxs-lookup"><span data-stu-id="3e1aa-125">Process the gesture in the **Gesture** event.</span></span>

<span data-ttu-id="3e1aa-126">Para evitar o fluxo de tinta enquanto gesturing, defina a propriedade [**DynamicRendering**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_dynamicrendering) como **false**.</span><span class="sxs-lookup"><span data-stu-id="3e1aa-126">To prevent the flow of ink while gesturing, set [**DynamicRendering**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_dynamicrendering) property to **FALSE**.</span></span>

<span data-ttu-id="3e1aa-127">Além de ao inserir tinta, o evento de **gesto** é acionado no modo de seleção ou apagamento.</span><span class="sxs-lookup"><span data-stu-id="3e1aa-127">In addition to when inserting ink, the **Gesture** event is fired when in select or erase mode.</span></span> <span data-ttu-id="3e1aa-128">Você é responsável por controlar o modo de edição e deve estar ciente do modo antes de interpretar o evento.</span><span class="sxs-lookup"><span data-stu-id="3e1aa-128">You are responsible for tracking the editing mode and should be aware of the mode before interpreting the event.</span></span>

> [!Note]  
> <span data-ttu-id="3e1aa-129">Para reconhecer gestos, você deve usar um objeto ou controle que possa coletar tinta.</span><span class="sxs-lookup"><span data-stu-id="3e1aa-129">To recognize gestures, you must use an object or control that can collect ink.</span></span>

 

<span data-ttu-id="3e1aa-130">Os gestos de aplicativo são definidos como gestos com suporte no seu aplicativo.</span><span class="sxs-lookup"><span data-stu-id="3e1aa-130">Application gestures are defined as gestures that are supported within your application.</span></span>

<span data-ttu-id="3e1aa-131">Para que esse evento ocorra, o objeto ou controle deve ter interesse em um conjunto de gestos de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="3e1aa-131">For this event to occur, the object or control must have interest in a set of application gestures.</span></span> <span data-ttu-id="3e1aa-132">Para definir os objetos ou controles de interesse em um conjunto de gestos, chame o método [**SetGestureStatus**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-setgesturestatus) do objeto ou controle.</span><span class="sxs-lookup"><span data-stu-id="3e1aa-132">To set the objects or controls interest in a set of gestures, call the [**SetGestureStatus**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-setgesturestatus) method of the object or control.</span></span>

<span data-ttu-id="3e1aa-133">Para obter uma lista de gestos de aplicativo específicos, consulte o tipo de enumeração [**InkApplicationGesture**](/windows/desktop/api/msinkaut/ne-msinkaut-inkapplicationgesture) .</span><span class="sxs-lookup"><span data-stu-id="3e1aa-133">For a list of specific application gestures, see the [**InkApplicationGesture**](/windows/desktop/api/msinkaut/ne-msinkaut-inkapplicationgesture) enumeration type.</span></span>

## <a name="requirements"></a><span data-ttu-id="3e1aa-134">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3e1aa-134">Requirements</span></span>



| <span data-ttu-id="3e1aa-135">Requisito</span><span class="sxs-lookup"><span data-stu-id="3e1aa-135">Requirement</span></span> | <span data-ttu-id="3e1aa-136">Valor</span><span class="sxs-lookup"><span data-stu-id="3e1aa-136">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3e1aa-137">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3e1aa-137">Minimum supported client</span></span><br/> | <span data-ttu-id="3e1aa-138">Somente aplicativos de área de trabalho do Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="3e1aa-138">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="3e1aa-139">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3e1aa-139">Minimum supported server</span></span><br/> | <span data-ttu-id="3e1aa-140">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="3e1aa-140">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="3e1aa-141">parâmetro</span><span class="sxs-lookup"><span data-stu-id="3e1aa-141">Header</span></span><br/>                   | <dl> <span data-ttu-id="3e1aa-142"><dt>Msinkaut. h (também requer Msinkaut \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="3e1aa-142"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="3e1aa-143">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="3e1aa-143">Library</span></span><br/>                  | <dl> <span data-ttu-id="3e1aa-144"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3e1aa-144"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="3e1aa-145">Consulte também</span><span class="sxs-lookup"><span data-stu-id="3e1aa-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3e1aa-146">**Classe InkCollector**</span><span class="sxs-lookup"><span data-stu-id="3e1aa-146">**InkCollector Class**</span></span>](inkcollector-class.md)
</dt> <dt>

[<span data-ttu-id="3e1aa-147">**Enumeração InkApplicationGesture**</span><span class="sxs-lookup"><span data-stu-id="3e1aa-147">**InkApplicationGesture Enumeration**</span></span>](/windows/desktop/api/msinkaut/ne-msinkaut-inkapplicationgesture)
</dt> <dt>

[<span data-ttu-id="3e1aa-148">**Método SetGestureStatus**</span><span class="sxs-lookup"><span data-stu-id="3e1aa-148">**SetGestureStatus Method**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-setgesturestatus)
</dt> <dt>

[<span data-ttu-id="3e1aa-149">Usando gestos</span><span class="sxs-lookup"><span data-stu-id="3e1aa-149">Using Gestures</span></span>](using-gestures.md)
</dt> </dl>

 

