---
description: Saiba mais sobre o elemento DocumentBannerSheetSource, que especifica a origem de uma folha de faixa personalizada.
ms.assetid: 3b55935f-3d71-43cc-9c59-5019d7eb5cc5
title: DocumentBannerSheetSource
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d33aa949982e98781c42cbf6aa770dbd4e3d1707
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/19/2021
ms.locfileid: "112409469"
---
# <a name="documentbannersheetsource"></a><span data-ttu-id="aa4b1-103">DocumentBannerSheetSource</span><span class="sxs-lookup"><span data-stu-id="aa4b1-103">DocumentBannerSheetSource</span></span>

<span data-ttu-id="aa4b1-104">Este tópico não é atual.</span><span class="sxs-lookup"><span data-stu-id="aa4b1-104">This topic is not current.</span></span> <span data-ttu-id="aa4b1-105">Para obter as informações mais atuais, consulte a [especificação do esquema de impressão](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="aa4b1-105">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="aa4b1-106">Especifica a origem de uma folha de faixa personalizada.</span><span class="sxs-lookup"><span data-stu-id="aa4b1-106">Specifies the source for a custom banner sheet.</span></span>

-   [<span data-ttu-id="aa4b1-107">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="aa4b1-107">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="aa4b1-108">Conteúdo da estrutura</span><span class="sxs-lookup"><span data-stu-id="aa4b1-108">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="aa4b1-109">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="aa4b1-109">Element Information</span></span>



| <span data-ttu-id="aa4b1-110">Name</span><span class="sxs-lookup"><span data-stu-id="aa4b1-110">Name</span></span> | <span data-ttu-id="aa4b1-111">Valor</span><span class="sxs-lookup"><span data-stu-id="aa4b1-111">Value</span></span> |
|----------------------------|--------------------------------------------------|
| <span data-ttu-id="aa4b1-112">Tipo de elemento</span><span class="sxs-lookup"><span data-stu-id="aa4b1-112">Element Type</span></span> <br/>   | <span data-ttu-id="aa4b1-113">ParameterDef</span><span class="sxs-lookup"><span data-stu-id="aa4b1-113">ParameterDef</span></span><br/>                          |
| <span data-ttu-id="aa4b1-114">Prefixo de escopo</span><span class="sxs-lookup"><span data-stu-id="aa4b1-114">Scoping Prefix</span></span> <br/> | <span data-ttu-id="aa4b1-115">Documento</span><span class="sxs-lookup"><span data-stu-id="aa4b1-115">Document</span></span><br/>                              |
| <span data-ttu-id="aa4b1-116">Observações</span><span class="sxs-lookup"><span data-stu-id="aa4b1-116">Notes</span></span> <br/>          | <span data-ttu-id="aa4b1-117">Vinculado ao elemento DocumentBannerSheet</span><span class="sxs-lookup"><span data-stu-id="aa4b1-117">Linked to DocumentBannerSheet element</span></span><br/> |



 

## <a name="structure-content"></a><span data-ttu-id="aa4b1-118">Conteúdo da estrutura</span><span class="sxs-lookup"><span data-stu-id="aa4b1-118">Structure Content</span></span>

<span data-ttu-id="aa4b1-119">A estrutura XML desse elemento é:</span><span class="sxs-lookup"><span data-stu-id="aa4b1-119">The XML structure of this element is:</span></span>

``` syntax
<psf:ParameterDef name="psk:DocumentBannerSheetSource">
  <psf:Property name="psf:DataType">
    <psf:Value xsi:type="xs:string">xs:string</psf:Value>
  </psf:Property>
  <psf:Property name="psf:DefaultValue">
    <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
  </psf:Property>
  <psf:Property name="psf:MaxLength">
    <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
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

## <a name="structure-properties"></a><span data-ttu-id="aa4b1-120">Propriedades da estrutura</span><span class="sxs-lookup"><span data-stu-id="aa4b1-120">Structure Properties</span></span>

<span data-ttu-id="aa4b1-121">A tabela a seguir descreve as características das variáveis definidas na estrutura XML.</span><span class="sxs-lookup"><span data-stu-id="aa4b1-121">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="aa4b1-122">Propriedade</span><span class="sxs-lookup"><span data-stu-id="aa4b1-122">Property</span></span>                | <span data-ttu-id="aa4b1-123">xsi:type</span><span class="sxs-lookup"><span data-stu-id="aa4b1-123">xsi:type</span></span>           | <span data-ttu-id="aa4b1-124">Valor</span><span class="sxs-lookup"><span data-stu-id="aa4b1-124">Value</span></span>                      |
|-------------------------|--------------------|----------------------------|
| <span data-ttu-id="aa4b1-125">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="aa4b1-125">DataType</span></span><br/>     | <span data-ttu-id="aa4b1-126">string</span><span class="sxs-lookup"><span data-stu-id="aa4b1-126">string</span></span><br/>  | <span data-ttu-id="aa4b1-127">xs:string</span><span class="sxs-lookup"><span data-stu-id="aa4b1-127">xs:string</span></span><br/>       |
| <span data-ttu-id="aa4b1-128">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="aa4b1-128">DefaultValue</span></span><br/> | <span data-ttu-id="aa4b1-129">string</span><span class="sxs-lookup"><span data-stu-id="aa4b1-129">string</span></span><br/>  | <span data-ttu-id="aa4b1-130">não definido</span><span class="sxs-lookup"><span data-stu-id="aa4b1-130">undefined</span></span><br/>       |
| <span data-ttu-id="aa4b1-131">MaxLength</span><span class="sxs-lookup"><span data-stu-id="aa4b1-131">MaxLength</span></span><br/>    | <span data-ttu-id="aa4b1-132">Número inteiro</span><span class="sxs-lookup"><span data-stu-id="aa4b1-132">integer</span></span><br/> | <span data-ttu-id="aa4b1-133">não definido</span><span class="sxs-lookup"><span data-stu-id="aa4b1-133">undefined</span></span><br/>       |
| <span data-ttu-id="aa4b1-134">MinLength</span><span class="sxs-lookup"><span data-stu-id="aa4b1-134">MinLength</span></span><br/>    | <span data-ttu-id="aa4b1-135">integer</span><span class="sxs-lookup"><span data-stu-id="aa4b1-135">integer</span></span><br/> | <span data-ttu-id="aa4b1-136">1</span><span class="sxs-lookup"><span data-stu-id="aa4b1-136">1</span></span><br/>               |
| <span data-ttu-id="aa4b1-137">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="aa4b1-137">Mandatory</span></span><br/>    | <span data-ttu-id="aa4b1-138">string</span><span class="sxs-lookup"><span data-stu-id="aa4b1-138">string</span></span><br/>  | <span data-ttu-id="aa4b1-139">PSK: condicional</span><span class="sxs-lookup"><span data-stu-id="aa4b1-139">psk:Conditional</span></span><br/> |
| <span data-ttu-id="aa4b1-140">UnitType</span><span class="sxs-lookup"><span data-stu-id="aa4b1-140">UnitType</span></span><br/>     | <span data-ttu-id="aa4b1-141">string</span><span class="sxs-lookup"><span data-stu-id="aa4b1-141">string</span></span><br/>  | <span data-ttu-id="aa4b1-142">characters</span><span class="sxs-lookup"><span data-stu-id="aa4b1-142">characters</span></span><br/>      |



 

## <a name="related-topics"></a><span data-ttu-id="aa4b1-143">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="aa4b1-143">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="aa4b1-144">Especificação de esquema de impressão</span><span class="sxs-lookup"><span data-stu-id="aa4b1-144">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




