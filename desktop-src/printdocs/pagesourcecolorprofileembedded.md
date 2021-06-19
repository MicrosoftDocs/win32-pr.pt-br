---
description: Saiba mais sobre o parâmetro PageSourceColorProfileEmbedded. Este tópico não é atual. Para obter as informações mais atuais, consulte a especificação do esquema de impressão.
ms.assetid: 38411802-2b2e-441c-b3a6-334d87b11b5d
title: PageSourceColorProfileEmbedded
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0633fa061601c1d575f174ab5572582efdf9a89e
ms.sourcegitcommit: 91530c19d26ba4c57a6af1f37b57f211f580464e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/19/2021
ms.locfileid: "112395631"
---
# <a name="pagesourcecolorprofileembedded"></a><span data-ttu-id="dcc06-105">PageSourceColorProfileEmbedded</span><span class="sxs-lookup"><span data-stu-id="dcc06-105">PageSourceColorProfileEmbedded</span></span>

<span data-ttu-id="dcc06-106">Este tópico não é atual.</span><span class="sxs-lookup"><span data-stu-id="dcc06-106">This topic is not current.</span></span> <span data-ttu-id="dcc06-107">Para obter as informações mais atuais, consulte a [especificação do esquema de impressão](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="dcc06-107">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="dcc06-108">Especifica o perfil de cor de origem inserido.</span><span class="sxs-lookup"><span data-stu-id="dcc06-108">Specifies the embedded source color profile.</span></span>

-   [<span data-ttu-id="dcc06-109">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="dcc06-109">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="dcc06-110">Conteúdo da estrutura</span><span class="sxs-lookup"><span data-stu-id="dcc06-110">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="dcc06-111">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="dcc06-111">Element Information</span></span>



| <span data-ttu-id="dcc06-112">Name</span><span class="sxs-lookup"><span data-stu-id="dcc06-112">Name</span></span> | <span data-ttu-id="dcc06-113">Valor</span><span class="sxs-lookup"><span data-stu-id="dcc06-113">Value</span></span> |
|----------------------------|-----------------------------------------------------|
| <span data-ttu-id="dcc06-114">Tipo de elemento</span><span class="sxs-lookup"><span data-stu-id="dcc06-114">Element Type</span></span> <br/>   | <span data-ttu-id="dcc06-115">ParameterDef</span><span class="sxs-lookup"><span data-stu-id="dcc06-115">ParameterDef</span></span><br/>                             |
| <span data-ttu-id="dcc06-116">Prefixo de escopo</span><span class="sxs-lookup"><span data-stu-id="dcc06-116">Scoping Prefix</span></span> <br/> | <span data-ttu-id="dcc06-117">?</span><span class="sxs-lookup"><span data-stu-id="dcc06-117">Page</span></span><br/>                                     |
| <span data-ttu-id="dcc06-118">Observações</span><span class="sxs-lookup"><span data-stu-id="dcc06-118">Notes</span></span> <br/>          | <span data-ttu-id="dcc06-119">Vinculado ao elemento PageSourceColorProfile</span><span class="sxs-lookup"><span data-stu-id="dcc06-119">Linked to PageSourceColorProfile element</span></span><br/> |



 

## <a name="structure-content"></a><span data-ttu-id="dcc06-120">Conteúdo da estrutura</span><span class="sxs-lookup"><span data-stu-id="dcc06-120">Structure Content</span></span>

<span data-ttu-id="dcc06-121">A estrutura XML desse elemento é:</span><span class="sxs-lookup"><span data-stu-id="dcc06-121">The XML structure of this element is:</span></span>

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

## <a name="structure-properties"></a><span data-ttu-id="dcc06-122">Propriedades da estrutura</span><span class="sxs-lookup"><span data-stu-id="dcc06-122">Structure Properties</span></span>

<span data-ttu-id="dcc06-123">A tabela a seguir descreve as características das variáveis definidas na estrutura XML.</span><span class="sxs-lookup"><span data-stu-id="dcc06-123">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="dcc06-124">Propriedade</span><span class="sxs-lookup"><span data-stu-id="dcc06-124">Property</span></span>                | <span data-ttu-id="dcc06-125">xsi:type</span><span class="sxs-lookup"><span data-stu-id="dcc06-125">xsi:type</span></span>           | <span data-ttu-id="dcc06-126">Valor</span><span class="sxs-lookup"><span data-stu-id="dcc06-126">Value</span></span>                      |
|-------------------------|--------------------|----------------------------|
| <span data-ttu-id="dcc06-127">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="dcc06-127">DataType</span></span><br/>     | <span data-ttu-id="dcc06-128">string</span><span class="sxs-lookup"><span data-stu-id="dcc06-128">string</span></span><br/>  | <span data-ttu-id="dcc06-129">xs:string</span><span class="sxs-lookup"><span data-stu-id="dcc06-129">xs:string</span></span><br/>       |
| <span data-ttu-id="dcc06-130">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="dcc06-130">DefaultValue</span></span><br/> | <span data-ttu-id="dcc06-131">string</span><span class="sxs-lookup"><span data-stu-id="dcc06-131">string</span></span><br/>  | <span data-ttu-id="dcc06-132">não definido</span><span class="sxs-lookup"><span data-stu-id="dcc06-132">undefined</span></span><br/>       |
| <span data-ttu-id="dcc06-133">MaxLength</span><span class="sxs-lookup"><span data-stu-id="dcc06-133">MaxLength</span></span><br/>    | <span data-ttu-id="dcc06-134">Número inteiro</span><span class="sxs-lookup"><span data-stu-id="dcc06-134">integer</span></span><br/> | <span data-ttu-id="dcc06-135">não definido</span><span class="sxs-lookup"><span data-stu-id="dcc06-135">undefined</span></span><br/>       |
| <span data-ttu-id="dcc06-136">MinLength</span><span class="sxs-lookup"><span data-stu-id="dcc06-136">MinLength</span></span><br/>    | <span data-ttu-id="dcc06-137">integer</span><span class="sxs-lookup"><span data-stu-id="dcc06-137">integer</span></span><br/> | <span data-ttu-id="dcc06-138">1</span><span class="sxs-lookup"><span data-stu-id="dcc06-138">1</span></span><br/>               |
| <span data-ttu-id="dcc06-139">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="dcc06-139">Mandatory</span></span><br/>    | <span data-ttu-id="dcc06-140">string</span><span class="sxs-lookup"><span data-stu-id="dcc06-140">string</span></span><br/>  | <span data-ttu-id="dcc06-141">PSK: condicional</span><span class="sxs-lookup"><span data-stu-id="dcc06-141">psk:Conditional</span></span><br/> |
| <span data-ttu-id="dcc06-142">UnitType</span><span class="sxs-lookup"><span data-stu-id="dcc06-142">UnitType</span></span><br/>     | <span data-ttu-id="dcc06-143">string</span><span class="sxs-lookup"><span data-stu-id="dcc06-143">string</span></span><br/>  | <span data-ttu-id="dcc06-144">characters</span><span class="sxs-lookup"><span data-stu-id="dcc06-144">characters</span></span><br/>      |



 

## <a name="related-topics"></a><span data-ttu-id="dcc06-145">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="dcc06-145">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="dcc06-146">Especificação de esquema de impressão</span><span class="sxs-lookup"><span data-stu-id="dcc06-146">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




