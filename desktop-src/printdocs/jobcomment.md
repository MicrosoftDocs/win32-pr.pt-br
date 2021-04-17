---
description: Este tópico não é atual. Para obter as informações mais atuais, consulte a especificação do esquema de impressão.
ms.assetid: 100fe310-8e64-453f-8eaf-10abaf8b10b7
title: JobComment
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a8ebfbd2e62c18153dd0930197b6f49cbb3480d6
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/05/2021
ms.locfileid: "105748474"
---
# <a name="jobcomment"></a><span data-ttu-id="e204d-104">JobComment</span><span class="sxs-lookup"><span data-stu-id="e204d-104">JobComment</span></span>

<span data-ttu-id="e204d-105">Este tópico não é atual.</span><span class="sxs-lookup"><span data-stu-id="e204d-105">This topic is not current.</span></span> <span data-ttu-id="e204d-106">Para obter as informações mais atuais, consulte a [especificação do esquema de impressão](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="e204d-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="e204d-107">Especifica um comentário associado ao trabalho.</span><span class="sxs-lookup"><span data-stu-id="e204d-107">Specifies a comment associated with the job.</span></span> <span data-ttu-id="e204d-108">Exemplo: "forneça a sala 1234 quando concluído".</span><span class="sxs-lookup"><span data-stu-id="e204d-108">Example: "Please deliver to room 1234 when completed".</span></span>

-   [<span data-ttu-id="e204d-109">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="e204d-109">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="e204d-110">Conteúdo da estrutura</span><span class="sxs-lookup"><span data-stu-id="e204d-110">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="e204d-111">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="e204d-111">Element Information</span></span>



| <span data-ttu-id="e204d-112">Nome</span><span class="sxs-lookup"><span data-stu-id="e204d-112">Name</span></span>                       |                         |
|----------------------------|-------------------------|
| <span data-ttu-id="e204d-113">Tipo de elemento</span><span class="sxs-lookup"><span data-stu-id="e204d-113">Element Type</span></span> <br/>   | <span data-ttu-id="e204d-114">ParameterDef</span><span class="sxs-lookup"><span data-stu-id="e204d-114">ParameterDef</span></span><br/> |
| <span data-ttu-id="e204d-115">Prefixo de escopo</span><span class="sxs-lookup"><span data-stu-id="e204d-115">Scoping Prefix</span></span> <br/> | <span data-ttu-id="e204d-116">Trabalho</span><span class="sxs-lookup"><span data-stu-id="e204d-116">Job</span></span><br/>          |
| <span data-ttu-id="e204d-117">Observações</span><span class="sxs-lookup"><span data-stu-id="e204d-117">Notes</span></span> <br/>          | <span data-ttu-id="e204d-118">Nenhum</span><span class="sxs-lookup"><span data-stu-id="e204d-118">None</span></span><br/>         |



 

## <a name="structure-content"></a><span data-ttu-id="e204d-119">Conteúdo da estrutura</span><span class="sxs-lookup"><span data-stu-id="e204d-119">Structure Content</span></span>

<span data-ttu-id="e204d-120">A estrutura XML desse elemento é a seguinte:</span><span class="sxs-lookup"><span data-stu-id="e204d-120">The XML structure of this element is as follows:</span></span>

``` syntax
<psf:ParameterDef name="psk:JobComment">
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

## <a name="structure-properties"></a><span data-ttu-id="e204d-121">Propriedades da estrutura</span><span class="sxs-lookup"><span data-stu-id="e204d-121">Structure Properties</span></span>

<span data-ttu-id="e204d-122">A tabela a seguir descreve as características das variáveis definidas na estrutura XML.</span><span class="sxs-lookup"><span data-stu-id="e204d-122">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="e204d-123">Propriedade</span><span class="sxs-lookup"><span data-stu-id="e204d-123">Property</span></span>                | <span data-ttu-id="e204d-124">xsi:type</span><span class="sxs-lookup"><span data-stu-id="e204d-124">xsi:type</span></span>           | <span data-ttu-id="e204d-125">Valor</span><span class="sxs-lookup"><span data-stu-id="e204d-125">Value</span></span>                      |
|-------------------------|--------------------|----------------------------|
| <span data-ttu-id="e204d-126">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="e204d-126">DataType</span></span><br/>     | <span data-ttu-id="e204d-127">string</span><span class="sxs-lookup"><span data-stu-id="e204d-127">string</span></span><br/>  | <span data-ttu-id="e204d-128">xs:string</span><span class="sxs-lookup"><span data-stu-id="e204d-128">xs:string</span></span><br/>       |
| <span data-ttu-id="e204d-129">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="e204d-129">DefaultValue</span></span><br/> | <span data-ttu-id="e204d-130">string</span><span class="sxs-lookup"><span data-stu-id="e204d-130">string</span></span><br/>  | <span data-ttu-id="e204d-131">não definido</span><span class="sxs-lookup"><span data-stu-id="e204d-131">undefined</span></span><br/>       |
| <span data-ttu-id="e204d-132">MaxLength</span><span class="sxs-lookup"><span data-stu-id="e204d-132">MaxLength</span></span><br/>    | <span data-ttu-id="e204d-133">Número inteiro</span><span class="sxs-lookup"><span data-stu-id="e204d-133">integer</span></span><br/> | <span data-ttu-id="e204d-134">não definido</span><span class="sxs-lookup"><span data-stu-id="e204d-134">undefined</span></span><br/>       |
| <span data-ttu-id="e204d-135">MinLength</span><span class="sxs-lookup"><span data-stu-id="e204d-135">MinLength</span></span><br/>    | <span data-ttu-id="e204d-136">integer</span><span class="sxs-lookup"><span data-stu-id="e204d-136">integer</span></span><br/> | <span data-ttu-id="e204d-137">1</span><span class="sxs-lookup"><span data-stu-id="e204d-137">1</span></span><br/>               |
| <span data-ttu-id="e204d-138">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="e204d-138">Mandatory</span></span><br/>    | <span data-ttu-id="e204d-139">string</span><span class="sxs-lookup"><span data-stu-id="e204d-139">string</span></span><br/>  | <span data-ttu-id="e204d-140">PSK: condicional</span><span class="sxs-lookup"><span data-stu-id="e204d-140">psk:Conditional</span></span><br/> |
| <span data-ttu-id="e204d-141">UnitType</span><span class="sxs-lookup"><span data-stu-id="e204d-141">UnitType</span></span><br/>     | <span data-ttu-id="e204d-142">string</span><span class="sxs-lookup"><span data-stu-id="e204d-142">string</span></span><br/>  | <span data-ttu-id="e204d-143">characters</span><span class="sxs-lookup"><span data-stu-id="e204d-143">characters</span></span><br/>      |



 

## <a name="related-topics"></a><span data-ttu-id="e204d-144">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="e204d-144">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e204d-145">Especificação de esquema de impressão</span><span class="sxs-lookup"><span data-stu-id="e204d-145">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




