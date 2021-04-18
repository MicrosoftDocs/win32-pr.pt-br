---
title: Elemento BuyCD
description: Observação Esta seção descreve a funcionalidade projetada para uso por lojas online. | Elemento BuyCD
ms.assetid: 01aaf20a-49ee-420b-a612-f09155390d4a
keywords:
- Elemento BuyCD do Windows Media Player
topic_type:
- apiref
api_name:
- BuyCD Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5ca1ebe4bd85015ca9ce1c0bece24e7dc47ff9fe
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105760459"
---
# <a name="buycd-element"></a><span data-ttu-id="bde41-105">Elemento BuyCD</span><span class="sxs-lookup"><span data-stu-id="bde41-105">BuyCD Element</span></span>

> [!Note]  
> <span data-ttu-id="bde41-106">Esta seção descreve a funcionalidade projetada para uso por lojas online.</span><span class="sxs-lookup"><span data-stu-id="bde41-106">This section describes functionality designed for use by online stores.</span></span> <span data-ttu-id="bde41-107">Não há suporte para o uso dessa funcionalidade fora do contexto de uma loja online.</span><span class="sxs-lookup"><span data-stu-id="bde41-107">Use of this functionality outside the context of an online store is not supported.</span></span>

 

<span data-ttu-id="bde41-108">O elemento **BuyCD** especifica as URLs para páginas da Web que o Windows Media Player exibe quando o usuário opta por fazer uma compra.</span><span class="sxs-lookup"><span data-stu-id="bde41-108">The **BuyCD** element specifies the URLs for webpages that Windows Media Player displays when the user chooses to make a purchase.</span></span>

``` syntax
<BuyCD
    MediaPlayerURL = "URL"
    MediaCenterURL = "URL"
    BrowserURL = "URL"
/>
```

## <a name="attributes"></a><span data-ttu-id="bde41-109">Atributos</span><span class="sxs-lookup"><span data-stu-id="bde41-109">Attributes</span></span>

<dl> <dt>

<span data-ttu-id="bde41-110"><span id="MediaPlayerURL__required_"></span><span id="mediaplayerurl__required_"></span><span id="MEDIAPLAYERURL__REQUIRED_"></span>**MediaPlayerURL** (obrigatório)</span><span class="sxs-lookup"><span data-stu-id="bde41-110"><span id="MediaPlayerURL__required_"></span><span id="mediaplayerurl__required_"></span><span id="MEDIAPLAYERURL__REQUIRED_"></span>**MediaPlayerURL** (required)</span></span>
</dt> <dd>

<span data-ttu-id="bde41-111">A URL da página da Web que a loja online exibe para oferecer um CD ou DVD para compra no Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="bde41-111">URL for the webpage that the online store displays to offer a CD or DVD for purchase in Windows Media Player.</span></span>

</dd> <dt>

<span data-ttu-id="bde41-112"><span id="MediaCenterURL"></span><span id="mediacenterurl"></span><span id="MEDIACENTERURL"></span>**MediaCenterURL**</span><span class="sxs-lookup"><span data-stu-id="bde41-112"><span id="MediaCenterURL"></span><span id="mediacenterurl"></span><span id="MEDIACENTERURL"></span>**MediaCenterURL**</span></span>
</dt> <dd>

<span data-ttu-id="bde41-113">A URL da página da Web que a loja online exibe para oferecer um CD ou DVD para compra na atualização do Windows XP Media Center Edition 2004.</span><span class="sxs-lookup"><span data-stu-id="bde41-113">URL for the webpage the online store displays to offer a CD or DVD for purchase in Windows XP Media Center Edition 2004 Update.</span></span>

</dd> <dt>

<span data-ttu-id="bde41-114"><span id="BrowserURL"></span><span id="browserurl"></span><span id="BROWSERURL"></span>**BrowserURL**</span><span class="sxs-lookup"><span data-stu-id="bde41-114"><span id="BrowserURL"></span><span id="browserurl"></span><span id="BROWSERURL"></span>**BrowserURL**</span></span>
</dt> <dd>

<span data-ttu-id="bde41-115">A URL da página da Web que a loja online exibe para oferecer um CD ou DVD para compra em uma janela separada do navegador.</span><span class="sxs-lookup"><span data-stu-id="bde41-115">URL for the webpage that the online store displays to offer a CD or DVD for purchase in a separate browser window.</span></span> <span data-ttu-id="bde41-116">Essa URL também é usada pelo Windows XP Service Pack 2 ou posterior para o recurso **comprar para música online** .</span><span class="sxs-lookup"><span data-stu-id="bde41-116">This URL is also used by Windows XP Service Pack 2 or later for the **Shop for music online** feature.</span></span>

