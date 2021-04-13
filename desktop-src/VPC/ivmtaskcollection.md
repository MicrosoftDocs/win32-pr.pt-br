---
title: Interface IVMTaskCollection (VPCCOMInterfaces. h)
description: Define a coleção de objetos de tarefa. Para obter um objeto IVMTaskCollection, use a propriedade IVMVirtualPC Tasks.
ms.assetid: 5cfc543c-81a1-49d2-93a9-9b1db1cb5070
keywords:
- Virtual PC de interface IVMTaskCollection
- Virtual PC de interface IVMTaskCollection, descrito
topic_type:
- apiref
api_name:
- IVMTaskCollection
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 43ff7a4b12b936f2b5c72a73818eca0f927eef12
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104369808"
---
# <a name="ivmtaskcollection-interface"></a><span data-ttu-id="39c1a-106">Interface IVMTaskCollection</span><span class="sxs-lookup"><span data-stu-id="39c1a-106">IVMTaskCollection interface</span></span>

<span data-ttu-id="39c1a-107">\[O Windows Virtual PC não está mais disponível para uso a partir do Windows 8.</span><span class="sxs-lookup"><span data-stu-id="39c1a-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="39c1a-108">Em vez disso, use o [provedor WMI do Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="39c1a-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="39c1a-109">Define a coleção de objetos de tarefa.</span><span class="sxs-lookup"><span data-stu-id="39c1a-109">Defines the collection of task objects.</span></span> <span data-ttu-id="39c1a-110">Para obter um objeto **IVMTaskCollection** , use a propriedade [**IVMVirtualPC:: Tasks**](ivmvirtualpc-tasks.md) .</span><span class="sxs-lookup"><span data-stu-id="39c1a-110">To obtain an **IVMTaskCollection** object, use the [**IVMVirtualPC::Tasks**](ivmvirtualpc-tasks.md) property.</span></span>

## <a name="members"></a><span data-ttu-id="39c1a-111">Membros</span><span class="sxs-lookup"><span data-stu-id="39c1a-111">Members</span></span>

<span data-ttu-id="39c1a-112">A interface **IVMTaskCollection** herda da interface [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) .</span><span class="sxs-lookup"><span data-stu-id="39c1a-112">The **IVMTaskCollection** interface inherits from the [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interface.</span></span> <span data-ttu-id="39c1a-113">**IVMTaskCollection** também tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="39c1a-113">**IVMTaskCollection** also has these types of members:</span></span>

-   [<span data-ttu-id="39c1a-114">Propriedades</span><span class="sxs-lookup"><span data-stu-id="39c1a-114">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="39c1a-115">Propriedades</span><span class="sxs-lookup"><span data-stu-id="39c1a-115">Properties</span></span>

<span data-ttu-id="39c1a-116">A interface **IVMTaskCollection** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="39c1a-116">The **IVMTaskCollection** interface has these properties.</span></span>



| <span data-ttu-id="39c1a-117">Propriedade</span><span class="sxs-lookup"><span data-stu-id="39c1a-117">Property</span></span>                                                   | <span data-ttu-id="39c1a-118">Tipo de acesso</span><span class="sxs-lookup"><span data-stu-id="39c1a-118">Access type</span></span>          | <span data-ttu-id="39c1a-119">Descrição</span><span class="sxs-lookup"><span data-stu-id="39c1a-119">Description</span></span>                                                         |
|:-----------------------------------------------------------|:---------------------|:--------------------------------------------------------------------|
| [<span data-ttu-id="39c1a-120">**\_NewEnum**</span><span class="sxs-lookup"><span data-stu-id="39c1a-120">**\_NewEnum**</span></span>](ivmtaskcollection--newenum.md)<br/> | <span data-ttu-id="39c1a-121">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="39c1a-121">Read-only</span></span><br/> | <span data-ttu-id="39c1a-122">Um enumerador para a coleção.</span><span class="sxs-lookup"><span data-stu-id="39c1a-122">An enumerator for the collection.</span></span><br/>                        |
| [<span data-ttu-id="39c1a-123">**Contar**</span><span class="sxs-lookup"><span data-stu-id="39c1a-123">**Count**</span></span>](ivmtaskcollection-count.md)<br/>        | <span data-ttu-id="39c1a-124">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="39c1a-124">Read-only</span></span><br/> | <span data-ttu-id="39c1a-125">O número de tarefas nesta coleção.</span><span class="sxs-lookup"><span data-stu-id="39c1a-125">The number of tasks in this collection.</span></span><br/>                  |
| [<span data-ttu-id="39c1a-126">**Item**</span><span class="sxs-lookup"><span data-stu-id="39c1a-126">**Item**</span></span>](ivmtaskcollection-item.md)<br/>          | <span data-ttu-id="39c1a-127">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="39c1a-127">Read-only</span></span><br/> | <span data-ttu-id="39c1a-128">O objeto de tarefa que corresponde ao índice especificado.</span><span class="sxs-lookup"><span data-stu-id="39c1a-128">The task object that corresponds to the specified index.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="39c1a-129">Requisitos</span><span class="sxs-lookup"><span data-stu-id="39c1a-129">Requirements</span></span>



| <span data-ttu-id="39c1a-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="39c1a-130">Requirement</span></span> | <span data-ttu-id="39c1a-131">Valor</span><span class="sxs-lookup"><span data-stu-id="39c1a-131">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="39c1a-132">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="39c1a-132">Minimum supported client</span></span><br/> | <span data-ttu-id="39c1a-133">\[Somente aplicativos de área de trabalho do Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="39c1a-133">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="39c1a-134">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="39c1a-134">Minimum supported server</span></span><br/> | <span data-ttu-id="39c1a-135">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="39c1a-135">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="39c1a-136">Fim do suporte do cliente</span><span class="sxs-lookup"><span data-stu-id="39c1a-136">End of client support</span></span><br/>    | <span data-ttu-id="39c1a-137">Windows 7</span><span class="sxs-lookup"><span data-stu-id="39c1a-137">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="39c1a-138">Produto</span><span class="sxs-lookup"><span data-stu-id="39c1a-138">Product</span></span><br/>                  | <span data-ttu-id="39c1a-139">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="39c1a-139">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="39c1a-140">parâmetro</span><span class="sxs-lookup"><span data-stu-id="39c1a-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="39c1a-141"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="39c1a-141"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="39c1a-142">IID</span><span class="sxs-lookup"><span data-stu-id="39c1a-142">IID</span></span><br/>                      | <span data-ttu-id="39c1a-143">IID \_ IVMTaskCollection é definido como 5c4387c8-0e8b-4b97-8058-84679adf4c40</span><span class="sxs-lookup"><span data-stu-id="39c1a-143">IID\_IVMTaskCollection is defined as 5c4387c8-0e8b-4b97-8058-84679adf4c40</span></span><br/>          |



## <a name="see-also"></a><span data-ttu-id="39c1a-144">Confira também</span><span class="sxs-lookup"><span data-stu-id="39c1a-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="39c1a-145">**IVMTask**</span><span class="sxs-lookup"><span data-stu-id="39c1a-145">**IVMTask**</span></span>](ivmtask.md)
</dt> <dt>

[<span data-ttu-id="39c1a-146">**IVMVirtualPC:: Tasks**</span><span class="sxs-lookup"><span data-stu-id="39c1a-146">**IVMVirtualPC::Tasks**</span></span>](ivmvirtualpc-tasks.md)
</dt> </dl>

 

