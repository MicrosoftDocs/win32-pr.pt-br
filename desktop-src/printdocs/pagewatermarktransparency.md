---
description: Este tópico não é atual. Para obter as informações mais atuais, consulte a especificação do esquema de impressão.
ms.assetid: f94c1450-9648-4aee-8f88-2a9213eba4a9
title: PageWatermarkTransparency
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7f0e96382656b1092a0dbc71352e788208f70b34
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/05/2021
ms.locfileid: "105788744"
---
# <a name="pagewatermarktransparency"></a><span data-ttu-id="97db8-104">PageWatermarkTransparency</span><span class="sxs-lookup"><span data-stu-id="97db8-104">PageWatermarkTransparency</span></span>

<span data-ttu-id="97db8-105">Este tópico não é atual.</span><span class="sxs-lookup"><span data-stu-id="97db8-105">This topic is not current.</span></span> <span data-ttu-id="97db8-106">Para obter as informações mais atuais, consulte a [especificação do esquema de impressão](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="97db8-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="97db8-107">Especifica a transparência da marca d' água.</span><span class="sxs-lookup"><span data-stu-id="97db8-107">Specifies the transparency for the watermark.</span></span> <span data-ttu-id="97db8-108">Totalmente opaco teria um valor de 0.</span><span class="sxs-lookup"><span data-stu-id="97db8-108">Fully opaque would have a value of 0.</span></span>

-   [<span data-ttu-id="97db8-109">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="97db8-109">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="97db8-110">Conteúdo da estrutura</span><span class="sxs-lookup"><span data-stu-id="97db8-110">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="97db8-111">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="97db8-111">Element Information</span></span>



| <span data-ttu-id="97db8-112">Nome</span><span class="sxs-lookup"><span data-stu-id="97db8-112">Name</span></span>                       |                                            |
|----------------------------|--------------------------------------------|
| <span data-ttu-id="97db8-113">Tipo de elemento</span><span class="sxs-lookup"><span data-stu-id="97db8-113">Element Type</span></span> <br/>   | <span data-ttu-id="97db8-114">ParameterDef</span><span class="sxs-lookup"><span data-stu-id="97db8-114">ParameterDef</span></span><br/>                    |
| <span data-ttu-id="97db8-115">Prefixo de escopo</span><span class="sxs-lookup"><span data-stu-id="97db8-115">Scoping Prefix</span></span> <br/> | <span data-ttu-id="97db8-116">?</span><span class="sxs-lookup"><span data-stu-id="97db8-116">Page</span></span><br/>                            |
| <span data-ttu-id="97db8-117">Observações</span><span class="sxs-lookup"><span data-stu-id="97db8-117">Notes</span></span> <br/>          | <span data-ttu-id="97db8-118">Vinculado ao elemento PageWatermark</span><span class="sxs-lookup"><span data-stu-id="97db8-118">Linked to PageWatermark element</span></span><br/> |



 

## <a name="structure-content"></a><span data-ttu-id="97db8-119">Conteúdo da estrutura</span><span class="sxs-lookup"><span data-stu-id="97db8-119">Structure Content</span></span>

<span data-ttu-id="97db8-120">A estrutura XML desse elemento é a seguinte:</span><span class="sxs-lookup"><span data-stu-id="97db8-120">The XML structure of this element is as follows:</span></span>

``` syntax
<psf:ParameterDef name="psk:PageWatermarkTransparency">
  <psf:Property name="psf:DataType">
    <psf:Value xsi:type="xs:string">xs:integer</psf:Value>
  </psf:Property>
  <psf:Property name="psf:DefaultValue">
    <psf:Value xsi:type="xs:integer">0</psf:Value>
  </psf:Property>
  <psf:Property name="psf:MaxValue">
    <psf:Value xsi:type="xs:integer">100</psf:Value>
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
    <psf:Value xsi:type="xs:string">percent</psf:Value>
  </psf:Property>
</psf:ParameterDef>
```

## <a name="structure-properties"></a><span data-ttu-id="97db8-121">Propriedades da estrutura</span><span class="sxs-lookup"><span data-stu-id="97db8-121">Structure Properties</span></span>

<span data-ttu-id="97db8-122">A tabela a seguir descreve as características das variáveis definidas na estrutura XML.</span><span class="sxs-lookup"><span data-stu-id="97db8-122">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="97db8-123">Propriedade</span><span class="sxs-lookup"><span data-stu-id="97db8-123">Property</span></span>                | <span data-ttu-id="97db8-124">xsi:type</span><span class="sxs-lookup"><span data-stu-id="97db8-124">xsi:type</span></span>           | <span data-ttu-id="97db8-125">Valor</span><span class="sxs-lookup"><span data-stu-id="97db8-125">Value</span></span>                      |
|-------------------------|--------------------|----------------------------|
| <span data-ttu-id="97db8-126">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="97db8-126">DataType</span></span><br/>     | <span data-ttu-id="97db8-127">string</span><span class="sxs-lookup"><span data-stu-id="97db8-127">string</span></span><br/>  | <span data-ttu-id="97db8-128">xs:integer</span><span class="sxs-lookup"><span data-stu-id="97db8-128">xs:integer</span></span><br/>      |
| <span data-ttu-id="97db8-129">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="97db8-129">DefaultValue</span></span><br/> | <span data-ttu-id="97db8-130">integer</span><span class="sxs-lookup"><span data-stu-id="97db8-130">integer</span></span><br/> | <span data-ttu-id="97db8-131">0</span><span class="sxs-lookup"><span data-stu-id="97db8-131">0</span></span><br/>               |
| <span data-ttu-id="97db8-132">MaxValue</span><span class="sxs-lookup"><span data-stu-id="97db8-132">MaxValue</span></span><br/>     | <span data-ttu-id="97db8-133">Número inteiro</span><span class="sxs-lookup"><span data-stu-id="97db8-133">integer</span></span><br/> | <span data-ttu-id="97db8-134">100</span><span class="sxs-lookup"><span data-stu-id="97db8-134">100</span></span><br/>             |
| <span data-ttu-id="97db8-135">MinValue</span><span class="sxs-lookup"><span data-stu-id="97db8-135">MinValue</span></span><br/>     | <span data-ttu-id="97db8-136">integer</span><span class="sxs-lookup"><span data-stu-id="97db8-136">integer</span></span><br/> | <span data-ttu-id="97db8-137">0</span><span class="sxs-lookup"><span data-stu-id="97db8-137">0</span></span><br/>               |
| <span data-ttu-id="97db8-138">Vários</span><span class="sxs-lookup"><span data-stu-id="97db8-138">Multiple</span></span><br/>     | <span data-ttu-id="97db8-139">integer</span><span class="sxs-lookup"><span data-stu-id="97db8-139">integer</span></span><br/> | <span data-ttu-id="97db8-140">1</span><span class="sxs-lookup"><span data-stu-id="97db8-140">1</span></span><br/>               |
| <span data-ttu-id="97db8-141">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="97db8-141">Mandatory</span></span><br/>    | <span data-ttu-id="97db8-142">string</span><span class="sxs-lookup"><span data-stu-id="97db8-142">string</span></span><br/>  | <span data-ttu-id="97db8-143">PSK: condicional</span><span class="sxs-lookup"><span data-stu-id="97db8-143">psk:Conditional</span></span><br/> |
| <span data-ttu-id="97db8-144">UnitType</span><span class="sxs-lookup"><span data-stu-id="97db8-144">UnitType</span></span><br/>     | <span data-ttu-id="97db8-145">string</span><span class="sxs-lookup"><span data-stu-id="97db8-145">string</span></span><br/>  | <span data-ttu-id="97db8-146">{1&gt;percent&lt;1}</span><span class="sxs-lookup"><span data-stu-id="97db8-146">percent</span></span><br/>         |



 

## <a name="related-topics"></a><span data-ttu-id="97db8-147">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="97db8-147">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="97db8-148">Especificação de esquema de impressão</span><span class="sxs-lookup"><span data-stu-id="97db8-148">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




