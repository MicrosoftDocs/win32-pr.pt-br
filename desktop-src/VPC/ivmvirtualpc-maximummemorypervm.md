---
title: Propriedade IVMVirtualPC MaximumMemoryPerVM (VPCCOMInterfaces. h)
description: Recupera a quantidade máxima permitida de memória física por máquina virtual, em megabytes.
ms.assetid: eb30dd6c-8f37-4cf9-9ed7-47925b5b1112
keywords:
- Propriedade MaximumMemoryPerVM Virtual PC
- Propriedade MaximumMemoryPerVM Virtual PC, interface IVMVirtualPC
- IVMVirtualPC interface virtual PC, Propriedade MaximumMemoryPerVM
topic_type:
- apiref
api_name:
- IVMVirtualPC.MaximumMemoryPerVM
- IVMVirtualPC.get_MaximumMemoryPerVM
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 936d88c29df4be934e03d1c0b7bde60139bde268
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103824138"
---
# <a name="ivmvirtualpcmaximummemorypervm-property"></a><span data-ttu-id="a130b-106">Propriedade IVMVirtualPC:: MaximumMemoryPerVM</span><span class="sxs-lookup"><span data-stu-id="a130b-106">IVMVirtualPC::MaximumMemoryPerVM property</span></span>

<span data-ttu-id="a130b-107">\[O Windows Virtual PC não está mais disponível para uso a partir do Windows 8.</span><span class="sxs-lookup"><span data-stu-id="a130b-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="a130b-108">Em vez disso, use o [provedor WMI do Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="a130b-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="a130b-109">Recupera a quantidade máxima permitida de memória física por máquina virtual, em megabytes.</span><span class="sxs-lookup"><span data-stu-id="a130b-109">Retrieves the maximum allowable quantity of physical memory per virtual machine, in megabytes.</span></span>

<span data-ttu-id="a130b-110">Esta propriedade é somente para leitura.</span><span class="sxs-lookup"><span data-stu-id="a130b-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="a130b-111">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="a130b-111">Syntax</span></span>


```C++
HRESULT get_MaximumMemoryPerVM(
  [out, retval] long *megabytesOfMemory
);
```



## <a name="property-value"></a><span data-ttu-id="a130b-112">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="a130b-112">Property value</span></span>

<span data-ttu-id="a130b-113">A quantidade máxima permitida, em megabytes, de memória física por máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="a130b-113">The maximum allowable quantity, in megabytes, of physical memory per virtual machine.</span></span>

## <a name="error-codes"></a><span data-ttu-id="a130b-114">Códigos do Erro</span><span class="sxs-lookup"><span data-stu-id="a130b-114">Error codes</span></span>



| <span data-ttu-id="a130b-115">Nome/valor</span><span class="sxs-lookup"><span data-stu-id="a130b-115">Name/value</span></span>                                                                                                                                                                           | <span data-ttu-id="a130b-116">Significado</span><span class="sxs-lookup"><span data-stu-id="a130b-116">Meaning</span></span>                                                                                         |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="a130b-117"><dt>S \_ OK</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="a130b-117"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                                              | <span data-ttu-id="a130b-118">A operação foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="a130b-118">The operation was successful.</span></span><br/>                                                        |
| <dl> <span data-ttu-id="a130b-119"><dt>E \_ </dt> <dt>0X80004003</dt> de ponteiro</span><span class="sxs-lookup"><span data-stu-id="a130b-119"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>                                | <span data-ttu-id="a130b-120">O parâmetro é **NULL**.</span><span class="sxs-lookup"><span data-stu-id="a130b-120">The parameter is **NULL**.</span></span><br/>                                                           |
| <dl> <span data-ttu-id="a130b-121"><dt>DISP \_ E \_ </dt> <dt>0x80020009</dt> de exceção</span><span class="sxs-lookup"><span data-stu-id="a130b-121"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl>                        | <span data-ttu-id="a130b-122">Ocorreu um erro inesperado.</span><span class="sxs-lookup"><span data-stu-id="a130b-122">An unexpected error has occurred.</span></span><br/>                                                    |
| <dl> <span data-ttu-id="a130b-123"><dt>VM \_ E 0xA0040951 de \_ \_ virtualização de hardware \_ desabilitada</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="a130b-123"><dt>VM\_E\_HARDWARE\_VIRTUALIZATION\_DISABLED</dt> <dt>0xA0040951</dt></span></span> </dl> | <span data-ttu-id="a130b-124">O processador não oferece suporte a extensões de corre (virtualização acelerada por hardware).</span><span class="sxs-lookup"><span data-stu-id="a130b-124">The processor does not support Hardware Accelerated Virtualization (HAV) extensions.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="a130b-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a130b-125">Requirements</span></span>



| <span data-ttu-id="a130b-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="a130b-126">Requirement</span></span> | <span data-ttu-id="a130b-127">Valor</span><span class="sxs-lookup"><span data-stu-id="a130b-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="a130b-128">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a130b-128">Minimum supported client</span></span><br/> | <span data-ttu-id="a130b-129">\[Somente aplicativos de área de trabalho do Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="a130b-129">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="a130b-130">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a130b-130">Minimum supported server</span></span><br/> | <span data-ttu-id="a130b-131">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="a130b-131">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="a130b-132">Fim do suporte do cliente</span><span class="sxs-lookup"><span data-stu-id="a130b-132">End of client support</span></span><br/>    | <span data-ttu-id="a130b-133">Windows 7</span><span class="sxs-lookup"><span data-stu-id="a130b-133">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="a130b-134">Produto</span><span class="sxs-lookup"><span data-stu-id="a130b-134">Product</span></span><br/>                  | <span data-ttu-id="a130b-135">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="a130b-135">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="a130b-136">parâmetro</span><span class="sxs-lookup"><span data-stu-id="a130b-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="a130b-137"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="a130b-137"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="a130b-138">IID</span><span class="sxs-lookup"><span data-stu-id="a130b-138">IID</span></span><br/>                      | <span data-ttu-id="a130b-139">IID \_ IVMVirtualPC é definido como 236ba0d9-a24a-4292-a132-27c1421dfd01</span><span class="sxs-lookup"><span data-stu-id="a130b-139">IID\_IVMVirtualPC is defined as 236ba0d9-a24a-4292-a132-27c1421dfd01</span></span><br/>               |



## <a name="see-also"></a><span data-ttu-id="a130b-140">Confira também</span><span class="sxs-lookup"><span data-stu-id="a130b-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a130b-141">**IVMVirtualPC**</span><span class="sxs-lookup"><span data-stu-id="a130b-141">**IVMVirtualPC**</span></span>](ivmvirtualpc.md)
</dt> </dl>

 

