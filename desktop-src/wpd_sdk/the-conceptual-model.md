---
description: O modelo conceitual
ms.assetid: f906466e-acdc-4d0f-bf27-c5a25dc56c01
title: O modelo conceitual
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8a17538e7fdb454fa8eb61ab951a3316b0f0c327
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104170993"
---
# <a name="the-conceptual-model"></a><span data-ttu-id="10297-103">O modelo conceitual</span><span class="sxs-lookup"><span data-stu-id="10297-103">The Conceptual Model</span></span>

<span data-ttu-id="10297-104">Esta seção descreve os objetos, as propriedades e os recursos que constituem o modelo conceitual WPD.</span><span class="sxs-lookup"><span data-stu-id="10297-104">This section describes the objects, properties, and resources that constitute the WPD conceptual model.</span></span>

### <a name="objects"></a><span data-ttu-id="10297-105">Objetos</span><span class="sxs-lookup"><span data-stu-id="10297-105">Objects</span></span>

<span data-ttu-id="10297-106">Em WPD, entidades lógicas em dispositivos são conhecidas como objetos.</span><span class="sxs-lookup"><span data-stu-id="10297-106">In WPD, logical entities on devices are referred to as objects.</span></span> <span data-ttu-id="10297-107">Normalmente, mas nem sempre, eles representam dados no dispositivo.</span><span class="sxs-lookup"><span data-stu-id="10297-107">Typically, but not always, these represent data on the device.</span></span> <span data-ttu-id="10297-108">Os objetos têm propriedades e são referenciados por identificadores de objeto.</span><span class="sxs-lookup"><span data-stu-id="10297-108">Objects have properties, and are referenced by object identifiers.</span></span> <span data-ttu-id="10297-109">Exemplos de objetos incluem imagens e pastas em uma câmera, músicas e listas de reprodução em um player de mídia, contatos em um telefone celular e assim por diante.</span><span class="sxs-lookup"><span data-stu-id="10297-109">Examples of objects include pictures and folders on a camera, songs and playlists on a media player, contacts on a mobile phone, and so on.</span></span>

<span data-ttu-id="10297-110">Os objetos também podem representar partes funcionais ou informativas do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="10297-110">Objects can also represent functional or informational parts of the device.</span></span> <span data-ttu-id="10297-111">Exemplos desses controles de Player (reproduzir/gravar/pausar), configurações de câmera, recursos de SMS de um telefone celular e assim por diante.</span><span class="sxs-lookup"><span data-stu-id="10297-111">Examples of these include player controls (play/record/pause), camera settings, a mobile phone's SMS capabilities, and so on.</span></span>

<span data-ttu-id="10297-112">Os dois tópicos a seguir fornecem exemplos e ilustrações de dois tipos de objetos: o objeto Image e o objeto Mediacast.</span><span class="sxs-lookup"><span data-stu-id="10297-112">The two following topics give examples and illustrations of two types of objects: the Image object and the Mediacast object.</span></span>

### <a name="image-object"></a><span data-ttu-id="10297-113">Objeto de imagem</span><span class="sxs-lookup"><span data-stu-id="10297-113">Image Object</span></span>

<span data-ttu-id="10297-114">Um objeto de imagem representa uma imagem ainda.</span><span class="sxs-lookup"><span data-stu-id="10297-114">An image object represents a still image.</span></span> <span data-ttu-id="10297-115">O diagrama a seguir mostra as relações entre um objeto Image, suas propriedades e seus recursos.</span><span class="sxs-lookup"><span data-stu-id="10297-115">The following diagram shows the relationships between an Image object, its properties, and its resources.</span></span>

![diagrama mostrando um objeto WPD e sua relação com suas propriedades e recursos](images/wpd-overview-figure2.gif)

<span data-ttu-id="10297-117">Para obter mais informações sobre o objeto de imagem e suas propriedades, consulte o tópico [**\_ imagem de \_ tipo \_ de conteúdo WPD**](wpd-content-type-image.md) .</span><span class="sxs-lookup"><span data-stu-id="10297-117">For more information about the Image object and its properties, see the [**WPD\_CONTENT\_TYPE\_IMAGE**](wpd-content-type-image.md) topic.</span></span>

### <a name="mediacast-object"></a><span data-ttu-id="10297-118">Objeto Mediacast</span><span class="sxs-lookup"><span data-stu-id="10297-118">Mediacast Object</span></span>

