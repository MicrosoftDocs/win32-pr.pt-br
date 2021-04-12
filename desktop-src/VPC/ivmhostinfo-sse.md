---
title: Propriedade SSE IVMHostInfo (VPCCOMInterfaces. h)
description: Determina se o processador dá suporte ao conjunto de instruções SSE. | Propriedade SSE IVMHostInfo (VPCCOMInterfaces. h)
ms.assetid: 135704db-757a-45b1-884a-5e26ef7d65c7
keywords:
- PC virtual de propriedade SSE
- Propriedade SSE Virtual PC, interface IVMHostInfo
- Virtual PC interface IVMHostInfo, Propriedade SSE
topic_type:
- apiref
api_name:
- IVMHostInfo.SSE
- IVMHostInfo.get_SSE
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 02bef292e7dbcae48b9e2a6a94e7f879212a0dfc
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104298345"
---
# <a name="ivmhostinfosse-property"></a><span data-ttu-id="cb5b3-107">Propriedade IVMHostInfo:: SSE</span><span class="sxs-lookup"><span data-stu-id="cb5b3-107">IVMHostInfo::SSE property</span></span>

<span data-ttu-id="cb5b3-108">\[O Windows Virtual PC não está mais disponível para uso a partir do Windows 8.</span><span class="sxs-lookup"><span data-stu-id="cb5b3-108">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="cb5b3-109">Em vez disso, use o [provedor WMI do Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="cb5b3-109">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="cb5b3-110">Determina se o processador dá suporte ao conjunto de instruções SSE.</span><span class="sxs-lookup"><span data-stu-id="cb5b3-110">Determines whether the processor supports the SSE instruction set.</span></span>

<span data-ttu-id="cb5b3-111">Esta propriedade é somente para leitura.</span><span class="sxs-lookup"><span data-stu-id="cb5b3-111">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="cb5b3-112">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="cb5b3-112">Syntax</span></span>


```C++
HRESULT get_SSE(
  [out, retval] VARIANT_BOOL *sseEnabled
);
```



## <a name="property-value"></a><span data-ttu-id="cb5b3-113">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="cb5b3-113">Property value</span></span>

<span data-ttu-id="cb5b3-114">**True** se as instruções SSE forem suportadas pelo processador do host; caso contrário, **false** .</span><span class="sxs-lookup"><span data-stu-id="cb5b3-114">**TRUE** if SSE instructions are supported by the host processor, **FALSE** otherwise.</span></span>

## <a name="error-codes"></a><span data-ttu-id="cb5b3-115">Códigos do Erro</span><span class="sxs-lookup"><span data-stu-id="cb5b3-115">Error codes</span></span>



| <span data-ttu-id="cb5b3-116">Nome/valor</span><span class="sxs-lookup"><span data-stu-id="cb5b3-116">Name/value</span></span>                                                                                                                                                    | <span data-ttu-id="cb5b3-117">Significado</span><span class="sxs-lookup"><span data-stu-id="cb5b3-117">Meaning</span></span>                                      |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="cb5b3-118"><dt>S \_ OK</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="cb5b3-118"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                       | <span data-ttu-id="cb5b3-119">A operação foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="cb5b3-119">The operation was successful.</span></span><br/>     |
| <dl> <span data-ttu-id="cb5b3-120"><dt>E \_ </dt> <dt>0X80004003</dt> de ponteiro</span><span class="sxs-lookup"><span data-stu-id="cb5b3-120"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>         | <span data-ttu-id="cb5b3-121">O parâmetro é **NULL**.</span><span class="sxs-lookup"><span data-stu-id="cb5b3-121">The parameter is **NULL**.</span></span><br/>        |
| <dl> <span data-ttu-id="cb5b3-122"><dt>DISP \_ E \_ </dt> <dt>0x80020009</dt> de exceção</span><span class="sxs-lookup"><span data-stu-id="cb5b3-122"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl> | <span data-ttu-id="cb5b3-123">Ocorreu um erro inesperado.</span><span class="sxs-lookup"><span data-stu-id="cb5b3-123">An unexpected error has occurred.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="cb5b3-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="cb5b3-124">Requirements</span></span>



| <span data-ttu-id="cb5b3-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="cb5b3-125">Requirement</span></span> | <span data-ttu-id="cb5b3-126">Valor</span><span class="sxs-lookup"><span data-stu-id="cb5b3-126">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="cb5b3-127">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="cb5b3-127">Minimum supported client</span></span><br/> | <span data-ttu-id="cb5b3-128">\[Somente aplicativos de área de trabalho do Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="cb5b3-128">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="cb5b3-129">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="cb5b3-129">Minimum supported server</span></span><br/> | <span data-ttu-id="cb5b3-130">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="cb5b3-130">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="cb5b3-131">Fim do suporte do cliente</span><span class="sxs-lookup"><span data-stu-id="cb5b3-131">End of client support</span></span><br/>    | <span data-ttu-id="cb5b3-132">Windows 7</span><span class="sxs-lookup"><span data-stu-id="cb5b3-132">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="cb5b3-133">Produto</span><span class="sxs-lookup"><span data-stu-id="cb5b3-133">Product</span></span><br/>                  | <span data-ttu-id="cb5b3-134">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="cb5b3-134">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="cb5b3-135">parâmetro</span><span class="sxs-lookup"><span data-stu-id="cb5b3-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="cb5b3-136"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="cb5b3-136"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="cb5b3-137">IID</span><span class="sxs-lookup"><span data-stu-id="cb5b3-137">IID</span></span><br/>                      | <span data-ttu-id="cb5b3-138">IID \_ IVMHostInfo é definido como 5b5cf343-05ad-453b-be99-adf4e27b2ebc</span><span class="sxs-lookup"><span data-stu-id="cb5b3-138">IID\_IVMHostInfo is defined as 5b5cf343-05ad-453b-be99-adf4e27b2ebc</span></span><br/>                |



## <a name="see-also"></a><span data-ttu-id="cb5b3-139">Confira também</span><span class="sxs-lookup"><span data-stu-id="cb5b3-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cb5b3-140">**IVMHostInfo**</span><span class="sxs-lookup"><span data-stu-id="cb5b3-140">**IVMHostInfo**</span></span>](ivmhostinfo.md)
</dt> </dl>

 

