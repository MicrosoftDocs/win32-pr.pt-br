---
description: Este tópico não é atual. Para obter as informações mais atuais, consulte a especificação do esquema de impressão.
ms.assetid: ef429727-d881-408b-95ce-2acce667654a
title: PageWatermarkOriginHeight
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c1d3e12591f6c648e6e636e1bb72f4df694d0d13
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/05/2021
ms.locfileid: "103930255"
---
# <a name="pagewatermarkoriginheight"></a><span data-ttu-id="27e9e-104">PageWatermarkOriginHeight</span><span class="sxs-lookup"><span data-stu-id="27e9e-104">PageWatermarkOriginHeight</span></span>

<span data-ttu-id="27e9e-105">Este tópico não é atual.</span><span class="sxs-lookup"><span data-stu-id="27e9e-105">This topic is not current.</span></span> <span data-ttu-id="27e9e-106">Para obter as informações mais atuais, consulte a [especificação do esquema de impressão](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="27e9e-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="27e9e-107">Especifica a origem de uma marca d' água em relação à origem do PageImageableSize.</span><span class="sxs-lookup"><span data-stu-id="27e9e-107">Specifies the origin of a watermark relative to the origin of the PageImageableSize.</span></span>

-   [<span data-ttu-id="27e9e-108">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="27e9e-108">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="27e9e-109">Conteúdo da estrutura</span><span class="sxs-lookup"><span data-stu-id="27e9e-109">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="27e9e-110">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="27e9e-110">Element Information</span></span>



| <span data-ttu-id="27e9e-111">Nome</span><span class="sxs-lookup"><span data-stu-id="27e9e-111">Name</span></span>                       |                                            |
|----------------------------|--------------------------------------------|
| <span data-ttu-id="27e9e-112">Tipo de elemento</span><span class="sxs-lookup"><span data-stu-id="27e9e-112">Element Type</span></span> <br/>   | <span data-ttu-id="27e9e-113">ParameterDef</span><span class="sxs-lookup"><span data-stu-id="27e9e-113">ParameterDef</span></span><br/>                    |
| <span data-ttu-id="27e9e-114">Prefixo de escopo</span><span class="sxs-lookup"><span data-stu-id="27e9e-114">Scoping Prefix</span></span> <br/> | <span data-ttu-id="27e9e-115">?</span><span class="sxs-lookup"><span data-stu-id="27e9e-115">Page</span></span><br/>                            |
| <span data-ttu-id="27e9e-116">Observações</span><span class="sxs-lookup"><span data-stu-id="27e9e-116">Notes</span></span> <br/>          | <span data-ttu-id="27e9e-117">Vinculado ao elemento PageWatermark</span><span class="sxs-lookup"><span data-stu-id="27e9e-117">Linked to PageWatermark element</span></span><br/> |



 

## <a name="structure-content"></a><span data-ttu-id="27e9e-118">Conteúdo da estrutura</span><span class="sxs-lookup"><span data-stu-id="27e9e-118">Structure Content</span></span>

<span data-ttu-id="27e9e-119">A estrutura XML desse elemento é a seguinte:</span><span class="sxs-lookup"><span data-stu-id="27e9e-119">The XML structure of this element is as follows:</span></span>

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

## <a name="structure-properties"></a><span data-ttu-id="27e9e-120">Propriedades da estrutura</span><span class="sxs-lookup"><span data-stu-id="27e9e-120">Structure Properties</span></span>

<span data-ttu-id="27e9e-121">A tabela a seguir descreve as características das variáveis definidas na estrutura XML.</span><span class="sxs-lookup"><span data-stu-id="27e9e-121">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="27e9e-122">Propriedade</span><span class="sxs-lookup"><span data-stu-id="27e9e-122">Property</span></span>                | <span data-ttu-id="27e9e-123">xsi:type</span><span class="sxs-lookup"><span data-stu-id="27e9e-123">xsi:type</span></span>           | <span data-ttu-id="27e9e-124">Valor</span><span class="sxs-lookup"><span data-stu-id="27e9e-124">Value</span></span>                                                                   |
|-------------------------|--------------------|-------------------------------------------------------------------------|
| <span data-ttu-id="27e9e-125">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="27e9e-125">DataType</span></span><br/>     | <span data-ttu-id="27e9e-126">string</span><span class="sxs-lookup"><span data-stu-id="27e9e-126">string</span></span><br/>  | <span data-ttu-id="27e9e-127">xs:integer</span><span class="sxs-lookup"><span data-stu-id="27e9e-127">xs:integer</span></span><br/>                                                   |
| <span data-ttu-id="27e9e-128">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="27e9e-128">DefaultValue</span></span><br/> | <span data-ttu-id="27e9e-129">Número inteiro</span><span class="sxs-lookup"><span data-stu-id="27e9e-129">integer</span></span><br/> | <span data-ttu-id="27e9e-130">não definido</span><span class="sxs-lookup"><span data-stu-id="27e9e-130">undefined</span></span><br/>                                                    |
| <span data-ttu-id="27e9e-131">MaxValue</span><span class="sxs-lookup"><span data-stu-id="27e9e-131">MaxValue</span></span><br/>     | <span data-ttu-id="27e9e-132">Número inteiro</span><span class="sxs-lookup"><span data-stu-id="27e9e-132">integer</span></span><br/> | <span data-ttu-id="27e9e-133">Menor ou igual ao valor de PageImageableSize-ExtentHeight</span><span class="sxs-lookup"><span data-stu-id="27e9e-133">Less than or equal to PageImageableSize - ExtentHeight value</span></span><br/> |
| <span data-ttu-id="27e9e-134">MinValue</span><span class="sxs-lookup"><span data-stu-id="27e9e-134">MinValue</span></span><br/>     | <span data-ttu-id="27e9e-135">integer</span><span class="sxs-lookup"><span data-stu-id="27e9e-135">integer</span></span><br/> | <span data-ttu-id="27e9e-136">0</span><span class="sxs-lookup"><span data-stu-id="27e9e-136">0</span></span><br/>                                                            |
| <span data-ttu-id="27e9e-137">Vários</span><span class="sxs-lookup"><span data-stu-id="27e9e-137">Multiple</span></span><br/>     | <span data-ttu-id="27e9e-138">integer</span><span class="sxs-lookup"><span data-stu-id="27e9e-138">integer</span></span><br/> | <span data-ttu-id="27e9e-139">1</span><span class="sxs-lookup"><span data-stu-id="27e9e-139">1</span></span><br/>                                                            |
| <span data-ttu-id="27e9e-140">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="27e9e-140">Mandatory</span></span><br/>    | <span data-ttu-id="27e9e-141">string</span><span class="sxs-lookup"><span data-stu-id="27e9e-141">string</span></span><br/>  | <span data-ttu-id="27e9e-142">PSK: condicional</span><span class="sxs-lookup"><span data-stu-id="27e9e-142">psk:Conditional</span></span><br/>                                              |
| <span data-ttu-id="27e9e-143">UnitType</span><span class="sxs-lookup"><span data-stu-id="27e9e-143">UnitType</span></span><br/>     | <span data-ttu-id="27e9e-144">string</span><span class="sxs-lookup"><span data-stu-id="27e9e-144">string</span></span><br/>  | <span data-ttu-id="27e9e-145">mícrons</span><span class="sxs-lookup"><span data-stu-id="27e9e-145">microns</span></span><br/>                                                      |



 

## <a name="related-topics"></a><span data-ttu-id="27e9e-146">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="27e9e-146">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="27e9e-147">Especificação de esquema de impressão</span><span class="sxs-lookup"><span data-stu-id="27e9e-147">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




