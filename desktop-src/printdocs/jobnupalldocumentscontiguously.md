---
description: Saiba mais sobre o elemento JobNUpAllDocumentsContiguously, que descreve a saída de várias páginas lógicas para uma única folha física.
ms.assetid: e73e1736-9be5-4831-8277-23a62658b7b5
title: JobNUpAllDocumentsContiguously
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9106259c80a7efb89cc4481780bfb55af4f07e23
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/19/2021
ms.locfileid: "112408859"
---
# <a name="jobnupalldocumentscontiguously"></a><span data-ttu-id="65592-103">JobNUpAllDocumentsContiguously</span><span class="sxs-lookup"><span data-stu-id="65592-103">JobNUpAllDocumentsContiguously</span></span>

<span data-ttu-id="65592-104">Este tópico não é atual.</span><span class="sxs-lookup"><span data-stu-id="65592-104">This topic is not current.</span></span> <span data-ttu-id="65592-105">Para obter as informações mais atuais, consulte a [especificação do esquema de impressão](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="65592-105">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="65592-106">Descreve a saída de várias páginas lógicas para uma única folha física.</span><span class="sxs-lookup"><span data-stu-id="65592-106">Describes the output of multiple logical pages to a single physical sheet.</span></span> <span data-ttu-id="65592-107">Todos os documentos no trabalho são compilados em conjunto de forma contígua.</span><span class="sxs-lookup"><span data-stu-id="65592-107">All documents in the job are compiled together contiguously.</span></span> <span data-ttu-id="65592-108">JobNUpAllDocumentsContiguously e DocumentNUp são mutuamente exclusivos.</span><span class="sxs-lookup"><span data-stu-id="65592-108">JobNUpAllDocumentsContiguously and DocumentNUp are mutually exclusive.</span></span> <span data-ttu-id="65592-109">Cabe ao driver determinar o tratamento de restrições entre essas palavras-chave.</span><span class="sxs-lookup"><span data-stu-id="65592-109">It is up to the driver to determine constraint handling between these keywords.</span></span>

<span data-ttu-id="65592-110">O diagrama a seguir ilustra um exemplo com o documento 1 contendo 3 páginas e o documento 2 contendo 2 páginas.</span><span class="sxs-lookup"><span data-stu-id="65592-110">The following diagram illustrates an example with Document 1 containing 3 pages, and Document 2 containing 2 pages.</span></span> <span data-ttu-id="65592-111">Cada documento no trabalho fica duplexado de forma contígua.</span><span class="sxs-lookup"><span data-stu-id="65592-111">Each document in the job is duplexed contiguously.</span></span> <span data-ttu-id="65592-112">As instruções de apresentação mostradas no exemplo são a opção RightBottom.</span><span class="sxs-lookup"><span data-stu-id="65592-112">The presentation directions shown in the example is the RightBottom option.</span></span>

![um diagrama que mostra como as páginas do documento são colocadas em uma única planilha com base na configuração DocumentNUp](images/local-1242234459-jobduplexpics.gif)

-   [<span data-ttu-id="65592-114">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="65592-114">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="65592-115">Conteúdo estrutural</span><span class="sxs-lookup"><span data-stu-id="65592-115">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="65592-116">Conteúdo de linguagem XML (XML)</span><span class="sxs-lookup"><span data-stu-id="65592-116">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="65592-117">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="65592-117">Element Information</span></span>



| <span data-ttu-id="65592-118">Name</span><span class="sxs-lookup"><span data-stu-id="65592-118">Name</span></span> | <span data-ttu-id="65592-119">Valor</span><span class="sxs-lookup"><span data-stu-id="65592-119">Value</span></span> |
|----------------------------|------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="65592-120">Tipo de elemento</span><span class="sxs-lookup"><span data-stu-id="65592-120">Element Type</span></span> <br/>   | <span data-ttu-id="65592-121">Recurso</span><span class="sxs-lookup"><span data-stu-id="65592-121">Feature</span></span><br/>                                                                                                                             |
| <span data-ttu-id="65592-122">Prefixo de escopo</span><span class="sxs-lookup"><span data-stu-id="65592-122">Scoping Prefix</span></span> <br/> | <span data-ttu-id="65592-123">Trabalho</span><span class="sxs-lookup"><span data-stu-id="65592-123">Job</span></span><br/>                                                                                                                                 |
| <span data-ttu-id="65592-124">Observações</span><span class="sxs-lookup"><span data-stu-id="65592-124">Notes</span></span> <br/>          | <span data-ttu-id="65592-125">As partes superior, inferior, esquerda e direita são relativas ao PageImageableSize, em que TopLeft é indicado pela origem da altura e da largura.</span><span class="sxs-lookup"><span data-stu-id="65592-125">Top, Bottom, Left, and Right are relative to the PageImageableSize, where TopLeft is denoted by the origin of the height and width.</span></span><br/> |



 

## <a name="structural-content"></a><span data-ttu-id="65592-126">Conteúdo estrutural</span><span class="sxs-lookup"><span data-stu-id="65592-126">Structural Content</span></span>

<span data-ttu-id="65592-127">A estrutura XML desse elemento é:</span><span class="sxs-lookup"><span data-stu-id="65592-127">The XML structure of this element is:</span></span>

``` syntax
<psf:Feature name="psk:JobNUpAllDocumentsContiguously">
  <psf:Property name="psf:SelectionType">
    <psf:Value xsi:type="xs:string">psk:PickOne</psf:Value>
  </psf:Property>
  <psf:Option name="psk:_OptionName_">
    <psf:Property name="psf:IdentityOption">
      <psf:Value xsi:type="xs:string">_IdentityOptionValue_</psf:Value>
    </psf:Property>
    <psf:ScoredProperty name="psk:PagesPerSheet">
      <psf:Value xsi:type="xs:integer">_PagesPerSheetValue_</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <!-- Specifies the ordering direction of the pages.  First direction followed by second direction. -->
  <psf:Feature name="psk:PresentationDirection">
    <psf:Option name="psk:_PresentationDirectionOptionName_" />
  </psf:Feature>
</psf:Feature>
      
```

## <a name="structure-variables"></a><span data-ttu-id="65592-128">Variáveis de estrutura</span><span class="sxs-lookup"><span data-stu-id="65592-128">Structure Variables</span></span>

<span data-ttu-id="65592-129">A tabela a seguir descreve as características das variáveis definidas na estrutura XML.</span><span class="sxs-lookup"><span data-stu-id="65592-129">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="65592-130">Nome</span><span class="sxs-lookup"><span data-stu-id="65592-130">Name</span></span>                                           | <span data-ttu-id="65592-131">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="65592-131">Data type</span></span>          | <span data-ttu-id="65592-132">Unidade</span><span class="sxs-lookup"><span data-stu-id="65592-132">Unit</span></span>                     | <span data-ttu-id="65592-133">Valores com suporte</span><span class="sxs-lookup"><span data-stu-id="65592-133">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="65592-134">Resumo</span><span class="sxs-lookup"><span data-stu-id="65592-134">Summary</span></span>                                                                                                                              |
|------------------------------------------------|--------------------|--------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="65592-135">\_OptionName\_</span><span class="sxs-lookup"><span data-stu-id="65592-135">\_OptionName\_</span></span><br/>                      | <span data-ttu-id="65592-136">string</span><span class="sxs-lookup"><span data-stu-id="65592-136">string</span></span><br/>  | <span data-ttu-id="65592-137">characters</span><span class="sxs-lookup"><span data-stu-id="65592-137">characters</span></span><br/>    | <span data-ttu-id="65592-138">Nome totalmente qualificado válido, conforme definido pelos [namespaces em XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span><span class="sxs-lookup"><span data-stu-id="65592-138">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="65592-139">Se nenhum namespace for especificado, o namespace padrão será assumido.</span><span class="sxs-lookup"><span data-stu-id="65592-139">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="65592-140">O nome da opção.</span><span class="sxs-lookup"><span data-stu-id="65592-140">The name of the option.</span></span><br/>                                                                                                   |
| <span data-ttu-id="65592-141">\_IdentityOptionValue\_</span><span class="sxs-lookup"><span data-stu-id="65592-141">\_IdentityOptionValue\_</span></span><br/>             | <span data-ttu-id="65592-142">string</span><span class="sxs-lookup"><span data-stu-id="65592-142">string</span></span><br/>  | <span data-ttu-id="65592-143">n/d</span><span class="sxs-lookup"><span data-stu-id="65592-143">n/a</span></span><br/>           | <span data-ttu-id="65592-144">True, False.</span><span class="sxs-lookup"><span data-stu-id="65592-144">True, False.</span></span><br/>                                                                                                                                                               | <span data-ttu-id="65592-145">Define uma opção que, quando selecionada, desabilita esse recurso.</span><span class="sxs-lookup"><span data-stu-id="65592-145">Defines an Option which when selected would disable this feature.</span></span><br/>                                                         |
| <span data-ttu-id="65592-146">\_PagesPerSheetValue\_</span><span class="sxs-lookup"><span data-stu-id="65592-146">\_PagesPerSheetValue\_</span></span><br/>              | <span data-ttu-id="65592-147">Número inteiro</span><span class="sxs-lookup"><span data-stu-id="65592-147">integer</span></span><br/> | <span data-ttu-id="65592-148">Páginas lógicas</span><span class="sxs-lookup"><span data-stu-id="65592-148">Logical pages</span></span><br/> | <span data-ttu-id="65592-149">Todos os inteiros (maiores que zero).</span><span class="sxs-lookup"><span data-stu-id="65592-149">All integers (Greater than zero).</span></span><br/>                                                                                                                                          | <span data-ttu-id="65592-150">Especifica o número de páginas lógicas por folha física.</span><span class="sxs-lookup"><span data-stu-id="65592-150">Specifies the number of logical pages per physical sheet.</span></span> <span data-ttu-id="65592-151">O conjunto com suporte pode ser qualquer conjunto de inteiros, por exemplo,</span><span class="sxs-lookup"><span data-stu-id="65592-151">Supported set can be any set of integers E.g.</span></span> <span data-ttu-id="65592-152">{1,2,4,6,8,9,16}.</span><span class="sxs-lookup"><span data-stu-id="65592-152">{1,2,4,6,8,9,16}.</span></span><br/> |
| <span data-ttu-id="65592-153">\_PresentationDirectionOptionName\_</span><span class="sxs-lookup"><span data-stu-id="65592-153">\_PresentationDirectionOptionName\_</span></span><br/> | <span data-ttu-id="65592-154">string</span><span class="sxs-lookup"><span data-stu-id="65592-154">string</span></span><br/>  | <span data-ttu-id="65592-155">characters</span><span class="sxs-lookup"><span data-stu-id="65592-155">characters</span></span><br/>    | <span data-ttu-id="65592-156">Nome totalmente qualificado válido, conforme definido pelos [namespaces em XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span><span class="sxs-lookup"><span data-stu-id="65592-156">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="65592-157">Se nenhum namespace for especificado, o namespace padrão será assumido.</span><span class="sxs-lookup"><span data-stu-id="65592-157">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="65592-158">O nome da opção.</span><span class="sxs-lookup"><span data-stu-id="65592-158">The name of the option.</span></span><br/>                                                                                                   |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="65592-159">Conteúdo de linguagem XML (XML)</span><span class="sxs-lookup"><span data-stu-id="65592-159">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="65592-160">As palavras-chave do esquema de impressão pública são definidas no https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span><span class="sxs-lookup"><span data-stu-id="65592-160">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="65592-161">O conteúdo do linguagem XML público (XML) para essa palavra-chave é definido abaixo:</span><span class="sxs-lookup"><span data-stu-id="65592-161">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

``` syntax
<psf:Feature name="psk:JobNUpAllDocumentsContiguously">
  <psf:Property name="psf:SelectionType">
    <psf:Value xsi:type="xs:string">psk:PickOne</psf:Value>
  </psf:Property>
  <psf:Option>
    <psf:ScoredProperty name="psk:PagesPerSheet">
      <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Feature name="psk:PresentationDirection">
    <!-- Specifies left to right, top to bottom. -->
    <psf:Option name="psk:RightBottom" />
    <!-- Specifies top to bottom, left to right. -->
    <psf:Option name="psk:BottomRight" />
    <!-- Specifies right to left, top to bottom. -->
    <psf:Option name="psk:LeftBottom" />
    <!-- Specifies top to bottom, right to left. -->
    <psf:Option name="psk:BottomLeft" />
    <!-- Specifies left to right, bottom to top. -->
    <psf:Option name="psk:RightTop" />
    <!-- Specifies bottom to top, left to right. -->
    <psf:Option name="psk:TopRight" />
    <!-- Specifies right to left, bottom to top. -->
    <psf:Option name="psk:LeftTop" />
    <!-- Specifies bottom to top, right to left. -->
    <psf:Option name="psk:TopLeft" />
  </psf:Feature>
</psf:Feature>
    
```

## <a name="related-topics"></a><span data-ttu-id="65592-162">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="65592-162">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="65592-163">Especificação de esquema de impressão</span><span class="sxs-lookup"><span data-stu-id="65592-163">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




