---
description: Este tópico não é atual. Para obter as informações mais atuais, consulte a especificação do esquema de impressão.
ms.assetid: 7ccd02c2-7cec-4d9d-83c1-512f25f4045c
title: PageBlackGenerationProcessingTotalInkCoverageLimit
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 29918bfe48d1547a3c61b8d79425b36368f6d249
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/26/2021
ms.locfileid: "107993873"
---
# <a name="pageblackgenerationprocessingtotalinkcoveragelimit"></a><span data-ttu-id="0e209-104">PageBlackGenerationProcessingTotalInkCoverageLimit</span><span class="sxs-lookup"><span data-stu-id="0e209-104">PageBlackGenerationProcessingTotalInkCoverageLimit</span></span>

<span data-ttu-id="0e209-105">Este tópico não é atual.</span><span class="sxs-lookup"><span data-stu-id="0e209-105">This topic is not current.</span></span> <span data-ttu-id="0e209-106">Para obter as informações mais atuais, consulte a [especificação do esquema de impressão](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="0e209-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="0e209-107">Especifica a soma máxima permitida da cobertura de quatro tinta em qualquer lugar em uma imagem.</span><span class="sxs-lookup"><span data-stu-id="0e209-107">Specifies the maximum allowed sum of the four ink coverage anywhere in an image.</span></span>

-   [<span data-ttu-id="0e209-108">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="0e209-108">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="0e209-109">Conteúdo da estrutura</span><span class="sxs-lookup"><span data-stu-id="0e209-109">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="0e209-110">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="0e209-110">Element Information</span></span>



| <span data-ttu-id="0e209-111">Nome</span><span class="sxs-lookup"><span data-stu-id="0e209-111">Name</span></span> | <span data-ttu-id="0e209-112">Valor</span><span class="sxs-lookup"><span data-stu-id="0e209-112">Value</span></span> |
|----------------------------|------------------------------------------------------------|
| <span data-ttu-id="0e209-113">Tipo de elemento</span><span class="sxs-lookup"><span data-stu-id="0e209-113">Element Type</span></span> <br/>   | <span data-ttu-id="0e209-114">ParameterDef</span><span class="sxs-lookup"><span data-stu-id="0e209-114">ParameterDef</span></span><br/>                                    |
| <span data-ttu-id="0e209-115">Prefixo de escopo</span><span class="sxs-lookup"><span data-stu-id="0e209-115">Scoping Prefix</span></span> <br/> | <span data-ttu-id="0e209-116">?</span><span class="sxs-lookup"><span data-stu-id="0e209-116">Page</span></span><br/>                                            |
| <span data-ttu-id="0e209-117">Observações</span><span class="sxs-lookup"><span data-stu-id="0e209-117">Notes</span></span> <br/>          | <span data-ttu-id="0e209-118">Vinculado ao elemento PageBlackGenerationProcessing</span><span class="sxs-lookup"><span data-stu-id="0e209-118">Linked to PageBlackGenerationProcessing element</span></span><br/> |



 

## <a name="structure-content"></a><span data-ttu-id="0e209-119">Conteúdo da estrutura</span><span class="sxs-lookup"><span data-stu-id="0e209-119">Structure Content</span></span>

<span data-ttu-id="0e209-120">A estrutura XML desse elemento é:</span><span class="sxs-lookup"><span data-stu-id="0e209-120">The XML structure of this element is:</span></span>

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

## <a name="structure-properties"></a><span data-ttu-id="0e209-121">Propriedades da estrutura</span><span class="sxs-lookup"><span data-stu-id="0e209-121">Structure Properties</span></span>

<span data-ttu-id="0e209-122">A tabela a seguir descreve as características das variáveis definidas na estrutura XML.</span><span class="sxs-lookup"><span data-stu-id="0e209-122">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="0e209-123">Propriedade</span><span class="sxs-lookup"><span data-stu-id="0e209-123">Property</span></span>                | <span data-ttu-id="0e209-124">xsi:type</span><span class="sxs-lookup"><span data-stu-id="0e209-124">xsi:type</span></span>           | <span data-ttu-id="0e209-125">Valor</span><span class="sxs-lookup"><span data-stu-id="0e209-125">Value</span></span>                      |
|-------------------------|--------------------|----------------------------|
| <span data-ttu-id="0e209-126">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="0e209-126">DataType</span></span><br/>     | <span data-ttu-id="0e209-127">string</span><span class="sxs-lookup"><span data-stu-id="0e209-127">string</span></span><br/>  | <span data-ttu-id="0e209-128">xs:integer</span><span class="sxs-lookup"><span data-stu-id="0e209-128">xs:integer</span></span><br/>      |
| <span data-ttu-id="0e209-129">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="0e209-129">DefaultValue</span></span><br/> | <span data-ttu-id="0e209-130">string</span><span class="sxs-lookup"><span data-stu-id="0e209-130">string</span></span><br/>  | <span data-ttu-id="0e209-131">não definido</span><span class="sxs-lookup"><span data-stu-id="0e209-131">undefined</span></span><br/>       |
| <span data-ttu-id="0e209-132">MaxValue</span><span class="sxs-lookup"><span data-stu-id="0e209-132">MaxValue</span></span><br/>     | <span data-ttu-id="0e209-133">Número inteiro</span><span class="sxs-lookup"><span data-stu-id="0e209-133">integer</span></span><br/> | <span data-ttu-id="0e209-134">400</span><span class="sxs-lookup"><span data-stu-id="0e209-134">400</span></span><br/>             |
| <span data-ttu-id="0e209-135">MinValue</span><span class="sxs-lookup"><span data-stu-id="0e209-135">MinValue</span></span><br/>     | <span data-ttu-id="0e209-136">Número inteiro</span><span class="sxs-lookup"><span data-stu-id="0e209-136">integer</span></span><br/> | <span data-ttu-id="0e209-137">200</span><span class="sxs-lookup"><span data-stu-id="0e209-137">200</span></span><br/>             |
| <span data-ttu-id="0e209-138">Vários</span><span class="sxs-lookup"><span data-stu-id="0e209-138">Multiple</span></span><br/>     | <span data-ttu-id="0e209-139">integer</span><span class="sxs-lookup"><span data-stu-id="0e209-139">integer</span></span><br/> | <span data-ttu-id="0e209-140">1</span><span class="sxs-lookup"><span data-stu-id="0e209-140">1</span></span><br/>               |
| <span data-ttu-id="0e209-141">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="0e209-141">Mandatory</span></span><br/>    | <span data-ttu-id="0e209-142">string</span><span class="sxs-lookup"><span data-stu-id="0e209-142">string</span></span><br/>  | <span data-ttu-id="0e209-143">PSK: condicional</span><span class="sxs-lookup"><span data-stu-id="0e209-143">psk:Conditional</span></span><br/> |
| <span data-ttu-id="0e209-144">UnitType</span><span class="sxs-lookup"><span data-stu-id="0e209-144">UnitType</span></span><br/>     | <span data-ttu-id="0e209-145">string</span><span class="sxs-lookup"><span data-stu-id="0e209-145">string</span></span><br/>  | <span data-ttu-id="0e209-146">{1&gt;percent&lt;1}</span><span class="sxs-lookup"><span data-stu-id="0e209-146">percent</span></span><br/>         |



 

## <a name="related-topics"></a><span data-ttu-id="0e209-147">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="0e209-147">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0e209-148">Especificação de esquema de impressão</span><span class="sxs-lookup"><span data-stu-id="0e209-148">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




