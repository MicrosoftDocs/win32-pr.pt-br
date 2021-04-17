---
title: Interface IVMHardDiskConnection (VPCCOMInterfaces. h)
description: Define a conexão para um disco rígido dentro da máquina virtual.
ms.assetid: 7ba1ace5-a3af-4b97-b329-f12a0ecbf7d3
keywords:
- Virtual PC de interface IVMHardDiskConnection
- Virtual PC de interface IVMHardDiskConnection, descrito
topic_type:
- apiref
api_name:
- IVMHardDiskConnection
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7e53a092bdca26eee0c46db1d75f7fc040d5ce7e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105763807"
---
# <a name="ivmharddiskconnection-interface"></a><span data-ttu-id="fc98d-105">Interface IVMHardDiskConnection</span><span class="sxs-lookup"><span data-stu-id="fc98d-105">IVMHardDiskConnection interface</span></span>

<span data-ttu-id="fc98d-106">\[O Windows Virtual PC não está mais disponível para uso a partir do Windows 8.</span><span class="sxs-lookup"><span data-stu-id="fc98d-106">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="fc98d-107">Em vez disso, use o [provedor WMI do Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="fc98d-107">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="fc98d-108">Define a conexão para um disco rígido dentro da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="fc98d-108">Defines the connection for a hard disk within the virtual machine.</span></span> <span data-ttu-id="fc98d-109">Um objeto **IVMHardDiskConnection** é retornado do método [**IVMVirtualMachine:: AddHardDiskConnection**](ivmvirtualmachine-addharddiskconnection.md) .</span><span class="sxs-lookup"><span data-stu-id="fc98d-109">An **IVMHardDiskConnection** object is returned from the [**IVMVirtualMachine::AddHardDiskConnection**](ivmvirtualmachine-addharddiskconnection.md) method.</span></span> <span data-ttu-id="fc98d-110">Você também pode recuperar um objeto **IVMHardDiskConnection** do objeto [**IVMHardDiskConnectionCollection**](ivmharddiskconnectioncollection.md) retornado da propriedade [**IVMVirtualMachine:: HardDiskConnections**](ivmvirtualmachine-harddiskconnections.md) .</span><span class="sxs-lookup"><span data-stu-id="fc98d-110">You can also retrieve an **IVMHardDiskConnection** object from the [**IVMHardDiskConnectionCollection**](ivmharddiskconnectioncollection.md) object returned from the [**IVMVirtualMachine::HardDiskConnections**](ivmvirtualmachine-harddiskconnections.md) property.</span></span>

## <a name="members"></a><span data-ttu-id="fc98d-111">Membros</span><span class="sxs-lookup"><span data-stu-id="fc98d-111">Members</span></span>

<span data-ttu-id="fc98d-112">A interface **IVMHardDiskConnection** herda da interface [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) .</span><span class="sxs-lookup"><span data-stu-id="fc98d-112">The **IVMHardDiskConnection** interface inherits from the [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interface.</span></span> <span data-ttu-id="fc98d-113">**IVMHardDiskConnection** também tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="fc98d-113">**IVMHardDiskConnection** also has these types of members:</span></span>

-   [<span data-ttu-id="fc98d-114">Métodos</span><span class="sxs-lookup"><span data-stu-id="fc98d-114">Methods</span></span>](#methods)
-   [<span data-ttu-id="fc98d-115">Propriedades</span><span class="sxs-lookup"><span data-stu-id="fc98d-115">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="fc98d-116">Métodos</span><span class="sxs-lookup"><span data-stu-id="fc98d-116">Methods</span></span>

<span data-ttu-id="fc98d-117">A interface **IVMHardDiskConnection** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="fc98d-117">The **IVMHardDiskConnection** interface has these methods.</span></span>



| <span data-ttu-id="fc98d-118">Método</span><span class="sxs-lookup"><span data-stu-id="fc98d-118">Method</span></span>                                                         | <span data-ttu-id="fc98d-119">Descrição</span><span class="sxs-lookup"><span data-stu-id="fc98d-119">Description</span></span>                                                           |
|:---------------------------------------------------------------|:----------------------------------------------------------------------|
| [<span data-ttu-id="fc98d-120">**SetBusLocation**</span><span class="sxs-lookup"><span data-stu-id="fc98d-120">**SetBusLocation**</span></span>](ivmharddiskconnection-setbuslocation.md) | <span data-ttu-id="fc98d-121">Define o local do barramento ao qual este disco rígido está anexado.</span><span class="sxs-lookup"><span data-stu-id="fc98d-121">Sets the bus location to which this hard disk is attached.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="fc98d-122">Propriedades</span><span class="sxs-lookup"><span data-stu-id="fc98d-122">Properties</span></span>

<span data-ttu-id="fc98d-123">A interface **IVMHardDiskConnection** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="fc98d-123">The **IVMHardDiskConnection** interface has these properties.</span></span>



| <span data-ttu-id="fc98d-124">Propriedade</span><span class="sxs-lookup"><span data-stu-id="fc98d-124">Property</span></span>                                                              | <span data-ttu-id="fc98d-125">Tipo de acesso</span><span class="sxs-lookup"><span data-stu-id="fc98d-125">Access type</span></span>          | <span data-ttu-id="fc98d-126">Descrição</span><span class="sxs-lookup"><span data-stu-id="fc98d-126">Description</span></span>                                                                       |
|:----------------------------------------------------------------------|:---------------------|:----------------------------------------------------------------------------------|
| [<span data-ttu-id="fc98d-127">**BusNumber**</span><span class="sxs-lookup"><span data-stu-id="fc98d-127">**BusNumber**</span></span>](ivmharddiskconnection-busnumber.md)<br/>       | <span data-ttu-id="fc98d-128">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="fc98d-128">Read-only</span></span><br/> | <span data-ttu-id="fc98d-129">O número do barramento ao qual a imagem da unidade está anexada.</span><span class="sxs-lookup"><span data-stu-id="fc98d-129">The bus number to which the drive image is attached.</span></span><br/>                   |
| [<span data-ttu-id="fc98d-130">**DeviceNumber**</span><span class="sxs-lookup"><span data-stu-id="fc98d-130">**DeviceNumber**</span></span>](ivmharddiskconnection-devicenumber.md)<br/> | <span data-ttu-id="fc98d-131">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="fc98d-131">Read-only</span></span><br/> | <span data-ttu-id="fc98d-132">O número do dispositivo ao qual a imagem da unidade está anexada.</span><span class="sxs-lookup"><span data-stu-id="fc98d-132">The device number to which the drive image is attached.</span></span><br/>                |
| [<span data-ttu-id="fc98d-133">**HD**</span><span class="sxs-lookup"><span data-stu-id="fc98d-133">**HardDisk**</span></span>](ivmharddiskconnection-harddisk.md)<br/>         | <span data-ttu-id="fc98d-134">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="fc98d-134">Read-only</span></span><br/> | <span data-ttu-id="fc98d-135">Um objeto de disco rígido correspondente a essa conexão.</span><span class="sxs-lookup"><span data-stu-id="fc98d-135">A hard disk object corresponding to this connection.</span></span><br/>                   |
| [<span data-ttu-id="fc98d-136">**UndoHardDisk**</span><span class="sxs-lookup"><span data-stu-id="fc98d-136">**UndoHardDisk**</span></span>](ivmharddiskconnection-undoharddisk.md)<br/> | <span data-ttu-id="fc98d-137">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="fc98d-137">Read-only</span></span><br/> | <span data-ttu-id="fc98d-138">Um objeto de disco rígido correspondente à imagem de desfazer disco da conexão.</span><span class="sxs-lookup"><span data-stu-id="fc98d-138">A hard disk object corresponding to this connection's undo disk image.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="fc98d-139">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fc98d-139">Requirements</span></span>



| <span data-ttu-id="fc98d-140">Requisito</span><span class="sxs-lookup"><span data-stu-id="fc98d-140">Requirement</span></span> | <span data-ttu-id="fc98d-141">Valor</span><span class="sxs-lookup"><span data-stu-id="fc98d-141">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="fc98d-142">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="fc98d-142">Minimum supported client</span></span><br/> | <span data-ttu-id="fc98d-143">\[Somente aplicativos de área de trabalho do Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="fc98d-143">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="fc98d-144">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="fc98d-144">Minimum supported server</span></span><br/> | <span data-ttu-id="fc98d-145">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="fc98d-145">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="fc98d-146">Fim do suporte do cliente</span><span class="sxs-lookup"><span data-stu-id="fc98d-146">End of client support</span></span><br/>    | <span data-ttu-id="fc98d-147">Windows 7</span><span class="sxs-lookup"><span data-stu-id="fc98d-147">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="fc98d-148">Produto</span><span class="sxs-lookup"><span data-stu-id="fc98d-148">Product</span></span><br/>                  | <span data-ttu-id="fc98d-149">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="fc98d-149">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="fc98d-150">parâmetro</span><span class="sxs-lookup"><span data-stu-id="fc98d-150">Header</span></span><br/>                   | <dl> <span data-ttu-id="fc98d-151"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="fc98d-151"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="fc98d-152">IID</span><span class="sxs-lookup"><span data-stu-id="fc98d-152">IID</span></span><br/>                      | <span data-ttu-id="fc98d-153">IID \_ IVMHardDiskconnection é definido como aefa36a5-463a-46ae-9e6c-a1fb4e12e671</span><span class="sxs-lookup"><span data-stu-id="fc98d-153">IID\_IVMHardDiskconnection is defined as aefa36a5-463a-46ae-9e6c-a1fb4e12e671</span></span><br/>      |



 

