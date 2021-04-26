---
description: Este tópico não é atual. Para obter as informações mais atuais, consulte a especificação do esquema de impressão.
ms.assetid: d1c36c47-107c-4012-a839-1018c2652209
title: PageWatermark
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5e16a475255e42bda8e60b3bfb2ab41ea3998738
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/26/2021
ms.locfileid: "107994453"
---
# <a name="pagewatermark"></a><span data-ttu-id="dd9e4-104">PageWatermark</span><span class="sxs-lookup"><span data-stu-id="dd9e4-104">PageWatermark</span></span>

<span data-ttu-id="dd9e4-105">Este tópico não é atual.</span><span class="sxs-lookup"><span data-stu-id="dd9e4-105">This topic is not current.</span></span> <span data-ttu-id="dd9e4-106">Para obter as informações mais atuais, consulte a [especificação do esquema de impressão](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="dd9e4-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="dd9e4-107">Descreve a configuração de marca d' água da saída e as características da marca d' água.</span><span class="sxs-lookup"><span data-stu-id="dd9e4-107">Describes the watermark setting of the output and the watermark characteristics.</span></span> <span data-ttu-id="dd9e4-108">As marcas d' água se aplicam à página lógica, não à página física.</span><span class="sxs-lookup"><span data-stu-id="dd9e4-108">Watermarks apply to the logical page, not the physical page.</span></span> <span data-ttu-id="dd9e4-109">Por exemplo, se DocumentDuplex estiver habilitado, uma marca d' água será exibida em cada página do Mpeza em cada planilha.</span><span class="sxs-lookup"><span data-stu-id="dd9e4-109">For example, if DocumentDuplex is enabled, a watermark will appear on each NUp page on each sheet.</span></span> <span data-ttu-id="dd9e4-110">Se DocumentDuplex, PagesPerSheet = 2, cada planilha terá 2 marcas-d ' água.</span><span class="sxs-lookup"><span data-stu-id="dd9e4-110">If DocumentDuplex, PagesPerSheet=2, then each sheet will have 2 watermarks.</span></span>

-   [<span data-ttu-id="dd9e4-111">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="dd9e4-111">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="dd9e4-112">Conteúdo estrutural</span><span class="sxs-lookup"><span data-stu-id="dd9e4-112">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="dd9e4-113">Conteúdo de linguagem XML (XML)</span><span class="sxs-lookup"><span data-stu-id="dd9e4-113">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="dd9e4-114">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="dd9e4-114">Element Information</span></span>



| <span data-ttu-id="dd9e4-115">Nome</span><span class="sxs-lookup"><span data-stu-id="dd9e4-115">Name</span></span> | <span data-ttu-id="dd9e4-116">Valor</span><span class="sxs-lookup"><span data-stu-id="dd9e4-116">Value</span></span> |
|----------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="dd9e4-117">Tipo de elemento</span><span class="sxs-lookup"><span data-stu-id="dd9e4-117">Element Type</span></span> <br/>   | <span data-ttu-id="dd9e4-118">Recurso</span><span class="sxs-lookup"><span data-stu-id="dd9e4-118">Feature</span></span><br/>                                                                                                                              |
| <span data-ttu-id="dd9e4-119">Prefixo de escopo</span><span class="sxs-lookup"><span data-stu-id="dd9e4-119">Scoping Prefix</span></span> <br/> | <span data-ttu-id="dd9e4-120">?</span><span class="sxs-lookup"><span data-stu-id="dd9e4-120">Page</span></span><br/>                                                                                                                                 |
| <span data-ttu-id="dd9e4-121">Observações</span><span class="sxs-lookup"><span data-stu-id="dd9e4-121">Notes</span></span> <br/>          | <span data-ttu-id="dd9e4-122">As coordenadas são relativas a PageImageableSize, em que a origem da marca d' água é relativa à origem do PageImageableSize.</span><span class="sxs-lookup"><span data-stu-id="dd9e4-122">Coordinates are relative to PageImageableSize, where the origin of the watermark is relative to the origin of the PageImageableSize.</span></span><br/> |



 

## <a name="structural-content"></a><span data-ttu-id="dd9e4-123">Conteúdo estrutural</span><span class="sxs-lookup"><span data-stu-id="dd9e4-123">Structural Content</span></span>

<span data-ttu-id="dd9e4-124">A estrutura XML desse elemento é a seguinte:</span><span class="sxs-lookup"><span data-stu-id="dd9e4-124">The XML structure of this element is as follows:</span></span>

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

## <a name="structure-variables"></a><span data-ttu-id="dd9e4-125">Variáveis de estrutura</span><span class="sxs-lookup"><span data-stu-id="dd9e4-125">Structure Variables</span></span>

<span data-ttu-id="dd9e4-126">A tabela a seguir descreve as características das variáveis definidas na estrutura XML.</span><span class="sxs-lookup"><span data-stu-id="dd9e4-126">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="dd9e4-127">Nome</span><span class="sxs-lookup"><span data-stu-id="dd9e4-127">Name</span></span>                               | <span data-ttu-id="dd9e4-128">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="dd9e4-128">Data type</span></span>         | <span data-ttu-id="dd9e4-129">Unidade</span><span class="sxs-lookup"><span data-stu-id="dd9e4-129">Unit</span></span>                  | <span data-ttu-id="dd9e4-130">Valores com suporte</span><span class="sxs-lookup"><span data-stu-id="dd9e4-130">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="dd9e4-131">Resumo</span><span class="sxs-lookup"><span data-stu-id="dd9e4-131">Summary</span></span>                                                                      |
|------------------------------------|-------------------|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="dd9e4-132">\_OptionName\_</span><span class="sxs-lookup"><span data-stu-id="dd9e4-132">\_OptionName\_</span></span><br/>          | <span data-ttu-id="dd9e4-133">string</span><span class="sxs-lookup"><span data-stu-id="dd9e4-133">string</span></span><br/> | <span data-ttu-id="dd9e4-134">characters</span><span class="sxs-lookup"><span data-stu-id="dd9e4-134">characters</span></span><br/> | <span data-ttu-id="dd9e4-135">Nome totalmente qualificado válido, conforme definido pelos [namespaces em XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span><span class="sxs-lookup"><span data-stu-id="dd9e4-135">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="dd9e4-136">Se nenhum namespace for especificado, o namespace padrão será assumido.</span><span class="sxs-lookup"><span data-stu-id="dd9e4-136">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="dd9e4-137">O nome da opção.</span><span class="sxs-lookup"><span data-stu-id="dd9e4-137">The name of the option.</span></span><br/>                                           |
| <span data-ttu-id="dd9e4-138">\_IdentityOptionValue\_</span><span class="sxs-lookup"><span data-stu-id="dd9e4-138">\_IdentityOptionValue\_</span></span><br/> | <span data-ttu-id="dd9e4-139">string</span><span class="sxs-lookup"><span data-stu-id="dd9e4-139">string</span></span><br/> | <span data-ttu-id="dd9e4-140">N/D</span><span class="sxs-lookup"><span data-stu-id="dd9e4-140">n/a</span></span><br/>        | <span data-ttu-id="dd9e4-141">True, False.</span><span class="sxs-lookup"><span data-stu-id="dd9e4-141">True, False.</span></span><br/>                                                                                                                                                               | <span data-ttu-id="dd9e4-142">Define uma opção que, quando selecionada, desabilita esse recurso.</span><span class="sxs-lookup"><span data-stu-id="dd9e4-142">Defines an Option which when selected would disable this feature.</span></span><br/> |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="dd9e4-143">Conteúdo de linguagem XML (XML)</span><span class="sxs-lookup"><span data-stu-id="dd9e4-143">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="dd9e4-144">As palavras-chave do esquema de impressão pública são definidas no https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span><span class="sxs-lookup"><span data-stu-id="dd9e4-144">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="dd9e4-145">O conteúdo do linguagem XML público (XML) para essa palavra-chave é definido abaixo:</span><span class="sxs-lookup"><span data-stu-id="dd9e4-145">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

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

## <a name="related-topics"></a><span data-ttu-id="dd9e4-146">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="dd9e4-146">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="dd9e4-147">Especificação de esquema de impressão</span><span class="sxs-lookup"><span data-stu-id="dd9e4-147">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




