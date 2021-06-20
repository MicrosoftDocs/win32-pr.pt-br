---
description: Saiba mais sobre o elemento PageBlackGenerationProcessing, que especifica o comportamento de geração de preto para separações CMYK.
ms.assetid: 4edd1fdf-9601-440d-b967-82ffa6dceeb1
title: PageBlackGenerationProcessing
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d21861595917b67390857b380a416e441d454081
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/19/2021
ms.locfileid: "112408509"
---
# <a name="pageblackgenerationprocessing"></a><span data-ttu-id="24a85-103">PageBlackGenerationProcessing</span><span class="sxs-lookup"><span data-stu-id="24a85-103">PageBlackGenerationProcessing</span></span>

<span data-ttu-id="24a85-104">Este tópico não é atual.</span><span class="sxs-lookup"><span data-stu-id="24a85-104">This topic is not current.</span></span> <span data-ttu-id="24a85-105">Para obter as informações mais atuais, consulte a [especificação do esquema de impressão](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="24a85-105">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="24a85-106">Especifica o comportamento de geração de preto para separações CMYK.</span><span class="sxs-lookup"><span data-stu-id="24a85-106">Specifies black generation behavior for CMYK separations.</span></span>

-   [<span data-ttu-id="24a85-107">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="24a85-107">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="24a85-108">Conteúdo estrutural</span><span class="sxs-lookup"><span data-stu-id="24a85-108">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="24a85-109">Conteúdo de linguagem XML (XML)</span><span class="sxs-lookup"><span data-stu-id="24a85-109">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="24a85-110">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="24a85-110">Element Information</span></span>



| <span data-ttu-id="24a85-111">Name</span><span class="sxs-lookup"><span data-stu-id="24a85-111">Name</span></span> | <span data-ttu-id="24a85-112">Valor</span><span class="sxs-lookup"><span data-stu-id="24a85-112">Value</span></span> |
|----------------------------|--------------------|
| <span data-ttu-id="24a85-113">Tipo de elemento</span><span class="sxs-lookup"><span data-stu-id="24a85-113">Element Type</span></span> <br/>   | <span data-ttu-id="24a85-114">Recurso</span><span class="sxs-lookup"><span data-stu-id="24a85-114">Feature</span></span><br/> |
| <span data-ttu-id="24a85-115">Prefixo de escopo</span><span class="sxs-lookup"><span data-stu-id="24a85-115">Scoping Prefix</span></span> <br/> | <span data-ttu-id="24a85-116">?</span><span class="sxs-lookup"><span data-stu-id="24a85-116">Page</span></span><br/>    |
| <span data-ttu-id="24a85-117">Observações</span><span class="sxs-lookup"><span data-stu-id="24a85-117">Notes</span></span> <br/>          | <span data-ttu-id="24a85-118">Nenhum</span><span class="sxs-lookup"><span data-stu-id="24a85-118">None</span></span> <br/>   |



 

## <a name="structural-content"></a><span data-ttu-id="24a85-119">Conteúdo estrutural</span><span class="sxs-lookup"><span data-stu-id="24a85-119">Structural Content</span></span>

<span data-ttu-id="24a85-120">A estrutura XML desse elemento é:</span><span class="sxs-lookup"><span data-stu-id="24a85-120">The XML structure of this element is:</span></span>

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

## <a name="structure-variables"></a><span data-ttu-id="24a85-121">Variáveis de estrutura</span><span class="sxs-lookup"><span data-stu-id="24a85-121">Structure Variables</span></span>

<span data-ttu-id="24a85-122">A tabela a seguir descreve as características das variáveis definidas na estrutura XML.</span><span class="sxs-lookup"><span data-stu-id="24a85-122">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="24a85-123">Nome</span><span class="sxs-lookup"><span data-stu-id="24a85-123">Name</span></span>                               | <span data-ttu-id="24a85-124">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="24a85-124">Data type</span></span>         | <span data-ttu-id="24a85-125">Unidade</span><span class="sxs-lookup"><span data-stu-id="24a85-125">Unit</span></span>                  | <span data-ttu-id="24a85-126">Valores com suporte</span><span class="sxs-lookup"><span data-stu-id="24a85-126">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="24a85-127">Resumo</span><span class="sxs-lookup"><span data-stu-id="24a85-127">Summary</span></span>                                                                      |
|------------------------------------|-------------------|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="24a85-128">\_OptionName\_</span><span class="sxs-lookup"><span data-stu-id="24a85-128">\_OptionName\_</span></span><br/>          | <span data-ttu-id="24a85-129">string</span><span class="sxs-lookup"><span data-stu-id="24a85-129">string</span></span><br/> | <span data-ttu-id="24a85-130">characters</span><span class="sxs-lookup"><span data-stu-id="24a85-130">characters</span></span><br/> | <span data-ttu-id="24a85-131">Nome totalmente qualificado válido, conforme definido pelos [namespaces em XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span><span class="sxs-lookup"><span data-stu-id="24a85-131">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="24a85-132">Se nenhum namespace for especificado, o namespace padrão será assumido.</span><span class="sxs-lookup"><span data-stu-id="24a85-132">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="24a85-133">O nome da opção.</span><span class="sxs-lookup"><span data-stu-id="24a85-133">The name of the option.</span></span><br/>                                           |
| <span data-ttu-id="24a85-134">\_IdentityOptionValue\_</span><span class="sxs-lookup"><span data-stu-id="24a85-134">\_IdentityOptionValue\_</span></span><br/> | <span data-ttu-id="24a85-135">string</span><span class="sxs-lookup"><span data-stu-id="24a85-135">string</span></span><br/> | <span data-ttu-id="24a85-136">n/d</span><span class="sxs-lookup"><span data-stu-id="24a85-136">n/a</span></span><br/>        | <span data-ttu-id="24a85-137">True, False.</span><span class="sxs-lookup"><span data-stu-id="24a85-137">True, False.</span></span><br/>                                                                                                                                                               | <span data-ttu-id="24a85-138">Define uma opção que, quando selecionada, desabilita esse recurso.</span><span class="sxs-lookup"><span data-stu-id="24a85-138">Defines an Option which when selected would disable this feature.</span></span><br/> |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="24a85-139">Conteúdo de linguagem XML (XML)</span><span class="sxs-lookup"><span data-stu-id="24a85-139">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="24a85-140">As palavras-chave do esquema de impressão pública são definidas no https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span><span class="sxs-lookup"><span data-stu-id="24a85-140">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="24a85-141">O conteúdo do linguagem XML público (XML) para essa palavra-chave é definido abaixo:</span><span class="sxs-lookup"><span data-stu-id="24a85-141">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

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

## <a name="related-topics"></a><span data-ttu-id="24a85-142">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="24a85-142">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="24a85-143">Especificação de esquema de impressão</span><span class="sxs-lookup"><span data-stu-id="24a85-143">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




