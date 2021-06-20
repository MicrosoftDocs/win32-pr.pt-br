---
description: Saiba mais sobre o elemento JobComment, que especifica um comentário associado ao trabalho, por exemplo, Entregue à sala 1234 quando concluído.
ms.assetid: 100fe310-8e64-453f-8eaf-10abaf8b10b7
title: JobComment
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1decf4cf3af7b3a992b07d8008579ac005d3d14e
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/19/2021
ms.locfileid: "112409039"
---
# <a name="jobcomment"></a><span data-ttu-id="91302-103">JobComment</span><span class="sxs-lookup"><span data-stu-id="91302-103">JobComment</span></span>

<span data-ttu-id="91302-104">Este tópico não é atual.</span><span class="sxs-lookup"><span data-stu-id="91302-104">This topic is not current.</span></span> <span data-ttu-id="91302-105">Para obter as informações mais atuais, consulte a [Especificação de Esquema de Impressão](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="91302-105">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="91302-106">Especifica um comentário associado ao trabalho.</span><span class="sxs-lookup"><span data-stu-id="91302-106">Specifies a comment associated with the job.</span></span> <span data-ttu-id="91302-107">Exemplo: "Entregue ao quarto 1234 quando concluído".</span><span class="sxs-lookup"><span data-stu-id="91302-107">Example: "Please deliver to room 1234 when completed".</span></span>

-   [<span data-ttu-id="91302-108">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="91302-108">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="91302-109">Conteúdo da estrutura</span><span class="sxs-lookup"><span data-stu-id="91302-109">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="91302-110">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="91302-110">Element Information</span></span>



| <span data-ttu-id="91302-111">Name</span><span class="sxs-lookup"><span data-stu-id="91302-111">Name</span></span> | <span data-ttu-id="91302-112">Valor</span><span class="sxs-lookup"><span data-stu-id="91302-112">Value</span></span> |
|----------------------------|-------------------------|
| <span data-ttu-id="91302-113">Tipo de elemento</span><span class="sxs-lookup"><span data-stu-id="91302-113">Element Type</span></span> <br/>   | <span data-ttu-id="91302-114">ParameterDef</span><span class="sxs-lookup"><span data-stu-id="91302-114">ParameterDef</span></span><br/> |
| <span data-ttu-id="91302-115">Prefixo de definição de scoping</span><span class="sxs-lookup"><span data-stu-id="91302-115">Scoping Prefix</span></span> <br/> | <span data-ttu-id="91302-116">Trabalho</span><span class="sxs-lookup"><span data-stu-id="91302-116">Job</span></span><br/>          |
| <span data-ttu-id="91302-117">Observações</span><span class="sxs-lookup"><span data-stu-id="91302-117">Notes</span></span> <br/>          | <span data-ttu-id="91302-118">Nenhum</span><span class="sxs-lookup"><span data-stu-id="91302-118">None</span></span><br/>         |



 

## <a name="structure-content"></a><span data-ttu-id="91302-119">Conteúdo da estrutura</span><span class="sxs-lookup"><span data-stu-id="91302-119">Structure Content</span></span>

<span data-ttu-id="91302-120">A estrutura XML desse elemento é a seguinte:</span><span class="sxs-lookup"><span data-stu-id="91302-120">The XML structure of this element is as follows:</span></span>

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

## <a name="structure-properties"></a><span data-ttu-id="91302-121">Propriedades da estrutura</span><span class="sxs-lookup"><span data-stu-id="91302-121">Structure Properties</span></span>

<span data-ttu-id="91302-122">A tabela a seguir descreve as características das variáveis definidas na estrutura XML.</span><span class="sxs-lookup"><span data-stu-id="91302-122">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="91302-123">Propriedade</span><span class="sxs-lookup"><span data-stu-id="91302-123">Property</span></span>                | <span data-ttu-id="91302-124">xsi:type</span><span class="sxs-lookup"><span data-stu-id="91302-124">xsi:type</span></span>           | <span data-ttu-id="91302-125">Valor</span><span class="sxs-lookup"><span data-stu-id="91302-125">Value</span></span>                      |
|-------------------------|--------------------|----------------------------|
| <span data-ttu-id="91302-126">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="91302-126">DataType</span></span><br/>     | <span data-ttu-id="91302-127">string</span><span class="sxs-lookup"><span data-stu-id="91302-127">string</span></span><br/>  | <span data-ttu-id="91302-128">xs:string</span><span class="sxs-lookup"><span data-stu-id="91302-128">xs:string</span></span><br/>       |
| <span data-ttu-id="91302-129">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="91302-129">DefaultValue</span></span><br/> | <span data-ttu-id="91302-130">string</span><span class="sxs-lookup"><span data-stu-id="91302-130">string</span></span><br/>  | <span data-ttu-id="91302-131">não definido</span><span class="sxs-lookup"><span data-stu-id="91302-131">undefined</span></span><br/>       |
| <span data-ttu-id="91302-132">MaxLength</span><span class="sxs-lookup"><span data-stu-id="91302-132">MaxLength</span></span><br/>    | <span data-ttu-id="91302-133">Número inteiro</span><span class="sxs-lookup"><span data-stu-id="91302-133">integer</span></span><br/> | <span data-ttu-id="91302-134">não definido</span><span class="sxs-lookup"><span data-stu-id="91302-134">undefined</span></span><br/>       |
| <span data-ttu-id="91302-135">Minlength</span><span class="sxs-lookup"><span data-stu-id="91302-135">MinLength</span></span><br/>    | <span data-ttu-id="91302-136">integer</span><span class="sxs-lookup"><span data-stu-id="91302-136">integer</span></span><br/> | <span data-ttu-id="91302-137">1</span><span class="sxs-lookup"><span data-stu-id="91302-137">1</span></span><br/>               |
| <span data-ttu-id="91302-138">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="91302-138">Mandatory</span></span><br/>    | <span data-ttu-id="91302-139">string</span><span class="sxs-lookup"><span data-stu-id="91302-139">string</span></span><br/>  | <span data-ttu-id="91302-140">psk:Conditional</span><span class="sxs-lookup"><span data-stu-id="91302-140">psk:Conditional</span></span><br/> |
| <span data-ttu-id="91302-141">Unittype</span><span class="sxs-lookup"><span data-stu-id="91302-141">UnitType</span></span><br/>     | <span data-ttu-id="91302-142">string</span><span class="sxs-lookup"><span data-stu-id="91302-142">string</span></span><br/>  | <span data-ttu-id="91302-143">characters</span><span class="sxs-lookup"><span data-stu-id="91302-143">characters</span></span><br/>      |



 

## <a name="related-topics"></a><span data-ttu-id="91302-144">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="91302-144">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="91302-145">Especificação de esquema de impressão</span><span class="sxs-lookup"><span data-stu-id="91302-145">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




