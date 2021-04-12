---
description: Ocorre quando a roda do mouse se move enquanto o controle InkPicture tem foco.
ms.assetid: f56a8af9-7618-4fa3-8dd5-aa81a7f817e4
title: Evento InkPicture. MouseWheel (Msinkaut. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6cab870f3a00b2aa0cea3c003993e2b35cd2abbf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104296871"
---
# <a name="inkpicturemousewheel-event"></a><span data-ttu-id="428d5-103">Evento InkPicture. MouseWheel</span><span class="sxs-lookup"><span data-stu-id="428d5-103">InkPicture.MouseWheel event</span></span>

<span data-ttu-id="428d5-104">Ocorre quando a roda do mouse se move enquanto o controle [InkPicture](inkpicture-control-reference.md) tem foco.</span><span class="sxs-lookup"><span data-stu-id="428d5-104">Occurs when the mouse wheel moves while the [InkPicture](inkpicture-control-reference.md) control has focus.</span></span>

## <a name="syntax"></a><span data-ttu-id="428d5-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="428d5-105">Syntax</span></span>


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



## <a name="parameters"></a><span data-ttu-id="428d5-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="428d5-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="428d5-107">*Botão* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="428d5-107">*Button* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="428d5-108">O botão que foi pressionado.</span><span class="sxs-lookup"><span data-stu-id="428d5-108">The button that was pressed.</span></span>

</dd> <dt>

<span data-ttu-id="428d5-109">*Shift* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="428d5-109">*Shift* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="428d5-110">O estado da tecla SHIFT.</span><span class="sxs-lookup"><span data-stu-id="428d5-110">The state of the SHIFT key.</span></span>

</dd> <dt>

<span data-ttu-id="428d5-111">*Delta* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="428d5-111">*Delta* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="428d5-112">A distância que a roda do mouse ativou.</span><span class="sxs-lookup"><span data-stu-id="428d5-112">The distance that the mouse wheel turned.</span></span>

</dd> <dt>

<span data-ttu-id="428d5-113">*x* \[ em\]</span><span class="sxs-lookup"><span data-stu-id="428d5-113">*x* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="428d5-114">A coordenada x, em pixels, do objeto [**IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) .</span><span class="sxs-lookup"><span data-stu-id="428d5-114">The x-coordinate, in pixels, of the [**IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) object.</span></span>

</dd> <dt>

<span data-ttu-id="428d5-115">*y* \[ em\]</span><span class="sxs-lookup"><span data-stu-id="428d5-115">*y* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="428d5-116">A coordenada y, em pixels, do objeto [**IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) .</span><span class="sxs-lookup"><span data-stu-id="428d5-116">The y-coordinate, in pixels, of the [**IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) object.</span></span>

</dd> <dt>

<span data-ttu-id="428d5-117">*Cancelar* \[ entrada, saída\]</span><span class="sxs-lookup"><span data-stu-id="428d5-117">*Cancel* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="428d5-118">VARIANT \_ true para cancelar o evento **MouseWheel** para o controle pai; caso contrário, Variant \_ false.</span><span class="sxs-lookup"><span data-stu-id="428d5-118">VARIANT\_TRUE to cancel the **MouseWheel** event for the parent control; otherwise, VARIANT\_FALSE.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="428d5-119">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="428d5-119">Return value</span></span>

<span data-ttu-id="428d5-120">Esse evento não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="428d5-120">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="428d5-121">Comentários</span><span class="sxs-lookup"><span data-stu-id="428d5-121">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="428d5-122">Os parâmetros *x* e *y* estão em pixels, e não as unidades HIMETRIC associadas ao sistema de coordenadas do espaço de tinta.</span><span class="sxs-lookup"><span data-stu-id="428d5-122">The parameters *x* and *y* are in pixels, and not the HIMETRIC units that are associated with the ink space coordinate system.</span></span> <span data-ttu-id="428d5-123">Isso ocorre porque esse evento substitui o evento de mouse relacionado de um aplicativo que não reconhece a caneta e esse tipo de aplicativo refere-se apenas a pixels.</span><span class="sxs-lookup"><span data-stu-id="428d5-123">This is because this event replaces the related mouse event of an application that is not pen-aware, and that type of application refers only to pixels.</span></span>

 

<span data-ttu-id="428d5-124">Esse método de evento é definido na interface **\_ IInkPictureEvents** .</span><span class="sxs-lookup"><span data-stu-id="428d5-124">This event method is defined in the **\_IInkPictureEvents** interface.</span></span> <span data-ttu-id="428d5-125">A interface **\_ IInkPictureEvents** implementa a interface [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) com um identificador de \_ IPEMouseWheel DISPID.</span><span class="sxs-lookup"><span data-stu-id="428d5-125">The **\_IInkPictureEvents** interface implements the [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interface with an identifier of DISPID\_IPEMouseWheel.</span></span>

## <a name="requirements"></a><span data-ttu-id="428d5-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="428d5-126">Requirements</span></span>



| <span data-ttu-id="428d5-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="428d5-127">Requirement</span></span> | <span data-ttu-id="428d5-128">Valor</span><span class="sxs-lookup"><span data-stu-id="428d5-128">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="428d5-129">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="428d5-129">Minimum supported client</span></span><br/> | <span data-ttu-id="428d5-130">Somente aplicativos de área de trabalho do Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="428d5-130">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="428d5-131">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="428d5-131">Minimum supported server</span></span><br/> | <span data-ttu-id="428d5-132">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="428d5-132">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="428d5-133">parâmetro</span><span class="sxs-lookup"><span data-stu-id="428d5-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="428d5-134"><dt>Msinkaut. h (também requer Msinkaut \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="428d5-134"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="428d5-135">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="428d5-135">Library</span></span><br/>                  | <dl> <span data-ttu-id="428d5-136"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="428d5-136"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="428d5-137">Confira também</span><span class="sxs-lookup"><span data-stu-id="428d5-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="428d5-138">InkPicture</span><span class="sxs-lookup"><span data-stu-id="428d5-138">InkPicture</span></span>](inkpicture-control-reference.md)
</dt> </dl>

 

