---
description: Evento InkOverlay. MouseDown-ocorre quando o ponteiro do mouse está sobre o objeto InkCollector ou InkOverlay e um botão do mouse é pressionado.
ms.assetid: 95c3b1ae-0e77-4ca2-ab73-a0e97ab115b5
title: Evento InkOverlay. MouseDown (Msinkaut. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3ff1e4bff715a6585ee607de766c809579f527aa
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108086814"
---
# <a name="inkoverlaymousedown-event"></a><span data-ttu-id="43a42-103">Evento InkOverlay. MouseDown</span><span class="sxs-lookup"><span data-stu-id="43a42-103">InkOverlay.MouseDown event</span></span>

<span data-ttu-id="43a42-104">Ocorre quando o ponteiro do mouse está sobre o objeto [**InkCollector**](inkcollector-class.md) ou [**InkOverlay**](inkoverlay-class.md) e um botão do mouse é pressionado.</span><span class="sxs-lookup"><span data-stu-id="43a42-104">Occurs when the mouse pointer is over the [**InkCollector**](inkcollector-class.md) or [**InkOverlay**](inkoverlay-class.md) object and a mouse button is pressed.</span></span>

## <a name="syntax"></a><span data-ttu-id="43a42-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="43a42-105">Syntax</span></span>


```C++
void MouseDown(
  [in]      InkMouseButton           Button,
  [in]      InkShiftKeyModifierFlags Shift,
  [in]      long                     pX,
  [in]      long                     pY,
  [in, out] VARIANT_BOOL             *Cancel
);
```



## <a name="parameters"></a><span data-ttu-id="43a42-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="43a42-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="43a42-107">*Botão* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="43a42-107">*Button* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="43a42-108">O botão do mouse que foi pressionado.</span><span class="sxs-lookup"><span data-stu-id="43a42-108">The mouse button that was pressed.</span></span>

</dd> <dt>

<span data-ttu-id="43a42-109">*Shift* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="43a42-109">*Shift* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="43a42-110">O estado da tecla SHIFT.</span><span class="sxs-lookup"><span data-stu-id="43a42-110">The state of the SHIFT key.</span></span>

</dd> <dt>

<span data-ttu-id="43a42-111">*PX* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="43a42-111">*pX* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="43a42-112">A coordenada X, em pixels, de um clique do mouse.</span><span class="sxs-lookup"><span data-stu-id="43a42-112">The X-coordinate, in pixels, of a mouse click.</span></span>

</dd> <dt>

<span data-ttu-id="43a42-113">*pY* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="43a42-113">*pY* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="43a42-114">A coordenada Y, em pixels, de um clique do mouse.</span><span class="sxs-lookup"><span data-stu-id="43a42-114">The Y-coordinate, in pixels, of a mouse click.</span></span>

</dd> <dt>

<span data-ttu-id="43a42-115">*Cancelar* \[ entrada, saída\]</span><span class="sxs-lookup"><span data-stu-id="43a42-115">*Cancel* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="43a42-116">**Variante \_ TRUE** para cancelar o evento para o controle pai; caso contrário, **Variant \_ false**.</span><span class="sxs-lookup"><span data-stu-id="43a42-116">**VARIANT\_TRUE** to cancelt he event forthe parent control; otherwise, **VARIANT\_FALSE**.</span></span> <span data-ttu-id="43a42-117">O valor padrão é **Variant \_ false**</span><span class="sxs-lookup"><span data-stu-id="43a42-117">The default value is **VARIANT\_FALSE**</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="43a42-118">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="43a42-118">Return value</span></span>

<span data-ttu-id="43a42-119">Esse evento não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="43a42-119">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="43a42-120">Comentários</span><span class="sxs-lookup"><span data-stu-id="43a42-120">Remarks</span></span>

<span data-ttu-id="43a42-121">Para melhorar o desempenho de tinta em tempo real, oculte ou mostre o cursor do mouse nos manipuladores de eventos [**MouseDown**](inkcollector-mousedown.md) e [**MouseUp**](inkcollector-mouseup.md) .</span><span class="sxs-lookup"><span data-stu-id="43a42-121">To improve real-time ink performance, hide or show the mouse cursor in the [**MouseDown**](inkcollector-mousedown.md) and [**MouseUp**](inkcollector-mouseup.md) event handlers.</span></span>

> [!Note]  
> <span data-ttu-id="43a42-122">As propriedades pX e pY estão em pixels, e não as unidades HIMETRIC associadas ao espaço de tinta.</span><span class="sxs-lookup"><span data-stu-id="43a42-122">The properties pX and pY are in pixels, and not the HIMETRIC units that are associated with the ink space.</span></span> <span data-ttu-id="43a42-123">Isso ocorre porque esse evento substitui o evento de mouse relacionado de um aplicativo sem reconhecimento de caneta e esse tipo de aplicativo compreende apenas os pixels.</span><span class="sxs-lookup"><span data-stu-id="43a42-123">This is because this event replaces the related mouse event of a pen-unaware application and this type of application understands only pixels.</span></span>

 

> [!Note]  
> <span data-ttu-id="43a42-124">Alguns controles dependem de uma relação específica entre os eventos [**MouseDown**](inkcollector-mousedown.md), [**MouseMove**](inkcollector-mousemove.md)e [**MouseUp**](inkcollector-mouseup.md) .</span><span class="sxs-lookup"><span data-stu-id="43a42-124">Some controls rely on a specific relationship between [**MouseDown**](inkcollector-mousedown.md), [**MouseMove**](inkcollector-mousemove.md), and [**MouseUp**](inkcollector-mouseup.md) events.</span></span> <span data-ttu-id="43a42-125">Cancelar alguns desses eventos pode ter resultados imprevistos.</span><span class="sxs-lookup"><span data-stu-id="43a42-125">Canceling some of these events may have unanticipated results.</span></span>

 

<span data-ttu-id="43a42-126">Esse método de evento é definido nas \_ \_ interfaces somente de expedição IInkCollectorEvents, IInkOverlayEvents e \_ IInkPictureEvents (dispinterfaces) com uma ID de IPEMouseDown de DISPID \_ .</span><span class="sxs-lookup"><span data-stu-id="43a42-126">This event method is defined in the \_IInkCollectorEvents, \_IInkOverlayEvents, and \_IInkPictureEvents dispatch-only interfaces (dispinterfaces) with an ID of DISPID\_IPEMouseDown.</span></span>

## <a name="requirements"></a><span data-ttu-id="43a42-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="43a42-127">Requirements</span></span>



| <span data-ttu-id="43a42-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="43a42-128">Requirement</span></span> | <span data-ttu-id="43a42-129">Valor</span><span class="sxs-lookup"><span data-stu-id="43a42-129">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="43a42-130">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="43a42-130">Minimum supported client</span></span><br/> | <span data-ttu-id="43a42-131">Somente aplicativos de área de trabalho do Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="43a42-131">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="43a42-132">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="43a42-132">Minimum supported server</span></span><br/> | <span data-ttu-id="43a42-133">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="43a42-133">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="43a42-134">parâmetro</span><span class="sxs-lookup"><span data-stu-id="43a42-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="43a42-135"><dt>Msinkaut. h (também requer Msinkaut \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="43a42-135"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="43a42-136">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="43a42-136">Library</span></span><br/>                  | <dl> <span data-ttu-id="43a42-137"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="43a42-137"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="43a42-138">Consulte também</span><span class="sxs-lookup"><span data-stu-id="43a42-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="43a42-139">**Classe InkOverlay**</span><span class="sxs-lookup"><span data-stu-id="43a42-139">**InkOverlay Class**</span></span>](inkoverlay-class.md)
</dt> <dt>

[<span data-ttu-id="43a42-140">**Enumeração InkMouseButton**</span><span class="sxs-lookup"><span data-stu-id="43a42-140">**InkMouseButton Enumeration**</span></span>](/windows/desktop/api/msinkaut/ne-msinkaut-inkmousebutton)
</dt> <dt>

[<span data-ttu-id="43a42-141">**Enumeração InkShiftKeyModifierFlags**</span><span class="sxs-lookup"><span data-stu-id="43a42-141">**InkShiftKeyModifierFlags Enumeration**</span></span>](/windows/desktop/api/msinkaut/ne-msinkaut-inkshiftkeymodifierflags)
</dt> <dt>

[<span data-ttu-id="43a42-142">**Evento MouseUp**</span><span class="sxs-lookup"><span data-stu-id="43a42-142">**MouseUp Event**</span></span>](inkcollector-mouseup.md)
</dt> </dl>

 

 




