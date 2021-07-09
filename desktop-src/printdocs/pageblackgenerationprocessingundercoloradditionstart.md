---
title: PageBlackGenerationProcessingUnderColorAdditionStart
description: Revise o parâmetro PageBlackGenerationProcessingUnderColorAdditionStart. Este tópico não é atual. Para obter informações atuais, consulte a Especificação de Esquema de Impressão.
ms.assetid: 6c2a7bb5-436d-40ed-a855-242a6a04bc16
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 11bdbd970f30a7d573b7c803ea447e4ac3e94ca2
ms.sourcegitcommit: 998d50f6def8a25850fc113fc8a2df903c829c5e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/09/2021
ms.locfileid: "113549344"
---
# <a name="pageblackgenerationprocessingundercoloradditionstart"></a><span data-ttu-id="c99a0-105">PageBlackGenerationProcessingUnderColorAdditionStart</span><span class="sxs-lookup"><span data-stu-id="c99a0-105">PageBlackGenerationProcessingUnderColorAdditionStart</span></span>

<span data-ttu-id="c99a0-106">Este tópico não é atual.</span><span class="sxs-lookup"><span data-stu-id="c99a0-106">This topic is not current.</span></span> <span data-ttu-id="c99a0-107">Para obter as informações mais atuais, consulte a [Especificação de Esquema de Impressão](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="c99a0-107">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="c99a0-108">Descreve o nível de sombra abaixo do qual o LTDA será aplicado.</span><span class="sxs-lookup"><span data-stu-id="c99a0-108">Describes the shadow level below which UCA will be applied.</span></span>

-   [<span data-ttu-id="c99a0-109">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="c99a0-109">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="c99a0-110">Conteúdo da estrutura</span><span class="sxs-lookup"><span data-stu-id="c99a0-110">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="c99a0-111">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="c99a0-111">Element Information</span></span>



| <span data-ttu-id="c99a0-112">Nome</span><span class="sxs-lookup"><span data-stu-id="c99a0-112">Name</span></span> | <span data-ttu-id="c99a0-113">Valor</span><span class="sxs-lookup"><span data-stu-id="c99a0-113">Value</span></span> |
|----------------------------|------------------------------------------------------------|
| <span data-ttu-id="c99a0-114">Tipo de elemento</span><span class="sxs-lookup"><span data-stu-id="c99a0-114">Element Type</span></span> <br/>   | <span data-ttu-id="c99a0-115">ParameterDef</span><span class="sxs-lookup"><span data-stu-id="c99a0-115">ParameterDef</span></span><br/>                                    |
| <span data-ttu-id="c99a0-116">Prefixo de definição de scoping</span><span class="sxs-lookup"><span data-stu-id="c99a0-116">Scoping Prefix</span></span> <br/> | <span data-ttu-id="c99a0-117">Página</span><span class="sxs-lookup"><span data-stu-id="c99a0-117">Page</span></span><br/>                                            |
| <span data-ttu-id="c99a0-118">Observações</span><span class="sxs-lookup"><span data-stu-id="c99a0-118">Notes</span></span> <br/>          | <span data-ttu-id="c99a0-119">Vinculado ao elemento PageBlackGenerationProcessing</span><span class="sxs-lookup"><span data-stu-id="c99a0-119">Linked to PageBlackGenerationProcessing element</span></span><br/> |



 

## <a name="structure-content"></a><span data-ttu-id="c99a0-120">Conteúdo da estrutura</span><span class="sxs-lookup"><span data-stu-id="c99a0-120">Structure Content</span></span>

<span data-ttu-id="c99a0-121">A estrutura XML desse elemento é:</span><span class="sxs-lookup"><span data-stu-id="c99a0-121">The XML structure of this element is:</span></span>

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

## <a name="structure-properties"></a><span data-ttu-id="c99a0-122">Propriedades da estrutura</span><span class="sxs-lookup"><span data-stu-id="c99a0-122">Structure Properties</span></span>

<span data-ttu-id="c99a0-123">A tabela a seguir descreve as características das variáveis definidas na estrutura XML.</span><span class="sxs-lookup"><span data-stu-id="c99a0-123">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="c99a0-124">Propriedade</span><span class="sxs-lookup"><span data-stu-id="c99a0-124">Property</span></span>                | <span data-ttu-id="c99a0-125">xsi:type</span><span class="sxs-lookup"><span data-stu-id="c99a0-125">xsi:type</span></span>           | <span data-ttu-id="c99a0-126">Valor</span><span class="sxs-lookup"><span data-stu-id="c99a0-126">Value</span></span>                      |
|-------------------------|--------------------|----------------------------|
| <span data-ttu-id="c99a0-127">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="c99a0-127">DataType</span></span><br/>     | <span data-ttu-id="c99a0-128">string</span><span class="sxs-lookup"><span data-stu-id="c99a0-128">string</span></span><br/>  | <span data-ttu-id="c99a0-129">xs:integer</span><span class="sxs-lookup"><span data-stu-id="c99a0-129">xs:integer</span></span><br/>      |
| <span data-ttu-id="c99a0-130">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="c99a0-130">DefaultValue</span></span><br/> | <span data-ttu-id="c99a0-131">string</span><span class="sxs-lookup"><span data-stu-id="c99a0-131">string</span></span><br/>  | <span data-ttu-id="c99a0-132">não definido</span><span class="sxs-lookup"><span data-stu-id="c99a0-132">undefined</span></span><br/>       |
| <span data-ttu-id="c99a0-133">MaxValue</span><span class="sxs-lookup"><span data-stu-id="c99a0-133">MaxValue</span></span><br/>     | <span data-ttu-id="c99a0-134">Número inteiro</span><span class="sxs-lookup"><span data-stu-id="c99a0-134">integer</span></span><br/> | <span data-ttu-id="c99a0-135">100</span><span class="sxs-lookup"><span data-stu-id="c99a0-135">100</span></span><br/>             |
| <span data-ttu-id="c99a0-136">Minvalue</span><span class="sxs-lookup"><span data-stu-id="c99a0-136">MinValue</span></span><br/>     | <span data-ttu-id="c99a0-137">inteiro</span><span class="sxs-lookup"><span data-stu-id="c99a0-137">integer</span></span><br/> | <span data-ttu-id="c99a0-138">0</span><span class="sxs-lookup"><span data-stu-id="c99a0-138">0</span></span><br/>               |
| <span data-ttu-id="c99a0-139">Vários</span><span class="sxs-lookup"><span data-stu-id="c99a0-139">Multiple</span></span><br/>     | <span data-ttu-id="c99a0-140">integer</span><span class="sxs-lookup"><span data-stu-id="c99a0-140">integer</span></span><br/> | <span data-ttu-id="c99a0-141">1</span><span class="sxs-lookup"><span data-stu-id="c99a0-141">1</span></span><br/>               |
| <span data-ttu-id="c99a0-142">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="c99a0-142">Mandatory</span></span><br/>    | <span data-ttu-id="c99a0-143">string</span><span class="sxs-lookup"><span data-stu-id="c99a0-143">string</span></span><br/>  | <span data-ttu-id="c99a0-144">psk:Conditional</span><span class="sxs-lookup"><span data-stu-id="c99a0-144">psk:Conditional</span></span><br/> |
| <span data-ttu-id="c99a0-145">Unittype</span><span class="sxs-lookup"><span data-stu-id="c99a0-145">UnitType</span></span><br/>     | <span data-ttu-id="c99a0-146">string</span><span class="sxs-lookup"><span data-stu-id="c99a0-146">string</span></span><br/>  | <span data-ttu-id="c99a0-147">{1&gt;percent&lt;1}</span><span class="sxs-lookup"><span data-stu-id="c99a0-147">percent</span></span><br/>         |



 

## <a name="related-topics"></a><span data-ttu-id="c99a0-148">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="c99a0-148">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c99a0-149">Especificação de esquema de impressão</span><span class="sxs-lookup"><span data-stu-id="c99a0-149">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




