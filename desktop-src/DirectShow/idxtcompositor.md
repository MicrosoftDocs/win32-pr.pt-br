---
description: A interface IDxtCompositor define propriedades na transição do compositor. Essa interface é usada internamente pelos serviços de edição do DirectShow (DES) quando ele renderiza a transição do compositor.
ms.assetid: 519f1e00-4b67-4014-906b-043f2478baa7
title: Interface IDxtCompositor (QEdit. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDxtCompositor
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: c2e19f555fe01cbec3763bc1dc76d11aeb5f5ecb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105759290"
---
# <a name="idxtcompositor-interface"></a><span data-ttu-id="fddc9-103">Interface IDxtCompositor</span><span class="sxs-lookup"><span data-stu-id="fddc9-103">IDxtCompositor interface</span></span>

> [!Note]  
> <span data-ttu-id="fddc9-104">\[Preterido.</span><span class="sxs-lookup"><span data-stu-id="fddc9-104">\[Deprecated.</span></span> <span data-ttu-id="fddc9-105">Essa API pode ser removida de versões futuras do Windows.\]</span><span class="sxs-lookup"><span data-stu-id="fddc9-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="fddc9-106">A `IDxtCompositor` interface define propriedades na transição do [compositor](compositor-transition.md) .</span><span class="sxs-lookup"><span data-stu-id="fddc9-106">The `IDxtCompositor` interface sets properties on the [Compositor](compositor-transition.md) transition.</span></span>

<span data-ttu-id="fddc9-107">Essa interface é usada internamente pelos serviços de edição do DirectShow (DES) quando ele renderiza a transição do compositor.</span><span class="sxs-lookup"><span data-stu-id="fddc9-107">This interface is used internally by DirectShow Editing Services (DES) when it renders the Compositor transition.</span></span> <span data-ttu-id="fddc9-108">Os aplicativos DES não precisam usar essa interface.</span><span class="sxs-lookup"><span data-stu-id="fddc9-108">DES applications do not have to use this interface.</span></span> <span data-ttu-id="fddc9-109">Para definir as propriedades em uma transição em DES, use a interface [**IPropertySetter**](ipropertysetter.md) .</span><span class="sxs-lookup"><span data-stu-id="fddc9-109">To set the properties on a transition in DES, use the [**IPropertySetter**](ipropertysetter.md) interface.</span></span>

<span data-ttu-id="fddc9-110">A transição do compositor compõe uma imagem em primeiro plano em uma imagem de plano de fundo.</span><span class="sxs-lookup"><span data-stu-id="fddc9-110">The Compositor transition composites a foreground image onto a background image.</span></span> <span data-ttu-id="fddc9-111">O *retângulo de origem* define a seção da imagem em primeiro plano que é composta.</span><span class="sxs-lookup"><span data-stu-id="fddc9-111">The *source rectangle* defines the section of the foreground image that is composited.</span></span> <span data-ttu-id="fddc9-112">O *retângulo de destino* define a seção da imagem de plano de fundo que recebe a imagem em primeiro plano.</span><span class="sxs-lookup"><span data-stu-id="fddc9-112">The *destination rectangle* defines the section of the background image that receives the foreground image.</span></span> <span data-ttu-id="fddc9-113">O diagrama a seguir ilustra esses retângulos.</span><span class="sxs-lookup"><span data-stu-id="fddc9-113">The following diagram illustrates these rectangles.</span></span>

![Propriedades de transição do compositor](images/compmeasure.png)

## <a name="members"></a><span data-ttu-id="fddc9-115">Membros</span><span class="sxs-lookup"><span data-stu-id="fddc9-115">Members</span></span>

<span data-ttu-id="fddc9-116">A interface **IDxtCompositor** herda de **IDXEffect**.</span><span class="sxs-lookup"><span data-stu-id="fddc9-116">The **IDxtCompositor** interface inherits from **IDXEffect**.</span></span> <span data-ttu-id="fddc9-117">**IDxtCompositor** também tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="fddc9-117">**IDxtCompositor** also has these types of members:</span></span>

-   [<span data-ttu-id="fddc9-118">Métodos</span><span class="sxs-lookup"><span data-stu-id="fddc9-118">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="fddc9-119">Métodos</span><span class="sxs-lookup"><span data-stu-id="fddc9-119">Methods</span></span>

<span data-ttu-id="fddc9-120">A interface **IDxtCompositor** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="fddc9-120">The **IDxtCompositor** interface has these methods.</span></span>



| <span data-ttu-id="fddc9-121">Método</span><span class="sxs-lookup"><span data-stu-id="fddc9-121">Method</span></span>                                                   | <span data-ttu-id="fddc9-122">Descrição</span><span class="sxs-lookup"><span data-stu-id="fddc9-122">Description</span></span>                                                         |
|:---------------------------------------------------------|:--------------------------------------------------------------------|
| [<span data-ttu-id="fddc9-123">**obter \_ altura**</span><span class="sxs-lookup"><span data-stu-id="fddc9-123">**get\_Height**</span></span>](idxtcompositor-get-height.md)         | <span data-ttu-id="fddc9-124">Recupera a altura do retângulo de destino.</span><span class="sxs-lookup"><span data-stu-id="fddc9-124">Retrieves the height of the target rectangle.</span></span><br/>            |
| [<span data-ttu-id="fddc9-125">**obter \_ OffsetX**</span><span class="sxs-lookup"><span data-stu-id="fddc9-125">**get\_OffsetX**</span></span>](idxtcompositor-get-offsetx.md)       | <span data-ttu-id="fddc9-126">Recupera o deslocamento horizontal do retângulo de destino.</span><span class="sxs-lookup"><span data-stu-id="fddc9-126">Retrieves the horizontal offset of the target rectangle.</span></span><br/> |
| [<span data-ttu-id="fddc9-127">**obter \_ OffsetY**</span><span class="sxs-lookup"><span data-stu-id="fddc9-127">**get\_OffsetY**</span></span>](idxtcompositor-get-offsety.md)       | <span data-ttu-id="fddc9-128">Recupera o deslocamento vertical do retângulo de destino.</span><span class="sxs-lookup"><span data-stu-id="fddc9-128">Retrieves the vertical offset of the target rectangle.</span></span><br/>   |
| [<span data-ttu-id="fddc9-129">**obter \_ SrcHeight**</span><span class="sxs-lookup"><span data-stu-id="fddc9-129">**get\_SrcHeight**</span></span>](idxtcompositor-get-srcheight.md)   | <span data-ttu-id="fddc9-130">Recupera a altura do retângulo de origem.</span><span class="sxs-lookup"><span data-stu-id="fddc9-130">Retrieves the height of the source rectangle.</span></span><br/>            |
| [<span data-ttu-id="fddc9-131">**obter \_ SrcOffsetX**</span><span class="sxs-lookup"><span data-stu-id="fddc9-131">**get\_SrcOffsetX**</span></span>](idxtcompositor-get-srcoffsetx.md) | <span data-ttu-id="fddc9-132">Recupera o deslocamento horizontal do retângulo de origem.</span><span class="sxs-lookup"><span data-stu-id="fddc9-132">Retrieves the horizontal offset of the source rectangle.</span></span><br/> |
| [<span data-ttu-id="fddc9-133">**obter \_ SrcOffsetY**</span><span class="sxs-lookup"><span data-stu-id="fddc9-133">**get\_SrcOffsetY**</span></span>](idxtcompositor-get-srcoffsety.md) | <span data-ttu-id="fddc9-134">Recupera o deslocamento vertical do retângulo de origem.</span><span class="sxs-lookup"><span data-stu-id="fddc9-134">Retrieves the vertical offset of the source rectangle.</span></span><br/>   |
| [<span data-ttu-id="fddc9-135">**obter \_ SrcWidth**</span><span class="sxs-lookup"><span data-stu-id="fddc9-135">**get\_SrcWidth**</span></span>](idxtcompositor-get-srcwidth.md)     | <span data-ttu-id="fddc9-136">Recupera a largura do retângulo de origem.</span><span class="sxs-lookup"><span data-stu-id="fddc9-136">Retrieves the width of the source rectangle.</span></span><br/>             |
| [<span data-ttu-id="fddc9-137">**obter \_ largura**</span><span class="sxs-lookup"><span data-stu-id="fddc9-137">**get\_Width**</span></span>](idxtcompositor-get-width.md)           | <span data-ttu-id="fddc9-138">Recupera a largura do retângulo de destino.</span><span class="sxs-lookup"><span data-stu-id="fddc9-138">Retrieves the width of the target rectangle.</span></span><br/>             |
| [<span data-ttu-id="fddc9-139">**colocar \_ altura**</span><span class="sxs-lookup"><span data-stu-id="fddc9-139">**put\_Height**</span></span>](idxtcompositor-put-height.md)         | <span data-ttu-id="fddc9-140">Especifica a altura do retângulo de destino.</span><span class="sxs-lookup"><span data-stu-id="fddc9-140">Specifies the height of the target rectangle.</span></span><br/>            |
| [<span data-ttu-id="fddc9-141">**colocar \_ OffsetX**</span><span class="sxs-lookup"><span data-stu-id="fddc9-141">**put\_OffsetX**</span></span>](idxtcompositor-put-offsetx.md)       | <span data-ttu-id="fddc9-142">Especifica o deslocamento horizontal do retângulo de destino.</span><span class="sxs-lookup"><span data-stu-id="fddc9-142">Specifies the horizontal offset of the target rectangle.</span></span><br/> |
| [<span data-ttu-id="fddc9-143">**colocar \_ OffsetY**</span><span class="sxs-lookup"><span data-stu-id="fddc9-143">**put\_OffsetY**</span></span>](idxtcompositor-put-offsety.md)       | <span data-ttu-id="fddc9-144">Especifica o deslocamento vertical do retângulo de destino.</span><span class="sxs-lookup"><span data-stu-id="fddc9-144">Specifies the vertical offset of the target rectangle.</span></span><br/>   |
| [<span data-ttu-id="fddc9-145">**colocar \_ SrcHeight**</span><span class="sxs-lookup"><span data-stu-id="fddc9-145">**put\_SrcHeight**</span></span>](idxtcompositor-put-srcheight.md)   | <span data-ttu-id="fddc9-146">Especifica a altura do retângulo de origem.</span><span class="sxs-lookup"><span data-stu-id="fddc9-146">Specifies the height of the source rectangle.</span></span><br/>            |
| [<span data-ttu-id="fddc9-147">**colocar \_ SrcOffsetX**</span><span class="sxs-lookup"><span data-stu-id="fddc9-147">**put\_SrcOffsetX**</span></span>](idxtcompositor-put-srcoffsetx.md) | <span data-ttu-id="fddc9-148">Especifica o deslocamento horizontal do retângulo de origem.</span><span class="sxs-lookup"><span data-stu-id="fddc9-148">Specifies the horizontal offset of the source rectangle.</span></span><br/> |
| [<span data-ttu-id="fddc9-149">**colocar \_ SrcOffsetY**</span><span class="sxs-lookup"><span data-stu-id="fddc9-149">**put\_SrcOffsetY**</span></span>](idxtcompositor-put-srcoffsety.md) | <span data-ttu-id="fddc9-150">Especifica o deslocamento vertical do retângulo de origem.</span><span class="sxs-lookup"><span data-stu-id="fddc9-150">Specifies the vertical offset of the source rectangle.</span></span><br/>   |
| [<span data-ttu-id="fddc9-151">**colocar \_ SrcWidth**</span><span class="sxs-lookup"><span data-stu-id="fddc9-151">**put\_SrcWidth**</span></span>](idxtcompositor-put-srcwidth.md)     | <span data-ttu-id="fddc9-152">Especifica a largura do retângulo de origem.</span><span class="sxs-lookup"><span data-stu-id="fddc9-152">Specifies the width of the source rectangle.</span></span><br/>             |
| [<span data-ttu-id="fddc9-153">**colocar \_ largura**</span><span class="sxs-lookup"><span data-stu-id="fddc9-153">**put\_Width**</span></span>](idxtcompositor-put-width.md)           | <span data-ttu-id="fddc9-154">Especifica a largura do retângulo de destino.</span><span class="sxs-lookup"><span data-stu-id="fddc9-154">Specifies the width of the target rectangle.</span></span><br/>             |



 

## <a name="remarks"></a><span data-ttu-id="fddc9-155">Comentários</span><span class="sxs-lookup"><span data-stu-id="fddc9-155">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="fddc9-156">O arquivo de cabeçalho QEdit. h não é compatível com cabeçalhos do Direct3D posteriores à versão 7.</span><span class="sxs-lookup"><span data-stu-id="fddc9-156">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="fddc9-157">Para obter o QEdit. h, baixe a [atualização SDK do Microsoft Windows para Windows Vista e .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="fddc9-157">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="fddc9-158">O QEdit. h não está disponível no SDK do Microsoft Windows para Windows 7 e .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="fddc9-158">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="fddc9-159">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fddc9-159">Requirements</span></span>



| <span data-ttu-id="fddc9-160">Requisito</span><span class="sxs-lookup"><span data-stu-id="fddc9-160">Requirement</span></span> | <span data-ttu-id="fddc9-161">Valor</span><span class="sxs-lookup"><span data-stu-id="fddc9-161">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="fddc9-162">parâmetro</span><span class="sxs-lookup"><span data-stu-id="fddc9-162">Header</span></span><br/>  | <dl> <span data-ttu-id="fddc9-163"><dt>QEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="fddc9-163"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="fddc9-164">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="fddc9-164">Library</span></span><br/> | <dl> <span data-ttu-id="fddc9-165"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="fddc9-165"><dt>Strmiids.lib</dt></span></span> </dl> |



 

 




