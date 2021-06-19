---
description: Saiba mais sobre o elemento DocumentBinding, que descreve o método de associação. DocumentBinding e JobBindAllDocuments são mutuamente exclusivos.
ms.assetid: 36a7c360-2d26-46b9-b829-0fb35b36c79c
title: DocumentBinding
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bf2b8f44c90cdef37a6599bf25904949748c82ba
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/19/2021
ms.locfileid: "112409459"
---
# <a name="documentbinding"></a><span data-ttu-id="f74fa-104">DocumentBinding</span><span class="sxs-lookup"><span data-stu-id="f74fa-104">DocumentBinding</span></span>

<span data-ttu-id="f74fa-105">Este tópico não é atual.</span><span class="sxs-lookup"><span data-stu-id="f74fa-105">This topic is not current.</span></span> <span data-ttu-id="f74fa-106">Para obter as informações mais atuais, consulte a [Especificação de Esquema de Impressão](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="f74fa-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="f74fa-107">Descreve o método de associação.</span><span class="sxs-lookup"><span data-stu-id="f74fa-107">Describes the method of binding.</span></span> <span data-ttu-id="f74fa-108">Cada documento é vinculado separadamente.</span><span class="sxs-lookup"><span data-stu-id="f74fa-108">Each document is bound separately.</span></span> <span data-ttu-id="f74fa-109">DocumentBinding e JobBindAllDocuments são mutuamente exclusivos.</span><span class="sxs-lookup"><span data-stu-id="f74fa-109">DocumentBinding and JobBindAllDocuments are mutually exclusive.</span></span> <span data-ttu-id="f74fa-110">O driver deve determinar a manipulação de restrição entre palavras-chave.</span><span class="sxs-lookup"><span data-stu-id="f74fa-110">It is up to the driver to determine constraint handling between keywords.</span></span>

-   [<span data-ttu-id="f74fa-111">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="f74fa-111">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="f74fa-112">Conteúdo estrutural</span><span class="sxs-lookup"><span data-stu-id="f74fa-112">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="f74fa-113">linguagem XML conteúdo (XML)</span><span class="sxs-lookup"><span data-stu-id="f74fa-113">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="f74fa-114">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="f74fa-114">Element Information</span></span>



| <span data-ttu-id="f74fa-115">Name</span><span class="sxs-lookup"><span data-stu-id="f74fa-115">Name</span></span> | <span data-ttu-id="f74fa-116">Valor</span><span class="sxs-lookup"><span data-stu-id="f74fa-116">Value</span></span> |
|----------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f74fa-117">Tipo de elemento</span><span class="sxs-lookup"><span data-stu-id="f74fa-117">Element Type</span></span> <br/>   | <span data-ttu-id="f74fa-118">Recurso</span><span class="sxs-lookup"><span data-stu-id="f74fa-118">Feature</span></span><br/>                                                                                                                              |
| <span data-ttu-id="f74fa-119">Prefixo de definição de scoping</span><span class="sxs-lookup"><span data-stu-id="f74fa-119">Scoping Prefix</span></span> <br/> | <span data-ttu-id="f74fa-120">Documento</span><span class="sxs-lookup"><span data-stu-id="f74fa-120">Document</span></span><br/>                                                                                                                             |
| <span data-ttu-id="f74fa-121">Observações</span><span class="sxs-lookup"><span data-stu-id="f74fa-121">Notes</span></span> <br/>          | <span data-ttu-id="f74fa-122">Top, Bottom, Left e Right são relativos ao PageImageableSize, em que TopLeft é anotado pela origem do eixo x e do eixo y.</span><span class="sxs-lookup"><span data-stu-id="f74fa-122">Top, Bottom, Left, and Right are relative to the PageImageableSize, where TopLeft is denoted by the origin of the x-axis and y-axis.</span></span><br/> |



 

## <a name="structural-content"></a><span data-ttu-id="f74fa-123">Conteúdo estrutural</span><span class="sxs-lookup"><span data-stu-id="f74fa-123">Structural Content</span></span>

<span data-ttu-id="f74fa-124">A estrutura XML desse elemento é a seguinte:</span><span class="sxs-lookup"><span data-stu-id="f74fa-124">The XML structure of this element is as follows:</span></span>

``` syntax
<psf:Feature name="psk:DocumentBinding">
  <psf:Property name="psf:SelectionType">
    <psf:Value xsi:type="xs:string">psk:PickOne</psf:Value>
  </psf:Property>
  <psf:Option name="psk:_OptionName_">
    <psf:Property name="psf:IdentityOption">
      <psf:Value xsi:type="xs:string">_IdentityOptionValue_</psf:Value>
    </psf:Property>
    <psf:ScoredProperty name="psk:BindingGutter">
      <psf:Value xsi:type="xs:integer">_BindingGutterValue_</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
</psf:Feature>
```

## <a name="structure-variables"></a><span data-ttu-id="f74fa-125">Variáveis de estrutura</span><span class="sxs-lookup"><span data-stu-id="f74fa-125">Structure Variables</span></span>

<span data-ttu-id="f74fa-126">A tabela a seguir descreve as características das variáveis definidas na estrutura XML.</span><span class="sxs-lookup"><span data-stu-id="f74fa-126">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="f74fa-127">Nome</span><span class="sxs-lookup"><span data-stu-id="f74fa-127">Name</span></span>                               | <span data-ttu-id="f74fa-128">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="f74fa-128">Data type</span></span>          | <span data-ttu-id="f74fa-129">Unidade</span><span class="sxs-lookup"><span data-stu-id="f74fa-129">Unit</span></span>                  | <span data-ttu-id="f74fa-130">Valores com suporte</span><span class="sxs-lookup"><span data-stu-id="f74fa-130">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="f74fa-131">Resumo</span><span class="sxs-lookup"><span data-stu-id="f74fa-131">Summary</span></span>                                                                                                                                                                |
|------------------------------------|--------------------|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f74fa-132">\_Optionname\_</span><span class="sxs-lookup"><span data-stu-id="f74fa-132">\_OptionName\_</span></span><br/>          | <span data-ttu-id="f74fa-133">string</span><span class="sxs-lookup"><span data-stu-id="f74fa-133">string</span></span><br/>  | <span data-ttu-id="f74fa-134">characters</span><span class="sxs-lookup"><span data-stu-id="f74fa-134">characters</span></span><br/> | <span data-ttu-id="f74fa-135">Nome totalmente qualificado válido, conforme definido [por Namespaces em XML.](https://www.w3.org/TR/1999/REC-xml-names-19990114/)</span><span class="sxs-lookup"><span data-stu-id="f74fa-135">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="f74fa-136">Se nenhum namespace for especificado, o namespace padrão será assumido.</span><span class="sxs-lookup"><span data-stu-id="f74fa-136">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="f74fa-137">O nome da opção.</span><span class="sxs-lookup"><span data-stu-id="f74fa-137">The name of the option.</span></span><br/>                                                                                                                                     |
| <span data-ttu-id="f74fa-138">\_IdentityOptionValue\_</span><span class="sxs-lookup"><span data-stu-id="f74fa-138">\_IdentityOptionValue\_</span></span><br/> | <span data-ttu-id="f74fa-139">string</span><span class="sxs-lookup"><span data-stu-id="f74fa-139">string</span></span><br/>  | <span data-ttu-id="f74fa-140">n/d</span><span class="sxs-lookup"><span data-stu-id="f74fa-140">n/a</span></span><br/>        | <span data-ttu-id="f74fa-141">True, False.</span><span class="sxs-lookup"><span data-stu-id="f74fa-141">True, False.</span></span><br/>                                                                                                                                                               | <span data-ttu-id="f74fa-142">Define uma Opção que, quando selecionada, desabilitará esse recurso.</span><span class="sxs-lookup"><span data-stu-id="f74fa-142">Defines an Option which when selected would disable this feature.</span></span><br/>                                                                                           |
| <span data-ttu-id="f74fa-143">\_BindingGutterValue\_</span><span class="sxs-lookup"><span data-stu-id="f74fa-143">\_BindingGutterValue\_</span></span><br/>  | <span data-ttu-id="f74fa-144">Integer</span><span class="sxs-lookup"><span data-stu-id="f74fa-144">Integer</span></span><br/> | <span data-ttu-id="f74fa-145">Mícrons</span><span class="sxs-lookup"><span data-stu-id="f74fa-145">microns</span></span><br/>    | <span data-ttu-id="f74fa-146">Maior ou igual a 0.</span><span class="sxs-lookup"><span data-stu-id="f74fa-146">Greater than or equal to 0.</span></span><br/>                                                                                                                                                | <span data-ttu-id="f74fa-147">Define a mediana de associação mínima para a associação final especificada.</span><span class="sxs-lookup"><span data-stu-id="f74fa-147">Defines minimum binding gutter for the specified finishing binding.</span></span> <span data-ttu-id="f74fa-148">A media mediana é medida em mícronos em relação à borda da dimensão de mídia física.</span><span class="sxs-lookup"><span data-stu-id="f74fa-148">The gutter is measured in microns relative to the edge of the physical media dimension.</span></span><br/> |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="f74fa-149">linguagem XML conteúdo (XML)</span><span class="sxs-lookup"><span data-stu-id="f74fa-149">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="f74fa-150">As palavras-chave public Print Schema são definidas no https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace .</span><span class="sxs-lookup"><span data-stu-id="f74fa-150">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="f74fa-151">O conteúdo linguagem XML XML (public linguagem XML) para essa palavra-chave é definido abaixo:</span><span class="sxs-lookup"><span data-stu-id="f74fa-151">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

``` syntax
<psf:Feature name="psk:DocumentBinding">
  <psf:Property name="psf:SelectionType">
    <psf:Value xsi:type="xs:string">psk:PickOne</psf:Value>
  </psf:Property>
  <!-- Specifies bale binding. -->
  <psf:Option name="psk:Bale" >
    <psf:ScoredProperty name="psk:BindingGutter">
      <psf:ParameterRef name="psk:DocumentBindingGutter" />
    </psf:ScoredProperty>
  </psf:Option>
  <!-- Specifies binding along the bottom edge. -->
  <psf:Option name="psk:BindBottom">
    <psf:ScoredProperty name="psk:BindingGutter">
      <psf:ParameterRef name="psk:DocumentBindingGutter" />
    </psf:ScoredProperty>
  </psf:Option>
  <!-- Specifies binding along the left edge. -->
  <psf:Option name="psk:BindLeft">
    <psf:ScoredProperty name="psk:BindingGutter">
      <psf:ParameterRef name="psk:DocumentBindingGutter" />
    </psf:ScoredProperty>
  </psf:Option>
  <!-- Specifies binding along the right edge. -->
  <psf:Option name="psk:BindRight">
    <psf:ScoredProperty name="psk:BindingGutter">
      <psf:ParameterRef name="psk:DocumentBindingGutter" />
    </psf:ScoredProperty>
  </psf:Option>
  <!-- Specifies binding along the top edge. -->
  <psf:Option name="psk:BindTop">
    <psf:ScoredProperty name="psk:BindingGutter">
      <psf:ParameterRef name="psk:DocumentBindingGutter" />
    </psf:ScoredProperty>
  </psf:Option>
  <!-- Specifies booklet binding. -->
  <psf:Option name="psk:Booklet" />
    <psf:ScoredProperty name="psk:BindingGutter">
      <psf:ParameterRef name="psk:DocumentBindingGutter" />
    </psf:ScoredProperty>
  </psf:Option>
  <!-- Specifies edge stitching along the bottom edge. -->
  <psf:Option name="psk:EdgeStitchBottom">
    <psf:ScoredProperty name="psk:BindingGutter">
      <psf:ParameterRef name="psk:DocumentBindingGutter" />
    </psf:ScoredProperty>
  </psf:Option>
  <!-- Specifies edge stitching along the left edge. -->
  <psf:Option name="psk:EdgeStitchLeft">
    <psf:ScoredProperty name="psk:BindingGutter">
      <psf:ParameterRef name="psk:DocumentBindingGutter" />
    </psf:ScoredProperty>
  </psf:Option>
  <!-- Specifies edge stitching along the right edge. -->
  <psf:Option name="psk:EdgeStitchRight">
    <psf:ScoredProperty name="psk:BindingGutter">
      <psf:ParameterRef name="psk:DocumentBindingGutter" />
    </psf:ScoredProperty>
  </psf:Option>
  <!-- Specifies edge stitching along the top edge. -->
  <psf:Option name="psk:EdgeStitchTop">
    <psf:ScoredProperty name="psk:BindingGutter">
      <psf:ParameterRef name="psk:DocumentBindingGutter" />
    </psf:ScoredProperty>
  </psf:Option>
  <!-- Specifies a folded binding. -->
  <psf:Option name="psk:Fold" />
    <psf:ScoredProperty name="psk:BindingGutter">
      <psf:ParameterRef name="psk:DocumentBindingGutter" />
    </psf:ScoredProperty>
  </psf:Option>
  <!-- Specifies jog offset binding. -->
  <psf:Option name="psk:JogOffset" />
    <psf:ScoredProperty name="psk:BindingGutter">
      <psf:ParameterRef name="psk:DocumentBindingGutter" />
    </psf:ScoredProperty>
  </psf:Option>
  <!-- Specifies trimming binding. -->
  <psf:Option name="psk:Trim" />
    <psf:ScoredProperty name="psk:BindingGutter">
      <psf:ParameterRef name="psk:DocumentBindingGutter" />
    </psf:ScoredProperty>
  </psf:Option>
  <!-- Specifies no binding. -->
  <psf:Option name="psk:None" />
</psf:Feature>
```

## <a name="related-topics"></a><span data-ttu-id="f74fa-152">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="f74fa-152">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f74fa-153">Especificação de esquema de impressão</span><span class="sxs-lookup"><span data-stu-id="f74fa-153">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




