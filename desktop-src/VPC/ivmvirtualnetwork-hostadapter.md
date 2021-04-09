---
title: Propriedade IVMVirtualNetwork HostAdapter (VPCCOMInterfaces. h)
description: Nome do adaptador ao qual a rede virtual está conectada.
ms.assetid: 7ee074d2-13ba-42db-84db-ecfd22576a9a
keywords:
- Propriedade HostAdapter Virtual PC
- Propriedade HostAdapter Virtual PC, interface IVMVirtualNetwork
- IVMVirtualNetwork interface virtual PC, Propriedade HostAdapter
topic_type:
- apiref
api_name:
- IVMVirtualNetwork.HostAdapter
- IVMVirtualNetwork.get_HostAdapter
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0485303c2328a85c70779f16652121729546f3ed
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104009625"
---
# <a name="ivmvirtualnetworkhostadapter-property"></a><span data-ttu-id="4d787-106">Propriedade IVMVirtualNetwork:: HostAdapter</span><span class="sxs-lookup"><span data-stu-id="4d787-106">IVMVirtualNetwork::HostAdapter property</span></span>

<span data-ttu-id="4d787-107">\[O Windows Virtual PC não está mais disponível para uso a partir do Windows 8.</span><span class="sxs-lookup"><span data-stu-id="4d787-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="4d787-108">Em vez disso, use o [provedor WMI do Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="4d787-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="4d787-109">Recupera o nome do adaptador ao qual a rede virtual está conectada.</span><span class="sxs-lookup"><span data-stu-id="4d787-109">Retrieves the name of the adapter to which the virtual network is connected.</span></span>

<span data-ttu-id="4d787-110">Esta propriedade é somente para leitura.</span><span class="sxs-lookup"><span data-stu-id="4d787-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="4d787-111">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="4d787-111">Syntax</span></span>


```C++
HRESULT get_HostAdapter(
  [out, retval] BSTR *hostAdapter
);
```



## <a name="property-value"></a><span data-ttu-id="4d787-112">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="4d787-112">Property value</span></span>

<span data-ttu-id="4d787-113">O nome do adaptador de host ao qual a rede virtual está conectada.</span><span class="sxs-lookup"><span data-stu-id="4d787-113">The name of the host adapter to which the virtual network is connected.</span></span>

## <a name="error-codes"></a><span data-ttu-id="4d787-114">Códigos do Erro</span><span class="sxs-lookup"><span data-stu-id="4d787-114">Error codes</span></span>



| <span data-ttu-id="4d787-115">Nome/valor</span><span class="sxs-lookup"><span data-stu-id="4d787-115">Name/value</span></span>                                                                                                                                                            | <span data-ttu-id="4d787-116">Significado</span><span class="sxs-lookup"><span data-stu-id="4d787-116">Meaning</span></span>                                                                                                                                                               |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="4d787-117"><dt>S \_ OK</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="4d787-117"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                               | <span data-ttu-id="4d787-118">A operação foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="4d787-118">The operation was successful.</span></span><br/>                                                                                                                              |
| <dl> <span data-ttu-id="4d787-119"><dt>E \_ </dt> <dt>0X80004003</dt> de ponteiro</span><span class="sxs-lookup"><span data-stu-id="4d787-119"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>                 | <span data-ttu-id="4d787-120">O parâmetro é **NULL**.</span><span class="sxs-lookup"><span data-stu-id="4d787-120">The parameter is **NULL**.</span></span><br/>                                                                                                                                 |
| <dl> <span data-ttu-id="4d787-121"><dt>VM \_ \_Adaptador E \_ não \_ encontrado</dt> <dt>0xA0040700</dt></span><span class="sxs-lookup"><span data-stu-id="4d787-121"><dt>VM\_E\_ADAPTER\_NOT\_FOUND</dt> <dt>0xA0040700</dt></span></span> </dl> | <span data-ttu-id="4d787-122">O adaptador de Ethernet do host ao qual essa rede virtual estava conectada não está mais disponível.</span><span class="sxs-lookup"><span data-stu-id="4d787-122">The host Ethernet adapter to which this virtual network was connected is no longer available.</span></span> <span data-ttu-id="4d787-123">O adaptador Ethernet do host pode ter sido removido ou desabilitado.</span><span class="sxs-lookup"><span data-stu-id="4d787-123">The host Ethernet adapter may have been removed or disabled.</span></span><br/> |
| <dl> <span data-ttu-id="4d787-124"><dt>DISP \_ E \_ </dt> <dt>0x80020009</dt> de exceção</span><span class="sxs-lookup"><span data-stu-id="4d787-124"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl>         | <span data-ttu-id="4d787-125">Ocorreu um erro inesperado.</span><span class="sxs-lookup"><span data-stu-id="4d787-125">An unexpected error has occurred.</span></span><br/>                                                                                                                          |



## <a name="remarks"></a><span data-ttu-id="4d787-126">Comentários</span><span class="sxs-lookup"><span data-stu-id="4d787-126">Remarks</span></span>

<span data-ttu-id="4d787-127">O adaptador de rede virtual permite que uma rede virtual se comunique com redes externas.</span><span class="sxs-lookup"><span data-stu-id="4d787-127">The virtual network adapter allows a virtual network to talk to external networks.</span></span> <span data-ttu-id="4d787-128">Normalmente, há um adaptador por adaptador Ethernet instalado no computador host.</span><span class="sxs-lookup"><span data-stu-id="4d787-128">There is normally one adapter per Ethernet adapter installed in the host machine.</span></span> <span data-ttu-id="4d787-129">Por exemplo, digamos que uma máquina host tivesse um adaptador chamado "10/100 ENET".</span><span class="sxs-lookup"><span data-stu-id="4d787-129">For example, let's say a host machine had an adapter labeled "10/100 ENET".</span></span> <span data-ttu-id="4d787-130">Para conectar uma NIC virtual à rede anexada a "10/100 ENET", defina a propriedade **HostAdapter** de rede da rede virtual como "10/100 enet" e conecte a NIC virtual a essa rede virtual.</span><span class="sxs-lookup"><span data-stu-id="4d787-130">To connect a virtual NIC to the network attached to "10/100 ENET", set the virtual network's Network **HostAdapter** property to "10/100 ENET" and connect the virtual NIC to this virtual network.</span></span>

<span data-ttu-id="4d787-131">Se a propriedade **HostAdapter** for definida como uma cadeia de caracteres vazia (""), o adaptador NIC virtual será conectado à rede "rede interna" ou "rede compartilhada (NAT)".</span><span class="sxs-lookup"><span data-stu-id="4d787-131">If the **HostAdapter** property is set to an empty string (""), the virtual NIC adapter is connected to the "Internal Network" or "Shared Networking (NAT)" network.</span></span> <span data-ttu-id="4d787-132">As NICs virtuais conectadas à rede "rede interna" não terão acesso a redes externas no host do sistema.</span><span class="sxs-lookup"><span data-stu-id="4d787-132">Virtual NICs attached to the "Internal Network" network will have no access to external networks on the system host.</span></span> <span data-ttu-id="4d787-133">No entanto, as NICs virtuais conectadas a essa rede virtual ainda podem se comunicar entre si.</span><span class="sxs-lookup"><span data-stu-id="4d787-133">However, the virtual NICs attached to this virtual network are still able to communicate with each other.</span></span>

<span data-ttu-id="4d787-134">A lista completa de adaptadores pode ser acessada por meio da propriedade [**IVMHostInfo:: adaptadores**](ivmhostinfo-networkadapters.md) .</span><span class="sxs-lookup"><span data-stu-id="4d787-134">The complete list of adapters can be accessed through the [**IVMHostInfo::NetworkAdapters**](ivmhostinfo-networkadapters.md) property.</span></span>

## <a name="requirements"></a><span data-ttu-id="4d787-135">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4d787-135">Requirements</span></span>



| <span data-ttu-id="4d787-136">Requisito</span><span class="sxs-lookup"><span data-stu-id="4d787-136">Requirement</span></span> | <span data-ttu-id="4d787-137">Valor</span><span class="sxs-lookup"><span data-stu-id="4d787-137">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="4d787-138">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="4d787-138">Minimum supported client</span></span><br/> | <span data-ttu-id="4d787-139">\[Somente aplicativos de área de trabalho do Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="4d787-139">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="4d787-140">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="4d787-140">Minimum supported server</span></span><br/> | <span data-ttu-id="4d787-141">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="4d787-141">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="4d787-142">Fim do suporte do cliente</span><span class="sxs-lookup"><span data-stu-id="4d787-142">End of client support</span></span><br/>    | <span data-ttu-id="4d787-143">Windows 7</span><span class="sxs-lookup"><span data-stu-id="4d787-143">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="4d787-144">Produto</span><span class="sxs-lookup"><span data-stu-id="4d787-144">Product</span></span><br/>                  | <span data-ttu-id="4d787-145">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="4d787-145">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="4d787-146">parâmetro</span><span class="sxs-lookup"><span data-stu-id="4d787-146">Header</span></span><br/>                   | <dl> <span data-ttu-id="4d787-147"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="4d787-147"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="4d787-148">IID</span><span class="sxs-lookup"><span data-stu-id="4d787-148">IID</span></span><br/>                      | <span data-ttu-id="4d787-149">IID \_ IVMVirtualNetwork é definido como 431cb7a1-2469-4563-b94e-38b987adca63</span><span class="sxs-lookup"><span data-stu-id="4d787-149">IID\_IVMVirtualNetwork is defined as 431cb7a1-2469-4563-b94e-38b987adca63</span></span><br/>          |



## <a name="see-also"></a><span data-ttu-id="4d787-150">Confira também</span><span class="sxs-lookup"><span data-stu-id="4d787-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4d787-151">**IVMVirtualNetwork**</span><span class="sxs-lookup"><span data-stu-id="4d787-151">**IVMVirtualNetwork**</span></span>](ivmvirtualnetwork.md)
</dt> </dl>

 

