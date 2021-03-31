---
title: Propriedade IVMTask ErrorDescription (VPCCOMInterfaces. h)
description: Recupera a descrição de erro localizada registrada para esta tarefa.
ms.assetid: 85728775-14b6-4031-9ccd-4c4f8c410705
keywords:
- Propriedade ErrorDescription Virtual PC
- Propriedade ErrorDescription Virtual PC, interface IVMTask
- IVMTask interface virtual PC, Propriedade ErrorDescription
topic_type:
- apiref
api_name:
- IVMTask.ErrorDescription
- IVMTask.get_ErrorDescription
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9d5c95eac383d8e071832fdbf7843c01345278c4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103645049"
---
# <a name="ivmtaskerrordescription-property"></a><span data-ttu-id="344b2-106">Propriedade IVMTask:: ErrorDescription</span><span class="sxs-lookup"><span data-stu-id="344b2-106">IVMTask::ErrorDescription property</span></span>

<span data-ttu-id="344b2-107">\[O Windows Virtual PC não está mais disponível para uso a partir do Windows 8.</span><span class="sxs-lookup"><span data-stu-id="344b2-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="344b2-108">Em vez disso, use o [provedor WMI do Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="344b2-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="344b2-109">Recupera a descrição de erro localizada registrada para esta tarefa.</span><span class="sxs-lookup"><span data-stu-id="344b2-109">Retrieves the localized error description recorded for this task.</span></span>

<span data-ttu-id="344b2-110">Esta propriedade é somente para leitura.</span><span class="sxs-lookup"><span data-stu-id="344b2-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="344b2-111">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="344b2-111">Syntax</span></span>


```C++
HRESULT get_ErrorDescription(
  [out, retval] BSTR *outErrorDesc
);
```



## <a name="property-value"></a><span data-ttu-id="344b2-112">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="344b2-112">Property value</span></span>

<span data-ttu-id="344b2-113">A descrição do erro.</span><span class="sxs-lookup"><span data-stu-id="344b2-113">The error description.</span></span>

## <a name="error-codes"></a><span data-ttu-id="344b2-114">Códigos do Erro</span><span class="sxs-lookup"><span data-stu-id="344b2-114">Error codes</span></span>



| <span data-ttu-id="344b2-115">Nome/valor</span><span class="sxs-lookup"><span data-stu-id="344b2-115">Name/value</span></span>                                                                                                                                                    | <span data-ttu-id="344b2-116">Significado</span><span class="sxs-lookup"><span data-stu-id="344b2-116">Meaning</span></span>                                      |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="344b2-117"><dt>S \_ OK</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="344b2-117"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                       | <span data-ttu-id="344b2-118">A operação foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="344b2-118">The operation was successful.</span></span><br/>     |
| <dl> <span data-ttu-id="344b2-119"><dt>E \_ </dt> <dt>0X80004003</dt> de ponteiro</span><span class="sxs-lookup"><span data-stu-id="344b2-119"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>         | <span data-ttu-id="344b2-120">O valor do parâmetro é **NULL**.</span><span class="sxs-lookup"><span data-stu-id="344b2-120">The parameter value is **NULL**.</span></span><br/>  |
| <dl> <span data-ttu-id="344b2-121"><dt>DISP \_ E \_ </dt> <dt>0x80020009</dt> de exceção</span><span class="sxs-lookup"><span data-stu-id="344b2-121"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl> | <span data-ttu-id="344b2-122">Ocorreu um erro inesperado.</span><span class="sxs-lookup"><span data-stu-id="344b2-122">An unexpected error has occurred.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="344b2-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="344b2-123">Requirements</span></span>



| <span data-ttu-id="344b2-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="344b2-124">Requirement</span></span> | <span data-ttu-id="344b2-125">Valor</span><span class="sxs-lookup"><span data-stu-id="344b2-125">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="344b2-126">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="344b2-126">Minimum supported client</span></span><br/> | <span data-ttu-id="344b2-127">\[Somente aplicativos de área de trabalho do Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="344b2-127">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="344b2-128">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="344b2-128">Minimum supported server</span></span><br/> | <span data-ttu-id="344b2-129">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="344b2-129">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="344b2-130">Fim do suporte do cliente</span><span class="sxs-lookup"><span data-stu-id="344b2-130">End of client support</span></span><br/>    | <span data-ttu-id="344b2-131">Windows 7</span><span class="sxs-lookup"><span data-stu-id="344b2-131">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="344b2-132">Produto</span><span class="sxs-lookup"><span data-stu-id="344b2-132">Product</span></span><br/>                  | <span data-ttu-id="344b2-133">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="344b2-133">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="344b2-134">parâmetro</span><span class="sxs-lookup"><span data-stu-id="344b2-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="344b2-135"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="344b2-135"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="344b2-136">IID</span><span class="sxs-lookup"><span data-stu-id="344b2-136">IID</span></span><br/>                      | <span data-ttu-id="344b2-137">IID \_ IVMTask é definido como ab72b222-6e9c-48ae-aa54-85e3e635767c</span><span class="sxs-lookup"><span data-stu-id="344b2-137">IID\_IVMTask is defined as ab72b222-6e9c-48ae-aa54-85e3e635767c</span></span><br/>                    |



## <a name="see-also"></a><span data-ttu-id="344b2-138">Consulte também</span><span class="sxs-lookup"><span data-stu-id="344b2-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="344b2-139">**IVMTask**</span><span class="sxs-lookup"><span data-stu-id="344b2-139">**IVMTask**</span></span>](ivmtask.md)
</dt> </dl>

 

