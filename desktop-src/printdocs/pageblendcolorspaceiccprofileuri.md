---
description: Leia sobre o parâmetro PageBlendColorSpaceICCProfileURI. Este tópico não é atual. Para obter as informações mais atuais, consulte a Especificação de Esquema de Impressão.
ms.assetid: 05924c7d-e074-4835-b42c-53c77dc1bbb5
title: PageBlendColorSpaceICCProfileURI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 50db89757737ff5aa6a1358af418ee33809b960e
ms.sourcegitcommit: 998d50f6def8a25850fc113fc8a2df903c829c5e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/09/2021
ms.locfileid: "113549314"
---
# <a name="pageblendcolorspaceiccprofileuri"></a><span data-ttu-id="a6a90-105">PageBlendColorSpaceICCProfileURI</span><span class="sxs-lookup"><span data-stu-id="a6a90-105">PageBlendColorSpaceICCProfileURI</span></span>

<span data-ttu-id="a6a90-106">Este tópico não é atual.</span><span class="sxs-lookup"><span data-stu-id="a6a90-106">This topic is not current.</span></span> <span data-ttu-id="a6a90-107">Para obter as informações mais atuais, consulte a [Especificação de Esquema de Impressão](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="a6a90-107">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="a6a90-108">Especifica uma referência de URI relativa a um perfil ICC que define o espaço de cores que DEVE ser usado para mesclagem.</span><span class="sxs-lookup"><span data-stu-id="a6a90-108">Specifies a relative URI reference to an ICC profile defining the color space that SHOULD be used for blending.</span></span> <span data-ttu-id="a6a90-109">O <Uri> é um nome de parte absoluto em relação à raiz do \_ pacote.</span><span class="sxs-lookup"><span data-stu-id="a6a90-109">The <Uri> is an absolute part\_name relative to the package root.</span></span>

-   [<span data-ttu-id="a6a90-110">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="a6a90-110">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="a6a90-111">Conteúdo da estrutura</span><span class="sxs-lookup"><span data-stu-id="a6a90-111">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="a6a90-112">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="a6a90-112">Element Information</span></span>



| <span data-ttu-id="a6a90-113">Nome</span><span class="sxs-lookup"><span data-stu-id="a6a90-113">Name</span></span> | <span data-ttu-id="a6a90-114">Valor</span><span class="sxs-lookup"><span data-stu-id="a6a90-114">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a6a90-115">Tipo de elemento</span><span class="sxs-lookup"><span data-stu-id="a6a90-115">Element Type</span></span> <br/>   | <span data-ttu-id="a6a90-116">ParameterDef</span><span class="sxs-lookup"><span data-stu-id="a6a90-116">ParameterDef</span></span><br/>                                                                                                                |
| <span data-ttu-id="a6a90-117">Prefixo de definição de scoping</span><span class="sxs-lookup"><span data-stu-id="a6a90-117">Scoping Prefix</span></span> <br/> | <span data-ttu-id="a6a90-118">Página</span><span class="sxs-lookup"><span data-stu-id="a6a90-118">Page</span></span><br/>                                                                                                                        |
| <span data-ttu-id="a6a90-119">Observações</span><span class="sxs-lookup"><span data-stu-id="a6a90-119">Notes</span></span> <br/>          | <span data-ttu-id="a6a90-120">Isso se aplica somente a documentos XPS e não deve ser usado em PrintTickets arbitrários.</span><span class="sxs-lookup"><span data-stu-id="a6a90-120">This applies to XPS Documents only and should not be used in arbitrary PrintTickets.</span></span> <span data-ttu-id="a6a90-121">Vinculado ao elemento PageBlendColorSpace.</span><span class="sxs-lookup"><span data-stu-id="a6a90-121">Linked to PageBlendColorSpace element.</span></span><br/> |



 

## <a name="structure-content"></a><span data-ttu-id="a6a90-122">Conteúdo da estrutura</span><span class="sxs-lookup"><span data-stu-id="a6a90-122">Structure Content</span></span>

<span data-ttu-id="a6a90-123">A estrutura XML desse elemento é:</span><span class="sxs-lookup"><span data-stu-id="a6a90-123">The XML structure of this element is:</span></span>

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

## <a name="structure-properties"></a><span data-ttu-id="a6a90-124">Propriedades da estrutura</span><span class="sxs-lookup"><span data-stu-id="a6a90-124">Structure Properties</span></span>

<span data-ttu-id="a6a90-125">A tabela a seguir descreve as características das variáveis definidas na estrutura XML.</span><span class="sxs-lookup"><span data-stu-id="a6a90-125">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="a6a90-126">Propriedade</span><span class="sxs-lookup"><span data-stu-id="a6a90-126">Property</span></span>                | <span data-ttu-id="a6a90-127">xsi:type</span><span class="sxs-lookup"><span data-stu-id="a6a90-127">xsi:type</span></span>           | <span data-ttu-id="a6a90-128">Valor</span><span class="sxs-lookup"><span data-stu-id="a6a90-128">Value</span></span>                      |
|-------------------------|--------------------|----------------------------|
| <span data-ttu-id="a6a90-129">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="a6a90-129">DataType</span></span><br/>     | <span data-ttu-id="a6a90-130">string</span><span class="sxs-lookup"><span data-stu-id="a6a90-130">string</span></span><br/>  | <span data-ttu-id="a6a90-131">xs:string</span><span class="sxs-lookup"><span data-stu-id="a6a90-131">xs:string</span></span><br/>       |
| <span data-ttu-id="a6a90-132">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="a6a90-132">DefaultValue</span></span><br/> | <span data-ttu-id="a6a90-133">string</span><span class="sxs-lookup"><span data-stu-id="a6a90-133">string</span></span><br/>  | <span data-ttu-id="a6a90-134">não definido</span><span class="sxs-lookup"><span data-stu-id="a6a90-134">undefined</span></span><br/>       |
| <span data-ttu-id="a6a90-135">MaxLength</span><span class="sxs-lookup"><span data-stu-id="a6a90-135">MaxLength</span></span><br/>    | <span data-ttu-id="a6a90-136">Número inteiro</span><span class="sxs-lookup"><span data-stu-id="a6a90-136">integer</span></span><br/> | <span data-ttu-id="a6a90-137">não definido</span><span class="sxs-lookup"><span data-stu-id="a6a90-137">undefined</span></span><br/>       |
| <span data-ttu-id="a6a90-138">Minlength</span><span class="sxs-lookup"><span data-stu-id="a6a90-138">MinLength</span></span><br/>    | <span data-ttu-id="a6a90-139">integer</span><span class="sxs-lookup"><span data-stu-id="a6a90-139">integer</span></span><br/> | <span data-ttu-id="a6a90-140">1</span><span class="sxs-lookup"><span data-stu-id="a6a90-140">1</span></span><br/>               |
| <span data-ttu-id="a6a90-141">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="a6a90-141">Mandatory</span></span><br/>    | <span data-ttu-id="a6a90-142">string</span><span class="sxs-lookup"><span data-stu-id="a6a90-142">string</span></span><br/>  | <span data-ttu-id="a6a90-143">psk:Conditional</span><span class="sxs-lookup"><span data-stu-id="a6a90-143">psk:Conditional</span></span><br/> |
| <span data-ttu-id="a6a90-144">Unittype</span><span class="sxs-lookup"><span data-stu-id="a6a90-144">UnitType</span></span><br/>     | <span data-ttu-id="a6a90-145">string</span><span class="sxs-lookup"><span data-stu-id="a6a90-145">string</span></span><br/>  | <span data-ttu-id="a6a90-146">characters</span><span class="sxs-lookup"><span data-stu-id="a6a90-146">characters</span></span><br/>      |



 

## <a name="related-topics"></a><span data-ttu-id="a6a90-147">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="a6a90-147">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a6a90-148">Especificação de esquema de impressão</span><span class="sxs-lookup"><span data-stu-id="a6a90-148">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




