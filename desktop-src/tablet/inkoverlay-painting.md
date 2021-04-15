---
description: Ocorre antes que o objeto InkOverlay ou InkPicture tenha concluído o redesenho.
ms.assetid: abfd37fb-2d2b-4d60-96a1-08f68b73417b
title: Evento InkOverlay. Pintation (Msinkaut. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5fc056667f88c0631e84a76767fc97f90ca05a98
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104506144"
---
# <a name="inkoverlaypainting-event"></a><span data-ttu-id="a5e2e-103">Evento InkOverlay. Pintation</span><span class="sxs-lookup"><span data-stu-id="a5e2e-103">InkOverlay.Painting event</span></span>

<span data-ttu-id="a5e2e-104">Ocorre antes que o objeto [**InkOverlay**](inkoverlay-class.md) ou [InkPicture](inkpicture-control-reference.md) tenha concluído o redesenho.</span><span class="sxs-lookup"><span data-stu-id="a5e2e-104">Occurs before the [**InkOverlay**](inkoverlay-class.md) object or [InkPicture](inkpicture-control-reference.md) has completed redrawing itself.</span></span>

## <a name="syntax"></a><span data-ttu-id="a5e2e-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="a5e2e-105">Syntax</span></span>


```C++
void Painting(
  [in]      long          hDC,
  [in]      IInkRectangle *Rect,
  [in, out] VARIANT_BOOL  *Allow
);
```



## <a name="parameters"></a><span data-ttu-id="a5e2e-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="a5e2e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a5e2e-107">*HDC* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="a5e2e-107">*hDC* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a5e2e-108">O contexto do dispositivo no qual a pintura ocorrerá.</span><span class="sxs-lookup"><span data-stu-id="a5e2e-108">The device context on which painting will occur.</span></span>

</dd> <dt>

<span data-ttu-id="a5e2e-109">*Rect* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="a5e2e-109">*Rect* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a5e2e-110">O retângulo que será redesenhado.</span><span class="sxs-lookup"><span data-stu-id="a5e2e-110">The rectangle that is to be repainted.</span></span>

</dd> <dt>

<span data-ttu-id="a5e2e-111">*Permitir* \[ entrada, saída\]</span><span class="sxs-lookup"><span data-stu-id="a5e2e-111">*Allow* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="a5e2e-112">Se o redesenho ocorrerá.</span><span class="sxs-lookup"><span data-stu-id="a5e2e-112">Whether the repaint will occur.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a5e2e-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="a5e2e-113">Return value</span></span>

<span data-ttu-id="a5e2e-114">Esse evento não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="a5e2e-114">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="a5e2e-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="a5e2e-115">Remarks</span></span>

<span data-ttu-id="a5e2e-116">Esse método de evento é definido nas \_ \_ interfaces somente de expedição IInkOverlayEvents e IInkPictureEvents (dispinterfaces) com uma ID de DISPID \_ IOEPainting.</span><span class="sxs-lookup"><span data-stu-id="a5e2e-116">This event method is defined in the \_IInkOverlayEvents and \_IInkPictureEvents dispatch-only interfaces (dispinterfaces) with an ID of DISPID\_IOEPainting.</span></span>

## <a name="requirements"></a><span data-ttu-id="a5e2e-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a5e2e-117">Requirements</span></span>



| <span data-ttu-id="a5e2e-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="a5e2e-118">Requirement</span></span> | <span data-ttu-id="a5e2e-119">Valor</span><span class="sxs-lookup"><span data-stu-id="a5e2e-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a5e2e-120">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a5e2e-120">Minimum supported client</span></span><br/> | <span data-ttu-id="a5e2e-121">Somente aplicativos de área de trabalho do Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="a5e2e-121">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="a5e2e-122">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a5e2e-122">Minimum supported server</span></span><br/> | <span data-ttu-id="a5e2e-123">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="a5e2e-123">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="a5e2e-124">parâmetro</span><span class="sxs-lookup"><span data-stu-id="a5e2e-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="a5e2e-125"><dt>Msinkaut. h (também requer Msinkaut \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="a5e2e-125"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="a5e2e-126">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="a5e2e-126">Library</span></span><br/>                  | <dl> <span data-ttu-id="a5e2e-127"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a5e2e-127"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="a5e2e-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="a5e2e-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a5e2e-129">**Classe InkOverlay**</span><span class="sxs-lookup"><span data-stu-id="a5e2e-129">**InkOverlay Class**</span></span>](inkoverlay-class.md)
</dt> </dl>

 

 




