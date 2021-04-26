---
description: Este tópico não é atual. Para obter as informações mais atuais, consulte a especificação do esquema de impressão.
ms.assetid: 28ea95a2-e602-4f71-9488-48525e995814
title: PageBlackGenerationProcessingGrayComponentReplacementStart
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2608535c65cbde04005334ed970c0d27cb1feffb
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/26/2021
ms.locfileid: "107996173"
---
# <a name="pageblackgenerationprocessinggraycomponentreplacementstart"></a><span data-ttu-id="7cca9-104">PageBlackGenerationProcessingGrayComponentReplacementStart</span><span class="sxs-lookup"><span data-stu-id="7cca9-104">PageBlackGenerationProcessingGrayComponentReplacementStart</span></span>

<span data-ttu-id="7cca9-105">Este tópico não é atual.</span><span class="sxs-lookup"><span data-stu-id="7cca9-105">This topic is not current.</span></span> <span data-ttu-id="7cca9-106">Para obter as informações mais atuais, consulte a [especificação do esquema de impressão](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="7cca9-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="7cca9-107">Descreve o ponto no intervalo de "realce para sombra" em que GCR deve iniciar (100% de sombra mais escura).</span><span class="sxs-lookup"><span data-stu-id="7cca9-107">Describes the point in the "highlight to shadow" range where GCR should start (100% darkest shadow).</span></span>

-   [<span data-ttu-id="7cca9-108">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="7cca9-108">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="7cca9-109">Conteúdo da estrutura</span><span class="sxs-lookup"><span data-stu-id="7cca9-109">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="7cca9-110">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="7cca9-110">Element Information</span></span>



| <span data-ttu-id="7cca9-111">Nome</span><span class="sxs-lookup"><span data-stu-id="7cca9-111">Name</span></span> | <span data-ttu-id="7cca9-112">Valor</span><span class="sxs-lookup"><span data-stu-id="7cca9-112">Value</span></span> |
|----------------------------|------------------------------------------------------------|
| <span data-ttu-id="7cca9-113">Tipo de elemento</span><span class="sxs-lookup"><span data-stu-id="7cca9-113">Element Type</span></span> <br/>   | <span data-ttu-id="7cca9-114">ParameterDef</span><span class="sxs-lookup"><span data-stu-id="7cca9-114">ParameterDef</span></span><br/>                                    |
| <span data-ttu-id="7cca9-115">Prefixo de escopo</span><span class="sxs-lookup"><span data-stu-id="7cca9-115">Scoping Prefix</span></span> <br/> | <span data-ttu-id="7cca9-116">?</span><span class="sxs-lookup"><span data-stu-id="7cca9-116">Page</span></span><br/>                                            |
| <span data-ttu-id="7cca9-117">Observações</span><span class="sxs-lookup"><span data-stu-id="7cca9-117">Notes</span></span> <br/>          | <span data-ttu-id="7cca9-118">Vinculado ao elemento PageBlackGenerationProcessing</span><span class="sxs-lookup"><span data-stu-id="7cca9-118">Linked to PageBlackGenerationProcessing element</span></span><br/> |



 

## <a name="structure-content"></a><span data-ttu-id="7cca9-119">Conteúdo da estrutura</span><span class="sxs-lookup"><span data-stu-id="7cca9-119">Structure Content</span></span>

<span data-ttu-id="7cca9-120">A estrutura XML desse elemento é:</span><span class="sxs-lookup"><span data-stu-id="7cca9-120">The XML structure of this element is:</span></span>

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

## <a name="structure-properties"></a><span data-ttu-id="7cca9-121">Propriedades da estrutura</span><span class="sxs-lookup"><span data-stu-id="7cca9-121">Structure Properties</span></span>

<span data-ttu-id="7cca9-122">A tabela a seguir descreve as características das variáveis definidas na estrutura XML.</span><span class="sxs-lookup"><span data-stu-id="7cca9-122">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="7cca9-123">Propriedade</span><span class="sxs-lookup"><span data-stu-id="7cca9-123">Property</span></span>                | <span data-ttu-id="7cca9-124">xsi:type</span><span class="sxs-lookup"><span data-stu-id="7cca9-124">xsi:type</span></span>           | <span data-ttu-id="7cca9-125">Valor</span><span class="sxs-lookup"><span data-stu-id="7cca9-125">Value</span></span>                      |
|-------------------------|--------------------|----------------------------|
| <span data-ttu-id="7cca9-126">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="7cca9-126">DataType</span></span><br/>     | <span data-ttu-id="7cca9-127">string</span><span class="sxs-lookup"><span data-stu-id="7cca9-127">string</span></span><br/>  | <span data-ttu-id="7cca9-128">xs:integer</span><span class="sxs-lookup"><span data-stu-id="7cca9-128">xs:integer</span></span><br/>      |
| <span data-ttu-id="7cca9-129">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="7cca9-129">DefaultValue</span></span><br/> | <span data-ttu-id="7cca9-130">string</span><span class="sxs-lookup"><span data-stu-id="7cca9-130">string</span></span><br/>  | <span data-ttu-id="7cca9-131">não definido</span><span class="sxs-lookup"><span data-stu-id="7cca9-131">undefined</span></span><br/>       |
| <span data-ttu-id="7cca9-132">MaxValue</span><span class="sxs-lookup"><span data-stu-id="7cca9-132">MaxValue</span></span><br/>     | <span data-ttu-id="7cca9-133">Número inteiro</span><span class="sxs-lookup"><span data-stu-id="7cca9-133">integer</span></span><br/> | <span data-ttu-id="7cca9-134">100</span><span class="sxs-lookup"><span data-stu-id="7cca9-134">100</span></span><br/>             |
| <span data-ttu-id="7cca9-135">MinValue</span><span class="sxs-lookup"><span data-stu-id="7cca9-135">MinValue</span></span><br/>     | <span data-ttu-id="7cca9-136">integer</span><span class="sxs-lookup"><span data-stu-id="7cca9-136">integer</span></span><br/> | <span data-ttu-id="7cca9-137">0</span><span class="sxs-lookup"><span data-stu-id="7cca9-137">0</span></span><br/>               |
| <span data-ttu-id="7cca9-138">Vários</span><span class="sxs-lookup"><span data-stu-id="7cca9-138">Multiple</span></span><br/>     | <span data-ttu-id="7cca9-139">integer</span><span class="sxs-lookup"><span data-stu-id="7cca9-139">integer</span></span><br/> | <span data-ttu-id="7cca9-140">1</span><span class="sxs-lookup"><span data-stu-id="7cca9-140">1</span></span><br/>               |
| <span data-ttu-id="7cca9-141">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="7cca9-141">Mandatory</span></span><br/>    | <span data-ttu-id="7cca9-142">string</span><span class="sxs-lookup"><span data-stu-id="7cca9-142">string</span></span><br/>  | <span data-ttu-id="7cca9-143">PSK: condicional</span><span class="sxs-lookup"><span data-stu-id="7cca9-143">psk:Conditional</span></span><br/> |
| <span data-ttu-id="7cca9-144">UnitType</span><span class="sxs-lookup"><span data-stu-id="7cca9-144">UnitType</span></span><br/>     | <span data-ttu-id="7cca9-145">string</span><span class="sxs-lookup"><span data-stu-id="7cca9-145">string</span></span><br/>  | <span data-ttu-id="7cca9-146">{1&gt;percent&lt;1}</span><span class="sxs-lookup"><span data-stu-id="7cca9-146">percent</span></span><br/>         |



 

## <a name="related-topics"></a><span data-ttu-id="7cca9-147">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="7cca9-147">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7cca9-148">Especificação de esquema de impressão</span><span class="sxs-lookup"><span data-stu-id="7cca9-148">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




