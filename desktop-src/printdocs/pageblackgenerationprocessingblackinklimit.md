---
description: Saiba mais sobre o parâmetro PageBlackGenerationProcessingBlackInkLimit. Este tópico não é atual. Para obter as informações mais atuais, consulte a Especificação de Esquema de Impressão.
ms.assetid: 96b48917-1fbc-467f-b2b4-1a9673f1ee99
title: PageBlackGenerationProcessingBlackInkLimit
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7c753554b240a5fef0012a81c533b6efe938075e
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/30/2021
ms.locfileid: "113118421"
---
# <a name="pageblackgenerationprocessingblackinklimit"></a><span data-ttu-id="15dfd-105">PageBlackGenerationProcessingBlackInkLimit</span><span class="sxs-lookup"><span data-stu-id="15dfd-105">PageBlackGenerationProcessingBlackInkLimit</span></span>

<span data-ttu-id="15dfd-106">Este tópico não é atual.</span><span class="sxs-lookup"><span data-stu-id="15dfd-106">This topic is not current.</span></span> <span data-ttu-id="15dfd-107">Para obter as informações mais atuais, consulte a [Especificação de Esquema de Impressão](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="15dfd-107">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="15dfd-108">O conteúdo do aplicativo rotulado com a cor nomeada especificada DEVE aparecer em todas as separações de cores.</span><span class="sxs-lookup"><span data-stu-id="15dfd-108">Application content labeled with the specified named color MUST appear on all color separations.</span></span>

-   [<span data-ttu-id="15dfd-109">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="15dfd-109">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="15dfd-110">Conteúdo da estrutura</span><span class="sxs-lookup"><span data-stu-id="15dfd-110">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="15dfd-111">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="15dfd-111">Element Information</span></span>



| <span data-ttu-id="15dfd-112">Nome</span><span class="sxs-lookup"><span data-stu-id="15dfd-112">Name</span></span> | <span data-ttu-id="15dfd-113">Valor</span><span class="sxs-lookup"><span data-stu-id="15dfd-113">Value</span></span> |
|----------------------------|------------------------------------------------------------|
| <span data-ttu-id="15dfd-114">Tipo de elemento</span><span class="sxs-lookup"><span data-stu-id="15dfd-114">Element Type</span></span> <br/>   | <span data-ttu-id="15dfd-115">ParameterDef</span><span class="sxs-lookup"><span data-stu-id="15dfd-115">ParameterDef</span></span><br/>                                    |
| <span data-ttu-id="15dfd-116">Prefixo de definição de scoping</span><span class="sxs-lookup"><span data-stu-id="15dfd-116">Scoping Prefix</span></span> <br/> | <span data-ttu-id="15dfd-117">?</span><span class="sxs-lookup"><span data-stu-id="15dfd-117">Page</span></span><br/>                                            |
| <span data-ttu-id="15dfd-118">Observações</span><span class="sxs-lookup"><span data-stu-id="15dfd-118">Notes</span></span> <br/>          | <span data-ttu-id="15dfd-119">Vinculado ao elemento PageBlackGenerationProcessing</span><span class="sxs-lookup"><span data-stu-id="15dfd-119">Linked to PageBlackGenerationProcessing element</span></span><br/> |



 

## <a name="structure-content"></a><span data-ttu-id="15dfd-120">Conteúdo da estrutura</span><span class="sxs-lookup"><span data-stu-id="15dfd-120">Structure Content</span></span>

<span data-ttu-id="15dfd-121">A estrutura XML desse elemento é:</span><span class="sxs-lookup"><span data-stu-id="15dfd-121">The XML structure of this element is:</span></span>

``` syntax
<psf:ParameterDef name="psk:PageBlackGenerationProcessingBlackInkLimit">
  <psf:Property name="psf:DataType">
    <psf:Value xsi:type="xs:string">xs:integer</psf:Value>
  </psf:Property>
  <psf:Property name="psf:DefaultValue">
    <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
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

## <a name="structure-properties"></a><span data-ttu-id="15dfd-122">Propriedades da estrutura</span><span class="sxs-lookup"><span data-stu-id="15dfd-122">Structure Properties</span></span>

<span data-ttu-id="15dfd-123">A tabela a seguir descreve as características das variáveis definidas na estrutura XML.</span><span class="sxs-lookup"><span data-stu-id="15dfd-123">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="15dfd-124">Propriedade</span><span class="sxs-lookup"><span data-stu-id="15dfd-124">Property</span></span>                | <span data-ttu-id="15dfd-125">xsi:type</span><span class="sxs-lookup"><span data-stu-id="15dfd-125">xsi:type</span></span>           | <span data-ttu-id="15dfd-126">Valor</span><span class="sxs-lookup"><span data-stu-id="15dfd-126">Value</span></span>                      |
|-------------------------|--------------------|----------------------------|
| <span data-ttu-id="15dfd-127">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="15dfd-127">DataType</span></span><br/>     | <span data-ttu-id="15dfd-128">string</span><span class="sxs-lookup"><span data-stu-id="15dfd-128">string</span></span><br/>  | <span data-ttu-id="15dfd-129">xs:integer</span><span class="sxs-lookup"><span data-stu-id="15dfd-129">xs:integer</span></span><br/>      |
| <span data-ttu-id="15dfd-130">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="15dfd-130">DefaultValue</span></span><br/> | <span data-ttu-id="15dfd-131">string</span><span class="sxs-lookup"><span data-stu-id="15dfd-131">string</span></span><br/>  | <span data-ttu-id="15dfd-132">não definido</span><span class="sxs-lookup"><span data-stu-id="15dfd-132">undefined</span></span><br/>       |
| <span data-ttu-id="15dfd-133">MaxValue</span><span class="sxs-lookup"><span data-stu-id="15dfd-133">MaxValue</span></span><br/>     | <span data-ttu-id="15dfd-134">Número inteiro</span><span class="sxs-lookup"><span data-stu-id="15dfd-134">integer</span></span><br/> | <span data-ttu-id="15dfd-135">100</span><span class="sxs-lookup"><span data-stu-id="15dfd-135">100</span></span><br/>             |
| <span data-ttu-id="15dfd-136">Minvalue</span><span class="sxs-lookup"><span data-stu-id="15dfd-136">MinValue</span></span><br/>     | <span data-ttu-id="15dfd-137">inteiro</span><span class="sxs-lookup"><span data-stu-id="15dfd-137">integer</span></span><br/> | <span data-ttu-id="15dfd-138">0</span><span class="sxs-lookup"><span data-stu-id="15dfd-138">0</span></span><br/>               |
| <span data-ttu-id="15dfd-139">Vários</span><span class="sxs-lookup"><span data-stu-id="15dfd-139">Multiple</span></span><br/>     | <span data-ttu-id="15dfd-140">integer</span><span class="sxs-lookup"><span data-stu-id="15dfd-140">integer</span></span><br/> | <span data-ttu-id="15dfd-141">1</span><span class="sxs-lookup"><span data-stu-id="15dfd-141">1</span></span><br/>               |
| <span data-ttu-id="15dfd-142">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="15dfd-142">Mandatory</span></span><br/>    | <span data-ttu-id="15dfd-143">string</span><span class="sxs-lookup"><span data-stu-id="15dfd-143">string</span></span><br/>  | <span data-ttu-id="15dfd-144">psk:Conditional</span><span class="sxs-lookup"><span data-stu-id="15dfd-144">psk:Conditional</span></span><br/> |
| <span data-ttu-id="15dfd-145">Unittype</span><span class="sxs-lookup"><span data-stu-id="15dfd-145">UnitType</span></span><br/>     | <span data-ttu-id="15dfd-146">string</span><span class="sxs-lookup"><span data-stu-id="15dfd-146">string</span></span><br/>  | <span data-ttu-id="15dfd-147">{1&gt;percent&lt;1}</span><span class="sxs-lookup"><span data-stu-id="15dfd-147">percent</span></span><br/>         |



 

## <a name="related-topics"></a><span data-ttu-id="15dfd-148">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="15dfd-148">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="15dfd-149">Especificação de esquema de impressão</span><span class="sxs-lookup"><span data-stu-id="15dfd-149">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




