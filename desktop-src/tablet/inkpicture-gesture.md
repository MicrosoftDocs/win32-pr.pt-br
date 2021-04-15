---
description: Ocorre quando um gesto específico do aplicativo é reconhecido.
ms.assetid: a20f2d78-6cfe-4755-968e-91369021db1b
title: Evento InkPicture. Gesture (Msinkaut. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 94581369554b4aef16530c9ddc8b3fd1a31ad861
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105761249"
---
# <a name="inkpicturegesture-event"></a><span data-ttu-id="331fb-103">Evento InkPicture. Gesture</span><span class="sxs-lookup"><span data-stu-id="331fb-103">InkPicture.Gesture event</span></span>

<span data-ttu-id="331fb-104">Ocorre quando um *gesto* específico do aplicativo é reconhecido.</span><span class="sxs-lookup"><span data-stu-id="331fb-104">Occurs when an application-specific *gesture* is recognized.</span></span>

## <a name="syntax"></a><span data-ttu-id="331fb-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="331fb-105">Syntax</span></span>


```C++
void Gesture(
  [in]      IInkCursor   *Cursor,
  [in]      IInkStrokes  *Strokes,
  [in]      VARIANT      Gestures,
  [in, out] VARIANT_BOOL *Cancel
);
```



## <a name="parameters"></a><span data-ttu-id="331fb-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="331fb-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="331fb-107">*Cursor* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="331fb-107">*Cursor* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="331fb-108">O objeto [**IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) que gerou o evento de **gesto** .</span><span class="sxs-lookup"><span data-stu-id="331fb-108">The [**IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) object that generated the **Gesture** event.</span></span>

</dd> <dt>

<span data-ttu-id="331fb-109">*Traços* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="331fb-109">*Strokes* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="331fb-110">A coleção [IInkStrokes](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) que o reconhecedor retornou como gesto.</span><span class="sxs-lookup"><span data-stu-id="331fb-110">The [IInkStrokes](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) collection that the recognizer returned as the gesture.</span></span>

</dd> <dt>

<span data-ttu-id="331fb-111">*Gestos* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="331fb-111">*Gestures* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="331fb-112">Uma matriz de objetos [**IInkGesture**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkgesture) , em ordem de confiança, do reconhecedor.</span><span class="sxs-lookup"><span data-stu-id="331fb-112">An array of [**IInkGesture**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkgesture) objects, in order of confidence, from the recognizer.</span></span>

<span data-ttu-id="331fb-113">Para obter mais informações sobre a estrutura de VARIAntes, consulte [usando a biblioteca com](using-the-com-library.md).</span><span class="sxs-lookup"><span data-stu-id="331fb-113">For more information about the VARIANT structure, see [Using the COM Library](using-the-com-library.md).</span></span>

</dd> <dt>

<span data-ttu-id="331fb-114">*Cancelar* \[ entrada, saída\]</span><span class="sxs-lookup"><span data-stu-id="331fb-114">*Cancel* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="331fb-115">**Variante \_ TRUE** se esse evento deve ser cancelado, como não apagar a tinta e disparar o evento [**Stroke**](inkpicture-stroke.md) .</span><span class="sxs-lookup"><span data-stu-id="331fb-115">**VARIANT\_TRUE** if this event should be cancelled, such as not to erase the ink and to fire the [**Stroke**](inkpicture-stroke.md) event.</span></span> <span data-ttu-id="331fb-116">Caso contrário, **Variant \_ false**.</span><span class="sxs-lookup"><span data-stu-id="331fb-116">Otherwise, **VARIANT\_FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="331fb-117">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="331fb-117">Return value</span></span>

<span data-ttu-id="331fb-118">Esse evento não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="331fb-118">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="331fb-119">Comentários</span><span class="sxs-lookup"><span data-stu-id="331fb-119">Remarks</span></span>

<span data-ttu-id="331fb-120">Esse método de evento é definido nas interfaces somente de expedição **\_ IInkCollectorEvents**, **\_ IInkOverlayEvents** e **\_ IInkPictureEvents** (dispinterfaces) com uma ID de ICEGesture de DISPID \_ .</span><span class="sxs-lookup"><span data-stu-id="331fb-120">This event method is defined in the **\_IInkCollectorEvents**, **\_IInkOverlayEvents**, and **\_IInkPictureEvents** dispatch-only interfaces (dispinterfaces) with an ID of DISPID\_ICEGesture.</span></span>

<span data-ttu-id="331fb-121">Quando a propriedade [**CollectionMode**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_collectionmode) é definida como [**GestureOnly**](/windows/desktop/api/msinkaut/ne-msinkaut-inkcollectionmode), o tempo limite entre quando um usuário adiciona um gesto e quando o evento de **gesto** ocorre é um valor fixo que você não pode alterar programaticamente.</span><span class="sxs-lookup"><span data-stu-id="331fb-121">When the [**CollectionMode**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_collectionmode) property is set to [**GestureOnly**](/windows/desktop/api/msinkaut/ne-msinkaut-inkcollectionmode), the timeout between when a user adds a gesture and when the **Gesture** event occurs is a fixed value that you cannot alter programmatically.</span></span> <span data-ttu-id="331fb-122">O reconhecimento de gestos é mais rápido no modo **InkAndGesture** .</span><span class="sxs-lookup"><span data-stu-id="331fb-122">Gesture recognition is faster in **InkAndGesture** mode.</span></span>

<span data-ttu-id="331fb-123">Para evitar a coleta de tinta no modo [**InkAndGesture**](/windows/desktop/api/msinkaut/ne-msinkaut-inkcollectionmode) :</span><span class="sxs-lookup"><span data-stu-id="331fb-123">To prevent the collection of ink while in [**InkAndGesture**](/windows/desktop/api/msinkaut/ne-msinkaut-inkcollectionmode) mode:</span></span>

-   <span data-ttu-id="331fb-124">Defina [**CollectionMode**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_collectionmode) como [**InkAndGesture**](/windows/desktop/api/msinkaut/ne-msinkaut-inkcollectionmode).</span><span class="sxs-lookup"><span data-stu-id="331fb-124">Set [**CollectionMode**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_collectionmode) to [**InkAndGesture**](/windows/desktop/api/msinkaut/ne-msinkaut-inkcollectionmode).</span></span>
-   <span data-ttu-id="331fb-125">Exclua o traço no evento de [**traço**](inkpicture-stroke.md) .</span><span class="sxs-lookup"><span data-stu-id="331fb-125">Delete the stroke in the [**Stroke**](inkpicture-stroke.md) event.</span></span>
-   <span data-ttu-id="331fb-126">Processe o gesto no evento de **gesto** .</span><span class="sxs-lookup"><span data-stu-id="331fb-126">Process the gesture in the **Gesture** event.</span></span>

<span data-ttu-id="331fb-127">Para evitar o fluxo de tinta enquanto gesturing, defina a propriedade [**DynamicRendering**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_dynamicrendering) como **false**.</span><span class="sxs-lookup"><span data-stu-id="331fb-127">To prevent the flow of ink while gesturing, set [**DynamicRendering**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_dynamicrendering) property to **FALSE**.</span></span>

<span data-ttu-id="331fb-128">Além de ao inserir tinta, o evento de **gesto** é acionado no modo de seleção ou apagamento.</span><span class="sxs-lookup"><span data-stu-id="331fb-128">In addition to when inserting ink, the **Gesture** event is fired when in select or erase mode.</span></span> <span data-ttu-id="331fb-129">Você é responsável por controlar o modo de edição e deve estar ciente do modo antes de interpretar o evento.</span><span class="sxs-lookup"><span data-stu-id="331fb-129">You are responsible for tracking the editing mode and should be aware of the mode before interpreting the event.</span></span>

> [!Note]  
> <span data-ttu-id="331fb-130">Para reconhecer gestos, você deve usar um objeto ou controle que possa coletar tinta.</span><span class="sxs-lookup"><span data-stu-id="331fb-130">To recognize gestures, you must use an object or control that can collect ink.</span></span>

 

<span data-ttu-id="331fb-131">Os gestos de aplicativo são definidos como gestos com suporte no seu aplicativo.</span><span class="sxs-lookup"><span data-stu-id="331fb-131">Application gestures are defined as gestures that are supported within your application.</span></span>

<span data-ttu-id="331fb-132">Para que esse evento ocorra, o objeto ou controle deve ter interesse em um conjunto de gestos de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="331fb-132">For this event to occur, the object or control must have interest in a set of application gestures.</span></span> <span data-ttu-id="331fb-133">Para definir os objetos ou controles de interesse em um conjunto de gestos, chame o método [**SetGestureStatus**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-setgesturestatus) do objeto ou controle.</span><span class="sxs-lookup"><span data-stu-id="331fb-133">To set the objects or controls interest in a set of gestures, call the [**SetGestureStatus**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-setgesturestatus) method of the object or control.</span></span>

<span data-ttu-id="331fb-134">Para obter uma lista de gestos de aplicativo específicos, consulte o tipo de enumeração [**InkApplicationGesture**](/windows/desktop/api/msinkaut/ne-msinkaut-inkapplicationgesture) .</span><span class="sxs-lookup"><span data-stu-id="331fb-134">For a list of specific application gestures, see the [**InkApplicationGesture**](/windows/desktop/api/msinkaut/ne-msinkaut-inkapplicationgesture) enumeration type.</span></span>

## <a name="requirements"></a><span data-ttu-id="331fb-135">Requisitos</span><span class="sxs-lookup"><span data-stu-id="331fb-135">Requirements</span></span>



| <span data-ttu-id="331fb-136">Requisito</span><span class="sxs-lookup"><span data-stu-id="331fb-136">Requirement</span></span> | <span data-ttu-id="331fb-137">Valor</span><span class="sxs-lookup"><span data-stu-id="331fb-137">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="331fb-138">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="331fb-138">Minimum supported client</span></span><br/> | <span data-ttu-id="331fb-139">Somente aplicativos de área de trabalho do Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="331fb-139">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="331fb-140">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="331fb-140">Minimum supported server</span></span><br/> | <span data-ttu-id="331fb-141">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="331fb-141">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="331fb-142">parâmetro</span><span class="sxs-lookup"><span data-stu-id="331fb-142">Header</span></span><br/>                   | <dl> <span data-ttu-id="331fb-143"><dt>Msinkaut. h (também requer Msinkaut \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="331fb-143"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="331fb-144">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="331fb-144">Library</span></span><br/>                  | <dl> <span data-ttu-id="331fb-145"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="331fb-145"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="331fb-146">Confira também</span><span class="sxs-lookup"><span data-stu-id="331fb-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="331fb-147">InkPicture</span><span class="sxs-lookup"><span data-stu-id="331fb-147">InkPicture</span></span>](inkpicture-control-reference.md)
</dt> <dt>

[<span data-ttu-id="331fb-148">**Enumeração InkApplicationGesture**</span><span class="sxs-lookup"><span data-stu-id="331fb-148">**InkApplicationGesture Enumeration**</span></span>](/windows/desktop/api/msinkaut/ne-msinkaut-inkapplicationgesture)
</dt> <dt>

[<span data-ttu-id="331fb-149">**Método SetGestureStatus**</span><span class="sxs-lookup"><span data-stu-id="331fb-149">**SetGestureStatus Method**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-setgesturestatus)
</dt> <dt>

[<span data-ttu-id="331fb-150">Usando gestos</span><span class="sxs-lookup"><span data-stu-id="331fb-150">Using Gestures</span></span>](using-gestures.md)
</dt> </dl>

 

