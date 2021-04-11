---
description: Este tópico não é atual. Para obter as informações mais atuais, consulte a especificação do esquema de impressão.
ms.assetid: 157bb79c-68d2-4121-8a85-cd2f48095541
title: PageWatermarkTextAngle
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 916e409040f0c7163f1168d48581270f077aaa3a
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/05/2021
ms.locfileid: "104172564"
---
# <a name="pagewatermarktextangle"></a><span data-ttu-id="735e8-104">PageWatermarkTextAngle</span><span class="sxs-lookup"><span data-stu-id="735e8-104">PageWatermarkTextAngle</span></span>

<span data-ttu-id="735e8-105">Este tópico não é atual.</span><span class="sxs-lookup"><span data-stu-id="735e8-105">This topic is not current.</span></span> <span data-ttu-id="735e8-106">Para obter as informações mais atuais, consulte a [especificação do esquema de impressão](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="735e8-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="735e8-107">Especifica o ângulo do texto da marca d' água em relação à direção do PageImageableSizeWidth.</span><span class="sxs-lookup"><span data-stu-id="735e8-107">Specifies the angle of the watermark text relative to the PageImageableSizeWidth direction.</span></span> <span data-ttu-id="735e8-108">O ângulo é medido na direção do sentido anti-horário.</span><span class="sxs-lookup"><span data-stu-id="735e8-108">The angle is measured in the counter-clockwise direction.</span></span>

-   [<span data-ttu-id="735e8-109">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="735e8-109">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="735e8-110">Conteúdo da estrutura</span><span class="sxs-lookup"><span data-stu-id="735e8-110">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="735e8-111">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="735e8-111">Element Information</span></span>



| <span data-ttu-id="735e8-112">Nome</span><span class="sxs-lookup"><span data-stu-id="735e8-112">Name</span></span>                       |                                            |
|----------------------------|--------------------------------------------|
| <span data-ttu-id="735e8-113">Tipo de elemento</span><span class="sxs-lookup"><span data-stu-id="735e8-113">Element Type</span></span> <br/>   | <span data-ttu-id="735e8-114">ParameterDef</span><span class="sxs-lookup"><span data-stu-id="735e8-114">ParameterDef</span></span><br/>                    |
| <span data-ttu-id="735e8-115">Prefixo de escopo</span><span class="sxs-lookup"><span data-stu-id="735e8-115">Scoping Prefix</span></span> <br/> | <span data-ttu-id="735e8-116">?</span><span class="sxs-lookup"><span data-stu-id="735e8-116">Page</span></span><br/>                            |
| <span data-ttu-id="735e8-117">Observações</span><span class="sxs-lookup"><span data-stu-id="735e8-117">Notes</span></span> <br/>          | <span data-ttu-id="735e8-118">Vinculado ao elemento PageWatermark</span><span class="sxs-lookup"><span data-stu-id="735e8-118">Linked to PageWatermark element</span></span><br/> |



 

## <a name="structure-content"></a><span data-ttu-id="735e8-119">Conteúdo da estrutura</span><span class="sxs-lookup"><span data-stu-id="735e8-119">Structure Content</span></span>

<span data-ttu-id="735e8-120">A estrutura XML desse elemento é a seguinte:</span><span class="sxs-lookup"><span data-stu-id="735e8-120">The XML structure of this element is as follows:</span></span>

``` syntax
<psf:ParameterDef name="psk:PageWatermarkTextAngle">
  <psf:Property name="psf:DataType">
    <psf:Value xsi:type="xs:string">xs:integer</psf:Value>
  </psf:Property>
  <psf:Property name="psf:DefaultValue">
    <psf:Value xsi:type="xs:integer">0</psf:Value>
  </psf:Property>
  <psf:Property name="psf:MaxValue">
    <psf:Value xsi:type="xs:integer">359</psf:Value>
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
    <psf:Value xsi:type="xs:string">degrees</psf:Value>
  </psf:Property>
</psf:ParameterDef>
      
```

## <a name="structure-properties"></a><span data-ttu-id="735e8-121">Propriedades da estrutura</span><span class="sxs-lookup"><span data-stu-id="735e8-121">Structure Properties</span></span>

<span data-ttu-id="735e8-122">A tabela a seguir descreve as características das variáveis definidas na estrutura XML.</span><span class="sxs-lookup"><span data-stu-id="735e8-122">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="735e8-123">Propriedade</span><span class="sxs-lookup"><span data-stu-id="735e8-123">Property</span></span>                | <span data-ttu-id="735e8-124">xsi:type</span><span class="sxs-lookup"><span data-stu-id="735e8-124">xsi:type</span></span>           | <span data-ttu-id="735e8-125">Valor</span><span class="sxs-lookup"><span data-stu-id="735e8-125">Value</span></span>                      |
|-------------------------|--------------------|----------------------------|
| <span data-ttu-id="735e8-126">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="735e8-126">DataType</span></span><br/>     | <span data-ttu-id="735e8-127">string</span><span class="sxs-lookup"><span data-stu-id="735e8-127">string</span></span><br/>  | <span data-ttu-id="735e8-128">xs:integer</span><span class="sxs-lookup"><span data-stu-id="735e8-128">xs:integer</span></span><br/>      |
| <span data-ttu-id="735e8-129">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="735e8-129">DefaultValue</span></span><br/> | <span data-ttu-id="735e8-130">integer</span><span class="sxs-lookup"><span data-stu-id="735e8-130">integer</span></span><br/> | <span data-ttu-id="735e8-131">0</span><span class="sxs-lookup"><span data-stu-id="735e8-131">0</span></span><br/>               |
| <span data-ttu-id="735e8-132">MaxValue</span><span class="sxs-lookup"><span data-stu-id="735e8-132">MaxValue</span></span><br/>     | <span data-ttu-id="735e8-133">Número inteiro</span><span class="sxs-lookup"><span data-stu-id="735e8-133">integer</span></span><br/> | <span data-ttu-id="735e8-134">359</span><span class="sxs-lookup"><span data-stu-id="735e8-134">359</span></span><br/>             |
| <span data-ttu-id="735e8-135">MinValue</span><span class="sxs-lookup"><span data-stu-id="735e8-135">MinValue</span></span><br/>     | <span data-ttu-id="735e8-136">integer</span><span class="sxs-lookup"><span data-stu-id="735e8-136">integer</span></span><br/> | <span data-ttu-id="735e8-137">0</span><span class="sxs-lookup"><span data-stu-id="735e8-137">0</span></span><br/>               |
| <span data-ttu-id="735e8-138">Vários</span><span class="sxs-lookup"><span data-stu-id="735e8-138">Multiple</span></span><br/>     | <span data-ttu-id="735e8-139">integer</span><span class="sxs-lookup"><span data-stu-id="735e8-139">integer</span></span><br/> | <span data-ttu-id="735e8-140">1</span><span class="sxs-lookup"><span data-stu-id="735e8-140">1</span></span><br/>               |
| <span data-ttu-id="735e8-141">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="735e8-141">Mandatory</span></span><br/>    | <span data-ttu-id="735e8-142">string</span><span class="sxs-lookup"><span data-stu-id="735e8-142">string</span></span><br/>  | <span data-ttu-id="735e8-143">PSK: condicional</span><span class="sxs-lookup"><span data-stu-id="735e8-143">psk:Conditional</span></span><br/> |
| <span data-ttu-id="735e8-144">UnitType</span><span class="sxs-lookup"><span data-stu-id="735e8-144">UnitType</span></span><br/>     | <span data-ttu-id="735e8-145">string</span><span class="sxs-lookup"><span data-stu-id="735e8-145">string</span></span><br/>  | <span data-ttu-id="735e8-146">graus</span><span class="sxs-lookup"><span data-stu-id="735e8-146">degrees</span></span><br/>         |



 

## <a name="related-topics"></a><span data-ttu-id="735e8-147">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="735e8-147">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="735e8-148">Especificação de esquema de impressão</span><span class="sxs-lookup"><span data-stu-id="735e8-148">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




