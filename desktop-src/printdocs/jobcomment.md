---
description: Este tópico não é atual. Para obter as informações mais atuais, consulte a especificação do esquema de impressão.
ms.assetid: 100fe310-8e64-453f-8eaf-10abaf8b10b7
title: JobComment
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5210b80d4f81771dfa98d79d4ecf187b3ef145f5
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/26/2021
ms.locfileid: "107998343"
---
# <a name="jobcomment"></a><span data-ttu-id="545a3-104">JobComment</span><span class="sxs-lookup"><span data-stu-id="545a3-104">JobComment</span></span>

<span data-ttu-id="545a3-105">Este tópico não é atual.</span><span class="sxs-lookup"><span data-stu-id="545a3-105">This topic is not current.</span></span> <span data-ttu-id="545a3-106">Para obter as informações mais atuais, consulte a [especificação do esquema de impressão](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="545a3-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="545a3-107">Especifica um comentário associado ao trabalho.</span><span class="sxs-lookup"><span data-stu-id="545a3-107">Specifies a comment associated with the job.</span></span> <span data-ttu-id="545a3-108">Exemplo: "forneça a sala 1234 quando concluído".</span><span class="sxs-lookup"><span data-stu-id="545a3-108">Example: "Please deliver to room 1234 when completed".</span></span>

-   [<span data-ttu-id="545a3-109">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="545a3-109">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="545a3-110">Conteúdo da estrutura</span><span class="sxs-lookup"><span data-stu-id="545a3-110">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="545a3-111">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="545a3-111">Element Information</span></span>



| <span data-ttu-id="545a3-112">Nome</span><span class="sxs-lookup"><span data-stu-id="545a3-112">Name</span></span> | <span data-ttu-id="545a3-113">Valor</span><span class="sxs-lookup"><span data-stu-id="545a3-113">Value</span></span> |
|----------------------------|-------------------------|
| <span data-ttu-id="545a3-114">Tipo de elemento</span><span class="sxs-lookup"><span data-stu-id="545a3-114">Element Type</span></span> <br/>   | <span data-ttu-id="545a3-115">ParameterDef</span><span class="sxs-lookup"><span data-stu-id="545a3-115">ParameterDef</span></span><br/> |
| <span data-ttu-id="545a3-116">Prefixo de escopo</span><span class="sxs-lookup"><span data-stu-id="545a3-116">Scoping Prefix</span></span> <br/> | <span data-ttu-id="545a3-117">Trabalho</span><span class="sxs-lookup"><span data-stu-id="545a3-117">Job</span></span><br/>          |
| <span data-ttu-id="545a3-118">Observações</span><span class="sxs-lookup"><span data-stu-id="545a3-118">Notes</span></span> <br/>          | <span data-ttu-id="545a3-119">Nenhum</span><span class="sxs-lookup"><span data-stu-id="545a3-119">None</span></span><br/>         |



 

## <a name="structure-content"></a><span data-ttu-id="545a3-120">Conteúdo da estrutura</span><span class="sxs-lookup"><span data-stu-id="545a3-120">Structure Content</span></span>

<span data-ttu-id="545a3-121">A estrutura XML desse elemento é a seguinte:</span><span class="sxs-lookup"><span data-stu-id="545a3-121">The XML structure of this element is as follows:</span></span>

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

## <a name="structure-properties"></a><span data-ttu-id="545a3-122">Propriedades da estrutura</span><span class="sxs-lookup"><span data-stu-id="545a3-122">Structure Properties</span></span>

<span data-ttu-id="545a3-123">A tabela a seguir descreve as características das variáveis definidas na estrutura XML.</span><span class="sxs-lookup"><span data-stu-id="545a3-123">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="545a3-124">Propriedade</span><span class="sxs-lookup"><span data-stu-id="545a3-124">Property</span></span>                | <span data-ttu-id="545a3-125">xsi:type</span><span class="sxs-lookup"><span data-stu-id="545a3-125">xsi:type</span></span>           | <span data-ttu-id="545a3-126">Valor</span><span class="sxs-lookup"><span data-stu-id="545a3-126">Value</span></span>                      |
|-------------------------|--------------------|----------------------------|
| <span data-ttu-id="545a3-127">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="545a3-127">DataType</span></span><br/>     | <span data-ttu-id="545a3-128">string</span><span class="sxs-lookup"><span data-stu-id="545a3-128">string</span></span><br/>  | <span data-ttu-id="545a3-129">xs:string</span><span class="sxs-lookup"><span data-stu-id="545a3-129">xs:string</span></span><br/>       |
| <span data-ttu-id="545a3-130">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="545a3-130">DefaultValue</span></span><br/> | <span data-ttu-id="545a3-131">string</span><span class="sxs-lookup"><span data-stu-id="545a3-131">string</span></span><br/>  | <span data-ttu-id="545a3-132">não definido</span><span class="sxs-lookup"><span data-stu-id="545a3-132">undefined</span></span><br/>       |
| <span data-ttu-id="545a3-133">MaxLength</span><span class="sxs-lookup"><span data-stu-id="545a3-133">MaxLength</span></span><br/>    | <span data-ttu-id="545a3-134">Número inteiro</span><span class="sxs-lookup"><span data-stu-id="545a3-134">integer</span></span><br/> | <span data-ttu-id="545a3-135">não definido</span><span class="sxs-lookup"><span data-stu-id="545a3-135">undefined</span></span><br/>       |
| <span data-ttu-id="545a3-136">MinLength</span><span class="sxs-lookup"><span data-stu-id="545a3-136">MinLength</span></span><br/>    | <span data-ttu-id="545a3-137">integer</span><span class="sxs-lookup"><span data-stu-id="545a3-137">integer</span></span><br/> | <span data-ttu-id="545a3-138">1</span><span class="sxs-lookup"><span data-stu-id="545a3-138">1</span></span><br/>               |
| <span data-ttu-id="545a3-139">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="545a3-139">Mandatory</span></span><br/>    | <span data-ttu-id="545a3-140">string</span><span class="sxs-lookup"><span data-stu-id="545a3-140">string</span></span><br/>  | <span data-ttu-id="545a3-141">PSK: condicional</span><span class="sxs-lookup"><span data-stu-id="545a3-141">psk:Conditional</span></span><br/> |
| <span data-ttu-id="545a3-142">UnitType</span><span class="sxs-lookup"><span data-stu-id="545a3-142">UnitType</span></span><br/>     | <span data-ttu-id="545a3-143">string</span><span class="sxs-lookup"><span data-stu-id="545a3-143">string</span></span><br/>  | <span data-ttu-id="545a3-144">characters</span><span class="sxs-lookup"><span data-stu-id="545a3-144">characters</span></span><br/>      |



 

## <a name="related-topics"></a><span data-ttu-id="545a3-145">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="545a3-145">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="545a3-146">Especificação de esquema de impressão</span><span class="sxs-lookup"><span data-stu-id="545a3-146">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




