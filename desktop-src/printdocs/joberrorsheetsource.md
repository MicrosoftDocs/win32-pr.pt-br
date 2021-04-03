---
description: Este tópico não é atual. Para obter as informações mais atuais, consulte a especificação do esquema de impressão.
ms.assetid: 6de13ed8-bf15-4e2c-b42a-ea8178a6b5f9
title: JobErrorSheetSource
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ca3cd991772b902239914d02d1bfa57d5ef03374
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/05/2021
ms.locfileid: "103930243"
---
# <a name="joberrorsheetsource"></a><span data-ttu-id="96e7c-104">JobErrorSheetSource</span><span class="sxs-lookup"><span data-stu-id="96e7c-104">JobErrorSheetSource</span></span>

<span data-ttu-id="96e7c-105">Este tópico não é atual.</span><span class="sxs-lookup"><span data-stu-id="96e7c-105">This topic is not current.</span></span> <span data-ttu-id="96e7c-106">Para obter as informações mais atuais, consulte a [especificação do esquema de impressão](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="96e7c-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="96e7c-107">Especifica a origem de uma planilha de erros personalizada.</span><span class="sxs-lookup"><span data-stu-id="96e7c-107">Specifies the source for a custom error sheet.</span></span>

-   [<span data-ttu-id="96e7c-108">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="96e7c-108">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="96e7c-109">Conteúdo da estrutura</span><span class="sxs-lookup"><span data-stu-id="96e7c-109">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="96e7c-110">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="96e7c-110">Element Information</span></span>



| <span data-ttu-id="96e7c-111">Nome</span><span class="sxs-lookup"><span data-stu-id="96e7c-111">Name</span></span>                       |                                            |
|----------------------------|--------------------------------------------|
| <span data-ttu-id="96e7c-112">Tipo de elemento</span><span class="sxs-lookup"><span data-stu-id="96e7c-112">Element Type</span></span> <br/>   | <span data-ttu-id="96e7c-113">ParameterDef</span><span class="sxs-lookup"><span data-stu-id="96e7c-113">ParameterDef</span></span><br/>                    |
| <span data-ttu-id="96e7c-114">Prefixo de escopo</span><span class="sxs-lookup"><span data-stu-id="96e7c-114">Scoping Prefix</span></span> <br/> | <span data-ttu-id="96e7c-115">Documento</span><span class="sxs-lookup"><span data-stu-id="96e7c-115">Document</span></span><br/>                        |
| <span data-ttu-id="96e7c-116">Observações</span><span class="sxs-lookup"><span data-stu-id="96e7c-116">Notes</span></span> <br/>          | <span data-ttu-id="96e7c-117">Vinculado ao elemento JobErrorSheet</span><span class="sxs-lookup"><span data-stu-id="96e7c-117">Linked to JobErrorSheet element</span></span><br/> |



 

## <a name="structure-content"></a><span data-ttu-id="96e7c-118">Conteúdo da estrutura</span><span class="sxs-lookup"><span data-stu-id="96e7c-118">Structure Content</span></span>

<span data-ttu-id="96e7c-119">A estrutura XML desse elemento é:</span><span class="sxs-lookup"><span data-stu-id="96e7c-119">The XML structure of this element is:</span></span>

``` syntax
<psf:ParameterDef name="psk:JobErrorSheetSource">
  <psf:Property name="psf:DataType">
    <psf:Value xsi:type="xs:string">xs:string</psf:Value>
  </psf:Property>
  <psf:Property name="psf:DefaultValue">
    <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
  </psf:Property>
  <psf:Property name="psf:MaxLength">
    <psf:Value xsi:type="xs:integer ">_Undefined_</psf:Value>
  </psf:Property>
  <psf:Property name="psf:MinLength">
    <psf:Value xsi:type="xs:integer">1</psf:Value>
  </psf:Property>
  <psf:Property name="psf:Mandatory">
    <psf:Value xsi:type="xs:string">psk:Conditional</psf:Value>
  </psf:Property>
  <psf:Property name="psf:UnitType">
    <psf:Value xsi:type="xs:string">characters</psf:Value>
  </psf:Property>
</psf:ParameterDef>      
```

## <a name="structure-properties"></a><span data-ttu-id="96e7c-120">Propriedades da estrutura</span><span class="sxs-lookup"><span data-stu-id="96e7c-120">Structure Properties</span></span>

<span data-ttu-id="96e7c-121">A tabela a seguir descreve as características das variáveis definidas na estrutura XML.</span><span class="sxs-lookup"><span data-stu-id="96e7c-121">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="96e7c-122">Propriedade</span><span class="sxs-lookup"><span data-stu-id="96e7c-122">Property</span></span>                | <span data-ttu-id="96e7c-123">xsi:type</span><span class="sxs-lookup"><span data-stu-id="96e7c-123">xsi:type</span></span>           | <span data-ttu-id="96e7c-124">Valor</span><span class="sxs-lookup"><span data-stu-id="96e7c-124">Value</span></span>                      |
|-------------------------|--------------------|----------------------------|
| <span data-ttu-id="96e7c-125">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="96e7c-125">DataType</span></span><br/>     | <span data-ttu-id="96e7c-126">string</span><span class="sxs-lookup"><span data-stu-id="96e7c-126">string</span></span><br/>  | <span data-ttu-id="96e7c-127">xs:string</span><span class="sxs-lookup"><span data-stu-id="96e7c-127">xs:string</span></span><br/>       |
| <span data-ttu-id="96e7c-128">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="96e7c-128">DefaultValue</span></span><br/> | <span data-ttu-id="96e7c-129">string</span><span class="sxs-lookup"><span data-stu-id="96e7c-129">string</span></span><br/>  | <span data-ttu-id="96e7c-130">não definido</span><span class="sxs-lookup"><span data-stu-id="96e7c-130">undefined</span></span><br/>       |
| <span data-ttu-id="96e7c-131">MaxLength</span><span class="sxs-lookup"><span data-stu-id="96e7c-131">MaxLength</span></span><br/>    | <span data-ttu-id="96e7c-132">Número inteiro</span><span class="sxs-lookup"><span data-stu-id="96e7c-132">integer</span></span><br/> | <span data-ttu-id="96e7c-133">não definido</span><span class="sxs-lookup"><span data-stu-id="96e7c-133">undefined</span></span><br/>       |
| <span data-ttu-id="96e7c-134">MinLength</span><span class="sxs-lookup"><span data-stu-id="96e7c-134">MinLength</span></span><br/>    | <span data-ttu-id="96e7c-135">integer</span><span class="sxs-lookup"><span data-stu-id="96e7c-135">integer</span></span><br/> | <span data-ttu-id="96e7c-136">1</span><span class="sxs-lookup"><span data-stu-id="96e7c-136">1</span></span><br/>               |
| <span data-ttu-id="96e7c-137">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="96e7c-137">Mandatory</span></span><br/>    | <span data-ttu-id="96e7c-138">string</span><span class="sxs-lookup"><span data-stu-id="96e7c-138">string</span></span><br/>  | <span data-ttu-id="96e7c-139">PSK: condicional</span><span class="sxs-lookup"><span data-stu-id="96e7c-139">psk:Conditional</span></span><br/> |
| <span data-ttu-id="96e7c-140">UnitType</span><span class="sxs-lookup"><span data-stu-id="96e7c-140">UnitType</span></span><br/>     | <span data-ttu-id="96e7c-141">string</span><span class="sxs-lookup"><span data-stu-id="96e7c-141">string</span></span><br/>  | <span data-ttu-id="96e7c-142">characters</span><span class="sxs-lookup"><span data-stu-id="96e7c-142">characters</span></span><br/>      |



 

## <a name="related-topics"></a><span data-ttu-id="96e7c-143">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="96e7c-143">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="96e7c-144">Especificação de esquema de impressão</span><span class="sxs-lookup"><span data-stu-id="96e7c-144">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




