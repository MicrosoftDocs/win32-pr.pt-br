---
title: Interface IVMDVDDriveCollection (VPCCOMInterfaces. h)
description: Define a coleção de unidades de CD e DVD na máquina virtual. Para obter um objeto IVMDVDDriveCollection, use a propriedade IVMVirtualMachine DVDROMDrives.
ms.assetid: 3069f530-9bc7-4f55-bf5a-82d1244d0cc5
keywords:
- Virtual PC de interface IVMDVDDriveCollection
- Virtual PC de interface IVMDVDDriveCollection, descrito
topic_type:
- apiref
api_name:
- IVMDVDDriveCollection
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6afcf14a1ffe53dea0dcd7e21fcde8729e0bd0ca
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105752418"
---
# <a name="ivmdvddrivecollection-interface"></a><span data-ttu-id="8f9ff-106">Interface IVMDVDDriveCollection</span><span class="sxs-lookup"><span data-stu-id="8f9ff-106">IVMDVDDriveCollection interface</span></span>

<span data-ttu-id="8f9ff-107">\[O Windows Virtual PC não está mais disponível para uso a partir do Windows 8.</span><span class="sxs-lookup"><span data-stu-id="8f9ff-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="8f9ff-108">Em vez disso, use o [provedor WMI do Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="8f9ff-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="8f9ff-109">Define a coleção de unidades de CD e DVD na máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="8f9ff-109">Defines the collection of CD and DVD drives within the virtual machine.</span></span> <span data-ttu-id="8f9ff-110">Para obter um objeto **IVMDVDDriveCollection** , use a propriedade [**IVMVirtualMachine::D vdromdrives**](ivmvirtualmachine-dvdromdrives.md) .</span><span class="sxs-lookup"><span data-stu-id="8f9ff-110">To obtain an **IVMDVDDriveCollection** object, use the [**IVMVirtualMachine::DVDROMDrives**](ivmvirtualmachine-dvdromdrives.md) property.</span></span>

## <a name="members"></a><span data-ttu-id="8f9ff-111">Membros</span><span class="sxs-lookup"><span data-stu-id="8f9ff-111">Members</span></span>

<span data-ttu-id="8f9ff-112">A interface **IVMDVDDriveCollection** herda da interface [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) .</span><span class="sxs-lookup"><span data-stu-id="8f9ff-112">The **IVMDVDDriveCollection** interface inherits from the [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interface.</span></span> <span data-ttu-id="8f9ff-113">**IVMDVDDriveCollection** também tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="8f9ff-113">**IVMDVDDriveCollection** also has these types of members:</span></span>

-   [<span data-ttu-id="8f9ff-114">Propriedades</span><span class="sxs-lookup"><span data-stu-id="8f9ff-114">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="8f9ff-115">Propriedades</span><span class="sxs-lookup"><span data-stu-id="8f9ff-115">Properties</span></span>

<span data-ttu-id="8f9ff-116">A interface **IVMDVDDriveCollection** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="8f9ff-116">The **IVMDVDDriveCollection** interface has these properties.</span></span>



| <span data-ttu-id="8f9ff-117">Propriedade</span><span class="sxs-lookup"><span data-stu-id="8f9ff-117">Property</span></span>                                                       | <span data-ttu-id="8f9ff-118">Tipo de acesso</span><span class="sxs-lookup"><span data-stu-id="8f9ff-118">Access type</span></span>          | <span data-ttu-id="8f9ff-119">Descrição</span><span class="sxs-lookup"><span data-stu-id="8f9ff-119">Description</span></span>                                                                    |
|:---------------------------------------------------------------|:---------------------|:-------------------------------------------------------------------------------|
| [<span data-ttu-id="8f9ff-120">**\_NewEnum**</span><span class="sxs-lookup"><span data-stu-id="8f9ff-120">**\_NewEnum**</span></span>](ivmdvddrivecollection--newenum.md)<br/> | <span data-ttu-id="8f9ff-121">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="8f9ff-121">Read-only</span></span><br/> | <span data-ttu-id="8f9ff-122">Um enumerador para a coleção.</span><span class="sxs-lookup"><span data-stu-id="8f9ff-122">An enumerator for the collection.</span></span><br/>                                   |
| [<span data-ttu-id="8f9ff-123">**Contar**</span><span class="sxs-lookup"><span data-stu-id="8f9ff-123">**Count**</span></span>](ivmdvddrivecollection-count.md)<br/>        | <span data-ttu-id="8f9ff-124">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="8f9ff-124">Read-only</span></span><br/> | <span data-ttu-id="8f9ff-125">O número de unidades de CD e DVD nesta coleção.</span><span class="sxs-lookup"><span data-stu-id="8f9ff-125">The number of CD and DVD drives in this collection.</span></span><br/>                 |
| [<span data-ttu-id="8f9ff-126">**Item**</span><span class="sxs-lookup"><span data-stu-id="8f9ff-126">**Item**</span></span>](ivmdvddrivecollection-item.md)<br/>          | <span data-ttu-id="8f9ff-127">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="8f9ff-127">Read-only</span></span><br/> | <span data-ttu-id="8f9ff-128">O objeto da unidade de CD ou DVD que corresponde ao índice especificado.</span><span class="sxs-lookup"><span data-stu-id="8f9ff-128">The CD or DVD drive object that corresponds to the specified index.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="8f9ff-129">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8f9ff-129">Requirements</span></span>



| <span data-ttu-id="8f9ff-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="8f9ff-130">Requirement</span></span> | <span data-ttu-id="8f9ff-131">Valor</span><span class="sxs-lookup"><span data-stu-id="8f9ff-131">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="8f9ff-132">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="8f9ff-132">Minimum supported client</span></span><br/> | <span data-ttu-id="8f9ff-133">\[Somente aplicativos de área de trabalho do Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="8f9ff-133">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="8f9ff-134">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="8f9ff-134">Minimum supported server</span></span><br/> | <span data-ttu-id="8f9ff-135">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="8f9ff-135">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="8f9ff-136">Fim do suporte do cliente</span><span class="sxs-lookup"><span data-stu-id="8f9ff-136">End of client support</span></span><br/>    | <span data-ttu-id="8f9ff-137">Windows 7</span><span class="sxs-lookup"><span data-stu-id="8f9ff-137">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="8f9ff-138">Produto</span><span class="sxs-lookup"><span data-stu-id="8f9ff-138">Product</span></span><br/>                  | <span data-ttu-id="8f9ff-139">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="8f9ff-139">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="8f9ff-140">parâmetro</span><span class="sxs-lookup"><span data-stu-id="8f9ff-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="8f9ff-141"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="8f9ff-141"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="8f9ff-142">IID</span><span class="sxs-lookup"><span data-stu-id="8f9ff-142">IID</span></span><br/>                      | <span data-ttu-id="8f9ff-143">IID \_ IVMDVDDriveCollection é definido como bc86e297-e55f-4742-9614-ad11d3131f68</span><span class="sxs-lookup"><span data-stu-id="8f9ff-143">IID\_IVMDVDDriveCollection is defined as bc86e297-e55f-4742-9614-ad11d3131f68</span></span><br/>      |



## <a name="see-also"></a><span data-ttu-id="8f9ff-144">Confira também</span><span class="sxs-lookup"><span data-stu-id="8f9ff-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8f9ff-145">**IVMDVDDrive**</span><span class="sxs-lookup"><span data-stu-id="8f9ff-145">**IVMDVDDrive**</span></span>](ivmdvddrive.md)
</dt> <dt>

[<span data-ttu-id="8f9ff-146">**IVMVirtualMachine::D VDROMDrives**</span><span class="sxs-lookup"><span data-stu-id="8f9ff-146">**IVMVirtualMachine::DVDROMDrives**</span></span>](ivmvirtualmachine-dvdromdrives.md)
</dt> </dl>

 

