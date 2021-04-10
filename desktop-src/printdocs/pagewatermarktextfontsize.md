---
description: Este tópico não é atual. Para obter as informações mais atuais, consulte a especificação do esquema de impressão.
ms.assetid: 4c379898-d21f-4c6c-93c8-e5f386e032ba
title: PageWatermarkTextFontSize
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 678630b7b7f6650a1317efef95c30effc71c6082
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/05/2021
ms.locfileid: "104011976"
---
# <a name="pagewatermarktextfontsize"></a><span data-ttu-id="07776-104">PageWatermarkTextFontSize</span><span class="sxs-lookup"><span data-stu-id="07776-104">PageWatermarkTextFontSize</span></span>

<span data-ttu-id="07776-105">Este tópico não é atual.</span><span class="sxs-lookup"><span data-stu-id="07776-105">This topic is not current.</span></span> <span data-ttu-id="07776-106">Para obter as informações mais atuais, consulte a [especificação do esquema de impressão](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="07776-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="07776-107">Define os tamanhos de fonte disponíveis para o texto de marca d' água.</span><span class="sxs-lookup"><span data-stu-id="07776-107">Defines the available font sizes for the watermark text.</span></span>

-   [<span data-ttu-id="07776-108">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="07776-108">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="07776-109">Conteúdo da estrutura</span><span class="sxs-lookup"><span data-stu-id="07776-109">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="07776-110">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="07776-110">Element Information</span></span>



| <span data-ttu-id="07776-111">Nome</span><span class="sxs-lookup"><span data-stu-id="07776-111">Name</span></span>                       |                                            |
|----------------------------|--------------------------------------------|
| <span data-ttu-id="07776-112">Tipo de elemento</span><span class="sxs-lookup"><span data-stu-id="07776-112">Element Type</span></span> <br/>   | <span data-ttu-id="07776-113">ParameterDef</span><span class="sxs-lookup"><span data-stu-id="07776-113">ParameterDef</span></span><br/>                    |
| <span data-ttu-id="07776-114">Prefixo de escopo</span><span class="sxs-lookup"><span data-stu-id="07776-114">Scoping Prefix</span></span> <br/> | <span data-ttu-id="07776-115">?</span><span class="sxs-lookup"><span data-stu-id="07776-115">Page</span></span><br/>                            |
| <span data-ttu-id="07776-116">Observações</span><span class="sxs-lookup"><span data-stu-id="07776-116">Notes</span></span> <br/>          | <span data-ttu-id="07776-117">Vinculado ao elemento PageWatermark</span><span class="sxs-lookup"><span data-stu-id="07776-117">Linked to PageWatermark element</span></span><br/> |



 

## <a name="structure-content"></a><span data-ttu-id="07776-118">Conteúdo da estrutura</span><span class="sxs-lookup"><span data-stu-id="07776-118">Structure Content</span></span>

<span data-ttu-id="07776-119">A estrutura XML desse elemento é a seguinte:</span><span class="sxs-lookup"><span data-stu-id="07776-119">The XML structure of this element is as follows:</span></span>

``` syntax
<psf:ParameterDef name="psk:PageWatermarkTextFontSize">
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
    <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
  </psf:Property>
  <psf:Property name="psf:Multiple">
    <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
  </psf:Property>
  <psf:Property name="psf:Mandatory">
    <psf:Value xsi:type="xs:string">psk:Conditional</psf:Value>
  </psf:Property>
  <psf:Property name="psf:UnitType">
    <psf:Value xsi:type="xs:string">points</psf:Value>
  </psf:Property>
</psf:ParameterDef>
      
```

## <a name="structure-properties"></a><span data-ttu-id="07776-120">Propriedades da estrutura</span><span class="sxs-lookup"><span data-stu-id="07776-120">Structure Properties</span></span>

<span data-ttu-id="07776-121">A tabela a seguir descreve as características das variáveis definidas na estrutura XML.</span><span class="sxs-lookup"><span data-stu-id="07776-121">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="07776-122">Propriedade</span><span class="sxs-lookup"><span data-stu-id="07776-122">Property</span></span>                | <span data-ttu-id="07776-123">xsi:type</span><span class="sxs-lookup"><span data-stu-id="07776-123">xsi:type</span></span>           | <span data-ttu-id="07776-124">Valor</span><span class="sxs-lookup"><span data-stu-id="07776-124">Value</span></span>                      |
|-------------------------|--------------------|----------------------------|
| <span data-ttu-id="07776-125">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="07776-125">DataType</span></span><br/>     | <span data-ttu-id="07776-126">string</span><span class="sxs-lookup"><span data-stu-id="07776-126">string</span></span><br/>  | <span data-ttu-id="07776-127">xs:integer</span><span class="sxs-lookup"><span data-stu-id="07776-127">xs:integer</span></span><br/>      |
| <span data-ttu-id="07776-128">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="07776-128">DefaultValue</span></span><br/> | <span data-ttu-id="07776-129">Número inteiro</span><span class="sxs-lookup"><span data-stu-id="07776-129">integer</span></span><br/> | <span data-ttu-id="07776-130">não definido</span><span class="sxs-lookup"><span data-stu-id="07776-130">undefined</span></span><br/>       |
| <span data-ttu-id="07776-131">MaxValue</span><span class="sxs-lookup"><span data-stu-id="07776-131">MaxValue</span></span><br/>     | <span data-ttu-id="07776-132">Número inteiro</span><span class="sxs-lookup"><span data-stu-id="07776-132">integer</span></span><br/> | <span data-ttu-id="07776-133">não definido</span><span class="sxs-lookup"><span data-stu-id="07776-133">undefined</span></span><br/>       |
| <span data-ttu-id="07776-134">MinValue</span><span class="sxs-lookup"><span data-stu-id="07776-134">MinValue</span></span><br/>     | <span data-ttu-id="07776-135">Número inteiro</span><span class="sxs-lookup"><span data-stu-id="07776-135">integer</span></span><br/> | <span data-ttu-id="07776-136">não definido</span><span class="sxs-lookup"><span data-stu-id="07776-136">undefined</span></span><br/>       |
| <span data-ttu-id="07776-137">Vários</span><span class="sxs-lookup"><span data-stu-id="07776-137">Multiple</span></span><br/>     | <span data-ttu-id="07776-138">Número inteiro</span><span class="sxs-lookup"><span data-stu-id="07776-138">integer</span></span><br/> | <span data-ttu-id="07776-139">não definido</span><span class="sxs-lookup"><span data-stu-id="07776-139">undefined</span></span><br/>       |
| <span data-ttu-id="07776-140">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="07776-140">Mandatory</span></span><br/>    | <span data-ttu-id="07776-141">string</span><span class="sxs-lookup"><span data-stu-id="07776-141">string</span></span><br/>  | <span data-ttu-id="07776-142">PSK: condicional</span><span class="sxs-lookup"><span data-stu-id="07776-142">psk:Conditional</span></span><br/> |
| <span data-ttu-id="07776-143">UnitType</span><span class="sxs-lookup"><span data-stu-id="07776-143">UnitType</span></span><br/>     | <span data-ttu-id="07776-144">string</span><span class="sxs-lookup"><span data-stu-id="07776-144">string</span></span><br/>  | <span data-ttu-id="07776-145">pontos</span><span class="sxs-lookup"><span data-stu-id="07776-145">points</span></span><br/>          |



 

## <a name="related-topics"></a><span data-ttu-id="07776-146">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="07776-146">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="07776-147">Especificação de esquema de impressão</span><span class="sxs-lookup"><span data-stu-id="07776-147">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




