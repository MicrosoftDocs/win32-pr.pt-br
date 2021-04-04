---
title: Propriedade IVMNetworkAdapter VirtualNetwork (VPCCOMInterfaces. h)
description: Recupera a rede virtual à qual a interface de rede está conectada.
ms.assetid: 7f52fd86-5f83-41d8-ba48-7db65e9c357c
keywords:
- Propriedade VirtualNetwork Virtual PC
- Propriedade VirtualNetwork Virtual PC, interface IVMNetworkAdapter
- Virtual PC interface IVMNetworkAdapter, Propriedade VirtualNetwork
topic_type:
- apiref
api_name:
- IVMNetworkAdapter.VirtualNetwork
- IVMNetworkAdapter.get_VirtualNetwork
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b932ef553d3952fbc69edba3416ac20049984810
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104008806"
---
# <a name="ivmnetworkadaptervirtualnetwork-property"></a><span data-ttu-id="4e2b1-106">Propriedade IVMNetworkAdapter:: VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="4e2b1-106">IVMNetworkAdapter::VirtualNetwork property</span></span>

<span data-ttu-id="4e2b1-107">\[O Windows Virtual PC não está mais disponível para uso a partir do Windows 8.</span><span class="sxs-lookup"><span data-stu-id="4e2b1-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="4e2b1-108">Em vez disso, use o [provedor WMI do Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="4e2b1-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="4e2b1-109">Recupera a rede virtual à qual a interface de rede está conectada.</span><span class="sxs-lookup"><span data-stu-id="4e2b1-109">Retrieves the virtual network to which the network interface is attached.</span></span>

<span data-ttu-id="4e2b1-110">Esta propriedade é somente para leitura.</span><span class="sxs-lookup"><span data-stu-id="4e2b1-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="4e2b1-111">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="4e2b1-111">Syntax</span></span>


```C++
HRESULT get_VirtualNetwork(
  [out, retval] IVMVirtualNetwork **virtualNetwork
);
```



## <a name="property-value"></a><span data-ttu-id="4e2b1-112">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="4e2b1-112">Property value</span></span>

<span data-ttu-id="4e2b1-113">Uma interface [**IVMVirtualNetwork**](ivmvirtualnetwork.md) que representa a rede virtual à qual essa interface de rede virtual está anexada.</span><span class="sxs-lookup"><span data-stu-id="4e2b1-113">An [**IVMVirtualNetwork**](ivmvirtualnetwork.md) interface that represents the virtual network to which this virtual network interface is attached.</span></span>

## <a name="error-codes"></a><span data-ttu-id="4e2b1-114">Códigos do Erro</span><span class="sxs-lookup"><span data-stu-id="4e2b1-114">Error codes</span></span>



| <span data-ttu-id="4e2b1-115">Nome/valor</span><span class="sxs-lookup"><span data-stu-id="4e2b1-115">Name/value</span></span>                                                                                                                                                                       | <span data-ttu-id="4e2b1-116">Significado</span><span class="sxs-lookup"><span data-stu-id="4e2b1-116">Meaning</span></span>                                                                                   |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="4e2b1-117"><dt>S \_ OK</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="4e2b1-117"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                                          | <span data-ttu-id="4e2b1-118">A operação foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="4e2b1-118">The operation was successful.</span></span><br/>                                                  |
| <dl> <span data-ttu-id="4e2b1-119"><dt>E \_ </dt> <dt>0X80004003</dt> de ponteiro</span><span class="sxs-lookup"><span data-stu-id="4e2b1-119"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>                            | <span data-ttu-id="4e2b1-120">O parâmetro é **NULL**.</span><span class="sxs-lookup"><span data-stu-id="4e2b1-120">The parameter is **NULL**.</span></span><br/>                                                     |
| <dl> <span data-ttu-id="4e2b1-121"><dt>S \_ FALSO</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="4e2b1-121"><dt>S\_FALSE</dt> <dt>1</dt></span></span> </dl>                                       | <span data-ttu-id="4e2b1-122">Esta interface de rede está desconectada e não está conectada a uma rede virtual.</span><span class="sxs-lookup"><span data-stu-id="4e2b1-122">This network interface is unplugged and is not connected to a virtual network.</span></span><br/> |
| <dl> <span data-ttu-id="4e2b1-123"><dt>VM \_ E \_ \_ ID de \_ rede \_ virtual inválida</dt> <dt>0xA00400702</dt></span><span class="sxs-lookup"><span data-stu-id="4e2b1-123"><dt>VM\_E\_INVALID\_VIRTUAL\_NETWORK\_ID</dt> <dt>0xA00400702</dt></span></span> </dl> | <span data-ttu-id="4e2b1-124">Esta interface está conectada a uma rede virtual com uma ID inválida.</span><span class="sxs-lookup"><span data-stu-id="4e2b1-124">This interface is connected to a virtual network with an invalid ID.</span></span><br/>           |
| <dl> <span data-ttu-id="4e2b1-125"><dt>DISP \_ E \_ </dt> <dt>0x80020009</dt> de exceção</span><span class="sxs-lookup"><span data-stu-id="4e2b1-125"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl>                    | <span data-ttu-id="4e2b1-126">Ocorreu um erro inesperado.</span><span class="sxs-lookup"><span data-stu-id="4e2b1-126">An unexpected error has occurred.</span></span><br/>                                              |



## <a name="requirements"></a><span data-ttu-id="4e2b1-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4e2b1-127">Requirements</span></span>



| <span data-ttu-id="4e2b1-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="4e2b1-128">Requirement</span></span> | <span data-ttu-id="4e2b1-129">Valor</span><span class="sxs-lookup"><span data-stu-id="4e2b1-129">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="4e2b1-130">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="4e2b1-130">Minimum supported client</span></span><br/> | <span data-ttu-id="4e2b1-131">\[Somente aplicativos de área de trabalho do Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="4e2b1-131">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="4e2b1-132">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="4e2b1-132">Minimum supported server</span></span><br/> | <span data-ttu-id="4e2b1-133">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="4e2b1-133">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="4e2b1-134">Fim do suporte do cliente</span><span class="sxs-lookup"><span data-stu-id="4e2b1-134">End of client support</span></span><br/>    | <span data-ttu-id="4e2b1-135">Windows 7</span><span class="sxs-lookup"><span data-stu-id="4e2b1-135">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="4e2b1-136">Produto</span><span class="sxs-lookup"><span data-stu-id="4e2b1-136">Product</span></span><br/>                  | <span data-ttu-id="4e2b1-137">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="4e2b1-137">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="4e2b1-138">parâmetro</span><span class="sxs-lookup"><span data-stu-id="4e2b1-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="4e2b1-139"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="4e2b1-139"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="4e2b1-140">IID</span><span class="sxs-lookup"><span data-stu-id="4e2b1-140">IID</span></span><br/>                      | <span data-ttu-id="4e2b1-141">IID \_ IVMNetworkAdapter é definido como e32e4165-22b8-4DC0-8d57-850171ae207a</span><span class="sxs-lookup"><span data-stu-id="4e2b1-141">IID\_IVMNetworkAdapter is defined as e32e4165-22b8-4dc0-8d57-850171ae207a</span></span><br/>          |



## <a name="see-also"></a><span data-ttu-id="4e2b1-142">Confira também</span><span class="sxs-lookup"><span data-stu-id="4e2b1-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4e2b1-143">**IVMNetworkAdapter**</span><span class="sxs-lookup"><span data-stu-id="4e2b1-143">**IVMNetworkAdapter**</span></span>](ivmnetworkadapter.md)
</dt> </dl>

 

