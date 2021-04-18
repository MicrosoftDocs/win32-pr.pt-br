---
title: Elemento serviceInfo
description: Observação Esta seção descreve a funcionalidade projetada para uso por lojas online. Não há suporte para o uso dessa funcionalidade fora do contexto de uma loja online. O elemento serviceInfo é o elemento principal para o ServiceInfo.xml documento.
ms.assetid: d2f9e642-143e-405d-8588-c78e4355b9b9
keywords:
- Elemento serviceInfo do Windows Media Player
topic_type:
- apiref
api_name:
- ServiceInfo Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 7ac41edd4ae8548ecdb6d3ef6631fba5d6175762
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105749730"
---
# <a name="serviceinfo-element"></a><span data-ttu-id="5ac4f-106">Elemento serviceInfo</span><span class="sxs-lookup"><span data-stu-id="5ac4f-106">ServiceInfo Element</span></span>

> [!Note]  
> <span data-ttu-id="5ac4f-107">Esta seção descreve a funcionalidade projetada para uso por lojas online.</span><span class="sxs-lookup"><span data-stu-id="5ac4f-107">This section describes functionality designed for use by online stores.</span></span> <span data-ttu-id="5ac4f-108">Não há suporte para o uso dessa funcionalidade fora do contexto de uma loja online.</span><span class="sxs-lookup"><span data-stu-id="5ac4f-108">Use of this functionality outside the context of an online store is not supported.</span></span>

 

<span data-ttu-id="5ac4f-109">O elemento **serviceInfo** é o elemento principal para o ServiceInfo.xml documento.</span><span class="sxs-lookup"><span data-stu-id="5ac4f-109">The **ServiceInfo** element is the main element for the ServiceInfo.xml document.</span></span>

``` syntax
<ServiceInfo
    Version = 1.00
    Key = "service key"
    ContentPartner = "true|false"
/>
```

## <a name="attributes"></a><span data-ttu-id="5ac4f-110">Atributos</span><span class="sxs-lookup"><span data-stu-id="5ac4f-110">Attributes</span></span>



| <span data-ttu-id="5ac4f-111">Termo</span><span class="sxs-lookup"><span data-stu-id="5ac4f-111">Term</span></span>                                                                                                                                             | <span data-ttu-id="5ac4f-112">Descrição</span><span class="sxs-lookup"><span data-stu-id="5ac4f-112">Description</span></span>                                                                                                                                                                                                                                                    |
|--------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5ac4f-113"><span id="Version__optional_"></span><span id="version__optional_"></span><span id="VERSION__OPTIONAL_"></span>**Versão** (opcional)</span><span class="sxs-lookup"><span data-stu-id="5ac4f-113"><span id="Version__optional_"></span><span id="version__optional_"></span><span id="VERSION__OPTIONAL_"></span>**Version** (optional)</span></span><br/> | <span data-ttu-id="5ac4f-114">Versão do arquivo de ServiceInfo.xml.</span><span class="sxs-lookup"><span data-stu-id="5ac4f-114">Version of the ServiceInfo.xml file.</span></span> <span data-ttu-id="5ac4f-115">A versão 1, 0 tem suporte para o Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="5ac4f-115">Version 1.00 is supported for Windows Media Player.</span></span><br/>                                                                                                                                                            |
| <span data-ttu-id="5ac4f-116"><span id="Key__required_"></span><span id="key__required_"></span><span id="KEY__REQUIRED_"></span>**Chave** (obrigatório)</span><span class="sxs-lookup"><span data-stu-id="5ac4f-116"><span id="Key__required_"></span><span id="key__required_"></span><span id="KEY__REQUIRED_"></span>**Key** (required)</span></span><br/>                 | <span data-ttu-id="5ac4f-117">A cadeia de caracteres da chave de serviço que identifica exclusivamente a loja online.</span><span class="sxs-lookup"><span data-stu-id="5ac4f-117">The service key string that uniquely identifies the online store.</span></span><br/>                                                                                                                                                                                   |
| <span data-ttu-id="5ac4f-118"><span id="ContentPartner"></span><span id="contentpartner"></span><span id="CONTENTPARTNER"></span>**ContentPartner**</span><span class="sxs-lookup"><span data-stu-id="5ac4f-118"><span id="ContentPartner"></span><span id="contentpartner"></span><span id="CONTENTPARTNER"></span>**ContentPartner**</span></span><br/>                 | <span data-ttu-id="5ac4f-119">Indica se o repositório online é um repositório do tipo 1.</span><span class="sxs-lookup"><span data-stu-id="5ac4f-119">Indicates whether the online store is a type 1 store.</span></span> <span data-ttu-id="5ac4f-120">Um valor de "true" indica que o repositório é do tipo 1.</span><span class="sxs-lookup"><span data-stu-id="5ac4f-120">A value of "true" indicates that the store is a type 1 store.</span></span> <span data-ttu-id="5ac4f-121">Um valor de "false" indica que o repositório não é um repositório tipo 1; ou seja, é um repositório tipo 2.</span><span class="sxs-lookup"><span data-stu-id="5ac4f-121">A value of "false" indicates that the store is not a type 1 store; that is, it is a type 2 store.</span></span> <span data-ttu-id="5ac4f-122">O valor padrão é "falso".</span><span class="sxs-lookup"><span data-stu-id="5ac4f-122">The default value is "false".</span></span><br/> |



 

