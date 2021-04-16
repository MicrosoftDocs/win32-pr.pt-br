---
description: Este tópico não é atual. Para obter as informações mais atuais, consulte a especificação do esquema de impressão.
ms.assetid: 3b01f05c-fe2e-4467-b2a7-5431a41200cd
title: PageWatermarkTextText
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aef2310efaa91532493f7add14de8c2510e24e9b
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/05/2021
ms.locfileid: "105759096"
---
# <a name="pagewatermarktexttext"></a><span data-ttu-id="19bce-104">PageWatermarkTextText</span><span class="sxs-lookup"><span data-stu-id="19bce-104">PageWatermarkTextText</span></span>

<span data-ttu-id="19bce-105">Este tópico não é atual.</span><span class="sxs-lookup"><span data-stu-id="19bce-105">This topic is not current.</span></span> <span data-ttu-id="19bce-106">Para obter as informações mais atuais, consulte a [especificação do esquema de impressão](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="19bce-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="19bce-107">Especifica o texto da marca d' água.</span><span class="sxs-lookup"><span data-stu-id="19bce-107">Specifies the text of the watermark.</span></span>

-   [<span data-ttu-id="19bce-108">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="19bce-108">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="19bce-109">Conteúdo da estrutura</span><span class="sxs-lookup"><span data-stu-id="19bce-109">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="19bce-110">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="19bce-110">Element Information</span></span>



| <span data-ttu-id="19bce-111">Nome</span><span class="sxs-lookup"><span data-stu-id="19bce-111">Name</span></span>                       |                                            |
|----------------------------|--------------------------------------------|
| <span data-ttu-id="19bce-112">Tipo de elemento</span><span class="sxs-lookup"><span data-stu-id="19bce-112">Element Type</span></span> <br/>   | <span data-ttu-id="19bce-113">ParameterDef</span><span class="sxs-lookup"><span data-stu-id="19bce-113">ParameterDef</span></span><br/>                    |
| <span data-ttu-id="19bce-114">Prefixo de escopo</span><span class="sxs-lookup"><span data-stu-id="19bce-114">Scoping Prefix</span></span> <br/> | <span data-ttu-id="19bce-115">?</span><span class="sxs-lookup"><span data-stu-id="19bce-115">Page</span></span><br/>                            |
| <span data-ttu-id="19bce-116">Observações</span><span class="sxs-lookup"><span data-stu-id="19bce-116">Notes</span></span> <br/>          | <span data-ttu-id="19bce-117">Vinculado ao elemento PageWatermark</span><span class="sxs-lookup"><span data-stu-id="19bce-117">Linked to PageWatermark element</span></span><br/> |



 

## <a name="structure-content"></a><span data-ttu-id="19bce-118">Conteúdo da estrutura</span><span class="sxs-lookup"><span data-stu-id="19bce-118">Structure Content</span></span>

<span data-ttu-id="19bce-119">A estrutura XML desse elemento é a seguinte:</span><span class="sxs-lookup"><span data-stu-id="19bce-119">The XML structure of this element is as follows:</span></span>

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

## <a name="structure-properties"></a><span data-ttu-id="19bce-120">Propriedades da estrutura</span><span class="sxs-lookup"><span data-stu-id="19bce-120">Structure Properties</span></span>

<span data-ttu-id="19bce-121">A tabela a seguir descreve as características das variáveis definidas na estrutura XML.</span><span class="sxs-lookup"><span data-stu-id="19bce-121">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="19bce-122">Propriedade</span><span class="sxs-lookup"><span data-stu-id="19bce-122">Property</span></span>                | <span data-ttu-id="19bce-123">xsi:type</span><span class="sxs-lookup"><span data-stu-id="19bce-123">xsi:type</span></span>           | <span data-ttu-id="19bce-124">Valor</span><span class="sxs-lookup"><span data-stu-id="19bce-124">Value</span></span>                      |
|-------------------------|--------------------|----------------------------|
| <span data-ttu-id="19bce-125">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="19bce-125">DataType</span></span><br/>     | <span data-ttu-id="19bce-126">String</span><span class="sxs-lookup"><span data-stu-id="19bce-126">String</span></span><br/>  | <span data-ttu-id="19bce-127">xs:string</span><span class="sxs-lookup"><span data-stu-id="19bce-127">xs:string</span></span><br/>       |
| <span data-ttu-id="19bce-128">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="19bce-128">DefaultValue</span></span><br/> | <span data-ttu-id="19bce-129">Integer</span><span class="sxs-lookup"><span data-stu-id="19bce-129">Integer</span></span><br/> | <span data-ttu-id="19bce-130">não definido</span><span class="sxs-lookup"><span data-stu-id="19bce-130">undefined</span></span><br/>       |
| <span data-ttu-id="19bce-131">MaxLength</span><span class="sxs-lookup"><span data-stu-id="19bce-131">MaxLength</span></span><br/>    | <span data-ttu-id="19bce-132">Integer</span><span class="sxs-lookup"><span data-stu-id="19bce-132">Integer</span></span><br/> | <span data-ttu-id="19bce-133">não definido</span><span class="sxs-lookup"><span data-stu-id="19bce-133">undefined</span></span><br/>       |
| <span data-ttu-id="19bce-134">MinLength</span><span class="sxs-lookup"><span data-stu-id="19bce-134">MinLength</span></span><br/>    | <span data-ttu-id="19bce-135">Integer</span><span class="sxs-lookup"><span data-stu-id="19bce-135">Integer</span></span><br/> | <span data-ttu-id="19bce-136">1</span><span class="sxs-lookup"><span data-stu-id="19bce-136">1</span></span><br/>               |
| <span data-ttu-id="19bce-137">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="19bce-137">Mandatory</span></span><br/>    | <span data-ttu-id="19bce-138">String</span><span class="sxs-lookup"><span data-stu-id="19bce-138">String</span></span><br/>  | <span data-ttu-id="19bce-139">PSK: condicional</span><span class="sxs-lookup"><span data-stu-id="19bce-139">psk:Conditional</span></span><br/> |
| <span data-ttu-id="19bce-140">UnitType</span><span class="sxs-lookup"><span data-stu-id="19bce-140">UnitType</span></span><br/>     | <span data-ttu-id="19bce-141">String</span><span class="sxs-lookup"><span data-stu-id="19bce-141">String</span></span><br/>  | <span data-ttu-id="19bce-142">characters</span><span class="sxs-lookup"><span data-stu-id="19bce-142">characters</span></span><br/>      |



 

## <a name="related-topics"></a><span data-ttu-id="19bce-143">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="19bce-143">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="19bce-144">Especificação de esquema de impressão</span><span class="sxs-lookup"><span data-stu-id="19bce-144">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




