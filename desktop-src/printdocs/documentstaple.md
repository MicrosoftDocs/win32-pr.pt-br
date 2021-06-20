---
description: Saiba mais sobre o elemento JobStapleAllDocuments, que descreve as características de grampeamento da saída.
ms.assetid: 53e38979-2065-4304-a0ed-0434c8d2efc8
title: DocumentStaple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bc2cda02c452ebb053c71811fb2642cea7371b2f
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/19/2021
ms.locfileid: "112409129"
---
# <a name="documentstaple"></a><span data-ttu-id="62793-103">DocumentStaple</span><span class="sxs-lookup"><span data-stu-id="62793-103">DocumentStaple</span></span>

<span data-ttu-id="62793-104">Este tópico não é atual.</span><span class="sxs-lookup"><span data-stu-id="62793-104">This topic is not current.</span></span> <span data-ttu-id="62793-105">Para obter as informações mais atuais, consulte a [especificação do esquema de impressão](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="62793-105">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="62793-106">Descreve as características de grampeamento da saída.</span><span class="sxs-lookup"><span data-stu-id="62793-106">Describes the stapling characteristics of the output.</span></span> <span data-ttu-id="62793-107">Cada documento é grampeado separadamente.</span><span class="sxs-lookup"><span data-stu-id="62793-107">Each document is stapled separately.</span></span> <span data-ttu-id="62793-108">As palavras-chave JobStapleAllDocuments e DocumentStaple são mutuamente exclusivas.</span><span class="sxs-lookup"><span data-stu-id="62793-108">The JobStapleAllDocuments and DocumentStaple keywords are mutually exclusive.</span></span> <span data-ttu-id="62793-109">Cabe ao driver determinar o tratamento de restrições entre essas palavras-chave.</span><span class="sxs-lookup"><span data-stu-id="62793-109">It is up to the driver to determine constraint handling between these keywords.</span></span>

-   [<span data-ttu-id="62793-110">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="62793-110">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="62793-111">Conteúdo estrutural</span><span class="sxs-lookup"><span data-stu-id="62793-111">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="62793-112">Conteúdo de linguagem XML (XML)</span><span class="sxs-lookup"><span data-stu-id="62793-112">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="62793-113">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="62793-113">Element Information</span></span>



| <span data-ttu-id="62793-114">Name</span><span class="sxs-lookup"><span data-stu-id="62793-114">Name</span></span> | <span data-ttu-id="62793-115">Valor</span><span class="sxs-lookup"><span data-stu-id="62793-115">Value</span></span> |
|----------------------------|--------------------------------------------------------------------------------|
| <span data-ttu-id="62793-116">Tipo de elemento</span><span class="sxs-lookup"><span data-stu-id="62793-116">Element Type</span></span> <br/>   | <span data-ttu-id="62793-117">Recurso</span><span class="sxs-lookup"><span data-stu-id="62793-117">Feature</span></span><br/>                                                             |
| <span data-ttu-id="62793-118">Prefixo de escopo</span><span class="sxs-lookup"><span data-stu-id="62793-118">Scoping Prefix</span></span> <br/> | <span data-ttu-id="62793-119">Documento</span><span class="sxs-lookup"><span data-stu-id="62793-119">Document</span></span><br/>                                                            |
| <span data-ttu-id="62793-120">Observações</span><span class="sxs-lookup"><span data-stu-id="62793-120">Notes</span></span> <br/>          | <span data-ttu-id="62793-121">Superior, inferior, esquerda e direita são relativos ao PageImageableSize.</span><span class="sxs-lookup"><span data-stu-id="62793-121">Top, Bottom, Left, and Right are relative to the PageImageableSize.</span></span><br/> |



 

## <a name="structural-content"></a><span data-ttu-id="62793-122">Conteúdo estrutural</span><span class="sxs-lookup"><span data-stu-id="62793-122">Structural Content</span></span>

<span data-ttu-id="62793-123">A estrutura XML desse elemento é:</span><span class="sxs-lookup"><span data-stu-id="62793-123">The XML structure of this element is:</span></span>

``` syntax
<psf:Feature name="psk:DocumentStaple">
  <psf:Property name="psf:SelectionType">
    <psf:Value xsi:type="xs:string">psk:PickOne</psf:Value>
  </psf:Property>
  <psf:Option name="psk:_OptionName_">
    <psf:Property name="psf:IdentityOption">
      <psf:Value xsi:type="xs:string">_IdentityOptionValue_</psf:Value>
    </psf:Property>
    <psf:ScoredProperty name="psk:Angle" >
      <psf:Value xsi:type="xs:integer">_AngleValue_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:SheetCapacity" >
      <psf:Value xsi:type="xs:integer">_SheetCapacityValue_</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
</psf:Feature>
      
```

## <a name="structure-variables"></a><span data-ttu-id="62793-124">Variáveis de estrutura</span><span class="sxs-lookup"><span data-stu-id="62793-124">Structure Variables</span></span>

<span data-ttu-id="62793-125">A tabela a seguir descreve as características das variáveis definidas na estrutura XML.</span><span class="sxs-lookup"><span data-stu-id="62793-125">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="62793-126">Nome</span><span class="sxs-lookup"><span data-stu-id="62793-126">Name</span></span>                               | <span data-ttu-id="62793-127">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="62793-127">Data type</span></span>          | <span data-ttu-id="62793-128">Unidade</span><span class="sxs-lookup"><span data-stu-id="62793-128">Unit</span></span>                       | <span data-ttu-id="62793-129">Valores com suporte</span><span class="sxs-lookup"><span data-stu-id="62793-129">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="62793-130">Resumo</span><span class="sxs-lookup"><span data-stu-id="62793-130">Summary</span></span>                                                                                                                                                     |
|------------------------------------|--------------------|----------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="62793-131">\_OptionName\_</span><span class="sxs-lookup"><span data-stu-id="62793-131">\_OptionName\_</span></span><br/>          | <span data-ttu-id="62793-132">string</span><span class="sxs-lookup"><span data-stu-id="62793-132">string</span></span><br/>  | <span data-ttu-id="62793-133">characters</span><span class="sxs-lookup"><span data-stu-id="62793-133">characters</span></span><br/>      | <span data-ttu-id="62793-134">Nome totalmente qualificado válido, conforme definido pelos [namespaces em XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span><span class="sxs-lookup"><span data-stu-id="62793-134">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="62793-135">Se nenhum namespace for especificado, o namespace padrão será assumido.</span><span class="sxs-lookup"><span data-stu-id="62793-135">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="62793-136">O nome da opção.</span><span class="sxs-lookup"><span data-stu-id="62793-136">The name of the option.</span></span><br/>                                                                                                                          |
| <span data-ttu-id="62793-137">\_IdentityOptionValue\_</span><span class="sxs-lookup"><span data-stu-id="62793-137">\_IdentityOptionValue\_</span></span><br/> | <span data-ttu-id="62793-138">string</span><span class="sxs-lookup"><span data-stu-id="62793-138">string</span></span><br/>  | <span data-ttu-id="62793-139">n/d</span><span class="sxs-lookup"><span data-stu-id="62793-139">n/a</span></span><br/>             | <span data-ttu-id="62793-140">True, False.</span><span class="sxs-lookup"><span data-stu-id="62793-140">True, False.</span></span><br/>                                                                                                                                                               | <span data-ttu-id="62793-141">Define uma opção que, quando selecionada, desabilita esse recurso.</span><span class="sxs-lookup"><span data-stu-id="62793-141">Defines an Option which when selected would disable this feature.</span></span><br/>                                                                                |
| <span data-ttu-id="62793-142">\_Ângulovalue\_</span><span class="sxs-lookup"><span data-stu-id="62793-142">\_AngleValue\_</span></span><br/>          | <span data-ttu-id="62793-143">Número inteiro</span><span class="sxs-lookup"><span data-stu-id="62793-143">integer</span></span><br/> | <span data-ttu-id="62793-144">graus</span><span class="sxs-lookup"><span data-stu-id="62793-144">degrees</span></span><br/>         | <span data-ttu-id="62793-145">Maior que 0.</span><span class="sxs-lookup"><span data-stu-id="62793-145">Greater than 0.</span></span><br/>                                                                                                                                                            | <span data-ttu-id="62793-146">Especifica o ângulo do grampo, em relação à direção X do PageImageableSize.</span><span class="sxs-lookup"><span data-stu-id="62793-146">Specifies the staple angle, relative to the X direction of the PageImageableSize.</span></span> <span data-ttu-id="62793-147">O ângulo do grampo é medido em uma direção no sentido anti-horário.</span><span class="sxs-lookup"><span data-stu-id="62793-147">The staple angle is measured in a counter-clockwise direction.</span></span><br/> |
| <span data-ttu-id="62793-148">\_SheetCapacityValue\_</span><span class="sxs-lookup"><span data-stu-id="62793-148">\_SheetCapacityValue\_</span></span><br/>  | <span data-ttu-id="62793-149">Número inteiro</span><span class="sxs-lookup"><span data-stu-id="62793-149">integer</span></span><br/> | <span data-ttu-id="62793-150">folhas de mídia</span><span class="sxs-lookup"><span data-stu-id="62793-150">sheets of media</span></span><br/> | <span data-ttu-id="62793-151">Maior que 0.</span><span class="sxs-lookup"><span data-stu-id="62793-151">Greater than 0.</span></span><br/>                                                                                                                                                            | <span data-ttu-id="62793-152">Especifica o número de planilhas com suporte da opção de grampeamento para o MediaType selecionado no momento.</span><span class="sxs-lookup"><span data-stu-id="62793-152">Specifies number of sheets supported by the stapling option for the currently selected MediaType.</span></span><br/>                                                |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="62793-153">Conteúdo de linguagem XML (XML)</span><span class="sxs-lookup"><span data-stu-id="62793-153">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="62793-154">As palavras-chave do esquema de impressão pública são definidas no https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span><span class="sxs-lookup"><span data-stu-id="62793-154">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="62793-155">O conteúdo do linguagem XML público (XML) para essa palavra-chave é definido abaixo:</span><span class="sxs-lookup"><span data-stu-id="62793-155">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

``` syntax
<psf:Feature name="psk:DocumentStaple">
  <psf:Property name="psf:SelectionType">
    <psf:Value xsi:type="xs:string">psk:PickOne</psf:Value>
  </psf:Property>
  <!-- Specifies saddle stitch stapling -->
  <psf:Option name="psk:SaddleStitch">
    <psf:ScoredProperty name="psk:SheetCapacity" >
      <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <!-- Specifies a single staple in the bottom, left corner. -->
  <psf:Option name="psk:StapleBottomLeft">
    <psf:ScoredProperty name="psk:Angle">
      <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:SheetCapacity" >
      <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <!-- Specifies a single staple in the bottom, right corner. -->
  <psf:Option name="psk:StapleBottomRight">
    <psf:ScoredProperty name="psk:Angle">
      <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:SheetCapacity" >
      <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <!-- Specifies two staples along the left edge. -->
  <psf:Option name="psk:StapleDualLeft">
    <psf:ScoredProperty name="psk:Angle">
      <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:SheetCapacity" >
      <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <!-- Specifies two staples along the right edge. -->
  <psf:Option name="psk:StapleDualRight">
    <psf:ScoredProperty name="psk:Angle">
      <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:SheetCapacity" >
      <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <!-- Specifies two staples along the top edge. -->
  <psf:Option name="psk:StapleDualTop">
    <psf:ScoredProperty name="psk:Angle">
      <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:SheetCapacity" >
      <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <!-- Specifies no stapling. -->
  <psf:Option name="psk:None" />
  <!-- Specifies a single staple in the top, left corner. -->
  <psf:Option name="psk:StapleTopLeft">
    <psf:ScoredProperty name="psk:Angle">
      <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:SheetCapacity" >
      <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <!-- Specifies a single staple in the top, right corner. -->
  <psf:Option name="psk:StapleTopRight">
    <psf:ScoredProperty name="psk:Angle">
      <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:SheetCapacity" >
      <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <!-- Specifies two staples along the bottom edge. -->
  <psf:Option name="psk:StapleDualBottom">
    <psf:ScoredProperty name="psk:Angle">
      <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:SheetCapacity" >
      <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
</psf:Feature>
```

## <a name="related-topics"></a><span data-ttu-id="62793-156">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="62793-156">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="62793-157">Especificação de esquema de impressão</span><span class="sxs-lookup"><span data-stu-id="62793-157">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




