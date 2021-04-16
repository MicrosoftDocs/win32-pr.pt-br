---
description: Metadados de mídia
ms.assetid: dd7c4bc9-e2a6-49cd-8f29-865a44d5b5c9
title: Metadados de mídia
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: adb17f286673663976e17b4178239507765c2101
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/03/2021
ms.locfileid: "105761566"
---
# <a name="media-metadata"></a><span data-ttu-id="cc4a7-103">Metadados de mídia</span><span class="sxs-lookup"><span data-stu-id="cc4a7-103">Media Metadata</span></span>

<span data-ttu-id="cc4a7-104">Os arquivos de mídia contêm propriedades que descrevem o conteúdo do arquivo.</span><span class="sxs-lookup"><span data-stu-id="cc4a7-104">Media files contain properties that describe the contents of the file.</span></span> <span data-ttu-id="cc4a7-105">No Microsoft Media Foundation, essas propriedades podem ser categorizadas da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="cc4a7-105">In Microsoft Media Foundation, these properties can be categorized as follows:</span></span>

-   <span data-ttu-id="cc4a7-106">**Atributos de tipo de mídia** especificam os parâmetros de codificação, como o algoritmo de codificação (subtipo de mídia), o tamanho do quadro de vídeo, a taxa de quadros de vídeo, a taxa de bits de áudio e a taxa de amostragem de áudio.</span><span class="sxs-lookup"><span data-stu-id="cc4a7-106">**Media-type attributes** specify the encoding parameters, such as the encoding algorithm (media subtype), video frame size, video frame rate, audio bit rate, and audio sample rate.</span></span> <span data-ttu-id="cc4a7-107">Para obter mais informações sobre atributos de tipo de mídia, consulte [tipos de mídia](media-types.md).</span><span class="sxs-lookup"><span data-stu-id="cc4a7-107">For more information about media-type attributes, see [Media Types](media-types.md).</span></span>
-   <span data-ttu-id="cc4a7-108">Os **metadados** contêm informações descritivas para o conteúdo de mídia, como título, artista, compositor e gênero.</span><span class="sxs-lookup"><span data-stu-id="cc4a7-108">**Metadata** contains descriptive information for the media content, such as title, artist, composer, and genre.</span></span> <span data-ttu-id="cc4a7-109">Os metadados também podem descrever os parâmetros de codificação.</span><span class="sxs-lookup"><span data-stu-id="cc4a7-109">Metadata can also describe encoding parameters.</span></span> <span data-ttu-id="cc4a7-110">Pode ser mais rápido acessar essas informações por meio de metadados do que por meio de atributos de tipo de mídia.</span><span class="sxs-lookup"><span data-stu-id="cc4a7-110">It can be faster to access this information through metadata than through media-type attributes.</span></span>
-   <span data-ttu-id="cc4a7-111">**As propriedades de DRM** contêm informações sobre restrições de uso.</span><span class="sxs-lookup"><span data-stu-id="cc4a7-111">**DRM properties** contain information on usage restrictions.</span></span> <span data-ttu-id="cc4a7-112">Atualmente Media Foundation não oferece suporte a propriedades de DRM por meio de metadados, com exceção da propriedade **PKEY \_ DRM \_ isproteged** .</span><span class="sxs-lookup"><span data-stu-id="cc4a7-112">Currently Media Foundation does not support DRM properties through metadata, with the exception of the **PKEY\_DRM\_IsProtected** property.</span></span>

<span data-ttu-id="cc4a7-113">Há duas maneiras de ler metadados em Media Foundation:</span><span class="sxs-lookup"><span data-stu-id="cc4a7-113">There are two ways to read metadata in Media Foundation:</span></span>

-   <span data-ttu-id="cc4a7-114">A interface [**IMFMetadata**](/windows/desktop/api/mfidl/nn-mfidl-imfmetadata) (Media Foundation metadados da versão 1).</span><span class="sxs-lookup"><span data-stu-id="cc4a7-114">The [**IMFMetadata**](/windows/desktop/api/mfidl/nn-mfidl-imfmetadata) interface (Media Foundation version 1 metadata).</span></span>
-   <span data-ttu-id="cc4a7-115">A interface [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) do shell do Windows (metadados do Shell).</span><span class="sxs-lookup"><span data-stu-id="cc4a7-115">The Windows Shell [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) interface (Shell metadata).</span></span>