<span data-ttu-id="10297-119">Um objeto Mediacast pode ser considerado como um objeto de contêiner que agrupa conteúdo relacionado, assim como uma lista de reprodução de músicas.</span><span class="sxs-lookup"><span data-stu-id="10297-119">A Mediacast object can be thought of as a container object that groups related content, just as a playlist groups music.</span></span> <span data-ttu-id="10297-120">Geralmente, um objeto Mediacast é usado para agrupar o conteúdo de mídia que foi publicado online.</span><span class="sxs-lookup"><span data-stu-id="10297-120">Often, a Mediacast object is used to group media content that was published online.</span></span> <span data-ttu-id="10297-121">Por exemplo, um canal RSS pode ser representado como um objeto Mediacast, cujas referências de objeto apontam para objetos de conteúdo que representam cada item no canal.</span><span class="sxs-lookup"><span data-stu-id="10297-121">For example, an RSS channel can be represented as a Mediacast object whose object references point to content objects that represent each item in the channel.</span></span> <span data-ttu-id="10297-122">O diagrama a seguir mostra a relação entre um objeto Mediacast e os três objetos de áudio que ele contém.</span><span class="sxs-lookup"><span data-stu-id="10297-122">The following diagram shows the relationship between a Mediacast object and the three audio objects it contains.</span></span>

![diagrama mostrando a estrutura hierárquica de um objeto medicast e três objetos que ele contém](images/mediacast1.gif)

<span data-ttu-id="10297-124">As referências ao objeto de áudio são especificadas na propriedade [de \_ \_ referências de objeto WPD](object-properties.md) para o objeto Mediacast.</span><span class="sxs-lookup"><span data-stu-id="10297-124">The references to the audio object are specified in the [WPD\_OBJECT\_REFERENCES](object-properties.md) property for the Mediacast object.</span></span> <span data-ttu-id="10297-125">Para obter mais informações sobre as propriedades com suporte de um objeto Mediacast, consulte o tópico de [**\_ conteúdo de \_ \_ mídia \_ WPD**](wpd-content-type-media-cast.md) .</span><span class="sxs-lookup"><span data-stu-id="10297-125">For more information about the properties supported by a Mediacast object, see the [**WPD\_CONTENT\_TYPE\_MEDIA\_CAST**](wpd-content-type-media-cast.md) topic.</span></span>

### <a name="properties"></a><span data-ttu-id="10297-126">Propriedades</span><span class="sxs-lookup"><span data-stu-id="10297-126">Properties</span></span>

<span data-ttu-id="10297-127">As propriedades do objeto fornecem um mecanismo para a troca de metadados que descrevem objetos.</span><span class="sxs-lookup"><span data-stu-id="10297-127">Object properties provide a mechanism for exchanging object-describing metadata.</span></span> <span data-ttu-id="10297-128">Por exemplo, um objeto de imagem pode incluir propriedades que descrevem seu nome de arquivo, tamanho, formato, largura em pixels e assim por diante.</span><span class="sxs-lookup"><span data-stu-id="10297-128">For example, an image object may include properties that describe its filename, size, format, width in pixels, and so on.</span></span>

<span data-ttu-id="10297-129">As propriedades têm um valor atual, bem como atributos.</span><span class="sxs-lookup"><span data-stu-id="10297-129">Properties have a current value, as well as attributes.</span></span> <span data-ttu-id="10297-130">WPD define um conjunto de propriedades padrão que compõem as definições de API e de DDI.</span><span class="sxs-lookup"><span data-stu-id="10297-130">WPD defines a set of standard properties that make up the API and DDI definitions.</span></span> <span data-ttu-id="10297-131">Os fornecedores não estão limitados às propriedades predefinidas do WPD e são livres para adicionar seus próprios.</span><span class="sxs-lookup"><span data-stu-id="10297-131">Vendors are not limited to the predefined WPD properties and are free to add their own.</span></span>

### <a name="property-attributes"></a><span data-ttu-id="10297-132">Atributos de propriedade</span><span class="sxs-lookup"><span data-stu-id="10297-132">Property Attributes</span></span>

<span data-ttu-id="10297-133">Atributos de propriedade descrevem os direitos de acesso, os valores válidos e outras informações relacionadas a uma propriedade.</span><span class="sxs-lookup"><span data-stu-id="10297-133">Property attributes describe the access rights, valid values, and other information related to a property.</span></span> <span data-ttu-id="10297-134">Por exemplo, a propriedade que representa a taxa de bits pode ser um intervalo de 8 kilobits por segundo (Kbps) a 20 Kbps com um valor de etapa de 1 kbps.</span><span class="sxs-lookup"><span data-stu-id="10297-134">For example, the property representing bit rate could be a range from 8 kilobits per second (Kbps) to 20 Kbps with a step value of 1 Kbps.</span></span>

