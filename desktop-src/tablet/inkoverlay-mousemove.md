---
description: Evento InkOverlay. MouseMove-ocorre quando o ponteiro do mouse é movido sobre o objeto InkCollector ou InkOverlay.
ms.assetid: b25aeead-9fb1-4221-82fa-ce2d81f5fed8
title: Evento InkOverlay. MouseMove (Msinkaut. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5f8290a11b00dcf97b3f3d8568ebe9890f715454
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108116904"
---
# <a name="inkoverlaymousemove-event"></a><span data-ttu-id="87025-103">Evento InkOverlay. MouseMove</span><span class="sxs-lookup"><span data-stu-id="87025-103">InkOverlay.MouseMove event</span></span>

<span data-ttu-id="87025-104">Ocorre quando o ponteiro do mouse é movido sobre o objeto [**InkCollector**](inkcollector-class.md) ou [**InkOverlay**](inkoverlay-class.md) .</span><span class="sxs-lookup"><span data-stu-id="87025-104">Occurs when the mouse pointer is moved over the [**InkCollector**](inkcollector-class.md) or [**InkOverlay**](inkoverlay-class.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="87025-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="87025-105">Syntax</span></span>


```C++
void MouseMove(
  [in]      InkMouseButton           Button,
  [in]      InkShiftKeyModifierFlags Shift,
  [in]      long                     pX,
  [in]      long                     pY,
  [in, out] VARIANT_BOOL             *Cancel
);
```



## <a name="parameters"></a><span data-ttu-id="87025-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="87025-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="87025-107">*Botão* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="87025-107">*Button* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="87025-108">O botão do mouse que foi pressionado.</span><span class="sxs-lookup"><span data-stu-id="87025-108">The mouse button that was pressed.</span></span>

</dd> <dt>

<span data-ttu-id="87025-109">*Shift* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="87025-109">*Shift* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="87025-110">O estado da tecla SHIFT.</span><span class="sxs-lookup"><span data-stu-id="87025-110">The state of the SHIFT key.</span></span>

</dd> <dt>

<span data-ttu-id="87025-111">*PX* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="87025-111">*pX* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="87025-112">A coordenada x, em pixels, de um clique do mouse.</span><span class="sxs-lookup"><span data-stu-id="87025-112">The x-coordinate, in pixels, of a mouse click.</span></span>

</dd> <dt>

<span data-ttu-id="87025-113">*pY* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="87025-113">*pY* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="87025-114">A coordenada y, em pixels, de um clique do mouse.</span><span class="sxs-lookup"><span data-stu-id="87025-114">The y-coordinate, in pixels, of a mouse click.</span></span>

</dd> <dt>

<span data-ttu-id="87025-115">*Cancelar* \[ entrada, saída\]</span><span class="sxs-lookup"><span data-stu-id="87025-115">*Cancel* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="87025-116">Se o evento deve ser cancelado para o controle pai.</span><span class="sxs-lookup"><span data-stu-id="87025-116">Whether the event should be canceled for the parent control.</span></span> <span data-ttu-id="87025-117">O valor padrão é **false**, que especifica que o evento não deve ser cancelado.</span><span class="sxs-lookup"><span data-stu-id="87025-117">The default value is **FALSE**, which specifies that the event should not be canceled.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="87025-118">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="87025-118">Return value</span></span>

<span data-ttu-id="87025-119">Esse evento não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="87025-119">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="87025-120">Comentários</span><span class="sxs-lookup"><span data-stu-id="87025-120">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="87025-121">As propriedades *PX* e *pY* estão em pixels, e não as unidades HIMETRIC associadas ao espaço de tinta.</span><span class="sxs-lookup"><span data-stu-id="87025-121">The properties *pX* and *pY* are in pixels, and not the HIMETRIC units that are associated with the ink space.</span></span> <span data-ttu-id="87025-122">Isso ocorre porque esse evento substitui o evento de mouse relacionado de um aplicativo sem reconhecimento de caneta e esse tipo de aplicativo compreende apenas os pixels.</span><span class="sxs-lookup"><span data-stu-id="87025-122">This is because this event replaces the related mouse event of a pen-unaware application and this type of application understands only pixels.</span></span>

 

> [!Note]  
> <span data-ttu-id="87025-123">Alguns controles dependem de uma relação específica entre os eventos [**MouseDown**](inkcollector-mousedown.md), [**MouseMove**](inkcollector-mousemove.md)e [**MouseUp**](inkcollector-mouseup.md) .</span><span class="sxs-lookup"><span data-stu-id="87025-123">Some controls rely on a specific relationship between [**MouseDown**](inkcollector-mousedown.md), [**MouseMove**](inkcollector-mousemove.md), and [**MouseUp**](inkcollector-mouseup.md) events.</span></span> <span data-ttu-id="87025-124">Cancelar alguns desses eventos pode ter resultados imprevistos.</span><span class="sxs-lookup"><span data-stu-id="87025-124">Canceling some of these events may have unanticipated results.</span></span>

 

<span data-ttu-id="87025-125">Esse método de evento é definido nas \_ \_ interfaces somente de expedição IInkCollectorEvents, IInkOverlayEvents e \_ IInkPictureEvents (dispinterfaces) com uma ID de IPEMouseMove de DISPID \_ .</span><span class="sxs-lookup"><span data-stu-id="87025-125">This event method is defined in the \_IInkCollectorEvents, \_IInkOverlayEvents, and \_IInkPictureEvents dispatch-only interfaces (dispinterfaces) with an ID of DISPID\_IPEMouseMove.</span></span>

## <a name="requirements"></a><span data-ttu-id="87025-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="87025-126">Requirements</span></span>



| <span data-ttu-id="87025-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="87025-127">Requirement</span></span> | <span data-ttu-id="87025-128">Valor</span><span class="sxs-lookup"><span data-stu-id="87025-128">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="87025-129">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="87025-129">Minimum supported client</span></span><br/> | <span data-ttu-id="87025-130">Somente aplicativos de área de trabalho do Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="87025-130">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="87025-131">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="87025-131">Minimum supported server</span></span><br/> | <span data-ttu-id="87025-132">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="87025-132">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="87025-133">parâmetro</span><span class="sxs-lookup"><span data-stu-id="87025-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="87025-134"><dt>Msinkaut. h (também requer Msinkaut \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="87025-134"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="87025-135">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="87025-135">Library</span></span><br/>                  | <dl> <span data-ttu-id="87025-136"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="87025-136"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="87025-137">Consulte também</span><span class="sxs-lookup"><span data-stu-id="87025-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="87025-138">**Classe InkOverlay**</span><span class="sxs-lookup"><span data-stu-id="87025-138">**InkOverlay Class**</span></span>](inkoverlay-class.md)
</dt> <dt>

[<span data-ttu-id="87025-139">**Enumeração InkMouseButton**</span><span class="sxs-lookup"><span data-stu-id="87025-139">**InkMouseButton Enumeration**</span></span>](/windows/desktop/api/msinkaut/ne-msinkaut-inkmousebutton)
</dt> <dt>

[<span data-ttu-id="87025-140">**Enumeração InkShiftKeyModifierFlags**</span><span class="sxs-lookup"><span data-stu-id="87025-140">**InkShiftKeyModifierFlags Enumeration**</span></span>](/windows/desktop/api/msinkaut/ne-msinkaut-inkshiftkeymodifierflags)
</dt> </dl>

 

 




