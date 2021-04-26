---
description: Este tópico não é atual. Para obter as informações mais atuais, consulte a especificação do esquema de impressão.
ms.assetid: 53e38979-2065-4304-a0ed-0434c8d2efc8
title: DocumentStaple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 338a72baecc62d22ac63ef50d8ce8967c7fd534a
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/26/2021
ms.locfileid: "107997033"
---
# <a name="documentstaple"></a><span data-ttu-id="af349-104">DocumentStaple</span><span class="sxs-lookup"><span data-stu-id="af349-104">DocumentStaple</span></span>

<span data-ttu-id="af349-105">Este tópico não é atual.</span><span class="sxs-lookup"><span data-stu-id="af349-105">This topic is not current.</span></span> <span data-ttu-id="af349-106">Para obter as informações mais atuais, consulte a [especificação do esquema de impressão](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="af349-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="af349-107">Descreve as características de grampeamento da saída.</span><span class="sxs-lookup"><span data-stu-id="af349-107">Describes the stapling characteristics of the output.</span></span> <span data-ttu-id="af349-108">Cada documento é grampeado separadamente.</span><span class="sxs-lookup"><span data-stu-id="af349-108">Each document is stapled separately.</span></span> <span data-ttu-id="af349-109">As palavras-chave JobStapleAllDocuments e DocumentStaple são mutuamente exclusivas.</span><span class="sxs-lookup"><span data-stu-id="af349-109">The JobStapleAllDocuments and DocumentStaple keywords are mutually exclusive.</span></span> <span data-ttu-id="af349-110">Cabe ao driver determinar o tratamento de restrições entre essas palavras-chave.</span><span class="sxs-lookup"><span data-stu-id="af349-110">It is up to the driver to determine constraint handling between these keywords.</span></span>

-   [<span data-ttu-id="af349-111">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="af349-111">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="af349-112">Conteúdo estrutural</span><span class="sxs-lookup"><span data-stu-id="af349-112">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="af349-113">Conteúdo de linguagem XML (XML)</span><span class="sxs-lookup"><span data-stu-id="af349-113">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="af349-114">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="af349-114">Element Information</span></span>



| <span data-ttu-id="af349-115">Nome</span><span class="sxs-lookup"><span data-stu-id="af349-115">Name</span></span> | <span data-ttu-id="af349-116">Valor</span><span class="sxs-lookup"><span data-stu-id="af349-116">Value</span></span> |
|----------------------------|--------------------------------------------------------------------------------|
| <span data-ttu-id="af349-117">Tipo de elemento</span><span class="sxs-lookup"><span data-stu-id="af349-117">Element Type</span></span> <br/>   | <span data-ttu-id="af349-118">Recurso</span><span class="sxs-lookup"><span data-stu-id="af349-118">Feature</span></span><br/>                                                             |
| <span data-ttu-id="af349-119">Prefixo de escopo</span><span class="sxs-lookup"><span data-stu-id="af349-119">Scoping Prefix</span></span> <br/> | <span data-ttu-id="af349-120">Documento</span><span class="sxs-lookup"><span data-stu-id="af349-120">Document</span></span><br/>                                                            |
| <span data-ttu-id="af349-121">Observações</span><span class="sxs-lookup"><span data-stu-id="af349-121">Notes</span></span> <br/>          | <span data-ttu-id="af349-122">Superior, inferior, esquerda e direita são relativos ao PageImageableSize.</span><span class="sxs-lookup"><span data-stu-id="af349-122">Top, Bottom, Left, and Right are relative to the PageImageableSize.</span></span><br/> |



 

## <a name="structural-content"></a><span data-ttu-id="af349-123">Conteúdo estrutural</span><span class="sxs-lookup"><span data-stu-id="af349-123">Structural Content</span></span>

<span data-ttu-id="af349-124">A estrutura XML desse elemento é:</span><span class="sxs-lookup"><span data-stu-id="af349-124">The XML structure of this element is:</span></span>

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

## <a name="structure-variables"></a><span data-ttu-id="af349-125">Variáveis de estrutura</span><span class="sxs-lookup"><span data-stu-id="af349-125">Structure Variables</span></span>

<span data-ttu-id="af349-126">A tabela a seguir descreve as características das variáveis definidas na estrutura XML.</span><span class="sxs-lookup"><span data-stu-id="af349-126">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="af349-127">Nome</span><span class="sxs-lookup"><span data-stu-id="af349-127">Name</span></span>                               | <span data-ttu-id="af349-128">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="af349-128">Data type</span></span>          | <span data-ttu-id="af349-129">Unidade</span><span class="sxs-lookup"><span data-stu-id="af349-129">Unit</span></span>                       | <span data-ttu-id="af349-130">Valores com suporte</span><span class="sxs-lookup"><span data-stu-id="af349-130">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="af349-131">Resumo</span><span class="sxs-lookup"><span data-stu-id="af349-131">Summary</span></span>                                                                                                                                                     |
|------------------------------------|--------------------|----------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="af349-132">\_OptionName\_</span><span class="sxs-lookup"><span data-stu-id="af349-132">\_OptionName\_</span></span><br/>          | <span data-ttu-id="af349-133">string</span><span class="sxs-lookup"><span data-stu-id="af349-133">string</span></span><br/>  | <span data-ttu-id="af349-134">characters</span><span class="sxs-lookup"><span data-stu-id="af349-134">characters</span></span><br/>      | <span data-ttu-id="af349-135">Nome totalmente qualificado válido, conforme definido pelos [namespaces em XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span><span class="sxs-lookup"><span data-stu-id="af349-135">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="af349-136">Se nenhum namespace for especificado, o namespace padrão será assumido.</span><span class="sxs-lookup"><span data-stu-id="af349-136">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="af349-137">O nome da opção.</span><span class="sxs-lookup"><span data-stu-id="af349-137">The name of the option.</span></span><br/>                                                                                                                          |
| <span data-ttu-id="af349-138">\_IdentityOptionValue\_</span><span class="sxs-lookup"><span data-stu-id="af349-138">\_IdentityOptionValue\_</span></span><br/> | <span data-ttu-id="af349-139">string</span><span class="sxs-lookup"><span data-stu-id="af349-139">string</span></span><br/>  | <span data-ttu-id="af349-140">N/D</span><span class="sxs-lookup"><span data-stu-id="af349-140">n/a</span></span><br/>             | <span data-ttu-id="af349-141">True, False.</span><span class="sxs-lookup"><span data-stu-id="af349-141">True, False.</span></span><br/>                                                                                                                                                               | <span data-ttu-id="af349-142">Define uma opção que, quando selecionada, desabilita esse recurso.</span><span class="sxs-lookup"><span data-stu-id="af349-142">Defines an Option which when selected would disable this feature.</span></span><br/>                                                                                |
| <span data-ttu-id="af349-143">\_Ângulovalue\_</span><span class="sxs-lookup"><span data-stu-id="af349-143">\_AngleValue\_</span></span><br/>          | <span data-ttu-id="af349-144">Número inteiro</span><span class="sxs-lookup"><span data-stu-id="af349-144">integer</span></span><br/> | <span data-ttu-id="af349-145">graus</span><span class="sxs-lookup"><span data-stu-id="af349-145">degrees</span></span><br/>         | <span data-ttu-id="af349-146">Maior que 0.</span><span class="sxs-lookup"><span data-stu-id="af349-146">Greater than 0.</span></span><br/>                                                                                                                                                            | <span data-ttu-id="af349-147">Especifica o ângulo do grampo, em relação à direção X do PageImageableSize.</span><span class="sxs-lookup"><span data-stu-id="af349-147">Specifies the staple angle, relative to the X direction of the PageImageableSize.</span></span> <span data-ttu-id="af349-148">O ângulo do grampo é medido em uma direção no sentido anti-horário.</span><span class="sxs-lookup"><span data-stu-id="af349-148">The staple angle is measured in a counter-clockwise direction.</span></span><br/> |
| <span data-ttu-id="af349-149">\_SheetCapacityValue\_</span><span class="sxs-lookup"><span data-stu-id="af349-149">\_SheetCapacityValue\_</span></span><br/>  | <span data-ttu-id="af349-150">Número inteiro</span><span class="sxs-lookup"><span data-stu-id="af349-150">integer</span></span><br/> | <span data-ttu-id="af349-151">folhas de mídia</span><span class="sxs-lookup"><span data-stu-id="af349-151">sheets of media</span></span><br/> | <span data-ttu-id="af349-152">Maior que 0.</span><span class="sxs-lookup"><span data-stu-id="af349-152">Greater than 0.</span></span><br/>                                                                                                                                                            | <span data-ttu-id="af349-153">Especifica o número de planilhas com suporte da opção de grampeamento para o MediaType selecionado no momento.</span><span class="sxs-lookup"><span data-stu-id="af349-153">Specifies number of sheets supported by the stapling option for the currently selected MediaType.</span></span><br/>                                                |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="af349-154">Conteúdo de linguagem XML (XML)</span><span class="sxs-lookup"><span data-stu-id="af349-154">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="af349-155">As palavras-chave do esquema de impressão pública são definidas no https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span><span class="sxs-lookup"><span data-stu-id="af349-155">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="af349-156">O conteúdo do linguagem XML público (XML) para essa palavra-chave é definido abaixo:</span><span class="sxs-lookup"><span data-stu-id="af349-156">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

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

## <a name="related-topics"></a><span data-ttu-id="af349-157">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="af349-157">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="af349-158">Especificação de esquema de impressão</span><span class="sxs-lookup"><span data-stu-id="af349-158">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




