---
title: Propriedade IVMVirtualPC VirtualNetworks (VPCCOMInterfaces. h)
description: Recupera uma coleção enumerável de redes virtuais.
ms.assetid: 88c68178-0399-44cd-8145-1f2e4d6ac632
keywords:
- Propriedade VirtualNetworks Virtual PC
- Propriedade VirtualNetworks Virtual PC, interface IVMVirtualPC
- IVMVirtualPC interface virtual PC, Propriedade VirtualNetworks
topic_type:
- apiref
api_name:
- IVMVirtualPC.VirtualNetworks
- IVMVirtualPC.get_VirtualNetworks
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bf2ea97a7d9bb65bb41842ca028ded88f9a26b63
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104086441"
---
# <a name="ivmvirtualpcvirtualnetworks-property"></a><span data-ttu-id="6d158-106">Propriedade IVMVirtualPC:: VirtualNetworks</span><span class="sxs-lookup"><span data-stu-id="6d158-106">IVMVirtualPC::VirtualNetworks property</span></span>

<span data-ttu-id="6d158-107">\[O Windows Virtual PC não está mais disponível para uso a partir do Windows 8.</span><span class="sxs-lookup"><span data-stu-id="6d158-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="6d158-108">Em vez disso, use o [provedor WMI do Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="6d158-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="6d158-109">Recupera uma coleção enumerável de redes virtuais.</span><span class="sxs-lookup"><span data-stu-id="6d158-109">Retrieves an enumerable collection of virtual networks.</span></span>

<span data-ttu-id="6d158-110">Esta propriedade é somente para leitura.</span><span class="sxs-lookup"><span data-stu-id="6d158-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="6d158-111">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="6d158-111">Syntax</span></span>


```C++
HRESULT get_VirtualNetworks(
  [out, retval] IVMVirtualNetworkCollection **virtualNetworkCollection
);
```



## <a name="property-value"></a><span data-ttu-id="6d158-112">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="6d158-112">Property value</span></span>

<span data-ttu-id="6d158-113">Uma coleção de objetos [**IVMVirtualNetwork**](ivmvirtualnetwork.md) .</span><span class="sxs-lookup"><span data-stu-id="6d158-113">A collection of [**IVMVirtualNetwork**](ivmvirtualnetwork.md) objects.</span></span> <span data-ttu-id="6d158-114">Consulte [**IVMVirtualNetworkCollection**](ivmvirtualnetworkcollection.md).</span><span class="sxs-lookup"><span data-stu-id="6d158-114">See [**IVMVirtualNetworkCollection**](ivmvirtualnetworkcollection.md).</span></span>

## <a name="error-codes"></a><span data-ttu-id="6d158-115">Códigos do Erro</span><span class="sxs-lookup"><span data-stu-id="6d158-115">Error codes</span></span>



| <span data-ttu-id="6d158-116">Nome/valor</span><span class="sxs-lookup"><span data-stu-id="6d158-116">Name/value</span></span>                                                                                                                                                                           | <span data-ttu-id="6d158-117">Significado</span><span class="sxs-lookup"><span data-stu-id="6d158-117">Meaning</span></span>                                                                                         |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="6d158-118"><dt>S \_ OK</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="6d158-118"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                                              | <span data-ttu-id="6d158-119">A operação foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="6d158-119">The operation was successful.</span></span><br/>                                                        |
| <dl> <span data-ttu-id="6d158-120"><dt>E \_ </dt> <dt>0X80004003</dt> de ponteiro</span><span class="sxs-lookup"><span data-stu-id="6d158-120"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>                                | <span data-ttu-id="6d158-121">O parâmetro é **NULL**.</span><span class="sxs-lookup"><span data-stu-id="6d158-121">The parameter is **NULL**.</span></span><br/>                                                           |
| <dl> <span data-ttu-id="6d158-122"><dt>DISP \_ E \_ </dt> <dt>0x80020009</dt> de exceção</span><span class="sxs-lookup"><span data-stu-id="6d158-122"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl>                        | <span data-ttu-id="6d158-123">Ocorreu um erro inesperado.</span><span class="sxs-lookup"><span data-stu-id="6d158-123">An unexpected error has occurred.</span></span><br/>                                                    |
| <dl> <span data-ttu-id="6d158-124"><dt>VM \_ E 0xA0040951 de \_ \_ virtualização de hardware \_ desabilitada</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="6d158-124"><dt>VM\_E\_HARDWARE\_VIRTUALIZATION\_DISABLED</dt> <dt>0xA0040951</dt></span></span> </dl> | <span data-ttu-id="6d158-125">O processador não oferece suporte a extensões de corre (virtualização acelerada por hardware).</span><span class="sxs-lookup"><span data-stu-id="6d158-125">The processor does not support Hardware Accelerated Virtualization (HAV) extensions.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="6d158-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6d158-126">Requirements</span></span>



| <span data-ttu-id="6d158-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="6d158-127">Requirement</span></span> | <span data-ttu-id="6d158-128">Valor</span><span class="sxs-lookup"><span data-stu-id="6d158-128">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="6d158-129">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6d158-129">Minimum supported client</span></span><br/> | <span data-ttu-id="6d158-130">\[Somente aplicativos de área de trabalho do Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="6d158-130">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="6d158-131">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6d158-131">Minimum supported server</span></span><br/> | <span data-ttu-id="6d158-132">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="6d158-132">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="6d158-133">Fim do suporte do cliente</span><span class="sxs-lookup"><span data-stu-id="6d158-133">End of client support</span></span><br/>    | <span data-ttu-id="6d158-134">Windows 7</span><span class="sxs-lookup"><span data-stu-id="6d158-134">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="6d158-135">Produto</span><span class="sxs-lookup"><span data-stu-id="6d158-135">Product</span></span><br/>                  | <span data-ttu-id="6d158-136">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="6d158-136">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="6d158-137">parâmetro</span><span class="sxs-lookup"><span data-stu-id="6d158-137">Header</span></span><br/>                   | <dl> <span data-ttu-id="6d158-138"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="6d158-138"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="6d158-139">IID</span><span class="sxs-lookup"><span data-stu-id="6d158-139">IID</span></span><br/>                      | <span data-ttu-id="6d158-140">IID \_ IVMVirtualPC é definido como 236ba0d9-a24a-4292-a132-27c1421dfd01</span><span class="sxs-lookup"><span data-stu-id="6d158-140">IID\_IVMVirtualPC is defined as 236ba0d9-a24a-4292-a132-27c1421dfd01</span></span><br/>               |



## <a name="see-also"></a><span data-ttu-id="6d158-141">Confira também</span><span class="sxs-lookup"><span data-stu-id="6d158-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6d158-142">**IVMVirtualPC**</span><span class="sxs-lookup"><span data-stu-id="6d158-142">**IVMVirtualPC**</span></span>](ivmvirtualpc.md)
</dt> </dl>

 

