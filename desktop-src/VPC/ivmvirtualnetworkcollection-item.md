---
title: Propriedade de item IVMVirtualNetworkCollection (VPCCOMInterfaces. h)
description: Objeto IVMVirtualNetwork que corresponde ao índice especificado.
ms.assetid: 1c6a3449-f76a-4216-8840-0fb9fb133e67
keywords:
- Propriedade do item Virtual PC
- Propriedade de item Virtual PC, interface IVMVirtualNetworkCollection
- IVMVirtualNetworkCollection interface virtual PC, Propriedade Item
topic_type:
- apiref
api_name:
- IVMVirtualNetworkCollection.Item
- IVMVirtualNetworkCollection.get_Item
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ac5a7648db4708fbc1b445029419ee794809abcb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104009460"
---
# <a name="ivmvirtualnetworkcollectionitem-property"></a><span data-ttu-id="3dbe8-106">Propriedade IVMVirtualNetworkCollection:: item</span><span class="sxs-lookup"><span data-stu-id="3dbe8-106">IVMVirtualNetworkCollection::Item property</span></span>

<span data-ttu-id="3dbe8-107">\[O Windows Virtual PC não está mais disponível para uso a partir do Windows 8.</span><span class="sxs-lookup"><span data-stu-id="3dbe8-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="3dbe8-108">Em vez disso, use o [provedor WMI do Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="3dbe8-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="3dbe8-109">Recupera o objeto [**IVMVirtualNetwork**](ivmvirtualnetwork.md) que corresponde ao índice especificado.</span><span class="sxs-lookup"><span data-stu-id="3dbe8-109">Retrieves the [**IVMVirtualNetwork**](ivmvirtualnetwork.md) object that corresponds to the specified index.</span></span>

<span data-ttu-id="3dbe8-110">Esta propriedade é somente para leitura.</span><span class="sxs-lookup"><span data-stu-id="3dbe8-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="3dbe8-111">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="3dbe8-111">Syntax</span></span>


```C++
HRESULT get_Item(
  [in]          long              index,
  [out, retval] IVMVirtualNetwork **virtualNetwork
);
```



## <a name="property-value"></a><span data-ttu-id="3dbe8-112">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="3dbe8-112">Property value</span></span>

<span data-ttu-id="3dbe8-113">O objeto [**IVMVirtualNetwork**](ivmvirtualnetwork.md) .</span><span class="sxs-lookup"><span data-stu-id="3dbe8-113">The [**IVMVirtualNetwork**](ivmvirtualnetwork.md) object.</span></span>

## <a name="error-codes"></a><span data-ttu-id="3dbe8-114">Códigos do Erro</span><span class="sxs-lookup"><span data-stu-id="3dbe8-114">Error codes</span></span>



| <span data-ttu-id="3dbe8-115">Nome/valor</span><span class="sxs-lookup"><span data-stu-id="3dbe8-115">Name/value</span></span>                                                                                                                                                    | <span data-ttu-id="3dbe8-116">Significado</span><span class="sxs-lookup"><span data-stu-id="3dbe8-116">Meaning</span></span>                                                                                       |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="3dbe8-117"><dt>S \_ OK</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="3dbe8-117"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                       | <span data-ttu-id="3dbe8-118">A operação foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="3dbe8-118">The operation was successful.</span></span><br/>                                                      |
| <dl> <span data-ttu-id="3dbe8-119"><dt>E \_ </dt> <dt>0X80004003</dt> de ponteiro</span><span class="sxs-lookup"><span data-stu-id="3dbe8-119"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>         | <span data-ttu-id="3dbe8-120">O parâmetro *virtualNetwork* é **NULL**.</span><span class="sxs-lookup"><span data-stu-id="3dbe8-120">The *virtualNetwork* parameter is **NULL**.</span></span><br/>                                        |
| <dl> <span data-ttu-id="3dbe8-121"><dt>DISP \_ E \_ BADINDEX</dt> <dt>0x8002000B</dt></span><span class="sxs-lookup"><span data-stu-id="3dbe8-121"><dt>DISP\_E\_BADINDEX</dt> <dt>0x8002000B</dt></span></span> </dl>  | <span data-ttu-id="3dbe8-122">O índice do item solicitado não corresponde a um item nesta coleção.</span><span class="sxs-lookup"><span data-stu-id="3dbe8-122">The index of the requested item does not correspond to an item in this collection.</span></span><br/> |
| <dl> <span data-ttu-id="3dbe8-123"><dt>DISP \_ E \_ </dt> <dt>0x80020009</dt> de exceção</span><span class="sxs-lookup"><span data-stu-id="3dbe8-123"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl> | <span data-ttu-id="3dbe8-124">Ocorreu um erro inesperado.</span><span class="sxs-lookup"><span data-stu-id="3dbe8-124">An unexpected error has occurred.</span></span><br/>                                                  |



## <a name="requirements"></a><span data-ttu-id="3dbe8-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3dbe8-125">Requirements</span></span>



| <span data-ttu-id="3dbe8-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="3dbe8-126">Requirement</span></span> | <span data-ttu-id="3dbe8-127">Valor</span><span class="sxs-lookup"><span data-stu-id="3dbe8-127">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3dbe8-128">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3dbe8-128">Minimum supported client</span></span><br/> | <span data-ttu-id="3dbe8-129">\[Somente aplicativos de área de trabalho do Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="3dbe8-129">Windows 7 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="3dbe8-130">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3dbe8-130">Minimum supported server</span></span><br/> | <span data-ttu-id="3dbe8-131">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="3dbe8-131">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="3dbe8-132">Fim do suporte do cliente</span><span class="sxs-lookup"><span data-stu-id="3dbe8-132">End of client support</span></span><br/>    | <span data-ttu-id="3dbe8-133">Windows 7</span><span class="sxs-lookup"><span data-stu-id="3dbe8-133">Windows 7</span></span><br/>                                                                           |
| <span data-ttu-id="3dbe8-134">Produto</span><span class="sxs-lookup"><span data-stu-id="3dbe8-134">Product</span></span><br/>                  | <span data-ttu-id="3dbe8-135">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="3dbe8-135">Windows Virtual PC</span></span><br/>                                                                  |
| <span data-ttu-id="3dbe8-136">parâmetro</span><span class="sxs-lookup"><span data-stu-id="3dbe8-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="3dbe8-137"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="3dbe8-137"><dt>VPCCOMInterfaces.h</dt></span></span> </dl>  |
| <span data-ttu-id="3dbe8-138">IID</span><span class="sxs-lookup"><span data-stu-id="3dbe8-138">IID</span></span><br/>                      | <span data-ttu-id="3dbe8-139">IID \_ IVMVirtualNetworkCollection é definido como 8ed680be-4242-4B2A-a21c-1982d8b0f675</span><span class="sxs-lookup"><span data-stu-id="3dbe8-139">IID\_IVMVirtualNetworkCollection is defined as 8ed680be-4242-4b2a-a21c-1982d8b0f675</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="3dbe8-140">Confira também</span><span class="sxs-lookup"><span data-stu-id="3dbe8-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3dbe8-141">**IVMVirtualNetwork**</span><span class="sxs-lookup"><span data-stu-id="3dbe8-141">**IVMVirtualNetwork**</span></span>](ivmvirtualnetwork.md)
</dt> <dt>

[<span data-ttu-id="3dbe8-142">**IVMVirtualNetworkCollection**</span><span class="sxs-lookup"><span data-stu-id="3dbe8-142">**IVMVirtualNetworkCollection**</span></span>](ivmvirtualnetworkcollection.md)
</dt> </dl>

 

