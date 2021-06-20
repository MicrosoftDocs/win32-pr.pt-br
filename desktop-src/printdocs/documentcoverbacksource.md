---
description: Saiba mais sobre o elemento DocumentCoverBackSource, que especifica a origem de uma folha de back-cover personalizada.
ms.assetid: 43a0c881-75cc-4fbc-a0c3-b3eab9dfe4df
title: DocumentCoverBackSource
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5be16ab26a4aa3dd7109fee7d630ed354b9b686d
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/19/2021
ms.locfileid: "112409349"
---
# <a name="documentcoverbacksource"></a><span data-ttu-id="4ee12-103">DocumentCoverBackSource</span><span class="sxs-lookup"><span data-stu-id="4ee12-103">DocumentCoverBackSource</span></span>

<span data-ttu-id="4ee12-104">Este tópico não é atual.</span><span class="sxs-lookup"><span data-stu-id="4ee12-104">This topic is not current.</span></span> <span data-ttu-id="4ee12-105">Para obter as informações mais atuais, consulte a [Especificação de Esquema de Impressão](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="4ee12-105">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="4ee12-106">Especifica a origem de uma folha de back-cover personalizada.</span><span class="sxs-lookup"><span data-stu-id="4ee12-106">Specifies the source for a custom back-cover sheet.</span></span>

-   [<span data-ttu-id="4ee12-107">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="4ee12-107">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="4ee12-108">Conteúdo da estrutura</span><span class="sxs-lookup"><span data-stu-id="4ee12-108">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="4ee12-109">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="4ee12-109">Element Information</span></span>



| <span data-ttu-id="4ee12-110">Name</span><span class="sxs-lookup"><span data-stu-id="4ee12-110">Name</span></span> | <span data-ttu-id="4ee12-111">Valor</span><span class="sxs-lookup"><span data-stu-id="4ee12-111">Value</span></span> |
|----------------------------|------------------------------------------------|
| <span data-ttu-id="4ee12-112">Tipo de elemento</span><span class="sxs-lookup"><span data-stu-id="4ee12-112">Element Type</span></span> <br/>   | <span data-ttu-id="4ee12-113">ParameterDef</span><span class="sxs-lookup"><span data-stu-id="4ee12-113">ParameterDef</span></span><br/>                        |
| <span data-ttu-id="4ee12-114">Prefixo de definição de scoping</span><span class="sxs-lookup"><span data-stu-id="4ee12-114">Scoping Prefix</span></span> <br/> | <span data-ttu-id="4ee12-115">Documento</span><span class="sxs-lookup"><span data-stu-id="4ee12-115">Document</span></span><br/>                            |
| <span data-ttu-id="4ee12-116">Observações</span><span class="sxs-lookup"><span data-stu-id="4ee12-116">Notes</span></span> <br/>          | <span data-ttu-id="4ee12-117">Vinculado ao elemento DocumentCoverBack</span><span class="sxs-lookup"><span data-stu-id="4ee12-117">Linked to DocumentCoverBack element</span></span><br/> |



 

## <a name="structure-content"></a><span data-ttu-id="4ee12-118">Conteúdo da estrutura</span><span class="sxs-lookup"><span data-stu-id="4ee12-118">Structure Content</span></span>

<span data-ttu-id="4ee12-119">A estrutura XML desse elemento é:</span><span class="sxs-lookup"><span data-stu-id="4ee12-119">The XML structure of this element is:</span></span>

``` syntax
<psf:ParameterDef name="psk:DocumentCoverBackSource">
  <psf:Property name="psf:DataType">
    <psf:Value xsi:type="xs:string">xs:string</psf:Value>
  </psf:Property>
  <psf:Property name="psf:DefaultValue">
    <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
  </psf:Property>
  <psf:Property name="psf:MaxLength">
    <psf:Value xsi:type="xs:integer ">_Undefined_</psf:Value>
  </psf:Property>
  <psf:Property name="psf:MinLength">
    <psf:Value xsi:type="xs:integer ">1</psf:Value>
  </psf:Property>
  <psf:Property name="psf:Mandatory">
    <psf:Value xsi:type="xs:string">psk:Conditional</psf:Value>
  </psf:Property>
  <psf:Property name="psf:UnitType">
    <psf:Value xsi:type="xs:string">characters</psf:Value>
  </psf:Property>
</psf:ParameterDef>      
```

## <a name="structure-properties"></a><span data-ttu-id="4ee12-120">Propriedades da estrutura</span><span class="sxs-lookup"><span data-stu-id="4ee12-120">Structure Properties</span></span>

<span data-ttu-id="4ee12-121">A tabela a seguir descreve as características das variáveis definidas na estrutura XML.</span><span class="sxs-lookup"><span data-stu-id="4ee12-121">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="4ee12-122">Propriedade</span><span class="sxs-lookup"><span data-stu-id="4ee12-122">Property</span></span>                | <span data-ttu-id="4ee12-123">xsi:type</span><span class="sxs-lookup"><span data-stu-id="4ee12-123">xsi:type</span></span>           | <span data-ttu-id="4ee12-124">Valor</span><span class="sxs-lookup"><span data-stu-id="4ee12-124">Value</span></span>                      |
|-------------------------|--------------------|----------------------------|
| <span data-ttu-id="4ee12-125">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="4ee12-125">DataType</span></span><br/>     | <span data-ttu-id="4ee12-126">string</span><span class="sxs-lookup"><span data-stu-id="4ee12-126">string</span></span><br/>  | <span data-ttu-id="4ee12-127">xs:string</span><span class="sxs-lookup"><span data-stu-id="4ee12-127">xs:string</span></span><br/>       |
| <span data-ttu-id="4ee12-128">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="4ee12-128">DefaultValue</span></span><br/> | <span data-ttu-id="4ee12-129">string</span><span class="sxs-lookup"><span data-stu-id="4ee12-129">string</span></span><br/>  | <span data-ttu-id="4ee12-130">não definido</span><span class="sxs-lookup"><span data-stu-id="4ee12-130">undefined</span></span><br/>       |
| <span data-ttu-id="4ee12-131">MaxLength</span><span class="sxs-lookup"><span data-stu-id="4ee12-131">MaxLength</span></span><br/>    | <span data-ttu-id="4ee12-132">Número inteiro</span><span class="sxs-lookup"><span data-stu-id="4ee12-132">integer</span></span><br/> | <span data-ttu-id="4ee12-133">não definido</span><span class="sxs-lookup"><span data-stu-id="4ee12-133">undefined</span></span><br/>       |
| <span data-ttu-id="4ee12-134">Minlength</span><span class="sxs-lookup"><span data-stu-id="4ee12-134">MinLength</span></span><br/>    | <span data-ttu-id="4ee12-135">integer</span><span class="sxs-lookup"><span data-stu-id="4ee12-135">integer</span></span><br/> | <span data-ttu-id="4ee12-136">1</span><span class="sxs-lookup"><span data-stu-id="4ee12-136">1</span></span><br/>               |
| <span data-ttu-id="4ee12-137">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="4ee12-137">Mandatory</span></span><br/>    | <span data-ttu-id="4ee12-138">string</span><span class="sxs-lookup"><span data-stu-id="4ee12-138">string</span></span><br/>  | <span data-ttu-id="4ee12-139">psk:Conditional</span><span class="sxs-lookup"><span data-stu-id="4ee12-139">psk:Conditional</span></span><br/> |
| <span data-ttu-id="4ee12-140">Unittype</span><span class="sxs-lookup"><span data-stu-id="4ee12-140">UnitType</span></span><br/>     | <span data-ttu-id="4ee12-141">string</span><span class="sxs-lookup"><span data-stu-id="4ee12-141">string</span></span><br/>  | <span data-ttu-id="4ee12-142">characters</span><span class="sxs-lookup"><span data-stu-id="4ee12-142">characters</span></span><br/>      |



 

## <a name="related-topics"></a><span data-ttu-id="4ee12-143">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="4ee12-143">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4ee12-144">Especificação de esquema de impressão</span><span class="sxs-lookup"><span data-stu-id="4ee12-144">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




