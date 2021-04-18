---
description: Este tópico não é atual. Para obter as informações mais atuais, consulte a especificação do esquema de impressão.
ms.assetid: 28ea95a2-e602-4f71-9488-48525e995814
title: PageBlackGenerationProcessingGrayComponentReplacementStart
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7dedf425cd31dd83bce877358c456d1cd16183fa
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/05/2021
ms.locfileid: "105772916"
---
# <a name="pageblackgenerationprocessinggraycomponentreplacementstart"></a><span data-ttu-id="88ab4-104">PageBlackGenerationProcessingGrayComponentReplacementStart</span><span class="sxs-lookup"><span data-stu-id="88ab4-104">PageBlackGenerationProcessingGrayComponentReplacementStart</span></span>

<span data-ttu-id="88ab4-105">Este tópico não é atual.</span><span class="sxs-lookup"><span data-stu-id="88ab4-105">This topic is not current.</span></span> <span data-ttu-id="88ab4-106">Para obter as informações mais atuais, consulte a [especificação do esquema de impressão](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="88ab4-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="88ab4-107">Descreve o ponto no intervalo de "realce para sombra" em que GCR deve iniciar (100% de sombra mais escura).</span><span class="sxs-lookup"><span data-stu-id="88ab4-107">Describes the point in the "highlight to shadow" range where GCR should start (100% darkest shadow).</span></span>

-   [<span data-ttu-id="88ab4-108">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="88ab4-108">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="88ab4-109">Conteúdo da estrutura</span><span class="sxs-lookup"><span data-stu-id="88ab4-109">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="88ab4-110">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="88ab4-110">Element Information</span></span>



| <span data-ttu-id="88ab4-111">Nome</span><span class="sxs-lookup"><span data-stu-id="88ab4-111">Name</span></span>                       |                                                            |
|----------------------------|------------------------------------------------------------|
| <span data-ttu-id="88ab4-112">Tipo de elemento</span><span class="sxs-lookup"><span data-stu-id="88ab4-112">Element Type</span></span> <br/>   | <span data-ttu-id="88ab4-113">ParameterDef</span><span class="sxs-lookup"><span data-stu-id="88ab4-113">ParameterDef</span></span><br/>                                    |
| <span data-ttu-id="88ab4-114">Prefixo de escopo</span><span class="sxs-lookup"><span data-stu-id="88ab4-114">Scoping Prefix</span></span> <br/> | <span data-ttu-id="88ab4-115">?</span><span class="sxs-lookup"><span data-stu-id="88ab4-115">Page</span></span><br/>                                            |
| <span data-ttu-id="88ab4-116">Observações</span><span class="sxs-lookup"><span data-stu-id="88ab4-116">Notes</span></span> <br/>          | <span data-ttu-id="88ab4-117">Vinculado ao elemento PageBlackGenerationProcessing</span><span class="sxs-lookup"><span data-stu-id="88ab4-117">Linked to PageBlackGenerationProcessing element</span></span><br/> |



 

## <a name="structure-content"></a><span data-ttu-id="88ab4-118">Conteúdo da estrutura</span><span class="sxs-lookup"><span data-stu-id="88ab4-118">Structure Content</span></span>

<span data-ttu-id="88ab4-119">A estrutura XML desse elemento é:</span><span class="sxs-lookup"><span data-stu-id="88ab4-119">The XML structure of this element is:</span></span>

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

## <a name="structure-properties"></a><span data-ttu-id="88ab4-120">Propriedades da estrutura</span><span class="sxs-lookup"><span data-stu-id="88ab4-120">Structure Properties</span></span>

<span data-ttu-id="88ab4-121">A tabela a seguir descreve as características das variáveis definidas na estrutura XML.</span><span class="sxs-lookup"><span data-stu-id="88ab4-121">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="88ab4-122">Propriedade</span><span class="sxs-lookup"><span data-stu-id="88ab4-122">Property</span></span>                | <span data-ttu-id="88ab4-123">xsi:type</span><span class="sxs-lookup"><span data-stu-id="88ab4-123">xsi:type</span></span>           | <span data-ttu-id="88ab4-124">Valor</span><span class="sxs-lookup"><span data-stu-id="88ab4-124">Value</span></span>                      |
|-------------------------|--------------------|----------------------------|
| <span data-ttu-id="88ab4-125">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="88ab4-125">DataType</span></span><br/>     | <span data-ttu-id="88ab4-126">string</span><span class="sxs-lookup"><span data-stu-id="88ab4-126">string</span></span><br/>  | <span data-ttu-id="88ab4-127">xs:integer</span><span class="sxs-lookup"><span data-stu-id="88ab4-127">xs:integer</span></span><br/>      |
| <span data-ttu-id="88ab4-128">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="88ab4-128">DefaultValue</span></span><br/> | <span data-ttu-id="88ab4-129">string</span><span class="sxs-lookup"><span data-stu-id="88ab4-129">string</span></span><br/>  | <span data-ttu-id="88ab4-130">não definido</span><span class="sxs-lookup"><span data-stu-id="88ab4-130">undefined</span></span><br/>       |
| <span data-ttu-id="88ab4-131">MaxValue</span><span class="sxs-lookup"><span data-stu-id="88ab4-131">MaxValue</span></span><br/>     | <span data-ttu-id="88ab4-132">Número inteiro</span><span class="sxs-lookup"><span data-stu-id="88ab4-132">integer</span></span><br/> | <span data-ttu-id="88ab4-133">100</span><span class="sxs-lookup"><span data-stu-id="88ab4-133">100</span></span><br/>             |
| <span data-ttu-id="88ab4-134">MinValue</span><span class="sxs-lookup"><span data-stu-id="88ab4-134">MinValue</span></span><br/>     | <span data-ttu-id="88ab4-135">integer</span><span class="sxs-lookup"><span data-stu-id="88ab4-135">integer</span></span><br/> | <span data-ttu-id="88ab4-136">0</span><span class="sxs-lookup"><span data-stu-id="88ab4-136">0</span></span><br/>               |
| <span data-ttu-id="88ab4-137">Vários</span><span class="sxs-lookup"><span data-stu-id="88ab4-137">Multiple</span></span><br/>     | <span data-ttu-id="88ab4-138">integer</span><span class="sxs-lookup"><span data-stu-id="88ab4-138">integer</span></span><br/> | <span data-ttu-id="88ab4-139">1</span><span class="sxs-lookup"><span data-stu-id="88ab4-139">1</span></span><br/>               |
| <span data-ttu-id="88ab4-140">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="88ab4-140">Mandatory</span></span><br/>    | <span data-ttu-id="88ab4-141">string</span><span class="sxs-lookup"><span data-stu-id="88ab4-141">string</span></span><br/>  | <span data-ttu-id="88ab4-142">PSK: condicional</span><span class="sxs-lookup"><span data-stu-id="88ab4-142">psk:Conditional</span></span><br/> |
| <span data-ttu-id="88ab4-143">UnitType</span><span class="sxs-lookup"><span data-stu-id="88ab4-143">UnitType</span></span><br/>     | <span data-ttu-id="88ab4-144">string</span><span class="sxs-lookup"><span data-stu-id="88ab4-144">string</span></span><br/>  | <span data-ttu-id="88ab4-145">{1&gt;percent&lt;1}</span><span class="sxs-lookup"><span data-stu-id="88ab4-145">percent</span></span><br/>         |



 

## <a name="related-topics"></a><span data-ttu-id="88ab4-146">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="88ab4-146">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="88ab4-147">Especificação de esquema de impressão</span><span class="sxs-lookup"><span data-stu-id="88ab4-147">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




