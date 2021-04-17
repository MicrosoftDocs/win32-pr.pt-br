---
description: Ocorre quando o objeto InkOverlay ou o controle InkPicture concluiu o redesenho.
ms.assetid: de3c69de-4a33-46e4-96e5-462805681bda
title: Evento InkOverlay. pintado (Msinkaut. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3de0628679aa034b16a3562aa08cdbd1928653ad
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104461320"
---
# <a name="inkoverlaypainted-event"></a><span data-ttu-id="9aa2e-103">Evento InkOverlay. pintado</span><span class="sxs-lookup"><span data-stu-id="9aa2e-103">InkOverlay.Painted event</span></span>

<span data-ttu-id="9aa2e-104">Ocorre quando o objeto [**InkOverlay**](inkoverlay-class.md) ou o controle [InkPicture](inkpicture-control-reference.md) concluiu o redesenho.</span><span class="sxs-lookup"><span data-stu-id="9aa2e-104">Occurs when the [**InkOverlay**](inkoverlay-class.md) object or [InkPicture](inkpicture-control-reference.md) control has completed redrawing itself.</span></span>

## <a name="syntax"></a><span data-ttu-id="9aa2e-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="9aa2e-105">Syntax</span></span>


```C++
void Painted(
  [in] long         hDC,
  [in] InkRectangle *Rect
);
```



## <a name="parameters"></a><span data-ttu-id="9aa2e-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="9aa2e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9aa2e-107">*HDC* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="9aa2e-107">*hDC* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9aa2e-108">O contexto do dispositivo no qual o evento ocorreu.</span><span class="sxs-lookup"><span data-stu-id="9aa2e-108">The device context on which the event occurred.</span></span>

</dd> <dt>

<span data-ttu-id="9aa2e-109">*Rect* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="9aa2e-109">*Rect* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9aa2e-110">O [**InkRectangle**](inkrectangle-class.md) que foi redesenhado.</span><span class="sxs-lookup"><span data-stu-id="9aa2e-110">The [**InkRectangle**](inkrectangle-class.md) that was repainted.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9aa2e-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="9aa2e-111">Return value</span></span>

<span data-ttu-id="9aa2e-112">Esse evento não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="9aa2e-112">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="9aa2e-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="9aa2e-113">Remarks</span></span>

<span data-ttu-id="9aa2e-114">Esse método de evento é definido nas \_ \_ interfaces somente de expedição IInkOverlayEvents e IInkPictureEvents (dispinterfaces) com uma ID de DISPID \_ IOEPainted.</span><span class="sxs-lookup"><span data-stu-id="9aa2e-114">This event method is defined in the \_IInkOverlayEvents and \_IInkPictureEvents dispatch-only interfaces (dispinterfaces) with an ID of DISPID\_IOEPainted.</span></span>

## <a name="requirements"></a><span data-ttu-id="9aa2e-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9aa2e-115">Requirements</span></span>



| <span data-ttu-id="9aa2e-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="9aa2e-116">Requirement</span></span> | <span data-ttu-id="9aa2e-117">Valor</span><span class="sxs-lookup"><span data-stu-id="9aa2e-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9aa2e-118">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="9aa2e-118">Minimum supported client</span></span><br/> | <span data-ttu-id="9aa2e-119">Somente aplicativos de área de trabalho do Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="9aa2e-119">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="9aa2e-120">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="9aa2e-120">Minimum supported server</span></span><br/> | <span data-ttu-id="9aa2e-121">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="9aa2e-121">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="9aa2e-122">parâmetro</span><span class="sxs-lookup"><span data-stu-id="9aa2e-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="9aa2e-123"><dt>Msinkaut. h (também requer Msinkaut \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="9aa2e-123"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="9aa2e-124">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="9aa2e-124">Library</span></span><br/>                  | <dl> <span data-ttu-id="9aa2e-125"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9aa2e-125"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="9aa2e-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="9aa2e-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9aa2e-127">**Classe InkOverlay**</span><span class="sxs-lookup"><span data-stu-id="9aa2e-127">**InkOverlay Class**</span></span>](inkoverlay-class.md)
</dt> </dl>

 

 




