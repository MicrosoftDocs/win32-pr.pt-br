---
title: Propriedade IVMHostInfo LogicalProcessorCount (VPCCOMInterfaces. h)
description: Recupera o número de processadores lógicos no computador host.
ms.assetid: bf978a80-9a21-426a-ac18-109f20d38cbb
keywords:
- Propriedade LogicalProcessorCount Virtual PC
- Propriedade LogicalProcessorCount Virtual PC, interface IVMHostInfo
- IVMHostInfo interface virtual PC, Propriedade LogicalProcessorCount
topic_type:
- apiref
api_name:
- IVMHostInfo.LogicalProcessorCount
- IVMHostInfo.get_LogicalProcessorCount
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e7668bb4332a41b1cae809c6c2f29a8eac99bade
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105763183"
---
# <a name="ivmhostinfologicalprocessorcount-property"></a><span data-ttu-id="4ab55-106">Propriedade IVMHostInfo:: LogicalProcessorCount</span><span class="sxs-lookup"><span data-stu-id="4ab55-106">IVMHostInfo::LogicalProcessorCount property</span></span>

<span data-ttu-id="4ab55-107">\[O Windows Virtual PC não está mais disponível para uso a partir do Windows 8.</span><span class="sxs-lookup"><span data-stu-id="4ab55-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="4ab55-108">Em vez disso, use o [provedor WMI do Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="4ab55-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="4ab55-109">Recupera o número de processadores lógicos no computador host.</span><span class="sxs-lookup"><span data-stu-id="4ab55-109">Retrieves the number of logical processors in the host machine.</span></span>

<span data-ttu-id="4ab55-110">Esta propriedade é somente para leitura.</span><span class="sxs-lookup"><span data-stu-id="4ab55-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="4ab55-111">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="4ab55-111">Syntax</span></span>


```C++
HRESULT get_LogicalProcessorCount(
  [out, retval] long *processorCount
);
```



## <a name="property-value"></a><span data-ttu-id="4ab55-112">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="4ab55-112">Property value</span></span>

<span data-ttu-id="4ab55-113">O número de processadores lógicos.</span><span class="sxs-lookup"><span data-stu-id="4ab55-113">The number of logical processors.</span></span>

## <a name="error-codes"></a><span data-ttu-id="4ab55-114">Códigos do Erro</span><span class="sxs-lookup"><span data-stu-id="4ab55-114">Error codes</span></span>



| <span data-ttu-id="4ab55-115">Nome/valor</span><span class="sxs-lookup"><span data-stu-id="4ab55-115">Name/value</span></span>                                                                                                                                                    | <span data-ttu-id="4ab55-116">Significado</span><span class="sxs-lookup"><span data-stu-id="4ab55-116">Meaning</span></span>                                      |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="4ab55-117"><dt>S \_ OK</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="4ab55-117"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                       | <span data-ttu-id="4ab55-118">A operação foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="4ab55-118">The operation was successful.</span></span><br/>     |
| <dl> <span data-ttu-id="4ab55-119"><dt>E \_ </dt> <dt>0X80004003</dt> de ponteiro</span><span class="sxs-lookup"><span data-stu-id="4ab55-119"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>         | <span data-ttu-id="4ab55-120">O parâmetro é **NULL**.</span><span class="sxs-lookup"><span data-stu-id="4ab55-120">The parameter is **NULL**.</span></span><br/>        |
| <dl> <span data-ttu-id="4ab55-121"><dt>DISP \_ E \_ </dt> <dt>0x80020009</dt> de exceção</span><span class="sxs-lookup"><span data-stu-id="4ab55-121"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl> | <span data-ttu-id="4ab55-122">Ocorreu um erro inesperado.</span><span class="sxs-lookup"><span data-stu-id="4ab55-122">An unexpected error has occurred.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="4ab55-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4ab55-123">Requirements</span></span>



| <span data-ttu-id="4ab55-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="4ab55-124">Requirement</span></span> | <span data-ttu-id="4ab55-125">Valor</span><span class="sxs-lookup"><span data-stu-id="4ab55-125">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="4ab55-126">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="4ab55-126">Minimum supported client</span></span><br/> | <span data-ttu-id="4ab55-127">\[Somente aplicativos de área de trabalho do Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="4ab55-127">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="4ab55-128">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="4ab55-128">Minimum supported server</span></span><br/> | <span data-ttu-id="4ab55-129">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="4ab55-129">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="4ab55-130">Fim do suporte do cliente</span><span class="sxs-lookup"><span data-stu-id="4ab55-130">End of client support</span></span><br/>    | <span data-ttu-id="4ab55-131">Windows 7</span><span class="sxs-lookup"><span data-stu-id="4ab55-131">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="4ab55-132">Produto</span><span class="sxs-lookup"><span data-stu-id="4ab55-132">Product</span></span><br/>                  | <span data-ttu-id="4ab55-133">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="4ab55-133">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="4ab55-134">parâmetro</span><span class="sxs-lookup"><span data-stu-id="4ab55-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="4ab55-135"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="4ab55-135"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="4ab55-136">IID</span><span class="sxs-lookup"><span data-stu-id="4ab55-136">IID</span></span><br/>                      | <span data-ttu-id="4ab55-137">IID \_ IVMHostInfo é definido como 5b5cf343-05ad-453b-be99-adf4e27b2ebc</span><span class="sxs-lookup"><span data-stu-id="4ab55-137">IID\_IVMHostInfo is defined as 5b5cf343-05ad-453b-be99-adf4e27b2ebc</span></span><br/>                |



## <a name="see-also"></a><span data-ttu-id="4ab55-138">Confira também</span><span class="sxs-lookup"><span data-stu-id="4ab55-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4ab55-139">**IVMHostInfo**</span><span class="sxs-lookup"><span data-stu-id="4ab55-139">**IVMHostInfo**</span></span>](ivmhostinfo.md)
</dt> </dl>

 

