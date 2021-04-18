---
description: Ocorre quando o ponteiro do mouse é movido sobre o objeto InkCollector ou InkOverlay.
ms.assetid: 688ac7ef-dcee-44a4-8947-117966365061
title: Evento InkCollector. MouseMove (Msinkaut. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 27ad88c35871ed73125be73b66329ede464f0c00
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105807812"
---
# <a name="inkcollectormousemove-event"></a><span data-ttu-id="9f2ec-103">Evento InkCollector. MouseMove</span><span class="sxs-lookup"><span data-stu-id="9f2ec-103">InkCollector.MouseMove event</span></span>

<span data-ttu-id="9f2ec-104">Ocorre quando o ponteiro do mouse é movido sobre o objeto [**InkCollector**](inkcollector-class.md) ou [**InkOverlay**](inkoverlay-class.md) .</span><span class="sxs-lookup"><span data-stu-id="9f2ec-104">Occurs when the mouse pointer is moved over the [**InkCollector**](inkcollector-class.md) or [**InkOverlay**](inkoverlay-class.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="9f2ec-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="9f2ec-105">Syntax</span></span>


```C++
void MouseMove(
  [in]      InkMouseButton           Button,
  [in]      InkShiftKeyModifierFlags Shift,
  [in]      long                     pX,
  [in]      long                     pY,
  [in, out] VARIANT_BOOL             *Cancel
);
```



## <a name="parameters"></a><span data-ttu-id="9f2ec-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="9f2ec-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9f2ec-107">*Botão* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="9f2ec-107">*Button* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9f2ec-108">O botão do mouse que foi pressionado.</span><span class="sxs-lookup"><span data-stu-id="9f2ec-108">The mouse button that was pressed.</span></span>

</dd> <dt>

<span data-ttu-id="9f2ec-109">*Shift* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="9f2ec-109">*Shift* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9f2ec-110">O estado da tecla SHIFT.</span><span class="sxs-lookup"><span data-stu-id="9f2ec-110">The state of the SHIFT key.</span></span>

</dd> <dt>

<span data-ttu-id="9f2ec-111">*PX* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="9f2ec-111">*pX* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9f2ec-112">A coordenada x, em pixels, de um clique do mouse.</span><span class="sxs-lookup"><span data-stu-id="9f2ec-112">The x-coordinate, in pixels, of a mouse click.</span></span>

</dd> <dt>

<span data-ttu-id="9f2ec-113">*pY* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="9f2ec-113">*pY* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9f2ec-114">A coordenada y, em pixels, de um clique do mouse.</span><span class="sxs-lookup"><span data-stu-id="9f2ec-114">The y-coordinate, in pixels, of a mouse click.</span></span>

</dd> <dt>

<span data-ttu-id="9f2ec-115">*Cancelar* \[ entrada, saída\]</span><span class="sxs-lookup"><span data-stu-id="9f2ec-115">*Cancel* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="9f2ec-116">**Variante \_ TRUE** para cancelar o evento para o controle pai; caso contrário, **Variant \_ false**.</span><span class="sxs-lookup"><span data-stu-id="9f2ec-116">**VARIANT\_TRUE** to cancel the event for the parent control; otherwise, **VARIANT\_FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9f2ec-117">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="9f2ec-117">Return value</span></span>

<span data-ttu-id="9f2ec-118">Esse evento não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="9f2ec-118">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="9f2ec-119">Comentários</span><span class="sxs-lookup"><span data-stu-id="9f2ec-119">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="9f2ec-120">As propriedades *PX* e *pY* estão em pixels, e não as unidades HIMETRIC associadas ao espaço de tinta.</span><span class="sxs-lookup"><span data-stu-id="9f2ec-120">The properties *pX* and *pY* are in pixels, and not the HIMETRIC units that are associated with the ink space.</span></span> <span data-ttu-id="9f2ec-121">Isso ocorre porque esse evento substitui o evento de mouse relacionado de um aplicativo sem reconhecimento de caneta e esse tipo de aplicativo compreende apenas os pixels.</span><span class="sxs-lookup"><span data-stu-id="9f2ec-121">This is because this event replaces the related mouse event of a pen-unaware application and this type of application understands only pixels.</span></span>

 

> [!Note]  
> <span data-ttu-id="9f2ec-122">Alguns controles dependem de uma relação específica entre os eventos [**MouseDown**](inkcollector-mousedown.md), **MouseMove** e [**MouseUp**](inkcollector-mouseup.md) .</span><span class="sxs-lookup"><span data-stu-id="9f2ec-122">Some controls rely on a specific relationship between [**MouseDown**](inkcollector-mousedown.md), **MouseMove**, and [**MouseUp**](inkcollector-mouseup.md) events.</span></span> <span data-ttu-id="9f2ec-123">Cancelar alguns desses eventos pode ter resultados imprevistos.</span><span class="sxs-lookup"><span data-stu-id="9f2ec-123">Canceling some of these events may have unanticipated results.</span></span>

 

<span data-ttu-id="9f2ec-124">Esse método de evento é definido nas \_ \_ interfaces somente de expedição IInkCollectorEvents, IInkOverlayEvents e \_ IInkPictureEvents (dispinterfaces) com uma ID de IPEMouseMove de DISPID \_ .</span><span class="sxs-lookup"><span data-stu-id="9f2ec-124">This event method is defined in the \_IInkCollectorEvents, \_IInkOverlayEvents, and \_IInkPictureEvents dispatch-only interfaces (dispinterfaces) with an ID of DISPID\_IPEMouseMove.</span></span>

## <a name="requirements"></a><span data-ttu-id="9f2ec-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9f2ec-125">Requirements</span></span>



| <span data-ttu-id="9f2ec-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="9f2ec-126">Requirement</span></span> | <span data-ttu-id="9f2ec-127">Valor</span><span class="sxs-lookup"><span data-stu-id="9f2ec-127">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9f2ec-128">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="9f2ec-128">Minimum supported client</span></span><br/> | <span data-ttu-id="9f2ec-129">Somente aplicativos de área de trabalho do Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="9f2ec-129">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="9f2ec-130">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="9f2ec-130">Minimum supported server</span></span><br/> | <span data-ttu-id="9f2ec-131">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="9f2ec-131">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="9f2ec-132">parâmetro</span><span class="sxs-lookup"><span data-stu-id="9f2ec-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="9f2ec-133"><dt>Msinkaut. h (também requer Msinkaut \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="9f2ec-133"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="9f2ec-134">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="9f2ec-134">Library</span></span><br/>                  | <dl> <span data-ttu-id="9f2ec-135"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9f2ec-135"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="9f2ec-136">Confira também</span><span class="sxs-lookup"><span data-stu-id="9f2ec-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9f2ec-137">**Classe InkCollector**</span><span class="sxs-lookup"><span data-stu-id="9f2ec-137">**InkCollector Class**</span></span>](inkcollector-class.md)
</dt> <dt>

[<span data-ttu-id="9f2ec-138">**Enumeração InkMouseButton**</span><span class="sxs-lookup"><span data-stu-id="9f2ec-138">**InkMouseButton Enumeration**</span></span>](/windows/desktop/api/msinkaut/ne-msinkaut-inkmousebutton)
</dt> <dt>

[<span data-ttu-id="9f2ec-139">**Enumeração InkShiftKeyModifierFlags**</span><span class="sxs-lookup"><span data-stu-id="9f2ec-139">**InkShiftKeyModifierFlags Enumeration**</span></span>](/windows/desktop/api/msinkaut/ne-msinkaut-inkshiftkeymodifierflags)
</dt> </dl>

 

 




