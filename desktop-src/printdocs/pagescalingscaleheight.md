---
description: Este tópico não é atual. Para obter as informações mais atuais, consulte a especificação do esquema de impressão.
ms.assetid: ccc2ad1c-b0c2-4c45-bc95-7c15426c2534
title: PageScalingScaleHeight
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 92d718d80f6b3cc369ddcb5c088a1299d639634b
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/26/2021
ms.locfileid: "107997473"
---
# <a name="pagescalingscaleheight"></a><span data-ttu-id="d4302-104">PageScalingScaleHeight</span><span class="sxs-lookup"><span data-stu-id="d4302-104">PageScalingScaleHeight</span></span>

<span data-ttu-id="d4302-105">Este tópico não é atual.</span><span class="sxs-lookup"><span data-stu-id="d4302-105">This topic is not current.</span></span> <span data-ttu-id="d4302-106">Para obter as informações mais atuais, consulte a [especificação do esquema de impressão](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="d4302-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="d4302-107">Especifica o fator de dimensionamento na direção do ImageableSizeHeight para o dimensionamento personalizado.</span><span class="sxs-lookup"><span data-stu-id="d4302-107">Specifies the scaling factor in the ImageableSizeHeight direction for custom scaling.</span></span>

-   [<span data-ttu-id="d4302-108">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="d4302-108">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="d4302-109">Conteúdo da estrutura</span><span class="sxs-lookup"><span data-stu-id="d4302-109">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="d4302-110">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="d4302-110">Element Information</span></span>



| <span data-ttu-id="d4302-111">Nome</span><span class="sxs-lookup"><span data-stu-id="d4302-111">Name</span></span> | <span data-ttu-id="d4302-112">Valor</span><span class="sxs-lookup"><span data-stu-id="d4302-112">Value</span></span> |
|----------------------------|---------------------------------------------------------|
| <span data-ttu-id="d4302-113">Tipo de elemento</span><span class="sxs-lookup"><span data-stu-id="d4302-113">Element Type</span></span> <br/>   | <span data-ttu-id="d4302-114">ParameterDef</span><span class="sxs-lookup"><span data-stu-id="d4302-114">ParameterDef</span></span><br/>                                 |
| <span data-ttu-id="d4302-115">Prefixo de escopo</span><span class="sxs-lookup"><span data-stu-id="d4302-115">Scoping Prefix</span></span> <br/> | <span data-ttu-id="d4302-116">?</span><span class="sxs-lookup"><span data-stu-id="d4302-116">Page</span></span><br/>                                         |
| <span data-ttu-id="d4302-117">Observações</span><span class="sxs-lookup"><span data-stu-id="d4302-117">Notes</span></span> <br/>          | <span data-ttu-id="d4302-118">Vinculado ao elemento PageScaling, opção personalizada</span><span class="sxs-lookup"><span data-stu-id="d4302-118">Linked to PageScaling element, Custom option</span></span><br/> |



 

## <a name="structure-content"></a><span data-ttu-id="d4302-119">Conteúdo da estrutura</span><span class="sxs-lookup"><span data-stu-id="d4302-119">Structure Content</span></span>

<span data-ttu-id="d4302-120">A estrutura XML desse elemento é:</span><span class="sxs-lookup"><span data-stu-id="d4302-120">The XML structure of this element is:</span></span>

``` syntax
<psf:ParameterDef name="psk:PageScalingScaleHeight">
  <psf:Property name="psf:DataType">
    <psf:Value xsi:type="xs:string">xs:integer</psf:Value>
  </psf:Property>
  <psf:Property name="psf:DefaultValue">
    <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
  </psf:Property>
  <psf:Property name="psf:MaxValue">
    <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
  </psf:Property>
  <psf:Property name="psf:MinValue">
    <psf:Value xsi:type="xs:integer">1</psf:Value>
  </psf:Property>
  <psf:Property name="psf:Multiple">
    <psf:Value xsi:type="xs:integer">1</psf:Value>
  </psf:Property>
  <psf:Property name="psf:Mandatory">
    <psf:Value xsi:type="xs:string">psk:Conditional</psf:Value>
  </psf:Property>
  <psf:Property name="psf:UnitType">
    <psf:Value xsi:type="xs:string">percent</psf:Value>
  </psf:Property>
</psf:ParameterDef>
      
```

## <a name="structure-properties"></a><span data-ttu-id="d4302-121">Propriedades da estrutura</span><span class="sxs-lookup"><span data-stu-id="d4302-121">Structure Properties</span></span>

<span data-ttu-id="d4302-122">A tabela a seguir descreve as características das variáveis definidas na estrutura XML.</span><span class="sxs-lookup"><span data-stu-id="d4302-122">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="d4302-123">Propriedade</span><span class="sxs-lookup"><span data-stu-id="d4302-123">Property</span></span>                | <span data-ttu-id="d4302-124">xsi:type</span><span class="sxs-lookup"><span data-stu-id="d4302-124">xsi:type</span></span>           | <span data-ttu-id="d4302-125">Valor</span><span class="sxs-lookup"><span data-stu-id="d4302-125">Value</span></span>                      |
|-------------------------|--------------------|----------------------------|
| <span data-ttu-id="d4302-126">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="d4302-126">DataType</span></span><br/>     | <span data-ttu-id="d4302-127">String</span><span class="sxs-lookup"><span data-stu-id="d4302-127">String</span></span><br/>  | <span data-ttu-id="d4302-128">xs:integer</span><span class="sxs-lookup"><span data-stu-id="d4302-128">xs:integer</span></span><br/>      |
| <span data-ttu-id="d4302-129">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="d4302-129">DefaultValue</span></span><br/> | <span data-ttu-id="d4302-130">Integer</span><span class="sxs-lookup"><span data-stu-id="d4302-130">Integer</span></span><br/> | <span data-ttu-id="d4302-131">não definido</span><span class="sxs-lookup"><span data-stu-id="d4302-131">undefined</span></span><br/>       |
| <span data-ttu-id="d4302-132">MaxValue</span><span class="sxs-lookup"><span data-stu-id="d4302-132">MaxValue</span></span><br/>     | <span data-ttu-id="d4302-133">Integer</span><span class="sxs-lookup"><span data-stu-id="d4302-133">Integer</span></span><br/> | <span data-ttu-id="d4302-134">não definido</span><span class="sxs-lookup"><span data-stu-id="d4302-134">undefined</span></span><br/>       |
| <span data-ttu-id="d4302-135">MinValue</span><span class="sxs-lookup"><span data-stu-id="d4302-135">MinValue</span></span><br/>     | <span data-ttu-id="d4302-136">Integer</span><span class="sxs-lookup"><span data-stu-id="d4302-136">Integer</span></span><br/> | <span data-ttu-id="d4302-137">1</span><span class="sxs-lookup"><span data-stu-id="d4302-137">1</span></span><br/>               |
| <span data-ttu-id="d4302-138">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="d4302-138">Mandatory</span></span><br/>    | <span data-ttu-id="d4302-139">String</span><span class="sxs-lookup"><span data-stu-id="d4302-139">String</span></span><br/>  | <span data-ttu-id="d4302-140">PSK: condicional</span><span class="sxs-lookup"><span data-stu-id="d4302-140">psk:Conditional</span></span><br/> |
| <span data-ttu-id="d4302-141">Vários</span><span class="sxs-lookup"><span data-stu-id="d4302-141">Multiple</span></span><br/>     | <span data-ttu-id="d4302-142">Integer</span><span class="sxs-lookup"><span data-stu-id="d4302-142">Integer</span></span><br/> | <span data-ttu-id="d4302-143">1</span><span class="sxs-lookup"><span data-stu-id="d4302-143">1</span></span><br/>               |
| <span data-ttu-id="d4302-144">UnitType</span><span class="sxs-lookup"><span data-stu-id="d4302-144">UnitType</span></span><br/>     | <span data-ttu-id="d4302-145">String</span><span class="sxs-lookup"><span data-stu-id="d4302-145">String</span></span><br/>  | <span data-ttu-id="d4302-146">{1&gt;percent&lt;1}</span><span class="sxs-lookup"><span data-stu-id="d4302-146">percent</span></span><br/>         |



 

## <a name="related-topics"></a><span data-ttu-id="d4302-147">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="d4302-147">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d4302-148">Especificação de esquema de impressão</span><span class="sxs-lookup"><span data-stu-id="d4302-148">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




