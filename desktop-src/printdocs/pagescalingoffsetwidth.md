---
description: Obtenha informações sobre o parâmetro PageScalingOffsetWidth. Este tópico não é atual. Para obter as informações mais atuais, consulte a especificação do esquema de impressão.
ms.assetid: e82394d1-f765-4679-b1de-ea17825d6478
title: PageScalingOffsetWidth
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 63152e6a3d9f8ea47bac3b5a0efe559e71e0cb35
ms.sourcegitcommit: 998d50f6def8a25850fc113fc8a2df903c829c5e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/09/2021
ms.locfileid: "113548844"
---
# <a name="pagescalingoffsetwidth"></a><span data-ttu-id="dcfa9-105">PageScalingOffsetWidth</span><span class="sxs-lookup"><span data-stu-id="dcfa9-105">PageScalingOffsetWidth</span></span>

<span data-ttu-id="dcfa9-106">Este tópico não é atual.</span><span class="sxs-lookup"><span data-stu-id="dcfa9-106">This topic is not current.</span></span> <span data-ttu-id="dcfa9-107">Para obter as informações mais atuais, consulte a [especificação do esquema de impressão](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="dcfa9-107">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="dcfa9-108">Especifica o deslocamento de escala na direção do ImageableSizeWidth para o dimensionamento personalizado.</span><span class="sxs-lookup"><span data-stu-id="dcfa9-108">Specifies the scaling offset in the ImageableSizeWidth direction for custom scaling.</span></span>

-   [<span data-ttu-id="dcfa9-109">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="dcfa9-109">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="dcfa9-110">Conteúdo da estrutura</span><span class="sxs-lookup"><span data-stu-id="dcfa9-110">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="dcfa9-111">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="dcfa9-111">Element Information</span></span>



| <span data-ttu-id="dcfa9-112">Nome</span><span class="sxs-lookup"><span data-stu-id="dcfa9-112">Name</span></span> | <span data-ttu-id="dcfa9-113">Valor</span><span class="sxs-lookup"><span data-stu-id="dcfa9-113">Value</span></span> |
|----------------------------|---------------------------------------------------------|
| <span data-ttu-id="dcfa9-114">Tipo de elemento</span><span class="sxs-lookup"><span data-stu-id="dcfa9-114">Element Type</span></span> <br/>   | <span data-ttu-id="dcfa9-115">ParameterDef</span><span class="sxs-lookup"><span data-stu-id="dcfa9-115">ParameterDef</span></span><br/>                                 |
| <span data-ttu-id="dcfa9-116">Prefixo de escopo</span><span class="sxs-lookup"><span data-stu-id="dcfa9-116">Scoping Prefix</span></span> <br/> | <span data-ttu-id="dcfa9-117">Página</span><span class="sxs-lookup"><span data-stu-id="dcfa9-117">Page</span></span><br/>                                         |
| <span data-ttu-id="dcfa9-118">Observações</span><span class="sxs-lookup"><span data-stu-id="dcfa9-118">Notes</span></span> <br/>          | <span data-ttu-id="dcfa9-119">Vinculado ao elemento PageScaling, opção personalizada</span><span class="sxs-lookup"><span data-stu-id="dcfa9-119">Linked to PageScaling element, Custom option</span></span><br/> |



 

## <a name="structure-content"></a><span data-ttu-id="dcfa9-120">Conteúdo da estrutura</span><span class="sxs-lookup"><span data-stu-id="dcfa9-120">Structure Content</span></span>

<span data-ttu-id="dcfa9-121">A estrutura XML desse elemento é:</span><span class="sxs-lookup"><span data-stu-id="dcfa9-121">The XML structure of this element is:</span></span>

``` syntax
<psf:ParameterDef name="psk:PageScalingOffsetWidth">
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
    <psf:Value xsi:type="xs:decimal">_Undefined_</psf:Value>
  </psf:Property>
  <psf:Property name="psf:Multiple">
    <psf:Value xsi:type="xs:integer">1</psf:Value>
  </psf:Property>
  <psf:Property name="psf:Mandatory">
    <psf:Value xsi:type="xs:string">psk:Conditional</psf:Value>
  </psf:Property>
  <psf:Property name="psf:UnitType">
    <psf:Value xsi:type="xs:string">microns</psf:Value>
  </psf:Property>
</psf:ParameterDef>
      
```

## <a name="structure-properties"></a><span data-ttu-id="dcfa9-122">Propriedades da estrutura</span><span class="sxs-lookup"><span data-stu-id="dcfa9-122">Structure Properties</span></span>

<span data-ttu-id="dcfa9-123">A tabela a seguir descreve as características das variáveis definidas na estrutura XML.</span><span class="sxs-lookup"><span data-stu-id="dcfa9-123">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="dcfa9-124">Propriedade</span><span class="sxs-lookup"><span data-stu-id="dcfa9-124">Property</span></span>                | <span data-ttu-id="dcfa9-125">xsi:type</span><span class="sxs-lookup"><span data-stu-id="dcfa9-125">xsi:type</span></span>           | <span data-ttu-id="dcfa9-126">Valor</span><span class="sxs-lookup"><span data-stu-id="dcfa9-126">Value</span></span>                      |
|-------------------------|--------------------|----------------------------|
| <span data-ttu-id="dcfa9-127">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="dcfa9-127">DataType</span></span><br/>     | <span data-ttu-id="dcfa9-128">string</span><span class="sxs-lookup"><span data-stu-id="dcfa9-128">string</span></span><br/>  | <span data-ttu-id="dcfa9-129">xs:integer</span><span class="sxs-lookup"><span data-stu-id="dcfa9-129">xs:integer</span></span><br/>      |
| <span data-ttu-id="dcfa9-130">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="dcfa9-130">DefaultValue</span></span><br/> | <span data-ttu-id="dcfa9-131">Número inteiro</span><span class="sxs-lookup"><span data-stu-id="dcfa9-131">integer</span></span><br/> | <span data-ttu-id="dcfa9-132">não definido</span><span class="sxs-lookup"><span data-stu-id="dcfa9-132">undefined</span></span><br/>       |
| <span data-ttu-id="dcfa9-133">MaxValue</span><span class="sxs-lookup"><span data-stu-id="dcfa9-133">MaxValue</span></span><br/>     | <span data-ttu-id="dcfa9-134">Número inteiro</span><span class="sxs-lookup"><span data-stu-id="dcfa9-134">integer</span></span><br/> | <span data-ttu-id="dcfa9-135">não definido</span><span class="sxs-lookup"><span data-stu-id="dcfa9-135">undefined</span></span><br/>       |
| <span data-ttu-id="dcfa9-136">MinValue</span><span class="sxs-lookup"><span data-stu-id="dcfa9-136">MinValue</span></span><br/>     | <span data-ttu-id="dcfa9-137">Número inteiro</span><span class="sxs-lookup"><span data-stu-id="dcfa9-137">integer</span></span><br/> | <span data-ttu-id="dcfa9-138">não definido</span><span class="sxs-lookup"><span data-stu-id="dcfa9-138">undefined</span></span><br/>       |
| <span data-ttu-id="dcfa9-139">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="dcfa9-139">Mandatory</span></span><br/>    | <span data-ttu-id="dcfa9-140">string</span><span class="sxs-lookup"><span data-stu-id="dcfa9-140">string</span></span><br/>  | <span data-ttu-id="dcfa9-141">PSK: condicional</span><span class="sxs-lookup"><span data-stu-id="dcfa9-141">psk:Conditional</span></span><br/> |
| <span data-ttu-id="dcfa9-142">Vários</span><span class="sxs-lookup"><span data-stu-id="dcfa9-142">Multiple</span></span><br/>     | <span data-ttu-id="dcfa9-143">integer</span><span class="sxs-lookup"><span data-stu-id="dcfa9-143">integer</span></span><br/> | <span data-ttu-id="dcfa9-144">1</span><span class="sxs-lookup"><span data-stu-id="dcfa9-144">1</span></span><br/>               |
| <span data-ttu-id="dcfa9-145">UnitType</span><span class="sxs-lookup"><span data-stu-id="dcfa9-145">UnitType</span></span><br/>     | <span data-ttu-id="dcfa9-146">string</span><span class="sxs-lookup"><span data-stu-id="dcfa9-146">string</span></span><br/>  | <span data-ttu-id="dcfa9-147">mícrons</span><span class="sxs-lookup"><span data-stu-id="dcfa9-147">microns</span></span><br/>         |



 

## <a name="related-topics"></a><span data-ttu-id="dcfa9-148">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="dcfa9-148">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="dcfa9-149">Especificação de esquema de impressão</span><span class="sxs-lookup"><span data-stu-id="dcfa9-149">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