## <a name="parentchild-elements"></a><span data-ttu-id="5ac4f-123">Elementos pai/filho</span><span class="sxs-lookup"><span data-stu-id="5ac4f-123">Parent/Child Elements</span></span>



| <span data-ttu-id="5ac4f-124">Hierarquia</span><span class="sxs-lookup"><span data-stu-id="5ac4f-124">Hierarchy</span></span>       | <span data-ttu-id="5ac4f-125">Elemento</span><span class="sxs-lookup"><span data-stu-id="5ac4f-125">Element</span></span>                                                                                                                                                                            |
|-----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5ac4f-126">Elementos pai</span><span class="sxs-lookup"><span data-stu-id="5ac4f-126">Parent elements</span></span> | <span data-ttu-id="5ac4f-127">Nenhum</span><span class="sxs-lookup"><span data-stu-id="5ac4f-127">None</span></span>                                                                                                                                                                               |
| <span data-ttu-id="5ac4f-128">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="5ac4f-128">Child elements</span></span>  | <span data-ttu-id="5ac4f-129">**AlbumInfo**, **BuyCD**, **cor**, **Descrição**, **FriendlyName**, **HtmlView**, **imagem**, **InfoCenter**, **instalação**, **ServiceTask1**, **ServiceTask2**, **ServiceTask3**</span><span class="sxs-lookup"><span data-stu-id="5ac4f-129">**AlbumInfo**, **BuyCD**, **Color**, **Description**, **FriendlyName**, **HTMLView**, **Image**, **InfoCenter**, **Install**, **ServiceTask1**, **ServiceTask2**, **ServiceTask3**</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="5ac4f-130">Comentários</span><span class="sxs-lookup"><span data-stu-id="5ac4f-130">Remarks</span></span>

<span data-ttu-id="5ac4f-131">A tabela a seguir detalha os parâmetros enviados com a solicitação de URL.</span><span class="sxs-lookup"><span data-stu-id="5ac4f-131">The following table details the parameters sent with the URL request.</span></span> <span data-ttu-id="5ac4f-132">Outros podem estar presentes para fins de compatibilidade herdada.</span><span class="sxs-lookup"><span data-stu-id="5ac4f-132">Others may be present for legacy compatibility purposes.</span></span> <span data-ttu-id="5ac4f-133">A solicitação também incluirá todos os parâmetros que você especificou usando o parâmetro de linha de comando netextra da instalação do Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="5ac4f-133">The request will also include any parameters you specified using the ServiceExtra command-line parameter of Windows Media Player setup.</span></span>



