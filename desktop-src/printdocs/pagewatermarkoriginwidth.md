---
description: Este tópico não é atual. Para obter as informações mais atuais, consulte a especificação do esquema de impressão.
ms.assetid: e1bea06b-11b9-4652-915a-deb563ad59f8
title: PageWatermarkOriginWidth
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6780dd5cc3b90a4f15cb6ada66ab82c4269acd82
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/05/2021
ms.locfileid: "103837704"
---
# <a name="pagewatermarkoriginwidth"></a><span data-ttu-id="badec-104">PageWatermarkOriginWidth</span><span class="sxs-lookup"><span data-stu-id="badec-104">PageWatermarkOriginWidth</span></span>

<span data-ttu-id="badec-105">Este tópico não é atual.</span><span class="sxs-lookup"><span data-stu-id="badec-105">This topic is not current.</span></span> <span data-ttu-id="badec-106">Para obter as informações mais atuais, consulte a [especificação do esquema de impressão](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="badec-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="badec-107">Especifica a origem de uma marca d' água em relação à origem do PageImageableSize.</span><span class="sxs-lookup"><span data-stu-id="badec-107">Specifies the origin of a watermark relative to the origin of the PageImageableSize.</span></span>

-   [<span data-ttu-id="badec-108">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="badec-108">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="badec-109">Conteúdo da estrutura</span><span class="sxs-lookup"><span data-stu-id="badec-109">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="badec-110">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="badec-110">Element Information</span></span>



| <span data-ttu-id="badec-111">Nome</span><span class="sxs-lookup"><span data-stu-id="badec-111">Name</span></span>                       |                                            |
|----------------------------|--------------------------------------------|
| <span data-ttu-id="badec-112">Tipo de elemento</span><span class="sxs-lookup"><span data-stu-id="badec-112">Element Type</span></span> <br/>   | <span data-ttu-id="badec-113">ParameterDef</span><span class="sxs-lookup"><span data-stu-id="badec-113">ParameterDef</span></span><br/>                    |
| <span data-ttu-id="badec-114">Prefixo de escopo</span><span class="sxs-lookup"><span data-stu-id="badec-114">Scoping Prefix</span></span> <br/> | <span data-ttu-id="badec-115">?</span><span class="sxs-lookup"><span data-stu-id="badec-115">Page</span></span><br/>                            |
| <span data-ttu-id="badec-116">Observações</span><span class="sxs-lookup"><span data-stu-id="badec-116">Notes</span></span> <br/>          | <span data-ttu-id="badec-117">Vinculado ao elemento PageWatermark</span><span class="sxs-lookup"><span data-stu-id="badec-117">Linked to PageWatermark element</span></span><br/> |



 

## <a name="structure-content"></a><span data-ttu-id="badec-118">Conteúdo da estrutura</span><span class="sxs-lookup"><span data-stu-id="badec-118">Structure Content</span></span>

<span data-ttu-id="badec-119">A estrutura XML desse elemento é:</span><span class="sxs-lookup"><span data-stu-id="badec-119">The XML structure of this element is:</span></span>

``` syntax
<psf:ParameterDef name="psk:PageWatermarkOriginWidth">
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
    <psf:Value xsi:type="xs:integer">0</psf:Value>
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

## <a name="structure-properties"></a><span data-ttu-id="badec-120">Propriedades da estrutura</span><span class="sxs-lookup"><span data-stu-id="badec-120">Structure Properties</span></span>

<span data-ttu-id="badec-121">A tabela a seguir descreve as características das variáveis definidas na estrutura XML.</span><span class="sxs-lookup"><span data-stu-id="badec-121">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="badec-122">Propriedade</span><span class="sxs-lookup"><span data-stu-id="badec-122">Property</span></span>                | <span data-ttu-id="badec-123">xsi:type</span><span class="sxs-lookup"><span data-stu-id="badec-123">xsi:type</span></span>           | <span data-ttu-id="badec-124">Valor</span><span class="sxs-lookup"><span data-stu-id="badec-124">Value</span></span>                                                                  |
|-------------------------|--------------------|------------------------------------------------------------------------|
| <span data-ttu-id="badec-125">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="badec-125">DataType</span></span><br/>     | <span data-ttu-id="badec-126">string</span><span class="sxs-lookup"><span data-stu-id="badec-126">string</span></span><br/>  | <span data-ttu-id="badec-127">xs:integer</span><span class="sxs-lookup"><span data-stu-id="badec-127">xs:integer</span></span><br/>                                                  |
| <span data-ttu-id="badec-128">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="badec-128">DefaultValue</span></span><br/> | <span data-ttu-id="badec-129">Número inteiro</span><span class="sxs-lookup"><span data-stu-id="badec-129">integer</span></span><br/> | <span data-ttu-id="badec-130">não definido</span><span class="sxs-lookup"><span data-stu-id="badec-130">undefined</span></span><br/>                                                   |
| <span data-ttu-id="badec-131">MaxValue</span><span class="sxs-lookup"><span data-stu-id="badec-131">MaxValue</span></span><br/>     | <span data-ttu-id="badec-132">Número inteiro</span><span class="sxs-lookup"><span data-stu-id="badec-132">integer</span></span><br/> | <span data-ttu-id="badec-133">Menor ou igual ao valor de PageImageableSize-ExtentWidth</span><span class="sxs-lookup"><span data-stu-id="badec-133">Less than or equal to PageImageableSize - ExtentWidth value</span></span><br/> |
| <span data-ttu-id="badec-134">MinValue</span><span class="sxs-lookup"><span data-stu-id="badec-134">MinValue</span></span><br/>     | <span data-ttu-id="badec-135">integer</span><span class="sxs-lookup"><span data-stu-id="badec-135">integer</span></span><br/> | <span data-ttu-id="badec-136">0</span><span class="sxs-lookup"><span data-stu-id="badec-136">0</span></span><br/>                                                           |
| <span data-ttu-id="badec-137">Vários</span><span class="sxs-lookup"><span data-stu-id="badec-137">Multiple</span></span><br/>     | <span data-ttu-id="badec-138">integer</span><span class="sxs-lookup"><span data-stu-id="badec-138">integer</span></span><br/> | <span data-ttu-id="badec-139">1</span><span class="sxs-lookup"><span data-stu-id="badec-139">1</span></span><br/>                                                           |
| <span data-ttu-id="badec-140">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="badec-140">Mandatory</span></span><br/>    | <span data-ttu-id="badec-141">string</span><span class="sxs-lookup"><span data-stu-id="badec-141">string</span></span><br/>  | <span data-ttu-id="badec-142">PSK: condicional</span><span class="sxs-lookup"><span data-stu-id="badec-142">psk:Conditional</span></span><br/>                                             |
| <span data-ttu-id="badec-143">UnitType</span><span class="sxs-lookup"><span data-stu-id="badec-143">UnitType</span></span><br/>     | <span data-ttu-id="badec-144">string</span><span class="sxs-lookup"><span data-stu-id="badec-144">string</span></span><br/>  | <span data-ttu-id="badec-145">mícrons</span><span class="sxs-lookup"><span data-stu-id="badec-145">microns</span></span><br/>                                                     |



 

## <a name="related-topics"></a><span data-ttu-id="badec-146">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="badec-146">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="badec-147">Especificação de esquema de impressão</span><span class="sxs-lookup"><span data-stu-id="badec-147">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




