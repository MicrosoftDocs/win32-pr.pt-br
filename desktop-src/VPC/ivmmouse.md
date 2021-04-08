---
title: Interface IVMMouse (VPCCOMInterfaces. h)
description: Controla o dispositivo de mouse em uma VM.
ms.assetid: 13bbf980-aafd-4c63-b1cb-60f00b738d1f
keywords:
- Virtual PC de interface IVMMouse
- Virtual PC de interface IVMMouse, descrito
topic_type:
- apiref
api_name:
- IVMMouse
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7041b8a28b924ffedc8ff23edd2b04afdaa78be2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103824696"
---
# <a name="ivmmouse-interface"></a><span data-ttu-id="75353-105">Interface IVMMouse</span><span class="sxs-lookup"><span data-stu-id="75353-105">IVMMouse interface</span></span>

<span data-ttu-id="75353-106">\[O Windows Virtual PC não está mais disponível para uso a partir do Windows 8.</span><span class="sxs-lookup"><span data-stu-id="75353-106">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="75353-107">Em vez disso, use o [provedor WMI do Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="75353-107">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="75353-108">Controla o dispositivo de mouse em uma máquina virtual (VM).</span><span class="sxs-lookup"><span data-stu-id="75353-108">Controls the mouse device within a virtual machine (VM).</span></span> <span data-ttu-id="75353-109">O **IVMMouse** para uma máquina virtual pode ser recuperado usando a propriedade [**IVMVirtualMachine:: mouse**](ivmvirtualmachine-mouse.md) .</span><span class="sxs-lookup"><span data-stu-id="75353-109">The **IVMMouse** for a virtual machine can be retrieved using the [**IVMVirtualMachine::Mouse**](ivmvirtualmachine-mouse.md) property.</span></span> <span data-ttu-id="75353-110">As coordenadas para o dispositivo de mouse podem ser representadas em coordenadas absolutas ou em coordenadas Delta.</span><span class="sxs-lookup"><span data-stu-id="75353-110">Coordinates for the mouse device can be represented either in absolute coordinates or in delta coordinates.</span></span> <span data-ttu-id="75353-111">Use a propriedade [**UsingAbsoluteCoordinates**](ivmmouse-usingabsolutecoordinates.md) para distinguir entre os dois métodos de representação de coordenadas.</span><span class="sxs-lookup"><span data-stu-id="75353-111">Use the [**UsingAbsoluteCoordinates**](ivmmouse-usingabsolutecoordinates.md) property to distinguish between the two methods of coordinate representation.</span></span> <span data-ttu-id="75353-112">Observe que a recuperação da posição atual do cursor e o uso de coordenadas absolutas só têm suporte se o sistema operacional convidado tiver os componentes de integração instalados.</span><span class="sxs-lookup"><span data-stu-id="75353-112">Note that retrieving the current cursor position and the use of absolute coordinates are only supported if the guest operating system has the integration components installed.</span></span>

## <a name="members"></a><span data-ttu-id="75353-113">Membros</span><span class="sxs-lookup"><span data-stu-id="75353-113">Members</span></span>

<span data-ttu-id="75353-114">A interface **IVMMouse** herda da interface [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) .</span><span class="sxs-lookup"><span data-stu-id="75353-114">The **IVMMouse** interface inherits from the [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interface.</span></span> <span data-ttu-id="75353-115">**IVMMouse** também tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="75353-115">**IVMMouse** also has these types of members:</span></span>

-   [<span data-ttu-id="75353-116">Métodos</span><span class="sxs-lookup"><span data-stu-id="75353-116">Methods</span></span>](#methods)
-   [<span data-ttu-id="75353-117">Propriedades</span><span class="sxs-lookup"><span data-stu-id="75353-117">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="75353-118">Métodos</span><span class="sxs-lookup"><span data-stu-id="75353-118">Methods</span></span>

<span data-ttu-id="75353-119">A interface **IVMMouse** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="75353-119">The **IVMMouse** interface has these methods.</span></span>



| <span data-ttu-id="75353-120">Método</span><span class="sxs-lookup"><span data-stu-id="75353-120">Method</span></span>                                  | <span data-ttu-id="75353-121">Descrição</span><span class="sxs-lookup"><span data-stu-id="75353-121">Description</span></span>                                                                        |
|:----------------------------------------|:-----------------------------------------------------------------------------------|
| [<span data-ttu-id="75353-122">**Clicar**</span><span class="sxs-lookup"><span data-stu-id="75353-122">**Click**</span></span>](ivmmouse-click.md)         | <span data-ttu-id="75353-123">Simula um clique no botão do mouse.</span><span class="sxs-lookup"><span data-stu-id="75353-123">Simulates a mouse button click.</span></span><br/>                                         |
| [<span data-ttu-id="75353-124">**Getbutton**</span><span class="sxs-lookup"><span data-stu-id="75353-124">**GetButton**</span></span>](ivmmouse-getbutton.md) | <span data-ttu-id="75353-125">Recupera o estado atual (para cima ou para baixo) do botão do mouse especificado.</span><span class="sxs-lookup"><span data-stu-id="75353-125">Retrieves the current state (up or down) of the specified mouse button.</span></span><br/> |
| [<span data-ttu-id="75353-126">**SetButton**</span><span class="sxs-lookup"><span data-stu-id="75353-126">**SetButton**</span></span>](ivmmouse-setbutton.md) | <span data-ttu-id="75353-127">Define o estado atual (para cima ou para baixo) do botão do mouse especificado.</span><span class="sxs-lookup"><span data-stu-id="75353-127">Sets the current state (up or down) of the specified mouse button.</span></span><br/>      |



 

### <a name="properties"></a><span data-ttu-id="75353-128">Propriedades</span><span class="sxs-lookup"><span data-stu-id="75353-128">Properties</span></span>

<span data-ttu-id="75353-129">A interface **IVMMouse** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="75353-129">The **IVMMouse** interface has these properties.</span></span>



| <span data-ttu-id="75353-130">Propriedade</span><span class="sxs-lookup"><span data-stu-id="75353-130">Property</span></span>                                                                         | <span data-ttu-id="75353-131">Tipo de acesso</span><span class="sxs-lookup"><span data-stu-id="75353-131">Access type</span></span>           | <span data-ttu-id="75353-132">Descrição</span><span class="sxs-lookup"><span data-stu-id="75353-132">Description</span></span>                                                                                |
|:---------------------------------------------------------------------------------|:----------------------|:-------------------------------------------------------------------------------------------|
| [<span data-ttu-id="75353-133">**HorizontalPosition**</span><span class="sxs-lookup"><span data-stu-id="75353-133">**HorizontalPosition**</span></span>](ivmmouse-horizontalposition.md)<br/>             | <span data-ttu-id="75353-134">Leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="75353-134">Read/write</span></span><br/> | <span data-ttu-id="75353-135">A coordenada x absoluta do mouse.</span><span class="sxs-lookup"><span data-stu-id="75353-135">The absolute x-coordinate of the mouse.</span></span><br/>                                         |
| [<span data-ttu-id="75353-136">**ScrollWheelPosition**</span><span class="sxs-lookup"><span data-stu-id="75353-136">**ScrollWheelPosition**</span></span>](ivmmouse-scrollwheelposition.md)<br/>           | <span data-ttu-id="75353-137">Somente gravação</span><span class="sxs-lookup"><span data-stu-id="75353-137">Write-only</span></span><br/> | <span data-ttu-id="75353-138">A coordenada z do mouse (somente relativo).</span><span class="sxs-lookup"><span data-stu-id="75353-138">The z-coordinate of the mouse (relative only).</span></span><br/>                                  |
| [<span data-ttu-id="75353-139">**UsingAbsoluteCoordinates**</span><span class="sxs-lookup"><span data-stu-id="75353-139">**UsingAbsoluteCoordinates**</span></span>](ivmmouse-usingabsolutecoordinates.md)<br/> | <span data-ttu-id="75353-140">Leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="75353-140">Read/write</span></span><br/> | <span data-ttu-id="75353-141">Indica se as coordenadas do mouse representam coordenadas absolutas ou relativas.</span><span class="sxs-lookup"><span data-stu-id="75353-141">Indicates whether mouse coordinates represent absolute or relative coordinates.</span></span><br/> |
| [<span data-ttu-id="75353-142">**VerticalPosition**</span><span class="sxs-lookup"><span data-stu-id="75353-142">**VerticalPosition**</span></span>](ivmmouse-verticalposition.md)<br/>                 | <span data-ttu-id="75353-143">Leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="75353-143">Read/write</span></span><br/> | <span data-ttu-id="75353-144">A coordenada y absoluta do mouse.</span><span class="sxs-lookup"><span data-stu-id="75353-144">The absolute y-coordinate of the mouse.</span></span><br/>                                         |



 

## <a name="requirements"></a><span data-ttu-id="75353-145">Requisitos</span><span class="sxs-lookup"><span data-stu-id="75353-145">Requirements</span></span>



| <span data-ttu-id="75353-146">Requisito</span><span class="sxs-lookup"><span data-stu-id="75353-146">Requirement</span></span> | <span data-ttu-id="75353-147">Valor</span><span class="sxs-lookup"><span data-stu-id="75353-147">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="75353-148">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="75353-148">Minimum supported client</span></span><br/> | <span data-ttu-id="75353-149">\[Somente aplicativos de área de trabalho do Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="75353-149">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="75353-150">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="75353-150">Minimum supported server</span></span><br/> | <span data-ttu-id="75353-151">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="75353-151">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="75353-152">Fim do suporte do cliente</span><span class="sxs-lookup"><span data-stu-id="75353-152">End of client support</span></span><br/>    | <span data-ttu-id="75353-153">Windows 7</span><span class="sxs-lookup"><span data-stu-id="75353-153">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="75353-154">Produto</span><span class="sxs-lookup"><span data-stu-id="75353-154">Product</span></span><br/>                  | <span data-ttu-id="75353-155">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="75353-155">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="75353-156">parâmetro</span><span class="sxs-lookup"><span data-stu-id="75353-156">Header</span></span><br/>                   | <dl> <span data-ttu-id="75353-157"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="75353-157"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="75353-158">IID</span><span class="sxs-lookup"><span data-stu-id="75353-158">IID</span></span><br/>                      | <span data-ttu-id="75353-159">IID \_ IVMmouse é definido como ac903f6d-6346-4f29-8875-5d511a13895e</span><span class="sxs-lookup"><span data-stu-id="75353-159">IID\_IVMmouse is defined as ac903f6d-6346-4f29-8875-5d511a13895e</span></span><br/>                   |



 

