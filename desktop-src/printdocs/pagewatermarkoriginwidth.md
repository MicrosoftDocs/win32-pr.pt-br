---
description: Obter informações sobre o parâmetro PageWatermarkOriginWidth. Este tópico não é atual. Para obter as informações mais atuais, consulte a Especificação de Esquema de Impressão.
ms.assetid: e1bea06b-11b9-4652-915a-deb563ad59f8
title: PageWatermarkOriginWidth
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bffe6457496972231877af2a51e03bc5109083d0
ms.sourcegitcommit: 91530c19d26ba4c57a6af1f37b57f211f580464e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/19/2021
ms.locfileid: "112396001"
---
# <a name="pagewatermarkoriginwidth"></a><span data-ttu-id="87aa9-105">PageWatermarkOriginWidth</span><span class="sxs-lookup"><span data-stu-id="87aa9-105">PageWatermarkOriginWidth</span></span>

<span data-ttu-id="87aa9-106">Este tópico não é atual.</span><span class="sxs-lookup"><span data-stu-id="87aa9-106">This topic is not current.</span></span> <span data-ttu-id="87aa9-107">Para obter as informações mais atuais, consulte a [Especificação de Esquema de Impressão](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="87aa9-107">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="87aa9-108">Especifica a origem de uma marca-d'água em relação à origem de PageImageableSize.</span><span class="sxs-lookup"><span data-stu-id="87aa9-108">Specifies the origin of a watermark relative to the origin of the PageImageableSize.</span></span>

-   [<span data-ttu-id="87aa9-109">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="87aa9-109">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="87aa9-110">Conteúdo da estrutura</span><span class="sxs-lookup"><span data-stu-id="87aa9-110">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="87aa9-111">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="87aa9-111">Element Information</span></span>



| <span data-ttu-id="87aa9-112">Name</span><span class="sxs-lookup"><span data-stu-id="87aa9-112">Name</span></span> | <span data-ttu-id="87aa9-113">Valor</span><span class="sxs-lookup"><span data-stu-id="87aa9-113">Value</span></span> |
|----------------------------|--------------------------------------------|
| <span data-ttu-id="87aa9-114">Tipo de elemento</span><span class="sxs-lookup"><span data-stu-id="87aa9-114">Element Type</span></span> <br/>   | <span data-ttu-id="87aa9-115">ParameterDef</span><span class="sxs-lookup"><span data-stu-id="87aa9-115">ParameterDef</span></span><br/>                    |
| <span data-ttu-id="87aa9-116">Prefixo de definição de scoping</span><span class="sxs-lookup"><span data-stu-id="87aa9-116">Scoping Prefix</span></span> <br/> | <span data-ttu-id="87aa9-117">?</span><span class="sxs-lookup"><span data-stu-id="87aa9-117">Page</span></span><br/>                            |
| <span data-ttu-id="87aa9-118">Observações</span><span class="sxs-lookup"><span data-stu-id="87aa9-118">Notes</span></span> <br/>          | <span data-ttu-id="87aa9-119">Vinculado ao elemento PageWatermark</span><span class="sxs-lookup"><span data-stu-id="87aa9-119">Linked to PageWatermark element</span></span><br/> |



 

## <a name="structure-content"></a><span data-ttu-id="87aa9-120">Conteúdo da estrutura</span><span class="sxs-lookup"><span data-stu-id="87aa9-120">Structure Content</span></span>

<span data-ttu-id="87aa9-121">A estrutura XML desse elemento é:</span><span class="sxs-lookup"><span data-stu-id="87aa9-121">The XML structure of this element is:</span></span>

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

## <a name="structure-properties"></a><span data-ttu-id="87aa9-122">Propriedades da estrutura</span><span class="sxs-lookup"><span data-stu-id="87aa9-122">Structure Properties</span></span>

<span data-ttu-id="87aa9-123">A tabela a seguir descreve as características das variáveis definidas na estrutura XML.</span><span class="sxs-lookup"><span data-stu-id="87aa9-123">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="87aa9-124">Propriedade</span><span class="sxs-lookup"><span data-stu-id="87aa9-124">Property</span></span>                | <span data-ttu-id="87aa9-125">xsi:type</span><span class="sxs-lookup"><span data-stu-id="87aa9-125">xsi:type</span></span>           | <span data-ttu-id="87aa9-126">Valor</span><span class="sxs-lookup"><span data-stu-id="87aa9-126">Value</span></span>                                                                  |
|-------------------------|--------------------|------------------------------------------------------------------------|
| <span data-ttu-id="87aa9-127">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="87aa9-127">DataType</span></span><br/>     | <span data-ttu-id="87aa9-128">string</span><span class="sxs-lookup"><span data-stu-id="87aa9-128">string</span></span><br/>  | <span data-ttu-id="87aa9-129">xs:integer</span><span class="sxs-lookup"><span data-stu-id="87aa9-129">xs:integer</span></span><br/>                                                  |
| <span data-ttu-id="87aa9-130">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="87aa9-130">DefaultValue</span></span><br/> | <span data-ttu-id="87aa9-131">Número inteiro</span><span class="sxs-lookup"><span data-stu-id="87aa9-131">integer</span></span><br/> | <span data-ttu-id="87aa9-132">não definido</span><span class="sxs-lookup"><span data-stu-id="87aa9-132">undefined</span></span><br/>                                                   |
| <span data-ttu-id="87aa9-133">MaxValue</span><span class="sxs-lookup"><span data-stu-id="87aa9-133">MaxValue</span></span><br/>     | <span data-ttu-id="87aa9-134">Número inteiro</span><span class="sxs-lookup"><span data-stu-id="87aa9-134">integer</span></span><br/> | <span data-ttu-id="87aa9-135">Menor ou igual a PageImageableSize – valor ExtentWidth</span><span class="sxs-lookup"><span data-stu-id="87aa9-135">Less than or equal to PageImageableSize - ExtentWidth value</span></span><br/> |
| <span data-ttu-id="87aa9-136">Minvalue</span><span class="sxs-lookup"><span data-stu-id="87aa9-136">MinValue</span></span><br/>     | <span data-ttu-id="87aa9-137">inteiro</span><span class="sxs-lookup"><span data-stu-id="87aa9-137">integer</span></span><br/> | <span data-ttu-id="87aa9-138">0</span><span class="sxs-lookup"><span data-stu-id="87aa9-138">0</span></span><br/>                                                           |
| <span data-ttu-id="87aa9-139">Vários</span><span class="sxs-lookup"><span data-stu-id="87aa9-139">Multiple</span></span><br/>     | <span data-ttu-id="87aa9-140">integer</span><span class="sxs-lookup"><span data-stu-id="87aa9-140">integer</span></span><br/> | <span data-ttu-id="87aa9-141">1</span><span class="sxs-lookup"><span data-stu-id="87aa9-141">1</span></span><br/>                                                           |
| <span data-ttu-id="87aa9-142">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="87aa9-142">Mandatory</span></span><br/>    | <span data-ttu-id="87aa9-143">string</span><span class="sxs-lookup"><span data-stu-id="87aa9-143">string</span></span><br/>  | <span data-ttu-id="87aa9-144">psk:Conditional</span><span class="sxs-lookup"><span data-stu-id="87aa9-144">psk:Conditional</span></span><br/>                                             |
| <span data-ttu-id="87aa9-145">Unittype</span><span class="sxs-lookup"><span data-stu-id="87aa9-145">UnitType</span></span><br/>     | <span data-ttu-id="87aa9-146">string</span><span class="sxs-lookup"><span data-stu-id="87aa9-146">string</span></span><br/>  | <span data-ttu-id="87aa9-147">Mícrons</span><span class="sxs-lookup"><span data-stu-id="87aa9-147">microns</span></span><br/>                                                     |



 

## <a name="related-topics"></a><span data-ttu-id="87aa9-148">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="87aa9-148">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="87aa9-149">Especificação de esquema de impressão</span><span class="sxs-lookup"><span data-stu-id="87aa9-149">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




