---
title: Propriedade de ID IVMTask (VPCCOMInterfaces. h)
description: Recupera um identificador exclusivo para esta tarefa.
ms.assetid: 56a63b94-139b-4445-aef6-1b988e548b4b
keywords:
- Propriedade de ID Virtual PC
- Propriedade de ID Virtual PC, interface IVMTask
- IVMTask interface virtual PC, Propriedade ID
topic_type:
- apiref
api_name:
- IVMTask.ID
- IVMTask.get_ID
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 821650fcec725a43d86e539bd7f6cc9e7a6e2677
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103824694"
---
# <a name="ivmtaskid-property"></a><span data-ttu-id="3e66c-106">Propriedade IVMTask:: ID</span><span class="sxs-lookup"><span data-stu-id="3e66c-106">IVMTask::ID property</span></span>

<span data-ttu-id="3e66c-107">\[O Windows Virtual PC não está mais disponível para uso a partir do Windows 8.</span><span class="sxs-lookup"><span data-stu-id="3e66c-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="3e66c-108">Em vez disso, use o [provedor WMI do Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="3e66c-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="3e66c-109">Recupera um identificador exclusivo para esta tarefa.</span><span class="sxs-lookup"><span data-stu-id="3e66c-109">Retrieves a unique identifier for this task.</span></span>

<span data-ttu-id="3e66c-110">Esta propriedade é somente para leitura.</span><span class="sxs-lookup"><span data-stu-id="3e66c-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="3e66c-111">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="3e66c-111">Syntax</span></span>


```C++
HRESULT get_ID(
  [out, retval] long *ID
);
```



## <a name="property-value"></a><span data-ttu-id="3e66c-112">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="3e66c-112">Property value</span></span>

<span data-ttu-id="3e66c-113">O identificador exclusivo.</span><span class="sxs-lookup"><span data-stu-id="3e66c-113">The unique identifier.</span></span>

## <a name="error-codes"></a><span data-ttu-id="3e66c-114">Códigos do Erro</span><span class="sxs-lookup"><span data-stu-id="3e66c-114">Error codes</span></span>



| <span data-ttu-id="3e66c-115">Nome/valor</span><span class="sxs-lookup"><span data-stu-id="3e66c-115">Name/value</span></span>                                                                                                                                                    | <span data-ttu-id="3e66c-116">Significado</span><span class="sxs-lookup"><span data-stu-id="3e66c-116">Meaning</span></span>                                      |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="3e66c-117"><dt>S \_ OK</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="3e66c-117"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                       | <span data-ttu-id="3e66c-118">A operação foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="3e66c-118">The operation was successful.</span></span><br/>     |
| <dl> <span data-ttu-id="3e66c-119"><dt>E \_ </dt> <dt>0X80004003</dt> de ponteiro</span><span class="sxs-lookup"><span data-stu-id="3e66c-119"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>         | <span data-ttu-id="3e66c-120">O valor do parâmetro é **NULL**.</span><span class="sxs-lookup"><span data-stu-id="3e66c-120">The parameter value is **NULL**.</span></span><br/>  |
| <dl> <span data-ttu-id="3e66c-121"><dt>DISP \_ E \_ </dt> <dt>0x80020009</dt> de exceção</span><span class="sxs-lookup"><span data-stu-id="3e66c-121"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl> | <span data-ttu-id="3e66c-122">Ocorreu um erro inesperado.</span><span class="sxs-lookup"><span data-stu-id="3e66c-122">An unexpected error has occurred.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="3e66c-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3e66c-123">Requirements</span></span>



| <span data-ttu-id="3e66c-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="3e66c-124">Requirement</span></span> | <span data-ttu-id="3e66c-125">Valor</span><span class="sxs-lookup"><span data-stu-id="3e66c-125">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="3e66c-126">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3e66c-126">Minimum supported client</span></span><br/> | <span data-ttu-id="3e66c-127">\[Somente aplicativos de área de trabalho do Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="3e66c-127">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="3e66c-128">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3e66c-128">Minimum supported server</span></span><br/> | <span data-ttu-id="3e66c-129">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="3e66c-129">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="3e66c-130">Fim do suporte do cliente</span><span class="sxs-lookup"><span data-stu-id="3e66c-130">End of client support</span></span><br/>    | <span data-ttu-id="3e66c-131">Windows 7</span><span class="sxs-lookup"><span data-stu-id="3e66c-131">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="3e66c-132">Produto</span><span class="sxs-lookup"><span data-stu-id="3e66c-132">Product</span></span><br/>                  | <span data-ttu-id="3e66c-133">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="3e66c-133">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="3e66c-134">parâmetro</span><span class="sxs-lookup"><span data-stu-id="3e66c-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="3e66c-135"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="3e66c-135"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="3e66c-136">IID</span><span class="sxs-lookup"><span data-stu-id="3e66c-136">IID</span></span><br/>                      | <span data-ttu-id="3e66c-137">IID \_ IVMTask é definido como ab72b222-6e9c-48ae-aa54-85e3e635767c</span><span class="sxs-lookup"><span data-stu-id="3e66c-137">IID\_IVMTask is defined as ab72b222-6e9c-48ae-aa54-85e3e635767c</span></span><br/>                    |



## <a name="see-also"></a><span data-ttu-id="3e66c-138">Confira também</span><span class="sxs-lookup"><span data-stu-id="3e66c-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3e66c-139">**IVMTask**</span><span class="sxs-lookup"><span data-stu-id="3e66c-139">**IVMTask**</span></span>](ivmtask.md)
</dt> </dl>

 

