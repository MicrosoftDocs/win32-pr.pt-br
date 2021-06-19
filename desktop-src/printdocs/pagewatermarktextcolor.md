---
description: Obtenha informações sobre o parâmetro PageWatermarkTextColor. Este tópico não é atual. Para obter as informações mais atuais, consulte a especificação do esquema de impressão.
ms.assetid: edbdd2c7-da04-49fb-a0f8-31a7df88f8ef
title: PageWatermarkTextColor
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: db7cb7b893ec9a2ecf774173cf2a9f2410549087
ms.sourcegitcommit: 91530c19d26ba4c57a6af1f37b57f211f580464e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/19/2021
ms.locfileid: "112396011"
---
# <a name="pagewatermarktextcolor"></a><span data-ttu-id="70e81-105">PageWatermarkTextColor</span><span class="sxs-lookup"><span data-stu-id="70e81-105">PageWatermarkTextColor</span></span>

<span data-ttu-id="70e81-106">Este tópico não é atual.</span><span class="sxs-lookup"><span data-stu-id="70e81-106">This topic is not current.</span></span> <span data-ttu-id="70e81-107">Para obter as informações mais atuais, consulte a [especificação do esquema de impressão](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="70e81-107">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="70e81-108">Define a cor sRGB para o texto da marca d' água.</span><span class="sxs-lookup"><span data-stu-id="70e81-108">Defines the sRGB color for the watermark text.</span></span> <span data-ttu-id="70e81-109">O formato é ARGB: \# AARRGGBB.</span><span class="sxs-lookup"><span data-stu-id="70e81-109">Format is ARGB: \#AARRGGBB.</span></span>

-   [<span data-ttu-id="70e81-110">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="70e81-110">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="70e81-111">Conteúdo da estrutura</span><span class="sxs-lookup"><span data-stu-id="70e81-111">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="70e81-112">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="70e81-112">Element Information</span></span>



| <span data-ttu-id="70e81-113">Name</span><span class="sxs-lookup"><span data-stu-id="70e81-113">Name</span></span> | <span data-ttu-id="70e81-114">Valor</span><span class="sxs-lookup"><span data-stu-id="70e81-114">Value</span></span> |
|----------------------------|--------------------------------------------|
| <span data-ttu-id="70e81-115">Tipo de elemento</span><span class="sxs-lookup"><span data-stu-id="70e81-115">Element Type</span></span> <br/>   | <span data-ttu-id="70e81-116">ParameterDef</span><span class="sxs-lookup"><span data-stu-id="70e81-116">ParameterDef</span></span><br/>                    |
| <span data-ttu-id="70e81-117">Prefixo de escopo</span><span class="sxs-lookup"><span data-stu-id="70e81-117">Scoping Prefix</span></span> <br/> | <span data-ttu-id="70e81-118">?</span><span class="sxs-lookup"><span data-stu-id="70e81-118">Page</span></span><br/>                            |
| <span data-ttu-id="70e81-119">Observações</span><span class="sxs-lookup"><span data-stu-id="70e81-119">Notes</span></span> <br/>          | <span data-ttu-id="70e81-120">Vinculado ao elemento PageWatermark</span><span class="sxs-lookup"><span data-stu-id="70e81-120">Linked to PageWatermark element</span></span><br/> |



 

## <a name="structure-content"></a><span data-ttu-id="70e81-121">Conteúdo da estrutura</span><span class="sxs-lookup"><span data-stu-id="70e81-121">Structure Content</span></span>

<span data-ttu-id="70e81-122">A estrutura XML desse elemento é a seguinte:</span><span class="sxs-lookup"><span data-stu-id="70e81-122">The XML structure of this element is as follows:</span></span>

``` syntax
<psf:ParameterDef name="psk:PageWatermarkTextColor">
  <psf:Property name="psf:DataType">
    <psf:Value xsi:type="xs:string">xs:string</psf:Value>
  </psf:Property>
  <psf:Property name="psf:DefaultValue">
    <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
  </psf:Property>
  <psf:Property name="psf:MaxLength">
    <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
  </psf:Property>
  <psf:Property name="psf:MinLength">
    <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
  </psf:Property>
  <psf:Property name="psf:Mandatory">
    <psf:Value xsi:type="xs:string">psk:Conditional</psf:Value>
  </psf:Property>
  <psf:Property name="psf:UnitType">
    <psf:Value xsi:type="xs:string">sRGB</psf:Value>
  </psf:Property>
</psf:ParameterDef>
      
```

## <a name="structure-properties"></a><span data-ttu-id="70e81-123">Propriedades da estrutura</span><span class="sxs-lookup"><span data-stu-id="70e81-123">Structure Properties</span></span>

<span data-ttu-id="70e81-124">A tabela a seguir descreve as características das variáveis definidas na estrutura XML.</span><span class="sxs-lookup"><span data-stu-id="70e81-124">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="70e81-125">Propriedade</span><span class="sxs-lookup"><span data-stu-id="70e81-125">Property</span></span>                | <span data-ttu-id="70e81-126">xsi:type</span><span class="sxs-lookup"><span data-stu-id="70e81-126">xsi:type</span></span>           | <span data-ttu-id="70e81-127">Valor</span><span class="sxs-lookup"><span data-stu-id="70e81-127">Value</span></span>                      |
|-------------------------|--------------------|----------------------------|
| <span data-ttu-id="70e81-128">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="70e81-128">DataType</span></span><br/>     | <span data-ttu-id="70e81-129">string</span><span class="sxs-lookup"><span data-stu-id="70e81-129">string</span></span><br/>  | <span data-ttu-id="70e81-130">xs:string</span><span class="sxs-lookup"><span data-stu-id="70e81-130">xs:string</span></span><br/>       |
| <span data-ttu-id="70e81-131">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="70e81-131">DefaultValue</span></span><br/> | <span data-ttu-id="70e81-132">Número inteiro</span><span class="sxs-lookup"><span data-stu-id="70e81-132">integer</span></span><br/> | <span data-ttu-id="70e81-133">não definido</span><span class="sxs-lookup"><span data-stu-id="70e81-133">undefined</span></span><br/>       |
| <span data-ttu-id="70e81-134">MaxValue</span><span class="sxs-lookup"><span data-stu-id="70e81-134">MaxValue</span></span><br/>     | <span data-ttu-id="70e81-135">Número inteiro</span><span class="sxs-lookup"><span data-stu-id="70e81-135">integer</span></span><br/> | <span data-ttu-id="70e81-136">não definido</span><span class="sxs-lookup"><span data-stu-id="70e81-136">undefined</span></span><br/>       |
| <span data-ttu-id="70e81-137">MinValue</span><span class="sxs-lookup"><span data-stu-id="70e81-137">MinValue</span></span><br/>     | <span data-ttu-id="70e81-138">Número inteiro</span><span class="sxs-lookup"><span data-stu-id="70e81-138">integer</span></span><br/> | <span data-ttu-id="70e81-139">não definido</span><span class="sxs-lookup"><span data-stu-id="70e81-139">undefined</span></span><br/>       |
| <span data-ttu-id="70e81-140">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="70e81-140">Mandatory</span></span><br/>    | <span data-ttu-id="70e81-141">string</span><span class="sxs-lookup"><span data-stu-id="70e81-141">string</span></span><br/>  | <span data-ttu-id="70e81-142">PSK: condicional</span><span class="sxs-lookup"><span data-stu-id="70e81-142">psk:Conditional</span></span><br/> |
| <span data-ttu-id="70e81-143">UnitType</span><span class="sxs-lookup"><span data-stu-id="70e81-143">UnitType</span></span><br/>     | <span data-ttu-id="70e81-144">string</span><span class="sxs-lookup"><span data-stu-id="70e81-144">string</span></span><br/>  | <span data-ttu-id="70e81-145">sRGB</span><span class="sxs-lookup"><span data-stu-id="70e81-145">sRGB</span></span><br/>            |



 

## <a name="related-topics"></a><span data-ttu-id="70e81-146">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="70e81-146">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="70e81-147">Especificação de esquema de impressão</span><span class="sxs-lookup"><span data-stu-id="70e81-147">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




