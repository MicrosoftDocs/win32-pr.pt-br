---
title: Propriedade Count de IVMNetworkAdapterCollection (VPCCOMInterfaces. h)
description: Recupera o número de interfaces de rede nesta coleção.
ms.assetid: 0b6391fa-62fe-4db1-b0a2-565ab17157ab
keywords:
- Propriedade de contagem Virtual PC
- Propriedade Count Virtual PC, interface IVMNetworkAdapterCollection
- Virtual PC de interface IVMNetworkAdapterCollection, Propriedade Count
topic_type:
- apiref
api_name:
- IVMNetworkAdapterCollection.Count
- IVMNetworkAdapterCollection.get_Count
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1a287122d9829cd98f355d44e6bd408f6ca0d67a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104085126"
---
# <a name="ivmnetworkadaptercollectioncount-property"></a><span data-ttu-id="87545-106">Propriedade IVMNetworkAdapterCollection:: Count</span><span class="sxs-lookup"><span data-stu-id="87545-106">IVMNetworkAdapterCollection::Count property</span></span>

<span data-ttu-id="87545-107">\[O Windows Virtual PC não está mais disponível para uso a partir do Windows 8.</span><span class="sxs-lookup"><span data-stu-id="87545-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="87545-108">Em vez disso, use o [provedor WMI do Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="87545-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="87545-109">Recupera o número de interfaces de rede nesta coleção.</span><span class="sxs-lookup"><span data-stu-id="87545-109">Retrieves the number of network interfaces in this collection.</span></span>

<span data-ttu-id="87545-110">Esta propriedade é somente para leitura.</span><span class="sxs-lookup"><span data-stu-id="87545-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="87545-111">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="87545-111">Syntax</span></span>


```C++
HRESULT get_Count(
  [out, retval] long *count
);
```



## <a name="property-value"></a><span data-ttu-id="87545-112">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="87545-112">Property value</span></span>

<span data-ttu-id="87545-113">O número de interfaces de rede.</span><span class="sxs-lookup"><span data-stu-id="87545-113">The number of network interfaces.</span></span>

## <a name="error-codes"></a><span data-ttu-id="87545-114">Códigos do Erro</span><span class="sxs-lookup"><span data-stu-id="87545-114">Error codes</span></span>



| <span data-ttu-id="87545-115">Nome/valor</span><span class="sxs-lookup"><span data-stu-id="87545-115">Name/value</span></span>                                                                                                                                                    | <span data-ttu-id="87545-116">Significado</span><span class="sxs-lookup"><span data-stu-id="87545-116">Meaning</span></span>                                      |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="87545-117"><dt>S \_ OK</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="87545-117"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                       | <span data-ttu-id="87545-118">A operação foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="87545-118">The operation was successful.</span></span><br/>     |
| <dl> <span data-ttu-id="87545-119"><dt>E \_ </dt> <dt>0X80004003</dt> de ponteiro</span><span class="sxs-lookup"><span data-stu-id="87545-119"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>         | <span data-ttu-id="87545-120">O parâmetro é **NULL**.</span><span class="sxs-lookup"><span data-stu-id="87545-120">The parameter is **NULL**.</span></span><br/>        |
| <dl> <span data-ttu-id="87545-121"><dt>DISP \_ E \_ </dt> <dt>0x80020009</dt> de exceção</span><span class="sxs-lookup"><span data-stu-id="87545-121"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl> | <span data-ttu-id="87545-122">Ocorreu um erro inesperado.</span><span class="sxs-lookup"><span data-stu-id="87545-122">An unexpected error has occurred.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="87545-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="87545-123">Requirements</span></span>



| <span data-ttu-id="87545-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="87545-124">Requirement</span></span> | <span data-ttu-id="87545-125">Valor</span><span class="sxs-lookup"><span data-stu-id="87545-125">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="87545-126">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="87545-126">Minimum supported client</span></span><br/> | <span data-ttu-id="87545-127">\[Somente aplicativos de área de trabalho do Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="87545-127">Windows 7 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="87545-128">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="87545-128">Minimum supported server</span></span><br/> | <span data-ttu-id="87545-129">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="87545-129">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="87545-130">Fim do suporte do cliente</span><span class="sxs-lookup"><span data-stu-id="87545-130">End of client support</span></span><br/>    | <span data-ttu-id="87545-131">Windows 7</span><span class="sxs-lookup"><span data-stu-id="87545-131">Windows 7</span></span><br/>                                                                           |
| <span data-ttu-id="87545-132">Produto</span><span class="sxs-lookup"><span data-stu-id="87545-132">Product</span></span><br/>                  | <span data-ttu-id="87545-133">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="87545-133">Windows Virtual PC</span></span><br/>                                                                  |
| <span data-ttu-id="87545-134">parâmetro</span><span class="sxs-lookup"><span data-stu-id="87545-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="87545-135"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="87545-135"><dt>VPCCOMInterfaces.h</dt></span></span> </dl>  |
| <span data-ttu-id="87545-136">IID</span><span class="sxs-lookup"><span data-stu-id="87545-136">IID</span></span><br/>                      | <span data-ttu-id="87545-137">IID \_ IVMNetworkAdapterCollection é definido como ebaeafe9-EBCD-47CF-866e-ad87d735e479</span><span class="sxs-lookup"><span data-stu-id="87545-137">IID\_IVMNetworkAdapterCollection is defined as ebaeafe9-ebcd-47cf-866e-ad87d735e479</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="87545-138">Confira também</span><span class="sxs-lookup"><span data-stu-id="87545-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="87545-139">**IVMNetworkAdapterCollection**</span><span class="sxs-lookup"><span data-stu-id="87545-139">**IVMNetworkAdapterCollection**</span></span>](ivmnetworkadaptercollection.md)
</dt> </dl>

 

