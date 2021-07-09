---
description: Leia sobre o elemento PageOutputBin configurável pelo usuário. Este tópico não é atual. Para obter as informações mais atuais, consulte a especificação do esquema de impressão.
ms.assetid: c5050804-0e77-4d26-bf00-5d9690102b18
title: PageOutputBin
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5a9963bf2ca7a2dd60be37c797a27c6ff09b1206
ms.sourcegitcommit: 998d50f6def8a25850fc113fc8a2df903c829c5e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/09/2021
ms.locfileid: "113548994"
---
# <a name="pageoutputbin"></a><span data-ttu-id="de4e2-105">PageOutputBin</span><span class="sxs-lookup"><span data-stu-id="de4e2-105">PageOutputBin</span></span>

<span data-ttu-id="de4e2-106">Este tópico não é atual.</span><span class="sxs-lookup"><span data-stu-id="de4e2-106">This topic is not current.</span></span> <span data-ttu-id="de4e2-107">Para obter as informações mais atuais, consulte a [especificação do esquema de impressão](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="de4e2-107">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="de4e2-108">Descreve a lista completa de compartimentos com suporte para o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="de4e2-108">Describes the full list of supported bins for the device.</span></span> <span data-ttu-id="de4e2-109">Permite a especificação do compartimento de saída por página.</span><span class="sxs-lookup"><span data-stu-id="de4e2-109">Allows specification of output bin on a per page basis.</span></span> <span data-ttu-id="de4e2-110">As palavras-chave JobOutputBin, DocumentOutputBin e PageOutputBin são mutuamente exclusivas apenas uma deve ser especificada em um documento de recursos de impressão ou PrintTicket.</span><span class="sxs-lookup"><span data-stu-id="de4e2-110">The JobOutputBin, DocumentOutputBin and PageOutputBin keywords are mutually exclusive only one should be specified in a PrintTicket or Print Capabilities document.</span></span>

-   [<span data-ttu-id="de4e2-111">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="de4e2-111">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="de4e2-112">Conteúdo estrutural</span><span class="sxs-lookup"><span data-stu-id="de4e2-112">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="de4e2-113">Conteúdo de linguagem XML (XML)</span><span class="sxs-lookup"><span data-stu-id="de4e2-113">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="de4e2-114">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="de4e2-114">Element Information</span></span>



| <span data-ttu-id="de4e2-115">Nome</span><span class="sxs-lookup"><span data-stu-id="de4e2-115">Name</span></span> | <span data-ttu-id="de4e2-116">Valor</span><span class="sxs-lookup"><span data-stu-id="de4e2-116">Value</span></span> |
|----------------------------|--------------------|
| <span data-ttu-id="de4e2-117">Tipo de elemento</span><span class="sxs-lookup"><span data-stu-id="de4e2-117">Element Type</span></span> <br/>   | <span data-ttu-id="de4e2-118">Recurso</span><span class="sxs-lookup"><span data-stu-id="de4e2-118">Feature</span></span><br/> |
| <span data-ttu-id="de4e2-119">Prefixo de escopo</span><span class="sxs-lookup"><span data-stu-id="de4e2-119">Scoping Prefix</span></span> <br/> | <span data-ttu-id="de4e2-120">Página</span><span class="sxs-lookup"><span data-stu-id="de4e2-120">Page</span></span><br/>    |
| <span data-ttu-id="de4e2-121">Observações</span><span class="sxs-lookup"><span data-stu-id="de4e2-121">Notes</span></span> <br/>          | <span data-ttu-id="de4e2-122">Nenhum</span><span class="sxs-lookup"><span data-stu-id="de4e2-122">None</span></span><br/>    |



 

## <a name="structural-content"></a><span data-ttu-id="de4e2-123">Conteúdo estrutural</span><span class="sxs-lookup"><span data-stu-id="de4e2-123">Structural Content</span></span>

<span data-ttu-id="de4e2-124">A estrutura XML desse elemento é:</span><span class="sxs-lookup"><span data-stu-id="de4e2-124">The XML structure of this element is:</span></span>

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

## <a name="structure-variables"></a><span data-ttu-id="de4e2-125">Variáveis de estrutura</span><span class="sxs-lookup"><span data-stu-id="de4e2-125">Structure Variables</span></span>

<span data-ttu-id="de4e2-126">A tabela a seguir descreve as características das variáveis definidas na estrutura XML.</span><span class="sxs-lookup"><span data-stu-id="de4e2-126">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="de4e2-127">Nome</span><span class="sxs-lookup"><span data-stu-id="de4e2-127">Name</span></span>                                   | <span data-ttu-id="de4e2-128">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="de4e2-128">Data type</span></span>          | <span data-ttu-id="de4e2-129">Unidade</span><span class="sxs-lookup"><span data-stu-id="de4e2-129">Unit</span></span>                  | <span data-ttu-id="de4e2-130">Valores com suporte</span><span class="sxs-lookup"><span data-stu-id="de4e2-130">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="de4e2-131">Resumo</span><span class="sxs-lookup"><span data-stu-id="de4e2-131">Summary</span></span>                                                                             |
|----------------------------------------|--------------------|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="de4e2-132">\_OptionName\_</span><span class="sxs-lookup"><span data-stu-id="de4e2-132">\_OptionName\_</span></span><br/>              | <span data-ttu-id="de4e2-133">string</span><span class="sxs-lookup"><span data-stu-id="de4e2-133">string</span></span><br/>  | <span data-ttu-id="de4e2-134">characters</span><span class="sxs-lookup"><span data-stu-id="de4e2-134">characters</span></span><br/> | <span data-ttu-id="de4e2-135">Nome totalmente qualificado válido, conforme definido pelos [namespaces em XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span><span class="sxs-lookup"><span data-stu-id="de4e2-135">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="de4e2-136">Se nenhum namespace for especificado, o namespace padrão será assumido.</span><span class="sxs-lookup"><span data-stu-id="de4e2-136">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="de4e2-137">O nome da opção.</span><span class="sxs-lookup"><span data-stu-id="de4e2-137">The name of the option.</span></span><br/>                                                  |
| <span data-ttu-id="de4e2-138">\_IdentityOptionValue\_</span><span class="sxs-lookup"><span data-stu-id="de4e2-138">\_IdentityOptionValue\_</span></span><br/>     | <span data-ttu-id="de4e2-139">string</span><span class="sxs-lookup"><span data-stu-id="de4e2-139">string</span></span><br/>  | <span data-ttu-id="de4e2-140">n/d</span><span class="sxs-lookup"><span data-stu-id="de4e2-140">n/a</span></span><br/>        | <span data-ttu-id="de4e2-141">True, False.</span><span class="sxs-lookup"><span data-stu-id="de4e2-141">True, False.</span></span><br/>                                                                                                                                                               | <span data-ttu-id="de4e2-142">Define uma opção que, quando selecionada, desabilita esse recurso.</span><span class="sxs-lookup"><span data-stu-id="de4e2-142">Defines an Option which when selected would disable this feature.</span></span><br/>        |
| <span data-ttu-id="de4e2-143">\_BinTypeValue\_</span><span class="sxs-lookup"><span data-stu-id="de4e2-143">\_BinTypeValue\_</span></span><br/>            | <span data-ttu-id="de4e2-144">string</span><span class="sxs-lookup"><span data-stu-id="de4e2-144">string</span></span><br/>  | <span data-ttu-id="de4e2-145">n/d</span><span class="sxs-lookup"><span data-stu-id="de4e2-145">n/a</span></span><br/>        | <span data-ttu-id="de4e2-146">FaceDownTray, FaceUpTray, caixa de correio, classificador, empilhador, terminador nenhum.</span><span class="sxs-lookup"><span data-stu-id="de4e2-146">FaceDownTray, FaceUpTray, MailBox, Sorter, Stacker, Finisher None.</span></span><br/>                                                                                                         | <span data-ttu-id="de4e2-147">Especifica o tipo geral do compartimento.</span><span class="sxs-lookup"><span data-stu-id="de4e2-147">Specifies the general type of the bin.</span></span><br/>                                   |
| <span data-ttu-id="de4e2-148">\_MediaSheetCapacityValue\_</span><span class="sxs-lookup"><span data-stu-id="de4e2-148">\_MediaSheetCapacityValue\_</span></span><br/> | <span data-ttu-id="de4e2-149">Número inteiro</span><span class="sxs-lookup"><span data-stu-id="de4e2-149">integer</span></span><br/> | <span data-ttu-id="de4e2-150">folhas</span><span class="sxs-lookup"><span data-stu-id="de4e2-150">sheets</span></span><br/>     | <span data-ttu-id="de4e2-151">Maior que 0.</span><span class="sxs-lookup"><span data-stu-id="de4e2-151">Greater than 0.</span></span><br/>                                                                                                                                                            | <span data-ttu-id="de4e2-152">Especifica a capacidade de mídia no número de páginas (nível completo) do compartimento.</span><span class="sxs-lookup"><span data-stu-id="de4e2-152">Specifies the Media capacity in number of pages (full level) of the bin.</span></span><br/> |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="de4e2-153">Conteúdo de linguagem XML (XML)</span><span class="sxs-lookup"><span data-stu-id="de4e2-153">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="de4e2-154">As palavras-chave do esquema de impressão pública são definidas no https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span><span class="sxs-lookup"><span data-stu-id="de4e2-154">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="de4e2-155">O conteúdo do linguagem XML público (XML) para essa palavra-chave é definido abaixo:</span><span class="sxs-lookup"><span data-stu-id="de4e2-155">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

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

## <a name="related-topics"></a><span data-ttu-id="de4e2-156">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="de4e2-156">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="de4e2-157">Especificação de esquema de impressão</span><span class="sxs-lookup"><span data-stu-id="de4e2-157">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




