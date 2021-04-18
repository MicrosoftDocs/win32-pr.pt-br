---
title: Propriedade IVMHostInfo MemoryAvail (VPCCOMInterfaces. h)
description: Recupera a quantidade de memória física disponível no computador host, em megabytes.
ms.assetid: cb593d02-cdb9-40f6-b57f-72fc3278f1bb
keywords:
- Propriedade MemoryAvail Virtual PC
- Propriedade MemoryAvail Virtual PC, interface IVMHostInfo
- IVMHostInfo interface virtual PC, Propriedade MemoryAvail
topic_type:
- apiref
api_name:
- IVMHostInfo.MemoryAvail
- IVMHostInfo.get_MemoryAvail
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1df6be8bf62595720d01372ee891184952a0dd5d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105778519"
---
# <a name="ivmhostinfomemoryavail-property"></a><span data-ttu-id="63b5c-106">Propriedade IVMHostInfo:: MemoryAvail</span><span class="sxs-lookup"><span data-stu-id="63b5c-106">IVMHostInfo::MemoryAvail property</span></span>

<span data-ttu-id="63b5c-107">\[O Windows Virtual PC não está mais disponível para uso a partir do Windows 8.</span><span class="sxs-lookup"><span data-stu-id="63b5c-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="63b5c-108">Em vez disso, use o [provedor WMI do Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="63b5c-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="63b5c-109">Recupera a quantidade de memória física disponível no computador host, em megabytes.</span><span class="sxs-lookup"><span data-stu-id="63b5c-109">Retrieves the amount of available physical memory in the host machine, in megabytes.</span></span>

<span data-ttu-id="63b5c-110">Esta propriedade é somente para leitura.</span><span class="sxs-lookup"><span data-stu-id="63b5c-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="63b5c-111">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="63b5c-111">Syntax</span></span>


```C++
HRESULT get_MemoryAvail(
  [out, retval] VARIANT *megabytesOfMemory
);
```



## <a name="property-value"></a><span data-ttu-id="63b5c-112">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="63b5c-112">Property value</span></span>

<span data-ttu-id="63b5c-113">A memória física disponível, em megabytes.</span><span class="sxs-lookup"><span data-stu-id="63b5c-113">The available physical memory, in megabytes.</span></span> <span data-ttu-id="63b5c-114">Esse valor é uma **variante** do tipo VT \_ decimal.</span><span class="sxs-lookup"><span data-stu-id="63b5c-114">This value is a **VARIANT** of type VT\_DECIMAL.</span></span>

## <a name="error-codes"></a><span data-ttu-id="63b5c-115">Códigos do Erro</span><span class="sxs-lookup"><span data-stu-id="63b5c-115">Error codes</span></span>



| <span data-ttu-id="63b5c-116">Nome/valor</span><span class="sxs-lookup"><span data-stu-id="63b5c-116">Name/value</span></span>                                                                                                                                                    | <span data-ttu-id="63b5c-117">Significado</span><span class="sxs-lookup"><span data-stu-id="63b5c-117">Meaning</span></span>                                      |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="63b5c-118"><dt>S \_ OK</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="63b5c-118"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                       | <span data-ttu-id="63b5c-119">A operação foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="63b5c-119">The operation was successful.</span></span><br/>     |
| <dl> <span data-ttu-id="63b5c-120"><dt>E \_ </dt> <dt>0X80004003</dt> de ponteiro</span><span class="sxs-lookup"><span data-stu-id="63b5c-120"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>         | <span data-ttu-id="63b5c-121">O parâmetro é **NULL**.</span><span class="sxs-lookup"><span data-stu-id="63b5c-121">The parameter is **NULL**.</span></span><br/>        |
| <dl> <span data-ttu-id="63b5c-122"><dt>DISP \_ E \_ </dt> <dt>0x80020009</dt> de exceção</span><span class="sxs-lookup"><span data-stu-id="63b5c-122"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl> | <span data-ttu-id="63b5c-123">Ocorreu um erro inesperado.</span><span class="sxs-lookup"><span data-stu-id="63b5c-123">An unexpected error has occurred.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="63b5c-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="63b5c-124">Requirements</span></span>



| <span data-ttu-id="63b5c-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="63b5c-125">Requirement</span></span> | <span data-ttu-id="63b5c-126">Valor</span><span class="sxs-lookup"><span data-stu-id="63b5c-126">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="63b5c-127">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="63b5c-127">Minimum supported client</span></span><br/> | <span data-ttu-id="63b5c-128">\[Somente aplicativos de área de trabalho do Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="63b5c-128">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="63b5c-129">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="63b5c-129">Minimum supported server</span></span><br/> | <span data-ttu-id="63b5c-130">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="63b5c-130">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="63b5c-131">Fim do suporte do cliente</span><span class="sxs-lookup"><span data-stu-id="63b5c-131">End of client support</span></span><br/>    | <span data-ttu-id="63b5c-132">Windows 7</span><span class="sxs-lookup"><span data-stu-id="63b5c-132">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="63b5c-133">Produto</span><span class="sxs-lookup"><span data-stu-id="63b5c-133">Product</span></span><br/>                  | <span data-ttu-id="63b5c-134">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="63b5c-134">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="63b5c-135">parâmetro</span><span class="sxs-lookup"><span data-stu-id="63b5c-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="63b5c-136"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="63b5c-136"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="63b5c-137">IID</span><span class="sxs-lookup"><span data-stu-id="63b5c-137">IID</span></span><br/>                      | <span data-ttu-id="63b5c-138">IID \_ IVMHostInfo é definido como 5b5cf343-05ad-453b-be99-adf4e27b2ebc</span><span class="sxs-lookup"><span data-stu-id="63b5c-138">IID\_IVMHostInfo is defined as 5b5cf343-05ad-453b-be99-adf4e27b2ebc</span></span><br/>                |



## <a name="see-also"></a><span data-ttu-id="63b5c-139">Confira também</span><span class="sxs-lookup"><span data-stu-id="63b5c-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="63b5c-140">**IVMHostInfo**</span><span class="sxs-lookup"><span data-stu-id="63b5c-140">**IVMHostInfo**</span></span>](ivmhostinfo.md)
</dt> </dl>

 

