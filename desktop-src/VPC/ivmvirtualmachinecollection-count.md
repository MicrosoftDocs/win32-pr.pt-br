---
title: Propriedade Count de IVMVirtualMachineCollection (VPCCOMInterfaces. h)
description: Recupera o número de máquinas virtuais nesta coleção.
ms.assetid: c1f38528-fd9b-4b86-aac6-de944379b92e
keywords:
- Propriedade de contagem Virtual PC
- Propriedade Count Virtual PC, interface IVMVirtualMachineCollection
- Virtual PC de interface IVMVirtualMachineCollection, Propriedade Count
topic_type:
- apiref
api_name:
- IVMVirtualMachineCollection.Count
- IVMVirtualMachineCollection.get_Count
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f641fad504c6dd593737cf35014813f49609a4aa
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104086212"
---
# <a name="ivmvirtualmachinecollectioncount-property"></a><span data-ttu-id="beebb-106">Propriedade IVMVirtualMachineCollection:: Count</span><span class="sxs-lookup"><span data-stu-id="beebb-106">IVMVirtualMachineCollection::Count property</span></span>

<span data-ttu-id="beebb-107">\[O Windows Virtual PC não está mais disponível para uso a partir do Windows 8.</span><span class="sxs-lookup"><span data-stu-id="beebb-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="beebb-108">Em vez disso, use o [provedor WMI do Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="beebb-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="beebb-109">Recupera o número de máquinas virtuais nesta coleção.</span><span class="sxs-lookup"><span data-stu-id="beebb-109">Retrieves the number of virtual machines in this collection.</span></span>

<span data-ttu-id="beebb-110">Esta propriedade é somente para leitura.</span><span class="sxs-lookup"><span data-stu-id="beebb-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="beebb-111">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="beebb-111">Syntax</span></span>


```C++
HRESULT get_Count(
  [out, retval] long *count
);
```



## <a name="property-value"></a><span data-ttu-id="beebb-112">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="beebb-112">Property value</span></span>

<span data-ttu-id="beebb-113">O número de máquinas virtuais.</span><span class="sxs-lookup"><span data-stu-id="beebb-113">The number of virtual machines.</span></span>

## <a name="error-codes"></a><span data-ttu-id="beebb-114">Códigos do Erro</span><span class="sxs-lookup"><span data-stu-id="beebb-114">Error codes</span></span>



| <span data-ttu-id="beebb-115">Nome/valor</span><span class="sxs-lookup"><span data-stu-id="beebb-115">Name/value</span></span>                                                                                                                                                    | <span data-ttu-id="beebb-116">Significado</span><span class="sxs-lookup"><span data-stu-id="beebb-116">Meaning</span></span>                                      |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="beebb-117"><dt>S \_ OK</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="beebb-117"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                       | <span data-ttu-id="beebb-118">A operação foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="beebb-118">The operation was successful.</span></span><br/>     |
| <dl> <span data-ttu-id="beebb-119"><dt>E \_ </dt> <dt>0X80004003</dt> de ponteiro</span><span class="sxs-lookup"><span data-stu-id="beebb-119"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>         | <span data-ttu-id="beebb-120">O parâmetro é **NULL**.</span><span class="sxs-lookup"><span data-stu-id="beebb-120">The parameter is **NULL**.</span></span><br/>        |
| <dl> <span data-ttu-id="beebb-121"><dt>DISP \_ E \_ </dt> <dt>0x80020009</dt> de exceção</span><span class="sxs-lookup"><span data-stu-id="beebb-121"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl> | <span data-ttu-id="beebb-122">Ocorreu um erro inesperado.</span><span class="sxs-lookup"><span data-stu-id="beebb-122">An unexpected error has occurred.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="beebb-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="beebb-123">Requirements</span></span>



| <span data-ttu-id="beebb-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="beebb-124">Requirement</span></span> | <span data-ttu-id="beebb-125">Valor</span><span class="sxs-lookup"><span data-stu-id="beebb-125">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="beebb-126">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="beebb-126">Minimum supported client</span></span><br/> | <span data-ttu-id="beebb-127">\[Somente aplicativos de área de trabalho do Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="beebb-127">Windows 7 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="beebb-128">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="beebb-128">Minimum supported server</span></span><br/> | <span data-ttu-id="beebb-129">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="beebb-129">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="beebb-130">Fim do suporte do cliente</span><span class="sxs-lookup"><span data-stu-id="beebb-130">End of client support</span></span><br/>    | <span data-ttu-id="beebb-131">Windows 7</span><span class="sxs-lookup"><span data-stu-id="beebb-131">Windows 7</span></span><br/>                                                                           |
| <span data-ttu-id="beebb-132">Produto</span><span class="sxs-lookup"><span data-stu-id="beebb-132">Product</span></span><br/>                  | <span data-ttu-id="beebb-133">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="beebb-133">Windows Virtual PC</span></span><br/>                                                                  |
| <span data-ttu-id="beebb-134">parâmetro</span><span class="sxs-lookup"><span data-stu-id="beebb-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="beebb-135"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="beebb-135"><dt>VPCCOMInterfaces.h</dt></span></span> </dl>  |
| <span data-ttu-id="beebb-136">IID</span><span class="sxs-lookup"><span data-stu-id="beebb-136">IID</span></span><br/>                      | <span data-ttu-id="beebb-137">IID \_ IVMVirtualMachineCollection é definido como 59f31786-2a3d-4fbf-9896-d85338ca0da1</span><span class="sxs-lookup"><span data-stu-id="beebb-137">IID\_IVMVirtualMachineCollection is defined as 59f31786-2a3d-4fbf-9896-d85338ca0da1</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="beebb-138">Confira também</span><span class="sxs-lookup"><span data-stu-id="beebb-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="beebb-139">**IVMVirtualMachineCollection**</span><span class="sxs-lookup"><span data-stu-id="beebb-139">**IVMVirtualMachineCollection**</span></span>](ivmvirtualmachinecollection.md)
</dt> </dl>

 

