---
description: Este tópico não é atual. Para obter as informações mais atuais, consulte a especificação do esquema de impressão.
ms.assetid: a15fe075-6696-4c70-b658-ae62d542bb4e
title: PageCopies
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 83b1fc822d27d104364c2414ca89cf1fdf30c7d3
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/26/2021
ms.locfileid: "107997663"
---
# <a name="pagecopies"></a><span data-ttu-id="d75fb-104">PageCopies</span><span class="sxs-lookup"><span data-stu-id="d75fb-104">PageCopies</span></span>

<span data-ttu-id="d75fb-105">Este tópico não é atual.</span><span class="sxs-lookup"><span data-stu-id="d75fb-105">This topic is not current.</span></span> <span data-ttu-id="d75fb-106">Para obter as informações mais atuais, consulte a [especificação do esquema de impressão](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="d75fb-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="d75fb-107">Especifica o número de cópias de uma página.</span><span class="sxs-lookup"><span data-stu-id="d75fb-107">Specifies the number of copies of a page.</span></span>

-   [<span data-ttu-id="d75fb-108">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="d75fb-108">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="d75fb-109">Conteúdo da estrutura</span><span class="sxs-lookup"><span data-stu-id="d75fb-109">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="d75fb-110">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="d75fb-110">Element Information</span></span>



| <span data-ttu-id="d75fb-111">Nome</span><span class="sxs-lookup"><span data-stu-id="d75fb-111">Name</span></span> | <span data-ttu-id="d75fb-112">Valor</span><span class="sxs-lookup"><span data-stu-id="d75fb-112">Value</span></span> |
|----------------------------|-------------------------|
| <span data-ttu-id="d75fb-113">Tipo de elemento</span><span class="sxs-lookup"><span data-stu-id="d75fb-113">Element Type</span></span> <br/>   | <span data-ttu-id="d75fb-114">ParameterDef</span><span class="sxs-lookup"><span data-stu-id="d75fb-114">ParameterDef</span></span><br/> |
| <span data-ttu-id="d75fb-115">Prefixo de escopo</span><span class="sxs-lookup"><span data-stu-id="d75fb-115">Scoping Prefix</span></span> <br/> | <span data-ttu-id="d75fb-116">?</span><span class="sxs-lookup"><span data-stu-id="d75fb-116">Page</span></span><br/>         |
| <span data-ttu-id="d75fb-117">Observações</span><span class="sxs-lookup"><span data-stu-id="d75fb-117">Notes</span></span> <br/>          | <span data-ttu-id="d75fb-118">Nenhum</span><span class="sxs-lookup"><span data-stu-id="d75fb-118">None</span></span><br/>         |



 

## <a name="structure-content"></a><span data-ttu-id="d75fb-119">Conteúdo da estrutura</span><span class="sxs-lookup"><span data-stu-id="d75fb-119">Structure Content</span></span>

<span data-ttu-id="d75fb-120">A estrutura XML desse elemento é:</span><span class="sxs-lookup"><span data-stu-id="d75fb-120">The XML structure of this element is:</span></span>

``` syntax
<psf:ParameterDef name="psk:PageCopies">
  <psf:Property name="psf:DataType">
    <psf:Value xsi:type="xs:string">xs:integer</psf:Value>
  </psf:Property>
  <psf:Property name="psf:DefaultValue">
    <psf:Value xsi:type="xs:integer">1</psf:Value>
  </psf:Property>
  <psf:Property name="psf:MaxValue">
    <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
  </psf:Property>
  <psf:Property name="psf:MinValue">
    <psf:Value xsi:type="xs:integer">1</psf:Value>
  </psf:Property>
  <psf:Property name="psf:Multiple">
    <psf:Value xsi:type="xs:integer">1</psf:Value>
  </psf:Property>
  <psf:Property name="psf:Mandatory">
    <psf:Value xsi:type="xs:string">psk:Unconditional</psf:Value>
  </psf:Property>
  <psf:Property name="psf:UnitType">
    <psf:Value xsi:type="xs:string">copies</psf:Value>
  </psf:Property>
</psf:ParameterDef>
      
```

## <a name="structure-properties"></a><span data-ttu-id="d75fb-121">Propriedades da estrutura</span><span class="sxs-lookup"><span data-stu-id="d75fb-121">Structure Properties</span></span>

<span data-ttu-id="d75fb-122">A tabela a seguir descreve as características das variáveis definidas na estrutura XML.</span><span class="sxs-lookup"><span data-stu-id="d75fb-122">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="d75fb-123">Propriedade</span><span class="sxs-lookup"><span data-stu-id="d75fb-123">Property</span></span>                | <span data-ttu-id="d75fb-124">xsi:type</span><span class="sxs-lookup"><span data-stu-id="d75fb-124">xsi:type</span></span>           | <span data-ttu-id="d75fb-125">Valor</span><span class="sxs-lookup"><span data-stu-id="d75fb-125">Value</span></span>                        |
|-------------------------|--------------------|------------------------------|
| <span data-ttu-id="d75fb-126">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="d75fb-126">DataType</span></span><br/>     | <span data-ttu-id="d75fb-127">string</span><span class="sxs-lookup"><span data-stu-id="d75fb-127">string</span></span><br/>  | <span data-ttu-id="d75fb-128">xs:integer</span><span class="sxs-lookup"><span data-stu-id="d75fb-128">xs:integer</span></span><br/>        |
| <span data-ttu-id="d75fb-129">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="d75fb-129">DefaultValue</span></span><br/> | <span data-ttu-id="d75fb-130">integer</span><span class="sxs-lookup"><span data-stu-id="d75fb-130">integer</span></span><br/> | <span data-ttu-id="d75fb-131">1</span><span class="sxs-lookup"><span data-stu-id="d75fb-131">1</span></span><br/>                 |
| <span data-ttu-id="d75fb-132">MaxValue</span><span class="sxs-lookup"><span data-stu-id="d75fb-132">MaxValue</span></span><br/>     | <span data-ttu-id="d75fb-133">Número inteiro</span><span class="sxs-lookup"><span data-stu-id="d75fb-133">integer</span></span><br/> | <span data-ttu-id="d75fb-134">não definido</span><span class="sxs-lookup"><span data-stu-id="d75fb-134">undefined</span></span><br/>         |
| <span data-ttu-id="d75fb-135">MinValue</span><span class="sxs-lookup"><span data-stu-id="d75fb-135">MinValue</span></span><br/>     | <span data-ttu-id="d75fb-136">integer</span><span class="sxs-lookup"><span data-stu-id="d75fb-136">integer</span></span><br/> | <span data-ttu-id="d75fb-137">1</span><span class="sxs-lookup"><span data-stu-id="d75fb-137">1</span></span><br/>                 |
| <span data-ttu-id="d75fb-138">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="d75fb-138">Mandatory</span></span><br/>    | <span data-ttu-id="d75fb-139">string</span><span class="sxs-lookup"><span data-stu-id="d75fb-139">string</span></span><br/>  | <span data-ttu-id="d75fb-140">PSK: incondicional</span><span class="sxs-lookup"><span data-stu-id="d75fb-140">psk:Unconditional</span></span><br/> |
| <span data-ttu-id="d75fb-141">Vários</span><span class="sxs-lookup"><span data-stu-id="d75fb-141">Multiple</span></span><br/>     | <span data-ttu-id="d75fb-142">integer</span><span class="sxs-lookup"><span data-stu-id="d75fb-142">integer</span></span><br/> | <span data-ttu-id="d75fb-143">1</span><span class="sxs-lookup"><span data-stu-id="d75fb-143">1</span></span><br/>                 |
| <span data-ttu-id="d75fb-144">UnitType</span><span class="sxs-lookup"><span data-stu-id="d75fb-144">UnitType</span></span><br/>     | <span data-ttu-id="d75fb-145">string</span><span class="sxs-lookup"><span data-stu-id="d75fb-145">string</span></span><br/>  | <span data-ttu-id="d75fb-146">cópia</span><span class="sxs-lookup"><span data-stu-id="d75fb-146">copies</span></span><br/>            |



 

## <a name="related-topics"></a><span data-ttu-id="d75fb-147">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="d75fb-147">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d75fb-148">Especificação de esquema de impressão</span><span class="sxs-lookup"><span data-stu-id="d75fb-148">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




