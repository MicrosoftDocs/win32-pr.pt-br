---
description: Saiba mais sobre o elemento configurável pelo usuário PageWatermark. Este tópico não é atual. Para obter as informações mais atuais, consulte a Especificação de Esquema de Impressão.
ms.assetid: d1c36c47-107c-4012-a839-1018c2652209
title: PageWatermark
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4b93eadfb3aeaa2c0be1de2cf5775bd1b5c88666
ms.sourcegitcommit: 91530c19d26ba4c57a6af1f37b57f211f580464e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/19/2021
ms.locfileid: "112396081"
---
# <a name="pagewatermark"></a><span data-ttu-id="005a6-105">PageWatermark</span><span class="sxs-lookup"><span data-stu-id="005a6-105">PageWatermark</span></span>

<span data-ttu-id="005a6-106">Este tópico não é atual.</span><span class="sxs-lookup"><span data-stu-id="005a6-106">This topic is not current.</span></span> <span data-ttu-id="005a6-107">Para obter as informações mais atuais, consulte a [Especificação de Esquema de Impressão](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="005a6-107">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="005a6-108">Descreve a configuração de marca-d'água da saída e as características da marca-d'água.</span><span class="sxs-lookup"><span data-stu-id="005a6-108">Describes the watermark setting of the output and the watermark characteristics.</span></span> <span data-ttu-id="005a6-109">As marcas-d'água se aplicam à página lógica, não à página física.</span><span class="sxs-lookup"><span data-stu-id="005a6-109">Watermarks apply to the logical page, not the physical page.</span></span> <span data-ttu-id="005a6-110">Por exemplo, se DocumentDuplex estiver habilitado, uma marca-d'água será exibida em cada página NUp em cada planilha.</span><span class="sxs-lookup"><span data-stu-id="005a6-110">For example, if DocumentDuplex is enabled, a watermark will appear on each NUp page on each sheet.</span></span> <span data-ttu-id="005a6-111">Se DocumentDuplex, PagesPerSheet=2, cada planilha terá duas marcas-d'água.</span><span class="sxs-lookup"><span data-stu-id="005a6-111">If DocumentDuplex, PagesPerSheet=2, then each sheet will have 2 watermarks.</span></span>

-   [<span data-ttu-id="005a6-112">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="005a6-112">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="005a6-113">Conteúdo estrutural</span><span class="sxs-lookup"><span data-stu-id="005a6-113">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="005a6-114">linguagem XML conteúdo (XML)</span><span class="sxs-lookup"><span data-stu-id="005a6-114">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="005a6-115">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="005a6-115">Element Information</span></span>



| <span data-ttu-id="005a6-116">Name</span><span class="sxs-lookup"><span data-stu-id="005a6-116">Name</span></span> | <span data-ttu-id="005a6-117">Valor</span><span class="sxs-lookup"><span data-stu-id="005a6-117">Value</span></span> |
|----------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="005a6-118">Tipo de elemento</span><span class="sxs-lookup"><span data-stu-id="005a6-118">Element Type</span></span> <br/>   | <span data-ttu-id="005a6-119">Recurso</span><span class="sxs-lookup"><span data-stu-id="005a6-119">Feature</span></span><br/>                                                                                                                              |
| <span data-ttu-id="005a6-120">Prefixo de definição de scoping</span><span class="sxs-lookup"><span data-stu-id="005a6-120">Scoping Prefix</span></span> <br/> | <span data-ttu-id="005a6-121">?</span><span class="sxs-lookup"><span data-stu-id="005a6-121">Page</span></span><br/>                                                                                                                                 |
| <span data-ttu-id="005a6-122">Observações</span><span class="sxs-lookup"><span data-stu-id="005a6-122">Notes</span></span> <br/>          | <span data-ttu-id="005a6-123">As coordenadas são relativas a PageImageableSize, em que a origem da marca-d'água é relativa à origem de PageImageableSize.</span><span class="sxs-lookup"><span data-stu-id="005a6-123">Coordinates are relative to PageImageableSize, where the origin of the watermark is relative to the origin of the PageImageableSize.</span></span><br/> |



 

## <a name="structural-content"></a><span data-ttu-id="005a6-124">Conteúdo estrutural</span><span class="sxs-lookup"><span data-stu-id="005a6-124">Structural Content</span></span>

<span data-ttu-id="005a6-125">A estrutura XML desse elemento é a seguinte:</span><span class="sxs-lookup"><span data-stu-id="005a6-125">The XML structure of this element is as follows:</span></span>

``` syntax
<psf:Feature name="psk:PageWatermark">
  <psf:Property name="psf:SelectionType">
    <psf:Value xsi:type="xs:string">psk:PickOne</psf:Value>
  </psf:Property>
  <psf:Option name="psk:_OptionName_">
    <psf:Property name="psf:IdentityOption">
      <psf:Value xsi:type="xs:string">_IdentityOptionValue_</psf:Value>
    </psf:Property>
    <!-- Defines the width origin of the watermark. See the PageWatermarkOriginWidth ParameterDefinition for more information. -->
    <psf:ScoredProperty name="psk:OriginWidth">
      <psf:ParameterRef name="psk:PageWatermarkOriginWidth" />
    </psf:ScoredProperty>
    <!-- Defines the height origin of the watermark. See the PageWatermarkOriginHeight ParameterDefinition for more information. -->
    <psf:ScoredProperty name="psk:OriginHeight">
      <psf:ParameterRef name="psk:PageWatermarkOriginHeight" />
    </psf:ScoredProperty>
    <!-- Defines the transparency value of the watermark.  Transparency should be applied to all content, including transparent content. See the PageWatermarkTransparency ParameterDefinition for more information. -->
    <psf:ScoredProperty name="psk:Transparency">
      <psf:ParameterRef name="psk:PageWatermarkTransparency" />
    </psf:ScoredProperty>
    <!-- Defines the angle value of the watermark.  See the PageWatermarkAngle ParameterDefinition for more information. -->
    <psf:ScoredProperty name="psk:Angle">
      <psf:ParameterRef name="psk:PageWatermarkAngle" />
    </psf:ScoredProperty>
    <!-- Applicable to options that include bitmaps.  -->
    <!-- Specifies the text font color -->
    <!-- Applicable to options that include text. Defines the sRGB color for the watermark text.  Format is ARGB: #AARRGGBB.   -->
    <psf:ScoredProperty name="psk:FontColor">
      <psf:ParameterRef name="psk:PageWatermarkTextColor" />
    </psf:ScoredProperty>
    <!-- Applicable to options that include text.  Defines the available font sizes for the watermark text. Measured in points.-->
    <psf:ScoredProperty name="psk:FontSize">
      <psf:ParameterRef name="psk:PageWatermarkTextFontSize" />
    </psf:ScoredProperty>
    <!-- Applicable to options that include text. Defines the text to be displayed in the watermark. -->
    <psf:ScoredProperty name="psk:Text">
      <psf:ParameterRef name="psk:PageWatermarkTextText" />
    </psf:ScoredProperty>
  </psf:Option>
  <!--Defines the layering behavior of the watermark. -->
  <psf:Feature name="psk:Layering">
    <!-- Watermark appears over page content. -->
    <psf:Option name="psk:Overlay" />
    <!-- Watermark appear under page content. -->
    <psf:Option name="psk:Underlay" />
  </psf:Feature>
</psf:Feature>
```

## <a name="structure-variables"></a><span data-ttu-id="005a6-126">Variáveis de estrutura</span><span class="sxs-lookup"><span data-stu-id="005a6-126">Structure Variables</span></span>

<span data-ttu-id="005a6-127">A tabela a seguir descreve as características das variáveis definidas na estrutura XML.</span><span class="sxs-lookup"><span data-stu-id="005a6-127">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="005a6-128">Nome</span><span class="sxs-lookup"><span data-stu-id="005a6-128">Name</span></span>                               | <span data-ttu-id="005a6-129">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="005a6-129">Data type</span></span>         | <span data-ttu-id="005a6-130">Unidade</span><span class="sxs-lookup"><span data-stu-id="005a6-130">Unit</span></span>                  | <span data-ttu-id="005a6-131">Valores com suporte</span><span class="sxs-lookup"><span data-stu-id="005a6-131">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="005a6-132">Resumo</span><span class="sxs-lookup"><span data-stu-id="005a6-132">Summary</span></span>                                                                      |
|------------------------------------|-------------------|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="005a6-133">\_Optionname\_</span><span class="sxs-lookup"><span data-stu-id="005a6-133">\_OptionName\_</span></span><br/>          | <span data-ttu-id="005a6-134">string</span><span class="sxs-lookup"><span data-stu-id="005a6-134">string</span></span><br/> | <span data-ttu-id="005a6-135">characters</span><span class="sxs-lookup"><span data-stu-id="005a6-135">characters</span></span><br/> | <span data-ttu-id="005a6-136">Nome totalmente qualificado válido, conforme definido [por Namespaces em XML.](https://www.w3.org/TR/1999/REC-xml-names-19990114/)</span><span class="sxs-lookup"><span data-stu-id="005a6-136">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="005a6-137">Se nenhum namespace for especificado, o namespace padrão será assumido.</span><span class="sxs-lookup"><span data-stu-id="005a6-137">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="005a6-138">O nome da opção.</span><span class="sxs-lookup"><span data-stu-id="005a6-138">The name of the option.</span></span><br/>                                           |
| <span data-ttu-id="005a6-139">\_IdentityOptionValue\_</span><span class="sxs-lookup"><span data-stu-id="005a6-139">\_IdentityOptionValue\_</span></span><br/> | <span data-ttu-id="005a6-140">string</span><span class="sxs-lookup"><span data-stu-id="005a6-140">string</span></span><br/> | <span data-ttu-id="005a6-141">n/d</span><span class="sxs-lookup"><span data-stu-id="005a6-141">n/a</span></span><br/>        | <span data-ttu-id="005a6-142">True, False.</span><span class="sxs-lookup"><span data-stu-id="005a6-142">True, False.</span></span><br/>                                                                                                                                                               | <span data-ttu-id="005a6-143">Define uma Opção que, quando selecionada, desabilitará esse recurso.</span><span class="sxs-lookup"><span data-stu-id="005a6-143">Defines an Option which when selected would disable this feature.</span></span><br/> |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="005a6-144">linguagem XML conteúdo (XML)</span><span class="sxs-lookup"><span data-stu-id="005a6-144">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="005a6-145">As palavras-chave public Print Schema são definidas no https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace .</span><span class="sxs-lookup"><span data-stu-id="005a6-145">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="005a6-146">O conteúdo linguagem XML XML (public linguagem XML) para essa palavra-chave é definido abaixo:</span><span class="sxs-lookup"><span data-stu-id="005a6-146">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

``` syntax
<psf:Feature name="psk:PageWatermark">
  <psf:Property name="psf:SelectionType">
    <psf:Value xsi:type="xs:string">psk:PickOne</psf:Value>
  </psf:Property>
  <!-- Specifies a text only watermark -->
  <psf:Option name="psk:Text">
    <psf:Property name="psf:IdentityOption">
      <psf:Value xsi:type="xs:string">True</psf:Value>
    </psf:Property>
    <psf:ScoredProperty name="psk:OriginWidth">
      <psf:ParameterRef name="psk:PageWatermarkOriginWidth" />
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:OriginHeight">
      <psf:ParameterRef name="psk:PageWatermarkOriginHeight" />
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:FontColor">
      <psf:ParameterRef name="psk:PageWatermarkTextColor" />
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:FontSize">
      <psf:ParameterRef name="psk:PageWatermarkTextFontSize" />
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:Text">
      <psf:ParameterRef name="psk:PageWatermarkTextText" />
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:Transparency">
      <psf:ParameterRef name="psk:PageWatermarkTransparency" />
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:Angle">
      <psf:ParameterRef name="psk:PageWatermarkTextAngle" />
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Feature name="psk:Layering">
    <!--Specifies Overlay Layering-->
    <psf:Option name="psk:Overlay" />
    <!--Specifies Underlay Layering-->
    <psf:Option name="psk:Underlay" />
  </psf:Feature>
</psf:Feature>
```

## <a name="related-topics"></a><span data-ttu-id="005a6-147">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="005a6-147">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="005a6-148">Especificação de esquema de impressão</span><span class="sxs-lookup"><span data-stu-id="005a6-148">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




