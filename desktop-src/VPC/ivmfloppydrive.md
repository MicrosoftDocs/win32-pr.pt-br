---
title: Interface IVMFloppyDrive (VPCCOMInterfaces. h)
description: Controla uma unidade de disquete em uma máquina virtual.
ms.assetid: b652182a-27ae-4390-81b1-b644a82924df
keywords:
- Virtual PC de interface IVMFloppyDrive
- Virtual PC de interface IVMFloppyDrive, descrito
topic_type:
- apiref
api_name:
- IVMFloppyDrive
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bab1034bc56c5fe10bb12941bd99309e13e22dca
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103919002"
---
# <a name="ivmfloppydrive-interface"></a><span data-ttu-id="02dae-105">Interface IVMFloppyDrive</span><span class="sxs-lookup"><span data-stu-id="02dae-105">IVMFloppyDrive interface</span></span>

<span data-ttu-id="02dae-106">\[O Windows Virtual PC não está mais disponível para uso a partir do Windows 8.</span><span class="sxs-lookup"><span data-stu-id="02dae-106">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="02dae-107">Em vez disso, use o [provedor WMI do Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="02dae-107">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="02dae-108">Controla uma unidade de disquete em uma máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="02dae-108">Controls a floppy drive within a virtual machine.</span></span> <span data-ttu-id="02dae-109">**IVMFloppyDrive** pode notificar clientes sobre eventos usando a interface de saída do [**IVMFloppyDriveEvents**](ivmfloppydriveevents.md) .</span><span class="sxs-lookup"><span data-stu-id="02dae-109">**IVMFloppyDrive** can notify clients about events using the [**IVMFloppyDriveEvents**](ivmfloppydriveevents.md) outgoing interface.</span></span> <span data-ttu-id="02dae-110">Você pode recuperar um objeto **IVMFloppyDrive** do objeto [**IVMFloppyDriveCollection**](ivmfloppydrivecollection.md) retornado da propriedade [**IVMVirtualMachine:: FloppyDrives**](ivmvirtualmachine-floppydrives.md) .</span><span class="sxs-lookup"><span data-stu-id="02dae-110">You can retrieve an **IVMFloppyDrive** object from the [**IVMFloppyDriveCollection**](ivmfloppydrivecollection.md) object returned from the [**IVMVirtualMachine::FloppyDrives**](ivmvirtualmachine-floppydrives.md) property.</span></span>

## <a name="members"></a><span data-ttu-id="02dae-111">Membros</span><span class="sxs-lookup"><span data-stu-id="02dae-111">Members</span></span>

<span data-ttu-id="02dae-112">A interface **IVMFloppyDrive** herda da interface [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) .</span><span class="sxs-lookup"><span data-stu-id="02dae-112">The **IVMFloppyDrive** interface inherits from the [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interface.</span></span> <span data-ttu-id="02dae-113">**IVMFloppyDrive** também tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="02dae-113">**IVMFloppyDrive** also has these types of members:</span></span>

-   [<span data-ttu-id="02dae-114">Métodos</span><span class="sxs-lookup"><span data-stu-id="02dae-114">Methods</span></span>](#methods)
-   [<span data-ttu-id="02dae-115">Propriedades</span><span class="sxs-lookup"><span data-stu-id="02dae-115">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="02dae-116">Métodos</span><span class="sxs-lookup"><span data-stu-id="02dae-116">Methods</span></span>

<span data-ttu-id="02dae-117">A interface **IVMFloppyDrive** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="02dae-117">The **IVMFloppyDrive** interface has these methods.</span></span>



| <span data-ttu-id="02dae-118">Método</span><span class="sxs-lookup"><span data-stu-id="02dae-118">Method</span></span>                                                      | <span data-ttu-id="02dae-119">Descrição</span><span class="sxs-lookup"><span data-stu-id="02dae-119">Description</span></span>                                                                                  |
|:------------------------------------------------------------|:---------------------------------------------------------------------------------------------|
| [<span data-ttu-id="02dae-120">**AttachHostDrive**</span><span class="sxs-lookup"><span data-stu-id="02dae-120">**AttachHostDrive**</span></span>](ivmfloppydrive-attachhostdrive.md)   | <span data-ttu-id="02dae-121">Anexa uma unidade física no host à unidade de disquete na máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="02dae-121">Attaches a physical drive on the host to the floppy drive in the virtual machine.</span></span><br/> |
| [<span data-ttu-id="02dae-122">**AttachImage**</span><span class="sxs-lookup"><span data-stu-id="02dae-122">**AttachImage**</span></span>](ivmfloppydrive-attachimage.md)           | <span data-ttu-id="02dae-123">Anexa uma imagem de mídia de disquete no host à unidade de disquete.</span><span class="sxs-lookup"><span data-stu-id="02dae-123">Attaches a floppy media image on the host to the floppy drive.</span></span><br/>                    |
| [<span data-ttu-id="02dae-124">**ReleaseHostDrive**</span><span class="sxs-lookup"><span data-stu-id="02dae-124">**ReleaseHostDrive**</span></span>](ivmfloppydrive-releasehostdrive.md) | <span data-ttu-id="02dae-125">Libera uma unidade física no host da unidade de disquete.</span><span class="sxs-lookup"><span data-stu-id="02dae-125">Releases a physical drive on the host from the floppy drive.</span></span><br/>                      |
| [<span data-ttu-id="02dae-126">**ReleaseImage**</span><span class="sxs-lookup"><span data-stu-id="02dae-126">**ReleaseImage**</span></span>](ivmfloppydrive-releaseimage.md)         | <span data-ttu-id="02dae-127">Libera uma imagem de mídia de disquete no host da unidade de disquete.</span><span class="sxs-lookup"><span data-stu-id="02dae-127">Releases a floppy media image on the host from the floppy drive.</span></span><br/>                  |



 

### <a name="properties"></a><span data-ttu-id="02dae-128">Propriedades</span><span class="sxs-lookup"><span data-stu-id="02dae-128">Properties</span></span>

<span data-ttu-id="02dae-129">A interface **IVMFloppyDrive** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="02dae-129">The **IVMFloppyDrive** interface has these properties.</span></span>



| <span data-ttu-id="02dae-130">Propriedade</span><span class="sxs-lookup"><span data-stu-id="02dae-130">Property</span></span>                                                             | <span data-ttu-id="02dae-131">Tipo de acesso</span><span class="sxs-lookup"><span data-stu-id="02dae-131">Access type</span></span>          | <span data-ttu-id="02dae-132">Descrição</span><span class="sxs-lookup"><span data-stu-id="02dae-132">Description</span></span>                                                                               |
|:---------------------------------------------------------------------|:---------------------|:------------------------------------------------------------------------------------------|
| [<span data-ttu-id="02dae-133">**Anexo**</span><span class="sxs-lookup"><span data-stu-id="02dae-133">**Attachment**</span></span>](ivmfloppydrive-attachment.md)<br/>           | <span data-ttu-id="02dae-134">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="02dae-134">Read-only</span></span><br/> | <span data-ttu-id="02dae-135">O tipo de mídia anexada à unidade de disquete na máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="02dae-135">The type of media attached to the floppy drive within the virtual machine.</span></span><br/>     |
| [<span data-ttu-id="02dae-136">**DriveNumber**</span><span class="sxs-lookup"><span data-stu-id="02dae-136">**DriveNumber**</span></span>](ivmfloppydrive-drivenumber.md)<br/>         | <span data-ttu-id="02dae-137">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="02dae-137">Read-only</span></span><br/> | <span data-ttu-id="02dae-138">O índice de base zero do controlador ao qual esta unidade de disquete está anexada.</span><span class="sxs-lookup"><span data-stu-id="02dae-138">The zero-based index of the controller to which this floppy drive is attached.</span></span><br/> |
| [<span data-ttu-id="02dae-139">**HostDriveLetter**</span><span class="sxs-lookup"><span data-stu-id="02dae-139">**HostDriveLetter**</span></span>](ivmfloppydrive-hostdriveletter.md)<br/> | <span data-ttu-id="02dae-140">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="02dae-140">Read-only</span></span><br/> | <span data-ttu-id="02dae-141">A letra da unidade do host à qual a unidade de disquete está conectada.</span><span class="sxs-lookup"><span data-stu-id="02dae-141">The letter of the host drive to which the floppy drive is attached.</span></span><br/>            |
| [<span data-ttu-id="02dae-142">**ImageFile**</span><span class="sxs-lookup"><span data-stu-id="02dae-142">**ImageFile**</span></span>](ivmfloppydrive-imagefile.md)<br/>             | <span data-ttu-id="02dae-143">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="02dae-143">Read-only</span></span><br/> | <span data-ttu-id="02dae-144">O caminho completo do arquivo de imagem ao qual a unidade de disquete está anexada.</span><span class="sxs-lookup"><span data-stu-id="02dae-144">The full path of the image file to which the floppy drive is attached.</span></span><br/>         |



 

## <a name="requirements"></a><span data-ttu-id="02dae-145">Requisitos</span><span class="sxs-lookup"><span data-stu-id="02dae-145">Requirements</span></span>



| <span data-ttu-id="02dae-146">Requisito</span><span class="sxs-lookup"><span data-stu-id="02dae-146">Requirement</span></span> | <span data-ttu-id="02dae-147">Valor</span><span class="sxs-lookup"><span data-stu-id="02dae-147">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="02dae-148">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="02dae-148">Minimum supported client</span></span><br/> | <span data-ttu-id="02dae-149">\[Somente aplicativos de área de trabalho do Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="02dae-149">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="02dae-150">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="02dae-150">Minimum supported server</span></span><br/> | <span data-ttu-id="02dae-151">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="02dae-151">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="02dae-152">Fim do suporte do cliente</span><span class="sxs-lookup"><span data-stu-id="02dae-152">End of client support</span></span><br/>    | <span data-ttu-id="02dae-153">Windows 7</span><span class="sxs-lookup"><span data-stu-id="02dae-153">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="02dae-154">Produto</span><span class="sxs-lookup"><span data-stu-id="02dae-154">Product</span></span><br/>                  | <span data-ttu-id="02dae-155">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="02dae-155">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="02dae-156">parâmetro</span><span class="sxs-lookup"><span data-stu-id="02dae-156">Header</span></span><br/>                   | <dl> <span data-ttu-id="02dae-157"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="02dae-157"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="02dae-158">IID</span><span class="sxs-lookup"><span data-stu-id="02dae-158">IID</span></span><br/>                      | <span data-ttu-id="02dae-159">IID \_ IVMFloppyDrive é definido como 661abee6-112a-4ed9-babf-3c874969f10e</span><span class="sxs-lookup"><span data-stu-id="02dae-159">IID\_IVMFloppyDrive is defined as 661abee6-112a-4ed9-babf-3c874969f10e</span></span><br/>             |



 

