---
title: Propriedade IVMHostInfo MemoryAvailString (VPCCOMInterfaces. h)
description: Recupera a quantidade de memória física disponível no computador host, em megabytes, como uma cadeia de caracteres.
ms.assetid: a0f17dda-2042-4aec-9968-6662d32684cf
keywords:
- Propriedade MemoryAvailString Virtual PC
- Propriedade MemoryAvailString Virtual PC, interface IVMHostInfo
- IVMHostInfo interface virtual PC, Propriedade MemoryAvailString
topic_type:
- apiref
api_name:
- IVMHostInfo.MemoryAvailString
- IVMHostInfo.get_MemoryAvailString
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ea003b94d0d4604dfba3daf545a51b9d69b6708c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455379"
---
# <a name="ivmhostinfomemoryavailstring-property"></a><span data-ttu-id="03a0b-106">Propriedade IVMHostInfo:: MemoryAvailString</span><span class="sxs-lookup"><span data-stu-id="03a0b-106">IVMHostInfo::MemoryAvailString property</span></span>

<span data-ttu-id="03a0b-107">\[O Windows Virtual PC não está mais disponível para uso a partir do Windows 8.</span><span class="sxs-lookup"><span data-stu-id="03a0b-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="03a0b-108">Em vez disso, use o [provedor WMI do Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="03a0b-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="03a0b-109">Recupera a quantidade de memória física disponível no computador host, em megabytes, como uma cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="03a0b-109">Retrieves the amount of available physical memory in the host machine, in megabytes, as a string.</span></span>

<span data-ttu-id="03a0b-110">Esta propriedade é somente para leitura.</span><span class="sxs-lookup"><span data-stu-id="03a0b-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="03a0b-111">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="03a0b-111">Syntax</span></span>


```C++
HRESULT get_MemoryAvailString(
  [out, retval] BSTR *megabytesOfMemory
);
```



## <a name="property-value"></a><span data-ttu-id="03a0b-112">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="03a0b-112">Property value</span></span>

<span data-ttu-id="03a0b-113">A memória física disponível, em megabytes.</span><span class="sxs-lookup"><span data-stu-id="03a0b-113">The available physical memory, in megabytes.</span></span>

## <a name="error-codes"></a><span data-ttu-id="03a0b-114">Códigos do Erro</span><span class="sxs-lookup"><span data-stu-id="03a0b-114">Error codes</span></span>



| <span data-ttu-id="03a0b-115">Nome/valor</span><span class="sxs-lookup"><span data-stu-id="03a0b-115">Name/value</span></span>                                                                                                                                                    | <span data-ttu-id="03a0b-116">Significado</span><span class="sxs-lookup"><span data-stu-id="03a0b-116">Meaning</span></span>                                      |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="03a0b-117"><dt>S \_ OK</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="03a0b-117"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                       | <span data-ttu-id="03a0b-118">A operação foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="03a0b-118">The operation was successful.</span></span><br/>     |
| <dl> <span data-ttu-id="03a0b-119"><dt>E \_ </dt> <dt>0X80004003</dt> de ponteiro</span><span class="sxs-lookup"><span data-stu-id="03a0b-119"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>         | <span data-ttu-id="03a0b-120">O parâmetro é **NULL**.</span><span class="sxs-lookup"><span data-stu-id="03a0b-120">The parameter is **NULL**.</span></span><br/>        |
| <dl> <span data-ttu-id="03a0b-121"><dt>DISP \_ E \_ </dt> <dt>0x80020009</dt> de exceção</span><span class="sxs-lookup"><span data-stu-id="03a0b-121"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl> | <span data-ttu-id="03a0b-122">Ocorreu um erro inesperado.</span><span class="sxs-lookup"><span data-stu-id="03a0b-122">An unexpected error has occurred.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="03a0b-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="03a0b-123">Requirements</span></span>



| <span data-ttu-id="03a0b-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="03a0b-124">Requirement</span></span> | <span data-ttu-id="03a0b-125">Valor</span><span class="sxs-lookup"><span data-stu-id="03a0b-125">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="03a0b-126">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="03a0b-126">Minimum supported client</span></span><br/> | <span data-ttu-id="03a0b-127">\[Somente aplicativos de área de trabalho do Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="03a0b-127">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="03a0b-128">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="03a0b-128">Minimum supported server</span></span><br/> | <span data-ttu-id="03a0b-129">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="03a0b-129">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="03a0b-130">Fim do suporte do cliente</span><span class="sxs-lookup"><span data-stu-id="03a0b-130">End of client support</span></span><br/>    | <span data-ttu-id="03a0b-131">Windows 7</span><span class="sxs-lookup"><span data-stu-id="03a0b-131">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="03a0b-132">Produto</span><span class="sxs-lookup"><span data-stu-id="03a0b-132">Product</span></span><br/>                  | <span data-ttu-id="03a0b-133">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="03a0b-133">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="03a0b-134">parâmetro</span><span class="sxs-lookup"><span data-stu-id="03a0b-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="03a0b-135"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="03a0b-135"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="03a0b-136">IID</span><span class="sxs-lookup"><span data-stu-id="03a0b-136">IID</span></span><br/>                      | <span data-ttu-id="03a0b-137">IID \_ IVMHostInfo é definido como 5b5cf343-05ad-453b-be99-adf4e27b2ebc</span><span class="sxs-lookup"><span data-stu-id="03a0b-137">IID\_IVMHostInfo is defined as 5b5cf343-05ad-453b-be99-adf4e27b2ebc</span></span><br/>                |



## <a name="see-also"></a><span data-ttu-id="03a0b-138">Confira também</span><span class="sxs-lookup"><span data-stu-id="03a0b-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="03a0b-139">**IVMHostInfo**</span><span class="sxs-lookup"><span data-stu-id="03a0b-139">**IVMHostInfo**</span></span>](ivmhostinfo.md)
</dt> </dl>

 

