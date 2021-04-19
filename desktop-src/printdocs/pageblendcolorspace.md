---
description: Este tópico não é atual. Para obter as informações mais atuais, consulte a especificação do esquema de impressão.
ms.assetid: 86e3f44d-192e-412a-abb1-118e8592d90b
title: PageBlendColorSpace
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: adf68660929839fad79be26daebf32b9bc0f7ea5
ms.sourcegitcommit: 7b8f6151ebe247536304866459b2973276271d4d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/06/2021
ms.locfileid: "105782439"
---
# <a name="pageblendcolorspace"></a><span data-ttu-id="5d553-104">PageBlendColorSpace</span><span class="sxs-lookup"><span data-stu-id="5d553-104">PageBlendColorSpace</span></span>

<span data-ttu-id="5d553-105">Este tópico não é atual.</span><span class="sxs-lookup"><span data-stu-id="5d553-105">This topic is not current.</span></span> <span data-ttu-id="5d553-106">Para obter as informações mais atuais, consulte a [especificação do esquema de impressão](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="5d553-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="5d553-107">Descreve o espaço de cores que deve ser usado para operações de mesclagem.</span><span class="sxs-lookup"><span data-stu-id="5d553-107">Describes the color space that should be used for blending operations.</span></span>

-   [<span data-ttu-id="5d553-108">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="5d553-108">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="5d553-109">Conteúdo estrutural</span><span class="sxs-lookup"><span data-stu-id="5d553-109">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="5d553-110">Conteúdo de linguagem XML (XML)</span><span class="sxs-lookup"><span data-stu-id="5d553-110">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="5d553-111">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="5d553-111">Element Information</span></span>



| <span data-ttu-id="5d553-112">Nome</span><span class="sxs-lookup"><span data-stu-id="5d553-112">Name</span></span>                       |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
|----------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5d553-113">Tipo de elemento</span><span class="sxs-lookup"><span data-stu-id="5d553-113">Element Type</span></span> <br/>   | <span data-ttu-id="5d553-114">Recurso</span><span class="sxs-lookup"><span data-stu-id="5d553-114">Feature</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| <span data-ttu-id="5d553-115">Prefixo de escopo</span><span class="sxs-lookup"><span data-stu-id="5d553-115">Scoping Prefix</span></span> <br/> | <span data-ttu-id="5d553-116">Trabalho</span><span class="sxs-lookup"><span data-stu-id="5d553-116">Job</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| <span data-ttu-id="5d553-117">Observações</span><span class="sxs-lookup"><span data-stu-id="5d553-117">Notes</span></span> <br/>          | <span data-ttu-id="5d553-118">Os consumidores em conformidade com XPS devem impor que uma referência de URI a um recurso como uma imagem ou um perfil de cor em um documento de recursos de impressão ou PrintTicket deve se referir a um nome de parte (um URI relativo para a raiz do pacote) dentro do mesmo pacote de documento XPS que contém o PrintTicket resultante.</span><span class="sxs-lookup"><span data-stu-id="5d553-118">XPS-compliant consumers MUST enforce that a URI reference to a resource such as an image or color profile in either a Print Capabilities document or PrintTicket MUST refer to a part name (a relative URI to the package root) within the same XPS Document package that contains the resultant PrintTicket.</span></span> <span data-ttu-id="5d553-119">Um consumidor XPS compatível não deve usar um URI que não seja compatível com a sintaxe do nome da parte.</span><span class="sxs-lookup"><span data-stu-id="5d553-119">A compliant XPS consumer MUST NOT use a URI that is not compliant with the part name syntax.</span></span> <span data-ttu-id="5d553-120">Essas configurações são específicas do XPS.</span><span class="sxs-lookup"><span data-stu-id="5d553-120">These settings are XPS specific.</span></span> <br/> <span data-ttu-id="5d553-121">Os URIs que são referenciados em um documento de recursos de impressão ou PrintTicket não devem ser resolvidos como URLs.</span><span class="sxs-lookup"><span data-stu-id="5d553-121">URIs which are referenced in either a Print Capabilities document or PrintTicket MUST NOT be resolved as URLs.</span></span> <span data-ttu-id="5d553-122">Isso não é seguro, pois eles podem não ser resolvidos como pretendidos e podem criar riscos de segurança prejudiciais para o driver e o sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="5d553-122">This is unsafe as they may not resolve as intended and may create harmful security risks for the driver and operating system.</span></span><br/> |



 

## <a name="structural-content"></a><span data-ttu-id="5d553-123">Conteúdo estrutural</span><span class="sxs-lookup"><span data-stu-id="5d553-123">Structural Content</span></span>

<span data-ttu-id="5d553-124">A estrutura XML desse elemento é:</span><span class="sxs-lookup"><span data-stu-id="5d553-124">The XML structure of this element is:</span></span>

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

## <a name="structure-variables"></a><span data-ttu-id="5d553-125">Variáveis de estrutura</span><span class="sxs-lookup"><span data-stu-id="5d553-125">Structure Variables</span></span>

<span data-ttu-id="5d553-126">A tabela a seguir descreve as características das variáveis definidas na estrutura XML.</span><span class="sxs-lookup"><span data-stu-id="5d553-126">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="5d553-127">Nome</span><span class="sxs-lookup"><span data-stu-id="5d553-127">Name</span></span>                               | <span data-ttu-id="5d553-128">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="5d553-128">Data type</span></span>         | <span data-ttu-id="5d553-129">Unidade</span><span class="sxs-lookup"><span data-stu-id="5d553-129">Unit</span></span>                  | <span data-ttu-id="5d553-130">Valores com suporte</span><span class="sxs-lookup"><span data-stu-id="5d553-130">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="5d553-131">Resumo</span><span class="sxs-lookup"><span data-stu-id="5d553-131">Summary</span></span>                                                                      |
|------------------------------------|-------------------|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="5d553-132">\_OptionName\_</span><span class="sxs-lookup"><span data-stu-id="5d553-132">\_OptionName\_</span></span><br/>          | <span data-ttu-id="5d553-133">string</span><span class="sxs-lookup"><span data-stu-id="5d553-133">string</span></span><br/> | <span data-ttu-id="5d553-134">characters</span><span class="sxs-lookup"><span data-stu-id="5d553-134">characters</span></span><br/> | <span data-ttu-id="5d553-135">Nome totalmente qualificado válido, conforme definido pelos [namespaces em XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span><span class="sxs-lookup"><span data-stu-id="5d553-135">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="5d553-136">Se nenhum namespace for especificado, o namespace padrão será assumido.</span><span class="sxs-lookup"><span data-stu-id="5d553-136">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="5d553-137">O nome da opção.</span><span class="sxs-lookup"><span data-stu-id="5d553-137">The name of the option.</span></span><br/>                                           |
| <span data-ttu-id="5d553-138">\_IdentityOptionValue\_</span><span class="sxs-lookup"><span data-stu-id="5d553-138">\_IdentityOptionValue\_</span></span><br/> | <span data-ttu-id="5d553-139">string</span><span class="sxs-lookup"><span data-stu-id="5d553-139">string</span></span><br/> | <span data-ttu-id="5d553-140">N/D</span><span class="sxs-lookup"><span data-stu-id="5d553-140">n/a</span></span><br/>        | <span data-ttu-id="5d553-141">True, False.</span><span class="sxs-lookup"><span data-stu-id="5d553-141">True, False.</span></span><br/>                                                                                                                                                               | <span data-ttu-id="5d553-142">Define uma opção que, quando selecionada, desabilita esse recurso.</span><span class="sxs-lookup"><span data-stu-id="5d553-142">Defines an Option which when selected would disable this feature.</span></span><br/> |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="5d553-143">Conteúdo de linguagem XML (XML)</span><span class="sxs-lookup"><span data-stu-id="5d553-143">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="5d553-144">As palavras-chave do esquema de impressão pública são definidas no https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span><span class="sxs-lookup"><span data-stu-id="5d553-144">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="5d553-145">O conteúdo do linguagem XML público (XML) para essa palavra-chave é definido abaixo:</span><span class="sxs-lookup"><span data-stu-id="5d553-145">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

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

## <a name="related-topics"></a><span data-ttu-id="5d553-146">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="5d553-146">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5d553-147">Especificação de esquema de impressão</span><span class="sxs-lookup"><span data-stu-id="5d553-147">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




