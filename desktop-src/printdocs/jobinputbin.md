---
description: Este tópico não é atual. Para obter as informações mais atuais, consulte a especificação do esquema de impressão.
ms.assetid: 9192ceb1-90c4-480e-9247-68d457976f42
title: JobInputBin
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9e48cb6bc5de419ffdda2e1c352c72623baf3ba9
ms.sourcegitcommit: 7b8f6151ebe247536304866459b2973276271d4d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/06/2021
ms.locfileid: "104172584"
---
# <a name="jobinputbin"></a><span data-ttu-id="1ddba-104">JobInputBin</span><span class="sxs-lookup"><span data-stu-id="1ddba-104">JobInputBin</span></span>

<span data-ttu-id="1ddba-105">Este tópico não é atual.</span><span class="sxs-lookup"><span data-stu-id="1ddba-105">This topic is not current.</span></span> <span data-ttu-id="1ddba-106">Para obter as informações mais atuais, consulte a [especificação do esquema de impressão](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="1ddba-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="1ddba-107">Descreve o compartimento de entrada instalado em um dispositivo ou a lista completa de compartimentos com suporte para um dispositivo.</span><span class="sxs-lookup"><span data-stu-id="1ddba-107">Describes the installed input bin in a device or the full list of supported bins for a device.</span></span> <span data-ttu-id="1ddba-108">Permite a especificação de compartimento de entrada por trabalho.</span><span class="sxs-lookup"><span data-stu-id="1ddba-108">Allows specification of input bin on a per job basis.</span></span> <span data-ttu-id="1ddba-109">As palavras-chave JobInputBin, DocumentInputBin e PageInputBin são mutuamente exclusivas.</span><span class="sxs-lookup"><span data-stu-id="1ddba-109">The JobInputBin, DocumentInputBin, and PageInputBin keywords are mutually exclusive.</span></span> <span data-ttu-id="1ddba-110">Ambos não devem ser especificados simultaneamente em um documento de PrintTicket ou recursos de impressão.</span><span class="sxs-lookup"><span data-stu-id="1ddba-110">Both should not be specified simultaneously in a PrintTicket or Print Capabilities document.</span></span>

-   [<span data-ttu-id="1ddba-111">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="1ddba-111">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="1ddba-112">Conteúdo estrutural</span><span class="sxs-lookup"><span data-stu-id="1ddba-112">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="1ddba-113">Conteúdo de linguagem XML (XML)</span><span class="sxs-lookup"><span data-stu-id="1ddba-113">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="1ddba-114">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="1ddba-114">Element Information</span></span>



| <span data-ttu-id="1ddba-115">Nome</span><span class="sxs-lookup"><span data-stu-id="1ddba-115">Name</span></span>                       |                    |
|----------------------------|--------------------|
| <span data-ttu-id="1ddba-116">Tipo de elemento</span><span class="sxs-lookup"><span data-stu-id="1ddba-116">Element Type</span></span> <br/>   | <span data-ttu-id="1ddba-117">Recurso</span><span class="sxs-lookup"><span data-stu-id="1ddba-117">Feature</span></span><br/> |
| <span data-ttu-id="1ddba-118">Prefixo de escopo</span><span class="sxs-lookup"><span data-stu-id="1ddba-118">Scoping Prefix</span></span> <br/> | <span data-ttu-id="1ddba-119">Trabalho</span><span class="sxs-lookup"><span data-stu-id="1ddba-119">Job</span></span><br/>     |
| <span data-ttu-id="1ddba-120">Observações</span><span class="sxs-lookup"><span data-stu-id="1ddba-120">Notes</span></span> <br/>          | <span data-ttu-id="1ddba-121">Nenhum</span><span class="sxs-lookup"><span data-stu-id="1ddba-121">None</span></span><br/>    |



 

## <a name="structural-content"></a><span data-ttu-id="1ddba-122">Conteúdo estrutural</span><span class="sxs-lookup"><span data-stu-id="1ddba-122">Structural Content</span></span>

<span data-ttu-id="1ddba-123">A estrutura XML desse elemento é a seguinte:</span><span class="sxs-lookup"><span data-stu-id="1ddba-123">The XML structure of this element is as follows:</span></span>

``` syntax
<psf:Feature name="psk:JobInputBin">
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

## <a name="structure-variables"></a><span data-ttu-id="1ddba-124">Variáveis de estrutura</span><span class="sxs-lookup"><span data-stu-id="1ddba-124">Structure Variables</span></span>

<span data-ttu-id="1ddba-125">A tabela a seguir descreve as características das variáveis definidas na estrutura XML.</span><span class="sxs-lookup"><span data-stu-id="1ddba-125">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="1ddba-126">Nome</span><span class="sxs-lookup"><span data-stu-id="1ddba-126">Name</span></span>                                   | <span data-ttu-id="1ddba-127">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="1ddba-127">Data type</span></span>          | <span data-ttu-id="1ddba-128">Unidade</span><span class="sxs-lookup"><span data-stu-id="1ddba-128">Unit</span></span>                  | <span data-ttu-id="1ddba-129">Valores com suporte</span><span class="sxs-lookup"><span data-stu-id="1ddba-129">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="1ddba-130">Resumo</span><span class="sxs-lookup"><span data-stu-id="1ddba-130">Summary</span></span>                                                                             |
|----------------------------------------|--------------------|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="1ddba-131">\_OptionName\_</span><span class="sxs-lookup"><span data-stu-id="1ddba-131">\_OptionName\_</span></span><br/>              | <span data-ttu-id="1ddba-132">string</span><span class="sxs-lookup"><span data-stu-id="1ddba-132">string</span></span><br/>  | <span data-ttu-id="1ddba-133">characters</span><span class="sxs-lookup"><span data-stu-id="1ddba-133">characters</span></span><br/> | <span data-ttu-id="1ddba-134">Nome totalmente qualificado válido, conforme definido pelos [namespaces em XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span><span class="sxs-lookup"><span data-stu-id="1ddba-134">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="1ddba-135">Se nenhum namespace for especificado, o namespace padrão será assumido.</span><span class="sxs-lookup"><span data-stu-id="1ddba-135">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="1ddba-136">O nome da opção.</span><span class="sxs-lookup"><span data-stu-id="1ddba-136">The name of the option.</span></span><br/>                                                  |
| <span data-ttu-id="1ddba-137">\_IdentityOptionValue\_</span><span class="sxs-lookup"><span data-stu-id="1ddba-137">\_IdentityOptionValue\_</span></span><br/>     | <span data-ttu-id="1ddba-138">string</span><span class="sxs-lookup"><span data-stu-id="1ddba-138">string</span></span><br/>  | <span data-ttu-id="1ddba-139">N/D</span><span class="sxs-lookup"><span data-stu-id="1ddba-139">n/a</span></span><br/>        | <span data-ttu-id="1ddba-140">True, False.</span><span class="sxs-lookup"><span data-stu-id="1ddba-140">True, False.</span></span><br/>                                                                                                                                                               | <span data-ttu-id="1ddba-141">Define uma opção que, quando selecionada, desabilita esse recurso.</span><span class="sxs-lookup"><span data-stu-id="1ddba-141">Defines an Option which when selected would disable this feature.</span></span><br/>        |
| <span data-ttu-id="1ddba-142">\_EnvelopeOptionValue\_</span><span class="sxs-lookup"><span data-stu-id="1ddba-142">\_EnvelopeOptionValue\_</span></span><br/>     | <span data-ttu-id="1ddba-143">string</span><span class="sxs-lookup"><span data-stu-id="1ddba-143">string</span></span><br/>  | <span data-ttu-id="1ddba-144">N/D</span><span class="sxs-lookup"><span data-stu-id="1ddba-144">n/a</span></span><br/>        | <span data-ttu-id="1ddba-145">True, False.</span><span class="sxs-lookup"><span data-stu-id="1ddba-145">True, False.</span></span><br/>                                                                                                                                                               | <span data-ttu-id="1ddba-146">Define uma opção que, quando selecionada, desabilita esse recurso.</span><span class="sxs-lookup"><span data-stu-id="1ddba-146">Defines an Option which when selected would disable this feature.</span></span><br/>        |
| <span data-ttu-id="1ddba-147">\_BinTypeValue\_</span><span class="sxs-lookup"><span data-stu-id="1ddba-147">\_BinTypeValue\_</span></span><br/>            | <span data-ttu-id="1ddba-148">string</span><span class="sxs-lookup"><span data-stu-id="1ddba-148">string</span></span><br/>  | <span data-ttu-id="1ddba-149">N/D</span><span class="sxs-lookup"><span data-stu-id="1ddba-149">n/a</span></span><br/>        | <span data-ttu-id="1ddba-150">ContinuousFeed, SheetFeed.</span><span class="sxs-lookup"><span data-stu-id="1ddba-150">ContinuousFeed, SheetFeed.</span></span><br/>                                                                                                                                                 | <span data-ttu-id="1ddba-151">Especifica o tipo do compartimento.</span><span class="sxs-lookup"><span data-stu-id="1ddba-151">Specifies the type of the bin.</span></span><br/>                                           |
| <span data-ttu-id="1ddba-152">\_FeedTypeValue\_</span><span class="sxs-lookup"><span data-stu-id="1ddba-152">\_FeedTypeValue\_</span></span><br/>           | <span data-ttu-id="1ddba-153">string</span><span class="sxs-lookup"><span data-stu-id="1ddba-153">string</span></span><br/>  | <span data-ttu-id="1ddba-154">N/D</span><span class="sxs-lookup"><span data-stu-id="1ddba-154">n/a</span></span><br/>        | <span data-ttu-id="1ddba-155">Automático, manual.</span><span class="sxs-lookup"><span data-stu-id="1ddba-155">Automatic, Manual.</span></span><br/>                                                                                                                                                         | <span data-ttu-id="1ddba-156">Especifica o mecanismo de feed do compartimento.</span><span class="sxs-lookup"><span data-stu-id="1ddba-156">Specifies the feed mechanism of the bin.</span></span><br/>                                 |
| <span data-ttu-id="1ddba-157">\_MediaCapacityValue\_</span><span class="sxs-lookup"><span data-stu-id="1ddba-157">\_MediaCapacityValue\_</span></span><br/>      | <span data-ttu-id="1ddba-158">string</span><span class="sxs-lookup"><span data-stu-id="1ddba-158">string</span></span><br/>  | <span data-ttu-id="1ddba-159">N/D</span><span class="sxs-lookup"><span data-stu-id="1ddba-159">n/a</span></span><br/>        | <span data-ttu-id="1ddba-160">Alta, padrão.</span><span class="sxs-lookup"><span data-stu-id="1ddba-160">High, Standard.</span></span><br/>                                                                                                                                                            | <span data-ttu-id="1ddba-161">Especifica se o compartimento é uma bandeja de alta capacidade (qualitativa).</span><span class="sxs-lookup"><span data-stu-id="1ddba-161">Specifies whether the bin is a high capacity bin (qualitative).</span></span><br/>          |
| <span data-ttu-id="1ddba-162">\_MediaSizeAutoSenseValue\_</span><span class="sxs-lookup"><span data-stu-id="1ddba-162">\_MediaSizeAutoSenseValue\_</span></span><br/> | <span data-ttu-id="1ddba-163">string</span><span class="sxs-lookup"><span data-stu-id="1ddba-163">string</span></span><br/>  | <span data-ttu-id="1ddba-164">N/D</span><span class="sxs-lookup"><span data-stu-id="1ddba-164">n/a</span></span><br/>        | <span data-ttu-id="1ddba-165">Com suporte, nenhum.</span><span class="sxs-lookup"><span data-stu-id="1ddba-165">Supported, None.</span></span><br/>                                                                                                                                                           | <span data-ttu-id="1ddba-166">Especifica o recurso de detecção automática de tamanho de mídia do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="1ddba-166">Specifies the media size auto sense capability of device.</span></span><br/>                |
| <span data-ttu-id="1ddba-167">\_MediaTypeAutoSenseValue\_</span><span class="sxs-lookup"><span data-stu-id="1ddba-167">\_MediaTypeAutoSenseValue\_</span></span><br/> | <span data-ttu-id="1ddba-168">string</span><span class="sxs-lookup"><span data-stu-id="1ddba-168">string</span></span><br/>  | <span data-ttu-id="1ddba-169">N/D</span><span class="sxs-lookup"><span data-stu-id="1ddba-169">n/a</span></span><br/>        | <span data-ttu-id="1ddba-170">Com suporte, nenhum.</span><span class="sxs-lookup"><span data-stu-id="1ddba-170">Supported, None.</span></span><br/>                                                                                                                                                           | <span data-ttu-id="1ddba-171">Especifica o recurso de detecção automática de tipo de mídia do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="1ddba-171">Specifies the media type auto sense capability of device.</span></span><br/>                |
| <span data-ttu-id="1ddba-172">\_MediaSheetCapacityValue\_</span><span class="sxs-lookup"><span data-stu-id="1ddba-172">\_MediaSheetCapacityValue\_</span></span><br/> | <span data-ttu-id="1ddba-173">Número inteiro</span><span class="sxs-lookup"><span data-stu-id="1ddba-173">integer</span></span><br/> | <span data-ttu-id="1ddba-174">folhas</span><span class="sxs-lookup"><span data-stu-id="1ddba-174">sheets</span></span><br/>     | <span data-ttu-id="1ddba-175">Restrição de inteiro máximo permitida pelo dispositivo.</span><span class="sxs-lookup"><span data-stu-id="1ddba-175">Maximum integer constraint allowed by device.</span></span><br/>                                                                                                                              | <span data-ttu-id="1ddba-176">Especifica a capacidade de mídia no número de páginas (nível completo) do compartimento.</span><span class="sxs-lookup"><span data-stu-id="1ddba-176">Specifies the Media capacity in number of pages (full level) of the bin.</span></span><br/> |
| <span data-ttu-id="1ddba-177">\_MediaPathValue\_</span><span class="sxs-lookup"><span data-stu-id="1ddba-177">\_MediaPathValue\_</span></span><br/>          | <span data-ttu-id="1ddba-178">string</span><span class="sxs-lookup"><span data-stu-id="1ddba-178">string</span></span><br/>  | <span data-ttu-id="1ddba-179">N/D</span><span class="sxs-lookup"><span data-stu-id="1ddba-179">n/a</span></span><br/>        | <span data-ttu-id="1ddba-180">Direto, Serpentine.</span><span class="sxs-lookup"><span data-stu-id="1ddba-180">Straight, Serpentine.</span></span><br/>                                                                                                                                                      | <span data-ttu-id="1ddba-181">Especifica as características do caminho de mídia.</span><span class="sxs-lookup"><span data-stu-id="1ddba-181">Specifies the characteristics of the media path.</span></span><br/>                         |
| <span data-ttu-id="1ddba-182">\_FeedFaceValue\_</span><span class="sxs-lookup"><span data-stu-id="1ddba-182">\_FeedFaceValue\_</span></span><br/>           | <span data-ttu-id="1ddba-183">string</span><span class="sxs-lookup"><span data-stu-id="1ddba-183">string</span></span><br/>  | <span data-ttu-id="1ddba-184">N/D</span><span class="sxs-lookup"><span data-stu-id="1ddba-184">n/a</span></span><br/>        | <span data-ttu-id="1ddba-185">Virado, FaceDown</span><span class="sxs-lookup"><span data-stu-id="1ddba-185">FaceUp, FaceDown</span></span><br/>                                                                                                                                                           | <span data-ttu-id="1ddba-186">Especifica se a mídia a ser impressa ou face para baixo.</span><span class="sxs-lookup"><span data-stu-id="1ddba-186">Specifies whether media is to be printed face up or face down.</span></span><br/>           |
| <span data-ttu-id="1ddba-187">\_FeedDirectionValue\_</span><span class="sxs-lookup"><span data-stu-id="1ddba-187">\_FeedDirectionValue\_</span></span><br/>      | <span data-ttu-id="1ddba-188">string</span><span class="sxs-lookup"><span data-stu-id="1ddba-188">string</span></span><br/>  | <span data-ttu-id="1ddba-189">N/D</span><span class="sxs-lookup"><span data-stu-id="1ddba-189">n/a</span></span><br/>        | <span data-ttu-id="1ddba-190">LongEdgeFirst, ShortEdgeFirst</span><span class="sxs-lookup"><span data-stu-id="1ddba-190">LongEdgeFirst, ShortEdgeFirst</span></span><br/>                                                                                                                                              | <span data-ttu-id="1ddba-191">Especifica se a mídia é alimentada pela borda longa ou pela borda curta primeiro.</span><span class="sxs-lookup"><span data-stu-id="1ddba-191">Specifies whether media is fed long edge first or short edge first.</span></span><br/>      |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="1ddba-192">Conteúdo de linguagem XML (XML)</span><span class="sxs-lookup"><span data-stu-id="1ddba-192">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="1ddba-193">As palavras-chave do esquema de impressão pública são definidas no https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span><span class="sxs-lookup"><span data-stu-id="1ddba-193">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="1ddba-194">O conteúdo do linguagem XML público (XML) para essa palavra-chave é definido abaixo:</span><span class="sxs-lookup"><span data-stu-id="1ddba-194">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

``` syntax
<psf:Feature name="psk:JobInputBin">
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

## <a name="related-topics"></a><span data-ttu-id="1ddba-195">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="1ddba-195">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1ddba-196">Especificação de esquema de impressão</span><span class="sxs-lookup"><span data-stu-id="1ddba-196">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




