---
description: Este tópico não é atual. Para obter as informações mais atuais, consulte a especificação do esquema de impressão.
ms.assetid: 4edd1fdf-9601-440d-b967-82ffa6dceeb1
title: PageBlackGenerationProcessing
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a4aba727cfa1c11850b62a883b95ab78a6dfae50
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/26/2021
ms.locfileid: "107996253"
---
# <a name="pageblackgenerationprocessing"></a><span data-ttu-id="258bd-104">PageBlackGenerationProcessing</span><span class="sxs-lookup"><span data-stu-id="258bd-104">PageBlackGenerationProcessing</span></span>

<span data-ttu-id="258bd-105">Este tópico não é atual.</span><span class="sxs-lookup"><span data-stu-id="258bd-105">This topic is not current.</span></span> <span data-ttu-id="258bd-106">Para obter as informações mais atuais, consulte a [especificação do esquema de impressão](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="258bd-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="258bd-107">Especifica o comportamento de geração de preto para separações CMYK.</span><span class="sxs-lookup"><span data-stu-id="258bd-107">Specifies black generation behavior for CMYK separations.</span></span>

-   [<span data-ttu-id="258bd-108">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="258bd-108">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="258bd-109">Conteúdo estrutural</span><span class="sxs-lookup"><span data-stu-id="258bd-109">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="258bd-110">Conteúdo de linguagem XML (XML)</span><span class="sxs-lookup"><span data-stu-id="258bd-110">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="258bd-111">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="258bd-111">Element Information</span></span>



| <span data-ttu-id="258bd-112">Nome</span><span class="sxs-lookup"><span data-stu-id="258bd-112">Name</span></span> | <span data-ttu-id="258bd-113">Valor</span><span class="sxs-lookup"><span data-stu-id="258bd-113">Value</span></span> |
|----------------------------|--------------------|
| <span data-ttu-id="258bd-114">Tipo de elemento</span><span class="sxs-lookup"><span data-stu-id="258bd-114">Element Type</span></span> <br/>   | <span data-ttu-id="258bd-115">Recurso</span><span class="sxs-lookup"><span data-stu-id="258bd-115">Feature</span></span><br/> |
| <span data-ttu-id="258bd-116">Prefixo de escopo</span><span class="sxs-lookup"><span data-stu-id="258bd-116">Scoping Prefix</span></span> <br/> | <span data-ttu-id="258bd-117">?</span><span class="sxs-lookup"><span data-stu-id="258bd-117">Page</span></span><br/>    |
| <span data-ttu-id="258bd-118">Observações</span><span class="sxs-lookup"><span data-stu-id="258bd-118">Notes</span></span> <br/>          | <span data-ttu-id="258bd-119">Nenhum</span><span class="sxs-lookup"><span data-stu-id="258bd-119">None</span></span> <br/>   |



 

## <a name="structural-content"></a><span data-ttu-id="258bd-120">Conteúdo estrutural</span><span class="sxs-lookup"><span data-stu-id="258bd-120">Structural Content</span></span>

<span data-ttu-id="258bd-121">A estrutura XML desse elemento é:</span><span class="sxs-lookup"><span data-stu-id="258bd-121">The XML structure of this element is:</span></span>

``` syntax
<psf:Feature name="psk:PageBlackGenerationProcessing">
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

## <a name="structure-variables"></a><span data-ttu-id="258bd-122">Variáveis de estrutura</span><span class="sxs-lookup"><span data-stu-id="258bd-122">Structure Variables</span></span>

<span data-ttu-id="258bd-123">A tabela a seguir descreve as características das variáveis definidas na estrutura XML.</span><span class="sxs-lookup"><span data-stu-id="258bd-123">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="258bd-124">Nome</span><span class="sxs-lookup"><span data-stu-id="258bd-124">Name</span></span>                               | <span data-ttu-id="258bd-125">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="258bd-125">Data type</span></span>         | <span data-ttu-id="258bd-126">Unidade</span><span class="sxs-lookup"><span data-stu-id="258bd-126">Unit</span></span>                  | <span data-ttu-id="258bd-127">Valores com suporte</span><span class="sxs-lookup"><span data-stu-id="258bd-127">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="258bd-128">Resumo</span><span class="sxs-lookup"><span data-stu-id="258bd-128">Summary</span></span>                                                                      |
|------------------------------------|-------------------|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="258bd-129">\_OptionName\_</span><span class="sxs-lookup"><span data-stu-id="258bd-129">\_OptionName\_</span></span><br/>          | <span data-ttu-id="258bd-130">string</span><span class="sxs-lookup"><span data-stu-id="258bd-130">string</span></span><br/> | <span data-ttu-id="258bd-131">characters</span><span class="sxs-lookup"><span data-stu-id="258bd-131">characters</span></span><br/> | <span data-ttu-id="258bd-132">Nome totalmente qualificado válido, conforme definido pelos [namespaces em XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span><span class="sxs-lookup"><span data-stu-id="258bd-132">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="258bd-133">Se nenhum namespace for especificado, o namespace padrão será assumido.</span><span class="sxs-lookup"><span data-stu-id="258bd-133">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="258bd-134">O nome da opção.</span><span class="sxs-lookup"><span data-stu-id="258bd-134">The name of the option.</span></span><br/>                                           |
| <span data-ttu-id="258bd-135">\_IdentityOptionValue\_</span><span class="sxs-lookup"><span data-stu-id="258bd-135">\_IdentityOptionValue\_</span></span><br/> | <span data-ttu-id="258bd-136">string</span><span class="sxs-lookup"><span data-stu-id="258bd-136">string</span></span><br/> | <span data-ttu-id="258bd-137">N/D</span><span class="sxs-lookup"><span data-stu-id="258bd-137">n/a</span></span><br/>        | <span data-ttu-id="258bd-138">True, False.</span><span class="sxs-lookup"><span data-stu-id="258bd-138">True, False.</span></span><br/>                                                                                                                                                               | <span data-ttu-id="258bd-139">Define uma opção que, quando selecionada, desabilita esse recurso.</span><span class="sxs-lookup"><span data-stu-id="258bd-139">Defines an Option which when selected would disable this feature.</span></span><br/> |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="258bd-140">Conteúdo de linguagem XML (XML)</span><span class="sxs-lookup"><span data-stu-id="258bd-140">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="258bd-141">As palavras-chave do esquema de impressão pública são definidas no https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span><span class="sxs-lookup"><span data-stu-id="258bd-141">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="258bd-142">O conteúdo do linguagem XML público (XML) para essa palavra-chave é definido abaixo:</span><span class="sxs-lookup"><span data-stu-id="258bd-142">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

``` syntax
<psf:Feature name="psk:PageBlackGenerationProcessing">
  <psf:Option name="psk:Automatic" />
  <psf:Option name="psk:Custom">
    <!-- The max allowable sum of the four ink coverages anywhere in an image. -->
    <psf:ScoredProperty name="psk:TotalInkCoverageLimit">
      <psf:ParameterRef name="psk:PageBlackGenerationProcessingTotalInkCoverageLimit" />
    </psf:ScoredProperty>
    <!-- The maximum allowed K channel value. -->
    <psf:ScoredProperty name="psk:BlackInkLimit">
      <psf:ParameterRef name="psk:PageBlackGenerationProcessingBlackInkLimit" />
    </psf:ScoredProperty>
    <!-- The percentage of gray component replacement to perform. -->
    <psf:ScoredProperty name="psk:GrayComponentReplacementLevel">
      <psf:ParameterRef name="psk:PageBlackGenerationProcessingGrayComponentReplacementLevel" />
    </psf:ScoredProperty>
    <!-- The point in the highlight to shadow range where GCR should start (100% = darkest shadow). -->
    <psf:ScoredProperty name="psk:GrayComponentReplacementStart">
      <psf:ParameterRef name="psk:PageBlackGenerationProcessingGrayComponentReplacementStart" />
    </psf:ScoredProperty>
    <!-- The extented beyond neutrals (into chromatic colors) that GCR applies.  0% = Undercolor component replacement, 100% = Gray component replacement.  -->
    <psf:ScoredProperty name="psk:GrayComponentReplacementExtent">
      <psf:ParameterRef name="psk:PageBlackGenerationProcessingGrayComponentReplacementExtent" />
    </psf:ScoredProperty>
    <!-- The shadow level below which UCA will be applied.  -->
    <psf:ScoredProperty name="psk:UnderColorAdditionStart">
      <psf:ParameterRef name="psk:PageBlackGenerationProcessingUnderColorAdditionStart" />
    </psf:ScoredProperty>
    <!-- The amount chromatic ink (in gray component ratios) to add to areas where GCR/UCR has generated "BlackInkLimit" (or UCAStart, if specified) in the dark neutrals and near-neutral areas.  -->
    <psf:ScoredProperty name="psk:UnderColorAdditionLevel">
      <psf:ParameterRef name="psk:PageBlackGenerationProcessingUnderColorAdditionLevel" />
    </psf:ScoredProperty>
  </psf:Option>
</psf:Feature> 
```

## <a name="related-topics"></a><span data-ttu-id="258bd-143">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="258bd-143">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="258bd-144">Especificação de esquema de impressão</span><span class="sxs-lookup"><span data-stu-id="258bd-144">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




