---
title: Interface IVMNetworkAdapter (VPCCOMInterfaces. h)
description: Serve como a interface para uma placa de interface de rede virtual.
ms.assetid: df050706-09be-47d1-9ae1-1eb0e1836d64
keywords:
- Virtual PC de interface IVMNetworkAdapter
- Virtual PC de interface IVMNetworkAdapter, descrito
topic_type:
- apiref
api_name:
- IVMNetworkAdapter
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 74a0ccf722715896743129b6666609bd8a88df3f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104369661"
---
# <a name="ivmnetworkadapter-interface"></a><span data-ttu-id="fc971-105">Interface IVMNetworkAdapter</span><span class="sxs-lookup"><span data-stu-id="fc971-105">IVMNetworkAdapter interface</span></span>

<span data-ttu-id="fc971-106">\[O Windows Virtual PC não está mais disponível para uso a partir do Windows 8.</span><span class="sxs-lookup"><span data-stu-id="fc971-106">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="fc971-107">Em vez disso, use o [provedor WMI do Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="fc971-107">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="fc971-108">Serve como a interface para uma NIC (placa de interface de rede) virtual.</span><span class="sxs-lookup"><span data-stu-id="fc971-108">Serves as the interface to a virtual network interface card (NIC).</span></span> <span data-ttu-id="fc971-109">Ele é usado para configurar como uma máquina virtual é em rede.</span><span class="sxs-lookup"><span data-stu-id="fc971-109">It is used to set up how a virtual machine is networked.</span></span> <span data-ttu-id="fc971-110">As placas de interface de rede podem ser adicionadas e removidas usando [**IVMVirtualMachine:: AddNetworkAdapter**](ivmvirtualmachine-addnetworkadapter.md) e [**IVMVirtualMachine:: RemoveNetworkAdapter**](ivmvirtualmachine-removenetworkadapter.md).</span><span class="sxs-lookup"><span data-stu-id="fc971-110">Network interface cards can be added and removed by using [**IVMVirtualMachine::AddNetworkAdapter**](ivmvirtualmachine-addnetworkadapter.md) and [**IVMVirtualMachine::RemoveNetworkAdapter**](ivmvirtualmachine-removenetworkadapter.md).</span></span> <span data-ttu-id="fc971-111">Você também pode recuperar um objeto **IVMNetworkAdapter** da coleção [**IVMNetworkAdapterCollection**](ivmnetworkadaptercollection.md) retornada pelas propriedades [**IVMVirtualMachine:: adaptadores**](ivmvirtualmachine-networkadapters.md) ou [**IVMVirtualNetwork:: adaptadores**](ivmvirtualnetwork-networkadapters.md) .</span><span class="sxs-lookup"><span data-stu-id="fc971-111">You can also retrieve an **IVMNetworkAdapter** object from the [**IVMNetworkAdapterCollection**](ivmnetworkadaptercollection.md) collection returned from the [**IVMVirtualMachine::NetworkAdapters**](ivmvirtualmachine-networkadapters.md) or [**IVMVirtualNetwork::NetworkAdapters**](ivmvirtualnetwork-networkadapters.md) properties.</span></span>

## <a name="members"></a><span data-ttu-id="fc971-112">Membros</span><span class="sxs-lookup"><span data-stu-id="fc971-112">Members</span></span>

<span data-ttu-id="fc971-113">A interface **IVMNetworkAdapter** herda da interface [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) .</span><span class="sxs-lookup"><span data-stu-id="fc971-113">The **IVMNetworkAdapter** interface inherits from the [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interface.</span></span> <span data-ttu-id="fc971-114">**IVMNetworkAdapter** também tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="fc971-114">**IVMNetworkAdapter** also has these types of members:</span></span>

-   [<span data-ttu-id="fc971-115">Métodos</span><span class="sxs-lookup"><span data-stu-id="fc971-115">Methods</span></span>](#methods)
-   [<span data-ttu-id="fc971-116">Propriedades</span><span class="sxs-lookup"><span data-stu-id="fc971-116">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="fc971-117">Métodos</span><span class="sxs-lookup"><span data-stu-id="fc971-117">Methods</span></span>

<span data-ttu-id="fc971-118">A interface **IVMNetworkAdapter** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="fc971-118">The **IVMNetworkAdapter** interface has these methods.</span></span>



| <span data-ttu-id="fc971-119">Método</span><span class="sxs-lookup"><span data-stu-id="fc971-119">Method</span></span>                                                                         | <span data-ttu-id="fc971-120">Descrição</span><span class="sxs-lookup"><span data-stu-id="fc971-120">Description</span></span>                                                                 |
|:-------------------------------------------------------------------------------|:----------------------------------------------------------------------------|
| [<span data-ttu-id="fc971-121">**\_SESSÃO**</span><span class="sxs-lookup"><span data-stu-id="fc971-121">**\_ID**</span></span>](ivmnetworkadapter--id.md)                                          | <span data-ttu-id="fc971-122">Recupera o identificador interno desta interface de rede.</span><span class="sxs-lookup"><span data-stu-id="fc971-122">Retrieves the internal identifier of this network interface.</span></span><br/>     |
| [<span data-ttu-id="fc971-123">**AttachToVirtualNetwork**</span><span class="sxs-lookup"><span data-stu-id="fc971-123">**AttachToVirtualNetwork**</span></span>](ivmnetworkadapter-attachtovirtualnetwork.md)     | <span data-ttu-id="fc971-124">Anexa a interface de rede à rede virtual especificada.</span><span class="sxs-lookup"><span data-stu-id="fc971-124">Attaches the network interface to the specified virtual network.</span></span><br/> |
| [<span data-ttu-id="fc971-125">**DetachFromVirtualNetwork**</span><span class="sxs-lookup"><span data-stu-id="fc971-125">**DetachFromVirtualNetwork**</span></span>](ivmnetworkadapter-detachfromvirtualnetwork.md) | <span data-ttu-id="fc971-126">Desanexa a interface de rede de sua rede virtual.</span><span class="sxs-lookup"><span data-stu-id="fc971-126">Detaches the network interface from its virtual network.</span></span><br/>         |



 

### <a name="properties"></a><span data-ttu-id="fc971-127">Propriedades</span><span class="sxs-lookup"><span data-stu-id="fc971-127">Properties</span></span>

<span data-ttu-id="fc971-128">A interface **IVMNetworkAdapter** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="fc971-128">The **IVMNetworkAdapter** interface has these properties.</span></span>



| <span data-ttu-id="fc971-129">Propriedade</span><span class="sxs-lookup"><span data-stu-id="fc971-129">Property</span></span>                                                                                  | <span data-ttu-id="fc971-130">Tipo de acesso</span><span class="sxs-lookup"><span data-stu-id="fc971-130">Access type</span></span>           | <span data-ttu-id="fc971-131">Descrição</span><span class="sxs-lookup"><span data-stu-id="fc971-131">Description</span></span>                                                                 |
|:------------------------------------------------------------------------------------------|:----------------------|:----------------------------------------------------------------------------|
| [<span data-ttu-id="fc971-132">**EthernetAddress**</span><span class="sxs-lookup"><span data-stu-id="fc971-132">**EthernetAddress**</span></span>](ivmnetworkadapter-ethernetaddress.md)<br/>                   | <span data-ttu-id="fc971-133">Leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="fc971-133">Read/write</span></span><br/> | <span data-ttu-id="fc971-134">O endereço Ethernet (MAC) da interface de rede.</span><span class="sxs-lookup"><span data-stu-id="fc971-134">The Ethernet (MAC) address of the network interface.</span></span><br/>             |
| [<span data-ttu-id="fc971-135">**IsEthernetAddressDynamic**</span><span class="sxs-lookup"><span data-stu-id="fc971-135">**IsEthernetAddressDynamic**</span></span>](ivmnetworkadapter-isethernetaddressdynamic.md)<br/> | <span data-ttu-id="fc971-136">Leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="fc971-136">Read/write</span></span><br/> | <span data-ttu-id="fc971-137">Indica se o endereço Ethernet é gerado dinamicamente.</span><span class="sxs-lookup"><span data-stu-id="fc971-137">Indicates whether the Ethernet address is dynamically generated.</span></span><br/> |
| [<span data-ttu-id="fc971-138">**VirtualMachine**</span><span class="sxs-lookup"><span data-stu-id="fc971-138">**VirtualMachine**</span></span>](ivmnetworkadapter-virtualmachine.md)<br/>                     | <span data-ttu-id="fc971-139">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="fc971-139">Read-only</span></span><br/>  | <span data-ttu-id="fc971-140">A máquina virtual associada a esta interface de rede.</span><span class="sxs-lookup"><span data-stu-id="fc971-140">The virtual machine associated with this network interface.</span></span><br/>      |
| [<span data-ttu-id="fc971-141">**VirtualNetwork**</span><span class="sxs-lookup"><span data-stu-id="fc971-141">**VirtualNetwork**</span></span>](ivmnetworkadapter-virtualnetwork.md)<br/>                     | <span data-ttu-id="fc971-142">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="fc971-142">Read-only</span></span><br/>  | <span data-ttu-id="fc971-143">A rede virtual à qual a interface de rede está conectada.</span><span class="sxs-lookup"><span data-stu-id="fc971-143">The virtual network to which the network interface is attached.</span></span><br/>  |



 

## <a name="remarks"></a><span data-ttu-id="fc971-144">Comentários</span><span class="sxs-lookup"><span data-stu-id="fc971-144">Remarks</span></span>

<span data-ttu-id="fc971-145">O endereço Ethernet padrão para uma interface de rede é "00-00-00-00-00-00", que é considerado um endereço Ethernet inválido pela maioria dos sistemas operacionais.</span><span class="sxs-lookup"><span data-stu-id="fc971-145">The default Ethernet address for a network interface is "00-00-00-00-00-00", which is considered an invalid Ethernet address by most operating systems.</span></span> <span data-ttu-id="fc971-146">Se [**IsEthernetAddressDynamic**](ivmnetworkadapter-isethernetaddressdynamic.md) for definido como **false**, [**EthernetAddress**](ivmnetworkadapter-ethernetaddress.md) deverá ser inicializado com um endereço de rede Ethernet válido.</span><span class="sxs-lookup"><span data-stu-id="fc971-146">If [**IsEthernetAddressDynamic**](ivmnetworkadapter-isethernetaddressdynamic.md) is set to **FALSE**, [**EthernetAddress**](ivmnetworkadapter-ethernetaddress.md) must be initialized with a valid Ethernet network address.</span></span>

<span data-ttu-id="fc971-147">Os procedimentos a seguir explicam como usar a interface **IVMNetworkAdapter** .</span><span class="sxs-lookup"><span data-stu-id="fc971-147">The following procedures explain how to use the **IVMNetworkAdapter** interface.</span></span>

<span data-ttu-id="fc971-148">**Para anexar uma NIC virtual a uma NIC de host**</span><span class="sxs-lookup"><span data-stu-id="fc971-148">**To attach a virtual NIC to a host NIC**</span></span>

-   <span data-ttu-id="fc971-149">NICs virtuais (convidados) não são anexadas diretamente a uma NIC de host.</span><span class="sxs-lookup"><span data-stu-id="fc971-149">Virtual (guest) NICs are not attached directly to a host NIC.</span></span> <span data-ttu-id="fc971-150">Em vez disso, a NIC virtual é anexada a uma rede virtual anexada a uma NIC de host.</span><span class="sxs-lookup"><span data-stu-id="fc971-150">Instead, the virtual NIC is attached to a virtual network that is attached to a host NIC.</span></span> <span data-ttu-id="fc971-151">Para obter mais informações sobre como configurar redes virtuais, consulte [**IVMVirtualNetwork**](ivmvirtualnetwork.md).</span><span class="sxs-lookup"><span data-stu-id="fc971-151">For more information about configuring virtual networks, see [**IVMVirtualNetwork**](ivmvirtualnetwork.md).</span></span> <span data-ttu-id="fc971-152">Para anexar a NIC virtual a uma rede virtual, use o método [**AttachToVirtualNetwork**](ivmnetworkadapter-attachtovirtualnetwork.md) .</span><span class="sxs-lookup"><span data-stu-id="fc971-152">To attach the virtual NIC to a virtual network, use the [**AttachToVirtualNetwork**](ivmnetworkadapter-attachtovirtualnetwork.md) method.</span></span>

<span data-ttu-id="fc971-153">**Para desconectar uma NIC virtual da rede virtual**</span><span class="sxs-lookup"><span data-stu-id="fc971-153">**To disconnect a virtual NIC from the virtual network**</span></span>

-   <span data-ttu-id="fc971-154">O método [**DetachFromVirtualNetwork**](ivmnetworkadapter-detachfromvirtualnetwork.md) desanexará a NIC virtual da rede virtual.</span><span class="sxs-lookup"><span data-stu-id="fc971-154">The [**DetachFromVirtualNetwork**](ivmnetworkadapter-detachfromvirtualnetwork.md) method will detach the virtual NIC from the virtual network.</span></span> <span data-ttu-id="fc971-155">Depois que essa função for chamada, a propriedade [**VirtualNetwork**](ivmnetworkadapter-virtualnetwork.md) retornará uma ID de rede virtual que não é válida.</span><span class="sxs-lookup"><span data-stu-id="fc971-155">After this function is called, the [**VirtualNetwork**](ivmnetworkadapter-virtualnetwork.md) property will return a virtual network ID that is not valid.</span></span>

<span data-ttu-id="fc971-156">**Para remover uma NIC virtual de uma máquina virtual se você tiver o objeto NIC virtual**</span><span class="sxs-lookup"><span data-stu-id="fc971-156">**To remove a virtual NIC from a virtual machine if you have the virtual NIC object**</span></span>

1.  <span data-ttu-id="fc971-157">Obtenha a máquina virtual associada à NIC virtual usando a propriedade [**VirtualMachine**](ivmnetworkadapter-virtualmachine.md) .</span><span class="sxs-lookup"><span data-stu-id="fc971-157">Get the virtual machine associated with the virtual NIC by using the [**VirtualMachine**](ivmnetworkadapter-virtualmachine.md) property.</span></span>
2.  <span data-ttu-id="fc971-158">Use o objeto atual como um parâmetro para o método [**IVMVirtualMachine:: RemoveNetworkAdapter**](ivmvirtualmachine-removenetworkadapter.md) .</span><span class="sxs-lookup"><span data-stu-id="fc971-158">Use the current object as a parameter to the [**IVMVirtualMachine::RemoveNetworkAdapter**](ivmvirtualmachine-removenetworkadapter.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="fc971-159">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fc971-159">Requirements</span></span>



| <span data-ttu-id="fc971-160">Requisito</span><span class="sxs-lookup"><span data-stu-id="fc971-160">Requirement</span></span> | <span data-ttu-id="fc971-161">Valor</span><span class="sxs-lookup"><span data-stu-id="fc971-161">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="fc971-162">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="fc971-162">Minimum supported client</span></span><br/> | <span data-ttu-id="fc971-163">\[Somente aplicativos de área de trabalho do Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="fc971-163">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="fc971-164">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="fc971-164">Minimum supported server</span></span><br/> | <span data-ttu-id="fc971-165">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="fc971-165">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="fc971-166">Fim do suporte do cliente</span><span class="sxs-lookup"><span data-stu-id="fc971-166">End of client support</span></span><br/>    | <span data-ttu-id="fc971-167">Windows 7</span><span class="sxs-lookup"><span data-stu-id="fc971-167">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="fc971-168">Produto</span><span class="sxs-lookup"><span data-stu-id="fc971-168">Product</span></span><br/>                  | <span data-ttu-id="fc971-169">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="fc971-169">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="fc971-170">parâmetro</span><span class="sxs-lookup"><span data-stu-id="fc971-170">Header</span></span><br/>                   | <dl> <span data-ttu-id="fc971-171"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="fc971-171"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="fc971-172">IID</span><span class="sxs-lookup"><span data-stu-id="fc971-172">IID</span></span><br/>                      | <span data-ttu-id="fc971-173">IID \_ IVMNetworkAdapter é definido como e32e4165-22b8-4DC0-8d57-850171ae207a</span><span class="sxs-lookup"><span data-stu-id="fc971-173">IID\_IVMNetworkAdapter is defined as e32e4165-22b8-4dc0-8d57-850171ae207a</span></span><br/>          |



 

