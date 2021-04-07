---
title: Propriedade IsComplete IVMTask (VPCCOMInterfaces. h)
description: Determina se a tarefa foi concluída.
ms.assetid: 181fa220-4de2-4ab3-950b-fffc4fe4de64
keywords:
- Propriedade IsComplete Virtual PC
- Propriedade IsComplete Virtual PC, interface IVMTask
- IVMTask interface virtual PC, IsComplete Property
topic_type:
- apiref
api_name:
- IVMTask.IsComplete
- IVMTask.get_IsComplete
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4bbf046b4a16ef4e907f1fec0126d08815ca2955
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918573"
---
# <a name="ivmtaskiscomplete-property"></a><span data-ttu-id="7cccd-106">Propriedade IVMTask:: IsComplete</span><span class="sxs-lookup"><span data-stu-id="7cccd-106">IVMTask::IsComplete property</span></span>

<span data-ttu-id="7cccd-107">\[O Windows Virtual PC não está mais disponível para uso a partir do Windows 8.</span><span class="sxs-lookup"><span data-stu-id="7cccd-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="7cccd-108">Em vez disso, use o [provedor WMI do Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="7cccd-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="7cccd-109">Determina se a tarefa foi concluída.</span><span class="sxs-lookup"><span data-stu-id="7cccd-109">Determines whether the task has completed.</span></span>

<span data-ttu-id="7cccd-110">Esta propriedade é somente para leitura.</span><span class="sxs-lookup"><span data-stu-id="7cccd-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="7cccd-111">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="7cccd-111">Syntax</span></span>


```C++
HRESULT get_IsComplete(
  [out, retval] VARIANT_BOOL *isComplete
);
```



## <a name="property-value"></a><span data-ttu-id="7cccd-112">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="7cccd-112">Property value</span></span>

<span data-ttu-id="7cccd-113">**True** se a tarefa for concluída e **false** caso contrário.</span><span class="sxs-lookup"><span data-stu-id="7cccd-113">**TRUE** if the task has completed and **FALSE** otherwise.</span></span>

## <a name="error-codes"></a><span data-ttu-id="7cccd-114">Códigos do Erro</span><span class="sxs-lookup"><span data-stu-id="7cccd-114">Error codes</span></span>



| <span data-ttu-id="7cccd-115">Nome/valor</span><span class="sxs-lookup"><span data-stu-id="7cccd-115">Name/value</span></span>                                                                                                                                                    | <span data-ttu-id="7cccd-116">Significado</span><span class="sxs-lookup"><span data-stu-id="7cccd-116">Meaning</span></span>                                      |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="7cccd-117"><dt>S \_ OK</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="7cccd-117"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                       | <span data-ttu-id="7cccd-118">A operação foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="7cccd-118">The operation was successful.</span></span><br/>     |
| <dl> <span data-ttu-id="7cccd-119"><dt>E \_ </dt> <dt>0X80004003</dt> de ponteiro</span><span class="sxs-lookup"><span data-stu-id="7cccd-119"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>         | <span data-ttu-id="7cccd-120">O valor do parâmetro é **NULL**.</span><span class="sxs-lookup"><span data-stu-id="7cccd-120">The parameter value is **NULL**.</span></span><br/>  |
| <dl> <span data-ttu-id="7cccd-121"><dt>DISP \_ E \_ </dt> <dt>0x80020009</dt> de exceção</span><span class="sxs-lookup"><span data-stu-id="7cccd-121"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl> | <span data-ttu-id="7cccd-122">Ocorreu um erro inesperado.</span><span class="sxs-lookup"><span data-stu-id="7cccd-122">An unexpected error has occurred.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="7cccd-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7cccd-123">Requirements</span></span>



| <span data-ttu-id="7cccd-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="7cccd-124">Requirement</span></span> | <span data-ttu-id="7cccd-125">Valor</span><span class="sxs-lookup"><span data-stu-id="7cccd-125">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="7cccd-126">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="7cccd-126">Minimum supported client</span></span><br/> | <span data-ttu-id="7cccd-127">\[Somente aplicativos de área de trabalho do Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="7cccd-127">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="7cccd-128">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="7cccd-128">Minimum supported server</span></span><br/> | <span data-ttu-id="7cccd-129">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="7cccd-129">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="7cccd-130">Fim do suporte do cliente</span><span class="sxs-lookup"><span data-stu-id="7cccd-130">End of client support</span></span><br/>    | <span data-ttu-id="7cccd-131">Windows 7</span><span class="sxs-lookup"><span data-stu-id="7cccd-131">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="7cccd-132">Produto</span><span class="sxs-lookup"><span data-stu-id="7cccd-132">Product</span></span><br/>                  | <span data-ttu-id="7cccd-133">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="7cccd-133">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="7cccd-134">parâmetro</span><span class="sxs-lookup"><span data-stu-id="7cccd-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="7cccd-135"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="7cccd-135"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="7cccd-136">IID</span><span class="sxs-lookup"><span data-stu-id="7cccd-136">IID</span></span><br/>                      | <span data-ttu-id="7cccd-137">IID \_ IVMTask é definido como ab72b222-6e9c-48ae-aa54-85e3e635767c</span><span class="sxs-lookup"><span data-stu-id="7cccd-137">IID\_IVMTask is defined as ab72b222-6e9c-48ae-aa54-85e3e635767c</span></span><br/>                    |



## <a name="see-also"></a><span data-ttu-id="7cccd-138">Confira também</span><span class="sxs-lookup"><span data-stu-id="7cccd-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7cccd-139">**IVMTask**</span><span class="sxs-lookup"><span data-stu-id="7cccd-139">**IVMTask**</span></span>](ivmtask.md)
</dt> </dl>

 

