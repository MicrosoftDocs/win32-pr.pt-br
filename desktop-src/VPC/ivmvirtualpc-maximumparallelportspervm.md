---
title: Propriedade IVMVirtualPC MaximumParallelPortsPerVM (VPCCOMInterfaces. h)
description: Recupera o número máximo de portas paralelas por máquina virtual.
ms.assetid: c5baac59-386c-4373-a560-460750178894
keywords:
- Propriedade MaximumParallelPortsPerVM Virtual PC
- Propriedade MaximumParallelPortsPerVM Virtual PC, interface IVMVirtualPC
- IVMVirtualPC interface virtual PC, Propriedade MaximumParallelPortsPerVM
topic_type:
- apiref
api_name:
- IVMVirtualPC.MaximumParallelPortsPerVM
- IVMVirtualPC.get_MaximumParallelPortsPerVM
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 57c5bed446a421190eb47630bde0d05f0cbcee7f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105790453"
---
# <a name="ivmvirtualpcmaximumparallelportspervm-property"></a><span data-ttu-id="93052-106">Propriedade IVMVirtualPC:: MaximumParallelPortsPerVM</span><span class="sxs-lookup"><span data-stu-id="93052-106">IVMVirtualPC::MaximumParallelPortsPerVM property</span></span>

<span data-ttu-id="93052-107">\[O Windows Virtual PC não está mais disponível para uso a partir do Windows 8.</span><span class="sxs-lookup"><span data-stu-id="93052-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="93052-108">Em vez disso, use o [provedor WMI do Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="93052-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="93052-109">Recupera o número máximo de portas paralelas por máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="93052-109">Retrieves the maximum number of parallel ports per virtual machine.</span></span>

<span data-ttu-id="93052-110">Esta propriedade é somente para leitura.</span><span class="sxs-lookup"><span data-stu-id="93052-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="93052-111">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="93052-111">Syntax</span></span>


```C++
HRESULT get_MaximumParallelPortsPerVM(
  [out, retval] long *maxPorts
);
```



## <a name="property-value"></a><span data-ttu-id="93052-112">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="93052-112">Property value</span></span>

<span data-ttu-id="93052-113">O número máximo de portas paralelas por máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="93052-113">The maximum number of parallel ports per virtual machine.</span></span>

## <a name="error-codes"></a><span data-ttu-id="93052-114">Códigos do Erro</span><span class="sxs-lookup"><span data-stu-id="93052-114">Error codes</span></span>



| <span data-ttu-id="93052-115">Nome/valor</span><span class="sxs-lookup"><span data-stu-id="93052-115">Name/value</span></span>                                                                                                                                                                           | <span data-ttu-id="93052-116">Significado</span><span class="sxs-lookup"><span data-stu-id="93052-116">Meaning</span></span>                                                                                         |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="93052-117"><dt>S \_ OK</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="93052-117"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                                              | <span data-ttu-id="93052-118">A operação foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="93052-118">The operation was successful.</span></span><br/>                                                        |
| <dl> <span data-ttu-id="93052-119"><dt>E \_ </dt> <dt>0X80004003</dt> de ponteiro</span><span class="sxs-lookup"><span data-stu-id="93052-119"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>                                | <span data-ttu-id="93052-120">O parâmetro é **NULL**.</span><span class="sxs-lookup"><span data-stu-id="93052-120">The parameter is **NULL**.</span></span><br/>                                                           |
| <dl> <span data-ttu-id="93052-121"><dt>DISP \_ E \_ </dt> <dt>0x80020009</dt> de exceção</span><span class="sxs-lookup"><span data-stu-id="93052-121"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl>                        | <span data-ttu-id="93052-122">Ocorreu um erro inesperado.</span><span class="sxs-lookup"><span data-stu-id="93052-122">An unexpected error has occurred.</span></span><br/>                                                    |
| <dl> <span data-ttu-id="93052-123"><dt>VM \_ E 0xA0040951 de \_ \_ virtualização de hardware \_ desabilitada</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="93052-123"><dt>VM\_E\_HARDWARE\_VIRTUALIZATION\_DISABLED</dt> <dt>0xA0040951</dt></span></span> </dl> | <span data-ttu-id="93052-124">O processador não oferece suporte a extensões de corre (virtualização acelerada por hardware).</span><span class="sxs-lookup"><span data-stu-id="93052-124">The processor does not support Hardware Accelerated Virtualization (HAV) extensions.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="93052-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="93052-125">Requirements</span></span>



| <span data-ttu-id="93052-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="93052-126">Requirement</span></span> | <span data-ttu-id="93052-127">Valor</span><span class="sxs-lookup"><span data-stu-id="93052-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="93052-128">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="93052-128">Minimum supported client</span></span><br/> | <span data-ttu-id="93052-129">\[Somente aplicativos de área de trabalho do Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="93052-129">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="93052-130">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="93052-130">Minimum supported server</span></span><br/> | <span data-ttu-id="93052-131">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="93052-131">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="93052-132">Fim do suporte do cliente</span><span class="sxs-lookup"><span data-stu-id="93052-132">End of client support</span></span><br/>    | <span data-ttu-id="93052-133">Windows 7</span><span class="sxs-lookup"><span data-stu-id="93052-133">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="93052-134">Produto</span><span class="sxs-lookup"><span data-stu-id="93052-134">Product</span></span><br/>                  | <span data-ttu-id="93052-135">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="93052-135">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="93052-136">parâmetro</span><span class="sxs-lookup"><span data-stu-id="93052-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="93052-137"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="93052-137"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="93052-138">IID</span><span class="sxs-lookup"><span data-stu-id="93052-138">IID</span></span><br/>                      | <span data-ttu-id="93052-139">IID \_ IVMVirtualPC é definido como 236ba0d9-a24a-4292-a132-27c1421dfd01</span><span class="sxs-lookup"><span data-stu-id="93052-139">IID\_IVMVirtualPC is defined as 236ba0d9-a24a-4292-a132-27c1421dfd01</span></span><br/>               |



## <a name="see-also"></a><span data-ttu-id="93052-140">Confira também</span><span class="sxs-lookup"><span data-stu-id="93052-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="93052-141">**IVMVirtualPC**</span><span class="sxs-lookup"><span data-stu-id="93052-141">**IVMVirtualPC**</span></span>](ivmvirtualpc.md)
</dt> </dl>

 

