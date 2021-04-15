---
title: Interface IVMFloppyDriveCollection (VPCCOMInterfaces. h)
description: Define uma coleção de unidades de disquete na máquina virtual.
ms.assetid: ba05fa84-81c3-4e70-98f5-404a9bc517ad
keywords:
- Virtual PC de interface IVMFloppyDriveCollection
- Virtual PC de interface IVMFloppyDriveCollection, descrito
topic_type:
- apiref
api_name:
- IVMFloppyDriveCollection
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 664937a08bf7576c35b94a162fb5b6f4a7400f15
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104369906"
---
# <a name="ivmfloppydrivecollection-interface"></a><span data-ttu-id="73087-105">Interface IVMFloppyDriveCollection</span><span class="sxs-lookup"><span data-stu-id="73087-105">IVMFloppyDriveCollection interface</span></span>

<span data-ttu-id="73087-106">\[O Windows Virtual PC não está mais disponível para uso a partir do Windows 8.</span><span class="sxs-lookup"><span data-stu-id="73087-106">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="73087-107">Em vez disso, use o [provedor WMI do Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="73087-107">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="73087-108">Define uma coleção de unidades de disquete na máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="73087-108">Defines a collection of floppy drives within the virtual machine.</span></span> <span data-ttu-id="73087-109">Para obter um objeto **IVMFloppyDriveCollection** , use a propriedade [**IVMVirtualMachine:: FloppyDrives**](ivmvirtualmachine-floppydrives.md) .</span><span class="sxs-lookup"><span data-stu-id="73087-109">To obtain an **IVMFloppyDriveCollection** object, use the [**IVMVirtualMachine::FloppyDrives**](ivmvirtualmachine-floppydrives.md) property.</span></span>

## <a name="members"></a><span data-ttu-id="73087-110">Membros</span><span class="sxs-lookup"><span data-stu-id="73087-110">Members</span></span>

<span data-ttu-id="73087-111">A interface **IVMFloppyDriveCollection** herda da interface [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) .</span><span class="sxs-lookup"><span data-stu-id="73087-111">The **IVMFloppyDriveCollection** interface inherits from the [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interface.</span></span> <span data-ttu-id="73087-112">**IVMFloppyDriveCollection** também tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="73087-112">**IVMFloppyDriveCollection** also has these types of members:</span></span>

-   [<span data-ttu-id="73087-113">Propriedades</span><span class="sxs-lookup"><span data-stu-id="73087-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="73087-114">Propriedades</span><span class="sxs-lookup"><span data-stu-id="73087-114">Properties</span></span>

<span data-ttu-id="73087-115">A interface **IVMFloppyDriveCollection** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="73087-115">The **IVMFloppyDriveCollection** interface has these properties.</span></span>



| <span data-ttu-id="73087-116">Propriedade</span><span class="sxs-lookup"><span data-stu-id="73087-116">Property</span></span>                                                          | <span data-ttu-id="73087-117">Tipo de acesso</span><span class="sxs-lookup"><span data-stu-id="73087-117">Access type</span></span>          | <span data-ttu-id="73087-118">Descrição</span><span class="sxs-lookup"><span data-stu-id="73087-118">Description</span></span>                                                                 |
|:------------------------------------------------------------------|:---------------------|:----------------------------------------------------------------------------|
| [<span data-ttu-id="73087-119">**\_NewEnum**</span><span class="sxs-lookup"><span data-stu-id="73087-119">**\_NewEnum**</span></span>](ivmfloppydrivecollection--newenum.md)<br/> | <span data-ttu-id="73087-120">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="73087-120">Read-only</span></span><br/> | <span data-ttu-id="73087-121">Um enumerador para a coleção.</span><span class="sxs-lookup"><span data-stu-id="73087-121">An enumerator for the collection.</span></span><br/>                                |
| [<span data-ttu-id="73087-122">**Contar**</span><span class="sxs-lookup"><span data-stu-id="73087-122">**Count**</span></span>](ivmfloppydrivecollection-count.md)<br/>        | <span data-ttu-id="73087-123">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="73087-123">Read-only</span></span><br/> | <span data-ttu-id="73087-124">O número de unidades de disquete nesta coleção.</span><span class="sxs-lookup"><span data-stu-id="73087-124">The number of floppy drives in this collection.</span></span><br/>                  |
| [<span data-ttu-id="73087-125">**Item**</span><span class="sxs-lookup"><span data-stu-id="73087-125">**Item**</span></span>](ivmfloppydrivecollection-item.md)<br/>          | <span data-ttu-id="73087-126">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="73087-126">Read-only</span></span><br/> | <span data-ttu-id="73087-127">O objeto da unidade de disquete que corresponde ao índice especificado.</span><span class="sxs-lookup"><span data-stu-id="73087-127">The floppy drive object that corresponds to the specified index.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="73087-128">Requisitos</span><span class="sxs-lookup"><span data-stu-id="73087-128">Requirements</span></span>



| <span data-ttu-id="73087-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="73087-129">Requirement</span></span> | <span data-ttu-id="73087-130">Valor</span><span class="sxs-lookup"><span data-stu-id="73087-130">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="73087-131">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="73087-131">Minimum supported client</span></span><br/> | <span data-ttu-id="73087-132">\[Somente aplicativos de área de trabalho do Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="73087-132">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="73087-133">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="73087-133">Minimum supported server</span></span><br/> | <span data-ttu-id="73087-134">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="73087-134">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="73087-135">Fim do suporte do cliente</span><span class="sxs-lookup"><span data-stu-id="73087-135">End of client support</span></span><br/>    | <span data-ttu-id="73087-136">Windows 7</span><span class="sxs-lookup"><span data-stu-id="73087-136">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="73087-137">Produto</span><span class="sxs-lookup"><span data-stu-id="73087-137">Product</span></span><br/>                  | <span data-ttu-id="73087-138">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="73087-138">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="73087-139">parâmetro</span><span class="sxs-lookup"><span data-stu-id="73087-139">Header</span></span><br/>                   | <dl> <span data-ttu-id="73087-140"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="73087-140"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="73087-141">IID</span><span class="sxs-lookup"><span data-stu-id="73087-141">IID</span></span><br/>                      | <span data-ttu-id="73087-142">IID \_ IVMFloppyDriveCollection é definido como 8ba70a25-f698-4ee5-85CE-3cc93a925516</span><span class="sxs-lookup"><span data-stu-id="73087-142">IID\_IVMFloppyDriveCollection is defined as 8ba70a25-f698-4ee5-85ce-3cc93a925516</span></span><br/>   |



## <a name="see-also"></a><span data-ttu-id="73087-143">Confira também</span><span class="sxs-lookup"><span data-stu-id="73087-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="73087-144">**IVMFloppyDrive**</span><span class="sxs-lookup"><span data-stu-id="73087-144">**IVMFloppyDrive**</span></span>](ivmfloppydrive.md)
</dt> <dt>

[<span data-ttu-id="73087-145">**IVMVirtualMachine::FloppyDrives**</span><span class="sxs-lookup"><span data-stu-id="73087-145">**IVMVirtualMachine::FloppyDrives**</span></span>](ivmvirtualmachine-floppydrives.md)
</dt> </dl>

 

