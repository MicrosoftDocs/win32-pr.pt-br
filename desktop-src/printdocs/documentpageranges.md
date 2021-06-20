---
description: Saiba mais sobre o elemento DocumentPageRanges, que descreve o intervalo de saída do documento em páginas.
ms.assetid: 4cd1b0f8-7f7e-40cc-8d19-d44187822cd1
title: DocumentPageRanges
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0e854736c72b3bff5ba2e4750e0b09e0b87c2c9f
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/19/2021
ms.locfileid: "112409249"
---
# <a name="documentpageranges"></a><span data-ttu-id="cee80-103">DocumentPageRanges</span><span class="sxs-lookup"><span data-stu-id="cee80-103">DocumentPageRanges</span></span>

<span data-ttu-id="cee80-104">Este tópico não é atual.</span><span class="sxs-lookup"><span data-stu-id="cee80-104">This topic is not current.</span></span> <span data-ttu-id="cee80-105">Para obter as informações mais atuais, consulte a [especificação do esquema de impressão](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="cee80-105">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="cee80-106">Descreve o intervalo de saída do documento em páginas.</span><span class="sxs-lookup"><span data-stu-id="cee80-106">Describes the output range of the document in pages.</span></span> <span data-ttu-id="cee80-107">O valor do parâmetro deve estar de acordo com a seguinte estrutura:</span><span class="sxs-lookup"><span data-stu-id="cee80-107">The parameter value must conform to the following structure:</span></span>

-   <span data-ttu-id="cee80-108">PageRangeText: "*PageRange*" ou "*PageRange*,*PageRange*"</span><span class="sxs-lookup"><span data-stu-id="cee80-108">PageRangeText: "*PageRange*" or "*PageRange*,*PageRange*"</span></span>

-   <span data-ttu-id="cee80-109">PageRange: "*PageNumber*" ou "*PageNumber* - *PageNumber*"</span><span class="sxs-lookup"><span data-stu-id="cee80-109">PageRange: "*PageNumber*" or "*PageNumber*-*PageNumber*"</span></span>

-   <span data-ttu-id="cee80-110">PageNumber: 1 a N, em que N é o número de páginas no documento.</span><span class="sxs-lookup"><span data-stu-id="cee80-110">PageNumber: 1 to N, where N is the number of pages in the document.</span></span> <span data-ttu-id="cee80-111">Se *pagenumber* > N, *PageNumber* = N.</span><span class="sxs-lookup"><span data-stu-id="cee80-111">If *PageNumber* > N, then *PageNumber* = N.</span></span>

<span data-ttu-id="cee80-112">O espaço em branco na cadeia de caracteres deve ser ignorado.</span><span class="sxs-lookup"><span data-stu-id="cee80-112">Whitespace in the string should be ignored.</span></span>

-   [<span data-ttu-id="cee80-113">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="cee80-113">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="cee80-114">Conteúdo estrutural</span><span class="sxs-lookup"><span data-stu-id="cee80-114">Structural Content</span></span>](#structural-content)

## <a name="element-information"></a><span data-ttu-id="cee80-115">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="cee80-115">Element Information</span></span>



| <span data-ttu-id="cee80-116">Name</span><span class="sxs-lookup"><span data-stu-id="cee80-116">Name</span></span> | <span data-ttu-id="cee80-117">Valor</span><span class="sxs-lookup"><span data-stu-id="cee80-117">Value</span></span> |
|----------------------------|-------------------------|
| <span data-ttu-id="cee80-118">Tipo de elemento</span><span class="sxs-lookup"><span data-stu-id="cee80-118">Element Type</span></span> <br/>   | <span data-ttu-id="cee80-119">ParameterDef</span><span class="sxs-lookup"><span data-stu-id="cee80-119">ParameterDef</span></span><br/> |
| <span data-ttu-id="cee80-120">Prefixo de escopo</span><span class="sxs-lookup"><span data-stu-id="cee80-120">Scoping Prefix</span></span> <br/> | <span data-ttu-id="cee80-121">Documento</span><span class="sxs-lookup"><span data-stu-id="cee80-121">Document</span></span><br/>     |
| <span data-ttu-id="cee80-122">Observações</span><span class="sxs-lookup"><span data-stu-id="cee80-122">Notes</span></span> <br/>          | <span data-ttu-id="cee80-123">Nenhum</span><span class="sxs-lookup"><span data-stu-id="cee80-123">None</span></span><br/>         |



 

## <a name="structural-content"></a><span data-ttu-id="cee80-124">Conteúdo estrutural</span><span class="sxs-lookup"><span data-stu-id="cee80-124">Structural Content</span></span>

<span data-ttu-id="cee80-125">A estrutura XML desse elemento é:</span><span class="sxs-lookup"><span data-stu-id="cee80-125">The XML structure of this element is:</span></span>

``` syntax
<psf:ParameterDef name="psk:DocumentPageRanges">
  <psf:Property name="psf:DataType">
    <psf:Value xsi:type="xs:string">xs:string</psf:Value>
  </psf:Property>
  <psf:Property name="psf:DefaultValue">
    <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
  </psf:Property>
  <psf:Property name="psf:MaxLength">
    <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
  </psf:Property>
  <psf:Property name="psf:MinLength">
    <psf:Value xsi:type="xs:integer">1</psf:Value>
  </psf:Property>
  <psf:Property name="psf:Mandatory">
    <psf:Value xsi:type="xs:string">psk:Conditional</psf:Value>
  </psf:Property>
  <psf:Property name="psf:UnitType">
    <psf:Value xsi:type="xs:string">characters</psf:Value>
  </psf:Property>
</psf:ParameterDef>
      
```

## <a name="structure-properties"></a><span data-ttu-id="cee80-126">Propriedades da estrutura</span><span class="sxs-lookup"><span data-stu-id="cee80-126">Structure Properties</span></span>

<span data-ttu-id="cee80-127">A tabela a seguir descreve as características das variáveis definidas na estrutura XML.</span><span class="sxs-lookup"><span data-stu-id="cee80-127">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="cee80-128">Propriedade</span><span class="sxs-lookup"><span data-stu-id="cee80-128">Property</span></span>                | <span data-ttu-id="cee80-129">xsi:type</span><span class="sxs-lookup"><span data-stu-id="cee80-129">xsi:type</span></span>           | <span data-ttu-id="cee80-130">Valor</span><span class="sxs-lookup"><span data-stu-id="cee80-130">Value</span></span>                      |
|-------------------------|--------------------|----------------------------|
| <span data-ttu-id="cee80-131">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="cee80-131">DataType</span></span><br/>     | <span data-ttu-id="cee80-132">string</span><span class="sxs-lookup"><span data-stu-id="cee80-132">string</span></span><br/>  | <span data-ttu-id="cee80-133">xs:string</span><span class="sxs-lookup"><span data-stu-id="cee80-133">xs:string</span></span><br/>       |
| <span data-ttu-id="cee80-134">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="cee80-134">DefaultValue</span></span><br/> | <span data-ttu-id="cee80-135">string</span><span class="sxs-lookup"><span data-stu-id="cee80-135">string</span></span><br/>  | <span data-ttu-id="cee80-136">não definido</span><span class="sxs-lookup"><span data-stu-id="cee80-136">undefined</span></span><br/>       |
| <span data-ttu-id="cee80-137">MaxLength</span><span class="sxs-lookup"><span data-stu-id="cee80-137">MaxLength</span></span><br/>    | <span data-ttu-id="cee80-138">Número inteiro</span><span class="sxs-lookup"><span data-stu-id="cee80-138">integer</span></span><br/> | <span data-ttu-id="cee80-139">não definido</span><span class="sxs-lookup"><span data-stu-id="cee80-139">undefined</span></span><br/>       |
| <span data-ttu-id="cee80-140">MinLength</span><span class="sxs-lookup"><span data-stu-id="cee80-140">MinLength</span></span><br/>    | <span data-ttu-id="cee80-141">integer</span><span class="sxs-lookup"><span data-stu-id="cee80-141">integer</span></span><br/> | <span data-ttu-id="cee80-142">1</span><span class="sxs-lookup"><span data-stu-id="cee80-142">1</span></span><br/>               |
| <span data-ttu-id="cee80-143">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="cee80-143">Mandatory</span></span><br/>    | <span data-ttu-id="cee80-144">string</span><span class="sxs-lookup"><span data-stu-id="cee80-144">string</span></span><br/>  | <span data-ttu-id="cee80-145">PSK: condicional</span><span class="sxs-lookup"><span data-stu-id="cee80-145">psk:Conditional</span></span><br/> |
| <span data-ttu-id="cee80-146">UnitType</span><span class="sxs-lookup"><span data-stu-id="cee80-146">UnitType</span></span><br/>     | <span data-ttu-id="cee80-147">string</span><span class="sxs-lookup"><span data-stu-id="cee80-147">string</span></span><br/>  | <span data-ttu-id="cee80-148">characters</span><span class="sxs-lookup"><span data-stu-id="cee80-148">characters</span></span><br/>      |



 

## <a name="related-topics"></a><span data-ttu-id="cee80-149">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="cee80-149">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="cee80-150">Especificação de esquema de impressão</span><span class="sxs-lookup"><span data-stu-id="cee80-150">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




