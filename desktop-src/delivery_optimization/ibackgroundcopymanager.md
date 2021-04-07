---
title: Interface IBackgroundCopyManager (Deliveryoptimization. h)
description: Cria trabalhos de transferência, recupera um objeto enumerador que contém os trabalhos na fila e recupera trabalhos individuais da fila.
ms.assetid: EA7CB5CE-5E95-4C6D-8026-4B8375EE216A
keywords:
- Interface IBackgroundCopyManager
- Interface IBackgroundCopyManager, descrita
topic_type:
- apiref
api_name:
- IBackgroundCopyManager
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 6fa752398c0849c987e2a28b804e65a8361e15b0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918571"
---
# <a name="ibackgroundcopymanager-interface"></a><span data-ttu-id="660aa-105">Interface IBackgroundCopyManager</span><span class="sxs-lookup"><span data-stu-id="660aa-105">IBackgroundCopyManager interface</span></span>

<span data-ttu-id="660aa-106">Cria trabalhos de transferência, recupera um objeto enumerador que contém os trabalhos na fila e recupera trabalhos individuais da fila.</span><span class="sxs-lookup"><span data-stu-id="660aa-106">Creates transfer jobs, retrieves an enumerator object that contains the jobs in the queue, and retrieves individual jobs from the queue.</span></span>

## <a name="members"></a><span data-ttu-id="660aa-107">Membros</span><span class="sxs-lookup"><span data-stu-id="660aa-107">Members</span></span>

<span data-ttu-id="660aa-108">A interface **IBackgroundCopyManager** herda da interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="660aa-108">The **IBackgroundCopyManager** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="660aa-109">**IBackgroundCopyManager** também tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="660aa-109">**IBackgroundCopyManager** also has these types of members:</span></span>

-   [<span data-ttu-id="660aa-110">Métodos</span><span class="sxs-lookup"><span data-stu-id="660aa-110">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="660aa-111">Métodos</span><span class="sxs-lookup"><span data-stu-id="660aa-111">Methods</span></span>

<span data-ttu-id="660aa-112">A interface **IBackgroundCopyManager** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="660aa-112">The **IBackgroundCopyManager** interface has these methods.</span></span>



| <span data-ttu-id="660aa-113">Método</span><span class="sxs-lookup"><span data-stu-id="660aa-113">Method</span></span>                                                | <span data-ttu-id="660aa-114">Descrição</span><span class="sxs-lookup"><span data-stu-id="660aa-114">Description</span></span>                                          |
|:------------------------------------------------------|:-----------------------------------------------------|
| [<span data-ttu-id="660aa-115">**CreateJob**</span><span class="sxs-lookup"><span data-stu-id="660aa-115">**CreateJob**</span></span>](ibackgroundcopymanager-createjob.md) | <span data-ttu-id="660aa-116">Cria um trabalho de transferência.</span><span class="sxs-lookup"><span data-stu-id="660aa-116">Creates a transfer job.</span></span><br/>                   |
| [<span data-ttu-id="660aa-117">**GetJob**</span><span class="sxs-lookup"><span data-stu-id="660aa-117">**GetJob**</span></span>](ibackgroundcopymanager-getjob.md)       | <span data-ttu-id="660aa-118">Recupera um trabalho especificado da fila.</span><span class="sxs-lookup"><span data-stu-id="660aa-118">Retrieves a specified job from the queue.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="660aa-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="660aa-119">Requirements</span></span>



| <span data-ttu-id="660aa-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="660aa-120">Requirement</span></span> | <span data-ttu-id="660aa-121">Valor</span><span class="sxs-lookup"><span data-stu-id="660aa-121">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="660aa-122">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="660aa-122">Minimum supported client</span></span><br/> | <span data-ttu-id="660aa-123">\[Somente aplicativos da área de trabalho do Windows 10, versão 1709\]</span><span class="sxs-lookup"><span data-stu-id="660aa-123">Windows 10, version 1709 \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="660aa-124">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="660aa-124">Minimum supported server</span></span><br/> | <span data-ttu-id="660aa-125">Windows Server, \[ somente aplicativos da área de trabalho da versão 1709\]</span><span class="sxs-lookup"><span data-stu-id="660aa-125">Windows Server, version 1709 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="660aa-126">parâmetro</span><span class="sxs-lookup"><span data-stu-id="660aa-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="660aa-127"><dt>Deliveryoptimization. h</dt></span><span class="sxs-lookup"><span data-stu-id="660aa-127"><dt>Deliveryoptimization.h</dt></span></span> </dl>   |
| <span data-ttu-id="660aa-128">INSERI</span><span class="sxs-lookup"><span data-stu-id="660aa-128">IDL</span></span><br/>                      | <dl> <span data-ttu-id="660aa-129"><dt>DeliveryOptimization. idl</dt></span><span class="sxs-lookup"><span data-stu-id="660aa-129"><dt>DeliveryOptimization.idl</dt></span></span> </dl> |
| <span data-ttu-id="660aa-130">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="660aa-130">Library</span></span><br/>                  | <dl> <span data-ttu-id="660aa-131"><dt>Dosvc. lib</dt></span><span class="sxs-lookup"><span data-stu-id="660aa-131"><dt>Dosvc.lib</dt></span></span> </dl>                |
| <span data-ttu-id="660aa-132">DLL</span><span class="sxs-lookup"><span data-stu-id="660aa-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="660aa-133"><dt>Dosvc.dll</dt></span><span class="sxs-lookup"><span data-stu-id="660aa-133"><dt>Dosvc.dll</dt></span></span> </dl>                |
| <span data-ttu-id="660aa-134">IID</span><span class="sxs-lookup"><span data-stu-id="660aa-134">IID</span></span><br/>                      | <span data-ttu-id="660aa-135">IID_IBackgroundCopyManager é definido como 5CE34C0D-0DC9-4C1F-897C-DAA1B78CEE7C</span><span class="sxs-lookup"><span data-stu-id="660aa-135">IID_IBackgroundCopyManager is defined as 5CE34C0D-0DC9-4C1F-897C-DAA1B78CEE7C</span></span><br/>           |



## <a name="see-also"></a><span data-ttu-id="660aa-136">Confira também</span><span class="sxs-lookup"><span data-stu-id="660aa-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="660aa-137">**Método ibackgroundcopyjob**</span><span class="sxs-lookup"><span data-stu-id="660aa-137">**IBackgroundCopyJob**</span></span>](ibackgroundcopyjob-.md)
</dt> </dl>

 

