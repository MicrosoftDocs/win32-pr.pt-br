---
description: Este tópico não é atual. Para obter as informações mais atuais, consulte a especificação do esquema de impressão.
ms.assetid: 6b81814f-2d9e-4862-8633-6ba016c11dac
title: PageImageableSize
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 26dca243defc08b43a79e897bfa91913a954bf37
ms.sourcegitcommit: 7b8f6151ebe247536304866459b2973276271d4d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/06/2021
ms.locfileid: "104553995"
---
# <a name="pageimageablesize"></a><span data-ttu-id="99c16-104">PageImageableSize</span><span class="sxs-lookup"><span data-stu-id="99c16-104">PageImageableSize</span></span>

<span data-ttu-id="99c16-105">Este tópico não é atual.</span><span class="sxs-lookup"><span data-stu-id="99c16-105">This topic is not current.</span></span> <span data-ttu-id="99c16-106">Para obter as informações mais atuais, consulte a [especificação do esquema de impressão](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="99c16-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="99c16-107">Descreve a tela de imagem para layout e renderização.</span><span class="sxs-lookup"><span data-stu-id="99c16-107">Describes the imaged canvas for layout and rendering.</span></span> <span data-ttu-id="99c16-108">Isso será relatado com base em PageMediaSize e PageOrientation.</span><span class="sxs-lookup"><span data-stu-id="99c16-108">This will be reported based on PageMediaSize and PageOrientation.</span></span>

<span data-ttu-id="99c16-109">Os diagramas a seguir ilustram o uso de variáveis PageImageableSize com base em PageOrientation.</span><span class="sxs-lookup"><span data-stu-id="99c16-109">The following diagrams illustrate the PageImageableSize variables usage based on PageOrientation.</span></span>

![um diagrama que mostra as medidas de página](images/local-1641910626-image.png)

-   [<span data-ttu-id="99c16-111">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="99c16-111">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="99c16-112">Conteúdo estrutural</span><span class="sxs-lookup"><span data-stu-id="99c16-112">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="99c16-113">Conteúdo de linguagem XML (XML)</span><span class="sxs-lookup"><span data-stu-id="99c16-113">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="99c16-114">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="99c16-114">Element Information</span></span>



|                            |                     |
|----------------------------|---------------------|
| <span data-ttu-id="99c16-115">Nome</span><span class="sxs-lookup"><span data-stu-id="99c16-115">Name</span></span>                       |                     |
| <span data-ttu-id="99c16-116">Tipo de elemento</span><span class="sxs-lookup"><span data-stu-id="99c16-116">Element Type</span></span><br/>    | <span data-ttu-id="99c16-117">Propriedade</span><span class="sxs-lookup"><span data-stu-id="99c16-117">Property</span></span><br/> |
| <span data-ttu-id="99c16-118">Prefixo de escopo</span><span class="sxs-lookup"><span data-stu-id="99c16-118">Scoping Prefix</span></span> <br/> | <span data-ttu-id="99c16-119">?</span><span class="sxs-lookup"><span data-stu-id="99c16-119">Page</span></span><br/>     |
| <span data-ttu-id="99c16-120">Observações</span><span class="sxs-lookup"><span data-stu-id="99c16-120">Notes</span></span> <br/>          | <span data-ttu-id="99c16-121">Nenhum</span><span class="sxs-lookup"><span data-stu-id="99c16-121">None</span></span><br/>     |



 

## <a name="structural-content"></a><span data-ttu-id="99c16-122">Conteúdo estrutural</span><span class="sxs-lookup"><span data-stu-id="99c16-122">Structural Content</span></span>

<span data-ttu-id="99c16-123">A estrutura XML desse elemento é:</span><span class="sxs-lookup"><span data-stu-id="99c16-123">The XML structure of this element is:</span></span>

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

## <a name="structure-variables"></a><span data-ttu-id="99c16-124">Variáveis de estrutura</span><span class="sxs-lookup"><span data-stu-id="99c16-124">Structure Variables</span></span>

<span data-ttu-id="99c16-125">A tabela a seguir descreve as características das variáveis definidas na estrutura XML.</span><span class="sxs-lookup"><span data-stu-id="99c16-125">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="99c16-126">Nome</span><span class="sxs-lookup"><span data-stu-id="99c16-126">Name</span></span>                                    | <span data-ttu-id="99c16-127">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="99c16-127">Data type</span></span>          | <span data-ttu-id="99c16-128">Unidade</span><span class="sxs-lookup"><span data-stu-id="99c16-128">Unit</span></span>               | <span data-ttu-id="99c16-129">Valores com suporte</span><span class="sxs-lookup"><span data-stu-id="99c16-129">Supported values</span></span>                       | <span data-ttu-id="99c16-130">Resumo</span><span class="sxs-lookup"><span data-stu-id="99c16-130">Summary</span></span>                                                                                                                    |
|-----------------------------------------|--------------------|--------------------|----------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="99c16-131">\_ImageableSizeWidthValue\_</span><span class="sxs-lookup"><span data-stu-id="99c16-131">\_ImageableSizeWidthValue\_</span></span><br/>  | <span data-ttu-id="99c16-132">Número inteiro</span><span class="sxs-lookup"><span data-stu-id="99c16-132">integer</span></span><br/> | <span data-ttu-id="99c16-133">mícrons</span><span class="sxs-lookup"><span data-stu-id="99c16-133">microns</span></span><br/> | <span data-ttu-id="99c16-134">Maior que 0.</span><span class="sxs-lookup"><span data-stu-id="99c16-134">Greater than 0.</span></span><br/>             | <span data-ttu-id="99c16-135">Especifica a dimensão horizontal do tamanho da mídia do aplicativo em relação ao PageOrientation.</span><span class="sxs-lookup"><span data-stu-id="99c16-135">Specifies the horizontal dimension of the application media size relative to the PageOrientation.</span></span><br/>               |
| <span data-ttu-id="99c16-136">\_ImageableSizeHeightValue\_</span><span class="sxs-lookup"><span data-stu-id="99c16-136">\_ImageableSizeHeightValue\_</span></span><br/> | <span data-ttu-id="99c16-137">Número inteiro</span><span class="sxs-lookup"><span data-stu-id="99c16-137">integer</span></span><br/> | <span data-ttu-id="99c16-138">mícrons</span><span class="sxs-lookup"><span data-stu-id="99c16-138">microns</span></span><br/> | <span data-ttu-id="99c16-139">Maior que 0.</span><span class="sxs-lookup"><span data-stu-id="99c16-139">Greater than 0.</span></span><br/>             | <span data-ttu-id="99c16-140">Especifica a dimensão vertical do tamanho da mídia do aplicativo em relação ao PageOrientation.</span><span class="sxs-lookup"><span data-stu-id="99c16-140">Specifies the vertical dimension of the application media size relative to the PageOrientation.</span></span><br/>                 |
| <span data-ttu-id="99c16-141">\_OriginWidthValue\_</span><span class="sxs-lookup"><span data-stu-id="99c16-141">\_OriginWidthValue\_</span></span><br/>         | <span data-ttu-id="99c16-142">Número inteiro</span><span class="sxs-lookup"><span data-stu-id="99c16-142">integer</span></span><br/> | <span data-ttu-id="99c16-143">mícrons</span><span class="sxs-lookup"><span data-stu-id="99c16-143">microns</span></span><br/> | <span data-ttu-id="99c16-144">Maior ou igual a 0.</span><span class="sxs-lookup"><span data-stu-id="99c16-144">Greater than or equal to 0.</span></span><br/> | <span data-ttu-id="99c16-145">Especifica a origem horizontal da área de imagem em relação ao tamanho da mídia do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="99c16-145">Specifies the horizontal origin of the imageable area relative to the application media size.</span></span><br/>                   |
| <span data-ttu-id="99c16-146">\_OriginHeightValue\_</span><span class="sxs-lookup"><span data-stu-id="99c16-146">\_OriginHeightValue\_</span></span><br/>        | <span data-ttu-id="99c16-147">Número inteiro</span><span class="sxs-lookup"><span data-stu-id="99c16-147">integer</span></span><br/> | <span data-ttu-id="99c16-148">mícrons</span><span class="sxs-lookup"><span data-stu-id="99c16-148">microns</span></span><br/> | <span data-ttu-id="99c16-149">Maior ou igual a 0.</span><span class="sxs-lookup"><span data-stu-id="99c16-149">Greater than or equal to 0.</span></span><br/> | <span data-ttu-id="99c16-150">Especifica a origem vertical da área de imagem em relação ao tamanho da mídia do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="99c16-150">Specifies the vertical origin of the imageable area relative to the application media size.</span></span><br/>                     |
| <span data-ttu-id="99c16-151">\_ExtentWidthValue\_</span><span class="sxs-lookup"><span data-stu-id="99c16-151">\_ExtentWidthValue\_</span></span><br/>         | <span data-ttu-id="99c16-152">Número inteiro</span><span class="sxs-lookup"><span data-stu-id="99c16-152">integer</span></span><br/> | <span data-ttu-id="99c16-153">mícrons</span><span class="sxs-lookup"><span data-stu-id="99c16-153">microns</span></span><br/> | <span data-ttu-id="99c16-154">Maior que 0.</span><span class="sxs-lookup"><span data-stu-id="99c16-154">Greater than 0.</span></span><br/>             | <span data-ttu-id="99c16-155">Especifica a distância horizontal entre a origem e o limite delimitador do tamanho da mídia do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="99c16-155">Specifies the horizontal distance between the origin and the bounding limit of the application media size.</span></span><br/>      |
| <span data-ttu-id="99c16-156">\_ExtentHeightValue\_</span><span class="sxs-lookup"><span data-stu-id="99c16-156">\_ExtentHeightValue\_</span></span><br/>        | <span data-ttu-id="99c16-157">Número inteiro</span><span class="sxs-lookup"><span data-stu-id="99c16-157">integer</span></span><br/> | <span data-ttu-id="99c16-158">mícrons</span><span class="sxs-lookup"><span data-stu-id="99c16-158">microns</span></span><br/> | <span data-ttu-id="99c16-159">Maior que 0.</span><span class="sxs-lookup"><span data-stu-id="99c16-159">Greater than 0.</span></span><br/>             | <span data-ttu-id="99c16-160">Especifica a distância vertical entre a origem e o limite delimitador do tamanho da mídia do aplicativo Canvas.</span><span class="sxs-lookup"><span data-stu-id="99c16-160">Specifies the vertical distance between the origin and the bounding limit of the canvas application media size.</span></span><br/> |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="99c16-161">Conteúdo de linguagem XML (XML)</span><span class="sxs-lookup"><span data-stu-id="99c16-161">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="99c16-162">As palavras-chave do esquema de impressão pública são definidas no https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span><span class="sxs-lookup"><span data-stu-id="99c16-162">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="99c16-163">O conteúdo do linguagem XML público (XML) para essa palavra-chave é definido abaixo:</span><span class="sxs-lookup"><span data-stu-id="99c16-163">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

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

## <a name="related-topics"></a><span data-ttu-id="99c16-164">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="99c16-164">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="99c16-165">Especificação de esquema de impressão</span><span class="sxs-lookup"><span data-stu-id="99c16-165">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




