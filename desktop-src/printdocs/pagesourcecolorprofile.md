---
description: Este tópico não é atual. Para obter as informações mais atuais, consulte a especificação do esquema de impressão.
ms.assetid: aa4f5425-6ca1-4820-b15d-bbead1f6d735
title: PageSourceColorProfile
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 32de15ec5110788ad85d8ceb2f251eb3b30000d8
ms.sourcegitcommit: 7b8f6151ebe247536304866459b2973276271d4d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/06/2021
ms.locfileid: "105784966"
---
# <a name="pagesourcecolorprofile"></a><span data-ttu-id="31555-104">PageSourceColorProfile</span><span class="sxs-lookup"><span data-stu-id="31555-104">PageSourceColorProfile</span></span>

<span data-ttu-id="31555-105">Este tópico não é atual.</span><span class="sxs-lookup"><span data-stu-id="31555-105">This topic is not current.</span></span> <span data-ttu-id="31555-106">Para obter as informações mais atuais, consulte a [especificação do esquema de impressão](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="31555-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="31555-107">Define as características do perfil de cor de origem.</span><span class="sxs-lookup"><span data-stu-id="31555-107">Defines the characteristics of the source color profile.</span></span>

-   [<span data-ttu-id="31555-108">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="31555-108">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="31555-109">Conteúdo estrutural</span><span class="sxs-lookup"><span data-stu-id="31555-109">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="31555-110">Conteúdo de linguagem XML (XML)</span><span class="sxs-lookup"><span data-stu-id="31555-110">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="31555-111">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="31555-111">Element Information</span></span>



| <span data-ttu-id="31555-112">Nome</span><span class="sxs-lookup"><span data-stu-id="31555-112">Name</span></span>                       |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
|----------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="31555-113">Tipo de elemento</span><span class="sxs-lookup"><span data-stu-id="31555-113">Element Type</span></span> <br/>   | <span data-ttu-id="31555-114">Recurso</span><span class="sxs-lookup"><span data-stu-id="31555-114">Feature</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| <span data-ttu-id="31555-115">Prefixo de escopo</span><span class="sxs-lookup"><span data-stu-id="31555-115">Scoping Prefix</span></span> <br/> | <span data-ttu-id="31555-116">?</span><span class="sxs-lookup"><span data-stu-id="31555-116">Page</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| <span data-ttu-id="31555-117">Observações</span><span class="sxs-lookup"><span data-stu-id="31555-117">Notes</span></span> <br/>          | <span data-ttu-id="31555-118">Os consumidores em conformidade com XPS devem impor que uma referência de URI a um recurso como uma imagem ou um perfil de cor em um documento de recursos de impressão ou PrintTicket deve se referir a um nome de parte (um URI relativo para a raiz do pacote) dentro do mesmo pacote de documento XPS que contém o PrintTicket resultante.</span><span class="sxs-lookup"><span data-stu-id="31555-118">XPS-compliant consumers MUST enforce that a URI reference to a resource such as an image or color profile in either a Print Capabilities document or PrintTicket MUST refer to a part name (a relative URI to the package root) within the same XPS Document package that contains the resultant PrintTicket.</span></span> <span data-ttu-id="31555-119">Um consumidor XPS compatível não deve usar um URI que não seja compatível com a sintaxe do nome da parte.</span><span class="sxs-lookup"><span data-stu-id="31555-119">A compliant XPS consumer MUST NOT use a URI that is not compliant with the part name syntax.</span></span> <span data-ttu-id="31555-120">Essas configurações são específicas do XPS.</span><span class="sxs-lookup"><span data-stu-id="31555-120">These settings are XPS specific.</span></span> <br/> <span data-ttu-id="31555-121">Os URIs que são referenciados em um documento de recursos de impressão ou PrintTicket não devem ser resolvidos como URLs.</span><span class="sxs-lookup"><span data-stu-id="31555-121">URIs which are referenced in either a Print Capabilities document or PrintTicket MUST NOT be resolved as URLs.</span></span> <span data-ttu-id="31555-122">Isso não é seguro, pois eles podem não ser resolvidos como pretendidos e podem criar riscos de segurança prejudiciais para o driver e o sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="31555-122">This is unsafe as they may not resolve as intended and may create harmful security risks for the driver and operating system.</span></span><br/> |



 

## <a name="structural-content"></a><span data-ttu-id="31555-123">Conteúdo estrutural</span><span class="sxs-lookup"><span data-stu-id="31555-123">Structural Content</span></span>

<span data-ttu-id="31555-124">A estrutura XML desse elemento é:</span><span class="sxs-lookup"><span data-stu-id="31555-124">The XML structure of this element is:</span></span>

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

## <a name="structure-variables"></a><span data-ttu-id="31555-125">Variáveis de estrutura</span><span class="sxs-lookup"><span data-stu-id="31555-125">Structure Variables</span></span>

<span data-ttu-id="31555-126">A tabela a seguir descreve as características das variáveis definidas na estrutura XML.</span><span class="sxs-lookup"><span data-stu-id="31555-126">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="31555-127">Nome</span><span class="sxs-lookup"><span data-stu-id="31555-127">Name</span></span>                               | <span data-ttu-id="31555-128">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="31555-128">Data type</span></span>         | <span data-ttu-id="31555-129">Unidade</span><span class="sxs-lookup"><span data-stu-id="31555-129">Unit</span></span>                  | <span data-ttu-id="31555-130">Valores com suporte</span><span class="sxs-lookup"><span data-stu-id="31555-130">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="31555-131">Resumo</span><span class="sxs-lookup"><span data-stu-id="31555-131">Summary</span></span>                                                                      |
|------------------------------------|-------------------|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="31555-132">\_OptionName\_</span><span class="sxs-lookup"><span data-stu-id="31555-132">\_OptionName\_</span></span><br/>          | <span data-ttu-id="31555-133">string</span><span class="sxs-lookup"><span data-stu-id="31555-133">string</span></span><br/> | <span data-ttu-id="31555-134">characters</span><span class="sxs-lookup"><span data-stu-id="31555-134">characters</span></span><br/> | <span data-ttu-id="31555-135">Nome totalmente qualificado válido, conforme definido pelos [namespaces em XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span><span class="sxs-lookup"><span data-stu-id="31555-135">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="31555-136">Se nenhum namespace for especificado, o namespace padrão será assumido.</span><span class="sxs-lookup"><span data-stu-id="31555-136">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="31555-137">O nome da opção.</span><span class="sxs-lookup"><span data-stu-id="31555-137">The name of the option.</span></span><br/>                                           |
| <span data-ttu-id="31555-138">\_IdentityOptionValue\_</span><span class="sxs-lookup"><span data-stu-id="31555-138">\_IdentityOptionValue\_</span></span><br/> | <span data-ttu-id="31555-139">string</span><span class="sxs-lookup"><span data-stu-id="31555-139">string</span></span><br/> | <span data-ttu-id="31555-140">N/D</span><span class="sxs-lookup"><span data-stu-id="31555-140">n/a</span></span><br/>        | <span data-ttu-id="31555-141">True, False.</span><span class="sxs-lookup"><span data-stu-id="31555-141">True, False.</span></span><br/>                                                                                                                                                               | <span data-ttu-id="31555-142">Define uma opção que, quando selecionada, desabilita esse recurso.</span><span class="sxs-lookup"><span data-stu-id="31555-142">Defines an Option which when selected would disable this feature.</span></span><br/> |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="31555-143">Conteúdo de linguagem XML (XML)</span><span class="sxs-lookup"><span data-stu-id="31555-143">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="31555-144">As palavras-chave do esquema de impressão pública são definidas no https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span><span class="sxs-lookup"><span data-stu-id="31555-144">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="31555-145">O conteúdo do linguagem XML público (XML) para essa palavra-chave é definido abaixo:</span><span class="sxs-lookup"><span data-stu-id="31555-145">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

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

## <a name="related-topics"></a><span data-ttu-id="31555-146">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="31555-146">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="31555-147">Especificação de esquema de impressão</span><span class="sxs-lookup"><span data-stu-id="31555-147">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




