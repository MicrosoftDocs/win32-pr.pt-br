---
title: Propriedade nome do IVMVirtualNetwork (VPCCOMInterfaces. h)
description: Nome exclusivo da instância de rede virtual.
ms.assetid: dd4807dc-abae-4bdb-ba27-597cf1337834
keywords:
- Propriedade do nome Virtual PC
- Propriedade de nome Virtual PC, interface IVMVirtualNetwork
- IVMVirtualNetwork interface virtual PC, Propriedade Name
topic_type:
- apiref
api_name:
- IVMVirtualNetwork.Name
- IVMVirtualNetwork.get_Name
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c962d7b65bfddaf5293bd391ae84f04bae512ba9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103919000"
---
# <a name="ivmvirtualnetworkname-property"></a><span data-ttu-id="6109a-106">Propriedade IVMVirtualNetwork:: Name</span><span class="sxs-lookup"><span data-stu-id="6109a-106">IVMVirtualNetwork::Name property</span></span>

<span data-ttu-id="6109a-107">\[O Windows Virtual PC não está mais disponível para uso a partir do Windows 8.</span><span class="sxs-lookup"><span data-stu-id="6109a-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="6109a-108">Em vez disso, use o [provedor WMI do Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="6109a-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="6109a-109">Recupera o nome exclusivo da instância de rede virtual.</span><span class="sxs-lookup"><span data-stu-id="6109a-109">Retrieves the unique name of the virtual network instance.</span></span>

<span data-ttu-id="6109a-110">Esta propriedade é somente para leitura.</span><span class="sxs-lookup"><span data-stu-id="6109a-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="6109a-111">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="6109a-111">Syntax</span></span>


```C++
HRESULT get_Name(
  [out, retval] BSTR *virtualNetworkName
);
```



## <a name="property-value"></a><span data-ttu-id="6109a-112">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="6109a-112">Property value</span></span>

<span data-ttu-id="6109a-113">O nome da rede virtual.</span><span class="sxs-lookup"><span data-stu-id="6109a-113">The name of the virtual network.</span></span>

## <a name="error-codes"></a><span data-ttu-id="6109a-114">Códigos do Erro</span><span class="sxs-lookup"><span data-stu-id="6109a-114">Error codes</span></span>



| <span data-ttu-id="6109a-115">Nome/valor</span><span class="sxs-lookup"><span data-stu-id="6109a-115">Name/value</span></span>                                                                                                                                                    | <span data-ttu-id="6109a-116">Significado</span><span class="sxs-lookup"><span data-stu-id="6109a-116">Meaning</span></span>                                                                                 |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="6109a-117"><dt>S \_ OK</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="6109a-117"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                       | <span data-ttu-id="6109a-118">A operação foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="6109a-118">The operation was successful.</span></span><br/>                                                |
| <dl> <span data-ttu-id="6109a-119"><dt>E \_ </dt> <dt>0X80004003</dt> de ponteiro</span><span class="sxs-lookup"><span data-stu-id="6109a-119"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>         | <span data-ttu-id="6109a-120">O parâmetro é **NULL**.</span><span class="sxs-lookup"><span data-stu-id="6109a-120">The parameter is **NULL**.</span></span><br/>                                                   |
| <dl> <span data-ttu-id="6109a-121"><dt>DISP \_ E \_ </dt> <dt>0x80020009</dt> de exceção</span><span class="sxs-lookup"><span data-stu-id="6109a-121"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl> | <span data-ttu-id="6109a-122">Ocorreu um erro inesperado ou a instância da rede virtual é desconhecida.</span><span class="sxs-lookup"><span data-stu-id="6109a-122">An unexpected error has occurred or the virtual network instance is unknown.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="6109a-123">Comentários</span><span class="sxs-lookup"><span data-stu-id="6109a-123">Remarks</span></span>

<span data-ttu-id="6109a-124">Os nomes de rede virtual não diferenciam maiúsculas de minúsculas, por exemplo, "mynetwork" e "mynetwork" referem-se à mesma rede virtual.</span><span class="sxs-lookup"><span data-stu-id="6109a-124">Virtual network names are case-insensitive, for example, "MyNetwork" and "mynetwork" refer to the same virtual network.</span></span>

## <a name="requirements"></a><span data-ttu-id="6109a-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6109a-125">Requirements</span></span>



| <span data-ttu-id="6109a-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="6109a-126">Requirement</span></span> | <span data-ttu-id="6109a-127">Valor</span><span class="sxs-lookup"><span data-stu-id="6109a-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="6109a-128">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6109a-128">Minimum supported client</span></span><br/> | <span data-ttu-id="6109a-129">\[Somente aplicativos de área de trabalho do Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="6109a-129">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="6109a-130">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6109a-130">Minimum supported server</span></span><br/> | <span data-ttu-id="6109a-131">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="6109a-131">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="6109a-132">Fim do suporte do cliente</span><span class="sxs-lookup"><span data-stu-id="6109a-132">End of client support</span></span><br/>    | <span data-ttu-id="6109a-133">Windows 7</span><span class="sxs-lookup"><span data-stu-id="6109a-133">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="6109a-134">Produto</span><span class="sxs-lookup"><span data-stu-id="6109a-134">Product</span></span><br/>                  | <span data-ttu-id="6109a-135">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="6109a-135">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="6109a-136">parâmetro</span><span class="sxs-lookup"><span data-stu-id="6109a-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="6109a-137"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="6109a-137"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="6109a-138">IID</span><span class="sxs-lookup"><span data-stu-id="6109a-138">IID</span></span><br/>                      | <span data-ttu-id="6109a-139">IID \_ IVMVirtualNetwork é definido como 431cb7a1-2469-4563-b94e-38b987adca63</span><span class="sxs-lookup"><span data-stu-id="6109a-139">IID\_IVMVirtualNetwork is defined as 431cb7a1-2469-4563-b94e-38b987adca63</span></span><br/>          |



## <a name="see-also"></a><span data-ttu-id="6109a-140">Confira também</span><span class="sxs-lookup"><span data-stu-id="6109a-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6109a-141">**IVMVirtualNetwork**</span><span class="sxs-lookup"><span data-stu-id="6109a-141">**IVMVirtualNetwork**</span></span>](ivmvirtualnetwork.md)
</dt> </dl>

 

