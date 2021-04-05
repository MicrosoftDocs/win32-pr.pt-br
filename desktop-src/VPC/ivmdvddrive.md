---
title: Interface IVMDVDDrive (VPCCOMInterfaces. h)
description: Controla uma unidade de CD-ROM ou DVD-ROM em uma máquina virtual. IVMDVDDrive pode notificar clientes sobre eventos usando a interface de saída do IVMDVDDriveEvents.
ms.assetid: 0900b3a8-ba52-4c26-bd96-b37334d6d03c
keywords:
- Virtual PC de interface IVMDVDDrive
- Virtual PC de interface IVMDVDDrive, descrito
topic_type:
- apiref
api_name:
- IVMDVDDrive
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 951213923f74f8425fc4d9eaec85e76f7481eeb9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104009504"
---
# <a name="ivmdvddrive-interface"></a><span data-ttu-id="246ad-106">Interface IVMDVDDrive</span><span class="sxs-lookup"><span data-stu-id="246ad-106">IVMDVDDrive interface</span></span>

<span data-ttu-id="246ad-107">\[O Windows Virtual PC não está mais disponível para uso a partir do Windows 8.</span><span class="sxs-lookup"><span data-stu-id="246ad-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="246ad-108">Em vez disso, use o [provedor WMI do Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="246ad-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="246ad-109">Controla uma unidade de CD-ROM ou DVD-ROM em uma máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="246ad-109">Controls a CD-ROM or DVD-ROM drive within a virtual machine.</span></span> <span data-ttu-id="246ad-110">**IVMDVDDrive** pode notificar clientes sobre eventos usando a interface de saída do [**IVMDVDDriveEvents**](ivmdvddriveevents.md) .</span><span class="sxs-lookup"><span data-stu-id="246ad-110">**IVMDVDDrive** can notify clients about events using the [**IVMDVDDriveEvents**](ivmdvddriveevents.md) outgoing interface.</span></span>

<span data-ttu-id="246ad-111">Você pode adicionar uma nova unidade de CD-ROM ou DVD-ROM a uma máquina virtual usando o método [**IVMVirtualMachine:: AddDVDROMDrive**](ivmvirtualmachine-adddvdromdrive.md) .</span><span class="sxs-lookup"><span data-stu-id="246ad-111">You can add a new CD-ROM or DVD-ROM drive to a virtual machine using the [**IVMVirtualMachine::AddDVDROMDrive**](ivmvirtualmachine-adddvdromdrive.md) method.</span></span> <span data-ttu-id="246ad-112">Você pode remover uma unidade de CD-ROM ou DVD-ROM existente de uma máquina virtual usando o método [**IVMVirtualMachine:: RemoveDVDROMDrive**](ivmvirtualmachine-removedvdromdrive.md) .</span><span class="sxs-lookup"><span data-stu-id="246ad-112">You can remove an existing CD-ROM or DVD-ROM drive from a virtual machine using the [**IVMVirtualMachine::RemoveDVDROMDrive**](ivmvirtualmachine-removedvdromdrive.md) method.</span></span> <span data-ttu-id="246ad-113">Você pode recuperar um objeto **IVMDVDDrive** do objeto [**IVMDVDDriveCollection**](ivmdvddrivecollection.md) retornado da propriedade [**IVMVirtualMachine::D vdromdrives**](ivmvirtualmachine-dvdromdrives.md) .</span><span class="sxs-lookup"><span data-stu-id="246ad-113">You can retrieve an **IVMDVDDrive** object from the [**IVMDVDDriveCollection**](ivmdvddrivecollection.md) object returned from the [**IVMVirtualMachine::DVDROMDrives**](ivmvirtualmachine-dvdromdrives.md) property.</span></span>

## <a name="members"></a><span data-ttu-id="246ad-114">Membros</span><span class="sxs-lookup"><span data-stu-id="246ad-114">Members</span></span>

<span data-ttu-id="246ad-115">A interface **IVMDVDDrive** herda da interface [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) .</span><span class="sxs-lookup"><span data-stu-id="246ad-115">The **IVMDVDDrive** interface inherits from the [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interface.</span></span> <span data-ttu-id="246ad-116">**IVMDVDDrive** também tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="246ad-116">**IVMDVDDrive** also has these types of members:</span></span>

-   [<span data-ttu-id="246ad-117">Métodos</span><span class="sxs-lookup"><span data-stu-id="246ad-117">Methods</span></span>](#methods)
-   [<span data-ttu-id="246ad-118">Propriedades</span><span class="sxs-lookup"><span data-stu-id="246ad-118">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="246ad-119">Métodos</span><span class="sxs-lookup"><span data-stu-id="246ad-119">Methods</span></span>

<span data-ttu-id="246ad-120">A interface **IVMDVDDrive** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="246ad-120">The **IVMDVDDrive** interface has these methods.</span></span>



| <span data-ttu-id="246ad-121">Método</span><span class="sxs-lookup"><span data-stu-id="246ad-121">Method</span></span>                                                   | <span data-ttu-id="246ad-122">Descrição</span><span class="sxs-lookup"><span data-stu-id="246ad-122">Description</span></span>                                                                             |
|:---------------------------------------------------------|:----------------------------------------------------------------------------------------|
| [<span data-ttu-id="246ad-123">**AttachHostDrive**</span><span class="sxs-lookup"><span data-stu-id="246ad-123">**AttachHostDrive**</span></span>](ivmdvddrive-attachhostdrive.md)   | <span data-ttu-id="246ad-124">Anexa uma unidade de host à unidade de DVD na máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="246ad-124">Attaches a host drive to the DVD drive within the virtual machine.</span></span><br/>           |
| [<span data-ttu-id="246ad-125">**AttachImage**</span><span class="sxs-lookup"><span data-stu-id="246ad-125">**AttachImage**</span></span>](ivmdvddrive-attachimage.md)           | <span data-ttu-id="246ad-126">Anexa uma imagem ISO à unidade de DVD na máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="246ad-126">Attaches an ISO image to the DVD drive within the virtual machine.</span></span><br/>           |
| [<span data-ttu-id="246ad-127">**ReleaseHostDrive**</span><span class="sxs-lookup"><span data-stu-id="246ad-127">**ReleaseHostDrive**</span></span>](ivmdvddrive-releasehostdrive.md) | <span data-ttu-id="246ad-128">Libera uma unidade de host capturada da unidade de DVD.</span><span class="sxs-lookup"><span data-stu-id="246ad-128">Releases a captured host drive from the DVD drive.</span></span><br/>                           |
| [<span data-ttu-id="246ad-129">**ReleaseImage**</span><span class="sxs-lookup"><span data-stu-id="246ad-129">**ReleaseImage**</span></span>](ivmdvddrive-releaseimage.md)         | <span data-ttu-id="246ad-130">Libera uma imagem ISO capturada da unidade de DVD.</span><span class="sxs-lookup"><span data-stu-id="246ad-130">Releases a captured ISO image from the DVD drive.</span></span><br/>                            |
| [<span data-ttu-id="246ad-131">**SetBusLocation**</span><span class="sxs-lookup"><span data-stu-id="246ad-131">**SetBusLocation**</span></span>](ivmdvddrive-setbuslocation.md)     | <span data-ttu-id="246ad-132">Anexa a unidade de DVD ao local do barramento especificado na máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="246ad-132">Attaches the DVD drive to the specified bus location in the virtual machine.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="246ad-133">Propriedades</span><span class="sxs-lookup"><span data-stu-id="246ad-133">Properties</span></span>

<span data-ttu-id="246ad-134">A interface **IVMDVDDrive** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="246ad-134">The **IVMDVDDrive** interface has these properties.</span></span>



| <span data-ttu-id="246ad-135">Propriedade</span><span class="sxs-lookup"><span data-stu-id="246ad-135">Property</span></span>                                                          | <span data-ttu-id="246ad-136">Tipo de acesso</span><span class="sxs-lookup"><span data-stu-id="246ad-136">Access type</span></span>          | <span data-ttu-id="246ad-137">Descrição</span><span class="sxs-lookup"><span data-stu-id="246ad-137">Description</span></span>                                                                        |
|:------------------------------------------------------------------|:---------------------|:-----------------------------------------------------------------------------------|
| [<span data-ttu-id="246ad-138">**Anexo**</span><span class="sxs-lookup"><span data-stu-id="246ad-138">**Attachment**</span></span>](ivmdvddrive-attachment.md)<br/>           | <span data-ttu-id="246ad-139">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="246ad-139">Read-only</span></span><br/> | <span data-ttu-id="246ad-140">O tipo de mídia anexada à unidade de DVD na máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="246ad-140">The type of media attached to the DVD drive within the virtual machine.</span></span><br/> |
| [<span data-ttu-id="246ad-141">**BusNumber**</span><span class="sxs-lookup"><span data-stu-id="246ad-141">**BusNumber**</span></span>](ivmdvddrive-busnumber.md)<br/>             | <span data-ttu-id="246ad-142">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="246ad-142">Read-only</span></span><br/> | <span data-ttu-id="246ad-143">O número do barramento ao qual este dispositivo está anexado.</span><span class="sxs-lookup"><span data-stu-id="246ad-143">The bus number to which this device is attached.</span></span><br/>                        |
| [<span data-ttu-id="246ad-144">**DeviceNumber**</span><span class="sxs-lookup"><span data-stu-id="246ad-144">**DeviceNumber**</span></span>](ivmdvddrive-devicenumber.md)<br/>       | <span data-ttu-id="246ad-145">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="246ad-145">Read-only</span></span><br/> | <span data-ttu-id="246ad-146">O número do dispositivo ao qual esta unidade está anexada.</span><span class="sxs-lookup"><span data-stu-id="246ad-146">The device number to which this drive is attached.</span></span><br/>                      |
| [<span data-ttu-id="246ad-147">**HostDriveLetter**</span><span class="sxs-lookup"><span data-stu-id="246ad-147">**HostDriveLetter**</span></span>](ivmdvddrive-hostdriveletter.md)<br/> | <span data-ttu-id="246ad-148">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="246ad-148">Read-only</span></span><br/> | <span data-ttu-id="246ad-149">A letra da unidade do host definida para este dispositivo.</span><span class="sxs-lookup"><span data-stu-id="246ad-149">The letter of the host drive set for this device.</span></span><br/>                       |
| [<span data-ttu-id="246ad-150">**ImageFile**</span><span class="sxs-lookup"><span data-stu-id="246ad-150">**ImageFile**</span></span>](ivmdvddrive-imagefile.md)<br/>             | <span data-ttu-id="246ad-151">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="246ad-151">Read-only</span></span><br/> | <span data-ttu-id="246ad-152">O caminho completo do conjunto de arquivos de imagem para este dispositivo.</span><span class="sxs-lookup"><span data-stu-id="246ad-152">The full path of the image file set for this device.</span></span><br/>                    |



 

## <a name="requirements"></a><span data-ttu-id="246ad-153">Requisitos</span><span class="sxs-lookup"><span data-stu-id="246ad-153">Requirements</span></span>



| <span data-ttu-id="246ad-154">Requisito</span><span class="sxs-lookup"><span data-stu-id="246ad-154">Requirement</span></span> | <span data-ttu-id="246ad-155">Valor</span><span class="sxs-lookup"><span data-stu-id="246ad-155">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="246ad-156">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="246ad-156">Minimum supported client</span></span><br/> | <span data-ttu-id="246ad-157">\[Somente aplicativos de área de trabalho do Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="246ad-157">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="246ad-158">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="246ad-158">Minimum supported server</span></span><br/> | <span data-ttu-id="246ad-159">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="246ad-159">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="246ad-160">Fim do suporte do cliente</span><span class="sxs-lookup"><span data-stu-id="246ad-160">End of client support</span></span><br/>    | <span data-ttu-id="246ad-161">Windows 7</span><span class="sxs-lookup"><span data-stu-id="246ad-161">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="246ad-162">Produto</span><span class="sxs-lookup"><span data-stu-id="246ad-162">Product</span></span><br/>                  | <span data-ttu-id="246ad-163">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="246ad-163">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="246ad-164">parâmetro</span><span class="sxs-lookup"><span data-stu-id="246ad-164">Header</span></span><br/>                   | <dl> <span data-ttu-id="246ad-165"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="246ad-165"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="246ad-166">IID</span><span class="sxs-lookup"><span data-stu-id="246ad-166">IID</span></span><br/>                      | <span data-ttu-id="246ad-167">IID \_ IVMDVDDrive é definido como b96328f6-6732-437d-a00d-ffa47e43971c</span><span class="sxs-lookup"><span data-stu-id="246ad-167">IID\_IVMDVDDrive is defined as b96328f6-6732-437d-a00d-ffa47e43971c</span></span><br/>                |



 

