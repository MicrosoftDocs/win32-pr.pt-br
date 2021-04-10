---
description: Ocorre antes de o controle InkPicture ser redesenhado.
ms.assetid: 97d017ce-fdab-49e5-9ea6-0bcc5d7b14fb
title: Evento InkPicture. Pintation (Msinkaut. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3dc76bbf3079d61c84ac14d1b22690d645a7cce4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104170076"
---
# <a name="inkpicturepainting-event"></a><span data-ttu-id="6cb3b-103">Evento InkPicture. Pintation</span><span class="sxs-lookup"><span data-stu-id="6cb3b-103">InkPicture.Painting event</span></span>

<span data-ttu-id="6cb3b-104">Ocorre antes de o controle [InkPicture](inkpicture-control-reference.md) ser redesenhado.</span><span class="sxs-lookup"><span data-stu-id="6cb3b-104">Occurs before the [InkPicture](inkpicture-control-reference.md) control redraws itself.</span></span>

## <a name="syntax"></a><span data-ttu-id="6cb3b-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="6cb3b-105">Syntax</span></span>


```C++
void Painting(
  [in]      long          hDC,
  [in]      IInkRectangle *Rect,
  [in, out] VARIANT_BOOL  *Allow
);
```



## <a name="parameters"></a><span data-ttu-id="6cb3b-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="6cb3b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6cb3b-107">*HDC* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="6cb3b-107">*hDC* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6cb3b-108">O contexto do dispositivo no qual a pintura ocorrerá.</span><span class="sxs-lookup"><span data-stu-id="6cb3b-108">The device context on which painting will occur.</span></span>

</dd> <dt>

<span data-ttu-id="6cb3b-109">*Rect* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="6cb3b-109">*Rect* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6cb3b-110">O retângulo de tinta que deve ser redesenhado.</span><span class="sxs-lookup"><span data-stu-id="6cb3b-110">The ink rectangle that is to be repainted.</span></span>

</dd> <dt>

<span data-ttu-id="6cb3b-111">*Permitir* \[ entrada, saída\]</span><span class="sxs-lookup"><span data-stu-id="6cb3b-111">*Allow* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="6cb3b-112">Se o redesenho ocorrerá.</span><span class="sxs-lookup"><span data-stu-id="6cb3b-112">Whether the repaint will occur.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6cb3b-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="6cb3b-113">Return value</span></span>

<span data-ttu-id="6cb3b-114">Esse evento não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="6cb3b-114">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="6cb3b-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="6cb3b-115">Remarks</span></span>

<span data-ttu-id="6cb3b-116">Esse método de evento é definido nas interfaces somente de expedição **\_ IInkOverlayEvents** e **\_ IInkPictureEvents** (dispinterfaces) com uma ID de DISPID \_ IOEPainting.</span><span class="sxs-lookup"><span data-stu-id="6cb3b-116">This event method is defined in the **\_IInkOverlayEvents** and **\_IInkPictureEvents** dispatch-only interfaces (dispinterfaces) with an ID of DISPID\_IOEPainting.</span></span>

## <a name="requirements"></a><span data-ttu-id="6cb3b-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6cb3b-117">Requirements</span></span>



| <span data-ttu-id="6cb3b-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="6cb3b-118">Requirement</span></span> | <span data-ttu-id="6cb3b-119">Valor</span><span class="sxs-lookup"><span data-stu-id="6cb3b-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6cb3b-120">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6cb3b-120">Minimum supported client</span></span><br/> | <span data-ttu-id="6cb3b-121">Somente aplicativos de área de trabalho do Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="6cb3b-121">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="6cb3b-122">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6cb3b-122">Minimum supported server</span></span><br/> | <span data-ttu-id="6cb3b-123">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="6cb3b-123">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="6cb3b-124">parâmetro</span><span class="sxs-lookup"><span data-stu-id="6cb3b-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="6cb3b-125"><dt>Msinkaut. h (também requer Msinkaut \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="6cb3b-125"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="6cb3b-126">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="6cb3b-126">Library</span></span><br/>                  | <dl> <span data-ttu-id="6cb3b-127"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6cb3b-127"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="6cb3b-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="6cb3b-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6cb3b-129">InkPicture</span><span class="sxs-lookup"><span data-stu-id="6cb3b-129">InkPicture</span></span>](inkpicture-control-reference.md)
</dt> </dl>

 

 




