---
description: Este tópico não é atual. Para obter as informações mais atuais, consulte a especificação do esquema de impressão.
ms.assetid: 4cd1b0f8-7f7e-40cc-8d19-d44187822cd1
title: DocumentPageRanges
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 563ed1746743d3329e0cd31c84c32bb8b407c56c
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/05/2021
ms.locfileid: "104298010"
---
# <a name="documentpageranges"></a><span data-ttu-id="3ad85-104">DocumentPageRanges</span><span class="sxs-lookup"><span data-stu-id="3ad85-104">DocumentPageRanges</span></span>

<span data-ttu-id="3ad85-105">Este tópico não é atual.</span><span class="sxs-lookup"><span data-stu-id="3ad85-105">This topic is not current.</span></span> <span data-ttu-id="3ad85-106">Para obter as informações mais atuais, consulte a [especificação do esquema de impressão](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="3ad85-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="3ad85-107">Descreve o intervalo de saída do documento em páginas.</span><span class="sxs-lookup"><span data-stu-id="3ad85-107">Describes the output range of the document in pages.</span></span> <span data-ttu-id="3ad85-108">O valor do parâmetro deve estar de acordo com a seguinte estrutura:</span><span class="sxs-lookup"><span data-stu-id="3ad85-108">The parameter value must conform to the following structure:</span></span>

-   <span data-ttu-id="3ad85-109">PageRangeText: "*PageRange*" ou "*PageRange*,*PageRange*"</span><span class="sxs-lookup"><span data-stu-id="3ad85-109">PageRangeText: "*PageRange*" or "*PageRange*,*PageRange*"</span></span>

-   <span data-ttu-id="3ad85-110">PageRange: "*PageNumber*" ou "*PageNumber* - *PageNumber*"</span><span class="sxs-lookup"><span data-stu-id="3ad85-110">PageRange: "*PageNumber*" or "*PageNumber*-*PageNumber*"</span></span>

-   <span data-ttu-id="3ad85-111">PageNumber: 1 a N, em que N é o número de páginas no documento.</span><span class="sxs-lookup"><span data-stu-id="3ad85-111">PageNumber: 1 to N, where N is the number of pages in the document.</span></span> <span data-ttu-id="3ad85-112">Se *pagenumber* > N, *PageNumber* = N.</span><span class="sxs-lookup"><span data-stu-id="3ad85-112">If *PageNumber* > N, then *PageNumber* = N.</span></span>

<span data-ttu-id="3ad85-113">O espaço em branco na cadeia de caracteres deve ser ignorado.</span><span class="sxs-lookup"><span data-stu-id="3ad85-113">Whitespace in the string should be ignored.</span></span>

-   [<span data-ttu-id="3ad85-114">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="3ad85-114">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="3ad85-115">Conteúdo estrutural</span><span class="sxs-lookup"><span data-stu-id="3ad85-115">Structural Content</span></span>](#structural-content)

## <a name="element-information"></a><span data-ttu-id="3ad85-116">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="3ad85-116">Element Information</span></span>



| <span data-ttu-id="3ad85-117">Nome</span><span class="sxs-lookup"><span data-stu-id="3ad85-117">Name</span></span>                       |                         |
|----------------------------|-------------------------|
| <span data-ttu-id="3ad85-118">Tipo de elemento</span><span class="sxs-lookup"><span data-stu-id="3ad85-118">Element Type</span></span> <br/>   | <span data-ttu-id="3ad85-119">ParameterDef</span><span class="sxs-lookup"><span data-stu-id="3ad85-119">ParameterDef</span></span><br/> |
| <span data-ttu-id="3ad85-120">Prefixo de escopo</span><span class="sxs-lookup"><span data-stu-id="3ad85-120">Scoping Prefix</span></span> <br/> | <span data-ttu-id="3ad85-121">Documento</span><span class="sxs-lookup"><span data-stu-id="3ad85-121">Document</span></span><br/>     |
| <span data-ttu-id="3ad85-122">Observações</span><span class="sxs-lookup"><span data-stu-id="3ad85-122">Notes</span></span> <br/>          | <span data-ttu-id="3ad85-123">Nenhum</span><span class="sxs-lookup"><span data-stu-id="3ad85-123">None</span></span><br/>         |



 

## <a name="structural-content"></a><span data-ttu-id="3ad85-124">Conteúdo estrutural</span><span class="sxs-lookup"><span data-stu-id="3ad85-124">Structural Content</span></span>

<span data-ttu-id="3ad85-125">A estrutura XML desse elemento é:</span><span class="sxs-lookup"><span data-stu-id="3ad85-125">The XML structure of this element is:</span></span>

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

## <a name="structure-properties"></a><span data-ttu-id="3ad85-126">Propriedades da estrutura</span><span class="sxs-lookup"><span data-stu-id="3ad85-126">Structure Properties</span></span>

<span data-ttu-id="3ad85-127">A tabela a seguir descreve as características das variáveis definidas na estrutura XML.</span><span class="sxs-lookup"><span data-stu-id="3ad85-127">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="3ad85-128">Propriedade</span><span class="sxs-lookup"><span data-stu-id="3ad85-128">Property</span></span>                | <span data-ttu-id="3ad85-129">xsi:type</span><span class="sxs-lookup"><span data-stu-id="3ad85-129">xsi:type</span></span>           | <span data-ttu-id="3ad85-130">Valor</span><span class="sxs-lookup"><span data-stu-id="3ad85-130">Value</span></span>                      |
|-------------------------|--------------------|----------------------------|
| <span data-ttu-id="3ad85-131">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="3ad85-131">DataType</span></span><br/>     | <span data-ttu-id="3ad85-132">string</span><span class="sxs-lookup"><span data-stu-id="3ad85-132">string</span></span><br/>  | <span data-ttu-id="3ad85-133">xs:string</span><span class="sxs-lookup"><span data-stu-id="3ad85-133">xs:string</span></span><br/>       |
| <span data-ttu-id="3ad85-134">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="3ad85-134">DefaultValue</span></span><br/> | <span data-ttu-id="3ad85-135">string</span><span class="sxs-lookup"><span data-stu-id="3ad85-135">string</span></span><br/>  | <span data-ttu-id="3ad85-136">não definido</span><span class="sxs-lookup"><span data-stu-id="3ad85-136">undefined</span></span><br/>       |
| <span data-ttu-id="3ad85-137">MaxLength</span><span class="sxs-lookup"><span data-stu-id="3ad85-137">MaxLength</span></span><br/>    | <span data-ttu-id="3ad85-138">Número inteiro</span><span class="sxs-lookup"><span data-stu-id="3ad85-138">integer</span></span><br/> | <span data-ttu-id="3ad85-139">não definido</span><span class="sxs-lookup"><span data-stu-id="3ad85-139">undefined</span></span><br/>       |
| <span data-ttu-id="3ad85-140">MinLength</span><span class="sxs-lookup"><span data-stu-id="3ad85-140">MinLength</span></span><br/>    | <span data-ttu-id="3ad85-141">integer</span><span class="sxs-lookup"><span data-stu-id="3ad85-141">integer</span></span><br/> | <span data-ttu-id="3ad85-142">1</span><span class="sxs-lookup"><span data-stu-id="3ad85-142">1</span></span><br/>               |
| <span data-ttu-id="3ad85-143">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="3ad85-143">Mandatory</span></span><br/>    | <span data-ttu-id="3ad85-144">string</span><span class="sxs-lookup"><span data-stu-id="3ad85-144">string</span></span><br/>  | <span data-ttu-id="3ad85-145">PSK: condicional</span><span class="sxs-lookup"><span data-stu-id="3ad85-145">psk:Conditional</span></span><br/> |
| <span data-ttu-id="3ad85-146">UnitType</span><span class="sxs-lookup"><span data-stu-id="3ad85-146">UnitType</span></span><br/>     | <span data-ttu-id="3ad85-147">string</span><span class="sxs-lookup"><span data-stu-id="3ad85-147">string</span></span><br/>  | <span data-ttu-id="3ad85-148">characters</span><span class="sxs-lookup"><span data-stu-id="3ad85-148">characters</span></span><br/>      |



 

## <a name="related-topics"></a><span data-ttu-id="3ad85-149">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="3ad85-149">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3ad85-150">Especificação de esquema de impressão</span><span class="sxs-lookup"><span data-stu-id="3ad85-150">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




