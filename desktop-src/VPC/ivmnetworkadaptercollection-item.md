---
title: Propriedade de item IVMNetworkAdapterCollection (VPCCOMInterfaces. h)
description: Objeto IVMNetworkAdapter que corresponde ao índice especificado.
ms.assetid: 3de76e24-3315-473f-870b-074be8bcfe70
keywords:
- Propriedade do item Virtual PC
- Propriedade de item Virtual PC, interface IVMNetworkAdapterCollection
- IVMNetworkAdapterCollection interface virtual PC, Propriedade Item
topic_type:
- apiref
api_name:
- IVMNetworkAdapterCollection.Item
- IVMNetworkAdapterCollection.get_Item
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 63d2f7ee389938a44c6608241fb3fb2d48ec1bca
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103919098"
---
# <a name="ivmnetworkadaptercollectionitem-property"></a><span data-ttu-id="8732e-106">Propriedade IVMNetworkAdapterCollection:: item</span><span class="sxs-lookup"><span data-stu-id="8732e-106">IVMNetworkAdapterCollection::Item property</span></span>

<span data-ttu-id="8732e-107">\[O Windows Virtual PC não está mais disponível para uso a partir do Windows 8.</span><span class="sxs-lookup"><span data-stu-id="8732e-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="8732e-108">Em vez disso, use o [provedor WMI do Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="8732e-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="8732e-109">Recupera o objeto [**IVMNetworkAdapter**](ivmnetworkadapter.md) que corresponde ao índice especificado.</span><span class="sxs-lookup"><span data-stu-id="8732e-109">Retrieves the [**IVMNetworkAdapter**](ivmnetworkadapter.md) object that corresponds to the specified index.</span></span>

<span data-ttu-id="8732e-110">Esta propriedade é somente para leitura.</span><span class="sxs-lookup"><span data-stu-id="8732e-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="8732e-111">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="8732e-111">Syntax</span></span>


```C++
HRESULT get_Item(
  [in]          long              index,
  [out, retval] IVMNetworkAdapter **networkInterface
);
```



## <a name="property-value"></a><span data-ttu-id="8732e-112">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="8732e-112">Property value</span></span>

<span data-ttu-id="8732e-113">O objeto [**IVMNetworkAdapter**](ivmnetworkadapter.md) .</span><span class="sxs-lookup"><span data-stu-id="8732e-113">The [**IVMNetworkAdapter**](ivmnetworkadapter.md) object.</span></span>

## <a name="error-codes"></a><span data-ttu-id="8732e-114">Códigos do Erro</span><span class="sxs-lookup"><span data-stu-id="8732e-114">Error codes</span></span>



| <span data-ttu-id="8732e-115">Nome/valor</span><span class="sxs-lookup"><span data-stu-id="8732e-115">Name/value</span></span>                                                                                                                                                    | <span data-ttu-id="8732e-116">Significado</span><span class="sxs-lookup"><span data-stu-id="8732e-116">Meaning</span></span>                                                                                        |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="8732e-117"><dt>S \_ OK</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="8732e-117"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                       | <span data-ttu-id="8732e-118">A operação foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="8732e-118">The operation was successful.</span></span> <br/>                                                      |
| <dl> <span data-ttu-id="8732e-119"><dt>E \_ </dt> <dt>0X80004003</dt> de ponteiro</span><span class="sxs-lookup"><span data-stu-id="8732e-119"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>         | <span data-ttu-id="8732e-120">O parâmetro *networkInterface* é **nulo**.</span><span class="sxs-lookup"><span data-stu-id="8732e-120">The *networkInterface* parameter is **NULL**.</span></span> <br/>                                      |
| <dl> <span data-ttu-id="8732e-121"><dt>DISP \_ E \_ BADINDEX</dt> <dt>0x8002000B</dt></span><span class="sxs-lookup"><span data-stu-id="8732e-121"><dt>DISP\_E\_BADINDEX</dt> <dt>0x8002000B</dt></span></span> </dl>  | <span data-ttu-id="8732e-122">O índice do item solicitado não corresponde a um item nesta coleção.</span><span class="sxs-lookup"><span data-stu-id="8732e-122">The index of the requested item does not correspond to an item in this collection.</span></span> <br/> |
| <dl> <span data-ttu-id="8732e-123"><dt>DISP \_ E \_ </dt> <dt>0x80020009</dt> de exceção</span><span class="sxs-lookup"><span data-stu-id="8732e-123"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl> | <span data-ttu-id="8732e-124">Ocorreu um erro inesperado.</span><span class="sxs-lookup"><span data-stu-id="8732e-124">An unexpected error has occurred.</span></span><br/>                                                   |



## <a name="requirements"></a><span data-ttu-id="8732e-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8732e-125">Requirements</span></span>



| <span data-ttu-id="8732e-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="8732e-126">Requirement</span></span> | <span data-ttu-id="8732e-127">Valor</span><span class="sxs-lookup"><span data-stu-id="8732e-127">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8732e-128">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="8732e-128">Minimum supported client</span></span><br/> | <span data-ttu-id="8732e-129">\[Somente aplicativos de área de trabalho do Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="8732e-129">Windows 7 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="8732e-130">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="8732e-130">Minimum supported server</span></span><br/> | <span data-ttu-id="8732e-131">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="8732e-131">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="8732e-132">Fim do suporte do cliente</span><span class="sxs-lookup"><span data-stu-id="8732e-132">End of client support</span></span><br/>    | <span data-ttu-id="8732e-133">Windows 7</span><span class="sxs-lookup"><span data-stu-id="8732e-133">Windows 7</span></span><br/>                                                                           |
| <span data-ttu-id="8732e-134">Produto</span><span class="sxs-lookup"><span data-stu-id="8732e-134">Product</span></span><br/>                  | <span data-ttu-id="8732e-135">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="8732e-135">Windows Virtual PC</span></span><br/>                                                                  |
| <span data-ttu-id="8732e-136">parâmetro</span><span class="sxs-lookup"><span data-stu-id="8732e-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="8732e-137"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="8732e-137"><dt>VPCCOMInterfaces.h</dt></span></span> </dl>  |
| <span data-ttu-id="8732e-138">IID</span><span class="sxs-lookup"><span data-stu-id="8732e-138">IID</span></span><br/>                      | <span data-ttu-id="8732e-139">IID \_ IVMNetworkAdapterCollection é definido como ebaeafe9-EBCD-47CF-866e-ad87d735e479</span><span class="sxs-lookup"><span data-stu-id="8732e-139">IID\_IVMNetworkAdapterCollection is defined as ebaeafe9-ebcd-47cf-866e-ad87d735e479</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="8732e-140">Confira também</span><span class="sxs-lookup"><span data-stu-id="8732e-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8732e-141">**IVMNetworkAdapter**</span><span class="sxs-lookup"><span data-stu-id="8732e-141">**IVMNetworkAdapter**</span></span>](ivmnetworkadapter.md)
</dt> <dt>

[<span data-ttu-id="8732e-142">**IVMNetworkAdapterCollection**</span><span class="sxs-lookup"><span data-stu-id="8732e-142">**IVMNetworkAdapterCollection**</span></span>](ivmnetworkadaptercollection.md)
</dt> </dl>

 