</dd> </dl>

## <a name="parentchild-elements"></a><span data-ttu-id="bde41-117">Elementos pai/filho</span><span class="sxs-lookup"><span data-stu-id="bde41-117">Parent/Child Elements</span></span>



| <span data-ttu-id="bde41-118">Hierarquia</span><span class="sxs-lookup"><span data-stu-id="bde41-118">Hierarchy</span></span>       | <span data-ttu-id="bde41-119">Elemento</span><span class="sxs-lookup"><span data-stu-id="bde41-119">Element</span></span>         |
|-----------------|-----------------|
| <span data-ttu-id="bde41-120">Elementos pai</span><span class="sxs-lookup"><span data-stu-id="bde41-120">Parent elements</span></span> | <span data-ttu-id="bde41-121">**ServiceInfo**</span><span class="sxs-lookup"><span data-stu-id="bde41-121">**ServiceInfo**</span></span> |
| <span data-ttu-id="bde41-122">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="bde41-122">Child elements</span></span>  | <span data-ttu-id="bde41-123">Nenhum</span><span class="sxs-lookup"><span data-stu-id="bde41-123">None</span></span>            |



 

## <a name="remarks"></a><span data-ttu-id="bde41-124">Comentários</span><span class="sxs-lookup"><span data-stu-id="bde41-124">Remarks</span></span>

<span data-ttu-id="bde41-125">Quando o usuário clica em um botão ou link no Windows Media Player para comprar um CD ou DVD, o Player envia a solicitação de URL para ServiceTask1 com parâmetros anexados usando um separador de cadeia de caracteres de consulta de ponto de interrogação (?).</span><span class="sxs-lookup"><span data-stu-id="bde41-125">When the user clicks a button or link in Windows Media Player to purchase a CD or DVD, the Player sends the URL request to ServiceTask1 with parameters attached using a question mark (?) query string separator.</span></span> <span data-ttu-id="bde41-126">A tabela a seguir detalha os parâmetros enviados com a solicitação de URL.</span><span class="sxs-lookup"><span data-stu-id="bde41-126">The following table details the parameters sent with the URL request.</span></span> <span data-ttu-id="bde41-127">Outros podem estar presentes para fins de compatibilidade herdada.</span><span class="sxs-lookup"><span data-stu-id="bde41-127">Others may be present for legacy compatibility purposes.</span></span>



| <span data-ttu-id="bde41-128">Nome</span><span class="sxs-lookup"><span data-stu-id="bde41-128">Name</span></span>         | <span data-ttu-id="bde41-129">Valor</span><span class="sxs-lookup"><span data-stu-id="bde41-129">Value</span></span>                                                                                                                                                               |
|--------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bde41-130">*Álbuns*</span><span class="sxs-lookup"><span data-stu-id="bde41-130">*Album*</span></span>      | <span data-ttu-id="bde41-131">Valor do atributo **WM/campos AlbumTitle** para o item de mídia.</span><span class="sxs-lookup"><span data-stu-id="bde41-131">Value of the **WM/AlbumTitle** attribute for the media item.</span></span>                                                                                                        |
| <span data-ttu-id="bde41-132">*Autor*</span><span class="sxs-lookup"><span data-stu-id="bde41-132">*Artist*</span></span>     | <span data-ttu-id="bde41-133">Valor do atributo **WM/AlbumArtist** , se houver um, ou o valor do atributo **Author** para o item de mídia.</span><span class="sxs-lookup"><span data-stu-id="bde41-133">Value of the **WM/AlbumArtist** attribute, if one exists, or else the value of the **Author** attribute for the media item.</span></span>                                         |
| <span data-ttu-id="bde41-134">*GeoId*</span><span class="sxs-lookup"><span data-stu-id="bde41-134">*geoid*</span></span>      | <span data-ttu-id="bde41-135">ID da localização geográfica do Windows.</span><span class="sxs-lookup"><span data-stu-id="bde41-135">Windows geographical location ID.</span></span> <span data-ttu-id="bde41-136">A ID de local é especificada pelo usuário na área **local** das configurações de opções regionais e de idiomas no painel de controle.</span><span class="sxs-lookup"><span data-stu-id="bde41-136">The location ID is specified by the user in the **Location** area of the Regional and Language Options settings in Control Panel.</span></span> |
| <span data-ttu-id="bde41-137">*locale*</span><span class="sxs-lookup"><span data-stu-id="bde41-137">*locale*</span></span>     | <span data-ttu-id="bde41-138">ID de localidade do Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="bde41-138">Windows Media Player locale ID.</span></span>                                                                                                                                     |
| <span data-ttu-id="bde41-139">*Título*</span><span class="sxs-lookup"><span data-stu-id="bde41-139">*Title*</span></span>      | <span data-ttu-id="bde41-140">Valor do atributo de **título** para o item de mídia.</span><span class="sxs-lookup"><span data-stu-id="bde41-140">Value of the **Title** attribute for the media item.</span></span>                                                                                                                |
| <span data-ttu-id="bde41-141">*UFID*</span><span class="sxs-lookup"><span data-stu-id="bde41-141">*UFID*</span></span>       | <span data-ttu-id="bde41-142">Valor do atributo **WM/UniqueFileIdentifier** para o item de mídia.</span><span class="sxs-lookup"><span data-stu-id="bde41-142">Value of the **WM/UniqueFileIdentifier** attribute for the media item.</span></span>                                                                                              |
| <span data-ttu-id="bde41-143">*UserLocale*</span><span class="sxs-lookup"><span data-stu-id="bde41-143">*userlocale*</span></span> | <span data-ttu-id="bde41-144">IDENTIFICAÇÃO de localidade do Windows.</span><span class="sxs-lookup"><span data-stu-id="bde41-144">Windows locale ID.</span></span> <span data-ttu-id="bde41-145">A localidade é especificada pelo usuário na área **padrões e formatos** das configurações de opções regionais e de idiomas no painel de controle.</span><span class="sxs-lookup"><span data-stu-id="bde41-145">The locale is specified by the user in the **Standards and Formats** area of the Regional and Language Options settings in Control Panel.</span></span>        |
| <span data-ttu-id="bde41-146">*version*</span><span class="sxs-lookup"><span data-stu-id="bde41-146">*version*</span></span>    | <span data-ttu-id="bde41-147">Número de versão do Windows Media Player usando o seguinte formato: 10.0. x. xxxx ou 11.0. x. xxxx.</span><span class="sxs-lookup"><span data-stu-id="bde41-147">Windows Media Player version number using the following format: 10.0.x.xxxx or 11.0.x.xxxx.</span></span>                                                                         |



 

