---
title: Interface IVMVirtualNetworkCollection (VPCCOMInterfaces. h)
description: Define uma coleção de objetos IVMVirtualNetwork. Para obter um objeto IVMVirtualNetworkCollection, use a propriedade IVMVirtualPC VirtualNetworks.
ms.assetid: 3d595bc3-1a8d-4e09-a809-944d4dcdc675
keywords:
- Virtual PC de interface IVMVirtualNetworkCollection
- Virtual PC de interface IVMVirtualNetworkCollection, descrito
topic_type:
- apiref
api_name:
- IVMVirtualNetworkCollection
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 76935fd4a67983847e211d8aa53f4a616bed9d4d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103645045"
---
# <a name="ivmvirtualnetworkcollection-interface"></a><span data-ttu-id="d1ae7-106">Interface IVMVirtualNetworkCollection</span><span class="sxs-lookup"><span data-stu-id="d1ae7-106">IVMVirtualNetworkCollection interface</span></span>

<span data-ttu-id="d1ae7-107">\[O Windows Virtual PC não está mais disponível para uso a partir do Windows 8.</span><span class="sxs-lookup"><span data-stu-id="d1ae7-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="d1ae7-108">Em vez disso, use o [provedor WMI do Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="d1ae7-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="d1ae7-109">Define uma coleção de objetos [**IVMVirtualNetwork**](ivmvirtualnetwork.md) .</span><span class="sxs-lookup"><span data-stu-id="d1ae7-109">Defines a collection of [**IVMVirtualNetwork**](ivmvirtualnetwork.md) objects.</span></span> <span data-ttu-id="d1ae7-110">Para obter um objeto **IVMVirtualNetworkCollection** , use a propriedade [**IVMVirtualPC:: VirtualNetworks**](ivmvirtualpc-virtualnetworks.md) .</span><span class="sxs-lookup"><span data-stu-id="d1ae7-110">To obtain an **IVMVirtualNetworkCollection** object, use the [**IVMVirtualPC::VirtualNetworks**](ivmvirtualpc-virtualnetworks.md) property.</span></span>

## <a name="members"></a><span data-ttu-id="d1ae7-111">Membros</span><span class="sxs-lookup"><span data-stu-id="d1ae7-111">Members</span></span>

<span data-ttu-id="d1ae7-112">A interface **IVMVirtualNetworkCollection** herda da interface [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) .</span><span class="sxs-lookup"><span data-stu-id="d1ae7-112">The **IVMVirtualNetworkCollection** interface inherits from the [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interface.</span></span> <span data-ttu-id="d1ae7-113">**IVMVirtualNetworkCollection** também tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="d1ae7-113">**IVMVirtualNetworkCollection** also has these types of members:</span></span>

-   [<span data-ttu-id="d1ae7-114">Propriedades</span><span class="sxs-lookup"><span data-stu-id="d1ae7-114">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="d1ae7-115">Propriedades</span><span class="sxs-lookup"><span data-stu-id="d1ae7-115">Properties</span></span>

<span data-ttu-id="d1ae7-116">A interface **IVMVirtualNetworkCollection** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="d1ae7-116">The **IVMVirtualNetworkCollection** interface has these properties.</span></span>



| <span data-ttu-id="d1ae7-117">Propriedade</span><span class="sxs-lookup"><span data-stu-id="d1ae7-117">Property</span></span>                                                             | <span data-ttu-id="d1ae7-118">Tipo de acesso</span><span class="sxs-lookup"><span data-stu-id="d1ae7-118">Access type</span></span>          | <span data-ttu-id="d1ae7-119">Descrição</span><span class="sxs-lookup"><span data-stu-id="d1ae7-119">Description</span></span>                                                                                                   |
|:---------------------------------------------------------------------|:---------------------|:--------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="d1ae7-120">**\_NewEnum**</span><span class="sxs-lookup"><span data-stu-id="d1ae7-120">**\_NewEnum**</span></span>](ivmvirtualnetworkcollection--newenum.md)<br/> | <span data-ttu-id="d1ae7-121">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="d1ae7-121">Read-only</span></span><br/> | <span data-ttu-id="d1ae7-122">Um enumerador para a coleção.</span><span class="sxs-lookup"><span data-stu-id="d1ae7-122">An enumerator for the collection.</span></span><br/>                                                                  |
| [<span data-ttu-id="d1ae7-123">**Contar**</span><span class="sxs-lookup"><span data-stu-id="d1ae7-123">**Count**</span></span>](ivmvirtualnetworkcollection-count.md)<br/>        | <span data-ttu-id="d1ae7-124">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="d1ae7-124">Read-only</span></span><br/> | <span data-ttu-id="d1ae7-125">O número de redes virtuais nesta coleção.</span><span class="sxs-lookup"><span data-stu-id="d1ae7-125">The number of virtual networks in this collection.</span></span><br/>                                                 |
| [<span data-ttu-id="d1ae7-126">**Item**</span><span class="sxs-lookup"><span data-stu-id="d1ae7-126">**Item**</span></span>](ivmvirtualnetworkcollection-item.md)<br/>          | <span data-ttu-id="d1ae7-127">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="d1ae7-127">Read-only</span></span><br/> | <span data-ttu-id="d1ae7-128">O objeto [**IVMVirtualNetwork**](ivmvirtualnetwork.md) que corresponde ao índice especificado.</span><span class="sxs-lookup"><span data-stu-id="d1ae7-128">The [**IVMVirtualNetwork**](ivmvirtualnetwork.md) object that corresponds to the specified index.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="d1ae7-129">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d1ae7-129">Requirements</span></span>



| <span data-ttu-id="d1ae7-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="d1ae7-130">Requirement</span></span> | <span data-ttu-id="d1ae7-131">Valor</span><span class="sxs-lookup"><span data-stu-id="d1ae7-131">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d1ae7-132">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d1ae7-132">Minimum supported client</span></span><br/> | <span data-ttu-id="d1ae7-133">\[Somente aplicativos de área de trabalho do Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="d1ae7-133">Windows 7 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="d1ae7-134">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d1ae7-134">Minimum supported server</span></span><br/> | <span data-ttu-id="d1ae7-135">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="d1ae7-135">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="d1ae7-136">Fim do suporte do cliente</span><span class="sxs-lookup"><span data-stu-id="d1ae7-136">End of client support</span></span><br/>    | <span data-ttu-id="d1ae7-137">Windows 7</span><span class="sxs-lookup"><span data-stu-id="d1ae7-137">Windows 7</span></span><br/>                                                                           |
| <span data-ttu-id="d1ae7-138">Produto</span><span class="sxs-lookup"><span data-stu-id="d1ae7-138">Product</span></span><br/>                  | <span data-ttu-id="d1ae7-139">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="d1ae7-139">Windows Virtual PC</span></span><br/>                                                                  |
| <span data-ttu-id="d1ae7-140">parâmetro</span><span class="sxs-lookup"><span data-stu-id="d1ae7-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="d1ae7-141"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="d1ae7-141"><dt>VPCCOMInterfaces.h</dt></span></span> </dl>  |
| <span data-ttu-id="d1ae7-142">IID</span><span class="sxs-lookup"><span data-stu-id="d1ae7-142">IID</span></span><br/>                      | <span data-ttu-id="d1ae7-143">IID \_ IVMVirtualNetworkCollection é definido como 8ed680be-4242-4B2A-a21c-1982d8b0f675</span><span class="sxs-lookup"><span data-stu-id="d1ae7-143">IID\_IVMVirtualNetworkCollection is defined as 8ed680be-4242-4b2a-a21c-1982d8b0f675</span></span><br/> |



 

