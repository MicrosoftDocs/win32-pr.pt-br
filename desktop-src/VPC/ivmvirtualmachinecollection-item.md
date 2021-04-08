---
title: Propriedade de item IVMVirtualMachineCollection (VPCCOMInterfaces. h)
description: Recupera o objeto de máquina virtual que corresponde ao índice especificado.
ms.assetid: b3afe211-5d97-4ccf-96b7-e074deb320fb
keywords:
- Propriedade do item Virtual PC
- Propriedade de item Virtual PC, interface IVMVirtualMachineCollection
- IVMVirtualMachineCollection interface virtual PC, Propriedade Item
topic_type:
- apiref
api_name:
- IVMVirtualMachineCollection.Item
- IVMVirtualMachineCollection.get_Item
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d4d70a6e30ff53f234f40803cd02fa16539f09e4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104008802"
---
# <a name="ivmvirtualmachinecollectionitem-property"></a><span data-ttu-id="3a543-106">Propriedade IVMVirtualMachineCollection:: item</span><span class="sxs-lookup"><span data-stu-id="3a543-106">IVMVirtualMachineCollection::Item property</span></span>

<span data-ttu-id="3a543-107">\[O Windows Virtual PC não está mais disponível para uso a partir do Windows 8.</span><span class="sxs-lookup"><span data-stu-id="3a543-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="3a543-108">Em vez disso, use o [provedor WMI do Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="3a543-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="3a543-109">Recupera o objeto de máquina virtual que corresponde ao índice especificado.</span><span class="sxs-lookup"><span data-stu-id="3a543-109">Retrieves the virtual machine object that corresponds to the specified index.</span></span>

<span data-ttu-id="3a543-110">Esta propriedade é somente para leitura.</span><span class="sxs-lookup"><span data-stu-id="3a543-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="3a543-111">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="3a543-111">Syntax</span></span>


```C++
HRESULT get_Item(
  [in]          long              index,
  [out, retval] IVMVirtualMachine **virtualMachine
);
```



## <a name="property-value"></a><span data-ttu-id="3a543-112">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="3a543-112">Property value</span></span>

<span data-ttu-id="3a543-113">O objeto [**IVMVirtualMachine**](ivmvirtualmachine.md) .</span><span class="sxs-lookup"><span data-stu-id="3a543-113">The [**IVMVirtualMachine**](ivmvirtualmachine.md) object.</span></span>

## <a name="error-codes"></a><span data-ttu-id="3a543-114">Códigos do Erro</span><span class="sxs-lookup"><span data-stu-id="3a543-114">Error codes</span></span>



| <span data-ttu-id="3a543-115">Nome/valor</span><span class="sxs-lookup"><span data-stu-id="3a543-115">Name/value</span></span>                                                                                                                                                    | <span data-ttu-id="3a543-116">Significado</span><span class="sxs-lookup"><span data-stu-id="3a543-116">Meaning</span></span>                                                                                        |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="3a543-117"><dt>S \_ OK</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="3a543-117"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                       | <span data-ttu-id="3a543-118">A operação foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="3a543-118">The operation was successful.</span></span> <br/>                                                      |
| <dl> <span data-ttu-id="3a543-119"><dt>E \_ </dt> <dt>0X80004003</dt> de ponteiro</span><span class="sxs-lookup"><span data-stu-id="3a543-119"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>         | <span data-ttu-id="3a543-120">O parâmetro *VirtualMachine* é **nulo**.</span><span class="sxs-lookup"><span data-stu-id="3a543-120">The *virtualMachine* parameter is **NULL**.</span></span> <br/>                                        |
| <dl> <span data-ttu-id="3a543-121"><dt>DISP \_ E \_ BADINDEX</dt> <dt>0x8002000B</dt></span><span class="sxs-lookup"><span data-stu-id="3a543-121"><dt>DISP\_E\_BADINDEX</dt> <dt>0x8002000B</dt></span></span> </dl>  | <span data-ttu-id="3a543-122">O índice do item solicitado não corresponde a um item nesta coleção.</span><span class="sxs-lookup"><span data-stu-id="3a543-122">The index of the requested item does not correspond to an item in this collection.</span></span> <br/> |
| <dl> <span data-ttu-id="3a543-123"><dt>DISP \_ E \_ </dt> <dt>0x80020009</dt> de exceção</span><span class="sxs-lookup"><span data-stu-id="3a543-123"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl> | <span data-ttu-id="3a543-124">Ocorreu um erro inesperado.</span><span class="sxs-lookup"><span data-stu-id="3a543-124">An unexpected error has occurred.</span></span><br/>                                                   |



## <a name="requirements"></a><span data-ttu-id="3a543-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3a543-125">Requirements</span></span>



| <span data-ttu-id="3a543-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="3a543-126">Requirement</span></span> | <span data-ttu-id="3a543-127">Valor</span><span class="sxs-lookup"><span data-stu-id="3a543-127">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3a543-128">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3a543-128">Minimum supported client</span></span><br/> | <span data-ttu-id="3a543-129">\[Somente aplicativos de área de trabalho do Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="3a543-129">Windows 7 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="3a543-130">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3a543-130">Minimum supported server</span></span><br/> | <span data-ttu-id="3a543-131">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="3a543-131">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="3a543-132">Fim do suporte do cliente</span><span class="sxs-lookup"><span data-stu-id="3a543-132">End of client support</span></span><br/>    | <span data-ttu-id="3a543-133">Windows 7</span><span class="sxs-lookup"><span data-stu-id="3a543-133">Windows 7</span></span><br/>                                                                           |
| <span data-ttu-id="3a543-134">Produto</span><span class="sxs-lookup"><span data-stu-id="3a543-134">Product</span></span><br/>                  | <span data-ttu-id="3a543-135">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="3a543-135">Windows Virtual PC</span></span><br/>                                                                  |
| <span data-ttu-id="3a543-136">parâmetro</span><span class="sxs-lookup"><span data-stu-id="3a543-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="3a543-137"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="3a543-137"><dt>VPCCOMInterfaces.h</dt></span></span> </dl>  |
| <span data-ttu-id="3a543-138">IID</span><span class="sxs-lookup"><span data-stu-id="3a543-138">IID</span></span><br/>                      | <span data-ttu-id="3a543-139">IID \_ IVMVirtualMachineCollection é definido como 59f31786-2a3d-4fbf-9896-d85338ca0da1</span><span class="sxs-lookup"><span data-stu-id="3a543-139">IID\_IVMVirtualMachineCollection is defined as 59f31786-2a3d-4fbf-9896-d85338ca0da1</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="3a543-140">Confira também</span><span class="sxs-lookup"><span data-stu-id="3a543-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3a543-141">**IVMVirtualMachine**</span><span class="sxs-lookup"><span data-stu-id="3a543-141">**IVMVirtualMachine**</span></span>](ivmvirtualmachine.md)
</dt> <dt>

[<span data-ttu-id="3a543-142">**IVMVirtualMachineCollection**</span><span class="sxs-lookup"><span data-stu-id="3a543-142">**IVMVirtualMachineCollection**</span></span>](ivmvirtualmachinecollection.md)
</dt> </dl>

 

