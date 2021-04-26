---
description: Este tópico não é atual. Para obter as informações mais atuais, consulte a especificação do esquema de impressão.
ms.assetid: ef429727-d881-408b-95ce-2acce667654a
title: PageWatermarkOriginHeight
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 90736f8cac9c919f9d640ffc01311024ef79bc3a
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/26/2021
ms.locfileid: "107994483"
---
# <a name="pagewatermarkoriginheight"></a><span data-ttu-id="525a6-104">PageWatermarkOriginHeight</span><span class="sxs-lookup"><span data-stu-id="525a6-104">PageWatermarkOriginHeight</span></span>

<span data-ttu-id="525a6-105">Este tópico não é atual.</span><span class="sxs-lookup"><span data-stu-id="525a6-105">This topic is not current.</span></span> <span data-ttu-id="525a6-106">Para obter as informações mais atuais, consulte a [especificação do esquema de impressão](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="525a6-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="525a6-107">Especifica a origem de uma marca d' água em relação à origem do PageImageableSize.</span><span class="sxs-lookup"><span data-stu-id="525a6-107">Specifies the origin of a watermark relative to the origin of the PageImageableSize.</span></span>

-   [<span data-ttu-id="525a6-108">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="525a6-108">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="525a6-109">Conteúdo da estrutura</span><span class="sxs-lookup"><span data-stu-id="525a6-109">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="525a6-110">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="525a6-110">Element Information</span></span>



| <span data-ttu-id="525a6-111">Nome</span><span class="sxs-lookup"><span data-stu-id="525a6-111">Name</span></span> | <span data-ttu-id="525a6-112">Valor</span><span class="sxs-lookup"><span data-stu-id="525a6-112">Value</span></span> |
|----------------------------|--------------------------------------------|
| <span data-ttu-id="525a6-113">Tipo de elemento</span><span class="sxs-lookup"><span data-stu-id="525a6-113">Element Type</span></span> <br/>   | <span data-ttu-id="525a6-114">ParameterDef</span><span class="sxs-lookup"><span data-stu-id="525a6-114">ParameterDef</span></span><br/>                    |
| <span data-ttu-id="525a6-115">Prefixo de escopo</span><span class="sxs-lookup"><span data-stu-id="525a6-115">Scoping Prefix</span></span> <br/> | <span data-ttu-id="525a6-116">?</span><span class="sxs-lookup"><span data-stu-id="525a6-116">Page</span></span><br/>                            |
| <span data-ttu-id="525a6-117">Observações</span><span class="sxs-lookup"><span data-stu-id="525a6-117">Notes</span></span> <br/>          | <span data-ttu-id="525a6-118">Vinculado ao elemento PageWatermark</span><span class="sxs-lookup"><span data-stu-id="525a6-118">Linked to PageWatermark element</span></span><br/> |



 

## <a name="structure-content"></a><span data-ttu-id="525a6-119">Conteúdo da estrutura</span><span class="sxs-lookup"><span data-stu-id="525a6-119">Structure Content</span></span>

<span data-ttu-id="525a6-120">A estrutura XML desse elemento é a seguinte:</span><span class="sxs-lookup"><span data-stu-id="525a6-120">The XML structure of this element is as follows:</span></span>

``` syntax
<psf:ParameterDef name="psk:PageWatermarkOriginHeight">
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

## <a name="structure-properties"></a><span data-ttu-id="525a6-121">Propriedades da estrutura</span><span class="sxs-lookup"><span data-stu-id="525a6-121">Structure Properties</span></span>

<span data-ttu-id="525a6-122">A tabela a seguir descreve as características das variáveis definidas na estrutura XML.</span><span class="sxs-lookup"><span data-stu-id="525a6-122">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="525a6-123">Propriedade</span><span class="sxs-lookup"><span data-stu-id="525a6-123">Property</span></span>                | <span data-ttu-id="525a6-124">xsi:type</span><span class="sxs-lookup"><span data-stu-id="525a6-124">xsi:type</span></span>           | <span data-ttu-id="525a6-125">Valor</span><span class="sxs-lookup"><span data-stu-id="525a6-125">Value</span></span>                                                                   |
|-------------------------|--------------------|-------------------------------------------------------------------------|
| <span data-ttu-id="525a6-126">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="525a6-126">DataType</span></span><br/>     | <span data-ttu-id="525a6-127">string</span><span class="sxs-lookup"><span data-stu-id="525a6-127">string</span></span><br/>  | <span data-ttu-id="525a6-128">xs:integer</span><span class="sxs-lookup"><span data-stu-id="525a6-128">xs:integer</span></span><br/>                                                   |
| <span data-ttu-id="525a6-129">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="525a6-129">DefaultValue</span></span><br/> | <span data-ttu-id="525a6-130">Número inteiro</span><span class="sxs-lookup"><span data-stu-id="525a6-130">integer</span></span><br/> | <span data-ttu-id="525a6-131">não definido</span><span class="sxs-lookup"><span data-stu-id="525a6-131">undefined</span></span><br/>                                                    |
| <span data-ttu-id="525a6-132">MaxValue</span><span class="sxs-lookup"><span data-stu-id="525a6-132">MaxValue</span></span><br/>     | <span data-ttu-id="525a6-133">Número inteiro</span><span class="sxs-lookup"><span data-stu-id="525a6-133">integer</span></span><br/> | <span data-ttu-id="525a6-134">Menor ou igual ao valor de PageImageableSize-ExtentHeight</span><span class="sxs-lookup"><span data-stu-id="525a6-134">Less than or equal to PageImageableSize - ExtentHeight value</span></span><br/> |
| <span data-ttu-id="525a6-135">MinValue</span><span class="sxs-lookup"><span data-stu-id="525a6-135">MinValue</span></span><br/>     | <span data-ttu-id="525a6-136">integer</span><span class="sxs-lookup"><span data-stu-id="525a6-136">integer</span></span><br/> | <span data-ttu-id="525a6-137">0</span><span class="sxs-lookup"><span data-stu-id="525a6-137">0</span></span><br/>                                                            |
| <span data-ttu-id="525a6-138">Vários</span><span class="sxs-lookup"><span data-stu-id="525a6-138">Multiple</span></span><br/>     | <span data-ttu-id="525a6-139">integer</span><span class="sxs-lookup"><span data-stu-id="525a6-139">integer</span></span><br/> | <span data-ttu-id="525a6-140">1</span><span class="sxs-lookup"><span data-stu-id="525a6-140">1</span></span><br/>                                                            |
| <span data-ttu-id="525a6-141">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="525a6-141">Mandatory</span></span><br/>    | <span data-ttu-id="525a6-142">string</span><span class="sxs-lookup"><span data-stu-id="525a6-142">string</span></span><br/>  | <span data-ttu-id="525a6-143">PSK: condicional</span><span class="sxs-lookup"><span data-stu-id="525a6-143">psk:Conditional</span></span><br/>                                              |
| <span data-ttu-id="525a6-144">UnitType</span><span class="sxs-lookup"><span data-stu-id="525a6-144">UnitType</span></span><br/>     | <span data-ttu-id="525a6-145">string</span><span class="sxs-lookup"><span data-stu-id="525a6-145">string</span></span><br/>  | <span data-ttu-id="525a6-146">mícrons</span><span class="sxs-lookup"><span data-stu-id="525a6-146">microns</span></span><br/>                                                      |



 

## <a name="related-topics"></a><span data-ttu-id="525a6-147">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="525a6-147">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="525a6-148">Especificação de esquema de impressão</span><span class="sxs-lookup"><span data-stu-id="525a6-148">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




