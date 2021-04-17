---
description: Ocorre quando o ponteiro do mouse é movido sobre o controle InkPicture e um botão do mouse é liberado.
ms.assetid: 5e49acc8-1ce1-45ff-b87c-04bdc653156a
title: Evento InkPicture. MouseUp (Msinkaut. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bf652e1ad4110afb4819e5326a5a19a894a310a2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105791584"
---
# <a name="inkpicturemouseup-event"></a><span data-ttu-id="3b6d1-103">Evento InkPicture. MouseUp</span><span class="sxs-lookup"><span data-stu-id="3b6d1-103">InkPicture.MouseUp event</span></span>

<span data-ttu-id="3b6d1-104">Ocorre quando o ponteiro do mouse é movido sobre o controle [InkPicture](inkpicture-control-reference.md) e um botão do mouse é liberado.</span><span class="sxs-lookup"><span data-stu-id="3b6d1-104">Occurs when the mouse pointer is moved over the [InkPicture](inkpicture-control-reference.md) control and a mouse button is released.</span></span>

## <a name="syntax"></a><span data-ttu-id="3b6d1-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="3b6d1-105">Syntax</span></span>


```C++
void MouseUp(
  [in]      InkMouseButton           Button,
  [in]      InkShiftKeyModifierFlags Shift,
  [in]      long                     pX,
  [in]      long                     pY,
  [in, out] VARIANT_BOOL             *Cancel
);
```



## <a name="parameters"></a><span data-ttu-id="3b6d1-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="3b6d1-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3b6d1-107">*Botão* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="3b6d1-107">*Button* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3b6d1-108">O botão que foi pressionado.</span><span class="sxs-lookup"><span data-stu-id="3b6d1-108">The button that was pressed.</span></span>

</dd> <dt>

<span data-ttu-id="3b6d1-109">*Shift* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="3b6d1-109">*Shift* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3b6d1-110">O estado da tecla SHIFT.</span><span class="sxs-lookup"><span data-stu-id="3b6d1-110">The state of the SHIFT key.</span></span>

</dd> <dt>

<span data-ttu-id="3b6d1-111">*PX* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="3b6d1-111">*pX* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3b6d1-112">A coordenada x, em pixels, do objeto [**IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) .</span><span class="sxs-lookup"><span data-stu-id="3b6d1-112">The x-coordinate, in pixels, of the [**IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) object.</span></span>

</dd> <dt>

<span data-ttu-id="3b6d1-113">*pY* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="3b6d1-113">*pY* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3b6d1-114">A coordenada y, em pixels, do objeto [**IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) .</span><span class="sxs-lookup"><span data-stu-id="3b6d1-114">The y-coordinate, in pixels, of the [**IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) object.</span></span>

</dd> <dt>

<span data-ttu-id="3b6d1-115">*Cancelar* \[ entrada, saída\]</span><span class="sxs-lookup"><span data-stu-id="3b6d1-115">*Cancel* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="3b6d1-116">**Variante \_ TRUE** para cancelar o evento MouseUp para o controle pai; caso contrário, **Variant \_ false**.</span><span class="sxs-lookup"><span data-stu-id="3b6d1-116">**VARIANT\_TRUE** to cancel the MouseUp event for the parent control; otherwise, **VARIANT\_FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3b6d1-117">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="3b6d1-117">Return value</span></span>

<span data-ttu-id="3b6d1-118">Esse evento não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="3b6d1-118">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="3b6d1-119">Comentários</span><span class="sxs-lookup"><span data-stu-id="3b6d1-119">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="3b6d1-120">Os parâmetros *PX* e *pY* estão em pixels, e não as unidades HIMETRIC associadas ao sistema de coordenadas do espaço de tinta.</span><span class="sxs-lookup"><span data-stu-id="3b6d1-120">The parameters *pX* and *pY* are in pixels, and not the HIMETRIC units that are associated with the ink space coordinate system.</span></span> <span data-ttu-id="3b6d1-121">Isso ocorre porque esse evento substitui o evento de mouse relacionado de um aplicativo que não reconhece a caneta e esse tipo de aplicativo refere-se apenas a pixels.</span><span class="sxs-lookup"><span data-stu-id="3b6d1-121">This is because this event replaces the related mouse event of an application that is not pen-aware, and that type of application refers only to pixels.</span></span>

 

> [!Caution]  
> <span data-ttu-id="3b6d1-122">Alguns controles dependem de uma relação específica entre os eventos [**MouseDown**](inkpicture-mousedown.md), [**MouseMove**](inkpicture-mousemove.md)e **MouseUp** .</span><span class="sxs-lookup"><span data-stu-id="3b6d1-122">Some controls rely on a specific relationship between [**MouseDown**](inkpicture-mousedown.md), [**MouseMove**](inkpicture-mousemove.md), and **MouseUp** events.</span></span> <span data-ttu-id="3b6d1-123">Cancelar alguns desses eventos pode ter resultados imprevistos.</span><span class="sxs-lookup"><span data-stu-id="3b6d1-123">Canceling some of these events may have unanticipated results.</span></span>

 

<span data-ttu-id="3b6d1-124">Esse método de evento é definido na interface **\_ IInkPictureEvents** .</span><span class="sxs-lookup"><span data-stu-id="3b6d1-124">This event method is defined in the **\_IInkPictureEvents** interface.</span></span> <span data-ttu-id="3b6d1-125">A interface **\_ IInkPictureEvents** implementa a interface [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) com um identificador de \_ IPEMouseDown DISPID.</span><span class="sxs-lookup"><span data-stu-id="3b6d1-125">The **\_IInkPictureEvents** interface implements the [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interface with an identifier of DISPID\_IPEMouseDown.</span></span>

## <a name="requirements"></a><span data-ttu-id="3b6d1-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3b6d1-126">Requirements</span></span>



| <span data-ttu-id="3b6d1-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="3b6d1-127">Requirement</span></span> | <span data-ttu-id="3b6d1-128">Valor</span><span class="sxs-lookup"><span data-stu-id="3b6d1-128">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3b6d1-129">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3b6d1-129">Minimum supported client</span></span><br/> | <span data-ttu-id="3b6d1-130">Somente aplicativos de área de trabalho do Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="3b6d1-130">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="3b6d1-131">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3b6d1-131">Minimum supported server</span></span><br/> | <span data-ttu-id="3b6d1-132">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="3b6d1-132">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="3b6d1-133">parâmetro</span><span class="sxs-lookup"><span data-stu-id="3b6d1-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="3b6d1-134"><dt>Msinkaut. h (também requer Msinkaut \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="3b6d1-134"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="3b6d1-135">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="3b6d1-135">Library</span></span><br/>                  | <dl> <span data-ttu-id="3b6d1-136"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3b6d1-136"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="3b6d1-137">Confira também</span><span class="sxs-lookup"><span data-stu-id="3b6d1-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3b6d1-138">InkPicture</span><span class="sxs-lookup"><span data-stu-id="3b6d1-138">InkPicture</span></span>](inkpicture-control-reference.md)
</dt> </dl>

 

