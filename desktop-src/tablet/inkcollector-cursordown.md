---
description: Evento InkCollector. CursorDown – ocorre quando a dica de cursor entra em contato com a superfície do Tablet de digitalização.
ms.assetid: bf914849-ef33-4746-b2e1-c768cd1d87aa
title: Evento InkCollector. CursorDown (Msinkaut. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: da0cdb729f36706202fad2c6c03ab8031e90c845
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108110294"
---
# <a name="inkcollectorcursordown-event"></a><span data-ttu-id="a6a53-103">Evento InkCollector. CursorDown</span><span class="sxs-lookup"><span data-stu-id="a6a53-103">InkCollector.CursorDown event</span></span>

<span data-ttu-id="a6a53-104">Ocorre quando a dica de cursor entra na superfície do Tablet de digitalização.</span><span class="sxs-lookup"><span data-stu-id="a6a53-104">Occurs when the cursor tip contacts the digitizing tablet surface.</span></span>

## <a name="syntax"></a><span data-ttu-id="a6a53-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="a6a53-105">Syntax</span></span>


```C++
void CursorDown(
  [in] IInkCursor     *Cursor,
  [in] IInkStrokeDisp *Stroke
);
```



## <a name="parameters"></a><span data-ttu-id="a6a53-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="a6a53-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a6a53-107">*Cursor* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="a6a53-107">*Cursor* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a6a53-108">O objeto [**IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) que gerou o evento **CursorDown** .</span><span class="sxs-lookup"><span data-stu-id="a6a53-108">The [**IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) object that generated the **CursorDown** event.</span></span>

</dd> <dt>

<span data-ttu-id="a6a53-109">*Traço* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="a6a53-109">*Stroke* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a6a53-110">O objeto [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) que foi iniciado quando o objeto [**IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) fez com que o evento **CursorDown** fosse disparado.</span><span class="sxs-lookup"><span data-stu-id="a6a53-110">The [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) object that was started when the [**IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) object caused the **CursorDown** event to fire.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a6a53-111">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="a6a53-111">Return value</span></span>

<span data-ttu-id="a6a53-112">Esse evento não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="a6a53-112">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="a6a53-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="a6a53-113">Remarks</span></span>

<span data-ttu-id="a6a53-114">Esse método de evento é definido em \_ IInkCollectorEvents, \_ IInkOverlayEvents e \_ IInkPictureEvents.</span><span class="sxs-lookup"><span data-stu-id="a6a53-114">This event method is defined in the \_IInkCollectorEvents, \_IInkOverlayEvents, and \_IInkPictureEvents.</span></span> <span data-ttu-id="a6a53-115">as \_ interfaces IInkCollectorEvents, \_ IInkOverlayEvents e \_ IInkPictureEvents implementam a interface [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) com um identificador de ICECursorDown DISPID \_ .</span><span class="sxs-lookup"><span data-stu-id="a6a53-115">the \_IInkCollectorEvents, \_IInkOverlayEvents, and \_IInkPictureEvents interfaces implements the [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interface with an identifier of DISPID\_ICECursorDown.</span></span>

<span data-ttu-id="a6a53-116">Use esse evento com cuidado porque ele pode ter um efeito adverso no desempenho da tinta se um código excessivo for executado nos manipuladores de eventos.</span><span class="sxs-lookup"><span data-stu-id="a6a53-116">Use this event carefully because it could have an adverse effect on ink performance if too much code is executed in the event handlers.</span></span> <span data-ttu-id="a6a53-117">Para melhorar o desempenho de tinta em tempo real, oculte ou mostre o cursor do mouse nos manipuladores de eventos [**MouseDown**](inkcollector-mousedown.md) e [**MouseUp**](inkcollector-mouseup.md) .</span><span class="sxs-lookup"><span data-stu-id="a6a53-117">To improve real-time ink performance, hide or show the mouse cursor in the [**MouseDown**](inkcollector-mousedown.md) and [**MouseUp**](inkcollector-mouseup.md) event handlers.</span></span>

## <a name="requirements"></a><span data-ttu-id="a6a53-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a6a53-118">Requirements</span></span>



| <span data-ttu-id="a6a53-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="a6a53-119">Requirement</span></span> | <span data-ttu-id="a6a53-120">Valor</span><span class="sxs-lookup"><span data-stu-id="a6a53-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a6a53-121">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a6a53-121">Minimum supported client</span></span><br/> | <span data-ttu-id="a6a53-122">Somente aplicativos de área de trabalho do Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="a6a53-122">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="a6a53-123">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a6a53-123">Minimum supported server</span></span><br/> | <span data-ttu-id="a6a53-124">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="a6a53-124">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="a6a53-125">parâmetro</span><span class="sxs-lookup"><span data-stu-id="a6a53-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="a6a53-126"><dt>Msinkaut. h (também requer Msinkaut \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="a6a53-126"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="a6a53-127">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="a6a53-127">Library</span></span><br/>                  | <dl> <span data-ttu-id="a6a53-128"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a6a53-128"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="a6a53-129">Consulte também</span><span class="sxs-lookup"><span data-stu-id="a6a53-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a6a53-130">**Classe InkCollector**</span><span class="sxs-lookup"><span data-stu-id="a6a53-130">**InkCollector Class**</span></span>](inkcollector-class.md)
</dt> <dt>

[<span data-ttu-id="a6a53-131">**Evento CursorButtonDown**</span><span class="sxs-lookup"><span data-stu-id="a6a53-131">**CursorButtonDown Event**</span></span>](inkcollector-cursorbuttondown.md)
</dt> <dt>

[<span data-ttu-id="a6a53-132">**Evento CursorButtonUp**</span><span class="sxs-lookup"><span data-stu-id="a6a53-132">**CursorButtonUp Event**</span></span>](inkcollector-cursorbuttonup.md)
</dt> <dt>

[<span data-ttu-id="a6a53-133">**Interface IInkCursor**</span><span class="sxs-lookup"><span data-stu-id="a6a53-133">**IInkCursor Interface**</span></span>](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor)
</dt> <dt>

[<span data-ttu-id="a6a53-134">**Interface IInkStrokeDisp**</span><span class="sxs-lookup"><span data-stu-id="a6a53-134">**IInkStrokeDisp Interface**</span></span>](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp)
</dt> </dl>

 

