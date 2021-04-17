---
title: Propriedade de memória IVMHostInfo (VPCCOMInterfaces. h)
description: Recupera a quantidade total de memória física no computador host, em megabytes.
ms.assetid: 178013c0-cf29-4f1e-9a9d-d6a5dbd4fe2d
keywords:
- Propriedade de memória virtual PC
- Propriedade de memória virtual PC, interface IVMHostInfo
- Virtual PC interface IVMHostInfo, Propriedade Memory
topic_type:
- apiref
api_name:
- IVMHostInfo.Memory
- IVMHostInfo.get_Memory
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 39f634bfe3bf81dcb13c9f09d8f19a5a82aa6902
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105764012"
---
# <a name="ivmhostinfomemory-property"></a><span data-ttu-id="2b7cb-106">Propriedade IVMHostInfo:: Memory</span><span class="sxs-lookup"><span data-stu-id="2b7cb-106">IVMHostInfo::Memory property</span></span>

<span data-ttu-id="2b7cb-107">\[O Windows Virtual PC não está mais disponível para uso a partir do Windows 8.</span><span class="sxs-lookup"><span data-stu-id="2b7cb-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="2b7cb-108">Em vez disso, use o [provedor WMI do Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="2b7cb-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="2b7cb-109">Recupera a quantidade total de memória física no computador host, em megabytes.</span><span class="sxs-lookup"><span data-stu-id="2b7cb-109">Retrieves the total amount of physical memory in the host machine, in megabytes.</span></span>

<span data-ttu-id="2b7cb-110">Esta propriedade é somente para leitura.</span><span class="sxs-lookup"><span data-stu-id="2b7cb-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="2b7cb-111">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="2b7cb-111">Syntax</span></span>


```C++
HRESULT get_Memory(
  [out, retval] VARIANT *megabytesOfMemory
);
```



## <a name="property-value"></a><span data-ttu-id="2b7cb-112">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="2b7cb-112">Property value</span></span>

<span data-ttu-id="2b7cb-113">A quantidade total de memória física, em megabytes.</span><span class="sxs-lookup"><span data-stu-id="2b7cb-113">The total amount of physical memory, in megabytes.</span></span> <span data-ttu-id="2b7cb-114">Esse valor é uma **variante** do tipo VT \_ decimal.</span><span class="sxs-lookup"><span data-stu-id="2b7cb-114">This value is a **VARIANT** of type VT\_DECIMAL.</span></span>

## <a name="error-codes"></a><span data-ttu-id="2b7cb-115">Códigos do Erro</span><span class="sxs-lookup"><span data-stu-id="2b7cb-115">Error codes</span></span>



| <span data-ttu-id="2b7cb-116">Nome/valor</span><span class="sxs-lookup"><span data-stu-id="2b7cb-116">Name/value</span></span>                                                                                                                                                    | <span data-ttu-id="2b7cb-117">Significado</span><span class="sxs-lookup"><span data-stu-id="2b7cb-117">Meaning</span></span>                                      |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="2b7cb-118"><dt>S \_ OK</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="2b7cb-118"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                       | <span data-ttu-id="2b7cb-119">A operação foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="2b7cb-119">The operation was successful.</span></span><br/>     |
| <dl> <span data-ttu-id="2b7cb-120"><dt>E \_ </dt> <dt>0X80004003</dt> de ponteiro</span><span class="sxs-lookup"><span data-stu-id="2b7cb-120"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>         | <span data-ttu-id="2b7cb-121">O parâmetro é **NULL**.</span><span class="sxs-lookup"><span data-stu-id="2b7cb-121">The parameter is **NULL**.</span></span><br/>        |
| <dl> <span data-ttu-id="2b7cb-122"><dt>DISP \_ E \_ </dt> <dt>0x80020009</dt> de exceção</span><span class="sxs-lookup"><span data-stu-id="2b7cb-122"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl> | <span data-ttu-id="2b7cb-123">Ocorreu um erro inesperado.</span><span class="sxs-lookup"><span data-stu-id="2b7cb-123">An unexpected error has occurred.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="2b7cb-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2b7cb-124">Requirements</span></span>



| <span data-ttu-id="2b7cb-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="2b7cb-125">Requirement</span></span> | <span data-ttu-id="2b7cb-126">Valor</span><span class="sxs-lookup"><span data-stu-id="2b7cb-126">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="2b7cb-127">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="2b7cb-127">Minimum supported client</span></span><br/> | <span data-ttu-id="2b7cb-128">\[Somente aplicativos de área de trabalho do Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="2b7cb-128">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="2b7cb-129">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="2b7cb-129">Minimum supported server</span></span><br/> | <span data-ttu-id="2b7cb-130">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="2b7cb-130">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="2b7cb-131">Fim do suporte do cliente</span><span class="sxs-lookup"><span data-stu-id="2b7cb-131">End of client support</span></span><br/>    | <span data-ttu-id="2b7cb-132">Windows 7</span><span class="sxs-lookup"><span data-stu-id="2b7cb-132">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="2b7cb-133">Produto</span><span class="sxs-lookup"><span data-stu-id="2b7cb-133">Product</span></span><br/>                  | <span data-ttu-id="2b7cb-134">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="2b7cb-134">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="2b7cb-135">parâmetro</span><span class="sxs-lookup"><span data-stu-id="2b7cb-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="2b7cb-136"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="2b7cb-136"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="2b7cb-137">IID</span><span class="sxs-lookup"><span data-stu-id="2b7cb-137">IID</span></span><br/>                      | <span data-ttu-id="2b7cb-138">IID \_ IVMHostInfo é definido como 5b5cf343-05ad-453b-be99-adf4e27b2ebc</span><span class="sxs-lookup"><span data-stu-id="2b7cb-138">IID\_IVMHostInfo is defined as 5b5cf343-05ad-453b-be99-adf4e27b2ebc</span></span><br/>                |



## <a name="see-also"></a><span data-ttu-id="2b7cb-139">Confira também</span><span class="sxs-lookup"><span data-stu-id="2b7cb-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2b7cb-140">**IVMHostInfo**</span><span class="sxs-lookup"><span data-stu-id="2b7cb-140">**IVMHostInfo**</span></span>](ivmhostinfo.md)
</dt> </dl>

 

