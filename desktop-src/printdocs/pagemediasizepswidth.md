---
description: Obtenha informações sobre o parâmetro PageMediaSizePSWidth. Este tópico não é atual. Para obter as informações mais atuais, consulte a especificação do esquema de impressão.
ms.assetid: a1a684ce-5615-4ff7-a7aa-5c9f786f84ed
title: PageMediaSizePSWidth
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dfe678107d2a183ee0f0bf6ce290dfe230fa8cc2
ms.sourcegitcommit: 91530c19d26ba4c57a6af1f37b57f211f580464e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/19/2021
ms.locfileid: "112395641"
---
# <a name="pagemediasizepswidth"></a><span data-ttu-id="a102f-105">PageMediaSizePSWidth</span><span class="sxs-lookup"><span data-stu-id="a102f-105">PageMediaSizePSWidth</span></span>

<span data-ttu-id="a102f-106">Este tópico não é atual.</span><span class="sxs-lookup"><span data-stu-id="a102f-106">This topic is not current.</span></span> <span data-ttu-id="a102f-107">Para obter as informações mais atuais, consulte a [especificação do esquema de impressão](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="a102f-107">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="a102f-108">Especifica a largura da página perpendicular à direção da orientação do feed (referência à [especificação de formato de arquivo de descrição de impressora PostScript](https://www.adobe.com/products/postscript/pdfs/PLRM.pdf)).</span><span class="sxs-lookup"><span data-stu-id="a102f-108">Specifies the width of the page perpendicular to the feed-orientation direction (Reference [PostScript Printer Description File Format Specification](https://www.adobe.com/products/postscript/pdfs/PLRM.pdf)).</span></span>

-   [<span data-ttu-id="a102f-109">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="a102f-109">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="a102f-110">Conteúdo da estrutura</span><span class="sxs-lookup"><span data-stu-id="a102f-110">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="a102f-111">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="a102f-111">Element Information</span></span>



| <span data-ttu-id="a102f-112">Name</span><span class="sxs-lookup"><span data-stu-id="a102f-112">Name</span></span> | <span data-ttu-id="a102f-113">Valor</span><span class="sxs-lookup"><span data-stu-id="a102f-113">Value</span></span> |
|----------------------------|-------------------------------------------------------------|
| <span data-ttu-id="a102f-114">Tipo de elemento</span><span class="sxs-lookup"><span data-stu-id="a102f-114">Element Type</span></span> <br/>   | <span data-ttu-id="a102f-115">ParameterDef</span><span class="sxs-lookup"><span data-stu-id="a102f-115">ParameterDef</span></span><br/>                                     |
| <span data-ttu-id="a102f-116">Prefixo de escopo</span><span class="sxs-lookup"><span data-stu-id="a102f-116">Scoping Prefix</span></span> <br/> | <span data-ttu-id="a102f-117">?</span><span class="sxs-lookup"><span data-stu-id="a102f-117">Page</span></span><br/>                                             |
| <span data-ttu-id="a102f-118">Observações</span><span class="sxs-lookup"><span data-stu-id="a102f-118">Notes</span></span> <br/>          | <span data-ttu-id="a102f-119">Vinculado ao elemento PageMediaSize, opção CustomPS</span><span class="sxs-lookup"><span data-stu-id="a102f-119">Linked to PageMediaSize element, CustomPS option</span></span><br/> |



 

## <a name="structure-content"></a><span data-ttu-id="a102f-120">Conteúdo da estrutura</span><span class="sxs-lookup"><span data-stu-id="a102f-120">Structure Content</span></span>

<span data-ttu-id="a102f-121">A estrutura XML desse elemento é:</span><span class="sxs-lookup"><span data-stu-id="a102f-121">The XML structure of this element is:</span></span>

``` syntax
<psf:ParameterDef name="psk:PageMediaSizePSWidth">
  <psf:Property name="psf:DataType">
    <psf:Value xsi:type="xs:string">xs:integer</psf:Value>
  </psf:Property>
  <psf:Property name="psf:DefaultValue">
    <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
  </psf:Property>
  <psf:Property name="psf:MaxValue">
    <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
  </psf:Property>
  <psf:Property name="psf:MinValue">
    <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
  </psf:Property>
  <psf:Property name="psf:Multiple">
    <psf:Value xsi:type="xs:integer">1</psf:Value>
  </psf:Property>
  <psf:Property name="psf:Mandatory">
    <psf:Value xsi:type="xs:string">psk:Conditional</psf:Value>
  </psf:Property>
  <psf:Property name="psf:UnitType">
    <psf:Value xsi:type="xs:string">microns</psf:Value>
  </psf:Property>
</psf:ParameterDef>
      
```

## <a name="structure-properties"></a><span data-ttu-id="a102f-122">Propriedades da estrutura</span><span class="sxs-lookup"><span data-stu-id="a102f-122">Structure Properties</span></span>

<span data-ttu-id="a102f-123">A tabela a seguir descreve as características das variáveis definidas na estrutura XML.</span><span class="sxs-lookup"><span data-stu-id="a102f-123">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="a102f-124">Propriedade</span><span class="sxs-lookup"><span data-stu-id="a102f-124">Property</span></span>                | <span data-ttu-id="a102f-125">xsi:type</span><span class="sxs-lookup"><span data-stu-id="a102f-125">xsi:type</span></span>           | <span data-ttu-id="a102f-126">Valor</span><span class="sxs-lookup"><span data-stu-id="a102f-126">Value</span></span>                      |
|-------------------------|--------------------|----------------------------|
| <span data-ttu-id="a102f-127">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="a102f-127">DataType</span></span><br/>     | <span data-ttu-id="a102f-128">string</span><span class="sxs-lookup"><span data-stu-id="a102f-128">string</span></span><br/>  | <span data-ttu-id="a102f-129">xs:integer</span><span class="sxs-lookup"><span data-stu-id="a102f-129">xs:integer</span></span><br/>      |
| <span data-ttu-id="a102f-130">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="a102f-130">DefaultValue</span></span><br/> | <span data-ttu-id="a102f-131">Número inteiro</span><span class="sxs-lookup"><span data-stu-id="a102f-131">integer</span></span><br/> | <span data-ttu-id="a102f-132">não definido</span><span class="sxs-lookup"><span data-stu-id="a102f-132">undefined</span></span><br/>       |
| <span data-ttu-id="a102f-133">MaxValue</span><span class="sxs-lookup"><span data-stu-id="a102f-133">MaxValue</span></span><br/>     | <span data-ttu-id="a102f-134">Número inteiro</span><span class="sxs-lookup"><span data-stu-id="a102f-134">integer</span></span><br/> | <span data-ttu-id="a102f-135">não definido</span><span class="sxs-lookup"><span data-stu-id="a102f-135">undefined</span></span><br/>       |
| <span data-ttu-id="a102f-136">MinValue</span><span class="sxs-lookup"><span data-stu-id="a102f-136">MinValue</span></span><br/>     | <span data-ttu-id="a102f-137">Número inteiro</span><span class="sxs-lookup"><span data-stu-id="a102f-137">integer</span></span><br/> | <span data-ttu-id="a102f-138">não definido</span><span class="sxs-lookup"><span data-stu-id="a102f-138">undefined</span></span><br/>       |
| <span data-ttu-id="a102f-139">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="a102f-139">Mandatory</span></span><br/>    | <span data-ttu-id="a102f-140">string</span><span class="sxs-lookup"><span data-stu-id="a102f-140">string</span></span><br/>  | <span data-ttu-id="a102f-141">PSK: condicional</span><span class="sxs-lookup"><span data-stu-id="a102f-141">psk:Conditional</span></span><br/> |
| <span data-ttu-id="a102f-142">Vários</span><span class="sxs-lookup"><span data-stu-id="a102f-142">Multiple</span></span><br/>     | <span data-ttu-id="a102f-143">integer</span><span class="sxs-lookup"><span data-stu-id="a102f-143">integer</span></span><br/> | <span data-ttu-id="a102f-144">1</span><span class="sxs-lookup"><span data-stu-id="a102f-144">1</span></span><br/>               |
| <span data-ttu-id="a102f-145">UnitType</span><span class="sxs-lookup"><span data-stu-id="a102f-145">UnitType</span></span><br/>     | <span data-ttu-id="a102f-146">string</span><span class="sxs-lookup"><span data-stu-id="a102f-146">string</span></span><br/>  | <span data-ttu-id="a102f-147">mícrons</span><span class="sxs-lookup"><span data-stu-id="a102f-147">microns</span></span><br/>         |



 

## <a name="related-topics"></a><span data-ttu-id="a102f-148">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="a102f-148">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a102f-149">Especificação de formato de arquivo de descrição de impressora PostScript</span><span class="sxs-lookup"><span data-stu-id="a102f-149">PostScript Printer Description File Format Specification</span></span>](https://www.adobe.com/products/postscript/pdfs/PLRM.pdf)
</dt> <dt>

[<span data-ttu-id="a102f-150">Especificação de esquema de impressão</span><span class="sxs-lookup"><span data-stu-id="a102f-150">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




