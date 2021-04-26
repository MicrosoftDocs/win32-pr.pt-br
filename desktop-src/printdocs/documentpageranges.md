---
description: Este tópico não é atual. Para obter as informações mais atuais, consulte a especificação do esquema de impressão.
ms.assetid: 4cd1b0f8-7f7e-40cc-8d19-d44187822cd1
title: DocumentPageRanges
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 84ded7c18fc781fd4374feb8958a98b845d95546
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/26/2021
ms.locfileid: "107997173"
---
# <a name="documentpageranges"></a><span data-ttu-id="3b846-104">DocumentPageRanges</span><span class="sxs-lookup"><span data-stu-id="3b846-104">DocumentPageRanges</span></span>

<span data-ttu-id="3b846-105">Este tópico não é atual.</span><span class="sxs-lookup"><span data-stu-id="3b846-105">This topic is not current.</span></span> <span data-ttu-id="3b846-106">Para obter as informações mais atuais, consulte a [especificação do esquema de impressão](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="3b846-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="3b846-107">Descreve o intervalo de saída do documento em páginas.</span><span class="sxs-lookup"><span data-stu-id="3b846-107">Describes the output range of the document in pages.</span></span> <span data-ttu-id="3b846-108">O valor do parâmetro deve estar de acordo com a seguinte estrutura:</span><span class="sxs-lookup"><span data-stu-id="3b846-108">The parameter value must conform to the following structure:</span></span>

-   <span data-ttu-id="3b846-109">PageRangeText: "*PageRange*" ou "*PageRange*,*PageRange*"</span><span class="sxs-lookup"><span data-stu-id="3b846-109">PageRangeText: "*PageRange*" or "*PageRange*,*PageRange*"</span></span>

-   <span data-ttu-id="3b846-110">PageRange: "*PageNumber*" ou "*PageNumber* - *PageNumber*"</span><span class="sxs-lookup"><span data-stu-id="3b846-110">PageRange: "*PageNumber*" or "*PageNumber*-*PageNumber*"</span></span>

-   <span data-ttu-id="3b846-111">PageNumber: 1 a N, em que N é o número de páginas no documento.</span><span class="sxs-lookup"><span data-stu-id="3b846-111">PageNumber: 1 to N, where N is the number of pages in the document.</span></span> <span data-ttu-id="3b846-112">Se *pagenumber* > N, *PageNumber* = N.</span><span class="sxs-lookup"><span data-stu-id="3b846-112">If *PageNumber* > N, then *PageNumber* = N.</span></span>

<span data-ttu-id="3b846-113">O espaço em branco na cadeia de caracteres deve ser ignorado.</span><span class="sxs-lookup"><span data-stu-id="3b846-113">Whitespace in the string should be ignored.</span></span>

-   [<span data-ttu-id="3b846-114">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="3b846-114">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="3b846-115">Conteúdo estrutural</span><span class="sxs-lookup"><span data-stu-id="3b846-115">Structural Content</span></span>](#structural-content)

## <a name="element-information"></a><span data-ttu-id="3b846-116">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="3b846-116">Element Information</span></span>



| <span data-ttu-id="3b846-117">Nome</span><span class="sxs-lookup"><span data-stu-id="3b846-117">Name</span></span> | <span data-ttu-id="3b846-118">Valor</span><span class="sxs-lookup"><span data-stu-id="3b846-118">Value</span></span> |
|----------------------------|-------------------------|
| <span data-ttu-id="3b846-119">Tipo de elemento</span><span class="sxs-lookup"><span data-stu-id="3b846-119">Element Type</span></span> <br/>   | <span data-ttu-id="3b846-120">ParameterDef</span><span class="sxs-lookup"><span data-stu-id="3b846-120">ParameterDef</span></span><br/> |
| <span data-ttu-id="3b846-121">Prefixo de escopo</span><span class="sxs-lookup"><span data-stu-id="3b846-121">Scoping Prefix</span></span> <br/> | <span data-ttu-id="3b846-122">Documento</span><span class="sxs-lookup"><span data-stu-id="3b846-122">Document</span></span><br/>     |
| <span data-ttu-id="3b846-123">Observações</span><span class="sxs-lookup"><span data-stu-id="3b846-123">Notes</span></span> <br/>          | <span data-ttu-id="3b846-124">Nenhum</span><span class="sxs-lookup"><span data-stu-id="3b846-124">None</span></span><br/>         |



 

## <a name="structural-content"></a><span data-ttu-id="3b846-125">Conteúdo estrutural</span><span class="sxs-lookup"><span data-stu-id="3b846-125">Structural Content</span></span>

<span data-ttu-id="3b846-126">A estrutura XML desse elemento é:</span><span class="sxs-lookup"><span data-stu-id="3b846-126">The XML structure of this element is:</span></span>

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

## <a name="structure-properties"></a><span data-ttu-id="3b846-127">Propriedades da estrutura</span><span class="sxs-lookup"><span data-stu-id="3b846-127">Structure Properties</span></span>

<span data-ttu-id="3b846-128">A tabela a seguir descreve as características das variáveis definidas na estrutura XML.</span><span class="sxs-lookup"><span data-stu-id="3b846-128">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="3b846-129">Propriedade</span><span class="sxs-lookup"><span data-stu-id="3b846-129">Property</span></span>                | <span data-ttu-id="3b846-130">xsi:type</span><span class="sxs-lookup"><span data-stu-id="3b846-130">xsi:type</span></span>           | <span data-ttu-id="3b846-131">Valor</span><span class="sxs-lookup"><span data-stu-id="3b846-131">Value</span></span>                      |
|-------------------------|--------------------|----------------------------|
| <span data-ttu-id="3b846-132">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="3b846-132">DataType</span></span><br/>     | <span data-ttu-id="3b846-133">string</span><span class="sxs-lookup"><span data-stu-id="3b846-133">string</span></span><br/>  | <span data-ttu-id="3b846-134">xs:string</span><span class="sxs-lookup"><span data-stu-id="3b846-134">xs:string</span></span><br/>       |
| <span data-ttu-id="3b846-135">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="3b846-135">DefaultValue</span></span><br/> | <span data-ttu-id="3b846-136">string</span><span class="sxs-lookup"><span data-stu-id="3b846-136">string</span></span><br/>  | <span data-ttu-id="3b846-137">não definido</span><span class="sxs-lookup"><span data-stu-id="3b846-137">undefined</span></span><br/>       |
| <span data-ttu-id="3b846-138">MaxLength</span><span class="sxs-lookup"><span data-stu-id="3b846-138">MaxLength</span></span><br/>    | <span data-ttu-id="3b846-139">Número inteiro</span><span class="sxs-lookup"><span data-stu-id="3b846-139">integer</span></span><br/> | <span data-ttu-id="3b846-140">não definido</span><span class="sxs-lookup"><span data-stu-id="3b846-140">undefined</span></span><br/>       |
| <span data-ttu-id="3b846-141">MinLength</span><span class="sxs-lookup"><span data-stu-id="3b846-141">MinLength</span></span><br/>    | <span data-ttu-id="3b846-142">integer</span><span class="sxs-lookup"><span data-stu-id="3b846-142">integer</span></span><br/> | <span data-ttu-id="3b846-143">1</span><span class="sxs-lookup"><span data-stu-id="3b846-143">1</span></span><br/>               |
| <span data-ttu-id="3b846-144">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="3b846-144">Mandatory</span></span><br/>    | <span data-ttu-id="3b846-145">string</span><span class="sxs-lookup"><span data-stu-id="3b846-145">string</span></span><br/>  | <span data-ttu-id="3b846-146">PSK: condicional</span><span class="sxs-lookup"><span data-stu-id="3b846-146">psk:Conditional</span></span><br/> |
| <span data-ttu-id="3b846-147">UnitType</span><span class="sxs-lookup"><span data-stu-id="3b846-147">UnitType</span></span><br/>     | <span data-ttu-id="3b846-148">string</span><span class="sxs-lookup"><span data-stu-id="3b846-148">string</span></span><br/>  | <span data-ttu-id="3b846-149">characters</span><span class="sxs-lookup"><span data-stu-id="3b846-149">characters</span></span><br/>      |



 

## <a name="related-topics"></a><span data-ttu-id="3b846-150">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="3b846-150">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3b846-151">Especificação de esquema de impressão</span><span class="sxs-lookup"><span data-stu-id="3b846-151">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




