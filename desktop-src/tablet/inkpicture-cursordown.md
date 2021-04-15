---
description: Ocorre quando a dica de cursor entra na superfície do Tablet de digitalização.
ms.assetid: 6d524400-1341-45da-86b2-098e34ed5a1c
title: Evento InkPicture. CursorDown (Msinkaut. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 15724f0a71e801393ca8e93100ba2105da9ff2b7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104506142"
---
# <a name="inkpicturecursordown-event"></a><span data-ttu-id="1811b-103">Evento InkPicture. CursorDown</span><span class="sxs-lookup"><span data-stu-id="1811b-103">InkPicture.CursorDown event</span></span>

<span data-ttu-id="1811b-104">Ocorre quando a dica de cursor entra na superfície do Tablet de digitalização.</span><span class="sxs-lookup"><span data-stu-id="1811b-104">Occurs when the cursor tip contacts the digitizing tablet surface.</span></span>

## <a name="syntax"></a><span data-ttu-id="1811b-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="1811b-105">Syntax</span></span>


```C++
void CursorDown(
  [in] IInkCursor     *Cursor,
  [in] IInkStrokeDisp *Stroke
);
```



## <a name="parameters"></a><span data-ttu-id="1811b-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="1811b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1811b-107">*Cursor* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="1811b-107">*Cursor* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1811b-108">O objeto [**IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) que gerou o evento **CursorDown** .</span><span class="sxs-lookup"><span data-stu-id="1811b-108">The [**IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) object that generated the **CursorDown** event.</span></span>

</dd> <dt>

<span data-ttu-id="1811b-109">*Traço* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="1811b-109">*Stroke* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1811b-110">O objeto [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) que foi iniciado quando o objeto [**IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) fez com que o evento **CursorDown** fosse disparado.</span><span class="sxs-lookup"><span data-stu-id="1811b-110">The [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) object that was started when the [**IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) object caused the **CursorDown** event to fire.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1811b-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="1811b-111">Return value</span></span>

<span data-ttu-id="1811b-112">Esse evento não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="1811b-112">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="1811b-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="1811b-113">Remarks</span></span>

<span data-ttu-id="1811b-114">Esses métodos de evento são definidos nas interfaces **\_ IInkCollectorEvents**, **\_ IInkOverlayEvents** e **\_ IInkPictureEvents** .</span><span class="sxs-lookup"><span data-stu-id="1811b-114">These event methods are defined in the **\_IInkCollectorEvents**, **\_IInkOverlayEvents**, and **\_IInkPictureEvents** interfaces.</span></span> <span data-ttu-id="1811b-115">As interfaces **\_ IInkCollectorEvents**, **\_ IInkOverlayEvents** e **\_ IInkPictureEvents** implementam a interface [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) com um identificador de \_ ICECursorDown DISPID.</span><span class="sxs-lookup"><span data-stu-id="1811b-115">The **\_IInkCollectorEvents**, **\_IInkOverlayEvents**, and **\_IInkPictureEvents** interfaces implements the [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interface with an identifier of DISPID\_ICECursorDown.</span></span>

<span data-ttu-id="1811b-116">Use esse evento com cuidado porque ele pode ter um efeito adverso no desempenho da tinta se um código excessivo for executado nos manipuladores de eventos.</span><span class="sxs-lookup"><span data-stu-id="1811b-116">Use this event carefully because it could have an adverse effect on ink performance if too much code is executed in the event handlers.</span></span> <span data-ttu-id="1811b-117">Para melhorar o desempenho de tinta em tempo real, oculte ou mostre o cursor do mouse nos manipuladores de eventos [**MouseDown**](inkpicture-mousedown.md) e [**MouseUp**](inkpicture-mouseup.md) .</span><span class="sxs-lookup"><span data-stu-id="1811b-117">To improve real-time ink performance, hide or show the mouse cursor in the [**MouseDown**](inkpicture-mousedown.md) and [**MouseUp**](inkpicture-mouseup.md) event handlers.</span></span>

## <a name="requirements"></a><span data-ttu-id="1811b-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1811b-118">Requirements</span></span>



| <span data-ttu-id="1811b-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="1811b-119">Requirement</span></span> | <span data-ttu-id="1811b-120">Valor</span><span class="sxs-lookup"><span data-stu-id="1811b-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1811b-121">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="1811b-121">Minimum supported client</span></span><br/> | <span data-ttu-id="1811b-122">Somente aplicativos de área de trabalho do Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="1811b-122">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="1811b-123">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="1811b-123">Minimum supported server</span></span><br/> | <span data-ttu-id="1811b-124">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="1811b-124">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="1811b-125">parâmetro</span><span class="sxs-lookup"><span data-stu-id="1811b-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="1811b-126"><dt>Msinkaut. h (também requer Msinkaut \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="1811b-126"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="1811b-127">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="1811b-127">Library</span></span><br/>                  | <dl> <span data-ttu-id="1811b-128"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1811b-128"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="1811b-129">Confira também</span><span class="sxs-lookup"><span data-stu-id="1811b-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1811b-130">InkPicture</span><span class="sxs-lookup"><span data-stu-id="1811b-130">InkPicture</span></span>](inkpicture-control-reference.md)
</dt> <dt>

[<span data-ttu-id="1811b-131">**Evento CursorButtonUp**</span><span class="sxs-lookup"><span data-stu-id="1811b-131">**CursorButtonUp Event**</span></span>](inkpicture-cursorbuttonup.md)
</dt> <dt>

[<span data-ttu-id="1811b-132">**Evento CursorButtonDown**</span><span class="sxs-lookup"><span data-stu-id="1811b-132">**CursorButtonDown Event**</span></span>](inkpicture-cursorbuttondown.md)
</dt> <dt>

[<span data-ttu-id="1811b-133">**Interface IInkCursor**</span><span class="sxs-lookup"><span data-stu-id="1811b-133">**IInkCursor Interface**</span></span>](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor)
</dt> <dt>

[<span data-ttu-id="1811b-134">**Interface IInkStrokeDisp**</span><span class="sxs-lookup"><span data-stu-id="1811b-134">**IInkStrokeDisp Interface**</span></span>](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp)
</dt> </dl>

 

