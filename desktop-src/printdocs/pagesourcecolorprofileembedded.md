---
description: Este tópico não é atual. Para obter as informações mais atuais, consulte a especificação do esquema de impressão.
ms.assetid: 38411802-2b2e-441c-b3a6-334d87b11b5d
title: PageSourceColorProfileEmbedded
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 91e97e768561fd13d5033b12f69a9bc481448e0e
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/26/2021
ms.locfileid: "107999113"
---
# <a name="pagesourcecolorprofileembedded"></a><span data-ttu-id="93083-104">PageSourceColorProfileEmbedded</span><span class="sxs-lookup"><span data-stu-id="93083-104">PageSourceColorProfileEmbedded</span></span>

<span data-ttu-id="93083-105">Este tópico não é atual.</span><span class="sxs-lookup"><span data-stu-id="93083-105">This topic is not current.</span></span> <span data-ttu-id="93083-106">Para obter as informações mais atuais, consulte a [especificação do esquema de impressão](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="93083-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="93083-107">Especifica o perfil de cor de origem inserido.</span><span class="sxs-lookup"><span data-stu-id="93083-107">Specifies the embedded source color profile.</span></span>

-   [<span data-ttu-id="93083-108">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="93083-108">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="93083-109">Conteúdo da estrutura</span><span class="sxs-lookup"><span data-stu-id="93083-109">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="93083-110">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="93083-110">Element Information</span></span>



| <span data-ttu-id="93083-111">Nome</span><span class="sxs-lookup"><span data-stu-id="93083-111">Name</span></span> | <span data-ttu-id="93083-112">Valor</span><span class="sxs-lookup"><span data-stu-id="93083-112">Value</span></span> |
|----------------------------|-----------------------------------------------------|
| <span data-ttu-id="93083-113">Tipo de elemento</span><span class="sxs-lookup"><span data-stu-id="93083-113">Element Type</span></span> <br/>   | <span data-ttu-id="93083-114">ParameterDef</span><span class="sxs-lookup"><span data-stu-id="93083-114">ParameterDef</span></span><br/>                             |
| <span data-ttu-id="93083-115">Prefixo de escopo</span><span class="sxs-lookup"><span data-stu-id="93083-115">Scoping Prefix</span></span> <br/> | <span data-ttu-id="93083-116">?</span><span class="sxs-lookup"><span data-stu-id="93083-116">Page</span></span><br/>                                     |
| <span data-ttu-id="93083-117">Observações</span><span class="sxs-lookup"><span data-stu-id="93083-117">Notes</span></span> <br/>          | <span data-ttu-id="93083-118">Vinculado ao elemento PageSourceColorProfile</span><span class="sxs-lookup"><span data-stu-id="93083-118">Linked to PageSourceColorProfile element</span></span><br/> |



 

## <a name="structure-content"></a><span data-ttu-id="93083-119">Conteúdo da estrutura</span><span class="sxs-lookup"><span data-stu-id="93083-119">Structure Content</span></span>

<span data-ttu-id="93083-120">A estrutura XML desse elemento é:</span><span class="sxs-lookup"><span data-stu-id="93083-120">The XML structure of this element is:</span></span>

``` syntax
<psf:ParameterDef name="psk:PageSourceColorProfileEmbedded">
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

## <a name="structure-properties"></a><span data-ttu-id="93083-121">Propriedades da estrutura</span><span class="sxs-lookup"><span data-stu-id="93083-121">Structure Properties</span></span>

<span data-ttu-id="93083-122">A tabela a seguir descreve as características das variáveis definidas na estrutura XML.</span><span class="sxs-lookup"><span data-stu-id="93083-122">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="93083-123">Propriedade</span><span class="sxs-lookup"><span data-stu-id="93083-123">Property</span></span>                | <span data-ttu-id="93083-124">xsi:type</span><span class="sxs-lookup"><span data-stu-id="93083-124">xsi:type</span></span>           | <span data-ttu-id="93083-125">Valor</span><span class="sxs-lookup"><span data-stu-id="93083-125">Value</span></span>                      |
|-------------------------|--------------------|----------------------------|
| <span data-ttu-id="93083-126">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="93083-126">DataType</span></span><br/>     | <span data-ttu-id="93083-127">string</span><span class="sxs-lookup"><span data-stu-id="93083-127">string</span></span><br/>  | <span data-ttu-id="93083-128">xs:string</span><span class="sxs-lookup"><span data-stu-id="93083-128">xs:string</span></span><br/>       |
| <span data-ttu-id="93083-129">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="93083-129">DefaultValue</span></span><br/> | <span data-ttu-id="93083-130">string</span><span class="sxs-lookup"><span data-stu-id="93083-130">string</span></span><br/>  | <span data-ttu-id="93083-131">não definido</span><span class="sxs-lookup"><span data-stu-id="93083-131">undefined</span></span><br/>       |
| <span data-ttu-id="93083-132">MaxLength</span><span class="sxs-lookup"><span data-stu-id="93083-132">MaxLength</span></span><br/>    | <span data-ttu-id="93083-133">Número inteiro</span><span class="sxs-lookup"><span data-stu-id="93083-133">integer</span></span><br/> | <span data-ttu-id="93083-134">não definido</span><span class="sxs-lookup"><span data-stu-id="93083-134">undefined</span></span><br/>       |
| <span data-ttu-id="93083-135">MinLength</span><span class="sxs-lookup"><span data-stu-id="93083-135">MinLength</span></span><br/>    | <span data-ttu-id="93083-136">integer</span><span class="sxs-lookup"><span data-stu-id="93083-136">integer</span></span><br/> | <span data-ttu-id="93083-137">1</span><span class="sxs-lookup"><span data-stu-id="93083-137">1</span></span><br/>               |
| <span data-ttu-id="93083-138">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="93083-138">Mandatory</span></span><br/>    | <span data-ttu-id="93083-139">string</span><span class="sxs-lookup"><span data-stu-id="93083-139">string</span></span><br/>  | <span data-ttu-id="93083-140">PSK: condicional</span><span class="sxs-lookup"><span data-stu-id="93083-140">psk:Conditional</span></span><br/> |
| <span data-ttu-id="93083-141">UnitType</span><span class="sxs-lookup"><span data-stu-id="93083-141">UnitType</span></span><br/>     | <span data-ttu-id="93083-142">string</span><span class="sxs-lookup"><span data-stu-id="93083-142">string</span></span><br/>  | <span data-ttu-id="93083-143">characters</span><span class="sxs-lookup"><span data-stu-id="93083-143">characters</span></span><br/>      |



 

## <a name="related-topics"></a><span data-ttu-id="93083-144">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="93083-144">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="93083-145">Especificação de esquema de impressão</span><span class="sxs-lookup"><span data-stu-id="93083-145">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




