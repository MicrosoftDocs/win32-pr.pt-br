---
description: Obter informações sobre o parâmetro PageScalingScaleHeight. Este tópico não é atual. Para obter as informações mais atuais, consulte a Especificação de Esquema de Impressão.
ms.assetid: ccc2ad1c-b0c2-4c45-bc95-7c15426c2534
title: PageScalingScaleHeight
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d51bdb5577b5e3863cfadab1fa9eb74ff40d54da
ms.sourcegitcommit: 998d50f6def8a25850fc113fc8a2df903c829c5e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/09/2021
ms.locfileid: "113548834"
---
# <a name="pagescalingscaleheight"></a><span data-ttu-id="7d5de-105">PageScalingScaleHeight</span><span class="sxs-lookup"><span data-stu-id="7d5de-105">PageScalingScaleHeight</span></span>

<span data-ttu-id="7d5de-106">Este tópico não é atual.</span><span class="sxs-lookup"><span data-stu-id="7d5de-106">This topic is not current.</span></span> <span data-ttu-id="7d5de-107">Para obter as informações mais atuais, consulte a [Especificação de Esquema de Impressão](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="7d5de-107">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="7d5de-108">Especifica o fator de dimensionamento na direção ImageableSizeHeight para dimensionamento personalizado.</span><span class="sxs-lookup"><span data-stu-id="7d5de-108">Specifies the scaling factor in the ImageableSizeHeight direction for custom scaling.</span></span>

-   [<span data-ttu-id="7d5de-109">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="7d5de-109">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="7d5de-110">Conteúdo da estrutura</span><span class="sxs-lookup"><span data-stu-id="7d5de-110">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="7d5de-111">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="7d5de-111">Element Information</span></span>



| <span data-ttu-id="7d5de-112">Nome</span><span class="sxs-lookup"><span data-stu-id="7d5de-112">Name</span></span> | <span data-ttu-id="7d5de-113">Valor</span><span class="sxs-lookup"><span data-stu-id="7d5de-113">Value</span></span> |
|----------------------------|---------------------------------------------------------|
| <span data-ttu-id="7d5de-114">Tipo de elemento</span><span class="sxs-lookup"><span data-stu-id="7d5de-114">Element Type</span></span> <br/>   | <span data-ttu-id="7d5de-115">ParameterDef</span><span class="sxs-lookup"><span data-stu-id="7d5de-115">ParameterDef</span></span><br/>                                 |
| <span data-ttu-id="7d5de-116">Prefixo de definição de scoping</span><span class="sxs-lookup"><span data-stu-id="7d5de-116">Scoping Prefix</span></span> <br/> | <span data-ttu-id="7d5de-117">Página</span><span class="sxs-lookup"><span data-stu-id="7d5de-117">Page</span></span><br/>                                         |
| <span data-ttu-id="7d5de-118">Observações</span><span class="sxs-lookup"><span data-stu-id="7d5de-118">Notes</span></span> <br/>          | <span data-ttu-id="7d5de-119">Vinculado ao elemento PageScaling, opção Personalizada</span><span class="sxs-lookup"><span data-stu-id="7d5de-119">Linked to PageScaling element, Custom option</span></span><br/> |



 

## <a name="structure-content"></a><span data-ttu-id="7d5de-120">Conteúdo da estrutura</span><span class="sxs-lookup"><span data-stu-id="7d5de-120">Structure Content</span></span>

<span data-ttu-id="7d5de-121">A estrutura XML desse elemento é:</span><span class="sxs-lookup"><span data-stu-id="7d5de-121">The XML structure of this element is:</span></span>

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

## <a name="structure-properties"></a><span data-ttu-id="7d5de-122">Propriedades da estrutura</span><span class="sxs-lookup"><span data-stu-id="7d5de-122">Structure Properties</span></span>

<span data-ttu-id="7d5de-123">A tabela a seguir descreve as características das variáveis definidas na estrutura XML.</span><span class="sxs-lookup"><span data-stu-id="7d5de-123">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="7d5de-124">Propriedade</span><span class="sxs-lookup"><span data-stu-id="7d5de-124">Property</span></span>                | <span data-ttu-id="7d5de-125">xsi:type</span><span class="sxs-lookup"><span data-stu-id="7d5de-125">xsi:type</span></span>           | <span data-ttu-id="7d5de-126">Valor</span><span class="sxs-lookup"><span data-stu-id="7d5de-126">Value</span></span>                      |
|-------------------------|--------------------|----------------------------|
| <span data-ttu-id="7d5de-127">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="7d5de-127">DataType</span></span><br/>     | <span data-ttu-id="7d5de-128">String</span><span class="sxs-lookup"><span data-stu-id="7d5de-128">String</span></span><br/>  | <span data-ttu-id="7d5de-129">xs:integer</span><span class="sxs-lookup"><span data-stu-id="7d5de-129">xs:integer</span></span><br/>      |
| <span data-ttu-id="7d5de-130">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="7d5de-130">DefaultValue</span></span><br/> | <span data-ttu-id="7d5de-131">Integer</span><span class="sxs-lookup"><span data-stu-id="7d5de-131">Integer</span></span><br/> | <span data-ttu-id="7d5de-132">não definido</span><span class="sxs-lookup"><span data-stu-id="7d5de-132">undefined</span></span><br/>       |
| <span data-ttu-id="7d5de-133">MaxValue</span><span class="sxs-lookup"><span data-stu-id="7d5de-133">MaxValue</span></span><br/>     | <span data-ttu-id="7d5de-134">Integer</span><span class="sxs-lookup"><span data-stu-id="7d5de-134">Integer</span></span><br/> | <span data-ttu-id="7d5de-135">não definido</span><span class="sxs-lookup"><span data-stu-id="7d5de-135">undefined</span></span><br/>       |
| <span data-ttu-id="7d5de-136">Minvalue</span><span class="sxs-lookup"><span data-stu-id="7d5de-136">MinValue</span></span><br/>     | <span data-ttu-id="7d5de-137">Integer</span><span class="sxs-lookup"><span data-stu-id="7d5de-137">Integer</span></span><br/> | <span data-ttu-id="7d5de-138">1</span><span class="sxs-lookup"><span data-stu-id="7d5de-138">1</span></span><br/>               |
| <span data-ttu-id="7d5de-139">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="7d5de-139">Mandatory</span></span><br/>    | <span data-ttu-id="7d5de-140">String</span><span class="sxs-lookup"><span data-stu-id="7d5de-140">String</span></span><br/>  | <span data-ttu-id="7d5de-141">psk:Conditional</span><span class="sxs-lookup"><span data-stu-id="7d5de-141">psk:Conditional</span></span><br/> |
| <span data-ttu-id="7d5de-142">Vários</span><span class="sxs-lookup"><span data-stu-id="7d5de-142">Multiple</span></span><br/>     | <span data-ttu-id="7d5de-143">Integer</span><span class="sxs-lookup"><span data-stu-id="7d5de-143">Integer</span></span><br/> | <span data-ttu-id="7d5de-144">1</span><span class="sxs-lookup"><span data-stu-id="7d5de-144">1</span></span><br/>               |
| <span data-ttu-id="7d5de-145">Unittype</span><span class="sxs-lookup"><span data-stu-id="7d5de-145">UnitType</span></span><br/>     | <span data-ttu-id="7d5de-146">String</span><span class="sxs-lookup"><span data-stu-id="7d5de-146">String</span></span><br/>  | <span data-ttu-id="7d5de-147">{1&gt;percent&lt;1}</span><span class="sxs-lookup"><span data-stu-id="7d5de-147">percent</span></span><br/>         |



 

## <a name="related-topics"></a><span data-ttu-id="7d5de-148">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="7d5de-148">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7d5de-149">Especificação de esquema de impressão</span><span class="sxs-lookup"><span data-stu-id="7d5de-149">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




