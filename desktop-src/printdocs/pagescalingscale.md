---
description: Obtenha informações sobre o parâmetro PageScalingScale. Este tópico não é atual. Para obter as informações mais atuais, consulte a especificação do esquema de impressão.
ms.assetid: 49a60a94-fb65-4439-bebf-3f77ea0861fe
title: PageScalingScale
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d8c6cee5fc46568e3cf7f15ecd43c07c6584c856
ms.sourcegitcommit: 998d50f6def8a25850fc113fc8a2df903c829c5e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/09/2021
ms.locfileid: "113548824"
---
# <a name="pagescalingscale"></a><span data-ttu-id="c646d-105">PageScalingScale</span><span class="sxs-lookup"><span data-stu-id="c646d-105">PageScalingScale</span></span>

<span data-ttu-id="c646d-106">Este tópico não é atual.</span><span class="sxs-lookup"><span data-stu-id="c646d-106">This topic is not current.</span></span> <span data-ttu-id="c646d-107">Para obter as informações mais atuais, consulte a [especificação do esquema de impressão](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="c646d-107">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="c646d-108">Especifica o fator de dimensionamento para o dimensionamento quadrado personalizado.</span><span class="sxs-lookup"><span data-stu-id="c646d-108">Specifies the scaling factor for custom square scaling.</span></span>

-   [<span data-ttu-id="c646d-109">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="c646d-109">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="c646d-110">Conteúdo da estrutura</span><span class="sxs-lookup"><span data-stu-id="c646d-110">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="c646d-111">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="c646d-111">Element Information</span></span>



| <span data-ttu-id="c646d-112">Nome</span><span class="sxs-lookup"><span data-stu-id="c646d-112">Name</span></span> | <span data-ttu-id="c646d-113">Valor</span><span class="sxs-lookup"><span data-stu-id="c646d-113">Value</span></span> |
|----------------------------|---------------------------------------------------------|
| <span data-ttu-id="c646d-114">Tipo de elemento</span><span class="sxs-lookup"><span data-stu-id="c646d-114">Element Type</span></span> <br/>   | <span data-ttu-id="c646d-115">ParameterDef</span><span class="sxs-lookup"><span data-stu-id="c646d-115">ParameterDef</span></span><br/>                                 |
| <span data-ttu-id="c646d-116">Prefixo de escopo</span><span class="sxs-lookup"><span data-stu-id="c646d-116">Scoping Prefix</span></span> <br/> | <span data-ttu-id="c646d-117">Página</span><span class="sxs-lookup"><span data-stu-id="c646d-117">Page</span></span><br/>                                         |
| <span data-ttu-id="c646d-118">Observações</span><span class="sxs-lookup"><span data-stu-id="c646d-118">Notes</span></span> <br/>          | <span data-ttu-id="c646d-119">Vinculado ao elemento PageScaling, opção personalizada</span><span class="sxs-lookup"><span data-stu-id="c646d-119">Linked to PageScaling element, Custom option</span></span><br/> |



 

## <a name="structure-content"></a><span data-ttu-id="c646d-120">Conteúdo da estrutura</span><span class="sxs-lookup"><span data-stu-id="c646d-120">Structure Content</span></span>

<span data-ttu-id="c646d-121">A estrutura XML desse elemento é:</span><span class="sxs-lookup"><span data-stu-id="c646d-121">The XML structure of this element is:</span></span>

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

## <a name="structure-properties"></a><span data-ttu-id="c646d-122">Propriedades da estrutura</span><span class="sxs-lookup"><span data-stu-id="c646d-122">Structure Properties</span></span>

<span data-ttu-id="c646d-123">A tabela a seguir descreve as características das variáveis definidas na estrutura XML.</span><span class="sxs-lookup"><span data-stu-id="c646d-123">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="c646d-124">Propriedade</span><span class="sxs-lookup"><span data-stu-id="c646d-124">Property</span></span>                | <span data-ttu-id="c646d-125">xsi:type</span><span class="sxs-lookup"><span data-stu-id="c646d-125">xsi:type</span></span>           | <span data-ttu-id="c646d-126">Valor</span><span class="sxs-lookup"><span data-stu-id="c646d-126">Value</span></span>                      |
|-------------------------|--------------------|----------------------------|
| <span data-ttu-id="c646d-127">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="c646d-127">DataType</span></span><br/>     | <span data-ttu-id="c646d-128">string</span><span class="sxs-lookup"><span data-stu-id="c646d-128">string</span></span><br/>  | <span data-ttu-id="c646d-129">xs:integer</span><span class="sxs-lookup"><span data-stu-id="c646d-129">xs:integer</span></span><br/>      |
| <span data-ttu-id="c646d-130">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="c646d-130">DefaultValue</span></span><br/> | <span data-ttu-id="c646d-131">Número inteiro</span><span class="sxs-lookup"><span data-stu-id="c646d-131">integer</span></span><br/> | <span data-ttu-id="c646d-132">não definido</span><span class="sxs-lookup"><span data-stu-id="c646d-132">undefined</span></span><br/>       |
| <span data-ttu-id="c646d-133">MaxValue</span><span class="sxs-lookup"><span data-stu-id="c646d-133">MaxValue</span></span><br/>     | <span data-ttu-id="c646d-134">Número inteiro</span><span class="sxs-lookup"><span data-stu-id="c646d-134">integer</span></span><br/> | <span data-ttu-id="c646d-135">não definido</span><span class="sxs-lookup"><span data-stu-id="c646d-135">undefined</span></span><br/>       |
| <span data-ttu-id="c646d-136">MinValue</span><span class="sxs-lookup"><span data-stu-id="c646d-136">MinValue</span></span><br/>     | <span data-ttu-id="c646d-137">integer</span><span class="sxs-lookup"><span data-stu-id="c646d-137">integer</span></span><br/> | <span data-ttu-id="c646d-138">1</span><span class="sxs-lookup"><span data-stu-id="c646d-138">1</span></span><br/>               |
| <span data-ttu-id="c646d-139">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="c646d-139">Mandatory</span></span><br/>    | <span data-ttu-id="c646d-140">string</span><span class="sxs-lookup"><span data-stu-id="c646d-140">string</span></span><br/>  | <span data-ttu-id="c646d-141">PSK: condicional</span><span class="sxs-lookup"><span data-stu-id="c646d-141">psk:Conditional</span></span><br/> |
| <span data-ttu-id="c646d-142">Vários</span><span class="sxs-lookup"><span data-stu-id="c646d-142">Multiple</span></span><br/>     | <span data-ttu-id="c646d-143">integer</span><span class="sxs-lookup"><span data-stu-id="c646d-143">integer</span></span><br/> | <span data-ttu-id="c646d-144">1</span><span class="sxs-lookup"><span data-stu-id="c646d-144">1</span></span><br/>               |
| <span data-ttu-id="c646d-145">UnitType</span><span class="sxs-lookup"><span data-stu-id="c646d-145">UnitType</span></span><br/>     | <span data-ttu-id="c646d-146">string</span><span class="sxs-lookup"><span data-stu-id="c646d-146">string</span></span><br/>  | <span data-ttu-id="c646d-147">{1&gt;percent&lt;1}</span><span class="sxs-lookup"><span data-stu-id="c646d-147">percent</span></span><br/>         |



 

## <a name="related-topics"></a><span data-ttu-id="c646d-148">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="c646d-148">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c646d-149">Especificação de esquema de impressão</span><span class="sxs-lookup"><span data-stu-id="c646d-149">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




