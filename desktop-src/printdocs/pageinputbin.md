---
description: Obter informações sobre o elemento configurável pelo usuário PageInputBin. Este tópico não é atual. Para obter as informações mais atuais, consulte a Especificação de Esquema de Impressão.
ms.assetid: 78eb3119-a52f-4ff8-83bb-903e181c8a11
title: Pageinputbin
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dc53d377106b95b26e694d531af2952cea98a8b1
ms.sourcegitcommit: 998d50f6def8a25850fc113fc8a2df903c829c5e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/09/2021
ms.locfileid: "113549164"
---
# <a name="pageinputbin"></a><span data-ttu-id="5e236-105">Pageinputbin</span><span class="sxs-lookup"><span data-stu-id="5e236-105">PageInputBin</span></span>

<span data-ttu-id="5e236-106">Este tópico não é atual.</span><span class="sxs-lookup"><span data-stu-id="5e236-106">This topic is not current.</span></span> <span data-ttu-id="5e236-107">Para obter as informações mais atuais, consulte a [Especificação de Esquema de Impressão](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="5e236-107">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="5e236-108">Descreve o compartimento de entrada instalado em um dispositivo ou a lista completa de compartimentos com suporte para um dispositivo.</span><span class="sxs-lookup"><span data-stu-id="5e236-108">Describes the installed input bin in a device or the full list of supported bins for a device.</span></span> <span data-ttu-id="5e236-109">Permite a especificação do compartimento de entrada por página.</span><span class="sxs-lookup"><span data-stu-id="5e236-109">Allows specification of input bin on a per page basis.</span></span> <span data-ttu-id="5e236-110">As palavras-chave JobInputBin, DocumentInputBin e PageInputBin são mutuamente exclusivas.</span><span class="sxs-lookup"><span data-stu-id="5e236-110">The JobInputBin, DocumentInputBin, and PageInputBin keywords are mutually exclusive.</span></span> <span data-ttu-id="5e236-111">Ambos não devem ser especificados simultaneamente em um documento PrintTicket ou Recursos de Impressão.</span><span class="sxs-lookup"><span data-stu-id="5e236-111">Both should not be specified simultaneously in a PrintTicket or Print Capabilities document.</span></span>

-   [<span data-ttu-id="5e236-112">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="5e236-112">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="5e236-113">Conteúdo estrutural</span><span class="sxs-lookup"><span data-stu-id="5e236-113">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="5e236-114">linguagem XML conteúdo (XML)</span><span class="sxs-lookup"><span data-stu-id="5e236-114">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="5e236-115">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="5e236-115">Element Information</span></span>



| <span data-ttu-id="5e236-116">Nome</span><span class="sxs-lookup"><span data-stu-id="5e236-116">Name</span></span> | <span data-ttu-id="5e236-117">Valor</span><span class="sxs-lookup"><span data-stu-id="5e236-117">Value</span></span> |
|----------------------------|--------------------|
| <span data-ttu-id="5e236-118">Tipo de elemento</span><span class="sxs-lookup"><span data-stu-id="5e236-118">Element Type</span></span> <br/>   | <span data-ttu-id="5e236-119">Recurso</span><span class="sxs-lookup"><span data-stu-id="5e236-119">Feature</span></span><br/> |
| <span data-ttu-id="5e236-120">Prefixo de definição de scoping</span><span class="sxs-lookup"><span data-stu-id="5e236-120">Scoping Prefix</span></span> <br/> | <span data-ttu-id="5e236-121">Página</span><span class="sxs-lookup"><span data-stu-id="5e236-121">Page</span></span><br/>    |
| <span data-ttu-id="5e236-122">Observações</span><span class="sxs-lookup"><span data-stu-id="5e236-122">Notes</span></span> <br/>          | <span data-ttu-id="5e236-123">Nenhum</span><span class="sxs-lookup"><span data-stu-id="5e236-123">None</span></span><br/>    |



 

## <a name="structural-content"></a><span data-ttu-id="5e236-124">Conteúdo estrutural</span><span class="sxs-lookup"><span data-stu-id="5e236-124">Structural Content</span></span>

<span data-ttu-id="5e236-125">A estrutura XML desse elemento é:</span><span class="sxs-lookup"><span data-stu-id="5e236-125">The XML structure of this element is:</span></span>

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

## <a name="structure-variables"></a><span data-ttu-id="5e236-126">Variáveis de estrutura</span><span class="sxs-lookup"><span data-stu-id="5e236-126">Structure Variables</span></span>

<span data-ttu-id="5e236-127">A tabela a seguir descreve as características das variáveis definidas na estrutura XML.</span><span class="sxs-lookup"><span data-stu-id="5e236-127">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="5e236-128">Nome</span><span class="sxs-lookup"><span data-stu-id="5e236-128">Name</span></span>                                   | <span data-ttu-id="5e236-129">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="5e236-129">Data type</span></span>          | <span data-ttu-id="5e236-130">Unidade</span><span class="sxs-lookup"><span data-stu-id="5e236-130">Unit</span></span>                  | <span data-ttu-id="5e236-131">Valores com suporte</span><span class="sxs-lookup"><span data-stu-id="5e236-131">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="5e236-132">Resumo</span><span class="sxs-lookup"><span data-stu-id="5e236-132">Summary</span></span>                                                                             |
|----------------------------------------|--------------------|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="5e236-133">\_Optionname\_</span><span class="sxs-lookup"><span data-stu-id="5e236-133">\_OptionName\_</span></span><br/>              | <span data-ttu-id="5e236-134">string</span><span class="sxs-lookup"><span data-stu-id="5e236-134">string</span></span><br/>  | <span data-ttu-id="5e236-135">characters</span><span class="sxs-lookup"><span data-stu-id="5e236-135">characters</span></span><br/> | <span data-ttu-id="5e236-136">Nome totalmente qualificado válido, conforme definido [por Namespaces em XML.](https://www.w3.org/TR/1999/REC-xml-names-19990114/)</span><span class="sxs-lookup"><span data-stu-id="5e236-136">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="5e236-137">Se nenhum namespace for especificado, o namespace padrão será assumido.</span><span class="sxs-lookup"><span data-stu-id="5e236-137">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="5e236-138">O nome da opção.</span><span class="sxs-lookup"><span data-stu-id="5e236-138">The name of the option.</span></span><br/>                                                  |
| <span data-ttu-id="5e236-139">\_IdentityOptionValue\_</span><span class="sxs-lookup"><span data-stu-id="5e236-139">\_IdentityOptionValue\_</span></span><br/>     | <span data-ttu-id="5e236-140">string</span><span class="sxs-lookup"><span data-stu-id="5e236-140">string</span></span><br/>  | <span data-ttu-id="5e236-141">n/d</span><span class="sxs-lookup"><span data-stu-id="5e236-141">n/a</span></span><br/>        | <span data-ttu-id="5e236-142">True, False.</span><span class="sxs-lookup"><span data-stu-id="5e236-142">True, False.</span></span><br/>                                                                                                                                                               | <span data-ttu-id="5e236-143">Define uma Opção que, quando selecionada, desabilitará esse recurso.</span><span class="sxs-lookup"><span data-stu-id="5e236-143">Defines an Option which when selected would disable this feature.</span></span><br/>        |
| <span data-ttu-id="5e236-144">\_EnvelopeOptionValue\_</span><span class="sxs-lookup"><span data-stu-id="5e236-144">\_EnvelopeOptionValue\_</span></span><br/>     | <span data-ttu-id="5e236-145">string</span><span class="sxs-lookup"><span data-stu-id="5e236-145">string</span></span><br/>  | <span data-ttu-id="5e236-146">n/d</span><span class="sxs-lookup"><span data-stu-id="5e236-146">n/a</span></span><br/>        | <span data-ttu-id="5e236-147">True, False.</span><span class="sxs-lookup"><span data-stu-id="5e236-147">True, False.</span></span><br/>                                                                                                                                                               | <span data-ttu-id="5e236-148">Define uma Opção que, quando selecionada, desabilitará esse recurso.</span><span class="sxs-lookup"><span data-stu-id="5e236-148">Defines an Option which when selected would disable this feature.</span></span><br/>        |
| <span data-ttu-id="5e236-149">\_BinTypeValue\_</span><span class="sxs-lookup"><span data-stu-id="5e236-149">\_BinTypeValue\_</span></span><br/>            | <span data-ttu-id="5e236-150">string</span><span class="sxs-lookup"><span data-stu-id="5e236-150">string</span></span><br/>  | <span data-ttu-id="5e236-151">n/d</span><span class="sxs-lookup"><span data-stu-id="5e236-151">n/a</span></span><br/>        | <span data-ttu-id="5e236-152">ContinuousFeed, SheetFeed.</span><span class="sxs-lookup"><span data-stu-id="5e236-152">ContinuousFeed, SheetFeed.</span></span><br/>                                                                                                                                                 | <span data-ttu-id="5e236-153">Especifica o tipo do compartimento.</span><span class="sxs-lookup"><span data-stu-id="5e236-153">Specifies the type of the bin.</span></span><br/>                                           |
| <span data-ttu-id="5e236-154">\_FeedTypeValue\_</span><span class="sxs-lookup"><span data-stu-id="5e236-154">\_FeedTypeValue\_</span></span><br/>           | <span data-ttu-id="5e236-155">string</span><span class="sxs-lookup"><span data-stu-id="5e236-155">string</span></span><br/>  | <span data-ttu-id="5e236-156">n/d</span><span class="sxs-lookup"><span data-stu-id="5e236-156">n/a</span></span><br/>        | <span data-ttu-id="5e236-157">Automático, Manual.</span><span class="sxs-lookup"><span data-stu-id="5e236-157">Automatic, Manual.</span></span><br/>                                                                                                                                                         | <span data-ttu-id="5e236-158">Especifica o mecanismo de feed do compartimento.</span><span class="sxs-lookup"><span data-stu-id="5e236-158">Specifies the feed mechanism of the bin.</span></span><br/>                                 |
| <span data-ttu-id="5e236-159">\_MediaCapacityValue\_</span><span class="sxs-lookup"><span data-stu-id="5e236-159">\_MediaCapacityValue\_</span></span><br/>      | <span data-ttu-id="5e236-160">string</span><span class="sxs-lookup"><span data-stu-id="5e236-160">string</span></span><br/>  | <span data-ttu-id="5e236-161">n/d</span><span class="sxs-lookup"><span data-stu-id="5e236-161">n/a</span></span><br/>        | <span data-ttu-id="5e236-162">Alto, Standard.</span><span class="sxs-lookup"><span data-stu-id="5e236-162">High, Standard.</span></span><br/>                                                                                                                                                            | <span data-ttu-id="5e236-163">Especifica se o compartimento é um compartimento de alta capacidade (qualitativo).</span><span class="sxs-lookup"><span data-stu-id="5e236-163">Specifies whether the bin is a high capacity bin (qualitative).</span></span><br/>          |
| <span data-ttu-id="5e236-164">\_MediaSizeAutoSenseValue\_</span><span class="sxs-lookup"><span data-stu-id="5e236-164">\_MediaSizeAutoSenseValue\_</span></span><br/> | <span data-ttu-id="5e236-165">string</span><span class="sxs-lookup"><span data-stu-id="5e236-165">string</span></span><br/>  | <span data-ttu-id="5e236-166">n/d</span><span class="sxs-lookup"><span data-stu-id="5e236-166">n/a</span></span><br/>        | <span data-ttu-id="5e236-167">Com suporte, Nenhum.</span><span class="sxs-lookup"><span data-stu-id="5e236-167">Supported, None.</span></span><br/>                                                                                                                                                           | <span data-ttu-id="5e236-168">Especifica a funcionalidade de detecção automática de tamanho de mídia do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="5e236-168">Specifies the media size auto sense capability of device.</span></span><br/>                |
| <span data-ttu-id="5e236-169">\_MediaTypeAutoSenseValue\_</span><span class="sxs-lookup"><span data-stu-id="5e236-169">\_MediaTypeAutoSenseValue\_</span></span><br/> | <span data-ttu-id="5e236-170">string</span><span class="sxs-lookup"><span data-stu-id="5e236-170">string</span></span><br/>  | <span data-ttu-id="5e236-171">n/d</span><span class="sxs-lookup"><span data-stu-id="5e236-171">n/a</span></span><br/>        | <span data-ttu-id="5e236-172">Com suporte, Nenhum.</span><span class="sxs-lookup"><span data-stu-id="5e236-172">Supported, None.</span></span><br/>                                                                                                                                                           | <span data-ttu-id="5e236-173">Especifica a funcionalidade de detecção automática do tipo de mídia do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="5e236-173">Specifies the media type auto sense capability of device.</span></span><br/>                |
| <span data-ttu-id="5e236-174">\_MediaSheetCapacityValue\_</span><span class="sxs-lookup"><span data-stu-id="5e236-174">\_MediaSheetCapacityValue\_</span></span><br/> | <span data-ttu-id="5e236-175">Número inteiro</span><span class="sxs-lookup"><span data-stu-id="5e236-175">integer</span></span><br/> | <span data-ttu-id="5e236-176">Folhas</span><span class="sxs-lookup"><span data-stu-id="5e236-176">sheets</span></span><br/>     | <span data-ttu-id="5e236-177">Restrição de inteiro máxima permitida pelo dispositivo.</span><span class="sxs-lookup"><span data-stu-id="5e236-177">Maximum integer constraint allowed by device.</span></span><br/>                                                                                                                              | <span data-ttu-id="5e236-178">Especifica a capacidade de Mídia no número de páginas (nível completo) do compartimento.</span><span class="sxs-lookup"><span data-stu-id="5e236-178">Specifies the Media capacity in number of pages (full level) of the bin.</span></span><br/> |
| <span data-ttu-id="5e236-179">\_MediaPathValue\_</span><span class="sxs-lookup"><span data-stu-id="5e236-179">\_MediaPathValue\_</span></span><br/>          | <span data-ttu-id="5e236-180">string</span><span class="sxs-lookup"><span data-stu-id="5e236-180">string</span></span><br/>  | <span data-ttu-id="5e236-181">n/d</span><span class="sxs-lookup"><span data-stu-id="5e236-181">n/a</span></span><br/>        | <span data-ttu-id="5e236-182">Straight, Longine.</span><span class="sxs-lookup"><span data-stu-id="5e236-182">Straight, Serpentine.</span></span><br/>                                                                                                                                                      | <span data-ttu-id="5e236-183">Especifica as características do caminho de mídia.</span><span class="sxs-lookup"><span data-stu-id="5e236-183">Specifies the characteristics of the media path.</span></span><br/>                         |
| <span data-ttu-id="5e236-184">\_FeedFaceValue\_</span><span class="sxs-lookup"><span data-stu-id="5e236-184">\_FeedFaceValue\_</span></span><br/>           | <span data-ttu-id="5e236-185">string</span><span class="sxs-lookup"><span data-stu-id="5e236-185">string</span></span><br/>  | <span data-ttu-id="5e236-186">n/d</span><span class="sxs-lookup"><span data-stu-id="5e236-186">n/a</span></span><br/>        | <span data-ttu-id="5e236-187">FaceUp, FaceDown</span><span class="sxs-lookup"><span data-stu-id="5e236-187">FaceUp, FaceDown</span></span><br/>                                                                                                                                                           | <span data-ttu-id="5e236-188">Especifica se a mídia deve ser impressa com a face para cima ou com a face para baixo.</span><span class="sxs-lookup"><span data-stu-id="5e236-188">Specifies whether media is to be printed face up or face down.</span></span><br/>           |
| <span data-ttu-id="5e236-189">\_FeedDirectionValue\_</span><span class="sxs-lookup"><span data-stu-id="5e236-189">\_FeedDirectionValue\_</span></span><br/>      | <span data-ttu-id="5e236-190">string</span><span class="sxs-lookup"><span data-stu-id="5e236-190">string</span></span><br/>  | <span data-ttu-id="5e236-191">n/d</span><span class="sxs-lookup"><span data-stu-id="5e236-191">n/a</span></span><br/>        | <span data-ttu-id="5e236-192">LongEdgeFirst, ShortEdgeFirst</span><span class="sxs-lookup"><span data-stu-id="5e236-192">LongEdgeFirst, ShortEdgeFirst</span></span><br/>                                                                                                                                              | <span data-ttu-id="5e236-193">Especifica se a mídia é alimentada pela borda longa primeiro ou pela borda curta primeiro.</span><span class="sxs-lookup"><span data-stu-id="5e236-193">Specifies whether media is fed long edge first or short edge first.</span></span><br/>      |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="5e236-194">linguagem XML conteúdo (XML)</span><span class="sxs-lookup"><span data-stu-id="5e236-194">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="5e236-195">As palavras-chave public Print Schema são definidas no https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace .</span><span class="sxs-lookup"><span data-stu-id="5e236-195">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="5e236-196">O conteúdo linguagem XML XML (public linguagem XML) para essa palavra-chave é definido abaixo:</span><span class="sxs-lookup"><span data-stu-id="5e236-196">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

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

## <a name="related-topics"></a><span data-ttu-id="5e236-197">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="5e236-197">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5e236-198">Especificação de esquema de impressão</span><span class="sxs-lookup"><span data-stu-id="5e236-198">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




