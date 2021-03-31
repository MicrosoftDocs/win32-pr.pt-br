---
title: Propriedade IVMTask PercentCompleted (VPCCOMInterfaces. h)
description: Recupera o percentual de conclusão da tarefa.
ms.assetid: 23ba9696-06ed-44ec-a1ec-ef3bf9122c6f
keywords:
- Propriedade PercentCompleted Virtual PC
- Propriedade PercentCompleted Virtual PC, interface IVMTask
- IVMTask interface virtual PC, Propriedade PercentCompleted
topic_type:
- apiref
api_name:
- IVMTask.PercentCompleted
- IVMTask.get_PercentCompleted
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fa820adbbde2fc68632da27a9b146bd0e8f40143
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103645048"
---
# <a name="ivmtaskpercentcompleted-property"></a><span data-ttu-id="e0632-106">IVMTask: Propriedade ercentCompleted de:P</span><span class="sxs-lookup"><span data-stu-id="e0632-106">IVMTask::PercentCompleted property</span></span>

<span data-ttu-id="e0632-107">\[O Windows Virtual PC não está mais disponível para uso a partir do Windows 8.</span><span class="sxs-lookup"><span data-stu-id="e0632-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="e0632-108">Em vez disso, use o [provedor WMI do Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="e0632-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="e0632-109">Recupera o percentual de conclusão da tarefa.</span><span class="sxs-lookup"><span data-stu-id="e0632-109">Retrieves the completion percentage of the task.</span></span>

<span data-ttu-id="e0632-110">Esta propriedade é somente para leitura.</span><span class="sxs-lookup"><span data-stu-id="e0632-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="e0632-111">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="e0632-111">Syntax</span></span>


```C++
HRESULT get_PercentCompleted(
  [out, retval] long *percentCompleted
);
```



## <a name="property-value"></a><span data-ttu-id="e0632-112">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="e0632-112">Property value</span></span>

<span data-ttu-id="e0632-113">A porcentagem de conclusão atual.</span><span class="sxs-lookup"><span data-stu-id="e0632-113">The current completion percentage.</span></span> <span data-ttu-id="e0632-114">O valor é um número entre 0 e 100.</span><span class="sxs-lookup"><span data-stu-id="e0632-114">The value is a number between 0 and 100.</span></span>

## <a name="error-codes"></a><span data-ttu-id="e0632-115">Códigos do Erro</span><span class="sxs-lookup"><span data-stu-id="e0632-115">Error codes</span></span>



| <span data-ttu-id="e0632-116">Nome/valor</span><span class="sxs-lookup"><span data-stu-id="e0632-116">Name/value</span></span>                                                                                                                                                    | <span data-ttu-id="e0632-117">Significado</span><span class="sxs-lookup"><span data-stu-id="e0632-117">Meaning</span></span>                                      |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="e0632-118"><dt>S \_ OK</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="e0632-118"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                       | <span data-ttu-id="e0632-119">A operação foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="e0632-119">The operation was successful.</span></span><br/>     |
| <dl> <span data-ttu-id="e0632-120"><dt>E \_ </dt> <dt>0X80004003</dt> de ponteiro</span><span class="sxs-lookup"><span data-stu-id="e0632-120"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>         | <span data-ttu-id="e0632-121">O valor do parâmetro é **NULL**.</span><span class="sxs-lookup"><span data-stu-id="e0632-121">The parameter value is **NULL**.</span></span><br/>  |
| <dl> <span data-ttu-id="e0632-122"><dt>DISP \_ E \_ </dt> <dt>0x80020009</dt> de exceção</span><span class="sxs-lookup"><span data-stu-id="e0632-122"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl> | <span data-ttu-id="e0632-123">Ocorreu um erro inesperado.</span><span class="sxs-lookup"><span data-stu-id="e0632-123">An unexpected error has occurred.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="e0632-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e0632-124">Requirements</span></span>



| <span data-ttu-id="e0632-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="e0632-125">Requirement</span></span> | <span data-ttu-id="e0632-126">Valor</span><span class="sxs-lookup"><span data-stu-id="e0632-126">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="e0632-127">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e0632-127">Minimum supported client</span></span><br/> | <span data-ttu-id="e0632-128">\[Somente aplicativos de área de trabalho do Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="e0632-128">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="e0632-129">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e0632-129">Minimum supported server</span></span><br/> | <span data-ttu-id="e0632-130">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="e0632-130">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="e0632-131">Fim do suporte do cliente</span><span class="sxs-lookup"><span data-stu-id="e0632-131">End of client support</span></span><br/>    | <span data-ttu-id="e0632-132">Windows 7</span><span class="sxs-lookup"><span data-stu-id="e0632-132">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="e0632-133">Produto</span><span class="sxs-lookup"><span data-stu-id="e0632-133">Product</span></span><br/>                  | <span data-ttu-id="e0632-134">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="e0632-134">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="e0632-135">parâmetro</span><span class="sxs-lookup"><span data-stu-id="e0632-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="e0632-136"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="e0632-136"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="e0632-137">IID</span><span class="sxs-lookup"><span data-stu-id="e0632-137">IID</span></span><br/>                      | <span data-ttu-id="e0632-138">IID \_ IVMTask é definido como ab72b222-6e9c-48ae-aa54-85e3e635767c</span><span class="sxs-lookup"><span data-stu-id="e0632-138">IID\_IVMTask is defined as ab72b222-6e9c-48ae-aa54-85e3e635767c</span></span><br/>                    |



## <a name="see-also"></a><span data-ttu-id="e0632-139">Consulte também</span><span class="sxs-lookup"><span data-stu-id="e0632-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e0632-140">**IVMTask**</span><span class="sxs-lookup"><span data-stu-id="e0632-140">**IVMTask**</span></span>](ivmtask.md)
</dt> </dl>

 

