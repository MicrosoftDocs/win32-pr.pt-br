---
description: Este tópico não é atual. Para obter as informações mais atuais, consulte a especificação do esquema de impressão.
ms.assetid: 584a71cd-fc32-485e-a627-27be95c377a9
title: JobCopiesAllDocuments
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3e8e606095462dc3a2eee1391121bf663de3655c
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/26/2021
ms.locfileid: "107998363"
---
# <a name="jobcopiesalldocuments"></a><span data-ttu-id="5a71f-104">JobCopiesAllDocuments</span><span class="sxs-lookup"><span data-stu-id="5a71f-104">JobCopiesAllDocuments</span></span>

<span data-ttu-id="5a71f-105">Este tópico não é atual.</span><span class="sxs-lookup"><span data-stu-id="5a71f-105">This topic is not current.</span></span> <span data-ttu-id="5a71f-106">Para obter as informações mais atuais, consulte a [especificação do esquema de impressão](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="5a71f-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="5a71f-107">Especifica o número de cópias de um trabalho.</span><span class="sxs-lookup"><span data-stu-id="5a71f-107">Specifies the number of copies of a job.</span></span>

-   [<span data-ttu-id="5a71f-108">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="5a71f-108">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="5a71f-109">Conteúdo da estrutura</span><span class="sxs-lookup"><span data-stu-id="5a71f-109">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="5a71f-110">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="5a71f-110">Element Information</span></span>



| <span data-ttu-id="5a71f-111">Nome</span><span class="sxs-lookup"><span data-stu-id="5a71f-111">Name</span></span> | <span data-ttu-id="5a71f-112">Valor</span><span class="sxs-lookup"><span data-stu-id="5a71f-112">Value</span></span> |
|----------------------------|-------------------------|
| <span data-ttu-id="5a71f-113">Tipo de elemento</span><span class="sxs-lookup"><span data-stu-id="5a71f-113">Element Type</span></span> <br/>   | <span data-ttu-id="5a71f-114">ParameterDef</span><span class="sxs-lookup"><span data-stu-id="5a71f-114">ParameterDef</span></span><br/> |
| <span data-ttu-id="5a71f-115">Prefixo de escopo</span><span class="sxs-lookup"><span data-stu-id="5a71f-115">Scoping Prefix</span></span> <br/> | <span data-ttu-id="5a71f-116">Trabalho</span><span class="sxs-lookup"><span data-stu-id="5a71f-116">Job</span></span><br/>          |
| <span data-ttu-id="5a71f-117">Observações</span><span class="sxs-lookup"><span data-stu-id="5a71f-117">Notes</span></span> <br/>          | <span data-ttu-id="5a71f-118">Nenhum</span><span class="sxs-lookup"><span data-stu-id="5a71f-118">None</span></span><br/>         |



 

## <a name="structure-content"></a><span data-ttu-id="5a71f-119">Conteúdo da estrutura</span><span class="sxs-lookup"><span data-stu-id="5a71f-119">Structure Content</span></span>

<span data-ttu-id="5a71f-120">A estrutura XML desse elemento é:</span><span class="sxs-lookup"><span data-stu-id="5a71f-120">The XML structure of this element is:</span></span>

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

## <a name="structure-properties"></a><span data-ttu-id="5a71f-121">Propriedades da estrutura</span><span class="sxs-lookup"><span data-stu-id="5a71f-121">Structure Properties</span></span>

<span data-ttu-id="5a71f-122">A tabela a seguir descreve as características das variáveis definidas na estrutura XML.</span><span class="sxs-lookup"><span data-stu-id="5a71f-122">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="5a71f-123">Propriedade</span><span class="sxs-lookup"><span data-stu-id="5a71f-123">Property</span></span>                | <span data-ttu-id="5a71f-124">xsi:type</span><span class="sxs-lookup"><span data-stu-id="5a71f-124">xsi:type</span></span>           | <span data-ttu-id="5a71f-125">Valor</span><span class="sxs-lookup"><span data-stu-id="5a71f-125">Value</span></span>                        |
|-------------------------|--------------------|------------------------------|
| <span data-ttu-id="5a71f-126">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="5a71f-126">DataType</span></span><br/>     | <span data-ttu-id="5a71f-127">string</span><span class="sxs-lookup"><span data-stu-id="5a71f-127">string</span></span><br/>  | <span data-ttu-id="5a71f-128">xs:integer</span><span class="sxs-lookup"><span data-stu-id="5a71f-128">xs:integer</span></span><br/>        |
| <span data-ttu-id="5a71f-129">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="5a71f-129">DefaultValue</span></span><br/> | <span data-ttu-id="5a71f-130">integer</span><span class="sxs-lookup"><span data-stu-id="5a71f-130">integer</span></span><br/> | <span data-ttu-id="5a71f-131">1</span><span class="sxs-lookup"><span data-stu-id="5a71f-131">1</span></span><br/>                 |
| <span data-ttu-id="5a71f-132">MaxValue</span><span class="sxs-lookup"><span data-stu-id="5a71f-132">MaxValue</span></span><br/>     | <span data-ttu-id="5a71f-133">Número inteiro</span><span class="sxs-lookup"><span data-stu-id="5a71f-133">integer</span></span><br/> | <span data-ttu-id="5a71f-134">não definido</span><span class="sxs-lookup"><span data-stu-id="5a71f-134">undefined</span></span><br/>         |
| <span data-ttu-id="5a71f-135">MinValue</span><span class="sxs-lookup"><span data-stu-id="5a71f-135">MinValue</span></span><br/>     | <span data-ttu-id="5a71f-136">integer</span><span class="sxs-lookup"><span data-stu-id="5a71f-136">integer</span></span><br/> | <span data-ttu-id="5a71f-137">1</span><span class="sxs-lookup"><span data-stu-id="5a71f-137">1</span></span><br/>                 |
| <span data-ttu-id="5a71f-138">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="5a71f-138">Mandatory</span></span><br/>    | <span data-ttu-id="5a71f-139">string</span><span class="sxs-lookup"><span data-stu-id="5a71f-139">string</span></span><br/>  | <span data-ttu-id="5a71f-140">PSK: incondicional</span><span class="sxs-lookup"><span data-stu-id="5a71f-140">psk:Unconditional</span></span><br/> |
| <span data-ttu-id="5a71f-141">Vários</span><span class="sxs-lookup"><span data-stu-id="5a71f-141">Multiple</span></span><br/>     | <span data-ttu-id="5a71f-142">integer</span><span class="sxs-lookup"><span data-stu-id="5a71f-142">integer</span></span><br/> | <span data-ttu-id="5a71f-143">1</span><span class="sxs-lookup"><span data-stu-id="5a71f-143">1</span></span><br/>                 |
| <span data-ttu-id="5a71f-144">UnitType</span><span class="sxs-lookup"><span data-stu-id="5a71f-144">UnitType</span></span><br/>     | <span data-ttu-id="5a71f-145">string</span><span class="sxs-lookup"><span data-stu-id="5a71f-145">string</span></span><br/>  | <span data-ttu-id="5a71f-146">cópia</span><span class="sxs-lookup"><span data-stu-id="5a71f-146">copies</span></span><br/>            |



 

## <a name="related-topics"></a><span data-ttu-id="5a71f-147">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="5a71f-147">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5a71f-148">Especificação de esquema de impressão</span><span class="sxs-lookup"><span data-stu-id="5a71f-148">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




