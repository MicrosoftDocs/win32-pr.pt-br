---
title: Propriedade IVMVirtualMachine HasMMX (VPCCOMInterfaces. h)
description: Determina se o processador dá suporte ao conjunto de instruções MMX. | Propriedade IVMVirtualMachine HasMMX (VPCCOMInterfaces. h)
ms.assetid: 85350abe-ab44-42d2-9f3e-0fbdb64ff854
keywords:
- Propriedade HasMMX Virtual PC
- Propriedade HasMMX Virtual PC, interface IVMVirtualMachine
- IVMVirtualMachine interface virtual PC, Propriedade HasMMX
topic_type:
- apiref
api_name:
- IVMVirtualMachine.HasMMX
- IVMVirtualMachine.get_HasMMX
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 26e6b780d14749db193b2a7ce9a41083c6bf7031
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104012058"
---
# <a name="ivmvirtualmachinehasmmx-property"></a><span data-ttu-id="dfd25-107">Propriedade IVMVirtualMachine:: HasMMX</span><span class="sxs-lookup"><span data-stu-id="dfd25-107">IVMVirtualMachine::HasMMX property</span></span>

<span data-ttu-id="dfd25-108">\[O Windows Virtual PC não está mais disponível para uso a partir do Windows 8.</span><span class="sxs-lookup"><span data-stu-id="dfd25-108">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="dfd25-109">Em vez disso, use o [provedor WMI do Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="dfd25-109">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="dfd25-110">Determina se o processador dá suporte ao conjunto de instruções MMX.</span><span class="sxs-lookup"><span data-stu-id="dfd25-110">Determines whether the processor supports the MMX instruction set.</span></span>

<span data-ttu-id="dfd25-111">Esta propriedade é somente para leitura.</span><span class="sxs-lookup"><span data-stu-id="dfd25-111">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="dfd25-112">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="dfd25-112">Syntax</span></span>


```C++
HRESULT get_HasMMX(
  [out, retval] VARIANT_BOOL *mmxEnabled
);
```



## <a name="property-value"></a><span data-ttu-id="dfd25-113">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="dfd25-113">Property value</span></span>

<span data-ttu-id="dfd25-114">**True** se o processador tiver suporte para o conjunto de instruções MMX; caso contrário, **false** .</span><span class="sxs-lookup"><span data-stu-id="dfd25-114">**TRUE** if the processor supported the MMX instruction set, **FALSE** otherwise.</span></span>

## <a name="error-codes"></a><span data-ttu-id="dfd25-115">Códigos do Erro</span><span class="sxs-lookup"><span data-stu-id="dfd25-115">Error codes</span></span>



| <span data-ttu-id="dfd25-116">Nome/valor</span><span class="sxs-lookup"><span data-stu-id="dfd25-116">Name/value</span></span>                                                                                                                                                    | <span data-ttu-id="dfd25-117">Significado</span><span class="sxs-lookup"><span data-stu-id="dfd25-117">Meaning</span></span>                                      |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="dfd25-118"><dt>S \_ OK</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="dfd25-118"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                       | <span data-ttu-id="dfd25-119">A operação foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="dfd25-119">The operation was successful.</span></span><br/>     |
| <dl> <span data-ttu-id="dfd25-120"><dt>E \_ </dt> <dt>0X80004003</dt> de ponteiro</span><span class="sxs-lookup"><span data-stu-id="dfd25-120"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>         | <span data-ttu-id="dfd25-121">O parâmetro é **NULL**.</span><span class="sxs-lookup"><span data-stu-id="dfd25-121">The parameter is **NULL**.</span></span><br/>        |
| <dl> <span data-ttu-id="dfd25-122"><dt>VM \_ E 0xA0040207 de \_ VM \_ desconhecido</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="dfd25-122"><dt>VM\_E\_VM\_UNKNOWN</dt> <dt>0xA0040207</dt></span></span> </dl> | <span data-ttu-id="dfd25-123">A configuração é desconhecida.</span><span class="sxs-lookup"><span data-stu-id="dfd25-123">The configuration is unknown.</span></span><br/>     |
| <dl> <span data-ttu-id="dfd25-124"><dt>DISP \_ E \_ </dt> <dt>0x80020009</dt> de exceção</span><span class="sxs-lookup"><span data-stu-id="dfd25-124"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl> | <span data-ttu-id="dfd25-125">Ocorreu um erro inesperado.</span><span class="sxs-lookup"><span data-stu-id="dfd25-125">An unexpected error has occurred.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="dfd25-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="dfd25-126">Requirements</span></span>



| <span data-ttu-id="dfd25-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="dfd25-127">Requirement</span></span> | <span data-ttu-id="dfd25-128">Valor</span><span class="sxs-lookup"><span data-stu-id="dfd25-128">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="dfd25-129">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="dfd25-129">Minimum supported client</span></span><br/> | <span data-ttu-id="dfd25-130">\[Somente aplicativos de área de trabalho do Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="dfd25-130">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="dfd25-131">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="dfd25-131">Minimum supported server</span></span><br/> | <span data-ttu-id="dfd25-132">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="dfd25-132">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="dfd25-133">Fim do suporte do cliente</span><span class="sxs-lookup"><span data-stu-id="dfd25-133">End of client support</span></span><br/>    | <span data-ttu-id="dfd25-134">Windows 7</span><span class="sxs-lookup"><span data-stu-id="dfd25-134">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="dfd25-135">Produto</span><span class="sxs-lookup"><span data-stu-id="dfd25-135">Product</span></span><br/>                  | <span data-ttu-id="dfd25-136">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="dfd25-136">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="dfd25-137">parâmetro</span><span class="sxs-lookup"><span data-stu-id="dfd25-137">Header</span></span><br/>                   | <dl> <span data-ttu-id="dfd25-138"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="dfd25-138"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="dfd25-139">IID</span><span class="sxs-lookup"><span data-stu-id="dfd25-139">IID</span></span><br/>                      | <span data-ttu-id="dfd25-140">IID \_ IVMVirtualMachine é definido como f7092aa1-33ed-4f78-a59f-c00adfc2edd7</span><span class="sxs-lookup"><span data-stu-id="dfd25-140">IID\_IVMVirtualMachine is defined as f7092aa1-33ed-4f78-a59f-c00adfc2edd7</span></span><br/>          |



## <a name="see-also"></a><span data-ttu-id="dfd25-141">Confira também</span><span class="sxs-lookup"><span data-stu-id="dfd25-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dfd25-142">**IVMVirtualMachine**</span><span class="sxs-lookup"><span data-stu-id="dfd25-142">**IVMVirtualMachine**</span></span>](ivmvirtualmachine.md)
</dt> </dl>

 

