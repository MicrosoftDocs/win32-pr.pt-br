---
description: Saiba mais sobre o elemento PageBlackGenerationProcessingGrayComponentReplacementLevel, que especifica a porcentagem de substituição de componentes cinza.
ms.assetid: e33634bb-5db5-4197-889d-82caf2e74191
title: PageBlackGenerationProcessingGrayComponentReplacementLevel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8499c8521b974d01657c171a99e86e738c82b4e5
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/19/2021
ms.locfileid: "112408479"
---
# <a name="pageblackgenerationprocessinggraycomponentreplacementlevel"></a><span data-ttu-id="92041-103">PageBlackGenerationProcessingGrayComponentReplacementLevel</span><span class="sxs-lookup"><span data-stu-id="92041-103">PageBlackGenerationProcessingGrayComponentReplacementLevel</span></span>

<span data-ttu-id="92041-104">Este tópico não é atual.</span><span class="sxs-lookup"><span data-stu-id="92041-104">This topic is not current.</span></span> <span data-ttu-id="92041-105">Para obter as informações mais atuais, consulte a [especificação do esquema de impressão](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="92041-105">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="92041-106">Especifica a porcentagem de substituição do componente cinza a ser executada.</span><span class="sxs-lookup"><span data-stu-id="92041-106">Specifies the percentage of gray component replacement to perform.</span></span>

-   [<span data-ttu-id="92041-107">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="92041-107">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="92041-108">Conteúdo da estrutura</span><span class="sxs-lookup"><span data-stu-id="92041-108">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="92041-109">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="92041-109">Element Information</span></span>



| <span data-ttu-id="92041-110">Name</span><span class="sxs-lookup"><span data-stu-id="92041-110">Name</span></span> | <span data-ttu-id="92041-111">Valor</span><span class="sxs-lookup"><span data-stu-id="92041-111">Value</span></span> |
|----------------------------|------------------------------------------------------------|
| <span data-ttu-id="92041-112">Tipo de elemento</span><span class="sxs-lookup"><span data-stu-id="92041-112">Element Type</span></span> <br/>   | <span data-ttu-id="92041-113">ParameterDef</span><span class="sxs-lookup"><span data-stu-id="92041-113">ParameterDef</span></span><br/>                                    |
| <span data-ttu-id="92041-114">Prefixo de escopo</span><span class="sxs-lookup"><span data-stu-id="92041-114">Scoping Prefix</span></span> <br/> | <span data-ttu-id="92041-115">?</span><span class="sxs-lookup"><span data-stu-id="92041-115">Page</span></span><br/>                                            |
| <span data-ttu-id="92041-116">Observações</span><span class="sxs-lookup"><span data-stu-id="92041-116">Notes</span></span> <br/>          | <span data-ttu-id="92041-117">Vinculado ao elemento PageBlackGenerationProcessing</span><span class="sxs-lookup"><span data-stu-id="92041-117">Linked to PageBlackGenerationProcessing element</span></span><br/> |



 

## <a name="structure-content"></a><span data-ttu-id="92041-118">Conteúdo da estrutura</span><span class="sxs-lookup"><span data-stu-id="92041-118">Structure Content</span></span>

<span data-ttu-id="92041-119">A estrutura XML desse elemento é:</span><span class="sxs-lookup"><span data-stu-id="92041-119">The XML structure of this element is:</span></span>

``` syntax
<psf:ParameterDef name="psk:PageBlackGenerationProcessingGrayComponentReplacementLevel">
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

## <a name="structure-properties"></a><span data-ttu-id="92041-120">Propriedades da estrutura</span><span class="sxs-lookup"><span data-stu-id="92041-120">Structure Properties</span></span>

<span data-ttu-id="92041-121">A tabela a seguir descreve as características das variáveis definidas na estrutura XML.</span><span class="sxs-lookup"><span data-stu-id="92041-121">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="92041-122">Propriedade</span><span class="sxs-lookup"><span data-stu-id="92041-122">Property</span></span>                | <span data-ttu-id="92041-123">xsi:type</span><span class="sxs-lookup"><span data-stu-id="92041-123">xsi:type</span></span>           | <span data-ttu-id="92041-124">Valor</span><span class="sxs-lookup"><span data-stu-id="92041-124">Value</span></span>                      |
|-------------------------|--------------------|----------------------------|
| <span data-ttu-id="92041-125">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="92041-125">DataType</span></span><br/>     | <span data-ttu-id="92041-126">string</span><span class="sxs-lookup"><span data-stu-id="92041-126">string</span></span><br/>  | <span data-ttu-id="92041-127">xs:integer</span><span class="sxs-lookup"><span data-stu-id="92041-127">xs:integer</span></span><br/>      |
| <span data-ttu-id="92041-128">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="92041-128">DefaultValue</span></span><br/> | <span data-ttu-id="92041-129">string</span><span class="sxs-lookup"><span data-stu-id="92041-129">string</span></span><br/>  | <span data-ttu-id="92041-130">não definido</span><span class="sxs-lookup"><span data-stu-id="92041-130">undefined</span></span><br/>       |
| <span data-ttu-id="92041-131">MaxValue</span><span class="sxs-lookup"><span data-stu-id="92041-131">MaxValue</span></span><br/>     | <span data-ttu-id="92041-132">Número inteiro</span><span class="sxs-lookup"><span data-stu-id="92041-132">integer</span></span><br/> | <span data-ttu-id="92041-133">100</span><span class="sxs-lookup"><span data-stu-id="92041-133">100</span></span><br/>             |
| <span data-ttu-id="92041-134">MinValue</span><span class="sxs-lookup"><span data-stu-id="92041-134">MinValue</span></span><br/>     | <span data-ttu-id="92041-135">inteiro</span><span class="sxs-lookup"><span data-stu-id="92041-135">integer</span></span><br/> | <span data-ttu-id="92041-136">0</span><span class="sxs-lookup"><span data-stu-id="92041-136">0</span></span><br/>               |
| <span data-ttu-id="92041-137">Vários</span><span class="sxs-lookup"><span data-stu-id="92041-137">Multiple</span></span><br/>     | <span data-ttu-id="92041-138">integer</span><span class="sxs-lookup"><span data-stu-id="92041-138">integer</span></span><br/> | <span data-ttu-id="92041-139">1</span><span class="sxs-lookup"><span data-stu-id="92041-139">1</span></span><br/>               |
| <span data-ttu-id="92041-140">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="92041-140">Mandatory</span></span><br/>    | <span data-ttu-id="92041-141">string</span><span class="sxs-lookup"><span data-stu-id="92041-141">string</span></span><br/>  | <span data-ttu-id="92041-142">PSK: condicional</span><span class="sxs-lookup"><span data-stu-id="92041-142">psk:Conditional</span></span><br/> |
| <span data-ttu-id="92041-143">UnitType</span><span class="sxs-lookup"><span data-stu-id="92041-143">UnitType</span></span><br/>     | <span data-ttu-id="92041-144">string</span><span class="sxs-lookup"><span data-stu-id="92041-144">string</span></span><br/>  | <span data-ttu-id="92041-145">{1&gt;percent&lt;1}</span><span class="sxs-lookup"><span data-stu-id="92041-145">percent</span></span><br/>         |



 

## <a name="related-topics"></a><span data-ttu-id="92041-146">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="92041-146">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="92041-147">Especificação de esquema de impressão</span><span class="sxs-lookup"><span data-stu-id="92041-147">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




