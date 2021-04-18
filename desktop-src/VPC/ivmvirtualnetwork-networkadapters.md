---
title: Propriedade IVMVirtualNetwork adaptadores (VPCCOMInterfaces. h)
description: Recupera uma coleção enumerável de NICs anexadas à rede virtual.
ms.assetid: d5b95831-4642-441e-93e8-34e125087a43
keywords:
- Propriedade adaptadores Virtual PC
- Propriedade adaptadores Virtual PC, interface IVMVirtualNetwork
- IVMVirtualNetwork interface virtual PC, Propriedade adaptadores
topic_type:
- apiref
api_name:
- IVMVirtualNetwork.NetworkAdapters
- IVMVirtualNetwork.get_NetworkAdapters
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8ba86f649744eeb34139c65de9aa4523ddc74d1f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105761172"
---
# <a name="ivmvirtualnetworknetworkadapters-property"></a><span data-ttu-id="336dc-106">Propriedade IVMVirtualNetwork:: adaptadores</span><span class="sxs-lookup"><span data-stu-id="336dc-106">IVMVirtualNetwork::NetworkAdapters property</span></span>

<span data-ttu-id="336dc-107">\[O Windows Virtual PC não está mais disponível para uso a partir do Windows 8.</span><span class="sxs-lookup"><span data-stu-id="336dc-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="336dc-108">Em vez disso, use o [provedor WMI do Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="336dc-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="336dc-109">Recupera uma coleção enumerável de NICs anexadas à rede virtual.</span><span class="sxs-lookup"><span data-stu-id="336dc-109">Retrieves an enumerable collection of NICs attached to the virtual network.</span></span>

<span data-ttu-id="336dc-110">Esta propriedade é somente para leitura.</span><span class="sxs-lookup"><span data-stu-id="336dc-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="336dc-111">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="336dc-111">Syntax</span></span>


```C++
HRESULT get_NetworkAdapters(
  [out, retval] IVMNetworkAdapterCollection **networkInterfaceCollection
);
```



## <a name="property-value"></a><span data-ttu-id="336dc-112">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="336dc-112">Property value</span></span>

<span data-ttu-id="336dc-113">Um novo [**IVMNetworkAdapterCollection**](ivmnetworkadaptercollection.md) que contém as NICs virtuais anexadas a essa rede virtual.</span><span class="sxs-lookup"><span data-stu-id="336dc-113">A new [**IVMNetworkAdapterCollection**](ivmnetworkadaptercollection.md) which holds the virtual NICs attached to this virtual network.</span></span>

## <a name="error-codes"></a><span data-ttu-id="336dc-114">Códigos do Erro</span><span class="sxs-lookup"><span data-stu-id="336dc-114">Error codes</span></span>



| <span data-ttu-id="336dc-115">Nome/valor</span><span class="sxs-lookup"><span data-stu-id="336dc-115">Name/value</span></span>                                                                                                                                                    | <span data-ttu-id="336dc-116">Significado</span><span class="sxs-lookup"><span data-stu-id="336dc-116">Meaning</span></span>                                      |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="336dc-117"><dt>S \_ OK</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="336dc-117"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                       | <span data-ttu-id="336dc-118">A operação foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="336dc-118">The operation was successful.</span></span><br/>     |
| <dl> <span data-ttu-id="336dc-119"><dt>E \_ </dt> <dt>0X80004003</dt> de ponteiro</span><span class="sxs-lookup"><span data-stu-id="336dc-119"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>         | <span data-ttu-id="336dc-120">O parâmetro é **NULL**.</span><span class="sxs-lookup"><span data-stu-id="336dc-120">The parameter is **NULL**.</span></span><br/>        |
| <dl> <span data-ttu-id="336dc-121"><dt>DISP \_ E \_ </dt> <dt>0x80020009</dt> de exceção</span><span class="sxs-lookup"><span data-stu-id="336dc-121"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl> | <span data-ttu-id="336dc-122">Ocorreu um erro inesperado.</span><span class="sxs-lookup"><span data-stu-id="336dc-122">An unexpected error has occurred.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="336dc-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="336dc-123">Requirements</span></span>



| <span data-ttu-id="336dc-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="336dc-124">Requirement</span></span> | <span data-ttu-id="336dc-125">Valor</span><span class="sxs-lookup"><span data-stu-id="336dc-125">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="336dc-126">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="336dc-126">Minimum supported client</span></span><br/> | <span data-ttu-id="336dc-127">\[Somente aplicativos de área de trabalho do Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="336dc-127">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="336dc-128">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="336dc-128">Minimum supported server</span></span><br/> | <span data-ttu-id="336dc-129">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="336dc-129">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="336dc-130">Fim do suporte do cliente</span><span class="sxs-lookup"><span data-stu-id="336dc-130">End of client support</span></span><br/>    | <span data-ttu-id="336dc-131">Windows 7</span><span class="sxs-lookup"><span data-stu-id="336dc-131">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="336dc-132">Produto</span><span class="sxs-lookup"><span data-stu-id="336dc-132">Product</span></span><br/>                  | <span data-ttu-id="336dc-133">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="336dc-133">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="336dc-134">parâmetro</span><span class="sxs-lookup"><span data-stu-id="336dc-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="336dc-135"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="336dc-135"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="336dc-136">IID</span><span class="sxs-lookup"><span data-stu-id="336dc-136">IID</span></span><br/>                      | <span data-ttu-id="336dc-137">IID \_ IVMVirtualNetwork é definido como 431cb7a1-2469-4563-b94e-38b987adca63</span><span class="sxs-lookup"><span data-stu-id="336dc-137">IID\_IVMVirtualNetwork is defined as 431cb7a1-2469-4563-b94e-38b987adca63</span></span><br/>          |



## <a name="see-also"></a><span data-ttu-id="336dc-138">Confira também</span><span class="sxs-lookup"><span data-stu-id="336dc-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="336dc-139">**IVMVirtualNetwork**</span><span class="sxs-lookup"><span data-stu-id="336dc-139">**IVMVirtualNetwork**</span></span>](ivmvirtualnetwork.md)
</dt> </dl>

 

