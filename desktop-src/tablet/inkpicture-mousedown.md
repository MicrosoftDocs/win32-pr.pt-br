---
description: Ocorre quando o ponteiro do mouse está sobre o controle InkPicture e um botão do mouse é pressionado.
ms.assetid: ff776b2b-7dd8-4d3d-b0f6-714b186d447e
title: Evento InkPicture. MouseDown (Msinkaut. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 40e4459f5c304b3350f9cbad6aba69418bd24844
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104170468"
---
# <a name="inkpicturemousedown-event"></a><span data-ttu-id="77fac-103">Evento InkPicture. MouseDown</span><span class="sxs-lookup"><span data-stu-id="77fac-103">InkPicture.MouseDown event</span></span>

<span data-ttu-id="77fac-104">Ocorre quando o ponteiro do mouse está sobre o controle [InkPicture](inkpicture-control-reference.md) e um botão do mouse é pressionado.</span><span class="sxs-lookup"><span data-stu-id="77fac-104">Occurs when the mouse pointer is over the [InkPicture](inkpicture-control-reference.md) control and a mouse button is pressed.</span></span>

## <a name="syntax"></a><span data-ttu-id="77fac-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="77fac-105">Syntax</span></span>


```C++
void MouseDown(
  [in]      InkMouseButton           Button,
  [in]      InkShiftKeyModifierFlags Shift,
  [in]      long                     pX,
  [in]      long                     pY,
  [in, out] VARIANT_BOOL             *Cancel
);
```



## <a name="parameters"></a><span data-ttu-id="77fac-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="77fac-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="77fac-107">*Botão* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="77fac-107">*Button* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="77fac-108">O botão que foi pressionado.</span><span class="sxs-lookup"><span data-stu-id="77fac-108">The button that was pressed.</span></span>

</dd> <dt>

<span data-ttu-id="77fac-109">*Shift* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="77fac-109">*Shift* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="77fac-110">O estado da tecla SHIFT.</span><span class="sxs-lookup"><span data-stu-id="77fac-110">The state of the SHIFT key.</span></span>

</dd> <dt>

<span data-ttu-id="77fac-111">*PX* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="77fac-111">*pX* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="77fac-112">A coordenada x, em pixels, do objeto [**IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) .</span><span class="sxs-lookup"><span data-stu-id="77fac-112">The x-coordinate, in pixels, of the [**IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) object.</span></span>

</dd> <dt>

<span data-ttu-id="77fac-113">*pY* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="77fac-113">*pY* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="77fac-114">A coordenada y, em pixels, do objeto [**IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) .</span><span class="sxs-lookup"><span data-stu-id="77fac-114">The y-coordinate, in pixels, of the [**IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) object.</span></span>

</dd> <dt>

<span data-ttu-id="77fac-115">*Cancelar* \[ entrada, saída\]</span><span class="sxs-lookup"><span data-stu-id="77fac-115">*Cancel* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="77fac-116">**Variante \_ TRUE** para cancelar este evento para o controle pai; caso contrário, **Variant \_ false**.</span><span class="sxs-lookup"><span data-stu-id="77fac-116">**VARIANT\_TRUE** to cancel this event for the parent control; otherwise, **VARIANT\_FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="77fac-117">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="77fac-117">Return value</span></span>

<span data-ttu-id="77fac-118">Esse evento não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="77fac-118">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="77fac-119">Comentários</span><span class="sxs-lookup"><span data-stu-id="77fac-119">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="77fac-120">Os parâmetros pX e pY estão em pixels, e não as unidades HIMETRIC associadas ao sistema de coordenadas do espaço de tinta.</span><span class="sxs-lookup"><span data-stu-id="77fac-120">The parameters pX and pY are in pixels, and not the HIMETRIC units that are associated with the ink space coordinate system.</span></span> <span data-ttu-id="77fac-121">Isso ocorre porque esse evento substitui o evento de mouse relacionado de um aplicativo que não reconhece a caneta e esse tipo de aplicativo refere-se apenas a pixels.</span><span class="sxs-lookup"><span data-stu-id="77fac-121">This is because this event replaces the related mouse event of an application that is not pen-aware, and that type of application refers only to pixels.</span></span>

 

> [!Caution]  
> <span data-ttu-id="77fac-122">Alguns controles dependem de uma relação específica entre os eventos **MouseDown**, [**MouseMove**](inkpicture-mousemove.md)e [**MouseUp**](inkpicture-mouseup.md) .</span><span class="sxs-lookup"><span data-stu-id="77fac-122">Some controls rely on a specific relationship between **MouseDown**, [**MouseMove**](inkpicture-mousemove.md), and [**MouseUp**](inkpicture-mouseup.md) events.</span></span> <span data-ttu-id="77fac-123">Cancelar alguns desses eventos pode ter resultados imprevistos.</span><span class="sxs-lookup"><span data-stu-id="77fac-123">Canceling some of these events may have unanticipated results.</span></span>

 

<span data-ttu-id="77fac-124">Esse método de evento é definido na interface **\_ IInkPictureEvents** .</span><span class="sxs-lookup"><span data-stu-id="77fac-124">This event method is defined in the **\_IInkPictureEvents** interface.</span></span> <span data-ttu-id="77fac-125">A interface **\_ IInkPictureEvents** implementa a interface [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) com um identificador de \_ IPEMouseDown DISPID.</span><span class="sxs-lookup"><span data-stu-id="77fac-125">The **\_IInkPictureEvents** interface implements the [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interface with an identifier of DISPID\_IPEMouseDown.</span></span>

## <a name="requirements"></a><span data-ttu-id="77fac-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="77fac-126">Requirements</span></span>



| <span data-ttu-id="77fac-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="77fac-127">Requirement</span></span> | <span data-ttu-id="77fac-128">Valor</span><span class="sxs-lookup"><span data-stu-id="77fac-128">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="77fac-129">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="77fac-129">Minimum supported client</span></span><br/> | <span data-ttu-id="77fac-130">Somente aplicativos de área de trabalho do Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="77fac-130">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="77fac-131">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="77fac-131">Minimum supported server</span></span><br/> | <span data-ttu-id="77fac-132">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="77fac-132">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="77fac-133">parâmetro</span><span class="sxs-lookup"><span data-stu-id="77fac-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="77fac-134"><dt>Msinkaut. h (também requer Msinkaut \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="77fac-134"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="77fac-135">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="77fac-135">Library</span></span><br/>                  | <dl> <span data-ttu-id="77fac-136"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="77fac-136"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="77fac-137">Confira também</span><span class="sxs-lookup"><span data-stu-id="77fac-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="77fac-138">InkPicture</span><span class="sxs-lookup"><span data-stu-id="77fac-138">InkPicture</span></span>](inkpicture-control-reference.md)
</dt> </dl>

 

