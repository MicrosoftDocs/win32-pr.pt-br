---
description: Ocorre quando o InkCollector detecta um botão de cursor que está ativo.
ms.assetid: f07daad7-e0d1-45cf-a708-5486a5dfda8b
title: Evento InkCollector. CursorButtonUp (Msinkaut. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 932d768c13da953d1926b28fb651c63dc26be572
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105797655"
---
# <a name="inkcollectorcursorbuttonup-event"></a><span data-ttu-id="7990d-103">Evento InkCollector. CursorButtonUp</span><span class="sxs-lookup"><span data-stu-id="7990d-103">InkCollector.CursorButtonUp event</span></span>

<span data-ttu-id="7990d-104">Ocorre quando o [**InkCollector**](inkcollector-class.md) detecta um botão de cursor que está ativo.</span><span class="sxs-lookup"><span data-stu-id="7990d-104">Occurs when the [**InkCollector**](inkcollector-class.md) detects a cursor button that is up.</span></span>

## <a name="syntax"></a><span data-ttu-id="7990d-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="7990d-105">Syntax</span></span>


```C++
void CursorButtonUp(
  [in] IInkCursor       *Cursor,
  [in] IInkCursorButton *Button
);
```



## <a name="parameters"></a><span data-ttu-id="7990d-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="7990d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7990d-107">*Cursor* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="7990d-107">*Cursor* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7990d-108">O objeto da [**interface IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) que gerou o evento **CursorButtonUp** .</span><span class="sxs-lookup"><span data-stu-id="7990d-108">The [**IInkCursor Interface**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) object that generated the **CursorButtonUp** event.</span></span>

</dd> <dt>

<span data-ttu-id="7990d-109">*Botão* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="7990d-109">*Button* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7990d-110">O botão que foi lançado.</span><span class="sxs-lookup"><span data-stu-id="7990d-110">The button that was released.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7990d-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="7990d-111">Return value</span></span>

<span data-ttu-id="7990d-112">Esse evento não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="7990d-112">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="7990d-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="7990d-113">Remarks</span></span>

<span data-ttu-id="7990d-114">Um botão em uma dica de caneta fica ativo quando o usuário conclui um traço e levanta a caneta do digitalizador.</span><span class="sxs-lookup"><span data-stu-id="7990d-114">A button on a pen tip is up when the user completes a stroke and lifts the pen from the digitizer.</span></span> <span data-ttu-id="7990d-115">Um botão em um cilindro fica ativo quando o botão não é pressionado.</span><span class="sxs-lookup"><span data-stu-id="7990d-115">A button on a barrel is up when the button is not pressed.</span></span>

<span data-ttu-id="7990d-116">Ao liberar o botão direito do mouse, você realmente recebe dois eventos **CursorButtonUp** -um para o botão direito e outro para o botão esquerdo para cima.</span><span class="sxs-lookup"><span data-stu-id="7990d-116">When you release the right mouse button, you actually receive two **CursorButtonUp** events - one for right button up and one for left button up.</span></span>

<span data-ttu-id="7990d-117">Esse método de evento é definido nas \_ \_ interfaces somente de expedição IInkCollectorEvents, IInkOverlayEvents e \_ IInkPictureEvents (dispinterfaces) com uma ID de ICECursorButtonUp de DISPID \_ .</span><span class="sxs-lookup"><span data-stu-id="7990d-117">This event method is defined in the \_IInkCollectorEvents, \_IInkOverlayEvents, and \_IInkPictureEvents dispatch-only interfaces (dispinterfaces) with an ID of DISPID\_ICECursorButtonUp.</span></span>

## <a name="requirements"></a><span data-ttu-id="7990d-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7990d-118">Requirements</span></span>



| <span data-ttu-id="7990d-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="7990d-119">Requirement</span></span> | <span data-ttu-id="7990d-120">Valor</span><span class="sxs-lookup"><span data-stu-id="7990d-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7990d-121">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="7990d-121">Minimum supported client</span></span><br/> | <span data-ttu-id="7990d-122">Somente aplicativos de área de trabalho do Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="7990d-122">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="7990d-123">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="7990d-123">Minimum supported server</span></span><br/> | <span data-ttu-id="7990d-124">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="7990d-124">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="7990d-125">parâmetro</span><span class="sxs-lookup"><span data-stu-id="7990d-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="7990d-126"><dt>Msinkaut. h (também requer Msinkaut \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="7990d-126"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="7990d-127">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="7990d-127">Library</span></span><br/>                  | <dl> <span data-ttu-id="7990d-128"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7990d-128"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="7990d-129">Confira também</span><span class="sxs-lookup"><span data-stu-id="7990d-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7990d-130">**Classe InkCollector**</span><span class="sxs-lookup"><span data-stu-id="7990d-130">**InkCollector Class**</span></span>](inkcollector-class.md)
</dt> <dt>

[<span data-ttu-id="7990d-131">**Evento CursorButtonDown**</span><span class="sxs-lookup"><span data-stu-id="7990d-131">**CursorButtonDown Event**</span></span>](inkcollector-cursorbuttondown.md)
</dt> <dt>

[<span data-ttu-id="7990d-132">**Evento CursorDown**</span><span class="sxs-lookup"><span data-stu-id="7990d-132">**CursorDown Event**</span></span>](inkcollector-cursordown.md)
</dt> <dt>

[<span data-ttu-id="7990d-133">**Interface IInkCursor**</span><span class="sxs-lookup"><span data-stu-id="7990d-133">**IInkCursor Interface**</span></span>](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor)
</dt> <dt>

[<span data-ttu-id="7990d-134">**Interface IInkCursorButton**</span><span class="sxs-lookup"><span data-stu-id="7990d-134">**IInkCursorButton Interface**</span></span>](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursorbutton)
</dt> </dl>

 

 




