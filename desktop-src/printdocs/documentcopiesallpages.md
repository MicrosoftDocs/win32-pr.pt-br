---
description: Saiba como o elemento DocumentCopiesAllPages, que especifica o número de cópias de um documento.
ms.assetid: 6319e8fc-787f-4bc8-8436-1b498b3882d2
title: DocumentCopiesAllPages
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 05bf82c23b764f3fe1f8257f4cdb2e7fa03374bd
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/19/2021
ms.locfileid: "112409439"
---
# <a name="documentcopiesallpages"></a><span data-ttu-id="7624b-103">DocumentCopiesAllPages</span><span class="sxs-lookup"><span data-stu-id="7624b-103">DocumentCopiesAllPages</span></span>

<span data-ttu-id="7624b-104">Este tópico não é atual.</span><span class="sxs-lookup"><span data-stu-id="7624b-104">This topic is not current.</span></span> <span data-ttu-id="7624b-105">Para obter as informações mais atuais, consulte a [especificação do esquema de impressão](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="7624b-105">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="7624b-106">Especifica o número de cópias de um documento.</span><span class="sxs-lookup"><span data-stu-id="7624b-106">Specifies the number of copies of a document.</span></span>

-   [<span data-ttu-id="7624b-107">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="7624b-107">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="7624b-108">Conteúdo da estrutura</span><span class="sxs-lookup"><span data-stu-id="7624b-108">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="7624b-109">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="7624b-109">Element Information</span></span>



| <span data-ttu-id="7624b-110">Name</span><span class="sxs-lookup"><span data-stu-id="7624b-110">Name</span></span> | <span data-ttu-id="7624b-111">Valor</span><span class="sxs-lookup"><span data-stu-id="7624b-111">Value</span></span> |
|----------------------------|-------------------------|
| <span data-ttu-id="7624b-112">Tipo de elemento</span><span class="sxs-lookup"><span data-stu-id="7624b-112">Element Type</span></span> <br/>   | <span data-ttu-id="7624b-113">ParameterDef</span><span class="sxs-lookup"><span data-stu-id="7624b-113">ParameterDef</span></span><br/> |
| <span data-ttu-id="7624b-114">Prefixo de escopo</span><span class="sxs-lookup"><span data-stu-id="7624b-114">Scoping Prefix</span></span> <br/> | <span data-ttu-id="7624b-115">Documento</span><span class="sxs-lookup"><span data-stu-id="7624b-115">Document</span></span><br/>     |
| <span data-ttu-id="7624b-116">Observações</span><span class="sxs-lookup"><span data-stu-id="7624b-116">Notes</span></span> <br/>          | <span data-ttu-id="7624b-117">Nenhum</span><span class="sxs-lookup"><span data-stu-id="7624b-117">None</span></span><br/>         |



 

## <a name="structure-content"></a><span data-ttu-id="7624b-118">Conteúdo da estrutura</span><span class="sxs-lookup"><span data-stu-id="7624b-118">Structure Content</span></span>

<span data-ttu-id="7624b-119">A estrutura XML desse elemento é:</span><span class="sxs-lookup"><span data-stu-id="7624b-119">The XML structure of this element is:</span></span>

``` syntax
<psf:ParameterDef name="psk:DocumentCopiesAllPages">
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

## <a name="structure-properties"></a><span data-ttu-id="7624b-120">Propriedades da estrutura</span><span class="sxs-lookup"><span data-stu-id="7624b-120">Structure Properties</span></span>

<span data-ttu-id="7624b-121">A tabela a seguir descreve as características das variáveis definidas na estrutura XML.</span><span class="sxs-lookup"><span data-stu-id="7624b-121">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="7624b-122">Propriedade</span><span class="sxs-lookup"><span data-stu-id="7624b-122">Property</span></span>                | <span data-ttu-id="7624b-123">xsi:type</span><span class="sxs-lookup"><span data-stu-id="7624b-123">xsi:type</span></span>           | <span data-ttu-id="7624b-124">Valor</span><span class="sxs-lookup"><span data-stu-id="7624b-124">Value</span></span>                        |
|-------------------------|--------------------|------------------------------|
| <span data-ttu-id="7624b-125">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="7624b-125">DataType</span></span><br/>     | <span data-ttu-id="7624b-126">string</span><span class="sxs-lookup"><span data-stu-id="7624b-126">string</span></span><br/>  | <span data-ttu-id="7624b-127">xs:integer</span><span class="sxs-lookup"><span data-stu-id="7624b-127">xs:integer</span></span><br/>        |
| <span data-ttu-id="7624b-128">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="7624b-128">DefaultValue</span></span><br/> | <span data-ttu-id="7624b-129">integer</span><span class="sxs-lookup"><span data-stu-id="7624b-129">integer</span></span><br/> | <span data-ttu-id="7624b-130">1</span><span class="sxs-lookup"><span data-stu-id="7624b-130">1</span></span><br/>                 |
| <span data-ttu-id="7624b-131">MaxValue</span><span class="sxs-lookup"><span data-stu-id="7624b-131">MaxValue</span></span><br/>     | <span data-ttu-id="7624b-132">Número inteiro</span><span class="sxs-lookup"><span data-stu-id="7624b-132">integer</span></span><br/> | <span data-ttu-id="7624b-133">não definido</span><span class="sxs-lookup"><span data-stu-id="7624b-133">undefined</span></span><br/>         |
| <span data-ttu-id="7624b-134">MinValue</span><span class="sxs-lookup"><span data-stu-id="7624b-134">MinValue</span></span><br/>     | <span data-ttu-id="7624b-135">integer</span><span class="sxs-lookup"><span data-stu-id="7624b-135">integer</span></span><br/> | <span data-ttu-id="7624b-136">1</span><span class="sxs-lookup"><span data-stu-id="7624b-136">1</span></span><br/>                 |
| <span data-ttu-id="7624b-137">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="7624b-137">Mandatory</span></span><br/>    | <span data-ttu-id="7624b-138">string</span><span class="sxs-lookup"><span data-stu-id="7624b-138">string</span></span><br/>  | <span data-ttu-id="7624b-139">PSK: incondicional</span><span class="sxs-lookup"><span data-stu-id="7624b-139">psk:Unconditional</span></span><br/> |
| <span data-ttu-id="7624b-140">Vários</span><span class="sxs-lookup"><span data-stu-id="7624b-140">Multiple</span></span><br/>     | <span data-ttu-id="7624b-141">integer</span><span class="sxs-lookup"><span data-stu-id="7624b-141">integer</span></span><br/> | <span data-ttu-id="7624b-142">1</span><span class="sxs-lookup"><span data-stu-id="7624b-142">1</span></span><br/>                 |
| <span data-ttu-id="7624b-143">UnitType</span><span class="sxs-lookup"><span data-stu-id="7624b-143">UnitType</span></span><br/>     | <span data-ttu-id="7624b-144">string</span><span class="sxs-lookup"><span data-stu-id="7624b-144">string</span></span><br/>  | <span data-ttu-id="7624b-145">cópia</span><span class="sxs-lookup"><span data-stu-id="7624b-145">copies</span></span><br/>            |



 

## <a name="related-topics"></a><span data-ttu-id="7624b-146">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="7624b-146">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7624b-147">Especificação de esquema de impressão</span><span class="sxs-lookup"><span data-stu-id="7624b-147">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




