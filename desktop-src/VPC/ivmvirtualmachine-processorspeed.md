---
title: Propriedade IVMVirtualMachine ProcessorSpeed (VPCCOMInterfaces. h)
description: Velocidade do processador, em megahertz (MHz) ou gigahertz (GHz).
ms.assetid: 465157a9-08ad-4636-b7c6-a188ff21e131
keywords:
- Propriedade ProcessorSpeed Virtual PC
- Propriedade ProcessorSpeed Virtual PC, interface IVMVirtualMachine
- IVMVirtualMachine interface virtual PC, Propriedade ProcessorSpeed
topic_type:
- apiref
api_name:
- IVMVirtualMachine.ProcessorSpeed
- IVMVirtualMachine.get_ProcessorSpeed
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ebaeb6f17e867d7618241b099b765ff450a2a4e6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455799"
---
# <a name="ivmvirtualmachineprocessorspeed-property"></a><span data-ttu-id="7a0cd-106">IVMVirtualMachine: Propriedade rocessorSpeed de:P</span><span class="sxs-lookup"><span data-stu-id="7a0cd-106">IVMVirtualMachine::ProcessorSpeed property</span></span>

<span data-ttu-id="7a0cd-107">\[O Windows Virtual PC não está mais disponível para uso a partir do Windows 8.</span><span class="sxs-lookup"><span data-stu-id="7a0cd-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="7a0cd-108">Em vez disso, use o [provedor WMI do Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="7a0cd-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="7a0cd-109">Recupera a velocidade do processador, em megahertz (MHz) ou gigahertz (GHz).</span><span class="sxs-lookup"><span data-stu-id="7a0cd-109">Retrieves the speed of the processor, in megahertz (MHz) or gigahertz (GHz).</span></span>

<span data-ttu-id="7a0cd-110">Esta propriedade é somente para leitura.</span><span class="sxs-lookup"><span data-stu-id="7a0cd-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="7a0cd-111">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="7a0cd-111">Syntax</span></span>


```C++
HRESULT get_ProcessorSpeed(
  [out, retval] long *processorSpeed
);
```



## <a name="property-value"></a><span data-ttu-id="7a0cd-112">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="7a0cd-112">Property value</span></span>

<span data-ttu-id="7a0cd-113">A velocidade, em megahertz ou gigahertz.</span><span class="sxs-lookup"><span data-stu-id="7a0cd-113">The speed, in megahertz or gigahertz.</span></span>

## <a name="error-codes"></a><span data-ttu-id="7a0cd-114">Códigos do Erro</span><span class="sxs-lookup"><span data-stu-id="7a0cd-114">Error codes</span></span>



| <span data-ttu-id="7a0cd-115">Nome/valor</span><span class="sxs-lookup"><span data-stu-id="7a0cd-115">Name/value</span></span>                                                                                                                                                    | <span data-ttu-id="7a0cd-116">Significado</span><span class="sxs-lookup"><span data-stu-id="7a0cd-116">Meaning</span></span>                                      |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="7a0cd-117"><dt>S \_ OK</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="7a0cd-117"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                       | <span data-ttu-id="7a0cd-118">A operação foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="7a0cd-118">The operation was successful.</span></span><br/>     |
| <dl> <span data-ttu-id="7a0cd-119"><dt>E \_ </dt> <dt>0X80004003</dt> de ponteiro</span><span class="sxs-lookup"><span data-stu-id="7a0cd-119"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>         | <span data-ttu-id="7a0cd-120">O parâmetro é **NULL**.</span><span class="sxs-lookup"><span data-stu-id="7a0cd-120">The parameter is **NULL**.</span></span><br/>        |
| <dl> <span data-ttu-id="7a0cd-121"><dt>VM \_ E 0xA0040207 de \_ VM \_ desconhecido</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="7a0cd-121"><dt>VM\_E\_VM\_UNKNOWN</dt> <dt>0xA0040207</dt></span></span> </dl> | <span data-ttu-id="7a0cd-122">A configuração é desconhecida.</span><span class="sxs-lookup"><span data-stu-id="7a0cd-122">The configuration is unknown.</span></span><br/>     |
| <dl> <span data-ttu-id="7a0cd-123"><dt>DISP \_ E \_ </dt> <dt>0x80020009</dt> de exceção</span><span class="sxs-lookup"><span data-stu-id="7a0cd-123"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl> | <span data-ttu-id="7a0cd-124">Ocorreu um erro inesperado.</span><span class="sxs-lookup"><span data-stu-id="7a0cd-124">An unexpected error has occurred.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="7a0cd-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7a0cd-125">Requirements</span></span>



| <span data-ttu-id="7a0cd-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="7a0cd-126">Requirement</span></span> | <span data-ttu-id="7a0cd-127">Valor</span><span class="sxs-lookup"><span data-stu-id="7a0cd-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="7a0cd-128">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="7a0cd-128">Minimum supported client</span></span><br/> | <span data-ttu-id="7a0cd-129">\[Somente aplicativos de área de trabalho do Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="7a0cd-129">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="7a0cd-130">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="7a0cd-130">Minimum supported server</span></span><br/> | <span data-ttu-id="7a0cd-131">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="7a0cd-131">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="7a0cd-132">Fim do suporte do cliente</span><span class="sxs-lookup"><span data-stu-id="7a0cd-132">End of client support</span></span><br/>    | <span data-ttu-id="7a0cd-133">Windows 7</span><span class="sxs-lookup"><span data-stu-id="7a0cd-133">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="7a0cd-134">Produto</span><span class="sxs-lookup"><span data-stu-id="7a0cd-134">Product</span></span><br/>                  | <span data-ttu-id="7a0cd-135">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="7a0cd-135">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="7a0cd-136">parâmetro</span><span class="sxs-lookup"><span data-stu-id="7a0cd-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="7a0cd-137"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="7a0cd-137"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="7a0cd-138">IID</span><span class="sxs-lookup"><span data-stu-id="7a0cd-138">IID</span></span><br/>                      | <span data-ttu-id="7a0cd-139">IID \_ IVMVirtualMachine é definido como f7092aa1-33ed-4f78-a59f-c00adfc2edd7</span><span class="sxs-lookup"><span data-stu-id="7a0cd-139">IID\_IVMVirtualMachine is defined as f7092aa1-33ed-4f78-a59f-c00adfc2edd7</span></span><br/>          |



## <a name="see-also"></a><span data-ttu-id="7a0cd-140">Confira também</span><span class="sxs-lookup"><span data-stu-id="7a0cd-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7a0cd-141">**IVMVirtualMachine**</span><span class="sxs-lookup"><span data-stu-id="7a0cd-141">**IVMVirtualMachine**</span></span>](ivmvirtualmachine.md)
</dt> </dl>

 

