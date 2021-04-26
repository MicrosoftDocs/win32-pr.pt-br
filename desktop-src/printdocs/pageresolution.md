---
description: Este tópico não é atual. Para obter as informações mais atuais, consulte a especificação do esquema de impressão.
ms.assetid: 88f9a9a3-520e-4044-9ab2-961de03878fa
title: PageResolution
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4e44a7ff73c03929d3dfc8bc9f7c31c878ad039c
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/26/2021
ms.locfileid: "107993713"
---
# <a name="pageresolution"></a><span data-ttu-id="5245e-104">PageResolution</span><span class="sxs-lookup"><span data-stu-id="5245e-104">PageResolution</span></span>

<span data-ttu-id="5245e-105">Este tópico não é atual.</span><span class="sxs-lookup"><span data-stu-id="5245e-105">This topic is not current.</span></span> <span data-ttu-id="5245e-106">Para obter as informações mais atuais, consulte a [especificação do esquema de impressão](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="5245e-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="5245e-107">Define a resolução de página da saída impressa como um valor qualitativo ou pontos por polegada ou ambos.</span><span class="sxs-lookup"><span data-stu-id="5245e-107">Defines the page resolution of printed output as either a qualitative value or as dots per inch, or both.</span></span>

-   [<span data-ttu-id="5245e-108">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="5245e-108">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="5245e-109">Conteúdo estrutural</span><span class="sxs-lookup"><span data-stu-id="5245e-109">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="5245e-110">Conteúdo de linguagem XML (XML)</span><span class="sxs-lookup"><span data-stu-id="5245e-110">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="5245e-111">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="5245e-111">Element Information</span></span>



| <span data-ttu-id="5245e-112">Nome</span><span class="sxs-lookup"><span data-stu-id="5245e-112">Name</span></span> | <span data-ttu-id="5245e-113">Valor</span><span class="sxs-lookup"><span data-stu-id="5245e-113">Value</span></span> |
|----------------------------|--------------------|
| <span data-ttu-id="5245e-114">Tipo de elemento</span><span class="sxs-lookup"><span data-stu-id="5245e-114">Element Type</span></span> <br/>   | <span data-ttu-id="5245e-115">Recurso</span><span class="sxs-lookup"><span data-stu-id="5245e-115">Feature</span></span><br/> |
| <span data-ttu-id="5245e-116">Prefixo de escopo</span><span class="sxs-lookup"><span data-stu-id="5245e-116">Scoping Prefix</span></span> <br/> | <span data-ttu-id="5245e-117">?</span><span class="sxs-lookup"><span data-stu-id="5245e-117">Page</span></span><br/>    |
| <span data-ttu-id="5245e-118">Observações</span><span class="sxs-lookup"><span data-stu-id="5245e-118">Notes</span></span> <br/>          | <span data-ttu-id="5245e-119">Nenhum</span><span class="sxs-lookup"><span data-stu-id="5245e-119">None</span></span><br/>    |



 

## <a name="structural-content"></a><span data-ttu-id="5245e-120">Conteúdo estrutural</span><span class="sxs-lookup"><span data-stu-id="5245e-120">Structural Content</span></span>

<span data-ttu-id="5245e-121">A estrutura XML desse elemento é:</span><span class="sxs-lookup"><span data-stu-id="5245e-121">The XML structure of this element is:</span></span>

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

## <a name="structure-variables"></a><span data-ttu-id="5245e-122">Variáveis de estrutura</span><span class="sxs-lookup"><span data-stu-id="5245e-122">Structure Variables</span></span>

<span data-ttu-id="5245e-123">A tabela a seguir descreve as características das variáveis definidas na estrutura XML.</span><span class="sxs-lookup"><span data-stu-id="5245e-123">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="5245e-124">Nome</span><span class="sxs-lookup"><span data-stu-id="5245e-124">Name</span></span>                                      | <span data-ttu-id="5245e-125">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="5245e-125">Data type</span></span>          | <span data-ttu-id="5245e-126">Unidade</span><span class="sxs-lookup"><span data-stu-id="5245e-126">Unit</span></span>                  | <span data-ttu-id="5245e-127">Valores com suporte</span><span class="sxs-lookup"><span data-stu-id="5245e-127">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="5245e-128">Resumo</span><span class="sxs-lookup"><span data-stu-id="5245e-128">Summary</span></span>                                                                                                                                                          |
|-------------------------------------------|--------------------|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5245e-129">\_OptionName\_</span><span class="sxs-lookup"><span data-stu-id="5245e-129">\_OptionName\_</span></span><br/>                 | <span data-ttu-id="5245e-130">string</span><span class="sxs-lookup"><span data-stu-id="5245e-130">string</span></span><br/>  | <span data-ttu-id="5245e-131">characters</span><span class="sxs-lookup"><span data-stu-id="5245e-131">characters</span></span><br/> | <span data-ttu-id="5245e-132">Nome totalmente qualificado válido, conforme definido pelos [namespaces em XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span><span class="sxs-lookup"><span data-stu-id="5245e-132">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="5245e-133">Se nenhum namespace for especificado, o namespace padrão será assumido.</span><span class="sxs-lookup"><span data-stu-id="5245e-133">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="5245e-134">O nome da opção.</span><span class="sxs-lookup"><span data-stu-id="5245e-134">The name of the option.</span></span><br/>                                                                                                                               |
| <span data-ttu-id="5245e-135">\_IdentityOptionValue\_</span><span class="sxs-lookup"><span data-stu-id="5245e-135">\_IdentityOptionValue\_</span></span><br/>        | <span data-ttu-id="5245e-136">string</span><span class="sxs-lookup"><span data-stu-id="5245e-136">string</span></span><br/>  | <span data-ttu-id="5245e-137">N/D</span><span class="sxs-lookup"><span data-stu-id="5245e-137">n/a</span></span><br/>        | <span data-ttu-id="5245e-138">True, False.</span><span class="sxs-lookup"><span data-stu-id="5245e-138">True, False.</span></span><br/>                                                                                                                                                               | <span data-ttu-id="5245e-139">Define uma opção que, quando selecionada, desabilita esse recurso.</span><span class="sxs-lookup"><span data-stu-id="5245e-139">Defines an Option which when selected would disable this feature.</span></span><br/>                                                                                     |
| <span data-ttu-id="5245e-140">\_ResolutionXValue\_</span><span class="sxs-lookup"><span data-stu-id="5245e-140">\_ResolutionXValue\_</span></span><br/>           | <span data-ttu-id="5245e-141">Número inteiro</span><span class="sxs-lookup"><span data-stu-id="5245e-141">integer</span></span><br/> | <span data-ttu-id="5245e-142">EXIBI</span><span class="sxs-lookup"><span data-stu-id="5245e-142">DPI</span></span><br/>        | <span data-ttu-id="5245e-143">Maior que 0.</span><span class="sxs-lookup"><span data-stu-id="5245e-143">Greater than 0.</span></span><br/>                                                                                                                                                            | <span data-ttu-id="5245e-144">Especifica o componente x da resolução em relação ao PageImageableSize em DPI (em relação à PageMediaSize e à direção do feed da mídia).</span><span class="sxs-lookup"><span data-stu-id="5245e-144">Specifies the x component of the resolution relative to the PageImageableSize in DPI (relative to the PageMediaSize and feed direction of the media).</span></span><br/> |
| <span data-ttu-id="5245e-145">\_ResolutionYValue\_</span><span class="sxs-lookup"><span data-stu-id="5245e-145">\_ResolutionYValue\_</span></span><br/>           | <span data-ttu-id="5245e-146">Número inteiro</span><span class="sxs-lookup"><span data-stu-id="5245e-146">integer</span></span><br/> | <span data-ttu-id="5245e-147">EXIBI</span><span class="sxs-lookup"><span data-stu-id="5245e-147">DPI</span></span><br/>        | <span data-ttu-id="5245e-148">Maior que 0.</span><span class="sxs-lookup"><span data-stu-id="5245e-148">Greater than 0.</span></span><br/>                                                                                                                                                            | <span data-ttu-id="5245e-149">Especifica o componente y da resolução em relação ao PageImageableSize em DPI (em relação à PageMediaSize e à direção do feed da mídia).</span><span class="sxs-lookup"><span data-stu-id="5245e-149">Specifies the y component of the resolution relative to the PageImageableSize in DPI (relative to the PageMediaSize and feed direction of the media).</span></span><br/> |
| <span data-ttu-id="5245e-150">\_QualitativeResolutionValue\_</span><span class="sxs-lookup"><span data-stu-id="5245e-150">\_QualitativeResolutionValue\_</span></span><br/> | <span data-ttu-id="5245e-151">string</span><span class="sxs-lookup"><span data-stu-id="5245e-151">string</span></span><br/>  | <span data-ttu-id="5245e-152">N/D</span><span class="sxs-lookup"><span data-stu-id="5245e-152">n/a</span></span><br/>        | <span data-ttu-id="5245e-153">Padrão, rascunho, alto, normal, outro.</span><span class="sxs-lookup"><span data-stu-id="5245e-153">Default, Draft, High, Normal, Other.</span></span><br/>                                                                                                                                       | <span data-ttu-id="5245e-154">Especifica um rótulo de qualidade para a resolução.</span><span class="sxs-lookup"><span data-stu-id="5245e-154">Specifies a quality label for the resolution.</span></span><br/>                                                                                                         |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="5245e-155">Conteúdo de linguagem XML (XML)</span><span class="sxs-lookup"><span data-stu-id="5245e-155">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="5245e-156">As palavras-chave do esquema de impressão pública são definidas no https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span><span class="sxs-lookup"><span data-stu-id="5245e-156">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="5245e-157">O conteúdo do linguagem XML público (XML) para essa palavra-chave é definido abaixo:</span><span class="sxs-lookup"><span data-stu-id="5245e-157">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

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

## <a name="related-topics"></a><span data-ttu-id="5245e-158">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="5245e-158">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5245e-159">Especificação de esquema de impressão</span><span class="sxs-lookup"><span data-stu-id="5245e-159">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




