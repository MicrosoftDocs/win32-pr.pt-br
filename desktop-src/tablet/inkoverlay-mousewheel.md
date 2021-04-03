---
description: Ocorre quando a roda do mouse se move enquanto o objeto InkCollector ou InkOverlay tem foco.
ms.assetid: b7269e07-7001-48ca-8e20-a39cb02f3719
title: Evento InkOverlay. MouseWheel (Msinkaut. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7bbd919fdf02d85c32efa2a1a923d5de7ebe4f5b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103837026"
---
# <a name="inkoverlaymousewheel-event"></a><span data-ttu-id="ba0df-103">Evento InkOverlay. MouseWheel</span><span class="sxs-lookup"><span data-stu-id="ba0df-103">InkOverlay.MouseWheel event</span></span>

<span data-ttu-id="ba0df-104">Ocorre quando a roda do mouse se move enquanto o objeto [**InkCollector**](inkcollector-class.md) ou [**InkOverlay**](inkoverlay-class.md) tem foco.</span><span class="sxs-lookup"><span data-stu-id="ba0df-104">Occurs when the mouse wheel moves while the [**InkCollector**](inkcollector-class.md) or [**InkOverlay**](inkoverlay-class.md) object has focus.</span></span>

## <a name="syntax"></a><span data-ttu-id="ba0df-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="ba0df-105">Syntax</span></span>


```C++
void MouseWheel(
  [in]      InkMouseButton           Button,
  [in]      InkShiftKeyModifierFlags Shift,
  [in]      long                     Delta,
  [in]      long                     x,
  [in]      long                     y,
  [in, out] VARIANT_BOOL             *Cancel
);
```



## <a name="parameters"></a><span data-ttu-id="ba0df-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="ba0df-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ba0df-107">*Botão* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="ba0df-107">*Button* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ba0df-108">O botão do mouse que foi pressionado.</span><span class="sxs-lookup"><span data-stu-id="ba0df-108">The mouse button that was pressed.</span></span>

</dd> <dt>

<span data-ttu-id="ba0df-109">*Shift* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="ba0df-109">*Shift* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ba0df-110">O estado da tecla SHIFT.</span><span class="sxs-lookup"><span data-stu-id="ba0df-110">The state of the SHIFT key.</span></span>

</dd> <dt>

<span data-ttu-id="ba0df-111">*Delta* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="ba0df-111">*Delta* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ba0df-112">Uma contagem assinada do número de tentativas que a roda do mouse gira.</span><span class="sxs-lookup"><span data-stu-id="ba0df-112">A signed count of the number of detents the mouse wheel has rotated.</span></span> <span data-ttu-id="ba0df-113">Um detentor é um ponto da roda do mouse.</span><span class="sxs-lookup"><span data-stu-id="ba0df-113">A detent is one notch of the mouse wheel.</span></span>

</dd> <dt>

<span data-ttu-id="ba0df-114">*x* \[ em\]</span><span class="sxs-lookup"><span data-stu-id="ba0df-114">*x* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ba0df-115">A coordenada x, em pixels, de um clique do mouse.</span><span class="sxs-lookup"><span data-stu-id="ba0df-115">The x-coordinate, in pixels, of a mouse click.</span></span>

</dd> <dt>

<span data-ttu-id="ba0df-116">*y* \[ em\]</span><span class="sxs-lookup"><span data-stu-id="ba0df-116">*y* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ba0df-117">A coordenada y, em pixels, de um clique do mouse.</span><span class="sxs-lookup"><span data-stu-id="ba0df-117">The y-coordinate, in pixels, of a mouse click.</span></span>

</dd> <dt>

<span data-ttu-id="ba0df-118">*Cancelar* \[ entrada, saída\]</span><span class="sxs-lookup"><span data-stu-id="ba0df-118">*Cancel* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="ba0df-119">Se o evento deve ser cancelado para o controle pai.</span><span class="sxs-lookup"><span data-stu-id="ba0df-119">Whether the event should be canceled for the parent control.</span></span> <span data-ttu-id="ba0df-120">O valor padrão é **false**, que especifica que o evento não deve ser cancelado.</span><span class="sxs-lookup"><span data-stu-id="ba0df-120">The default value is **FALSE**, which specifies that the event should not be canceled.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ba0df-121">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="ba0df-121">Return value</span></span>

<span data-ttu-id="ba0df-122">Esse evento não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="ba0df-122">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="ba0df-123">Comentários</span><span class="sxs-lookup"><span data-stu-id="ba0df-123">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="ba0df-124">As propriedades *PX* e *pY* estão em pixels, e não as unidades HIMETRIC associadas ao espaço de tinta.</span><span class="sxs-lookup"><span data-stu-id="ba0df-124">The properties *pX* and *pY* are in pixels, and not the HIMETRIC units that are associated with the ink space.</span></span> <span data-ttu-id="ba0df-125">Isso ocorre porque esse evento substitui o evento de mouse relacionado de um aplicativo sem reconhecimento de caneta e esse tipo de aplicativo compreende apenas os pixels.</span><span class="sxs-lookup"><span data-stu-id="ba0df-125">This is because this event replaces the related mouse event of a pen-unaware application and this type of application understands only pixels.</span></span>

 

<span data-ttu-id="ba0df-126">Esse método de evento é definido nas \_ \_ interfaces somente de expedição IInkCollectorEvents, IInkOverlayEvents e \_ IInkPictureEvents (dispinterfaces) com uma ID de IPEMouseWheel de DISPID \_ .</span><span class="sxs-lookup"><span data-stu-id="ba0df-126">This event method is defined in the \_IInkCollectorEvents, \_IInkOverlayEvents, and \_IInkPictureEvents dispatch-only interfaces (dispinterfaces) with an ID of DISPID\_IPEMouseWheel.</span></span>

## <a name="requirements"></a><span data-ttu-id="ba0df-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ba0df-127">Requirements</span></span>



| <span data-ttu-id="ba0df-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="ba0df-128">Requirement</span></span> | <span data-ttu-id="ba0df-129">Valor</span><span class="sxs-lookup"><span data-stu-id="ba0df-129">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ba0df-130">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ba0df-130">Minimum supported client</span></span><br/> | <span data-ttu-id="ba0df-131">Somente aplicativos de área de trabalho do Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="ba0df-131">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="ba0df-132">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ba0df-132">Minimum supported server</span></span><br/> | <span data-ttu-id="ba0df-133">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="ba0df-133">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="ba0df-134">parâmetro</span><span class="sxs-lookup"><span data-stu-id="ba0df-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="ba0df-135"><dt>Msinkaut. h (também requer Msinkaut \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="ba0df-135"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="ba0df-136">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="ba0df-136">Library</span></span><br/>                  | <dl> <span data-ttu-id="ba0df-137"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ba0df-137"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="ba0df-138">Confira também</span><span class="sxs-lookup"><span data-stu-id="ba0df-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ba0df-139">**Classe InkOverlay**</span><span class="sxs-lookup"><span data-stu-id="ba0df-139">**InkOverlay Class**</span></span>](inkoverlay-class.md)
</dt> <dt>

[<span data-ttu-id="ba0df-140">**Enumeração InkMouseButton**</span><span class="sxs-lookup"><span data-stu-id="ba0df-140">**InkMouseButton Enumeration**</span></span>](/windows/desktop/api/msinkaut/ne-msinkaut-inkmousebutton)
</dt> <dt>

[<span data-ttu-id="ba0df-141">**Enumeração InkShiftKeyModifierFlags**</span><span class="sxs-lookup"><span data-stu-id="ba0df-141">**InkShiftKeyModifierFlags Enumeration**</span></span>](/windows/desktop/api/msinkaut/ne-msinkaut-inkshiftkeymodifierflags)
</dt> </dl>

 

 




