---
description: Este tópico não é atual. Para obter as informações mais atuais, consulte a especificação do esquema de impressão.
ms.assetid: f94c1450-9648-4aee-8f88-2a9213eba4a9
title: PageWatermarkTransparency
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e8d46a03cfb1b2129f4c89a6ea7c751e23cd565e
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/26/2021
ms.locfileid: "107996873"
---
# <a name="pagewatermarktransparency"></a><span data-ttu-id="f7c9a-104">PageWatermarkTransparency</span><span class="sxs-lookup"><span data-stu-id="f7c9a-104">PageWatermarkTransparency</span></span>

<span data-ttu-id="f7c9a-105">Este tópico não é atual.</span><span class="sxs-lookup"><span data-stu-id="f7c9a-105">This topic is not current.</span></span> <span data-ttu-id="f7c9a-106">Para obter as informações mais atuais, consulte a [especificação do esquema de impressão](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="f7c9a-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="f7c9a-107">Especifica a transparência da marca d' água.</span><span class="sxs-lookup"><span data-stu-id="f7c9a-107">Specifies the transparency for the watermark.</span></span> <span data-ttu-id="f7c9a-108">Totalmente opaco teria um valor de 0.</span><span class="sxs-lookup"><span data-stu-id="f7c9a-108">Fully opaque would have a value of 0.</span></span>

-   [<span data-ttu-id="f7c9a-109">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="f7c9a-109">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="f7c9a-110">Conteúdo da estrutura</span><span class="sxs-lookup"><span data-stu-id="f7c9a-110">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="f7c9a-111">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="f7c9a-111">Element Information</span></span>



| <span data-ttu-id="f7c9a-112">Nome</span><span class="sxs-lookup"><span data-stu-id="f7c9a-112">Name</span></span> | <span data-ttu-id="f7c9a-113">Valor</span><span class="sxs-lookup"><span data-stu-id="f7c9a-113">Value</span></span> |
|----------------------------|--------------------------------------------|
| <span data-ttu-id="f7c9a-114">Tipo de elemento</span><span class="sxs-lookup"><span data-stu-id="f7c9a-114">Element Type</span></span> <br/>   | <span data-ttu-id="f7c9a-115">ParameterDef</span><span class="sxs-lookup"><span data-stu-id="f7c9a-115">ParameterDef</span></span><br/>                    |
| <span data-ttu-id="f7c9a-116">Prefixo de escopo</span><span class="sxs-lookup"><span data-stu-id="f7c9a-116">Scoping Prefix</span></span> <br/> | <span data-ttu-id="f7c9a-117">?</span><span class="sxs-lookup"><span data-stu-id="f7c9a-117">Page</span></span><br/>                            |
| <span data-ttu-id="f7c9a-118">Observações</span><span class="sxs-lookup"><span data-stu-id="f7c9a-118">Notes</span></span> <br/>          | <span data-ttu-id="f7c9a-119">Vinculado ao elemento PageWatermark</span><span class="sxs-lookup"><span data-stu-id="f7c9a-119">Linked to PageWatermark element</span></span><br/> |



 

## <a name="structure-content"></a><span data-ttu-id="f7c9a-120">Conteúdo da estrutura</span><span class="sxs-lookup"><span data-stu-id="f7c9a-120">Structure Content</span></span>

<span data-ttu-id="f7c9a-121">A estrutura XML desse elemento é a seguinte:</span><span class="sxs-lookup"><span data-stu-id="f7c9a-121">The XML structure of this element is as follows:</span></span>

``` syntax
<psf:ParameterDef name="psk:PageWatermarkTransparency">
  <psf:Property name="psf:DataType">
    <psf:Value xsi:type="xs:string">xs:integer</psf:Value>
  </psf:Property>
  <psf:Property name="psf:DefaultValue">
    <psf:Value xsi:type="xs:integer">0</psf:Value>
  </psf:Property>
  <psf:Property name="psf:MaxValue">
    <psf:Value xsi:type="xs:integer">100</psf:Value>
  </psf:Property>
  <psf:Property name="psf:MinValue">
    <psf:Value xsi:type="xs:integer">0</psf:Value>
  </psf:Property>
  <psf:Property name="psf:Multiple">
    <psf:Value xsi:type="xs:integer">1</psf:Value>
  </psf:Property>
  <psf:Property name="psf:Mandatory">
    <psf:Value xsi:type="xs:string">psk:Conditional</psf:Value>
  </psf:Property>
  <psf:Property name="psf:UnitType">
    <psf:Value xsi:type="xs:string">percent</psf:Value>
  </psf:Property>
</psf:ParameterDef>
```

## <a name="structure-properties"></a><span data-ttu-id="f7c9a-122">Propriedades da estrutura</span><span class="sxs-lookup"><span data-stu-id="f7c9a-122">Structure Properties</span></span>

<span data-ttu-id="f7c9a-123">A tabela a seguir descreve as características das variáveis definidas na estrutura XML.</span><span class="sxs-lookup"><span data-stu-id="f7c9a-123">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="f7c9a-124">Propriedade</span><span class="sxs-lookup"><span data-stu-id="f7c9a-124">Property</span></span>                | <span data-ttu-id="f7c9a-125">xsi:type</span><span class="sxs-lookup"><span data-stu-id="f7c9a-125">xsi:type</span></span>           | <span data-ttu-id="f7c9a-126">Valor</span><span class="sxs-lookup"><span data-stu-id="f7c9a-126">Value</span></span>                      |
|-------------------------|--------------------|----------------------------|
| <span data-ttu-id="f7c9a-127">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="f7c9a-127">DataType</span></span><br/>     | <span data-ttu-id="f7c9a-128">string</span><span class="sxs-lookup"><span data-stu-id="f7c9a-128">string</span></span><br/>  | <span data-ttu-id="f7c9a-129">xs:integer</span><span class="sxs-lookup"><span data-stu-id="f7c9a-129">xs:integer</span></span><br/>      |
| <span data-ttu-id="f7c9a-130">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="f7c9a-130">DefaultValue</span></span><br/> | <span data-ttu-id="f7c9a-131">integer</span><span class="sxs-lookup"><span data-stu-id="f7c9a-131">integer</span></span><br/> | <span data-ttu-id="f7c9a-132">0</span><span class="sxs-lookup"><span data-stu-id="f7c9a-132">0</span></span><br/>               |
| <span data-ttu-id="f7c9a-133">MaxValue</span><span class="sxs-lookup"><span data-stu-id="f7c9a-133">MaxValue</span></span><br/>     | <span data-ttu-id="f7c9a-134">Número inteiro</span><span class="sxs-lookup"><span data-stu-id="f7c9a-134">integer</span></span><br/> | <span data-ttu-id="f7c9a-135">100</span><span class="sxs-lookup"><span data-stu-id="f7c9a-135">100</span></span><br/>             |
| <span data-ttu-id="f7c9a-136">MinValue</span><span class="sxs-lookup"><span data-stu-id="f7c9a-136">MinValue</span></span><br/>     | <span data-ttu-id="f7c9a-137">integer</span><span class="sxs-lookup"><span data-stu-id="f7c9a-137">integer</span></span><br/> | <span data-ttu-id="f7c9a-138">0</span><span class="sxs-lookup"><span data-stu-id="f7c9a-138">0</span></span><br/>               |
| <span data-ttu-id="f7c9a-139">Vários</span><span class="sxs-lookup"><span data-stu-id="f7c9a-139">Multiple</span></span><br/>     | <span data-ttu-id="f7c9a-140">integer</span><span class="sxs-lookup"><span data-stu-id="f7c9a-140">integer</span></span><br/> | <span data-ttu-id="f7c9a-141">1</span><span class="sxs-lookup"><span data-stu-id="f7c9a-141">1</span></span><br/>               |
| <span data-ttu-id="f7c9a-142">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="f7c9a-142">Mandatory</span></span><br/>    | <span data-ttu-id="f7c9a-143">string</span><span class="sxs-lookup"><span data-stu-id="f7c9a-143">string</span></span><br/>  | <span data-ttu-id="f7c9a-144">PSK: condicional</span><span class="sxs-lookup"><span data-stu-id="f7c9a-144">psk:Conditional</span></span><br/> |
| <span data-ttu-id="f7c9a-145">UnitType</span><span class="sxs-lookup"><span data-stu-id="f7c9a-145">UnitType</span></span><br/>     | <span data-ttu-id="f7c9a-146">string</span><span class="sxs-lookup"><span data-stu-id="f7c9a-146">string</span></span><br/>  | <span data-ttu-id="f7c9a-147">{1&gt;percent&lt;1}</span><span class="sxs-lookup"><span data-stu-id="f7c9a-147">percent</span></span><br/>         |



 

## <a name="related-topics"></a><span data-ttu-id="f7c9a-148">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="f7c9a-148">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f7c9a-149">Especificação de esquema de impressão</span><span class="sxs-lookup"><span data-stu-id="f7c9a-149">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




