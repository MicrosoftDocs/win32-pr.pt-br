---
description: Este tópico não é atual. Para obter as informações mais atuais, consulte a especificação do esquema de impressão.
ms.assetid: f21199e2-2220-40c4-9429-72aa2a34a5f2
title: JobBindAllDocuments
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: deff299aa5c8d76c9fb8e904539c287ecc881ee6
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/26/2021
ms.locfileid: "107998443"
---
# <a name="jobbindalldocuments"></a><span data-ttu-id="e1c77-104">JobBindAllDocuments</span><span class="sxs-lookup"><span data-stu-id="e1c77-104">JobBindAllDocuments</span></span>

<span data-ttu-id="e1c77-105">Este tópico não é atual.</span><span class="sxs-lookup"><span data-stu-id="e1c77-105">This topic is not current.</span></span> <span data-ttu-id="e1c77-106">Para obter as informações mais atuais, consulte a [especificação do esquema de impressão](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="e1c77-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="e1c77-107">Descreve o método de associação.</span><span class="sxs-lookup"><span data-stu-id="e1c77-107">Describes the method of binding.</span></span> <span data-ttu-id="e1c77-108">Todos os documentos no trabalho são vinculados em conjunto.</span><span class="sxs-lookup"><span data-stu-id="e1c77-108">All documents in the job are bound together.</span></span> <span data-ttu-id="e1c77-109">JobBindAllDocuments e Documentbinding são mutuamente exclusivos.</span><span class="sxs-lookup"><span data-stu-id="e1c77-109">JobBindAllDocuments and DocumentBinding are mutually exclusive.</span></span> <span data-ttu-id="e1c77-110">Cabe ao driver determinar o tratamento de restrições entre essas palavras-chave.</span><span class="sxs-lookup"><span data-stu-id="e1c77-110">It is up to the driver to determine constraint handling between these keywords.</span></span>

-   [<span data-ttu-id="e1c77-111">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="e1c77-111">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="e1c77-112">Conteúdo estrutural</span><span class="sxs-lookup"><span data-stu-id="e1c77-112">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="e1c77-113">Conteúdo de linguagem XML (XML)</span><span class="sxs-lookup"><span data-stu-id="e1c77-113">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="e1c77-114">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="e1c77-114">Element Information</span></span>



| <span data-ttu-id="e1c77-115">Nome</span><span class="sxs-lookup"><span data-stu-id="e1c77-115">Name</span></span> | <span data-ttu-id="e1c77-116">Valor</span><span class="sxs-lookup"><span data-stu-id="e1c77-116">Value</span></span> |
|----------------------------|--------------------------------------------------------------------------------|
| <span data-ttu-id="e1c77-117">Tipo de elemento</span><span class="sxs-lookup"><span data-stu-id="e1c77-117">Element Type</span></span> <br/>   | <span data-ttu-id="e1c77-118">Recurso</span><span class="sxs-lookup"><span data-stu-id="e1c77-118">Feature</span></span><br/>                                                             |
| <span data-ttu-id="e1c77-119">Prefixo de escopo</span><span class="sxs-lookup"><span data-stu-id="e1c77-119">Scoping Prefix</span></span> <br/> | <span data-ttu-id="e1c77-120">Trabalho</span><span class="sxs-lookup"><span data-stu-id="e1c77-120">Job</span></span><br/>                                                                 |
| <span data-ttu-id="e1c77-121">Observações</span><span class="sxs-lookup"><span data-stu-id="e1c77-121">Notes</span></span> <br/>          | <span data-ttu-id="e1c77-122">Superior, inferior, esquerda e direita são relativos ao PageImageableSize.</span><span class="sxs-lookup"><span data-stu-id="e1c77-122">Top, Bottom, Left, and Right are relative to the PageImageableSize.</span></span><br/> |



 

## <a name="structural-content"></a><span data-ttu-id="e1c77-123">Conteúdo estrutural</span><span class="sxs-lookup"><span data-stu-id="e1c77-123">Structural Content</span></span>

<span data-ttu-id="e1c77-124">A estrutura XML desse elemento é:</span><span class="sxs-lookup"><span data-stu-id="e1c77-124">The XML structure of this element is:</span></span>

``` syntax
<psf:Feature name="psk:JobBindAllDocuments">
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

## <a name="structure-variables"></a><span data-ttu-id="e1c77-125">Variáveis de estrutura</span><span class="sxs-lookup"><span data-stu-id="e1c77-125">Structure Variables</span></span>

<span data-ttu-id="e1c77-126">A tabela a seguir descreve as características das variáveis definidas na estrutura XML.</span><span class="sxs-lookup"><span data-stu-id="e1c77-126">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="e1c77-127">Nome</span><span class="sxs-lookup"><span data-stu-id="e1c77-127">Name</span></span>                               | <span data-ttu-id="e1c77-128">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="e1c77-128">Data type</span></span>          | <span data-ttu-id="e1c77-129">Unidade</span><span class="sxs-lookup"><span data-stu-id="e1c77-129">Unit</span></span>                  | <span data-ttu-id="e1c77-130">Valores com suporte</span><span class="sxs-lookup"><span data-stu-id="e1c77-130">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="e1c77-131">Resumo</span><span class="sxs-lookup"><span data-stu-id="e1c77-131">Summary</span></span>                                                                                                                                                                |
|------------------------------------|--------------------|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e1c77-132">\_OptionName\_</span><span class="sxs-lookup"><span data-stu-id="e1c77-132">\_OptionName\_</span></span><br/>          | <span data-ttu-id="e1c77-133">string</span><span class="sxs-lookup"><span data-stu-id="e1c77-133">string</span></span><br/>  | <span data-ttu-id="e1c77-134">characters</span><span class="sxs-lookup"><span data-stu-id="e1c77-134">characters</span></span><br/> | <span data-ttu-id="e1c77-135">Nome totalmente qualificado válido, conforme definido pelos [namespaces em XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span><span class="sxs-lookup"><span data-stu-id="e1c77-135">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="e1c77-136">Se nenhum namespace for especificado, o namespace padrão será assumido.</span><span class="sxs-lookup"><span data-stu-id="e1c77-136">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="e1c77-137">O nome da opção.</span><span class="sxs-lookup"><span data-stu-id="e1c77-137">The name of the option.</span></span><br/>                                                                                                                                     |
| <span data-ttu-id="e1c77-138">\_IdentityOptionValue\_</span><span class="sxs-lookup"><span data-stu-id="e1c77-138">\_IdentityOptionValue\_</span></span><br/> | <span data-ttu-id="e1c77-139">string</span><span class="sxs-lookup"><span data-stu-id="e1c77-139">string</span></span><br/>  | <span data-ttu-id="e1c77-140">N/D</span><span class="sxs-lookup"><span data-stu-id="e1c77-140">n/a</span></span><br/>        | <span data-ttu-id="e1c77-141">True, False.</span><span class="sxs-lookup"><span data-stu-id="e1c77-141">True, False.</span></span><br/>                                                                                                                                                               | <span data-ttu-id="e1c77-142">Define uma opção que, quando selecionada, desabilita esse recurso.</span><span class="sxs-lookup"><span data-stu-id="e1c77-142">Defines an Option which when selected would disable this feature.</span></span><br/>                                                                                           |
| <span data-ttu-id="e1c77-143">\_BindingGutterValue\_</span><span class="sxs-lookup"><span data-stu-id="e1c77-143">\_BindingGutterValue\_</span></span><br/>  | <span data-ttu-id="e1c77-144">Número inteiro</span><span class="sxs-lookup"><span data-stu-id="e1c77-144">integer</span></span><br/> | <span data-ttu-id="e1c77-145">mícrons</span><span class="sxs-lookup"><span data-stu-id="e1c77-145">microns</span></span><br/>    | <span data-ttu-id="e1c77-146">Maior que 0.</span><span class="sxs-lookup"><span data-stu-id="e1c77-146">Greater than 0.</span></span><br/>                                                                                                                                                            | <span data-ttu-id="e1c77-147">Define a medianiz de associação mínima para a associação de conclusão especificada.</span><span class="sxs-lookup"><span data-stu-id="e1c77-147">Defines minimum binding gutter for the specified finishing binding.</span></span> <span data-ttu-id="e1c77-148">A medianiz é medida em mícrons em relação à borda da dimensão de mídia física.</span><span class="sxs-lookup"><span data-stu-id="e1c77-148">The gutter is measured in microns relative to the edge of the physical media dimension.</span></span><br/> |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="e1c77-149">Conteúdo de linguagem XML (XML)</span><span class="sxs-lookup"><span data-stu-id="e1c77-149">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="e1c77-150">As palavras-chave do esquema de impressão pública são definidas no https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span><span class="sxs-lookup"><span data-stu-id="e1c77-150">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="e1c77-151">O conteúdo do linguagem XML público (XML) para essa palavra-chave é definido abaixo:</span><span class="sxs-lookup"><span data-stu-id="e1c77-151">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

``` syntax
<psf:Feature name="psk:JobBindAllDocuments">
  <psf:Property name="psf:SelectionType">
    <psf:Value xsi:type="xs:string">psk:PickOne</psf:Value>
  </psf:Property>
  <!-- Specifies bale binding. -->
  <psf:Option name="psk:Bale">
    <psf:ScoredProperty name="psk:BindingGutter">
      <psf:ParameterRef name="psk:JobBindAllDocumentsGutter" />
    </psf:ScoredProperty>
  </psf:Option>
  <!-- Specifies binding along the bottom edge. -->
  <psf:Option name="psk:BindBottom">
    <psf:ScoredProperty name="psk:BindingGutter">
      <psf:ParameterRef name="psk:JobBindAllDocumentsGutter" />
    </psf:ScoredProperty>
  </psf:Option>
  <!-- Specifies binding along the left edge. -->
  <psf:Option name="psk:BindLeft">
    <psf:ScoredProperty name="psk:BindingGutter">
      <psf:ParameterRef name="psk:JobBindAllDocumentsGutter" />
    </psf:ScoredProperty>
  </psf:Option>
  <!-- Specifies binding along the right edge. -->
  <psf:Option name="psk:BindRight">
    <psf:ScoredProperty name="psk:BindingGutter">
      <psf:ParameterRef name="psk:JobBindAllDocumentsGutter" />
    </psf:ScoredProperty>
  </psf:Option>
  <!-- Specifies binding along the top edge. -->
  <psf:Option name="psk:BindTop">
    <psf:ScoredProperty name="psk:BindingGutter">
      <psf:ParameterRef name="psk:JobBindAllDocumentsGutter" />
    </psf:ScoredProperty>
  </psf:Option>
  <!-- Specifies booklet binding. -->
  <psf:Option name="psk:Booklet" />
    <psf:ScoredProperty name="psk:BindingGutter">
      <psf:ParameterRef name="psk:JobBindAllDocumentsGutter" />
    </psf:ScoredProperty>
  </psf:Option>
  <!-- Specifies edge stitching along the bottom edge. -->
  <psf:Option name="psk:EdgeStitchBottom">
    <psf:ScoredProperty name="psk:BindingGutter">
      <psf:ParameterRef name="psk:JobBindAllDocumentsGutter" />
    </psf:ScoredProperty>
  </psf:Option>
  <!-- Specifies edge stitching along the left edge. -->
  <psf:Option name="psk:EdgeStitchLeft">
    <psf:ScoredProperty name="psk:BindingGutter">
      <psf:ParameterRef name="psk:JobBindAllDocumentsGutter" />
    </psf:ScoredProperty>
  </psf:Option>
  <!-- Specifies edge stitching along the right edge. -->
  <psf:Option name="psk:EdgeStitchRight">
    <psf:ScoredProperty name="psk:BindingGutter">
      <psf:ParameterRef name="psk:JobBindAllDocumentsGutter" />
    </psf:ScoredProperty>
  </psf:Option>
  <!-- Specifies edge stitching along the top edge. -->
  <psf:Option name="psk:EdgeStitchTop">
    <psf:ScoredProperty name="psk:BindingGutter">
      <psf:ParameterRef name="psk:JobBindAllDocumentsGutter" />
    </psf:ScoredProperty>
  </psf:Option>
  <!-- Specifies a folded binding. -->
  <psf:Option name="psk:Fold" />
    <psf:ScoredProperty name="psk:BindingGutter">
      <psf:ParameterRef name="psk:JobBindAllDocumentsGutter" />
    </psf:ScoredProperty>
  </psf:Option>
  <!-- Specifies jog offset binding. -->
  <psf:Option name="psk:JogOffset" />
    <psf:ScoredProperty name="psk:BindingGutter">
      <psf:ParameterRef name="psk:JobBindAllDocumentsGutter" />
    </psf:ScoredProperty>
  </psf:Option>
  <!-- Specifies trimming binding. -->
  <psf:Option name="psk:Trim" />
    <psf:ScoredProperty name="psk:BindingGutter">
      <psf:ParameterRef name="psk:JobBindAllDocumentsGutter" />
    </psf:ScoredProperty>
  </psf:Option>
  <!-- Specifies no binding. -->
  <psf:Option name="psk:None" />
</psf:Feature>
```

## <a name="related-topics"></a><span data-ttu-id="e1c77-152">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="e1c77-152">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e1c77-153">Especificação de esquema de impressão</span><span class="sxs-lookup"><span data-stu-id="e1c77-153">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




