---
description: Este tópico não é atual. Para obter as informações mais atuais, consulte a especificação do esquema de impressão.
ms.assetid: c5050804-0e77-4d26-bf00-5d9690102b18
title: PageOutputBin
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 557a742604f6e643e8812493049b7f2b118e262c
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/26/2021
ms.locfileid: "107997523"
---
# <a name="pageoutputbin"></a><span data-ttu-id="6618f-104">PageOutputBin</span><span class="sxs-lookup"><span data-stu-id="6618f-104">PageOutputBin</span></span>

<span data-ttu-id="6618f-105">Este tópico não é atual.</span><span class="sxs-lookup"><span data-stu-id="6618f-105">This topic is not current.</span></span> <span data-ttu-id="6618f-106">Para obter as informações mais atuais, consulte a [especificação do esquema de impressão](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="6618f-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="6618f-107">Descreve a lista completa de compartimentos com suporte para o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="6618f-107">Describes the full list of supported bins for the device.</span></span> <span data-ttu-id="6618f-108">Permite a especificação do compartimento de saída por página.</span><span class="sxs-lookup"><span data-stu-id="6618f-108">Allows specification of output bin on a per page basis.</span></span> <span data-ttu-id="6618f-109">As palavras-chave JobOutputBin, DocumentOutputBin e PageOutputBin são mutuamente exclusivas apenas uma deve ser especificada em um documento de recursos de impressão ou PrintTicket.</span><span class="sxs-lookup"><span data-stu-id="6618f-109">The JobOutputBin, DocumentOutputBin and PageOutputBin keywords are mutually exclusive only one should be specified in a PrintTicket or Print Capabilities document.</span></span>

-   [<span data-ttu-id="6618f-110">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="6618f-110">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="6618f-111">Conteúdo estrutural</span><span class="sxs-lookup"><span data-stu-id="6618f-111">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="6618f-112">Conteúdo de linguagem XML (XML)</span><span class="sxs-lookup"><span data-stu-id="6618f-112">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="6618f-113">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="6618f-113">Element Information</span></span>



| <span data-ttu-id="6618f-114">Nome</span><span class="sxs-lookup"><span data-stu-id="6618f-114">Name</span></span> | <span data-ttu-id="6618f-115">Valor</span><span class="sxs-lookup"><span data-stu-id="6618f-115">Value</span></span> |
|----------------------------|--------------------|
| <span data-ttu-id="6618f-116">Tipo de elemento</span><span class="sxs-lookup"><span data-stu-id="6618f-116">Element Type</span></span> <br/>   | <span data-ttu-id="6618f-117">Recurso</span><span class="sxs-lookup"><span data-stu-id="6618f-117">Feature</span></span><br/> |
| <span data-ttu-id="6618f-118">Prefixo de escopo</span><span class="sxs-lookup"><span data-stu-id="6618f-118">Scoping Prefix</span></span> <br/> | <span data-ttu-id="6618f-119">?</span><span class="sxs-lookup"><span data-stu-id="6618f-119">Page</span></span><br/>    |
| <span data-ttu-id="6618f-120">Observações</span><span class="sxs-lookup"><span data-stu-id="6618f-120">Notes</span></span> <br/>          | <span data-ttu-id="6618f-121">Nenhum</span><span class="sxs-lookup"><span data-stu-id="6618f-121">None</span></span><br/>    |



 

## <a name="structural-content"></a><span data-ttu-id="6618f-122">Conteúdo estrutural</span><span class="sxs-lookup"><span data-stu-id="6618f-122">Structural Content</span></span>

<span data-ttu-id="6618f-123">A estrutura XML desse elemento é:</span><span class="sxs-lookup"><span data-stu-id="6618f-123">The XML structure of this element is:</span></span>

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

## <a name="structure-variables"></a><span data-ttu-id="6618f-124">Variáveis de estrutura</span><span class="sxs-lookup"><span data-stu-id="6618f-124">Structure Variables</span></span>

<span data-ttu-id="6618f-125">A tabela a seguir descreve as características das variáveis definidas na estrutura XML.</span><span class="sxs-lookup"><span data-stu-id="6618f-125">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="6618f-126">Nome</span><span class="sxs-lookup"><span data-stu-id="6618f-126">Name</span></span>                                   | <span data-ttu-id="6618f-127">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="6618f-127">Data type</span></span>          | <span data-ttu-id="6618f-128">Unidade</span><span class="sxs-lookup"><span data-stu-id="6618f-128">Unit</span></span>                  | <span data-ttu-id="6618f-129">Valores com suporte</span><span class="sxs-lookup"><span data-stu-id="6618f-129">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="6618f-130">Resumo</span><span class="sxs-lookup"><span data-stu-id="6618f-130">Summary</span></span>                                                                             |
|----------------------------------------|--------------------|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="6618f-131">\_OptionName\_</span><span class="sxs-lookup"><span data-stu-id="6618f-131">\_OptionName\_</span></span><br/>              | <span data-ttu-id="6618f-132">string</span><span class="sxs-lookup"><span data-stu-id="6618f-132">string</span></span><br/>  | <span data-ttu-id="6618f-133">characters</span><span class="sxs-lookup"><span data-stu-id="6618f-133">characters</span></span><br/> | <span data-ttu-id="6618f-134">Nome totalmente qualificado válido, conforme definido pelos [namespaces em XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span><span class="sxs-lookup"><span data-stu-id="6618f-134">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="6618f-135">Se nenhum namespace for especificado, o namespace padrão será assumido.</span><span class="sxs-lookup"><span data-stu-id="6618f-135">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="6618f-136">O nome da opção.</span><span class="sxs-lookup"><span data-stu-id="6618f-136">The name of the option.</span></span><br/>                                                  |
| <span data-ttu-id="6618f-137">\_IdentityOptionValue\_</span><span class="sxs-lookup"><span data-stu-id="6618f-137">\_IdentityOptionValue\_</span></span><br/>     | <span data-ttu-id="6618f-138">string</span><span class="sxs-lookup"><span data-stu-id="6618f-138">string</span></span><br/>  | <span data-ttu-id="6618f-139">N/D</span><span class="sxs-lookup"><span data-stu-id="6618f-139">n/a</span></span><br/>        | <span data-ttu-id="6618f-140">True, False.</span><span class="sxs-lookup"><span data-stu-id="6618f-140">True, False.</span></span><br/>                                                                                                                                                               | <span data-ttu-id="6618f-141">Define uma opção que, quando selecionada, desabilita esse recurso.</span><span class="sxs-lookup"><span data-stu-id="6618f-141">Defines an Option which when selected would disable this feature.</span></span><br/>        |
| <span data-ttu-id="6618f-142">\_BinTypeValue\_</span><span class="sxs-lookup"><span data-stu-id="6618f-142">\_BinTypeValue\_</span></span><br/>            | <span data-ttu-id="6618f-143">string</span><span class="sxs-lookup"><span data-stu-id="6618f-143">string</span></span><br/>  | <span data-ttu-id="6618f-144">N/D</span><span class="sxs-lookup"><span data-stu-id="6618f-144">n/a</span></span><br/>        | <span data-ttu-id="6618f-145">FaceDownTray, FaceUpTray, caixa de correio, classificador, empilhador, terminador nenhum.</span><span class="sxs-lookup"><span data-stu-id="6618f-145">FaceDownTray, FaceUpTray, MailBox, Sorter, Stacker, Finisher None.</span></span><br/>                                                                                                         | <span data-ttu-id="6618f-146">Especifica o tipo geral do compartimento.</span><span class="sxs-lookup"><span data-stu-id="6618f-146">Specifies the general type of the bin.</span></span><br/>                                   |
| <span data-ttu-id="6618f-147">\_MediaSheetCapacityValue\_</span><span class="sxs-lookup"><span data-stu-id="6618f-147">\_MediaSheetCapacityValue\_</span></span><br/> | <span data-ttu-id="6618f-148">Número inteiro</span><span class="sxs-lookup"><span data-stu-id="6618f-148">integer</span></span><br/> | <span data-ttu-id="6618f-149">folhas</span><span class="sxs-lookup"><span data-stu-id="6618f-149">sheets</span></span><br/>     | <span data-ttu-id="6618f-150">Maior que 0.</span><span class="sxs-lookup"><span data-stu-id="6618f-150">Greater than 0.</span></span><br/>                                                                                                                                                            | <span data-ttu-id="6618f-151">Especifica a capacidade de mídia no número de páginas (nível completo) do compartimento.</span><span class="sxs-lookup"><span data-stu-id="6618f-151">Specifies the Media capacity in number of pages (full level) of the bin.</span></span><br/> |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="6618f-152">Conteúdo de linguagem XML (XML)</span><span class="sxs-lookup"><span data-stu-id="6618f-152">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="6618f-153">As palavras-chave do esquema de impressão pública são definidas no https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span><span class="sxs-lookup"><span data-stu-id="6618f-153">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="6618f-154">O conteúdo do linguagem XML público (XML) para essa palavra-chave é definido abaixo:</span><span class="sxs-lookup"><span data-stu-id="6618f-154">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

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

## <a name="related-topics"></a><span data-ttu-id="6618f-155">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="6618f-155">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6618f-156">Especificação de esquema de impressão</span><span class="sxs-lookup"><span data-stu-id="6618f-156">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




