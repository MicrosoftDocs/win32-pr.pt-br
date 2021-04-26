---
description: Este tópico não é atual. Para obter as informações mais atuais, consulte a especificação do esquema de impressão.
ms.assetid: b360f870-bfaa-4d4d-adce-17fcfc48b6a6
title: PageDestinationColorProfileEmbedded
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a7053cfaf82d7fdfccfe79cebcd76e49befeb125
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/26/2021
ms.locfileid: "107996123"
---
# <a name="pagedestinationcolorprofileembedded"></a><span data-ttu-id="e4f33-104">PageDestinationColorProfileEmbedded</span><span class="sxs-lookup"><span data-stu-id="e4f33-104">PageDestinationColorProfileEmbedded</span></span>

<span data-ttu-id="e4f33-105">Este tópico não é atual.</span><span class="sxs-lookup"><span data-stu-id="e4f33-105">This topic is not current.</span></span> <span data-ttu-id="e4f33-106">Para obter as informações mais atuais, consulte a [especificação do esquema de impressão](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="e4f33-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="e4f33-107">Especifica o perfil de cor de destino inserido.</span><span class="sxs-lookup"><span data-stu-id="e4f33-107">Specifies the embedded destination color profile.</span></span>

-   [<span data-ttu-id="e4f33-108">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="e4f33-108">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="e4f33-109">Conteúdo da estrutura</span><span class="sxs-lookup"><span data-stu-id="e4f33-109">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="e4f33-110">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="e4f33-110">Element Information</span></span>



| <span data-ttu-id="e4f33-111">Nome</span><span class="sxs-lookup"><span data-stu-id="e4f33-111">Name</span></span> | <span data-ttu-id="e4f33-112">Valor</span><span class="sxs-lookup"><span data-stu-id="e4f33-112">Value</span></span> |
|----------------------------|----------------------------------------------------------|
| <span data-ttu-id="e4f33-113">Tipo de elemento</span><span class="sxs-lookup"><span data-stu-id="e4f33-113">Element Type</span></span> <br/>   | <span data-ttu-id="e4f33-114">ParameterDef</span><span class="sxs-lookup"><span data-stu-id="e4f33-114">ParameterDef</span></span><br/>                                  |
| <span data-ttu-id="e4f33-115">Prefixo de escopo</span><span class="sxs-lookup"><span data-stu-id="e4f33-115">Scoping Prefix</span></span> <br/> | <span data-ttu-id="e4f33-116">?</span><span class="sxs-lookup"><span data-stu-id="e4f33-116">Page</span></span><br/>                                          |
| <span data-ttu-id="e4f33-117">Observações</span><span class="sxs-lookup"><span data-stu-id="e4f33-117">Notes</span></span> <br/>          | <span data-ttu-id="e4f33-118">Vinculado ao elemento PageDestinationColorProfile</span><span class="sxs-lookup"><span data-stu-id="e4f33-118">Linked to PageDestinationColorProfile element</span></span><br/> |



 

## <a name="structure-content"></a><span data-ttu-id="e4f33-119">Conteúdo da estrutura</span><span class="sxs-lookup"><span data-stu-id="e4f33-119">Structure Content</span></span>

<span data-ttu-id="e4f33-120">A estrutura XML desse elemento é:</span><span class="sxs-lookup"><span data-stu-id="e4f33-120">The XML structure of this element is:</span></span>

``` syntax
<psf:ParameterDef name="psk:PageDestinationColorProfileEmbedded">
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

## <a name="structure-properties"></a><span data-ttu-id="e4f33-121">Propriedades da estrutura</span><span class="sxs-lookup"><span data-stu-id="e4f33-121">Structure Properties</span></span>

<span data-ttu-id="e4f33-122">A tabela a seguir descreve as características das variáveis definidas na estrutura XML.</span><span class="sxs-lookup"><span data-stu-id="e4f33-122">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="e4f33-123">Propriedade</span><span class="sxs-lookup"><span data-stu-id="e4f33-123">Property</span></span>                | <span data-ttu-id="e4f33-124">xsi:type</span><span class="sxs-lookup"><span data-stu-id="e4f33-124">xsi:type</span></span>           | <span data-ttu-id="e4f33-125">Valor</span><span class="sxs-lookup"><span data-stu-id="e4f33-125">Value</span></span>                      |
|-------------------------|--------------------|----------------------------|
| <span data-ttu-id="e4f33-126">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="e4f33-126">DataType</span></span><br/>     | <span data-ttu-id="e4f33-127">string</span><span class="sxs-lookup"><span data-stu-id="e4f33-127">string</span></span><br/>  | <span data-ttu-id="e4f33-128">xs:string</span><span class="sxs-lookup"><span data-stu-id="e4f33-128">xs:string</span></span><br/>       |
| <span data-ttu-id="e4f33-129">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="e4f33-129">DefaultValue</span></span><br/> | <span data-ttu-id="e4f33-130">string</span><span class="sxs-lookup"><span data-stu-id="e4f33-130">string</span></span><br/>  | <span data-ttu-id="e4f33-131">não definido</span><span class="sxs-lookup"><span data-stu-id="e4f33-131">undefined</span></span><br/>       |
| <span data-ttu-id="e4f33-132">MaxLength</span><span class="sxs-lookup"><span data-stu-id="e4f33-132">MaxLength</span></span><br/>    | <span data-ttu-id="e4f33-133">Número inteiro</span><span class="sxs-lookup"><span data-stu-id="e4f33-133">integer</span></span><br/> | <span data-ttu-id="e4f33-134">não definido</span><span class="sxs-lookup"><span data-stu-id="e4f33-134">undefined</span></span><br/>       |
| <span data-ttu-id="e4f33-135">MinLength</span><span class="sxs-lookup"><span data-stu-id="e4f33-135">MinLength</span></span><br/>    | <span data-ttu-id="e4f33-136">integer</span><span class="sxs-lookup"><span data-stu-id="e4f33-136">integer</span></span><br/> | <span data-ttu-id="e4f33-137">1</span><span class="sxs-lookup"><span data-stu-id="e4f33-137">1</span></span><br/>               |
| <span data-ttu-id="e4f33-138">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="e4f33-138">Mandatory</span></span><br/>    | <span data-ttu-id="e4f33-139">string</span><span class="sxs-lookup"><span data-stu-id="e4f33-139">string</span></span><br/>  | <span data-ttu-id="e4f33-140">PSK: condicional</span><span class="sxs-lookup"><span data-stu-id="e4f33-140">psk:Conditional</span></span><br/> |
| <span data-ttu-id="e4f33-141">UnitType</span><span class="sxs-lookup"><span data-stu-id="e4f33-141">UnitType</span></span><br/>     | <span data-ttu-id="e4f33-142">string</span><span class="sxs-lookup"><span data-stu-id="e4f33-142">string</span></span><br/>  | <span data-ttu-id="e4f33-143">characters</span><span class="sxs-lookup"><span data-stu-id="e4f33-143">characters</span></span><br/>      |



 

## <a name="related-topics"></a><span data-ttu-id="e4f33-144">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="e4f33-144">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e4f33-145">Especificação de esquema de impressão</span><span class="sxs-lookup"><span data-stu-id="e4f33-145">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




