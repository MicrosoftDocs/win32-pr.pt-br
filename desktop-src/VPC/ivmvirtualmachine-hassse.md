---
title: Propriedade IVMVirtualMachine HasSSE (VPCCOMInterfaces. h)
description: Determina se o processador dá suporte ao conjunto de instruções SSE. | Propriedade IVMVirtualMachine HasSSE (VPCCOMInterfaces. h)
ms.assetid: 949dd93b-aa4e-4506-91ed-ed625a535d5f
keywords:
- Propriedade HasSSE Virtual PC
- Propriedade HasSSE Virtual PC, interface IVMVirtualMachine
- IVMVirtualMachine interface virtual PC, Propriedade HasSSE
topic_type:
- apiref
api_name:
- IVMVirtualMachine.HasSSE
- IVMVirtualMachine.get_HasSSE
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a367ddc7b32ff4627976d2c5b63ec3565dbace53
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "103837891"
---
# <a name="ivmvirtualmachinehassse-property"></a><span data-ttu-id="453b5-107">Propriedade IVMVirtualMachine:: HasSSE</span><span class="sxs-lookup"><span data-stu-id="453b5-107">IVMVirtualMachine::HasSSE property</span></span>

<span data-ttu-id="453b5-108">\[O Windows Virtual PC não está mais disponível para uso a partir do Windows 8.</span><span class="sxs-lookup"><span data-stu-id="453b5-108">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="453b5-109">Em vez disso, use o [provedor WMI do Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="453b5-109">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="453b5-110">Determina se o processador dá suporte ao conjunto de instruções SSE.</span><span class="sxs-lookup"><span data-stu-id="453b5-110">Determines whether the processor supports the SSE instruction set.</span></span>

<span data-ttu-id="453b5-111">Esta propriedade é somente para leitura.</span><span class="sxs-lookup"><span data-stu-id="453b5-111">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="453b5-112">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="453b5-112">Syntax</span></span>


```C++
HRESULT get_HasSSE(
  [out, retval] VARIANT_BOOL *sseEnabled
);
```



## <a name="property-value"></a><span data-ttu-id="453b5-113">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="453b5-113">Property value</span></span>

<span data-ttu-id="453b5-114">**True** se o processador tiver suporte para o conjunto de instruções SSE; caso contrário, **false** .</span><span class="sxs-lookup"><span data-stu-id="453b5-114">**TRUE** if the processor supported the SSE instruction set, **FALSE** otherwise.</span></span>

## <a name="error-codes"></a><span data-ttu-id="453b5-115">Códigos do Erro</span><span class="sxs-lookup"><span data-stu-id="453b5-115">Error codes</span></span>



| <span data-ttu-id="453b5-116">Nome/valor</span><span class="sxs-lookup"><span data-stu-id="453b5-116">Name/value</span></span>                                                                                                                                                    | <span data-ttu-id="453b5-117">Significado</span><span class="sxs-lookup"><span data-stu-id="453b5-117">Meaning</span></span>                                      |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="453b5-118"><dt>S \_ OK</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="453b5-118"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                       | <span data-ttu-id="453b5-119">A operação foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="453b5-119">The operation was successful.</span></span><br/>     |
| <dl> <span data-ttu-id="453b5-120"><dt>E \_ </dt> <dt>0X80004003</dt> de ponteiro</span><span class="sxs-lookup"><span data-stu-id="453b5-120"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>         | <span data-ttu-id="453b5-121">O parâmetro é **NULL**.</span><span class="sxs-lookup"><span data-stu-id="453b5-121">The parameter is **NULL**.</span></span><br/>        |
| <dl> <span data-ttu-id="453b5-122"><dt>VM \_ E 0xA0040207 de \_ VM \_ desconhecido</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="453b5-122"><dt>VM\_E\_VM\_UNKNOWN</dt> <dt>0xA0040207</dt></span></span> </dl> | <span data-ttu-id="453b5-123">A configuração é desconhecida.</span><span class="sxs-lookup"><span data-stu-id="453b5-123">The configuration is unknown.</span></span><br/>     |
| <dl> <span data-ttu-id="453b5-124"><dt>DISP \_ E \_ </dt> <dt>0x80020009</dt> de exceção</span><span class="sxs-lookup"><span data-stu-id="453b5-124"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl> | <span data-ttu-id="453b5-125">Ocorreu um erro inesperado.</span><span class="sxs-lookup"><span data-stu-id="453b5-125">An unexpected error has occurred.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="453b5-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="453b5-126">Requirements</span></span>



| <span data-ttu-id="453b5-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="453b5-127">Requirement</span></span> | <span data-ttu-id="453b5-128">Valor</span><span class="sxs-lookup"><span data-stu-id="453b5-128">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="453b5-129">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="453b5-129">Minimum supported client</span></span><br/> | <span data-ttu-id="453b5-130">\[Somente aplicativos de área de trabalho do Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="453b5-130">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="453b5-131">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="453b5-131">Minimum supported server</span></span><br/> | <span data-ttu-id="453b5-132">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="453b5-132">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="453b5-133">Fim do suporte do cliente</span><span class="sxs-lookup"><span data-stu-id="453b5-133">End of client support</span></span><br/>    | <span data-ttu-id="453b5-134">Windows 7</span><span class="sxs-lookup"><span data-stu-id="453b5-134">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="453b5-135">Produto</span><span class="sxs-lookup"><span data-stu-id="453b5-135">Product</span></span><br/>                  | <span data-ttu-id="453b5-136">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="453b5-136">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="453b5-137">parâmetro</span><span class="sxs-lookup"><span data-stu-id="453b5-137">Header</span></span><br/>                   | <dl> <span data-ttu-id="453b5-138"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="453b5-138"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="453b5-139">IID</span><span class="sxs-lookup"><span data-stu-id="453b5-139">IID</span></span><br/>                      | <span data-ttu-id="453b5-140">IID \_ IVMVirtualMachine é definido como f7092aa1-33ed-4f78-a59f-c00adfc2edd7</span><span class="sxs-lookup"><span data-stu-id="453b5-140">IID\_IVMVirtualMachine is defined as f7092aa1-33ed-4f78-a59f-c00adfc2edd7</span></span><br/>          |



## <a name="see-also"></a><span data-ttu-id="453b5-141">Confira também</span><span class="sxs-lookup"><span data-stu-id="453b5-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="453b5-142">**IVMVirtualMachine**</span><span class="sxs-lookup"><span data-stu-id="453b5-142">**IVMVirtualMachine**</span></span>](ivmvirtualmachine.md)
</dt> </dl>

 

