---
title: Interface IDeliveryOptimizationFile
description: Implemente a interface IDeliveryOptimizationFile para identificar o status de um arquivo específico.
ms.assetid: 4D1D82E1-B39C-4634-A0B7-BC4322796AB2
keywords:
- Interface IDeliveryOptimizationFile
- Interface IDeliveryOptimizationFile, descrita
topic_type:
- apiref
api_name:
- IDeliveryOptimizationFile
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 2b86434f4be2f7d14ae46f4af92784c1be4fd1aa
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105764247"
---
# <a name="ideliveryoptimizationfile-interface"></a><span data-ttu-id="1ce1e-105">Interface IDeliveryOptimizationFile</span><span class="sxs-lookup"><span data-stu-id="1ce1e-105">IDeliveryOptimizationFile interface</span></span>

<span data-ttu-id="1ce1e-106">Implemente a interface **IDeliveryOptimizationFile** para identificar o status de um arquivo específico.</span><span class="sxs-lookup"><span data-stu-id="1ce1e-106">Implement the **IDeliveryOptimizationFile** interface to identify the status of a specific file.</span></span>

## <a name="members"></a><span data-ttu-id="1ce1e-107">Membros</span><span class="sxs-lookup"><span data-stu-id="1ce1e-107">Members</span></span>

<span data-ttu-id="1ce1e-108">A interface **IDeliveryOptimizationFile** herda da interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="1ce1e-108">The **IDeliveryOptimizationFile** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="1ce1e-109">**IDeliveryOptimizationFile** também tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="1ce1e-109">**IDeliveryOptimizationFile** also has these types of members:</span></span>

-   [<span data-ttu-id="1ce1e-110">Métodos</span><span class="sxs-lookup"><span data-stu-id="1ce1e-110">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="1ce1e-111">Métodos</span><span class="sxs-lookup"><span data-stu-id="1ce1e-111">Methods</span></span>

<span data-ttu-id="1ce1e-112">A interface **IDeliveryOptimizationFile** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="1ce1e-112">The **IDeliveryOptimizationFile** interface has these methods.</span></span>



| <span data-ttu-id="1ce1e-113">Método</span><span class="sxs-lookup"><span data-stu-id="1ce1e-113">Method</span></span>                                                 | <span data-ttu-id="1ce1e-114">Descrição</span><span class="sxs-lookup"><span data-stu-id="1ce1e-114">Description</span></span>                                                       |
|:-------------------------------------------------------|:------------------------------------------------------------------|
| [<span data-ttu-id="1ce1e-115">**GetStats**</span><span class="sxs-lookup"><span data-stu-id="1ce1e-115">**GetStats**</span></span>](ideliveryoptimizationfile-getstats.md) | <span data-ttu-id="1ce1e-116">Retorna o download e o upload de estatísticas para um arquivo específico.</span><span class="sxs-lookup"><span data-stu-id="1ce1e-116">Returns download and upload stats for a specific file.</span></span><br/> |

## <a name="requirements"></a><span data-ttu-id="1ce1e-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1ce1e-117">Requirements</span></span>

| <span data-ttu-id="1ce1e-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="1ce1e-118">Requirement</span></span> | <span data-ttu-id="1ce1e-119">Valor</span><span class="sxs-lookup"><span data-stu-id="1ce1e-119">Value</span></span> |
|-------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="1ce1e-120">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="1ce1e-120">Minimum supported client</span></span>      | <span data-ttu-id="1ce1e-121">\[Somente aplicativos da área de trabalho do Windows 10, versão 1709\]</span><span class="sxs-lookup"><span data-stu-id="1ce1e-121">Windows 10, version 1709 \[desktop apps only\]</span></span>                                   |
| <span data-ttu-id="1ce1e-122">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="1ce1e-122">Minimum supported server</span></span>      | <span data-ttu-id="1ce1e-123">Windows Server, \[ somente aplicativos da área de trabalho da versão 1709\]</span><span class="sxs-lookup"><span data-stu-id="1ce1e-123">Windows Server, version 1709 \[desktop apps only\]</span></span>                               |
| <span data-ttu-id="1ce1e-124">parâmetro</span><span class="sxs-lookup"><span data-stu-id="1ce1e-124">Header</span></span>                        | <span data-ttu-id="1ce1e-125">Deliveryoptimization. h</span><span class="sxs-lookup"><span data-stu-id="1ce1e-125">Deliveryoptimization.h</span></span>                                                           |
| <span data-ttu-id="1ce1e-126">INSERI</span><span class="sxs-lookup"><span data-stu-id="1ce1e-126">IDL</span></span>                           | <span data-ttu-id="1ce1e-127">DeliveryOptimization. idl</span><span class="sxs-lookup"><span data-stu-id="1ce1e-127">DeliveryOptimization.idl</span></span>                                                         |
| <span data-ttu-id="1ce1e-128">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="1ce1e-128">Library</span></span>                       | <span data-ttu-id="1ce1e-129">Dosvc. lib</span><span class="sxs-lookup"><span data-stu-id="1ce1e-129">Dosvc.lib</span></span>                                                                        |
| <span data-ttu-id="1ce1e-130">DLL</span><span class="sxs-lookup"><span data-stu-id="1ce1e-130">DLL</span></span>                           | <span data-ttu-id="1ce1e-131">Dosvc.dll</span><span class="sxs-lookup"><span data-stu-id="1ce1e-131">Dosvc.dll</span></span>                                                                        |
| <span data-ttu-id="1ce1e-132">IID</span><span class="sxs-lookup"><span data-stu-id="1ce1e-132">IID</span></span>                           | <span data-ttu-id="1ce1e-133">IID_IDeliveryOptimizationFile é definido como B76B9699-E99E-4101-803F-A20E325D93E2</span><span class="sxs-lookup"><span data-stu-id="1ce1e-133">IID_IDeliveryOptimizationFile is defined as B76B9699-E99E-4101-803F-A20E325D93E2</span></span> |