<span data-ttu-id="bde41-148">O Windows XP Media Center Edition 2004 fornece aos usuários uma interface do usuário projetada para ser exibida em uma distância.</span><span class="sxs-lookup"><span data-stu-id="bde41-148">Windows XP Media Center Edition 2004 provides users with a user interface designed to be viewed at a distance.</span></span> <span data-ttu-id="bde41-149">Você deve criar páginas da Web para que o parâmetro *MediaCenterURL* seja exibido em grandes exibições.</span><span class="sxs-lookup"><span data-stu-id="bde41-149">You should create webpages for the *MediaCenterURL* parameter to be viewed on large displays.</span></span>

## <a name="requirements"></a><span data-ttu-id="bde41-150">Requisitos</span><span class="sxs-lookup"><span data-stu-id="bde41-150">Requirements</span></span>



| <span data-ttu-id="bde41-151">Requisito</span><span class="sxs-lookup"><span data-stu-id="bde41-151">Requirement</span></span> | <span data-ttu-id="bde41-152">Valor</span><span class="sxs-lookup"><span data-stu-id="bde41-152">Value</span></span> |
|--------------------|----------------------------------------------|
| <span data-ttu-id="bde41-153">Versão</span><span class="sxs-lookup"><span data-stu-id="bde41-153">Version</span></span><br/> | <span data-ttu-id="bde41-154">Windows Media Player 10 ou posterior.</span><span class="sxs-lookup"><span data-stu-id="bde41-154">Windows Media Player 10 or later.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="bde41-155">Confira também</span><span class="sxs-lookup"><span data-stu-id="bde41-155">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bde41-156">**Documento de informações de exemplo para uma loja online tipo 1**</span><span class="sxs-lookup"><span data-stu-id="bde41-156">**Example ServiceInfo Document for a Type 1 Online Store**</span></span>](example-serviceinfo-document-for-a-type-1-online-store.md)
</dt> <dt>

[<span data-ttu-id="bde41-157">**Documento de informações de exemplo para uma loja online tipo 2**</span><span class="sxs-lookup"><span data-stu-id="bde41-157">**Example ServiceInfo Document for a Type 2 Online Store**</span></span>](example-serviceinfo-document-for-a-type-2-online-store.md)
</dt> <dt>

[<span data-ttu-id="bde41-158">**Documento do serviceInfo**</span><span class="sxs-lookup"><span data-stu-id="bde41-158">**ServiceInfo Document**</span></span>](serviceinfo-document.md)
</dt> </dl>

 

 





