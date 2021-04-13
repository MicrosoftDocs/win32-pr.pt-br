---
title: Propriedade IVMHostInfo MemoryTotalString (VPCCOMInterfaces. h)
description: Recupera a quantidade total de memória física no computador host, em megabytes, como uma cadeia de caracteres.
ms.assetid: 732c62e5-2776-4551-909f-7ddab74e067d
keywords:
- Propriedade MemoryTotalString Virtual PC
- Propriedade MemoryTotalString Virtual PC, interface IVMHostInfo
- IVMHostInfo interface virtual PC, Propriedade MemoryTotalString
topic_type:
- apiref
api_name:
- IVMHostInfo.MemoryTotalString
- IVMHostInfo.get_MemoryTotalString
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a5e6c16a4215aba141ff1803d340c63dc9faa868
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104369690"
---
# <a name="ivmhostinfomemorytotalstring-property"></a><span data-ttu-id="83e10-106">Propriedade IVMHostInfo:: MemoryTotalString</span><span class="sxs-lookup"><span data-stu-id="83e10-106">IVMHostInfo::MemoryTotalString property</span></span>

<span data-ttu-id="83e10-107">\[O Windows Virtual PC não está mais disponível para uso a partir do Windows 8.</span><span class="sxs-lookup"><span data-stu-id="83e10-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="83e10-108">Em vez disso, use o [provedor WMI do Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="83e10-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="83e10-109">Recupera a quantidade total de memória física no computador host, em megabytes, como uma cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="83e10-109">Retrieves the total amount of physical memory in the host machine, in megabytes, as a string.</span></span>

<span data-ttu-id="83e10-110">Esta propriedade é somente para leitura.</span><span class="sxs-lookup"><span data-stu-id="83e10-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="83e10-111">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="83e10-111">Syntax</span></span>


```C++
HRESULT get_MemoryTotalString(
  [out, retval] BSTR *megabytesOfMemory
);
```



## <a name="property-value"></a><span data-ttu-id="83e10-112">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="83e10-112">Property value</span></span>

<span data-ttu-id="83e10-113">A quantidade total de memória física, em megabytes.</span><span class="sxs-lookup"><span data-stu-id="83e10-113">The total amount of physical memory, in megabytes.</span></span>

## <a name="error-codes"></a><span data-ttu-id="83e10-114">Códigos do Erro</span><span class="sxs-lookup"><span data-stu-id="83e10-114">Error codes</span></span>



| <span data-ttu-id="83e10-115">Nome/valor</span><span class="sxs-lookup"><span data-stu-id="83e10-115">Name/value</span></span>                                                                                                                                                    | <span data-ttu-id="83e10-116">Significado</span><span class="sxs-lookup"><span data-stu-id="83e10-116">Meaning</span></span>                                      |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="83e10-117"><dt>S \_ OK</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="83e10-117"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                       | <span data-ttu-id="83e10-118">A operação foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="83e10-118">The operation was successful.</span></span><br/>     |
| <dl> <span data-ttu-id="83e10-119"><dt>E \_ </dt> <dt>0X80004003</dt> de ponteiro</span><span class="sxs-lookup"><span data-stu-id="83e10-119"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>         | <span data-ttu-id="83e10-120">O parâmetro é **NULL**.</span><span class="sxs-lookup"><span data-stu-id="83e10-120">The parameter is **NULL**.</span></span><br/>        |
| <dl> <span data-ttu-id="83e10-121"><dt>DISP \_ E \_ </dt> <dt>0x80020009</dt> de exceção</span><span class="sxs-lookup"><span data-stu-id="83e10-121"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl> | <span data-ttu-id="83e10-122">Ocorreu um erro inesperado.</span><span class="sxs-lookup"><span data-stu-id="83e10-122">An unexpected error has occurred.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="83e10-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="83e10-123">Requirements</span></span>



| <span data-ttu-id="83e10-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="83e10-124">Requirement</span></span> | <span data-ttu-id="83e10-125">Valor</span><span class="sxs-lookup"><span data-stu-id="83e10-125">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="83e10-126">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="83e10-126">Minimum supported client</span></span><br/> | <span data-ttu-id="83e10-127">\[Somente aplicativos de área de trabalho do Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="83e10-127">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="83e10-128">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="83e10-128">Minimum supported server</span></span><br/> | <span data-ttu-id="83e10-129">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="83e10-129">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="83e10-130">Fim do suporte do cliente</span><span class="sxs-lookup"><span data-stu-id="83e10-130">End of client support</span></span><br/>    | <span data-ttu-id="83e10-131">Windows 7</span><span class="sxs-lookup"><span data-stu-id="83e10-131">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="83e10-132">Produto</span><span class="sxs-lookup"><span data-stu-id="83e10-132">Product</span></span><br/>                  | <span data-ttu-id="83e10-133">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="83e10-133">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="83e10-134">parâmetro</span><span class="sxs-lookup"><span data-stu-id="83e10-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="83e10-135"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="83e10-135"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="83e10-136">IID</span><span class="sxs-lookup"><span data-stu-id="83e10-136">IID</span></span><br/>                      | <span data-ttu-id="83e10-137">IID \_ IVMHostInfo é definido como 5b5cf343-05ad-453b-be99-adf4e27b2ebc</span><span class="sxs-lookup"><span data-stu-id="83e10-137">IID\_IVMHostInfo is defined as 5b5cf343-05ad-453b-be99-adf4e27b2ebc</span></span><br/>                |



## <a name="see-also"></a><span data-ttu-id="83e10-138">Confira também</span><span class="sxs-lookup"><span data-stu-id="83e10-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="83e10-139">**IVMHostInfo**</span><span class="sxs-lookup"><span data-stu-id="83e10-139">**IVMHostInfo**</span></span>](ivmhostinfo.md)
</dt> </dl>

 

