---
description: 'Saiba mais sobre: <span id=vhd.vhd_functions></span> funções de disco virtual'
MS-HAID: vhd.vhd\_functions
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: Funções de disco virtual
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c4f31af2b24a55baa3c64bfe5bd9e09e0b9e2f59
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105800198"
---
# <a name="span-idvhdvhd_functionsspanvirtual-disk-functions"></a><span data-ttu-id="02c6b-103"><span id="vhd.vhd_functions"></span>Funções de disco virtual</span><span class="sxs-lookup"><span data-stu-id="02c6b-103"><span id="vhd.vhd_functions"></span>Virtual Disk Functions</span></span>

<span data-ttu-id="02c6b-104">As funções a seguir são usadas em discos virtuais:</span><span class="sxs-lookup"><span data-stu-id="02c6b-104">The following functions are used in Virtual Disks:</span></span>

## <a name="span-idin_this_sectionspanin-this-section"></a><span data-ttu-id="02c6b-105"><span id="in_this_section"></span>Nesta seção</span><span class="sxs-lookup"><span data-stu-id="02c6b-105"><span id="in_this_section"></span>In this section</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="02c6b-106">Tópico</span><span class="sxs-lookup"><span data-stu-id="02c6b-106">Topic</span></span></th>
<th><span data-ttu-id="02c6b-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="02c6b-107">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="02c6b-108"><a href="/windows/win32/api/virtdisk/nf-virtdisk-applysnapshotvhdset"><strong>ApplySnapshotVhdSet</strong></a></span><span class="sxs-lookup"><span data-stu-id="02c6b-108"><a href="/windows/win32/api/virtdisk/nf-virtdisk-applysnapshotvhdset"><strong>ApplySnapshotVhdSet</strong></a></span></span></p></td>
<td><p><span data-ttu-id="02c6b-109">Aplica um instantâneo do disco virtual atual para arquivos de conjunto VHD.</span><span class="sxs-lookup"><span data-stu-id="02c6b-109">Applies a snapshot of the current virtual disk for VHD Set files.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="02c6b-110"><a href="/windows/desktop/api/virtdisk/nf-virtdisk-addvirtualdiskparent"><strong>AddVirtualDiskParent</strong></a></span><span class="sxs-lookup"><span data-stu-id="02c6b-110"><a href="/windows/desktop/api/virtdisk/nf-virtdisk-addvirtualdiskparent"><strong>AddVirtualDiskParent</strong></a></span></span></p></td>
<td><p><span data-ttu-id="02c6b-111">Anexa um pai a um disco virtual aberto com o sinalizador <strong>OPEN_VIRTUAL_DISK_FLAG_CUSTOM_DIFF_CHAIN</strong> .</span><span class="sxs-lookup"><span data-stu-id="02c6b-111">Attaches a parent to a virtual disk opened with the <strong>OPEN_VIRTUAL_DISK_FLAG_CUSTOM_DIFF_CHAIN</strong> flag.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="02c6b-112"><a href="/windows/win32/api/virtdisk/nf-virtdisk-attachvirtualdisk"><strong>AttachVirtualDisk</strong></a></span><span class="sxs-lookup"><span data-stu-id="02c6b-112"><a href="/windows/win32/api/virtdisk/nf-virtdisk-attachvirtualdisk"><strong>AttachVirtualDisk</strong></a></span></span></p></td>
<td><p><span data-ttu-id="02c6b-113">Anexa um VHD (disco rígido virtual) ou um arquivo de imagem de CD ou DVD (ISO) localizando um provedor VHD apropriado para realizar o anexo.</span><span class="sxs-lookup"><span data-stu-id="02c6b-113">Attaches a virtual hard disk (VHD) or CD or DVD image file (ISO) by locating an appropriate VHD provider to accomplish the attachment.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="02c6b-114"><a href="/windows/win32/api/virtdisk/nf-virtdisk-breakmirrorvirtualdisk"><strong>BreakMirrorVirtualDisk</strong></a></span><span class="sxs-lookup"><span data-stu-id="02c6b-114"><a href="/windows/win32/api/virtdisk/nf-virtdisk-breakmirrorvirtualdisk"><strong>BreakMirrorVirtualDisk</strong></a></span></span></p></td>
<td><p><span data-ttu-id="02c6b-115">Interrompe uma operação de espelhamento iniciada anteriormente e define o espelho como o disco virtual ativo.</span><span class="sxs-lookup"><span data-stu-id="02c6b-115">Breaks a previously initiated mirror operation and sets the mirror to be the active virtual disk.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="02c6b-116"><a href="/windows/win32/api/virtdisk/nf-virtdisk-compactvirtualdisk"><strong>CompactVirtualDisk</strong></a></span><span class="sxs-lookup"><span data-stu-id="02c6b-116"><a href="/windows/win32/api/virtdisk/nf-virtdisk-compactvirtualdisk"><strong>CompactVirtualDisk</strong></a></span></span></p></td>
<td><p><span data-ttu-id="02c6b-117">Reduz o tamanho de um arquivo de repositório de backup do VHD (disco rígido virtual).</span><span class="sxs-lookup"><span data-stu-id="02c6b-117">Reduces the size of a virtual hard disk (VHD) backing store file.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="02c6b-118"><a href="/windows/win32/api/virtdisk/nf-virtdisk-createvirtualdisk"><strong>CreateVirtualDisk</strong></a></span><span class="sxs-lookup"><span data-stu-id="02c6b-118"><a href="/windows/win32/api/virtdisk/nf-virtdisk-createvirtualdisk"><strong>CreateVirtualDisk</strong></a></span></span></p></td>
<td><p><span data-ttu-id="02c6b-119">Cria um arquivo de imagem de disco rígido virtual (VHD), usando parâmetros padrão ou um disco virtual ou disco físico existente.</span><span class="sxs-lookup"><span data-stu-id="02c6b-119">Creates a virtual hard disk (VHD) image file, either using default parameters or using an existing virtual disk or physical disk.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="02c6b-120"><a href="/windows/win32/api/virtdisk/nf-virtdisk-deletesnapshotvhdset"><strong>DeleteSnapshotVhdSet</strong></a></span><span class="sxs-lookup"><span data-stu-id="02c6b-120"><a href="/windows/win32/api/virtdisk/nf-virtdisk-deletesnapshotvhdset"><strong>DeleteSnapshotVhdSet</strong></a></span></span></p></td>
<td><p><span data-ttu-id="02c6b-121">Exclui um instantâneo de um arquivo de conjunto de VHD.</span><span class="sxs-lookup"><span data-stu-id="02c6b-121">Deletes a snapshot from a VHD Set file.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="02c6b-122"><a href="/windows/desktop/api/virtdisk/nf-virtdisk-deletevirtualdiskmetadata"><strong>DeleteVirtualDiskMetadata</strong></a></span><span class="sxs-lookup"><span data-stu-id="02c6b-122"><a href="/windows/desktop/api/virtdisk/nf-virtdisk-deletevirtualdiskmetadata"><strong>DeleteVirtualDiskMetadata</strong></a></span></span></p></td>
<td><p><span data-ttu-id="02c6b-123">Exclui os metadados de um disco virtual.</span><span class="sxs-lookup"><span data-stu-id="02c6b-123">Deletes metadata from a virtual disk.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="02c6b-124"><a href="/windows/win32/api/virtdisk/nf-virtdisk-detachvirtualdisk"><strong>DetachVirtualDisk</strong></a></span><span class="sxs-lookup"><span data-stu-id="02c6b-124"><a href="/windows/win32/api/virtdisk/nf-virtdisk-detachvirtualdisk"><strong>DetachVirtualDisk</strong></a></span></span></p></td>
<td><p><span data-ttu-id="02c6b-125">Desanexa um VHD (disco rígido virtual) ou um arquivo de imagem de CD ou DVD (ISO) localizando um provedor de disco virtual apropriado para realizar a operação.</span><span class="sxs-lookup"><span data-stu-id="02c6b-125">Detaches a virtual hard disk (VHD) or CD or DVD image file (ISO) by locating an appropriate virtual disk provider to accomplish the operation.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="02c6b-126"><a href="/windows/desktop/api/virtdisk/nf-virtdisk-enumeratevirtualdiskmetadata"><strong>EnumerateVirtualDiskMetadata</strong></a></span><span class="sxs-lookup"><span data-stu-id="02c6b-126"><a href="/windows/desktop/api/virtdisk/nf-virtdisk-enumeratevirtualdiskmetadata"><strong>EnumerateVirtualDiskMetadata</strong></a></span></span></p></td>
<td><p><span data-ttu-id="02c6b-127">Enumera os metadados associados a um disco virtual.</span><span class="sxs-lookup"><span data-stu-id="02c6b-127">Enumerates the metadata associated with a virtual disk.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="02c6b-128"><a href="/windows/win32/api/virtdisk/nf-virtdisk-expandvirtualdisk"><strong>ExpandVirtualDisk</strong></a></span><span class="sxs-lookup"><span data-stu-id="02c6b-128"><a href="/windows/win32/api/virtdisk/nf-virtdisk-expandvirtualdisk"><strong>ExpandVirtualDisk</strong></a></span></span></p></td>
<td><p><span data-ttu-id="02c6b-129">Aumenta o tamanho de um VHD (disco rígido virtual) fixo ou expansível dinamicamente.</span><span class="sxs-lookup"><span data-stu-id="02c6b-129">Increases the size of a fixed or dynamically expandable virtual hard disk (VHD).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="02c6b-130"><a href="/windows/win32/api/virtdisk/nf-virtdisk-getstoragedependencyinformation"><strong>GetStorageDependencyInformation</strong></a></span><span class="sxs-lookup"><span data-stu-id="02c6b-130"><a href="/windows/win32/api/virtdisk/nf-virtdisk-getstoragedependencyinformation"><strong>GetStorageDependencyInformation</strong></a></span></span></p></td>
<td><p><span data-ttu-id="02c6b-131">Retorna as relações entre os discos rígidos virtuais (VHDs) ou o arquivo de imagem de CD ou DVD (ISO) ou os volumes contidos nesses discos e seu disco ou volume pai.</span><span class="sxs-lookup"><span data-stu-id="02c6b-131">Returns the relationships between virtual hard disks (VHDs) or CD or DVD image file (ISO) or the volumes contained within those disks and their parent disk or volume.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="02c6b-132"><a href="/windows/win32/api/virtdisk/nf-virtdisk-getvirtualdiskinformation"><strong>GetVirtualDiskInformation</strong></a></span><span class="sxs-lookup"><span data-stu-id="02c6b-132"><a href="/windows/win32/api/virtdisk/nf-virtdisk-getvirtualdiskinformation"><strong>GetVirtualDiskInformation</strong></a></span></span></p></td>
<td><p><span data-ttu-id="02c6b-133">Recupera informações sobre um VHD.</span><span class="sxs-lookup"><span data-stu-id="02c6b-133">Retrieves information about a VHD.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="02c6b-134"><a href="/windows/desktop/api/virtdisk/nf-virtdisk-getvirtualdiskmetadata"><strong>GetVirtualDiskMetadata</strong></a></span><span class="sxs-lookup"><span data-stu-id="02c6b-134"><a href="/windows/desktop/api/virtdisk/nf-virtdisk-getvirtualdiskmetadata"><strong>GetVirtualDiskMetadata</strong></a></span></span></p></td>
<td><p><span data-ttu-id="02c6b-135">Recupera os metadados especificados do disco virtual.</span><span class="sxs-lookup"><span data-stu-id="02c6b-135">Retrieves the specified metadata from the virtual disk.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="02c6b-136"><a href="/windows/win32/api/virtdisk/nf-virtdisk-getvirtualdiskoperationprogress"><strong>GetVirtualDiskOperationProgress</strong></a></span><span class="sxs-lookup"><span data-stu-id="02c6b-136"><a href="/windows/win32/api/virtdisk/nf-virtdisk-getvirtualdiskoperationprogress"><strong>GetVirtualDiskOperationProgress</strong></a></span></span></p></td>
<td><p><span data-ttu-id="02c6b-137">Verifica o progresso de uma operação de disco rígido virtual (VHD) assíncrona.</span><span class="sxs-lookup"><span data-stu-id="02c6b-137">Checks the progress of an asynchronous virtual hard disk (VHD) operation.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="02c6b-138"><a href="/windows/win32/api/virtdisk/nf-virtdisk-getvirtualdiskphysicalpath"><strong>GetVirtualDiskPhysicalPath</strong></a></span><span class="sxs-lookup"><span data-stu-id="02c6b-138"><a href="/windows/win32/api/virtdisk/nf-virtdisk-getvirtualdiskphysicalpath"><strong>GetVirtualDiskPhysicalPath</strong></a></span></span></p></td>
<td><p><span data-ttu-id="02c6b-139">Recupera o caminho para o objeto de dispositivo físico que contém um VHD (disco rígido virtual) ou um arquivo de imagem de CD ou DVD (ISO).</span><span class="sxs-lookup"><span data-stu-id="02c6b-139">Retrieves the path to the physical device object that contains a virtual hard disk (VHD) or CD or DVD image file (ISO).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="02c6b-140"><a href="/windows/win32/api/virtdisk/nf-virtdisk-mergevirtualdisk"><strong>MergeVirtualDisk</strong></a></span><span class="sxs-lookup"><span data-stu-id="02c6b-140"><a href="/windows/win32/api/virtdisk/nf-virtdisk-mergevirtualdisk"><strong>MergeVirtualDisk</strong></a></span></span></p></td>
<td><p><span data-ttu-id="02c6b-141">Mescla um VHD (disco rígido virtual) filho em uma cadeia diferencial com um ou mais discos virtuais pai na cadeia.</span><span class="sxs-lookup"><span data-stu-id="02c6b-141">Merges a child virtual hard disk (VHD) in a differencing chain with one or more parent virtual disks in the chain.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="02c6b-142"><a href="/windows/win32/api/virtdisk/nf-virtdisk-mirrorvirtualdisk"><strong>MirrorVirtualDisk</strong></a></span><span class="sxs-lookup"><span data-stu-id="02c6b-142"><a href="/windows/win32/api/virtdisk/nf-virtdisk-mirrorvirtualdisk"><strong>MirrorVirtualDisk</strong></a></span></span></p></td>
<td><p><span data-ttu-id="02c6b-143">Inicia uma operação de espelhamento para um disco virtual.</span><span class="sxs-lookup"><span data-stu-id="02c6b-143">Initiates a mirror operation for a virtual disk.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="02c6b-144"><a href="/windows/win32/api/virtdisk/nf-virtdisk-modifyvhdset"><strong>ModifyVhdSet</strong></a></span><span class="sxs-lookup"><span data-stu-id="02c6b-144"><a href="/windows/win32/api/virtdisk/nf-virtdisk-modifyvhdset"><strong>ModifyVhdSet</strong></a></span></span></p></td>
<td><p><span data-ttu-id="02c6b-145">Modifica o conteúdo interno de um arquivo de disco virtual.</span><span class="sxs-lookup"><span data-stu-id="02c6b-145">Modifies the internal contents of a virtual disk file.</span></span> <span data-ttu-id="02c6b-146">Pode ser usado para definir a folha ativa ou para corrigir entradas de instantâneo.</span><span class="sxs-lookup"><span data-stu-id="02c6b-146">Can be used to set the active leaf, or to fix up snapshot entries.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="02c6b-147"><a href="/windows/win32/api/virtdisk/nf-virtdisk-openvirtualdisk"><strong>OpenVirtualDisk</strong></a></span><span class="sxs-lookup"><span data-stu-id="02c6b-147"><a href="/windows/win32/api/virtdisk/nf-virtdisk-openvirtualdisk"><strong>OpenVirtualDisk</strong></a></span></span></p></td>
<td><p><span data-ttu-id="02c6b-148">Abre um disco rígido virtual (VHD) ou um arquivo de imagem de CD ou DVD (ISO) para uso.</span><span class="sxs-lookup"><span data-stu-id="02c6b-148">Opens a virtual hard disk (VHD) or CD or DVD image file (ISO) for use.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="02c6b-149"><a href="/windows/win32/api/virtdisk/nf-virtdisk-querychangesvirtualdisk"><strong>QueryChangesVirtualDisk</strong></a></span><span class="sxs-lookup"><span data-stu-id="02c6b-149"><a href="/windows/win32/api/virtdisk/nf-virtdisk-querychangesvirtualdisk"><strong>QueryChangesVirtualDisk</strong></a></span></span></p></td>
<td><p><span data-ttu-id="02c6b-150">Recupera informações sobre alterações nas áreas especificadas de um disco rígido virtual (VHD) que são rastreadas pelo RCT (controle de alterações resiliente).</span><span class="sxs-lookup"><span data-stu-id="02c6b-150">Retrieves information about changes to the specified areas of a virtual hard disk (VHD) that are tracked by resilient change tracking (RCT).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="02c6b-151"><a href="/windows/win32/api/virtdisk/nf-virtdisk-rawscsivirtualdisk"><strong>RawSCSIVirtualDisk</strong></a></span><span class="sxs-lookup"><span data-stu-id="02c6b-151"><a href="/windows/win32/api/virtdisk/nf-virtdisk-rawscsivirtualdisk"><strong>RawSCSIVirtualDisk</strong></a></span></span></p></td>
<td><p><span data-ttu-id="02c6b-152">Emite uma solicitação SCSI inserida diretamente para um disco rígido virtual.</span><span class="sxs-lookup"><span data-stu-id="02c6b-152">Issues an embedded SCSI request directly to a virtual hard disk.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="02c6b-153"><a href="/windows/desktop/api/virtdisk/nf-virtdisk-resizevirtualdisk"><strong>ResizeVirtualDisk</strong></a></span><span class="sxs-lookup"><span data-stu-id="02c6b-153"><a href="/windows/desktop/api/virtdisk/nf-virtdisk-resizevirtualdisk"><strong>ResizeVirtualDisk</strong></a></span></span></p></td>
<td><p><span data-ttu-id="02c6b-154">Redimensiona um disco virtual.</span><span class="sxs-lookup"><span data-stu-id="02c6b-154">Resizes a virtual disk.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="02c6b-155"><a href="/windows/win32/api/virtdisk/nf-virtdisk-setvirtualdiskinformation"><strong>SetVirtualDiskInformation</strong></a></span><span class="sxs-lookup"><span data-stu-id="02c6b-155"><a href="/windows/win32/api/virtdisk/nf-virtdisk-setvirtualdiskinformation"><strong>SetVirtualDiskInformation</strong></a></span></span></p></td>
<td><p><span data-ttu-id="02c6b-156">Define informações sobre um VHD (disco rígido virtual).</span><span class="sxs-lookup"><span data-stu-id="02c6b-156">Sets information about a virtual hard disk (VHD).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="02c6b-157"><a href="/windows/desktop/api/virtdisk/nf-virtdisk-setvirtualdiskmetadata"><strong>SetVirtualDiskMetadata</strong></a></span><span class="sxs-lookup"><span data-stu-id="02c6b-157"><a href="/windows/desktop/api/virtdisk/nf-virtdisk-setvirtualdiskmetadata"><strong>SetVirtualDiskMetadata</strong></a></span></span></p></td>
<td><p><span data-ttu-id="02c6b-158">Define um item de metadados para um disco virtual.</span><span class="sxs-lookup"><span data-stu-id="02c6b-158">Sets a metadata item for a virtual disk.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="02c6b-159"><a href="/windows/win32/api/virtdisk/nf-virtdisk-takesnapshotvhdset"><strong>TakeSnapshotVhdSet</strong></a></span><span class="sxs-lookup"><span data-stu-id="02c6b-159"><a href="/windows/win32/api/virtdisk/nf-virtdisk-takesnapshotvhdset"><strong>TakeSnapshotVhdSet</strong></a></span></span></p></td>
<td><p><span data-ttu-id="02c6b-160">Cria um instantâneo do disco virtual atual para arquivos de conjunto VHD.</span><span class="sxs-lookup"><span data-stu-id="02c6b-160">Creates a snapshot of the current virtual disk for VHD Set files.</span></span></p></td>
</tr>
</tbody>
</table>

 

 

 
