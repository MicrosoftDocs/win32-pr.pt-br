---
description: Este tópico não é atual. Para obter as informações mais atuais, consulte a especificação do esquema de impressão.
ms.assetid: 88f9a9a3-520e-4044-9ab2-961de03878fa
title: PageResolution
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6e0fdd16cf3dc0beb6a418b23d8ee6a93e4a6a61
ms.sourcegitcommit: 7b8f6151ebe247536304866459b2973276271d4d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/06/2021
ms.locfileid: "105785095"
---
# <a name="pageresolution"></a><span data-ttu-id="9a6d3-104">PageResolution</span><span class="sxs-lookup"><span data-stu-id="9a6d3-104">PageResolution</span></span>

<span data-ttu-id="9a6d3-105">Este tópico não é atual.</span><span class="sxs-lookup"><span data-stu-id="9a6d3-105">This topic is not current.</span></span> <span data-ttu-id="9a6d3-106">Para obter as informações mais atuais, consulte a [especificação do esquema de impressão](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="9a6d3-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="9a6d3-107">Define a resolução de página da saída impressa como um valor qualitativo ou pontos por polegada ou ambos.</span><span class="sxs-lookup"><span data-stu-id="9a6d3-107">Defines the page resolution of printed output as either a qualitative value or as dots per inch, or both.</span></span>

-   [<span data-ttu-id="9a6d3-108">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="9a6d3-108">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="9a6d3-109">Conteúdo estrutural</span><span class="sxs-lookup"><span data-stu-id="9a6d3-109">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="9a6d3-110">Conteúdo de linguagem XML (XML)</span><span class="sxs-lookup"><span data-stu-id="9a6d3-110">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="9a6d3-111">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="9a6d3-111">Element Information</span></span>



| <span data-ttu-id="9a6d3-112">Nome</span><span class="sxs-lookup"><span data-stu-id="9a6d3-112">Name</span></span>                       |                    |
|----------------------------|--------------------|
| <span data-ttu-id="9a6d3-113">Tipo de elemento</span><span class="sxs-lookup"><span data-stu-id="9a6d3-113">Element Type</span></span> <br/>   | <span data-ttu-id="9a6d3-114">Recurso</span><span class="sxs-lookup"><span data-stu-id="9a6d3-114">Feature</span></span><br/> |
| <span data-ttu-id="9a6d3-115">Prefixo de escopo</span><span class="sxs-lookup"><span data-stu-id="9a6d3-115">Scoping Prefix</span></span> <br/> | <span data-ttu-id="9a6d3-116">?</span><span class="sxs-lookup"><span data-stu-id="9a6d3-116">Page</span></span><br/>    |
| <span data-ttu-id="9a6d3-117">Observações</span><span class="sxs-lookup"><span data-stu-id="9a6d3-117">Notes</span></span> <br/>          | <span data-ttu-id="9a6d3-118">Nenhum</span><span class="sxs-lookup"><span data-stu-id="9a6d3-118">None</span></span><br/>    |



 

## <a name="structural-content"></a><span data-ttu-id="9a6d3-119">Conteúdo estrutural</span><span class="sxs-lookup"><span data-stu-id="9a6d3-119">Structural Content</span></span>

<span data-ttu-id="9a6d3-120">A estrutura XML desse elemento é:</span><span class="sxs-lookup"><span data-stu-id="9a6d3-120">The XML structure of this element is:</span></span>

``` syntax
<psf:Feature name="psk:PageResolution">
  <psf:Property name="psf:SelectionType">
    <psf:Value xsi:type="xs:string">psk:PickOne</psf:Value>
  </psf:Property>
  <psf:Option>
    <psf:Property name="psf:IdentityOption">
      <psf:Value xsi:type="xs:string">_IdentityOptionValue_</psf:Value>
    </psf:Property>
    <psf:ScoredProperty name="psk:ResolutionX">
      <psf:Value xsi:type="xs:integer">_ResolutionXValue_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:ResolutionY">
      <psf:Value xsi:type="xs:integer">_ResolutionYValue_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:QualitativeResolution">
      <psf:Value xsi:type="xs:string">_QualitativeResolutionValue_</psf:Value>
    </psf:ScoredProperty> 
  </psf:Option>
</psf:Feature>      
```

## <a name="structure-variables"></a><span data-ttu-id="9a6d3-121">Variáveis de estrutura</span><span class="sxs-lookup"><span data-stu-id="9a6d3-121">Structure Variables</span></span>

<span data-ttu-id="9a6d3-122">A tabela a seguir descreve as características das variáveis definidas na estrutura XML.</span><span class="sxs-lookup"><span data-stu-id="9a6d3-122">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="9a6d3-123">Nome</span><span class="sxs-lookup"><span data-stu-id="9a6d3-123">Name</span></span>                                      | <span data-ttu-id="9a6d3-124">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="9a6d3-124">Data type</span></span>          | <span data-ttu-id="9a6d3-125">Unidade</span><span class="sxs-lookup"><span data-stu-id="9a6d3-125">Unit</span></span>                  | <span data-ttu-id="9a6d3-126">Valores com suporte</span><span class="sxs-lookup"><span data-stu-id="9a6d3-126">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="9a6d3-127">Resumo</span><span class="sxs-lookup"><span data-stu-id="9a6d3-127">Summary</span></span>                                                                                                                                                          |
|-------------------------------------------|--------------------|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9a6d3-128">\_OptionName\_</span><span class="sxs-lookup"><span data-stu-id="9a6d3-128">\_OptionName\_</span></span><br/>                 | <span data-ttu-id="9a6d3-129">string</span><span class="sxs-lookup"><span data-stu-id="9a6d3-129">string</span></span><br/>  | <span data-ttu-id="9a6d3-130">characters</span><span class="sxs-lookup"><span data-stu-id="9a6d3-130">characters</span></span><br/> | <span data-ttu-id="9a6d3-131">Nome totalmente qualificado válido, conforme definido pelos [namespaces em XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span><span class="sxs-lookup"><span data-stu-id="9a6d3-131">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="9a6d3-132">Se nenhum namespace for especificado, o namespace padrão será assumido.</span><span class="sxs-lookup"><span data-stu-id="9a6d3-132">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="9a6d3-133">O nome da opção.</span><span class="sxs-lookup"><span data-stu-id="9a6d3-133">The name of the option.</span></span><br/>                                                                                                                               |
| <span data-ttu-id="9a6d3-134">\_IdentityOptionValue\_</span><span class="sxs-lookup"><span data-stu-id="9a6d3-134">\_IdentityOptionValue\_</span></span><br/>        | <span data-ttu-id="9a6d3-135">string</span><span class="sxs-lookup"><span data-stu-id="9a6d3-135">string</span></span><br/>  | <span data-ttu-id="9a6d3-136">N/D</span><span class="sxs-lookup"><span data-stu-id="9a6d3-136">n/a</span></span><br/>        | <span data-ttu-id="9a6d3-137">True, False.</span><span class="sxs-lookup"><span data-stu-id="9a6d3-137">True, False.</span></span><br/>                                                                                                                                                               | <span data-ttu-id="9a6d3-138">Define uma opção que, quando selecionada, desabilita esse recurso.</span><span class="sxs-lookup"><span data-stu-id="9a6d3-138">Defines an Option which when selected would disable this feature.</span></span><br/>                                                                                     |
| <span data-ttu-id="9a6d3-139">\_ResolutionXValue\_</span><span class="sxs-lookup"><span data-stu-id="9a6d3-139">\_ResolutionXValue\_</span></span><br/>           | <span data-ttu-id="9a6d3-140">Número inteiro</span><span class="sxs-lookup"><span data-stu-id="9a6d3-140">integer</span></span><br/> | <span data-ttu-id="9a6d3-141">EXIBI</span><span class="sxs-lookup"><span data-stu-id="9a6d3-141">DPI</span></span><br/>        | <span data-ttu-id="9a6d3-142">Maior que 0.</span><span class="sxs-lookup"><span data-stu-id="9a6d3-142">Greater than 0.</span></span><br/>                                                                                                                                                            | <span data-ttu-id="9a6d3-143">Especifica o componente x da resolução em relação ao PageImageableSize em DPI (em relação à PageMediaSize e à direção do feed da mídia).</span><span class="sxs-lookup"><span data-stu-id="9a6d3-143">Specifies the x component of the resolution relative to the PageImageableSize in DPI (relative to the PageMediaSize and feed direction of the media).</span></span><br/> |
| <span data-ttu-id="9a6d3-144">\_ResolutionYValue\_</span><span class="sxs-lookup"><span data-stu-id="9a6d3-144">\_ResolutionYValue\_</span></span><br/>           | <span data-ttu-id="9a6d3-145">Número inteiro</span><span class="sxs-lookup"><span data-stu-id="9a6d3-145">integer</span></span><br/> | <span data-ttu-id="9a6d3-146">EXIBI</span><span class="sxs-lookup"><span data-stu-id="9a6d3-146">DPI</span></span><br/>        | <span data-ttu-id="9a6d3-147">Maior que 0.</span><span class="sxs-lookup"><span data-stu-id="9a6d3-147">Greater than 0.</span></span><br/>                                                                                                                                                            | <span data-ttu-id="9a6d3-148">Especifica o componente y da resolução em relação ao PageImageableSize em DPI (em relação à PageMediaSize e à direção do feed da mídia).</span><span class="sxs-lookup"><span data-stu-id="9a6d3-148">Specifies the y component of the resolution relative to the PageImageableSize in DPI (relative to the PageMediaSize and feed direction of the media).</span></span><br/> |
| <span data-ttu-id="9a6d3-149">\_QualitativeResolutionValue\_</span><span class="sxs-lookup"><span data-stu-id="9a6d3-149">\_QualitativeResolutionValue\_</span></span><br/> | <span data-ttu-id="9a6d3-150">string</span><span class="sxs-lookup"><span data-stu-id="9a6d3-150">string</span></span><br/>  | <span data-ttu-id="9a6d3-151">N/D</span><span class="sxs-lookup"><span data-stu-id="9a6d3-151">n/a</span></span><br/>        | <span data-ttu-id="9a6d3-152">Padrão, rascunho, alto, normal, outro.</span><span class="sxs-lookup"><span data-stu-id="9a6d3-152">Default, Draft, High, Normal, Other.</span></span><br/>                                                                                                                                       | <span data-ttu-id="9a6d3-153">Especifica um rótulo de qualidade para a resolução.</span><span class="sxs-lookup"><span data-stu-id="9a6d3-153">Specifies a quality label for the resolution.</span></span><br/>                                                                                                         |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="9a6d3-154">Conteúdo de linguagem XML (XML)</span><span class="sxs-lookup"><span data-stu-id="9a6d3-154">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="9a6d3-155">As palavras-chave do esquema de impressão pública são definidas no https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span><span class="sxs-lookup"><span data-stu-id="9a6d3-155">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="9a6d3-156">O conteúdo do linguagem XML público (XML) para essa palavra-chave é definido abaixo:</span><span class="sxs-lookup"><span data-stu-id="9a6d3-156">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

``` syntax
<psf:Feature name="psk:PageResolution">
  <psf:Property name="psf:SelectionType">
    <psf:Value xsi:type="xs:string">psk:PickOne</psf:Value>
  </psf:Property>
  <psf:Option>
    <!-- The horizontal resolution in dots per inch -->
    <psf:ScoredProperty name="psk:ResolutionX">
      <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <!-- The vertical resolution in dots per inch -->
    <psf:ScoredProperty name="psk:ResolutionY">
      <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <!-- Value representing the resolution -->
    <psf:ScoredProperty name="psk:QualitativeResolution">
      <psf:Value xsi:type="xs:string">Other</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
</psf:Feature>    
```

## <a name="related-topics"></a><span data-ttu-id="9a6d3-157">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="9a6d3-157">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9a6d3-158">Especificação de esquema de impressão</span><span class="sxs-lookup"><span data-stu-id="9a6d3-158">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




