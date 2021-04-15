---
title: Interface IVMHardDisk (VPCCOMInterfaces. h)
description: Fornece acesso a uma imagem de disco rígido. Ele pode ser acessado por meio da propriedade IVMHardDiskConnection HD ou do método IVMVirtualPC GetHardDisk.
ms.assetid: 0c536906-91be-428a-8199-c452abef423d
keywords:
- Virtual PC de interface IVMHardDisk
- Virtual PC de interface IVMHardDisk, descrito
topic_type:
- apiref
api_name:
- IVMHardDisk
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 24d6df46e7c698676e3873dd17a854fd0b7d7933
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104454587"
---
# <a name="ivmharddisk-interface"></a><span data-ttu-id="b6014-106">Interface IVMHardDisk</span><span class="sxs-lookup"><span data-stu-id="b6014-106">IVMHardDisk interface</span></span>

<span data-ttu-id="b6014-107">\[O Windows Virtual PC não está mais disponível para uso a partir do Windows 8.</span><span class="sxs-lookup"><span data-stu-id="b6014-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="b6014-108">Em vez disso, use o [provedor WMI do Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="b6014-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="b6014-109">Fornece acesso a uma imagem de disco rígido.</span><span class="sxs-lookup"><span data-stu-id="b6014-109">Provides access to a hard disk image.</span></span> <span data-ttu-id="b6014-110">Ele pode ser acessado por meio da propriedade [**IVMHardDiskConnection:: HD**](ivmharddiskconnection-harddisk.md) ou do método [**IVMVirtualPC:: GetHardDisk**](ivmvirtualpc-getharddisk.md) .</span><span class="sxs-lookup"><span data-stu-id="b6014-110">It can be accessed through the [**IVMHardDiskConnection::HardDisk**](ivmharddiskconnection-harddisk.md) property or the [**IVMVirtualPC::GetHardDisk**](ivmvirtualpc-getharddisk.md) method.</span></span>

## <a name="members"></a><span data-ttu-id="b6014-111">Membros</span><span class="sxs-lookup"><span data-stu-id="b6014-111">Members</span></span>

<span data-ttu-id="b6014-112">A interface **IVMHardDisk** herda da interface [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) .</span><span class="sxs-lookup"><span data-stu-id="b6014-112">The **IVMHardDisk** interface inherits from the [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interface.</span></span> <span data-ttu-id="b6014-113">**IVMHardDisk** também tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="b6014-113">**IVMHardDisk** also has these types of members:</span></span>

-   [<span data-ttu-id="b6014-114">Métodos</span><span class="sxs-lookup"><span data-stu-id="b6014-114">Methods</span></span>](#methods)
-   [<span data-ttu-id="b6014-115">Propriedades</span><span class="sxs-lookup"><span data-stu-id="b6014-115">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="b6014-116">Métodos</span><span class="sxs-lookup"><span data-stu-id="b6014-116">Methods</span></span>

<span data-ttu-id="b6014-117">A interface **IVMHardDisk** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="b6014-117">The **IVMHardDisk** interface has these methods.</span></span>



| <span data-ttu-id="b6014-118">Método</span><span class="sxs-lookup"><span data-stu-id="b6014-118">Method</span></span>                                 | <span data-ttu-id="b6014-119">Descrição</span><span class="sxs-lookup"><span data-stu-id="b6014-119">Description</span></span>                                                                                                                                                 |
|:---------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="b6014-120">**Compacto**</span><span class="sxs-lookup"><span data-stu-id="b6014-120">**Compact**</span></span>](ivmharddisk-compact.md) | <span data-ttu-id="b6014-121">Compacta uma imagem de disco rígido virtual de expansão dinâmica.</span><span class="sxs-lookup"><span data-stu-id="b6014-121">Compacts a dynamically expanding virtual hard disk image.</span></span><br/>                                                                                        |
| [<span data-ttu-id="b6014-122">**Converter**</span><span class="sxs-lookup"><span data-stu-id="b6014-122">**Convert**</span></span>](ivmharddisk-convert.md) | <span data-ttu-id="b6014-123">Converte qualquer disco rígido virtual em um disco rígido virtual de expansão dinâmica ou em um disco rígido virtual de tamanho fixo.</span><span class="sxs-lookup"><span data-stu-id="b6014-123">Converts any virtual hard disk to either a dynamically expanding virtual hard disk or a fixed-size virtual hard disk.</span></span><br/>                            |
| [<span data-ttu-id="b6014-124">**Mescle**</span><span class="sxs-lookup"><span data-stu-id="b6014-124">**Merge**</span></span>](ivmharddisk-merge.md)     | <span data-ttu-id="b6014-125">Mescla um disco rígido virtual diferencial com sua imagem de disco pai.</span><span class="sxs-lookup"><span data-stu-id="b6014-125">Merges a differencing virtual hard disk with its parent disk image.</span></span><br/>                                                                              |
| [<span data-ttu-id="b6014-126">**Mesclar**</span><span class="sxs-lookup"><span data-stu-id="b6014-126">**MergeTo**</span></span>](ivmharddisk-mergeto.md) | <span data-ttu-id="b6014-127">Mescla um disco rígido virtual diferencial com todos os seus pais (até e incluindo o disco rígido virtual pai raiz) em um novo arquivo de disco rígido.</span><span class="sxs-lookup"><span data-stu-id="b6014-127">Merges a differencing virtual hard disk with all of its parents (up to and including the root parent virtual hard disk) to a new hard disk file.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="b6014-128">Propriedades</span><span class="sxs-lookup"><span data-stu-id="b6014-128">Properties</span></span>

<span data-ttu-id="b6014-129">A interface **IVMHardDisk** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="b6014-129">The **IVMHardDisk** interface has these properties.</span></span>



| <span data-ttu-id="b6014-130">Propriedade</span><span class="sxs-lookup"><span data-stu-id="b6014-130">Property</span></span>                                                              | <span data-ttu-id="b6014-131">Tipo de acesso</span><span class="sxs-lookup"><span data-stu-id="b6014-131">Access type</span></span>           | <span data-ttu-id="b6014-132">Descrição</span><span class="sxs-lookup"><span data-stu-id="b6014-132">Description</span></span>                                                                                    |
|:----------------------------------------------------------------------|:----------------------|:-----------------------------------------------------------------------------------------------|
| [<span data-ttu-id="b6014-133">**Arquivo**</span><span class="sxs-lookup"><span data-stu-id="b6014-133">**File**</span></span>](ivmharddisk-file.md)<br/>                           | <span data-ttu-id="b6014-134">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="b6014-134">Read-only</span></span><br/>  | <span data-ttu-id="b6014-135">O nome do caminho completo do arquivo de disco rígido virtual.</span><span class="sxs-lookup"><span data-stu-id="b6014-135">The full path name of the virtual hard disk file.</span></span><br/>                                   |
| [<span data-ttu-id="b6014-136">**HostFreeDiskSpace**</span><span class="sxs-lookup"><span data-stu-id="b6014-136">**HostFreeDiskSpace**</span></span>](ivmharddisk-hostfreediskspace.md)<br/> | <span data-ttu-id="b6014-137">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="b6014-137">Read-only</span></span><br/>  | <span data-ttu-id="b6014-138">A quantidade de espaço em disco restante disponível no host para o disco rígido virtual.</span><span class="sxs-lookup"><span data-stu-id="b6014-138">The amount of remaining disk space available on the host for the virtual hard disk.</span></span><br/> |
| [<span data-ttu-id="b6014-139">**Pai**</span><span class="sxs-lookup"><span data-stu-id="b6014-139">**Parent**</span></span>](ivmharddisk-parent.md)<br/>                       | <span data-ttu-id="b6014-140">Leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="b6014-140">Read/write</span></span><br/> | <span data-ttu-id="b6014-141">O pai do disco rígido virtual diferencial.</span><span class="sxs-lookup"><span data-stu-id="b6014-141">The parent of the differencing virtual hard disk.</span></span><br/>                                   |
| [<span data-ttu-id="b6014-142">**SizeInGuest**</span><span class="sxs-lookup"><span data-stu-id="b6014-142">**SizeInGuest**</span></span>](ivmharddisk-sizeinguest.md)<br/>             | <span data-ttu-id="b6014-143">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="b6014-143">Read-only</span></span><br/>  | <span data-ttu-id="b6014-144">O tamanho do disco rígido virtual no sistema operacional convidado.</span><span class="sxs-lookup"><span data-stu-id="b6014-144">The size of the virtual hard disk in the guest operating system.</span></span><br/>                    |
| [<span data-ttu-id="b6014-145">**SizeOnHost**</span><span class="sxs-lookup"><span data-stu-id="b6014-145">**SizeOnHost**</span></span>](ivmharddisk-sizeonhost.md)<br/>               | <span data-ttu-id="b6014-146">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="b6014-146">Read-only</span></span><br/>  | <span data-ttu-id="b6014-147">O tamanho do arquivo de disco rígido virtual no computador host.</span><span class="sxs-lookup"><span data-stu-id="b6014-147">The size of the virtual hard disk file on the host computer.</span></span><br/>                        |
| [<span data-ttu-id="b6014-148">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="b6014-148">**Type**</span></span>](ivmharddisk-type.md)<br/>                           | <span data-ttu-id="b6014-149">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="b6014-149">Read-only</span></span><br/>  | <span data-ttu-id="b6014-150">O tipo do disco rígido virtual.</span><span class="sxs-lookup"><span data-stu-id="b6014-150">The type of the virtual hard disk.</span></span><br/>                                                  |



 

## <a name="requirements"></a><span data-ttu-id="b6014-151">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b6014-151">Requirements</span></span>



| <span data-ttu-id="b6014-152">Requisito</span><span class="sxs-lookup"><span data-stu-id="b6014-152">Requirement</span></span> | <span data-ttu-id="b6014-153">Valor</span><span class="sxs-lookup"><span data-stu-id="b6014-153">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="b6014-154">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b6014-154">Minimum supported client</span></span><br/> | <span data-ttu-id="b6014-155">\[Somente aplicativos de área de trabalho do Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="b6014-155">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="b6014-156">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b6014-156">Minimum supported server</span></span><br/> | <span data-ttu-id="b6014-157">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="b6014-157">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="b6014-158">Fim do suporte do cliente</span><span class="sxs-lookup"><span data-stu-id="b6014-158">End of client support</span></span><br/>    | <span data-ttu-id="b6014-159">Windows 7</span><span class="sxs-lookup"><span data-stu-id="b6014-159">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="b6014-160">Produto</span><span class="sxs-lookup"><span data-stu-id="b6014-160">Product</span></span><br/>                  | <span data-ttu-id="b6014-161">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="b6014-161">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="b6014-162">parâmetro</span><span class="sxs-lookup"><span data-stu-id="b6014-162">Header</span></span><br/>                   | <dl> <span data-ttu-id="b6014-163"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="b6014-163"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="b6014-164">IID</span><span class="sxs-lookup"><span data-stu-id="b6014-164">IID</span></span><br/>                      | <span data-ttu-id="b6014-165">IID \_ IVMHardDisk é definido como ffa14ae6-48f5-42a4-8a22-186f2e5c7db0</span><span class="sxs-lookup"><span data-stu-id="b6014-165">IID\_IVMHardDisk is defined as ffa14ae6-48f5-42a4-8a22-186f2e5c7db0</span></span><br/>                |



 

