---
description: Ocorre quando um IInkTablet é removido do sistema.
ms.assetid: 2217a69e-5b39-4827-82cd-99a02e9d39c6
title: Evento InkOverlay. TabletRemoved (Msinkaut. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7a7d0e69bae7cb6360794b9624fcef7c8be639e5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105751115"
---
# <a name="inkoverlaytabletremoved-event"></a><span data-ttu-id="86f5a-103">Evento InkOverlay. TabletRemoved</span><span class="sxs-lookup"><span data-stu-id="86f5a-103">InkOverlay.TabletRemoved event</span></span>

<span data-ttu-id="86f5a-104">Ocorre quando um [**IInkTablet**](/windows/desktop/api/msinkaut/nn-msinkaut-iinktablet) é removido do sistema.</span><span class="sxs-lookup"><span data-stu-id="86f5a-104">Occurs when a [**IInkTablet**](/windows/desktop/api/msinkaut/nn-msinkaut-iinktablet) is removed from the system.</span></span>

## <a name="syntax"></a><span data-ttu-id="86f5a-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="86f5a-105">Syntax</span></span>


```C++
void TabletRemoved(
  [in] long TabletId
);
```



## <a name="parameters"></a><span data-ttu-id="86f5a-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="86f5a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="86f5a-107">*TabletId* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="86f5a-107">*TabletId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="86f5a-108">O valor longo que foi usado como a ID do objeto [**IInkTablet**](/windows/desktop/api/msinkaut/nn-msinkaut-iinktablet) que foi removido.</span><span class="sxs-lookup"><span data-stu-id="86f5a-108">The long value that was used as the ID for the [**IInkTablet**](/windows/desktop/api/msinkaut/nn-msinkaut-iinktablet) object that was removed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="86f5a-109">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="86f5a-109">Return value</span></span>

<span data-ttu-id="86f5a-110">Esse evento não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="86f5a-110">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="86f5a-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="86f5a-111">Remarks</span></span>

<span data-ttu-id="86f5a-112">Esse método de evento é definido nas \_ \_ interfaces somente de expedição IInkCollectorEvents, IInkOverlayEvents e \_ IInkPictureEvents (dispinterfaces) com uma ID de ICETabletRemoved de DISPID \_ .</span><span class="sxs-lookup"><span data-stu-id="86f5a-112">This event method is defined in the \_IInkCollectorEvents, \_IInkOverlayEvents, and \_IInkPictureEvents dispatch-only interfaces (dispinterfaces) with an ID of DISPID\_ICETabletRemoved.</span></span>

## <a name="requirements"></a><span data-ttu-id="86f5a-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="86f5a-113">Requirements</span></span>



| <span data-ttu-id="86f5a-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="86f5a-114">Requirement</span></span> | <span data-ttu-id="86f5a-115">Valor</span><span class="sxs-lookup"><span data-stu-id="86f5a-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="86f5a-116">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="86f5a-116">Minimum supported client</span></span><br/> | <span data-ttu-id="86f5a-117">Somente aplicativos de área de trabalho do Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="86f5a-117">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="86f5a-118">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="86f5a-118">Minimum supported server</span></span><br/> | <span data-ttu-id="86f5a-119">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="86f5a-119">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="86f5a-120">parâmetro</span><span class="sxs-lookup"><span data-stu-id="86f5a-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="86f5a-121"><dt>Msinkaut. h (também requer Msinkaut \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="86f5a-121"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="86f5a-122">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="86f5a-122">Library</span></span><br/>                  | <dl> <span data-ttu-id="86f5a-123"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="86f5a-123"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="86f5a-124">Confira também</span><span class="sxs-lookup"><span data-stu-id="86f5a-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="86f5a-125">**Classe InkOverlay**</span><span class="sxs-lookup"><span data-stu-id="86f5a-125">**InkOverlay Class**</span></span>](inkoverlay-class.md)
</dt> <dt>

[<span data-ttu-id="86f5a-126">**Interface IInkTablet**</span><span class="sxs-lookup"><span data-stu-id="86f5a-126">**IInkTablet Interface**</span></span>](/windows/desktop/api/msinkaut/nn-msinkaut-iinktablet)
</dt> </dl>

 

 




