---
description: Evento InkOverlay. TabletAdded – ocorre quando um IInkTablet é adicionado ao sistema.
ms.assetid: 2076a520-bd37-43b5-b57f-030828b096cb
title: Evento InkOverlay. TabletAdded (Msinkaut. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3c22630430622c98026c81adb1c6a131a53277a4
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108116784"
---
# <a name="inkoverlaytabletadded-event"></a><span data-ttu-id="37d0e-103">Evento InkOverlay. TabletAdded</span><span class="sxs-lookup"><span data-stu-id="37d0e-103">InkOverlay.TabletAdded event</span></span>

<span data-ttu-id="37d0e-104">Ocorre quando um [**IInkTablet**](/windows/desktop/api/msinkaut/nn-msinkaut-iinktablet) é adicionado ao sistema.</span><span class="sxs-lookup"><span data-stu-id="37d0e-104">Occurs when a [**IInkTablet**](/windows/desktop/api/msinkaut/nn-msinkaut-iinktablet) is added to the system.</span></span>

## <a name="syntax"></a><span data-ttu-id="37d0e-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="37d0e-105">Syntax</span></span>


```C++
void TabletAdded(
  [in] IInkTablet *Tablet
);
```



## <a name="parameters"></a><span data-ttu-id="37d0e-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="37d0e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="37d0e-107">*Tablet* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="37d0e-107">*Tablet* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="37d0e-108">O objeto [**IInkTablet**](/windows/desktop/api/msinkaut/nn-msinkaut-iinktablet) que foi adicionado ao sistema.</span><span class="sxs-lookup"><span data-stu-id="37d0e-108">The [**IInkTablet**](/windows/desktop/api/msinkaut/nn-msinkaut-iinktablet) object that has been added to the system.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="37d0e-109">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="37d0e-109">Return value</span></span>

<span data-ttu-id="37d0e-110">Esse evento não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="37d0e-110">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="37d0e-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="37d0e-111">Remarks</span></span>

<span data-ttu-id="37d0e-112">Esse método de evento é definido nas \_ \_ interfaces somente de expedição IInkCollectorEvents, IInkOverlayEvents e \_ IInkPictureEvents (dispinterfaces) com uma ID de ICETabletAdded de DISPID \_ .</span><span class="sxs-lookup"><span data-stu-id="37d0e-112">This event method is defined in the \_IInkCollectorEvents, \_IInkOverlayEvents, and \_IInkPictureEvents dispatch-only interfaces (dispinterfaces) with an ID of DISPID\_ICETabletAdded.</span></span>

## <a name="requirements"></a><span data-ttu-id="37d0e-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="37d0e-113">Requirements</span></span>



| <span data-ttu-id="37d0e-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="37d0e-114">Requirement</span></span> | <span data-ttu-id="37d0e-115">Valor</span><span class="sxs-lookup"><span data-stu-id="37d0e-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="37d0e-116">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="37d0e-116">Minimum supported client</span></span><br/> | <span data-ttu-id="37d0e-117">Somente aplicativos de área de trabalho do Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="37d0e-117">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="37d0e-118">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="37d0e-118">Minimum supported server</span></span><br/> | <span data-ttu-id="37d0e-119">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="37d0e-119">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="37d0e-120">parâmetro</span><span class="sxs-lookup"><span data-stu-id="37d0e-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="37d0e-121"><dt>Msinkaut. h (também requer Msinkaut \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="37d0e-121"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="37d0e-122">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="37d0e-122">Library</span></span><br/>                  | <dl> <span data-ttu-id="37d0e-123"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="37d0e-123"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="37d0e-124">Consulte também</span><span class="sxs-lookup"><span data-stu-id="37d0e-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="37d0e-125">**Classe InkOverlay**</span><span class="sxs-lookup"><span data-stu-id="37d0e-125">**InkOverlay Class**</span></span>](inkoverlay-class.md)
</dt> <dt>

[<span data-ttu-id="37d0e-126">**Interface IInkTablet**</span><span class="sxs-lookup"><span data-stu-id="37d0e-126">**IInkTablet Interface**</span></span>](/windows/desktop/api/msinkaut/nn-msinkaut-iinktablet)
</dt> </dl>

 

 




