---
description: Este tópico não é atual. Para obter as informações mais atuais, consulte a especificação do esquema de impressão.
ms.assetid: 941515a8-ba3f-47b9-9f3f-08a48122661a
title: DocumentNUp
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 08fdf22fa557ce1da4fde20ad1d8ea14625a1b77
ms.sourcegitcommit: 7b8f6151ebe247536304866459b2973276271d4d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/06/2021
ms.locfileid: "104172595"
---
# <a name="documentnup"></a><span data-ttu-id="c7cdd-104">DocumentNUp</span><span class="sxs-lookup"><span data-stu-id="c7cdd-104">DocumentNUp</span></span>

<span data-ttu-id="c7cdd-105">Este tópico não é atual.</span><span class="sxs-lookup"><span data-stu-id="c7cdd-105">This topic is not current.</span></span> <span data-ttu-id="c7cdd-106">Para obter as informações mais atuais, consulte a [especificação do esquema de impressão](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="c7cdd-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="c7cdd-107">Descreve a saída e o formato de várias páginas lógicas para uma única folha física.</span><span class="sxs-lookup"><span data-stu-id="c7cdd-107">Describes the output and format of multiple logical pages to a single physical sheet.</span></span> <span data-ttu-id="c7cdd-108">Cada documento é compilado separadamente.</span><span class="sxs-lookup"><span data-stu-id="c7cdd-108">Each document is compiled separately.</span></span> <span data-ttu-id="c7cdd-109">DocumentNUp e JobNUpAllDocumentsContiguously são mutuamente exclusivos.</span><span class="sxs-lookup"><span data-stu-id="c7cdd-109">DocumentNUp and JobNUpAllDocumentsContiguously are mutually exclusive.</span></span> <span data-ttu-id="c7cdd-110">Cabe ao driver determinar o tratamento de restrições entre essas palavras-chave.</span><span class="sxs-lookup"><span data-stu-id="c7cdd-110">It is up to the driver to determine constraint handling between these keywords.</span></span>

<span data-ttu-id="c7cdd-111">O diagrama a seguir ilustra um exemplo com o documento 1 contendo 3 páginas e o documento 2 contendo 2 páginas.</span><span class="sxs-lookup"><span data-stu-id="c7cdd-111">The following diagram illustrates an example with Document 1 containing 3 pages, and Document 2 containing 2 pages.</span></span> <span data-ttu-id="c7cdd-112">Cada documento fica duplexado separadamente.</span><span class="sxs-lookup"><span data-stu-id="c7cdd-112">Each document is duplexed separately.</span></span> <span data-ttu-id="c7cdd-113">A direção da apresentação mostrada abaixo é a opção RightBottom.</span><span class="sxs-lookup"><span data-stu-id="c7cdd-113">The presentation direction shown below is the RightBottom option.</span></span>

![um diagrama que mostra como as páginas do documento são colocadas em uma única planilha com base na configuração DocumentNUp](images/local-1663869164-docduplex1.gif)

-   [<span data-ttu-id="c7cdd-115">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="c7cdd-115">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="c7cdd-116">Conteúdo estrutural</span><span class="sxs-lookup"><span data-stu-id="c7cdd-116">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="c7cdd-117">Conteúdo de linguagem XML (XML)</span><span class="sxs-lookup"><span data-stu-id="c7cdd-117">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="c7cdd-118">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="c7cdd-118">Element Information</span></span>



| <span data-ttu-id="c7cdd-119">Nome</span><span class="sxs-lookup"><span data-stu-id="c7cdd-119">Name</span></span>                       |                                                                                                                                                 |
|----------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c7cdd-120">Tipo de elemento</span><span class="sxs-lookup"><span data-stu-id="c7cdd-120">Element Type</span></span> <br/>   | <span data-ttu-id="c7cdd-121">Recurso</span><span class="sxs-lookup"><span data-stu-id="c7cdd-121">Feature</span></span><br/>                                                                                                                              |
| <span data-ttu-id="c7cdd-122">Prefixo de escopo</span><span class="sxs-lookup"><span data-stu-id="c7cdd-122">Scoping Prefix</span></span> <br/> | <span data-ttu-id="c7cdd-123">Documento</span><span class="sxs-lookup"><span data-stu-id="c7cdd-123">Document</span></span><br/>                                                                                                                             |
| <span data-ttu-id="c7cdd-124">Observações</span><span class="sxs-lookup"><span data-stu-id="c7cdd-124">Notes</span></span> <br/>          | <span data-ttu-id="c7cdd-125">Superior, inferior, esquerda e direita são relativos ao PageImageableSize, em que TopLeft é indicado pela origem do eixo x e eixo y.</span><span class="sxs-lookup"><span data-stu-id="c7cdd-125">Top, Bottom, Left, and Right are relative to the PageImageableSize, where TopLeft is denoted by the origin of the x-axis and y-axis.</span></span><br/> |



 

## <a name="structural-content"></a><span data-ttu-id="c7cdd-126">Conteúdo estrutural</span><span class="sxs-lookup"><span data-stu-id="c7cdd-126">Structural Content</span></span>

<span data-ttu-id="c7cdd-127">A estrutura XML desse elemento é a seguinte:</span><span class="sxs-lookup"><span data-stu-id="c7cdd-127">The XML structure of this element is as follows:</span></span>

``` syntax
<psf:Feature name="psk:DocumentNUp">
  <psf:Property name="psf:SelectionType">
    <psf:Value xsi:type="xs:string">psk:PickOne</psf:Value>
  </psf:Property>
  <psf:Option>
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

## <a name="structure-variables"></a><span data-ttu-id="c7cdd-128">Variáveis de estrutura</span><span class="sxs-lookup"><span data-stu-id="c7cdd-128">Structure Variables</span></span>

<span data-ttu-id="c7cdd-129">A tabela a seguir descreve as características das variáveis definidas na estrutura XML.</span><span class="sxs-lookup"><span data-stu-id="c7cdd-129">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="c7cdd-130">Nome</span><span class="sxs-lookup"><span data-stu-id="c7cdd-130">Name</span></span>                                           | <span data-ttu-id="c7cdd-131">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="c7cdd-131">Data type</span></span>          | <span data-ttu-id="c7cdd-132">Unidade</span><span class="sxs-lookup"><span data-stu-id="c7cdd-132">Unit</span></span>                     | <span data-ttu-id="c7cdd-133">Valores com suporte</span><span class="sxs-lookup"><span data-stu-id="c7cdd-133">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="c7cdd-134">Resumo</span><span class="sxs-lookup"><span data-stu-id="c7cdd-134">Summary</span></span>                                                                                                                              |
|------------------------------------------------|--------------------|--------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c7cdd-135">\_OptionName\_</span><span class="sxs-lookup"><span data-stu-id="c7cdd-135">\_OptionName\_</span></span><br/>                      | <span data-ttu-id="c7cdd-136">string</span><span class="sxs-lookup"><span data-stu-id="c7cdd-136">string</span></span><br/>  | <span data-ttu-id="c7cdd-137">characters</span><span class="sxs-lookup"><span data-stu-id="c7cdd-137">characters</span></span><br/>    | <span data-ttu-id="c7cdd-138">Nome totalmente qualificado válido, conforme definido pelos [namespaces em XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span><span class="sxs-lookup"><span data-stu-id="c7cdd-138">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="c7cdd-139">Se nenhum namespace for especificado, o namespace padrão será assumido.</span><span class="sxs-lookup"><span data-stu-id="c7cdd-139">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="c7cdd-140">O nome da opção.</span><span class="sxs-lookup"><span data-stu-id="c7cdd-140">The name of the option.</span></span><br/>                                                                                                   |
| <span data-ttu-id="c7cdd-141">\_IdentityOptionValue\_</span><span class="sxs-lookup"><span data-stu-id="c7cdd-141">\_IdentityOptionValue\_</span></span><br/>             | <span data-ttu-id="c7cdd-142">string</span><span class="sxs-lookup"><span data-stu-id="c7cdd-142">string</span></span><br/>  | <span data-ttu-id="c7cdd-143">N/D</span><span class="sxs-lookup"><span data-stu-id="c7cdd-143">n/a</span></span><br/>           | <span data-ttu-id="c7cdd-144">True, False.</span><span class="sxs-lookup"><span data-stu-id="c7cdd-144">True, False.</span></span><br/>                                                                                                                                                               | <span data-ttu-id="c7cdd-145">Define uma opção que, quando selecionada, desabilita esse recurso.</span><span class="sxs-lookup"><span data-stu-id="c7cdd-145">Defines an Option which when selected would disable this feature.</span></span><br/>                                                         |
| <span data-ttu-id="c7cdd-146">\_PagesPerSheetValue\_</span><span class="sxs-lookup"><span data-stu-id="c7cdd-146">\_PagesPerSheetValue\_</span></span><br/>              | <span data-ttu-id="c7cdd-147">Número inteiro</span><span class="sxs-lookup"><span data-stu-id="c7cdd-147">integer</span></span><br/> | <span data-ttu-id="c7cdd-148">Páginas lógicas</span><span class="sxs-lookup"><span data-stu-id="c7cdd-148">Logical pages</span></span><br/> | <span data-ttu-id="c7cdd-149">Todos os inteiros (maiores que zero).</span><span class="sxs-lookup"><span data-stu-id="c7cdd-149">All integers (Greater than Zero).</span></span><br/>                                                                                                                                          | <span data-ttu-id="c7cdd-150">Especifica o número de páginas lógicas por folha física.</span><span class="sxs-lookup"><span data-stu-id="c7cdd-150">Specifies the number of logical pages per physical sheet.</span></span> <span data-ttu-id="c7cdd-151">O conjunto com suporte pode ser qualquer conjunto de inteiros, por exemplo,</span><span class="sxs-lookup"><span data-stu-id="c7cdd-151">Supported set can be any set of integers E.g.</span></span> <span data-ttu-id="c7cdd-152">{1,2,4,6,8,9,16}.</span><span class="sxs-lookup"><span data-stu-id="c7cdd-152">{1,2,4,6,8,9,16}.</span></span><br/> |
| <span data-ttu-id="c7cdd-153">\_PresentationDirectionOptionName\_</span><span class="sxs-lookup"><span data-stu-id="c7cdd-153">\_PresentationDirectionOptionName\_</span></span><br/> | <span data-ttu-id="c7cdd-154">string</span><span class="sxs-lookup"><span data-stu-id="c7cdd-154">string</span></span><br/>  | <span data-ttu-id="c7cdd-155">characters</span><span class="sxs-lookup"><span data-stu-id="c7cdd-155">characters</span></span><br/>    | <span data-ttu-id="c7cdd-156">Nome totalmente qualificado válido, conforme definido pelos [namespaces em XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span><span class="sxs-lookup"><span data-stu-id="c7cdd-156">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="c7cdd-157">Se nenhum namespace for especificado, o namespace padrão será assumido.</span><span class="sxs-lookup"><span data-stu-id="c7cdd-157">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="c7cdd-158">O nome da opção.</span><span class="sxs-lookup"><span data-stu-id="c7cdd-158">The name of the option.</span></span><br/>                                                                                                   |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="c7cdd-159">Conteúdo de linguagem XML (XML)</span><span class="sxs-lookup"><span data-stu-id="c7cdd-159">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="c7cdd-160">As palavras-chave do esquema de impressão pública são definidas no https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span><span class="sxs-lookup"><span data-stu-id="c7cdd-160">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="c7cdd-161">O conteúdo do linguagem XML público (XML) para essa palavra-chave é definido abaixo:</span><span class="sxs-lookup"><span data-stu-id="c7cdd-161">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

``` syntax
<psf:Feature name="psk:DocumentNUp">
  <psf:Property name="psf:SelectionType">
    <psf:Value xsi:type="xs:string">psk:PickOne</psf:Value>
  </psf:Property>
  <psf:Option>
    <psf:ScoredProperty name="psk:PagesPerSheet">
      <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Feature name="psk:PresentationDirection">
    <!-- Specifies format left to right, top to bottom. -->
    <psf:Option name="psk:RightBottom" />
    <!-- Specifies format top to bottom, left to right. -->
    <psf:Option name="psk:BottomRight" />
    <!-- Specifies format right to left, top to bottom. -->
    <psf:Option name="psk:LeftBottom" />
    <!-- Specifies format top to bottom, right to left. -->
    <psf:Option name="psk:BottomLeft" />
    <!-- Specifies format left to right, bottom to top. -->
    <psf:Option name="psk:RightTop" />
    <!-- Specifies format bottom to top, left to right. -->
    <psf:Option name="psk:TopRight" />
    <!-- Specifies format right to left, bottom to top. -->
    <psf:Option name="psk:LeftTop" />
    <!-- Specifies format bottom to top, right to left. -->
    <psf:Option name="psk:TopLeft" />
  </psf:Feature>
</psf:Feature>
    
```

## <a name="related-topics"></a><span data-ttu-id="c7cdd-162">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="c7cdd-162">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c7cdd-163">Especificação de esquema de impressão</span><span class="sxs-lookup"><span data-stu-id="c7cdd-163">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




