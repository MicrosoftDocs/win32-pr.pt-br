---
description: Este tópico não é atual. Para obter as informações mais atuais, consulte a especificação do esquema de impressão.
ms.assetid: c5050804-0e77-4d26-bf00-5d9690102b18
title: PageOutputBin
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a2bae72b69f83697cc2f482f21995acb587a2ace
ms.sourcegitcommit: 7b8f6151ebe247536304866459b2973276271d4d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/06/2021
ms.locfileid: "104172600"
---
# <a name="pageoutputbin"></a><span data-ttu-id="2fa65-104">PageOutputBin</span><span class="sxs-lookup"><span data-stu-id="2fa65-104">PageOutputBin</span></span>

<span data-ttu-id="2fa65-105">Este tópico não é atual.</span><span class="sxs-lookup"><span data-stu-id="2fa65-105">This topic is not current.</span></span> <span data-ttu-id="2fa65-106">Para obter as informações mais atuais, consulte a [especificação do esquema de impressão](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="2fa65-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="2fa65-107">Descreve a lista completa de compartimentos com suporte para o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="2fa65-107">Describes the full list of supported bins for the device.</span></span> <span data-ttu-id="2fa65-108">Permite a especificação do compartimento de saída por página.</span><span class="sxs-lookup"><span data-stu-id="2fa65-108">Allows specification of output bin on a per page basis.</span></span> <span data-ttu-id="2fa65-109">As palavras-chave JobOutputBin, DocumentOutputBin e PageOutputBin são mutuamente exclusivas apenas uma deve ser especificada em um documento de recursos de impressão ou PrintTicket.</span><span class="sxs-lookup"><span data-stu-id="2fa65-109">The JobOutputBin, DocumentOutputBin and PageOutputBin keywords are mutually exclusive only one should be specified in a PrintTicket or Print Capabilities document.</span></span>

-   [<span data-ttu-id="2fa65-110">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="2fa65-110">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="2fa65-111">Conteúdo estrutural</span><span class="sxs-lookup"><span data-stu-id="2fa65-111">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="2fa65-112">Conteúdo de linguagem XML (XML)</span><span class="sxs-lookup"><span data-stu-id="2fa65-112">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="2fa65-113">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="2fa65-113">Element Information</span></span>



| <span data-ttu-id="2fa65-114">Nome</span><span class="sxs-lookup"><span data-stu-id="2fa65-114">Name</span></span>                       |                    |
|----------------------------|--------------------|
| <span data-ttu-id="2fa65-115">Tipo de elemento</span><span class="sxs-lookup"><span data-stu-id="2fa65-115">Element Type</span></span> <br/>   | <span data-ttu-id="2fa65-116">Recurso</span><span class="sxs-lookup"><span data-stu-id="2fa65-116">Feature</span></span><br/> |
| <span data-ttu-id="2fa65-117">Prefixo de escopo</span><span class="sxs-lookup"><span data-stu-id="2fa65-117">Scoping Prefix</span></span> <br/> | <span data-ttu-id="2fa65-118">?</span><span class="sxs-lookup"><span data-stu-id="2fa65-118">Page</span></span><br/>    |
| <span data-ttu-id="2fa65-119">Observações</span><span class="sxs-lookup"><span data-stu-id="2fa65-119">Notes</span></span> <br/>          | <span data-ttu-id="2fa65-120">Nenhum</span><span class="sxs-lookup"><span data-stu-id="2fa65-120">None</span></span><br/>    |



 

## <a name="structural-content"></a><span data-ttu-id="2fa65-121">Conteúdo estrutural</span><span class="sxs-lookup"><span data-stu-id="2fa65-121">Structural Content</span></span>

<span data-ttu-id="2fa65-122">A estrutura XML desse elemento é:</span><span class="sxs-lookup"><span data-stu-id="2fa65-122">The XML structure of this element is:</span></span>

``` syntax
<psf:Feature name="psk:PageOutputBin">
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

## <a name="structure-variables"></a><span data-ttu-id="2fa65-123">Variáveis de estrutura</span><span class="sxs-lookup"><span data-stu-id="2fa65-123">Structure Variables</span></span>

<span data-ttu-id="2fa65-124">A tabela a seguir descreve as características das variáveis definidas na estrutura XML.</span><span class="sxs-lookup"><span data-stu-id="2fa65-124">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="2fa65-125">Nome</span><span class="sxs-lookup"><span data-stu-id="2fa65-125">Name</span></span>                                   | <span data-ttu-id="2fa65-126">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="2fa65-126">Data type</span></span>          | <span data-ttu-id="2fa65-127">Unidade</span><span class="sxs-lookup"><span data-stu-id="2fa65-127">Unit</span></span>                  | <span data-ttu-id="2fa65-128">Valores com suporte</span><span class="sxs-lookup"><span data-stu-id="2fa65-128">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="2fa65-129">Resumo</span><span class="sxs-lookup"><span data-stu-id="2fa65-129">Summary</span></span>                                                                             |
|----------------------------------------|--------------------|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="2fa65-130">\_OptionName\_</span><span class="sxs-lookup"><span data-stu-id="2fa65-130">\_OptionName\_</span></span><br/>              | <span data-ttu-id="2fa65-131">string</span><span class="sxs-lookup"><span data-stu-id="2fa65-131">string</span></span><br/>  | <span data-ttu-id="2fa65-132">characters</span><span class="sxs-lookup"><span data-stu-id="2fa65-132">characters</span></span><br/> | <span data-ttu-id="2fa65-133">Nome totalmente qualificado válido, conforme definido pelos [namespaces em XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span><span class="sxs-lookup"><span data-stu-id="2fa65-133">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="2fa65-134">Se nenhum namespace for especificado, o namespace padrão será assumido.</span><span class="sxs-lookup"><span data-stu-id="2fa65-134">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="2fa65-135">O nome da opção.</span><span class="sxs-lookup"><span data-stu-id="2fa65-135">The name of the option.</span></span><br/>                                                  |
| <span data-ttu-id="2fa65-136">\_IdentityOptionValue\_</span><span class="sxs-lookup"><span data-stu-id="2fa65-136">\_IdentityOptionValue\_</span></span><br/>     | <span data-ttu-id="2fa65-137">string</span><span class="sxs-lookup"><span data-stu-id="2fa65-137">string</span></span><br/>  | <span data-ttu-id="2fa65-138">N/D</span><span class="sxs-lookup"><span data-stu-id="2fa65-138">n/a</span></span><br/>        | <span data-ttu-id="2fa65-139">True, False.</span><span class="sxs-lookup"><span data-stu-id="2fa65-139">True, False.</span></span><br/>                                                                                                                                                               | <span data-ttu-id="2fa65-140">Define uma opção que, quando selecionada, desabilita esse recurso.</span><span class="sxs-lookup"><span data-stu-id="2fa65-140">Defines an Option which when selected would disable this feature.</span></span><br/>        |
| <span data-ttu-id="2fa65-141">\_BinTypeValue\_</span><span class="sxs-lookup"><span data-stu-id="2fa65-141">\_BinTypeValue\_</span></span><br/>            | <span data-ttu-id="2fa65-142">string</span><span class="sxs-lookup"><span data-stu-id="2fa65-142">string</span></span><br/>  | <span data-ttu-id="2fa65-143">N/D</span><span class="sxs-lookup"><span data-stu-id="2fa65-143">n/a</span></span><br/>        | <span data-ttu-id="2fa65-144">FaceDownTray, FaceUpTray, caixa de correio, classificador, empilhador, terminador nenhum.</span><span class="sxs-lookup"><span data-stu-id="2fa65-144">FaceDownTray, FaceUpTray, MailBox, Sorter, Stacker, Finisher None.</span></span><br/>                                                                                                         | <span data-ttu-id="2fa65-145">Especifica o tipo geral do compartimento.</span><span class="sxs-lookup"><span data-stu-id="2fa65-145">Specifies the general type of the bin.</span></span><br/>                                   |
| <span data-ttu-id="2fa65-146">\_MediaSheetCapacityValue\_</span><span class="sxs-lookup"><span data-stu-id="2fa65-146">\_MediaSheetCapacityValue\_</span></span><br/> | <span data-ttu-id="2fa65-147">Número inteiro</span><span class="sxs-lookup"><span data-stu-id="2fa65-147">integer</span></span><br/> | <span data-ttu-id="2fa65-148">folhas</span><span class="sxs-lookup"><span data-stu-id="2fa65-148">sheets</span></span><br/>     | <span data-ttu-id="2fa65-149">Maior que 0.</span><span class="sxs-lookup"><span data-stu-id="2fa65-149">Greater than 0.</span></span><br/>                                                                                                                                                            | <span data-ttu-id="2fa65-150">Especifica a capacidade de mídia no número de páginas (nível completo) do compartimento.</span><span class="sxs-lookup"><span data-stu-id="2fa65-150">Specifies the Media capacity in number of pages (full level) of the bin.</span></span><br/> |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="2fa65-151">Conteúdo de linguagem XML (XML)</span><span class="sxs-lookup"><span data-stu-id="2fa65-151">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="2fa65-152">As palavras-chave do esquema de impressão pública são definidas no https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span><span class="sxs-lookup"><span data-stu-id="2fa65-152">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="2fa65-153">O conteúdo do linguagem XML público (XML) para essa palavra-chave é definido abaixo:</span><span class="sxs-lookup"><span data-stu-id="2fa65-153">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

``` syntax
<psf:Feature name="psk:PageOutputBin">
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

## <a name="related-topics"></a><span data-ttu-id="2fa65-154">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="2fa65-154">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2fa65-155">Especificação de esquema de impressão</span><span class="sxs-lookup"><span data-stu-id="2fa65-155">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




