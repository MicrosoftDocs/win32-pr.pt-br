---
description: Saiba mais sobre o elemento PageBlackGenerationProcessingTotalInkCoverageLimit, que especifica a soma máxima permitida das quatro coberturas de tinta em qualquer lugar em uma imagem.
ms.assetid: 7ccd02c2-7cec-4d9d-83c1-512f25f4045c
title: PageBlackGenerationProcessingTotalInkCoverageLimit
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 68410cabdfafa5ce82450821e4ae45709ee8d4c9
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/19/2021
ms.locfileid: "112408439"
---
# <a name="pageblackgenerationprocessingtotalinkcoveragelimit"></a><span data-ttu-id="1a0ec-103">PageBlackGenerationProcessingTotalInkCoverageLimit</span><span class="sxs-lookup"><span data-stu-id="1a0ec-103">PageBlackGenerationProcessingTotalInkCoverageLimit</span></span>

<span data-ttu-id="1a0ec-104">Este tópico não é atual.</span><span class="sxs-lookup"><span data-stu-id="1a0ec-104">This topic is not current.</span></span> <span data-ttu-id="1a0ec-105">Para obter as informações mais atuais, consulte a [Especificação de Esquema de Impressão](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="1a0ec-105">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="1a0ec-106">Especifica a soma máxima permitida das quatro coberturas de tinta em qualquer lugar em uma imagem.</span><span class="sxs-lookup"><span data-stu-id="1a0ec-106">Specifies the maximum allowed sum of the four ink coverage anywhere in an image.</span></span>

-   [<span data-ttu-id="1a0ec-107">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="1a0ec-107">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="1a0ec-108">Conteúdo da estrutura</span><span class="sxs-lookup"><span data-stu-id="1a0ec-108">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="1a0ec-109">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="1a0ec-109">Element Information</span></span>



| <span data-ttu-id="1a0ec-110">Name</span><span class="sxs-lookup"><span data-stu-id="1a0ec-110">Name</span></span> | <span data-ttu-id="1a0ec-111">Valor</span><span class="sxs-lookup"><span data-stu-id="1a0ec-111">Value</span></span> |
|----------------------------|------------------------------------------------------------|
| <span data-ttu-id="1a0ec-112">Tipo de elemento</span><span class="sxs-lookup"><span data-stu-id="1a0ec-112">Element Type</span></span> <br/>   | <span data-ttu-id="1a0ec-113">ParameterDef</span><span class="sxs-lookup"><span data-stu-id="1a0ec-113">ParameterDef</span></span><br/>                                    |
| <span data-ttu-id="1a0ec-114">Prefixo de definição de scoping</span><span class="sxs-lookup"><span data-stu-id="1a0ec-114">Scoping Prefix</span></span> <br/> | <span data-ttu-id="1a0ec-115">?</span><span class="sxs-lookup"><span data-stu-id="1a0ec-115">Page</span></span><br/>                                            |
| <span data-ttu-id="1a0ec-116">Observações</span><span class="sxs-lookup"><span data-stu-id="1a0ec-116">Notes</span></span> <br/>          | <span data-ttu-id="1a0ec-117">Vinculado ao elemento PageBlackGenerationProcessing</span><span class="sxs-lookup"><span data-stu-id="1a0ec-117">Linked to PageBlackGenerationProcessing element</span></span><br/> |



 

## <a name="structure-content"></a><span data-ttu-id="1a0ec-118">Conteúdo da estrutura</span><span class="sxs-lookup"><span data-stu-id="1a0ec-118">Structure Content</span></span>

<span data-ttu-id="1a0ec-119">A estrutura XML desse elemento é:</span><span class="sxs-lookup"><span data-stu-id="1a0ec-119">The XML structure of this element is:</span></span>

``` syntax
<psf:ParameterDef name="psk:PageBlackGenerationProcessingTotalInkCoverageLimit">
  <psf:Property name="psf:DataType">
    <psf:Value xsi:type="xs:string">xs:integer</psf:Value>
  </psf:Property>
  <psf:Property name="psf:DefaultValue">
    <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
  </psf:Property>
  <psf:Property name="psf:MaxValue">
    <psf:Value xsi:type="xs:integer">400</psf:Value>
  </psf:Property>
  <psf:Property name="psf:MinValue">
    <psf:Value xsi:type="xs:integer">200</psf:Value>
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

## <a name="structure-properties"></a><span data-ttu-id="1a0ec-120">Propriedades da estrutura</span><span class="sxs-lookup"><span data-stu-id="1a0ec-120">Structure Properties</span></span>

<span data-ttu-id="1a0ec-121">A tabela a seguir descreve as características das variáveis definidas na estrutura XML.</span><span class="sxs-lookup"><span data-stu-id="1a0ec-121">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="1a0ec-122">Propriedade</span><span class="sxs-lookup"><span data-stu-id="1a0ec-122">Property</span></span>                | <span data-ttu-id="1a0ec-123">xsi:type</span><span class="sxs-lookup"><span data-stu-id="1a0ec-123">xsi:type</span></span>           | <span data-ttu-id="1a0ec-124">Valor</span><span class="sxs-lookup"><span data-stu-id="1a0ec-124">Value</span></span>                      |
|-------------------------|--------------------|----------------------------|
| <span data-ttu-id="1a0ec-125">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="1a0ec-125">DataType</span></span><br/>     | <span data-ttu-id="1a0ec-126">string</span><span class="sxs-lookup"><span data-stu-id="1a0ec-126">string</span></span><br/>  | <span data-ttu-id="1a0ec-127">xs:integer</span><span class="sxs-lookup"><span data-stu-id="1a0ec-127">xs:integer</span></span><br/>      |
| <span data-ttu-id="1a0ec-128">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="1a0ec-128">DefaultValue</span></span><br/> | <span data-ttu-id="1a0ec-129">string</span><span class="sxs-lookup"><span data-stu-id="1a0ec-129">string</span></span><br/>  | <span data-ttu-id="1a0ec-130">não definido</span><span class="sxs-lookup"><span data-stu-id="1a0ec-130">undefined</span></span><br/>       |
| <span data-ttu-id="1a0ec-131">MaxValue</span><span class="sxs-lookup"><span data-stu-id="1a0ec-131">MaxValue</span></span><br/>     | <span data-ttu-id="1a0ec-132">Número inteiro</span><span class="sxs-lookup"><span data-stu-id="1a0ec-132">integer</span></span><br/> | <span data-ttu-id="1a0ec-133">400</span><span class="sxs-lookup"><span data-stu-id="1a0ec-133">400</span></span><br/>             |
| <span data-ttu-id="1a0ec-134">Minvalue</span><span class="sxs-lookup"><span data-stu-id="1a0ec-134">MinValue</span></span><br/>     | <span data-ttu-id="1a0ec-135">Número inteiro</span><span class="sxs-lookup"><span data-stu-id="1a0ec-135">integer</span></span><br/> | <span data-ttu-id="1a0ec-136">200</span><span class="sxs-lookup"><span data-stu-id="1a0ec-136">200</span></span><br/>             |
| <span data-ttu-id="1a0ec-137">Vários</span><span class="sxs-lookup"><span data-stu-id="1a0ec-137">Multiple</span></span><br/>     | <span data-ttu-id="1a0ec-138">integer</span><span class="sxs-lookup"><span data-stu-id="1a0ec-138">integer</span></span><br/> | <span data-ttu-id="1a0ec-139">1</span><span class="sxs-lookup"><span data-stu-id="1a0ec-139">1</span></span><br/>               |
| <span data-ttu-id="1a0ec-140">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="1a0ec-140">Mandatory</span></span><br/>    | <span data-ttu-id="1a0ec-141">string</span><span class="sxs-lookup"><span data-stu-id="1a0ec-141">string</span></span><br/>  | <span data-ttu-id="1a0ec-142">psk:Conditional</span><span class="sxs-lookup"><span data-stu-id="1a0ec-142">psk:Conditional</span></span><br/> |
| <span data-ttu-id="1a0ec-143">Unittype</span><span class="sxs-lookup"><span data-stu-id="1a0ec-143">UnitType</span></span><br/>     | <span data-ttu-id="1a0ec-144">string</span><span class="sxs-lookup"><span data-stu-id="1a0ec-144">string</span></span><br/>  | <span data-ttu-id="1a0ec-145">{1&gt;percent&lt;1}</span><span class="sxs-lookup"><span data-stu-id="1a0ec-145">percent</span></span><br/>         |



 

## <a name="related-topics"></a><span data-ttu-id="1a0ec-146">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="1a0ec-146">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1a0ec-147">Especificação de esquema de impressão</span><span class="sxs-lookup"><span data-stu-id="1a0ec-147">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




