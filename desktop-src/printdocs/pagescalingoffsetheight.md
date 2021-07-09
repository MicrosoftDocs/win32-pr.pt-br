---
description: Obtenha informações sobre o parâmetro PageScalingOffsetHeight. Este tópico não é atual. Para obter as informações mais atuais, consulte a especificação do esquema de impressão.
ms.assetid: f6fa0421-a125-4ead-a540-d2f7327a26b6
title: PageScalingOffsetHeight
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5f02370d28716dd3a8840001959bb7d963307d2f
ms.sourcegitcommit: 998d50f6def8a25850fc113fc8a2df903c829c5e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/09/2021
ms.locfileid: "113548954"
---
# <a name="pagescalingoffsetheight"></a><span data-ttu-id="de2dd-105">PageScalingOffsetHeight</span><span class="sxs-lookup"><span data-stu-id="de2dd-105">PageScalingOffsetHeight</span></span>

<span data-ttu-id="de2dd-106">Este tópico não é atual.</span><span class="sxs-lookup"><span data-stu-id="de2dd-106">This topic is not current.</span></span> <span data-ttu-id="de2dd-107">Para obter as informações mais atuais, consulte a [especificação do esquema de impressão](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="de2dd-107">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="de2dd-108">Especifica o deslocamento de escala na direção do ImageableSizeHeight para o dimensionamento personalizado.</span><span class="sxs-lookup"><span data-stu-id="de2dd-108">Specifies the scaling offset in the ImageableSizeHeight direction for custom scaling.</span></span>

-   [<span data-ttu-id="de2dd-109">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="de2dd-109">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="de2dd-110">Conteúdo da estrutura</span><span class="sxs-lookup"><span data-stu-id="de2dd-110">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="de2dd-111">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="de2dd-111">Element Information</span></span>



| <span data-ttu-id="de2dd-112">Nome</span><span class="sxs-lookup"><span data-stu-id="de2dd-112">Name</span></span> | <span data-ttu-id="de2dd-113">Valor</span><span class="sxs-lookup"><span data-stu-id="de2dd-113">Value</span></span> |
|----------------------------|---------------------------------------------------------|
| <span data-ttu-id="de2dd-114">Tipo de elemento</span><span class="sxs-lookup"><span data-stu-id="de2dd-114">Element Type</span></span> <br/>   | <span data-ttu-id="de2dd-115">ParameterDef</span><span class="sxs-lookup"><span data-stu-id="de2dd-115">ParameterDef</span></span><br/>                                 |
| <span data-ttu-id="de2dd-116">Prefixo de escopo</span><span class="sxs-lookup"><span data-stu-id="de2dd-116">Scoping Prefix</span></span> <br/> | <span data-ttu-id="de2dd-117">Página</span><span class="sxs-lookup"><span data-stu-id="de2dd-117">Page</span></span><br/>                                         |
| <span data-ttu-id="de2dd-118">Observações</span><span class="sxs-lookup"><span data-stu-id="de2dd-118">Notes</span></span> <br/>          | <span data-ttu-id="de2dd-119">Vinculado ao elemento PageScaling, opção personalizada</span><span class="sxs-lookup"><span data-stu-id="de2dd-119">Linked to PageScaling element, Custom option</span></span><br/> |



 

## <a name="structure-content"></a><span data-ttu-id="de2dd-120">Conteúdo da estrutura</span><span class="sxs-lookup"><span data-stu-id="de2dd-120">Structure Content</span></span>

<span data-ttu-id="de2dd-121">A estrutura XML desse elemento é:</span><span class="sxs-lookup"><span data-stu-id="de2dd-121">The XML structure of this element is:</span></span>

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

## <a name="structure-properties"></a><span data-ttu-id="de2dd-122">Propriedades da estrutura</span><span class="sxs-lookup"><span data-stu-id="de2dd-122">Structure Properties</span></span>

<span data-ttu-id="de2dd-123">A tabela a seguir descreve as características das variáveis definidas na estrutura XML.</span><span class="sxs-lookup"><span data-stu-id="de2dd-123">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="de2dd-124">Propriedade</span><span class="sxs-lookup"><span data-stu-id="de2dd-124">Property</span></span>                | <span data-ttu-id="de2dd-125">xsi:type</span><span class="sxs-lookup"><span data-stu-id="de2dd-125">xsi:type</span></span>           | <span data-ttu-id="de2dd-126">Valor</span><span class="sxs-lookup"><span data-stu-id="de2dd-126">Value</span></span>                      |
|-------------------------|--------------------|----------------------------|
| <span data-ttu-id="de2dd-127">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="de2dd-127">DataType</span></span><br/>     | <span data-ttu-id="de2dd-128">string</span><span class="sxs-lookup"><span data-stu-id="de2dd-128">string</span></span><br/>  | <span data-ttu-id="de2dd-129">xs:integer</span><span class="sxs-lookup"><span data-stu-id="de2dd-129">xs:integer</span></span><br/>      |
| <span data-ttu-id="de2dd-130">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="de2dd-130">DefaultValue</span></span><br/> | <span data-ttu-id="de2dd-131">Número inteiro</span><span class="sxs-lookup"><span data-stu-id="de2dd-131">integer</span></span><br/> | <span data-ttu-id="de2dd-132">não definido</span><span class="sxs-lookup"><span data-stu-id="de2dd-132">undefined</span></span><br/>       |
| <span data-ttu-id="de2dd-133">MaxValue</span><span class="sxs-lookup"><span data-stu-id="de2dd-133">MaxValue</span></span><br/>     | <span data-ttu-id="de2dd-134">Número inteiro</span><span class="sxs-lookup"><span data-stu-id="de2dd-134">integer</span></span><br/> | <span data-ttu-id="de2dd-135">não definido</span><span class="sxs-lookup"><span data-stu-id="de2dd-135">undefined</span></span><br/>       |
| <span data-ttu-id="de2dd-136">MinValue</span><span class="sxs-lookup"><span data-stu-id="de2dd-136">MinValue</span></span><br/>     | <span data-ttu-id="de2dd-137">Número inteiro</span><span class="sxs-lookup"><span data-stu-id="de2dd-137">integer</span></span><br/> | <span data-ttu-id="de2dd-138">não definido</span><span class="sxs-lookup"><span data-stu-id="de2dd-138">undefined</span></span><br/>       |
| <span data-ttu-id="de2dd-139">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="de2dd-139">Mandatory</span></span><br/>    | <span data-ttu-id="de2dd-140">string</span><span class="sxs-lookup"><span data-stu-id="de2dd-140">string</span></span><br/>  | <span data-ttu-id="de2dd-141">PSK: condicional</span><span class="sxs-lookup"><span data-stu-id="de2dd-141">psk:Conditional</span></span><br/> |
| <span data-ttu-id="de2dd-142">Vários</span><span class="sxs-lookup"><span data-stu-id="de2dd-142">Multiple</span></span><br/>     | <span data-ttu-id="de2dd-143">integer</span><span class="sxs-lookup"><span data-stu-id="de2dd-143">integer</span></span><br/> | <span data-ttu-id="de2dd-144">1</span><span class="sxs-lookup"><span data-stu-id="de2dd-144">1</span></span><br/>               |
| <span data-ttu-id="de2dd-145">UnitType</span><span class="sxs-lookup"><span data-stu-id="de2dd-145">UnitType</span></span><br/>     | <span data-ttu-id="de2dd-146">string</span><span class="sxs-lookup"><span data-stu-id="de2dd-146">string</span></span><br/>  | <span data-ttu-id="de2dd-147">mícrons</span><span class="sxs-lookup"><span data-stu-id="de2dd-147">microns</span></span><br/>         |



 

## <a name="related-topics"></a><span data-ttu-id="de2dd-148">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="de2dd-148">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="de2dd-149">Especificação de esquema de impressão</span><span class="sxs-lookup"><span data-stu-id="de2dd-149">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




