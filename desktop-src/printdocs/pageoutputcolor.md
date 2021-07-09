---
description: Saiba mais sobre o elemento PageOutputColor configurável pelo usuário. Este tópico não é atual. Para obter as informações mais atuais, consulte a especificação do esquema de impressão.
ms.assetid: 1afcf2e6-5d6d-4b87-a005-15d42a610f69
title: PageOutputColor
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 79fc71f58bde44224642d3a5f6979e3aef929976
ms.sourcegitcommit: 998d50f6def8a25850fc113fc8a2df903c829c5e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/09/2021
ms.locfileid: "113548984"
---
# <a name="pageoutputcolor"></a><span data-ttu-id="56b8a-105">PageOutputColor</span><span class="sxs-lookup"><span data-stu-id="56b8a-105">PageOutputColor</span></span>

<span data-ttu-id="56b8a-106">Este tópico não é atual.</span><span class="sxs-lookup"><span data-stu-id="56b8a-106">This topic is not current.</span></span> <span data-ttu-id="56b8a-107">Para obter as informações mais atuais, consulte a [especificação do esquema de impressão](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="56b8a-107">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="56b8a-108">Descreve as características das configurações de cor para a saída.</span><span class="sxs-lookup"><span data-stu-id="56b8a-108">Describes the characteristics of the color settings for the output.</span></span>

-   [<span data-ttu-id="56b8a-109">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="56b8a-109">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="56b8a-110">Conteúdo estrutural</span><span class="sxs-lookup"><span data-stu-id="56b8a-110">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="56b8a-111">Conteúdo de linguagem XML (XML)</span><span class="sxs-lookup"><span data-stu-id="56b8a-111">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="56b8a-112">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="56b8a-112">Element Information</span></span>



| <span data-ttu-id="56b8a-113">Nome</span><span class="sxs-lookup"><span data-stu-id="56b8a-113">Name</span></span> | <span data-ttu-id="56b8a-114">Valor</span><span class="sxs-lookup"><span data-stu-id="56b8a-114">Value</span></span> |
|----------------------------|--------------------|
| <span data-ttu-id="56b8a-115">Tipo de elemento</span><span class="sxs-lookup"><span data-stu-id="56b8a-115">Element Type</span></span> <br/>   | <span data-ttu-id="56b8a-116">Recurso</span><span class="sxs-lookup"><span data-stu-id="56b8a-116">Feature</span></span><br/> |
| <span data-ttu-id="56b8a-117">Prefixo de escopo</span><span class="sxs-lookup"><span data-stu-id="56b8a-117">Scoping Prefix</span></span> <br/> | <span data-ttu-id="56b8a-118">Página</span><span class="sxs-lookup"><span data-stu-id="56b8a-118">Page</span></span><br/>    |
| <span data-ttu-id="56b8a-119">Observações</span><span class="sxs-lookup"><span data-stu-id="56b8a-119">Notes</span></span> <br/>          | <span data-ttu-id="56b8a-120">Nenhum</span><span class="sxs-lookup"><span data-stu-id="56b8a-120">None</span></span><br/>    |



 

## <a name="structural-content"></a><span data-ttu-id="56b8a-121">Conteúdo estrutural</span><span class="sxs-lookup"><span data-stu-id="56b8a-121">Structural Content</span></span>

<span data-ttu-id="56b8a-122">A estrutura XML desse elemento é:</span><span class="sxs-lookup"><span data-stu-id="56b8a-122">The XML structure of this element is:</span></span>

``` syntax
<psf:Feature name="psk:PageOutputColor">
  <psf:Property name="psf:SelectionType">
    <psf:Value xsi:type="xs:string">psk:PickOne</psf:Value>
  </psf:Property>
  <psf:Option name="psk:_OptionName_">
    <psf:Property name="psf:IdentityOption">
      <psf:Value xsi:type="xs:string">_IdentityOptionValue_</psf:Value>
    </psf:Property>
    <psf:ScoredProperty name=psk:DeviceBitsPerPixel>
      <psf:Value xsi:type="xs:integer">_DeviceBitsPerPixelValue_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name=psk:DriverBitsPerPixel>
      <psf:Value xsi:type="xs:integer">_DriverBitsPerPixelValue_</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
</psf:Feature>
      
```

## <a name="structure-variables"></a><span data-ttu-id="56b8a-123">Variáveis de estrutura</span><span class="sxs-lookup"><span data-stu-id="56b8a-123">Structure Variables</span></span>

<span data-ttu-id="56b8a-124">A tabela a seguir descreve as características das variáveis definidas na estrutura XML.</span><span class="sxs-lookup"><span data-stu-id="56b8a-124">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="56b8a-125">Nome</span><span class="sxs-lookup"><span data-stu-id="56b8a-125">Name</span></span>                                   | <span data-ttu-id="56b8a-126">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="56b8a-126">Data type</span></span>          | <span data-ttu-id="56b8a-127">Unidade</span><span class="sxs-lookup"><span data-stu-id="56b8a-127">Unit</span></span>                      | <span data-ttu-id="56b8a-128">Valores com suporte</span><span class="sxs-lookup"><span data-stu-id="56b8a-128">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="56b8a-129">Resumo</span><span class="sxs-lookup"><span data-stu-id="56b8a-129">Summary</span></span>                                                                                                                           |
|----------------------------------------|--------------------|---------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="56b8a-130">\_OptionName\_</span><span class="sxs-lookup"><span data-stu-id="56b8a-130">\_OptionName\_</span></span><br/>              | <span data-ttu-id="56b8a-131">string</span><span class="sxs-lookup"><span data-stu-id="56b8a-131">string</span></span><br/>  | <span data-ttu-id="56b8a-132">characters</span><span class="sxs-lookup"><span data-stu-id="56b8a-132">characters</span></span><br/>     | <span data-ttu-id="56b8a-133">Nome totalmente qualificado válido, conforme definido pelos [namespaces em XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span><span class="sxs-lookup"><span data-stu-id="56b8a-133">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="56b8a-134">Se nenhum namespace for especificado, o namespace padrão será assumido.</span><span class="sxs-lookup"><span data-stu-id="56b8a-134">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="56b8a-135">O nome da opção.</span><span class="sxs-lookup"><span data-stu-id="56b8a-135">The name of the option.</span></span><br/>                                                                                                |
| <span data-ttu-id="56b8a-136">\_IdentityOptionValue\_</span><span class="sxs-lookup"><span data-stu-id="56b8a-136">\_IdentityOptionValue\_</span></span><br/>     | <span data-ttu-id="56b8a-137">string</span><span class="sxs-lookup"><span data-stu-id="56b8a-137">string</span></span><br/>  | <span data-ttu-id="56b8a-138">n/d</span><span class="sxs-lookup"><span data-stu-id="56b8a-138">n/a</span></span><br/>            | <span data-ttu-id="56b8a-139">True, False.</span><span class="sxs-lookup"><span data-stu-id="56b8a-139">True, False.</span></span><br/>                                                                                                                                                               | <span data-ttu-id="56b8a-140">Define uma opção que, quando selecionada, desabilita esse recurso.</span><span class="sxs-lookup"><span data-stu-id="56b8a-140">Defines an Option which when selected would disable this feature.</span></span><br/>                                                      |
| <span data-ttu-id="56b8a-141">\_DeviceBitsPerPixelValue\_</span><span class="sxs-lookup"><span data-stu-id="56b8a-141">\_DeviceBitsPerPixelValue\_</span></span><br/> | <span data-ttu-id="56b8a-142">Número inteiro</span><span class="sxs-lookup"><span data-stu-id="56b8a-142">integer</span></span><br/> | <span data-ttu-id="56b8a-143">bits por pixel</span><span class="sxs-lookup"><span data-stu-id="56b8a-143">bits per pixel</span></span><br/> | <span data-ttu-id="56b8a-144">Maior que 0, menor que o valor máximo de suporte de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="56b8a-144">Greater than 0, less than maximum device support value.</span></span><br/>                                                                                                                    | <span data-ttu-id="56b8a-145">Valor numérico que indica o número de bits por pixel de dados de cor com suporte pela impressora.</span><span class="sxs-lookup"><span data-stu-id="56b8a-145">Numeric value indicating the number of bits per pixel of color data supported by the printer.</span></span><br/>                          |
| <span data-ttu-id="56b8a-146">\_DriverBitsPerPixelValue\_</span><span class="sxs-lookup"><span data-stu-id="56b8a-146">\_DriverBitsPerPixelValue\_</span></span><br/> | <span data-ttu-id="56b8a-147">Número inteiro</span><span class="sxs-lookup"><span data-stu-id="56b8a-147">integer</span></span><br/> | <span data-ttu-id="56b8a-148">bits por pixel</span><span class="sxs-lookup"><span data-stu-id="56b8a-148">bits per pixel</span></span><br/> | <span data-ttu-id="56b8a-149">Maior que 0, menor que o valor máximo de suporte de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="56b8a-149">Greater than 0, less than maximum device support value.</span></span><br/>                                                                                                                    | <span data-ttu-id="56b8a-150">Valor numérico que indica o número de bits por pixel que o driver principal deve usar para seu buffer de renderização de bitmap.</span><span class="sxs-lookup"><span data-stu-id="56b8a-150">Numeric value indicating the number of bits per pixel that the core driver should use for its bitmap rendering buffer.</span></span><br/> |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="56b8a-151">Conteúdo de linguagem XML (XML)</span><span class="sxs-lookup"><span data-stu-id="56b8a-151">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="56b8a-152">As palavras-chave do esquema de impressão pública são definidas no https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span><span class="sxs-lookup"><span data-stu-id="56b8a-152">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="56b8a-153">O conteúdo do linguagem XML público (XML) para essa palavra-chave é definido abaixo:</span><span class="sxs-lookup"><span data-stu-id="56b8a-153">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

``` syntax
<psf:Feature name="psk:PageOutputColor">
  <psf:Property name="psf:SelectionType">
    <psf:Value xsi:type="xs:string">psk:PickOne</psf:Value>
  </psf:Property>
  <!-- Specifies the output should be in color. -->
  <psf:Option name="psk:Color">
    <psf:ScoredProperty name="psk:DeviceBitsPerPixel">
      <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:DriverBitsPerPixel">
      <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <!-- Specifies the output should be in grayscale. -->
  <psf:Option name="psk:Grayscale">
    <psf:ScoredProperty name="psk:DeviceBitsPerPixel">
      <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:DriverBitsPerPixel">
      <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <!-- Specifies the output should be in monochrome (Black). -->
  <psf:Option name="psk:Monochrome">
    <psf:ScoredProperty name="psk:DeviceBitsPerPixel">
      <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:DriverBitsPerPixel">
      <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
</psf:Feature>
```

## <a name="related-topics"></a><span data-ttu-id="56b8a-154">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="56b8a-154">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="56b8a-155">Especificação de esquema de impressão</span><span class="sxs-lookup"><span data-stu-id="56b8a-155">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




