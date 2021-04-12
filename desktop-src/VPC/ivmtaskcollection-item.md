---
title: Propriedade de item IVMTaskCollection (VPCCOMInterfaces. h)
description: Recupera o objeto de tarefa que corresponde ao índice especificado.
ms.assetid: e4738b7a-12d6-4aed-992d-2f70c5cdd4d0
keywords:
- Propriedade do item Virtual PC
- Propriedade de item Virtual PC, interface IVMTaskCollection
- IVMTaskCollection interface virtual PC, Propriedade Item
topic_type:
- apiref
api_name:
- IVMTaskCollection.Item
- IVMTaskCollection.get_Item
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f445280834383ee594fbb53a3390c91b1928f4ad
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104499577"
---
# <a name="ivmtaskcollectionitem-property"></a><span data-ttu-id="7e8b4-106">Propriedade IVMTaskCollection:: item</span><span class="sxs-lookup"><span data-stu-id="7e8b4-106">IVMTaskCollection::Item property</span></span>

<span data-ttu-id="7e8b4-107">\[O Windows Virtual PC não está mais disponível para uso a partir do Windows 8.</span><span class="sxs-lookup"><span data-stu-id="7e8b4-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="7e8b4-108">Em vez disso, use o [provedor WMI do Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="7e8b4-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="7e8b4-109">Recupera o objeto de tarefa que corresponde ao índice especificado.</span><span class="sxs-lookup"><span data-stu-id="7e8b4-109">Retrieves the task object that corresponds to the specified index.</span></span>

<span data-ttu-id="7e8b4-110">Esta propriedade é somente para leitura.</span><span class="sxs-lookup"><span data-stu-id="7e8b4-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="7e8b4-111">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="7e8b4-111">Syntax</span></span>


```C++
HRESULT get_Item(
  [in]          long    index,
  [out, retval] IVMTask **task
);
```



## <a name="property-value"></a><span data-ttu-id="7e8b4-112">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="7e8b4-112">Property value</span></span>

<span data-ttu-id="7e8b4-113">O objeto [**IVMTask**](ivmtask.md) .</span><span class="sxs-lookup"><span data-stu-id="7e8b4-113">The [**IVMTask**](ivmtask.md) object.</span></span>

## <a name="error-codes"></a><span data-ttu-id="7e8b4-114">Códigos do Erro</span><span class="sxs-lookup"><span data-stu-id="7e8b4-114">Error codes</span></span>



| <span data-ttu-id="7e8b4-115">Nome/valor</span><span class="sxs-lookup"><span data-stu-id="7e8b4-115">Name/value</span></span>                                                                                                                                                    | <span data-ttu-id="7e8b4-116">Significado</span><span class="sxs-lookup"><span data-stu-id="7e8b4-116">Meaning</span></span>                                                                                        |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="7e8b4-117"><dt>S \_ OK</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="7e8b4-117"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                       | <span data-ttu-id="7e8b4-118">A operação foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="7e8b4-118">The operation was successful.</span></span> <br/>                                                      |
| <dl> <span data-ttu-id="7e8b4-119"><dt>E \_ </dt> <dt>0X80004003</dt> de ponteiro</span><span class="sxs-lookup"><span data-stu-id="7e8b4-119"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>         | <span data-ttu-id="7e8b4-120">O parâmetro de *tarefa* é **nulo**.</span><span class="sxs-lookup"><span data-stu-id="7e8b4-120">The *task* parameter is **NULL**.</span></span> <br/>                                                  |
| <dl> <span data-ttu-id="7e8b4-121"><dt>DISP \_ E \_ BADINDEX</dt> <dt>0x8002000B</dt></span><span class="sxs-lookup"><span data-stu-id="7e8b4-121"><dt>DISP\_E\_BADINDEX</dt> <dt>0x8002000B</dt></span></span> </dl>  | <span data-ttu-id="7e8b4-122">O índice do item solicitado não corresponde a um item nesta coleção.</span><span class="sxs-lookup"><span data-stu-id="7e8b4-122">The index of the requested item does not correspond to an item in this collection.</span></span> <br/> |
| <dl> <span data-ttu-id="7e8b4-123"><dt>DISP \_ E \_ </dt> <dt>0x80020009</dt> de exceção</span><span class="sxs-lookup"><span data-stu-id="7e8b4-123"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl> | <span data-ttu-id="7e8b4-124">Ocorreu um erro inesperado.</span><span class="sxs-lookup"><span data-stu-id="7e8b4-124">An unexpected error has occurred.</span></span><br/>                                                   |



## <a name="requirements"></a><span data-ttu-id="7e8b4-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7e8b4-125">Requirements</span></span>



| <span data-ttu-id="7e8b4-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="7e8b4-126">Requirement</span></span> | <span data-ttu-id="7e8b4-127">Valor</span><span class="sxs-lookup"><span data-stu-id="7e8b4-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="7e8b4-128">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="7e8b4-128">Minimum supported client</span></span><br/> | <span data-ttu-id="7e8b4-129">\[Somente aplicativos de área de trabalho do Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="7e8b4-129">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="7e8b4-130">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="7e8b4-130">Minimum supported server</span></span><br/> | <span data-ttu-id="7e8b4-131">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="7e8b4-131">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="7e8b4-132">Fim do suporte do cliente</span><span class="sxs-lookup"><span data-stu-id="7e8b4-132">End of client support</span></span><br/>    | <span data-ttu-id="7e8b4-133">Windows 7</span><span class="sxs-lookup"><span data-stu-id="7e8b4-133">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="7e8b4-134">Produto</span><span class="sxs-lookup"><span data-stu-id="7e8b4-134">Product</span></span><br/>                  | <span data-ttu-id="7e8b4-135">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="7e8b4-135">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="7e8b4-136">parâmetro</span><span class="sxs-lookup"><span data-stu-id="7e8b4-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="7e8b4-137"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="7e8b4-137"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="7e8b4-138">IID</span><span class="sxs-lookup"><span data-stu-id="7e8b4-138">IID</span></span><br/>                      | <span data-ttu-id="7e8b4-139">IID \_ IVMTaskCollection é definido como 5c4387c8-0e8b-4b97-8058-84679adf4c40</span><span class="sxs-lookup"><span data-stu-id="7e8b4-139">IID\_IVMTaskCollection is defined as 5c4387c8-0e8b-4b97-8058-84679adf4c40</span></span><br/>          |



## <a name="see-also"></a><span data-ttu-id="7e8b4-140">Confira também</span><span class="sxs-lookup"><span data-stu-id="7e8b4-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7e8b4-141">**IVMTask**</span><span class="sxs-lookup"><span data-stu-id="7e8b4-141">**IVMTask**</span></span>](ivmtask.md)
</dt> <dt>

[<span data-ttu-id="7e8b4-142">**IVMTaskCollection**</span><span class="sxs-lookup"><span data-stu-id="7e8b4-142">**IVMTaskCollection**</span></span>](ivmtaskcollection.md)
</dt> </dl>

 

