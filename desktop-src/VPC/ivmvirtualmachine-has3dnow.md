---
title: Propriedade IVMVirtualMachine Has3DNow (VPCCOMInterfaces. h)
description: Determina se o processador dá suporte ao conjunto de instruções 3DNow. | Propriedade IVMVirtualMachine Has3DNow (VPCCOMInterfaces. h)
ms.assetid: 525ee7f0-081c-4f87-b2b7-ffec09f632c4
keywords:
- Propriedade Has3DNow Virtual PC
- Propriedade Has3DNow Virtual PC, interface IVMVirtualMachine
- IVMVirtualMachine interface virtual PC, Propriedade Has3DNow
topic_type:
- apiref
api_name:
- IVMVirtualMachine.Has3DNow
- IVMVirtualMachine.get_Has3DNow
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7b347fa802b999707e43019e9b7808c844c0288f
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "103663942"
---
# <a name="ivmvirtualmachinehas3dnow-property"></a><span data-ttu-id="80e88-107">Propriedade IVMVirtualMachine:: Has3DNow</span><span class="sxs-lookup"><span data-stu-id="80e88-107">IVMVirtualMachine::Has3DNow property</span></span>

<span data-ttu-id="80e88-108">\[O Windows Virtual PC não está mais disponível para uso a partir do Windows 8.</span><span class="sxs-lookup"><span data-stu-id="80e88-108">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="80e88-109">Em vez disso, use o [provedor WMI do Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="80e88-109">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="80e88-110">Determina se o processador dá suporte ao conjunto de instruções 3DNow.</span><span class="sxs-lookup"><span data-stu-id="80e88-110">Determines whether the processor supports the 3DNow instruction set.</span></span>

<span data-ttu-id="80e88-111">Esta propriedade é somente para leitura.</span><span class="sxs-lookup"><span data-stu-id="80e88-111">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="80e88-112">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="80e88-112">Syntax</span></span>


```C++
HRESULT get_Has3DNow(
  [out, retval] VARIANT_BOOL *threeDNowEnabled
);
```



## <a name="property-value"></a><span data-ttu-id="80e88-113">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="80e88-113">Property value</span></span>

<span data-ttu-id="80e88-114">**True** se o processador tiver suporte para o conjunto de instruções 3DNow; caso contrário, **false** .</span><span class="sxs-lookup"><span data-stu-id="80e88-114">**TRUE** if the processor supported the 3DNow instruction set, **FALSE** otherwise.</span></span>

## <a name="error-codes"></a><span data-ttu-id="80e88-115">Códigos do Erro</span><span class="sxs-lookup"><span data-stu-id="80e88-115">Error codes</span></span>



| <span data-ttu-id="80e88-116">Nome/valor</span><span class="sxs-lookup"><span data-stu-id="80e88-116">Name/value</span></span>                                                                                                                                                    | <span data-ttu-id="80e88-117">Significado</span><span class="sxs-lookup"><span data-stu-id="80e88-117">Meaning</span></span>                                      |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="80e88-118"><dt>S \_ OK</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="80e88-118"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                       | <span data-ttu-id="80e88-119">A operação foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="80e88-119">The operation was successful.</span></span><br/>     |
| <dl> <span data-ttu-id="80e88-120"><dt>E \_ </dt> <dt>0X80004003</dt> de ponteiro</span><span class="sxs-lookup"><span data-stu-id="80e88-120"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>         | <span data-ttu-id="80e88-121">O parâmetro é **NULL**.</span><span class="sxs-lookup"><span data-stu-id="80e88-121">The parameter is **NULL**.</span></span><br/>        |
| <dl> <span data-ttu-id="80e88-122"><dt>VM \_ E 0xA0040207 de \_ VM \_ desconhecido</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="80e88-122"><dt>VM\_E\_VM\_UNKNOWN</dt> <dt>0xA0040207</dt></span></span> </dl> | <span data-ttu-id="80e88-123">A configuração é desconhecida.</span><span class="sxs-lookup"><span data-stu-id="80e88-123">The configuration is unknown.</span></span><br/>     |
| <dl> <span data-ttu-id="80e88-124"><dt>DISP \_ E \_ </dt> <dt>0x80020009</dt> de exceção</span><span class="sxs-lookup"><span data-stu-id="80e88-124"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl> | <span data-ttu-id="80e88-125">Ocorreu um erro inesperado.</span><span class="sxs-lookup"><span data-stu-id="80e88-125">An unexpected error has occurred.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="80e88-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="80e88-126">Requirements</span></span>



| <span data-ttu-id="80e88-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="80e88-127">Requirement</span></span> | <span data-ttu-id="80e88-128">Valor</span><span class="sxs-lookup"><span data-stu-id="80e88-128">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="80e88-129">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="80e88-129">Minimum supported client</span></span><br/> | <span data-ttu-id="80e88-130">\[Somente aplicativos de área de trabalho do Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="80e88-130">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="80e88-131">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="80e88-131">Minimum supported server</span></span><br/> | <span data-ttu-id="80e88-132">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="80e88-132">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="80e88-133">Fim do suporte do cliente</span><span class="sxs-lookup"><span data-stu-id="80e88-133">End of client support</span></span><br/>    | <span data-ttu-id="80e88-134">Windows 7</span><span class="sxs-lookup"><span data-stu-id="80e88-134">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="80e88-135">Produto</span><span class="sxs-lookup"><span data-stu-id="80e88-135">Product</span></span><br/>                  | <span data-ttu-id="80e88-136">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="80e88-136">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="80e88-137">parâmetro</span><span class="sxs-lookup"><span data-stu-id="80e88-137">Header</span></span><br/>                   | <dl> <span data-ttu-id="80e88-138"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="80e88-138"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="80e88-139">IID</span><span class="sxs-lookup"><span data-stu-id="80e88-139">IID</span></span><br/>                      | <span data-ttu-id="80e88-140">IID \_ IVMVirtualMachine é definido como f7092aa1-33ed-4f78-a59f-c00adfc2edd7</span><span class="sxs-lookup"><span data-stu-id="80e88-140">IID\_IVMVirtualMachine is defined as f7092aa1-33ed-4f78-a59f-c00adfc2edd7</span></span><br/>          |



## <a name="see-also"></a><span data-ttu-id="80e88-141">Confira também</span><span class="sxs-lookup"><span data-stu-id="80e88-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="80e88-142">**IVMVirtualMachine**</span><span class="sxs-lookup"><span data-stu-id="80e88-142">**IVMVirtualMachine**</span></span>](ivmvirtualmachine.md)
</dt> </dl>

 

