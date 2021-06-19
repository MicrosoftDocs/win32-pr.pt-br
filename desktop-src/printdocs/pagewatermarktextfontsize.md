---
description: Obter informações sobre o parâmetro PageWatermarkTextFontSize. Este tópico não é atual. Para obter as informações mais atuais, consulte a Especificação de Esquema de Impressão.
ms.assetid: 4c379898-d21f-4c6c-93c8-e5f386e032ba
title: PageWatermarkTextFontSize
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9eb28044ca676dedfb136cb58190db90a06fd624
ms.sourcegitcommit: 91530c19d26ba4c57a6af1f37b57f211f580464e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/19/2021
ms.locfileid: "112395991"
---
# <a name="pagewatermarktextfontsize"></a><span data-ttu-id="77e74-105">PageWatermarkTextFontSize</span><span class="sxs-lookup"><span data-stu-id="77e74-105">PageWatermarkTextFontSize</span></span>

<span data-ttu-id="77e74-106">Este tópico não é atual.</span><span class="sxs-lookup"><span data-stu-id="77e74-106">This topic is not current.</span></span> <span data-ttu-id="77e74-107">Para obter as informações mais atuais, consulte a [Especificação de Esquema de Impressão](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="77e74-107">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="77e74-108">Define os tamanhos de fonte disponíveis para o texto de marca-d'água.</span><span class="sxs-lookup"><span data-stu-id="77e74-108">Defines the available font sizes for the watermark text.</span></span>

-   [<span data-ttu-id="77e74-109">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="77e74-109">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="77e74-110">Conteúdo da estrutura</span><span class="sxs-lookup"><span data-stu-id="77e74-110">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="77e74-111">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="77e74-111">Element Information</span></span>



| <span data-ttu-id="77e74-112">Name</span><span class="sxs-lookup"><span data-stu-id="77e74-112">Name</span></span> | <span data-ttu-id="77e74-113">Valor</span><span class="sxs-lookup"><span data-stu-id="77e74-113">Value</span></span> |
|----------------------------|--------------------------------------------|
| <span data-ttu-id="77e74-114">Tipo de elemento</span><span class="sxs-lookup"><span data-stu-id="77e74-114">Element Type</span></span> <br/>   | <span data-ttu-id="77e74-115">ParameterDef</span><span class="sxs-lookup"><span data-stu-id="77e74-115">ParameterDef</span></span><br/>                    |
| <span data-ttu-id="77e74-116">Prefixo de definição de scoping</span><span class="sxs-lookup"><span data-stu-id="77e74-116">Scoping Prefix</span></span> <br/> | <span data-ttu-id="77e74-117">?</span><span class="sxs-lookup"><span data-stu-id="77e74-117">Page</span></span><br/>                            |
| <span data-ttu-id="77e74-118">Observações</span><span class="sxs-lookup"><span data-stu-id="77e74-118">Notes</span></span> <br/>          | <span data-ttu-id="77e74-119">Vinculado ao elemento PageWatermark</span><span class="sxs-lookup"><span data-stu-id="77e74-119">Linked to PageWatermark element</span></span><br/> |



 

## <a name="structure-content"></a><span data-ttu-id="77e74-120">Conteúdo da estrutura</span><span class="sxs-lookup"><span data-stu-id="77e74-120">Structure Content</span></span>

<span data-ttu-id="77e74-121">A estrutura XML desse elemento é a seguinte:</span><span class="sxs-lookup"><span data-stu-id="77e74-121">The XML structure of this element is as follows:</span></span>

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

## <a name="structure-properties"></a><span data-ttu-id="77e74-122">Propriedades da estrutura</span><span class="sxs-lookup"><span data-stu-id="77e74-122">Structure Properties</span></span>

<span data-ttu-id="77e74-123">A tabela a seguir descreve as características das variáveis definidas na estrutura XML.</span><span class="sxs-lookup"><span data-stu-id="77e74-123">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="77e74-124">Propriedade</span><span class="sxs-lookup"><span data-stu-id="77e74-124">Property</span></span>                | <span data-ttu-id="77e74-125">xsi:type</span><span class="sxs-lookup"><span data-stu-id="77e74-125">xsi:type</span></span>           | <span data-ttu-id="77e74-126">Valor</span><span class="sxs-lookup"><span data-stu-id="77e74-126">Value</span></span>                      |
|-------------------------|--------------------|----------------------------|
| <span data-ttu-id="77e74-127">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="77e74-127">DataType</span></span><br/>     | <span data-ttu-id="77e74-128">string</span><span class="sxs-lookup"><span data-stu-id="77e74-128">string</span></span><br/>  | <span data-ttu-id="77e74-129">xs:integer</span><span class="sxs-lookup"><span data-stu-id="77e74-129">xs:integer</span></span><br/>      |
| <span data-ttu-id="77e74-130">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="77e74-130">DefaultValue</span></span><br/> | <span data-ttu-id="77e74-131">Número inteiro</span><span class="sxs-lookup"><span data-stu-id="77e74-131">integer</span></span><br/> | <span data-ttu-id="77e74-132">não definido</span><span class="sxs-lookup"><span data-stu-id="77e74-132">undefined</span></span><br/>       |
| <span data-ttu-id="77e74-133">MaxValue</span><span class="sxs-lookup"><span data-stu-id="77e74-133">MaxValue</span></span><br/>     | <span data-ttu-id="77e74-134">Número inteiro</span><span class="sxs-lookup"><span data-stu-id="77e74-134">integer</span></span><br/> | <span data-ttu-id="77e74-135">não definido</span><span class="sxs-lookup"><span data-stu-id="77e74-135">undefined</span></span><br/>       |
| <span data-ttu-id="77e74-136">Minvalue</span><span class="sxs-lookup"><span data-stu-id="77e74-136">MinValue</span></span><br/>     | <span data-ttu-id="77e74-137">Número inteiro</span><span class="sxs-lookup"><span data-stu-id="77e74-137">integer</span></span><br/> | <span data-ttu-id="77e74-138">não definido</span><span class="sxs-lookup"><span data-stu-id="77e74-138">undefined</span></span><br/>       |
| <span data-ttu-id="77e74-139">Vários</span><span class="sxs-lookup"><span data-stu-id="77e74-139">Multiple</span></span><br/>     | <span data-ttu-id="77e74-140">Número inteiro</span><span class="sxs-lookup"><span data-stu-id="77e74-140">integer</span></span><br/> | <span data-ttu-id="77e74-141">não definido</span><span class="sxs-lookup"><span data-stu-id="77e74-141">undefined</span></span><br/>       |
| <span data-ttu-id="77e74-142">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="77e74-142">Mandatory</span></span><br/>    | <span data-ttu-id="77e74-143">string</span><span class="sxs-lookup"><span data-stu-id="77e74-143">string</span></span><br/>  | <span data-ttu-id="77e74-144">psk:Conditional</span><span class="sxs-lookup"><span data-stu-id="77e74-144">psk:Conditional</span></span><br/> |
| <span data-ttu-id="77e74-145">Unittype</span><span class="sxs-lookup"><span data-stu-id="77e74-145">UnitType</span></span><br/>     | <span data-ttu-id="77e74-146">string</span><span class="sxs-lookup"><span data-stu-id="77e74-146">string</span></span><br/>  | <span data-ttu-id="77e74-147">pontos</span><span class="sxs-lookup"><span data-stu-id="77e74-147">points</span></span><br/>          |



 

## <a name="related-topics"></a><span data-ttu-id="77e74-148">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="77e74-148">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="77e74-149">Especificação de esquema de impressão</span><span class="sxs-lookup"><span data-stu-id="77e74-149">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




