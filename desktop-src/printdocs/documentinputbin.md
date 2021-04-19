---
description: Este tópico não é atual. Para obter as informações mais atuais, consulte a especificação do esquema de impressão.
ms.assetid: 334503d7-c044-41f7-b6aa-892b002b7a4e
title: DocumentInputBin
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 95a4459f621ac4455a69e891c2eeda6f785b6d8b
ms.sourcegitcommit: 7b8f6151ebe247536304866459b2973276271d4d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/06/2021
ms.locfileid: "105812215"
---
# <a name="documentinputbin"></a><span data-ttu-id="f5cf6-104">DocumentInputBin</span><span class="sxs-lookup"><span data-stu-id="f5cf6-104">DocumentInputBin</span></span>

<span data-ttu-id="f5cf6-105">Este tópico não é atual.</span><span class="sxs-lookup"><span data-stu-id="f5cf6-105">This topic is not current.</span></span> <span data-ttu-id="f5cf6-106">Para obter as informações mais atuais, consulte a [especificação do esquema de impressão](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="f5cf6-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="f5cf6-107">Descreve o compartimento de entrada instalado em um dispositivo ou a lista completa de compartimentos com suporte para um dispositivo.</span><span class="sxs-lookup"><span data-stu-id="f5cf6-107">Describes the installed input bin in a device or the full list of supported bins for a device.</span></span> <span data-ttu-id="f5cf6-108">As palavras-chave JobInputBin, DocumentInputBin e PageInputBin são mutuamente exclusivas.</span><span class="sxs-lookup"><span data-stu-id="f5cf6-108">The JobInputBin, DocumentInputBin, and PageInputBin keywords are mutually exclusive.</span></span> <span data-ttu-id="f5cf6-109">Ambos não devem ser especificados simultaneamente em um documento de PrintTicket ou recursos de impressão.</span><span class="sxs-lookup"><span data-stu-id="f5cf6-109">Both should not be specified simultaneously in a PrintTicket or Print Capabilities document.</span></span>

-   [<span data-ttu-id="f5cf6-110">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="f5cf6-110">Element Information</span></span>](#element-information)

-   [<span data-ttu-id="f5cf6-111">Conteúdo estrutural</span><span class="sxs-lookup"><span data-stu-id="f5cf6-111">Structural Content</span></span>](#structural-content)

-   [<span data-ttu-id="f5cf6-112">Conteúdo XML</span><span class="sxs-lookup"><span data-stu-id="f5cf6-112">XML Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="f5cf6-113">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="f5cf6-113">Element Information</span></span>



| <span data-ttu-id="f5cf6-114">Nome</span><span class="sxs-lookup"><span data-stu-id="f5cf6-114">Name</span></span>                       |                                                                                                                                |
|----------------------------|--------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f5cf6-115">Tipo de elemento</span><span class="sxs-lookup"><span data-stu-id="f5cf6-115">Element Type</span></span> <br/>   | <span data-ttu-id="f5cf6-116">Recurso</span><span class="sxs-lookup"><span data-stu-id="f5cf6-116">Feature</span></span><br/>                                                                                                             |
| <span data-ttu-id="f5cf6-117">Prefixo de escopo</span><span class="sxs-lookup"><span data-stu-id="f5cf6-117">Scoping Prefix</span></span> <br/> | <span data-ttu-id="f5cf6-118">Documento</span><span class="sxs-lookup"><span data-stu-id="f5cf6-118">Document</span></span><br/>                                                                                                            |
| <span data-ttu-id="f5cf6-119">Observações</span><span class="sxs-lookup"><span data-stu-id="f5cf6-119">Notes</span></span> <br/>          | <span data-ttu-id="f5cf6-120">Os compartimentos com suporte que não estão instalados no momento devem ser sinalizados como restritos no documento PrintCapabilities.</span><span class="sxs-lookup"><span data-stu-id="f5cf6-120">Supported bins that are not currently installed should be flagged as constrained in the PrintCapabilities document.</span></span><br/> |



 

## <a name="structural-content"></a><span data-ttu-id="f5cf6-121">Conteúdo estrutural</span><span class="sxs-lookup"><span data-stu-id="f5cf6-121">Structural Content</span></span>

<span data-ttu-id="f5cf6-122">A estrutura XML desse elemento é:</span><span class="sxs-lookup"><span data-stu-id="f5cf6-122">The XML structure of this element is:</span></span>

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

## <a name="structure-variables"></a><span data-ttu-id="f5cf6-123">Variáveis de estrutura</span><span class="sxs-lookup"><span data-stu-id="f5cf6-123">Structure Variables</span></span>

<span data-ttu-id="f5cf6-124">A tabela a seguir descreve as características das variáveis definidas na estrutura XML.</span><span class="sxs-lookup"><span data-stu-id="f5cf6-124">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="f5cf6-125">Nome</span><span class="sxs-lookup"><span data-stu-id="f5cf6-125">Name</span></span>                                   | <span data-ttu-id="f5cf6-126">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="f5cf6-126">Data type</span></span>          | <span data-ttu-id="f5cf6-127">Unidade</span><span class="sxs-lookup"><span data-stu-id="f5cf6-127">Unit</span></span>                  | <span data-ttu-id="f5cf6-128">Valores com suporte</span><span class="sxs-lookup"><span data-stu-id="f5cf6-128">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="f5cf6-129">Resumo</span><span class="sxs-lookup"><span data-stu-id="f5cf6-129">Summary</span></span>                                                                             |
|----------------------------------------|--------------------|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="f5cf6-130">\_OptionName\_</span><span class="sxs-lookup"><span data-stu-id="f5cf6-130">\_OptionName\_</span></span><br/>              | <span data-ttu-id="f5cf6-131">string</span><span class="sxs-lookup"><span data-stu-id="f5cf6-131">string</span></span><br/>  | <span data-ttu-id="f5cf6-132">characters</span><span class="sxs-lookup"><span data-stu-id="f5cf6-132">characters</span></span><br/> | <span data-ttu-id="f5cf6-133">Nome totalmente qualificado válido, conforme definido pelos [namespaces em XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span><span class="sxs-lookup"><span data-stu-id="f5cf6-133">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="f5cf6-134">Se nenhum namespace for especificado, o namespace padrão será assumido.</span><span class="sxs-lookup"><span data-stu-id="f5cf6-134">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="f5cf6-135">O nome da opção.</span><span class="sxs-lookup"><span data-stu-id="f5cf6-135">The name of the option.</span></span><br/>                                                  |
| <span data-ttu-id="f5cf6-136">\_IdentityOptionValue\_</span><span class="sxs-lookup"><span data-stu-id="f5cf6-136">\_IdentityOptionValue\_</span></span><br/>     | <span data-ttu-id="f5cf6-137">string</span><span class="sxs-lookup"><span data-stu-id="f5cf6-137">string</span></span><br/>  | <span data-ttu-id="f5cf6-138">N/D</span><span class="sxs-lookup"><span data-stu-id="f5cf6-138">n/a</span></span><br/>        | <span data-ttu-id="f5cf6-139">True, False.</span><span class="sxs-lookup"><span data-stu-id="f5cf6-139">True, False.</span></span><br/>                                                                                                                                                               | <span data-ttu-id="f5cf6-140">Define uma opção que, quando selecionada, desabilita esse recurso.</span><span class="sxs-lookup"><span data-stu-id="f5cf6-140">Defines an Option which when selected would disable this feature.</span></span><br/>        |
| <span data-ttu-id="f5cf6-141">\_EnvelopeOptionValue\_</span><span class="sxs-lookup"><span data-stu-id="f5cf6-141">\_EnvelopeOptionValue\_</span></span><br/>     | <span data-ttu-id="f5cf6-142">string</span><span class="sxs-lookup"><span data-stu-id="f5cf6-142">string</span></span><br/>  | <span data-ttu-id="f5cf6-143">N/D</span><span class="sxs-lookup"><span data-stu-id="f5cf6-143">n/a</span></span><br/>        | <span data-ttu-id="f5cf6-144">True, False.</span><span class="sxs-lookup"><span data-stu-id="f5cf6-144">True, False.</span></span><br/>                                                                                                                                                               | <span data-ttu-id="f5cf6-145">Define uma opção que, quando selecionada, desabilita esse recurso.</span><span class="sxs-lookup"><span data-stu-id="f5cf6-145">Defines an Option which when selected would disable this feature.</span></span><br/>        |
| <span data-ttu-id="f5cf6-146">\_BinTypeValue\_</span><span class="sxs-lookup"><span data-stu-id="f5cf6-146">\_BinTypeValue\_</span></span><br/>            | <span data-ttu-id="f5cf6-147">string</span><span class="sxs-lookup"><span data-stu-id="f5cf6-147">string</span></span><br/>  | <span data-ttu-id="f5cf6-148">N/D</span><span class="sxs-lookup"><span data-stu-id="f5cf6-148">n/a</span></span><br/>        | <span data-ttu-id="f5cf6-149">ContinuousFeed, SheetFeed.</span><span class="sxs-lookup"><span data-stu-id="f5cf6-149">ContinuousFeed, SheetFeed.</span></span><br/>                                                                                                                                                 | <span data-ttu-id="f5cf6-150">Especifica o tipo do compartimento.</span><span class="sxs-lookup"><span data-stu-id="f5cf6-150">Specifies the type of the bin.</span></span><br/>                                           |
| <span data-ttu-id="f5cf6-151">\_FeedTypeValue\_</span><span class="sxs-lookup"><span data-stu-id="f5cf6-151">\_FeedTypeValue\_</span></span><br/>           | <span data-ttu-id="f5cf6-152">string</span><span class="sxs-lookup"><span data-stu-id="f5cf6-152">string</span></span><br/>  | <span data-ttu-id="f5cf6-153">N/D</span><span class="sxs-lookup"><span data-stu-id="f5cf6-153">n/a</span></span><br/>        | <span data-ttu-id="f5cf6-154">Automático, manual.</span><span class="sxs-lookup"><span data-stu-id="f5cf6-154">Automatic, Manual.</span></span><br/>                                                                                                                                                         | <span data-ttu-id="f5cf6-155">Especifica o mecanismo de feed do compartimento.</span><span class="sxs-lookup"><span data-stu-id="f5cf6-155">Specifies the feed mechanism of the bin.</span></span><br/>                                 |
| <span data-ttu-id="f5cf6-156">\_MediaCapacityValue\_</span><span class="sxs-lookup"><span data-stu-id="f5cf6-156">\_MediaCapacityValue\_</span></span><br/>      | <span data-ttu-id="f5cf6-157">Número inteiro</span><span class="sxs-lookup"><span data-stu-id="f5cf6-157">integer</span></span><br/> | <span data-ttu-id="f5cf6-158">folhas</span><span class="sxs-lookup"><span data-stu-id="f5cf6-158">sheets</span></span><br/>     | <span data-ttu-id="f5cf6-159">Restrição de inteiro máximo permitida pelo dispositivo.</span><span class="sxs-lookup"><span data-stu-id="f5cf6-159">Maximum integer constraint allowed by device.</span></span><br/>                                                                                                                              | <span data-ttu-id="f5cf6-160">Especifica se o compartimento é uma bandeja de alta capacidade (qualitativa).</span><span class="sxs-lookup"><span data-stu-id="f5cf6-160">Specifies whether the bin is a high capacity bin (qualitative).</span></span><br/>          |
| <span data-ttu-id="f5cf6-161">\_MediaSizeAutoSenseValue\_</span><span class="sxs-lookup"><span data-stu-id="f5cf6-161">\_MediaSizeAutoSenseValue\_</span></span><br/> | <span data-ttu-id="f5cf6-162">string</span><span class="sxs-lookup"><span data-stu-id="f5cf6-162">string</span></span><br/>  | <span data-ttu-id="f5cf6-163">N/D</span><span class="sxs-lookup"><span data-stu-id="f5cf6-163">n/a</span></span><br/>        | <span data-ttu-id="f5cf6-164">Com suporte, nenhum.</span><span class="sxs-lookup"><span data-stu-id="f5cf6-164">Supported, None.</span></span><br/>                                                                                                                                                           | <span data-ttu-id="f5cf6-165">Especifica o recurso de detecção automática de tamanho de mídia do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="f5cf6-165">Specifies the media size auto sense capability of the device.</span></span><br/>            |
| <span data-ttu-id="f5cf6-166">\_MediaTypeAutoSenseValue\_</span><span class="sxs-lookup"><span data-stu-id="f5cf6-166">\_MediaTypeAutoSenseValue\_</span></span><br/> | <span data-ttu-id="f5cf6-167">string</span><span class="sxs-lookup"><span data-stu-id="f5cf6-167">string</span></span><br/>  | <span data-ttu-id="f5cf6-168">N/D</span><span class="sxs-lookup"><span data-stu-id="f5cf6-168">n/a</span></span><br/>        | <span data-ttu-id="f5cf6-169">Com suporte, nenhum.</span><span class="sxs-lookup"><span data-stu-id="f5cf6-169">Supported, None.</span></span><br/>                                                                                                                                                           | <span data-ttu-id="f5cf6-170">Especifica a capacidade de mídia no número de páginas (nível completo) do compartimento.</span><span class="sxs-lookup"><span data-stu-id="f5cf6-170">Specifies the media capacity in number of pages (full level) of the bin.</span></span><br/> |
| <span data-ttu-id="f5cf6-171">\_MediaPathValue\_</span><span class="sxs-lookup"><span data-stu-id="f5cf6-171">\_MediaPathValue\_</span></span><br/>          | <span data-ttu-id="f5cf6-172">string</span><span class="sxs-lookup"><span data-stu-id="f5cf6-172">string</span></span><br/>  | <span data-ttu-id="f5cf6-173">N/D</span><span class="sxs-lookup"><span data-stu-id="f5cf6-173">n/a</span></span><br/>        | <span data-ttu-id="f5cf6-174">Direto, Serpentine.</span><span class="sxs-lookup"><span data-stu-id="f5cf6-174">Straight, Serpentine.</span></span><br/>                                                                                                                                                      | <span data-ttu-id="f5cf6-175">Especifica as características do caminho de mídia.</span><span class="sxs-lookup"><span data-stu-id="f5cf6-175">Specifies the characteristics of the media path.</span></span><br/>                         |
| <span data-ttu-id="f5cf6-176">\_FeedFaceValue\_</span><span class="sxs-lookup"><span data-stu-id="f5cf6-176">\_FeedFaceValue\_</span></span><br/>           | <span data-ttu-id="f5cf6-177">string</span><span class="sxs-lookup"><span data-stu-id="f5cf6-177">string</span></span><br/>  | <span data-ttu-id="f5cf6-178">N/D</span><span class="sxs-lookup"><span data-stu-id="f5cf6-178">n/a</span></span><br/>        | <span data-ttu-id="f5cf6-179">Virado, FaceDown</span><span class="sxs-lookup"><span data-stu-id="f5cf6-179">FaceUp, FaceDown</span></span><br/>                                                                                                                                                           | <span data-ttu-id="f5cf6-180">Especifica se a mídia a ser impressa ou face para baixo.</span><span class="sxs-lookup"><span data-stu-id="f5cf6-180">Specifies whether media is to be printed face up or face down.</span></span><br/>           |
| <span data-ttu-id="f5cf6-181">\_FeedDirectionValue\_</span><span class="sxs-lookup"><span data-stu-id="f5cf6-181">\_FeedDirectionValue\_</span></span><br/>      | <span data-ttu-id="f5cf6-182">string</span><span class="sxs-lookup"><span data-stu-id="f5cf6-182">string</span></span><br/>  | <span data-ttu-id="f5cf6-183">N/D</span><span class="sxs-lookup"><span data-stu-id="f5cf6-183">n/a</span></span><br/>        | <span data-ttu-id="f5cf6-184">LongEdgeFirst, ShortEdgeFirst</span><span class="sxs-lookup"><span data-stu-id="f5cf6-184">LongEdgeFirst, ShortEdgeFirst</span></span><br/>                                                                                                                                              | <span data-ttu-id="f5cf6-185">Especifica se a mídia é alimentada pela borda longa ou pela borda curta primeiro.</span><span class="sxs-lookup"><span data-stu-id="f5cf6-185">Specifies whether media is fed long edge first or short edge first.</span></span><br/>      |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="f5cf6-186">Conteúdo de linguagem XML (XML)</span><span class="sxs-lookup"><span data-stu-id="f5cf6-186">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="f5cf6-187">As palavras-chave do esquema de impressão pública são definidas no https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span><span class="sxs-lookup"><span data-stu-id="f5cf6-187">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="f5cf6-188">O conteúdo do linguagem XML público (XML) para essa palavra-chave é definido abaixo:</span><span class="sxs-lookup"><span data-stu-id="f5cf6-188">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

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

## <a name="related-topics"></a><span data-ttu-id="f5cf6-189">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="f5cf6-189">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f5cf6-190">Especificação de esquema de impressão</span><span class="sxs-lookup"><span data-stu-id="f5cf6-190">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




