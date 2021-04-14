---
description: Este tópico não é atual. Para obter as informações mais atuais, consulte a especificação do esquema de impressão.
ms.assetid: f6fa0421-a125-4ead-a540-d2f7327a26b6
title: PageScalingOffsetHeight
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a475f7fa68cd961d9d7a7f42e40fc9ea80a72a4e
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/05/2021
ms.locfileid: "104370826"
---
# <a name="pagescalingoffsetheight"></a><span data-ttu-id="dcb30-104">PageScalingOffsetHeight</span><span class="sxs-lookup"><span data-stu-id="dcb30-104">PageScalingOffsetHeight</span></span>

<span data-ttu-id="dcb30-105">Este tópico não é atual.</span><span class="sxs-lookup"><span data-stu-id="dcb30-105">This topic is not current.</span></span> <span data-ttu-id="dcb30-106">Para obter as informações mais atuais, consulte a [especificação do esquema de impressão](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="dcb30-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="dcb30-107">Especifica o deslocamento de escala na direção do ImageableSizeHeight para o dimensionamento personalizado.</span><span class="sxs-lookup"><span data-stu-id="dcb30-107">Specifies the scaling offset in the ImageableSizeHeight direction for custom scaling.</span></span>

-   [<span data-ttu-id="dcb30-108">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="dcb30-108">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="dcb30-109">Conteúdo da estrutura</span><span class="sxs-lookup"><span data-stu-id="dcb30-109">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="dcb30-110">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="dcb30-110">Element Information</span></span>



| <span data-ttu-id="dcb30-111">Nome</span><span class="sxs-lookup"><span data-stu-id="dcb30-111">Name</span></span>                       |                                                         |
|----------------------------|---------------------------------------------------------|
| <span data-ttu-id="dcb30-112">Tipo de elemento</span><span class="sxs-lookup"><span data-stu-id="dcb30-112">Element Type</span></span> <br/>   | <span data-ttu-id="dcb30-113">ParameterDef</span><span class="sxs-lookup"><span data-stu-id="dcb30-113">ParameterDef</span></span><br/>                                 |
| <span data-ttu-id="dcb30-114">Prefixo de escopo</span><span class="sxs-lookup"><span data-stu-id="dcb30-114">Scoping Prefix</span></span> <br/> | <span data-ttu-id="dcb30-115">?</span><span class="sxs-lookup"><span data-stu-id="dcb30-115">Page</span></span><br/>                                         |
| <span data-ttu-id="dcb30-116">Observações</span><span class="sxs-lookup"><span data-stu-id="dcb30-116">Notes</span></span> <br/>          | <span data-ttu-id="dcb30-117">Vinculado ao elemento PageScaling, opção personalizada</span><span class="sxs-lookup"><span data-stu-id="dcb30-117">Linked to PageScaling element, Custom option</span></span><br/> |



 

## <a name="structure-content"></a><span data-ttu-id="dcb30-118">Conteúdo da estrutura</span><span class="sxs-lookup"><span data-stu-id="dcb30-118">Structure Content</span></span>

<span data-ttu-id="dcb30-119">A estrutura XML desse elemento é:</span><span class="sxs-lookup"><span data-stu-id="dcb30-119">The XML structure of this element is:</span></span>

``` syntax
<psf:ParameterDef name="psk:PageScalingOffsetHeight">
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

## <a name="structure-properties"></a><span data-ttu-id="dcb30-120">Propriedades da estrutura</span><span class="sxs-lookup"><span data-stu-id="dcb30-120">Structure Properties</span></span>

<span data-ttu-id="dcb30-121">A tabela a seguir descreve as características das variáveis definidas na estrutura XML.</span><span class="sxs-lookup"><span data-stu-id="dcb30-121">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="dcb30-122">Propriedade</span><span class="sxs-lookup"><span data-stu-id="dcb30-122">Property</span></span>                | <span data-ttu-id="dcb30-123">xsi:type</span><span class="sxs-lookup"><span data-stu-id="dcb30-123">xsi:type</span></span>           | <span data-ttu-id="dcb30-124">Valor</span><span class="sxs-lookup"><span data-stu-id="dcb30-124">Value</span></span>                      |
|-------------------------|--------------------|----------------------------|
| <span data-ttu-id="dcb30-125">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="dcb30-125">DataType</span></span><br/>     | <span data-ttu-id="dcb30-126">string</span><span class="sxs-lookup"><span data-stu-id="dcb30-126">string</span></span><br/>  | <span data-ttu-id="dcb30-127">xs:integer</span><span class="sxs-lookup"><span data-stu-id="dcb30-127">xs:integer</span></span><br/>      |
| <span data-ttu-id="dcb30-128">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="dcb30-128">DefaultValue</span></span><br/> | <span data-ttu-id="dcb30-129">Número inteiro</span><span class="sxs-lookup"><span data-stu-id="dcb30-129">integer</span></span><br/> | <span data-ttu-id="dcb30-130">não definido</span><span class="sxs-lookup"><span data-stu-id="dcb30-130">undefined</span></span><br/>       |
| <span data-ttu-id="dcb30-131">MaxValue</span><span class="sxs-lookup"><span data-stu-id="dcb30-131">MaxValue</span></span><br/>     | <span data-ttu-id="dcb30-132">Número inteiro</span><span class="sxs-lookup"><span data-stu-id="dcb30-132">integer</span></span><br/> | <span data-ttu-id="dcb30-133">não definido</span><span class="sxs-lookup"><span data-stu-id="dcb30-133">undefined</span></span><br/>       |
| <span data-ttu-id="dcb30-134">MinValue</span><span class="sxs-lookup"><span data-stu-id="dcb30-134">MinValue</span></span><br/>     | <span data-ttu-id="dcb30-135">Número inteiro</span><span class="sxs-lookup"><span data-stu-id="dcb30-135">integer</span></span><br/> | <span data-ttu-id="dcb30-136">não definido</span><span class="sxs-lookup"><span data-stu-id="dcb30-136">undefined</span></span><br/>       |
| <span data-ttu-id="dcb30-137">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="dcb30-137">Mandatory</span></span><br/>    | <span data-ttu-id="dcb30-138">string</span><span class="sxs-lookup"><span data-stu-id="dcb30-138">string</span></span><br/>  | <span data-ttu-id="dcb30-139">PSK: condicional</span><span class="sxs-lookup"><span data-stu-id="dcb30-139">psk:Conditional</span></span><br/> |
| <span data-ttu-id="dcb30-140">Vários</span><span class="sxs-lookup"><span data-stu-id="dcb30-140">Multiple</span></span><br/>     | <span data-ttu-id="dcb30-141">integer</span><span class="sxs-lookup"><span data-stu-id="dcb30-141">integer</span></span><br/> | <span data-ttu-id="dcb30-142">1</span><span class="sxs-lookup"><span data-stu-id="dcb30-142">1</span></span><br/>               |
| <span data-ttu-id="dcb30-143">UnitType</span><span class="sxs-lookup"><span data-stu-id="dcb30-143">UnitType</span></span><br/>     | <span data-ttu-id="dcb30-144">string</span><span class="sxs-lookup"><span data-stu-id="dcb30-144">string</span></span><br/>  | <span data-ttu-id="dcb30-145">mícrons</span><span class="sxs-lookup"><span data-stu-id="dcb30-145">microns</span></span><br/>         |



 

## <a name="related-topics"></a><span data-ttu-id="dcb30-146">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="dcb30-146">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="dcb30-147">Especificação de esquema de impressão</span><span class="sxs-lookup"><span data-stu-id="dcb30-147">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




