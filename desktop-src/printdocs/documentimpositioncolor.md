---
description: Saiba mais sobre o parâmetro DocumentImpositionColor. Este tópico não é atual. Para obter as informações mais atuais, consulte a especificação do esquema de impressão.
ms.assetid: e1cb7e46-3078-46bf-a8c8-e10f6b9dd222
title: DocumentImpositionColor
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b747487c19160d29778f306a91b62cf43d245f65
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/30/2021
ms.locfileid: "113120001"
---
# <a name="documentimpositioncolor"></a><span data-ttu-id="80211-105">DocumentImpositionColor</span><span class="sxs-lookup"><span data-stu-id="80211-105">DocumentImpositionColor</span></span>

<span data-ttu-id="80211-106">Este tópico não é atual.</span><span class="sxs-lookup"><span data-stu-id="80211-106">This topic is not current.</span></span> <span data-ttu-id="80211-107">Para obter as informações mais atuais, consulte a [especificação do esquema de impressão](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="80211-107">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="80211-108">O conteúdo do aplicativo rotulado com a cor nomeada especificada deve aparecer em todas as separações de cores.</span><span class="sxs-lookup"><span data-stu-id="80211-108">Application content labeled with the specified named color MUST appear on all color separations.</span></span>

-   [<span data-ttu-id="80211-109">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="80211-109">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="80211-110">Conteúdo da estrutura</span><span class="sxs-lookup"><span data-stu-id="80211-110">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="80211-111">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="80211-111">Element Information</span></span>



| <span data-ttu-id="80211-112">Nome</span><span class="sxs-lookup"><span data-stu-id="80211-112">Name</span></span> | <span data-ttu-id="80211-113">Valor</span><span class="sxs-lookup"><span data-stu-id="80211-113">Value</span></span> |
|----------------------------|-------------------------|
| <span data-ttu-id="80211-114">Tipo de elemento</span><span class="sxs-lookup"><span data-stu-id="80211-114">Element Type</span></span> <br/>   | <span data-ttu-id="80211-115">ParameterDef</span><span class="sxs-lookup"><span data-stu-id="80211-115">ParameterDef</span></span><br/> |
| <span data-ttu-id="80211-116">Prefixo de escopo</span><span class="sxs-lookup"><span data-stu-id="80211-116">Scoping Prefix</span></span> <br/> | <span data-ttu-id="80211-117">Documento</span><span class="sxs-lookup"><span data-stu-id="80211-117">Document</span></span><br/>     |
| <span data-ttu-id="80211-118">Observações</span><span class="sxs-lookup"><span data-stu-id="80211-118">Notes</span></span> <br/>          | <span data-ttu-id="80211-119">Nenhum</span><span class="sxs-lookup"><span data-stu-id="80211-119">None</span></span><br/>         |



 

## <a name="structure-content"></a><span data-ttu-id="80211-120">Conteúdo da estrutura</span><span class="sxs-lookup"><span data-stu-id="80211-120">Structure Content</span></span>

<span data-ttu-id="80211-121">A estrutura XML desse elemento é:</span><span class="sxs-lookup"><span data-stu-id="80211-121">The XML structure of this element is:</span></span>

``` syntax
<psf:ParameterDef name="psk:DocumentImpositionColor">
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

## <a name="structure-properties"></a><span data-ttu-id="80211-122">Propriedades da estrutura</span><span class="sxs-lookup"><span data-stu-id="80211-122">Structure Properties</span></span>

<span data-ttu-id="80211-123">A tabela a seguir descreve as características das variáveis definidas na estrutura XML.</span><span class="sxs-lookup"><span data-stu-id="80211-123">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="80211-124">Propriedade</span><span class="sxs-lookup"><span data-stu-id="80211-124">Property</span></span>                | <span data-ttu-id="80211-125">xsi:type</span><span class="sxs-lookup"><span data-stu-id="80211-125">xsi:type</span></span>           | <span data-ttu-id="80211-126">Valor</span><span class="sxs-lookup"><span data-stu-id="80211-126">Value</span></span>                      |
|-------------------------|--------------------|----------------------------|
| <span data-ttu-id="80211-127">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="80211-127">DataType</span></span><br/>     | <span data-ttu-id="80211-128">string</span><span class="sxs-lookup"><span data-stu-id="80211-128">string</span></span><br/>  | <span data-ttu-id="80211-129">xs:string</span><span class="sxs-lookup"><span data-stu-id="80211-129">xs:string</span></span><br/>       |
| <span data-ttu-id="80211-130">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="80211-130">DefaultValue</span></span><br/> | <span data-ttu-id="80211-131">string</span><span class="sxs-lookup"><span data-stu-id="80211-131">string</span></span><br/>  | <span data-ttu-id="80211-132">não definido</span><span class="sxs-lookup"><span data-stu-id="80211-132">undefined</span></span><br/>       |
| <span data-ttu-id="80211-133">MaxLength</span><span class="sxs-lookup"><span data-stu-id="80211-133">MaxLength</span></span><br/>    | <span data-ttu-id="80211-134">Número inteiro</span><span class="sxs-lookup"><span data-stu-id="80211-134">integer</span></span><br/> | <span data-ttu-id="80211-135">não definido</span><span class="sxs-lookup"><span data-stu-id="80211-135">undefined</span></span><br/>       |
| <span data-ttu-id="80211-136">MinLength</span><span class="sxs-lookup"><span data-stu-id="80211-136">MinLength</span></span><br/>    | <span data-ttu-id="80211-137">integer</span><span class="sxs-lookup"><span data-stu-id="80211-137">integer</span></span><br/> | <span data-ttu-id="80211-138">1</span><span class="sxs-lookup"><span data-stu-id="80211-138">1</span></span><br/>               |
| <span data-ttu-id="80211-139">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="80211-139">Mandatory</span></span><br/>    | <span data-ttu-id="80211-140">string</span><span class="sxs-lookup"><span data-stu-id="80211-140">string</span></span><br/>  | <span data-ttu-id="80211-141">PSK: condicional</span><span class="sxs-lookup"><span data-stu-id="80211-141">psk:Conditional</span></span><br/> |
| <span data-ttu-id="80211-142">UnitType</span><span class="sxs-lookup"><span data-stu-id="80211-142">UnitType</span></span><br/>     | <span data-ttu-id="80211-143">string</span><span class="sxs-lookup"><span data-stu-id="80211-143">string</span></span><br/>  | <span data-ttu-id="80211-144">characters</span><span class="sxs-lookup"><span data-stu-id="80211-144">characters</span></span><br/>      |



 

## <a name="related-topics"></a><span data-ttu-id="80211-145">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="80211-145">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="80211-146">Especificação de esquema de impressão</span><span class="sxs-lookup"><span data-stu-id="80211-146">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




