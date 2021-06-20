---
description: Saiba mais sobre o DocumentOutputBin, que descreve a lista completa de compartimentos com suporte para o dispositivo e permite a especificação do compartimento de saída por documento.
ms.assetid: 73840548-f68b-4af8-acb4-6f7faa2e8879
title: DocumentOutputBin
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2afc20f15aed8d3076afb79d755c54791573b393
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/19/2021
ms.locfileid: "112409239"
---
# <a name="documentoutputbin"></a><span data-ttu-id="90b22-103">DocumentOutputBin</span><span class="sxs-lookup"><span data-stu-id="90b22-103">DocumentOutputBin</span></span>

<span data-ttu-id="90b22-104">Este tópico não é atual.</span><span class="sxs-lookup"><span data-stu-id="90b22-104">This topic is not current.</span></span> <span data-ttu-id="90b22-105">Para obter as informações mais atuais, consulte a [especificação do esquema de impressão](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="90b22-105">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="90b22-106">Descreve a lista completa de compartimentos com suporte para o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="90b22-106">Describes the full list of supported bins for the device.</span></span> <span data-ttu-id="90b22-107">Permite a especificação do compartimento de saída por documento.</span><span class="sxs-lookup"><span data-stu-id="90b22-107">Allows specification of output bin on a per document basis.</span></span> <span data-ttu-id="90b22-108">As palavras-chave JobOutputBin, DocumentOutputBin e PageOutputBin são mutuamente exclusivas apenas uma deve ser especificada em um documento de recursos de impressão ou PrintTicket.</span><span class="sxs-lookup"><span data-stu-id="90b22-108">The JobOutputBin, DocumentOutputBin and PageOutputBin keywords are mutually exclusive only one should be specified in a PrintTicket or Print Capabilities document.</span></span>

-   [<span data-ttu-id="90b22-109">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="90b22-109">Element Information</span></span>](#element-information)

-   [<span data-ttu-id="90b22-110">Conteúdo estrutural</span><span class="sxs-lookup"><span data-stu-id="90b22-110">Structural Content</span></span>](#structural-content)

-   [<span data-ttu-id="90b22-111">Conteúdo XML</span><span class="sxs-lookup"><span data-stu-id="90b22-111">XML Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="90b22-112">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="90b22-112">Element Information</span></span>



| <span data-ttu-id="90b22-113">Name</span><span class="sxs-lookup"><span data-stu-id="90b22-113">Name</span></span> | <span data-ttu-id="90b22-114">Valor</span><span class="sxs-lookup"><span data-stu-id="90b22-114">Value</span></span> |
|----------------------------|---------------------|
| <span data-ttu-id="90b22-115">Tipo de elemento</span><span class="sxs-lookup"><span data-stu-id="90b22-115">Element Type</span></span> <br/>   | <span data-ttu-id="90b22-116">Recurso</span><span class="sxs-lookup"><span data-stu-id="90b22-116">Feature</span></span><br/>  |
| <span data-ttu-id="90b22-117">Prefixo de escopo</span><span class="sxs-lookup"><span data-stu-id="90b22-117">Scoping Prefix</span></span> <br/> | <span data-ttu-id="90b22-118">Documento</span><span class="sxs-lookup"><span data-stu-id="90b22-118">Document</span></span><br/> |
| <span data-ttu-id="90b22-119">Observações</span><span class="sxs-lookup"><span data-stu-id="90b22-119">Notes</span></span> <br/>          | <span data-ttu-id="90b22-120">Nenhum</span><span class="sxs-lookup"><span data-stu-id="90b22-120">None</span></span><br/>     |



 

## <a name="structural-content"></a><span data-ttu-id="90b22-121">Conteúdo estrutural</span><span class="sxs-lookup"><span data-stu-id="90b22-121">Structural Content</span></span>

<span data-ttu-id="90b22-122">A estrutura XML desse elemento é:</span><span class="sxs-lookup"><span data-stu-id="90b22-122">The XML structure of this element is:</span></span>

``` syntax
<psf:Feature name="psk:DocumentOutputBin">
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

## <a name="structure-variables"></a><span data-ttu-id="90b22-123">Variáveis de estrutura</span><span class="sxs-lookup"><span data-stu-id="90b22-123">Structure Variables</span></span>

<span data-ttu-id="90b22-124">A tabela a seguir descreve as características das variáveis definidas na estrutura XML.</span><span class="sxs-lookup"><span data-stu-id="90b22-124">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="90b22-125">Nome</span><span class="sxs-lookup"><span data-stu-id="90b22-125">Name</span></span>                                   | <span data-ttu-id="90b22-126">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="90b22-126">Data type</span></span>          | <span data-ttu-id="90b22-127">Unidade</span><span class="sxs-lookup"><span data-stu-id="90b22-127">Unit</span></span>                  | <span data-ttu-id="90b22-128">Valores com suporte</span><span class="sxs-lookup"><span data-stu-id="90b22-128">Supported values</span></span>                                                                                                                                                             | <span data-ttu-id="90b22-129">Resumo</span><span class="sxs-lookup"><span data-stu-id="90b22-129">Summary</span></span>                                                                             |
|----------------------------------------|--------------------|-----------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="90b22-130">\_OptionName\_</span><span class="sxs-lookup"><span data-stu-id="90b22-130">\_OptionName\_</span></span><br/>              | <span data-ttu-id="90b22-131">string</span><span class="sxs-lookup"><span data-stu-id="90b22-131">string</span></span><br/>  | <span data-ttu-id="90b22-132">characters</span><span class="sxs-lookup"><span data-stu-id="90b22-132">characters</span></span><br/> | <span data-ttu-id="90b22-133">Nome totalmente qualificado válido, conforme definido pelo https://www.w3.org/TR/1999/REC-xml-names-19990114/\#dt-qname .</span><span class="sxs-lookup"><span data-stu-id="90b22-133">Valid fully qualified name as defined by https://www.w3.org/TR/1999/REC-xml-names-19990114/\#dt-qname.</span></span> <span data-ttu-id="90b22-134">Se nenhum namespace for especificado, o namespace padrão será assumido.</span><span class="sxs-lookup"><span data-stu-id="90b22-134">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="90b22-135">O nome da opção.</span><span class="sxs-lookup"><span data-stu-id="90b22-135">The name of the option.</span></span><br/>                                                  |
| <span data-ttu-id="90b22-136">\_IdentityOptionValue\_</span><span class="sxs-lookup"><span data-stu-id="90b22-136">\_IdentityOptionValue\_</span></span><br/>     | <span data-ttu-id="90b22-137">string</span><span class="sxs-lookup"><span data-stu-id="90b22-137">string</span></span><br/>  | <span data-ttu-id="90b22-138">n/d</span><span class="sxs-lookup"><span data-stu-id="90b22-138">n/a</span></span><br/>        | <span data-ttu-id="90b22-139">True, False.</span><span class="sxs-lookup"><span data-stu-id="90b22-139">True, False.</span></span><br/>                                                                                                                                                      | <span data-ttu-id="90b22-140">Define uma opção que, quando selecionada, desabilita esse recurso.</span><span class="sxs-lookup"><span data-stu-id="90b22-140">Defines an Option which when selected would disable this feature.</span></span><br/>        |
| <span data-ttu-id="90b22-141">\_BinTypeValue\_</span><span class="sxs-lookup"><span data-stu-id="90b22-141">\_BinTypeValue\_</span></span><br/>            | <span data-ttu-id="90b22-142">string</span><span class="sxs-lookup"><span data-stu-id="90b22-142">string</span></span><br/>  | <span data-ttu-id="90b22-143">n/d</span><span class="sxs-lookup"><span data-stu-id="90b22-143">n/a</span></span><br/>        | <span data-ttu-id="90b22-144">Caixa de correio, classificador, empilhador, finalizador, nenhum.</span><span class="sxs-lookup"><span data-stu-id="90b22-144">MailBox, Sorter, Stacker, Finisher, None.</span></span><br/>                                                                                                                         | <span data-ttu-id="90b22-145">Especifica o tipo geral do compartimento.</span><span class="sxs-lookup"><span data-stu-id="90b22-145">Specifies the general type of the bin.</span></span><br/>                                   |
| <span data-ttu-id="90b22-146">\_MediaSheetCapacityValue\_</span><span class="sxs-lookup"><span data-stu-id="90b22-146">\_MediaSheetCapacityValue\_</span></span><br/> | <span data-ttu-id="90b22-147">Número inteiro</span><span class="sxs-lookup"><span data-stu-id="90b22-147">integer</span></span><br/> | <span data-ttu-id="90b22-148">folhas</span><span class="sxs-lookup"><span data-stu-id="90b22-148">sheets</span></span><br/>     | <span data-ttu-id="90b22-149">Maior que 0.</span><span class="sxs-lookup"><span data-stu-id="90b22-149">Greater than 0.</span></span><br/>                                                                                                                                                   | <span data-ttu-id="90b22-150">Especifica a capacidade de mídia no número de páginas (nível completo) do compartimento.</span><span class="sxs-lookup"><span data-stu-id="90b22-150">Specifies the Media capacity in number of pages (full level) of the bin.</span></span><br/> |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="90b22-151">Conteúdo de linguagem XML (XML)</span><span class="sxs-lookup"><span data-stu-id="90b22-151">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="90b22-152">As palavras-chave do esquema de impressão pública são definidas no https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span><span class="sxs-lookup"><span data-stu-id="90b22-152">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="90b22-153">O conteúdo do linguagem XML público (XML) para essa palavra-chave é definido abaixo:</span><span class="sxs-lookup"><span data-stu-id="90b22-153">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

``` syntax
<psf:Feature name="psk:DocumentOutputBin">
  <psf:Property name="psf:SelectionType">
    <psf:Value xsi:type="xs:string">psk:PickOne</psf:Value>
  </psf:Property>
  <psf:Option>
    <!--Specifies type of output bin-->
    <psf:ScoredProperty name="psk:BinType">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <!--Specifies media capacity for output bin-->
    <psf:ScoredProperty name="psk:MediaSheetCapacity">
      <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
</psf:Feature>    
```

## <a name="related-topics"></a><span data-ttu-id="90b22-154">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="90b22-154">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="90b22-155">Especificação de esquema de impressão</span><span class="sxs-lookup"><span data-stu-id="90b22-155">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




