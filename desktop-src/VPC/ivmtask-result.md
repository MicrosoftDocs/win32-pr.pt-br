---
title: Propriedade de resultado IVMTask (VPCCOMInterfaces. h)
description: Recupera o resultado da tarefa.
ms.assetid: 640279ef-94b8-4e8f-88f3-a97cec54c121
keywords:
- Propriedade de resultado Virtual PC
- Propriedade de resultado Virtual PC, interface IVMTask
- Virtual PC de interface IVMTask, propriedade de resultado
topic_type:
- apiref
api_name:
- IVMTask.Result
- IVMTask.get_Result
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1f4dc36d1529633a850bc10e5c89e8c07147aea8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918826"
---
# <a name="ivmtaskresult-property"></a><span data-ttu-id="a431b-106">Propriedade IVMTask:: Result</span><span class="sxs-lookup"><span data-stu-id="a431b-106">IVMTask::Result property</span></span>

<span data-ttu-id="a431b-107">\[O Windows Virtual PC não está mais disponível para uso a partir do Windows 8.</span><span class="sxs-lookup"><span data-stu-id="a431b-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="a431b-108">Em vez disso, use o [provedor WMI do Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="a431b-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="a431b-109">Recupera o resultado da tarefa.</span><span class="sxs-lookup"><span data-stu-id="a431b-109">Retrieves the result of the task.</span></span>

<span data-ttu-id="a431b-110">Esta propriedade é somente para leitura.</span><span class="sxs-lookup"><span data-stu-id="a431b-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="a431b-111">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="a431b-111">Syntax</span></span>


```C++
HRESULT get_Result(
  [out, retval] VMTaskResult *result
);
```



## <a name="property-value"></a><span data-ttu-id="a431b-112">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="a431b-112">Property value</span></span>

<span data-ttu-id="a431b-113">O resultado da tarefa.</span><span class="sxs-lookup"><span data-stu-id="a431b-113">The result of the task.</span></span> <span data-ttu-id="a431b-114">Para obter uma lista de valores, consulte [**VMTaskResult**](vmtaskresult.md).</span><span class="sxs-lookup"><span data-stu-id="a431b-114">For a list of values, see [**VMTaskResult**](vmtaskresult.md).</span></span>

## <a name="error-codes"></a><span data-ttu-id="a431b-115">Códigos do Erro</span><span class="sxs-lookup"><span data-stu-id="a431b-115">Error codes</span></span>



| <span data-ttu-id="a431b-116">Nome/valor</span><span class="sxs-lookup"><span data-stu-id="a431b-116">Name/value</span></span>                                                                                                                                                    | <span data-ttu-id="a431b-117">Significado</span><span class="sxs-lookup"><span data-stu-id="a431b-117">Meaning</span></span>                                      |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="a431b-118"><dt>S \_ OK</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="a431b-118"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                       | <span data-ttu-id="a431b-119">A operação foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="a431b-119">The operation was successful.</span></span><br/>     |
| <dl> <span data-ttu-id="a431b-120"><dt>E \_ </dt> <dt>0X80004003</dt> de ponteiro</span><span class="sxs-lookup"><span data-stu-id="a431b-120"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>         | <span data-ttu-id="a431b-121">O valor do parâmetro é **NULL**.</span><span class="sxs-lookup"><span data-stu-id="a431b-121">The parameter value is **NULL**.</span></span><br/>  |
| <dl> <span data-ttu-id="a431b-122"><dt>DISP \_ E \_ </dt> <dt>0x80020009</dt> de exceção</span><span class="sxs-lookup"><span data-stu-id="a431b-122"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl> | <span data-ttu-id="a431b-123">Ocorreu um erro inesperado.</span><span class="sxs-lookup"><span data-stu-id="a431b-123">An unexpected error has occurred.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="a431b-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a431b-124">Requirements</span></span>



| <span data-ttu-id="a431b-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="a431b-125">Requirement</span></span> | <span data-ttu-id="a431b-126">Valor</span><span class="sxs-lookup"><span data-stu-id="a431b-126">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="a431b-127">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a431b-127">Minimum supported client</span></span><br/> | <span data-ttu-id="a431b-128">\[Somente aplicativos de área de trabalho do Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="a431b-128">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="a431b-129">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a431b-129">Minimum supported server</span></span><br/> | <span data-ttu-id="a431b-130">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="a431b-130">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="a431b-131">Fim do suporte do cliente</span><span class="sxs-lookup"><span data-stu-id="a431b-131">End of client support</span></span><br/>    | <span data-ttu-id="a431b-132">Windows 7</span><span class="sxs-lookup"><span data-stu-id="a431b-132">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="a431b-133">Produto</span><span class="sxs-lookup"><span data-stu-id="a431b-133">Product</span></span><br/>                  | <span data-ttu-id="a431b-134">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="a431b-134">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="a431b-135">parâmetro</span><span class="sxs-lookup"><span data-stu-id="a431b-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="a431b-136"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="a431b-136"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="a431b-137">IID</span><span class="sxs-lookup"><span data-stu-id="a431b-137">IID</span></span><br/>                      | <span data-ttu-id="a431b-138">IID \_ IVMTask é definido como ab72b222-6e9c-48ae-aa54-85e3e635767c</span><span class="sxs-lookup"><span data-stu-id="a431b-138">IID\_IVMTask is defined as ab72b222-6e9c-48ae-aa54-85e3e635767c</span></span><br/>                    |



## <a name="see-also"></a><span data-ttu-id="a431b-139">Confira também</span><span class="sxs-lookup"><span data-stu-id="a431b-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a431b-140">**IVMTask**</span><span class="sxs-lookup"><span data-stu-id="a431b-140">**IVMTask**</span></span>](ivmtask.md)
</dt> </dl>

 

