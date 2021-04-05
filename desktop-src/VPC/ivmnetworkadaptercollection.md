---
title: Interface IVMNetworkAdapterCollection (VPCCOMInterfaces. h)
description: Define uma coleção de placas de interface de rede virtual. Para obter um objeto IVMNetworkAdapterCollection, use as propriedades IVMVirtualMachine adaptadores, IVMVirtualNetwork adaptadores e IVMVirtualPC UnconnectedNetworkAdapters.
ms.assetid: cfb03a7c-a568-488c-9284-798b7e21027a
keywords:
- Virtual PC de interface IVMNetworkAdapterCollection
- Virtual PC de interface IVMNetworkAdapterCollection, descrito
topic_type:
- apiref
api_name:
- IVMNetworkAdapterCollection
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8005b88cb873f00708829672cdeb6563b606d42b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104009466"
---
# <a name="ivmnetworkadaptercollection-interface"></a><span data-ttu-id="9f350-106">Interface IVMNetworkAdapterCollection</span><span class="sxs-lookup"><span data-stu-id="9f350-106">IVMNetworkAdapterCollection interface</span></span>

<span data-ttu-id="9f350-107">\[O Windows Virtual PC não está mais disponível para uso a partir do Windows 8.</span><span class="sxs-lookup"><span data-stu-id="9f350-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="9f350-108">Em vez disso, use o [provedor WMI do Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="9f350-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="9f350-109">Define uma coleção de placas de interface de rede virtual.</span><span class="sxs-lookup"><span data-stu-id="9f350-109">Defines a collection of virtual network interface cards.</span></span> <span data-ttu-id="9f350-110">Para obter um objeto IVMNetworkAdapterCollection, use as propriedades [**IVMVirtualMachine:: adaptadores**](ivmvirtualmachine-networkadapters.md), [**IVMVirtualNetwork:: adaptadores**](ivmvirtualnetwork-networkadapters.md)e [**IVMVirtualPC:: UnconnectedNetworkAdapters**](ivmvirtualpc-unconnectednetworkadapters.md) .</span><span class="sxs-lookup"><span data-stu-id="9f350-110">To obtain an IVMNetworkAdapterCollection object, use the [**IVMVirtualMachine::NetworkAdapters**](ivmvirtualmachine-networkadapters.md), [**IVMVirtualNetwork::NetworkAdapters**](ivmvirtualnetwork-networkadapters.md), and [**IVMVirtualPC::UnconnectedNetworkAdapters**](ivmvirtualpc-unconnectednetworkadapters.md) properties.</span></span>

## <a name="members"></a><span data-ttu-id="9f350-111">Membros</span><span class="sxs-lookup"><span data-stu-id="9f350-111">Members</span></span>

<span data-ttu-id="9f350-112">A interface **IVMNetworkAdapterCollection** herda da interface [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) .</span><span class="sxs-lookup"><span data-stu-id="9f350-112">The **IVMNetworkAdapterCollection** interface inherits from the [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interface.</span></span> <span data-ttu-id="9f350-113">**IVMNetworkAdapterCollection** também tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="9f350-113">**IVMNetworkAdapterCollection** also has these types of members:</span></span>

-   [<span data-ttu-id="9f350-114">Propriedades</span><span class="sxs-lookup"><span data-stu-id="9f350-114">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="9f350-115">Propriedades</span><span class="sxs-lookup"><span data-stu-id="9f350-115">Properties</span></span>

<span data-ttu-id="9f350-116">A interface **IVMNetworkAdapterCollection** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="9f350-116">The **IVMNetworkAdapterCollection** interface has these properties.</span></span>



| <span data-ttu-id="9f350-117">Propriedade</span><span class="sxs-lookup"><span data-stu-id="9f350-117">Property</span></span>                                                             | <span data-ttu-id="9f350-118">Tipo de acesso</span><span class="sxs-lookup"><span data-stu-id="9f350-118">Access type</span></span>          | <span data-ttu-id="9f350-119">Descrição</span><span class="sxs-lookup"><span data-stu-id="9f350-119">Description</span></span>                                                                                                   |
|:---------------------------------------------------------------------|:---------------------|:--------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="9f350-120">**\_NewEnum**</span><span class="sxs-lookup"><span data-stu-id="9f350-120">**\_NewEnum**</span></span>](ivmnetworkadaptercollection--newenum.md)<br/> | <span data-ttu-id="9f350-121">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="9f350-121">Read-only</span></span><br/> | <span data-ttu-id="9f350-122">Um enumerador para a coleção.</span><span class="sxs-lookup"><span data-stu-id="9f350-122">An enumerator for the collection.</span></span><br/>                                                                  |
| [<span data-ttu-id="9f350-123">**Contar**</span><span class="sxs-lookup"><span data-stu-id="9f350-123">**Count**</span></span>](ivmnetworkadaptercollection-count.md)<br/>        | <span data-ttu-id="9f350-124">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="9f350-124">Read-only</span></span><br/> | <span data-ttu-id="9f350-125">O número de interfaces de rede nesta coleção.</span><span class="sxs-lookup"><span data-stu-id="9f350-125">The number of network interfaces in this collection.</span></span><br/>                                               |
| [<span data-ttu-id="9f350-126">**Item**</span><span class="sxs-lookup"><span data-stu-id="9f350-126">**Item**</span></span>](ivmnetworkadaptercollection-item.md)<br/>          | <span data-ttu-id="9f350-127">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="9f350-127">Read-only</span></span><br/> | <span data-ttu-id="9f350-128">O objeto [**IVMNetworkAdapter**](ivmnetworkadapter.md) que corresponde ao índice especificado.</span><span class="sxs-lookup"><span data-stu-id="9f350-128">The [**IVMNetworkAdapter**](ivmnetworkadapter.md) object that corresponds to the specified index.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="9f350-129">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9f350-129">Requirements</span></span>



| <span data-ttu-id="9f350-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="9f350-130">Requirement</span></span> | <span data-ttu-id="9f350-131">Valor</span><span class="sxs-lookup"><span data-stu-id="9f350-131">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9f350-132">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="9f350-132">Minimum supported client</span></span><br/> | <span data-ttu-id="9f350-133">\[Somente aplicativos de área de trabalho do Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="9f350-133">Windows 7 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="9f350-134">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="9f350-134">Minimum supported server</span></span><br/> | <span data-ttu-id="9f350-135">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="9f350-135">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="9f350-136">Fim do suporte do cliente</span><span class="sxs-lookup"><span data-stu-id="9f350-136">End of client support</span></span><br/>    | <span data-ttu-id="9f350-137">Windows 7</span><span class="sxs-lookup"><span data-stu-id="9f350-137">Windows 7</span></span><br/>                                                                           |
| <span data-ttu-id="9f350-138">Produto</span><span class="sxs-lookup"><span data-stu-id="9f350-138">Product</span></span><br/>                  | <span data-ttu-id="9f350-139">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="9f350-139">Windows Virtual PC</span></span><br/>                                                                  |
| <span data-ttu-id="9f350-140">parâmetro</span><span class="sxs-lookup"><span data-stu-id="9f350-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="9f350-141"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="9f350-141"><dt>VPCCOMInterfaces.h</dt></span></span> </dl>  |
| <span data-ttu-id="9f350-142">IID</span><span class="sxs-lookup"><span data-stu-id="9f350-142">IID</span></span><br/>                      | <span data-ttu-id="9f350-143">IID \_ IVMNetworkAdapterCollection é definido como ebaeafe9-EBCD-47CF-866e-ad87d735e479</span><span class="sxs-lookup"><span data-stu-id="9f350-143">IID\_IVMNetworkAdapterCollection is defined as ebaeafe9-ebcd-47cf-866e-ad87d735e479</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="9f350-144">Confira também</span><span class="sxs-lookup"><span data-stu-id="9f350-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9f350-145">**IVMNetworkAdapter**</span><span class="sxs-lookup"><span data-stu-id="9f350-145">**IVMNetworkAdapter**</span></span>](ivmnetworkadapter.md)
</dt> <dt>

[<span data-ttu-id="9f350-146">**IVMVirtualMachine:: adaptadores**</span><span class="sxs-lookup"><span data-stu-id="9f350-146">**IVMVirtualMachine::NetworkAdapters**</span></span>](ivmvirtualmachine-networkadapters.md)
</dt> <dt>

[<span data-ttu-id="9f350-147">**IVMVirtualNetwork:: adaptadores**</span><span class="sxs-lookup"><span data-stu-id="9f350-147">**IVMVirtualNetwork::NetworkAdapters**</span></span>](ivmvirtualnetwork-networkadapters.md)
</dt> <dt>

[<span data-ttu-id="9f350-148">**IVMVirtualPC::UnconnectedNetworkAdapters**</span><span class="sxs-lookup"><span data-stu-id="9f350-148">**IVMVirtualPC::UnconnectedNetworkAdapters**</span></span>](ivmvirtualpc-unconnectednetworkadapters.md)
</dt> </dl>

 

