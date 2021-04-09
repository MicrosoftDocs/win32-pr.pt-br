---
description: Este tópico não é atual. Para obter as informações mais atuais, consulte a especificação do esquema de impressão.
ms.assetid: 05924c7d-e074-4835-b42c-53c77dc1bbb5
title: PageBlendColorSpaceICCProfileURI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e1f3a6143bd934ebcb75c3e5455a30c7365f1a89
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/05/2021
ms.locfileid: "104011981"
---
# <a name="pageblendcolorspaceiccprofileuri"></a><span data-ttu-id="a190c-104">PageBlendColorSpaceICCProfileURI</span><span class="sxs-lookup"><span data-stu-id="a190c-104">PageBlendColorSpaceICCProfileURI</span></span>

<span data-ttu-id="a190c-105">Este tópico não é atual.</span><span class="sxs-lookup"><span data-stu-id="a190c-105">This topic is not current.</span></span> <span data-ttu-id="a190c-106">Para obter as informações mais atuais, consulte a [especificação do esquema de impressão](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="a190c-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="a190c-107">Especifica uma referência de URI relativa a um perfil ICC que define o espaço de cores que deve ser usado para mesclagem.</span><span class="sxs-lookup"><span data-stu-id="a190c-107">Specifies a relative URI reference to an ICC profile defining the color space that SHOULD be used for blending.</span></span> <span data-ttu-id="a190c-108">O <Uri> é um nome de parte absoluto \_ relativo à raiz do pacote.</span><span class="sxs-lookup"><span data-stu-id="a190c-108">The <Uri> is an absolute part\_name relative to the package root.</span></span>

-   [<span data-ttu-id="a190c-109">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="a190c-109">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="a190c-110">Conteúdo da estrutura</span><span class="sxs-lookup"><span data-stu-id="a190c-110">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="a190c-111">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="a190c-111">Element Information</span></span>



| <span data-ttu-id="a190c-112">Nome</span><span class="sxs-lookup"><span data-stu-id="a190c-112">Name</span></span>                       |                                                                                                                                        |
|----------------------------|----------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a190c-113">Tipo de elemento</span><span class="sxs-lookup"><span data-stu-id="a190c-113">Element Type</span></span> <br/>   | <span data-ttu-id="a190c-114">ParameterDef</span><span class="sxs-lookup"><span data-stu-id="a190c-114">ParameterDef</span></span><br/>                                                                                                                |
| <span data-ttu-id="a190c-115">Prefixo de escopo</span><span class="sxs-lookup"><span data-stu-id="a190c-115">Scoping Prefix</span></span> <br/> | <span data-ttu-id="a190c-116">?</span><span class="sxs-lookup"><span data-stu-id="a190c-116">Page</span></span><br/>                                                                                                                        |
| <span data-ttu-id="a190c-117">Observações</span><span class="sxs-lookup"><span data-stu-id="a190c-117">Notes</span></span> <br/>          | <span data-ttu-id="a190c-118">Isso se aplica somente a documentos XPS e não deve ser usado em PrintTickets arbitrários.</span><span class="sxs-lookup"><span data-stu-id="a190c-118">This applies to XPS Documents only and should not be used in arbitrary PrintTickets.</span></span> <span data-ttu-id="a190c-119">Vinculado ao elemento PageBlendColorSpace.</span><span class="sxs-lookup"><span data-stu-id="a190c-119">Linked to PageBlendColorSpace element.</span></span><br/> |



 

## <a name="structure-content"></a><span data-ttu-id="a190c-120">Conteúdo da estrutura</span><span class="sxs-lookup"><span data-stu-id="a190c-120">Structure Content</span></span>

<span data-ttu-id="a190c-121">A estrutura XML desse elemento é:</span><span class="sxs-lookup"><span data-stu-id="a190c-121">The XML structure of this element is:</span></span>

``` syntax
<psf:ParameterDef name="psk:PageBlendColorSpaceICCProfileURI">
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

## <a name="structure-properties"></a><span data-ttu-id="a190c-122">Propriedades da estrutura</span><span class="sxs-lookup"><span data-stu-id="a190c-122">Structure Properties</span></span>

<span data-ttu-id="a190c-123">A tabela a seguir descreve as características das variáveis definidas na estrutura XML.</span><span class="sxs-lookup"><span data-stu-id="a190c-123">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="a190c-124">Propriedade</span><span class="sxs-lookup"><span data-stu-id="a190c-124">Property</span></span>                | <span data-ttu-id="a190c-125">xsi:type</span><span class="sxs-lookup"><span data-stu-id="a190c-125">xsi:type</span></span>           | <span data-ttu-id="a190c-126">Valor</span><span class="sxs-lookup"><span data-stu-id="a190c-126">Value</span></span>                      |
|-------------------------|--------------------|----------------------------|
| <span data-ttu-id="a190c-127">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="a190c-127">DataType</span></span><br/>     | <span data-ttu-id="a190c-128">string</span><span class="sxs-lookup"><span data-stu-id="a190c-128">string</span></span><br/>  | <span data-ttu-id="a190c-129">xs:string</span><span class="sxs-lookup"><span data-stu-id="a190c-129">xs:string</span></span><br/>       |
| <span data-ttu-id="a190c-130">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="a190c-130">DefaultValue</span></span><br/> | <span data-ttu-id="a190c-131">string</span><span class="sxs-lookup"><span data-stu-id="a190c-131">string</span></span><br/>  | <span data-ttu-id="a190c-132">não definido</span><span class="sxs-lookup"><span data-stu-id="a190c-132">undefined</span></span><br/>       |
| <span data-ttu-id="a190c-133">MaxLength</span><span class="sxs-lookup"><span data-stu-id="a190c-133">MaxLength</span></span><br/>    | <span data-ttu-id="a190c-134">Número inteiro</span><span class="sxs-lookup"><span data-stu-id="a190c-134">integer</span></span><br/> | <span data-ttu-id="a190c-135">não definido</span><span class="sxs-lookup"><span data-stu-id="a190c-135">undefined</span></span><br/>       |
| <span data-ttu-id="a190c-136">MinLength</span><span class="sxs-lookup"><span data-stu-id="a190c-136">MinLength</span></span><br/>    | <span data-ttu-id="a190c-137">integer</span><span class="sxs-lookup"><span data-stu-id="a190c-137">integer</span></span><br/> | <span data-ttu-id="a190c-138">1</span><span class="sxs-lookup"><span data-stu-id="a190c-138">1</span></span><br/>               |
| <span data-ttu-id="a190c-139">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="a190c-139">Mandatory</span></span><br/>    | <span data-ttu-id="a190c-140">string</span><span class="sxs-lookup"><span data-stu-id="a190c-140">string</span></span><br/>  | <span data-ttu-id="a190c-141">PSK: condicional</span><span class="sxs-lookup"><span data-stu-id="a190c-141">psk:Conditional</span></span><br/> |
| <span data-ttu-id="a190c-142">UnitType</span><span class="sxs-lookup"><span data-stu-id="a190c-142">UnitType</span></span><br/>     | <span data-ttu-id="a190c-143">string</span><span class="sxs-lookup"><span data-stu-id="a190c-143">string</span></span><br/>  | <span data-ttu-id="a190c-144">characters</span><span class="sxs-lookup"><span data-stu-id="a190c-144">characters</span></span><br/>      |



 

## <a name="related-topics"></a><span data-ttu-id="a190c-145">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="a190c-145">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a190c-146">Especificação de esquema de impressão</span><span class="sxs-lookup"><span data-stu-id="a190c-146">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




