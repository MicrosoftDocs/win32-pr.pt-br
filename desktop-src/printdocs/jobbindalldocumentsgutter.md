---
description: Este tópico não é atual. Para obter as informações mais atuais, consulte a especificação do esquema de impressão.
ms.assetid: 97a00cd6-508c-47e9-a1c1-75646ca0c721
title: JobBindAllDocumentsGutter
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 219a86f016edf820532c20fa473876265776a4ee
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/05/2021
ms.locfileid: "104172570"
---
# <a name="jobbindalldocumentsgutter"></a><span data-ttu-id="30f86-104">JobBindAllDocumentsGutter</span><span class="sxs-lookup"><span data-stu-id="30f86-104">JobBindAllDocumentsGutter</span></span>

<span data-ttu-id="30f86-105">Este tópico não é atual.</span><span class="sxs-lookup"><span data-stu-id="30f86-105">This topic is not current.</span></span> <span data-ttu-id="30f86-106">Para obter as informações mais atuais, consulte a [especificação do esquema de impressão](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="30f86-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="30f86-107">Especifica a largura da medianiz de associação.</span><span class="sxs-lookup"><span data-stu-id="30f86-107">Specifies the width of the binding gutter.</span></span>

-   [<span data-ttu-id="30f86-108">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="30f86-108">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="30f86-109">Conteúdo da estrutura</span><span class="sxs-lookup"><span data-stu-id="30f86-109">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="30f86-110">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="30f86-110">Element Information</span></span>



| <span data-ttu-id="30f86-111">Name</span><span class="sxs-lookup"><span data-stu-id="30f86-111">Name</span></span>                       |                                         |
|----------------------------|-----------------------------------------|
| <span data-ttu-id="30f86-112">Tipo de elemento</span><span class="sxs-lookup"><span data-stu-id="30f86-112">Element Type</span></span> <br/>   | <span data-ttu-id="30f86-113">ParameterDef</span><span class="sxs-lookup"><span data-stu-id="30f86-113">ParameterDef</span></span><br/>                 |
| <span data-ttu-id="30f86-114">Prefixo de escopo</span><span class="sxs-lookup"><span data-stu-id="30f86-114">Scoping Prefix</span></span> <br/> | <span data-ttu-id="30f86-115">Trabalho</span><span class="sxs-lookup"><span data-stu-id="30f86-115">Job</span></span> <br/>                         |
| <span data-ttu-id="30f86-116">Observações</span><span class="sxs-lookup"><span data-stu-id="30f86-116">Notes</span></span> <br/>          | <span data-ttu-id="30f86-117">Vinculado ao elemento JobBinding</span><span class="sxs-lookup"><span data-stu-id="30f86-117">Linked to JobBinding element</span></span><br/> |



 

## <a name="structure-content"></a><span data-ttu-id="30f86-118">Conteúdo da estrutura</span><span class="sxs-lookup"><span data-stu-id="30f86-118">Structure Content</span></span>

<span data-ttu-id="30f86-119">A estrutura XML desse elemento é:</span><span class="sxs-lookup"><span data-stu-id="30f86-119">The XML structure of this element is:</span></span>

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

## <a name="structure-properties"></a><span data-ttu-id="30f86-120">Propriedades da estrutura</span><span class="sxs-lookup"><span data-stu-id="30f86-120">Structure Properties</span></span>

<span data-ttu-id="30f86-121">A tabela a seguir descreve as características das variáveis definidas na estrutura XML.</span><span class="sxs-lookup"><span data-stu-id="30f86-121">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="30f86-122">Propriedade</span><span class="sxs-lookup"><span data-stu-id="30f86-122">Property</span></span>                | <span data-ttu-id="30f86-123">xsi:type</span><span class="sxs-lookup"><span data-stu-id="30f86-123">xsi:type</span></span>           | <span data-ttu-id="30f86-124">Valor</span><span class="sxs-lookup"><span data-stu-id="30f86-124">Value</span></span>                      |
|-------------------------|--------------------|----------------------------|
| <span data-ttu-id="30f86-125">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="30f86-125">DataType</span></span><br/>     | <span data-ttu-id="30f86-126">string</span><span class="sxs-lookup"><span data-stu-id="30f86-126">string</span></span><br/>  | <span data-ttu-id="30f86-127">xs:integer</span><span class="sxs-lookup"><span data-stu-id="30f86-127">xs:integer</span></span><br/>      |
| <span data-ttu-id="30f86-128">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="30f86-128">DefaultValue</span></span><br/> | <span data-ttu-id="30f86-129">Número inteiro</span><span class="sxs-lookup"><span data-stu-id="30f86-129">integer</span></span><br/> | <span data-ttu-id="30f86-130">não definido</span><span class="sxs-lookup"><span data-stu-id="30f86-130">undefined</span></span><br/>       |
| <span data-ttu-id="30f86-131">MaxValue</span><span class="sxs-lookup"><span data-stu-id="30f86-131">MaxValue</span></span><br/>     | <span data-ttu-id="30f86-132">Número inteiro</span><span class="sxs-lookup"><span data-stu-id="30f86-132">integer</span></span><br/> | <span data-ttu-id="30f86-133">não definido</span><span class="sxs-lookup"><span data-stu-id="30f86-133">undefined</span></span><br/>       |
| <span data-ttu-id="30f86-134">MinValue</span><span class="sxs-lookup"><span data-stu-id="30f86-134">MinValue</span></span><br/>     | <span data-ttu-id="30f86-135">Número inteiro</span><span class="sxs-lookup"><span data-stu-id="30f86-135">integer</span></span><br/> | <span data-ttu-id="30f86-136">não definido</span><span class="sxs-lookup"><span data-stu-id="30f86-136">undefined</span></span><br/>       |
| <span data-ttu-id="30f86-137">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="30f86-137">Mandatory</span></span><br/>    | <span data-ttu-id="30f86-138">String</span><span class="sxs-lookup"><span data-stu-id="30f86-138">String</span></span><br/>  | <span data-ttu-id="30f86-139">PSK: condicional</span><span class="sxs-lookup"><span data-stu-id="30f86-139">psk:Conditional</span></span><br/> |
| <span data-ttu-id="30f86-140">Vários</span><span class="sxs-lookup"><span data-stu-id="30f86-140">Multiple</span></span><br/>     | <span data-ttu-id="30f86-141">integer</span><span class="sxs-lookup"><span data-stu-id="30f86-141">integer</span></span><br/> | <span data-ttu-id="30f86-142">1</span><span class="sxs-lookup"><span data-stu-id="30f86-142">1</span></span><br/>               |
| <span data-ttu-id="30f86-143">UnitType</span><span class="sxs-lookup"><span data-stu-id="30f86-143">UnitType</span></span><br/>     | <span data-ttu-id="30f86-144">string</span><span class="sxs-lookup"><span data-stu-id="30f86-144">string</span></span><br/>  | <span data-ttu-id="30f86-145">mícrons</span><span class="sxs-lookup"><span data-stu-id="30f86-145">microns</span></span><br/>         |



 

## <a name="related-topics"></a><span data-ttu-id="30f86-146">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="30f86-146">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="30f86-147">Especificação de esquema de impressão</span><span class="sxs-lookup"><span data-stu-id="30f86-147">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




