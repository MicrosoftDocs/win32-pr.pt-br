---
description: Saiba mais sobre o elemento PageBlackGenerationProcessingUnderColorAdditionLevel, que descreve a quantidade de tinta de desvio a ser adicionada às áreas com BlackInkLimit.
ms.assetid: da957aca-1655-4e8d-9e7b-4da0f253293b
title: PageBlackGenerationProcessingUnderColorAdditionLevel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e3b496fbe890f53d1da8d1054cc5a19fe6318811
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/19/2021
ms.locfileid: "112408409"
---
# <a name="pageblackgenerationprocessingundercoloradditionlevel"></a><span data-ttu-id="95d04-103">PageBlackGenerationProcessingUnderColorAdditionLevel</span><span class="sxs-lookup"><span data-stu-id="95d04-103">PageBlackGenerationProcessingUnderColorAdditionLevel</span></span>

<span data-ttu-id="95d04-104">Este tópico não é atual.</span><span class="sxs-lookup"><span data-stu-id="95d04-104">This topic is not current.</span></span> <span data-ttu-id="95d04-105">Para obter as informações mais atuais, consulte a [especificação do esquema de impressão](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="95d04-105">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="95d04-106">Descreve a quantidade de tinta de desvio (em proporção de componente cinza) para adicionar a áreas em que o GCR/UCR gerou "BlackInkLimit" (ou UCAStart, se especificado) nas áreas neutras escuras e quase neutros.</span><span class="sxs-lookup"><span data-stu-id="95d04-106">Describes the amount chromatic ink (in gray component ratios) to add to areas where GCR/UCR has generated "BlackInkLimit" (or UCAStart, if specified) in the dark neutrals and near-neutral areas.</span></span>

-   [<span data-ttu-id="95d04-107">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="95d04-107">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="95d04-108">Conteúdo da estrutura</span><span class="sxs-lookup"><span data-stu-id="95d04-108">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="95d04-109">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="95d04-109">Element Information</span></span>



| <span data-ttu-id="95d04-110">Name</span><span class="sxs-lookup"><span data-stu-id="95d04-110">Name</span></span> | <span data-ttu-id="95d04-111">Valor</span><span class="sxs-lookup"><span data-stu-id="95d04-111">Value</span></span> |
|----------------------------|------------------------------------------------------------|
| <span data-ttu-id="95d04-112">Tipo de elemento</span><span class="sxs-lookup"><span data-stu-id="95d04-112">Element Type</span></span> <br/>   | <span data-ttu-id="95d04-113">ParameterDef</span><span class="sxs-lookup"><span data-stu-id="95d04-113">ParameterDef</span></span><br/>                                    |
| <span data-ttu-id="95d04-114">Prefixo de escopo</span><span class="sxs-lookup"><span data-stu-id="95d04-114">Scoping Prefix</span></span> <br/> | <span data-ttu-id="95d04-115">?</span><span class="sxs-lookup"><span data-stu-id="95d04-115">Page</span></span><br/>                                            |
| <span data-ttu-id="95d04-116">Observações</span><span class="sxs-lookup"><span data-stu-id="95d04-116">Notes</span></span> <br/>          | <span data-ttu-id="95d04-117">Vinculado ao elemento PageBlackGenerationProcessing</span><span class="sxs-lookup"><span data-stu-id="95d04-117">Linked to PageBlackGenerationProcessing element</span></span><br/> |



 

## <a name="structure-content"></a><span data-ttu-id="95d04-118">Conteúdo da estrutura</span><span class="sxs-lookup"><span data-stu-id="95d04-118">Structure Content</span></span>

<span data-ttu-id="95d04-119">A estrutura XML desse elemento é:</span><span class="sxs-lookup"><span data-stu-id="95d04-119">The XML structure of this element is:</span></span>

``` syntax
<psf:ParameterDef name="psk:PageBlackGenerationProcessingUnderColorAdditionLevel">
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

## <a name="structure-properties"></a><span data-ttu-id="95d04-120">Propriedades da estrutura</span><span class="sxs-lookup"><span data-stu-id="95d04-120">Structure Properties</span></span>

<span data-ttu-id="95d04-121">A tabela a seguir descreve as características das variáveis definidas na estrutura XML.</span><span class="sxs-lookup"><span data-stu-id="95d04-121">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="95d04-122">Propriedade</span><span class="sxs-lookup"><span data-stu-id="95d04-122">Property</span></span>                | <span data-ttu-id="95d04-123">xsi:type</span><span class="sxs-lookup"><span data-stu-id="95d04-123">xsi:type</span></span>           | <span data-ttu-id="95d04-124">Valor</span><span class="sxs-lookup"><span data-stu-id="95d04-124">Value</span></span>                      |
|-------------------------|--------------------|----------------------------|
| <span data-ttu-id="95d04-125">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="95d04-125">DataType</span></span><br/>     | <span data-ttu-id="95d04-126">string</span><span class="sxs-lookup"><span data-stu-id="95d04-126">string</span></span><br/>  | <span data-ttu-id="95d04-127">xs:integer</span><span class="sxs-lookup"><span data-stu-id="95d04-127">xs:integer</span></span><br/>      |
| <span data-ttu-id="95d04-128">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="95d04-128">DefaultValue</span></span><br/> | <span data-ttu-id="95d04-129">string</span><span class="sxs-lookup"><span data-stu-id="95d04-129">string</span></span><br/>  | <span data-ttu-id="95d04-130">não definido</span><span class="sxs-lookup"><span data-stu-id="95d04-130">undefined</span></span><br/>       |
| <span data-ttu-id="95d04-131">MaxValue</span><span class="sxs-lookup"><span data-stu-id="95d04-131">MaxValue</span></span><br/>     | <span data-ttu-id="95d04-132">Número inteiro</span><span class="sxs-lookup"><span data-stu-id="95d04-132">integer</span></span><br/> | <span data-ttu-id="95d04-133">100</span><span class="sxs-lookup"><span data-stu-id="95d04-133">100</span></span><br/>             |
| <span data-ttu-id="95d04-134">MinValue</span><span class="sxs-lookup"><span data-stu-id="95d04-134">MinValue</span></span><br/>     | <span data-ttu-id="95d04-135">inteiro</span><span class="sxs-lookup"><span data-stu-id="95d04-135">integer</span></span><br/> | <span data-ttu-id="95d04-136">0</span><span class="sxs-lookup"><span data-stu-id="95d04-136">0</span></span><br/>               |
| <span data-ttu-id="95d04-137">Vários</span><span class="sxs-lookup"><span data-stu-id="95d04-137">Multiple</span></span><br/>     | <span data-ttu-id="95d04-138">integer</span><span class="sxs-lookup"><span data-stu-id="95d04-138">integer</span></span><br/> | <span data-ttu-id="95d04-139">1</span><span class="sxs-lookup"><span data-stu-id="95d04-139">1</span></span><br/>               |
| <span data-ttu-id="95d04-140">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="95d04-140">Mandatory</span></span><br/>    | <span data-ttu-id="95d04-141">string</span><span class="sxs-lookup"><span data-stu-id="95d04-141">string</span></span><br/>  | <span data-ttu-id="95d04-142">PSK: condicional</span><span class="sxs-lookup"><span data-stu-id="95d04-142">psk:Conditional</span></span><br/> |
| <span data-ttu-id="95d04-143">UnitType</span><span class="sxs-lookup"><span data-stu-id="95d04-143">UnitType</span></span><br/>     | <span data-ttu-id="95d04-144">string</span><span class="sxs-lookup"><span data-stu-id="95d04-144">string</span></span><br/>  | <span data-ttu-id="95d04-145">{1&gt;percent&lt;1}</span><span class="sxs-lookup"><span data-stu-id="95d04-145">percent</span></span><br/>         |



 

## <a name="related-topics"></a><span data-ttu-id="95d04-146">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="95d04-146">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="95d04-147">Especificação de esquema de impressão</span><span class="sxs-lookup"><span data-stu-id="95d04-147">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




