---
description: Este tópico não é atual. Para obter as informações mais atuais, consulte a especificação do esquema de impressão.
ms.assetid: 334503d7-c044-41f7-b6aa-892b002b7a4e
title: DocumentInputBin
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 57890492ed5f0b575e6d462351282dd199f34f45
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/26/2021
ms.locfileid: "107997763"
---
# <a name="documentinputbin"></a><span data-ttu-id="a8d58-104">DocumentInputBin</span><span class="sxs-lookup"><span data-stu-id="a8d58-104">DocumentInputBin</span></span>

<span data-ttu-id="a8d58-105">Este tópico não é atual.</span><span class="sxs-lookup"><span data-stu-id="a8d58-105">This topic is not current.</span></span> <span data-ttu-id="a8d58-106">Para obter as informações mais atuais, consulte a [especificação do esquema de impressão](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="a8d58-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="a8d58-107">Descreve o compartimento de entrada instalado em um dispositivo ou a lista completa de compartimentos com suporte para um dispositivo.</span><span class="sxs-lookup"><span data-stu-id="a8d58-107">Describes the installed input bin in a device or the full list of supported bins for a device.</span></span> <span data-ttu-id="a8d58-108">As palavras-chave JobInputBin, DocumentInputBin e PageInputBin são mutuamente exclusivas.</span><span class="sxs-lookup"><span data-stu-id="a8d58-108">The JobInputBin, DocumentInputBin, and PageInputBin keywords are mutually exclusive.</span></span> <span data-ttu-id="a8d58-109">Ambos não devem ser especificados simultaneamente em um documento de PrintTicket ou recursos de impressão.</span><span class="sxs-lookup"><span data-stu-id="a8d58-109">Both should not be specified simultaneously in a PrintTicket or Print Capabilities document.</span></span>

-   [<span data-ttu-id="a8d58-110">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="a8d58-110">Element Information</span></span>](#element-information)

-   [<span data-ttu-id="a8d58-111">Conteúdo estrutural</span><span class="sxs-lookup"><span data-stu-id="a8d58-111">Structural Content</span></span>](#structural-content)

-   [<span data-ttu-id="a8d58-112">Conteúdo XML</span><span class="sxs-lookup"><span data-stu-id="a8d58-112">XML Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="a8d58-113">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="a8d58-113">Element Information</span></span>



| <span data-ttu-id="a8d58-114">Nome</span><span class="sxs-lookup"><span data-stu-id="a8d58-114">Name</span></span> | <span data-ttu-id="a8d58-115">Valor</span><span class="sxs-lookup"><span data-stu-id="a8d58-115">Value</span></span> |
|----------------------------|--------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a8d58-116">Tipo de elemento</span><span class="sxs-lookup"><span data-stu-id="a8d58-116">Element Type</span></span> <br/>   | <span data-ttu-id="a8d58-117">Recurso</span><span class="sxs-lookup"><span data-stu-id="a8d58-117">Feature</span></span><br/>                                                                                                             |
| <span data-ttu-id="a8d58-118">Prefixo de escopo</span><span class="sxs-lookup"><span data-stu-id="a8d58-118">Scoping Prefix</span></span> <br/> | <span data-ttu-id="a8d58-119">Documento</span><span class="sxs-lookup"><span data-stu-id="a8d58-119">Document</span></span><br/>                                                                                                            |
| <span data-ttu-id="a8d58-120">Observações</span><span class="sxs-lookup"><span data-stu-id="a8d58-120">Notes</span></span> <br/>          | <span data-ttu-id="a8d58-121">Os compartimentos com suporte que não estão instalados no momento devem ser sinalizados como restritos no documento PrintCapabilities.</span><span class="sxs-lookup"><span data-stu-id="a8d58-121">Supported bins that are not currently installed should be flagged as constrained in the PrintCapabilities document.</span></span><br/> |



 

## <a name="structural-content"></a><span data-ttu-id="a8d58-122">Conteúdo estrutural</span><span class="sxs-lookup"><span data-stu-id="a8d58-122">Structural Content</span></span>

<span data-ttu-id="a8d58-123">A estrutura XML desse elemento é:</span><span class="sxs-lookup"><span data-stu-id="a8d58-123">The XML structure of this element is:</span></span>

``` syntax
<psf:Feature name="psk:DocumentInputBin">
  <psf:Property name="psf:SelectionType">
    <psf:Value xsi:type="xs:string">psk:PickOne</psf:Value>
  </psf:Property>
  <psf:Option name="psk:_OptionName_">
    <psf:Property name="psf:IdentityOption">
      <psf:Value xsi:type="xs:string">_IdentityOptionValue_</psf:Value>
    </psf:Property>
    <psf:Property name="psf:_EnvelopeOptionValue_">
      <psf:Value xsi:type="xs:string">_EnvelopeOptionValue_</psf:Value>
    </psf:Property>
    <psf:ScoredProperty name="psk:BinType">
      <psf:Value xsi:type="xs:string">_BinTypeValue_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:FeedType">
      <psf:Value xsi:type="xs:string">_FeedTypeValue_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaCapacity">
      <psf:Value xsi:type="xs:string">_MediaCapacityValue_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeAutoSense">
      <psf:Value xsi:type="xs:string">_MediaSizeAutoSenseValue_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaTypeAutoSense">
      <psf:Value xsi:type="xs:string">_MediaTypeAutoSenseValue_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSheetCapacity">
      <psf:Value xsi:type="xs:integer">_MediaSheetCapacityValue_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaPath">
      <psf:Value xsi:type="xs:string">_MediaPathValue_</psf:Value>
    </psf:ScoredProperty>
    <psf:Property name="psk:FeedFace">
      <psf:Value xsi:type="xs:string">_FeedFaceValue_</psf:Value>
    </psf:Property>
    <psf:Property name="psk:FeedDirection">
      <psf:Value xsi:type="xs:string">_FeedDirectionValue_</psf:Value>
    </psf:Property>
  </psf:Option>
</psf:Feature>
```

## <a name="structure-variables"></a><span data-ttu-id="a8d58-124">Variáveis de estrutura</span><span class="sxs-lookup"><span data-stu-id="a8d58-124">Structure Variables</span></span>

<span data-ttu-id="a8d58-125">A tabela a seguir descreve as características das variáveis definidas na estrutura XML.</span><span class="sxs-lookup"><span data-stu-id="a8d58-125">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="a8d58-126">Nome</span><span class="sxs-lookup"><span data-stu-id="a8d58-126">Name</span></span>                                   | <span data-ttu-id="a8d58-127">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="a8d58-127">Data type</span></span>          | <span data-ttu-id="a8d58-128">Unidade</span><span class="sxs-lookup"><span data-stu-id="a8d58-128">Unit</span></span>                  | <span data-ttu-id="a8d58-129">Valores com suporte</span><span class="sxs-lookup"><span data-stu-id="a8d58-129">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="a8d58-130">Resumo</span><span class="sxs-lookup"><span data-stu-id="a8d58-130">Summary</span></span>                                                                             |
|----------------------------------------|--------------------|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="a8d58-131">\_OptionName\_</span><span class="sxs-lookup"><span data-stu-id="a8d58-131">\_OptionName\_</span></span><br/>              | <span data-ttu-id="a8d58-132">string</span><span class="sxs-lookup"><span data-stu-id="a8d58-132">string</span></span><br/>  | <span data-ttu-id="a8d58-133">characters</span><span class="sxs-lookup"><span data-stu-id="a8d58-133">characters</span></span><br/> | <span data-ttu-id="a8d58-134">Nome totalmente qualificado válido, conforme definido pelos [namespaces em XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span><span class="sxs-lookup"><span data-stu-id="a8d58-134">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="a8d58-135">Se nenhum namespace for especificado, o namespace padrão será assumido.</span><span class="sxs-lookup"><span data-stu-id="a8d58-135">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="a8d58-136">O nome da opção.</span><span class="sxs-lookup"><span data-stu-id="a8d58-136">The name of the option.</span></span><br/>                                                  |
| <span data-ttu-id="a8d58-137">\_IdentityOptionValue\_</span><span class="sxs-lookup"><span data-stu-id="a8d58-137">\_IdentityOptionValue\_</span></span><br/>     | <span data-ttu-id="a8d58-138">string</span><span class="sxs-lookup"><span data-stu-id="a8d58-138">string</span></span><br/>  | <span data-ttu-id="a8d58-139">N/D</span><span class="sxs-lookup"><span data-stu-id="a8d58-139">n/a</span></span><br/>        | <span data-ttu-id="a8d58-140">True, False.</span><span class="sxs-lookup"><span data-stu-id="a8d58-140">True, False.</span></span><br/>                                                                                                                                                               | <span data-ttu-id="a8d58-141">Define uma opção que, quando selecionada, desabilita esse recurso.</span><span class="sxs-lookup"><span data-stu-id="a8d58-141">Defines an Option which when selected would disable this feature.</span></span><br/>        |
| <span data-ttu-id="a8d58-142">\_EnvelopeOptionValue\_</span><span class="sxs-lookup"><span data-stu-id="a8d58-142">\_EnvelopeOptionValue\_</span></span><br/>     | <span data-ttu-id="a8d58-143">string</span><span class="sxs-lookup"><span data-stu-id="a8d58-143">string</span></span><br/>  | <span data-ttu-id="a8d58-144">N/D</span><span class="sxs-lookup"><span data-stu-id="a8d58-144">n/a</span></span><br/>        | <span data-ttu-id="a8d58-145">True, False.</span><span class="sxs-lookup"><span data-stu-id="a8d58-145">True, False.</span></span><br/>                                                                                                                                                               | <span data-ttu-id="a8d58-146">Define uma opção que, quando selecionada, desabilita esse recurso.</span><span class="sxs-lookup"><span data-stu-id="a8d58-146">Defines an Option which when selected would disable this feature.</span></span><br/>        |
| <span data-ttu-id="a8d58-147">\_BinTypeValue\_</span><span class="sxs-lookup"><span data-stu-id="a8d58-147">\_BinTypeValue\_</span></span><br/>            | <span data-ttu-id="a8d58-148">string</span><span class="sxs-lookup"><span data-stu-id="a8d58-148">string</span></span><br/>  | <span data-ttu-id="a8d58-149">N/D</span><span class="sxs-lookup"><span data-stu-id="a8d58-149">n/a</span></span><br/>        | <span data-ttu-id="a8d58-150">ContinuousFeed, SheetFeed.</span><span class="sxs-lookup"><span data-stu-id="a8d58-150">ContinuousFeed, SheetFeed.</span></span><br/>                                                                                                                                                 | <span data-ttu-id="a8d58-151">Especifica o tipo do compartimento.</span><span class="sxs-lookup"><span data-stu-id="a8d58-151">Specifies the type of the bin.</span></span><br/>                                           |
| <span data-ttu-id="a8d58-152">\_FeedTypeValue\_</span><span class="sxs-lookup"><span data-stu-id="a8d58-152">\_FeedTypeValue\_</span></span><br/>           | <span data-ttu-id="a8d58-153">string</span><span class="sxs-lookup"><span data-stu-id="a8d58-153">string</span></span><br/>  | <span data-ttu-id="a8d58-154">N/D</span><span class="sxs-lookup"><span data-stu-id="a8d58-154">n/a</span></span><br/>        | <span data-ttu-id="a8d58-155">Automático, manual.</span><span class="sxs-lookup"><span data-stu-id="a8d58-155">Automatic, Manual.</span></span><br/>                                                                                                                                                         | <span data-ttu-id="a8d58-156">Especifica o mecanismo de feed do compartimento.</span><span class="sxs-lookup"><span data-stu-id="a8d58-156">Specifies the feed mechanism of the bin.</span></span><br/>                                 |
| <span data-ttu-id="a8d58-157">\_MediaCapacityValue\_</span><span class="sxs-lookup"><span data-stu-id="a8d58-157">\_MediaCapacityValue\_</span></span><br/>      | <span data-ttu-id="a8d58-158">Número inteiro</span><span class="sxs-lookup"><span data-stu-id="a8d58-158">integer</span></span><br/> | <span data-ttu-id="a8d58-159">folhas</span><span class="sxs-lookup"><span data-stu-id="a8d58-159">sheets</span></span><br/>     | <span data-ttu-id="a8d58-160">Restrição de inteiro máximo permitida pelo dispositivo.</span><span class="sxs-lookup"><span data-stu-id="a8d58-160">Maximum integer constraint allowed by device.</span></span><br/>                                                                                                                              | <span data-ttu-id="a8d58-161">Especifica se o compartimento é uma bandeja de alta capacidade (qualitativa).</span><span class="sxs-lookup"><span data-stu-id="a8d58-161">Specifies whether the bin is a high capacity bin (qualitative).</span></span><br/>          |
| <span data-ttu-id="a8d58-162">\_MediaSizeAutoSenseValue\_</span><span class="sxs-lookup"><span data-stu-id="a8d58-162">\_MediaSizeAutoSenseValue\_</span></span><br/> | <span data-ttu-id="a8d58-163">string</span><span class="sxs-lookup"><span data-stu-id="a8d58-163">string</span></span><br/>  | <span data-ttu-id="a8d58-164">N/D</span><span class="sxs-lookup"><span data-stu-id="a8d58-164">n/a</span></span><br/>        | <span data-ttu-id="a8d58-165">Com suporte, nenhum.</span><span class="sxs-lookup"><span data-stu-id="a8d58-165">Supported, None.</span></span><br/>                                                                                                                                                           | <span data-ttu-id="a8d58-166">Especifica o recurso de detecção automática de tamanho de mídia do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="a8d58-166">Specifies the media size auto sense capability of the device.</span></span><br/>            |
| <span data-ttu-id="a8d58-167">\_MediaTypeAutoSenseValue\_</span><span class="sxs-lookup"><span data-stu-id="a8d58-167">\_MediaTypeAutoSenseValue\_</span></span><br/> | <span data-ttu-id="a8d58-168">string</span><span class="sxs-lookup"><span data-stu-id="a8d58-168">string</span></span><br/>  | <span data-ttu-id="a8d58-169">N/D</span><span class="sxs-lookup"><span data-stu-id="a8d58-169">n/a</span></span><br/>        | <span data-ttu-id="a8d58-170">Com suporte, nenhum.</span><span class="sxs-lookup"><span data-stu-id="a8d58-170">Supported, None.</span></span><br/>                                                                                                                                                           | <span data-ttu-id="a8d58-171">Especifica a capacidade de mídia no número de páginas (nível completo) do compartimento.</span><span class="sxs-lookup"><span data-stu-id="a8d58-171">Specifies the media capacity in number of pages (full level) of the bin.</span></span><br/> |
| <span data-ttu-id="a8d58-172">\_MediaPathValue\_</span><span class="sxs-lookup"><span data-stu-id="a8d58-172">\_MediaPathValue\_</span></span><br/>          | <span data-ttu-id="a8d58-173">string</span><span class="sxs-lookup"><span data-stu-id="a8d58-173">string</span></span><br/>  | <span data-ttu-id="a8d58-174">N/D</span><span class="sxs-lookup"><span data-stu-id="a8d58-174">n/a</span></span><br/>        | <span data-ttu-id="a8d58-175">Direto, Serpentine.</span><span class="sxs-lookup"><span data-stu-id="a8d58-175">Straight, Serpentine.</span></span><br/>                                                                                                                                                      | <span data-ttu-id="a8d58-176">Especifica as características do caminho de mídia.</span><span class="sxs-lookup"><span data-stu-id="a8d58-176">Specifies the characteristics of the media path.</span></span><br/>                         |
| <span data-ttu-id="a8d58-177">\_FeedFaceValue\_</span><span class="sxs-lookup"><span data-stu-id="a8d58-177">\_FeedFaceValue\_</span></span><br/>           | <span data-ttu-id="a8d58-178">string</span><span class="sxs-lookup"><span data-stu-id="a8d58-178">string</span></span><br/>  | <span data-ttu-id="a8d58-179">N/D</span><span class="sxs-lookup"><span data-stu-id="a8d58-179">n/a</span></span><br/>        | <span data-ttu-id="a8d58-180">Virado, FaceDown</span><span class="sxs-lookup"><span data-stu-id="a8d58-180">FaceUp, FaceDown</span></span><br/>                                                                                                                                                           | <span data-ttu-id="a8d58-181">Especifica se a mídia a ser impressa ou face para baixo.</span><span class="sxs-lookup"><span data-stu-id="a8d58-181">Specifies whether media is to be printed face up or face down.</span></span><br/>           |
| <span data-ttu-id="a8d58-182">\_FeedDirectionValue\_</span><span class="sxs-lookup"><span data-stu-id="a8d58-182">\_FeedDirectionValue\_</span></span><br/>      | <span data-ttu-id="a8d58-183">string</span><span class="sxs-lookup"><span data-stu-id="a8d58-183">string</span></span><br/>  | <span data-ttu-id="a8d58-184">N/D</span><span class="sxs-lookup"><span data-stu-id="a8d58-184">n/a</span></span><br/>        | <span data-ttu-id="a8d58-185">LongEdgeFirst, ShortEdgeFirst</span><span class="sxs-lookup"><span data-stu-id="a8d58-185">LongEdgeFirst, ShortEdgeFirst</span></span><br/>                                                                                                                                              | <span data-ttu-id="a8d58-186">Especifica se a mídia é alimentada pela borda longa ou pela borda curta primeiro.</span><span class="sxs-lookup"><span data-stu-id="a8d58-186">Specifies whether media is fed long edge first or short edge first.</span></span><br/>      |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="a8d58-187">Conteúdo de linguagem XML (XML)</span><span class="sxs-lookup"><span data-stu-id="a8d58-187">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="a8d58-188">As palavras-chave do esquema de impressão pública são definidas no https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span><span class="sxs-lookup"><span data-stu-id="a8d58-188">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="a8d58-189">O conteúdo do linguagem XML público (XML) para essa palavra-chave é definido abaixo:</span><span class="sxs-lookup"><span data-stu-id="a8d58-189">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

``` syntax
<psf:Feature name="psk:DocumentInputBin">
  <psf:Property name="psf:SelectionType">
    <psf:Value xsi:type="xs:string">psk:PickOne</psf:Value>
  </psf:Property>
  <!-- Device will automatically choose best option based on configuration -->
  <psf:Option name="psk:AutoSelect">
    <psf:ScoredProperty name="psk:BinType">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:FeedType">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaCapacity">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeAutoSense">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaTypeAutoSense">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSheetCapacity">
      <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaPath">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:Property name="psk:FeedFace">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:Property>
    <psf:Property name="psk:FeedDirection">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:Property>
  </psf:Option>
  <!--Specifies the default manual feed bin -->
  <psf:Option name="psk:Manual">
    <psf:ScoredProperty name="psk:BinType">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:FeedType">
      <psf:Value xsi:type="xs:string">Manual</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaCapacity">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeAutoSense">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaTypeAutoSense">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSheetCapacity">
      <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaPath">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:Property name="psk:FeedFace">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:Property>
    <psf:Property name="psk:FeedDirection">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:Property>
  </psf:Option>
  <!--Specifies the feed bin is a cassette-->
  <psf:Option name="psk:Cassette">
    <psf:ScoredProperty name="psk:BinType">
      <psf:Value xsi:type="xs:string">SheetFeed</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:FeedType">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaCapacity">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeAutoSense">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaTypeAutoSense">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSheetCapacity">
      <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaPath">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:Property name="psk:FeedFace">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:Property>
    <psf:Property name="psk:FeedDirection">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:Property>
  </psf:Option>
  <!--Specifies the feed bin is a tractor-->
  <psf:Option name="psk:Tractor">
    <psf:ScoredProperty name="psk:BinType">
      <psf:Value xsi:type="xs:string">ContinuousFeed</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:FeedType">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaCapacity">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeAutoSense">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaTypeAutoSense">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSheetCapacity">
      <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaPath">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:Property name="psk:FeedFace">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:Property>
    <psf:Property name="psk:FeedDirection">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:Property>
  </psf:Option>
  <!-- Device Input tray for Inkjet Printers -->
  <psf:Option name="psk:AutoSheetFeeder">
    <psf:ScoredProperty name="psk:BinType">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:FeedType">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaCapacity">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeAutoSense">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaTypeAutoSense">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSheetCapacity">
      <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaPath">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:Property name="psk:FeedFace">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:Property>
    <psf:Property name="psk:FeedDirection">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:Property>
  </psf:Option>
</psf:Feature>
```

## <a name="related-topics"></a><span data-ttu-id="a8d58-190">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="a8d58-190">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a8d58-191">Especificação de esquema de impressão</span><span class="sxs-lookup"><span data-stu-id="a8d58-191">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




