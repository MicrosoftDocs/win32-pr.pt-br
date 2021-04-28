---
description: Evento InkCollector. TabletRemoved – ocorre quando um IInkTablet é removido do sistema.
ms.assetid: 659a9809-fe35-4d34-aa95-af353998c350
title: Evento InkCollector. TabletRemoved (Msinkaut. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: df76c27b1a0d47e456f69a789d17ef6343706284
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108109994"
---
# <a name="inkcollectortabletremoved-event"></a><span data-ttu-id="b1edd-103">Evento InkCollector. TabletRemoved</span><span class="sxs-lookup"><span data-stu-id="b1edd-103">InkCollector.TabletRemoved event</span></span>

<span data-ttu-id="b1edd-104">Ocorre quando um [**IInkTablet**](/windows/desktop/api/msinkaut/nn-msinkaut-iinktablet) é removido do sistema.</span><span class="sxs-lookup"><span data-stu-id="b1edd-104">Occurs when a [**IInkTablet**](/windows/desktop/api/msinkaut/nn-msinkaut-iinktablet) is removed from the system.</span></span>

## <a name="syntax"></a><span data-ttu-id="b1edd-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="b1edd-105">Syntax</span></span>


```C++
void TabletRemoved(
  [in] long TabletId
);
```



## <a name="parameters"></a><span data-ttu-id="b1edd-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="b1edd-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b1edd-107">*TabletId* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="b1edd-107">*TabletId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b1edd-108">O valor longo que foi usado como a ID do objeto [**IInkTablet**](/windows/desktop/api/msinkaut/nn-msinkaut-iinktablet) que foi removido.</span><span class="sxs-lookup"><span data-stu-id="b1edd-108">The long value that was used as the ID for the [**IInkTablet**](/windows/desktop/api/msinkaut/nn-msinkaut-iinktablet) object that was removed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b1edd-109">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="b1edd-109">Return value</span></span>

<span data-ttu-id="b1edd-110">Esse evento não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="b1edd-110">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="b1edd-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="b1edd-111">Remarks</span></span>

<span data-ttu-id="b1edd-112">Esse método de evento é definido nas \_ \_ interfaces somente de expedição IInkCollectorEvents, IInkOverlayEvents e \_ IInkPictureEvents (dispinterfaces) com uma ID de ICETabletRemoved de DISPID \_ .</span><span class="sxs-lookup"><span data-stu-id="b1edd-112">This event method is defined in the \_IInkCollectorEvents, \_IInkOverlayEvents, and \_IInkPictureEvents dispatch-only interfaces (dispinterfaces) with an ID of DISPID\_ICETabletRemoved.</span></span>

## <a name="requirements"></a><span data-ttu-id="b1edd-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b1edd-113">Requirements</span></span>



| <span data-ttu-id="b1edd-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="b1edd-114">Requirement</span></span> | <span data-ttu-id="b1edd-115">Valor</span><span class="sxs-lookup"><span data-stu-id="b1edd-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b1edd-116">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b1edd-116">Minimum supported client</span></span><br/> | <span data-ttu-id="b1edd-117">Somente aplicativos de área de trabalho do Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="b1edd-117">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="b1edd-118">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b1edd-118">Minimum supported server</span></span><br/> | <span data-ttu-id="b1edd-119">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="b1edd-119">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="b1edd-120">parâmetro</span><span class="sxs-lookup"><span data-stu-id="b1edd-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="b1edd-121"><dt>Msinkaut. h (também requer Msinkaut \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="b1edd-121"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="b1edd-122">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="b1edd-122">Library</span></span><br/>                  | <dl> <span data-ttu-id="b1edd-123"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b1edd-123"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="b1edd-124">Consulte também</span><span class="sxs-lookup"><span data-stu-id="b1edd-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b1edd-125">**Classe InkCollector**</span><span class="sxs-lookup"><span data-stu-id="b1edd-125">**InkCollector Class**</span></span>](inkcollector-class.md)
</dt> <dt>

[<span data-ttu-id="b1edd-126">**Interface IInkTablet**</span><span class="sxs-lookup"><span data-stu-id="b1edd-126">**IInkTablet Interface**</span></span>](/windows/desktop/api/msinkaut/nn-msinkaut-iinktablet)
</dt> </dl>

 

 




