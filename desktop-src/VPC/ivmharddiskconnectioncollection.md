---
title: Interface IVMHardDiskConnectionCollection (VPCCOMInterfaces. h)
description: Define a coleção de conexões de disco rígido na máquina virtual. Para obter um objeto IVMHardDiskConnectionCollection, use a propriedade IVMVirtualMachine HardDiskConnections.
ms.assetid: 3440318c-45f4-4d24-9609-dbe5ca59b005
keywords:
- Virtual PC de interface IVMHardDiskConnectionCollection
- Virtual PC de interface IVMHardDiskConnectionCollection, descrito
topic_type:
- apiref
api_name:
- IVMHardDiskConnectionCollection
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dbde67f226c5b2d8cb86a8764c6dd61c24c2a468
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104454585"
---
# <a name="ivmharddiskconnectioncollection-interface"></a><span data-ttu-id="fae23-106">Interface IVMHardDiskConnectionCollection</span><span class="sxs-lookup"><span data-stu-id="fae23-106">IVMHardDiskConnectionCollection interface</span></span>

<span data-ttu-id="fae23-107">\[O Windows Virtual PC não está mais disponível para uso a partir do Windows 8.</span><span class="sxs-lookup"><span data-stu-id="fae23-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="fae23-108">Em vez disso, use o [provedor WMI do Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="fae23-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="fae23-109">Define a coleção de conexões de disco rígido na máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="fae23-109">Defines the collection of hard disk connections within the virtual machine.</span></span> <span data-ttu-id="fae23-110">Para obter um objeto **IVMHardDiskConnectionCollection** , use a propriedade [**IVMVirtualMachine:: HardDiskConnections**](ivmvirtualmachine-harddiskconnections.md) .</span><span class="sxs-lookup"><span data-stu-id="fae23-110">To obtain an **IVMHardDiskConnectionCollection** object, use the [**IVMVirtualMachine::HardDiskConnections**](ivmvirtualmachine-harddiskconnections.md) property.</span></span>

## <a name="members"></a><span data-ttu-id="fae23-111">Membros</span><span class="sxs-lookup"><span data-stu-id="fae23-111">Members</span></span>

<span data-ttu-id="fae23-112">A interface **IVMHardDiskConnectionCollection** herda da interface [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) .</span><span class="sxs-lookup"><span data-stu-id="fae23-112">The **IVMHardDiskConnectionCollection** interface inherits from the [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interface.</span></span> <span data-ttu-id="fae23-113">**IVMHardDiskConnectionCollection** também tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="fae23-113">**IVMHardDiskConnectionCollection** also has these types of members:</span></span>

-   [<span data-ttu-id="fae23-114">Propriedades</span><span class="sxs-lookup"><span data-stu-id="fae23-114">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="fae23-115">Propriedades</span><span class="sxs-lookup"><span data-stu-id="fae23-115">Properties</span></span>

<span data-ttu-id="fae23-116">A interface **IVMHardDiskConnectionCollection** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="fae23-116">The **IVMHardDiskConnectionCollection** interface has these properties.</span></span>



| <span data-ttu-id="fae23-117">Propriedade</span><span class="sxs-lookup"><span data-stu-id="fae23-117">Property</span></span>                                                                 | <span data-ttu-id="fae23-118">Tipo de acesso</span><span class="sxs-lookup"><span data-stu-id="fae23-118">Access type</span></span>          | <span data-ttu-id="fae23-119">Descrição</span><span class="sxs-lookup"><span data-stu-id="fae23-119">Description</span></span>                                                                         |
|:-------------------------------------------------------------------------|:---------------------|:------------------------------------------------------------------------------------|
| [<span data-ttu-id="fae23-120">**\_NewEnum**</span><span class="sxs-lookup"><span data-stu-id="fae23-120">**\_NewEnum**</span></span>](ivmharddiskconnectioncollection--newenum.md)<br/> | <span data-ttu-id="fae23-121">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="fae23-121">Read-only</span></span><br/> | <span data-ttu-id="fae23-122">Um enumerador para a coleção.</span><span class="sxs-lookup"><span data-stu-id="fae23-122">An enumerator for the collection.</span></span><br/>                                        |
| [<span data-ttu-id="fae23-123">**Contar**</span><span class="sxs-lookup"><span data-stu-id="fae23-123">**Count**</span></span>](ivmharddiskconnectioncollection-count.md)<br/>        | <span data-ttu-id="fae23-124">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="fae23-124">Read-only</span></span><br/> | <span data-ttu-id="fae23-125">O número de conexões de disco rígido nesta coleção.</span><span class="sxs-lookup"><span data-stu-id="fae23-125">The number of hard disk connections in this collection.</span></span><br/>                  |
| [<span data-ttu-id="fae23-126">**Item**</span><span class="sxs-lookup"><span data-stu-id="fae23-126">**Item**</span></span>](ivmharddiskconnectioncollection-item.md)<br/>          | <span data-ttu-id="fae23-127">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="fae23-127">Read-only</span></span><br/> | <span data-ttu-id="fae23-128">O objeto de conexão de disco rígido que corresponde ao índice especificado.</span><span class="sxs-lookup"><span data-stu-id="fae23-128">The hard disk connection object that corresponds to the specified index.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="fae23-129">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fae23-129">Requirements</span></span>



| <span data-ttu-id="fae23-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="fae23-130">Requirement</span></span> | <span data-ttu-id="fae23-131">Valor</span><span class="sxs-lookup"><span data-stu-id="fae23-131">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fae23-132">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="fae23-132">Minimum supported client</span></span><br/> | <span data-ttu-id="fae23-133">\[Somente aplicativos de área de trabalho do Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="fae23-133">Windows 7 \[desktop apps only\]</span></span><br/>                                                         |
| <span data-ttu-id="fae23-134">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="fae23-134">Minimum supported server</span></span><br/> | <span data-ttu-id="fae23-135">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="fae23-135">None supported</span></span><br/>                                                                          |
| <span data-ttu-id="fae23-136">Fim do suporte do cliente</span><span class="sxs-lookup"><span data-stu-id="fae23-136">End of client support</span></span><br/>    | <span data-ttu-id="fae23-137">Windows 7</span><span class="sxs-lookup"><span data-stu-id="fae23-137">Windows 7</span></span><br/>                                                                               |
| <span data-ttu-id="fae23-138">Produto</span><span class="sxs-lookup"><span data-stu-id="fae23-138">Product</span></span><br/>                  | <span data-ttu-id="fae23-139">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="fae23-139">Windows Virtual PC</span></span><br/>                                                                      |
| <span data-ttu-id="fae23-140">parâmetro</span><span class="sxs-lookup"><span data-stu-id="fae23-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="fae23-141"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="fae23-141"><dt>VPCCOMInterfaces.h</dt></span></span> </dl>      |
| <span data-ttu-id="fae23-142">IID</span><span class="sxs-lookup"><span data-stu-id="fae23-142">IID</span></span><br/>                      | <span data-ttu-id="fae23-143">IID \_ IVMHardDiskconnectionCollection é definido como b9f2caf4-0aeb-4085-B105-ceddb90dbf62</span><span class="sxs-lookup"><span data-stu-id="fae23-143">IID\_IVMHardDiskconnectionCollection is defined as b9f2caf4-0aeb-4085-b105-ceddb90dbf62</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="fae23-144">Confira também</span><span class="sxs-lookup"><span data-stu-id="fae23-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fae23-145">**IVMHardDiskConnection**</span><span class="sxs-lookup"><span data-stu-id="fae23-145">**IVMHardDiskConnection**</span></span>](ivmharddiskconnection.md)
</dt> <dt>

[<span data-ttu-id="fae23-146">**IVMVirtualMachine::HardDiskConnections**</span><span class="sxs-lookup"><span data-stu-id="fae23-146">**IVMVirtualMachine::HardDiskConnections**</span></span>](ivmvirtualmachine-harddiskconnections.md)
</dt> </dl>

 

