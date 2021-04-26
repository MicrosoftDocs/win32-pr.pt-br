---
description: Este tópico não é atual. Para obter as informações mais atuais, consulte a especificação do esquema de impressão.
ms.assetid: cf35bb37-bf67-4e86-bfef-9838606982a5
title: PageScaling
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e32beceead1c0dc867a2bb7b24d476ef05bf8820
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/26/2021
ms.locfileid: "107997493"
---
# <a name="pagescaling"></a><span data-ttu-id="a7aa3-104">PageScaling</span><span class="sxs-lookup"><span data-stu-id="a7aa3-104">PageScaling</span></span>

<span data-ttu-id="a7aa3-105">Este tópico não é atual.</span><span class="sxs-lookup"><span data-stu-id="a7aa3-105">This topic is not current.</span></span> <span data-ttu-id="a7aa3-106">Para obter as informações mais atuais, consulte a [especificação do esquema de impressão](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="a7aa3-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="a7aa3-107">Descreve as características de dimensionamento da saída.</span><span class="sxs-lookup"><span data-stu-id="a7aa3-107">Describes the scaling characteristics of the output.</span></span> <span data-ttu-id="a7aa3-108">Determinadas opções desse recurso exigem que o consumidor possa determinar as características das "dimensões de conteúdo do aplicativo".</span><span class="sxs-lookup"><span data-stu-id="a7aa3-108">Certain Options of this Feature requires the consumer to be able to determine characteristics of the "application content dimensions."</span></span> <span data-ttu-id="a7aa3-109">Na ausência da capacidade de determinar essas características, o consumidor deve padronizar a opção de identidade.</span><span class="sxs-lookup"><span data-stu-id="a7aa3-109">In the absence of the ability to determine these characteristics, the consumer should default to the identity option.</span></span> <span data-ttu-id="a7aa3-110">Essas características são:</span><span class="sxs-lookup"><span data-stu-id="a7aa3-110">These characteristics are:</span></span>



|                          |                                                                                                                                                                                                                                                       |
|--------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a7aa3-111">Tamanho da mídia do aplicativo</span><span class="sxs-lookup"><span data-stu-id="a7aa3-111">Application Media Size</span></span>   | <span data-ttu-id="a7aa3-112">As dimensões da mídia definida pelo layout do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="a7aa3-112">The dimensions of the media defined by the application layout.</span></span> <span data-ttu-id="a7aa3-113">O tamanho da mídia do aplicativo pode ou não corresponder a um PageMediaSize com suporte do consumidor.</span><span class="sxs-lookup"><span data-stu-id="a7aa3-113">The application media size may or may not correspond to a PageMediaSize supported by the consumer.</span></span><br/>                                                                          |
| <span data-ttu-id="a7aa3-114">Tamanho do conteúdo do aplicativo</span><span class="sxs-lookup"><span data-stu-id="a7aa3-114">Application Content Size</span></span> | <span data-ttu-id="a7aa3-115">As dimensões da mídia definida pelo layout do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="a7aa3-115">The dimensions of the media defined by the application layout.</span></span> <span data-ttu-id="a7aa3-116">O tamanho da mídia do aplicativo pode ou não corresponder a um PageMediaSize com suporte do consumidor.</span><span class="sxs-lookup"><span data-stu-id="a7aa3-116">The application media size may or may not correspond to a PageMediaSize supported by the consumer.</span></span><br/>                                                                          |
| <span data-ttu-id="a7aa3-117">Tamanho da sangria do aplicativo</span><span class="sxs-lookup"><span data-stu-id="a7aa3-117">Application Bleed Size</span></span>   | <span data-ttu-id="a7aa3-118">O deslocamento e a extensão da área de sangria do aplicativo, uma caixa de estouro usada pelo aplicativo para registro e layout, em relação ao tamanho da mídia do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="a7aa3-118">The offset and extent of the application bleed area, an overflow box used by application for registration and layout, in relation to the application media size.</span></span> <span data-ttu-id="a7aa3-119">A área de sangria será excelente ou igual ao tamanho da mídia do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="a7aa3-119">The bleed area will be great than or equal to the application media size.</span></span><br/> |



 

-   [<span data-ttu-id="a7aa3-120">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="a7aa3-120">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="a7aa3-121">Conteúdo estrutural</span><span class="sxs-lookup"><span data-stu-id="a7aa3-121">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="a7aa3-122">Conteúdo de linguagem XML (XML)</span><span class="sxs-lookup"><span data-stu-id="a7aa3-122">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="a7aa3-123">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="a7aa3-123">Element Information</span></span>



| <span data-ttu-id="a7aa3-124">Nome</span><span class="sxs-lookup"><span data-stu-id="a7aa3-124">Name</span></span> | <span data-ttu-id="a7aa3-125">Valor</span><span class="sxs-lookup"><span data-stu-id="a7aa3-125">Value</span></span> |
|----------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a7aa3-126">Tipo de elemento</span><span class="sxs-lookup"><span data-stu-id="a7aa3-126">Element Type</span></span> <br/>   | <span data-ttu-id="a7aa3-127">Recurso</span><span class="sxs-lookup"><span data-stu-id="a7aa3-127">Feature</span></span><br/>                                                                                                                                                                                    |
| <span data-ttu-id="a7aa3-128">Prefixo de escopo</span><span class="sxs-lookup"><span data-stu-id="a7aa3-128">Scoping Prefix</span></span> <br/> | <span data-ttu-id="a7aa3-129">?</span><span class="sxs-lookup"><span data-stu-id="a7aa3-129">Page</span></span><br/>                                                                                                                                                                                       |
| <span data-ttu-id="a7aa3-130">Observações</span><span class="sxs-lookup"><span data-stu-id="a7aa3-130">Notes</span></span> <br/>          | <span data-ttu-id="a7aa3-131">Superior, inferior, esquerda e direita são relativos ao PageImageableSize.</span><span class="sxs-lookup"><span data-stu-id="a7aa3-131">Top, Bottom, Left, and Right are relative to the PageImageableSize.</span></span> <span data-ttu-id="a7aa3-132">As coordenadas são relativas a PageImageableSize, em que a origem de é relativa à origem do PageImageableSize.</span><span class="sxs-lookup"><span data-stu-id="a7aa3-132">Coordinates are relative to PageImageableSize, where the origin of is relative to the origin of the PageImageableSize.</span></span><br/> |



 

## <a name="structural-content"></a><span data-ttu-id="a7aa3-133">Conteúdo estrutural</span><span class="sxs-lookup"><span data-stu-id="a7aa3-133">Structural Content</span></span>

<span data-ttu-id="a7aa3-134">A estrutura XML desse elemento é:</span><span class="sxs-lookup"><span data-stu-id="a7aa3-134">The XML structure of this element is:</span></span>

``` syntax
<psf:Feature name="psk:PageScaling">
  <psf:Property name="psf:SelectionType">
    <psf:Value xsi:type="xs:string">psk:PickOne</psf:Value>
  </psf:Property>
  <psf:Option name="psk:_OptionName_">
    <psf:Property name="psf:IdentityOption">
      <psf:Value xsi:type="xs:string">_IdentityOptionValue_</psf:Value>
    </psf:Property>
    <!-- Specifies offset of the width relative to the PageImageableSize.  
         Measured in microns. -->
    <psf:ScoredProperty name="psk:OffsetWidth">
      <psf:ParameterRef name="psk:PageScalingOffsetWidth" />
    </psf:ScoredProperty>
    <!-- Specifies offset of the height relative to the PageImageableSize.  
         Measured in microns. -->
    <psf:ScoredProperty name="psk:OffsetHeight">
      <psf:ParameterRef name="psk:PageScalingOffsetHeight" />
    </psf:ScoredProperty>
    <!-- Specifies the scaling percentage for the width dimension relative to the PageImageableSize. -->
    <psf:ScoredProperty name="psk:ScaleWidth">
      <psf:ParameterRef name="psk:PageScalingScaleWidth" />
    </psf:ScoredProperty>
    <!-- Specifies the scaling percentage for the height dimension relative to the PageImageableSize. -->
    <psf:ScoredProperty name="psk:ScaleHeight">
      <psf:ParameterRef name="psk:PageScalingScaleHeight" />
    </psf:ScoredProperty>
    <!-- Specifies the scaling percentage for square scaling (both dimensions are scaled equally). -->
    <psf:ScoredProperty name="psk:Scale">
      <psf:ParameterRef name="psk:PageScalingScale" />
    </psf:ScoredProperty>
  </psf:Option>
  <!-- Specifies the alignment of the scaled content. -->
  <psf:Feature name="psk:ScaleOffsetAlignment">
    <!-- Specifies the scaling should be aligned on the center of the bottom edge of the media. -->
    <psf:Option name="psk:BottomCenter"/>
    <!-- Specifies the scaling should be aligned on the bottom left corner of the media. -->
    <psf:Option name="psk:BottomLeft" />
    <!-- Specifies the scaling should be aligned on the bottom right corner of the media. -->
    <psf:Option name="psk:BottomRight "/>
    <!-- Specifies the scaling should be aligned on the bottom right corner of the media. -->
    <psf:Option name="psk:Center"/>
    <!-- Specifies the scaling should be aligned on the center of the left edge of the media. -->
    <psf:Option name="psk:LeftCenter"/>
    <!-- Specifies the scaling should be aligned on the center of the right edge of the media. -->
    <psf:Option name="psk:RightCenter"/>
    <!-- Specifies the scaling should be aligned on the center of the top edge of the media. -->
    <psf:Option name="psk:TopCenter"/>
    <!-- Specifies the scaling should be aligned on the top left corner of the media. -->
    <psf:Option name="psk:TopLeft"/>
    <!-- Specifies the scaling should be aligned on the top right corner of the media. -->
    <psf:Option name="psk:TopRight"/>
  </psf:Feature>
</psf:Feature>
```

## <a name="structure-variables"></a><span data-ttu-id="a7aa3-135">Variáveis de estrutura</span><span class="sxs-lookup"><span data-stu-id="a7aa3-135">Structure Variables</span></span>

<span data-ttu-id="a7aa3-136">A tabela a seguir descreve as características das variáveis definidas na estrutura XML.</span><span class="sxs-lookup"><span data-stu-id="a7aa3-136">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="a7aa3-137">Nome</span><span class="sxs-lookup"><span data-stu-id="a7aa3-137">Name</span></span>                               | <span data-ttu-id="a7aa3-138">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="a7aa3-138">Data type</span></span>         | <span data-ttu-id="a7aa3-139">Unidade</span><span class="sxs-lookup"><span data-stu-id="a7aa3-139">Unit</span></span>                  | <span data-ttu-id="a7aa3-140">Valores com suporte</span><span class="sxs-lookup"><span data-stu-id="a7aa3-140">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="a7aa3-141">Resumo</span><span class="sxs-lookup"><span data-stu-id="a7aa3-141">Summary</span></span>                                                                      |
|------------------------------------|-------------------|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="a7aa3-142">\_OptionName\_</span><span class="sxs-lookup"><span data-stu-id="a7aa3-142">\_OptionName\_</span></span><br/>          | <span data-ttu-id="a7aa3-143">string</span><span class="sxs-lookup"><span data-stu-id="a7aa3-143">string</span></span><br/> | <span data-ttu-id="a7aa3-144">characters</span><span class="sxs-lookup"><span data-stu-id="a7aa3-144">characters</span></span><br/> | <span data-ttu-id="a7aa3-145">Nome totalmente qualificado válido, conforme definido pelos [namespaces em XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span><span class="sxs-lookup"><span data-stu-id="a7aa3-145">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="a7aa3-146">Se nenhum namespace for especificado, o namespace padrão será assumido.</span><span class="sxs-lookup"><span data-stu-id="a7aa3-146">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="a7aa3-147">O nome da opção.</span><span class="sxs-lookup"><span data-stu-id="a7aa3-147">The name of the option.</span></span><br/>                                           |
| <span data-ttu-id="a7aa3-148">\_IdentityOptionValue\_</span><span class="sxs-lookup"><span data-stu-id="a7aa3-148">\_IdentityOptionValue\_</span></span><br/> | <span data-ttu-id="a7aa3-149">string</span><span class="sxs-lookup"><span data-stu-id="a7aa3-149">string</span></span><br/> | <span data-ttu-id="a7aa3-150">N/D</span><span class="sxs-lookup"><span data-stu-id="a7aa3-150">n/a</span></span><br/>        | <span data-ttu-id="a7aa3-151">True, False.</span><span class="sxs-lookup"><span data-stu-id="a7aa3-151">True, False.</span></span><br/>                                                                                                                                                               | <span data-ttu-id="a7aa3-152">Define uma opção que, quando selecionada, desabilita esse recurso.</span><span class="sxs-lookup"><span data-stu-id="a7aa3-152">Defines an Option which when selected would disable this feature.</span></span><br/> |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="a7aa3-153">Conteúdo de linguagem XML (XML)</span><span class="sxs-lookup"><span data-stu-id="a7aa3-153">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="a7aa3-154">As palavras-chave do esquema de impressão pública são definidas no https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span><span class="sxs-lookup"><span data-stu-id="a7aa3-154">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="a7aa3-155">O conteúdo do linguagem XML público (XML) para essa palavra-chave é definido abaixo:</span><span class="sxs-lookup"><span data-stu-id="a7aa3-155">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

``` syntax
<psf:Feature name="psk:PageScaling">
  <psf:Property name="psf:SelectionType">
    <psf:Value xsi:type="xs:string">psk:PickOne</psf:Value>
  </psf:Property>
  <psf:Option name="psk:Custom">
    <psf:ScoredProperty name="psk:OffsetWidth">
      <psf:ParameterRef name="psk:PageScalingOffsetWidth" />
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:OffsetHeight">
      <psf:ParameterRef name="psk:PageScalingOffsetHeight" />
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:ScaleWidth">
      <psf:ParameterRef name="psk:PageScalingScaleWidth" />
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:ScaleHeight">
      <psf:ParameterRef name="psk:PageScalingScaleHeight" />
    </psf:ScoredProperty>
  </psf:Option>
  <!-- Specifies a custom square scaling should be applied to the Application Media Size. -->
  <psf:Option name="psk:CustomSquare">
    <psf:ScoredProperty name="psk:OffsetWidth">
      <psf:ParameterRef name="psk:PageScalingOffsetWidth" />
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:OffsetHeight">
      <psf:ParameterRef name="psk:PageScalingOffsetHeight" />
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:Scale">
      <psf:ParameterRef name="psk:PageScalingScale" />
    </psf:ScoredProperty>
  </psf:Option>

  <!-- Specifies the application bleed size should be scaled to the PageImageableSize preserving the aspect ratio. -->
  <psf:Option name="psk:FitApplicationBleedSizeToPageImageableSize" />
  <!-- Specifies the application content size should be scaled to the PageImageableSize preserving the aspect ratio. -->
  <psf:Option name="psk:FitApplicationContentSizeToPageImageableSize" />
  <!-- Specifies the application media size should be scaled to the PageImageableSize preserving the aspect ratio. -->
  <psf:Option name="psk:FitApplicationMediaSizeToPageImageableSize" />
  <!-- Specifies the application media size should be scaled to the PageMediaSize preserving the aspect ratio. -->
  <psf:Option name="psk:FitApplicationMediaSizeToPageMediaSize" />

  <!-- Specifies that no scaling should be applied. -->
  <psf:Option name="psk:None" />

  <!-- Specifies the alignment of the scaled content. -->
  <psf:Feature name="psk:ScaleOffsetAlignment">
    <!-- Specifies the scaling should be aligned on the center of the bottom edge of the media. -->
    <psf:Option name="psk:BottomCenter" />
    <!-- Specifies the scaling should be aligned on the bottom left corner of the media.-->
    <psf:Option name="psk:BottomLeft" />
    <!--Specifies the scaling should be aligned on the bottom right corner of the media.-->
    <psf:Option name="psk:BottomRight" />
    <!-- Specifies the scaling should be centered on the media.-->
    <psf:Option name="psk:Center" />
    <!-- Specifies the scaling should be aligned on the center of the left edge of the media.-->
    <psf:Option name="psk:LeftCenter" />
    <!--Specifies the scaling should be aligned on the center of the right edge of the media.-->
    <psf:Option name="psk:RightCenter" />
    <!-- Specifies the scaling should be aligned on the center of the top edge of the media.-->
    <psf:Option name="psk:TopCenter" />
    <!--  Specifies the scaling should be aligned on the top left corner of the media.-->
    <psf:Option name="psk:TopLeft" />
    <!-- Specifies the scaling should be aligned on the top right corner of the media.-->
    <psf:Option name="psk:TopRight" />
  </psf:Feature>
</psf:Feature>
```

## <a name="related-topics"></a><span data-ttu-id="a7aa3-156">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="a7aa3-156">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a7aa3-157">Especificação de esquema de impressão</span><span class="sxs-lookup"><span data-stu-id="a7aa3-157">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




