---
title: PageBlackGenerationProcessingUnderColorAdditionStart
description: Este tópico não é atual. Para obter as informações mais atuais, consulte a especificação do esquema de impressão.
ms.assetid: 6c2a7bb5-436d-40ed-a855-242a6a04bc16
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 595bc3e4514b1a2e8a4d302005b97e2625a560e2
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/26/2021
ms.locfileid: "107999183"
---
# <a name="pageblackgenerationprocessingundercoloradditionstart"></a><span data-ttu-id="afad8-104">PageBlackGenerationProcessingUnderColorAdditionStart</span><span class="sxs-lookup"><span data-stu-id="afad8-104">PageBlackGenerationProcessingUnderColorAdditionStart</span></span>

<span data-ttu-id="afad8-105">Este tópico não é atual.</span><span class="sxs-lookup"><span data-stu-id="afad8-105">This topic is not current.</span></span> <span data-ttu-id="afad8-106">Para obter as informações mais atuais, consulte a [especificação do esquema de impressão](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="afad8-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="afad8-107">Descreve o nível de sombra abaixo do qual UCA será aplicado.</span><span class="sxs-lookup"><span data-stu-id="afad8-107">Describes the shadow level below which UCA will be applied.</span></span>

-   [<span data-ttu-id="afad8-108">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="afad8-108">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="afad8-109">Conteúdo da estrutura</span><span class="sxs-lookup"><span data-stu-id="afad8-109">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="afad8-110">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="afad8-110">Element Information</span></span>



| <span data-ttu-id="afad8-111">Nome</span><span class="sxs-lookup"><span data-stu-id="afad8-111">Name</span></span> | <span data-ttu-id="afad8-112">Valor</span><span class="sxs-lookup"><span data-stu-id="afad8-112">Value</span></span> |
|----------------------------|------------------------------------------------------------|
| <span data-ttu-id="afad8-113">Tipo de elemento</span><span class="sxs-lookup"><span data-stu-id="afad8-113">Element Type</span></span> <br/>   | <span data-ttu-id="afad8-114">ParameterDef</span><span class="sxs-lookup"><span data-stu-id="afad8-114">ParameterDef</span></span><br/>                                    |
| <span data-ttu-id="afad8-115">Prefixo de escopo</span><span class="sxs-lookup"><span data-stu-id="afad8-115">Scoping Prefix</span></span> <br/> | <span data-ttu-id="afad8-116">?</span><span class="sxs-lookup"><span data-stu-id="afad8-116">Page</span></span><br/>                                            |
| <span data-ttu-id="afad8-117">Observações</span><span class="sxs-lookup"><span data-stu-id="afad8-117">Notes</span></span> <br/>          | <span data-ttu-id="afad8-118">Vinculado ao elemento PageBlackGenerationProcessing</span><span class="sxs-lookup"><span data-stu-id="afad8-118">Linked to PageBlackGenerationProcessing element</span></span><br/> |



 

## <a name="structure-content"></a><span data-ttu-id="afad8-119">Conteúdo da estrutura</span><span class="sxs-lookup"><span data-stu-id="afad8-119">Structure Content</span></span>

<span data-ttu-id="afad8-120">A estrutura XML desse elemento é:</span><span class="sxs-lookup"><span data-stu-id="afad8-120">The XML structure of this element is:</span></span>

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

## <a name="structure-properties"></a><span data-ttu-id="afad8-121">Propriedades da estrutura</span><span class="sxs-lookup"><span data-stu-id="afad8-121">Structure Properties</span></span>

<span data-ttu-id="afad8-122">A tabela a seguir descreve as características das variáveis definidas na estrutura XML.</span><span class="sxs-lookup"><span data-stu-id="afad8-122">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="afad8-123">Propriedade</span><span class="sxs-lookup"><span data-stu-id="afad8-123">Property</span></span>                | <span data-ttu-id="afad8-124">xsi:type</span><span class="sxs-lookup"><span data-stu-id="afad8-124">xsi:type</span></span>           | <span data-ttu-id="afad8-125">Valor</span><span class="sxs-lookup"><span data-stu-id="afad8-125">Value</span></span>                      |
|-------------------------|--------------------|----------------------------|
| <span data-ttu-id="afad8-126">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="afad8-126">DataType</span></span><br/>     | <span data-ttu-id="afad8-127">string</span><span class="sxs-lookup"><span data-stu-id="afad8-127">string</span></span><br/>  | <span data-ttu-id="afad8-128">xs:integer</span><span class="sxs-lookup"><span data-stu-id="afad8-128">xs:integer</span></span><br/>      |
| <span data-ttu-id="afad8-129">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="afad8-129">DefaultValue</span></span><br/> | <span data-ttu-id="afad8-130">string</span><span class="sxs-lookup"><span data-stu-id="afad8-130">string</span></span><br/>  | <span data-ttu-id="afad8-131">não definido</span><span class="sxs-lookup"><span data-stu-id="afad8-131">undefined</span></span><br/>       |
| <span data-ttu-id="afad8-132">MaxValue</span><span class="sxs-lookup"><span data-stu-id="afad8-132">MaxValue</span></span><br/>     | <span data-ttu-id="afad8-133">Número inteiro</span><span class="sxs-lookup"><span data-stu-id="afad8-133">integer</span></span><br/> | <span data-ttu-id="afad8-134">100</span><span class="sxs-lookup"><span data-stu-id="afad8-134">100</span></span><br/>             |
| <span data-ttu-id="afad8-135">MinValue</span><span class="sxs-lookup"><span data-stu-id="afad8-135">MinValue</span></span><br/>     | <span data-ttu-id="afad8-136">integer</span><span class="sxs-lookup"><span data-stu-id="afad8-136">integer</span></span><br/> | <span data-ttu-id="afad8-137">0</span><span class="sxs-lookup"><span data-stu-id="afad8-137">0</span></span><br/>               |
| <span data-ttu-id="afad8-138">Vários</span><span class="sxs-lookup"><span data-stu-id="afad8-138">Multiple</span></span><br/>     | <span data-ttu-id="afad8-139">integer</span><span class="sxs-lookup"><span data-stu-id="afad8-139">integer</span></span><br/> | <span data-ttu-id="afad8-140">1</span><span class="sxs-lookup"><span data-stu-id="afad8-140">1</span></span><br/>               |
| <span data-ttu-id="afad8-141">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="afad8-141">Mandatory</span></span><br/>    | <span data-ttu-id="afad8-142">string</span><span class="sxs-lookup"><span data-stu-id="afad8-142">string</span></span><br/>  | <span data-ttu-id="afad8-143">PSK: condicional</span><span class="sxs-lookup"><span data-stu-id="afad8-143">psk:Conditional</span></span><br/> |
| <span data-ttu-id="afad8-144">UnitType</span><span class="sxs-lookup"><span data-stu-id="afad8-144">UnitType</span></span><br/>     | <span data-ttu-id="afad8-145">string</span><span class="sxs-lookup"><span data-stu-id="afad8-145">string</span></span><br/>  | <span data-ttu-id="afad8-146">{1&gt;percent&lt;1}</span><span class="sxs-lookup"><span data-stu-id="afad8-146">percent</span></span><br/>         |



 

## <a name="related-topics"></a><span data-ttu-id="afad8-147">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="afad8-147">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="afad8-148">Especificação de esquema de impressão</span><span class="sxs-lookup"><span data-stu-id="afad8-148">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




