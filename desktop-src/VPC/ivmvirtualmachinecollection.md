---
title: Interface IVMVirtualMachineCollection (VPCCOMInterfaces. h)
description: Define a coleção de máquinas virtuais no Windows Virtual PC. Para obter um objeto IVMVirtualMachineCollection, use a propriedade IVMVirtualPC VirtualMachines.
ms.assetid: 3d34e791-2dba-4529-b489-96a0c6227294
keywords:
- Virtual PC de interface IVMVirtualMachineCollection
- Virtual PC de interface IVMVirtualMachineCollection, descrito
topic_type:
- apiref
api_name:
- IVMVirtualMachineCollection
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e27426f96e409a1e67eb519e7a864ee7461879a7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104086211"
---
# <a name="ivmvirtualmachinecollection-interface"></a><span data-ttu-id="59dc7-106">Interface IVMVirtualMachineCollection</span><span class="sxs-lookup"><span data-stu-id="59dc7-106">IVMVirtualMachineCollection interface</span></span>

<span data-ttu-id="59dc7-107">\[O Windows Virtual PC não está mais disponível para uso a partir do Windows 8.</span><span class="sxs-lookup"><span data-stu-id="59dc7-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="59dc7-108">Em vez disso, use o [provedor WMI do Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="59dc7-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="59dc7-109">Define a coleção de máquinas virtuais no Windows Virtual PC.</span><span class="sxs-lookup"><span data-stu-id="59dc7-109">Defines the collection of virtual machines within Windows Virtual PC.</span></span> <span data-ttu-id="59dc7-110">Para obter um objeto **IVMVirtualMachineCollection** , use a propriedade [**IVMVirtualPC:: VirtualMachines**](ivmvirtualpc-virtualmachines.md) .</span><span class="sxs-lookup"><span data-stu-id="59dc7-110">To obtain an **IVMVirtualMachineCollection** object, use the [**IVMVirtualPC::VirtualMachines**](ivmvirtualpc-virtualmachines.md) property.</span></span>

## <a name="members"></a><span data-ttu-id="59dc7-111">Membros</span><span class="sxs-lookup"><span data-stu-id="59dc7-111">Members</span></span>

<span data-ttu-id="59dc7-112">A interface **IVMVirtualMachineCollection** herda da interface [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) .</span><span class="sxs-lookup"><span data-stu-id="59dc7-112">The **IVMVirtualMachineCollection** interface inherits from the [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interface.</span></span> <span data-ttu-id="59dc7-113">**IVMVirtualMachineCollection** também tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="59dc7-113">**IVMVirtualMachineCollection** also has these types of members:</span></span>

-   [<span data-ttu-id="59dc7-114">Propriedades</span><span class="sxs-lookup"><span data-stu-id="59dc7-114">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="59dc7-115">Propriedades</span><span class="sxs-lookup"><span data-stu-id="59dc7-115">Properties</span></span>

<span data-ttu-id="59dc7-116">A interface **IVMVirtualMachineCollection** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="59dc7-116">The **IVMVirtualMachineCollection** interface has these properties.</span></span>



| <span data-ttu-id="59dc7-117">Propriedade</span><span class="sxs-lookup"><span data-stu-id="59dc7-117">Property</span></span>                                                             | <span data-ttu-id="59dc7-118">Tipo de acesso</span><span class="sxs-lookup"><span data-stu-id="59dc7-118">Access type</span></span>          | <span data-ttu-id="59dc7-119">Descrição</span><span class="sxs-lookup"><span data-stu-id="59dc7-119">Description</span></span>                                                                    |
|:---------------------------------------------------------------------|:---------------------|:-------------------------------------------------------------------------------|
| [<span data-ttu-id="59dc7-120">**\_NewEnum**</span><span class="sxs-lookup"><span data-stu-id="59dc7-120">**\_NewEnum**</span></span>](ivmvirtualmachinecollection--newenum.md)<br/> | <span data-ttu-id="59dc7-121">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="59dc7-121">Read-only</span></span><br/> | <span data-ttu-id="59dc7-122">Um enumerador para a coleção.</span><span class="sxs-lookup"><span data-stu-id="59dc7-122">An enumerator for the collection.</span></span><br/>                                   |
| [<span data-ttu-id="59dc7-123">**Contar**</span><span class="sxs-lookup"><span data-stu-id="59dc7-123">**Count**</span></span>](ivmvirtualmachinecollection-count.md)<br/>        | <span data-ttu-id="59dc7-124">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="59dc7-124">Read-only</span></span><br/> | <span data-ttu-id="59dc7-125">O número de máquinas virtuais nesta coleção.</span><span class="sxs-lookup"><span data-stu-id="59dc7-125">The number of virtual machines in this collection.</span></span><br/>                  |
| [<span data-ttu-id="59dc7-126">**Item**</span><span class="sxs-lookup"><span data-stu-id="59dc7-126">**Item**</span></span>](ivmvirtualmachinecollection-item.md)<br/>          | <span data-ttu-id="59dc7-127">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="59dc7-127">Read-only</span></span><br/> | <span data-ttu-id="59dc7-128">O objeto de máquina virtual que corresponde ao índice especificado.</span><span class="sxs-lookup"><span data-stu-id="59dc7-128">The virtual machine object that corresponds to the specified index.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="59dc7-129">Requisitos</span><span class="sxs-lookup"><span data-stu-id="59dc7-129">Requirements</span></span>



| <span data-ttu-id="59dc7-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="59dc7-130">Requirement</span></span> | <span data-ttu-id="59dc7-131">Valor</span><span class="sxs-lookup"><span data-stu-id="59dc7-131">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="59dc7-132">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="59dc7-132">Minimum supported client</span></span><br/> | <span data-ttu-id="59dc7-133">\[Somente aplicativos de área de trabalho do Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="59dc7-133">Windows 7 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="59dc7-134">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="59dc7-134">Minimum supported server</span></span><br/> | <span data-ttu-id="59dc7-135">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="59dc7-135">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="59dc7-136">Fim do suporte do cliente</span><span class="sxs-lookup"><span data-stu-id="59dc7-136">End of client support</span></span><br/>    | <span data-ttu-id="59dc7-137">Windows 7</span><span class="sxs-lookup"><span data-stu-id="59dc7-137">Windows 7</span></span><br/>                                                                           |
| <span data-ttu-id="59dc7-138">Produto</span><span class="sxs-lookup"><span data-stu-id="59dc7-138">Product</span></span><br/>                  | <span data-ttu-id="59dc7-139">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="59dc7-139">Windows Virtual PC</span></span><br/>                                                                  |
| <span data-ttu-id="59dc7-140">parâmetro</span><span class="sxs-lookup"><span data-stu-id="59dc7-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="59dc7-141"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="59dc7-141"><dt>VPCCOMInterfaces.h</dt></span></span> </dl>  |
| <span data-ttu-id="59dc7-142">IID</span><span class="sxs-lookup"><span data-stu-id="59dc7-142">IID</span></span><br/>                      | <span data-ttu-id="59dc7-143">IID \_ IVMVirtualMachineCollection é definido como 59f31786-2a3d-4fbf-9896-d85338ca0da1</span><span class="sxs-lookup"><span data-stu-id="59dc7-143">IID\_IVMVirtualMachineCollection is defined as 59f31786-2a3d-4fbf-9896-d85338ca0da1</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="59dc7-144">Confira também</span><span class="sxs-lookup"><span data-stu-id="59dc7-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="59dc7-145">**IVMVirtualMachine**</span><span class="sxs-lookup"><span data-stu-id="59dc7-145">**IVMVirtualMachine**</span></span>](ivmvirtualmachine.md)
</dt> <dt>

[<span data-ttu-id="59dc7-146">**IVMVirtualPC:: VirtualMachines**</span><span class="sxs-lookup"><span data-stu-id="59dc7-146">**IVMVirtualPC::VirtualMachines**</span></span>](ivmvirtualpc-virtualmachines.md)
</dt> </dl>

 

