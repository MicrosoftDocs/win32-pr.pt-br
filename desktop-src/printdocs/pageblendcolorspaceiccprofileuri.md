---
description: Este tópico não é atual. Para obter as informações mais atuais, consulte a especificação do esquema de impressão.
ms.assetid: 05924c7d-e074-4835-b42c-53c77dc1bbb5
title: PageBlendColorSpaceICCProfileURI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2cbf1233e172a81053baee0abe1e21d79064045a
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/26/2021
ms.locfileid: "107997693"
---
# <a name="pageblendcolorspaceiccprofileuri"></a><span data-ttu-id="52f23-104">PageBlendColorSpaceICCProfileURI</span><span class="sxs-lookup"><span data-stu-id="52f23-104">PageBlendColorSpaceICCProfileURI</span></span>

<span data-ttu-id="52f23-105">Este tópico não é atual.</span><span class="sxs-lookup"><span data-stu-id="52f23-105">This topic is not current.</span></span> <span data-ttu-id="52f23-106">Para obter as informações mais atuais, consulte a [especificação do esquema de impressão](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="52f23-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="52f23-107">Especifica uma referência de URI relativa a um perfil ICC que define o espaço de cores que deve ser usado para mesclagem.</span><span class="sxs-lookup"><span data-stu-id="52f23-107">Specifies a relative URI reference to an ICC profile defining the color space that SHOULD be used for blending.</span></span> <span data-ttu-id="52f23-108">O <Uri> é um nome de parte absoluto \_ relativo à raiz do pacote.</span><span class="sxs-lookup"><span data-stu-id="52f23-108">The <Uri> is an absolute part\_name relative to the package root.</span></span>

-   [<span data-ttu-id="52f23-109">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="52f23-109">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="52f23-110">Conteúdo da estrutura</span><span class="sxs-lookup"><span data-stu-id="52f23-110">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="52f23-111">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="52f23-111">Element Information</span></span>



| <span data-ttu-id="52f23-112">Nome</span><span class="sxs-lookup"><span data-stu-id="52f23-112">Name</span></span> | <span data-ttu-id="52f23-113">Valor</span><span class="sxs-lookup"><span data-stu-id="52f23-113">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="52f23-114">Tipo de elemento</span><span class="sxs-lookup"><span data-stu-id="52f23-114">Element Type</span></span> <br/>   | <span data-ttu-id="52f23-115">ParameterDef</span><span class="sxs-lookup"><span data-stu-id="52f23-115">ParameterDef</span></span><br/>                                                                                                                |
| <span data-ttu-id="52f23-116">Prefixo de escopo</span><span class="sxs-lookup"><span data-stu-id="52f23-116">Scoping Prefix</span></span> <br/> | <span data-ttu-id="52f23-117">?</span><span class="sxs-lookup"><span data-stu-id="52f23-117">Page</span></span><br/>                                                                                                                        |
| <span data-ttu-id="52f23-118">Observações</span><span class="sxs-lookup"><span data-stu-id="52f23-118">Notes</span></span> <br/>          | <span data-ttu-id="52f23-119">Isso se aplica somente a documentos XPS e não deve ser usado em PrintTickets arbitrários.</span><span class="sxs-lookup"><span data-stu-id="52f23-119">This applies to XPS Documents only and should not be used in arbitrary PrintTickets.</span></span> <span data-ttu-id="52f23-120">Vinculado ao elemento PageBlendColorSpace.</span><span class="sxs-lookup"><span data-stu-id="52f23-120">Linked to PageBlendColorSpace element.</span></span><br/> |



 

## <a name="structure-content"></a><span data-ttu-id="52f23-121">Conteúdo da estrutura</span><span class="sxs-lookup"><span data-stu-id="52f23-121">Structure Content</span></span>

<span data-ttu-id="52f23-122">A estrutura XML desse elemento é:</span><span class="sxs-lookup"><span data-stu-id="52f23-122">The XML structure of this element is:</span></span>

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

## <a name="structure-properties"></a><span data-ttu-id="52f23-123">Propriedades da estrutura</span><span class="sxs-lookup"><span data-stu-id="52f23-123">Structure Properties</span></span>

<span data-ttu-id="52f23-124">A tabela a seguir descreve as características das variáveis definidas na estrutura XML.</span><span class="sxs-lookup"><span data-stu-id="52f23-124">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="52f23-125">Propriedade</span><span class="sxs-lookup"><span data-stu-id="52f23-125">Property</span></span>                | <span data-ttu-id="52f23-126">xsi:type</span><span class="sxs-lookup"><span data-stu-id="52f23-126">xsi:type</span></span>           | <span data-ttu-id="52f23-127">Valor</span><span class="sxs-lookup"><span data-stu-id="52f23-127">Value</span></span>                      |
|-------------------------|--------------------|----------------------------|
| <span data-ttu-id="52f23-128">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="52f23-128">DataType</span></span><br/>     | <span data-ttu-id="52f23-129">string</span><span class="sxs-lookup"><span data-stu-id="52f23-129">string</span></span><br/>  | <span data-ttu-id="52f23-130">xs:string</span><span class="sxs-lookup"><span data-stu-id="52f23-130">xs:string</span></span><br/>       |
| <span data-ttu-id="52f23-131">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="52f23-131">DefaultValue</span></span><br/> | <span data-ttu-id="52f23-132">string</span><span class="sxs-lookup"><span data-stu-id="52f23-132">string</span></span><br/>  | <span data-ttu-id="52f23-133">não definido</span><span class="sxs-lookup"><span data-stu-id="52f23-133">undefined</span></span><br/>       |
| <span data-ttu-id="52f23-134">MaxLength</span><span class="sxs-lookup"><span data-stu-id="52f23-134">MaxLength</span></span><br/>    | <span data-ttu-id="52f23-135">Número inteiro</span><span class="sxs-lookup"><span data-stu-id="52f23-135">integer</span></span><br/> | <span data-ttu-id="52f23-136">não definido</span><span class="sxs-lookup"><span data-stu-id="52f23-136">undefined</span></span><br/>       |
| <span data-ttu-id="52f23-137">MinLength</span><span class="sxs-lookup"><span data-stu-id="52f23-137">MinLength</span></span><br/>    | <span data-ttu-id="52f23-138">integer</span><span class="sxs-lookup"><span data-stu-id="52f23-138">integer</span></span><br/> | <span data-ttu-id="52f23-139">1</span><span class="sxs-lookup"><span data-stu-id="52f23-139">1</span></span><br/>               |
| <span data-ttu-id="52f23-140">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="52f23-140">Mandatory</span></span><br/>    | <span data-ttu-id="52f23-141">string</span><span class="sxs-lookup"><span data-stu-id="52f23-141">string</span></span><br/>  | <span data-ttu-id="52f23-142">PSK: condicional</span><span class="sxs-lookup"><span data-stu-id="52f23-142">psk:Conditional</span></span><br/> |
| <span data-ttu-id="52f23-143">UnitType</span><span class="sxs-lookup"><span data-stu-id="52f23-143">UnitType</span></span><br/>     | <span data-ttu-id="52f23-144">string</span><span class="sxs-lookup"><span data-stu-id="52f23-144">string</span></span><br/>  | <span data-ttu-id="52f23-145">characters</span><span class="sxs-lookup"><span data-stu-id="52f23-145">characters</span></span><br/>      |



 

## <a name="related-topics"></a><span data-ttu-id="52f23-146">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="52f23-146">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="52f23-147">Especificação de esquema de impressão</span><span class="sxs-lookup"><span data-stu-id="52f23-147">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




