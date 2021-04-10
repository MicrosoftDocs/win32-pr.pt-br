---
description: Ocorre quando um gesto de aplicativo é reconhecido.
ms.assetid: 736715f4-c610-42cc-9fbb-c2b579da69e5
title: Evento InkEdit. Gesture (Inked. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a61f4fce033672fde8cc4d74dced727fe60b7f97
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104170082"
---
# <a name="inkeditgesture-event"></a><span data-ttu-id="6009e-103">Evento InkEdit. Gesture</span><span class="sxs-lookup"><span data-stu-id="6009e-103">InkEdit.Gesture event</span></span>

<span data-ttu-id="6009e-104">Ocorre quando um gesto de aplicativo é reconhecido.</span><span class="sxs-lookup"><span data-stu-id="6009e-104">Occurs when an application gesture is recognized.</span></span>

## <a name="syntax"></a><span data-ttu-id="6009e-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="6009e-105">Syntax</span></span>


```C++
HRESULT Gesture(
  [in]      IInkCursor   *Cursor,
  [in]      IInkStrokes  *Strokes,
  [in]      VARIANT      Gestures,
  [in, out] VARIANT_BOOL *Cancel
);
```



## <a name="parameters"></a><span data-ttu-id="6009e-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="6009e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6009e-107">*Cursor* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="6009e-107">*Cursor* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6009e-108">O objeto [**IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) que foi usado para criar esse gesto.</span><span class="sxs-lookup"><span data-stu-id="6009e-108">The [**IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) object that was used to create this gesture.</span></span>

</dd> <dt>

<span data-ttu-id="6009e-109">*Traços* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="6009e-109">*Strokes* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6009e-110">A coleção [InkStrokes](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) que contém os objetos [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) que compõem esse gesto.</span><span class="sxs-lookup"><span data-stu-id="6009e-110">The [InkStrokes](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) collection that contains the [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) objects that make up this gesture.</span></span>

</dd> <dt>

<span data-ttu-id="6009e-111">*Gestos* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="6009e-111">*Gestures* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6009e-112">Uma matriz de objetos [**IInkGesture**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkgesture) , em ordem de confiança.</span><span class="sxs-lookup"><span data-stu-id="6009e-112">An array of [**IInkGesture**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkgesture) objects, in order of confidence.</span></span>

<span data-ttu-id="6009e-113">Para obter mais informações sobre a estrutura de VARIAntes, consulte [usando a biblioteca com](using-the-com-library.md).</span><span class="sxs-lookup"><span data-stu-id="6009e-113">For more information about the VARIANT structure, see [Using the COM Library](using-the-com-library.md).</span></span>

</dd> <dt>

<span data-ttu-id="6009e-114">*Cancelar* \[ entrada, saída\]</span><span class="sxs-lookup"><span data-stu-id="6009e-114">*Cancel* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="6009e-115">Se a coleção [InkStrokes](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) que compõe esse gesto deve ser cancelada, para não apagar a tinta e disparar o evento [**Stroke**](inkedit-stroke.md) .</span><span class="sxs-lookup"><span data-stu-id="6009e-115">Whether the [InkStrokes](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) collection that makes up this gesture should be canceled, so as not to erase the ink and to fire the [**Stroke**](inkedit-stroke.md) event.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6009e-116">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="6009e-116">Return value</span></span>

<span data-ttu-id="6009e-117">Se esse evento for bem sucedido, ele retornará **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="6009e-117">If this event succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="6009e-118">Caso contrário, ele retorna um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="6009e-118">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="6009e-119">Comentários</span><span class="sxs-lookup"><span data-stu-id="6009e-119">Remarks</span></span>

<span data-ttu-id="6009e-120">Esse método de evento é definido na interface **\_ IInkEditEvents** .</span><span class="sxs-lookup"><span data-stu-id="6009e-120">This event method is defined in the **\_IInkEditEvents** interface.</span></span> <span data-ttu-id="6009e-121">A interface **\_ IInkEditEvents** implementa a interface IDispatch com um identificador de \_ IeeGesture DISPID.</span><span class="sxs-lookup"><span data-stu-id="6009e-121">The **\_IInkEditEvents** interface implements the IDispatch interface with an identifier of DISPID\_IeeGesture.</span></span>

<span data-ttu-id="6009e-122">Um evento de **gesto** será gerado somente se o [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) para o objeto [**IInkGesture**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkgesture) for o primeiro objeto **IInkStrokeDisp** desde a última chamada para o método [**Recognize**](/windows/desktop/api/inked/nf-inked-iinkedit-recognize) ou o último disparo do tempo limite de reconhecimento.</span><span class="sxs-lookup"><span data-stu-id="6009e-122">A **Gesture** event is raised only if the [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) for the [**IInkGesture**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkgesture) object is the first **IInkStrokeDisp** object since the last call to the [**Recognize**](/windows/desktop/api/inked/nf-inked-iinkedit-recognize) method or the last firing of the recognition timeout.</span></span>

<span data-ttu-id="6009e-123">Se o evento de **gesto** for cancelado, o evento [**Stroke**](inkedit-stroke.md) será gerado para a coleção [InkStrokes](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) que gerou o evento de **gesto** .</span><span class="sxs-lookup"><span data-stu-id="6009e-123">If the **Gesture** event is canceled, the [**Stroke**](inkedit-stroke.md) event is raised for the [InkStrokes](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) collection that raised the **Gesture** event.</span></span>

<span data-ttu-id="6009e-124">Para que esse evento ocorra, o controle [InkEdit](inkedit-control-reference.md) deve assinar um conjunto de gestos de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="6009e-124">For this event to occur, the [InkEdit](inkedit-control-reference.md) control must subscribe to a set of application gestures.</span></span> <span data-ttu-id="6009e-125">Para definir o interesse do controle InkEdit em um conjunto de gestos, chame o método [**SetGestureStatus**](/windows/desktop/api/inked/nf-inked-iinkedit-setgesturestatus) .</span><span class="sxs-lookup"><span data-stu-id="6009e-125">To set the InkEdit control's interest in a set of gestures, call the [**SetGestureStatus**](/windows/desktop/api/inked/nf-inked-iinkedit-setgesturestatus) method.</span></span>

<span data-ttu-id="6009e-126">Para obter uma lista de gestos de aplicativo, consulte o tipo de enumeração [**InkApplicationGesture**](/windows/desktop/api/msinkaut/ne-msinkaut-inkapplicationgesture) .</span><span class="sxs-lookup"><span data-stu-id="6009e-126">For a list of application gestures, see the [**InkApplicationGesture**](/windows/desktop/api/msinkaut/ne-msinkaut-inkapplicationgesture) enumeration type.</span></span>

<span data-ttu-id="6009e-127">O controle [InkEdit](inkedit-control-reference.md) não reconhece vários gestos de traço.</span><span class="sxs-lookup"><span data-stu-id="6009e-127">The [InkEdit](inkedit-control-reference.md) control does not recognize multiple stroke gestures.</span></span>

<span data-ttu-id="6009e-128">O controle [InkEdit](inkedit-control-reference.md) assina os seguintes gestos.</span><span class="sxs-lookup"><span data-stu-id="6009e-128">The [InkEdit](inkedit-control-reference.md) control subscribes to the following gestures.</span></span>



| <span data-ttu-id="6009e-129">Gesto</span><span class="sxs-lookup"><span data-stu-id="6009e-129">Gesture</span></span>                              | <span data-ttu-id="6009e-130">Ação</span><span class="sxs-lookup"><span data-stu-id="6009e-130">Action</span></span>               |
|--------------------------------------|----------------------|
| <span data-ttu-id="6009e-131">Para baixo à esquerda, para baixo-esquerda-longa</span><span class="sxs-lookup"><span data-stu-id="6009e-131">Down-left ,Down-left-long</span></span><br/> | <span data-ttu-id="6009e-132">Digite</span><span class="sxs-lookup"><span data-stu-id="6009e-132">Enter</span></span><br/>     |
| <span data-ttu-id="6009e-133">Direita</span><span class="sxs-lookup"><span data-stu-id="6009e-133">Right</span></span><br/>                     | <span data-ttu-id="6009e-134">Space</span><span class="sxs-lookup"><span data-stu-id="6009e-134">Space</span></span><br/>     |
| <span data-ttu-id="6009e-135">Esquerda</span><span class="sxs-lookup"><span data-stu-id="6009e-135">Left</span></span><br/>                      | <span data-ttu-id="6009e-136">Backspace</span><span class="sxs-lookup"><span data-stu-id="6009e-136">Backspace</span></span><br/> |
| <span data-ttu-id="6009e-137">Para cima à direita, para cima à direita</span><span class="sxs-lookup"><span data-stu-id="6009e-137">Up-right, Up-right-long</span></span><br/>   | <span data-ttu-id="6009e-138">Tab</span><span class="sxs-lookup"><span data-stu-id="6009e-138">Tab</span></span><br/>       |



 

<span data-ttu-id="6009e-139">Para alterar a ação padrão para um gesto:</span><span class="sxs-lookup"><span data-stu-id="6009e-139">To alter the default action for a gesture:</span></span>

1.  <span data-ttu-id="6009e-140">Adicione manipuladores de eventos para os eventos de **gesto** e [**traço**](inkedit-stroke.md) .</span><span class="sxs-lookup"><span data-stu-id="6009e-140">Add event handlers for the **Gesture** and [**Stroke**](inkedit-stroke.md) events.</span></span>
2.  <span data-ttu-id="6009e-141">No manipulador de eventos de **gesto** , cancele o evento de **gesto** para o gesto e execute a ação alternativa para o gesto.</span><span class="sxs-lookup"><span data-stu-id="6009e-141">In the **Gesture** event handler, cancel the **Gesture** event for the gesture, and perform the alternate action for the gesture.</span></span>
3.  <span data-ttu-id="6009e-142">No manipulador de eventos [**Stroke**](inkedit-stroke.md) , cancele o evento **Stroke** para o objeto [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) que gerou o evento de **gesto** cancelado.</span><span class="sxs-lookup"><span data-stu-id="6009e-142">In the [**Stroke**](inkedit-stroke.md) event handler, cancel the **Stroke** event for the [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) object that raised the canceled **Gesture** event.</span></span>

## <a name="requirements"></a><span data-ttu-id="6009e-143">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6009e-143">Requirements</span></span>



| <span data-ttu-id="6009e-144">Requisito</span><span class="sxs-lookup"><span data-stu-id="6009e-144">Requirement</span></span> | <span data-ttu-id="6009e-145">Valor</span><span class="sxs-lookup"><span data-stu-id="6009e-145">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6009e-146">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6009e-146">Minimum supported client</span></span><br/> | <span data-ttu-id="6009e-147">Somente aplicativos de área de trabalho do Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="6009e-147">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="6009e-148">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6009e-148">Minimum supported server</span></span><br/> | <span data-ttu-id="6009e-149">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="6009e-149">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="6009e-150">parâmetro</span><span class="sxs-lookup"><span data-stu-id="6009e-150">Header</span></span><br/>                   | <dl> <span data-ttu-id="6009e-151"><dt>Inked. h (também requer Inked \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="6009e-151"><dt>Inked.h (also requires inked\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="6009e-152">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="6009e-152">Library</span></span><br/>                  | <dl> <span data-ttu-id="6009e-153"><dt>InkEd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6009e-153"><dt>InkEd.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="6009e-154">Confira também</span><span class="sxs-lookup"><span data-stu-id="6009e-154">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6009e-155">InkEdit</span><span class="sxs-lookup"><span data-stu-id="6009e-155">InkEdit</span></span>](inkedit-control-reference.md)
</dt> <dt>

[<span data-ttu-id="6009e-156">**Enumeração InkApplicationGesture**</span><span class="sxs-lookup"><span data-stu-id="6009e-156">**InkApplicationGesture Enumeration**</span></span>](/windows/desktop/api/msinkaut/ne-msinkaut-inkapplicationgesture)
</dt> <dt>

<span data-ttu-id="6009e-157">[**Controle InkEdit do método SetGestureStatus \[\]**](/windows/desktop/api/inked/nf-inked-iinkedit-setgesturestatus)</span><span class="sxs-lookup"><span data-stu-id="6009e-157">[**SetGestureStatus Method \[InkEdit Control\]**](/windows/desktop/api/inked/nf-inked-iinkedit-setgesturestatus)</span></span>
</dt> <dt>

[<span data-ttu-id="6009e-158">**Propriedade RecoTimeout**</span><span class="sxs-lookup"><span data-stu-id="6009e-158">**RecoTimeout Property**</span></span>](/windows/desktop/api/inked/nf-inked-iinkedit-get_recognitiontimeout)
</dt> <dt>

<span data-ttu-id="6009e-159">[**Controle de evento InkEdit de Stroke \[\]**](inkedit-stroke.md)</span><span class="sxs-lookup"><span data-stu-id="6009e-159">[**Stroke Event \[InkEdit Control\]**](inkedit-stroke.md)</span></span>
</dt> <dt>

[<span data-ttu-id="6009e-160">Usando gestos</span><span class="sxs-lookup"><span data-stu-id="6009e-160">Using Gestures</span></span>](using-gestures.md)
</dt> </dl>

 

