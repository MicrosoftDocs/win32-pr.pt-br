---
description: Obter mais informações sobre o parâmetro PageWatermarkTextAngle. Este tópico não é atual. Para obter as informações mais atuais, consulte a Especificação de Esquema de Impressão.
ms.assetid: 157bb79c-68d2-4121-8a85-cd2f48095541
title: PageWatermarkTextAngle
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1dce37512314e1eaac0cbbe3b5b4b817cb2ee455
ms.sourcegitcommit: 91530c19d26ba4c57a6af1f37b57f211f580464e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/19/2021
ms.locfileid: "112395971"
---
# <a name="pagewatermarktextangle"></a><span data-ttu-id="85076-105">PageWatermarkTextAngle</span><span class="sxs-lookup"><span data-stu-id="85076-105">PageWatermarkTextAngle</span></span>

<span data-ttu-id="85076-106">Este tópico não é atual.</span><span class="sxs-lookup"><span data-stu-id="85076-106">This topic is not current.</span></span> <span data-ttu-id="85076-107">Para obter as informações mais atuais, consulte a [Especificação de Esquema de Impressão](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="85076-107">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="85076-108">Especifica o ângulo do texto da marca-d'água em relação à direção PageImageableSizeWidth.</span><span class="sxs-lookup"><span data-stu-id="85076-108">Specifies the angle of the watermark text relative to the PageImageableSizeWidth direction.</span></span> <span data-ttu-id="85076-109">O ângulo é medido na direção no sentido anti-horário.</span><span class="sxs-lookup"><span data-stu-id="85076-109">The angle is measured in the counter-clockwise direction.</span></span>

-   [<span data-ttu-id="85076-110">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="85076-110">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="85076-111">Conteúdo da estrutura</span><span class="sxs-lookup"><span data-stu-id="85076-111">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="85076-112">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="85076-112">Element Information</span></span>



| <span data-ttu-id="85076-113">Name</span><span class="sxs-lookup"><span data-stu-id="85076-113">Name</span></span> | <span data-ttu-id="85076-114">Valor</span><span class="sxs-lookup"><span data-stu-id="85076-114">Value</span></span> |
|----------------------------|--------------------------------------------|
| <span data-ttu-id="85076-115">Tipo de elemento</span><span class="sxs-lookup"><span data-stu-id="85076-115">Element Type</span></span> <br/>   | <span data-ttu-id="85076-116">ParameterDef</span><span class="sxs-lookup"><span data-stu-id="85076-116">ParameterDef</span></span><br/>                    |
| <span data-ttu-id="85076-117">Prefixo de definição de scoping</span><span class="sxs-lookup"><span data-stu-id="85076-117">Scoping Prefix</span></span> <br/> | <span data-ttu-id="85076-118">?</span><span class="sxs-lookup"><span data-stu-id="85076-118">Page</span></span><br/>                            |
| <span data-ttu-id="85076-119">Observações</span><span class="sxs-lookup"><span data-stu-id="85076-119">Notes</span></span> <br/>          | <span data-ttu-id="85076-120">Vinculado ao elemento PageWatermark</span><span class="sxs-lookup"><span data-stu-id="85076-120">Linked to PageWatermark element</span></span><br/> |



 

## <a name="structure-content"></a><span data-ttu-id="85076-121">Conteúdo da estrutura</span><span class="sxs-lookup"><span data-stu-id="85076-121">Structure Content</span></span>

<span data-ttu-id="85076-122">A estrutura XML desse elemento é a seguinte:</span><span class="sxs-lookup"><span data-stu-id="85076-122">The XML structure of this element is as follows:</span></span>

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

## <a name="structure-properties"></a><span data-ttu-id="85076-123">Propriedades da estrutura</span><span class="sxs-lookup"><span data-stu-id="85076-123">Structure Properties</span></span>

<span data-ttu-id="85076-124">A tabela a seguir descreve as características das variáveis definidas na estrutura XML.</span><span class="sxs-lookup"><span data-stu-id="85076-124">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="85076-125">Propriedade</span><span class="sxs-lookup"><span data-stu-id="85076-125">Property</span></span>                | <span data-ttu-id="85076-126">xsi:type</span><span class="sxs-lookup"><span data-stu-id="85076-126">xsi:type</span></span>           | <span data-ttu-id="85076-127">Valor</span><span class="sxs-lookup"><span data-stu-id="85076-127">Value</span></span>                      |
|-------------------------|--------------------|----------------------------|
| <span data-ttu-id="85076-128">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="85076-128">DataType</span></span><br/>     | <span data-ttu-id="85076-129">string</span><span class="sxs-lookup"><span data-stu-id="85076-129">string</span></span><br/>  | <span data-ttu-id="85076-130">xs:integer</span><span class="sxs-lookup"><span data-stu-id="85076-130">xs:integer</span></span><br/>      |
| <span data-ttu-id="85076-131">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="85076-131">DefaultValue</span></span><br/> | <span data-ttu-id="85076-132">inteiro</span><span class="sxs-lookup"><span data-stu-id="85076-132">integer</span></span><br/> | <span data-ttu-id="85076-133">0</span><span class="sxs-lookup"><span data-stu-id="85076-133">0</span></span><br/>               |
| <span data-ttu-id="85076-134">MaxValue</span><span class="sxs-lookup"><span data-stu-id="85076-134">MaxValue</span></span><br/>     | <span data-ttu-id="85076-135">Número inteiro</span><span class="sxs-lookup"><span data-stu-id="85076-135">integer</span></span><br/> | <span data-ttu-id="85076-136">359</span><span class="sxs-lookup"><span data-stu-id="85076-136">359</span></span><br/>             |
| <span data-ttu-id="85076-137">Minvalue</span><span class="sxs-lookup"><span data-stu-id="85076-137">MinValue</span></span><br/>     | <span data-ttu-id="85076-138">inteiro</span><span class="sxs-lookup"><span data-stu-id="85076-138">integer</span></span><br/> | <span data-ttu-id="85076-139">0</span><span class="sxs-lookup"><span data-stu-id="85076-139">0</span></span><br/>               |
| <span data-ttu-id="85076-140">Vários</span><span class="sxs-lookup"><span data-stu-id="85076-140">Multiple</span></span><br/>     | <span data-ttu-id="85076-141">integer</span><span class="sxs-lookup"><span data-stu-id="85076-141">integer</span></span><br/> | <span data-ttu-id="85076-142">1</span><span class="sxs-lookup"><span data-stu-id="85076-142">1</span></span><br/>               |
| <span data-ttu-id="85076-143">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="85076-143">Mandatory</span></span><br/>    | <span data-ttu-id="85076-144">string</span><span class="sxs-lookup"><span data-stu-id="85076-144">string</span></span><br/>  | <span data-ttu-id="85076-145">psk:Conditional</span><span class="sxs-lookup"><span data-stu-id="85076-145">psk:Conditional</span></span><br/> |
| <span data-ttu-id="85076-146">Unittype</span><span class="sxs-lookup"><span data-stu-id="85076-146">UnitType</span></span><br/>     | <span data-ttu-id="85076-147">string</span><span class="sxs-lookup"><span data-stu-id="85076-147">string</span></span><br/>  | <span data-ttu-id="85076-148">graus</span><span class="sxs-lookup"><span data-stu-id="85076-148">degrees</span></span><br/>         |



 

## <a name="related-topics"></a><span data-ttu-id="85076-149">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="85076-149">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="85076-150">Especificação de esquema de impressão</span><span class="sxs-lookup"><span data-stu-id="85076-150">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




