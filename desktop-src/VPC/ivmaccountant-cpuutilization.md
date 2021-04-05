---
title: Propriedade IVMAccountant CPUUtilization (VPCCOMInterfaces. h)
description: Recupera a porcentagem de utilização da CPU atual para esta máquina virtual.
ms.assetid: 69bb61ec-af41-4bd0-95bd-4698a1d33098
keywords:
- Propriedade CPUUtilization Virtual PC
- Propriedade CPUUtilization Virtual PC, interface IVMAccountant
- IVMAccountant interface virtual PC, Propriedade CPUUtilization
topic_type:
- apiref
api_name:
- IVMAccountant.CPUUtilization
- IVMAccountant.get_CPUUtilization
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c9e38c223f47678cdb9c2d49e06452d014083c94
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103919108"
---
# <a name="ivmaccountantcpuutilization-property"></a><span data-ttu-id="0c2e4-106">Propriedade IVMAccountant:: CPUUtilization</span><span class="sxs-lookup"><span data-stu-id="0c2e4-106">IVMAccountant::CPUUtilization property</span></span>

<span data-ttu-id="0c2e4-107">\[O Windows Virtual PC não está mais disponível para uso a partir do Windows 8.</span><span class="sxs-lookup"><span data-stu-id="0c2e4-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="0c2e4-108">Em vez disso, use o [provedor WMI do Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="0c2e4-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="0c2e4-109">Recupera a porcentagem de utilização da CPU atual para esta máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="0c2e4-109">Retrieves the percentage of current CPU utilization for this virtual machine.</span></span>

<span data-ttu-id="0c2e4-110">Esta propriedade é somente para leitura.</span><span class="sxs-lookup"><span data-stu-id="0c2e4-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="0c2e4-111">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="0c2e4-111">Syntax</span></span>


```C++
HRESULT get_CPUUtilization(
  [out, retval] long *percentageUtilization
);
```



## <a name="property-value"></a><span data-ttu-id="0c2e4-112">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="0c2e4-112">Property value</span></span>

<span data-ttu-id="0c2e4-113">A porcentagem de utilização atual da CPU.</span><span class="sxs-lookup"><span data-stu-id="0c2e4-113">The percentage of current CPU utilization.</span></span>

## <a name="error-codes"></a><span data-ttu-id="0c2e4-114">Códigos do Erro</span><span class="sxs-lookup"><span data-stu-id="0c2e4-114">Error codes</span></span>



| <span data-ttu-id="0c2e4-115">Nome/valor</span><span class="sxs-lookup"><span data-stu-id="0c2e4-115">Name/value</span></span>                                                                                                                                                    | <span data-ttu-id="0c2e4-116">Significado</span><span class="sxs-lookup"><span data-stu-id="0c2e4-116">Meaning</span></span>                                        |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------|
| <dl> <span data-ttu-id="0c2e4-117"><dt>S \_ OK</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="0c2e4-117"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                       | <span data-ttu-id="0c2e4-118">A operação foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="0c2e4-118">The operation was successful.</span></span><br/>       |
| <dl> <span data-ttu-id="0c2e4-119"><dt>E \_ </dt> <dt>0X80004003</dt> de ponteiro</span><span class="sxs-lookup"><span data-stu-id="0c2e4-119"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>         | <span data-ttu-id="0c2e4-120">O parâmetro é **NULL**.</span><span class="sxs-lookup"><span data-stu-id="0c2e4-120">The parameter is **NULL**.</span></span><br/>          |
| <dl> <span data-ttu-id="0c2e4-121"><dt>S \_ FALSO</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="0c2e4-121"><dt>S\_FALSE</dt> <dt>1</dt></span></span> </dl>                    | <span data-ttu-id="0c2e4-122">A máquina virtual não está em execução.</span><span class="sxs-lookup"><span data-stu-id="0c2e4-122">The virtual machine is not running.</span></span><br/> |
| <dl> <span data-ttu-id="0c2e4-123"><dt>DISP \_ E \_ </dt> <dt>0x80020009</dt> de exceção</span><span class="sxs-lookup"><span data-stu-id="0c2e4-123"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl> | <span data-ttu-id="0c2e4-124">Ocorreu um erro inesperado.</span><span class="sxs-lookup"><span data-stu-id="0c2e4-124">An unexpected error has occurred.</span></span><br/>   |



## <a name="requirements"></a><span data-ttu-id="0c2e4-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0c2e4-125">Requirements</span></span>



| <span data-ttu-id="0c2e4-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="0c2e4-126">Requirement</span></span> | <span data-ttu-id="0c2e4-127">Valor</span><span class="sxs-lookup"><span data-stu-id="0c2e4-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="0c2e4-128">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="0c2e4-128">Minimum supported client</span></span><br/> | <span data-ttu-id="0c2e4-129">\[Somente aplicativos de área de trabalho do Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="0c2e4-129">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="0c2e4-130">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="0c2e4-130">Minimum supported server</span></span><br/> | <span data-ttu-id="0c2e4-131">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="0c2e4-131">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="0c2e4-132">Fim do suporte do cliente</span><span class="sxs-lookup"><span data-stu-id="0c2e4-132">End of client support</span></span><br/>    | <span data-ttu-id="0c2e4-133">Windows 7</span><span class="sxs-lookup"><span data-stu-id="0c2e4-133">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="0c2e4-134">Produto</span><span class="sxs-lookup"><span data-stu-id="0c2e4-134">Product</span></span><br/>                  | <span data-ttu-id="0c2e4-135">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="0c2e4-135">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="0c2e4-136">parâmetro</span><span class="sxs-lookup"><span data-stu-id="0c2e4-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="0c2e4-137"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="0c2e4-137"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="0c2e4-138">IID</span><span class="sxs-lookup"><span data-stu-id="0c2e4-138">IID</span></span><br/>                      | <span data-ttu-id="0c2e4-139">IID \_ IVMAccountant é definido como 6376c067-7f57-4D63-b754-06e2e4f51d73</span><span class="sxs-lookup"><span data-stu-id="0c2e4-139">IID\_IVMAccountant is defined as 6376c067-7f57-4d63-b754-06e2e4f51d73</span></span><br/>              |



## <a name="see-also"></a><span data-ttu-id="0c2e4-140">Confira também</span><span class="sxs-lookup"><span data-stu-id="0c2e4-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0c2e4-141">**IVMAccountant**</span><span class="sxs-lookup"><span data-stu-id="0c2e4-141">**IVMAccountant**</span></span>](ivmaccountant.md)
</dt> </dl>

 

