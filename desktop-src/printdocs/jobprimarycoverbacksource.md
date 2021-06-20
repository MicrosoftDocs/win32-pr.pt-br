---
description: Saiba mais sobre o elemento JobPrimaryCoverBackSource, que especifica a origem de uma folha primária de capa de fundo personalizada para o trabalho.
ms.assetid: b5c8e79c-cdae-4c53-b594-915726423b4f
title: JobPrimaryCoverBackSource
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 74ed9bbc1b49e230eabc3fd7f45773a73401e058
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/19/2021
ms.locfileid: "112408689"
---
# <a name="jobprimarycoverbacksource"></a><span data-ttu-id="3b0d5-103">JobPrimaryCoverBackSource</span><span class="sxs-lookup"><span data-stu-id="3b0d5-103">JobPrimaryCoverBackSource</span></span>

<span data-ttu-id="3b0d5-104">Este tópico não é atual.</span><span class="sxs-lookup"><span data-stu-id="3b0d5-104">This topic is not current.</span></span> <span data-ttu-id="3b0d5-105">Para obter as informações mais atuais, consulte a [especificação do esquema de impressão](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="3b0d5-105">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="3b0d5-106">Especifica a origem de uma folha primária de capa de fundo personalizada para o trabalho.</span><span class="sxs-lookup"><span data-stu-id="3b0d5-106">Specifies the source for a custom back-cover primary sheet for the job.</span></span>

-   [<span data-ttu-id="3b0d5-107">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="3b0d5-107">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="3b0d5-108">Conteúdo da estrutura</span><span class="sxs-lookup"><span data-stu-id="3b0d5-108">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="3b0d5-109">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="3b0d5-109">Element Information</span></span>



| <span data-ttu-id="3b0d5-110">Name</span><span class="sxs-lookup"><span data-stu-id="3b0d5-110">Name</span></span> | <span data-ttu-id="3b0d5-111">Valor</span><span class="sxs-lookup"><span data-stu-id="3b0d5-111">Value</span></span> |
|----------------------------|-------------------------------------------|
| <span data-ttu-id="3b0d5-112">Tipo de elemento</span><span class="sxs-lookup"><span data-stu-id="3b0d5-112">Element Type</span></span> <br/>   | <span data-ttu-id="3b0d5-113">ParameterDef</span><span class="sxs-lookup"><span data-stu-id="3b0d5-113">ParameterDef</span></span><br/>                   |
| <span data-ttu-id="3b0d5-114">Prefixo de escopo</span><span class="sxs-lookup"><span data-stu-id="3b0d5-114">Scoping Prefix</span></span> <br/> | <span data-ttu-id="3b0d5-115">Trabalho</span><span class="sxs-lookup"><span data-stu-id="3b0d5-115">Job</span></span><br/>                            |
| <span data-ttu-id="3b0d5-116">Observações</span><span class="sxs-lookup"><span data-stu-id="3b0d5-116">Notes</span></span> <br/>          | <span data-ttu-id="3b0d5-117">Vinculado ao elemento JobCoverBack</span><span class="sxs-lookup"><span data-stu-id="3b0d5-117">Linked to JobCoverBack element</span></span><br/> |



 

## <a name="structure-content"></a><span data-ttu-id="3b0d5-118">Conteúdo da estrutura</span><span class="sxs-lookup"><span data-stu-id="3b0d5-118">Structure Content</span></span>

<span data-ttu-id="3b0d5-119">A estrutura XML desse elemento é:</span><span class="sxs-lookup"><span data-stu-id="3b0d5-119">The XML structure of this element is:</span></span>

``` syntax
<psf:ParameterDef name="psk:JobPrimaryCoverBackSource">
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

## <a name="structure-properties"></a><span data-ttu-id="3b0d5-120">Propriedades da estrutura</span><span class="sxs-lookup"><span data-stu-id="3b0d5-120">Structure Properties</span></span>

<span data-ttu-id="3b0d5-121">A tabela a seguir descreve as características das variáveis definidas na estrutura XML.</span><span class="sxs-lookup"><span data-stu-id="3b0d5-121">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="3b0d5-122">Propriedade</span><span class="sxs-lookup"><span data-stu-id="3b0d5-122">Property</span></span>                | <span data-ttu-id="3b0d5-123">xsi:type</span><span class="sxs-lookup"><span data-stu-id="3b0d5-123">xsi:type</span></span>           | <span data-ttu-id="3b0d5-124">Valor</span><span class="sxs-lookup"><span data-stu-id="3b0d5-124">Value</span></span>                      |
|-------------------------|--------------------|----------------------------|
| <span data-ttu-id="3b0d5-125">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="3b0d5-125">DataType</span></span><br/>     | <span data-ttu-id="3b0d5-126">string</span><span class="sxs-lookup"><span data-stu-id="3b0d5-126">string</span></span><br/>  | <span data-ttu-id="3b0d5-127">xs:string</span><span class="sxs-lookup"><span data-stu-id="3b0d5-127">xs:string</span></span><br/>       |
| <span data-ttu-id="3b0d5-128">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="3b0d5-128">DefaultValue</span></span><br/> | <span data-ttu-id="3b0d5-129">string</span><span class="sxs-lookup"><span data-stu-id="3b0d5-129">string</span></span><br/>  | <span data-ttu-id="3b0d5-130">não definido</span><span class="sxs-lookup"><span data-stu-id="3b0d5-130">undefined</span></span><br/>       |
| <span data-ttu-id="3b0d5-131">MaxLength</span><span class="sxs-lookup"><span data-stu-id="3b0d5-131">MaxLength</span></span><br/>    | <span data-ttu-id="3b0d5-132">Número inteiro</span><span class="sxs-lookup"><span data-stu-id="3b0d5-132">integer</span></span><br/> | <span data-ttu-id="3b0d5-133">não definido</span><span class="sxs-lookup"><span data-stu-id="3b0d5-133">undefined</span></span><br/>       |
| <span data-ttu-id="3b0d5-134">MinLength</span><span class="sxs-lookup"><span data-stu-id="3b0d5-134">MinLength</span></span><br/>    | <span data-ttu-id="3b0d5-135">integer</span><span class="sxs-lookup"><span data-stu-id="3b0d5-135">integer</span></span><br/> | <span data-ttu-id="3b0d5-136">1</span><span class="sxs-lookup"><span data-stu-id="3b0d5-136">1</span></span><br/>               |
| <span data-ttu-id="3b0d5-137">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="3b0d5-137">Mandatory</span></span><br/>    | <span data-ttu-id="3b0d5-138">string</span><span class="sxs-lookup"><span data-stu-id="3b0d5-138">string</span></span><br/>  | <span data-ttu-id="3b0d5-139">PSK: condicional</span><span class="sxs-lookup"><span data-stu-id="3b0d5-139">psk:Conditional</span></span><br/> |
| <span data-ttu-id="3b0d5-140">UnitType</span><span class="sxs-lookup"><span data-stu-id="3b0d5-140">UnitType</span></span><br/>     | <span data-ttu-id="3b0d5-141">string</span><span class="sxs-lookup"><span data-stu-id="3b0d5-141">string</span></span><br/>  | <span data-ttu-id="3b0d5-142">characters</span><span class="sxs-lookup"><span data-stu-id="3b0d5-142">characters</span></span><br/>      |



 

## <a name="related-topics"></a><span data-ttu-id="3b0d5-143">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="3b0d5-143">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3b0d5-144">Especificação de esquema de impressão</span><span class="sxs-lookup"><span data-stu-id="3b0d5-144">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