<span data-ttu-id="10297-135">Direitos de acesso indicam se os chamadores podem ler, gravar e/ou excluir a propriedade.</span><span class="sxs-lookup"><span data-stu-id="10297-135">Access rights indicate whether callers can read, write and/or delete the property.</span></span> <span data-ttu-id="10297-136">Os valores válidos indicam restrições para valores de propriedade.</span><span class="sxs-lookup"><span data-stu-id="10297-136">Valid values indicate restrictions for property values.</span></span> <span data-ttu-id="10297-137">Os valores válidos são considerados de um formulário específico.</span><span class="sxs-lookup"><span data-stu-id="10297-137">Valid values are said to be of a specific form.</span></span> <span data-ttu-id="10297-138">Os formulários de valor válidos incluem intervalo (ou seja, a propriedade pode levar um valor de mín a máx com a etapa especificada), a enumeração (ou seja, o valor da propriedade é um daqueles na lista especificada) e nenhum (ou seja, não há valores válidos específicos).</span><span class="sxs-lookup"><span data-stu-id="10297-138">Valid value forms include Range (that is, property can take a value from Min to Max with specified Step), Enumeration (that is, property value is one of those in the specified List), and None (that is, there are no specific valid values).</span></span>

### <a name="resources"></a><span data-ttu-id="10297-139">Recursos</span><span class="sxs-lookup"><span data-stu-id="10297-139">Resources</span></span>

<span data-ttu-id="10297-140">Os recursos são espaços reservados para dados binários.</span><span class="sxs-lookup"><span data-stu-id="10297-140">Resources are placeholders for binary data.</span></span> <span data-ttu-id="10297-141">Um objeto pode ter mais de um recurso.</span><span class="sxs-lookup"><span data-stu-id="10297-141">An object can have more than one resource.</span></span> <span data-ttu-id="10297-142">Por exemplo, se o objeto representasse um arquivo de imagem com uma anotação de áudio, os recursos desse objeto poderão ser os seguintes:</span><span class="sxs-lookup"><span data-stu-id="10297-142">For example, if the object represented an image file with an audio annotation, then the resources for this object might be as follows:</span></span>

-   <span data-ttu-id="10297-143">Um recurso padrão.</span><span class="sxs-lookup"><span data-stu-id="10297-143">A default resource.</span></span> <span data-ttu-id="10297-144">Esse recurso representa o arquivo de imagem inteiro.</span><span class="sxs-lookup"><span data-stu-id="10297-144">This resource represents the entire image file.</span></span> <span data-ttu-id="10297-145">(Isso inclui todos os dados inseridos, como anotações de áudio, miniaturas e assim por diante)</span><span class="sxs-lookup"><span data-stu-id="10297-145">(This includes any embedded data such as audio annotations, thumbnails, and so on)</span></span>
-   <span data-ttu-id="10297-146">Um recurso de miniatura.</span><span class="sxs-lookup"><span data-stu-id="10297-146">A thumbnail resource.</span></span> <span data-ttu-id="10297-147">Esse recurso representa os dados de miniatura da imagem.</span><span class="sxs-lookup"><span data-stu-id="10297-147">This resource represents the thumbnail data for the image.</span></span>
-   <span data-ttu-id="10297-148">Um recurso de anotação de áudio.</span><span class="sxs-lookup"><span data-stu-id="10297-148">An audio annotation resource.</span></span> <span data-ttu-id="10297-149">Esse recurso representa os dados de áudio associados à imagem.</span><span class="sxs-lookup"><span data-stu-id="10297-149">This resource represents the audio data associated with the image.</span></span>

### <a name="resource-attributes"></a><span data-ttu-id="10297-150">Atributos de recurso</span><span class="sxs-lookup"><span data-stu-id="10297-150">Resource Attributes</span></span>

<span data-ttu-id="10297-151">Semelhante aos atributos de propriedade, os atributos de recurso descrevem os direitos de acesso, o tamanho, o formato e outras informações relacionadas a um recurso.</span><span class="sxs-lookup"><span data-stu-id="10297-151">Similar to property attributes, resource attributes describe the access rights, size, format, and other information related to a resource.</span></span> <span data-ttu-id="10297-152">Por exemplo, os atributos de um recurso de anotação de áudio em um objeto de imagem podem especificar a taxa de bits, a contagem de canais e o formato de dados do áudio.</span><span class="sxs-lookup"><span data-stu-id="10297-152">For example, the attributes for an audio annotation resource on an image object may specify the bit rate, channel count, and data format of the audio.</span></span>

