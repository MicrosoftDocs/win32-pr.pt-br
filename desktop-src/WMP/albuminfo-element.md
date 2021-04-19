---
title: Elemento AlbumInfo
description: O elemento AlbumInfo especifica a URL para a página da Web que o Windows Media Player exibe quando o usuário escolhe para exibir mais informações sobre um item de mídia específico.
ms.assetid: c872e95a-3723-4ce8-8d61-e2bc9e12c785
keywords:
- Elemento AlbumInfo do Windows Media Player
topic_type:
- apiref
api_name:
- AlbumInfo Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c3805ae2d5fca687ce024efca74e0254db7c8ae3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105796448"
---
# <a name="albuminfo-element"></a><span data-ttu-id="fbf3c-104">Elemento AlbumInfo</span><span class="sxs-lookup"><span data-stu-id="fbf3c-104">AlbumInfo Element</span></span>

> [!Note]  
> <span data-ttu-id="fbf3c-105">Esta seção descreve a funcionalidade projetada para uso por lojas online.</span><span class="sxs-lookup"><span data-stu-id="fbf3c-105">This section describes functionality designed for use by online stores.</span></span> <span data-ttu-id="fbf3c-106">Não há suporte para o uso dessa funcionalidade fora do contexto de uma loja online.</span><span class="sxs-lookup"><span data-stu-id="fbf3c-106">Use of this functionality outside the context of an online store is not supported.</span></span>

 

<span data-ttu-id="fbf3c-107">O elemento **AlbumInfo** especifica a URL para a página da Web que o Windows Media Player exibe quando o usuário escolhe para exibir mais informações sobre um item de mídia específico.</span><span class="sxs-lookup"><span data-stu-id="fbf3c-107">The **AlbumInfo** element specifies the URL for the webpage that Windows Media Player displays when the user chooses to view more information about a particular media item.</span></span>

``` syntax
<AlbumInfo
   URL = "URL"
/>
      
```

## <a name="attributes"></a><span data-ttu-id="fbf3c-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="fbf3c-108">Attributes</span></span>

<dl> <dt>

<span data-ttu-id="fbf3c-109"><span id="URL__required_"></span><span id="url__required_"></span><span id="URL__REQUIRED_"></span>**URL** (obrigatório)</span><span class="sxs-lookup"><span data-stu-id="fbf3c-109"><span id="URL__required_"></span><span id="url__required_"></span><span id="URL__REQUIRED_"></span>**URL** (required)</span></span>
</dt> <dd>

<span data-ttu-id="fbf3c-110">URL da página da Web exibida pelo Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="fbf3c-110">URL for the webpage that Windows Media Player displays.</span></span>

</dd> </dl>

## <a name="parentchild-elements"></a><span data-ttu-id="fbf3c-111">Elementos pai/filho</span><span class="sxs-lookup"><span data-stu-id="fbf3c-111">Parent/Child Elements</span></span>



| <span data-ttu-id="fbf3c-112">Hierarquia</span><span class="sxs-lookup"><span data-stu-id="fbf3c-112">Hierarchy</span></span>       | <span data-ttu-id="fbf3c-113">Elemento</span><span class="sxs-lookup"><span data-stu-id="fbf3c-113">Element</span></span>         |
|-----------------|-----------------|
| <span data-ttu-id="fbf3c-114">Elementos pai</span><span class="sxs-lookup"><span data-stu-id="fbf3c-114">Parent elements</span></span> | <span data-ttu-id="fbf3c-115">**ServiceInfo**</span><span class="sxs-lookup"><span data-stu-id="fbf3c-115">**ServiceInfo**</span></span> |
| <span data-ttu-id="fbf3c-116">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="fbf3c-116">Child elements</span></span>  | <span data-ttu-id="fbf3c-117">Nenhum</span><span class="sxs-lookup"><span data-stu-id="fbf3c-117">None</span></span>            |



 

## <a name="remarks"></a><span data-ttu-id="fbf3c-118">Comentários</span><span class="sxs-lookup"><span data-stu-id="fbf3c-118">Remarks</span></span>

<span data-ttu-id="fbf3c-119">Quando o usuário clica em um botão no Windows Media Player para exibir informações adicionais sobre um item de mídia específico, o Player envia a solicitação de URL com parâmetros anexados usando um separador de cadeia de caracteres de consulta de ponto de interrogação (?).</span><span class="sxs-lookup"><span data-stu-id="fbf3c-119">When the user clicks a button in Windows Media Player to view additional information about a particular media item, the Player sends the URL request with parameters attached using a question mark (?) query string separator.</span></span> <span data-ttu-id="fbf3c-120">A tabela a seguir detalha os parâmetros enviados com a solicitação de URL.</span><span class="sxs-lookup"><span data-stu-id="fbf3c-120">The following table details the parameters sent with the URL request.</span></span> <span data-ttu-id="fbf3c-121">Outros podem estar presentes para fins de compatibilidade herdada.</span><span class="sxs-lookup"><span data-stu-id="fbf3c-121">Others may be present for legacy compatibility purposes.</span></span>



