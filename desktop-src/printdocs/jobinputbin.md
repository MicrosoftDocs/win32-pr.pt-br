---
description: Saiba mais sobre o elemento JobInputBin, que descreve o compartimento de entrada instalado em um dispositivo ou a lista completa de compartimentos com suporte para um dispositivo.
ms.assetid: 9192ceb1-90c4-480e-9247-68d457976f42
title: Jobinputbin
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 929df4cb4871e5a8d2ebacfe533b5da3ad9babf3
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/19/2021
ms.locfileid: "112408889"
---
# <a name="jobinputbin"></a><span data-ttu-id="db686-103">Jobinputbin</span><span class="sxs-lookup"><span data-stu-id="db686-103">JobInputBin</span></span>

<span data-ttu-id="db686-104">Este tópico não é atual.</span><span class="sxs-lookup"><span data-stu-id="db686-104">This topic is not current.</span></span> <span data-ttu-id="db686-105">Para obter as informações mais atuais, consulte a [Especificação de Esquema de Impressão](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="db686-105">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="db686-106">Descreve o compartimento de entrada instalado em um dispositivo ou a lista completa de compartimentos com suporte para um dispositivo.</span><span class="sxs-lookup"><span data-stu-id="db686-106">Describes the installed input bin in a device or the full list of supported bins for a device.</span></span> <span data-ttu-id="db686-107">Permite a especificação do compartimento de entrada por trabalho.</span><span class="sxs-lookup"><span data-stu-id="db686-107">Allows specification of input bin on a per job basis.</span></span> <span data-ttu-id="db686-108">As palavras-chave JobInputBin, DocumentInputBin e PageInputBin são mutuamente exclusivas.</span><span class="sxs-lookup"><span data-stu-id="db686-108">The JobInputBin, DocumentInputBin, and PageInputBin keywords are mutually exclusive.</span></span> <span data-ttu-id="db686-109">Ambos não devem ser especificados simultaneamente em um documento PrintTicket ou Recursos de Impressão.</span><span class="sxs-lookup"><span data-stu-id="db686-109">Both should not be specified simultaneously in a PrintTicket or Print Capabilities document.</span></span>

-   [<span data-ttu-id="db686-110">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="db686-110">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="db686-111">Conteúdo estrutural</span><span class="sxs-lookup"><span data-stu-id="db686-111">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="db686-112">linguagem XML conteúdo (XML)</span><span class="sxs-lookup"><span data-stu-id="db686-112">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="db686-113">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="db686-113">Element Information</span></span>



| <span data-ttu-id="db686-114">Name</span><span class="sxs-lookup"><span data-stu-id="db686-114">Name</span></span> | <span data-ttu-id="db686-115">Valor</span><span class="sxs-lookup"><span data-stu-id="db686-115">Value</span></span> |
|----------------------------|--------------------|
| <span data-ttu-id="db686-116">Tipo de elemento</span><span class="sxs-lookup"><span data-stu-id="db686-116">Element Type</span></span> <br/>   | <span data-ttu-id="db686-117">Recurso</span><span class="sxs-lookup"><span data-stu-id="db686-117">Feature</span></span><br/> |
| <span data-ttu-id="db686-118">Prefixo de definição de scoping</span><span class="sxs-lookup"><span data-stu-id="db686-118">Scoping Prefix</span></span> <br/> | <span data-ttu-id="db686-119">Trabalho</span><span class="sxs-lookup"><span data-stu-id="db686-119">Job</span></span><br/>     |
| <span data-ttu-id="db686-120">Observações</span><span class="sxs-lookup"><span data-stu-id="db686-120">Notes</span></span> <br/>          | <span data-ttu-id="db686-121">Nenhum</span><span class="sxs-lookup"><span data-stu-id="db686-121">None</span></span><br/>    |



 

## <a name="structural-content"></a><span data-ttu-id="db686-122">Conteúdo estrutural</span><span class="sxs-lookup"><span data-stu-id="db686-122">Structural Content</span></span>

<span data-ttu-id="db686-123">A estrutura XML desse elemento é a seguinte:</span><span class="sxs-lookup"><span data-stu-id="db686-123">The XML structure of this element is as follows:</span></span>

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

## <a name="structure-variables"></a><span data-ttu-id="db686-124">Variáveis de estrutura</span><span class="sxs-lookup"><span data-stu-id="db686-124">Structure Variables</span></span>

<span data-ttu-id="db686-125">A tabela a seguir descreve as características das variáveis definidas na estrutura XML.</span><span class="sxs-lookup"><span data-stu-id="db686-125">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="db686-126">Nome</span><span class="sxs-lookup"><span data-stu-id="db686-126">Name</span></span>                                   | <span data-ttu-id="db686-127">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="db686-127">Data type</span></span>          | <span data-ttu-id="db686-128">Unidade</span><span class="sxs-lookup"><span data-stu-id="db686-128">Unit</span></span>                  | <span data-ttu-id="db686-129">Valores com suporte</span><span class="sxs-lookup"><span data-stu-id="db686-129">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="db686-130">Resumo</span><span class="sxs-lookup"><span data-stu-id="db686-130">Summary</span></span>                                                                             |
|----------------------------------------|--------------------|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="db686-131">\_Optionname\_</span><span class="sxs-lookup"><span data-stu-id="db686-131">\_OptionName\_</span></span><br/>              | <span data-ttu-id="db686-132">string</span><span class="sxs-lookup"><span data-stu-id="db686-132">string</span></span><br/>  | <span data-ttu-id="db686-133">characters</span><span class="sxs-lookup"><span data-stu-id="db686-133">characters</span></span><br/> | <span data-ttu-id="db686-134">Nome totalmente qualificado válido, conforme definido [por Namespaces em XML.](https://www.w3.org/TR/1999/REC-xml-names-19990114/)</span><span class="sxs-lookup"><span data-stu-id="db686-134">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="db686-135">Se nenhum namespace for especificado, o namespace padrão será assumido.</span><span class="sxs-lookup"><span data-stu-id="db686-135">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="db686-136">O nome da opção.</span><span class="sxs-lookup"><span data-stu-id="db686-136">The name of the option.</span></span><br/>                                                  |
| <span data-ttu-id="db686-137">\_IdentityOptionValue\_</span><span class="sxs-lookup"><span data-stu-id="db686-137">\_IdentityOptionValue\_</span></span><br/>     | <span data-ttu-id="db686-138">string</span><span class="sxs-lookup"><span data-stu-id="db686-138">string</span></span><br/>  | <span data-ttu-id="db686-139">n/d</span><span class="sxs-lookup"><span data-stu-id="db686-139">n/a</span></span><br/>        | <span data-ttu-id="db686-140">True, False.</span><span class="sxs-lookup"><span data-stu-id="db686-140">True, False.</span></span><br/>                                                                                                                                                               | <span data-ttu-id="db686-141">Define uma Opção que, quando selecionada, desabilitará esse recurso.</span><span class="sxs-lookup"><span data-stu-id="db686-141">Defines an Option which when selected would disable this feature.</span></span><br/>        |
| <span data-ttu-id="db686-142">\_EnvelopeOptionValue\_</span><span class="sxs-lookup"><span data-stu-id="db686-142">\_EnvelopeOptionValue\_</span></span><br/>     | <span data-ttu-id="db686-143">string</span><span class="sxs-lookup"><span data-stu-id="db686-143">string</span></span><br/>  | <span data-ttu-id="db686-144">n/d</span><span class="sxs-lookup"><span data-stu-id="db686-144">n/a</span></span><br/>        | <span data-ttu-id="db686-145">True, False.</span><span class="sxs-lookup"><span data-stu-id="db686-145">True, False.</span></span><br/>                                                                                                                                                               | <span data-ttu-id="db686-146">Define uma Opção que, quando selecionada, desabilitará esse recurso.</span><span class="sxs-lookup"><span data-stu-id="db686-146">Defines an Option which when selected would disable this feature.</span></span><br/>        |
| <span data-ttu-id="db686-147">\_BinTypeValue\_</span><span class="sxs-lookup"><span data-stu-id="db686-147">\_BinTypeValue\_</span></span><br/>            | <span data-ttu-id="db686-148">string</span><span class="sxs-lookup"><span data-stu-id="db686-148">string</span></span><br/>  | <span data-ttu-id="db686-149">n/d</span><span class="sxs-lookup"><span data-stu-id="db686-149">n/a</span></span><br/>        | <span data-ttu-id="db686-150">ContinuousFeed, SheetFeed.</span><span class="sxs-lookup"><span data-stu-id="db686-150">ContinuousFeed, SheetFeed.</span></span><br/>                                                                                                                                                 | <span data-ttu-id="db686-151">Especifica o tipo do compartimento.</span><span class="sxs-lookup"><span data-stu-id="db686-151">Specifies the type of the bin.</span></span><br/>                                           |
| <span data-ttu-id="db686-152">\_FeedTypeValue\_</span><span class="sxs-lookup"><span data-stu-id="db686-152">\_FeedTypeValue\_</span></span><br/>           | <span data-ttu-id="db686-153">string</span><span class="sxs-lookup"><span data-stu-id="db686-153">string</span></span><br/>  | <span data-ttu-id="db686-154">n/d</span><span class="sxs-lookup"><span data-stu-id="db686-154">n/a</span></span><br/>        | <span data-ttu-id="db686-155">Automático, Manual.</span><span class="sxs-lookup"><span data-stu-id="db686-155">Automatic, Manual.</span></span><br/>                                                                                                                                                         | <span data-ttu-id="db686-156">Especifica o mecanismo de feed do compartimento.</span><span class="sxs-lookup"><span data-stu-id="db686-156">Specifies the feed mechanism of the bin.</span></span><br/>                                 |
| <span data-ttu-id="db686-157">\_MediaCapacityValue\_</span><span class="sxs-lookup"><span data-stu-id="db686-157">\_MediaCapacityValue\_</span></span><br/>      | <span data-ttu-id="db686-158">string</span><span class="sxs-lookup"><span data-stu-id="db686-158">string</span></span><br/>  | <span data-ttu-id="db686-159">n/d</span><span class="sxs-lookup"><span data-stu-id="db686-159">n/a</span></span><br/>        | <span data-ttu-id="db686-160">Alto, Standard.</span><span class="sxs-lookup"><span data-stu-id="db686-160">High, Standard.</span></span><br/>                                                                                                                                                            | <span data-ttu-id="db686-161">Especifica se o compartimento é um compartimento de alta capacidade (qualitativo).</span><span class="sxs-lookup"><span data-stu-id="db686-161">Specifies whether the bin is a high capacity bin (qualitative).</span></span><br/>          |
| <span data-ttu-id="db686-162">\_MediaSizeAutoSenseValue\_</span><span class="sxs-lookup"><span data-stu-id="db686-162">\_MediaSizeAutoSenseValue\_</span></span><br/> | <span data-ttu-id="db686-163">string</span><span class="sxs-lookup"><span data-stu-id="db686-163">string</span></span><br/>  | <span data-ttu-id="db686-164">n/d</span><span class="sxs-lookup"><span data-stu-id="db686-164">n/a</span></span><br/>        | <span data-ttu-id="db686-165">Com suporte, Nenhum.</span><span class="sxs-lookup"><span data-stu-id="db686-165">Supported, None.</span></span><br/>                                                                                                                                                           | <span data-ttu-id="db686-166">Especifica a funcionalidade de detecção automática de tamanho de mídia do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="db686-166">Specifies the media size auto sense capability of device.</span></span><br/>                |
| <span data-ttu-id="db686-167">\_MediaTypeAutoSenseValue\_</span><span class="sxs-lookup"><span data-stu-id="db686-167">\_MediaTypeAutoSenseValue\_</span></span><br/> | <span data-ttu-id="db686-168">string</span><span class="sxs-lookup"><span data-stu-id="db686-168">string</span></span><br/>  | <span data-ttu-id="db686-169">n/d</span><span class="sxs-lookup"><span data-stu-id="db686-169">n/a</span></span><br/>        | <span data-ttu-id="db686-170">Com suporte, Nenhum.</span><span class="sxs-lookup"><span data-stu-id="db686-170">Supported, None.</span></span><br/>                                                                                                                                                           | <span data-ttu-id="db686-171">Especifica a funcionalidade de detecção automática do tipo de mídia do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="db686-171">Specifies the media type auto sense capability of device.</span></span><br/>                |
| <span data-ttu-id="db686-172">\_MediaSheetCapacityValue\_</span><span class="sxs-lookup"><span data-stu-id="db686-172">\_MediaSheetCapacityValue\_</span></span><br/> | <span data-ttu-id="db686-173">Número inteiro</span><span class="sxs-lookup"><span data-stu-id="db686-173">integer</span></span><br/> | <span data-ttu-id="db686-174">Folhas</span><span class="sxs-lookup"><span data-stu-id="db686-174">sheets</span></span><br/>     | <span data-ttu-id="db686-175">Restrição de inteiro máxima permitida pelo dispositivo.</span><span class="sxs-lookup"><span data-stu-id="db686-175">Maximum integer constraint allowed by device.</span></span><br/>                                                                                                                              | <span data-ttu-id="db686-176">Especifica a capacidade de Mídia no número de páginas (nível completo) do compartimento.</span><span class="sxs-lookup"><span data-stu-id="db686-176">Specifies the Media capacity in number of pages (full level) of the bin.</span></span><br/> |
| <span data-ttu-id="db686-177">\_MediaPathValue\_</span><span class="sxs-lookup"><span data-stu-id="db686-177">\_MediaPathValue\_</span></span><br/>          | <span data-ttu-id="db686-178">string</span><span class="sxs-lookup"><span data-stu-id="db686-178">string</span></span><br/>  | <span data-ttu-id="db686-179">n/d</span><span class="sxs-lookup"><span data-stu-id="db686-179">n/a</span></span><br/>        | <span data-ttu-id="db686-180">Straight, Longine.</span><span class="sxs-lookup"><span data-stu-id="db686-180">Straight, Serpentine.</span></span><br/>                                                                                                                                                      | <span data-ttu-id="db686-181">Especifica as características do caminho de mídia.</span><span class="sxs-lookup"><span data-stu-id="db686-181">Specifies the characteristics of the media path.</span></span><br/>                         |
| <span data-ttu-id="db686-182">\_FeedFaceValue\_</span><span class="sxs-lookup"><span data-stu-id="db686-182">\_FeedFaceValue\_</span></span><br/>           | <span data-ttu-id="db686-183">string</span><span class="sxs-lookup"><span data-stu-id="db686-183">string</span></span><br/>  | <span data-ttu-id="db686-184">n/d</span><span class="sxs-lookup"><span data-stu-id="db686-184">n/a</span></span><br/>        | <span data-ttu-id="db686-185">FaceUp, FaceDown</span><span class="sxs-lookup"><span data-stu-id="db686-185">FaceUp, FaceDown</span></span><br/>                                                                                                                                                           | <span data-ttu-id="db686-186">Especifica se a mídia deve ser impressa com a face para cima ou com a face para baixo.</span><span class="sxs-lookup"><span data-stu-id="db686-186">Specifies whether media is to be printed face up or face down.</span></span><br/>           |
| <span data-ttu-id="db686-187">\_FeedDirectionValue\_</span><span class="sxs-lookup"><span data-stu-id="db686-187">\_FeedDirectionValue\_</span></span><br/>      | <span data-ttu-id="db686-188">string</span><span class="sxs-lookup"><span data-stu-id="db686-188">string</span></span><br/>  | <span data-ttu-id="db686-189">n/d</span><span class="sxs-lookup"><span data-stu-id="db686-189">n/a</span></span><br/>        | <span data-ttu-id="db686-190">LongEdgeFirst, ShortEdgeFirst</span><span class="sxs-lookup"><span data-stu-id="db686-190">LongEdgeFirst, ShortEdgeFirst</span></span><br/>                                                                                                                                              | <span data-ttu-id="db686-191">Especifica se a mídia é alimentada pela borda longa primeiro ou pela borda curta primeiro.</span><span class="sxs-lookup"><span data-stu-id="db686-191">Specifies whether media is fed long edge first or short edge first.</span></span><br/>      |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="db686-192">linguagem XML conteúdo (XML)</span><span class="sxs-lookup"><span data-stu-id="db686-192">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="db686-193">As palavras-chave public Print Schema são definidas no https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace .</span><span class="sxs-lookup"><span data-stu-id="db686-193">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="db686-194">O conteúdo linguagem XML XML (public linguagem XML) para essa palavra-chave é definido abaixo:</span><span class="sxs-lookup"><span data-stu-id="db686-194">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

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

## <a name="related-topics"></a><span data-ttu-id="db686-195">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="db686-195">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="db686-196">Especificação de esquema de impressão</span><span class="sxs-lookup"><span data-stu-id="db686-196">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




