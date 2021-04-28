---
description: Evento InkPicture. TabletRemoved – ocorre quando um IInkTablet é removido do sistema.
ms.assetid: 9a4640a7-cbd9-4304-88c6-86036423628d
title: Evento InkPicture. TabletRemoved (Msinkaut. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 929458c6b972143852b5921a8c8364a54a4b6f41
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108113644"
---
# <a name="inkpicturetabletremoved-event"></a><span data-ttu-id="d6a1d-103">Evento InkPicture. TabletRemoved</span><span class="sxs-lookup"><span data-stu-id="d6a1d-103">InkPicture.TabletRemoved event</span></span>

<span data-ttu-id="d6a1d-104">Ocorre quando um [**IInkTablet**](/windows/desktop/api/msinkaut/nn-msinkaut-iinktablet) é removido do sistema.</span><span class="sxs-lookup"><span data-stu-id="d6a1d-104">Occurs when a [**IInkTablet**](/windows/desktop/api/msinkaut/nn-msinkaut-iinktablet) is removed from the system.</span></span>

## <a name="syntax"></a><span data-ttu-id="d6a1d-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="d6a1d-105">Syntax</span></span>


```C++
void TabletRemoved(
  [in] long TabletId
);
```



## <a name="parameters"></a><span data-ttu-id="d6a1d-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="d6a1d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d6a1d-107">*TabletId* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="d6a1d-107">*TabletId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d6a1d-108">O valor longo que foi usado como a ID do objeto [**IInkTablet**](/windows/desktop/api/msinkaut/nn-msinkaut-iinktablet) que foi removido.</span><span class="sxs-lookup"><span data-stu-id="d6a1d-108">The long value that was used as the ID for the [**IInkTablet**](/windows/desktop/api/msinkaut/nn-msinkaut-iinktablet) object that was removed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d6a1d-109">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="d6a1d-109">Return value</span></span>

<span data-ttu-id="d6a1d-110">Esse evento não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="d6a1d-110">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="d6a1d-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="d6a1d-111">Remarks</span></span>

<span data-ttu-id="d6a1d-112">Esse método de evento é definido nas interfaces somente de expedição **\_ IInkCollectorEvents**, **\_ IInkOverlayEvents** e **\_ IInkPictureEvents** (dispinterfaces) com uma ID de ICETabletRemoved de DISPID \_ .</span><span class="sxs-lookup"><span data-stu-id="d6a1d-112">This event method is defined in the **\_IInkCollectorEvents**, **\_IInkOverlayEvents**, and **\_IInkPictureEvents** dispatch-only interfaces (dispinterfaces) with an ID of DISPID\_ICETabletRemoved.</span></span>

## <a name="requirements"></a><span data-ttu-id="d6a1d-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d6a1d-113">Requirements</span></span>



| <span data-ttu-id="d6a1d-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="d6a1d-114">Requirement</span></span> | <span data-ttu-id="d6a1d-115">Valor</span><span class="sxs-lookup"><span data-stu-id="d6a1d-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d6a1d-116">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d6a1d-116">Minimum supported client</span></span><br/> | <span data-ttu-id="d6a1d-117">Somente aplicativos de área de trabalho do Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="d6a1d-117">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="d6a1d-118">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d6a1d-118">Minimum supported server</span></span><br/> | <span data-ttu-id="d6a1d-119">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="d6a1d-119">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="d6a1d-120">parâmetro</span><span class="sxs-lookup"><span data-stu-id="d6a1d-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="d6a1d-121"><dt>Msinkaut. h (também requer Msinkaut \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="d6a1d-121"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="d6a1d-122">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="d6a1d-122">Library</span></span><br/>                  | <dl> <span data-ttu-id="d6a1d-123"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d6a1d-123"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="d6a1d-124">Consulte também</span><span class="sxs-lookup"><span data-stu-id="d6a1d-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d6a1d-125">InkPicture</span><span class="sxs-lookup"><span data-stu-id="d6a1d-125">InkPicture</span></span>](inkpicture-control-reference.md)
</dt> <dt>

[<span data-ttu-id="d6a1d-126">**Interface IInkTablet**</span><span class="sxs-lookup"><span data-stu-id="d6a1d-126">**IInkTablet Interface**</span></span>](/windows/desktop/api/msinkaut/nn-msinkaut-iinktablet)
</dt> </dl>

 

 




