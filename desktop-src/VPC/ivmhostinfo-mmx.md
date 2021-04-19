---
title: Propriedade MMX IVMHostInfo (VPCCOMInterfaces. h)
description: Determina se o processador dá suporte ao conjunto de instruções MMX. | Propriedade MMX IVMHostInfo (VPCCOMInterfaces. h)
ms.assetid: 2f556289-c752-4af2-a6d0-abb6e717e609
keywords:
- PC virtual da propriedade MMX
- Propriedade MMX Virtual PC, interface IVMHostInfo
- Virtual PC de interface IVMHostInfo, Propriedade MMX
topic_type:
- apiref
api_name:
- IVMHostInfo.MMX
- IVMHostInfo.get_MMX
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e224ed6a0f15da9143a884dd1c1dfacc1634fce7
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "105784985"
---
# <a name="ivmhostinfommx-property"></a><span data-ttu-id="52842-107">Propriedade IVMHostInfo:: MMX</span><span class="sxs-lookup"><span data-stu-id="52842-107">IVMHostInfo::MMX property</span></span>

<span data-ttu-id="52842-108">\[O Windows Virtual PC não está mais disponível para uso a partir do Windows 8.</span><span class="sxs-lookup"><span data-stu-id="52842-108">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="52842-109">Em vez disso, use o [provedor WMI do Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="52842-109">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="52842-110">Determina se o processador dá suporte ao conjunto de instruções MMX.</span><span class="sxs-lookup"><span data-stu-id="52842-110">Determines whether the processor supports the MMX instruction set.</span></span>

<span data-ttu-id="52842-111">Esta propriedade é somente para leitura.</span><span class="sxs-lookup"><span data-stu-id="52842-111">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="52842-112">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="52842-112">Syntax</span></span>


```C++
HRESULT get_MMX(
  [out, retval] VARIANT_BOOL *mmxEnabled
);
```



## <a name="property-value"></a><span data-ttu-id="52842-113">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="52842-113">Property value</span></span>

<span data-ttu-id="52842-114">**True** se houver suporte para instruções MMX; caso contrário, **false** .</span><span class="sxs-lookup"><span data-stu-id="52842-114">**TRUE** if MMX instructions are supported, **FALSE** otherwise.</span></span>

## <a name="error-codes"></a><span data-ttu-id="52842-115">Códigos do Erro</span><span class="sxs-lookup"><span data-stu-id="52842-115">Error codes</span></span>



| <span data-ttu-id="52842-116">Nome/valor</span><span class="sxs-lookup"><span data-stu-id="52842-116">Name/value</span></span>                                                                                                                                                    | <span data-ttu-id="52842-117">Significado</span><span class="sxs-lookup"><span data-stu-id="52842-117">Meaning</span></span>                                      |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="52842-118"><dt>S \_ OK</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="52842-118"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                       | <span data-ttu-id="52842-119">A operação foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="52842-119">The operation was successful.</span></span><br/>     |
| <dl> <span data-ttu-id="52842-120"><dt>E \_ </dt> <dt>0X80004003</dt> de ponteiro</span><span class="sxs-lookup"><span data-stu-id="52842-120"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>         | <span data-ttu-id="52842-121">O parâmetro é **NULL**.</span><span class="sxs-lookup"><span data-stu-id="52842-121">The parameter is **NULL**.</span></span><br/>        |
| <dl> <span data-ttu-id="52842-122"><dt>DISP \_ E \_ </dt> <dt>0x80020009</dt> de exceção</span><span class="sxs-lookup"><span data-stu-id="52842-122"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl> | <span data-ttu-id="52842-123">Ocorreu um erro inesperado.</span><span class="sxs-lookup"><span data-stu-id="52842-123">An unexpected error has occurred.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="52842-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="52842-124">Requirements</span></span>



| <span data-ttu-id="52842-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="52842-125">Requirement</span></span> | <span data-ttu-id="52842-126">Valor</span><span class="sxs-lookup"><span data-stu-id="52842-126">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="52842-127">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="52842-127">Minimum supported client</span></span><br/> | <span data-ttu-id="52842-128">\[Somente aplicativos de área de trabalho do Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="52842-128">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="52842-129">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="52842-129">Minimum supported server</span></span><br/> | <span data-ttu-id="52842-130">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="52842-130">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="52842-131">Fim do suporte do cliente</span><span class="sxs-lookup"><span data-stu-id="52842-131">End of client support</span></span><br/>    | <span data-ttu-id="52842-132">Windows 7</span><span class="sxs-lookup"><span data-stu-id="52842-132">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="52842-133">Produto</span><span class="sxs-lookup"><span data-stu-id="52842-133">Product</span></span><br/>                  | <span data-ttu-id="52842-134">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="52842-134">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="52842-135">parâmetro</span><span class="sxs-lookup"><span data-stu-id="52842-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="52842-136"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="52842-136"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="52842-137">IID</span><span class="sxs-lookup"><span data-stu-id="52842-137">IID</span></span><br/>                      | <span data-ttu-id="52842-138">IID \_ IVMHostInfo é definido como 5b5cf343-05ad-453b-be99-adf4e27b2ebc</span><span class="sxs-lookup"><span data-stu-id="52842-138">IID\_IVMHostInfo is defined as 5b5cf343-05ad-453b-be99-adf4e27b2ebc</span></span><br/>                |



## <a name="see-also"></a><span data-ttu-id="52842-139">Confira também</span><span class="sxs-lookup"><span data-stu-id="52842-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="52842-140">**IVMHostInfo**</span><span class="sxs-lookup"><span data-stu-id="52842-140">**IVMHostInfo**</span></span>](ivmhostinfo.md)
</dt> </dl>

 

