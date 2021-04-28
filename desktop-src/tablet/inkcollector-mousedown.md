---
description: Evento InkCollector. MouseDown-ocorre quando o ponteiro do mouse está sobre o objeto InkCollector ou InkOverlay e um botão do mouse é pressionado.
ms.assetid: db9ec396-b2a7-4f4f-99f2-95aad46eea28
title: Evento InkCollector. MouseDown (Msinkaut. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d29c8d3ba19856a8d6bfa038837b592c0b5f2b36
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108110174"
---
# <a name="inkcollectormousedown-event"></a><span data-ttu-id="d91b3-103">Evento InkCollector. MouseDown</span><span class="sxs-lookup"><span data-stu-id="d91b3-103">InkCollector.MouseDown event</span></span>

<span data-ttu-id="d91b3-104">Ocorre quando o ponteiro do mouse está sobre o objeto [**InkCollector**](inkcollector-class.md) ou [**InkOverlay**](inkoverlay-class.md) e um botão do mouse é pressionado.</span><span class="sxs-lookup"><span data-stu-id="d91b3-104">Occurs when the mouse pointer is over the [**InkCollector**](inkcollector-class.md) or [**InkOverlay**](inkoverlay-class.md) object and a mouse button is pressed.</span></span>

## <a name="syntax"></a><span data-ttu-id="d91b3-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="d91b3-105">Syntax</span></span>


```C++
void MouseDown(
  [in]      InkMouseButton           Button,
  [in]      InkShiftKeyModifierFlags Shift,
  [in]      long                     pX,
  [in]      long                     pY,
  [in, out] VARIANT_BOOL             *Cancel
);
```



## <a name="parameters"></a><span data-ttu-id="d91b3-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="d91b3-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d91b3-107">*Botão* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="d91b3-107">*Button* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d91b3-108">O botão do mouse que foi pressionado.</span><span class="sxs-lookup"><span data-stu-id="d91b3-108">The mouse button that was pressed.</span></span>

</dd> <dt>

<span data-ttu-id="d91b3-109">*Shift* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="d91b3-109">*Shift* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d91b3-110">O estado da tecla SHIFT.</span><span class="sxs-lookup"><span data-stu-id="d91b3-110">The state of the SHIFT key.</span></span>

</dd> <dt>

<span data-ttu-id="d91b3-111">*PX* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="d91b3-111">*pX* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d91b3-112">A coordenada X, em pixels, de um clique do mouse.</span><span class="sxs-lookup"><span data-stu-id="d91b3-112">The X-coordinate, in pixels, of a mouse click.</span></span>

</dd> <dt>

<span data-ttu-id="d91b3-113">*pY* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="d91b3-113">*pY* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d91b3-114">A coordenada Y, em pixels, de um clique do mouse.</span><span class="sxs-lookup"><span data-stu-id="d91b3-114">The Y-coordinate, in pixels, of a mouse click.</span></span>

</dd> <dt>

<span data-ttu-id="d91b3-115">*Cancelar* \[ entrada, saída\]</span><span class="sxs-lookup"><span data-stu-id="d91b3-115">*Cancel* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="d91b3-116">**Variante \_ TRUE** para cancelar o evento para o controle pai; caso contrário, **Variant \_ false**.</span><span class="sxs-lookup"><span data-stu-id="d91b3-116">**VARIANT\_TRUE** to cancel the event for the parent control; otherwise, **VARIANT\_FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d91b3-117">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="d91b3-117">Return value</span></span>

<span data-ttu-id="d91b3-118">Esse evento não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="d91b3-118">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="d91b3-119">Comentários</span><span class="sxs-lookup"><span data-stu-id="d91b3-119">Remarks</span></span>

<span data-ttu-id="d91b3-120">Para melhorar o desempenho de tinta em tempo real, oculte ou mostre o cursor do mouse nos manipuladores de eventos **MouseDown** e [**MouseUp**](inkcollector-mouseup.md) .</span><span class="sxs-lookup"><span data-stu-id="d91b3-120">To improve real-time ink performance, hide or show the mouse cursor in the **MouseDown** and [**MouseUp**](inkcollector-mouseup.md) event handlers.</span></span>

> [!Note]  
> <span data-ttu-id="d91b3-121">As propriedades *PX* e *pY* estão em pixels, e não as unidades HIMETRIC associadas ao espaço de tinta.</span><span class="sxs-lookup"><span data-stu-id="d91b3-121">The properties *pX* and *pY* are in pixels, and not the HIMETRIC units that are associated with the ink space.</span></span> <span data-ttu-id="d91b3-122">Isso ocorre porque esse evento substitui o evento de mouse relacionado de um aplicativo sem reconhecimento de caneta e esse tipo de aplicativo compreende apenas os pixels.</span><span class="sxs-lookup"><span data-stu-id="d91b3-122">This is because this event replaces the related mouse event of a pen-unaware application and this type of application understands only pixels.</span></span>

 

> [!Note]  
> <span data-ttu-id="d91b3-123">Alguns controles dependem de uma relação específica entre os eventos **MouseDown**, [**MouseMove**](inkcollector-mousemove.md)e [**MouseUp**](inkcollector-mouseup.md) .</span><span class="sxs-lookup"><span data-stu-id="d91b3-123">Some controls rely on a specific relationship between **MouseDown**, [**MouseMove**](inkcollector-mousemove.md), and [**MouseUp**](inkcollector-mouseup.md) events.</span></span> <span data-ttu-id="d91b3-124">Cancelar alguns desses eventos pode ter resultados imprevistos.</span><span class="sxs-lookup"><span data-stu-id="d91b3-124">Canceling some of these events may have unanticipated results.</span></span>

 

<span data-ttu-id="d91b3-125">Esse método de evento é definido nas \_ \_ interfaces somente de expedição IInkCollectorEvents, IInkOverlayEvents e \_ IInkPictureEvents (dispinterfaces) com uma ID de IPEMouseDown de DISPID \_ .</span><span class="sxs-lookup"><span data-stu-id="d91b3-125">This event method is defined in the \_IInkCollectorEvents, \_IInkOverlayEvents, and \_IInkPictureEvents dispatch-only interfaces (dispinterfaces) with an ID of DISPID\_IPEMouseDown.</span></span>

## <a name="requirements"></a><span data-ttu-id="d91b3-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d91b3-126">Requirements</span></span>



| <span data-ttu-id="d91b3-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="d91b3-127">Requirement</span></span> | <span data-ttu-id="d91b3-128">Valor</span><span class="sxs-lookup"><span data-stu-id="d91b3-128">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d91b3-129">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d91b3-129">Minimum supported client</span></span><br/> | <span data-ttu-id="d91b3-130">Somente aplicativos de área de trabalho do Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="d91b3-130">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="d91b3-131">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d91b3-131">Minimum supported server</span></span><br/> | <span data-ttu-id="d91b3-132">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="d91b3-132">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="d91b3-133">parâmetro</span><span class="sxs-lookup"><span data-stu-id="d91b3-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="d91b3-134"><dt>Msinkaut. h (também requer Msinkaut \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="d91b3-134"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="d91b3-135">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="d91b3-135">Library</span></span><br/>                  | <dl> <span data-ttu-id="d91b3-136"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d91b3-136"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="d91b3-137">Consulte também</span><span class="sxs-lookup"><span data-stu-id="d91b3-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d91b3-138">**Classe InkCollector**</span><span class="sxs-lookup"><span data-stu-id="d91b3-138">**InkCollector Class**</span></span>](inkcollector-class.md)
</dt> <dt>

[<span data-ttu-id="d91b3-139">**Enumeração InkMouseButton**</span><span class="sxs-lookup"><span data-stu-id="d91b3-139">**InkMouseButton Enumeration**</span></span>](/windows/desktop/api/msinkaut/ne-msinkaut-inkmousebutton)
</dt> <dt>

[<span data-ttu-id="d91b3-140">**Enumeração InkShiftKeyModifierFlags**</span><span class="sxs-lookup"><span data-stu-id="d91b3-140">**InkShiftKeyModifierFlags Enumeration**</span></span>](/windows/desktop/api/msinkaut/ne-msinkaut-inkshiftkeymodifierflags)
</dt> <dt>

[<span data-ttu-id="d91b3-141">**Evento MouseUp**</span><span class="sxs-lookup"><span data-stu-id="d91b3-141">**MouseUp Event**</span></span>](inkcollector-mouseup.md)
</dt> </dl>

 

 




