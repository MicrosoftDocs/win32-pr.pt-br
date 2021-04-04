---
description: Ocorre quando o ponteiro do mouse está sobre o objeto InkCollector ou InkOverlay e um botão do mouse é liberado.
ms.assetid: 049e1560-d4b2-4d34-9d54-2b45217001b2
title: Evento InkOverlay. MouseUp (Msinkaut. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1f16fd3dc5006f43e09e093cb2c474a8578f56c6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104171167"
---
# <a name="inkoverlaymouseup-event"></a><span data-ttu-id="4c4c4-103">Evento InkOverlay. MouseUp</span><span class="sxs-lookup"><span data-stu-id="4c4c4-103">InkOverlay.MouseUp event</span></span>

<span data-ttu-id="4c4c4-104">Ocorre quando o ponteiro do mouse está sobre o objeto [**InkCollector**](inkcollector-class.md) ou [**InkOverlay**](inkoverlay-class.md) e um botão do mouse é liberado.</span><span class="sxs-lookup"><span data-stu-id="4c4c4-104">Occurs when the mouse pointer is over the [**InkCollector**](inkcollector-class.md) or [**InkOverlay**](inkoverlay-class.md) object and a mouse button is released.</span></span>

## <a name="syntax"></a><span data-ttu-id="4c4c4-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="4c4c4-105">Syntax</span></span>


```C++
void MouseUp(
  [in]      InkMouseButton           Button,
  [in]      InkShiftKeyModifierFlags Shift,
  [in]      long                     pX,
  [in]      long                     pY,
  [in, out] VARIANT_BOOL             *Cancel
);
```



## <a name="parameters"></a><span data-ttu-id="4c4c4-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="4c4c4-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4c4c4-107">*Botão* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="4c4c4-107">*Button* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4c4c4-108">O botão do mouse que foi lançado.</span><span class="sxs-lookup"><span data-stu-id="4c4c4-108">The mouse button that was released.</span></span>

</dd> <dt>

<span data-ttu-id="4c4c4-109">*Shift* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="4c4c4-109">*Shift* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4c4c4-110">O estado da tecla SHIFT.</span><span class="sxs-lookup"><span data-stu-id="4c4c4-110">The state of the SHIFT key.</span></span>

</dd> <dt>

<span data-ttu-id="4c4c4-111">*PX* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="4c4c4-111">*pX* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4c4c4-112">A coordenada x, em pixels, de um clique do mouse.</span><span class="sxs-lookup"><span data-stu-id="4c4c4-112">The x-coordinate, in pixels, of a mouse click.</span></span>

</dd> <dt>

<span data-ttu-id="4c4c4-113">*pY* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="4c4c4-113">*pY* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4c4c4-114">A coordenada y, em pixels, de um clique do mouse.</span><span class="sxs-lookup"><span data-stu-id="4c4c4-114">The y-coordinate, in pixels, of a mouse click.</span></span>

</dd> <dt>

<span data-ttu-id="4c4c4-115">*Cancelar* \[ entrada, saída\]</span><span class="sxs-lookup"><span data-stu-id="4c4c4-115">*Cancel* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="4c4c4-116">Se o evento deve ser cancelado para o controle pai.</span><span class="sxs-lookup"><span data-stu-id="4c4c4-116">Whether the event should be canceled for the parent control.</span></span> <span data-ttu-id="4c4c4-117">O valor padrão é **false**, que especifica que o evento não deve ser cancelado.</span><span class="sxs-lookup"><span data-stu-id="4c4c4-117">The default value is **FALSE**, which specifies that the event should not be canceled.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4c4c4-118">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="4c4c4-118">Return value</span></span>

<span data-ttu-id="4c4c4-119">Esse evento não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="4c4c4-119">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="4c4c4-120">Comentários</span><span class="sxs-lookup"><span data-stu-id="4c4c4-120">Remarks</span></span>

<span data-ttu-id="4c4c4-121">Para melhorar o desempenho de tinta em tempo real, oculte ou mostre o cursor do mouse nos manipuladores de eventos [**MouseDown**](inkcollector-mousedown.md) e [**MouseUp**](inkcollector-mouseup.md) .</span><span class="sxs-lookup"><span data-stu-id="4c4c4-121">To improve real-time ink performance, hide or show the mouse cursor in the [**MouseDown**](inkcollector-mousedown.md) and [**MouseUp**](inkcollector-mouseup.md) event handlers.</span></span>

> [!Note]  
> <span data-ttu-id="4c4c4-122">As propriedades *PX* e *pY* estão em pixels, e não as unidades HIMETRIC associadas ao espaço de tinta.</span><span class="sxs-lookup"><span data-stu-id="4c4c4-122">The properties *pX* and *pY* are in pixels, and not the HIMETRIC units that are associated with the ink space.</span></span> <span data-ttu-id="4c4c4-123">Isso ocorre porque esse evento substitui o evento de mouse relacionado de um aplicativo sem reconhecimento de caneta e esse tipo de aplicativo compreende apenas os pixels.</span><span class="sxs-lookup"><span data-stu-id="4c4c4-123">This is because this event replaces the related mouse event of a pen-unaware application and this type of application understands only pixels.</span></span>

 

> [!Note]  
> <span data-ttu-id="4c4c4-124">Alguns controles dependem de uma relação específica entre os eventos [**MouseDown**](inkcollector-mousedown.md), [**MouseMove**](inkcollector-mousemove.md)e [**MouseUp**](inkcollector-mouseup.md) .</span><span class="sxs-lookup"><span data-stu-id="4c4c4-124">Some controls rely on a specific relationship between [**MouseDown**](inkcollector-mousedown.md), [**MouseMove**](inkcollector-mousemove.md), and [**MouseUp**](inkcollector-mouseup.md) events.</span></span> <span data-ttu-id="4c4c4-125">Cancelar alguns desses eventos pode ter resultados imprevistos.</span><span class="sxs-lookup"><span data-stu-id="4c4c4-125">Canceling some of these events may have unanticipated results.</span></span>

 

<span data-ttu-id="4c4c4-126">Esse método de evento é definido nas \_ \_ interfaces somente de expedição IInkCollectorEvents, IInkOverlayEvents e \_ IInkPictureEvents (dispinterfaces) com uma ID de IPEMouseUp de DISPID \_ .</span><span class="sxs-lookup"><span data-stu-id="4c4c4-126">This event method is defined in the \_IInkCollectorEvents, \_IInkOverlayEvents, and \_IInkPictureEvents dispatch-only interfaces (dispinterfaces) with an ID of DISPID\_IPEMouseUp.</span></span>

## <a name="requirements"></a><span data-ttu-id="4c4c4-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4c4c4-127">Requirements</span></span>



| <span data-ttu-id="4c4c4-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="4c4c4-128">Requirement</span></span> | <span data-ttu-id="4c4c4-129">Valor</span><span class="sxs-lookup"><span data-stu-id="4c4c4-129">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4c4c4-130">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="4c4c4-130">Minimum supported client</span></span><br/> | <span data-ttu-id="4c4c4-131">Somente aplicativos de área de trabalho do Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="4c4c4-131">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="4c4c4-132">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="4c4c4-132">Minimum supported server</span></span><br/> | <span data-ttu-id="4c4c4-133">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="4c4c4-133">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="4c4c4-134">parâmetro</span><span class="sxs-lookup"><span data-stu-id="4c4c4-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="4c4c4-135"><dt>Msinkaut. h (também requer Msinkaut \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="4c4c4-135"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="4c4c4-136">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="4c4c4-136">Library</span></span><br/>                  | <dl> <span data-ttu-id="4c4c4-137"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4c4c4-137"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="4c4c4-138">Confira também</span><span class="sxs-lookup"><span data-stu-id="4c4c4-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4c4c4-139">**Classe InkOverlay**</span><span class="sxs-lookup"><span data-stu-id="4c4c4-139">**InkOverlay Class**</span></span>](inkoverlay-class.md)
</dt> <dt>

[<span data-ttu-id="4c4c4-140">**Enumeração InkMouseButton**</span><span class="sxs-lookup"><span data-stu-id="4c4c4-140">**InkMouseButton Enumeration**</span></span>](/windows/desktop/api/msinkaut/ne-msinkaut-inkmousebutton)
</dt> <dt>

[<span data-ttu-id="4c4c4-141">**Enumeração InkShiftKeyModifierFlags**</span><span class="sxs-lookup"><span data-stu-id="4c4c4-141">**InkShiftKeyModifierFlags Enumeration**</span></span>](/windows/desktop/api/msinkaut/ne-msinkaut-inkshiftkeymodifierflags)
</dt> </dl>

 

 




