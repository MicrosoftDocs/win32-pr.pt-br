---
description: Este tópico não é atual. Para obter as informações mais atuais, consulte a especificação do esquema de impressão.
ms.assetid: b5c8e79c-cdae-4c53-b594-915726423b4f
title: JobPrimaryCoverBackSource
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1a8c15d5f5b8545b70f19bf181a00d05a8379212
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/05/2021
ms.locfileid: "104011968"
---
# <a name="jobprimarycoverbacksource"></a><span data-ttu-id="464ba-104">JobPrimaryCoverBackSource</span><span class="sxs-lookup"><span data-stu-id="464ba-104">JobPrimaryCoverBackSource</span></span>

<span data-ttu-id="464ba-105">Este tópico não é atual.</span><span class="sxs-lookup"><span data-stu-id="464ba-105">This topic is not current.</span></span> <span data-ttu-id="464ba-106">Para obter as informações mais atuais, consulte a [especificação do esquema de impressão](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="464ba-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="464ba-107">Especifica a origem de uma folha primária de capa de fundo personalizada para o trabalho.</span><span class="sxs-lookup"><span data-stu-id="464ba-107">Specifies the source for a custom back-cover primary sheet for the job.</span></span>

-   [<span data-ttu-id="464ba-108">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="464ba-108">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="464ba-109">Conteúdo da estrutura</span><span class="sxs-lookup"><span data-stu-id="464ba-109">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="464ba-110">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="464ba-110">Element Information</span></span>



| <span data-ttu-id="464ba-111">Nome</span><span class="sxs-lookup"><span data-stu-id="464ba-111">Name</span></span>                       |                                           |
|----------------------------|-------------------------------------------|
| <span data-ttu-id="464ba-112">Tipo de elemento</span><span class="sxs-lookup"><span data-stu-id="464ba-112">Element Type</span></span> <br/>   | <span data-ttu-id="464ba-113">ParameterDef</span><span class="sxs-lookup"><span data-stu-id="464ba-113">ParameterDef</span></span><br/>                   |
| <span data-ttu-id="464ba-114">Prefixo de escopo</span><span class="sxs-lookup"><span data-stu-id="464ba-114">Scoping Prefix</span></span> <br/> | <span data-ttu-id="464ba-115">Trabalho</span><span class="sxs-lookup"><span data-stu-id="464ba-115">Job</span></span><br/>                            |
| <span data-ttu-id="464ba-116">Observações</span><span class="sxs-lookup"><span data-stu-id="464ba-116">Notes</span></span> <br/>          | <span data-ttu-id="464ba-117">Vinculado ao elemento JobCoverBack</span><span class="sxs-lookup"><span data-stu-id="464ba-117">Linked to JobCoverBack element</span></span><br/> |



 

## <a name="structure-content"></a><span data-ttu-id="464ba-118">Conteúdo da estrutura</span><span class="sxs-lookup"><span data-stu-id="464ba-118">Structure Content</span></span>

<span data-ttu-id="464ba-119">A estrutura XML desse elemento é:</span><span class="sxs-lookup"><span data-stu-id="464ba-119">The XML structure of this element is:</span></span>

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

## <a name="structure-properties"></a><span data-ttu-id="464ba-120">Propriedades da estrutura</span><span class="sxs-lookup"><span data-stu-id="464ba-120">Structure Properties</span></span>

<span data-ttu-id="464ba-121">A tabela a seguir descreve as características das variáveis definidas na estrutura XML.</span><span class="sxs-lookup"><span data-stu-id="464ba-121">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="464ba-122">Propriedade</span><span class="sxs-lookup"><span data-stu-id="464ba-122">Property</span></span>                | <span data-ttu-id="464ba-123">xsi:type</span><span class="sxs-lookup"><span data-stu-id="464ba-123">xsi:type</span></span>           | <span data-ttu-id="464ba-124">Valor</span><span class="sxs-lookup"><span data-stu-id="464ba-124">Value</span></span>                      |
|-------------------------|--------------------|----------------------------|
| <span data-ttu-id="464ba-125">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="464ba-125">DataType</span></span><br/>     | <span data-ttu-id="464ba-126">string</span><span class="sxs-lookup"><span data-stu-id="464ba-126">string</span></span><br/>  | <span data-ttu-id="464ba-127">xs:string</span><span class="sxs-lookup"><span data-stu-id="464ba-127">xs:string</span></span><br/>       |
| <span data-ttu-id="464ba-128">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="464ba-128">DefaultValue</span></span><br/> | <span data-ttu-id="464ba-129">string</span><span class="sxs-lookup"><span data-stu-id="464ba-129">string</span></span><br/>  | <span data-ttu-id="464ba-130">não definido</span><span class="sxs-lookup"><span data-stu-id="464ba-130">undefined</span></span><br/>       |
| <span data-ttu-id="464ba-131">MaxLength</span><span class="sxs-lookup"><span data-stu-id="464ba-131">MaxLength</span></span><br/>    | <span data-ttu-id="464ba-132">Número inteiro</span><span class="sxs-lookup"><span data-stu-id="464ba-132">integer</span></span><br/> | <span data-ttu-id="464ba-133">não definido</span><span class="sxs-lookup"><span data-stu-id="464ba-133">undefined</span></span><br/>       |
| <span data-ttu-id="464ba-134">MinLength</span><span class="sxs-lookup"><span data-stu-id="464ba-134">MinLength</span></span><br/>    | <span data-ttu-id="464ba-135">integer</span><span class="sxs-lookup"><span data-stu-id="464ba-135">integer</span></span><br/> | <span data-ttu-id="464ba-136">1</span><span class="sxs-lookup"><span data-stu-id="464ba-136">1</span></span><br/>               |
| <span data-ttu-id="464ba-137">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="464ba-137">Mandatory</span></span><br/>    | <span data-ttu-id="464ba-138">string</span><span class="sxs-lookup"><span data-stu-id="464ba-138">string</span></span><br/>  | <span data-ttu-id="464ba-139">PSK: condicional</span><span class="sxs-lookup"><span data-stu-id="464ba-139">psk:Conditional</span></span><br/> |
| <span data-ttu-id="464ba-140">UnitType</span><span class="sxs-lookup"><span data-stu-id="464ba-140">UnitType</span></span><br/>     | <span data-ttu-id="464ba-141">string</span><span class="sxs-lookup"><span data-stu-id="464ba-141">string</span></span><br/>  | <span data-ttu-id="464ba-142">characters</span><span class="sxs-lookup"><span data-stu-id="464ba-142">characters</span></span><br/>      |



 

## <a name="related-topics"></a><span data-ttu-id="464ba-143">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="464ba-143">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="464ba-144">Especificação de esquema de impressão</span><span class="sxs-lookup"><span data-stu-id="464ba-144">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




