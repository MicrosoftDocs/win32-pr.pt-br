---
description: Saiba mais sobre o elemento PageSourceColorProfile. Esse elemento define as características do perfil de cor de origem.
ms.assetid: aa4f5425-6ca1-4820-b15d-bbead1f6d735
title: PageSourceColorProfile
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f709d44f8af7ea6c2709201e57bc047fe9b2d21b
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/30/2021
ms.locfileid: "113118991"
---
# <a name="pagesourcecolorprofile"></a><span data-ttu-id="d2518-104">PageSourceColorProfile</span><span class="sxs-lookup"><span data-stu-id="d2518-104">PageSourceColorProfile</span></span>

<span data-ttu-id="d2518-105">Este tópico não é atual.</span><span class="sxs-lookup"><span data-stu-id="d2518-105">This topic is not current.</span></span> <span data-ttu-id="d2518-106">Para obter as informações mais atuais, consulte a [Especificação de Esquema de Impressão](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="d2518-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="d2518-107">Define as características do perfil de cor de origem.</span><span class="sxs-lookup"><span data-stu-id="d2518-107">Defines the characteristics of the source color profile.</span></span>

-   [<span data-ttu-id="d2518-108">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="d2518-108">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="d2518-109">Conteúdo estrutural</span><span class="sxs-lookup"><span data-stu-id="d2518-109">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="d2518-110">linguagem XML conteúdo (XML)</span><span class="sxs-lookup"><span data-stu-id="d2518-110">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="d2518-111">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="d2518-111">Element Information</span></span>



| <span data-ttu-id="d2518-112">Nome</span><span class="sxs-lookup"><span data-stu-id="d2518-112">Name</span></span>                       | <span data-ttu-id="d2518-113">Valor</span><span class="sxs-lookup"><span data-stu-id="d2518-113">Value</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
|----------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d2518-114">Tipo de elemento</span><span class="sxs-lookup"><span data-stu-id="d2518-114">Element Type</span></span> <br/>   | <span data-ttu-id="d2518-115">Recurso</span><span class="sxs-lookup"><span data-stu-id="d2518-115">Feature</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| <span data-ttu-id="d2518-116">Prefixo de definição de scoping</span><span class="sxs-lookup"><span data-stu-id="d2518-116">Scoping Prefix</span></span> <br/> | <span data-ttu-id="d2518-117">?</span><span class="sxs-lookup"><span data-stu-id="d2518-117">Page</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| <span data-ttu-id="d2518-118">Observações</span><span class="sxs-lookup"><span data-stu-id="d2518-118">Notes</span></span> <br/>          | <span data-ttu-id="d2518-119">Os consumidores compatíveis com XPS DEVEM impor que uma referência de URI a um recurso, como uma imagem ou perfil de cor em um documento Recursos de Impressão ou PrintTicket, DEVE se referir a um nome de parte (um URI relativo para a raiz do pacote) dentro do mesmo pacote do Documento XPS que contém o PrintTicket resultante.</span><span class="sxs-lookup"><span data-stu-id="d2518-119">XPS-compliant consumers MUST enforce that a URI reference to a resource such as an image or color profile in either a Print Capabilities document or PrintTicket MUST refer to a part name (a relative URI to the package root) within the same XPS Document package that contains the resultant PrintTicket.</span></span> <span data-ttu-id="d2518-120">Um consumidor XPS compatível NÃO DEVE usar um URI que não está em conformidade com a sintaxe de nome da parte.</span><span class="sxs-lookup"><span data-stu-id="d2518-120">A compliant XPS consumer MUST NOT use a URI that is not compliant with the part name syntax.</span></span> <span data-ttu-id="d2518-121">Essas configurações são específicas do XPS.</span><span class="sxs-lookup"><span data-stu-id="d2518-121">These settings are XPS specific.</span></span> <br/> <span data-ttu-id="d2518-122">URIs que são referenciados em um documento Funcionalidades de Impressão ou PrintTicket NÃO DEVEM ser resolvidos como URLs.</span><span class="sxs-lookup"><span data-stu-id="d2518-122">URIs which are referenced in either a Print Capabilities document or PrintTicket MUST NOT be resolved as URLs.</span></span> <span data-ttu-id="d2518-123">Isso não é seguro, pois eles podem não ser resolvidos conforme o esperado e podem criar riscos de segurança prejudiciais para o driver e o sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="d2518-123">This is unsafe as they may not resolve as intended and may create harmful security risks for the driver and operating system.</span></span><br/> |



 

## <a name="structural-content"></a><span data-ttu-id="d2518-124">Conteúdo estrutural</span><span class="sxs-lookup"><span data-stu-id="d2518-124">Structural Content</span></span>

<span data-ttu-id="d2518-125">A estrutura XML desse elemento é:</span><span class="sxs-lookup"><span data-stu-id="d2518-125">The XML structure of this element is:</span></span>

``` syntax
<psf:Feature name="psk:PageSourceColorProfile">
  <psf:Property name="psf:SelectionType">
    <psf:Value xsi:type="xs:string">psk:PickOne</psf:Value>
  </psf:Property>
  <psf:Option name="psk:_OptionName_">
    <psf:Property name="psf:IdentityOption">
      <psf:Value xsi:type="xs:string">_IdentityOptionValue_</psf:Value>
    </psf:Property>
  </psf:Option>
</psf:Feature>
```

## <a name="structure-variables"></a><span data-ttu-id="d2518-126">Variáveis de estrutura</span><span class="sxs-lookup"><span data-stu-id="d2518-126">Structure Variables</span></span>

<span data-ttu-id="d2518-127">A tabela a seguir descreve as características das variáveis definidas na estrutura XML.</span><span class="sxs-lookup"><span data-stu-id="d2518-127">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="d2518-128">Nome</span><span class="sxs-lookup"><span data-stu-id="d2518-128">Name</span></span>                               | <span data-ttu-id="d2518-129">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="d2518-129">Data type</span></span>         | <span data-ttu-id="d2518-130">Unidade</span><span class="sxs-lookup"><span data-stu-id="d2518-130">Unit</span></span>                  | <span data-ttu-id="d2518-131">Valores com suporte</span><span class="sxs-lookup"><span data-stu-id="d2518-131">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="d2518-132">Resumo</span><span class="sxs-lookup"><span data-stu-id="d2518-132">Summary</span></span>                                                                      |
|------------------------------------|-------------------|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="d2518-133">\_Optionname\_</span><span class="sxs-lookup"><span data-stu-id="d2518-133">\_OptionName\_</span></span><br/>          | <span data-ttu-id="d2518-134">string</span><span class="sxs-lookup"><span data-stu-id="d2518-134">string</span></span><br/> | <span data-ttu-id="d2518-135">characters</span><span class="sxs-lookup"><span data-stu-id="d2518-135">characters</span></span><br/> | <span data-ttu-id="d2518-136">Nome totalmente qualificado válido, conforme definido [por Namespaces em XML.](https://www.w3.org/TR/1999/REC-xml-names-19990114/)</span><span class="sxs-lookup"><span data-stu-id="d2518-136">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="d2518-137">Se nenhum namespace for especificado, o namespace padrão será assumido.</span><span class="sxs-lookup"><span data-stu-id="d2518-137">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="d2518-138">O nome da opção.</span><span class="sxs-lookup"><span data-stu-id="d2518-138">The name of the option.</span></span><br/>                                           |
| <span data-ttu-id="d2518-139">\_IdentityOptionValue\_</span><span class="sxs-lookup"><span data-stu-id="d2518-139">\_IdentityOptionValue\_</span></span><br/> | <span data-ttu-id="d2518-140">string</span><span class="sxs-lookup"><span data-stu-id="d2518-140">string</span></span><br/> | <span data-ttu-id="d2518-141">n/d</span><span class="sxs-lookup"><span data-stu-id="d2518-141">n/a</span></span><br/>        | <span data-ttu-id="d2518-142">True, False.</span><span class="sxs-lookup"><span data-stu-id="d2518-142">True, False.</span></span><br/>                                                                                                                                                               | <span data-ttu-id="d2518-143">Define uma Opção que, quando selecionada, desabilitará esse recurso.</span><span class="sxs-lookup"><span data-stu-id="d2518-143">Defines an Option which when selected would disable this feature.</span></span><br/> |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="d2518-144">linguagem XML conteúdo (XML)</span><span class="sxs-lookup"><span data-stu-id="d2518-144">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="d2518-145">As palavras-chave public Print Schema são definidas no https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace .</span><span class="sxs-lookup"><span data-stu-id="d2518-145">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="d2518-146">O conteúdo linguagem XML XML (public linguagem XML) para essa palavra-chave é definido abaixo:</span><span class="sxs-lookup"><span data-stu-id="d2518-146">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

``` syntax
<psf:Feature name="psk:PageSourceColorProfile">
  <psf:Option name="psk:RGB">
    <!-- Source profile used to perform color management for untagged RGB data. -->
    <psf:ScoredProperty name="psk:SourceColorProfileURI">
      <psf:ParameterRef name="psk:PageSourceColorProfileURI" />
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:SourceColorProfileEmbedded">
      <psf:ParameterRef name="psk:PageSourceColorProfileEmbedded" />
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:CMYK">
    <!-- Source profile used to perform color management for untagged CMYK data. -->
    <psf:ScoredProperty name="psk:SourceColorProfileURI">
      <psf:ParameterRef name="psk:PageSourceColorProfileURI" />
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:SourceColorProfileEmbedded">
      <psf:ParameterRef name="psk:PageSourceColorProfileEmbedded" />
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:None" />
</psf:Feature>
```

## <a name="related-topics"></a><span data-ttu-id="d2518-147">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="d2518-147">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d2518-148">Especificação de esquema de impressão</span><span class="sxs-lookup"><span data-stu-id="d2518-148">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




