---
title: Propriedade Count de IVMTaskCollection (VPCCOMInterfaces. h)
description: Recupera o número de tarefas nesta coleção.
ms.assetid: 5ff33bea-3f27-47ad-bcbc-6c40f2a8d78d
keywords:
- Propriedade de contagem Virtual PC
- Propriedade Count Virtual PC, interface IVMTaskCollection
- Virtual PC de interface IVMTaskCollection, Propriedade Count
topic_type:
- apiref
api_name:
- IVMTaskCollection.Count
- IVMTaskCollection.get_Count
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f5e868296437a8939b29947e785aabaff08fdcb3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103824596"
---
# <a name="ivmtaskcollectioncount-property"></a><span data-ttu-id="76907-106">Propriedade IVMTaskCollection:: Count</span><span class="sxs-lookup"><span data-stu-id="76907-106">IVMTaskCollection::Count property</span></span>

<span data-ttu-id="76907-107">\[O Windows Virtual PC não está mais disponível para uso a partir do Windows 8.</span><span class="sxs-lookup"><span data-stu-id="76907-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="76907-108">Em vez disso, use o [provedor WMI do Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="76907-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="76907-109">Recupera o número de tarefas nesta coleção.</span><span class="sxs-lookup"><span data-stu-id="76907-109">Retrieves the number of tasks in this collection.</span></span>

<span data-ttu-id="76907-110">Esta propriedade é somente para leitura.</span><span class="sxs-lookup"><span data-stu-id="76907-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="76907-111">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="76907-111">Syntax</span></span>


```C++
HRESULT get_Count(
  [out, retval] long *count
);
```



## <a name="property-value"></a><span data-ttu-id="76907-112">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="76907-112">Property value</span></span>

<span data-ttu-id="76907-113">O número de tarefas.</span><span class="sxs-lookup"><span data-stu-id="76907-113">The number of tasks.</span></span>

## <a name="error-codes"></a><span data-ttu-id="76907-114">Códigos do Erro</span><span class="sxs-lookup"><span data-stu-id="76907-114">Error codes</span></span>



| <span data-ttu-id="76907-115">Nome/valor</span><span class="sxs-lookup"><span data-stu-id="76907-115">Name/value</span></span>                                                                                                                                                    | <span data-ttu-id="76907-116">Significado</span><span class="sxs-lookup"><span data-stu-id="76907-116">Meaning</span></span>                                      |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="76907-117"><dt>S \_ OK</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="76907-117"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                       | <span data-ttu-id="76907-118">A operação foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="76907-118">The operation was successful.</span></span><br/>     |
| <dl> <span data-ttu-id="76907-119"><dt>E \_ </dt> <dt>0X80004003</dt> de ponteiro</span><span class="sxs-lookup"><span data-stu-id="76907-119"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>         | <span data-ttu-id="76907-120">O parâmetro é **NULL**.</span><span class="sxs-lookup"><span data-stu-id="76907-120">The parameter is **NULL**.</span></span><br/>        |
| <dl> <span data-ttu-id="76907-121"><dt>DISP \_ E \_ </dt> <dt>0x80020009</dt> de exceção</span><span class="sxs-lookup"><span data-stu-id="76907-121"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl> | <span data-ttu-id="76907-122">Ocorreu um erro inesperado.</span><span class="sxs-lookup"><span data-stu-id="76907-122">An unexpected error has occurred.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="76907-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="76907-123">Requirements</span></span>



| <span data-ttu-id="76907-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="76907-124">Requirement</span></span> | <span data-ttu-id="76907-125">Valor</span><span class="sxs-lookup"><span data-stu-id="76907-125">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="76907-126">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="76907-126">Minimum supported client</span></span><br/> | <span data-ttu-id="76907-127">\[Somente aplicativos de área de trabalho do Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="76907-127">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="76907-128">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="76907-128">Minimum supported server</span></span><br/> | <span data-ttu-id="76907-129">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="76907-129">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="76907-130">Fim do suporte do cliente</span><span class="sxs-lookup"><span data-stu-id="76907-130">End of client support</span></span><br/>    | <span data-ttu-id="76907-131">Windows 7</span><span class="sxs-lookup"><span data-stu-id="76907-131">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="76907-132">Produto</span><span class="sxs-lookup"><span data-stu-id="76907-132">Product</span></span><br/>                  | <span data-ttu-id="76907-133">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="76907-133">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="76907-134">parâmetro</span><span class="sxs-lookup"><span data-stu-id="76907-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="76907-135"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="76907-135"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="76907-136">IID</span><span class="sxs-lookup"><span data-stu-id="76907-136">IID</span></span><br/>                      | <span data-ttu-id="76907-137">IID \_ IVMTaskCollection é definido como 5c4387c8-0e8b-4b97-8058-84679adf4c40</span><span class="sxs-lookup"><span data-stu-id="76907-137">IID\_IVMTaskCollection is defined as 5c4387c8-0e8b-4b97-8058-84679adf4c40</span></span><br/>          |



## <a name="see-also"></a><span data-ttu-id="76907-138">Confira também</span><span class="sxs-lookup"><span data-stu-id="76907-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="76907-139">**IVMTaskCollection**</span><span class="sxs-lookup"><span data-stu-id="76907-139">**IVMTaskCollection**</span></span>](ivmtaskcollection.md)
</dt> </dl>

 

