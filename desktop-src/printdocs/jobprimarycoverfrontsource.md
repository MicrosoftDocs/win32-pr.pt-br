---
description: Obter informações sobre o parâmetro JobPrimaryCoverFrontSource. Este tópico não é atual. Para obter as informações mais atuais, consulte a Especificação de Esquema de Impressão.
ms.assetid: f27c5e65-87b0-47a4-a5dc-27b52082f097
title: JobPrimaryCoverFrontSource
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6e4698d826e59e513d5eb171381cd1b18ea4a751
ms.sourcegitcommit: 998d50f6def8a25850fc113fc8a2df903c829c5e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/09/2021
ms.locfileid: "113549394"
---
# <a name="jobprimarycoverfrontsource"></a><span data-ttu-id="0ce2d-105">JobPrimaryCoverFrontSource</span><span class="sxs-lookup"><span data-stu-id="0ce2d-105">JobPrimaryCoverFrontSource</span></span>

<span data-ttu-id="0ce2d-106">Este tópico não é atual.</span><span class="sxs-lookup"><span data-stu-id="0ce2d-106">This topic is not current.</span></span> <span data-ttu-id="0ce2d-107">Para obter as informações mais atuais, consulte a [Especificação de Esquema de Impressão](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="0ce2d-107">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="0ce2d-108">Especifica a origem de uma folha primária de front-cover personalizada para o trabalho.</span><span class="sxs-lookup"><span data-stu-id="0ce2d-108">Specifies the source for a custom front-cover primary sheet for the job.</span></span>

-   [<span data-ttu-id="0ce2d-109">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="0ce2d-109">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="0ce2d-110">Conteúdo da estrutura</span><span class="sxs-lookup"><span data-stu-id="0ce2d-110">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="0ce2d-111">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="0ce2d-111">Element Information</span></span>



| <span data-ttu-id="0ce2d-112">Nome</span><span class="sxs-lookup"><span data-stu-id="0ce2d-112">Name</span></span> | <span data-ttu-id="0ce2d-113">Valor</span><span class="sxs-lookup"><span data-stu-id="0ce2d-113">Value</span></span> |
|----------------------------|--------------------------------------------|
| <span data-ttu-id="0ce2d-114">Tipo de elemento</span><span class="sxs-lookup"><span data-stu-id="0ce2d-114">Element Type</span></span> <br/>   | <span data-ttu-id="0ce2d-115">ParameterDef</span><span class="sxs-lookup"><span data-stu-id="0ce2d-115">ParameterDef</span></span><br/>                    |
| <span data-ttu-id="0ce2d-116">Prefixo de definição de scoping</span><span class="sxs-lookup"><span data-stu-id="0ce2d-116">Scoping Prefix</span></span> <br/> | <span data-ttu-id="0ce2d-117">Trabalho</span><span class="sxs-lookup"><span data-stu-id="0ce2d-117">Job</span></span><br/>                             |
| <span data-ttu-id="0ce2d-118">Observações</span><span class="sxs-lookup"><span data-stu-id="0ce2d-118">Notes</span></span> <br/>          | <span data-ttu-id="0ce2d-119">Vinculado ao elemento JobCoverFront</span><span class="sxs-lookup"><span data-stu-id="0ce2d-119">Linked to JobCoverFront element</span></span><br/> |



 

## <a name="structure-content"></a><span data-ttu-id="0ce2d-120">Conteúdo da estrutura</span><span class="sxs-lookup"><span data-stu-id="0ce2d-120">Structure Content</span></span>

<span data-ttu-id="0ce2d-121">A estrutura XML desse elemento é:</span><span class="sxs-lookup"><span data-stu-id="0ce2d-121">The XML structure of this element is:</span></span>

``` syntax
<psf:ParameterDef name="psk:JobPrimaryCoverFrontSource">
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

## <a name="structure-properties"></a><span data-ttu-id="0ce2d-122">Propriedades da estrutura</span><span class="sxs-lookup"><span data-stu-id="0ce2d-122">Structure Properties</span></span>

<span data-ttu-id="0ce2d-123">A tabela a seguir descreve as características das variáveis definidas na estrutura XML.</span><span class="sxs-lookup"><span data-stu-id="0ce2d-123">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="0ce2d-124">Propriedade</span><span class="sxs-lookup"><span data-stu-id="0ce2d-124">Property</span></span>                | <span data-ttu-id="0ce2d-125">xsi:type</span><span class="sxs-lookup"><span data-stu-id="0ce2d-125">xsi:type</span></span>           | <span data-ttu-id="0ce2d-126">Valor</span><span class="sxs-lookup"><span data-stu-id="0ce2d-126">Value</span></span>                      |
|-------------------------|--------------------|----------------------------|
| <span data-ttu-id="0ce2d-127">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="0ce2d-127">DataType</span></span><br/>     | <span data-ttu-id="0ce2d-128">string</span><span class="sxs-lookup"><span data-stu-id="0ce2d-128">string</span></span><br/>  | <span data-ttu-id="0ce2d-129">xs:string</span><span class="sxs-lookup"><span data-stu-id="0ce2d-129">xs:string</span></span><br/>       |
| <span data-ttu-id="0ce2d-130">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="0ce2d-130">DefaultValue</span></span><br/> | <span data-ttu-id="0ce2d-131">string</span><span class="sxs-lookup"><span data-stu-id="0ce2d-131">string</span></span><br/>  | <span data-ttu-id="0ce2d-132">não definido</span><span class="sxs-lookup"><span data-stu-id="0ce2d-132">undefined</span></span><br/>       |
| <span data-ttu-id="0ce2d-133">MaxLength</span><span class="sxs-lookup"><span data-stu-id="0ce2d-133">MaxLength</span></span><br/>    | <span data-ttu-id="0ce2d-134">Número inteiro</span><span class="sxs-lookup"><span data-stu-id="0ce2d-134">integer</span></span><br/> | <span data-ttu-id="0ce2d-135">não definido</span><span class="sxs-lookup"><span data-stu-id="0ce2d-135">undefined</span></span><br/>       |
| <span data-ttu-id="0ce2d-136">Minlength</span><span class="sxs-lookup"><span data-stu-id="0ce2d-136">MinLength</span></span><br/>    | <span data-ttu-id="0ce2d-137">integer</span><span class="sxs-lookup"><span data-stu-id="0ce2d-137">integer</span></span><br/> | <span data-ttu-id="0ce2d-138">1</span><span class="sxs-lookup"><span data-stu-id="0ce2d-138">1</span></span><br/>               |
| <span data-ttu-id="0ce2d-139">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="0ce2d-139">Mandatory</span></span><br/>    | <span data-ttu-id="0ce2d-140">string</span><span class="sxs-lookup"><span data-stu-id="0ce2d-140">string</span></span><br/>  | <span data-ttu-id="0ce2d-141">psk:Conditional</span><span class="sxs-lookup"><span data-stu-id="0ce2d-141">psk:Conditional</span></span><br/> |
| <span data-ttu-id="0ce2d-142">Unittype</span><span class="sxs-lookup"><span data-stu-id="0ce2d-142">UnitType</span></span><br/>     | <span data-ttu-id="0ce2d-143">string</span><span class="sxs-lookup"><span data-stu-id="0ce2d-143">string</span></span><br/>  | <span data-ttu-id="0ce2d-144">characters</span><span class="sxs-lookup"><span data-stu-id="0ce2d-144">characters</span></span><br/>      |



 

## <a name="related-topics"></a><span data-ttu-id="0ce2d-145">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="0ce2d-145">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0ce2d-146">Especificação de esquema de impressão</span><span class="sxs-lookup"><span data-stu-id="0ce2d-146">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




