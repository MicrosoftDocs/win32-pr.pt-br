---
title: Propriedade Count de IVMParallelPortCollection (VPCCOMInterfaces. h)
description: Número de portas paralelas nesta coleção.
ms.assetid: f2f4cac4-bb63-4ac2-ba6e-321a8a29c6d4
keywords:
- Propriedade de contagem Virtual PC
- Propriedade Count Virtual PC, interface IVMParallelPortCollection
- Virtual PC de interface IVMParallelPortCollection, Propriedade Count
topic_type:
- apiref
api_name:
- IVMParallelPortCollection.Count
- IVMParallelPortCollection.get_Count
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a0bb1af40f0e4d15b7eae65e18a8d9910deb769c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918541"
---
# <a name="ivmparallelportcollectioncount-property"></a><span data-ttu-id="79b08-106">Propriedade IVMParallelPortCollection:: Count</span><span class="sxs-lookup"><span data-stu-id="79b08-106">IVMParallelPortCollection::Count property</span></span>

<span data-ttu-id="79b08-107">\[O Windows Virtual PC não está mais disponível para uso a partir do Windows 8.</span><span class="sxs-lookup"><span data-stu-id="79b08-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="79b08-108">Em vez disso, use o [provedor WMI do Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="79b08-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="79b08-109">Recupera o número de portas paralelas nesta coleção.</span><span class="sxs-lookup"><span data-stu-id="79b08-109">Retrieves the number of parallel ports in this collection.</span></span>

<span data-ttu-id="79b08-110">Esta propriedade é somente para leitura.</span><span class="sxs-lookup"><span data-stu-id="79b08-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="79b08-111">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="79b08-111">Syntax</span></span>


```C++
HRESULT get_Count(
  [out, retval] long *count
);
```



## <a name="property-value"></a><span data-ttu-id="79b08-112">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="79b08-112">Property value</span></span>

<span data-ttu-id="79b08-113">O número de portas paralelas.</span><span class="sxs-lookup"><span data-stu-id="79b08-113">The number of parallel ports.</span></span>

## <a name="error-codes"></a><span data-ttu-id="79b08-114">Códigos do Erro</span><span class="sxs-lookup"><span data-stu-id="79b08-114">Error codes</span></span>



| <span data-ttu-id="79b08-115">Nome/valor</span><span class="sxs-lookup"><span data-stu-id="79b08-115">Name/value</span></span>                                                                                                                                            | <span data-ttu-id="79b08-116">Significado</span><span class="sxs-lookup"><span data-stu-id="79b08-116">Meaning</span></span>                                  |
|-------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------|
| <dl> <span data-ttu-id="79b08-117"><dt>S \_ OK</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="79b08-117"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>               | <span data-ttu-id="79b08-118">A operação foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="79b08-118">The operation was successful.</span></span><br/> |
| <dl> <span data-ttu-id="79b08-119"><dt>E \_ </dt> <dt>0X80004003</dt> de ponteiro</span><span class="sxs-lookup"><span data-stu-id="79b08-119"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl> | <span data-ttu-id="79b08-120">O parâmetro é **NULL**.</span><span class="sxs-lookup"><span data-stu-id="79b08-120">The parameter is **NULL**.</span></span><br/>    |



## <a name="requirements"></a><span data-ttu-id="79b08-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="79b08-121">Requirements</span></span>



| <span data-ttu-id="79b08-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="79b08-122">Requirement</span></span> | <span data-ttu-id="79b08-123">Valor</span><span class="sxs-lookup"><span data-stu-id="79b08-123">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="79b08-124">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="79b08-124">Minimum supported client</span></span><br/> | <span data-ttu-id="79b08-125">\[Somente aplicativos de área de trabalho do Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="79b08-125">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="79b08-126">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="79b08-126">Minimum supported server</span></span><br/> | <span data-ttu-id="79b08-127">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="79b08-127">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="79b08-128">Fim do suporte do cliente</span><span class="sxs-lookup"><span data-stu-id="79b08-128">End of client support</span></span><br/>    | <span data-ttu-id="79b08-129">Windows 7</span><span class="sxs-lookup"><span data-stu-id="79b08-129">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="79b08-130">Produto</span><span class="sxs-lookup"><span data-stu-id="79b08-130">Product</span></span><br/>                  | <span data-ttu-id="79b08-131">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="79b08-131">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="79b08-132">parâmetro</span><span class="sxs-lookup"><span data-stu-id="79b08-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="79b08-133"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="79b08-133"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="79b08-134">IID</span><span class="sxs-lookup"><span data-stu-id="79b08-134">IID</span></span><br/>                      | <span data-ttu-id="79b08-135">IID \_ IVMParallelPortCollection é definido como 27c3e036-198f-430c-8735-6e652f7203fd</span><span class="sxs-lookup"><span data-stu-id="79b08-135">IID\_IVMParallelPortCollection is defined as 27c3e036-198f-430c-8735-6e652f7203fd</span></span><br/>  |



## <a name="see-also"></a><span data-ttu-id="79b08-136">Confira também</span><span class="sxs-lookup"><span data-stu-id="79b08-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="79b08-137">**IVMParallelPortCollection**</span><span class="sxs-lookup"><span data-stu-id="79b08-137">**IVMParallelPortCollection**</span></span>](ivmparallelportcollection.md)
</dt> </dl>

 

