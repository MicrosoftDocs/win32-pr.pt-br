---
description: Este tópico não é atual. Para obter as informações mais atuais, consulte a especificação do esquema de impressão.
ms.assetid: ec41d0c8-ea77-44ac-a02b-6a48237b324f
title: DocumentCoverFrontSource
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 15b558a044716c5c13ae012665193f958f8ce6aa
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/26/2021
ms.locfileid: "107997893"
---
# <a name="documentcoverfrontsource"></a><span data-ttu-id="d1844-104">DocumentCoverFrontSource</span><span class="sxs-lookup"><span data-stu-id="d1844-104">DocumentCoverFrontSource</span></span>

<span data-ttu-id="d1844-105">Este tópico não é atual.</span><span class="sxs-lookup"><span data-stu-id="d1844-105">This topic is not current.</span></span> <span data-ttu-id="d1844-106">Para obter as informações mais atuais, consulte a [especificação do esquema de impressão](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="d1844-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="d1844-107">Especifica a origem de uma folha de capa personalizada.</span><span class="sxs-lookup"><span data-stu-id="d1844-107">Specifies the source for a custom front-cover sheet.</span></span>

-   [<span data-ttu-id="d1844-108">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="d1844-108">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="d1844-109">Conteúdo da estrutura</span><span class="sxs-lookup"><span data-stu-id="d1844-109">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="d1844-110">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="d1844-110">Element Information</span></span>



| <span data-ttu-id="d1844-111">Nome</span><span class="sxs-lookup"><span data-stu-id="d1844-111">Name</span></span> | <span data-ttu-id="d1844-112">Valor</span><span class="sxs-lookup"><span data-stu-id="d1844-112">Value</span></span> |
|----------------------------|-------------------------------------------------|
| <span data-ttu-id="d1844-113">Tipo de elemento</span><span class="sxs-lookup"><span data-stu-id="d1844-113">Element Type</span></span> <br/>   | <span data-ttu-id="d1844-114">ParameterDef</span><span class="sxs-lookup"><span data-stu-id="d1844-114">ParameterDef</span></span><br/>                         |
| <span data-ttu-id="d1844-115">Prefixo de escopo</span><span class="sxs-lookup"><span data-stu-id="d1844-115">Scoping Prefix</span></span> <br/> | <span data-ttu-id="d1844-116">Documento</span><span class="sxs-lookup"><span data-stu-id="d1844-116">Document</span></span><br/>                             |
| <span data-ttu-id="d1844-117">Observações</span><span class="sxs-lookup"><span data-stu-id="d1844-117">Notes</span></span> <br/>          | <span data-ttu-id="d1844-118">Vinculado ao elemento DocumentCoverFront</span><span class="sxs-lookup"><span data-stu-id="d1844-118">Linked to DocumentCoverFront element</span></span><br/> |



 

## <a name="structure-content"></a><span data-ttu-id="d1844-119">Conteúdo da estrutura</span><span class="sxs-lookup"><span data-stu-id="d1844-119">Structure Content</span></span>

<span data-ttu-id="d1844-120">A estrutura XML desse elemento é:</span><span class="sxs-lookup"><span data-stu-id="d1844-120">The XML structure of this element is:</span></span>

``` syntax
<psf:ParameterDef name="psk:DocumentCoverFrontSource">
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

## <a name="structure-properties"></a><span data-ttu-id="d1844-121">Propriedades da estrutura</span><span class="sxs-lookup"><span data-stu-id="d1844-121">Structure Properties</span></span>

<span data-ttu-id="d1844-122">A tabela a seguir descreve as características das variáveis definidas na estrutura XML.</span><span class="sxs-lookup"><span data-stu-id="d1844-122">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="d1844-123">Propriedade</span><span class="sxs-lookup"><span data-stu-id="d1844-123">Property</span></span>                | <span data-ttu-id="d1844-124">xsi:type</span><span class="sxs-lookup"><span data-stu-id="d1844-124">xsi:type</span></span>           | <span data-ttu-id="d1844-125">Valor</span><span class="sxs-lookup"><span data-stu-id="d1844-125">Value</span></span>                      |
|-------------------------|--------------------|----------------------------|
| <span data-ttu-id="d1844-126">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="d1844-126">DataType</span></span><br/>     | <span data-ttu-id="d1844-127">string</span><span class="sxs-lookup"><span data-stu-id="d1844-127">string</span></span><br/>  | <span data-ttu-id="d1844-128">xs:string</span><span class="sxs-lookup"><span data-stu-id="d1844-128">xs:string</span></span><br/>       |
| <span data-ttu-id="d1844-129">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="d1844-129">DefaultValue</span></span><br/> | <span data-ttu-id="d1844-130">string</span><span class="sxs-lookup"><span data-stu-id="d1844-130">string</span></span><br/>  | <span data-ttu-id="d1844-131">não definido</span><span class="sxs-lookup"><span data-stu-id="d1844-131">undefined</span></span><br/>       |
| <span data-ttu-id="d1844-132">MaxLength</span><span class="sxs-lookup"><span data-stu-id="d1844-132">MaxLength</span></span><br/>    | <span data-ttu-id="d1844-133">Número inteiro</span><span class="sxs-lookup"><span data-stu-id="d1844-133">integer</span></span><br/> | <span data-ttu-id="d1844-134">não definido</span><span class="sxs-lookup"><span data-stu-id="d1844-134">undefined</span></span><br/>       |
| <span data-ttu-id="d1844-135">MinLength</span><span class="sxs-lookup"><span data-stu-id="d1844-135">MinLength</span></span><br/>    | <span data-ttu-id="d1844-136">integer</span><span class="sxs-lookup"><span data-stu-id="d1844-136">integer</span></span><br/> | <span data-ttu-id="d1844-137">1</span><span class="sxs-lookup"><span data-stu-id="d1844-137">1</span></span><br/>               |
| <span data-ttu-id="d1844-138">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="d1844-138">Mandatory</span></span><br/>    | <span data-ttu-id="d1844-139">string</span><span class="sxs-lookup"><span data-stu-id="d1844-139">string</span></span><br/>  | <span data-ttu-id="d1844-140">PSK: condicional</span><span class="sxs-lookup"><span data-stu-id="d1844-140">psk:Conditional</span></span><br/> |
| <span data-ttu-id="d1844-141">UnitType</span><span class="sxs-lookup"><span data-stu-id="d1844-141">UnitType</span></span><br/>     | <span data-ttu-id="d1844-142">string</span><span class="sxs-lookup"><span data-stu-id="d1844-142">string</span></span><br/>  | <span data-ttu-id="d1844-143">characters</span><span class="sxs-lookup"><span data-stu-id="d1844-143">characters</span></span><br/>      |



 

## <a name="related-topics"></a><span data-ttu-id="d1844-144">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="d1844-144">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d1844-145">Especificação de esquema de impressão</span><span class="sxs-lookup"><span data-stu-id="d1844-145">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




