---
description: Ocorre quando a roda do mouse se move enquanto o objeto InkCollector ou InkOverlay tem foco.
ms.assetid: 418cf67c-0ec0-49e3-a17f-9eaeb40bb602
title: Evento InkCollector. MouseWheel (Msinkaut. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 401e6a6728bfcbe058ff5eab56499f6c8e885351
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105765699"
---
# <a name="inkcollectormousewheel-event"></a><span data-ttu-id="d6f34-103">Evento InkCollector. MouseWheel</span><span class="sxs-lookup"><span data-stu-id="d6f34-103">InkCollector.MouseWheel event</span></span>

<span data-ttu-id="d6f34-104">Ocorre quando a roda do mouse se move enquanto o objeto [**InkCollector**](inkcollector-class.md) ou [**InkOverlay**](inkoverlay-class.md) tem foco.</span><span class="sxs-lookup"><span data-stu-id="d6f34-104">Occurs when the mouse wheel moves while the [**InkCollector**](inkcollector-class.md) or [**InkOverlay**](inkoverlay-class.md) object has focus.</span></span>

## <a name="syntax"></a><span data-ttu-id="d6f34-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="d6f34-105">Syntax</span></span>


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



## <a name="parameters"></a><span data-ttu-id="d6f34-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="d6f34-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d6f34-107">*Botão* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="d6f34-107">*Button* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d6f34-108">O botão do mouse que foi pressionado.</span><span class="sxs-lookup"><span data-stu-id="d6f34-108">The mouse button that was pressed.</span></span>

</dd> <dt>

<span data-ttu-id="d6f34-109">*Shift* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="d6f34-109">*Shift* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d6f34-110">O estado da tecla SHIFT.</span><span class="sxs-lookup"><span data-stu-id="d6f34-110">The state of the SHIFT key.</span></span>

</dd> <dt>

<span data-ttu-id="d6f34-111">*Delta* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="d6f34-111">*Delta* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d6f34-112">Uma contagem assinada do número de tentativas que a roda do mouse gira.</span><span class="sxs-lookup"><span data-stu-id="d6f34-112">A signed count of the number of detents the mouse wheel has rotated.</span></span> <span data-ttu-id="d6f34-113">Um detentor é um ponto da roda do mouse.</span><span class="sxs-lookup"><span data-stu-id="d6f34-113">A detent is one notch of the mouse wheel.</span></span>

</dd> <dt>

<span data-ttu-id="d6f34-114">*x* \[ em\]</span><span class="sxs-lookup"><span data-stu-id="d6f34-114">*x* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d6f34-115">A coordenada x, em pixels, de um clique do mouse.</span><span class="sxs-lookup"><span data-stu-id="d6f34-115">The x-coordinate, in pixels, of a mouse click.</span></span>

</dd> <dt>

<span data-ttu-id="d6f34-116">*y* \[ em\]</span><span class="sxs-lookup"><span data-stu-id="d6f34-116">*y* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d6f34-117">A coordenada y, em pixels, de um clique do mouse.</span><span class="sxs-lookup"><span data-stu-id="d6f34-117">The y-coordinate, in pixels, of a mouse click.</span></span>

</dd> <dt>

<span data-ttu-id="d6f34-118">*Cancelar* \[ entrada, saída\]</span><span class="sxs-lookup"><span data-stu-id="d6f34-118">*Cancel* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="d6f34-119">**Variante \_ TRUE** para cancelar o evento para o controle pai; caso contrário, **Variant \_ false**.</span><span class="sxs-lookup"><span data-stu-id="d6f34-119">**VARIANT\_TRUE** to cancel the event for the parent control; otherwise, **VARIANT\_FALSE**.</span></span> <span data-ttu-id="d6f34-120">O valor padrão é **Variant \_ false**.</span><span class="sxs-lookup"><span data-stu-id="d6f34-120">The default value is **VARIANT\_FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d6f34-121">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="d6f34-121">Return value</span></span>

<span data-ttu-id="d6f34-122">Esse evento não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="d6f34-122">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="d6f34-123">Comentários</span><span class="sxs-lookup"><span data-stu-id="d6f34-123">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="d6f34-124">As propriedades *PX* e *pY* estão em pixels, e não as unidades HIMETRIC associadas ao espaço de tinta.</span><span class="sxs-lookup"><span data-stu-id="d6f34-124">The properties *pX* and *pY* are in pixels, and not the HIMETRIC units that are associated with the ink space.</span></span> <span data-ttu-id="d6f34-125">Isso ocorre porque esse evento substitui o evento de mouse relacionado de um aplicativo sem reconhecimento de caneta e esse tipo de aplicativo compreende apenas os pixels.</span><span class="sxs-lookup"><span data-stu-id="d6f34-125">This is because this event replaces the related mouse event of a pen-unaware application and this type of application understands only pixels.</span></span>

 

<span data-ttu-id="d6f34-126">Esse método de evento é definido nas \_ \_ interfaces somente de expedição IInkCollectorEvents, IInkOverlayEvents e \_ IInkPictureEvents (dispinterfaces) com uma ID de IPEMouseWheel de DISPID \_ .</span><span class="sxs-lookup"><span data-stu-id="d6f34-126">This event method is defined in the \_IInkCollectorEvents, \_IInkOverlayEvents, and \_IInkPictureEvents dispatch-only interfaces (dispinterfaces) with an ID of DISPID\_IPEMouseWheel.</span></span>

## <a name="requirements"></a><span data-ttu-id="d6f34-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d6f34-127">Requirements</span></span>



| <span data-ttu-id="d6f34-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="d6f34-128">Requirement</span></span> | <span data-ttu-id="d6f34-129">Valor</span><span class="sxs-lookup"><span data-stu-id="d6f34-129">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d6f34-130">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d6f34-130">Minimum supported client</span></span><br/> | <span data-ttu-id="d6f34-131">Somente aplicativos de área de trabalho do Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="d6f34-131">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="d6f34-132">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d6f34-132">Minimum supported server</span></span><br/> | <span data-ttu-id="d6f34-133">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="d6f34-133">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="d6f34-134">parâmetro</span><span class="sxs-lookup"><span data-stu-id="d6f34-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="d6f34-135"><dt>Msinkaut. h (também requer Msinkaut \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="d6f34-135"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="d6f34-136">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="d6f34-136">Library</span></span><br/>                  | <dl> <span data-ttu-id="d6f34-137"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d6f34-137"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="d6f34-138">Confira também</span><span class="sxs-lookup"><span data-stu-id="d6f34-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d6f34-139">**Classe InkCollector**</span><span class="sxs-lookup"><span data-stu-id="d6f34-139">**InkCollector Class**</span></span>](inkcollector-class.md)
</dt> <dt>

[<span data-ttu-id="d6f34-140">**Enumeração InkMouseButton**</span><span class="sxs-lookup"><span data-stu-id="d6f34-140">**InkMouseButton Enumeration**</span></span>](/windows/desktop/api/msinkaut/ne-msinkaut-inkmousebutton)
</dt> <dt>

[<span data-ttu-id="d6f34-141">**Enumeração InkShiftKeyModifierFlags**</span><span class="sxs-lookup"><span data-stu-id="d6f34-141">**InkShiftKeyModifierFlags Enumeration**</span></span>](/windows/desktop/api/msinkaut/ne-msinkaut-inkshiftkeymodifierflags)
</dt> </dl>

 

 




