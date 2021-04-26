---
description: Este tópico não é atual. Para obter as informações mais atuais, consulte a especificação do esquema de impressão.
ms.assetid: 3b01f05c-fe2e-4467-b2a7-5431a41200cd
title: PageWatermarkTextText
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eb19f5965347e79732aa116e5be51f90e4ef6943
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/26/2021
ms.locfileid: "107996073"
---
# <a name="pagewatermarktexttext"></a><span data-ttu-id="88326-104">PageWatermarkTextText</span><span class="sxs-lookup"><span data-stu-id="88326-104">PageWatermarkTextText</span></span>

<span data-ttu-id="88326-105">Este tópico não é atual.</span><span class="sxs-lookup"><span data-stu-id="88326-105">This topic is not current.</span></span> <span data-ttu-id="88326-106">Para obter as informações mais atuais, consulte a [especificação do esquema de impressão](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="88326-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="88326-107">Especifica o texto da marca d' água.</span><span class="sxs-lookup"><span data-stu-id="88326-107">Specifies the text of the watermark.</span></span>

-   [<span data-ttu-id="88326-108">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="88326-108">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="88326-109">Conteúdo da estrutura</span><span class="sxs-lookup"><span data-stu-id="88326-109">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="88326-110">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="88326-110">Element Information</span></span>



| <span data-ttu-id="88326-111">Nome</span><span class="sxs-lookup"><span data-stu-id="88326-111">Name</span></span> | <span data-ttu-id="88326-112">Valor</span><span class="sxs-lookup"><span data-stu-id="88326-112">Value</span></span> |
|----------------------------|--------------------------------------------|
| <span data-ttu-id="88326-113">Tipo de elemento</span><span class="sxs-lookup"><span data-stu-id="88326-113">Element Type</span></span> <br/>   | <span data-ttu-id="88326-114">ParameterDef</span><span class="sxs-lookup"><span data-stu-id="88326-114">ParameterDef</span></span><br/>                    |
| <span data-ttu-id="88326-115">Prefixo de escopo</span><span class="sxs-lookup"><span data-stu-id="88326-115">Scoping Prefix</span></span> <br/> | <span data-ttu-id="88326-116">?</span><span class="sxs-lookup"><span data-stu-id="88326-116">Page</span></span><br/>                            |
| <span data-ttu-id="88326-117">Observações</span><span class="sxs-lookup"><span data-stu-id="88326-117">Notes</span></span> <br/>          | <span data-ttu-id="88326-118">Vinculado ao elemento PageWatermark</span><span class="sxs-lookup"><span data-stu-id="88326-118">Linked to PageWatermark element</span></span><br/> |



 

## <a name="structure-content"></a><span data-ttu-id="88326-119">Conteúdo da estrutura</span><span class="sxs-lookup"><span data-stu-id="88326-119">Structure Content</span></span>

<span data-ttu-id="88326-120">A estrutura XML desse elemento é a seguinte:</span><span class="sxs-lookup"><span data-stu-id="88326-120">The XML structure of this element is as follows:</span></span>

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

## <a name="structure-properties"></a><span data-ttu-id="88326-121">Propriedades da estrutura</span><span class="sxs-lookup"><span data-stu-id="88326-121">Structure Properties</span></span>

<span data-ttu-id="88326-122">A tabela a seguir descreve as características das variáveis definidas na estrutura XML.</span><span class="sxs-lookup"><span data-stu-id="88326-122">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="88326-123">Propriedade</span><span class="sxs-lookup"><span data-stu-id="88326-123">Property</span></span>                | <span data-ttu-id="88326-124">xsi:type</span><span class="sxs-lookup"><span data-stu-id="88326-124">xsi:type</span></span>           | <span data-ttu-id="88326-125">Valor</span><span class="sxs-lookup"><span data-stu-id="88326-125">Value</span></span>                      |
|-------------------------|--------------------|----------------------------|
| <span data-ttu-id="88326-126">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="88326-126">DataType</span></span><br/>     | <span data-ttu-id="88326-127">String</span><span class="sxs-lookup"><span data-stu-id="88326-127">String</span></span><br/>  | <span data-ttu-id="88326-128">xs:string</span><span class="sxs-lookup"><span data-stu-id="88326-128">xs:string</span></span><br/>       |
| <span data-ttu-id="88326-129">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="88326-129">DefaultValue</span></span><br/> | <span data-ttu-id="88326-130">Integer</span><span class="sxs-lookup"><span data-stu-id="88326-130">Integer</span></span><br/> | <span data-ttu-id="88326-131">não definido</span><span class="sxs-lookup"><span data-stu-id="88326-131">undefined</span></span><br/>       |
| <span data-ttu-id="88326-132">MaxLength</span><span class="sxs-lookup"><span data-stu-id="88326-132">MaxLength</span></span><br/>    | <span data-ttu-id="88326-133">Integer</span><span class="sxs-lookup"><span data-stu-id="88326-133">Integer</span></span><br/> | <span data-ttu-id="88326-134">não definido</span><span class="sxs-lookup"><span data-stu-id="88326-134">undefined</span></span><br/>       |
| <span data-ttu-id="88326-135">MinLength</span><span class="sxs-lookup"><span data-stu-id="88326-135">MinLength</span></span><br/>    | <span data-ttu-id="88326-136">Integer</span><span class="sxs-lookup"><span data-stu-id="88326-136">Integer</span></span><br/> | <span data-ttu-id="88326-137">1</span><span class="sxs-lookup"><span data-stu-id="88326-137">1</span></span><br/>               |
| <span data-ttu-id="88326-138">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="88326-138">Mandatory</span></span><br/>    | <span data-ttu-id="88326-139">String</span><span class="sxs-lookup"><span data-stu-id="88326-139">String</span></span><br/>  | <span data-ttu-id="88326-140">PSK: condicional</span><span class="sxs-lookup"><span data-stu-id="88326-140">psk:Conditional</span></span><br/> |
| <span data-ttu-id="88326-141">UnitType</span><span class="sxs-lookup"><span data-stu-id="88326-141">UnitType</span></span><br/>     | <span data-ttu-id="88326-142">String</span><span class="sxs-lookup"><span data-stu-id="88326-142">String</span></span><br/>  | <span data-ttu-id="88326-143">characters</span><span class="sxs-lookup"><span data-stu-id="88326-143">characters</span></span><br/>      |



 

## <a name="related-topics"></a><span data-ttu-id="88326-144">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="88326-144">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="88326-145">Especificação de esquema de impressão</span><span class="sxs-lookup"><span data-stu-id="88326-145">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




