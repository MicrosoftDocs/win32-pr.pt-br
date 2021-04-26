---
description: Este tópico não é atual. Para obter as informações mais atuais, consulte a especificação do esquema de impressão.
ms.assetid: 157bb79c-68d2-4121-8a85-cd2f48095541
title: PageWatermarkTextAngle
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 86c13d759232670c6957a91de12f9c35cf48aeb4
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/26/2021
ms.locfileid: "107995543"
---
# <a name="pagewatermarktextangle"></a><span data-ttu-id="f7f73-104">PageWatermarkTextAngle</span><span class="sxs-lookup"><span data-stu-id="f7f73-104">PageWatermarkTextAngle</span></span>

<span data-ttu-id="f7f73-105">Este tópico não é atual.</span><span class="sxs-lookup"><span data-stu-id="f7f73-105">This topic is not current.</span></span> <span data-ttu-id="f7f73-106">Para obter as informações mais atuais, consulte a [especificação do esquema de impressão](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="f7f73-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="f7f73-107">Especifica o ângulo do texto da marca d' água em relação à direção do PageImageableSizeWidth.</span><span class="sxs-lookup"><span data-stu-id="f7f73-107">Specifies the angle of the watermark text relative to the PageImageableSizeWidth direction.</span></span> <span data-ttu-id="f7f73-108">O ângulo é medido na direção do sentido anti-horário.</span><span class="sxs-lookup"><span data-stu-id="f7f73-108">The angle is measured in the counter-clockwise direction.</span></span>

-   [<span data-ttu-id="f7f73-109">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="f7f73-109">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="f7f73-110">Conteúdo da estrutura</span><span class="sxs-lookup"><span data-stu-id="f7f73-110">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="f7f73-111">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="f7f73-111">Element Information</span></span>



| <span data-ttu-id="f7f73-112">Nome</span><span class="sxs-lookup"><span data-stu-id="f7f73-112">Name</span></span> | <span data-ttu-id="f7f73-113">Valor</span><span class="sxs-lookup"><span data-stu-id="f7f73-113">Value</span></span> |
|----------------------------|--------------------------------------------|
| <span data-ttu-id="f7f73-114">Tipo de elemento</span><span class="sxs-lookup"><span data-stu-id="f7f73-114">Element Type</span></span> <br/>   | <span data-ttu-id="f7f73-115">ParameterDef</span><span class="sxs-lookup"><span data-stu-id="f7f73-115">ParameterDef</span></span><br/>                    |
| <span data-ttu-id="f7f73-116">Prefixo de escopo</span><span class="sxs-lookup"><span data-stu-id="f7f73-116">Scoping Prefix</span></span> <br/> | <span data-ttu-id="f7f73-117">?</span><span class="sxs-lookup"><span data-stu-id="f7f73-117">Page</span></span><br/>                            |
| <span data-ttu-id="f7f73-118">Observações</span><span class="sxs-lookup"><span data-stu-id="f7f73-118">Notes</span></span> <br/>          | <span data-ttu-id="f7f73-119">Vinculado ao elemento PageWatermark</span><span class="sxs-lookup"><span data-stu-id="f7f73-119">Linked to PageWatermark element</span></span><br/> |



 

## <a name="structure-content"></a><span data-ttu-id="f7f73-120">Conteúdo da estrutura</span><span class="sxs-lookup"><span data-stu-id="f7f73-120">Structure Content</span></span>

<span data-ttu-id="f7f73-121">A estrutura XML desse elemento é a seguinte:</span><span class="sxs-lookup"><span data-stu-id="f7f73-121">The XML structure of this element is as follows:</span></span>

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

## <a name="structure-properties"></a><span data-ttu-id="f7f73-122">Propriedades da estrutura</span><span class="sxs-lookup"><span data-stu-id="f7f73-122">Structure Properties</span></span>

<span data-ttu-id="f7f73-123">A tabela a seguir descreve as características das variáveis definidas na estrutura XML.</span><span class="sxs-lookup"><span data-stu-id="f7f73-123">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="f7f73-124">Propriedade</span><span class="sxs-lookup"><span data-stu-id="f7f73-124">Property</span></span>                | <span data-ttu-id="f7f73-125">xsi:type</span><span class="sxs-lookup"><span data-stu-id="f7f73-125">xsi:type</span></span>           | <span data-ttu-id="f7f73-126">Valor</span><span class="sxs-lookup"><span data-stu-id="f7f73-126">Value</span></span>                      |
|-------------------------|--------------------|----------------------------|
| <span data-ttu-id="f7f73-127">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="f7f73-127">DataType</span></span><br/>     | <span data-ttu-id="f7f73-128">string</span><span class="sxs-lookup"><span data-stu-id="f7f73-128">string</span></span><br/>  | <span data-ttu-id="f7f73-129">xs:integer</span><span class="sxs-lookup"><span data-stu-id="f7f73-129">xs:integer</span></span><br/>      |
| <span data-ttu-id="f7f73-130">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="f7f73-130">DefaultValue</span></span><br/> | <span data-ttu-id="f7f73-131">integer</span><span class="sxs-lookup"><span data-stu-id="f7f73-131">integer</span></span><br/> | <span data-ttu-id="f7f73-132">0</span><span class="sxs-lookup"><span data-stu-id="f7f73-132">0</span></span><br/>               |
| <span data-ttu-id="f7f73-133">MaxValue</span><span class="sxs-lookup"><span data-stu-id="f7f73-133">MaxValue</span></span><br/>     | <span data-ttu-id="f7f73-134">Número inteiro</span><span class="sxs-lookup"><span data-stu-id="f7f73-134">integer</span></span><br/> | <span data-ttu-id="f7f73-135">359</span><span class="sxs-lookup"><span data-stu-id="f7f73-135">359</span></span><br/>             |
| <span data-ttu-id="f7f73-136">MinValue</span><span class="sxs-lookup"><span data-stu-id="f7f73-136">MinValue</span></span><br/>     | <span data-ttu-id="f7f73-137">integer</span><span class="sxs-lookup"><span data-stu-id="f7f73-137">integer</span></span><br/> | <span data-ttu-id="f7f73-138">0</span><span class="sxs-lookup"><span data-stu-id="f7f73-138">0</span></span><br/>               |
| <span data-ttu-id="f7f73-139">Vários</span><span class="sxs-lookup"><span data-stu-id="f7f73-139">Multiple</span></span><br/>     | <span data-ttu-id="f7f73-140">integer</span><span class="sxs-lookup"><span data-stu-id="f7f73-140">integer</span></span><br/> | <span data-ttu-id="f7f73-141">1</span><span class="sxs-lookup"><span data-stu-id="f7f73-141">1</span></span><br/>               |
| <span data-ttu-id="f7f73-142">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="f7f73-142">Mandatory</span></span><br/>    | <span data-ttu-id="f7f73-143">string</span><span class="sxs-lookup"><span data-stu-id="f7f73-143">string</span></span><br/>  | <span data-ttu-id="f7f73-144">PSK: condicional</span><span class="sxs-lookup"><span data-stu-id="f7f73-144">psk:Conditional</span></span><br/> |
| <span data-ttu-id="f7f73-145">UnitType</span><span class="sxs-lookup"><span data-stu-id="f7f73-145">UnitType</span></span><br/>     | <span data-ttu-id="f7f73-146">string</span><span class="sxs-lookup"><span data-stu-id="f7f73-146">string</span></span><br/>  | <span data-ttu-id="f7f73-147">graus</span><span class="sxs-lookup"><span data-stu-id="f7f73-147">degrees</span></span><br/>         |



 

## <a name="related-topics"></a><span data-ttu-id="f7f73-148">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="f7f73-148">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f7f73-149">Especificação de esquema de impressão</span><span class="sxs-lookup"><span data-stu-id="f7f73-149">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




