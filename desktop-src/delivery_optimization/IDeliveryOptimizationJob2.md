---
title: Interface IDeliveryOptimizationJob2
description: 'Saiba mais sobre: interface IDeliveryOptimizationJob2'
keywords:
- Interface IDeliveryOptimizationJob2
topic_type:
- apiref
api_name:
- IDeliveryOptimizationJob2
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 01/18/2019
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 13f5a32b4ddccc203bcae7d6674c4713069355cd
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105764209"
---
# <a name="ideliveryoptimizationjob2-interface"></a><span data-ttu-id="431fe-104">Interface IDeliveryOptimizationJob2</span><span class="sxs-lookup"><span data-stu-id="431fe-104">IDeliveryOptimizationJob2 interface</span></span>

<span data-ttu-id="431fe-105">O IDeliveryOptimizationJob2 permite adicionar um único arquivo ao trabalho de download e recuperar o arquivo imediatamente.</span><span class="sxs-lookup"><span data-stu-id="431fe-105">The IDeliveryOptimizationJob2 enables adding a single file to the download job, and retrieving the file immediately.</span></span> <span data-ttu-id="431fe-106">Essa interface também dá suporte à configuração e à obtenção de propriedades de trabalho opcionais.</span><span class="sxs-lookup"><span data-stu-id="431fe-106">This interface also supports setting and getting optional job properties.</span></span>

## <a name="members"></a><span data-ttu-id="431fe-107">Membros</span><span class="sxs-lookup"><span data-stu-id="431fe-107">Members</span></span>

<span data-ttu-id="431fe-108">A interface **IDeliveryOptimizationJob2** herda da interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="431fe-108">The **IDeliveryOptimizationJob2** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="431fe-109">**IDeliveryOptimizationJob2** também tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="431fe-109">**IDeliveryOptimizationJob2** also has these types of members:</span></span>

- [<span data-ttu-id="431fe-110">Métodos</span><span class="sxs-lookup"><span data-stu-id="431fe-110">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="431fe-111">Métodos</span><span class="sxs-lookup"><span data-stu-id="431fe-111">Methods</span></span>

<span data-ttu-id="431fe-112">A interface **IDeliveryOptimizationJob2** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="431fe-112">The **IDeliveryOptimizationJob2** interface has these methods.</span></span>

| <span data-ttu-id="431fe-113">Método</span><span class="sxs-lookup"><span data-stu-id="431fe-113">Method</span></span>                                              | <span data-ttu-id="431fe-114">Descrição</span><span class="sxs-lookup"><span data-stu-id="431fe-114">Description</span></span>                                                          |
|:----------------------------------------------------|----------------------------------------------------------------------|
| [<span data-ttu-id="431fe-115">**AddFile**</span><span class="sxs-lookup"><span data-stu-id="431fe-115">**AddFile**</span></span>](ideliveryoptimizationjob2-addfile.md) | <span data-ttu-id="431fe-116">O método AddFile adiciona um único arquivo a um trabalho existente DO.</span><span class="sxs-lookup"><span data-stu-id="431fe-116">The AddFile method adds a single file to an existing DO job.</span></span>         |
| [<span data-ttu-id="431fe-117">**GetProperty**</span><span class="sxs-lookup"><span data-stu-id="431fe-117">**GetProperty**</span></span>](ideliveryoptimizationjob2-getproperty.md) | <span data-ttu-id="431fe-118">O método AddFile adiciona um único arquivo a um trabalho existente DO.</span><span class="sxs-lookup"><span data-stu-id="431fe-118">The AddFile method adds a single file to an existing DO job.</span></span> |
| [<span data-ttu-id="431fe-119">**SetProperty**</span><span class="sxs-lookup"><span data-stu-id="431fe-119">**SetProperty**</span></span>](ideliveryoptimizationjob2-setproperty.md) | <span data-ttu-id="431fe-120">Este método não é usado.</span><span class="sxs-lookup"><span data-stu-id="431fe-120">This method is unused.</span></span>                                       |

## <a name="requirements"></a><span data-ttu-id="431fe-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="431fe-121">Requirements</span></span>

| <span data-ttu-id="431fe-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="431fe-122">Requirement</span></span> | <span data-ttu-id="431fe-123">Valor</span><span class="sxs-lookup"><span data-stu-id="431fe-123">Value</span></span> |
|--------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="431fe-124">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="431fe-124">Minimum supported client</span></span> | <span data-ttu-id="431fe-125">\[Somente aplicativos da área de trabalho do Windows 10, versão 1803\]</span><span class="sxs-lookup"><span data-stu-id="431fe-125">Windows 10, version 1803 \[desktop apps only\]</span></span>                                   |
| <span data-ttu-id="431fe-126">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="431fe-126">Minimum supported server</span></span> | <span data-ttu-id="431fe-127">Windows Server, \[ somente aplicativos da área de trabalho da versão 1709\]</span><span class="sxs-lookup"><span data-stu-id="431fe-127">Windows Server, version 1709 \[desktop apps only\]</span></span>                               |
| <span data-ttu-id="431fe-128">parâmetro</span><span class="sxs-lookup"><span data-stu-id="431fe-128">Header</span></span>                   | <span data-ttu-id="431fe-129">Deliveryoptimization. h</span><span class="sxs-lookup"><span data-stu-id="431fe-129">Deliveryoptimization.h</span></span>                                                           |
| <span data-ttu-id="431fe-130">INSERI</span><span class="sxs-lookup"><span data-stu-id="431fe-130">IDL</span></span>                      | <span data-ttu-id="431fe-131">DeliveryOptimization. idl</span><span class="sxs-lookup"><span data-stu-id="431fe-131">DeliveryOptimization.idl</span></span>                                                         |
| <span data-ttu-id="431fe-132">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="431fe-132">Library</span></span>                  | <span data-ttu-id="431fe-133">Dosvc. lib</span><span class="sxs-lookup"><span data-stu-id="431fe-133">Dosvc.lib</span></span>                                                                        |
| <span data-ttu-id="431fe-134">DLL</span><span class="sxs-lookup"><span data-stu-id="431fe-134">DLL</span></span>                      | <span data-ttu-id="431fe-135">Dosvc.dll</span><span class="sxs-lookup"><span data-stu-id="431fe-135">Dosvc.dll</span></span>                                                                        |
| <span data-ttu-id="431fe-136">IID</span><span class="sxs-lookup"><span data-stu-id="431fe-136">IID</span></span>                      | <span data-ttu-id="431fe-137">IID_IDeliveryOptimizationJob2 é definido como 18995A26-BF59-4ABE-9F8B-D5092D5A2405</span><span class="sxs-lookup"><span data-stu-id="431fe-137">IID_IDeliveryOptimizationJob2 is defined as 18995A26-BF59-4ABE-9F8B-D5092D5A2405</span></span> |
