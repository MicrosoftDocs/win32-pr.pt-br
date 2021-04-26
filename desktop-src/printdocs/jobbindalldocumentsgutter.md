---
description: Este tópico não é atual. Para obter as informações mais atuais, consulte a especificação do esquema de impressão.
ms.assetid: 97a00cd6-508c-47e9-a1c1-75646ca0c721
title: JobBindAllDocumentsGutter
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 04615b85939d483f6bd2e720afa65a88d44c1caf
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/26/2021
ms.locfileid: "107998373"
---
# <a name="jobbindalldocumentsgutter"></a><span data-ttu-id="44cd6-104">JobBindAllDocumentsGutter</span><span class="sxs-lookup"><span data-stu-id="44cd6-104">JobBindAllDocumentsGutter</span></span>

<span data-ttu-id="44cd6-105">Este tópico não é atual.</span><span class="sxs-lookup"><span data-stu-id="44cd6-105">This topic is not current.</span></span> <span data-ttu-id="44cd6-106">Para obter as informações mais atuais, consulte a [especificação do esquema de impressão](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="44cd6-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="44cd6-107">Especifica a largura da medianiz de associação.</span><span class="sxs-lookup"><span data-stu-id="44cd6-107">Specifies the width of the binding gutter.</span></span>

-   [<span data-ttu-id="44cd6-108">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="44cd6-108">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="44cd6-109">Conteúdo da estrutura</span><span class="sxs-lookup"><span data-stu-id="44cd6-109">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="44cd6-110">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="44cd6-110">Element Information</span></span>



| <span data-ttu-id="44cd6-111">Nome</span><span class="sxs-lookup"><span data-stu-id="44cd6-111">Name</span></span> | <span data-ttu-id="44cd6-112">Valor</span><span class="sxs-lookup"><span data-stu-id="44cd6-112">Value</span></span> |
|----------------------------|-----------------------------------------|
| <span data-ttu-id="44cd6-113">Tipo de elemento</span><span class="sxs-lookup"><span data-stu-id="44cd6-113">Element Type</span></span> <br/>   | <span data-ttu-id="44cd6-114">ParameterDef</span><span class="sxs-lookup"><span data-stu-id="44cd6-114">ParameterDef</span></span><br/>                 |
| <span data-ttu-id="44cd6-115">Prefixo de escopo</span><span class="sxs-lookup"><span data-stu-id="44cd6-115">Scoping Prefix</span></span> <br/> | <span data-ttu-id="44cd6-116">Trabalho</span><span class="sxs-lookup"><span data-stu-id="44cd6-116">Job</span></span> <br/>                         |
| <span data-ttu-id="44cd6-117">Observações</span><span class="sxs-lookup"><span data-stu-id="44cd6-117">Notes</span></span> <br/>          | <span data-ttu-id="44cd6-118">Vinculado ao elemento JobBinding</span><span class="sxs-lookup"><span data-stu-id="44cd6-118">Linked to JobBinding element</span></span><br/> |



 

## <a name="structure-content"></a><span data-ttu-id="44cd6-119">Conteúdo da estrutura</span><span class="sxs-lookup"><span data-stu-id="44cd6-119">Structure Content</span></span>

<span data-ttu-id="44cd6-120">A estrutura XML desse elemento é:</span><span class="sxs-lookup"><span data-stu-id="44cd6-120">The XML structure of this element is:</span></span>

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

## <a name="structure-properties"></a><span data-ttu-id="44cd6-121">Propriedades da estrutura</span><span class="sxs-lookup"><span data-stu-id="44cd6-121">Structure Properties</span></span>

<span data-ttu-id="44cd6-122">A tabela a seguir descreve as características das variáveis definidas na estrutura XML.</span><span class="sxs-lookup"><span data-stu-id="44cd6-122">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="44cd6-123">Propriedade</span><span class="sxs-lookup"><span data-stu-id="44cd6-123">Property</span></span>                | <span data-ttu-id="44cd6-124">xsi:type</span><span class="sxs-lookup"><span data-stu-id="44cd6-124">xsi:type</span></span>           | <span data-ttu-id="44cd6-125">Valor</span><span class="sxs-lookup"><span data-stu-id="44cd6-125">Value</span></span>                      |
|-------------------------|--------------------|----------------------------|
| <span data-ttu-id="44cd6-126">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="44cd6-126">DataType</span></span><br/>     | <span data-ttu-id="44cd6-127">string</span><span class="sxs-lookup"><span data-stu-id="44cd6-127">string</span></span><br/>  | <span data-ttu-id="44cd6-128">xs:integer</span><span class="sxs-lookup"><span data-stu-id="44cd6-128">xs:integer</span></span><br/>      |
| <span data-ttu-id="44cd6-129">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="44cd6-129">DefaultValue</span></span><br/> | <span data-ttu-id="44cd6-130">Número inteiro</span><span class="sxs-lookup"><span data-stu-id="44cd6-130">integer</span></span><br/> | <span data-ttu-id="44cd6-131">não definido</span><span class="sxs-lookup"><span data-stu-id="44cd6-131">undefined</span></span><br/>       |
| <span data-ttu-id="44cd6-132">MaxValue</span><span class="sxs-lookup"><span data-stu-id="44cd6-132">MaxValue</span></span><br/>     | <span data-ttu-id="44cd6-133">Número inteiro</span><span class="sxs-lookup"><span data-stu-id="44cd6-133">integer</span></span><br/> | <span data-ttu-id="44cd6-134">não definido</span><span class="sxs-lookup"><span data-stu-id="44cd6-134">undefined</span></span><br/>       |
| <span data-ttu-id="44cd6-135">MinValue</span><span class="sxs-lookup"><span data-stu-id="44cd6-135">MinValue</span></span><br/>     | <span data-ttu-id="44cd6-136">Número inteiro</span><span class="sxs-lookup"><span data-stu-id="44cd6-136">integer</span></span><br/> | <span data-ttu-id="44cd6-137">não definido</span><span class="sxs-lookup"><span data-stu-id="44cd6-137">undefined</span></span><br/>       |
| <span data-ttu-id="44cd6-138">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="44cd6-138">Mandatory</span></span><br/>    | <span data-ttu-id="44cd6-139">String</span><span class="sxs-lookup"><span data-stu-id="44cd6-139">String</span></span><br/>  | <span data-ttu-id="44cd6-140">PSK: condicional</span><span class="sxs-lookup"><span data-stu-id="44cd6-140">psk:Conditional</span></span><br/> |
| <span data-ttu-id="44cd6-141">Vários</span><span class="sxs-lookup"><span data-stu-id="44cd6-141">Multiple</span></span><br/>     | <span data-ttu-id="44cd6-142">integer</span><span class="sxs-lookup"><span data-stu-id="44cd6-142">integer</span></span><br/> | <span data-ttu-id="44cd6-143">1</span><span class="sxs-lookup"><span data-stu-id="44cd6-143">1</span></span><br/>               |
| <span data-ttu-id="44cd6-144">UnitType</span><span class="sxs-lookup"><span data-stu-id="44cd6-144">UnitType</span></span><br/>     | <span data-ttu-id="44cd6-145">string</span><span class="sxs-lookup"><span data-stu-id="44cd6-145">string</span></span><br/>  | <span data-ttu-id="44cd6-146">mícrons</span><span class="sxs-lookup"><span data-stu-id="44cd6-146">microns</span></span><br/>         |



 

## <a name="related-topics"></a><span data-ttu-id="44cd6-147">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="44cd6-147">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="44cd6-148">Especificação de esquema de impressão</span><span class="sxs-lookup"><span data-stu-id="44cd6-148">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