<span data-ttu-id="cc4a7-116">Os metadados do Shell pertencem não apenas aos arquivos de mídia, mas a um intervalo muito maior de arquivos no sistema.</span><span class="sxs-lookup"><span data-stu-id="cc4a7-116">Shell metadata pertains not only to media files but to a much wider range of files on the system.</span></span>

<span data-ttu-id="cc4a7-117">A tabela a seguir compara os recursos e as limitações de cada API de metadados.</span><span class="sxs-lookup"><span data-stu-id="cc4a7-117">The following table compares the features and limitations of each metadata API.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="cc4a7-118">Metadados do Media Foundation v1</span><span class="sxs-lookup"><span data-stu-id="cc4a7-118">Media Foundation v1 Metadata</span></span></th>
<th><span data-ttu-id="cc4a7-119">Metadados do Shell</span><span class="sxs-lookup"><span data-stu-id="cc4a7-119">Shell Metadata</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="cc4a7-120">Requer o Windows Vista ou posterior.</span><span class="sxs-lookup"><span data-stu-id="cc4a7-120">Requires Windows Vista or later.</span></span></td>
<td><span data-ttu-id="cc4a7-121">Requer o Windows 7.</span><span class="sxs-lookup"><span data-stu-id="cc4a7-121">Requires Windows 7.</span></span>
<blockquote>
[!Note]<br />
<span data-ttu-id="cc4a7-122">Os metadados do Shell em geral não exigem o Windows 7, mas Media Foundation não dava suporte aos metadados do Shell antes do Windows 7.</span><span class="sxs-lookup"><span data-stu-id="cc4a7-122">Shell metadata in general does not require Windows 7, but Media Foundation did not support Shell metadata prior to Windows 7.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="cc4a7-123">As propriedades não são compatíveis com o sistema de propriedades do Shell.</span><span class="sxs-lookup"><span data-stu-id="cc4a7-123">Properties are not compatible with Shell property system.</span></span></td>
<td><span data-ttu-id="cc4a7-124">As propriedades são compatíveis com o sistema de propriedades do Shell.</span><span class="sxs-lookup"><span data-stu-id="cc4a7-124">Properties are compatible with the Shell property system.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="cc4a7-125">As propriedades podem ser aplicadas a todo o arquivo ou no nível do fluxo.</span><span class="sxs-lookup"><span data-stu-id="cc4a7-125">Properties can apply to the entire file, or at the stream level.</span></span></td>
<td><span data-ttu-id="cc4a7-126">Há suporte apenas para propriedades em nível de arquivo.</span><span class="sxs-lookup"><span data-stu-id="cc4a7-126">Only file-level properties are supported.</span></span> <span data-ttu-id="cc4a7-127">Não há suporte para propriedades em nível de fluxo.</span><span class="sxs-lookup"><span data-stu-id="cc4a7-127">Stream-level properties are not supported.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="cc4a7-128">As propriedades podem ter valores em vários idiomas.</span><span class="sxs-lookup"><span data-stu-id="cc4a7-128">Properties can have values in multiple languages.</span></span></td>
<td><span data-ttu-id="cc4a7-129">Não há suporte para valores em vários idiomas.</span><span class="sxs-lookup"><span data-stu-id="cc4a7-129">Values in multiple languages are not supported.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="cc4a7-130">As chaves de propriedade são cadeias de caracteres largos.</span><span class="sxs-lookup"><span data-stu-id="cc4a7-130">Property keys are wide-character strings.</span></span></td>
<td><span data-ttu-id="cc4a7-131">As chaves de propriedade são valores de <a href="/windows/desktop/api/wtypes/ns-wtypes-propertykey"><strong>PROPERTYKEY</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="cc4a7-131">Property keys are <a href="/windows/desktop/api/wtypes/ns-wtypes-propertykey"><strong>PROPERTYKEY</strong></a> values.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="cc4a7-132">Os valores de propriedade são valores de <a href="/windows/win32/api/propidl/ns-propidl-propvariant"><strong>PROPVARIANT</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="cc4a7-132">Property values are <a href="/windows/win32/api/propidl/ns-propidl-propvariant"><strong>PROPVARIANT</strong></a> values.</span></span></td>
<td><span data-ttu-id="cc4a7-133">Os valores de propriedade são valores de <a href="/windows/win32/api/propidl/ns-propidl-propvariant"><strong>PROPVARIANT</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="cc4a7-133">Property values are <a href="/windows/win32/api/propidl/ns-propidl-propvariant"><strong>PROPVARIANT</strong></a> values.</span></span></td>
</tr>
</tbody>
</table>



 

