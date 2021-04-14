---
description: Ocorre quando o ponteiro do mouse está sobre o objeto InkCollector ou InkOverlay e um botão do mouse é liberado.
ms.assetid: 6dcc6c68-89f7-4020-b378-56df9d46974b
title: Evento InkCollector. MouseUp (Msinkaut. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e5f217cf6f5eeff930c1746d1a5ceac180686942
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104460972"
---
# <a name="inkcollectormouseup-event"></a><span data-ttu-id="393e8-103">Evento InkCollector. MouseUp</span><span class="sxs-lookup"><span data-stu-id="393e8-103">InkCollector.MouseUp event</span></span>

<span data-ttu-id="393e8-104">Ocorre quando o ponteiro do mouse está sobre o objeto [**InkCollector**](inkcollector-class.md) ou [**InkOverlay**](inkoverlay-class.md) e um botão do mouse é liberado.</span><span class="sxs-lookup"><span data-stu-id="393e8-104">Occurs when the mouse pointer is over the [**InkCollector**](inkcollector-class.md) or [**InkOverlay**](inkoverlay-class.md) object and a mouse button is released.</span></span>

## <a name="syntax"></a><span data-ttu-id="393e8-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="393e8-105">Syntax</span></span>


```C++
void MouseUp(
  [in]      InkMouseButton           Button,
  [in]      InkShiftKeyModifierFlags Shift,
  [in]      long                     pX,
  [in]      long                     pY,
  [in, out] VARIANT_BOOL             *Cancel
);
```



## <a name="parameters"></a><span data-ttu-id="393e8-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="393e8-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="393e8-107">*Botão* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="393e8-107">*Button* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="393e8-108">O botão do mouse que foi lançado.</span><span class="sxs-lookup"><span data-stu-id="393e8-108">The mouse button that was released.</span></span>

</dd> <dt>

<span data-ttu-id="393e8-109">*Shift* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="393e8-109">*Shift* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="393e8-110">O estado da tecla SHIFT.</span><span class="sxs-lookup"><span data-stu-id="393e8-110">The state of the SHIFT key.</span></span>

</dd> <dt>

<span data-ttu-id="393e8-111">*PX* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="393e8-111">*pX* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="393e8-112">A coordenada x, em pixels, de um clique do mouse.</span><span class="sxs-lookup"><span data-stu-id="393e8-112">The x-coordinate, in pixels, of a mouse click.</span></span>

</dd> <dt>

<span data-ttu-id="393e8-113">*pY* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="393e8-113">*pY* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="393e8-114">A coordenada y, em pixels, de um clique do mouse.</span><span class="sxs-lookup"><span data-stu-id="393e8-114">The y-coordinate, in pixels, of a mouse click.</span></span>

</dd> <dt>

<span data-ttu-id="393e8-115">*Cancelar* \[ entrada, saída\]</span><span class="sxs-lookup"><span data-stu-id="393e8-115">*Cancel* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="393e8-116">**Variante \_ TRUE** para cancelar o evento para o controle pai; caso contrário, **Variant \_ false**.</span><span class="sxs-lookup"><span data-stu-id="393e8-116">**VARIANT\_TRUE** to cancel the event for the parent control; otherwise, **VARIANT\_FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="393e8-117">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="393e8-117">Return value</span></span>

<span data-ttu-id="393e8-118">Esse evento não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="393e8-118">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="393e8-119">Comentários</span><span class="sxs-lookup"><span data-stu-id="393e8-119">Remarks</span></span>

<span data-ttu-id="393e8-120">Para melhorar o desempenho de tinta em tempo real, oculte ou mostre o cursor do mouse nos manipuladores de eventos [**MouseDown**](inkcollector-mousedown.md) e **MouseUp** .</span><span class="sxs-lookup"><span data-stu-id="393e8-120">To improve real-time ink performance, hide or show the mouse cursor in the [**MouseDown**](inkcollector-mousedown.md) and **MouseUp** event handlers.</span></span>

> [!Note]  
> <span data-ttu-id="393e8-121">As propriedades *PX* e *pY* estão em pixels, e não as unidades HIMETRIC associadas ao espaço de tinta.</span><span class="sxs-lookup"><span data-stu-id="393e8-121">The properties *pX* and *pY* are in pixels, and not the HIMETRIC units that are associated with the ink space.</span></span> <span data-ttu-id="393e8-122">Isso ocorre porque esse evento substitui o evento de mouse relacionado de um aplicativo sem reconhecimento de caneta e esse tipo de aplicativo compreende apenas os pixels.</span><span class="sxs-lookup"><span data-stu-id="393e8-122">This is because this event replaces the related mouse event of a pen-unaware application and this type of application understands only pixels.</span></span>

 

> [!Note]  
> <span data-ttu-id="393e8-123">Alguns controles dependem de uma relação específica entre os eventos [**MouseDown**](inkcollector-mousedown.md), [**MouseMove**](inkcollector-mousemove.md)e **MouseUp** .</span><span class="sxs-lookup"><span data-stu-id="393e8-123">Some controls rely on a specific relationship between [**MouseDown**](inkcollector-mousedown.md), [**MouseMove**](inkcollector-mousemove.md), and **MouseUp** events.</span></span> <span data-ttu-id="393e8-124">Cancelar alguns desses eventos pode ter resultados imprevistos.</span><span class="sxs-lookup"><span data-stu-id="393e8-124">Canceling some of these events may have unanticipated results.</span></span>

 

<span data-ttu-id="393e8-125">Esse método de evento é definido nas \_ \_ interfaces somente de expedição IInkCollectorEvents, IInkOverlayEvents e \_ IInkPictureEvents (dispinterfaces) com uma ID de IPEMouseUp de DISPID \_ .</span><span class="sxs-lookup"><span data-stu-id="393e8-125">This event method is defined in the \_IInkCollectorEvents, \_IInkOverlayEvents, and \_IInkPictureEvents dispatch-only interfaces (dispinterfaces) with an ID of DISPID\_IPEMouseUp.</span></span>

## <a name="requirements"></a><span data-ttu-id="393e8-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="393e8-126">Requirements</span></span>



| <span data-ttu-id="393e8-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="393e8-127">Requirement</span></span> | <span data-ttu-id="393e8-128">Valor</span><span class="sxs-lookup"><span data-stu-id="393e8-128">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="393e8-129">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="393e8-129">Minimum supported client</span></span><br/> | <span data-ttu-id="393e8-130">Somente aplicativos de área de trabalho do Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="393e8-130">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="393e8-131">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="393e8-131">Minimum supported server</span></span><br/> | <span data-ttu-id="393e8-132">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="393e8-132">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="393e8-133">parâmetro</span><span class="sxs-lookup"><span data-stu-id="393e8-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="393e8-134"><dt>Msinkaut. h (também requer Msinkaut \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="393e8-134"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="393e8-135">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="393e8-135">Library</span></span><br/>                  | <dl> <span data-ttu-id="393e8-136"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="393e8-136"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="393e8-137">Confira também</span><span class="sxs-lookup"><span data-stu-id="393e8-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="393e8-138">**Classe InkCollector**</span><span class="sxs-lookup"><span data-stu-id="393e8-138">**InkCollector Class**</span></span>](inkcollector-class.md)
</dt> <dt>

[<span data-ttu-id="393e8-139">**Enumeração InkMouseButton**</span><span class="sxs-lookup"><span data-stu-id="393e8-139">**InkMouseButton Enumeration**</span></span>](/windows/desktop/api/msinkaut/ne-msinkaut-inkmousebutton)
</dt> <dt>

[<span data-ttu-id="393e8-140">**Enumeração InkShiftKeyModifierFlags**</span><span class="sxs-lookup"><span data-stu-id="393e8-140">**InkShiftKeyModifierFlags Enumeration**</span></span>](/windows/desktop/api/msinkaut/ne-msinkaut-inkshiftkeymodifierflags)
</dt> </dl>

 

 




