---
title: Interface IVMParallelPort (VPCCOMInterfaces. h)
description: Define uma porta paralela dentro de uma máquina virtual.
ms.assetid: da8daf16-5d22-49be-8fe9-72d5018c0622
keywords:
- Virtual PC de interface IVMParallelPort
- Virtual PC de interface IVMParallelPort, descrito
topic_type:
- apiref
api_name:
- IVMParallelPort
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 71b76b23f48e728104a3826afa80a8f272cd7e66
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105797518"
---
# <a name="ivmparallelport-interface"></a><span data-ttu-id="cb5b1-105">Interface IVMParallelPort</span><span class="sxs-lookup"><span data-stu-id="cb5b1-105">IVMParallelPort interface</span></span>

<span data-ttu-id="cb5b1-106">\[O Windows Virtual PC não está mais disponível para uso a partir do Windows 8.</span><span class="sxs-lookup"><span data-stu-id="cb5b1-106">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="cb5b1-107">Em vez disso, use o [provedor WMI do Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="cb5b1-107">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="cb5b1-108">Define uma porta paralela dentro de uma máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="cb5b1-108">Defines a parallel port inside a virtual machine.</span></span> <span data-ttu-id="cb5b1-109">Essa interface permite que você configure portas paralelas dentro de uma máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="cb5b1-109">This interface allows you to configure parallel ports inside a virtual machine.</span></span> <span data-ttu-id="cb5b1-110">Você pode recuperar um objeto **IVMParallelPort** do objeto [**IVMParallelPortCollection**](ivmparallelportcollection.md) retornado da propriedade [**IVMVirtualMachine::P arallelports**](ivmvirtualmachine-parallelports.md) .</span><span class="sxs-lookup"><span data-stu-id="cb5b1-110">You can retrieve an **IVMParallelPort** object from the [**IVMParallelPortCollection**](ivmparallelportcollection.md) object returned from the [**IVMVirtualMachine::ParallelPorts**](ivmvirtualmachine-parallelports.md) property.</span></span>

## <a name="members"></a><span data-ttu-id="cb5b1-111">Membros</span><span class="sxs-lookup"><span data-stu-id="cb5b1-111">Members</span></span>

<span data-ttu-id="cb5b1-112">A interface **IVMParallelPort** herda da interface [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) .</span><span class="sxs-lookup"><span data-stu-id="cb5b1-112">The **IVMParallelPort** interface inherits from the [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interface.</span></span> <span data-ttu-id="cb5b1-113">**IVMParallelPort** também tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="cb5b1-113">**IVMParallelPort** also has these types of members:</span></span>

-   [<span data-ttu-id="cb5b1-114">Métodos</span><span class="sxs-lookup"><span data-stu-id="cb5b1-114">Methods</span></span>](#methods)
-   [<span data-ttu-id="cb5b1-115">Propriedades</span><span class="sxs-lookup"><span data-stu-id="cb5b1-115">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="cb5b1-116">Métodos</span><span class="sxs-lookup"><span data-stu-id="cb5b1-116">Methods</span></span>

<span data-ttu-id="cb5b1-117">A interface **IVMParallelPort** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="cb5b1-117">The **IVMParallelPort** interface has these methods.</span></span>



| <span data-ttu-id="cb5b1-118">Método</span><span class="sxs-lookup"><span data-stu-id="cb5b1-118">Method</span></span>                              | <span data-ttu-id="cb5b1-119">Descrição</span><span class="sxs-lookup"><span data-stu-id="cb5b1-119">Description</span></span>                                                        |
|:------------------------------------|:-------------------------------------------------------------------|
| [<span data-ttu-id="cb5b1-120">**\_ID**</span><span class="sxs-lookup"><span data-stu-id="cb5b1-120">**\_ID**</span></span>](ivmparallelport--id.md) | <span data-ttu-id="cb5b1-121">Recupera o identificador interno da porta paralela.</span><span class="sxs-lookup"><span data-stu-id="cb5b1-121">Retrieves the internal identifier of the parallel port.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="cb5b1-122">Propriedades</span><span class="sxs-lookup"><span data-stu-id="cb5b1-122">Properties</span></span>

<span data-ttu-id="cb5b1-123">A interface **IVMParallelPort** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="cb5b1-123">The **IVMParallelPort** interface has these properties.</span></span>



| <span data-ttu-id="cb5b1-124">Propriedade</span><span class="sxs-lookup"><span data-stu-id="cb5b1-124">Property</span></span>                                        | <span data-ttu-id="cb5b1-125">Tipo de acesso</span><span class="sxs-lookup"><span data-stu-id="cb5b1-125">Access type</span></span>           | <span data-ttu-id="cb5b1-126">Descrição</span><span class="sxs-lookup"><span data-stu-id="cb5b1-126">Description</span></span>                               |
|:------------------------------------------------|:----------------------|:------------------------------------------|
| [<span data-ttu-id="cb5b1-127">**Nome**</span><span class="sxs-lookup"><span data-stu-id="cb5b1-127">**Name**</span></span>](ivmparallelport-name.md)<br/> | <span data-ttu-id="cb5b1-128">Leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="cb5b1-128">Read/write</span></span><br/> | <span data-ttu-id="cb5b1-129">O nome da porta paralela.</span><span class="sxs-lookup"><span data-stu-id="cb5b1-129">The name of the parallel port.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="cb5b1-130">Requisitos</span><span class="sxs-lookup"><span data-stu-id="cb5b1-130">Requirements</span></span>



| <span data-ttu-id="cb5b1-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="cb5b1-131">Requirement</span></span> | <span data-ttu-id="cb5b1-132">Valor</span><span class="sxs-lookup"><span data-stu-id="cb5b1-132">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="cb5b1-133">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="cb5b1-133">Minimum supported client</span></span><br/> | <span data-ttu-id="cb5b1-134">\[Somente aplicativos de área de trabalho do Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="cb5b1-134">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="cb5b1-135">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="cb5b1-135">Minimum supported server</span></span><br/> | <span data-ttu-id="cb5b1-136">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="cb5b1-136">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="cb5b1-137">Fim do suporte do cliente</span><span class="sxs-lookup"><span data-stu-id="cb5b1-137">End of client support</span></span><br/>    | <span data-ttu-id="cb5b1-138">Windows 7</span><span class="sxs-lookup"><span data-stu-id="cb5b1-138">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="cb5b1-139">Produto</span><span class="sxs-lookup"><span data-stu-id="cb5b1-139">Product</span></span><br/>                  | <span data-ttu-id="cb5b1-140">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="cb5b1-140">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="cb5b1-141">parâmetro</span><span class="sxs-lookup"><span data-stu-id="cb5b1-141">Header</span></span><br/>                   | <dl> <span data-ttu-id="cb5b1-142"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="cb5b1-142"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="cb5b1-143">IID</span><span class="sxs-lookup"><span data-stu-id="cb5b1-143">IID</span></span><br/>                      | <span data-ttu-id="cb5b1-144">IID \_ IVMParallelPort é definido como 097beecb-0a02-474f-abd6-298b22293fc6</span><span class="sxs-lookup"><span data-stu-id="cb5b1-144">IID\_IVMParallelPort is defined as 097beecb-0a02-474f-abd6-298b22293fc6</span></span><br/>            |



 

