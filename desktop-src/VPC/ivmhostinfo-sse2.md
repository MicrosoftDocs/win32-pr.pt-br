---
title: Propriedade SSE2 IVMHostInfo (VPCCOMInterfaces. h)
description: Determina se o processador dá suporte ao conjunto de instruções SSE2. | Propriedade SSE2 IVMHostInfo (VPCCOMInterfaces. h)
ms.assetid: 1db5583c-fb8e-400e-87d3-3c4309696307
keywords:
- Propriedade SSE2 do Virtual PC
- Propriedade SSE2 Virtual PC, interface IVMHostInfo
- Virtual PC interface IVMHostInfo, Propriedade SSE2
topic_type:
- apiref
api_name:
- IVMHostInfo.SSE2
- IVMHostInfo.get_SSE2
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 28286262d02512f58df8c3a00e4ba07a67c2916f
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "103837855"
---
# <a name="ivmhostinfosse2-property"></a><span data-ttu-id="103f6-107">Propriedade IVMHostInfo:: SSE2</span><span class="sxs-lookup"><span data-stu-id="103f6-107">IVMHostInfo::SSE2 property</span></span>

<span data-ttu-id="103f6-108">\[O Windows Virtual PC não está mais disponível para uso a partir do Windows 8.</span><span class="sxs-lookup"><span data-stu-id="103f6-108">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="103f6-109">Em vez disso, use o [provedor WMI do Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="103f6-109">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="103f6-110">Determina se o processador dá suporte ao conjunto de instruções SSE2.</span><span class="sxs-lookup"><span data-stu-id="103f6-110">Determines whether the processor supports the SSE2 instruction set.</span></span>

<span data-ttu-id="103f6-111">Esta propriedade é somente para leitura.</span><span class="sxs-lookup"><span data-stu-id="103f6-111">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="103f6-112">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="103f6-112">Syntax</span></span>


```C++
HRESULT get_SSE2(
  [out, retval] VARIANT_BOOL *sse2Enabled
);
```



## <a name="property-value"></a><span data-ttu-id="103f6-113">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="103f6-113">Property value</span></span>

<span data-ttu-id="103f6-114">**True** se as instruções SSE2 forem suportadas pelo processador do host; caso contrário, **false** .</span><span class="sxs-lookup"><span data-stu-id="103f6-114">**TRUE** if SSE2 instructions are supported by the host processor, **FALSE** otherwise.</span></span>

## <a name="error-codes"></a><span data-ttu-id="103f6-115">Códigos do Erro</span><span class="sxs-lookup"><span data-stu-id="103f6-115">Error codes</span></span>



| <span data-ttu-id="103f6-116">Nome/valor</span><span class="sxs-lookup"><span data-stu-id="103f6-116">Name/value</span></span>                                                                                                                                                    | <span data-ttu-id="103f6-117">Significado</span><span class="sxs-lookup"><span data-stu-id="103f6-117">Meaning</span></span>                                      |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="103f6-118"><dt>S \_ OK</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="103f6-118"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                       | <span data-ttu-id="103f6-119">A operação foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="103f6-119">The operation was successful.</span></span><br/>     |
| <dl> <span data-ttu-id="103f6-120"><dt>E \_ </dt> <dt>0X80004003</dt> de ponteiro</span><span class="sxs-lookup"><span data-stu-id="103f6-120"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>         | <span data-ttu-id="103f6-121">O parâmetro é **NULL**.</span><span class="sxs-lookup"><span data-stu-id="103f6-121">The parameter is **NULL**.</span></span><br/>        |
| <dl> <span data-ttu-id="103f6-122"><dt>DISP \_ E \_ </dt> <dt>0x80020009</dt> de exceção</span><span class="sxs-lookup"><span data-stu-id="103f6-122"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl> | <span data-ttu-id="103f6-123">Ocorreu um erro inesperado.</span><span class="sxs-lookup"><span data-stu-id="103f6-123">An unexpected error has occurred.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="103f6-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="103f6-124">Requirements</span></span>



| <span data-ttu-id="103f6-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="103f6-125">Requirement</span></span> | <span data-ttu-id="103f6-126">Valor</span><span class="sxs-lookup"><span data-stu-id="103f6-126">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="103f6-127">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="103f6-127">Minimum supported client</span></span><br/> | <span data-ttu-id="103f6-128">\[Somente aplicativos de área de trabalho do Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="103f6-128">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="103f6-129">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="103f6-129">Minimum supported server</span></span><br/> | <span data-ttu-id="103f6-130">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="103f6-130">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="103f6-131">Fim do suporte do cliente</span><span class="sxs-lookup"><span data-stu-id="103f6-131">End of client support</span></span><br/>    | <span data-ttu-id="103f6-132">Windows 7</span><span class="sxs-lookup"><span data-stu-id="103f6-132">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="103f6-133">Produto</span><span class="sxs-lookup"><span data-stu-id="103f6-133">Product</span></span><br/>                  | <span data-ttu-id="103f6-134">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="103f6-134">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="103f6-135">parâmetro</span><span class="sxs-lookup"><span data-stu-id="103f6-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="103f6-136"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="103f6-136"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="103f6-137">IID</span><span class="sxs-lookup"><span data-stu-id="103f6-137">IID</span></span><br/>                      | <span data-ttu-id="103f6-138">IID \_ IVMHostInfo é definido como 5b5cf343-05ad-453b-be99-adf4e27b2ebc</span><span class="sxs-lookup"><span data-stu-id="103f6-138">IID\_IVMHostInfo is defined as 5b5cf343-05ad-453b-be99-adf4e27b2ebc</span></span><br/>                |



## <a name="see-also"></a><span data-ttu-id="103f6-139">Confira também</span><span class="sxs-lookup"><span data-stu-id="103f6-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="103f6-140">**IVMHostInfo**</span><span class="sxs-lookup"><span data-stu-id="103f6-140">**IVMHostInfo**</span></span>](ivmhostinfo.md)
</dt> </dl>

 

