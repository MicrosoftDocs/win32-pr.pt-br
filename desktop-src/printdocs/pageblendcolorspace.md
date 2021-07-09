---
description: Saiba mais sobre o elemento configurável pelo usuário PageBlendColorSpace. Este tópico não é atual. Para obter as informações mais atuais, consulte a Especificação de Esquema de Impressão.
ms.assetid: 86e3f44d-192e-412a-abb1-118e8592d90b
title: PageBlendColorSpace
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b36ce3a1def74058014fc396d9ef53aed6a32302
ms.sourcegitcommit: 998d50f6def8a25850fc113fc8a2df903c829c5e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/09/2021
ms.locfileid: "113549334"
---
# <a name="pageblendcolorspace"></a><span data-ttu-id="4077f-105">PageBlendColorSpace</span><span class="sxs-lookup"><span data-stu-id="4077f-105">PageBlendColorSpace</span></span>

<span data-ttu-id="4077f-106">Este tópico não é atual.</span><span class="sxs-lookup"><span data-stu-id="4077f-106">This topic is not current.</span></span> <span data-ttu-id="4077f-107">Para obter as informações mais atuais, consulte a [Especificação de Esquema de Impressão](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="4077f-107">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="4077f-108">Descreve o espaço de cores que deve ser usado para operações de mesclagem.</span><span class="sxs-lookup"><span data-stu-id="4077f-108">Describes the color space that should be used for blending operations.</span></span>

-   [<span data-ttu-id="4077f-109">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="4077f-109">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="4077f-110">Conteúdo estrutural</span><span class="sxs-lookup"><span data-stu-id="4077f-110">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="4077f-111">linguagem XML conteúdo (XML)</span><span class="sxs-lookup"><span data-stu-id="4077f-111">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="4077f-112">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="4077f-112">Element Information</span></span>



| <span data-ttu-id="4077f-113">Nome</span><span class="sxs-lookup"><span data-stu-id="4077f-113">Name</span></span> | <span data-ttu-id="4077f-114">Valor</span><span class="sxs-lookup"><span data-stu-id="4077f-114">Value</span></span> |
|----------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4077f-115">Tipo de elemento</span><span class="sxs-lookup"><span data-stu-id="4077f-115">Element Type</span></span> <br/>   | <span data-ttu-id="4077f-116">Recurso</span><span class="sxs-lookup"><span data-stu-id="4077f-116">Feature</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| <span data-ttu-id="4077f-117">Prefixo de definição de scoping</span><span class="sxs-lookup"><span data-stu-id="4077f-117">Scoping Prefix</span></span> <br/> | <span data-ttu-id="4077f-118">Trabalho</span><span class="sxs-lookup"><span data-stu-id="4077f-118">Job</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| <span data-ttu-id="4077f-119">Observações</span><span class="sxs-lookup"><span data-stu-id="4077f-119">Notes</span></span> <br/>          | <span data-ttu-id="4077f-120">Os consumidores compatíveis com XPS DEVEM impor que uma referência de URI a um recurso, como uma imagem ou perfil de cor em um documento Recursos de Impressão ou PrintTicket, DEVE se referir a um nome de parte (um URI relativo para a raiz do pacote) dentro do mesmo pacote do Documento XPS que contém o PrintTicket resultante.</span><span class="sxs-lookup"><span data-stu-id="4077f-120">XPS-compliant consumers MUST enforce that a URI reference to a resource such as an image or color profile in either a Print Capabilities document or PrintTicket MUST refer to a part name (a relative URI to the package root) within the same XPS Document package that contains the resultant PrintTicket.</span></span> <span data-ttu-id="4077f-121">Um consumidor XPS compatível NÃO DEVE usar um URI que não está em conformidade com a sintaxe de nome da parte.</span><span class="sxs-lookup"><span data-stu-id="4077f-121">A compliant XPS consumer MUST NOT use a URI that is not compliant with the part name syntax.</span></span> <span data-ttu-id="4077f-122">Essas configurações são específicas do XPS.</span><span class="sxs-lookup"><span data-stu-id="4077f-122">These settings are XPS specific.</span></span> <br/> <span data-ttu-id="4077f-123">URIs que são referenciados em um documento Funcionalidades de Impressão ou PrintTicket NÃO DEVEM ser resolvidos como URLs.</span><span class="sxs-lookup"><span data-stu-id="4077f-123">URIs which are referenced in either a Print Capabilities document or PrintTicket MUST NOT be resolved as URLs.</span></span> <span data-ttu-id="4077f-124">Isso não é seguro, pois eles podem não ser resolvidos conforme o esperado e podem criar riscos de segurança prejudiciais para o driver e o sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="4077f-124">This is unsafe as they may not resolve as intended and may create harmful security risks for the driver and operating system.</span></span><br/> |



 

## <a name="structural-content"></a><span data-ttu-id="4077f-125">Conteúdo estrutural</span><span class="sxs-lookup"><span data-stu-id="4077f-125">Structural Content</span></span>

<span data-ttu-id="4077f-126">A estrutura XML desse elemento é:</span><span class="sxs-lookup"><span data-stu-id="4077f-126">The XML structure of this element is:</span></span>

``` syntax
<psf:Feature name="psk:PageBlendColorSpace">
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

## <a name="structure-variables"></a><span data-ttu-id="4077f-127">Variáveis de estrutura</span><span class="sxs-lookup"><span data-stu-id="4077f-127">Structure Variables</span></span>

<span data-ttu-id="4077f-128">A tabela a seguir descreve as características das variáveis definidas na estrutura XML.</span><span class="sxs-lookup"><span data-stu-id="4077f-128">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="4077f-129">Nome</span><span class="sxs-lookup"><span data-stu-id="4077f-129">Name</span></span>                               | <span data-ttu-id="4077f-130">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="4077f-130">Data type</span></span>         | <span data-ttu-id="4077f-131">Unidade</span><span class="sxs-lookup"><span data-stu-id="4077f-131">Unit</span></span>                  | <span data-ttu-id="4077f-132">Valores com suporte</span><span class="sxs-lookup"><span data-stu-id="4077f-132">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="4077f-133">Resumo</span><span class="sxs-lookup"><span data-stu-id="4077f-133">Summary</span></span>                                                                      |
|------------------------------------|-------------------|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="4077f-134">\_Optionname\_</span><span class="sxs-lookup"><span data-stu-id="4077f-134">\_OptionName\_</span></span><br/>          | <span data-ttu-id="4077f-135">string</span><span class="sxs-lookup"><span data-stu-id="4077f-135">string</span></span><br/> | <span data-ttu-id="4077f-136">characters</span><span class="sxs-lookup"><span data-stu-id="4077f-136">characters</span></span><br/> | <span data-ttu-id="4077f-137">Nome totalmente qualificado válido, conforme definido [por Namespaces em XML.](https://www.w3.org/TR/1999/REC-xml-names-19990114/)</span><span class="sxs-lookup"><span data-stu-id="4077f-137">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="4077f-138">Se nenhum namespace for especificado, o namespace padrão será assumido.</span><span class="sxs-lookup"><span data-stu-id="4077f-138">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="4077f-139">O nome da opção.</span><span class="sxs-lookup"><span data-stu-id="4077f-139">The name of the option.</span></span><br/>                                           |
| <span data-ttu-id="4077f-140">\_IdentityOptionValue\_</span><span class="sxs-lookup"><span data-stu-id="4077f-140">\_IdentityOptionValue\_</span></span><br/> | <span data-ttu-id="4077f-141">string</span><span class="sxs-lookup"><span data-stu-id="4077f-141">string</span></span><br/> | <span data-ttu-id="4077f-142">n/d</span><span class="sxs-lookup"><span data-stu-id="4077f-142">n/a</span></span><br/>        | <span data-ttu-id="4077f-143">True, False.</span><span class="sxs-lookup"><span data-stu-id="4077f-143">True, False.</span></span><br/>                                                                                                                                                               | <span data-ttu-id="4077f-144">Define uma Opção que, quando selecionada, desabilitará esse recurso.</span><span class="sxs-lookup"><span data-stu-id="4077f-144">Defines an Option which when selected would disable this feature.</span></span><br/> |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="4077f-145">linguagem XML conteúdo (XML)</span><span class="sxs-lookup"><span data-stu-id="4077f-145">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="4077f-146">As palavras-chave public Print Schema são definidas no https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace .</span><span class="sxs-lookup"><span data-stu-id="4077f-146">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="4077f-147">O conteúdo linguagem XML XML (public linguagem XML) para essa palavra-chave é definido abaixo:</span><span class="sxs-lookup"><span data-stu-id="4077f-147">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

``` syntax
<psf:Feature name="psk:PageBlendColorSpace">
  <psf:Property name="SelectionType">
    <psf:Value xsi:type="xs:string">PickOne</psf:Value>
  </psf:Property>
  <!-- sRGB color space SHOULD be used for blending. -->
  <psf:Option name="psk:sRGB" />
  <!-- scRGB color space SHOULD be used for blending. -->
  <psf:Option name="psk:scRGB" />
  <!-- Specifies an ICC profile defining the color space that SHOULD be used for blending.  Note: This applies to XPS Documents only and should not be used in arbitrary PrintTickets. -->
  <psf:Option name="psk:ICCProfile">
    <!-- XPS specific part name for the blend mode ICC Profile -->
    <psf:ScoredProperty name="psk:URI">
      <psf:ParameterRef name="psk:PageBlendColorSpaceICCProfileURI" />
    </psf:ScoredProperty>
  </psf:Option>
</psf:Feature>
```

## <a name="related-topics"></a><span data-ttu-id="4077f-148">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="4077f-148">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4077f-149">Especificação de esquema de impressão</span><span class="sxs-lookup"><span data-stu-id="4077f-149">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




