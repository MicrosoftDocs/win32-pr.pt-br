---
description: Saiba mais sobre o elemento JobOutputBin, que descreve a bandeja de saída instalada em um dispositivo ou a lista completa de compartimentos com suporte para um dispositivo.
ms.assetid: 324ec426-b7c8-43af-96b9-74929358e262
title: JobOutputBin
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1243e9409f781b8babde6d6310ce7a2b083f8703
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/19/2021
ms.locfileid: "112408849"
---
# <a name="joboutputbin"></a><span data-ttu-id="aaa8a-103">JobOutputBin</span><span class="sxs-lookup"><span data-stu-id="aaa8a-103">JobOutputBin</span></span>

<span data-ttu-id="aaa8a-104">Este tópico não é atual.</span><span class="sxs-lookup"><span data-stu-id="aaa8a-104">This topic is not current.</span></span> <span data-ttu-id="aaa8a-105">Para obter as informações mais atuais, consulte a [especificação do esquema de impressão](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="aaa8a-105">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="aaa8a-106">Descreve a bandeja de saída instalada em um dispositivo ou a lista completa de compartimentos com suporte para um dispositivo.</span><span class="sxs-lookup"><span data-stu-id="aaa8a-106">Describes the installed output bin in a device or the full list of supported bins for a device.</span></span> <span data-ttu-id="aaa8a-107">As palavras-chave JobOutputBin, DocumentOutputBin e PageOutputBin são mutuamente exclusivas apenas uma deve ser especificada em um documento de recursos de impressão ou PrintTicket.</span><span class="sxs-lookup"><span data-stu-id="aaa8a-107">The JobOutputBin, DocumentOutputBin and PageOutputBin keywords are mutually exclusive only one should be specified in a PrintTicket or Print Capabilities document.</span></span>

-   [<span data-ttu-id="aaa8a-108">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="aaa8a-108">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="aaa8a-109">Conteúdo estrutural</span><span class="sxs-lookup"><span data-stu-id="aaa8a-109">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="aaa8a-110">Conteúdo de linguagem XML (XML)</span><span class="sxs-lookup"><span data-stu-id="aaa8a-110">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="aaa8a-111">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="aaa8a-111">Element Information</span></span>



| <span data-ttu-id="aaa8a-112">Name</span><span class="sxs-lookup"><span data-stu-id="aaa8a-112">Name</span></span> | <span data-ttu-id="aaa8a-113">Valor</span><span class="sxs-lookup"><span data-stu-id="aaa8a-113">Value</span></span> |
|----------------------------|--------------------|
| <span data-ttu-id="aaa8a-114">Tipo de elemento</span><span class="sxs-lookup"><span data-stu-id="aaa8a-114">Element Type</span></span> <br/>   | <span data-ttu-id="aaa8a-115">Recurso</span><span class="sxs-lookup"><span data-stu-id="aaa8a-115">Feature</span></span><br/> |
| <span data-ttu-id="aaa8a-116">Prefixo de escopo</span><span class="sxs-lookup"><span data-stu-id="aaa8a-116">Scoping Prefix</span></span> <br/> | <span data-ttu-id="aaa8a-117">Trabalho</span><span class="sxs-lookup"><span data-stu-id="aaa8a-117">Job</span></span><br/>     |
| <span data-ttu-id="aaa8a-118">Observações</span><span class="sxs-lookup"><span data-stu-id="aaa8a-118">Notes</span></span> <br/>          | <span data-ttu-id="aaa8a-119">Nenhum</span><span class="sxs-lookup"><span data-stu-id="aaa8a-119">None</span></span><br/>    |



 

## <a name="structural-content"></a><span data-ttu-id="aaa8a-120">Conteúdo estrutural</span><span class="sxs-lookup"><span data-stu-id="aaa8a-120">Structural Content</span></span>

<span data-ttu-id="aaa8a-121">A estrutura XML desse elemento é:</span><span class="sxs-lookup"><span data-stu-id="aaa8a-121">The XML structure of this element is:</span></span>

``` syntax
<psf:Feature name="psk:JobOutputBin">
  <psf:Property name="psf:SelectionType">
    <psf:Value xsi:type="xs:string">psk:PickOne</psf:Value>
  </psf:Property>
  <psf:Option name="psk:_OptionName_">
    <psf:Property name="psf:IdentityOption">
      <psf:Value xsi:type="xs:string">_IdentityOptionValue_</psf:Value>
    </psf:Property>
    <psf:ScoredProperty name="psk:BinType">
      <psf:Value xsi:type="xs:string">_BinTypeValue_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSheetCapacity">
      <psf:Value xsi:type="xs:integer">_MediaSheetCapacityValue_</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
</psf:Feature>
      
```

## <a name="structure-variables"></a><span data-ttu-id="aaa8a-122">Variáveis de estrutura</span><span class="sxs-lookup"><span data-stu-id="aaa8a-122">Structure Variables</span></span>

<span data-ttu-id="aaa8a-123">A tabela a seguir descreve as características das variáveis definidas na estrutura XML.</span><span class="sxs-lookup"><span data-stu-id="aaa8a-123">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="aaa8a-124">Nome</span><span class="sxs-lookup"><span data-stu-id="aaa8a-124">Name</span></span>                                   | <span data-ttu-id="aaa8a-125">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="aaa8a-125">Data type</span></span>          | <span data-ttu-id="aaa8a-126">Unidade</span><span class="sxs-lookup"><span data-stu-id="aaa8a-126">Unit</span></span>                  | <span data-ttu-id="aaa8a-127">Valores com suporte</span><span class="sxs-lookup"><span data-stu-id="aaa8a-127">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="aaa8a-128">Resumo</span><span class="sxs-lookup"><span data-stu-id="aaa8a-128">Summary</span></span>                                                                             |
|----------------------------------------|--------------------|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="aaa8a-129">\_OptionName\_</span><span class="sxs-lookup"><span data-stu-id="aaa8a-129">\_OptionName\_</span></span><br/>              | <span data-ttu-id="aaa8a-130">string</span><span class="sxs-lookup"><span data-stu-id="aaa8a-130">string</span></span><br/>  | <span data-ttu-id="aaa8a-131">characters</span><span class="sxs-lookup"><span data-stu-id="aaa8a-131">characters</span></span><br/> | <span data-ttu-id="aaa8a-132">Nome totalmente qualificado válido, conforme definido pelos [namespaces em XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span><span class="sxs-lookup"><span data-stu-id="aaa8a-132">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="aaa8a-133">Se nenhum namespace for especificado, o namespace padrão será assumido.</span><span class="sxs-lookup"><span data-stu-id="aaa8a-133">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="aaa8a-134">O nome da opção.</span><span class="sxs-lookup"><span data-stu-id="aaa8a-134">The name of the option.</span></span><br/>                                                  |
| <span data-ttu-id="aaa8a-135">\_IdentityOptionValue\_</span><span class="sxs-lookup"><span data-stu-id="aaa8a-135">\_IdentityOptionValue\_</span></span><br/>     | <span data-ttu-id="aaa8a-136">string</span><span class="sxs-lookup"><span data-stu-id="aaa8a-136">string</span></span><br/>  | <span data-ttu-id="aaa8a-137">n/d</span><span class="sxs-lookup"><span data-stu-id="aaa8a-137">n/a</span></span><br/>        | <span data-ttu-id="aaa8a-138">True, False.</span><span class="sxs-lookup"><span data-stu-id="aaa8a-138">True, False.</span></span><br/>                                                                                                                                                               | <span data-ttu-id="aaa8a-139">Define uma opção que, quando selecionada, desabilita esse recurso.</span><span class="sxs-lookup"><span data-stu-id="aaa8a-139">Defines an Option which when selected would disable this feature.</span></span><br/>        |
| <span data-ttu-id="aaa8a-140">\_BinTypeValue\_</span><span class="sxs-lookup"><span data-stu-id="aaa8a-140">\_BinTypeValue\_</span></span><br/>            | <span data-ttu-id="aaa8a-141">string</span><span class="sxs-lookup"><span data-stu-id="aaa8a-141">string</span></span><br/>  | <span data-ttu-id="aaa8a-142">n/d</span><span class="sxs-lookup"><span data-stu-id="aaa8a-142">n/a</span></span><br/>        | <span data-ttu-id="aaa8a-143">Caixa de correio, classificador, empilhador, finalizador, nenhum.</span><span class="sxs-lookup"><span data-stu-id="aaa8a-143">MailBox, Sorter, Stacker, Finisher, None.</span></span><br/>                                                                                                                                  | <span data-ttu-id="aaa8a-144">Especifica o tipo geral do compartimento.</span><span class="sxs-lookup"><span data-stu-id="aaa8a-144">Specifies the general type of the bin.</span></span><br/>                                   |
| <span data-ttu-id="aaa8a-145">\_MediaSheetCapacityValue\_</span><span class="sxs-lookup"><span data-stu-id="aaa8a-145">\_MediaSheetCapacityValue\_</span></span><br/> | <span data-ttu-id="aaa8a-146">Número inteiro</span><span class="sxs-lookup"><span data-stu-id="aaa8a-146">integer</span></span><br/> | <span data-ttu-id="aaa8a-147">folhas</span><span class="sxs-lookup"><span data-stu-id="aaa8a-147">sheets</span></span><br/>     | <span data-ttu-id="aaa8a-148">Restrição de inteiro máximo permitida pelo dispositivo.</span><span class="sxs-lookup"><span data-stu-id="aaa8a-148">Maximum integer constraint allowed by device.</span></span><br/>                                                                                                                              | <span data-ttu-id="aaa8a-149">Especifica a capacidade de mídia no número de páginas (nível completo) do compartimento.</span><span class="sxs-lookup"><span data-stu-id="aaa8a-149">Specifies the Media capacity in number of pages (full level) of the bin.</span></span><br/> |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="aaa8a-150">Conteúdo de linguagem XML (XML)</span><span class="sxs-lookup"><span data-stu-id="aaa8a-150">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="aaa8a-151">As palavras-chave do esquema de impressão pública são definidas no https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span><span class="sxs-lookup"><span data-stu-id="aaa8a-151">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="aaa8a-152">O conteúdo do linguagem XML público (XML) para essa palavra-chave é definido abaixo:</span><span class="sxs-lookup"><span data-stu-id="aaa8a-152">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

``` syntax
<psf:Feature name="psk:JobOutputBin">
  <psf:Property name="psf:SelectionType">
    <psf:Value xsi:type="xs:string">psk:PickOne</psf:Value>
  </psf:Property>
  <psf:Option>
    <psf:ScoredProperty name="psk:BinType">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>  
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSheetCapacity">
      <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>  
    </psf:ScoredProperty>
  </psf:Option>
</psf:Feature>
    
```

## <a name="related-topics"></a><span data-ttu-id="aaa8a-153">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="aaa8a-153">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="aaa8a-154">Especificação de esquema de impressão</span><span class="sxs-lookup"><span data-stu-id="aaa8a-154">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




