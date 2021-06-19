---
description: Leia sobre o elemento configurável pelo usuário PageResolution. Este tópico não é atual. Para obter as informações mais atuais, consulte a Especificação de Esquema de Impressão.
ms.assetid: 88f9a9a3-520e-4044-9ab2-961de03878fa
title: Pageresolution
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 760384ff900e7b35e37105fdb19e3635a434aa5a
ms.sourcegitcommit: 91530c19d26ba4c57a6af1f37b57f211f580464e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/19/2021
ms.locfileid: "112394811"
---
# <a name="pageresolution"></a><span data-ttu-id="f63de-105">Pageresolution</span><span class="sxs-lookup"><span data-stu-id="f63de-105">PageResolution</span></span>

<span data-ttu-id="f63de-106">Este tópico não é atual.</span><span class="sxs-lookup"><span data-stu-id="f63de-106">This topic is not current.</span></span> <span data-ttu-id="f63de-107">Para obter as informações mais atuais, consulte a [Especificação de Esquema de Impressão](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="f63de-107">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="f63de-108">Define a resolução de página da saída impressa como um valor qualitativo ou pontos por polegada ou ambos.</span><span class="sxs-lookup"><span data-stu-id="f63de-108">Defines the page resolution of printed output as either a qualitative value or as dots per inch, or both.</span></span>

-   [<span data-ttu-id="f63de-109">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="f63de-109">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="f63de-110">Conteúdo estrutural</span><span class="sxs-lookup"><span data-stu-id="f63de-110">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="f63de-111">linguagem XML conteúdo (XML)</span><span class="sxs-lookup"><span data-stu-id="f63de-111">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="f63de-112">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="f63de-112">Element Information</span></span>



| <span data-ttu-id="f63de-113">Name</span><span class="sxs-lookup"><span data-stu-id="f63de-113">Name</span></span> | <span data-ttu-id="f63de-114">Valor</span><span class="sxs-lookup"><span data-stu-id="f63de-114">Value</span></span> |
|----------------------------|--------------------|
| <span data-ttu-id="f63de-115">Tipo de elemento</span><span class="sxs-lookup"><span data-stu-id="f63de-115">Element Type</span></span> <br/>   | <span data-ttu-id="f63de-116">Recurso</span><span class="sxs-lookup"><span data-stu-id="f63de-116">Feature</span></span><br/> |
| <span data-ttu-id="f63de-117">Prefixo de definição de scoping</span><span class="sxs-lookup"><span data-stu-id="f63de-117">Scoping Prefix</span></span> <br/> | <span data-ttu-id="f63de-118">?</span><span class="sxs-lookup"><span data-stu-id="f63de-118">Page</span></span><br/>    |
| <span data-ttu-id="f63de-119">Observações</span><span class="sxs-lookup"><span data-stu-id="f63de-119">Notes</span></span> <br/>          | <span data-ttu-id="f63de-120">Nenhum</span><span class="sxs-lookup"><span data-stu-id="f63de-120">None</span></span><br/>    |



 

## <a name="structural-content"></a><span data-ttu-id="f63de-121">Conteúdo estrutural</span><span class="sxs-lookup"><span data-stu-id="f63de-121">Structural Content</span></span>

<span data-ttu-id="f63de-122">A estrutura XML desse elemento é:</span><span class="sxs-lookup"><span data-stu-id="f63de-122">The XML structure of this element is:</span></span>

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

## <a name="structure-variables"></a><span data-ttu-id="f63de-123">Variáveis de estrutura</span><span class="sxs-lookup"><span data-stu-id="f63de-123">Structure Variables</span></span>

<span data-ttu-id="f63de-124">A tabela a seguir descreve as características das variáveis definidas na estrutura XML.</span><span class="sxs-lookup"><span data-stu-id="f63de-124">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="f63de-125">Nome</span><span class="sxs-lookup"><span data-stu-id="f63de-125">Name</span></span>                                      | <span data-ttu-id="f63de-126">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="f63de-126">Data type</span></span>          | <span data-ttu-id="f63de-127">Unidade</span><span class="sxs-lookup"><span data-stu-id="f63de-127">Unit</span></span>                  | <span data-ttu-id="f63de-128">Valores com suporte</span><span class="sxs-lookup"><span data-stu-id="f63de-128">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="f63de-129">Resumo</span><span class="sxs-lookup"><span data-stu-id="f63de-129">Summary</span></span>                                                                                                                                                          |
|-------------------------------------------|--------------------|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f63de-130">\_Optionname\_</span><span class="sxs-lookup"><span data-stu-id="f63de-130">\_OptionName\_</span></span><br/>                 | <span data-ttu-id="f63de-131">string</span><span class="sxs-lookup"><span data-stu-id="f63de-131">string</span></span><br/>  | <span data-ttu-id="f63de-132">characters</span><span class="sxs-lookup"><span data-stu-id="f63de-132">characters</span></span><br/> | <span data-ttu-id="f63de-133">Nome totalmente qualificado válido, conforme definido [por Namespaces em XML.](https://www.w3.org/TR/1999/REC-xml-names-19990114/)</span><span class="sxs-lookup"><span data-stu-id="f63de-133">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="f63de-134">Se nenhum namespace for especificado, o namespace padrão será assumido.</span><span class="sxs-lookup"><span data-stu-id="f63de-134">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="f63de-135">O nome da opção.</span><span class="sxs-lookup"><span data-stu-id="f63de-135">The name of the option.</span></span><br/>                                                                                                                               |
| <span data-ttu-id="f63de-136">\_IdentityOptionValue\_</span><span class="sxs-lookup"><span data-stu-id="f63de-136">\_IdentityOptionValue\_</span></span><br/>        | <span data-ttu-id="f63de-137">string</span><span class="sxs-lookup"><span data-stu-id="f63de-137">string</span></span><br/>  | <span data-ttu-id="f63de-138">n/d</span><span class="sxs-lookup"><span data-stu-id="f63de-138">n/a</span></span><br/>        | <span data-ttu-id="f63de-139">True, False.</span><span class="sxs-lookup"><span data-stu-id="f63de-139">True, False.</span></span><br/>                                                                                                                                                               | <span data-ttu-id="f63de-140">Define uma Opção que, quando selecionada, desabilitará esse recurso.</span><span class="sxs-lookup"><span data-stu-id="f63de-140">Defines an Option which when selected would disable this feature.</span></span><br/>                                                                                     |
| <span data-ttu-id="f63de-141">\_ResolutionXValue\_</span><span class="sxs-lookup"><span data-stu-id="f63de-141">\_ResolutionXValue\_</span></span><br/>           | <span data-ttu-id="f63de-142">Número inteiro</span><span class="sxs-lookup"><span data-stu-id="f63de-142">integer</span></span><br/> | <span data-ttu-id="f63de-143">Dpi</span><span class="sxs-lookup"><span data-stu-id="f63de-143">DPI</span></span><br/>        | <span data-ttu-id="f63de-144">Maior que 0.</span><span class="sxs-lookup"><span data-stu-id="f63de-144">Greater than 0.</span></span><br/>                                                                                                                                                            | <span data-ttu-id="f63de-145">Especifica o componente x da resolução em relação ao PageImageableSize no DPI (em relação à direção pageMediaSize e feed da mídia).</span><span class="sxs-lookup"><span data-stu-id="f63de-145">Specifies the x component of the resolution relative to the PageImageableSize in DPI (relative to the PageMediaSize and feed direction of the media).</span></span><br/> |
| <span data-ttu-id="f63de-146">\_ResolutionYValue\_</span><span class="sxs-lookup"><span data-stu-id="f63de-146">\_ResolutionYValue\_</span></span><br/>           | <span data-ttu-id="f63de-147">Número inteiro</span><span class="sxs-lookup"><span data-stu-id="f63de-147">integer</span></span><br/> | <span data-ttu-id="f63de-148">Dpi</span><span class="sxs-lookup"><span data-stu-id="f63de-148">DPI</span></span><br/>        | <span data-ttu-id="f63de-149">Maior que 0.</span><span class="sxs-lookup"><span data-stu-id="f63de-149">Greater than 0.</span></span><br/>                                                                                                                                                            | <span data-ttu-id="f63de-150">Especifica o componente y da resolução em relação ao PageImageableSize no DPI (em relação à direção pageMediaSize e feed da mídia).</span><span class="sxs-lookup"><span data-stu-id="f63de-150">Specifies the y component of the resolution relative to the PageImageableSize in DPI (relative to the PageMediaSize and feed direction of the media).</span></span><br/> |
| <span data-ttu-id="f63de-151">\_QualitativeResolutionValue\_</span><span class="sxs-lookup"><span data-stu-id="f63de-151">\_QualitativeResolutionValue\_</span></span><br/> | <span data-ttu-id="f63de-152">string</span><span class="sxs-lookup"><span data-stu-id="f63de-152">string</span></span><br/>  | <span data-ttu-id="f63de-153">n/d</span><span class="sxs-lookup"><span data-stu-id="f63de-153">n/a</span></span><br/>        | <span data-ttu-id="f63de-154">Padrão, Rascunho, Alto, Normal, Outros.</span><span class="sxs-lookup"><span data-stu-id="f63de-154">Default, Draft, High, Normal, Other.</span></span><br/>                                                                                                                                       | <span data-ttu-id="f63de-155">Especifica um rótulo de qualidade para a resolução.</span><span class="sxs-lookup"><span data-stu-id="f63de-155">Specifies a quality label for the resolution.</span></span><br/>                                                                                                         |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="f63de-156">linguagem XML conteúdo (XML)</span><span class="sxs-lookup"><span data-stu-id="f63de-156">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="f63de-157">As palavras-chave public Print Schema são definidas no https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace .</span><span class="sxs-lookup"><span data-stu-id="f63de-157">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="f63de-158">O conteúdo linguagem XML XML (public linguagem XML) para essa palavra-chave é definido abaixo:</span><span class="sxs-lookup"><span data-stu-id="f63de-158">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

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

## <a name="related-topics"></a><span data-ttu-id="f63de-159">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="f63de-159">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f63de-160">Especificação de esquema de impressão</span><span class="sxs-lookup"><span data-stu-id="f63de-160">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




