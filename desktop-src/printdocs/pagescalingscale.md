---
description: Este tópico não é atual. Para obter as informações mais atuais, consulte a especificação do esquema de impressão.
ms.assetid: 49a60a94-fb65-4439-bebf-3f77ea0861fe
title: PageScalingScale
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 246f77c5878b74e1b149c6d4020230030fb3c5b0
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/05/2021
ms.locfileid: "105813984"
---
# <a name="pagescalingscale"></a><span data-ttu-id="f05c3-104">PageScalingScale</span><span class="sxs-lookup"><span data-stu-id="f05c3-104">PageScalingScale</span></span>

<span data-ttu-id="f05c3-105">Este tópico não é atual.</span><span class="sxs-lookup"><span data-stu-id="f05c3-105">This topic is not current.</span></span> <span data-ttu-id="f05c3-106">Para obter as informações mais atuais, consulte a [especificação do esquema de impressão](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="f05c3-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="f05c3-107">Especifica o fator de dimensionamento para o dimensionamento quadrado personalizado.</span><span class="sxs-lookup"><span data-stu-id="f05c3-107">Specifies the scaling factor for custom square scaling.</span></span>

-   [<span data-ttu-id="f05c3-108">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="f05c3-108">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="f05c3-109">Conteúdo da estrutura</span><span class="sxs-lookup"><span data-stu-id="f05c3-109">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="f05c3-110">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="f05c3-110">Element Information</span></span>



| <span data-ttu-id="f05c3-111">Nome</span><span class="sxs-lookup"><span data-stu-id="f05c3-111">Name</span></span>                       |                                                         |
|----------------------------|---------------------------------------------------------|
| <span data-ttu-id="f05c3-112">Tipo de elemento</span><span class="sxs-lookup"><span data-stu-id="f05c3-112">Element Type</span></span> <br/>   | <span data-ttu-id="f05c3-113">ParameterDef</span><span class="sxs-lookup"><span data-stu-id="f05c3-113">ParameterDef</span></span><br/>                                 |
| <span data-ttu-id="f05c3-114">Prefixo de escopo</span><span class="sxs-lookup"><span data-stu-id="f05c3-114">Scoping Prefix</span></span> <br/> | <span data-ttu-id="f05c3-115">?</span><span class="sxs-lookup"><span data-stu-id="f05c3-115">Page</span></span><br/>                                         |
| <span data-ttu-id="f05c3-116">Observações</span><span class="sxs-lookup"><span data-stu-id="f05c3-116">Notes</span></span> <br/>          | <span data-ttu-id="f05c3-117">Vinculado ao elemento PageScaling, opção personalizada</span><span class="sxs-lookup"><span data-stu-id="f05c3-117">Linked to PageScaling element, Custom option</span></span><br/> |



 

## <a name="structure-content"></a><span data-ttu-id="f05c3-118">Conteúdo da estrutura</span><span class="sxs-lookup"><span data-stu-id="f05c3-118">Structure Content</span></span>

<span data-ttu-id="f05c3-119">A estrutura XML desse elemento é:</span><span class="sxs-lookup"><span data-stu-id="f05c3-119">The XML structure of this element is:</span></span>

``` syntax
<psf:ParameterDef name="psk:PageScalingScale">
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

## <a name="structure-properties"></a><span data-ttu-id="f05c3-120">Propriedades da estrutura</span><span class="sxs-lookup"><span data-stu-id="f05c3-120">Structure Properties</span></span>

<span data-ttu-id="f05c3-121">A tabela a seguir descreve as características das variáveis definidas na estrutura XML.</span><span class="sxs-lookup"><span data-stu-id="f05c3-121">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="f05c3-122">Propriedade</span><span class="sxs-lookup"><span data-stu-id="f05c3-122">Property</span></span>                | <span data-ttu-id="f05c3-123">xsi:type</span><span class="sxs-lookup"><span data-stu-id="f05c3-123">xsi:type</span></span>           | <span data-ttu-id="f05c3-124">Valor</span><span class="sxs-lookup"><span data-stu-id="f05c3-124">Value</span></span>                      |
|-------------------------|--------------------|----------------------------|
| <span data-ttu-id="f05c3-125">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="f05c3-125">DataType</span></span><br/>     | <span data-ttu-id="f05c3-126">string</span><span class="sxs-lookup"><span data-stu-id="f05c3-126">string</span></span><br/>  | <span data-ttu-id="f05c3-127">xs:integer</span><span class="sxs-lookup"><span data-stu-id="f05c3-127">xs:integer</span></span><br/>      |
| <span data-ttu-id="f05c3-128">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="f05c3-128">DefaultValue</span></span><br/> | <span data-ttu-id="f05c3-129">Número inteiro</span><span class="sxs-lookup"><span data-stu-id="f05c3-129">integer</span></span><br/> | <span data-ttu-id="f05c3-130">não definido</span><span class="sxs-lookup"><span data-stu-id="f05c3-130">undefined</span></span><br/>       |
| <span data-ttu-id="f05c3-131">MaxValue</span><span class="sxs-lookup"><span data-stu-id="f05c3-131">MaxValue</span></span><br/>     | <span data-ttu-id="f05c3-132">Número inteiro</span><span class="sxs-lookup"><span data-stu-id="f05c3-132">integer</span></span><br/> | <span data-ttu-id="f05c3-133">não definido</span><span class="sxs-lookup"><span data-stu-id="f05c3-133">undefined</span></span><br/>       |
| <span data-ttu-id="f05c3-134">MinValue</span><span class="sxs-lookup"><span data-stu-id="f05c3-134">MinValue</span></span><br/>     | <span data-ttu-id="f05c3-135">integer</span><span class="sxs-lookup"><span data-stu-id="f05c3-135">integer</span></span><br/> | <span data-ttu-id="f05c3-136">1</span><span class="sxs-lookup"><span data-stu-id="f05c3-136">1</span></span><br/>               |
| <span data-ttu-id="f05c3-137">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="f05c3-137">Mandatory</span></span><br/>    | <span data-ttu-id="f05c3-138">string</span><span class="sxs-lookup"><span data-stu-id="f05c3-138">string</span></span><br/>  | <span data-ttu-id="f05c3-139">PSK: condicional</span><span class="sxs-lookup"><span data-stu-id="f05c3-139">psk:Conditional</span></span><br/> |
| <span data-ttu-id="f05c3-140">Vários</span><span class="sxs-lookup"><span data-stu-id="f05c3-140">Multiple</span></span><br/>     | <span data-ttu-id="f05c3-141">integer</span><span class="sxs-lookup"><span data-stu-id="f05c3-141">integer</span></span><br/> | <span data-ttu-id="f05c3-142">1</span><span class="sxs-lookup"><span data-stu-id="f05c3-142">1</span></span><br/>               |
| <span data-ttu-id="f05c3-143">UnitType</span><span class="sxs-lookup"><span data-stu-id="f05c3-143">UnitType</span></span><br/>     | <span data-ttu-id="f05c3-144">string</span><span class="sxs-lookup"><span data-stu-id="f05c3-144">string</span></span><br/>  | <span data-ttu-id="f05c3-145">{1&gt;percent&lt;1}</span><span class="sxs-lookup"><span data-stu-id="f05c3-145">percent</span></span><br/>         |



 

## <a name="related-topics"></a><span data-ttu-id="f05c3-146">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="f05c3-146">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f05c3-147">Especificação de esquema de impressão</span><span class="sxs-lookup"><span data-stu-id="f05c3-147">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




