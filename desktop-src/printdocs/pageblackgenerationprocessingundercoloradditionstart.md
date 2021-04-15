---
title: PageBlackGenerationProcessingUnderColorAdditionStart
description: Este tópico não é atual. Para obter as informações mais atuais, consulte a especificação do esquema de impressão.
ms.assetid: 6c2a7bb5-436d-40ed-a855-242a6a04bc16
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 41d44dbc63632479c66686cea50b781abf715c76
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/05/2021
ms.locfileid: "104370834"
---
# <a name="pageblackgenerationprocessingundercoloradditionstart"></a><span data-ttu-id="24e59-104">PageBlackGenerationProcessingUnderColorAdditionStart</span><span class="sxs-lookup"><span data-stu-id="24e59-104">PageBlackGenerationProcessingUnderColorAdditionStart</span></span>

<span data-ttu-id="24e59-105">Este tópico não é atual.</span><span class="sxs-lookup"><span data-stu-id="24e59-105">This topic is not current.</span></span> <span data-ttu-id="24e59-106">Para obter as informações mais atuais, consulte a [especificação do esquema de impressão](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="24e59-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="24e59-107">Descreve o nível de sombra abaixo do qual UCA será aplicado.</span><span class="sxs-lookup"><span data-stu-id="24e59-107">Describes the shadow level below which UCA will be applied.</span></span>

-   [<span data-ttu-id="24e59-108">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="24e59-108">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="24e59-109">Conteúdo da estrutura</span><span class="sxs-lookup"><span data-stu-id="24e59-109">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="24e59-110">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="24e59-110">Element Information</span></span>



| <span data-ttu-id="24e59-111">Nome</span><span class="sxs-lookup"><span data-stu-id="24e59-111">Name</span></span>                       |                                                            |
|----------------------------|------------------------------------------------------------|
| <span data-ttu-id="24e59-112">Tipo de elemento</span><span class="sxs-lookup"><span data-stu-id="24e59-112">Element Type</span></span> <br/>   | <span data-ttu-id="24e59-113">ParameterDef</span><span class="sxs-lookup"><span data-stu-id="24e59-113">ParameterDef</span></span><br/>                                    |
| <span data-ttu-id="24e59-114">Prefixo de escopo</span><span class="sxs-lookup"><span data-stu-id="24e59-114">Scoping Prefix</span></span> <br/> | <span data-ttu-id="24e59-115">?</span><span class="sxs-lookup"><span data-stu-id="24e59-115">Page</span></span><br/>                                            |
| <span data-ttu-id="24e59-116">Observações</span><span class="sxs-lookup"><span data-stu-id="24e59-116">Notes</span></span> <br/>          | <span data-ttu-id="24e59-117">Vinculado ao elemento PageBlackGenerationProcessing</span><span class="sxs-lookup"><span data-stu-id="24e59-117">Linked to PageBlackGenerationProcessing element</span></span><br/> |



 

## <a name="structure-content"></a><span data-ttu-id="24e59-118">Conteúdo da estrutura</span><span class="sxs-lookup"><span data-stu-id="24e59-118">Structure Content</span></span>

<span data-ttu-id="24e59-119">A estrutura XML desse elemento é:</span><span class="sxs-lookup"><span data-stu-id="24e59-119">The XML structure of this element is:</span></span>

``` syntax
<psf:ParameterDef name="psk:PageBlackGenerationProcessingUnderColorAdditionStart">
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

## <a name="structure-properties"></a><span data-ttu-id="24e59-120">Propriedades da estrutura</span><span class="sxs-lookup"><span data-stu-id="24e59-120">Structure Properties</span></span>

<span data-ttu-id="24e59-121">A tabela a seguir descreve as características das variáveis definidas na estrutura XML.</span><span class="sxs-lookup"><span data-stu-id="24e59-121">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="24e59-122">Propriedade</span><span class="sxs-lookup"><span data-stu-id="24e59-122">Property</span></span>                | <span data-ttu-id="24e59-123">xsi:type</span><span class="sxs-lookup"><span data-stu-id="24e59-123">xsi:type</span></span>           | <span data-ttu-id="24e59-124">Valor</span><span class="sxs-lookup"><span data-stu-id="24e59-124">Value</span></span>                      |
|-------------------------|--------------------|----------------------------|
| <span data-ttu-id="24e59-125">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="24e59-125">DataType</span></span><br/>     | <span data-ttu-id="24e59-126">string</span><span class="sxs-lookup"><span data-stu-id="24e59-126">string</span></span><br/>  | <span data-ttu-id="24e59-127">xs:integer</span><span class="sxs-lookup"><span data-stu-id="24e59-127">xs:integer</span></span><br/>      |
| <span data-ttu-id="24e59-128">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="24e59-128">DefaultValue</span></span><br/> | <span data-ttu-id="24e59-129">string</span><span class="sxs-lookup"><span data-stu-id="24e59-129">string</span></span><br/>  | <span data-ttu-id="24e59-130">não definido</span><span class="sxs-lookup"><span data-stu-id="24e59-130">undefined</span></span><br/>       |
| <span data-ttu-id="24e59-131">MaxValue</span><span class="sxs-lookup"><span data-stu-id="24e59-131">MaxValue</span></span><br/>     | <span data-ttu-id="24e59-132">Número inteiro</span><span class="sxs-lookup"><span data-stu-id="24e59-132">integer</span></span><br/> | <span data-ttu-id="24e59-133">100</span><span class="sxs-lookup"><span data-stu-id="24e59-133">100</span></span><br/>             |
| <span data-ttu-id="24e59-134">MinValue</span><span class="sxs-lookup"><span data-stu-id="24e59-134">MinValue</span></span><br/>     | <span data-ttu-id="24e59-135">integer</span><span class="sxs-lookup"><span data-stu-id="24e59-135">integer</span></span><br/> | <span data-ttu-id="24e59-136">0</span><span class="sxs-lookup"><span data-stu-id="24e59-136">0</span></span><br/>               |
| <span data-ttu-id="24e59-137">Vários</span><span class="sxs-lookup"><span data-stu-id="24e59-137">Multiple</span></span><br/>     | <span data-ttu-id="24e59-138">integer</span><span class="sxs-lookup"><span data-stu-id="24e59-138">integer</span></span><br/> | <span data-ttu-id="24e59-139">1</span><span class="sxs-lookup"><span data-stu-id="24e59-139">1</span></span><br/>               |
| <span data-ttu-id="24e59-140">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="24e59-140">Mandatory</span></span><br/>    | <span data-ttu-id="24e59-141">string</span><span class="sxs-lookup"><span data-stu-id="24e59-141">string</span></span><br/>  | <span data-ttu-id="24e59-142">PSK: condicional</span><span class="sxs-lookup"><span data-stu-id="24e59-142">psk:Conditional</span></span><br/> |
| <span data-ttu-id="24e59-143">UnitType</span><span class="sxs-lookup"><span data-stu-id="24e59-143">UnitType</span></span><br/>     | <span data-ttu-id="24e59-144">string</span><span class="sxs-lookup"><span data-stu-id="24e59-144">string</span></span><br/>  | <span data-ttu-id="24e59-145">{1&gt;percent&lt;1}</span><span class="sxs-lookup"><span data-stu-id="24e59-145">percent</span></span><br/>         |



 

## <a name="related-topics"></a><span data-ttu-id="24e59-146">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="24e59-146">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="24e59-147">Especificação de esquema de impressão</span><span class="sxs-lookup"><span data-stu-id="24e59-147">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




