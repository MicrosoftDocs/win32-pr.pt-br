---
description: Este tópico não é atual. Para obter as informações mais atuais, consulte a especificação do esquema de impressão.
ms.assetid: 6b81814f-2d9e-4862-8633-6ba016c11dac
title: PageImageableSize
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f1eef9012a7fda3eed6afd16add1d483c35c1111
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/26/2021
ms.locfileid: "107996103"
---
# <a name="pageimageablesize"></a><span data-ttu-id="06a25-104">PageImageableSize</span><span class="sxs-lookup"><span data-stu-id="06a25-104">PageImageableSize</span></span>

<span data-ttu-id="06a25-105">Este tópico não é atual.</span><span class="sxs-lookup"><span data-stu-id="06a25-105">This topic is not current.</span></span> <span data-ttu-id="06a25-106">Para obter as informações mais atuais, consulte a [especificação do esquema de impressão](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="06a25-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="06a25-107">Descreve a tela de imagem para layout e renderização.</span><span class="sxs-lookup"><span data-stu-id="06a25-107">Describes the imaged canvas for layout and rendering.</span></span> <span data-ttu-id="06a25-108">Isso será relatado com base em PageMediaSize e PageOrientation.</span><span class="sxs-lookup"><span data-stu-id="06a25-108">This will be reported based on PageMediaSize and PageOrientation.</span></span>

<span data-ttu-id="06a25-109">Os diagramas a seguir ilustram o uso de variáveis PageImageableSize com base em PageOrientation.</span><span class="sxs-lookup"><span data-stu-id="06a25-109">The following diagrams illustrate the PageImageableSize variables usage based on PageOrientation.</span></span>

![um diagrama que mostra as medidas de página](images/local-1641910626-image.png)

-   [<span data-ttu-id="06a25-111">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="06a25-111">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="06a25-112">Conteúdo estrutural</span><span class="sxs-lookup"><span data-stu-id="06a25-112">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="06a25-113">Conteúdo de linguagem XML (XML)</span><span class="sxs-lookup"><span data-stu-id="06a25-113">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="06a25-114">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="06a25-114">Element Information</span></span>



|                            |                     |
|----------------------------|---------------------|
| <span data-ttu-id="06a25-115">Nome</span><span class="sxs-lookup"><span data-stu-id="06a25-115">Name</span></span> | <span data-ttu-id="06a25-116">Valor</span><span class="sxs-lookup"><span data-stu-id="06a25-116">Value</span></span> |
| <span data-ttu-id="06a25-117">Tipo de elemento</span><span class="sxs-lookup"><span data-stu-id="06a25-117">Element Type</span></span><br/>    | <span data-ttu-id="06a25-118">Propriedade</span><span class="sxs-lookup"><span data-stu-id="06a25-118">Property</span></span><br/> |
| <span data-ttu-id="06a25-119">Prefixo de escopo</span><span class="sxs-lookup"><span data-stu-id="06a25-119">Scoping Prefix</span></span> <br/> | <span data-ttu-id="06a25-120">?</span><span class="sxs-lookup"><span data-stu-id="06a25-120">Page</span></span><br/>     |
| <span data-ttu-id="06a25-121">Observações</span><span class="sxs-lookup"><span data-stu-id="06a25-121">Notes</span></span> <br/>          | <span data-ttu-id="06a25-122">Nenhum</span><span class="sxs-lookup"><span data-stu-id="06a25-122">None</span></span><br/>     |



 

## <a name="structural-content"></a><span data-ttu-id="06a25-123">Conteúdo estrutural</span><span class="sxs-lookup"><span data-stu-id="06a25-123">Structural Content</span></span>

<span data-ttu-id="06a25-124">A estrutura XML desse elemento é:</span><span class="sxs-lookup"><span data-stu-id="06a25-124">The XML structure of this element is:</span></span>

``` syntax
<psf:Property name="psk:PageImageableSize">
  <psf:Property name="psk:ImageableSizeWidth">
    <psf:Value xsi:type="xs:integer">_ImageableSizeWidthValue_</psf:Value>
  </psf:Property>
  <psf:Property name="psk:ImageableSizeHeight">
    <psf:Value xsi:type="xs:integer">_ImageableSizeHeightValue_</psf:Value>
  </psf:Property>
  <!--Specifies the imageable area within the logical page.  -->
  <psf:Property name="psk:ImageableArea">
    <psf:Property name="psk:OriginWidth">
      <psf:Value xsi:type="xs:integer">_OriginWidthValue_</psf:Value>
    </psf:Property>
    <psf:Property name="psk:OriginHeight">
      <psf:Value xsi:type="xs:integer">_OriginHeightValue_</psf:Value>
    </psf:Property>
    <psf:Property name="psk:ExtentWidth">
      <psf:Value xsi:type="xs:integer">_ExtentWidthValue_</psf:Value>
    </psf:Property>
    <psf:Property name="psk:ExtentHeight">
      <psf:Value xsi:type="xs:integer">_ExtentHeightValue_</psf:Value>
    </psf:Property>
  </psf:Property>
</psf:Property>
```

## <a name="structure-variables"></a><span data-ttu-id="06a25-125">Variáveis de estrutura</span><span class="sxs-lookup"><span data-stu-id="06a25-125">Structure Variables</span></span>

<span data-ttu-id="06a25-126">A tabela a seguir descreve as características das variáveis definidas na estrutura XML.</span><span class="sxs-lookup"><span data-stu-id="06a25-126">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="06a25-127">Nome</span><span class="sxs-lookup"><span data-stu-id="06a25-127">Name</span></span>                                    | <span data-ttu-id="06a25-128">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="06a25-128">Data type</span></span>          | <span data-ttu-id="06a25-129">Unidade</span><span class="sxs-lookup"><span data-stu-id="06a25-129">Unit</span></span>               | <span data-ttu-id="06a25-130">Valores com suporte</span><span class="sxs-lookup"><span data-stu-id="06a25-130">Supported values</span></span>                       | <span data-ttu-id="06a25-131">Resumo</span><span class="sxs-lookup"><span data-stu-id="06a25-131">Summary</span></span>                                                                                                                    |
|-----------------------------------------|--------------------|--------------------|----------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="06a25-132">\_ImageableSizeWidthValue\_</span><span class="sxs-lookup"><span data-stu-id="06a25-132">\_ImageableSizeWidthValue\_</span></span><br/>  | <span data-ttu-id="06a25-133">Número inteiro</span><span class="sxs-lookup"><span data-stu-id="06a25-133">integer</span></span><br/> | <span data-ttu-id="06a25-134">mícrons</span><span class="sxs-lookup"><span data-stu-id="06a25-134">microns</span></span><br/> | <span data-ttu-id="06a25-135">Maior que 0.</span><span class="sxs-lookup"><span data-stu-id="06a25-135">Greater than 0.</span></span><br/>             | <span data-ttu-id="06a25-136">Especifica a dimensão horizontal do tamanho da mídia do aplicativo em relação ao PageOrientation.</span><span class="sxs-lookup"><span data-stu-id="06a25-136">Specifies the horizontal dimension of the application media size relative to the PageOrientation.</span></span><br/>               |
| <span data-ttu-id="06a25-137">\_ImageableSizeHeightValue\_</span><span class="sxs-lookup"><span data-stu-id="06a25-137">\_ImageableSizeHeightValue\_</span></span><br/> | <span data-ttu-id="06a25-138">Número inteiro</span><span class="sxs-lookup"><span data-stu-id="06a25-138">integer</span></span><br/> | <span data-ttu-id="06a25-139">mícrons</span><span class="sxs-lookup"><span data-stu-id="06a25-139">microns</span></span><br/> | <span data-ttu-id="06a25-140">Maior que 0.</span><span class="sxs-lookup"><span data-stu-id="06a25-140">Greater than 0.</span></span><br/>             | <span data-ttu-id="06a25-141">Especifica a dimensão vertical do tamanho da mídia do aplicativo em relação ao PageOrientation.</span><span class="sxs-lookup"><span data-stu-id="06a25-141">Specifies the vertical dimension of the application media size relative to the PageOrientation.</span></span><br/>                 |
| <span data-ttu-id="06a25-142">\_OriginWidthValue\_</span><span class="sxs-lookup"><span data-stu-id="06a25-142">\_OriginWidthValue\_</span></span><br/>         | <span data-ttu-id="06a25-143">Número inteiro</span><span class="sxs-lookup"><span data-stu-id="06a25-143">integer</span></span><br/> | <span data-ttu-id="06a25-144">mícrons</span><span class="sxs-lookup"><span data-stu-id="06a25-144">microns</span></span><br/> | <span data-ttu-id="06a25-145">Maior ou igual a 0.</span><span class="sxs-lookup"><span data-stu-id="06a25-145">Greater than or equal to 0.</span></span><br/> | <span data-ttu-id="06a25-146">Especifica a origem horizontal da área de imagem em relação ao tamanho da mídia do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="06a25-146">Specifies the horizontal origin of the imageable area relative to the application media size.</span></span><br/>                   |
| <span data-ttu-id="06a25-147">\_OriginHeightValue\_</span><span class="sxs-lookup"><span data-stu-id="06a25-147">\_OriginHeightValue\_</span></span><br/>        | <span data-ttu-id="06a25-148">Número inteiro</span><span class="sxs-lookup"><span data-stu-id="06a25-148">integer</span></span><br/> | <span data-ttu-id="06a25-149">mícrons</span><span class="sxs-lookup"><span data-stu-id="06a25-149">microns</span></span><br/> | <span data-ttu-id="06a25-150">Maior ou igual a 0.</span><span class="sxs-lookup"><span data-stu-id="06a25-150">Greater than or equal to 0.</span></span><br/> | <span data-ttu-id="06a25-151">Especifica a origem vertical da área de imagem em relação ao tamanho da mídia do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="06a25-151">Specifies the vertical origin of the imageable area relative to the application media size.</span></span><br/>                     |
| <span data-ttu-id="06a25-152">\_ExtentWidthValue\_</span><span class="sxs-lookup"><span data-stu-id="06a25-152">\_ExtentWidthValue\_</span></span><br/>         | <span data-ttu-id="06a25-153">Número inteiro</span><span class="sxs-lookup"><span data-stu-id="06a25-153">integer</span></span><br/> | <span data-ttu-id="06a25-154">mícrons</span><span class="sxs-lookup"><span data-stu-id="06a25-154">microns</span></span><br/> | <span data-ttu-id="06a25-155">Maior que 0.</span><span class="sxs-lookup"><span data-stu-id="06a25-155">Greater than 0.</span></span><br/>             | <span data-ttu-id="06a25-156">Especifica a distância horizontal entre a origem e o limite delimitador do tamanho da mídia do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="06a25-156">Specifies the horizontal distance between the origin and the bounding limit of the application media size.</span></span><br/>      |
| <span data-ttu-id="06a25-157">\_ExtentHeightValue\_</span><span class="sxs-lookup"><span data-stu-id="06a25-157">\_ExtentHeightValue\_</span></span><br/>        | <span data-ttu-id="06a25-158">Número inteiro</span><span class="sxs-lookup"><span data-stu-id="06a25-158">integer</span></span><br/> | <span data-ttu-id="06a25-159">mícrons</span><span class="sxs-lookup"><span data-stu-id="06a25-159">microns</span></span><br/> | <span data-ttu-id="06a25-160">Maior que 0.</span><span class="sxs-lookup"><span data-stu-id="06a25-160">Greater than 0.</span></span><br/>             | <span data-ttu-id="06a25-161">Especifica a distância vertical entre a origem e o limite delimitador do tamanho da mídia do aplicativo Canvas.</span><span class="sxs-lookup"><span data-stu-id="06a25-161">Specifies the vertical distance between the origin and the bounding limit of the canvas application media size.</span></span><br/> |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="06a25-162">Conteúdo de linguagem XML (XML)</span><span class="sxs-lookup"><span data-stu-id="06a25-162">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="06a25-163">As palavras-chave do esquema de impressão pública são definidas no https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span><span class="sxs-lookup"><span data-stu-id="06a25-163">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="06a25-164">O conteúdo do linguagem XML público (XML) para essa palavra-chave é definido abaixo:</span><span class="sxs-lookup"><span data-stu-id="06a25-164">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

``` syntax
<psf:Property name="psk:PageImageableSize">
  <psf:Property name="psk:ImageableSizeWidth">
    <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
  </psf:Property>
  <psf:Property name="psk:ImageableSizeHeight">
    <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
  </psf:Property>
    <psf:Property name="psk:ImageableArea">
      <psf:Property name="psk:OriginWidth">
        <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
      </psf:Property>
    <psf:Property name="psk:OriginHeight">
      <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
    </psf:Property>
    <psf:Property name="psk:ExtentWidth">
      <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
    </psf:Property>
    <psf:Property name="psk:ExtentHeight">
      <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
    </psf:Property>
  </psf:Property>
</psf:Property>
  
```

## <a name="related-topics"></a><span data-ttu-id="06a25-165">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="06a25-165">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="06a25-166">Especificação de esquema de impressão</span><span class="sxs-lookup"><span data-stu-id="06a25-166">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




