---
description: Este tópico não é atual. Para obter as informações mais atuais, consulte a especificação do esquema de impressão.
ms.assetid: ba62f902-9bc9-4492-ab53-4a4ddbc23530
title: PageBlackGenerationProcessingGrayComponentReplacementExtent
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 58c71700b23459c087361e9e28ac0c43120aff90
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/05/2021
ms.locfileid: "103837708"
---
# <a name="pageblackgenerationprocessinggraycomponentreplacementextent"></a><span data-ttu-id="c1ffe-104">PageBlackGenerationProcessingGrayComponentReplacementExtent</span><span class="sxs-lookup"><span data-stu-id="c1ffe-104">PageBlackGenerationProcessingGrayComponentReplacementExtent</span></span>

<span data-ttu-id="c1ffe-105">Este tópico não é atual.</span><span class="sxs-lookup"><span data-stu-id="c1ffe-105">This topic is not current.</span></span> <span data-ttu-id="c1ffe-106">Para obter as informações mais atuais, consulte a [especificação do esquema de impressão](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="c1ffe-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="c1ffe-107">Descreve a extensão além dos neutros (em cores de desvio) que o GCR aplica.</span><span class="sxs-lookup"><span data-stu-id="c1ffe-107">Describes the extented beyond neutrals (into chromatic colors) that GCR applies.</span></span> <span data-ttu-id="c1ffe-108">0% = substituição de componente uniforme, 100% = substituição de componente cinza.</span><span class="sxs-lookup"><span data-stu-id="c1ffe-108">0% = Uniform component replacement, 100% = Gray component replacement.</span></span>

-   [<span data-ttu-id="c1ffe-109">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="c1ffe-109">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="c1ffe-110">Conteúdo da estrutura</span><span class="sxs-lookup"><span data-stu-id="c1ffe-110">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="c1ffe-111">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="c1ffe-111">Element Information</span></span>



| <span data-ttu-id="c1ffe-112">Nome</span><span class="sxs-lookup"><span data-stu-id="c1ffe-112">Name</span></span>                       |                                                            |
|----------------------------|------------------------------------------------------------|
| <span data-ttu-id="c1ffe-113">Tipo de elemento</span><span class="sxs-lookup"><span data-stu-id="c1ffe-113">Element Type</span></span> <br/>   | <span data-ttu-id="c1ffe-114">ParameterDef</span><span class="sxs-lookup"><span data-stu-id="c1ffe-114">ParameterDef</span></span><br/>                                    |
| <span data-ttu-id="c1ffe-115">Prefixo de escopo</span><span class="sxs-lookup"><span data-stu-id="c1ffe-115">Scoping Prefix</span></span> <br/> | <span data-ttu-id="c1ffe-116">?</span><span class="sxs-lookup"><span data-stu-id="c1ffe-116">Page</span></span><br/>                                            |
| <span data-ttu-id="c1ffe-117">Observações</span><span class="sxs-lookup"><span data-stu-id="c1ffe-117">Notes</span></span> <br/>          | <span data-ttu-id="c1ffe-118">Vinculado ao elemento PageBlackGenerationProcessing</span><span class="sxs-lookup"><span data-stu-id="c1ffe-118">Linked to PageBlackGenerationProcessing element</span></span><br/> |



 

## <a name="structure-content"></a><span data-ttu-id="c1ffe-119">Conteúdo da estrutura</span><span class="sxs-lookup"><span data-stu-id="c1ffe-119">Structure Content</span></span>

<span data-ttu-id="c1ffe-120">A estrutura XML desse elemento é:</span><span class="sxs-lookup"><span data-stu-id="c1ffe-120">The XML structure of this element is:</span></span>

``` syntax
<psf:ParameterDef name="psk:PageBlackGenerationProcessingGrayComponentReplacementExtent">
  <psf:Property name="psf:DataType">
    <psf:Value xsi:type="xs:string">xs:integer</psf:Value>
  </psf:Property>
  <psf:Property name="psf:DefaultValue">
    <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
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

## <a name="structure-properties"></a><span data-ttu-id="c1ffe-121">Propriedades da estrutura</span><span class="sxs-lookup"><span data-stu-id="c1ffe-121">Structure Properties</span></span>

<span data-ttu-id="c1ffe-122">A tabela a seguir descreve as características das variáveis definidas na estrutura XML.</span><span class="sxs-lookup"><span data-stu-id="c1ffe-122">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="c1ffe-123">Propriedade</span><span class="sxs-lookup"><span data-stu-id="c1ffe-123">Property</span></span>                | <span data-ttu-id="c1ffe-124">xsi:type</span><span class="sxs-lookup"><span data-stu-id="c1ffe-124">xsi:type</span></span>           | <span data-ttu-id="c1ffe-125">Valor</span><span class="sxs-lookup"><span data-stu-id="c1ffe-125">Value</span></span>                      |
|-------------------------|--------------------|----------------------------|
| <span data-ttu-id="c1ffe-126">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="c1ffe-126">DataType</span></span><br/>     | <span data-ttu-id="c1ffe-127">string</span><span class="sxs-lookup"><span data-stu-id="c1ffe-127">string</span></span><br/>  | <span data-ttu-id="c1ffe-128">xs:integer</span><span class="sxs-lookup"><span data-stu-id="c1ffe-128">xs:integer</span></span><br/>      |
| <span data-ttu-id="c1ffe-129">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="c1ffe-129">DefaultValue</span></span><br/> | <span data-ttu-id="c1ffe-130">string</span><span class="sxs-lookup"><span data-stu-id="c1ffe-130">string</span></span><br/>  | <span data-ttu-id="c1ffe-131">não definido</span><span class="sxs-lookup"><span data-stu-id="c1ffe-131">undefined</span></span><br/>       |
| <span data-ttu-id="c1ffe-132">MaxValue</span><span class="sxs-lookup"><span data-stu-id="c1ffe-132">MaxValue</span></span><br/>     | <span data-ttu-id="c1ffe-133">Número inteiro</span><span class="sxs-lookup"><span data-stu-id="c1ffe-133">integer</span></span><br/> | <span data-ttu-id="c1ffe-134">100</span><span class="sxs-lookup"><span data-stu-id="c1ffe-134">100</span></span><br/>             |
| <span data-ttu-id="c1ffe-135">MinValue</span><span class="sxs-lookup"><span data-stu-id="c1ffe-135">MinValue</span></span><br/>     | <span data-ttu-id="c1ffe-136">integer</span><span class="sxs-lookup"><span data-stu-id="c1ffe-136">integer</span></span><br/> | <span data-ttu-id="c1ffe-137">0</span><span class="sxs-lookup"><span data-stu-id="c1ffe-137">0</span></span><br/>               |
| <span data-ttu-id="c1ffe-138">Vários</span><span class="sxs-lookup"><span data-stu-id="c1ffe-138">Multiple</span></span><br/>     | <span data-ttu-id="c1ffe-139">integer</span><span class="sxs-lookup"><span data-stu-id="c1ffe-139">integer</span></span><br/> | <span data-ttu-id="c1ffe-140">1</span><span class="sxs-lookup"><span data-stu-id="c1ffe-140">1</span></span><br/>               |
| <span data-ttu-id="c1ffe-141">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="c1ffe-141">Mandatory</span></span><br/>    | <span data-ttu-id="c1ffe-142">string</span><span class="sxs-lookup"><span data-stu-id="c1ffe-142">string</span></span><br/>  | <span data-ttu-id="c1ffe-143">PSK: condicional</span><span class="sxs-lookup"><span data-stu-id="c1ffe-143">psk:Conditional</span></span><br/> |
| <span data-ttu-id="c1ffe-144">UnitType</span><span class="sxs-lookup"><span data-stu-id="c1ffe-144">UnitType</span></span><br/>     | <span data-ttu-id="c1ffe-145">string</span><span class="sxs-lookup"><span data-stu-id="c1ffe-145">string</span></span><br/>  | <span data-ttu-id="c1ffe-146">{1&gt;percent&lt;1}</span><span class="sxs-lookup"><span data-stu-id="c1ffe-146">percent</span></span><br/>         |



 

## <a name="related-topics"></a><span data-ttu-id="c1ffe-147">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="c1ffe-147">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c1ffe-148">Especificação de esquema de impressão</span><span class="sxs-lookup"><span data-stu-id="c1ffe-148">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




