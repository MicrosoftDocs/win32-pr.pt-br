---
description: Obtenha informações sobre o parâmetro PageMediaSizeMediaSizeHeight. Este tópico não é atual. Para obter as informações mais atuais, consulte a especificação do esquema de impressão.
ms.assetid: 209b3024-60cf-47e0-8738-cd7795e38c2a
title: PageMediaSizeMediaSizeHeight
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 547077e7a63d91d6db43e8ebf6225a771bf237d8
ms.sourcegitcommit: 91530c19d26ba4c57a6af1f37b57f211f580464e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/19/2021
ms.locfileid: "112395791"
---
# <a name="pagemediasizemediasizeheight"></a><span data-ttu-id="2d9c5-105">PageMediaSizeMediaSizeHeight</span><span class="sxs-lookup"><span data-stu-id="2d9c5-105">PageMediaSizeMediaSizeHeight</span></span>

<span data-ttu-id="2d9c5-106">Este tópico não é atual.</span><span class="sxs-lookup"><span data-stu-id="2d9c5-106">This topic is not current.</span></span> <span data-ttu-id="2d9c5-107">Para obter as informações mais atuais, consulte a [especificação do esquema de impressão](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="2d9c5-107">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="2d9c5-108">Especifica a direção da dimensão MediaSizeHeight para a opção MediaSize personalizada.</span><span class="sxs-lookup"><span data-stu-id="2d9c5-108">Specifies the dimension MediaSizeHeight direction for the Custom MediaSize option.</span></span>

-   [<span data-ttu-id="2d9c5-109">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="2d9c5-109">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="2d9c5-110">Conteúdo da estrutura</span><span class="sxs-lookup"><span data-stu-id="2d9c5-110">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="2d9c5-111">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="2d9c5-111">Element Information</span></span>



| <span data-ttu-id="2d9c5-112">Name</span><span class="sxs-lookup"><span data-stu-id="2d9c5-112">Name</span></span> | <span data-ttu-id="2d9c5-113">Valor</span><span class="sxs-lookup"><span data-stu-id="2d9c5-113">Value</span></span> |
|----------------------------|-----------------------------------------------------------|
| <span data-ttu-id="2d9c5-114">Tipo de elemento</span><span class="sxs-lookup"><span data-stu-id="2d9c5-114">Element Type</span></span> <br/>   | <span data-ttu-id="2d9c5-115">ParameterDef</span><span class="sxs-lookup"><span data-stu-id="2d9c5-115">ParameterDef</span></span><br/>                                   |
| <span data-ttu-id="2d9c5-116">Prefixo de escopo</span><span class="sxs-lookup"><span data-stu-id="2d9c5-116">Scoping Prefix</span></span> <br/> | <span data-ttu-id="2d9c5-117">?</span><span class="sxs-lookup"><span data-stu-id="2d9c5-117">Page</span></span><br/>                                           |
| <span data-ttu-id="2d9c5-118">Observações</span><span class="sxs-lookup"><span data-stu-id="2d9c5-118">Notes</span></span> <br/>          | <span data-ttu-id="2d9c5-119">Vinculado ao elemento PageMediaSize, opção personalizada</span><span class="sxs-lookup"><span data-stu-id="2d9c5-119">Linked to PageMediaSize element, Custom option</span></span><br/> |



 

## <a name="structure-content"></a><span data-ttu-id="2d9c5-120">Conteúdo da estrutura</span><span class="sxs-lookup"><span data-stu-id="2d9c5-120">Structure Content</span></span>

<span data-ttu-id="2d9c5-121">A estrutura XML desse elemento é:</span><span class="sxs-lookup"><span data-stu-id="2d9c5-121">The XML structure of this element is:</span></span>

``` syntax
<psf:ParameterDef name="psk:PageMediaSizeMediaSizeHeight">
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
    <psf:Value xsi:type="xs:integer">1</psf:Value>
  </psf:Property>
  <psf:Property name="psf:Mandatory">
    <psf:Value xsi:type="xs:string">psk:Conditional</psf:Value>
  </psf:Property>
  <psf:Property name="psf:UnitType">
    <psf:Value xsi:type="xs:string">microns</psf:Value>
  </psf:Property>
</psf:ParameterDef>
      
```

## <a name="structure-properties"></a><span data-ttu-id="2d9c5-122">Propriedades da estrutura</span><span class="sxs-lookup"><span data-stu-id="2d9c5-122">Structure Properties</span></span>

<span data-ttu-id="2d9c5-123">A tabela a seguir descreve as características das variáveis definidas na estrutura XML.</span><span class="sxs-lookup"><span data-stu-id="2d9c5-123">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="2d9c5-124">Propriedade</span><span class="sxs-lookup"><span data-stu-id="2d9c5-124">Property</span></span>                | <span data-ttu-id="2d9c5-125">xsi:type</span><span class="sxs-lookup"><span data-stu-id="2d9c5-125">xsi:type</span></span>           | <span data-ttu-id="2d9c5-126">Valor</span><span class="sxs-lookup"><span data-stu-id="2d9c5-126">Value</span></span>                      |
|-------------------------|--------------------|----------------------------|
| <span data-ttu-id="2d9c5-127">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="2d9c5-127">DataType</span></span><br/>     | <span data-ttu-id="2d9c5-128">string</span><span class="sxs-lookup"><span data-stu-id="2d9c5-128">string</span></span><br/>  | <span data-ttu-id="2d9c5-129">xs:integer</span><span class="sxs-lookup"><span data-stu-id="2d9c5-129">xs:integer</span></span><br/>      |
| <span data-ttu-id="2d9c5-130">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="2d9c5-130">DefaultValue</span></span><br/> | <span data-ttu-id="2d9c5-131">Número inteiro</span><span class="sxs-lookup"><span data-stu-id="2d9c5-131">integer</span></span><br/> | <span data-ttu-id="2d9c5-132">não definido</span><span class="sxs-lookup"><span data-stu-id="2d9c5-132">undefined</span></span><br/>       |
| <span data-ttu-id="2d9c5-133">MaxValue</span><span class="sxs-lookup"><span data-stu-id="2d9c5-133">MaxValue</span></span><br/>     | <span data-ttu-id="2d9c5-134">Número inteiro</span><span class="sxs-lookup"><span data-stu-id="2d9c5-134">integer</span></span><br/> | <span data-ttu-id="2d9c5-135">não definido</span><span class="sxs-lookup"><span data-stu-id="2d9c5-135">undefined</span></span><br/>       |
| <span data-ttu-id="2d9c5-136">MinValue</span><span class="sxs-lookup"><span data-stu-id="2d9c5-136">MinValue</span></span><br/>     | <span data-ttu-id="2d9c5-137">Número inteiro</span><span class="sxs-lookup"><span data-stu-id="2d9c5-137">integer</span></span><br/> | <span data-ttu-id="2d9c5-138">não definido</span><span class="sxs-lookup"><span data-stu-id="2d9c5-138">undefined</span></span><br/>       |
| <span data-ttu-id="2d9c5-139">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="2d9c5-139">Mandatory</span></span><br/>    | <span data-ttu-id="2d9c5-140">string</span><span class="sxs-lookup"><span data-stu-id="2d9c5-140">string</span></span><br/>  | <span data-ttu-id="2d9c5-141">PSK: condicional</span><span class="sxs-lookup"><span data-stu-id="2d9c5-141">psk:Conditional</span></span><br/> |
| <span data-ttu-id="2d9c5-142">Vários</span><span class="sxs-lookup"><span data-stu-id="2d9c5-142">Multiple</span></span><br/>     | <span data-ttu-id="2d9c5-143">integer</span><span class="sxs-lookup"><span data-stu-id="2d9c5-143">integer</span></span><br/> | <span data-ttu-id="2d9c5-144">1</span><span class="sxs-lookup"><span data-stu-id="2d9c5-144">1</span></span><br/>               |
| <span data-ttu-id="2d9c5-145">UnitType</span><span class="sxs-lookup"><span data-stu-id="2d9c5-145">UnitType</span></span><br/>     | <span data-ttu-id="2d9c5-146">string</span><span class="sxs-lookup"><span data-stu-id="2d9c5-146">string</span></span><br/>  | <span data-ttu-id="2d9c5-147">mícrons</span><span class="sxs-lookup"><span data-stu-id="2d9c5-147">microns</span></span><br/>         |



 

## <a name="related-topics"></a><span data-ttu-id="2d9c5-148">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="2d9c5-148">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2d9c5-149">Especificação de esquema de impressão</span><span class="sxs-lookup"><span data-stu-id="2d9c5-149">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




