---
title: Propriedade IVMAccountant CPUUtilizationHistory (VPCCOMInterfaces. h)
description: Recupera a utilização de CPU recente desta máquina virtual (como uma matriz de valores percentuais).
ms.assetid: f6b92b25-9455-4061-8db0-3e42f9f7391d
keywords:
- Propriedade CPUUtilizationHistory Virtual PC
- Propriedade CPUUtilizationHistory Virtual PC, interface IVMAccountant
- IVMAccountant interface virtual PC, Propriedade CPUUtilizationHistory
topic_type:
- apiref
api_name:
- IVMAccountant.CPUUtilizationHistory
- IVMAccountant.get_CPUUtilizationHistory
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dfa7e91a83be7ab4c09a0b779a729745e80e1e74
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455914"
---
# <a name="ivmaccountantcpuutilizationhistory-property"></a><span data-ttu-id="ae3c4-106">Propriedade IVMAccountant:: CPUUtilizationHistory</span><span class="sxs-lookup"><span data-stu-id="ae3c4-106">IVMAccountant::CPUUtilizationHistory property</span></span>

<span data-ttu-id="ae3c4-107">\[O Windows Virtual PC não está mais disponível para uso a partir do Windows 8.</span><span class="sxs-lookup"><span data-stu-id="ae3c4-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="ae3c4-108">Em vez disso, use o [provedor WMI do Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="ae3c4-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="ae3c4-109">Recupera a utilização de CPU recente desta máquina virtual (como uma matriz de valores percentuais).</span><span class="sxs-lookup"><span data-stu-id="ae3c4-109">Retrieves the recent CPU utilization of this virtual machine (as an array of percentage values).</span></span>

<span data-ttu-id="ae3c4-110">Esta propriedade é somente para leitura.</span><span class="sxs-lookup"><span data-stu-id="ae3c4-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="ae3c4-111">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="ae3c4-111">Syntax</span></span>


```C++
HRESULT get_CPUUtilizationHistory(
  [out, retval] VARIANT *percentageUtilization
);
```



## <a name="property-value"></a><span data-ttu-id="ae3c4-112">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="ae3c4-112">Property value</span></span>

<span data-ttu-id="ae3c4-113">O recente uso da CPU desta máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="ae3c4-113">The recent CPU use of this virtual machine.</span></span> <span data-ttu-id="ae3c4-114">Esses dados são retornados como uma matriz de 60 elementos que representam a porcentagem de uso da CPU em cada segundo no último minuto.</span><span class="sxs-lookup"><span data-stu-id="ae3c4-114">This data is returned as an array of 60 elements that represent the percentage of CPU use at each second over the past minute.</span></span> <span data-ttu-id="ae3c4-115">O tipo de variante é a \_ matriz VT \| VT \_ UI1.</span><span class="sxs-lookup"><span data-stu-id="ae3c4-115">Variant type is VT\_ARRAY\|VT\_UI1.</span></span>

## <a name="error-codes"></a><span data-ttu-id="ae3c4-116">Códigos do Erro</span><span class="sxs-lookup"><span data-stu-id="ae3c4-116">Error codes</span></span>



| <span data-ttu-id="ae3c4-117">Nome/valor</span><span class="sxs-lookup"><span data-stu-id="ae3c4-117">Name/value</span></span>                                                                                                                                                    | <span data-ttu-id="ae3c4-118">Significado</span><span class="sxs-lookup"><span data-stu-id="ae3c4-118">Meaning</span></span>                                                                            |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="ae3c4-119"><dt>S \_ OK</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="ae3c4-119"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                       | <span data-ttu-id="ae3c4-120">A operação foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="ae3c4-120">The operation was successful.</span></span><br/>                                           |
| <dl> <span data-ttu-id="ae3c4-121"><dt>E \_ </dt> <dt>0X80004003</dt> de ponteiro</span><span class="sxs-lookup"><span data-stu-id="ae3c4-121"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>         | <span data-ttu-id="ae3c4-122">O parâmetro é **NULL**.</span><span class="sxs-lookup"><span data-stu-id="ae3c4-122">The parameter is **NULL**.</span></span><br/>                                              |
| <dl> <span data-ttu-id="ae3c4-123"><dt>S \_ FALSO</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="ae3c4-123"><dt>S\_FALSE</dt> <dt>1</dt></span></span> </dl>                    | <span data-ttu-id="ae3c4-124">A máquina virtual não está em execução.</span><span class="sxs-lookup"><span data-stu-id="ae3c4-124">The virtual machine is not running.</span></span> <span data-ttu-id="ae3c4-125">Todos os elementos da matriz 60 são definidos como 0.</span><span class="sxs-lookup"><span data-stu-id="ae3c4-125">All 60 array elements are set to 0.</span></span><br/> |
| <dl> <span data-ttu-id="ae3c4-126"><dt>DISP \_ E \_ </dt> <dt>0x80020009</dt> de exceção</span><span class="sxs-lookup"><span data-stu-id="ae3c4-126"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl> | <span data-ttu-id="ae3c4-127">Ocorreu um erro inesperado.</span><span class="sxs-lookup"><span data-stu-id="ae3c4-127">An unexpected error has occurred.</span></span><br/>                                       |



## <a name="requirements"></a><span data-ttu-id="ae3c4-128">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ae3c4-128">Requirements</span></span>



| <span data-ttu-id="ae3c4-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="ae3c4-129">Requirement</span></span> | <span data-ttu-id="ae3c4-130">Valor</span><span class="sxs-lookup"><span data-stu-id="ae3c4-130">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="ae3c4-131">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ae3c4-131">Minimum supported client</span></span><br/> | <span data-ttu-id="ae3c4-132">\[Somente aplicativos de área de trabalho do Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="ae3c4-132">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="ae3c4-133">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ae3c4-133">Minimum supported server</span></span><br/> | <span data-ttu-id="ae3c4-134">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="ae3c4-134">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="ae3c4-135">Fim do suporte do cliente</span><span class="sxs-lookup"><span data-stu-id="ae3c4-135">End of client support</span></span><br/>    | <span data-ttu-id="ae3c4-136">Windows 7</span><span class="sxs-lookup"><span data-stu-id="ae3c4-136">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="ae3c4-137">Produto</span><span class="sxs-lookup"><span data-stu-id="ae3c4-137">Product</span></span><br/>                  | <span data-ttu-id="ae3c4-138">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="ae3c4-138">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="ae3c4-139">parâmetro</span><span class="sxs-lookup"><span data-stu-id="ae3c4-139">Header</span></span><br/>                   | <dl> <span data-ttu-id="ae3c4-140"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="ae3c4-140"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="ae3c4-141">IID</span><span class="sxs-lookup"><span data-stu-id="ae3c4-141">IID</span></span><br/>                      | <span data-ttu-id="ae3c4-142">IID \_ IVMAccountant é definido como 6376c067-7f57-4D63-b754-06e2e4f51d73</span><span class="sxs-lookup"><span data-stu-id="ae3c4-142">IID\_IVMAccountant is defined as 6376c067-7f57-4d63-b754-06e2e4f51d73</span></span><br/>              |



## <a name="see-also"></a><span data-ttu-id="ae3c4-143">Confira também</span><span class="sxs-lookup"><span data-stu-id="ae3c4-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ae3c4-144">**IVMAccountant**</span><span class="sxs-lookup"><span data-stu-id="ae3c4-144">**IVMAccountant**</span></span>](ivmaccountant.md)
</dt> </dl>

 

