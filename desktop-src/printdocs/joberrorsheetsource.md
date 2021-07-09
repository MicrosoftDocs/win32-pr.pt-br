---
description: Obtenha informações sobre o parâmetro JobErrorSheetSource. Este tópico não é atual. Para obter as informações mais atuais, consulte a especificação do esquema de impressão.
ms.assetid: 6de13ed8-bf15-4e2c-b42a-ea8178a6b5f9
title: JobErrorSheetSource
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 656d71422c46800d6155c1dea1e221f9c6dfe021
ms.sourcegitcommit: 998d50f6def8a25850fc113fc8a2df903c829c5e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/09/2021
ms.locfileid: "113549384"
---
# <a name="joberrorsheetsource"></a><span data-ttu-id="3209e-105">JobErrorSheetSource</span><span class="sxs-lookup"><span data-stu-id="3209e-105">JobErrorSheetSource</span></span>

<span data-ttu-id="3209e-106">Este tópico não é atual.</span><span class="sxs-lookup"><span data-stu-id="3209e-106">This topic is not current.</span></span> <span data-ttu-id="3209e-107">Para obter as informações mais atuais, consulte a [especificação do esquema de impressão](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="3209e-107">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="3209e-108">Especifica a origem de uma planilha de erros personalizada.</span><span class="sxs-lookup"><span data-stu-id="3209e-108">Specifies the source for a custom error sheet.</span></span>

-   [<span data-ttu-id="3209e-109">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="3209e-109">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="3209e-110">Conteúdo da estrutura</span><span class="sxs-lookup"><span data-stu-id="3209e-110">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="3209e-111">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="3209e-111">Element Information</span></span>



| <span data-ttu-id="3209e-112">Nome</span><span class="sxs-lookup"><span data-stu-id="3209e-112">Name</span></span> | <span data-ttu-id="3209e-113">Valor</span><span class="sxs-lookup"><span data-stu-id="3209e-113">Value</span></span> |
|----------------------------|--------------------------------------------|
| <span data-ttu-id="3209e-114">Tipo de elemento</span><span class="sxs-lookup"><span data-stu-id="3209e-114">Element Type</span></span> <br/>   | <span data-ttu-id="3209e-115">ParameterDef</span><span class="sxs-lookup"><span data-stu-id="3209e-115">ParameterDef</span></span><br/>                    |
| <span data-ttu-id="3209e-116">Prefixo de escopo</span><span class="sxs-lookup"><span data-stu-id="3209e-116">Scoping Prefix</span></span> <br/> | <span data-ttu-id="3209e-117">Documento</span><span class="sxs-lookup"><span data-stu-id="3209e-117">Document</span></span><br/>                        |
| <span data-ttu-id="3209e-118">Observações</span><span class="sxs-lookup"><span data-stu-id="3209e-118">Notes</span></span> <br/>          | <span data-ttu-id="3209e-119">Vinculado ao elemento JobErrorSheet</span><span class="sxs-lookup"><span data-stu-id="3209e-119">Linked to JobErrorSheet element</span></span><br/> |



 

## <a name="structure-content"></a><span data-ttu-id="3209e-120">Conteúdo da estrutura</span><span class="sxs-lookup"><span data-stu-id="3209e-120">Structure Content</span></span>

<span data-ttu-id="3209e-121">A estrutura XML desse elemento é:</span><span class="sxs-lookup"><span data-stu-id="3209e-121">The XML structure of this element is:</span></span>

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

## <a name="structure-properties"></a><span data-ttu-id="3209e-122">Propriedades da estrutura</span><span class="sxs-lookup"><span data-stu-id="3209e-122">Structure Properties</span></span>

<span data-ttu-id="3209e-123">A tabela a seguir descreve as características das variáveis definidas na estrutura XML.</span><span class="sxs-lookup"><span data-stu-id="3209e-123">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="3209e-124">Propriedade</span><span class="sxs-lookup"><span data-stu-id="3209e-124">Property</span></span>                | <span data-ttu-id="3209e-125">xsi:type</span><span class="sxs-lookup"><span data-stu-id="3209e-125">xsi:type</span></span>           | <span data-ttu-id="3209e-126">Valor</span><span class="sxs-lookup"><span data-stu-id="3209e-126">Value</span></span>                      |
|-------------------------|--------------------|----------------------------|
| <span data-ttu-id="3209e-127">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="3209e-127">DataType</span></span><br/>     | <span data-ttu-id="3209e-128">string</span><span class="sxs-lookup"><span data-stu-id="3209e-128">string</span></span><br/>  | <span data-ttu-id="3209e-129">xs:string</span><span class="sxs-lookup"><span data-stu-id="3209e-129">xs:string</span></span><br/>       |
| <span data-ttu-id="3209e-130">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="3209e-130">DefaultValue</span></span><br/> | <span data-ttu-id="3209e-131">string</span><span class="sxs-lookup"><span data-stu-id="3209e-131">string</span></span><br/>  | <span data-ttu-id="3209e-132">não definido</span><span class="sxs-lookup"><span data-stu-id="3209e-132">undefined</span></span><br/>       |
| <span data-ttu-id="3209e-133">MaxLength</span><span class="sxs-lookup"><span data-stu-id="3209e-133">MaxLength</span></span><br/>    | <span data-ttu-id="3209e-134">Número inteiro</span><span class="sxs-lookup"><span data-stu-id="3209e-134">integer</span></span><br/> | <span data-ttu-id="3209e-135">não definido</span><span class="sxs-lookup"><span data-stu-id="3209e-135">undefined</span></span><br/>       |
| <span data-ttu-id="3209e-136">MinLength</span><span class="sxs-lookup"><span data-stu-id="3209e-136">MinLength</span></span><br/>    | <span data-ttu-id="3209e-137">integer</span><span class="sxs-lookup"><span data-stu-id="3209e-137">integer</span></span><br/> | <span data-ttu-id="3209e-138">1</span><span class="sxs-lookup"><span data-stu-id="3209e-138">1</span></span><br/>               |
| <span data-ttu-id="3209e-139">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="3209e-139">Mandatory</span></span><br/>    | <span data-ttu-id="3209e-140">string</span><span class="sxs-lookup"><span data-stu-id="3209e-140">string</span></span><br/>  | <span data-ttu-id="3209e-141">PSK: condicional</span><span class="sxs-lookup"><span data-stu-id="3209e-141">psk:Conditional</span></span><br/> |
| <span data-ttu-id="3209e-142">UnitType</span><span class="sxs-lookup"><span data-stu-id="3209e-142">UnitType</span></span><br/>     | <span data-ttu-id="3209e-143">string</span><span class="sxs-lookup"><span data-stu-id="3209e-143">string</span></span><br/>  | <span data-ttu-id="3209e-144">characters</span><span class="sxs-lookup"><span data-stu-id="3209e-144">characters</span></span><br/>      |



 

## <a name="related-topics"></a><span data-ttu-id="3209e-145">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="3209e-145">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3209e-146">Especificação de esquema de impressão</span><span class="sxs-lookup"><span data-stu-id="3209e-146">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




