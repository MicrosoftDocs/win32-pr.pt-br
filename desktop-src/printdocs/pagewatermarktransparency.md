---
description: Obter informações sobre o parâmetro PageWatermarkTransparency. Este tópico não é atual. Para obter as informações mais atuais, consulte a Especificação de Esquema de Impressão.
ms.assetid: f94c1450-9648-4aee-8f88-2a9213eba4a9
title: PageWatermarkTransparency
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 46ba405c3cd4a269edc4585ad8cba4c81f2c05e9
ms.sourcegitcommit: 91530c19d26ba4c57a6af1f37b57f211f580464e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/19/2021
ms.locfileid: "112394781"
---
# <a name="pagewatermarktransparency"></a><span data-ttu-id="02a74-105">PageWatermarkTransparency</span><span class="sxs-lookup"><span data-stu-id="02a74-105">PageWatermarkTransparency</span></span>

<span data-ttu-id="02a74-106">Este tópico não é atual.</span><span class="sxs-lookup"><span data-stu-id="02a74-106">This topic is not current.</span></span> <span data-ttu-id="02a74-107">Para obter as informações mais atuais, consulte a [Especificação de Esquema de Impressão](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="02a74-107">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="02a74-108">Especifica a transparência para a marca-d'água.</span><span class="sxs-lookup"><span data-stu-id="02a74-108">Specifies the transparency for the watermark.</span></span> <span data-ttu-id="02a74-109">Totalmente opaco teria um valor de 0.</span><span class="sxs-lookup"><span data-stu-id="02a74-109">Fully opaque would have a value of 0.</span></span>

-   [<span data-ttu-id="02a74-110">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="02a74-110">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="02a74-111">Conteúdo da estrutura</span><span class="sxs-lookup"><span data-stu-id="02a74-111">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="02a74-112">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="02a74-112">Element Information</span></span>



| <span data-ttu-id="02a74-113">Name</span><span class="sxs-lookup"><span data-stu-id="02a74-113">Name</span></span> | <span data-ttu-id="02a74-114">Valor</span><span class="sxs-lookup"><span data-stu-id="02a74-114">Value</span></span> |
|----------------------------|--------------------------------------------|
| <span data-ttu-id="02a74-115">Tipo de elemento</span><span class="sxs-lookup"><span data-stu-id="02a74-115">Element Type</span></span> <br/>   | <span data-ttu-id="02a74-116">ParameterDef</span><span class="sxs-lookup"><span data-stu-id="02a74-116">ParameterDef</span></span><br/>                    |
| <span data-ttu-id="02a74-117">Prefixo de definição de scoping</span><span class="sxs-lookup"><span data-stu-id="02a74-117">Scoping Prefix</span></span> <br/> | <span data-ttu-id="02a74-118">?</span><span class="sxs-lookup"><span data-stu-id="02a74-118">Page</span></span><br/>                            |
| <span data-ttu-id="02a74-119">Observações</span><span class="sxs-lookup"><span data-stu-id="02a74-119">Notes</span></span> <br/>          | <span data-ttu-id="02a74-120">Vinculado ao elemento PageWatermark</span><span class="sxs-lookup"><span data-stu-id="02a74-120">Linked to PageWatermark element</span></span><br/> |



 

## <a name="structure-content"></a><span data-ttu-id="02a74-121">Conteúdo da estrutura</span><span class="sxs-lookup"><span data-stu-id="02a74-121">Structure Content</span></span>

<span data-ttu-id="02a74-122">A estrutura XML desse elemento é a seguinte:</span><span class="sxs-lookup"><span data-stu-id="02a74-122">The XML structure of this element is as follows:</span></span>

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

## <a name="structure-properties"></a><span data-ttu-id="02a74-123">Propriedades da estrutura</span><span class="sxs-lookup"><span data-stu-id="02a74-123">Structure Properties</span></span>

<span data-ttu-id="02a74-124">A tabela a seguir descreve as características das variáveis definidas na estrutura XML.</span><span class="sxs-lookup"><span data-stu-id="02a74-124">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="02a74-125">Propriedade</span><span class="sxs-lookup"><span data-stu-id="02a74-125">Property</span></span>                | <span data-ttu-id="02a74-126">xsi:type</span><span class="sxs-lookup"><span data-stu-id="02a74-126">xsi:type</span></span>           | <span data-ttu-id="02a74-127">Valor</span><span class="sxs-lookup"><span data-stu-id="02a74-127">Value</span></span>                      |
|-------------------------|--------------------|----------------------------|
| <span data-ttu-id="02a74-128">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="02a74-128">DataType</span></span><br/>     | <span data-ttu-id="02a74-129">string</span><span class="sxs-lookup"><span data-stu-id="02a74-129">string</span></span><br/>  | <span data-ttu-id="02a74-130">xs:integer</span><span class="sxs-lookup"><span data-stu-id="02a74-130">xs:integer</span></span><br/>      |
| <span data-ttu-id="02a74-131">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="02a74-131">DefaultValue</span></span><br/> | <span data-ttu-id="02a74-132">inteiro</span><span class="sxs-lookup"><span data-stu-id="02a74-132">integer</span></span><br/> | <span data-ttu-id="02a74-133">0</span><span class="sxs-lookup"><span data-stu-id="02a74-133">0</span></span><br/>               |
| <span data-ttu-id="02a74-134">MaxValue</span><span class="sxs-lookup"><span data-stu-id="02a74-134">MaxValue</span></span><br/>     | <span data-ttu-id="02a74-135">Número inteiro</span><span class="sxs-lookup"><span data-stu-id="02a74-135">integer</span></span><br/> | <span data-ttu-id="02a74-136">100</span><span class="sxs-lookup"><span data-stu-id="02a74-136">100</span></span><br/>             |
| <span data-ttu-id="02a74-137">Minvalue</span><span class="sxs-lookup"><span data-stu-id="02a74-137">MinValue</span></span><br/>     | <span data-ttu-id="02a74-138">inteiro</span><span class="sxs-lookup"><span data-stu-id="02a74-138">integer</span></span><br/> | <span data-ttu-id="02a74-139">0</span><span class="sxs-lookup"><span data-stu-id="02a74-139">0</span></span><br/>               |
| <span data-ttu-id="02a74-140">Vários</span><span class="sxs-lookup"><span data-stu-id="02a74-140">Multiple</span></span><br/>     | <span data-ttu-id="02a74-141">integer</span><span class="sxs-lookup"><span data-stu-id="02a74-141">integer</span></span><br/> | <span data-ttu-id="02a74-142">1</span><span class="sxs-lookup"><span data-stu-id="02a74-142">1</span></span><br/>               |
| <span data-ttu-id="02a74-143">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="02a74-143">Mandatory</span></span><br/>    | <span data-ttu-id="02a74-144">string</span><span class="sxs-lookup"><span data-stu-id="02a74-144">string</span></span><br/>  | <span data-ttu-id="02a74-145">psk:Conditional</span><span class="sxs-lookup"><span data-stu-id="02a74-145">psk:Conditional</span></span><br/> |
| <span data-ttu-id="02a74-146">Unittype</span><span class="sxs-lookup"><span data-stu-id="02a74-146">UnitType</span></span><br/>     | <span data-ttu-id="02a74-147">string</span><span class="sxs-lookup"><span data-stu-id="02a74-147">string</span></span><br/>  | <span data-ttu-id="02a74-148">{1&gt;percent&lt;1}</span><span class="sxs-lookup"><span data-stu-id="02a74-148">percent</span></span><br/>         |



 

## <a name="related-topics"></a><span data-ttu-id="02a74-149">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="02a74-149">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="02a74-150">Especificação de esquema de impressão</span><span class="sxs-lookup"><span data-stu-id="02a74-150">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