| <span data-ttu-id="fbf3c-122">Nome</span><span class="sxs-lookup"><span data-stu-id="fbf3c-122">Name</span></span>         | <span data-ttu-id="fbf3c-123">Valor</span><span class="sxs-lookup"><span data-stu-id="fbf3c-123">Value</span></span>                                                                                                                                                               |
|--------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fbf3c-124">*Álbuns*</span><span class="sxs-lookup"><span data-stu-id="fbf3c-124">*Album*</span></span>      | <span data-ttu-id="fbf3c-125">Valor do atributo **WM/campos AlbumTitle** para o item de mídia.</span><span class="sxs-lookup"><span data-stu-id="fbf3c-125">Value of the **WM/AlbumTitle** attribute for the media item.</span></span>                                                                                                        |
| <span data-ttu-id="fbf3c-126">*Autor*</span><span class="sxs-lookup"><span data-stu-id="fbf3c-126">*Artist*</span></span>     | <span data-ttu-id="fbf3c-127">Valor do atributo **WM/AlbumArtist** , se houver um, ou o valor do atributo **Author** para o item de mídia.</span><span class="sxs-lookup"><span data-stu-id="fbf3c-127">Value of the **WM/AlbumArtist** attribute, if one exists, or else the value of the **Author** attribute for the media item.</span></span>                                         |
| <span data-ttu-id="fbf3c-128">*GeoId*</span><span class="sxs-lookup"><span data-stu-id="fbf3c-128">*geoid*</span></span>      | <span data-ttu-id="fbf3c-129">ID da localização geográfica do Windows.</span><span class="sxs-lookup"><span data-stu-id="fbf3c-129">Windows geographical location ID.</span></span> <span data-ttu-id="fbf3c-130">A ID de local é especificada pelo usuário na área **local** das configurações de opções regionais e de idiomas no painel de controle.</span><span class="sxs-lookup"><span data-stu-id="fbf3c-130">The location ID is specified by the user in the **Location** area of the Regional and Language Options settings in Control Panel.</span></span> |
| <span data-ttu-id="fbf3c-131">*locale*</span><span class="sxs-lookup"><span data-stu-id="fbf3c-131">*locale*</span></span>     | <span data-ttu-id="fbf3c-132">ID de localidade do Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="fbf3c-132">Windows Media Player locale ID.</span></span>                                                                                                                                     |
| <span data-ttu-id="fbf3c-133">*Título*</span><span class="sxs-lookup"><span data-stu-id="fbf3c-133">*Title*</span></span>      | <span data-ttu-id="fbf3c-134">Valor do atributo de **título** para o item de mídia.</span><span class="sxs-lookup"><span data-stu-id="fbf3c-134">Value of the **Title** attribute for the media item.</span></span>                                                                                                                |
| <span data-ttu-id="fbf3c-135">*UFID*</span><span class="sxs-lookup"><span data-stu-id="fbf3c-135">*UFID*</span></span>       | <span data-ttu-id="fbf3c-136">Valor do atributo **WM/UniqueFileIdentifier** para o item de mídia.</span><span class="sxs-lookup"><span data-stu-id="fbf3c-136">Value of the **WM/UniqueFileIdentifier** attribute for the media item.</span></span>                                                                                              |
| <span data-ttu-id="fbf3c-137">*UserLocale*</span><span class="sxs-lookup"><span data-stu-id="fbf3c-137">*userlocale*</span></span> | <span data-ttu-id="fbf3c-138">IDENTIFICAÇÃO de localidade do Windows.</span><span class="sxs-lookup"><span data-stu-id="fbf3c-138">Windows locale ID.</span></span> <span data-ttu-id="fbf3c-139">A localidade é especificada pelo usuário na área **padrões e formatos** das configurações de opções regionais e de idiomas no painel de controle.</span><span class="sxs-lookup"><span data-stu-id="fbf3c-139">The locale is specified by the user in the **Standards and Formats** area of the Regional and Language Options settings in Control Panel.</span></span>        |
| <span data-ttu-id="fbf3c-140">*version*</span><span class="sxs-lookup"><span data-stu-id="fbf3c-140">*version*</span></span>    | <span data-ttu-id="fbf3c-141">Número de versão do Windows Media Player usando o seguinte formato: 10.0. x. xxxx ou 11.0. x. xxxx.</span><span class="sxs-lookup"><span data-stu-id="fbf3c-141">Windows Media Player version number using the following format: 10.0.x.xxxx or 11.0.x.xxxx.</span></span>                                                                         |



 

## <a name="requirements"></a><span data-ttu-id="fbf3c-142">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fbf3c-142">Requirements</span></span>



| <span data-ttu-id="fbf3c-143">Requisito</span><span class="sxs-lookup"><span data-stu-id="fbf3c-143">Requirement</span></span> | <span data-ttu-id="fbf3c-144">Valor</span><span class="sxs-lookup"><span data-stu-id="fbf3c-144">Value</span></span> |
|--------------------|----------------------------------------------|
| <span data-ttu-id="fbf3c-145">Versão</span><span class="sxs-lookup"><span data-stu-id="fbf3c-145">Version</span></span><br/> | <span data-ttu-id="fbf3c-146">Windows Media Player 10 ou posterior.</span><span class="sxs-lookup"><span data-stu-id="fbf3c-146">Windows Media Player 10 or later.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="fbf3c-147">Confira também</span><span class="sxs-lookup"><span data-stu-id="fbf3c-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fbf3c-148">**Documento de informações de exemplo para uma loja online tipo 1**</span><span class="sxs-lookup"><span data-stu-id="fbf3c-148">**Example ServiceInfo Document for a Type 1 Online Store**</span></span>](example-serviceinfo-document-for-a-type-1-online-store.md)
</dt> <dt>

[<span data-ttu-id="fbf3c-149">**Documento de informações de exemplo para uma loja online tipo 2**</span><span class="sxs-lookup"><span data-stu-id="fbf3c-149">**Example ServiceInfo Document for a Type 2 Online Store**</span></span>](example-serviceinfo-document-for-a-type-2-online-store.md)
</dt> <dt>

[<span data-ttu-id="fbf3c-150">**Documento do serviceInfo**</span><span class="sxs-lookup"><span data-stu-id="fbf3c-150">**ServiceInfo Document**</span></span>](serviceinfo-document.md)
</dt> </dl>

 

 





