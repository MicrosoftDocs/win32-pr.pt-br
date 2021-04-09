---
title: Propriedade IVMVirtualPC SuggestedMaximumMemoryPerVM (VPCCOMInterfaces. h)
description: Recupera a quantidade permitida máxima de memória física sugerida por máquina virtual, em megabytes, para evitar condições de memória insuficiente no host.
ms.assetid: 533cca40-f41d-4717-87ae-d8072414a637
keywords:
- Propriedade SuggestedMaximumMemoryPerVM Virtual PC
- Propriedade SuggestedMaximumMemoryPerVM Virtual PC, interface IVMVirtualPC
- IVMVirtualPC interface virtual PC, Propriedade SuggestedMaximumMemoryPerVM
topic_type:
- apiref
api_name:
- IVMVirtualPC.SuggestedMaximumMemoryPerVM
- IVMVirtualPC.get_SuggestedMaximumMemoryPerVM
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 142c4ade861116876342d598fbf10b5925fa100e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104009759"
---
# <a name="ivmvirtualpcsuggestedmaximummemorypervm-property"></a><span data-ttu-id="980c4-106">Propriedade IVMVirtualPC:: SuggestedMaximumMemoryPerVM</span><span class="sxs-lookup"><span data-stu-id="980c4-106">IVMVirtualPC::SuggestedMaximumMemoryPerVM property</span></span>

<span data-ttu-id="980c4-107">\[O Windows Virtual PC não está mais disponível para uso a partir do Windows 8.</span><span class="sxs-lookup"><span data-stu-id="980c4-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="980c4-108">Em vez disso, use o [provedor WMI do Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="980c4-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="980c4-109">Recupera a quantidade permitida máxima de memória física sugerida por máquina virtual, em megabytes, para evitar condições de memória insuficiente no host.</span><span class="sxs-lookup"><span data-stu-id="980c4-109">Retrieves the suggested maximum allowable quantity of physical memory per virtual machine, in megabytes, to avoid low memory conditions on the host.</span></span>

<span data-ttu-id="980c4-110">Esta propriedade é somente para leitura.</span><span class="sxs-lookup"><span data-stu-id="980c4-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="980c4-111">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="980c4-111">Syntax</span></span>


```C++
HRESULT get_SuggestedMaximumMemoryPerVM(
  [out, retval] long *megabytesOfMemory
);
```



## <a name="property-value"></a><span data-ttu-id="980c4-112">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="980c4-112">Property value</span></span>

<span data-ttu-id="980c4-113">A quantidade máxima de permissão sugerida, em megabytes, da memória física por máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="980c4-113">The suggested maximum allowable quantity, in megabytes, of physical memory per virtual machine.</span></span>

## <a name="error-codes"></a><span data-ttu-id="980c4-114">Códigos do Erro</span><span class="sxs-lookup"><span data-stu-id="980c4-114">Error codes</span></span>



| <span data-ttu-id="980c4-115">Nome/valor</span><span class="sxs-lookup"><span data-stu-id="980c4-115">Name/value</span></span>                                                                                                                                                                           | <span data-ttu-id="980c4-116">Significado</span><span class="sxs-lookup"><span data-stu-id="980c4-116">Meaning</span></span>                                                                                         |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="980c4-117"><dt>S \_ OK</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="980c4-117"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                                              | <span data-ttu-id="980c4-118">A operação foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="980c4-118">The operation was successful.</span></span><br/>                                                        |
| <dl> <span data-ttu-id="980c4-119"><dt>E \_ </dt> <dt>0X80004003</dt> de ponteiro</span><span class="sxs-lookup"><span data-stu-id="980c4-119"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>                                | <span data-ttu-id="980c4-120">O parâmetro é **NULL**.</span><span class="sxs-lookup"><span data-stu-id="980c4-120">The parameter is **NULL**.</span></span><br/>                                                           |
| <dl> <span data-ttu-id="980c4-121"><dt>DISP \_ E \_ </dt> <dt>0x80020009</dt> de exceção</span><span class="sxs-lookup"><span data-stu-id="980c4-121"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl>                        | <span data-ttu-id="980c4-122">Ocorreu um erro inesperado.</span><span class="sxs-lookup"><span data-stu-id="980c4-122">An unexpected error has occurred.</span></span><br/>                                                    |
| <dl> <span data-ttu-id="980c4-123"><dt>VM \_ E 0xA0040951 de \_ \_ virtualização de hardware \_ desabilitada</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="980c4-123"><dt>VM\_E\_HARDWARE\_VIRTUALIZATION\_DISABLED</dt> <dt>0xA0040951</dt></span></span> </dl> | <span data-ttu-id="980c4-124">O processador não oferece suporte a extensões de corre (virtualização acelerada por hardware).</span><span class="sxs-lookup"><span data-stu-id="980c4-124">The processor does not support Hardware Accelerated Virtualization (HAV) extensions.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="980c4-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="980c4-125">Requirements</span></span>



| <span data-ttu-id="980c4-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="980c4-126">Requirement</span></span> | <span data-ttu-id="980c4-127">Valor</span><span class="sxs-lookup"><span data-stu-id="980c4-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="980c4-128">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="980c4-128">Minimum supported client</span></span><br/> | <span data-ttu-id="980c4-129">\[Somente aplicativos de área de trabalho do Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="980c4-129">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="980c4-130">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="980c4-130">Minimum supported server</span></span><br/> | <span data-ttu-id="980c4-131">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="980c4-131">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="980c4-132">Fim do suporte do cliente</span><span class="sxs-lookup"><span data-stu-id="980c4-132">End of client support</span></span><br/>    | <span data-ttu-id="980c4-133">Windows 7</span><span class="sxs-lookup"><span data-stu-id="980c4-133">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="980c4-134">Produto</span><span class="sxs-lookup"><span data-stu-id="980c4-134">Product</span></span><br/>                  | <span data-ttu-id="980c4-135">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="980c4-135">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="980c4-136">parâmetro</span><span class="sxs-lookup"><span data-stu-id="980c4-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="980c4-137"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="980c4-137"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="980c4-138">IID</span><span class="sxs-lookup"><span data-stu-id="980c4-138">IID</span></span><br/>                      | <span data-ttu-id="980c4-139">IID \_ IVMVirtualPC é definido como 236ba0d9-a24a-4292-a132-27c1421dfd01</span><span class="sxs-lookup"><span data-stu-id="980c4-139">IID\_IVMVirtualPC is defined as 236ba0d9-a24a-4292-a132-27c1421dfd01</span></span><br/>               |



## <a name="see-also"></a><span data-ttu-id="980c4-140">Confira também</span><span class="sxs-lookup"><span data-stu-id="980c4-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="980c4-141">**IVMVirtualPC**</span><span class="sxs-lookup"><span data-stu-id="980c4-141">**IVMVirtualPC**</span></span>](ivmvirtualpc.md)
</dt> </dl>

 