### <a name="rendering-profiles-and-resource-attributes"></a><span data-ttu-id="10297-153">Perfis de renderização e atributos de recurso</span><span class="sxs-lookup"><span data-stu-id="10297-153">Rendering Profiles and Resource Attributes</span></span>

<span data-ttu-id="10297-154">O perfil de renderização é um método usado pelos aplicativos para descobrir os atributos válidos para um determinado recurso.</span><span class="sxs-lookup"><span data-stu-id="10297-154">The rendering profile is one method that applications use to discover the valid attributes for a given resource.</span></span> <span data-ttu-id="10297-155">Por exemplo, um telefone celular pode dar suporte a bitmaps com restrições específicas nos valores mínimo e máximo de largura e altura.</span><span class="sxs-lookup"><span data-stu-id="10297-155">For example, a mobile phone may support bitmaps with specific restrictions on the minimum and maximum width and height values.</span></span> <span data-ttu-id="10297-156">Consultando os perfis de renderização do objeto bitmap, um aplicativo pode recuperar esses valores exatos.</span><span class="sxs-lookup"><span data-stu-id="10297-156">By querying the rendering profiles for the bitmap object, an application can retrieve those exact values.</span></span>

<span data-ttu-id="10297-157">A saída de exemplo a seguir identifica as informações de perfil de renderização que o dispositivo retornaria se ele der suporte a bitmaps com uma altura mínima de 10 pixels, uma largura mínima de 20 pixels, uma altura máxima de 1000 pixels e uma largura máxima de 2000 pixels.</span><span class="sxs-lookup"><span data-stu-id="10297-157">The following sample output identifies the rendering profile information that the device would return if it supported bitmaps with a minimum height of 10 pixels, a minimum width of 20 pixels, a maximum height of 1000 pixels and a maximum width of 2000 pixels.</span></span>


```C++
WPD_OBJECT_FORMAT = WPD_OBJECT_FORMAT_BMP
WPD_MEDIA_HEIGHT:
        WPD_PROPERTY_ATTRIBUTE_FORM = WPD_PROPERTY_ATTRIBUTE_FORM_RANGE
        WPD_PROPERTY_ATTRIBUTE_DEFAULT_VALUE =  10
        WPD_PROPERTY_ATTRIBUTE_RANGE_MIN =  10 
        WPD_PROPERTY_ATTRIBUTE_RANGE_MAX = 1000
        WPD_PROPERTY_ATTRIBUTE_RANGE_STEP = 1
WPD_MEDIA_WIDTH:
        WPD_PROPERTY_ATTRIBUTE_FORM = WPD_PROPERTY_ATTRIBUTE_FORM_RANGE
        WPD_PROPERTY_ATTRIBUTE_DEFAULT_VALUE =  20 
        WPD_PROPERTY_ATTRIBUTE_RANGE_MIN =  20 
        WPD_PROPERTY_ATTRIBUTE_RANGE_MAX =  2000
        WPD_PROPERTY_ATTRIBUTE_RANGE_STEP = 1
WPD_RESOURCE_ATTRIBUTE_TOTAL_SIZE:
        WPD_PROPERTY_ATTRIBUTE_FORM = WPD_PROPERTY_ATTRIBUTE_FORM_RANGE
        WPD_PROPERTY_ATTRIBUTE_DEFAULT_VALUE = 0
        WPD_PROPERTY_ATTRIBUTE_RANGE_MIN =  2000 
        WPD_PROPERTY_ATTRIBUTE_RANGE_MAX = 1000000
        WPD_PROPERTY_ATTRIBUTE_RANGE_STEP = 1
```



<span data-ttu-id="10297-158">Consulte o tópico [recuperando os recursos de renderização com suporte em um dispositivo](retrieving-the-rendering-capabilities-supported-by-a-device.md) no guia de programação para obter uma descrição de como seu aplicativo pode recuperar um perfil de renderização (e os atributos de recurso associados).</span><span class="sxs-lookup"><span data-stu-id="10297-158">See the [Retrieving the Rendering Capabilities Supported by a Device](retrieving-the-rendering-capabilities-supported-by-a-device.md) topic in the programming guide for a description of how your application can retrieve a rendering profile (and the associated resource attributes).</span></span>

## <a name="related-topics"></a><span data-ttu-id="10297-159">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="10297-159">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="10297-160">**Visão geral do aplicativo**</span><span class="sxs-lookup"><span data-stu-id="10297-160">**Application Overview**</span></span>](application-overview.md)
</dt> </dl>

 

 



