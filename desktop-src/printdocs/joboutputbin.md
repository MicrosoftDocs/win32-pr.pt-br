---
description: Este tópico não é atual. Para obter as informações mais atuais, consulte a especificação do esquema de impressão.
ms.assetid: 324ec426-b7c8-43af-96b9-74929358e262
title: JobOutputBin
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 973433ac7f6e051d4656777696cc3a37cedd953b
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/26/2021
ms.locfileid: "107999213"
---
# <a name="joboutputbin"></a><span data-ttu-id="42309-104">JobOutputBin</span><span class="sxs-lookup"><span data-stu-id="42309-104">JobOutputBin</span></span>

<span data-ttu-id="42309-105">Este tópico não é atual.</span><span class="sxs-lookup"><span data-stu-id="42309-105">This topic is not current.</span></span> <span data-ttu-id="42309-106">Para obter as informações mais atuais, consulte a [especificação do esquema de impressão](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="42309-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="42309-107">Descreve a bandeja de saída instalada em um dispositivo ou a lista completa de compartimentos com suporte para um dispositivo.</span><span class="sxs-lookup"><span data-stu-id="42309-107">Describes the installed output bin in a device or the full list of supported bins for a device.</span></span> <span data-ttu-id="42309-108">As palavras-chave JobOutputBin, DocumentOutputBin e PageOutputBin são mutuamente exclusivas apenas uma deve ser especificada em um documento de recursos de impressão ou PrintTicket.</span><span class="sxs-lookup"><span data-stu-id="42309-108">The JobOutputBin, DocumentOutputBin and PageOutputBin keywords are mutually exclusive only one should be specified in a PrintTicket or Print Capabilities document.</span></span>

-   [<span data-ttu-id="42309-109">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="42309-109">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="42309-110">Conteúdo estrutural</span><span class="sxs-lookup"><span data-stu-id="42309-110">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="42309-111">Conteúdo de linguagem XML (XML)</span><span class="sxs-lookup"><span data-stu-id="42309-111">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="42309-112">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="42309-112">Element Information</span></span>



| <span data-ttu-id="42309-113">Nome</span><span class="sxs-lookup"><span data-stu-id="42309-113">Name</span></span> | <span data-ttu-id="42309-114">Valor</span><span class="sxs-lookup"><span data-stu-id="42309-114">Value</span></span> |
|----------------------------|--------------------|
| <span data-ttu-id="42309-115">Tipo de elemento</span><span class="sxs-lookup"><span data-stu-id="42309-115">Element Type</span></span> <br/>   | <span data-ttu-id="42309-116">Recurso</span><span class="sxs-lookup"><span data-stu-id="42309-116">Feature</span></span><br/> |
| <span data-ttu-id="42309-117">Prefixo de escopo</span><span class="sxs-lookup"><span data-stu-id="42309-117">Scoping Prefix</span></span> <br/> | <span data-ttu-id="42309-118">Trabalho</span><span class="sxs-lookup"><span data-stu-id="42309-118">Job</span></span><br/>     |
| <span data-ttu-id="42309-119">Observações</span><span class="sxs-lookup"><span data-stu-id="42309-119">Notes</span></span> <br/>          | <span data-ttu-id="42309-120">Nenhum</span><span class="sxs-lookup"><span data-stu-id="42309-120">None</span></span><br/>    |



 

## <a name="structural-content"></a><span data-ttu-id="42309-121">Conteúdo estrutural</span><span class="sxs-lookup"><span data-stu-id="42309-121">Structural Content</span></span>

<span data-ttu-id="42309-122">A estrutura XML desse elemento é:</span><span class="sxs-lookup"><span data-stu-id="42309-122">The XML structure of this element is:</span></span>

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

## <a name="structure-variables"></a><span data-ttu-id="42309-123">Variáveis de estrutura</span><span class="sxs-lookup"><span data-stu-id="42309-123">Structure Variables</span></span>

<span data-ttu-id="42309-124">A tabela a seguir descreve as características das variáveis definidas na estrutura XML.</span><span class="sxs-lookup"><span data-stu-id="42309-124">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="42309-125">Nome</span><span class="sxs-lookup"><span data-stu-id="42309-125">Name</span></span>                                   | <span data-ttu-id="42309-126">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="42309-126">Data type</span></span>          | <span data-ttu-id="42309-127">Unidade</span><span class="sxs-lookup"><span data-stu-id="42309-127">Unit</span></span>                  | <span data-ttu-id="42309-128">Valores com suporte</span><span class="sxs-lookup"><span data-stu-id="42309-128">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="42309-129">Resumo</span><span class="sxs-lookup"><span data-stu-id="42309-129">Summary</span></span>                                                                             |
|----------------------------------------|--------------------|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="42309-130">\_OptionName\_</span><span class="sxs-lookup"><span data-stu-id="42309-130">\_OptionName\_</span></span><br/>              | <span data-ttu-id="42309-131">string</span><span class="sxs-lookup"><span data-stu-id="42309-131">string</span></span><br/>  | <span data-ttu-id="42309-132">characters</span><span class="sxs-lookup"><span data-stu-id="42309-132">characters</span></span><br/> | <span data-ttu-id="42309-133">Nome totalmente qualificado válido, conforme definido pelos [namespaces em XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span><span class="sxs-lookup"><span data-stu-id="42309-133">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="42309-134">Se nenhum namespace for especificado, o namespace padrão será assumido.</span><span class="sxs-lookup"><span data-stu-id="42309-134">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="42309-135">O nome da opção.</span><span class="sxs-lookup"><span data-stu-id="42309-135">The name of the option.</span></span><br/>                                                  |
| <span data-ttu-id="42309-136">\_IdentityOptionValue\_</span><span class="sxs-lookup"><span data-stu-id="42309-136">\_IdentityOptionValue\_</span></span><br/>     | <span data-ttu-id="42309-137">string</span><span class="sxs-lookup"><span data-stu-id="42309-137">string</span></span><br/>  | <span data-ttu-id="42309-138">N/D</span><span class="sxs-lookup"><span data-stu-id="42309-138">n/a</span></span><br/>        | <span data-ttu-id="42309-139">True, False.</span><span class="sxs-lookup"><span data-stu-id="42309-139">True, False.</span></span><br/>                                                                                                                                                               | <span data-ttu-id="42309-140">Define uma opção que, quando selecionada, desabilita esse recurso.</span><span class="sxs-lookup"><span data-stu-id="42309-140">Defines an Option which when selected would disable this feature.</span></span><br/>        |
| <span data-ttu-id="42309-141">\_BinTypeValue\_</span><span class="sxs-lookup"><span data-stu-id="42309-141">\_BinTypeValue\_</span></span><br/>            | <span data-ttu-id="42309-142">string</span><span class="sxs-lookup"><span data-stu-id="42309-142">string</span></span><br/>  | <span data-ttu-id="42309-143">N/D</span><span class="sxs-lookup"><span data-stu-id="42309-143">n/a</span></span><br/>        | <span data-ttu-id="42309-144">Caixa de correio, classificador, empilhador, finalizador, nenhum.</span><span class="sxs-lookup"><span data-stu-id="42309-144">MailBox, Sorter, Stacker, Finisher, None.</span></span><br/>                                                                                                                                  | <span data-ttu-id="42309-145">Especifica o tipo geral do compartimento.</span><span class="sxs-lookup"><span data-stu-id="42309-145">Specifies the general type of the bin.</span></span><br/>                                   |
| <span data-ttu-id="42309-146">\_MediaSheetCapacityValue\_</span><span class="sxs-lookup"><span data-stu-id="42309-146">\_MediaSheetCapacityValue\_</span></span><br/> | <span data-ttu-id="42309-147">Número inteiro</span><span class="sxs-lookup"><span data-stu-id="42309-147">integer</span></span><br/> | <span data-ttu-id="42309-148">folhas</span><span class="sxs-lookup"><span data-stu-id="42309-148">sheets</span></span><br/>     | <span data-ttu-id="42309-149">Restrição de inteiro máximo permitida pelo dispositivo.</span><span class="sxs-lookup"><span data-stu-id="42309-149">Maximum integer constraint allowed by device.</span></span><br/>                                                                                                                              | <span data-ttu-id="42309-150">Especifica a capacidade de mídia no número de páginas (nível completo) do compartimento.</span><span class="sxs-lookup"><span data-stu-id="42309-150">Specifies the Media capacity in number of pages (full level) of the bin.</span></span><br/> |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="42309-151">Conteúdo de linguagem XML (XML)</span><span class="sxs-lookup"><span data-stu-id="42309-151">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="42309-152">As palavras-chave do esquema de impressão pública são definidas no https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span><span class="sxs-lookup"><span data-stu-id="42309-152">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="42309-153">O conteúdo do linguagem XML público (XML) para essa palavra-chave é definido abaixo:</span><span class="sxs-lookup"><span data-stu-id="42309-153">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

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

## <a name="related-topics"></a><span data-ttu-id="42309-154">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="42309-154">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="42309-155">Especificação de esquema de impressão</span><span class="sxs-lookup"><span data-stu-id="42309-155">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




