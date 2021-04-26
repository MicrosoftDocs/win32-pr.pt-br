---
description: Este tópico não é atual. Para obter as informações mais atuais, consulte a especificação do esquema de impressão.
ms.assetid: 78eb3119-a52f-4ff8-83bb-903e181c8a11
title: PageInputBin
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f74e75653f7c6cbc6a586b80b3e8217286ce7c36
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/26/2021
ms.locfileid: "107993763"
---
# <a name="pageinputbin"></a><span data-ttu-id="08729-104">PageInputBin</span><span class="sxs-lookup"><span data-stu-id="08729-104">PageInputBin</span></span>

<span data-ttu-id="08729-105">Este tópico não é atual.</span><span class="sxs-lookup"><span data-stu-id="08729-105">This topic is not current.</span></span> <span data-ttu-id="08729-106">Para obter as informações mais atuais, consulte a [especificação do esquema de impressão](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="08729-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="08729-107">Descreve o compartimento de entrada instalado em um dispositivo ou a lista completa de compartimentos com suporte para um dispositivo.</span><span class="sxs-lookup"><span data-stu-id="08729-107">Describes the installed input bin in a device or the full list of supported bins for a device.</span></span> <span data-ttu-id="08729-108">Permite a especificação de compartimento de entrada por página.</span><span class="sxs-lookup"><span data-stu-id="08729-108">Allows specification of input bin on a per page basis.</span></span> <span data-ttu-id="08729-109">As palavras-chave JobInputBin, DocumentInputBin e PageInputBin são mutuamente exclusivas.</span><span class="sxs-lookup"><span data-stu-id="08729-109">The JobInputBin, DocumentInputBin, and PageInputBin keywords are mutually exclusive.</span></span> <span data-ttu-id="08729-110">Ambos não devem ser especificados simultaneamente em um documento de PrintTicket ou recursos de impressão.</span><span class="sxs-lookup"><span data-stu-id="08729-110">Both should not be specified simultaneously in a PrintTicket or Print Capabilities document.</span></span>

-   [<span data-ttu-id="08729-111">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="08729-111">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="08729-112">Conteúdo estrutural</span><span class="sxs-lookup"><span data-stu-id="08729-112">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="08729-113">Conteúdo de linguagem XML (XML)</span><span class="sxs-lookup"><span data-stu-id="08729-113">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="08729-114">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="08729-114">Element Information</span></span>



| <span data-ttu-id="08729-115">Nome</span><span class="sxs-lookup"><span data-stu-id="08729-115">Name</span></span> | <span data-ttu-id="08729-116">Valor</span><span class="sxs-lookup"><span data-stu-id="08729-116">Value</span></span> |
|----------------------------|--------------------|
| <span data-ttu-id="08729-117">Tipo de elemento</span><span class="sxs-lookup"><span data-stu-id="08729-117">Element Type</span></span> <br/>   | <span data-ttu-id="08729-118">Recurso</span><span class="sxs-lookup"><span data-stu-id="08729-118">Feature</span></span><br/> |
| <span data-ttu-id="08729-119">Prefixo de escopo</span><span class="sxs-lookup"><span data-stu-id="08729-119">Scoping Prefix</span></span> <br/> | <span data-ttu-id="08729-120">?</span><span class="sxs-lookup"><span data-stu-id="08729-120">Page</span></span><br/>    |
| <span data-ttu-id="08729-121">Observações</span><span class="sxs-lookup"><span data-stu-id="08729-121">Notes</span></span> <br/>          | <span data-ttu-id="08729-122">Nenhum</span><span class="sxs-lookup"><span data-stu-id="08729-122">None</span></span><br/>    |



 

## <a name="structural-content"></a><span data-ttu-id="08729-123">Conteúdo estrutural</span><span class="sxs-lookup"><span data-stu-id="08729-123">Structural Content</span></span>

<span data-ttu-id="08729-124">A estrutura XML desse elemento é:</span><span class="sxs-lookup"><span data-stu-id="08729-124">The XML structure of this element is:</span></span>

``` syntax
<psf:Feature name="psk:PageInputBin">
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

## <a name="structure-variables"></a><span data-ttu-id="08729-125">Variáveis de estrutura</span><span class="sxs-lookup"><span data-stu-id="08729-125">Structure Variables</span></span>

<span data-ttu-id="08729-126">A tabela a seguir descreve as características das variáveis definidas na estrutura XML.</span><span class="sxs-lookup"><span data-stu-id="08729-126">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="08729-127">Nome</span><span class="sxs-lookup"><span data-stu-id="08729-127">Name</span></span>                                   | <span data-ttu-id="08729-128">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="08729-128">Data type</span></span>          | <span data-ttu-id="08729-129">Unidade</span><span class="sxs-lookup"><span data-stu-id="08729-129">Unit</span></span>                  | <span data-ttu-id="08729-130">Valores com suporte</span><span class="sxs-lookup"><span data-stu-id="08729-130">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="08729-131">Resumo</span><span class="sxs-lookup"><span data-stu-id="08729-131">Summary</span></span>                                                                             |
|----------------------------------------|--------------------|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="08729-132">\_OptionName\_</span><span class="sxs-lookup"><span data-stu-id="08729-132">\_OptionName\_</span></span><br/>              | <span data-ttu-id="08729-133">string</span><span class="sxs-lookup"><span data-stu-id="08729-133">string</span></span><br/>  | <span data-ttu-id="08729-134">characters</span><span class="sxs-lookup"><span data-stu-id="08729-134">characters</span></span><br/> | <span data-ttu-id="08729-135">Nome totalmente qualificado válido, conforme definido pelos [namespaces em XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span><span class="sxs-lookup"><span data-stu-id="08729-135">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="08729-136">Se nenhum namespace for especificado, o namespace padrão será assumido.</span><span class="sxs-lookup"><span data-stu-id="08729-136">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="08729-137">O nome da opção.</span><span class="sxs-lookup"><span data-stu-id="08729-137">The name of the option.</span></span><br/>                                                  |
| <span data-ttu-id="08729-138">\_IdentityOptionValue\_</span><span class="sxs-lookup"><span data-stu-id="08729-138">\_IdentityOptionValue\_</span></span><br/>     | <span data-ttu-id="08729-139">string</span><span class="sxs-lookup"><span data-stu-id="08729-139">string</span></span><br/>  | <span data-ttu-id="08729-140">N/D</span><span class="sxs-lookup"><span data-stu-id="08729-140">n/a</span></span><br/>        | <span data-ttu-id="08729-141">True, False.</span><span class="sxs-lookup"><span data-stu-id="08729-141">True, False.</span></span><br/>                                                                                                                                                               | <span data-ttu-id="08729-142">Define uma opção que, quando selecionada, desabilita esse recurso.</span><span class="sxs-lookup"><span data-stu-id="08729-142">Defines an Option which when selected would disable this feature.</span></span><br/>        |
| <span data-ttu-id="08729-143">\_EnvelopeOptionValue\_</span><span class="sxs-lookup"><span data-stu-id="08729-143">\_EnvelopeOptionValue\_</span></span><br/>     | <span data-ttu-id="08729-144">string</span><span class="sxs-lookup"><span data-stu-id="08729-144">string</span></span><br/>  | <span data-ttu-id="08729-145">N/D</span><span class="sxs-lookup"><span data-stu-id="08729-145">n/a</span></span><br/>        | <span data-ttu-id="08729-146">True, False.</span><span class="sxs-lookup"><span data-stu-id="08729-146">True, False.</span></span><br/>                                                                                                                                                               | <span data-ttu-id="08729-147">Define uma opção que, quando selecionada, desabilita esse recurso.</span><span class="sxs-lookup"><span data-stu-id="08729-147">Defines an Option which when selected would disable this feature.</span></span><br/>        |
| <span data-ttu-id="08729-148">\_BinTypeValue\_</span><span class="sxs-lookup"><span data-stu-id="08729-148">\_BinTypeValue\_</span></span><br/>            | <span data-ttu-id="08729-149">string</span><span class="sxs-lookup"><span data-stu-id="08729-149">string</span></span><br/>  | <span data-ttu-id="08729-150">N/D</span><span class="sxs-lookup"><span data-stu-id="08729-150">n/a</span></span><br/>        | <span data-ttu-id="08729-151">ContinuousFeed, SheetFeed.</span><span class="sxs-lookup"><span data-stu-id="08729-151">ContinuousFeed, SheetFeed.</span></span><br/>                                                                                                                                                 | <span data-ttu-id="08729-152">Especifica o tipo do compartimento.</span><span class="sxs-lookup"><span data-stu-id="08729-152">Specifies the type of the bin.</span></span><br/>                                           |
| <span data-ttu-id="08729-153">\_FeedTypeValue\_</span><span class="sxs-lookup"><span data-stu-id="08729-153">\_FeedTypeValue\_</span></span><br/>           | <span data-ttu-id="08729-154">string</span><span class="sxs-lookup"><span data-stu-id="08729-154">string</span></span><br/>  | <span data-ttu-id="08729-155">N/D</span><span class="sxs-lookup"><span data-stu-id="08729-155">n/a</span></span><br/>        | <span data-ttu-id="08729-156">Automático, manual.</span><span class="sxs-lookup"><span data-stu-id="08729-156">Automatic, Manual.</span></span><br/>                                                                                                                                                         | <span data-ttu-id="08729-157">Especifica o mecanismo de feed do compartimento.</span><span class="sxs-lookup"><span data-stu-id="08729-157">Specifies the feed mechanism of the bin.</span></span><br/>                                 |
| <span data-ttu-id="08729-158">\_MediaCapacityValue\_</span><span class="sxs-lookup"><span data-stu-id="08729-158">\_MediaCapacityValue\_</span></span><br/>      | <span data-ttu-id="08729-159">string</span><span class="sxs-lookup"><span data-stu-id="08729-159">string</span></span><br/>  | <span data-ttu-id="08729-160">N/D</span><span class="sxs-lookup"><span data-stu-id="08729-160">n/a</span></span><br/>        | <span data-ttu-id="08729-161">Alta, padrão.</span><span class="sxs-lookup"><span data-stu-id="08729-161">High, Standard.</span></span><br/>                                                                                                                                                            | <span data-ttu-id="08729-162">Especifica se o compartimento é uma bandeja de alta capacidade (qualitativa).</span><span class="sxs-lookup"><span data-stu-id="08729-162">Specifies whether the bin is a high capacity bin (qualitative).</span></span><br/>          |
| <span data-ttu-id="08729-163">\_MediaSizeAutoSenseValue\_</span><span class="sxs-lookup"><span data-stu-id="08729-163">\_MediaSizeAutoSenseValue\_</span></span><br/> | <span data-ttu-id="08729-164">string</span><span class="sxs-lookup"><span data-stu-id="08729-164">string</span></span><br/>  | <span data-ttu-id="08729-165">N/D</span><span class="sxs-lookup"><span data-stu-id="08729-165">n/a</span></span><br/>        | <span data-ttu-id="08729-166">Com suporte, nenhum.</span><span class="sxs-lookup"><span data-stu-id="08729-166">Supported, None.</span></span><br/>                                                                                                                                                           | <span data-ttu-id="08729-167">Especifica o recurso de detecção automática de tamanho de mídia do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="08729-167">Specifies the media size auto sense capability of device.</span></span><br/>                |
| <span data-ttu-id="08729-168">\_MediaTypeAutoSenseValue\_</span><span class="sxs-lookup"><span data-stu-id="08729-168">\_MediaTypeAutoSenseValue\_</span></span><br/> | <span data-ttu-id="08729-169">string</span><span class="sxs-lookup"><span data-stu-id="08729-169">string</span></span><br/>  | <span data-ttu-id="08729-170">N/D</span><span class="sxs-lookup"><span data-stu-id="08729-170">n/a</span></span><br/>        | <span data-ttu-id="08729-171">Com suporte, nenhum.</span><span class="sxs-lookup"><span data-stu-id="08729-171">Supported, None.</span></span><br/>                                                                                                                                                           | <span data-ttu-id="08729-172">Especifica o recurso de detecção automática de tipo de mídia do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="08729-172">Specifies the media type auto sense capability of device.</span></span><br/>                |
| <span data-ttu-id="08729-173">\_MediaSheetCapacityValue\_</span><span class="sxs-lookup"><span data-stu-id="08729-173">\_MediaSheetCapacityValue\_</span></span><br/> | <span data-ttu-id="08729-174">Número inteiro</span><span class="sxs-lookup"><span data-stu-id="08729-174">integer</span></span><br/> | <span data-ttu-id="08729-175">folhas</span><span class="sxs-lookup"><span data-stu-id="08729-175">sheets</span></span><br/>     | <span data-ttu-id="08729-176">Restrição de inteiro máximo permitida pelo dispositivo.</span><span class="sxs-lookup"><span data-stu-id="08729-176">Maximum integer constraint allowed by device.</span></span><br/>                                                                                                                              | <span data-ttu-id="08729-177">Especifica a capacidade de mídia no número de páginas (nível completo) do compartimento.</span><span class="sxs-lookup"><span data-stu-id="08729-177">Specifies the Media capacity in number of pages (full level) of the bin.</span></span><br/> |
| <span data-ttu-id="08729-178">\_MediaPathValue\_</span><span class="sxs-lookup"><span data-stu-id="08729-178">\_MediaPathValue\_</span></span><br/>          | <span data-ttu-id="08729-179">string</span><span class="sxs-lookup"><span data-stu-id="08729-179">string</span></span><br/>  | <span data-ttu-id="08729-180">N/D</span><span class="sxs-lookup"><span data-stu-id="08729-180">n/a</span></span><br/>        | <span data-ttu-id="08729-181">Direto, Serpentine.</span><span class="sxs-lookup"><span data-stu-id="08729-181">Straight, Serpentine.</span></span><br/>                                                                                                                                                      | <span data-ttu-id="08729-182">Especifica as características do caminho de mídia.</span><span class="sxs-lookup"><span data-stu-id="08729-182">Specifies the characteristics of the media path.</span></span><br/>                         |
| <span data-ttu-id="08729-183">\_FeedFaceValue\_</span><span class="sxs-lookup"><span data-stu-id="08729-183">\_FeedFaceValue\_</span></span><br/>           | <span data-ttu-id="08729-184">string</span><span class="sxs-lookup"><span data-stu-id="08729-184">string</span></span><br/>  | <span data-ttu-id="08729-185">N/D</span><span class="sxs-lookup"><span data-stu-id="08729-185">n/a</span></span><br/>        | <span data-ttu-id="08729-186">Virado, FaceDown</span><span class="sxs-lookup"><span data-stu-id="08729-186">FaceUp, FaceDown</span></span><br/>                                                                                                                                                           | <span data-ttu-id="08729-187">Especifica se a mídia a ser impressa ou face para baixo.</span><span class="sxs-lookup"><span data-stu-id="08729-187">Specifies whether media is to be printed face up or face down.</span></span><br/>           |
| <span data-ttu-id="08729-188">\_FeedDirectionValue\_</span><span class="sxs-lookup"><span data-stu-id="08729-188">\_FeedDirectionValue\_</span></span><br/>      | <span data-ttu-id="08729-189">string</span><span class="sxs-lookup"><span data-stu-id="08729-189">string</span></span><br/>  | <span data-ttu-id="08729-190">N/D</span><span class="sxs-lookup"><span data-stu-id="08729-190">n/a</span></span><br/>        | <span data-ttu-id="08729-191">LongEdgeFirst, ShortEdgeFirst</span><span class="sxs-lookup"><span data-stu-id="08729-191">LongEdgeFirst, ShortEdgeFirst</span></span><br/>                                                                                                                                              | <span data-ttu-id="08729-192">Especifica se a mídia é alimentada pela borda longa ou pela borda curta primeiro.</span><span class="sxs-lookup"><span data-stu-id="08729-192">Specifies whether media is fed long edge first or short edge first.</span></span><br/>      |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="08729-193">Conteúdo de linguagem XML (XML)</span><span class="sxs-lookup"><span data-stu-id="08729-193">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="08729-194">As palavras-chave do esquema de impressão pública são definidas no https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span><span class="sxs-lookup"><span data-stu-id="08729-194">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="08729-195">O conteúdo do linguagem XML público (XML) para essa palavra-chave é definido abaixo:</span><span class="sxs-lookup"><span data-stu-id="08729-195">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

``` syntax
<psf:Feature name="psk:PageInputBin">
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

## <a name="related-topics"></a><span data-ttu-id="08729-196">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="08729-196">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="08729-197">Especificação de esquema de impressão</span><span class="sxs-lookup"><span data-stu-id="08729-197">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




