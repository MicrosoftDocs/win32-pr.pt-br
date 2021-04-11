---
description: Este tópico não é atual. Para obter as informações mais atuais, consulte a especificação do esquema de impressão.
ms.assetid: 1afcf2e6-5d6d-4b87-a005-15d42a610f69
title: PageOutputColor
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 71796bae9528fe6b32397f3467113630159c9954
ms.sourcegitcommit: 7b8f6151ebe247536304866459b2973276271d4d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/06/2021
ms.locfileid: "104172599"
---
# <a name="pageoutputcolor"></a><span data-ttu-id="9ae0b-104">PageOutputColor</span><span class="sxs-lookup"><span data-stu-id="9ae0b-104">PageOutputColor</span></span>

<span data-ttu-id="9ae0b-105">Este tópico não é atual.</span><span class="sxs-lookup"><span data-stu-id="9ae0b-105">This topic is not current.</span></span> <span data-ttu-id="9ae0b-106">Para obter as informações mais atuais, consulte a [especificação do esquema de impressão](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="9ae0b-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="9ae0b-107">Descreve as características das configurações de cor para a saída.</span><span class="sxs-lookup"><span data-stu-id="9ae0b-107">Describes the characteristics of the color settings for the output.</span></span>

-   [<span data-ttu-id="9ae0b-108">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="9ae0b-108">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="9ae0b-109">Conteúdo estrutural</span><span class="sxs-lookup"><span data-stu-id="9ae0b-109">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="9ae0b-110">Conteúdo de linguagem XML (XML)</span><span class="sxs-lookup"><span data-stu-id="9ae0b-110">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="9ae0b-111">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="9ae0b-111">Element Information</span></span>



| <span data-ttu-id="9ae0b-112">Nome</span><span class="sxs-lookup"><span data-stu-id="9ae0b-112">Name</span></span>                       |                    |
|----------------------------|--------------------|
| <span data-ttu-id="9ae0b-113">Tipo de elemento</span><span class="sxs-lookup"><span data-stu-id="9ae0b-113">Element Type</span></span> <br/>   | <span data-ttu-id="9ae0b-114">Recurso</span><span class="sxs-lookup"><span data-stu-id="9ae0b-114">Feature</span></span><br/> |
| <span data-ttu-id="9ae0b-115">Prefixo de escopo</span><span class="sxs-lookup"><span data-stu-id="9ae0b-115">Scoping Prefix</span></span> <br/> | <span data-ttu-id="9ae0b-116">?</span><span class="sxs-lookup"><span data-stu-id="9ae0b-116">Page</span></span><br/>    |
| <span data-ttu-id="9ae0b-117">Observações</span><span class="sxs-lookup"><span data-stu-id="9ae0b-117">Notes</span></span> <br/>          | <span data-ttu-id="9ae0b-118">Nenhum</span><span class="sxs-lookup"><span data-stu-id="9ae0b-118">None</span></span><br/>    |



 

## <a name="structural-content"></a><span data-ttu-id="9ae0b-119">Conteúdo estrutural</span><span class="sxs-lookup"><span data-stu-id="9ae0b-119">Structural Content</span></span>

<span data-ttu-id="9ae0b-120">A estrutura XML desse elemento é:</span><span class="sxs-lookup"><span data-stu-id="9ae0b-120">The XML structure of this element is:</span></span>

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

## <a name="structure-variables"></a><span data-ttu-id="9ae0b-121">Variáveis de estrutura</span><span class="sxs-lookup"><span data-stu-id="9ae0b-121">Structure Variables</span></span>

<span data-ttu-id="9ae0b-122">A tabela a seguir descreve as características das variáveis definidas na estrutura XML.</span><span class="sxs-lookup"><span data-stu-id="9ae0b-122">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="9ae0b-123">Nome</span><span class="sxs-lookup"><span data-stu-id="9ae0b-123">Name</span></span>                                   | <span data-ttu-id="9ae0b-124">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="9ae0b-124">Data type</span></span>          | <span data-ttu-id="9ae0b-125">Unidade</span><span class="sxs-lookup"><span data-stu-id="9ae0b-125">Unit</span></span>                      | <span data-ttu-id="9ae0b-126">Valores com suporte</span><span class="sxs-lookup"><span data-stu-id="9ae0b-126">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="9ae0b-127">Resumo</span><span class="sxs-lookup"><span data-stu-id="9ae0b-127">Summary</span></span>                                                                                                                           |
|----------------------------------------|--------------------|---------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9ae0b-128">\_OptionName\_</span><span class="sxs-lookup"><span data-stu-id="9ae0b-128">\_OptionName\_</span></span><br/>              | <span data-ttu-id="9ae0b-129">string</span><span class="sxs-lookup"><span data-stu-id="9ae0b-129">string</span></span><br/>  | <span data-ttu-id="9ae0b-130">characters</span><span class="sxs-lookup"><span data-stu-id="9ae0b-130">characters</span></span><br/>     | <span data-ttu-id="9ae0b-131">Nome totalmente qualificado válido, conforme definido pelos [namespaces em XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span><span class="sxs-lookup"><span data-stu-id="9ae0b-131">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="9ae0b-132">Se nenhum namespace for especificado, o namespace padrão será assumido.</span><span class="sxs-lookup"><span data-stu-id="9ae0b-132">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="9ae0b-133">O nome da opção.</span><span class="sxs-lookup"><span data-stu-id="9ae0b-133">The name of the option.</span></span><br/>                                                                                                |
| <span data-ttu-id="9ae0b-134">\_IdentityOptionValue\_</span><span class="sxs-lookup"><span data-stu-id="9ae0b-134">\_IdentityOptionValue\_</span></span><br/>     | <span data-ttu-id="9ae0b-135">string</span><span class="sxs-lookup"><span data-stu-id="9ae0b-135">string</span></span><br/>  | <span data-ttu-id="9ae0b-136">N/D</span><span class="sxs-lookup"><span data-stu-id="9ae0b-136">n/a</span></span><br/>            | <span data-ttu-id="9ae0b-137">True, False.</span><span class="sxs-lookup"><span data-stu-id="9ae0b-137">True, False.</span></span><br/>                                                                                                                                                               | <span data-ttu-id="9ae0b-138">Define uma opção que, quando selecionada, desabilita esse recurso.</span><span class="sxs-lookup"><span data-stu-id="9ae0b-138">Defines an Option which when selected would disable this feature.</span></span><br/>                                                      |
| <span data-ttu-id="9ae0b-139">\_DeviceBitsPerPixelValue\_</span><span class="sxs-lookup"><span data-stu-id="9ae0b-139">\_DeviceBitsPerPixelValue\_</span></span><br/> | <span data-ttu-id="9ae0b-140">Número inteiro</span><span class="sxs-lookup"><span data-stu-id="9ae0b-140">integer</span></span><br/> | <span data-ttu-id="9ae0b-141">bits por pixel</span><span class="sxs-lookup"><span data-stu-id="9ae0b-141">bits per pixel</span></span><br/> | <span data-ttu-id="9ae0b-142">Maior que 0, menor que o valor máximo de suporte de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="9ae0b-142">Greater than 0, less than maximum device support value.</span></span><br/>                                                                                                                    | <span data-ttu-id="9ae0b-143">Valor numérico que indica o número de bits por pixel de dados de cor com suporte pela impressora.</span><span class="sxs-lookup"><span data-stu-id="9ae0b-143">Numeric value indicating the number of bits per pixel of color data supported by the printer.</span></span><br/>                          |
| <span data-ttu-id="9ae0b-144">\_DriverBitsPerPixelValue\_</span><span class="sxs-lookup"><span data-stu-id="9ae0b-144">\_DriverBitsPerPixelValue\_</span></span><br/> | <span data-ttu-id="9ae0b-145">Número inteiro</span><span class="sxs-lookup"><span data-stu-id="9ae0b-145">integer</span></span><br/> | <span data-ttu-id="9ae0b-146">bits por pixel</span><span class="sxs-lookup"><span data-stu-id="9ae0b-146">bits per pixel</span></span><br/> | <span data-ttu-id="9ae0b-147">Maior que 0, menor que o valor máximo de suporte de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="9ae0b-147">Greater than 0, less than maximum device support value.</span></span><br/>                                                                                                                    | <span data-ttu-id="9ae0b-148">Valor numérico que indica o número de bits por pixel que o driver principal deve usar para seu buffer de renderização de bitmap.</span><span class="sxs-lookup"><span data-stu-id="9ae0b-148">Numeric value indicating the number of bits per pixel that the core driver should use for its bitmap rendering buffer.</span></span><br/> |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="9ae0b-149">Conteúdo de linguagem XML (XML)</span><span class="sxs-lookup"><span data-stu-id="9ae0b-149">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="9ae0b-150">As palavras-chave do esquema de impressão pública são definidas no https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span><span class="sxs-lookup"><span data-stu-id="9ae0b-150">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="9ae0b-151">O conteúdo do linguagem XML público (XML) para essa palavra-chave é definido abaixo:</span><span class="sxs-lookup"><span data-stu-id="9ae0b-151">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

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

## <a name="related-topics"></a><span data-ttu-id="9ae0b-152">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="9ae0b-152">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9ae0b-153">Especificação de esquema de impressão</span><span class="sxs-lookup"><span data-stu-id="9ae0b-153">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




