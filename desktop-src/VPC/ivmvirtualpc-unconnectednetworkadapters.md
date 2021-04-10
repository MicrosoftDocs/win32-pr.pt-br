---
title: Propriedade IVMVirtualPC UnconnectedNetworkAdapters (VPCCOMInterfaces. h)
description: Recupera uma coleção enumerável de interfaces de rede desconectadas.
ms.assetid: 2d95f289-083a-4388-b842-0a11b4e1a06f
keywords:
- Propriedade UnconnectedNetworkAdapters Virtual PC
- Propriedade UnconnectedNetworkAdapters Virtual PC, interface IVMVirtualPC
- IVMVirtualPC interface virtual PC, Propriedade UnconnectedNetworkAdapters
topic_type:
- apiref
api_name:
- IVMVirtualPC.UnconnectedNetworkAdapters
- IVMVirtualPC.get_UnconnectedNetworkAdapters
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c0694c6c5ce782e05ca322ba57f4ce7aaf5f708d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104009494"
---
# <a name="ivmvirtualpcunconnectednetworkadapters-property"></a><span data-ttu-id="975bf-106">Propriedade IVMVirtualPC:: UnconnectedNetworkAdapters</span><span class="sxs-lookup"><span data-stu-id="975bf-106">IVMVirtualPC::UnconnectedNetworkAdapters property</span></span>

<span data-ttu-id="975bf-107">\[O Windows Virtual PC não está mais disponível para uso a partir do Windows 8.</span><span class="sxs-lookup"><span data-stu-id="975bf-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="975bf-108">Em vez disso, use o [provedor WMI do Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="975bf-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="975bf-109">Recupera uma coleção enumerável de interfaces de rede desconectadas.</span><span class="sxs-lookup"><span data-stu-id="975bf-109">Retrieves an enumerable collection of unconnected network interfaces.</span></span>

<span data-ttu-id="975bf-110">Esta propriedade é somente para leitura.</span><span class="sxs-lookup"><span data-stu-id="975bf-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="975bf-111">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="975bf-111">Syntax</span></span>


```C++
HRESULT get_UnconnectedNetworkAdapters(
  [out, retval] IVMNetworkAdapterCollection **unconnectedNetworkAdapterCollection
);
```



## <a name="property-value"></a><span data-ttu-id="975bf-112">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="975bf-112">Property value</span></span>

<span data-ttu-id="975bf-113">Uma coleção de objetos [**IVMNetworkAdapter**](ivmnetworkadapter.md) não conectados.</span><span class="sxs-lookup"><span data-stu-id="975bf-113">A collection of unconnected [**IVMNetworkAdapter**](ivmnetworkadapter.md) objects.</span></span> <span data-ttu-id="975bf-114">Consulte [**IVMNetworkAdapterCollection**](ivmnetworkadaptercollection.md).</span><span class="sxs-lookup"><span data-stu-id="975bf-114">See [**IVMNetworkAdapterCollection**](ivmnetworkadaptercollection.md).</span></span>

## <a name="error-codes"></a><span data-ttu-id="975bf-115">Códigos do Erro</span><span class="sxs-lookup"><span data-stu-id="975bf-115">Error codes</span></span>



| <span data-ttu-id="975bf-116">Nome/valor</span><span class="sxs-lookup"><span data-stu-id="975bf-116">Name/value</span></span>                                                                                                                                                                           | <span data-ttu-id="975bf-117">Significado</span><span class="sxs-lookup"><span data-stu-id="975bf-117">Meaning</span></span>                                                                                         |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="975bf-118"><dt>S \_ OK</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="975bf-118"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                                              | <span data-ttu-id="975bf-119">A operação foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="975bf-119">The operation was successful.</span></span><br/>                                                        |
| <dl> <span data-ttu-id="975bf-120"><dt>E \_ </dt> <dt>0X80004003</dt> de ponteiro</span><span class="sxs-lookup"><span data-stu-id="975bf-120"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>                                | <span data-ttu-id="975bf-121">O parâmetro é **NULL**.</span><span class="sxs-lookup"><span data-stu-id="975bf-121">The parameter is **NULL**.</span></span><br/>                                                           |
| <dl> <span data-ttu-id="975bf-122"><dt>DISP \_ E \_ </dt> <dt>0x80020009</dt> de exceção</span><span class="sxs-lookup"><span data-stu-id="975bf-122"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl>                        | <span data-ttu-id="975bf-123">Ocorreu um erro inesperado.</span><span class="sxs-lookup"><span data-stu-id="975bf-123">An unexpected error has occurred.</span></span><br/>                                                    |
| <dl> <span data-ttu-id="975bf-124"><dt>VM \_ E 0xA0040951 de \_ \_ virtualização de hardware \_ desabilitada</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="975bf-124"><dt>VM\_E\_HARDWARE\_VIRTUALIZATION\_DISABLED</dt> <dt>0xA0040951</dt></span></span> </dl> | <span data-ttu-id="975bf-125">O processador não oferece suporte a extensões de corre (virtualização acelerada por hardware).</span><span class="sxs-lookup"><span data-stu-id="975bf-125">The processor does not support Hardware Accelerated Virtualization (HAV) extensions.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="975bf-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="975bf-126">Requirements</span></span>



| <span data-ttu-id="975bf-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="975bf-127">Requirement</span></span> | <span data-ttu-id="975bf-128">Valor</span><span class="sxs-lookup"><span data-stu-id="975bf-128">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="975bf-129">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="975bf-129">Minimum supported client</span></span><br/> | <span data-ttu-id="975bf-130">\[Somente aplicativos de área de trabalho do Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="975bf-130">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="975bf-131">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="975bf-131">Minimum supported server</span></span><br/> | <span data-ttu-id="975bf-132">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="975bf-132">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="975bf-133">Fim do suporte do cliente</span><span class="sxs-lookup"><span data-stu-id="975bf-133">End of client support</span></span><br/>    | <span data-ttu-id="975bf-134">Windows 7</span><span class="sxs-lookup"><span data-stu-id="975bf-134">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="975bf-135">Produto</span><span class="sxs-lookup"><span data-stu-id="975bf-135">Product</span></span><br/>                  | <span data-ttu-id="975bf-136">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="975bf-136">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="975bf-137">parâmetro</span><span class="sxs-lookup"><span data-stu-id="975bf-137">Header</span></span><br/>                   | <dl> <span data-ttu-id="975bf-138"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="975bf-138"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="975bf-139">IID</span><span class="sxs-lookup"><span data-stu-id="975bf-139">IID</span></span><br/>                      | <span data-ttu-id="975bf-140">IID \_ IVMVirtualPC é definido como 236ba0d9-a24a-4292-a132-27c1421dfd01</span><span class="sxs-lookup"><span data-stu-id="975bf-140">IID\_IVMVirtualPC is defined as 236ba0d9-a24a-4292-a132-27c1421dfd01</span></span><br/>               |



## <a name="see-also"></a><span data-ttu-id="975bf-141">Confira também</span><span class="sxs-lookup"><span data-stu-id="975bf-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="975bf-142">**IVMVirtualPC**</span><span class="sxs-lookup"><span data-stu-id="975bf-142">**IVMVirtualPC**</span></span>](ivmvirtualpc.md)
</dt> </dl>

 

