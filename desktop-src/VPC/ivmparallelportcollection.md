---
title: Interface IVMParallelPortCollection (VPCCOMInterfaces. h)
description: Define a coleção de portas paralelas na máquina virtual. Para obter um objeto IVMParallelPortCollection, use a propriedade IVMVirtualMachine ParallelPorts.
ms.assetid: 038a5c08-cd92-426f-a059-9a4c2110548d
keywords:
- Virtual PC de interface IVMParallelPortCollection
- Virtual PC de interface IVMParallelPortCollection, descrito
topic_type:
- apiref
api_name:
- IVMParallelPortCollection
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8284b3720e0272147c932cfbfd70448babf5606f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104086346"
---
# <a name="ivmparallelportcollection-interface"></a><span data-ttu-id="c1326-106">Interface IVMParallelPortCollection</span><span class="sxs-lookup"><span data-stu-id="c1326-106">IVMParallelPortCollection interface</span></span>

<span data-ttu-id="c1326-107">\[O Windows Virtual PC não está mais disponível para uso a partir do Windows 8.</span><span class="sxs-lookup"><span data-stu-id="c1326-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="c1326-108">Em vez disso, use o [provedor WMI do Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="c1326-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="c1326-109">Define a coleção de portas paralelas na máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="c1326-109">Defines the collection of parallel ports within the virtual machine.</span></span> <span data-ttu-id="c1326-110">Para obter um objeto **IVMParallelPortCollection** , use a propriedade [**IVMVirtualMachine::P arallelports**](ivmvirtualmachine-parallelports.md) .</span><span class="sxs-lookup"><span data-stu-id="c1326-110">To obtain an **IVMParallelPortCollection** object, use the [**IVMVirtualMachine::ParallelPorts**](ivmvirtualmachine-parallelports.md) property.</span></span>

## <a name="members"></a><span data-ttu-id="c1326-111">Membros</span><span class="sxs-lookup"><span data-stu-id="c1326-111">Members</span></span>

<span data-ttu-id="c1326-112">A interface **IVMParallelPortCollection** herda da interface [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) .</span><span class="sxs-lookup"><span data-stu-id="c1326-112">The **IVMParallelPortCollection** interface inherits from the [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interface.</span></span> <span data-ttu-id="c1326-113">**IVMParallelPortCollection** também tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="c1326-113">**IVMParallelPortCollection** also has these types of members:</span></span>

-   [<span data-ttu-id="c1326-114">Propriedades</span><span class="sxs-lookup"><span data-stu-id="c1326-114">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="c1326-115">Propriedades</span><span class="sxs-lookup"><span data-stu-id="c1326-115">Properties</span></span>

<span data-ttu-id="c1326-116">A interface **IVMParallelPortCollection** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="c1326-116">The **IVMParallelPortCollection** interface has these properties.</span></span>



| <span data-ttu-id="c1326-117">Propriedade</span><span class="sxs-lookup"><span data-stu-id="c1326-117">Property</span></span>                                                           | <span data-ttu-id="c1326-118">Tipo de acesso</span><span class="sxs-lookup"><span data-stu-id="c1326-118">Access type</span></span>          | <span data-ttu-id="c1326-119">Descrição</span><span class="sxs-lookup"><span data-stu-id="c1326-119">Description</span></span>                                                                  |
|:-------------------------------------------------------------------|:---------------------|:-----------------------------------------------------------------------------|
| [<span data-ttu-id="c1326-120">**\_NewEnum**</span><span class="sxs-lookup"><span data-stu-id="c1326-120">**\_NewEnum**</span></span>](ivmparallelportcollection--newenum.md)<br/> | <span data-ttu-id="c1326-121">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="c1326-121">Read-only</span></span><br/> | <span data-ttu-id="c1326-122">Um enumerador para a coleção.</span><span class="sxs-lookup"><span data-stu-id="c1326-122">An enumerator for the collection.</span></span><br/>                                 |
| [<span data-ttu-id="c1326-123">**Contar**</span><span class="sxs-lookup"><span data-stu-id="c1326-123">**Count**</span></span>](ivmparallelportcollection-count.md)<br/>        | <span data-ttu-id="c1326-124">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="c1326-124">Read-only</span></span><br/> | <span data-ttu-id="c1326-125">O número de portas paralelas nesta coleção.</span><span class="sxs-lookup"><span data-stu-id="c1326-125">The number of parallel ports in this collection.</span></span><br/>                  |
| [<span data-ttu-id="c1326-126">**Item**</span><span class="sxs-lookup"><span data-stu-id="c1326-126">**Item**</span></span>](ivmparallelportcollection-item.md)<br/>          | <span data-ttu-id="c1326-127">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="c1326-127">Read-only</span></span><br/> | <span data-ttu-id="c1326-128">O objeto de porta paralela que corresponde ao índice especificado.</span><span class="sxs-lookup"><span data-stu-id="c1326-128">The parallel port object that corresponds to the specified index.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="c1326-129">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c1326-129">Requirements</span></span>



| <span data-ttu-id="c1326-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="c1326-130">Requirement</span></span> | <span data-ttu-id="c1326-131">Valor</span><span class="sxs-lookup"><span data-stu-id="c1326-131">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="c1326-132">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c1326-132">Minimum supported client</span></span><br/> | <span data-ttu-id="c1326-133">\[Somente aplicativos de área de trabalho do Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="c1326-133">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="c1326-134">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c1326-134">Minimum supported server</span></span><br/> | <span data-ttu-id="c1326-135">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="c1326-135">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="c1326-136">Fim do suporte do cliente</span><span class="sxs-lookup"><span data-stu-id="c1326-136">End of client support</span></span><br/>    | <span data-ttu-id="c1326-137">Windows 7</span><span class="sxs-lookup"><span data-stu-id="c1326-137">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="c1326-138">Produto</span><span class="sxs-lookup"><span data-stu-id="c1326-138">Product</span></span><br/>                  | <span data-ttu-id="c1326-139">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="c1326-139">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="c1326-140">parâmetro</span><span class="sxs-lookup"><span data-stu-id="c1326-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="c1326-141"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="c1326-141"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="c1326-142">IID</span><span class="sxs-lookup"><span data-stu-id="c1326-142">IID</span></span><br/>                      | <span data-ttu-id="c1326-143">IID \_ IVMParallelPortCollection é definido como 27c3e036-198f-430c-8735-6e652f7203fd</span><span class="sxs-lookup"><span data-stu-id="c1326-143">IID\_IVMParallelPortCollection is defined as 27c3e036-198f-430c-8735-6e652f7203fd</span></span><br/>  |



## <a name="see-also"></a><span data-ttu-id="c1326-144">Confira também</span><span class="sxs-lookup"><span data-stu-id="c1326-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c1326-145">**IVMParallelPort**</span><span class="sxs-lookup"><span data-stu-id="c1326-145">**IVMParallelPort**</span></span>](ivmparallelport.md)
</dt> <dt>

[<span data-ttu-id="c1326-146">**IVMVirtualMachine::P arallelPorts**</span><span class="sxs-lookup"><span data-stu-id="c1326-146">**IVMVirtualMachine::ParallelPorts**</span></span>](ivmvirtualmachine-parallelports.md)
</dt> </dl>

 

