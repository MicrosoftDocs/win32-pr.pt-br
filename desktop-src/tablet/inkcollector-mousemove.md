---
description: Evento InkCollector. MouseMove – ocorre quando o ponteiro do mouse é movido sobre o objeto InkCollector ou InkOverlay.
ms.assetid: 688ac7ef-dcee-44a4-8947-117966365061
title: Evento InkCollector. MouseMove (Msinkaut. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3392f2022af39600cb24461b26d37e5d624f4cb4
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108110154"
---
# <a name="inkcollectormousemove-event"></a><span data-ttu-id="ff0d0-103">Evento InkCollector. MouseMove</span><span class="sxs-lookup"><span data-stu-id="ff0d0-103">InkCollector.MouseMove event</span></span>

<span data-ttu-id="ff0d0-104">Ocorre quando o ponteiro do mouse é movido sobre o objeto [**InkCollector**](inkcollector-class.md) ou [**InkOverlay**](inkoverlay-class.md) .</span><span class="sxs-lookup"><span data-stu-id="ff0d0-104">Occurs when the mouse pointer is moved over the [**InkCollector**](inkcollector-class.md) or [**InkOverlay**](inkoverlay-class.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="ff0d0-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="ff0d0-105">Syntax</span></span>


```C++
void MouseMove(
  [in]      InkMouseButton           Button,
  [in]      InkShiftKeyModifierFlags Shift,
  [in]      long                     pX,
  [in]      long                     pY,
  [in, out] VARIANT_BOOL             *Cancel
);
```



## <a name="parameters"></a><span data-ttu-id="ff0d0-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="ff0d0-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ff0d0-107">*Botão* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="ff0d0-107">*Button* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ff0d0-108">O botão do mouse que foi pressionado.</span><span class="sxs-lookup"><span data-stu-id="ff0d0-108">The mouse button that was pressed.</span></span>

</dd> <dt>

<span data-ttu-id="ff0d0-109">*Shift* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="ff0d0-109">*Shift* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ff0d0-110">O estado da tecla SHIFT.</span><span class="sxs-lookup"><span data-stu-id="ff0d0-110">The state of the SHIFT key.</span></span>

</dd> <dt>

<span data-ttu-id="ff0d0-111">*PX* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="ff0d0-111">*pX* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ff0d0-112">A coordenada x, em pixels, de um clique do mouse.</span><span class="sxs-lookup"><span data-stu-id="ff0d0-112">The x-coordinate, in pixels, of a mouse click.</span></span>

</dd> <dt>

<span data-ttu-id="ff0d0-113">*pY* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="ff0d0-113">*pY* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ff0d0-114">A coordenada y, em pixels, de um clique do mouse.</span><span class="sxs-lookup"><span data-stu-id="ff0d0-114">The y-coordinate, in pixels, of a mouse click.</span></span>

</dd> <dt>

<span data-ttu-id="ff0d0-115">*Cancelar* \[ entrada, saída\]</span><span class="sxs-lookup"><span data-stu-id="ff0d0-115">*Cancel* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="ff0d0-116">**Variante \_ TRUE** para cancelar o evento para o controle pai; caso contrário, **Variant \_ false**.</span><span class="sxs-lookup"><span data-stu-id="ff0d0-116">**VARIANT\_TRUE** to cancel the event for the parent control; otherwise, **VARIANT\_FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ff0d0-117">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="ff0d0-117">Return value</span></span>

<span data-ttu-id="ff0d0-118">Esse evento não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="ff0d0-118">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="ff0d0-119">Comentários</span><span class="sxs-lookup"><span data-stu-id="ff0d0-119">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="ff0d0-120">As propriedades *PX* e *pY* estão em pixels, e não as unidades HIMETRIC associadas ao espaço de tinta.</span><span class="sxs-lookup"><span data-stu-id="ff0d0-120">The properties *pX* and *pY* are in pixels, and not the HIMETRIC units that are associated with the ink space.</span></span> <span data-ttu-id="ff0d0-121">Isso ocorre porque esse evento substitui o evento de mouse relacionado de um aplicativo sem reconhecimento de caneta e esse tipo de aplicativo compreende apenas os pixels.</span><span class="sxs-lookup"><span data-stu-id="ff0d0-121">This is because this event replaces the related mouse event of a pen-unaware application and this type of application understands only pixels.</span></span>

 

> [!Note]  
> <span data-ttu-id="ff0d0-122">Alguns controles dependem de uma relação específica entre os eventos [**MouseDown**](inkcollector-mousedown.md), **MouseMove** e [**MouseUp**](inkcollector-mouseup.md) .</span><span class="sxs-lookup"><span data-stu-id="ff0d0-122">Some controls rely on a specific relationship between [**MouseDown**](inkcollector-mousedown.md), **MouseMove**, and [**MouseUp**](inkcollector-mouseup.md) events.</span></span> <span data-ttu-id="ff0d0-123">Cancelar alguns desses eventos pode ter resultados imprevistos.</span><span class="sxs-lookup"><span data-stu-id="ff0d0-123">Canceling some of these events may have unanticipated results.</span></span>

 

<span data-ttu-id="ff0d0-124">Esse método de evento é definido nas \_ \_ interfaces somente de expedição IInkCollectorEvents, IInkOverlayEvents e \_ IInkPictureEvents (dispinterfaces) com uma ID de IPEMouseMove de DISPID \_ .</span><span class="sxs-lookup"><span data-stu-id="ff0d0-124">This event method is defined in the \_IInkCollectorEvents, \_IInkOverlayEvents, and \_IInkPictureEvents dispatch-only interfaces (dispinterfaces) with an ID of DISPID\_IPEMouseMove.</span></span>

## <a name="requirements"></a><span data-ttu-id="ff0d0-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ff0d0-125">Requirements</span></span>



| <span data-ttu-id="ff0d0-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="ff0d0-126">Requirement</span></span> | <span data-ttu-id="ff0d0-127">Valor</span><span class="sxs-lookup"><span data-stu-id="ff0d0-127">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ff0d0-128">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ff0d0-128">Minimum supported client</span></span><br/> | <span data-ttu-id="ff0d0-129">Somente aplicativos de área de trabalho do Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="ff0d0-129">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="ff0d0-130">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ff0d0-130">Minimum supported server</span></span><br/> | <span data-ttu-id="ff0d0-131">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="ff0d0-131">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="ff0d0-132">parâmetro</span><span class="sxs-lookup"><span data-stu-id="ff0d0-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="ff0d0-133"><dt>Msinkaut. h (também requer Msinkaut \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="ff0d0-133"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="ff0d0-134">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="ff0d0-134">Library</span></span><br/>                  | <dl> <span data-ttu-id="ff0d0-135"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ff0d0-135"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="ff0d0-136">Consulte também</span><span class="sxs-lookup"><span data-stu-id="ff0d0-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ff0d0-137">**Classe InkCollector**</span><span class="sxs-lookup"><span data-stu-id="ff0d0-137">**InkCollector Class**</span></span>](inkcollector-class.md)
</dt> <dt>

[<span data-ttu-id="ff0d0-138">**Enumeração InkMouseButton**</span><span class="sxs-lookup"><span data-stu-id="ff0d0-138">**InkMouseButton Enumeration**</span></span>](/windows/desktop/api/msinkaut/ne-msinkaut-inkmousebutton)
</dt> <dt>

[<span data-ttu-id="ff0d0-139">**Enumeração InkShiftKeyModifierFlags**</span><span class="sxs-lookup"><span data-stu-id="ff0d0-139">**InkShiftKeyModifierFlags Enumeration**</span></span>](/windows/desktop/api/msinkaut/ne-msinkaut-inkshiftkeymodifierflags)
</dt> </dl>

 

 




