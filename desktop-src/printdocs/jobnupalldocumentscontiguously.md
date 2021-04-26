---
description: Este tópico não é atual. Para obter as informações mais atuais, consulte a especificação do esquema de impressão.
ms.assetid: e73e1736-9be5-4831-8277-23a62658b7b5
title: JobNUpAllDocumentsContiguously
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 35f90620ac99bf97e85acb22c723a938c31605bd
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/26/2021
ms.locfileid: "107998083"
---
# <a name="jobnupalldocumentscontiguously"></a><span data-ttu-id="a196a-104">JobNUpAllDocumentsContiguously</span><span class="sxs-lookup"><span data-stu-id="a196a-104">JobNUpAllDocumentsContiguously</span></span>

<span data-ttu-id="a196a-105">Este tópico não é atual.</span><span class="sxs-lookup"><span data-stu-id="a196a-105">This topic is not current.</span></span> <span data-ttu-id="a196a-106">Para obter as informações mais atuais, consulte a [especificação do esquema de impressão](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="a196a-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="a196a-107">Descreve a saída de várias páginas lógicas para uma única folha física.</span><span class="sxs-lookup"><span data-stu-id="a196a-107">Describes the output of multiple logical pages to a single physical sheet.</span></span> <span data-ttu-id="a196a-108">Todos os documentos no trabalho são compilados em conjunto de forma contígua.</span><span class="sxs-lookup"><span data-stu-id="a196a-108">All documents in the job are compiled together contiguously.</span></span> <span data-ttu-id="a196a-109">JobNUpAllDocumentsContiguously e DocumentNUp são mutuamente exclusivos.</span><span class="sxs-lookup"><span data-stu-id="a196a-109">JobNUpAllDocumentsContiguously and DocumentNUp are mutually exclusive.</span></span> <span data-ttu-id="a196a-110">Cabe ao driver determinar o tratamento de restrições entre essas palavras-chave.</span><span class="sxs-lookup"><span data-stu-id="a196a-110">It is up to the driver to determine constraint handling between these keywords.</span></span>

<span data-ttu-id="a196a-111">O diagrama a seguir ilustra um exemplo com o documento 1 contendo 3 páginas e o documento 2 contendo 2 páginas.</span><span class="sxs-lookup"><span data-stu-id="a196a-111">The following diagram illustrates an example with Document 1 containing 3 pages, and Document 2 containing 2 pages.</span></span> <span data-ttu-id="a196a-112">Cada documento no trabalho fica duplexado de forma contígua.</span><span class="sxs-lookup"><span data-stu-id="a196a-112">Each document in the job is duplexed contiguously.</span></span> <span data-ttu-id="a196a-113">As instruções de apresentação mostradas no exemplo são a opção RightBottom.</span><span class="sxs-lookup"><span data-stu-id="a196a-113">The presentation directions shown in the example is the RightBottom option.</span></span>

![um diagrama que mostra como as páginas do documento são colocadas em uma única planilha com base na configuração DocumentNUp](images/local-1242234459-jobduplexpics.gif)

-   [<span data-ttu-id="a196a-115">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="a196a-115">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="a196a-116">Conteúdo estrutural</span><span class="sxs-lookup"><span data-stu-id="a196a-116">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="a196a-117">Conteúdo de linguagem XML (XML)</span><span class="sxs-lookup"><span data-stu-id="a196a-117">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="a196a-118">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="a196a-118">Element Information</span></span>



| <span data-ttu-id="a196a-119">Nome</span><span class="sxs-lookup"><span data-stu-id="a196a-119">Name</span></span> | <span data-ttu-id="a196a-120">Valor</span><span class="sxs-lookup"><span data-stu-id="a196a-120">Value</span></span> |
|----------------------------|------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a196a-121">Tipo de elemento</span><span class="sxs-lookup"><span data-stu-id="a196a-121">Element Type</span></span> <br/>   | <span data-ttu-id="a196a-122">Recurso</span><span class="sxs-lookup"><span data-stu-id="a196a-122">Feature</span></span><br/>                                                                                                                             |
| <span data-ttu-id="a196a-123">Prefixo de escopo</span><span class="sxs-lookup"><span data-stu-id="a196a-123">Scoping Prefix</span></span> <br/> | <span data-ttu-id="a196a-124">Trabalho</span><span class="sxs-lookup"><span data-stu-id="a196a-124">Job</span></span><br/>                                                                                                                                 |
| <span data-ttu-id="a196a-125">Observações</span><span class="sxs-lookup"><span data-stu-id="a196a-125">Notes</span></span> <br/>          | <span data-ttu-id="a196a-126">As partes superior, inferior, esquerda e direita são relativas ao PageImageableSize, em que TopLeft é indicado pela origem da altura e da largura.</span><span class="sxs-lookup"><span data-stu-id="a196a-126">Top, Bottom, Left, and Right are relative to the PageImageableSize, where TopLeft is denoted by the origin of the height and width.</span></span><br/> |



 

## <a name="structural-content"></a><span data-ttu-id="a196a-127">Conteúdo estrutural</span><span class="sxs-lookup"><span data-stu-id="a196a-127">Structural Content</span></span>

<span data-ttu-id="a196a-128">A estrutura XML desse elemento é:</span><span class="sxs-lookup"><span data-stu-id="a196a-128">The XML structure of this element is:</span></span>

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

## <a name="structure-variables"></a><span data-ttu-id="a196a-129">Variáveis de estrutura</span><span class="sxs-lookup"><span data-stu-id="a196a-129">Structure Variables</span></span>

<span data-ttu-id="a196a-130">A tabela a seguir descreve as características das variáveis definidas na estrutura XML.</span><span class="sxs-lookup"><span data-stu-id="a196a-130">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="a196a-131">Nome</span><span class="sxs-lookup"><span data-stu-id="a196a-131">Name</span></span>                                           | <span data-ttu-id="a196a-132">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="a196a-132">Data type</span></span>          | <span data-ttu-id="a196a-133">Unidade</span><span class="sxs-lookup"><span data-stu-id="a196a-133">Unit</span></span>                     | <span data-ttu-id="a196a-134">Valores com suporte</span><span class="sxs-lookup"><span data-stu-id="a196a-134">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="a196a-135">Resumo</span><span class="sxs-lookup"><span data-stu-id="a196a-135">Summary</span></span>                                                                                                                              |
|------------------------------------------------|--------------------|--------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a196a-136">\_OptionName\_</span><span class="sxs-lookup"><span data-stu-id="a196a-136">\_OptionName\_</span></span><br/>                      | <span data-ttu-id="a196a-137">string</span><span class="sxs-lookup"><span data-stu-id="a196a-137">string</span></span><br/>  | <span data-ttu-id="a196a-138">characters</span><span class="sxs-lookup"><span data-stu-id="a196a-138">characters</span></span><br/>    | <span data-ttu-id="a196a-139">Nome totalmente qualificado válido, conforme definido pelos [namespaces em XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span><span class="sxs-lookup"><span data-stu-id="a196a-139">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="a196a-140">Se nenhum namespace for especificado, o namespace padrão será assumido.</span><span class="sxs-lookup"><span data-stu-id="a196a-140">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="a196a-141">O nome da opção.</span><span class="sxs-lookup"><span data-stu-id="a196a-141">The name of the option.</span></span><br/>                                                                                                   |
| <span data-ttu-id="a196a-142">\_IdentityOptionValue\_</span><span class="sxs-lookup"><span data-stu-id="a196a-142">\_IdentityOptionValue\_</span></span><br/>             | <span data-ttu-id="a196a-143">string</span><span class="sxs-lookup"><span data-stu-id="a196a-143">string</span></span><br/>  | <span data-ttu-id="a196a-144">N/D</span><span class="sxs-lookup"><span data-stu-id="a196a-144">n/a</span></span><br/>           | <span data-ttu-id="a196a-145">True, False.</span><span class="sxs-lookup"><span data-stu-id="a196a-145">True, False.</span></span><br/>                                                                                                                                                               | <span data-ttu-id="a196a-146">Define uma opção que, quando selecionada, desabilita esse recurso.</span><span class="sxs-lookup"><span data-stu-id="a196a-146">Defines an Option which when selected would disable this feature.</span></span><br/>                                                         |
| <span data-ttu-id="a196a-147">\_PagesPerSheetValue\_</span><span class="sxs-lookup"><span data-stu-id="a196a-147">\_PagesPerSheetValue\_</span></span><br/>              | <span data-ttu-id="a196a-148">Número inteiro</span><span class="sxs-lookup"><span data-stu-id="a196a-148">integer</span></span><br/> | <span data-ttu-id="a196a-149">Páginas lógicas</span><span class="sxs-lookup"><span data-stu-id="a196a-149">Logical pages</span></span><br/> | <span data-ttu-id="a196a-150">Todos os inteiros (maiores que zero).</span><span class="sxs-lookup"><span data-stu-id="a196a-150">All integers (Greater than zero).</span></span><br/>                                                                                                                                          | <span data-ttu-id="a196a-151">Especifica o número de páginas lógicas por folha física.</span><span class="sxs-lookup"><span data-stu-id="a196a-151">Specifies the number of logical pages per physical sheet.</span></span> <span data-ttu-id="a196a-152">O conjunto com suporte pode ser qualquer conjunto de inteiros, por exemplo,</span><span class="sxs-lookup"><span data-stu-id="a196a-152">Supported set can be any set of integers E.g.</span></span> <span data-ttu-id="a196a-153">{1,2,4,6,8,9,16}.</span><span class="sxs-lookup"><span data-stu-id="a196a-153">{1,2,4,6,8,9,16}.</span></span><br/> |
| <span data-ttu-id="a196a-154">\_PresentationDirectionOptionName\_</span><span class="sxs-lookup"><span data-stu-id="a196a-154">\_PresentationDirectionOptionName\_</span></span><br/> | <span data-ttu-id="a196a-155">string</span><span class="sxs-lookup"><span data-stu-id="a196a-155">string</span></span><br/>  | <span data-ttu-id="a196a-156">characters</span><span class="sxs-lookup"><span data-stu-id="a196a-156">characters</span></span><br/>    | <span data-ttu-id="a196a-157">Nome totalmente qualificado válido, conforme definido pelos [namespaces em XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span><span class="sxs-lookup"><span data-stu-id="a196a-157">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="a196a-158">Se nenhum namespace for especificado, o namespace padrão será assumido.</span><span class="sxs-lookup"><span data-stu-id="a196a-158">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="a196a-159">O nome da opção.</span><span class="sxs-lookup"><span data-stu-id="a196a-159">The name of the option.</span></span><br/>                                                                                                   |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="a196a-160">Conteúdo de linguagem XML (XML)</span><span class="sxs-lookup"><span data-stu-id="a196a-160">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="a196a-161">As palavras-chave do esquema de impressão pública são definidas no https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span><span class="sxs-lookup"><span data-stu-id="a196a-161">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="a196a-162">O conteúdo do linguagem XML público (XML) para essa palavra-chave é definido abaixo:</span><span class="sxs-lookup"><span data-stu-id="a196a-162">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

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

## <a name="related-topics"></a><span data-ttu-id="a196a-163">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="a196a-163">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a196a-164">Especificação de esquema de impressão</span><span class="sxs-lookup"><span data-stu-id="a196a-164">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