| <span data-ttu-id="5ac4f-134">Nome</span><span class="sxs-lookup"><span data-stu-id="5ac4f-134">Name</span></span>         | <span data-ttu-id="5ac4f-135">Valor</span><span class="sxs-lookup"><span data-stu-id="5ac4f-135">Value</span></span>                                                                                                                                                               |
|--------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5ac4f-136">*GeoId*</span><span class="sxs-lookup"><span data-stu-id="5ac4f-136">*geoid*</span></span>      | <span data-ttu-id="5ac4f-137">ID da localização geográfica do Windows.</span><span class="sxs-lookup"><span data-stu-id="5ac4f-137">Windows geographical location ID.</span></span> <span data-ttu-id="5ac4f-138">A ID de local é especificada pelo usuário na área **local** das configurações de opções regionais e de idiomas no painel de controle.</span><span class="sxs-lookup"><span data-stu-id="5ac4f-138">The location ID is specified by the user in the **Location** area of the Regional and Language Options settings in Control Panel.</span></span> |
| <span data-ttu-id="5ac4f-139">*locale*</span><span class="sxs-lookup"><span data-stu-id="5ac4f-139">*locale*</span></span>     | <span data-ttu-id="5ac4f-140">ID de localidade do Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="5ac4f-140">Windows Media Player locale ID.</span></span>                                                                                                                                     |
| <span data-ttu-id="5ac4f-141">*UserLocale*</span><span class="sxs-lookup"><span data-stu-id="5ac4f-141">*userlocale*</span></span> | <span data-ttu-id="5ac4f-142">IDENTIFICAÇÃO de localidade do Windows.</span><span class="sxs-lookup"><span data-stu-id="5ac4f-142">Windows locale ID.</span></span> <span data-ttu-id="5ac4f-143">A localidade é especificada pelo usuário na área **padrões e formatos** das configurações de opções regionais e de idiomas no painel de controle.</span><span class="sxs-lookup"><span data-stu-id="5ac4f-143">The locale is specified by the user in the **Standards and Formats** area of the Regional and Language Options settings in Control Panel.</span></span>        |
| <span data-ttu-id="5ac4f-144">*version*</span><span class="sxs-lookup"><span data-stu-id="5ac4f-144">*version*</span></span>    | <span data-ttu-id="5ac4f-145">Número de versão do Windows Media Player usando o seguinte formato: 10.0. x. xxxx ou 11.0. x. xxxx.</span><span class="sxs-lookup"><span data-stu-id="5ac4f-145">Windows Media Player version number using the following format: 10.0.x.xxxx or 11.0.x.xxxx.</span></span>                                                                         |



 

## <a name="requirements"></a><span data-ttu-id="5ac4f-146">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5ac4f-146">Requirements</span></span>



| <span data-ttu-id="5ac4f-147">Requisito</span><span class="sxs-lookup"><span data-stu-id="5ac4f-147">Requirement</span></span> | <span data-ttu-id="5ac4f-148">Valor</span><span class="sxs-lookup"><span data-stu-id="5ac4f-148">Value</span></span> |
|--------------------|----------------------------------------------|
| <span data-ttu-id="5ac4f-149">Versão</span><span class="sxs-lookup"><span data-stu-id="5ac4f-149">Version</span></span><br/> | <span data-ttu-id="5ac4f-150">Windows Media Player 10 ou posterior.</span><span class="sxs-lookup"><span data-stu-id="5ac4f-150">Windows Media Player 10 or later.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="5ac4f-151">Confira também</span><span class="sxs-lookup"><span data-stu-id="5ac4f-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5ac4f-152">**Documento de informações de exemplo para uma loja online tipo 1**</span><span class="sxs-lookup"><span data-stu-id="5ac4f-152">**Example ServiceInfo Document for a Type 1 Online Store**</span></span>](example-serviceinfo-document-for-a-type-1-online-store.md)
</dt> <dt>

[<span data-ttu-id="5ac4f-153">**Documento de informações de exemplo para uma loja online tipo 2**</span><span class="sxs-lookup"><span data-stu-id="5ac4f-153">**Example ServiceInfo Document for a Type 2 Online Store**</span></span>](example-serviceinfo-document-for-a-type-2-online-store.md)
</dt> <dt>

[<span data-ttu-id="5ac4f-154">**Documento do serviceInfo**</span><span class="sxs-lookup"><span data-stu-id="5ac4f-154">**ServiceInfo Document**</span></span>](serviceinfo-document.md)
</dt> </dl>

 

 





