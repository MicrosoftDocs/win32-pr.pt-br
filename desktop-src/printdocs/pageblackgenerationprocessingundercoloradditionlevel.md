---
description: Este tópico não é atual. Para obter as informações mais atuais, consulte a especificação do esquema de impressão.
ms.assetid: da957aca-1655-4e8d-9e7b-4da0f253293b
title: PageBlackGenerationProcessingUnderColorAdditionLevel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8e1b43d8d9ee366fc742dc3d7b1617f6297fc96e
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/26/2021
ms.locfileid: "107995663"
---
# <a name="pageblackgenerationprocessingundercoloradditionlevel"></a><span data-ttu-id="d53fb-104">PageBlackGenerationProcessingUnderColorAdditionLevel</span><span class="sxs-lookup"><span data-stu-id="d53fb-104">PageBlackGenerationProcessingUnderColorAdditionLevel</span></span>

<span data-ttu-id="d53fb-105">Este tópico não é atual.</span><span class="sxs-lookup"><span data-stu-id="d53fb-105">This topic is not current.</span></span> <span data-ttu-id="d53fb-106">Para obter as informações mais atuais, consulte a [especificação do esquema de impressão](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="d53fb-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="d53fb-107">Descreve a quantidade de tinta de desvio (em proporção de componente cinza) para adicionar a áreas em que o GCR/UCR gerou "BlackInkLimit" (ou UCAStart, se especificado) nas áreas neutras escuras e quase neutros.</span><span class="sxs-lookup"><span data-stu-id="d53fb-107">Describes the amount chromatic ink (in gray component ratios) to add to areas where GCR/UCR has generated "BlackInkLimit" (or UCAStart, if specified) in the dark neutrals and near-neutral areas.</span></span>

-   [<span data-ttu-id="d53fb-108">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="d53fb-108">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="d53fb-109">Conteúdo da estrutura</span><span class="sxs-lookup"><span data-stu-id="d53fb-109">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="d53fb-110">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="d53fb-110">Element Information</span></span>



| <span data-ttu-id="d53fb-111">Nome</span><span class="sxs-lookup"><span data-stu-id="d53fb-111">Name</span></span> | <span data-ttu-id="d53fb-112">Valor</span><span class="sxs-lookup"><span data-stu-id="d53fb-112">Value</span></span> |
|----------------------------|------------------------------------------------------------|
| <span data-ttu-id="d53fb-113">Tipo de elemento</span><span class="sxs-lookup"><span data-stu-id="d53fb-113">Element Type</span></span> <br/>   | <span data-ttu-id="d53fb-114">ParameterDef</span><span class="sxs-lookup"><span data-stu-id="d53fb-114">ParameterDef</span></span><br/>                                    |
| <span data-ttu-id="d53fb-115">Prefixo de escopo</span><span class="sxs-lookup"><span data-stu-id="d53fb-115">Scoping Prefix</span></span> <br/> | <span data-ttu-id="d53fb-116">?</span><span class="sxs-lookup"><span data-stu-id="d53fb-116">Page</span></span><br/>                                            |
| <span data-ttu-id="d53fb-117">Observações</span><span class="sxs-lookup"><span data-stu-id="d53fb-117">Notes</span></span> <br/>          | <span data-ttu-id="d53fb-118">Vinculado ao elemento PageBlackGenerationProcessing</span><span class="sxs-lookup"><span data-stu-id="d53fb-118">Linked to PageBlackGenerationProcessing element</span></span><br/> |



 

## <a name="structure-content"></a><span data-ttu-id="d53fb-119">Conteúdo da estrutura</span><span class="sxs-lookup"><span data-stu-id="d53fb-119">Structure Content</span></span>

<span data-ttu-id="d53fb-120">A estrutura XML desse elemento é:</span><span class="sxs-lookup"><span data-stu-id="d53fb-120">The XML structure of this element is:</span></span>

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

## <a name="structure-properties"></a><span data-ttu-id="d53fb-121">Propriedades da estrutura</span><span class="sxs-lookup"><span data-stu-id="d53fb-121">Structure Properties</span></span>

<span data-ttu-id="d53fb-122">A tabela a seguir descreve as características das variáveis definidas na estrutura XML.</span><span class="sxs-lookup"><span data-stu-id="d53fb-122">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="d53fb-123">Propriedade</span><span class="sxs-lookup"><span data-stu-id="d53fb-123">Property</span></span>                | <span data-ttu-id="d53fb-124">xsi:type</span><span class="sxs-lookup"><span data-stu-id="d53fb-124">xsi:type</span></span>           | <span data-ttu-id="d53fb-125">Valor</span><span class="sxs-lookup"><span data-stu-id="d53fb-125">Value</span></span>                      |
|-------------------------|--------------------|----------------------------|
| <span data-ttu-id="d53fb-126">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="d53fb-126">DataType</span></span><br/>     | <span data-ttu-id="d53fb-127">string</span><span class="sxs-lookup"><span data-stu-id="d53fb-127">string</span></span><br/>  | <span data-ttu-id="d53fb-128">xs:integer</span><span class="sxs-lookup"><span data-stu-id="d53fb-128">xs:integer</span></span><br/>      |
| <span data-ttu-id="d53fb-129">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="d53fb-129">DefaultValue</span></span><br/> | <span data-ttu-id="d53fb-130">string</span><span class="sxs-lookup"><span data-stu-id="d53fb-130">string</span></span><br/>  | <span data-ttu-id="d53fb-131">não definido</span><span class="sxs-lookup"><span data-stu-id="d53fb-131">undefined</span></span><br/>       |
| <span data-ttu-id="d53fb-132">MaxValue</span><span class="sxs-lookup"><span data-stu-id="d53fb-132">MaxValue</span></span><br/>     | <span data-ttu-id="d53fb-133">Número inteiro</span><span class="sxs-lookup"><span data-stu-id="d53fb-133">integer</span></span><br/> | <span data-ttu-id="d53fb-134">100</span><span class="sxs-lookup"><span data-stu-id="d53fb-134">100</span></span><br/>             |
| <span data-ttu-id="d53fb-135">MinValue</span><span class="sxs-lookup"><span data-stu-id="d53fb-135">MinValue</span></span><br/>     | <span data-ttu-id="d53fb-136">integer</span><span class="sxs-lookup"><span data-stu-id="d53fb-136">integer</span></span><br/> | <span data-ttu-id="d53fb-137">0</span><span class="sxs-lookup"><span data-stu-id="d53fb-137">0</span></span><br/>               |
| <span data-ttu-id="d53fb-138">Vários</span><span class="sxs-lookup"><span data-stu-id="d53fb-138">Multiple</span></span><br/>     | <span data-ttu-id="d53fb-139">integer</span><span class="sxs-lookup"><span data-stu-id="d53fb-139">integer</span></span><br/> | <span data-ttu-id="d53fb-140">1</span><span class="sxs-lookup"><span data-stu-id="d53fb-140">1</span></span><br/>               |
| <span data-ttu-id="d53fb-141">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="d53fb-141">Mandatory</span></span><br/>    | <span data-ttu-id="d53fb-142">string</span><span class="sxs-lookup"><span data-stu-id="d53fb-142">string</span></span><br/>  | <span data-ttu-id="d53fb-143">PSK: condicional</span><span class="sxs-lookup"><span data-stu-id="d53fb-143">psk:Conditional</span></span><br/> |
| <span data-ttu-id="d53fb-144">UnitType</span><span class="sxs-lookup"><span data-stu-id="d53fb-144">UnitType</span></span><br/>     | <span data-ttu-id="d53fb-145">string</span><span class="sxs-lookup"><span data-stu-id="d53fb-145">string</span></span><br/>  | <span data-ttu-id="d53fb-146">{1&gt;percent&lt;1}</span><span class="sxs-lookup"><span data-stu-id="d53fb-146">percent</span></span><br/>         |



 

## <a name="related-topics"></a><span data-ttu-id="d53fb-147">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="d53fb-147">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d53fb-148">Especificação de esquema de impressão</span><span class="sxs-lookup"><span data-stu-id="d53fb-148">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




