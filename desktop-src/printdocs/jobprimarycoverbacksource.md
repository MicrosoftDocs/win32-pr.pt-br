---
description: Este tópico não é atual. Para obter as informações mais atuais, consulte a especificação do esquema de impressão.
ms.assetid: b5c8e79c-cdae-4c53-b594-915726423b4f
title: JobPrimaryCoverBackSource
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2145bae0843323928d8a7d016fc61f10c0e388ac
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/26/2021
ms.locfileid: "107993973"
---
# <a name="jobprimarycoverbacksource"></a><span data-ttu-id="0d723-104">JobPrimaryCoverBackSource</span><span class="sxs-lookup"><span data-stu-id="0d723-104">JobPrimaryCoverBackSource</span></span>

<span data-ttu-id="0d723-105">Este tópico não é atual.</span><span class="sxs-lookup"><span data-stu-id="0d723-105">This topic is not current.</span></span> <span data-ttu-id="0d723-106">Para obter as informações mais atuais, consulte a [especificação do esquema de impressão](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="0d723-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="0d723-107">Especifica a origem de uma folha primária de capa de fundo personalizada para o trabalho.</span><span class="sxs-lookup"><span data-stu-id="0d723-107">Specifies the source for a custom back-cover primary sheet for the job.</span></span>

-   [<span data-ttu-id="0d723-108">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="0d723-108">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="0d723-109">Conteúdo da estrutura</span><span class="sxs-lookup"><span data-stu-id="0d723-109">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="0d723-110">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="0d723-110">Element Information</span></span>



| <span data-ttu-id="0d723-111">Nome</span><span class="sxs-lookup"><span data-stu-id="0d723-111">Name</span></span> | <span data-ttu-id="0d723-112">Valor</span><span class="sxs-lookup"><span data-stu-id="0d723-112">Value</span></span> |
|----------------------------|-------------------------------------------|
| <span data-ttu-id="0d723-113">Tipo de elemento</span><span class="sxs-lookup"><span data-stu-id="0d723-113">Element Type</span></span> <br/>   | <span data-ttu-id="0d723-114">ParameterDef</span><span class="sxs-lookup"><span data-stu-id="0d723-114">ParameterDef</span></span><br/>                   |
| <span data-ttu-id="0d723-115">Prefixo de escopo</span><span class="sxs-lookup"><span data-stu-id="0d723-115">Scoping Prefix</span></span> <br/> | <span data-ttu-id="0d723-116">Trabalho</span><span class="sxs-lookup"><span data-stu-id="0d723-116">Job</span></span><br/>                            |
| <span data-ttu-id="0d723-117">Observações</span><span class="sxs-lookup"><span data-stu-id="0d723-117">Notes</span></span> <br/>          | <span data-ttu-id="0d723-118">Vinculado ao elemento JobCoverBack</span><span class="sxs-lookup"><span data-stu-id="0d723-118">Linked to JobCoverBack element</span></span><br/> |



 

## <a name="structure-content"></a><span data-ttu-id="0d723-119">Conteúdo da estrutura</span><span class="sxs-lookup"><span data-stu-id="0d723-119">Structure Content</span></span>

<span data-ttu-id="0d723-120">A estrutura XML desse elemento é:</span><span class="sxs-lookup"><span data-stu-id="0d723-120">The XML structure of this element is:</span></span>

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

## <a name="structure-properties"></a><span data-ttu-id="0d723-121">Propriedades da estrutura</span><span class="sxs-lookup"><span data-stu-id="0d723-121">Structure Properties</span></span>

<span data-ttu-id="0d723-122">A tabela a seguir descreve as características das variáveis definidas na estrutura XML.</span><span class="sxs-lookup"><span data-stu-id="0d723-122">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="0d723-123">Propriedade</span><span class="sxs-lookup"><span data-stu-id="0d723-123">Property</span></span>                | <span data-ttu-id="0d723-124">xsi:type</span><span class="sxs-lookup"><span data-stu-id="0d723-124">xsi:type</span></span>           | <span data-ttu-id="0d723-125">Valor</span><span class="sxs-lookup"><span data-stu-id="0d723-125">Value</span></span>                      |
|-------------------------|--------------------|----------------------------|
| <span data-ttu-id="0d723-126">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="0d723-126">DataType</span></span><br/>     | <span data-ttu-id="0d723-127">string</span><span class="sxs-lookup"><span data-stu-id="0d723-127">string</span></span><br/>  | <span data-ttu-id="0d723-128">xs:string</span><span class="sxs-lookup"><span data-stu-id="0d723-128">xs:string</span></span><br/>       |
| <span data-ttu-id="0d723-129">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="0d723-129">DefaultValue</span></span><br/> | <span data-ttu-id="0d723-130">string</span><span class="sxs-lookup"><span data-stu-id="0d723-130">string</span></span><br/>  | <span data-ttu-id="0d723-131">não definido</span><span class="sxs-lookup"><span data-stu-id="0d723-131">undefined</span></span><br/>       |
| <span data-ttu-id="0d723-132">MaxLength</span><span class="sxs-lookup"><span data-stu-id="0d723-132">MaxLength</span></span><br/>    | <span data-ttu-id="0d723-133">Número inteiro</span><span class="sxs-lookup"><span data-stu-id="0d723-133">integer</span></span><br/> | <span data-ttu-id="0d723-134">não definido</span><span class="sxs-lookup"><span data-stu-id="0d723-134">undefined</span></span><br/>       |
| <span data-ttu-id="0d723-135">MinLength</span><span class="sxs-lookup"><span data-stu-id="0d723-135">MinLength</span></span><br/>    | <span data-ttu-id="0d723-136">integer</span><span class="sxs-lookup"><span data-stu-id="0d723-136">integer</span></span><br/> | <span data-ttu-id="0d723-137">1</span><span class="sxs-lookup"><span data-stu-id="0d723-137">1</span></span><br/>               |
| <span data-ttu-id="0d723-138">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="0d723-138">Mandatory</span></span><br/>    | <span data-ttu-id="0d723-139">string</span><span class="sxs-lookup"><span data-stu-id="0d723-139">string</span></span><br/>  | <span data-ttu-id="0d723-140">PSK: condicional</span><span class="sxs-lookup"><span data-stu-id="0d723-140">psk:Conditional</span></span><br/> |
| <span data-ttu-id="0d723-141">UnitType</span><span class="sxs-lookup"><span data-stu-id="0d723-141">UnitType</span></span><br/>     | <span data-ttu-id="0d723-142">string</span><span class="sxs-lookup"><span data-stu-id="0d723-142">string</span></span><br/>  | <span data-ttu-id="0d723-143">characters</span><span class="sxs-lookup"><span data-stu-id="0d723-143">characters</span></span><br/>      |



 

## <a name="related-topics"></a><span data-ttu-id="0d723-144">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="0d723-144">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0d723-145">Especificação de esquema de impressão</span><span class="sxs-lookup"><span data-stu-id="0d723-145">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




