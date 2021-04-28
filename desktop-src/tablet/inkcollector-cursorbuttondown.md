---
description: Evento InkCollector. CursorButtonDown – ocorre quando a classe InkCollector detecta um botão de cursor que está inoperante.
ms.assetid: 65e7f68b-f911-4634-b850-178eb6eaf86e
title: Evento InkCollector. CursorButtonDown (Msinkaut. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bd1a820445a1ba3ed07dad8a22a11ad86e8da96f
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108110324"
---
# <a name="inkcollectorcursorbuttondown-event"></a><span data-ttu-id="b0a3d-103">Evento InkCollector. CursorButtonDown</span><span class="sxs-lookup"><span data-stu-id="b0a3d-103">InkCollector.CursorButtonDown event</span></span>

<span data-ttu-id="b0a3d-104">Ocorre quando a [**classe InkCollector**](inkcollector-class.md) detecta um botão de cursor que está inoperante.</span><span class="sxs-lookup"><span data-stu-id="b0a3d-104">Occurs when the [**InkCollector Class**](inkcollector-class.md) detects a cursor button that is down.</span></span>

## <a name="syntax"></a><span data-ttu-id="b0a3d-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="b0a3d-105">Syntax</span></span>


```C++
void CursorButtonDown(
  [in] IInkCursor       *Cursor,
  [in] IInkCursorButton *Button
);
```



## <a name="parameters"></a><span data-ttu-id="b0a3d-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="b0a3d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b0a3d-107">*Cursor* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="b0a3d-107">*Cursor* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b0a3d-108">O objeto [**IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) que gerou o evento **CursorButtonDown** .</span><span class="sxs-lookup"><span data-stu-id="b0a3d-108">The [**IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) object that generated the **CursorButtonDown** event.</span></span>

</dd> <dt>

<span data-ttu-id="b0a3d-109">*Botão* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="b0a3d-109">*Button* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b0a3d-110">O botão que foi pressionado.</span><span class="sxs-lookup"><span data-stu-id="b0a3d-110">The button that was pressed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b0a3d-111">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="b0a3d-111">Return value</span></span>

<span data-ttu-id="b0a3d-112">Esse evento não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="b0a3d-112">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="b0a3d-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="b0a3d-113">Remarks</span></span>

<span data-ttu-id="b0a3d-114">Um botão em uma dica de caneta fica inoperante quando o usuário abaixa a caneta para o digitalizador e começa a rastrear um traço.</span><span class="sxs-lookup"><span data-stu-id="b0a3d-114">A button on a pen tip is down when the user lowers the pen to the digitizer and starts tracing a stroke.</span></span> <span data-ttu-id="b0a3d-115">Um botão em um cilindro fica inativo quando o botão é pressionado.</span><span class="sxs-lookup"><span data-stu-id="b0a3d-115">A button on a barrel is down when the button is pressed.</span></span>

<span data-ttu-id="b0a3d-116">Quando você pressiona o botão direito do mouse, você realmente recebe dois eventos **CursorButtonDown** – um para o botão direito pressionado e outro para o botão esquerdo pressionado.</span><span class="sxs-lookup"><span data-stu-id="b0a3d-116">When you press the right mouse button, you actually receive two **CursorButtonDown** events - one for right button pressed and one for left button pressed.</span></span>

<span data-ttu-id="b0a3d-117">Esse método de evento é definido nas \_ \_ interfaces somente de expedição IInkCollectorEvents, IInkOverlayEvents e \_ IInkPictureEvents (dispinterfaces) com uma ID de ICECursorButtonDown de DISPID \_ .</span><span class="sxs-lookup"><span data-stu-id="b0a3d-117">This event method is defined in the \_IInkCollectorEvents, \_IInkOverlayEvents, and \_IInkPictureEvents dispatch-only interfaces (dispinterfaces) with an ID of DISPID\_ICECursorButtonDown.</span></span>

## <a name="requirements"></a><span data-ttu-id="b0a3d-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b0a3d-118">Requirements</span></span>



| <span data-ttu-id="b0a3d-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="b0a3d-119">Requirement</span></span> | <span data-ttu-id="b0a3d-120">Valor</span><span class="sxs-lookup"><span data-stu-id="b0a3d-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b0a3d-121">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b0a3d-121">Minimum supported client</span></span><br/> | <span data-ttu-id="b0a3d-122">Somente aplicativos de área de trabalho do Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="b0a3d-122">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="b0a3d-123">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b0a3d-123">Minimum supported server</span></span><br/> | <span data-ttu-id="b0a3d-124">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="b0a3d-124">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="b0a3d-125">parâmetro</span><span class="sxs-lookup"><span data-stu-id="b0a3d-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="b0a3d-126"><dt>Msinkaut. h (também requer Msinkaut \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="b0a3d-126"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="b0a3d-127">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="b0a3d-127">Library</span></span><br/>                  | <dl> <span data-ttu-id="b0a3d-128"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b0a3d-128"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="b0a3d-129">Consulte também</span><span class="sxs-lookup"><span data-stu-id="b0a3d-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b0a3d-130">**Classe InkCollector**</span><span class="sxs-lookup"><span data-stu-id="b0a3d-130">**InkCollector Class**</span></span>](inkcollector-class.md)
</dt> <dt>

[<span data-ttu-id="b0a3d-131">**Evento CursorDown**</span><span class="sxs-lookup"><span data-stu-id="b0a3d-131">**CursorDown Event**</span></span>](inkcollector-cursordown.md)
</dt> <dt>

[<span data-ttu-id="b0a3d-132">**Evento CursorButtonUp**</span><span class="sxs-lookup"><span data-stu-id="b0a3d-132">**CursorButtonUp Event**</span></span>](inkcollector-cursorbuttonup.md)
</dt> <dt>

[<span data-ttu-id="b0a3d-133">**Interface IInkCursor**</span><span class="sxs-lookup"><span data-stu-id="b0a3d-133">**IInkCursor Interface**</span></span>](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor)
</dt> <dt>

[<span data-ttu-id="b0a3d-134">**Interface IInkCursorButton**</span><span class="sxs-lookup"><span data-stu-id="b0a3d-134">**IInkCursorButton Interface**</span></span>](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursorbutton)
</dt> </dl>

 

 




