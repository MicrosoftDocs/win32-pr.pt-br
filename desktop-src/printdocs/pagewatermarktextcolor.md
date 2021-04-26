---
description: Este tópico não é atual. Para obter as informações mais atuais, consulte a especificação do esquema de impressão.
ms.assetid: edbdd2c7-da04-49fb-a0f8-31a7df88f8ef
title: PageWatermarkTextColor
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5a2cc4d4f88724080b09ef52d7ded781039ff852
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/26/2021
ms.locfileid: "107996883"
---
# <a name="pagewatermarktextcolor"></a><span data-ttu-id="11559-104">PageWatermarkTextColor</span><span class="sxs-lookup"><span data-stu-id="11559-104">PageWatermarkTextColor</span></span>

<span data-ttu-id="11559-105">Este tópico não é atual.</span><span class="sxs-lookup"><span data-stu-id="11559-105">This topic is not current.</span></span> <span data-ttu-id="11559-106">Para obter as informações mais atuais, consulte a [especificação do esquema de impressão](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="11559-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="11559-107">Define a cor sRGB para o texto da marca d' água.</span><span class="sxs-lookup"><span data-stu-id="11559-107">Defines the sRGB color for the watermark text.</span></span> <span data-ttu-id="11559-108">O formato é ARGB: \# AARRGGBB.</span><span class="sxs-lookup"><span data-stu-id="11559-108">Format is ARGB: \#AARRGGBB.</span></span>

-   [<span data-ttu-id="11559-109">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="11559-109">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="11559-110">Conteúdo da estrutura</span><span class="sxs-lookup"><span data-stu-id="11559-110">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="11559-111">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="11559-111">Element Information</span></span>



| <span data-ttu-id="11559-112">Nome</span><span class="sxs-lookup"><span data-stu-id="11559-112">Name</span></span> | <span data-ttu-id="11559-113">Valor</span><span class="sxs-lookup"><span data-stu-id="11559-113">Value</span></span> |
|----------------------------|--------------------------------------------|
| <span data-ttu-id="11559-114">Tipo de elemento</span><span class="sxs-lookup"><span data-stu-id="11559-114">Element Type</span></span> <br/>   | <span data-ttu-id="11559-115">ParameterDef</span><span class="sxs-lookup"><span data-stu-id="11559-115">ParameterDef</span></span><br/>                    |
| <span data-ttu-id="11559-116">Prefixo de escopo</span><span class="sxs-lookup"><span data-stu-id="11559-116">Scoping Prefix</span></span> <br/> | <span data-ttu-id="11559-117">?</span><span class="sxs-lookup"><span data-stu-id="11559-117">Page</span></span><br/>                            |
| <span data-ttu-id="11559-118">Observações</span><span class="sxs-lookup"><span data-stu-id="11559-118">Notes</span></span> <br/>          | <span data-ttu-id="11559-119">Vinculado ao elemento PageWatermark</span><span class="sxs-lookup"><span data-stu-id="11559-119">Linked to PageWatermark element</span></span><br/> |



 

## <a name="structure-content"></a><span data-ttu-id="11559-120">Conteúdo da estrutura</span><span class="sxs-lookup"><span data-stu-id="11559-120">Structure Content</span></span>

<span data-ttu-id="11559-121">A estrutura XML desse elemento é a seguinte:</span><span class="sxs-lookup"><span data-stu-id="11559-121">The XML structure of this element is as follows:</span></span>

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

## <a name="structure-properties"></a><span data-ttu-id="11559-122">Propriedades da estrutura</span><span class="sxs-lookup"><span data-stu-id="11559-122">Structure Properties</span></span>

<span data-ttu-id="11559-123">A tabela a seguir descreve as características das variáveis definidas na estrutura XML.</span><span class="sxs-lookup"><span data-stu-id="11559-123">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="11559-124">Propriedade</span><span class="sxs-lookup"><span data-stu-id="11559-124">Property</span></span>                | <span data-ttu-id="11559-125">xsi:type</span><span class="sxs-lookup"><span data-stu-id="11559-125">xsi:type</span></span>           | <span data-ttu-id="11559-126">Valor</span><span class="sxs-lookup"><span data-stu-id="11559-126">Value</span></span>                      |
|-------------------------|--------------------|----------------------------|
| <span data-ttu-id="11559-127">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="11559-127">DataType</span></span><br/>     | <span data-ttu-id="11559-128">string</span><span class="sxs-lookup"><span data-stu-id="11559-128">string</span></span><br/>  | <span data-ttu-id="11559-129">xs:string</span><span class="sxs-lookup"><span data-stu-id="11559-129">xs:string</span></span><br/>       |
| <span data-ttu-id="11559-130">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="11559-130">DefaultValue</span></span><br/> | <span data-ttu-id="11559-131">Número inteiro</span><span class="sxs-lookup"><span data-stu-id="11559-131">integer</span></span><br/> | <span data-ttu-id="11559-132">não definido</span><span class="sxs-lookup"><span data-stu-id="11559-132">undefined</span></span><br/>       |
| <span data-ttu-id="11559-133">MaxValue</span><span class="sxs-lookup"><span data-stu-id="11559-133">MaxValue</span></span><br/>     | <span data-ttu-id="11559-134">Número inteiro</span><span class="sxs-lookup"><span data-stu-id="11559-134">integer</span></span><br/> | <span data-ttu-id="11559-135">não definido</span><span class="sxs-lookup"><span data-stu-id="11559-135">undefined</span></span><br/>       |
| <span data-ttu-id="11559-136">MinValue</span><span class="sxs-lookup"><span data-stu-id="11559-136">MinValue</span></span><br/>     | <span data-ttu-id="11559-137">Número inteiro</span><span class="sxs-lookup"><span data-stu-id="11559-137">integer</span></span><br/> | <span data-ttu-id="11559-138">não definido</span><span class="sxs-lookup"><span data-stu-id="11559-138">undefined</span></span><br/>       |
| <span data-ttu-id="11559-139">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="11559-139">Mandatory</span></span><br/>    | <span data-ttu-id="11559-140">string</span><span class="sxs-lookup"><span data-stu-id="11559-140">string</span></span><br/>  | <span data-ttu-id="11559-141">PSK: condicional</span><span class="sxs-lookup"><span data-stu-id="11559-141">psk:Conditional</span></span><br/> |
| <span data-ttu-id="11559-142">UnitType</span><span class="sxs-lookup"><span data-stu-id="11559-142">UnitType</span></span><br/>     | <span data-ttu-id="11559-143">string</span><span class="sxs-lookup"><span data-stu-id="11559-143">string</span></span><br/>  | <span data-ttu-id="11559-144">sRGB</span><span class="sxs-lookup"><span data-stu-id="11559-144">sRGB</span></span><br/>            |



 

## <a name="related-topics"></a><span data-ttu-id="11559-145">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="11559-145">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="11559-146">Especificação de esquema de impressão</span><span class="sxs-lookup"><span data-stu-id="11559-146">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




