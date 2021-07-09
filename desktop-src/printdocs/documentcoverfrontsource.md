---
description: Obter informações sobre o parâmetro DocumentCoverFrontSource. Este tópico não é atual. Para obter as informações mais atuais, consulte a Especificação de Esquema de Impressão.
ms.assetid: ec41d0c8-ea77-44ac-a02b-6a48237b324f
title: DocumentCoverFrontSource
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: afeb6ecb089eb271e0b8fff136e73a20194f0c8f
ms.sourcegitcommit: 998d50f6def8a25850fc113fc8a2df903c829c5e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/09/2021
ms.locfileid: "113548754"
---
# <a name="documentcoverfrontsource"></a><span data-ttu-id="60319-105">DocumentCoverFrontSource</span><span class="sxs-lookup"><span data-stu-id="60319-105">DocumentCoverFrontSource</span></span>

<span data-ttu-id="60319-106">Este tópico não é atual.</span><span class="sxs-lookup"><span data-stu-id="60319-106">This topic is not current.</span></span> <span data-ttu-id="60319-107">Para obter as informações mais atuais, consulte a [Especificação de Esquema de Impressão](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="60319-107">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="60319-108">Especifica a origem de uma folha de front-cover personalizada.</span><span class="sxs-lookup"><span data-stu-id="60319-108">Specifies the source for a custom front-cover sheet.</span></span>

-   [<span data-ttu-id="60319-109">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="60319-109">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="60319-110">Conteúdo da estrutura</span><span class="sxs-lookup"><span data-stu-id="60319-110">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="60319-111">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="60319-111">Element Information</span></span>



| <span data-ttu-id="60319-112">Nome</span><span class="sxs-lookup"><span data-stu-id="60319-112">Name</span></span> | <span data-ttu-id="60319-113">Valor</span><span class="sxs-lookup"><span data-stu-id="60319-113">Value</span></span> |
|----------------------------|-------------------------------------------------|
| <span data-ttu-id="60319-114">Tipo de elemento</span><span class="sxs-lookup"><span data-stu-id="60319-114">Element Type</span></span> <br/>   | <span data-ttu-id="60319-115">ParameterDef</span><span class="sxs-lookup"><span data-stu-id="60319-115">ParameterDef</span></span><br/>                         |
| <span data-ttu-id="60319-116">Prefixo de definição de scoping</span><span class="sxs-lookup"><span data-stu-id="60319-116">Scoping Prefix</span></span> <br/> | <span data-ttu-id="60319-117">Documento</span><span class="sxs-lookup"><span data-stu-id="60319-117">Document</span></span><br/>                             |
| <span data-ttu-id="60319-118">Observações</span><span class="sxs-lookup"><span data-stu-id="60319-118">Notes</span></span> <br/>          | <span data-ttu-id="60319-119">Vinculado ao elemento DocumentCoverFront</span><span class="sxs-lookup"><span data-stu-id="60319-119">Linked to DocumentCoverFront element</span></span><br/> |



 

## <a name="structure-content"></a><span data-ttu-id="60319-120">Conteúdo da estrutura</span><span class="sxs-lookup"><span data-stu-id="60319-120">Structure Content</span></span>

<span data-ttu-id="60319-121">A estrutura XML desse elemento é:</span><span class="sxs-lookup"><span data-stu-id="60319-121">The XML structure of this element is:</span></span>

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

## <a name="structure-properties"></a><span data-ttu-id="60319-122">Propriedades da estrutura</span><span class="sxs-lookup"><span data-stu-id="60319-122">Structure Properties</span></span>

<span data-ttu-id="60319-123">A tabela a seguir descreve as características das variáveis definidas na estrutura XML.</span><span class="sxs-lookup"><span data-stu-id="60319-123">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="60319-124">Propriedade</span><span class="sxs-lookup"><span data-stu-id="60319-124">Property</span></span>                | <span data-ttu-id="60319-125">xsi:type</span><span class="sxs-lookup"><span data-stu-id="60319-125">xsi:type</span></span>           | <span data-ttu-id="60319-126">Valor</span><span class="sxs-lookup"><span data-stu-id="60319-126">Value</span></span>                      |
|-------------------------|--------------------|----------------------------|
| <span data-ttu-id="60319-127">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="60319-127">DataType</span></span><br/>     | <span data-ttu-id="60319-128">string</span><span class="sxs-lookup"><span data-stu-id="60319-128">string</span></span><br/>  | <span data-ttu-id="60319-129">xs:string</span><span class="sxs-lookup"><span data-stu-id="60319-129">xs:string</span></span><br/>       |
| <span data-ttu-id="60319-130">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="60319-130">DefaultValue</span></span><br/> | <span data-ttu-id="60319-131">string</span><span class="sxs-lookup"><span data-stu-id="60319-131">string</span></span><br/>  | <span data-ttu-id="60319-132">não definido</span><span class="sxs-lookup"><span data-stu-id="60319-132">undefined</span></span><br/>       |
| <span data-ttu-id="60319-133">MaxLength</span><span class="sxs-lookup"><span data-stu-id="60319-133">MaxLength</span></span><br/>    | <span data-ttu-id="60319-134">Número inteiro</span><span class="sxs-lookup"><span data-stu-id="60319-134">integer</span></span><br/> | <span data-ttu-id="60319-135">não definido</span><span class="sxs-lookup"><span data-stu-id="60319-135">undefined</span></span><br/>       |
| <span data-ttu-id="60319-136">Minlength</span><span class="sxs-lookup"><span data-stu-id="60319-136">MinLength</span></span><br/>    | <span data-ttu-id="60319-137">integer</span><span class="sxs-lookup"><span data-stu-id="60319-137">integer</span></span><br/> | <span data-ttu-id="60319-138">1</span><span class="sxs-lookup"><span data-stu-id="60319-138">1</span></span><br/>               |
| <span data-ttu-id="60319-139">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="60319-139">Mandatory</span></span><br/>    | <span data-ttu-id="60319-140">string</span><span class="sxs-lookup"><span data-stu-id="60319-140">string</span></span><br/>  | <span data-ttu-id="60319-141">psk:Conditional</span><span class="sxs-lookup"><span data-stu-id="60319-141">psk:Conditional</span></span><br/> |
| <span data-ttu-id="60319-142">Unittype</span><span class="sxs-lookup"><span data-stu-id="60319-142">UnitType</span></span><br/>     | <span data-ttu-id="60319-143">string</span><span class="sxs-lookup"><span data-stu-id="60319-143">string</span></span><br/>  | <span data-ttu-id="60319-144">characters</span><span class="sxs-lookup"><span data-stu-id="60319-144">characters</span></span><br/>      |



 

## <a name="related-topics"></a><span data-ttu-id="60319-145">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="60319-145">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="60319-146">Especificação de esquema de impressão</span><span class="sxs-lookup"><span data-stu-id="60319-146">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




