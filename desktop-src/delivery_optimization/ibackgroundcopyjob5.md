---
title: Interface IBackgroundCopyJob5 (Deliveryoptimization. h)
description: Use essa interface para consultar ou definir vários comportamentos opcionais de um trabalho.
ms.assetid: C4706E10-40E6-489B-9772-59D581781038
keywords:
- Interface IBackgroundCopyJob5
- Interface IBackgroundCopyJob5, descrita
topic_type:
- apiref
api_name:
- IBackgroundCopyJob5
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: e76898f7bbfe4d4dc34aec035b842e6671091630
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104086104"
---
# <a name="ibackgroundcopyjob5-interface"></a><span data-ttu-id="f16b1-105">Interface IBackgroundCopyJob5</span><span class="sxs-lookup"><span data-stu-id="f16b1-105">IBackgroundCopyJob5 interface</span></span>

<span data-ttu-id="f16b1-106">Use essa interface para consultar ou definir vários comportamentos opcionais de um trabalho.</span><span class="sxs-lookup"><span data-stu-id="f16b1-106">Use this interface to query or set several optional behaviors of a job.</span></span>

<span data-ttu-id="f16b1-107">Para obter essa interface, chame o método **método ibackgroundcopyjob:: QueryInterface** usando `__uuidof(IBackgroundCopyJob5)` como o identificador de interface.</span><span class="sxs-lookup"><span data-stu-id="f16b1-107">To get this interface, call the **IBackgroundCopyJob::QueryInterface** method using `__uuidof(IBackgroundCopyJob5)` as the interface identifier.</span></span>

## <a name="members"></a><span data-ttu-id="f16b1-108">Membros</span><span class="sxs-lookup"><span data-stu-id="f16b1-108">Members</span></span>

<span data-ttu-id="f16b1-109">A interface **IBackgroundCopyJob5** herda de [**método ibackgroundcopyjob**](ibackgroundcopyjob-.md).</span><span class="sxs-lookup"><span data-stu-id="f16b1-109">The **IBackgroundCopyJob5** interface inherits from [**IBackgroundCopyJob**](ibackgroundcopyjob-.md).</span></span> <span data-ttu-id="f16b1-110">**IBackgroundCopyJob5** também tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="f16b1-110">**IBackgroundCopyJob5** also has these types of members:</span></span>

-   [<span data-ttu-id="f16b1-111">Métodos</span><span class="sxs-lookup"><span data-stu-id="f16b1-111">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="f16b1-112">Métodos</span><span class="sxs-lookup"><span data-stu-id="f16b1-112">Methods</span></span>

<span data-ttu-id="f16b1-113">A interface **IBackgroundCopyJob5** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="f16b1-113">The **IBackgroundCopyJob5** interface has these methods.</span></span>



| <span data-ttu-id="f16b1-114">Método</span><span class="sxs-lookup"><span data-stu-id="f16b1-114">Method</span></span>                                                 | <span data-ttu-id="f16b1-115">Descrição</span><span class="sxs-lookup"><span data-stu-id="f16b1-115">Description</span></span>                                                |
|:-------------------------------------------------------|:-----------------------------------------------------------|
| [<span data-ttu-id="f16b1-116">**GetProperty**</span><span class="sxs-lookup"><span data-stu-id="f16b1-116">**GetProperty**</span></span>](ibackgroundcopyjob5-getproperty.md) | <span data-ttu-id="f16b1-117">Um método genérico para obter as propriedades DO trabalho.</span><span class="sxs-lookup"><span data-stu-id="f16b1-117">A generic method for getting DO job properties.</span></span><br/> |
| [<span data-ttu-id="f16b1-118">**SetProperty**</span><span class="sxs-lookup"><span data-stu-id="f16b1-118">**SetProperty**</span></span>](ibackgroundcopyjob5-setproperty.md) | <span data-ttu-id="f16b1-119">Um método genérico para definir as propriedades DO trabalho.</span><span class="sxs-lookup"><span data-stu-id="f16b1-119">A generic method for setting DO job properties.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="f16b1-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f16b1-120">Requirements</span></span>



| <span data-ttu-id="f16b1-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="f16b1-121">Requirement</span></span> | <span data-ttu-id="f16b1-122">Valor</span><span class="sxs-lookup"><span data-stu-id="f16b1-122">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f16b1-123">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f16b1-123">Minimum supported client</span></span><br/> | <span data-ttu-id="f16b1-124">\[Somente aplicativos da área de trabalho do Windows 10, versão 1709\]</span><span class="sxs-lookup"><span data-stu-id="f16b1-124">Windows 10, version 1709 \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="f16b1-125">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f16b1-125">Minimum supported server</span></span><br/> | <span data-ttu-id="f16b1-126">Windows Server, \[ somente aplicativos da área de trabalho da versão 1709\]</span><span class="sxs-lookup"><span data-stu-id="f16b1-126">Windows Server, version 1709 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="f16b1-127">parâmetro</span><span class="sxs-lookup"><span data-stu-id="f16b1-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="f16b1-128"><dt>Deliveryoptimization. h</dt></span><span class="sxs-lookup"><span data-stu-id="f16b1-128"><dt>Deliveryoptimization.h</dt></span></span> </dl>   |
| <span data-ttu-id="f16b1-129">INSERI</span><span class="sxs-lookup"><span data-stu-id="f16b1-129">IDL</span></span><br/>                      | <dl> <span data-ttu-id="f16b1-130"><dt>DeliveryOptimization. idl</dt></span><span class="sxs-lookup"><span data-stu-id="f16b1-130"><dt>DeliveryOptimization.idl</dt></span></span> </dl> |
| <span data-ttu-id="f16b1-131">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="f16b1-131">Library</span></span><br/>                  | <dl> <span data-ttu-id="f16b1-132"><dt>Dosvc. lib</dt></span><span class="sxs-lookup"><span data-stu-id="f16b1-132"><dt>Dosvc.lib</dt></span></span> </dl>                |
| <span data-ttu-id="f16b1-133">DLL</span><span class="sxs-lookup"><span data-stu-id="f16b1-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f16b1-134"><dt>Dosvc.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f16b1-134"><dt>Dosvc.dll</dt></span></span> </dl>                |
| <span data-ttu-id="f16b1-135">IID</span><span class="sxs-lookup"><span data-stu-id="f16b1-135">IID</span></span><br/>                      | <span data-ttu-id="f16b1-136">IID_IBackgroundCopyJob5 é definido como E847030C-BBBA-4657-AF6D-484AA42BF1FE</span><span class="sxs-lookup"><span data-stu-id="f16b1-136">IID_IBackgroundCopyJob5 is defined as E847030C-BBBA-4657-AF6D-484AA42BF1FE</span></span><br/>              |



## <a name="see-also"></a><span data-ttu-id="f16b1-137">Confira também</span><span class="sxs-lookup"><span data-stu-id="f16b1-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f16b1-138">**Método ibackgroundcopyjob**</span><span class="sxs-lookup"><span data-stu-id="f16b1-138">**IBackgroundCopyJob**</span></span>](ibackgroundcopyjob-.md)
</dt> </dl>

 

 





