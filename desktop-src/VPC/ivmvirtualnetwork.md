---
title: Interface IVMVirtualNetwork (VPCCOMInterfaces. h)
description: Define uma rede virtual.
ms.assetid: 1ddafc33-05d4-45fb-924d-9830288aa240
keywords:
- Virtual PC de interface IVMVirtualNetwork
- Virtual PC de interface IVMVirtualNetwork, descrito
topic_type:
- apiref
api_name:
- IVMVirtualNetwork
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 06fb7c759059034874890f1dba7f7e2d1280ea8a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105764008"
---
# <a name="ivmvirtualnetwork-interface"></a><span data-ttu-id="3aab0-105">Interface IVMVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="3aab0-105">IVMVirtualNetwork interface</span></span>

<span data-ttu-id="3aab0-106">\[O Windows Virtual PC não está mais disponível para uso a partir do Windows 8.</span><span class="sxs-lookup"><span data-stu-id="3aab0-106">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="3aab0-107">Em vez disso, use o [provedor WMI do Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="3aab0-107">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="3aab0-108">Define uma rede virtual.</span><span class="sxs-lookup"><span data-stu-id="3aab0-108">Defines a virtual network.</span></span> <span data-ttu-id="3aab0-109">Os objetos **IVMVirtualNetwork** são retornados do método [**IVMVirtualPC**](ivmvirtualpc.md) [**FindVirtualNetwork**](ivmvirtualpc-findvirtualnetwork.md).</span><span class="sxs-lookup"><span data-stu-id="3aab0-109">**IVMVirtualNetwork** objects are returned from [**IVMVirtualPC**](ivmvirtualpc.md) method [**FindVirtualNetwork**](ivmvirtualpc-findvirtualnetwork.md).</span></span> <span data-ttu-id="3aab0-110">Você também pode recuperar um objeto **IVMVirtualNetwork** do objeto [**IVMVirtualNetworkCollection**](ivmvirtualnetworkcollection.md) retornado da propriedade [**IVMVirtualPC:: VirtualNetworks**](ivmvirtualpc-virtualnetworks.md) .</span><span class="sxs-lookup"><span data-stu-id="3aab0-110">You can also retrieve an **IVMVirtualNetwork** object from the [**IVMVirtualNetworkCollection**](ivmvirtualnetworkcollection.md) object returned from the [**IVMVirtualPC::VirtualNetworks**](ivmvirtualpc-virtualnetworks.md) property.</span></span>

<span data-ttu-id="3aab0-111">Uma rede virtual consiste em um comutador virtual, que executa todo o roteamento interno e várias conexões que estão "conectadas" ao comutador virtual.</span><span class="sxs-lookup"><span data-stu-id="3aab0-111">A virtual network consists of a virtual switch, which performs all internal routing, and several connections that are "plugged in" to the virtual switch.</span></span> <span data-ttu-id="3aab0-112">Essas conexões podem ser uma conexão de host externo real, uma "rede interna" ou uma rede compartilhada (NAT).</span><span class="sxs-lookup"><span data-stu-id="3aab0-112">These connections can be a real external host connection, an "internal network" or shared networking (NAT).</span></span>

## <a name="members"></a><span data-ttu-id="3aab0-113">Membros</span><span class="sxs-lookup"><span data-stu-id="3aab0-113">Members</span></span>

<span data-ttu-id="3aab0-114">A interface **IVMVirtualNetwork** herda da interface [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) .</span><span class="sxs-lookup"><span data-stu-id="3aab0-114">The **IVMVirtualNetwork** interface inherits from the [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interface.</span></span> <span data-ttu-id="3aab0-115">**IVMVirtualNetwork** também tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="3aab0-115">**IVMVirtualNetwork** also has these types of members:</span></span>

-   [<span data-ttu-id="3aab0-116">Métodos</span><span class="sxs-lookup"><span data-stu-id="3aab0-116">Methods</span></span>](#methods)
-   [<span data-ttu-id="3aab0-117">Propriedades</span><span class="sxs-lookup"><span data-stu-id="3aab0-117">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="3aab0-118">Métodos</span><span class="sxs-lookup"><span data-stu-id="3aab0-118">Methods</span></span>

<span data-ttu-id="3aab0-119">A interface **IVMVirtualNetwork** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="3aab0-119">The **IVMVirtualNetwork** interface has these methods.</span></span>



| <span data-ttu-id="3aab0-120">Método</span><span class="sxs-lookup"><span data-stu-id="3aab0-120">Method</span></span>                                | <span data-ttu-id="3aab0-121">Descrição</span><span class="sxs-lookup"><span data-stu-id="3aab0-121">Description</span></span>                                                          |
|:--------------------------------------|:---------------------------------------------------------------------|
| [<span data-ttu-id="3aab0-122">**\_ID**</span><span class="sxs-lookup"><span data-stu-id="3aab0-122">**\_ID**</span></span>](ivmvirtualnetwork--id.md) | <span data-ttu-id="3aab0-123">Recupera o identificador interno da rede virtual.</span><span class="sxs-lookup"><span data-stu-id="3aab0-123">Retrieves the internal identifier of the virtual network.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="3aab0-124">Propriedades</span><span class="sxs-lookup"><span data-stu-id="3aab0-124">Properties</span></span>

<span data-ttu-id="3aab0-125">A interface **IVMVirtualNetwork** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="3aab0-125">The **IVMVirtualNetwork** interface has these properties.</span></span>



| <span data-ttu-id="3aab0-126">Propriedade</span><span class="sxs-lookup"><span data-stu-id="3aab0-126">Property</span></span>                                                                | <span data-ttu-id="3aab0-127">Tipo de acesso</span><span class="sxs-lookup"><span data-stu-id="3aab0-127">Access type</span></span>          | <span data-ttu-id="3aab0-128">Descrição</span><span class="sxs-lookup"><span data-stu-id="3aab0-128">Description</span></span>                                                                    |
|:------------------------------------------------------------------------|:---------------------|:-------------------------------------------------------------------------------|
| [<span data-ttu-id="3aab0-129">**HostAdapter**</span><span class="sxs-lookup"><span data-stu-id="3aab0-129">**HostAdapter**</span></span>](ivmvirtualnetwork-hostadapter.md)<br/>         | <span data-ttu-id="3aab0-130">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="3aab0-130">Read-only</span></span><br/> | <span data-ttu-id="3aab0-131">O nome do adaptador ao qual a rede virtual está conectada.</span><span class="sxs-lookup"><span data-stu-id="3aab0-131">The name of the adapter to which the virtual network is connected.</span></span><br/>  |
| <span data-ttu-id="3aab0-132">[**MediaType**](/previous-versions/windows/desktop/legacy/dd796707(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="3aab0-132">[**MediaType**](/previous-versions/windows/desktop/legacy/dd796707(v=vs.85))</span></span><br/>             | <span data-ttu-id="3aab0-133">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="3aab0-133">Read-only</span></span><br/> | <span data-ttu-id="3aab0-134">Determina se a instância de rede virtual é sem fio ou não.</span><span class="sxs-lookup"><span data-stu-id="3aab0-134">Determines whether the virtual network instance is wireless or not.</span></span><br/> |
| [<span data-ttu-id="3aab0-135">**Nome**</span><span class="sxs-lookup"><span data-stu-id="3aab0-135">**Name**</span></span>](ivmvirtualnetwork-name.md)<br/>                       | <span data-ttu-id="3aab0-136">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="3aab0-136">Read-only</span></span><br/> | <span data-ttu-id="3aab0-137">O nome exclusivo da instância de rede virtual.</span><span class="sxs-lookup"><span data-stu-id="3aab0-137">The unique name of the virtual network instance.</span></span><br/>                    |
| [<span data-ttu-id="3aab0-138">**Adaptadores**</span><span class="sxs-lookup"><span data-stu-id="3aab0-138">**NetworkAdapters**</span></span>](ivmvirtualnetwork-networkadapters.md)<br/> | <span data-ttu-id="3aab0-139">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="3aab0-139">Read-only</span></span><br/> | <span data-ttu-id="3aab0-140">Uma coleção enumerável de NICs anexadas à rede virtual.</span><span class="sxs-lookup"><span data-stu-id="3aab0-140">An enumerable collection of NICs attached to the virtual network.</span></span><br/>   |



 

## <a name="requirements"></a><span data-ttu-id="3aab0-141">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3aab0-141">Requirements</span></span>



| <span data-ttu-id="3aab0-142">Requisito</span><span class="sxs-lookup"><span data-stu-id="3aab0-142">Requirement</span></span> | <span data-ttu-id="3aab0-143">Valor</span><span class="sxs-lookup"><span data-stu-id="3aab0-143">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="3aab0-144">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3aab0-144">Minimum supported client</span></span><br/> | <span data-ttu-id="3aab0-145">\[Somente aplicativos de área de trabalho do Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="3aab0-145">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="3aab0-146">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3aab0-146">Minimum supported server</span></span><br/> | <span data-ttu-id="3aab0-147">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="3aab0-147">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="3aab0-148">Fim do suporte do cliente</span><span class="sxs-lookup"><span data-stu-id="3aab0-148">End of client support</span></span><br/>    | <span data-ttu-id="3aab0-149">Windows 7</span><span class="sxs-lookup"><span data-stu-id="3aab0-149">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="3aab0-150">Produto</span><span class="sxs-lookup"><span data-stu-id="3aab0-150">Product</span></span><br/>                  | <span data-ttu-id="3aab0-151">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="3aab0-151">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="3aab0-152">parâmetro</span><span class="sxs-lookup"><span data-stu-id="3aab0-152">Header</span></span><br/>                   | <dl> <span data-ttu-id="3aab0-153"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="3aab0-153"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="3aab0-154">IID</span><span class="sxs-lookup"><span data-stu-id="3aab0-154">IID</span></span><br/>                      | <span data-ttu-id="3aab0-155">IID \_ IVMVirtualNetwork é definido como 431cb7a1-2469-4563-b94e-38b987adca63</span><span class="sxs-lookup"><span data-stu-id="3aab0-155">IID\_IVMVirtualNetwork is defined as 431cb7a1-2469-4563-b94e-38b987adca63</span></span><br/>          |



 

