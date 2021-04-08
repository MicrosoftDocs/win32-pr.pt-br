---
description: Ocorre quando um IInkTablet é adicionado ao sistema.
ms.assetid: c5f90fce-faf7-411b-a4d6-deb5d0f22f4a
title: Evento InkCollector. TabletAdded (Msinkaut. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f18f66a45570b269d36efc012f543a8b25e23f70
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103920739"
---
# <a name="inkcollectortabletadded-event"></a><span data-ttu-id="f81a3-103">Evento InkCollector. TabletAdded</span><span class="sxs-lookup"><span data-stu-id="f81a3-103">InkCollector.TabletAdded event</span></span>

<span data-ttu-id="f81a3-104">Ocorre quando um [**IInkTablet**](/windows/desktop/api/msinkaut/nn-msinkaut-iinktablet) é adicionado ao sistema.</span><span class="sxs-lookup"><span data-stu-id="f81a3-104">Occurs when a [**IInkTablet**](/windows/desktop/api/msinkaut/nn-msinkaut-iinktablet) is added to the system.</span></span>

## <a name="syntax"></a><span data-ttu-id="f81a3-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="f81a3-105">Syntax</span></span>


```C++
void TabletAdded(
  [in] IInkTablet *Tablet
);
```



## <a name="parameters"></a><span data-ttu-id="f81a3-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="f81a3-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f81a3-107">*Tablet* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="f81a3-107">*Tablet* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f81a3-108">O objeto [**IInkTablet**](/windows/desktop/api/msinkaut/nn-msinkaut-iinktablet) que foi adicionado ao sistema.</span><span class="sxs-lookup"><span data-stu-id="f81a3-108">The [**IInkTablet**](/windows/desktop/api/msinkaut/nn-msinkaut-iinktablet) object that has been added to the system.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f81a3-109">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="f81a3-109">Return value</span></span>

<span data-ttu-id="f81a3-110">Esse evento não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="f81a3-110">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="f81a3-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="f81a3-111">Remarks</span></span>

<span data-ttu-id="f81a3-112">Esse método de evento é definido nas \_ \_ interfaces somente de expedição IInkCollectorEvents, IInkOverlayEvents e \_ IInkPictureEvents (dispinterfaces) com uma ID de ICETabletAdded de DISPID \_ .</span><span class="sxs-lookup"><span data-stu-id="f81a3-112">This event method is defined in the \_IInkCollectorEvents, \_IInkOverlayEvents, and \_IInkPictureEvents dispatch-only interfaces (dispinterfaces) with an ID of DISPID\_ICETabletAdded.</span></span>

## <a name="requirements"></a><span data-ttu-id="f81a3-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f81a3-113">Requirements</span></span>



| <span data-ttu-id="f81a3-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="f81a3-114">Requirement</span></span> | <span data-ttu-id="f81a3-115">Valor</span><span class="sxs-lookup"><span data-stu-id="f81a3-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f81a3-116">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f81a3-116">Minimum supported client</span></span><br/> | <span data-ttu-id="f81a3-117">Somente aplicativos de área de trabalho do Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="f81a3-117">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="f81a3-118">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f81a3-118">Minimum supported server</span></span><br/> | <span data-ttu-id="f81a3-119">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="f81a3-119">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="f81a3-120">parâmetro</span><span class="sxs-lookup"><span data-stu-id="f81a3-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="f81a3-121"><dt>Msinkaut. h (também requer Msinkaut \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="f81a3-121"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="f81a3-122">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="f81a3-122">Library</span></span><br/>                  | <dl> <span data-ttu-id="f81a3-123"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f81a3-123"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="f81a3-124">Confira também</span><span class="sxs-lookup"><span data-stu-id="f81a3-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f81a3-125">**Classe InkCollector**</span><span class="sxs-lookup"><span data-stu-id="f81a3-125">**InkCollector Class**</span></span>](inkcollector-class.md)
</dt> <dt>

[<span data-ttu-id="f81a3-126">**Interface IInkTablet**</span><span class="sxs-lookup"><span data-stu-id="f81a3-126">**IInkTablet Interface**</span></span>](/windows/desktop/api/msinkaut/nn-msinkaut-iinktablet)
</dt> </dl>

 

 




