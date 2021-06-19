---
description: Obter mais informações sobre o parâmetro PageWatermarkTextText. Este tópico não é atual. Para obter as informações mais atuais, consulte a Especificação de Esquema de Impressão.
ms.assetid: 3b01f05c-fe2e-4467-b2a7-5431a41200cd
title: PageWatermarkTextText
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3db5ef33008f0ccb66b6af34e2cc245b90c1ebea
ms.sourcegitcommit: 91530c19d26ba4c57a6af1f37b57f211f580464e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/19/2021
ms.locfileid: "112395961"
---
# <a name="pagewatermarktexttext"></a><span data-ttu-id="3926e-105">PageWatermarkTextText</span><span class="sxs-lookup"><span data-stu-id="3926e-105">PageWatermarkTextText</span></span>

<span data-ttu-id="3926e-106">Este tópico não é atual.</span><span class="sxs-lookup"><span data-stu-id="3926e-106">This topic is not current.</span></span> <span data-ttu-id="3926e-107">Para obter as informações mais atuais, consulte a [Especificação de Esquema de Impressão](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="3926e-107">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="3926e-108">Especifica o texto da marca-d'água.</span><span class="sxs-lookup"><span data-stu-id="3926e-108">Specifies the text of the watermark.</span></span>

-   [<span data-ttu-id="3926e-109">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="3926e-109">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="3926e-110">Conteúdo da estrutura</span><span class="sxs-lookup"><span data-stu-id="3926e-110">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="3926e-111">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="3926e-111">Element Information</span></span>



| <span data-ttu-id="3926e-112">Name</span><span class="sxs-lookup"><span data-stu-id="3926e-112">Name</span></span> | <span data-ttu-id="3926e-113">Valor</span><span class="sxs-lookup"><span data-stu-id="3926e-113">Value</span></span> |
|----------------------------|--------------------------------------------|
| <span data-ttu-id="3926e-114">Tipo de elemento</span><span class="sxs-lookup"><span data-stu-id="3926e-114">Element Type</span></span> <br/>   | <span data-ttu-id="3926e-115">ParameterDef</span><span class="sxs-lookup"><span data-stu-id="3926e-115">ParameterDef</span></span><br/>                    |
| <span data-ttu-id="3926e-116">Prefixo de definição de scoping</span><span class="sxs-lookup"><span data-stu-id="3926e-116">Scoping Prefix</span></span> <br/> | <span data-ttu-id="3926e-117">?</span><span class="sxs-lookup"><span data-stu-id="3926e-117">Page</span></span><br/>                            |
| <span data-ttu-id="3926e-118">Observações</span><span class="sxs-lookup"><span data-stu-id="3926e-118">Notes</span></span> <br/>          | <span data-ttu-id="3926e-119">Vinculado ao elemento PageWatermark</span><span class="sxs-lookup"><span data-stu-id="3926e-119">Linked to PageWatermark element</span></span><br/> |



 

## <a name="structure-content"></a><span data-ttu-id="3926e-120">Conteúdo da estrutura</span><span class="sxs-lookup"><span data-stu-id="3926e-120">Structure Content</span></span>

<span data-ttu-id="3926e-121">A estrutura XML desse elemento é a seguinte:</span><span class="sxs-lookup"><span data-stu-id="3926e-121">The XML structure of this element is as follows:</span></span>

``` syntax
<psf:ParameterDef name="psk:PageWatermarkTextText">
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
    <psf:Value xsi:type="xs:integer">1</psf:Value>
  </psf:Property>
  <psf:Property name="psf:Mandatory">
    <psf:Value xsi:type="xs:string">psk:Conditional</psf:Value>
  </psf:Property>
  <psf:Property name="psf:UnitType">
    <psf:Value xsi:type="xs:string">characters</psf:Value>
  </psf:Property>
</psf:ParameterDef>
```

## <a name="structure-properties"></a><span data-ttu-id="3926e-122">Propriedades da estrutura</span><span class="sxs-lookup"><span data-stu-id="3926e-122">Structure Properties</span></span>

<span data-ttu-id="3926e-123">A tabela a seguir descreve as características das variáveis definidas na estrutura XML.</span><span class="sxs-lookup"><span data-stu-id="3926e-123">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="3926e-124">Propriedade</span><span class="sxs-lookup"><span data-stu-id="3926e-124">Property</span></span>                | <span data-ttu-id="3926e-125">xsi:type</span><span class="sxs-lookup"><span data-stu-id="3926e-125">xsi:type</span></span>           | <span data-ttu-id="3926e-126">Valor</span><span class="sxs-lookup"><span data-stu-id="3926e-126">Value</span></span>                      |
|-------------------------|--------------------|----------------------------|
| <span data-ttu-id="3926e-127">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="3926e-127">DataType</span></span><br/>     | <span data-ttu-id="3926e-128">String</span><span class="sxs-lookup"><span data-stu-id="3926e-128">String</span></span><br/>  | <span data-ttu-id="3926e-129">xs:string</span><span class="sxs-lookup"><span data-stu-id="3926e-129">xs:string</span></span><br/>       |
| <span data-ttu-id="3926e-130">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="3926e-130">DefaultValue</span></span><br/> | <span data-ttu-id="3926e-131">Integer</span><span class="sxs-lookup"><span data-stu-id="3926e-131">Integer</span></span><br/> | <span data-ttu-id="3926e-132">não definido</span><span class="sxs-lookup"><span data-stu-id="3926e-132">undefined</span></span><br/>       |
| <span data-ttu-id="3926e-133">MaxLength</span><span class="sxs-lookup"><span data-stu-id="3926e-133">MaxLength</span></span><br/>    | <span data-ttu-id="3926e-134">Integer</span><span class="sxs-lookup"><span data-stu-id="3926e-134">Integer</span></span><br/> | <span data-ttu-id="3926e-135">não definido</span><span class="sxs-lookup"><span data-stu-id="3926e-135">undefined</span></span><br/>       |
| <span data-ttu-id="3926e-136">Minlength</span><span class="sxs-lookup"><span data-stu-id="3926e-136">MinLength</span></span><br/>    | <span data-ttu-id="3926e-137">Integer</span><span class="sxs-lookup"><span data-stu-id="3926e-137">Integer</span></span><br/> | <span data-ttu-id="3926e-138">1</span><span class="sxs-lookup"><span data-stu-id="3926e-138">1</span></span><br/>               |
| <span data-ttu-id="3926e-139">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="3926e-139">Mandatory</span></span><br/>    | <span data-ttu-id="3926e-140">String</span><span class="sxs-lookup"><span data-stu-id="3926e-140">String</span></span><br/>  | <span data-ttu-id="3926e-141">psk:Conditional</span><span class="sxs-lookup"><span data-stu-id="3926e-141">psk:Conditional</span></span><br/> |
| <span data-ttu-id="3926e-142">Unittype</span><span class="sxs-lookup"><span data-stu-id="3926e-142">UnitType</span></span><br/>     | <span data-ttu-id="3926e-143">String</span><span class="sxs-lookup"><span data-stu-id="3926e-143">String</span></span><br/>  | <span data-ttu-id="3926e-144">characters</span><span class="sxs-lookup"><span data-stu-id="3926e-144">characters</span></span><br/>      |



 

## <a name="related-topics"></a><span data-ttu-id="3926e-145">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="3926e-145">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3926e-146">Especificação de esquema de impressão</span><span class="sxs-lookup"><span data-stu-id="3926e-146">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




