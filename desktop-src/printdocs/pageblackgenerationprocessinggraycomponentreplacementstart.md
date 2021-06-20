---
description: Saiba mais sobre o elemento PageBlackGenerationProcessingGrayComponentReplacementStart, que descreve o ponto em que o GCR deve começar.
ms.assetid: 28ea95a2-e602-4f71-9488-48525e995814
title: PageBlackGenerationProcessingGrayComponentReplacementStart
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f2e7e5a7e22c20b15dc373a2cce2bfe19e3417d4
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/19/2021
ms.locfileid: "112408459"
---
# <a name="pageblackgenerationprocessinggraycomponentreplacementstart"></a><span data-ttu-id="d58f3-103">PageBlackGenerationProcessingGrayComponentReplacementStart</span><span class="sxs-lookup"><span data-stu-id="d58f3-103">PageBlackGenerationProcessingGrayComponentReplacementStart</span></span>

<span data-ttu-id="d58f3-104">Este tópico não é atual.</span><span class="sxs-lookup"><span data-stu-id="d58f3-104">This topic is not current.</span></span> <span data-ttu-id="d58f3-105">Para obter as informações mais atuais, consulte a [Especificação de Esquema de Impressão](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="d58f3-105">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="d58f3-106">Descreve o ponto no intervalo "realçar para sombra" em que o GCR deve iniciar (sombra 100% mais escura).</span><span class="sxs-lookup"><span data-stu-id="d58f3-106">Describes the point in the "highlight to shadow" range where GCR should start (100% darkest shadow).</span></span>

-   [<span data-ttu-id="d58f3-107">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="d58f3-107">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="d58f3-108">Conteúdo da estrutura</span><span class="sxs-lookup"><span data-stu-id="d58f3-108">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="d58f3-109">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="d58f3-109">Element Information</span></span>



| <span data-ttu-id="d58f3-110">Name</span><span class="sxs-lookup"><span data-stu-id="d58f3-110">Name</span></span> | <span data-ttu-id="d58f3-111">Valor</span><span class="sxs-lookup"><span data-stu-id="d58f3-111">Value</span></span> |
|----------------------------|------------------------------------------------------------|
| <span data-ttu-id="d58f3-112">Tipo de elemento</span><span class="sxs-lookup"><span data-stu-id="d58f3-112">Element Type</span></span> <br/>   | <span data-ttu-id="d58f3-113">ParameterDef</span><span class="sxs-lookup"><span data-stu-id="d58f3-113">ParameterDef</span></span><br/>                                    |
| <span data-ttu-id="d58f3-114">Prefixo de definição de scoping</span><span class="sxs-lookup"><span data-stu-id="d58f3-114">Scoping Prefix</span></span> <br/> | <span data-ttu-id="d58f3-115">?</span><span class="sxs-lookup"><span data-stu-id="d58f3-115">Page</span></span><br/>                                            |
| <span data-ttu-id="d58f3-116">Observações</span><span class="sxs-lookup"><span data-stu-id="d58f3-116">Notes</span></span> <br/>          | <span data-ttu-id="d58f3-117">Vinculado ao elemento PageBlackGenerationProcessing</span><span class="sxs-lookup"><span data-stu-id="d58f3-117">Linked to PageBlackGenerationProcessing element</span></span><br/> |



 

## <a name="structure-content"></a><span data-ttu-id="d58f3-118">Conteúdo da estrutura</span><span class="sxs-lookup"><span data-stu-id="d58f3-118">Structure Content</span></span>

<span data-ttu-id="d58f3-119">A estrutura XML desse elemento é:</span><span class="sxs-lookup"><span data-stu-id="d58f3-119">The XML structure of this element is:</span></span>

``` syntax
<psf:ParameterDef name="psk:PageBlackGenerationProcessingGrayComponentReplacementStart">
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

## <a name="structure-properties"></a><span data-ttu-id="d58f3-120">Propriedades da estrutura</span><span class="sxs-lookup"><span data-stu-id="d58f3-120">Structure Properties</span></span>

<span data-ttu-id="d58f3-121">A tabela a seguir descreve as características das variáveis definidas na estrutura XML.</span><span class="sxs-lookup"><span data-stu-id="d58f3-121">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="d58f3-122">Propriedade</span><span class="sxs-lookup"><span data-stu-id="d58f3-122">Property</span></span>                | <span data-ttu-id="d58f3-123">xsi:type</span><span class="sxs-lookup"><span data-stu-id="d58f3-123">xsi:type</span></span>           | <span data-ttu-id="d58f3-124">Valor</span><span class="sxs-lookup"><span data-stu-id="d58f3-124">Value</span></span>                      |
|-------------------------|--------------------|----------------------------|
| <span data-ttu-id="d58f3-125">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="d58f3-125">DataType</span></span><br/>     | <span data-ttu-id="d58f3-126">string</span><span class="sxs-lookup"><span data-stu-id="d58f3-126">string</span></span><br/>  | <span data-ttu-id="d58f3-127">xs:integer</span><span class="sxs-lookup"><span data-stu-id="d58f3-127">xs:integer</span></span><br/>      |
| <span data-ttu-id="d58f3-128">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="d58f3-128">DefaultValue</span></span><br/> | <span data-ttu-id="d58f3-129">string</span><span class="sxs-lookup"><span data-stu-id="d58f3-129">string</span></span><br/>  | <span data-ttu-id="d58f3-130">não definido</span><span class="sxs-lookup"><span data-stu-id="d58f3-130">undefined</span></span><br/>       |
| <span data-ttu-id="d58f3-131">MaxValue</span><span class="sxs-lookup"><span data-stu-id="d58f3-131">MaxValue</span></span><br/>     | <span data-ttu-id="d58f3-132">Número inteiro</span><span class="sxs-lookup"><span data-stu-id="d58f3-132">integer</span></span><br/> | <span data-ttu-id="d58f3-133">100</span><span class="sxs-lookup"><span data-stu-id="d58f3-133">100</span></span><br/>             |
| <span data-ttu-id="d58f3-134">Minvalue</span><span class="sxs-lookup"><span data-stu-id="d58f3-134">MinValue</span></span><br/>     | <span data-ttu-id="d58f3-135">inteiro</span><span class="sxs-lookup"><span data-stu-id="d58f3-135">integer</span></span><br/> | <span data-ttu-id="d58f3-136">0</span><span class="sxs-lookup"><span data-stu-id="d58f3-136">0</span></span><br/>               |
| <span data-ttu-id="d58f3-137">Vários</span><span class="sxs-lookup"><span data-stu-id="d58f3-137">Multiple</span></span><br/>     | <span data-ttu-id="d58f3-138">integer</span><span class="sxs-lookup"><span data-stu-id="d58f3-138">integer</span></span><br/> | <span data-ttu-id="d58f3-139">1</span><span class="sxs-lookup"><span data-stu-id="d58f3-139">1</span></span><br/>               |
| <span data-ttu-id="d58f3-140">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="d58f3-140">Mandatory</span></span><br/>    | <span data-ttu-id="d58f3-141">string</span><span class="sxs-lookup"><span data-stu-id="d58f3-141">string</span></span><br/>  | <span data-ttu-id="d58f3-142">psk:Conditional</span><span class="sxs-lookup"><span data-stu-id="d58f3-142">psk:Conditional</span></span><br/> |
| <span data-ttu-id="d58f3-143">Unittype</span><span class="sxs-lookup"><span data-stu-id="d58f3-143">UnitType</span></span><br/>     | <span data-ttu-id="d58f3-144">string</span><span class="sxs-lookup"><span data-stu-id="d58f3-144">string</span></span><br/>  | <span data-ttu-id="d58f3-145">{1&gt;percent&lt;1}</span><span class="sxs-lookup"><span data-stu-id="d58f3-145">percent</span></span><br/>         |



 

## <a name="related-topics"></a><span data-ttu-id="d58f3-146">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="d58f3-146">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d58f3-147">Especificação de esquema de impressão</span><span class="sxs-lookup"><span data-stu-id="d58f3-147">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