## <a name="in-this-section"></a><span data-ttu-id="cc4a7-134">Nesta seção</span><span class="sxs-lookup"><span data-stu-id="cc4a7-134">In this section</span></span>



| <span data-ttu-id="cc4a7-135">Tópico</span><span class="sxs-lookup"><span data-stu-id="cc4a7-135">Topic</span></span>                                                                                     | <span data-ttu-id="cc4a7-136">Descrição</span><span class="sxs-lookup"><span data-stu-id="cc4a7-136">Description</span></span>                                                                                                                                |
|-------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="cc4a7-137">Provedores de metadados do Shell</span><span class="sxs-lookup"><span data-stu-id="cc4a7-137">Shell Metadata Providers</span></span>](shell-metadata-providers.md)<br/>                       | <span data-ttu-id="cc4a7-138">A partir do Windows 7, Media Foundation expõe os metadados por meio da interface [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) .</span><span class="sxs-lookup"><span data-stu-id="cc4a7-138">Starting in Windows 7, Media Foundation exposes metadata through the [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) interface.</span></span><br/> |
| [<span data-ttu-id="cc4a7-139">Propriedades de metadados para Arquivos de mídia</span><span class="sxs-lookup"><span data-stu-id="cc4a7-139">Metadata Properties for Media Files</span></span>](metadata-properties-for-media-files.md)<br/> | <span data-ttu-id="cc4a7-140">Este tópico lista as propriedades de metadados mais comuns para arquivos de mídia.</span><span class="sxs-lookup"><span data-stu-id="cc4a7-140">This topic lists the most common metadata properties for media files.</span></span><br/>                                                           |
| [<span data-ttu-id="cc4a7-141">Provedores de metadados no Windows Vista</span><span class="sxs-lookup"><span data-stu-id="cc4a7-141">Metadata Providers in Windows Vista</span></span>](metadata-providers-in-windows-vista.md)<br/> | <span data-ttu-id="cc4a7-142">No Windows Vista, Media Foundation expõe metadados por meio da interface [**IMFMetadata**](/windows/desktop/api/mfidl/nn-mfidl-imfmetadata) .</span><span class="sxs-lookup"><span data-stu-id="cc4a7-142">In Windows Vista, Media Foundation exposes metadata through the [**IMFMetadata**](/windows/desktop/api/mfidl/nn-mfidl-imfmetadata) interface.</span></span><br/>                   |



 

<span data-ttu-id="cc4a7-143">Se você estiver implementando uma fonte de mídia personalizada e quiser expor metadados do Shell, consulte [provedores de metadados personalizados para arquivos de mídia](custom-metadata-providers-for-media-files.md).</span><span class="sxs-lookup"><span data-stu-id="cc4a7-143">If you are implementing a custom media source and want to expose Shell metadata, see [Custom Metadata Providers for Media Files](custom-metadata-providers-for-media-files.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="cc4a7-144">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="cc4a7-144">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="cc4a7-145">Guia de programação Media Foundation</span><span class="sxs-lookup"><span data-stu-id="cc4a7-145">Media Foundation Programming Guide</span></span>](media-foundation-programming-guide.md)
</dt> </dl>

 

 
