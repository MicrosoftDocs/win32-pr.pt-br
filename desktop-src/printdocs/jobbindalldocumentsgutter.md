---
description: Saiba mais sobre o elemento JobBindAllDocumentsGutter, que especifica a largura da medianiz de associação.
ms.assetid: 97a00cd6-508c-47e9-a1c1-75646ca0c721
title: JobBindAllDocumentsGutter
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a42180ff9a00d1502d844b270fe5da7324825ca3
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/19/2021
ms.locfileid: "112409069"
---
# <a name="jobbindalldocumentsgutter"></a><span data-ttu-id="edcaf-103">JobBindAllDocumentsGutter</span><span class="sxs-lookup"><span data-stu-id="edcaf-103">JobBindAllDocumentsGutter</span></span>

<span data-ttu-id="edcaf-104">Este tópico não é atual.</span><span class="sxs-lookup"><span data-stu-id="edcaf-104">This topic is not current.</span></span> <span data-ttu-id="edcaf-105">Para obter as informações mais atuais, consulte a [Especificação de Esquema de Impressão](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="edcaf-105">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="edcaf-106">Especifica a largura da medianiz de associação.</span><span class="sxs-lookup"><span data-stu-id="edcaf-106">Specifies the width of the binding gutter.</span></span>

-   [<span data-ttu-id="edcaf-107">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="edcaf-107">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="edcaf-108">Conteúdo da estrutura</span><span class="sxs-lookup"><span data-stu-id="edcaf-108">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="edcaf-109">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="edcaf-109">Element Information</span></span>



| <span data-ttu-id="edcaf-110">Name</span><span class="sxs-lookup"><span data-stu-id="edcaf-110">Name</span></span> | <span data-ttu-id="edcaf-111">Valor</span><span class="sxs-lookup"><span data-stu-id="edcaf-111">Value</span></span> |
|----------------------------|-----------------------------------------|
| <span data-ttu-id="edcaf-112">Tipo de elemento</span><span class="sxs-lookup"><span data-stu-id="edcaf-112">Element Type</span></span> <br/>   | <span data-ttu-id="edcaf-113">ParameterDef</span><span class="sxs-lookup"><span data-stu-id="edcaf-113">ParameterDef</span></span><br/>                 |
| <span data-ttu-id="edcaf-114">Prefixo de definição de scoping</span><span class="sxs-lookup"><span data-stu-id="edcaf-114">Scoping Prefix</span></span> <br/> | <span data-ttu-id="edcaf-115">Trabalho</span><span class="sxs-lookup"><span data-stu-id="edcaf-115">Job</span></span> <br/>                         |
| <span data-ttu-id="edcaf-116">Observações</span><span class="sxs-lookup"><span data-stu-id="edcaf-116">Notes</span></span> <br/>          | <span data-ttu-id="edcaf-117">Vinculado ao elemento JobBinding</span><span class="sxs-lookup"><span data-stu-id="edcaf-117">Linked to JobBinding element</span></span><br/> |



 

## <a name="structure-content"></a><span data-ttu-id="edcaf-118">Conteúdo da estrutura</span><span class="sxs-lookup"><span data-stu-id="edcaf-118">Structure Content</span></span>

<span data-ttu-id="edcaf-119">A estrutura XML desse elemento é:</span><span class="sxs-lookup"><span data-stu-id="edcaf-119">The XML structure of this element is:</span></span>

``` syntax
<psf:ParameterDef name="psk:JobBindAllDocumentsGutter">
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

## <a name="structure-properties"></a><span data-ttu-id="edcaf-120">Propriedades da estrutura</span><span class="sxs-lookup"><span data-stu-id="edcaf-120">Structure Properties</span></span>

<span data-ttu-id="edcaf-121">A tabela a seguir descreve as características das variáveis definidas na estrutura XML.</span><span class="sxs-lookup"><span data-stu-id="edcaf-121">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="edcaf-122">Propriedade</span><span class="sxs-lookup"><span data-stu-id="edcaf-122">Property</span></span>                | <span data-ttu-id="edcaf-123">xsi:type</span><span class="sxs-lookup"><span data-stu-id="edcaf-123">xsi:type</span></span>           | <span data-ttu-id="edcaf-124">Valor</span><span class="sxs-lookup"><span data-stu-id="edcaf-124">Value</span></span>                      |
|-------------------------|--------------------|----------------------------|
| <span data-ttu-id="edcaf-125">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="edcaf-125">DataType</span></span><br/>     | <span data-ttu-id="edcaf-126">string</span><span class="sxs-lookup"><span data-stu-id="edcaf-126">string</span></span><br/>  | <span data-ttu-id="edcaf-127">xs:integer</span><span class="sxs-lookup"><span data-stu-id="edcaf-127">xs:integer</span></span><br/>      |
| <span data-ttu-id="edcaf-128">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="edcaf-128">DefaultValue</span></span><br/> | <span data-ttu-id="edcaf-129">Número inteiro</span><span class="sxs-lookup"><span data-stu-id="edcaf-129">integer</span></span><br/> | <span data-ttu-id="edcaf-130">não definido</span><span class="sxs-lookup"><span data-stu-id="edcaf-130">undefined</span></span><br/>       |
| <span data-ttu-id="edcaf-131">MaxValue</span><span class="sxs-lookup"><span data-stu-id="edcaf-131">MaxValue</span></span><br/>     | <span data-ttu-id="edcaf-132">Número inteiro</span><span class="sxs-lookup"><span data-stu-id="edcaf-132">integer</span></span><br/> | <span data-ttu-id="edcaf-133">não definido</span><span class="sxs-lookup"><span data-stu-id="edcaf-133">undefined</span></span><br/>       |
| <span data-ttu-id="edcaf-134">Minvalue</span><span class="sxs-lookup"><span data-stu-id="edcaf-134">MinValue</span></span><br/>     | <span data-ttu-id="edcaf-135">Número inteiro</span><span class="sxs-lookup"><span data-stu-id="edcaf-135">integer</span></span><br/> | <span data-ttu-id="edcaf-136">não definido</span><span class="sxs-lookup"><span data-stu-id="edcaf-136">undefined</span></span><br/>       |
| <span data-ttu-id="edcaf-137">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="edcaf-137">Mandatory</span></span><br/>    | <span data-ttu-id="edcaf-138">String</span><span class="sxs-lookup"><span data-stu-id="edcaf-138">String</span></span><br/>  | <span data-ttu-id="edcaf-139">psk:Conditional</span><span class="sxs-lookup"><span data-stu-id="edcaf-139">psk:Conditional</span></span><br/> |
| <span data-ttu-id="edcaf-140">Vários</span><span class="sxs-lookup"><span data-stu-id="edcaf-140">Multiple</span></span><br/>     | <span data-ttu-id="edcaf-141">integer</span><span class="sxs-lookup"><span data-stu-id="edcaf-141">integer</span></span><br/> | <span data-ttu-id="edcaf-142">1</span><span class="sxs-lookup"><span data-stu-id="edcaf-142">1</span></span><br/>               |
| <span data-ttu-id="edcaf-143">Unittype</span><span class="sxs-lookup"><span data-stu-id="edcaf-143">UnitType</span></span><br/>     | <span data-ttu-id="edcaf-144">string</span><span class="sxs-lookup"><span data-stu-id="edcaf-144">string</span></span><br/>  | <span data-ttu-id="edcaf-145">Mícrons</span><span class="sxs-lookup"><span data-stu-id="edcaf-145">microns</span></span><br/>         |



 

## <a name="related-topics"></a><span data-ttu-id="edcaf-146">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="edcaf-146">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="edcaf-147">Especificação de esquema de impressão</span><span class="sxs-lookup"><span data-stu-id="edcaf-147">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




