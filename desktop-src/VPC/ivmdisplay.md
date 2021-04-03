---
title: Interface IVMDisplay (VPCCOMInterfaces. h)
description: Controla as configurações de exibição de uma máquina virtual. A interface IVMDisplay para uma máquina virtual pode ser recuperada usando a propriedade de exibição IVMVirtualMachine.
ms.assetid: b2eafd86-459c-4807-aa77-8b9125bce53e
keywords:
- Virtual PC de interface IVMDisplay
- Virtual PC de interface IVMDisplay, descrito
topic_type:
- apiref
api_name:
- IVMDisplay
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2c0f410e49682d2fa9f5f8511d96e3b9ce9a1094
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918828"
---
# <a name="ivmdisplay-interface"></a><span data-ttu-id="d9deb-106">Interface IVMDisplay</span><span class="sxs-lookup"><span data-stu-id="d9deb-106">IVMDisplay interface</span></span>

<span data-ttu-id="d9deb-107">\[O Windows Virtual PC não está mais disponível para uso a partir do Windows 8.</span><span class="sxs-lookup"><span data-stu-id="d9deb-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="d9deb-108">Em vez disso, use o [provedor WMI do Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="d9deb-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="d9deb-109">Controla as configurações de exibição de uma máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="d9deb-109">Controls the display settings of a virtual machine.</span></span> <span data-ttu-id="d9deb-110">A interface **IVMDisplay** para uma máquina virtual pode ser recuperada usando a propriedade [**IVMVirtualMachine::D isplay**](ivmvirtualmachine-display.md) .</span><span class="sxs-lookup"><span data-stu-id="d9deb-110">The **IVMDisplay** interface for a virtual machine can be retrieved using the [**IVMVirtualMachine::Display**](ivmvirtualmachine-display.md) property.</span></span>

## <a name="members"></a><span data-ttu-id="d9deb-111">Membros</span><span class="sxs-lookup"><span data-stu-id="d9deb-111">Members</span></span>

<span data-ttu-id="d9deb-112">A interface **IVMDisplay** herda da interface [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) .</span><span class="sxs-lookup"><span data-stu-id="d9deb-112">The **IVMDisplay** interface inherits from the [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interface.</span></span> <span data-ttu-id="d9deb-113">**IVMDisplay** também tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="d9deb-113">**IVMDisplay** also has these types of members:</span></span>

-   [<span data-ttu-id="d9deb-114">Métodos</span><span class="sxs-lookup"><span data-stu-id="d9deb-114">Methods</span></span>](#methods)
-   [<span data-ttu-id="d9deb-115">Propriedades</span><span class="sxs-lookup"><span data-stu-id="d9deb-115">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="d9deb-116">Métodos</span><span class="sxs-lookup"><span data-stu-id="d9deb-116">Methods</span></span>

<span data-ttu-id="d9deb-117">A interface **IVMDisplay** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="d9deb-117">The **IVMDisplay** interface has these methods.</span></span>



| <span data-ttu-id="d9deb-118">Método</span><span class="sxs-lookup"><span data-stu-id="d9deb-118">Method</span></span>                                                       | <span data-ttu-id="d9deb-119">Descrição</span><span class="sxs-lookup"><span data-stu-id="d9deb-119">Description</span></span>                                                                                             |
|:-------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="d9deb-120">**\_GenerateThumbnail**</span><span class="sxs-lookup"><span data-stu-id="d9deb-120">**\_GenerateThumbnail**</span></span>](ivmdisplay--generatethumbnail.md) | <span data-ttu-id="d9deb-121">Recupera uma matriz de pixels que representa uma imagem em miniatura da tela da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="d9deb-121">Retrieves an array of pixels representing a thumbnail image of the virtual machine's screen.</span></span><br/> |
| [<span data-ttu-id="d9deb-122">**Setdimensions**</span><span class="sxs-lookup"><span data-stu-id="d9deb-122">**SetDimensions**</span></span>](ivmdisplay-setdimensions.md)            | <span data-ttu-id="d9deb-123">Define a altura e a largura da exibição da máquina virtual, em pixels.</span><span class="sxs-lookup"><span data-stu-id="d9deb-123">Sets the height and width of the virtual machine's display, in pixels.</span></span><br/>                       |



 

### <a name="properties"></a><span data-ttu-id="d9deb-124">Propriedades</span><span class="sxs-lookup"><span data-stu-id="d9deb-124">Properties</span></span>

<span data-ttu-id="d9deb-125">A interface **IVMDisplay** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="d9deb-125">The **IVMDisplay** interface has these properties.</span></span>



| <span data-ttu-id="d9deb-126">Propriedade</span><span class="sxs-lookup"><span data-stu-id="d9deb-126">Property</span></span>                                             | <span data-ttu-id="d9deb-127">Tipo de acesso</span><span class="sxs-lookup"><span data-stu-id="d9deb-127">Access type</span></span>          | <span data-ttu-id="d9deb-128">Descrição</span><span class="sxs-lookup"><span data-stu-id="d9deb-128">Description</span></span>                                                                                   |
|:-----------------------------------------------------|:---------------------|:----------------------------------------------------------------------------------------------|
| [<span data-ttu-id="d9deb-129">**Redimensionar**</span><span class="sxs-lookup"><span data-stu-id="d9deb-129">**CanResize**</span></span>](ivmdisplay-canresize.md)<br/> | <span data-ttu-id="d9deb-130">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="d9deb-130">Read-only</span></span><br/> | <span data-ttu-id="d9deb-131">Indica se o convidado permite alterações de resolução.</span><span class="sxs-lookup"><span data-stu-id="d9deb-131">Indicates whether the Guest allows resolution changes.</span></span><br/>                             |
| [<span data-ttu-id="d9deb-132">**Altura**</span><span class="sxs-lookup"><span data-stu-id="d9deb-132">**Height**</span></span>](ivmdisplay-height.md)<br/>       | <span data-ttu-id="d9deb-133">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="d9deb-133">Read-only</span></span><br/> | <span data-ttu-id="d9deb-134">A altura da exibição da máquina virtual, em pixels.</span><span class="sxs-lookup"><span data-stu-id="d9deb-134">The height of the virtual machine's display, in pixels.</span></span><br/>                            |
| [<span data-ttu-id="d9deb-135">**Thumbnail**</span><span class="sxs-lookup"><span data-stu-id="d9deb-135">**Thumbnail**</span></span>](ivmdisplay-thumbnail.md)<br/> | <span data-ttu-id="d9deb-136">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="d9deb-136">Read-only</span></span><br/> | <span data-ttu-id="d9deb-137">Uma matriz de pixels que representa uma imagem em miniatura da tela da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="d9deb-137">An array of pixels representing a thumbnail image of the virtual machine's screen.</span></span><br/> |
| [<span data-ttu-id="d9deb-138">**Videomode**</span><span class="sxs-lookup"><span data-stu-id="d9deb-138">**VideoMode**</span></span>](ivmdisplay-videomode.md)<br/> | <span data-ttu-id="d9deb-139">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="d9deb-139">Read-only</span></span><br/> | <span data-ttu-id="d9deb-140">O modo de vídeo atual (texto, VGA, SVGA e assim por diante).</span><span class="sxs-lookup"><span data-stu-id="d9deb-140">The current video mode (Text, VGA, SVGA, and so on).</span></span><br/>                               |
| [<span data-ttu-id="d9deb-141">**Largura**</span><span class="sxs-lookup"><span data-stu-id="d9deb-141">**Width**</span></span>](ivmdisplay-width.md)<br/>         | <span data-ttu-id="d9deb-142">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="d9deb-142">Read-only</span></span><br/> | <span data-ttu-id="d9deb-143">A largura da exibição da máquina virtual, em pixels.</span><span class="sxs-lookup"><span data-stu-id="d9deb-143">The width of the virtual machine's display, in pixels.</span></span><br/>                             |



 

## <a name="requirements"></a><span data-ttu-id="d9deb-144">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d9deb-144">Requirements</span></span>



| <span data-ttu-id="d9deb-145">Requisito</span><span class="sxs-lookup"><span data-stu-id="d9deb-145">Requirement</span></span> | <span data-ttu-id="d9deb-146">Valor</span><span class="sxs-lookup"><span data-stu-id="d9deb-146">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="d9deb-147">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d9deb-147">Minimum supported client</span></span><br/> | <span data-ttu-id="d9deb-148">\[Somente aplicativos de área de trabalho do Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="d9deb-148">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="d9deb-149">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d9deb-149">Minimum supported server</span></span><br/> | <span data-ttu-id="d9deb-150">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="d9deb-150">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="d9deb-151">Fim do suporte do cliente</span><span class="sxs-lookup"><span data-stu-id="d9deb-151">End of client support</span></span><br/>    | <span data-ttu-id="d9deb-152">Windows 7</span><span class="sxs-lookup"><span data-stu-id="d9deb-152">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="d9deb-153">Produto</span><span class="sxs-lookup"><span data-stu-id="d9deb-153">Product</span></span><br/>                  | <span data-ttu-id="d9deb-154">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="d9deb-154">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="d9deb-155">parâmetro</span><span class="sxs-lookup"><span data-stu-id="d9deb-155">Header</span></span><br/>                   | <dl> <span data-ttu-id="d9deb-156"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="d9deb-156"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="d9deb-157">IID</span><span class="sxs-lookup"><span data-stu-id="d9deb-157">IID</span></span><br/>                      | <span data-ttu-id="d9deb-158">IID \_ IVMDisplay é definido como 960895e9-f743-4498-96aa-261f867e7fc5</span><span class="sxs-lookup"><span data-stu-id="d9deb-158">IID\_IVMDisplay is defined as 960895e9-f743-4498-96aa-261f867e7fc5</span></span><br/>                 |



 

