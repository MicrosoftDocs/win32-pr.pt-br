---
title: Método IVMNetworkAdapter DetachFromVirtualNetwork (VPCCOMInterfaces. h)
description: Desanexa a interface de rede de sua rede virtual.
ms.assetid: f1a00ea2-2b79-4b5c-a4bd-3cab66deb0d0
keywords:
- DetachFromVirtualNetwork do método virtual PC
- Método DetachFromVirtualNetwork Virtual PC, interface IVMNetworkAdapter
- IVMNetworkAdapter interface virtual PC, método DetachFromVirtualNetwork
topic_type:
- apiref
api_name:
- IVMNetworkAdapter.DetachFromVirtualNetwork
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d90d5046844764fe9e9eb6552fe1a04b6140201b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104369689"
---
# <a name="ivmnetworkadapterdetachfromvirtualnetwork-method"></a><span data-ttu-id="37828-106">IVMNetworkAdapter: método etachFromVirtualNetwork de:D</span><span class="sxs-lookup"><span data-stu-id="37828-106">IVMNetworkAdapter::DetachFromVirtualNetwork method</span></span>

<span data-ttu-id="37828-107">\[O Windows Virtual PC não está mais disponível para uso a partir do Windows 8.</span><span class="sxs-lookup"><span data-stu-id="37828-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="37828-108">Em vez disso, use o [provedor WMI do Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="37828-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="37828-109">Desanexa a interface de rede de sua rede virtual.</span><span class="sxs-lookup"><span data-stu-id="37828-109">Detaches the network interface from its virtual network.</span></span>

## <a name="syntax"></a><span data-ttu-id="37828-110">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="37828-110">Syntax</span></span>


```C++
HRESULT DetachFromVirtualNetwork();
```



## <a name="parameters"></a><span data-ttu-id="37828-111">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="37828-111">Parameters</span></span>

<span data-ttu-id="37828-112">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="37828-112">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="37828-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="37828-113">Return value</span></span>

<span data-ttu-id="37828-114">Esse método pode retornar um desses valores.</span><span class="sxs-lookup"><span data-stu-id="37828-114">This method can return one of these values.</span></span>



| <span data-ttu-id="37828-115">Código/valor de retorno</span><span class="sxs-lookup"><span data-stu-id="37828-115">Return code/value</span></span>                                                                                                                                                 | <span data-ttu-id="37828-116">Descrição</span><span class="sxs-lookup"><span data-stu-id="37828-116">Description</span></span>                                  |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="37828-117"><dt>**S \_ OK**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="37828-117"><dt>**S\_OK**</dt> <dt>0</dt></span></span> </dl>                       | <span data-ttu-id="37828-118">A operação foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="37828-118">The operation was successful.</span></span><br/>     |
| <dl> <span data-ttu-id="37828-119"><dt>**DISP \_ E \_**</dt> <dt>0x80020009</dt> de exceção</span><span class="sxs-lookup"><span data-stu-id="37828-119"><dt>**DISP\_E\_EXCEPTION**</dt> <dt>0x80020009</dt></span></span> </dl> | <span data-ttu-id="37828-120">Ocorreu um erro inesperado.</span><span class="sxs-lookup"><span data-stu-id="37828-120">An unexpected error has occurred.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="37828-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="37828-121">Requirements</span></span>



| <span data-ttu-id="37828-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="37828-122">Requirement</span></span> | <span data-ttu-id="37828-123">Valor</span><span class="sxs-lookup"><span data-stu-id="37828-123">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="37828-124">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="37828-124">Minimum supported client</span></span><br/> | <span data-ttu-id="37828-125">\[Somente aplicativos de área de trabalho do Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="37828-125">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="37828-126">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="37828-126">Minimum supported server</span></span><br/> | <span data-ttu-id="37828-127">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="37828-127">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="37828-128">Fim do suporte do cliente</span><span class="sxs-lookup"><span data-stu-id="37828-128">End of client support</span></span><br/>    | <span data-ttu-id="37828-129">Windows 7</span><span class="sxs-lookup"><span data-stu-id="37828-129">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="37828-130">Produto</span><span class="sxs-lookup"><span data-stu-id="37828-130">Product</span></span><br/>                  | <span data-ttu-id="37828-131">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="37828-131">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="37828-132">parâmetro</span><span class="sxs-lookup"><span data-stu-id="37828-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="37828-133"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="37828-133"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="37828-134">IID</span><span class="sxs-lookup"><span data-stu-id="37828-134">IID</span></span><br/>                      | <span data-ttu-id="37828-135">IID \_ IVMNetworkAdapter é definido como e32e4165-22b8-4DC0-8d57-850171ae207a</span><span class="sxs-lookup"><span data-stu-id="37828-135">IID\_IVMNetworkAdapter is defined as e32e4165-22b8-4dc0-8d57-850171ae207a</span></span><br/>          |



## <a name="see-also"></a><span data-ttu-id="37828-136">Confira também</span><span class="sxs-lookup"><span data-stu-id="37828-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="37828-137">**IVMNetworkAdapter**</span><span class="sxs-lookup"><span data-stu-id="37828-137">**IVMNetworkAdapter**</span></span>](ivmnetworkadapter.md)
</dt> </dl>

 

