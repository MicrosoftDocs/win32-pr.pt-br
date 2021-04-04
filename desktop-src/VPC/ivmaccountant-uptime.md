---
title: Propriedade de tempo de atividade IVMAccountant (VPCCOMInterfaces. h)
description: Recupera o número de segundos em que a máquina virtual está em execução.
ms.assetid: 0c62d51b-fdf1-43f6-81d8-a5f0538c510f
keywords:
- Propriedade de tempo de atividade Virtual PC
- Propriedade de tempo de atividade Virtual PC, interface IVMAccountant
- Virtual PC de interface IVMAccountant, propriedade de tempo de atividade
topic_type:
- apiref
api_name:
- IVMAccountant.UpTime
- IVMAccountant.get_UpTime
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c496aa9c32d402dcc8e84bad5410ec7774d2a80a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104085655"
---
# <a name="ivmaccountantuptime-property"></a><span data-ttu-id="c199b-106">Propriedade IVMAccountant:: tempo de atividade</span><span class="sxs-lookup"><span data-stu-id="c199b-106">IVMAccountant::UpTime property</span></span>

<span data-ttu-id="c199b-107">\[O Windows Virtual PC não está mais disponível para uso a partir do Windows 8.</span><span class="sxs-lookup"><span data-stu-id="c199b-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="c199b-108">Em vez disso, use o [provedor WMI do Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="c199b-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="c199b-109">Recupera o número de segundos em que a máquina virtual está em execução.</span><span class="sxs-lookup"><span data-stu-id="c199b-109">Retrieves the number of seconds that the virtual machine has been running.</span></span>

<span data-ttu-id="c199b-110">Esta propriedade é somente para leitura.</span><span class="sxs-lookup"><span data-stu-id="c199b-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="c199b-111">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="c199b-111">Syntax</span></span>


```C++
HRESULT get_UpTime(
  [out, retval] long *secondsAlive
);
```



## <a name="property-value"></a><span data-ttu-id="c199b-112">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="c199b-112">Property value</span></span>

<span data-ttu-id="c199b-113">O número de segundos.</span><span class="sxs-lookup"><span data-stu-id="c199b-113">The number of seconds.</span></span>

## <a name="error-codes"></a><span data-ttu-id="c199b-114">Códigos do Erro</span><span class="sxs-lookup"><span data-stu-id="c199b-114">Error codes</span></span>



| <span data-ttu-id="c199b-115">Nome/valor</span><span class="sxs-lookup"><span data-stu-id="c199b-115">Name/value</span></span>                                                                                                                                                    | <span data-ttu-id="c199b-116">Significado</span><span class="sxs-lookup"><span data-stu-id="c199b-116">Meaning</span></span>                                        |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------|
| <dl> <span data-ttu-id="c199b-117"><dt>S \_ OK</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="c199b-117"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                       | <span data-ttu-id="c199b-118">A operação foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="c199b-118">The operation was successful.</span></span><br/>       |
| <dl> <span data-ttu-id="c199b-119"><dt>E \_ </dt> <dt>0X80004003</dt> de ponteiro</span><span class="sxs-lookup"><span data-stu-id="c199b-119"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>         | <span data-ttu-id="c199b-120">O parâmetro é **NULL**.</span><span class="sxs-lookup"><span data-stu-id="c199b-120">The parameter is **NULL**.</span></span><br/>          |
| <dl> <span data-ttu-id="c199b-121"><dt>S \_ FALSO</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="c199b-121"><dt>S\_FALSE</dt> <dt>1</dt></span></span> </dl>                    | <span data-ttu-id="c199b-122">A máquina virtual não está em execução.</span><span class="sxs-lookup"><span data-stu-id="c199b-122">The virtual machine is not running.</span></span><br/> |
| <dl> <span data-ttu-id="c199b-123"><dt>DISP \_ E \_ </dt> <dt>0x80020009</dt> de exceção</span><span class="sxs-lookup"><span data-stu-id="c199b-123"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl> | <span data-ttu-id="c199b-124">Ocorreu um erro inesperado.</span><span class="sxs-lookup"><span data-stu-id="c199b-124">An unexpected error has occurred.</span></span><br/>   |



## <a name="requirements"></a><span data-ttu-id="c199b-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c199b-125">Requirements</span></span>



| <span data-ttu-id="c199b-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="c199b-126">Requirement</span></span> | <span data-ttu-id="c199b-127">Valor</span><span class="sxs-lookup"><span data-stu-id="c199b-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="c199b-128">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c199b-128">Minimum supported client</span></span><br/> | <span data-ttu-id="c199b-129">\[Somente aplicativos de área de trabalho do Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="c199b-129">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="c199b-130">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c199b-130">Minimum supported server</span></span><br/> | <span data-ttu-id="c199b-131">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="c199b-131">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="c199b-132">Fim do suporte do cliente</span><span class="sxs-lookup"><span data-stu-id="c199b-132">End of client support</span></span><br/>    | <span data-ttu-id="c199b-133">Windows 7</span><span class="sxs-lookup"><span data-stu-id="c199b-133">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="c199b-134">Produto</span><span class="sxs-lookup"><span data-stu-id="c199b-134">Product</span></span><br/>                  | <span data-ttu-id="c199b-135">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="c199b-135">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="c199b-136">parâmetro</span><span class="sxs-lookup"><span data-stu-id="c199b-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="c199b-137"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="c199b-137"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="c199b-138">IID</span><span class="sxs-lookup"><span data-stu-id="c199b-138">IID</span></span><br/>                      | <span data-ttu-id="c199b-139">IID \_ IVMAccountant é definido como 6376c067-7f57-4D63-b754-06e2e4f51d73</span><span class="sxs-lookup"><span data-stu-id="c199b-139">IID\_IVMAccountant is defined as 6376c067-7f57-4d63-b754-06e2e4f51d73</span></span><br/>              |



## <a name="see-also"></a><span data-ttu-id="c199b-140">Confira também</span><span class="sxs-lookup"><span data-stu-id="c199b-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c199b-141">**IVMAccountant**</span><span class="sxs-lookup"><span data-stu-id="c199b-141">**IVMAccountant**</span></span>](ivmaccountant.md)
</dt> </dl>

 

