---
title: Propriedade Count de IVMVirtualNetworkCollection (VPCCOMInterfaces. h)
description: Recupera o número de redes virtuais nesta coleção.
ms.assetid: a9a3ab48-74a0-498e-936e-a99c7b027a85
keywords:
- Propriedade de contagem Virtual PC
- Propriedade Count Virtual PC, interface IVMVirtualNetworkCollection
- Virtual PC de interface IVMVirtualNetworkCollection, Propriedade Count
topic_type:
- apiref
api_name:
- IVMVirtualNetworkCollection.Count
- IVMVirtualNetworkCollection.get_Count
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 82e3244327d5840c8f7cce8ed498f90cd406d573
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103644958"
---
# <a name="ivmvirtualnetworkcollectioncount-property"></a><span data-ttu-id="5b5b6-106">Propriedade IVMVirtualNetworkCollection:: Count</span><span class="sxs-lookup"><span data-stu-id="5b5b6-106">IVMVirtualNetworkCollection::Count property</span></span>

<span data-ttu-id="5b5b6-107">\[O Windows Virtual PC não está mais disponível para uso a partir do Windows 8.</span><span class="sxs-lookup"><span data-stu-id="5b5b6-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="5b5b6-108">Em vez disso, use o [provedor WMI do Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="5b5b6-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="5b5b6-109">Recupera o número de redes virtuais nesta coleção.</span><span class="sxs-lookup"><span data-stu-id="5b5b6-109">Retrieves the number of virtual networks in this collection.</span></span>

<span data-ttu-id="5b5b6-110">Esta propriedade é somente para leitura.</span><span class="sxs-lookup"><span data-stu-id="5b5b6-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="5b5b6-111">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="5b5b6-111">Syntax</span></span>


```C++
HRESULT get_Count(
  [out, retval] long *count
);
```



## <a name="property-value"></a><span data-ttu-id="5b5b6-112">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="5b5b6-112">Property value</span></span>

<span data-ttu-id="5b5b6-113">O número de redes virtuais.</span><span class="sxs-lookup"><span data-stu-id="5b5b6-113">The number of virtual networks.</span></span>

## <a name="error-codes"></a><span data-ttu-id="5b5b6-114">Códigos do Erro</span><span class="sxs-lookup"><span data-stu-id="5b5b6-114">Error codes</span></span>



| <span data-ttu-id="5b5b6-115">Nome/valor</span><span class="sxs-lookup"><span data-stu-id="5b5b6-115">Name/value</span></span>                                                                                                                                                    | <span data-ttu-id="5b5b6-116">Significado</span><span class="sxs-lookup"><span data-stu-id="5b5b6-116">Meaning</span></span>                                      |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="5b5b6-117"><dt>S \_ OK</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="5b5b6-117"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                       | <span data-ttu-id="5b5b6-118">A operação foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="5b5b6-118">The operation was successful.</span></span><br/>     |
| <dl> <span data-ttu-id="5b5b6-119"><dt>E \_ </dt> <dt>0X80004003</dt> de ponteiro</span><span class="sxs-lookup"><span data-stu-id="5b5b6-119"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>         | <span data-ttu-id="5b5b6-120">O parâmetro é **NULL**.</span><span class="sxs-lookup"><span data-stu-id="5b5b6-120">The parameter is **NULL**.</span></span><br/>        |
| <dl> <span data-ttu-id="5b5b6-121"><dt>DISP \_ E \_ </dt> <dt>0x80020009</dt> de exceção</span><span class="sxs-lookup"><span data-stu-id="5b5b6-121"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl> | <span data-ttu-id="5b5b6-122">Ocorreu um erro inesperado.</span><span class="sxs-lookup"><span data-stu-id="5b5b6-122">An unexpected error has occurred.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="5b5b6-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5b5b6-123">Requirements</span></span>



| <span data-ttu-id="5b5b6-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="5b5b6-124">Requirement</span></span> | <span data-ttu-id="5b5b6-125">Valor</span><span class="sxs-lookup"><span data-stu-id="5b5b6-125">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5b5b6-126">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="5b5b6-126">Minimum supported client</span></span><br/> | <span data-ttu-id="5b5b6-127">\[Somente aplicativos de área de trabalho do Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="5b5b6-127">Windows 7 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="5b5b6-128">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="5b5b6-128">Minimum supported server</span></span><br/> | <span data-ttu-id="5b5b6-129">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="5b5b6-129">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="5b5b6-130">Fim do suporte do cliente</span><span class="sxs-lookup"><span data-stu-id="5b5b6-130">End of client support</span></span><br/>    | <span data-ttu-id="5b5b6-131">Windows 7</span><span class="sxs-lookup"><span data-stu-id="5b5b6-131">Windows 7</span></span><br/>                                                                           |
| <span data-ttu-id="5b5b6-132">Produto</span><span class="sxs-lookup"><span data-stu-id="5b5b6-132">Product</span></span><br/>                  | <span data-ttu-id="5b5b6-133">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="5b5b6-133">Windows Virtual PC</span></span><br/>                                                                  |
| <span data-ttu-id="5b5b6-134">parâmetro</span><span class="sxs-lookup"><span data-stu-id="5b5b6-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="5b5b6-135"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="5b5b6-135"><dt>VPCCOMInterfaces.h</dt></span></span> </dl>  |
| <span data-ttu-id="5b5b6-136">IID</span><span class="sxs-lookup"><span data-stu-id="5b5b6-136">IID</span></span><br/>                      | <span data-ttu-id="5b5b6-137">IID \_ IVMVirtualNetworkCollection é definido como 8ed680be-4242-4B2A-a21c-1982d8b0f675</span><span class="sxs-lookup"><span data-stu-id="5b5b6-137">IID\_IVMVirtualNetworkCollection is defined as 8ed680be-4242-4b2a-a21c-1982d8b0f675</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="5b5b6-138">Consulte também</span><span class="sxs-lookup"><span data-stu-id="5b5b6-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5b5b6-139">**IVMVirtualNetworkCollection**</span><span class="sxs-lookup"><span data-stu-id="5b5b6-139">**IVMVirtualNetworkCollection**</span></span>](ivmvirtualnetworkcollection.md)
</dt> </dl>

 

