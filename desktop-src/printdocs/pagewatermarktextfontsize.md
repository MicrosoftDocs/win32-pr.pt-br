---
description: Este tópico não é atual. Para obter as informações mais atuais, consulte a especificação do esquema de impressão.
ms.assetid: 4c379898-d21f-4c6c-93c8-e5f386e032ba
title: PageWatermarkTextFontSize
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 72cc8c7f3c9a692ffbe180c253d448d7c4e320d7
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/26/2021
ms.locfileid: "107999118"
---
# <a name="pagewatermarktextfontsize"></a><span data-ttu-id="7a24e-104">PageWatermarkTextFontSize</span><span class="sxs-lookup"><span data-stu-id="7a24e-104">PageWatermarkTextFontSize</span></span>

<span data-ttu-id="7a24e-105">Este tópico não é atual.</span><span class="sxs-lookup"><span data-stu-id="7a24e-105">This topic is not current.</span></span> <span data-ttu-id="7a24e-106">Para obter as informações mais atuais, consulte a [especificação do esquema de impressão](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="7a24e-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="7a24e-107">Define os tamanhos de fonte disponíveis para o texto de marca d' água.</span><span class="sxs-lookup"><span data-stu-id="7a24e-107">Defines the available font sizes for the watermark text.</span></span>

-   [<span data-ttu-id="7a24e-108">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="7a24e-108">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="7a24e-109">Conteúdo da estrutura</span><span class="sxs-lookup"><span data-stu-id="7a24e-109">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="7a24e-110">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="7a24e-110">Element Information</span></span>



| <span data-ttu-id="7a24e-111">Nome</span><span class="sxs-lookup"><span data-stu-id="7a24e-111">Name</span></span> | <span data-ttu-id="7a24e-112">Valor</span><span class="sxs-lookup"><span data-stu-id="7a24e-112">Value</span></span> |
|----------------------------|--------------------------------------------|
| <span data-ttu-id="7a24e-113">Tipo de elemento</span><span class="sxs-lookup"><span data-stu-id="7a24e-113">Element Type</span></span> <br/>   | <span data-ttu-id="7a24e-114">ParameterDef</span><span class="sxs-lookup"><span data-stu-id="7a24e-114">ParameterDef</span></span><br/>                    |
| <span data-ttu-id="7a24e-115">Prefixo de escopo</span><span class="sxs-lookup"><span data-stu-id="7a24e-115">Scoping Prefix</span></span> <br/> | <span data-ttu-id="7a24e-116">?</span><span class="sxs-lookup"><span data-stu-id="7a24e-116">Page</span></span><br/>                            |
| <span data-ttu-id="7a24e-117">Observações</span><span class="sxs-lookup"><span data-stu-id="7a24e-117">Notes</span></span> <br/>          | <span data-ttu-id="7a24e-118">Vinculado ao elemento PageWatermark</span><span class="sxs-lookup"><span data-stu-id="7a24e-118">Linked to PageWatermark element</span></span><br/> |



 

## <a name="structure-content"></a><span data-ttu-id="7a24e-119">Conteúdo da estrutura</span><span class="sxs-lookup"><span data-stu-id="7a24e-119">Structure Content</span></span>

<span data-ttu-id="7a24e-120">A estrutura XML desse elemento é a seguinte:</span><span class="sxs-lookup"><span data-stu-id="7a24e-120">The XML structure of this element is as follows:</span></span>

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

## <a name="structure-properties"></a><span data-ttu-id="7a24e-121">Propriedades da estrutura</span><span class="sxs-lookup"><span data-stu-id="7a24e-121">Structure Properties</span></span>

<span data-ttu-id="7a24e-122">A tabela a seguir descreve as características das variáveis definidas na estrutura XML.</span><span class="sxs-lookup"><span data-stu-id="7a24e-122">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="7a24e-123">Propriedade</span><span class="sxs-lookup"><span data-stu-id="7a24e-123">Property</span></span>                | <span data-ttu-id="7a24e-124">xsi:type</span><span class="sxs-lookup"><span data-stu-id="7a24e-124">xsi:type</span></span>           | <span data-ttu-id="7a24e-125">Valor</span><span class="sxs-lookup"><span data-stu-id="7a24e-125">Value</span></span>                      |
|-------------------------|--------------------|----------------------------|
| <span data-ttu-id="7a24e-126">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="7a24e-126">DataType</span></span><br/>     | <span data-ttu-id="7a24e-127">string</span><span class="sxs-lookup"><span data-stu-id="7a24e-127">string</span></span><br/>  | <span data-ttu-id="7a24e-128">xs:integer</span><span class="sxs-lookup"><span data-stu-id="7a24e-128">xs:integer</span></span><br/>      |
| <span data-ttu-id="7a24e-129">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="7a24e-129">DefaultValue</span></span><br/> | <span data-ttu-id="7a24e-130">Número inteiro</span><span class="sxs-lookup"><span data-stu-id="7a24e-130">integer</span></span><br/> | <span data-ttu-id="7a24e-131">não definido</span><span class="sxs-lookup"><span data-stu-id="7a24e-131">undefined</span></span><br/>       |
| <span data-ttu-id="7a24e-132">MaxValue</span><span class="sxs-lookup"><span data-stu-id="7a24e-132">MaxValue</span></span><br/>     | <span data-ttu-id="7a24e-133">Número inteiro</span><span class="sxs-lookup"><span data-stu-id="7a24e-133">integer</span></span><br/> | <span data-ttu-id="7a24e-134">não definido</span><span class="sxs-lookup"><span data-stu-id="7a24e-134">undefined</span></span><br/>       |
| <span data-ttu-id="7a24e-135">MinValue</span><span class="sxs-lookup"><span data-stu-id="7a24e-135">MinValue</span></span><br/>     | <span data-ttu-id="7a24e-136">Número inteiro</span><span class="sxs-lookup"><span data-stu-id="7a24e-136">integer</span></span><br/> | <span data-ttu-id="7a24e-137">não definido</span><span class="sxs-lookup"><span data-stu-id="7a24e-137">undefined</span></span><br/>       |
| <span data-ttu-id="7a24e-138">Vários</span><span class="sxs-lookup"><span data-stu-id="7a24e-138">Multiple</span></span><br/>     | <span data-ttu-id="7a24e-139">Número inteiro</span><span class="sxs-lookup"><span data-stu-id="7a24e-139">integer</span></span><br/> | <span data-ttu-id="7a24e-140">não definido</span><span class="sxs-lookup"><span data-stu-id="7a24e-140">undefined</span></span><br/>       |
| <span data-ttu-id="7a24e-141">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="7a24e-141">Mandatory</span></span><br/>    | <span data-ttu-id="7a24e-142">string</span><span class="sxs-lookup"><span data-stu-id="7a24e-142">string</span></span><br/>  | <span data-ttu-id="7a24e-143">PSK: condicional</span><span class="sxs-lookup"><span data-stu-id="7a24e-143">psk:Conditional</span></span><br/> |
| <span data-ttu-id="7a24e-144">UnitType</span><span class="sxs-lookup"><span data-stu-id="7a24e-144">UnitType</span></span><br/>     | <span data-ttu-id="7a24e-145">string</span><span class="sxs-lookup"><span data-stu-id="7a24e-145">string</span></span><br/>  | <span data-ttu-id="7a24e-146">pontos</span><span class="sxs-lookup"><span data-stu-id="7a24e-146">points</span></span><br/>          |



 

## <a name="related-topics"></a><span data-ttu-id="7a24e-147">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="7a24e-147">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7a24e-148">Especificação de esquema de impressão</span><span class="sxs-lookup"><span data-stu-id="7a24e-148">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




