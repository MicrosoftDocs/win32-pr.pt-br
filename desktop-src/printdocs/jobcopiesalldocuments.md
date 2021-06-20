---
description: Saiba mais sobre o elemento JobCopiesAllDocuments, que especifica o número de cópias de um trabalho.
ms.assetid: 584a71cd-fc32-485e-a627-27be95c377a9
title: JobCopiesAllDocuments
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 05166715a5985c5ddee33fa6808d0fb6b150774b
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/19/2021
ms.locfileid: "112409029"
---
# <a name="jobcopiesalldocuments"></a><span data-ttu-id="40b72-103">JobCopiesAllDocuments</span><span class="sxs-lookup"><span data-stu-id="40b72-103">JobCopiesAllDocuments</span></span>

<span data-ttu-id="40b72-104">Este tópico não é atual.</span><span class="sxs-lookup"><span data-stu-id="40b72-104">This topic is not current.</span></span> <span data-ttu-id="40b72-105">Para obter as informações mais atuais, consulte a [Especificação de Esquema de Impressão](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="40b72-105">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="40b72-106">Especifica o número de cópias de um trabalho.</span><span class="sxs-lookup"><span data-stu-id="40b72-106">Specifies the number of copies of a job.</span></span>

-   [<span data-ttu-id="40b72-107">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="40b72-107">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="40b72-108">Conteúdo da estrutura</span><span class="sxs-lookup"><span data-stu-id="40b72-108">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="40b72-109">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="40b72-109">Element Information</span></span>



| <span data-ttu-id="40b72-110">Name</span><span class="sxs-lookup"><span data-stu-id="40b72-110">Name</span></span> | <span data-ttu-id="40b72-111">Valor</span><span class="sxs-lookup"><span data-stu-id="40b72-111">Value</span></span> |
|----------------------------|-------------------------|
| <span data-ttu-id="40b72-112">Tipo de elemento</span><span class="sxs-lookup"><span data-stu-id="40b72-112">Element Type</span></span> <br/>   | <span data-ttu-id="40b72-113">ParameterDef</span><span class="sxs-lookup"><span data-stu-id="40b72-113">ParameterDef</span></span><br/> |
| <span data-ttu-id="40b72-114">Prefixo de definição de scoping</span><span class="sxs-lookup"><span data-stu-id="40b72-114">Scoping Prefix</span></span> <br/> | <span data-ttu-id="40b72-115">Trabalho</span><span class="sxs-lookup"><span data-stu-id="40b72-115">Job</span></span><br/>          |
| <span data-ttu-id="40b72-116">Observações</span><span class="sxs-lookup"><span data-stu-id="40b72-116">Notes</span></span> <br/>          | <span data-ttu-id="40b72-117">Nenhum</span><span class="sxs-lookup"><span data-stu-id="40b72-117">None</span></span><br/>         |



 

## <a name="structure-content"></a><span data-ttu-id="40b72-118">Conteúdo da estrutura</span><span class="sxs-lookup"><span data-stu-id="40b72-118">Structure Content</span></span>

<span data-ttu-id="40b72-119">A estrutura XML desse elemento é:</span><span class="sxs-lookup"><span data-stu-id="40b72-119">The XML structure of this element is:</span></span>

``` syntax
<psf:ParameterDef name="psk:JobCopiesAllDocuments">
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

## <a name="structure-properties"></a><span data-ttu-id="40b72-120">Propriedades da estrutura</span><span class="sxs-lookup"><span data-stu-id="40b72-120">Structure Properties</span></span>

<span data-ttu-id="40b72-121">A tabela a seguir descreve as características das variáveis definidas na estrutura XML.</span><span class="sxs-lookup"><span data-stu-id="40b72-121">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="40b72-122">Propriedade</span><span class="sxs-lookup"><span data-stu-id="40b72-122">Property</span></span>                | <span data-ttu-id="40b72-123">xsi:type</span><span class="sxs-lookup"><span data-stu-id="40b72-123">xsi:type</span></span>           | <span data-ttu-id="40b72-124">Valor</span><span class="sxs-lookup"><span data-stu-id="40b72-124">Value</span></span>                        |
|-------------------------|--------------------|------------------------------|
| <span data-ttu-id="40b72-125">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="40b72-125">DataType</span></span><br/>     | <span data-ttu-id="40b72-126">string</span><span class="sxs-lookup"><span data-stu-id="40b72-126">string</span></span><br/>  | <span data-ttu-id="40b72-127">xs:integer</span><span class="sxs-lookup"><span data-stu-id="40b72-127">xs:integer</span></span><br/>        |
| <span data-ttu-id="40b72-128">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="40b72-128">DefaultValue</span></span><br/> | <span data-ttu-id="40b72-129">integer</span><span class="sxs-lookup"><span data-stu-id="40b72-129">integer</span></span><br/> | <span data-ttu-id="40b72-130">1</span><span class="sxs-lookup"><span data-stu-id="40b72-130">1</span></span><br/>                 |
| <span data-ttu-id="40b72-131">MaxValue</span><span class="sxs-lookup"><span data-stu-id="40b72-131">MaxValue</span></span><br/>     | <span data-ttu-id="40b72-132">Número inteiro</span><span class="sxs-lookup"><span data-stu-id="40b72-132">integer</span></span><br/> | <span data-ttu-id="40b72-133">não definido</span><span class="sxs-lookup"><span data-stu-id="40b72-133">undefined</span></span><br/>         |
| <span data-ttu-id="40b72-134">Minvalue</span><span class="sxs-lookup"><span data-stu-id="40b72-134">MinValue</span></span><br/>     | <span data-ttu-id="40b72-135">integer</span><span class="sxs-lookup"><span data-stu-id="40b72-135">integer</span></span><br/> | <span data-ttu-id="40b72-136">1</span><span class="sxs-lookup"><span data-stu-id="40b72-136">1</span></span><br/>                 |
| <span data-ttu-id="40b72-137">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="40b72-137">Mandatory</span></span><br/>    | <span data-ttu-id="40b72-138">string</span><span class="sxs-lookup"><span data-stu-id="40b72-138">string</span></span><br/>  | <span data-ttu-id="40b72-139">psk:Incondicional</span><span class="sxs-lookup"><span data-stu-id="40b72-139">psk:Unconditional</span></span><br/> |
| <span data-ttu-id="40b72-140">Vários</span><span class="sxs-lookup"><span data-stu-id="40b72-140">Multiple</span></span><br/>     | <span data-ttu-id="40b72-141">integer</span><span class="sxs-lookup"><span data-stu-id="40b72-141">integer</span></span><br/> | <span data-ttu-id="40b72-142">1</span><span class="sxs-lookup"><span data-stu-id="40b72-142">1</span></span><br/>                 |
| <span data-ttu-id="40b72-143">Unittype</span><span class="sxs-lookup"><span data-stu-id="40b72-143">UnitType</span></span><br/>     | <span data-ttu-id="40b72-144">string</span><span class="sxs-lookup"><span data-stu-id="40b72-144">string</span></span><br/>  | <span data-ttu-id="40b72-145">Cópias</span><span class="sxs-lookup"><span data-stu-id="40b72-145">copies</span></span><br/>            |



 

## <a name="related-topics"></a><span data-ttu-id="40b72-146">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="40b72-146">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="40b72-147">Especificação de esquema de impressão</span><span class="sxs-lookup"><span data-stu-id="40b72-147">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




