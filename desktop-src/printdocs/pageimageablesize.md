---
description: Saiba mais sobre o elemento PageImageableSize configurável pelo usuário. Este tópico não é atual. Para obter as informações mais atuais, consulte a especificação do esquema de impressão.
ms.assetid: 6b81814f-2d9e-4862-8633-6ba016c11dac
title: PageImageableSize
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ee4e44bc9afe33b87d32b43c93eafc3b6d4ba4b0
ms.sourcegitcommit: 91530c19d26ba4c57a6af1f37b57f211f580464e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/19/2021
ms.locfileid: "112395301"
---
# <a name="pageimageablesize"></a><span data-ttu-id="d05dc-105">PageImageableSize</span><span class="sxs-lookup"><span data-stu-id="d05dc-105">PageImageableSize</span></span>

<span data-ttu-id="d05dc-106">Este tópico não é atual.</span><span class="sxs-lookup"><span data-stu-id="d05dc-106">This topic is not current.</span></span> <span data-ttu-id="d05dc-107">Para obter as informações mais atuais, consulte a [especificação do esquema de impressão](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="d05dc-107">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="d05dc-108">Descreve a tela de imagem para layout e renderização.</span><span class="sxs-lookup"><span data-stu-id="d05dc-108">Describes the imaged canvas for layout and rendering.</span></span> <span data-ttu-id="d05dc-109">Isso será relatado com base em PageMediaSize e PageOrientation.</span><span class="sxs-lookup"><span data-stu-id="d05dc-109">This will be reported based on PageMediaSize and PageOrientation.</span></span>

<span data-ttu-id="d05dc-110">Os diagramas a seguir ilustram o uso de variáveis PageImageableSize com base em PageOrientation.</span><span class="sxs-lookup"><span data-stu-id="d05dc-110">The following diagrams illustrate the PageImageableSize variables usage based on PageOrientation.</span></span>

![um diagrama que mostra as medidas de página](images/local-1641910626-image.png)

-   [<span data-ttu-id="d05dc-112">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="d05dc-112">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="d05dc-113">Conteúdo estrutural</span><span class="sxs-lookup"><span data-stu-id="d05dc-113">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="d05dc-114">Conteúdo de linguagem XML (XML)</span><span class="sxs-lookup"><span data-stu-id="d05dc-114">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="d05dc-115">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="d05dc-115">Element Information</span></span>

| <span data-ttu-id="d05dc-116">Name</span><span class="sxs-lookup"><span data-stu-id="d05dc-116">Name</span></span>                 | <span data-ttu-id="d05dc-117">Valor</span><span class="sxs-lookup"><span data-stu-id="d05dc-117">Value</span></span>         |
|----------------------|---------------|
| <span data-ttu-id="d05dc-118">Tipo de elemento</span><span class="sxs-lookup"><span data-stu-id="d05dc-118">Element Type</span></span><br/>    | <span data-ttu-id="d05dc-119">Propriedade</span><span class="sxs-lookup"><span data-stu-id="d05dc-119">Property</span></span><br/> |
| <span data-ttu-id="d05dc-120">Prefixo de escopo</span><span class="sxs-lookup"><span data-stu-id="d05dc-120">Scoping Prefix</span></span> <br/> | <span data-ttu-id="d05dc-121">?</span><span class="sxs-lookup"><span data-stu-id="d05dc-121">Page</span></span><br/>     |
| <span data-ttu-id="d05dc-122">Observações</span><span class="sxs-lookup"><span data-stu-id="d05dc-122">Notes</span></span> <br/>          | <span data-ttu-id="d05dc-123">Nenhum</span><span class="sxs-lookup"><span data-stu-id="d05dc-123">None</span></span><br/>     |

## <a name="structural-content"></a><span data-ttu-id="d05dc-124">Conteúdo estrutural</span><span class="sxs-lookup"><span data-stu-id="d05dc-124">Structural Content</span></span>

<span data-ttu-id="d05dc-125">A estrutura XML desse elemento é:</span><span class="sxs-lookup"><span data-stu-id="d05dc-125">The XML structure of this element is:</span></span>

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

## <a name="structure-variables"></a><span data-ttu-id="d05dc-126">Variáveis de estrutura</span><span class="sxs-lookup"><span data-stu-id="d05dc-126">Structure Variables</span></span>

<span data-ttu-id="d05dc-127">A tabela a seguir descreve as características das variáveis definidas na estrutura XML.</span><span class="sxs-lookup"><span data-stu-id="d05dc-127">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="d05dc-128">Nome</span><span class="sxs-lookup"><span data-stu-id="d05dc-128">Name</span></span>                                    | <span data-ttu-id="d05dc-129">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="d05dc-129">Data type</span></span>          | <span data-ttu-id="d05dc-130">Unidade</span><span class="sxs-lookup"><span data-stu-id="d05dc-130">Unit</span></span>               | <span data-ttu-id="d05dc-131">Valores com suporte</span><span class="sxs-lookup"><span data-stu-id="d05dc-131">Supported values</span></span>                       | <span data-ttu-id="d05dc-132">Resumo</span><span class="sxs-lookup"><span data-stu-id="d05dc-132">Summary</span></span>                                                                                                                    |
|-----------------------------------------|--------------------|--------------------|----------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d05dc-133">\_ImageableSizeWidthValue\_</span><span class="sxs-lookup"><span data-stu-id="d05dc-133">\_ImageableSizeWidthValue\_</span></span><br/>  | <span data-ttu-id="d05dc-134">Número inteiro</span><span class="sxs-lookup"><span data-stu-id="d05dc-134">integer</span></span><br/> | <span data-ttu-id="d05dc-135">mícrons</span><span class="sxs-lookup"><span data-stu-id="d05dc-135">microns</span></span><br/> | <span data-ttu-id="d05dc-136">Maior que 0.</span><span class="sxs-lookup"><span data-stu-id="d05dc-136">Greater than 0.</span></span><br/>             | <span data-ttu-id="d05dc-137">Especifica a dimensão horizontal do tamanho da mídia do aplicativo em relação ao PageOrientation.</span><span class="sxs-lookup"><span data-stu-id="d05dc-137">Specifies the horizontal dimension of the application media size relative to the PageOrientation.</span></span><br/>               |
| <span data-ttu-id="d05dc-138">\_ImageableSizeHeightValue\_</span><span class="sxs-lookup"><span data-stu-id="d05dc-138">\_ImageableSizeHeightValue\_</span></span><br/> | <span data-ttu-id="d05dc-139">Número inteiro</span><span class="sxs-lookup"><span data-stu-id="d05dc-139">integer</span></span><br/> | <span data-ttu-id="d05dc-140">mícrons</span><span class="sxs-lookup"><span data-stu-id="d05dc-140">microns</span></span><br/> | <span data-ttu-id="d05dc-141">Maior que 0.</span><span class="sxs-lookup"><span data-stu-id="d05dc-141">Greater than 0.</span></span><br/>             | <span data-ttu-id="d05dc-142">Especifica a dimensão vertical do tamanho da mídia do aplicativo em relação ao PageOrientation.</span><span class="sxs-lookup"><span data-stu-id="d05dc-142">Specifies the vertical dimension of the application media size relative to the PageOrientation.</span></span><br/>                 |
| <span data-ttu-id="d05dc-143">\_OriginWidthValue\_</span><span class="sxs-lookup"><span data-stu-id="d05dc-143">\_OriginWidthValue\_</span></span><br/>         | <span data-ttu-id="d05dc-144">Número inteiro</span><span class="sxs-lookup"><span data-stu-id="d05dc-144">integer</span></span><br/> | <span data-ttu-id="d05dc-145">mícrons</span><span class="sxs-lookup"><span data-stu-id="d05dc-145">microns</span></span><br/> | <span data-ttu-id="d05dc-146">Maior ou igual a 0.</span><span class="sxs-lookup"><span data-stu-id="d05dc-146">Greater than or equal to 0.</span></span><br/> | <span data-ttu-id="d05dc-147">Especifica a origem horizontal da área de imagem em relação ao tamanho da mídia do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="d05dc-147">Specifies the horizontal origin of the imageable area relative to the application media size.</span></span><br/>                   |
| <span data-ttu-id="d05dc-148">\_OriginHeightValue\_</span><span class="sxs-lookup"><span data-stu-id="d05dc-148">\_OriginHeightValue\_</span></span><br/>        | <span data-ttu-id="d05dc-149">Número inteiro</span><span class="sxs-lookup"><span data-stu-id="d05dc-149">integer</span></span><br/> | <span data-ttu-id="d05dc-150">mícrons</span><span class="sxs-lookup"><span data-stu-id="d05dc-150">microns</span></span><br/> | <span data-ttu-id="d05dc-151">Maior ou igual a 0.</span><span class="sxs-lookup"><span data-stu-id="d05dc-151">Greater than or equal to 0.</span></span><br/> | <span data-ttu-id="d05dc-152">Especifica a origem vertical da área de imagem em relação ao tamanho da mídia do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="d05dc-152">Specifies the vertical origin of the imageable area relative to the application media size.</span></span><br/>                     |
| <span data-ttu-id="d05dc-153">\_ExtentWidthValue\_</span><span class="sxs-lookup"><span data-stu-id="d05dc-153">\_ExtentWidthValue\_</span></span><br/>         | <span data-ttu-id="d05dc-154">Número inteiro</span><span class="sxs-lookup"><span data-stu-id="d05dc-154">integer</span></span><br/> | <span data-ttu-id="d05dc-155">mícrons</span><span class="sxs-lookup"><span data-stu-id="d05dc-155">microns</span></span><br/> | <span data-ttu-id="d05dc-156">Maior que 0.</span><span class="sxs-lookup"><span data-stu-id="d05dc-156">Greater than 0.</span></span><br/>             | <span data-ttu-id="d05dc-157">Especifica a distância horizontal entre a origem e o limite delimitador do tamanho da mídia do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="d05dc-157">Specifies the horizontal distance between the origin and the bounding limit of the application media size.</span></span><br/>      |
| <span data-ttu-id="d05dc-158">\_ExtentHeightValue\_</span><span class="sxs-lookup"><span data-stu-id="d05dc-158">\_ExtentHeightValue\_</span></span><br/>        | <span data-ttu-id="d05dc-159">Número inteiro</span><span class="sxs-lookup"><span data-stu-id="d05dc-159">integer</span></span><br/> | <span data-ttu-id="d05dc-160">mícrons</span><span class="sxs-lookup"><span data-stu-id="d05dc-160">microns</span></span><br/> | <span data-ttu-id="d05dc-161">Maior que 0.</span><span class="sxs-lookup"><span data-stu-id="d05dc-161">Greater than 0.</span></span><br/>             | <span data-ttu-id="d05dc-162">Especifica a distância vertical entre a origem e o limite delimitador do tamanho da mídia do aplicativo Canvas.</span><span class="sxs-lookup"><span data-stu-id="d05dc-162">Specifies the vertical distance between the origin and the bounding limit of the canvas application media size.</span></span><br/> |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="d05dc-163">Conteúdo de linguagem XML (XML)</span><span class="sxs-lookup"><span data-stu-id="d05dc-163">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="d05dc-164">As palavras-chave do esquema de impressão pública são definidas no https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span><span class="sxs-lookup"><span data-stu-id="d05dc-164">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="d05dc-165">O conteúdo do linguagem XML público (XML) para essa palavra-chave é definido abaixo:</span><span class="sxs-lookup"><span data-stu-id="d05dc-165">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

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

## <a name="related-topics"></a><span data-ttu-id="d05dc-166">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="d05dc-166">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d05dc-167">Especificação de esquema de impressão</span><span class="sxs-lookup"><span data-stu-id="d05dc-167">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




