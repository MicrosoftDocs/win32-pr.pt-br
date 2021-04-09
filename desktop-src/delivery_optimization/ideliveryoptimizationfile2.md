---
title: Interface IDeliveryOptimizationFile2
description: O IDeliveryOptimizationFile2 dá suporte à configuração e à obtenção de propriedades de arquivo opcionais.
keywords:
- Interface IDeliveryOptimizationFile2
- Interface IDeliveryOptimizationFile2, descrita
topic_type:
- apiref
api_name:
- IDeliveryOptimizationFile2
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 01/18/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: a45efd821116b24e883ec29d494a1d588559f57a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104009137"
---
# <a name="ideliveryoptimizationfile2-interface"></a><span data-ttu-id="f37a7-105">Interface IDeliveryOptimizationFile2</span><span class="sxs-lookup"><span data-stu-id="f37a7-105">IDeliveryOptimizationFile2 interface</span></span>

<span data-ttu-id="f37a7-106">O **IDeliveryOptimizationFile2** dá suporte à configuração e à obtenção de propriedades de arquivo opcionais.</span><span class="sxs-lookup"><span data-stu-id="f37a7-106">The **IDeliveryOptimizationFile2** supports setting and getting optional file properties.</span></span> 

## <a name="members"></a><span data-ttu-id="f37a7-107">Membros</span><span class="sxs-lookup"><span data-stu-id="f37a7-107">Members</span></span>

<span data-ttu-id="f37a7-108">A interface **IDeliveryOptimizationFile2** herda da interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="f37a7-108">The **IDeliveryOptimizationFile2** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="f37a7-109">**IDeliveryOptimizationFile2** também tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="f37a7-109">**IDeliveryOptimizationFile2** also has these types of members:</span></span>

- [<span data-ttu-id="f37a7-110">Métodos</span><span class="sxs-lookup"><span data-stu-id="f37a7-110">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="f37a7-111">Métodos</span><span class="sxs-lookup"><span data-stu-id="f37a7-111">Methods</span></span>

<span data-ttu-id="f37a7-112">A interface **IDeliveryOptimizationFile2** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="f37a7-112">The **IDeliveryOptimizationFile2** interface has these methods.</span></span>

| <span data-ttu-id="f37a7-113">Método</span><span class="sxs-lookup"><span data-stu-id="f37a7-113">Method</span></span>                                                 | <span data-ttu-id="f37a7-114">Descrição</span><span class="sxs-lookup"><span data-stu-id="f37a7-114">Description</span></span>                                                  |
|:-------------------------------------------------------|:-------------------------------------------------------------|
| [<span data-ttu-id="f37a7-115">**GetProperty**</span><span class="sxs-lookup"><span data-stu-id="f37a7-115">**GetProperty**</span></span>](ideliveryoptimizationfile2-getproperty.md)  | <span data-ttu-id="f37a7-116">Esse método retorna uma única propriedade do arquivo do.</span><span class="sxs-lookup"><span data-stu-id="f37a7-116">This method returns a single property of the DO file.</span></span> |
| [<span data-ttu-id="f37a7-117">**SetProperty**</span><span class="sxs-lookup"><span data-stu-id="f37a7-117">**SetProperty**</span></span>](ideliveryoptimizationfile2-setproperty.md)  | <span data-ttu-id="f37a7-118">Esse método define uma única propriedade do arquivo do.</span><span class="sxs-lookup"><span data-stu-id="f37a7-118">This method sets a single property of the DO file.</span></span>    |

## <a name="requirements"></a><span data-ttu-id="f37a7-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f37a7-119">Requirements</span></span>

| <span data-ttu-id="f37a7-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="f37a7-120">Requirement</span></span> | <span data-ttu-id="f37a7-121">Valor</span><span class="sxs-lookup"><span data-stu-id="f37a7-121">Value</span></span> |
|-------------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="f37a7-122">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f37a7-122">Minimum supported client</span></span>      | <span data-ttu-id="f37a7-123">\[Somente aplicativos da área de trabalho do Windows 10, versão 1803\]</span><span class="sxs-lookup"><span data-stu-id="f37a7-123">Windows 10, version 1803 \[desktop apps only\]</span></span>                                    |
| <span data-ttu-id="f37a7-124">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f37a7-124">Minimum supported server</span></span>      | <span data-ttu-id="f37a7-125">Windows Server, \[ somente aplicativos da área de trabalho da versão 1709\]</span><span class="sxs-lookup"><span data-stu-id="f37a7-125">Windows Server, version 1709 \[desktop apps only\]</span></span>                                |
| <span data-ttu-id="f37a7-126">parâmetro</span><span class="sxs-lookup"><span data-stu-id="f37a7-126">Header</span></span>                        | <span data-ttu-id="f37a7-127">Deliveryoptimization. h</span><span class="sxs-lookup"><span data-stu-id="f37a7-127">Deliveryoptimization.h</span></span>                                                            |
| <span data-ttu-id="f37a7-128">INSERI</span><span class="sxs-lookup"><span data-stu-id="f37a7-128">IDL</span></span>                           | <span data-ttu-id="f37a7-129">DeliveryOptimization. idl</span><span class="sxs-lookup"><span data-stu-id="f37a7-129">DeliveryOptimization.idl</span></span>                                                          |
| <span data-ttu-id="f37a7-130">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="f37a7-130">Library</span></span>                       | <span data-ttu-id="f37a7-131">Dosvc. lib</span><span class="sxs-lookup"><span data-stu-id="f37a7-131">Dosvc.lib</span></span>                                                                         |
| <span data-ttu-id="f37a7-132">DLL</span><span class="sxs-lookup"><span data-stu-id="f37a7-132">DLL</span></span>                           | <span data-ttu-id="f37a7-133">Dosvc.dll</span><span class="sxs-lookup"><span data-stu-id="f37a7-133">Dosvc.dll</span></span>                                                                         |
| <span data-ttu-id="f37a7-134">IID</span><span class="sxs-lookup"><span data-stu-id="f37a7-134">IID</span></span>                           | <span data-ttu-id="f37a7-135">IID_IDeliveryOptimizationFile2 é definido como 3A87296F-6EC2-4126-AB29-E3F8DC4CC390</span><span class="sxs-lookup"><span data-stu-id="f37a7-135">IID_IDeliveryOptimizationFile2 is defined as 3A87296F-6EC2-4126-AB29-E3F8DC4CC390</span></span> |
