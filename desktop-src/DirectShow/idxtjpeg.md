---
description: A interface IDxtJpeg define propriedades na transição de apagamento SMPTE. Essa interface é usada internamente pelos serviços de edição do DirectShow (DES) quando ele renderiza a transição de apagamento SMPTE.
ms.assetid: ce1920d4-ebe5-42d1-a2eb-d71ddeaf14fe
title: Interface IDxtJpeg (QEdit. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDxtJpeg
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: e9c32bee3f4041abaa9529036b7bc78250ac2487
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105760743"
---
# <a name="idxtjpeg-interface"></a><span data-ttu-id="c9c60-103">Interface IDxtJpeg</span><span class="sxs-lookup"><span data-stu-id="c9c60-103">IDxtJpeg interface</span></span>

> [!Note]  
> <span data-ttu-id="c9c60-104">\[Preterido.</span><span class="sxs-lookup"><span data-stu-id="c9c60-104">\[Deprecated.</span></span> <span data-ttu-id="c9c60-105">Essa API pode ser removida de versões futuras do Windows.\]</span><span class="sxs-lookup"><span data-stu-id="c9c60-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="c9c60-106">A `IDxtJpeg` interface define propriedades na transição de [apagamento SMPTE](smpte-wipe-transition.md) .</span><span class="sxs-lookup"><span data-stu-id="c9c60-106">The `IDxtJpeg` interface sets properties on the [SMPTE Wipe](smpte-wipe-transition.md) transition.</span></span>

<span data-ttu-id="c9c60-107">Essa interface é usada internamente pelos serviços de edição do DirectShow (DES) quando ele renderiza a transição de apagamento SMPTE.</span><span class="sxs-lookup"><span data-stu-id="c9c60-107">This interface is used internally by DirectShow Editing Services (DES) when it renders the SMPTE Wipe transition.</span></span> <span data-ttu-id="c9c60-108">Os aplicativos DES não precisam usar essa interface.</span><span class="sxs-lookup"><span data-stu-id="c9c60-108">DES applications do not need to use this interface.</span></span> <span data-ttu-id="c9c60-109">Para definir as propriedades em uma transição em DES, use a interface [**IPropertySetter**](ipropertysetter.md) .</span><span class="sxs-lookup"><span data-stu-id="c9c60-109">To set the properties on a transition in DES, use the [**IPropertySetter**](ipropertysetter.md) interface.</span></span>

## <a name="members"></a><span data-ttu-id="c9c60-110">Membros</span><span class="sxs-lookup"><span data-stu-id="c9c60-110">Members</span></span>

<span data-ttu-id="c9c60-111">A interface **IDxtJpeg** herda de **IDXEffect**.</span><span class="sxs-lookup"><span data-stu-id="c9c60-111">The **IDxtJpeg** interface inherits from **IDXEffect**.</span></span> <span data-ttu-id="c9c60-112">**IDxtJpeg** também tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="c9c60-112">**IDxtJpeg** also has these types of members:</span></span>

-   [<span data-ttu-id="c9c60-113">Métodos</span><span class="sxs-lookup"><span data-stu-id="c9c60-113">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="c9c60-114">Métodos</span><span class="sxs-lookup"><span data-stu-id="c9c60-114">Methods</span></span>

<span data-ttu-id="c9c60-115">A interface **IDxtJpeg** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="c9c60-115">The **IDxtJpeg** interface has these methods.</span></span>



| <span data-ttu-id="c9c60-116">Método</span><span class="sxs-lookup"><span data-stu-id="c9c60-116">Method</span></span>                                                     | <span data-ttu-id="c9c60-117">Descrição</span><span class="sxs-lookup"><span data-stu-id="c9c60-117">Description</span></span>                                                                               |
|:-----------------------------------------------------------|:------------------------------------------------------------------------------------------|
| [<span data-ttu-id="c9c60-118">**ApplyChanges**</span><span class="sxs-lookup"><span data-stu-id="c9c60-118">**ApplyChanges**</span></span>](idxtjpeg-applychanges.md)              | <span data-ttu-id="c9c60-119">Aplica todas as propriedades que foram alteradas.</span><span class="sxs-lookup"><span data-stu-id="c9c60-119">Applies any properties that have changed.</span></span><br/>                                      |
| [<span data-ttu-id="c9c60-120">**obter \_ BorderColor**</span><span class="sxs-lookup"><span data-stu-id="c9c60-120">**get\_BorderColor**</span></span>](idxtjpeg-get-bordercolor.md)       | <span data-ttu-id="c9c60-121">Recupera a cor da borda ao torno das bordas do padrão de apagamento.</span><span class="sxs-lookup"><span data-stu-id="c9c60-121">Retrieves the color of the border around the edges of the wipe pattern.</span></span><br/>        |
| [<span data-ttu-id="c9c60-122">**obter \_ BorderSoftness**</span><span class="sxs-lookup"><span data-stu-id="c9c60-122">**get\_BorderSoftness**</span></span>](idxtjpeg-get-bordersoftness.md) | <span data-ttu-id="c9c60-123">Recupera a largura da região borrada em volta das bordas do padrão de apagamento.</span><span class="sxs-lookup"><span data-stu-id="c9c60-123">Retrieves the width of the blurry region around the edges of the wipe pattern.</span></span><br/> |
| [<span data-ttu-id="c9c60-124">**obter \_ BorderWidth**</span><span class="sxs-lookup"><span data-stu-id="c9c60-124">**get\_BorderWidth**</span></span>](idxtjpeg-get-borderwidth.md)       | <span data-ttu-id="c9c60-125">Recupera a largura da borda sólida ao longo das bordas do padrão de apagamento.</span><span class="sxs-lookup"><span data-stu-id="c9c60-125">Retrieves the width of the solid border along the edges of the wipe pattern.</span></span><br/>   |
| [<span data-ttu-id="c9c60-126">**obter \_ máscaraname**</span><span class="sxs-lookup"><span data-stu-id="c9c60-126">**get\_MaskName**</span></span>](idxtjpeg-get-maskname.md)             | <span data-ttu-id="c9c60-127">Recupera o nome de um arquivo JPEG a ser usado como a máscara de apagamento.</span><span class="sxs-lookup"><span data-stu-id="c9c60-127">Retrieves the name of a JPEG file to be used as the wipe mask.</span></span><br/>                 |
| [<span data-ttu-id="c9c60-128">**obter \_ MaskNum**</span><span class="sxs-lookup"><span data-stu-id="c9c60-128">**get\_MaskNum**</span></span>](idxtjpeg-get-masknum.md)               | <span data-ttu-id="c9c60-129">Recupera o código de apagamento SMPTE do apagamento.</span><span class="sxs-lookup"><span data-stu-id="c9c60-129">Retrieves the SMPTE wipe code of the wipe.</span></span><br/>                                     |
| [<span data-ttu-id="c9c60-130">**obter \_ OffsetX**</span><span class="sxs-lookup"><span data-stu-id="c9c60-130">**get\_OffsetX**</span></span>](idxtjpeg-get-offsetx.md)               | <span data-ttu-id="c9c60-131">Recupera o deslocamento horizontal da origem do apagamento.</span><span class="sxs-lookup"><span data-stu-id="c9c60-131">Retrieves the horizontal offset of the wipe origin.</span></span><br/>                            |
| [<span data-ttu-id="c9c60-132">**obter \_ OffsetY**</span><span class="sxs-lookup"><span data-stu-id="c9c60-132">**get\_OffsetY**</span></span>](idxtjpeg-get-offsety.md)               | <span data-ttu-id="c9c60-133">Recupera o deslocamento vertical da origem do apagamento.</span><span class="sxs-lookup"><span data-stu-id="c9c60-133">Retrieves the vertical offset of the wipe origin.</span></span><br/>                              |
| [<span data-ttu-id="c9c60-134">**obter \_ ReplicateX**</span><span class="sxs-lookup"><span data-stu-id="c9c60-134">**get\_ReplicateX**</span></span>](idxtjpeg-get-replicatex.md)         | <span data-ttu-id="c9c60-135">Recupera o número de vezes que o padrão de apagamento é replicado horizontalmente.</span><span class="sxs-lookup"><span data-stu-id="c9c60-135">Retrieves the number of times the wipe pattern is replicated horizontally.</span></span><br/>     |
| [<span data-ttu-id="c9c60-136">**obter \_ complicação**</span><span class="sxs-lookup"><span data-stu-id="c9c60-136">**get\_ReplicateY**</span></span>](idxtjpeg-get-replicatey.md)         | <span data-ttu-id="c9c60-137">Recupera o número de vezes que o padrão de apagamento é replicado verticalmente.</span><span class="sxs-lookup"><span data-stu-id="c9c60-137">Retrieves the number of times the wipe pattern is replicated vertically.</span></span><br/>       |
| [<span data-ttu-id="c9c60-138">**obter \_ ScaleX**</span><span class="sxs-lookup"><span data-stu-id="c9c60-138">**get\_ScaleX**</span></span>](idxtjpeg-get-scalex.md)                 | <span data-ttu-id="c9c60-139">Recupera o valor pelo qual o apagamento é alongado horizontalmente.</span><span class="sxs-lookup"><span data-stu-id="c9c60-139">Retrieves the amount by which the wipe is stretched horizontally.</span></span><br/>              |
| [<span data-ttu-id="c9c60-140">**obter \_ ScaleY**</span><span class="sxs-lookup"><span data-stu-id="c9c60-140">**get\_ScaleY**</span></span>](idxtjpeg-get-scaley.md)                 | <span data-ttu-id="c9c60-141">Recupera o valor pelo qual o apagamento é alongado verticalmente.</span><span class="sxs-lookup"><span data-stu-id="c9c60-141">Retrieves the amount by which the wipe is stretched vertically.</span></span><br/>                |
| [<span data-ttu-id="c9c60-142">**LoadDefSettings**</span><span class="sxs-lookup"><span data-stu-id="c9c60-142">**LoadDefSettings**</span></span>](idxtjpeg-loaddefsettings.md)        | <span data-ttu-id="c9c60-143">Restaura as configurações padrão da transição de apagamento.</span><span class="sxs-lookup"><span data-stu-id="c9c60-143">Restores the default settings of the Wipe transition.</span></span><br/>                          |
| [<span data-ttu-id="c9c60-144">**colocar \_ BorderColor**</span><span class="sxs-lookup"><span data-stu-id="c9c60-144">**put\_BorderColor**</span></span>](idxtjpeg-put-bordercolor.md)       | <span data-ttu-id="c9c60-145">Especifica a cor da borda ao torno das bordas do padrão de apagamento.</span><span class="sxs-lookup"><span data-stu-id="c9c60-145">Specifies the color of the border around the edges of the wipe pattern.</span></span><br/>        |
| [<span data-ttu-id="c9c60-146">**colocar \_ BorderSoftness**</span><span class="sxs-lookup"><span data-stu-id="c9c60-146">**put\_BorderSoftness**</span></span>](idxtjpeg-put-bordersoftness.md) | <span data-ttu-id="c9c60-147">Especifica a largura da região borrada ao contrário das bordas do padrão de apagamento.</span><span class="sxs-lookup"><span data-stu-id="c9c60-147">Specifies the width of the blurry region around the edges of the wipe pattern.</span></span><br/> |
| [<span data-ttu-id="c9c60-148">**colocar \_ BorderWidth**</span><span class="sxs-lookup"><span data-stu-id="c9c60-148">**put\_BorderWidth**</span></span>](idxtjpeg-put-borderwidth.md)       | <span data-ttu-id="c9c60-149">Especifica a largura da borda sólida ao longo das bordas do padrão de apagamento.</span><span class="sxs-lookup"><span data-stu-id="c9c60-149">Specifies the width of the solid border along the edges of the wipe pattern.</span></span><br/>   |
| [<span data-ttu-id="c9c60-150">**colocar \_ maskname**</span><span class="sxs-lookup"><span data-stu-id="c9c60-150">**put\_MaskName**</span></span>](idxtjpeg-put-maskname.md)             | <span data-ttu-id="c9c60-151">Especifica o nome de um arquivo JPEG a ser usado como a máscara de apagamento.</span><span class="sxs-lookup"><span data-stu-id="c9c60-151">Specifies the name of a JPEG file to use as the wipe mask.</span></span><br/>                     |
| [<span data-ttu-id="c9c60-152">**colocar \_ MaskNum**</span><span class="sxs-lookup"><span data-stu-id="c9c60-152">**put\_MaskNum**</span></span>](idxtjpeg-put-masknum.md)               | <span data-ttu-id="c9c60-153">Especifica o código de apagamento SMPTE do apagamento.</span><span class="sxs-lookup"><span data-stu-id="c9c60-153">Specifies the SMPTE wipe code of the wipe.</span></span><br/>                                     |
| [<span data-ttu-id="c9c60-154">**colocar \_ OffsetX**</span><span class="sxs-lookup"><span data-stu-id="c9c60-154">**put\_OffsetX**</span></span>](idxtjpeg-put-offsetx.md)               | <span data-ttu-id="c9c60-155">Especifica o deslocamento horizontal da origem do apagamento.</span><span class="sxs-lookup"><span data-stu-id="c9c60-155">Specifies the horizontal offset of the wipe origin.</span></span><br/>                            |
| [<span data-ttu-id="c9c60-156">**colocar \_ OffsetY**</span><span class="sxs-lookup"><span data-stu-id="c9c60-156">**put\_OffsetY**</span></span>](idxtjpeg-put-offsety.md)               | <span data-ttu-id="c9c60-157">Especifica o deslocamento vertical da origem do apagamento.</span><span class="sxs-lookup"><span data-stu-id="c9c60-157">Specifies the vertical offset of the wipe origin.</span></span><br/>                              |
| [<span data-ttu-id="c9c60-158">**colocar \_ ReplicateX**</span><span class="sxs-lookup"><span data-stu-id="c9c60-158">**put\_ReplicateX**</span></span>](idxtjpeg-put-replicatex.md)         | <span data-ttu-id="c9c60-159">Especifica o número de vezes que o padrão de apagamento é replicado horizontalmente.</span><span class="sxs-lookup"><span data-stu-id="c9c60-159">Specifies the number of times the wipe pattern is replicated horizontally.</span></span><br/>     |
| [<span data-ttu-id="c9c60-160">**colocar \_ complicação**</span><span class="sxs-lookup"><span data-stu-id="c9c60-160">**put\_ReplicateY**</span></span>](idxtjpeg-put-replicatey.md)         | <span data-ttu-id="c9c60-161">Especifica o número de vezes que o padrão de apagamento é replicado verticalmente.</span><span class="sxs-lookup"><span data-stu-id="c9c60-161">Specifies the number of times the wipe pattern is replicated vertically.</span></span><br/>       |
| [<span data-ttu-id="c9c60-162">**colocar \_ ScaleX**</span><span class="sxs-lookup"><span data-stu-id="c9c60-162">**put\_ScaleX**</span></span>](idxtjpeg-put-scalex.md)                 | <span data-ttu-id="c9c60-163">Especifica o valor pelo qual o apagamento é alongado horizontalmente.</span><span class="sxs-lookup"><span data-stu-id="c9c60-163">Specifies the amount by which the wipe is stretched horizontally.</span></span><br/>              |
| [<span data-ttu-id="c9c60-164">**colocar \_ ScaleY**</span><span class="sxs-lookup"><span data-stu-id="c9c60-164">**put\_ScaleY**</span></span>](idxtjpeg-put-scaley.md)                 | <span data-ttu-id="c9c60-165">Especifica o valor pelo qual o apagamento é alongado verticalmente.</span><span class="sxs-lookup"><span data-stu-id="c9c60-165">Specifies the amount by which the wipe is stretched vertically.</span></span><br/>                |



 

## <a name="remarks"></a><span data-ttu-id="c9c60-166">Comentários</span><span class="sxs-lookup"><span data-stu-id="c9c60-166">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="c9c60-167">O arquivo de cabeçalho QEdit. h não é compatível com cabeçalhos do Direct3D posteriores à versão 7.</span><span class="sxs-lookup"><span data-stu-id="c9c60-167">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="c9c60-168">Para obter o QEdit. h, baixe a [atualização SDK do Microsoft Windows para Windows Vista e .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="c9c60-168">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="c9c60-169">O QEdit. h não está disponível no SDK do Microsoft Windows para Windows 7 e .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="c9c60-169">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="c9c60-170">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c9c60-170">Requirements</span></span>



| <span data-ttu-id="c9c60-171">Requisito</span><span class="sxs-lookup"><span data-stu-id="c9c60-171">Requirement</span></span> | <span data-ttu-id="c9c60-172">Valor</span><span class="sxs-lookup"><span data-stu-id="c9c60-172">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="c9c60-173">parâmetro</span><span class="sxs-lookup"><span data-stu-id="c9c60-173">Header</span></span><br/>  | <dl> <span data-ttu-id="c9c60-174"><dt>QEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="c9c60-174"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="c9c60-175">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="c9c60-175">Library</span></span><br/> | <dl> <span data-ttu-id="c9c60-176"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="c9c60-176"><dt>Strmiids.lib</dt></span></span> </dl> |



 

 




