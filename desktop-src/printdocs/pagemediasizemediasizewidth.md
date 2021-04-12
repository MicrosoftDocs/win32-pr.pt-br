---
description: Este tópico não é atual. Para obter as informações mais atuais, consulte a especificação do esquema de impressão.
ms.assetid: 22e4a6e9-4d18-4fff-873c-27ba59a79222
title: PageMediaSizeMediaSizeWidth
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bb1f72e667f3de3bce86beb1c65c5fde4ebc8669
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/05/2021
ms.locfileid: "104298006"
---
# <a name="pagemediasizemediasizewidth"></a><span data-ttu-id="0e06d-104">PageMediaSizeMediaSizeWidth</span><span class="sxs-lookup"><span data-stu-id="0e06d-104">PageMediaSizeMediaSizeWidth</span></span>

<span data-ttu-id="0e06d-105">Este tópico não é atual.</span><span class="sxs-lookup"><span data-stu-id="0e06d-105">This topic is not current.</span></span> <span data-ttu-id="0e06d-106">Para obter as informações mais atuais, consulte a [especificação do esquema de impressão](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="0e06d-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="0e06d-107">Especifica a direção da dimensão MediaSizeWidth para a opção MediaSize personalizada.</span><span class="sxs-lookup"><span data-stu-id="0e06d-107">Specifies the dimension MediaSizeWidth direction for the Custom MediaSize option.</span></span>

-   [<span data-ttu-id="0e06d-108">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="0e06d-108">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="0e06d-109">Conteúdo da estrutura</span><span class="sxs-lookup"><span data-stu-id="0e06d-109">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="0e06d-110">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="0e06d-110">Element Information</span></span>



| <span data-ttu-id="0e06d-111">Nome</span><span class="sxs-lookup"><span data-stu-id="0e06d-111">Name</span></span>                       |                                                           |
|----------------------------|-----------------------------------------------------------|
| <span data-ttu-id="0e06d-112">Tipo de elemento</span><span class="sxs-lookup"><span data-stu-id="0e06d-112">Element Type</span></span> <br/>   | <span data-ttu-id="0e06d-113">ParameterDef</span><span class="sxs-lookup"><span data-stu-id="0e06d-113">ParameterDef</span></span><br/>                                   |
| <span data-ttu-id="0e06d-114">Prefixo de escopo</span><span class="sxs-lookup"><span data-stu-id="0e06d-114">Scoping Prefix</span></span> <br/> | <span data-ttu-id="0e06d-115">?</span><span class="sxs-lookup"><span data-stu-id="0e06d-115">Page</span></span><br/>                                           |
| <span data-ttu-id="0e06d-116">Observações</span><span class="sxs-lookup"><span data-stu-id="0e06d-116">Notes</span></span> <br/>          | <span data-ttu-id="0e06d-117">Vinculado ao elemento PageMediaSize, opção personalizada</span><span class="sxs-lookup"><span data-stu-id="0e06d-117">Linked to PageMediaSize element, Custom option</span></span><br/> |



 

## <a name="structure-content"></a><span data-ttu-id="0e06d-118">Conteúdo da estrutura</span><span class="sxs-lookup"><span data-stu-id="0e06d-118">Structure Content</span></span>

<span data-ttu-id="0e06d-119">A estrutura XML desse elemento é:</span><span class="sxs-lookup"><span data-stu-id="0e06d-119">The XML structure of this element is:</span></span>

``` syntax
<psf:ParameterDef name="psk:PageMediaSizeMediaSizeWidth">
  <psf:Property name="psf:DataType">
    <psf:Value xsi:type="xs:string">xs:integer</psf:Value>
  </psf:Property>
  <psf:Property name="psf:DefaultValue">
    <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
  </psf:Property>
  <psf:Property name="psf:MaxValue">
    <psf:Value xsi:type="xs:integer">_Undefined</psf:Value>
  </psf:Property>
  <psf:Property name="psf:MinValue">
    <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
  </psf:Property>
  <psf:Property name="psf:Multiple">
    <psf:Value xsi:type="xs:integer">1</psf:Value>
  </psf:Property>
  <psf:Property name="psf:Mandatory">
    <psf:Value xsi:type="xs:string">psk:Conditional</psf:Value>
  </psf:Property>
  <psf:Property name="psf:UnitType">
    <psf:Value xsi:type="xs:string">microns</psf:Value>
  </psf:Property>
</psf:ParameterDef>
      
```

## <a name="structure-properties"></a><span data-ttu-id="0e06d-120">Propriedades da estrutura</span><span class="sxs-lookup"><span data-stu-id="0e06d-120">Structure Properties</span></span>

<span data-ttu-id="0e06d-121">A tabela a seguir descreve as características das variáveis definidas na estrutura XML.</span><span class="sxs-lookup"><span data-stu-id="0e06d-121">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="0e06d-122">Propriedade</span><span class="sxs-lookup"><span data-stu-id="0e06d-122">Property</span></span>                | <span data-ttu-id="0e06d-123">xsi:type</span><span class="sxs-lookup"><span data-stu-id="0e06d-123">xsi:type</span></span>           | <span data-ttu-id="0e06d-124">Valor</span><span class="sxs-lookup"><span data-stu-id="0e06d-124">Value</span></span>                      |
|-------------------------|--------------------|----------------------------|
| <span data-ttu-id="0e06d-125">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="0e06d-125">DataType</span></span><br/>     | <span data-ttu-id="0e06d-126">string</span><span class="sxs-lookup"><span data-stu-id="0e06d-126">string</span></span><br/>  | <span data-ttu-id="0e06d-127">xs:integer</span><span class="sxs-lookup"><span data-stu-id="0e06d-127">xs:integer</span></span><br/>      |
| <span data-ttu-id="0e06d-128">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="0e06d-128">DefaultValue</span></span><br/> | <span data-ttu-id="0e06d-129">Número inteiro</span><span class="sxs-lookup"><span data-stu-id="0e06d-129">integer</span></span><br/> | <span data-ttu-id="0e06d-130">não definido</span><span class="sxs-lookup"><span data-stu-id="0e06d-130">undefined</span></span><br/>       |
| <span data-ttu-id="0e06d-131">MaxValue</span><span class="sxs-lookup"><span data-stu-id="0e06d-131">MaxValue</span></span><br/>     | <span data-ttu-id="0e06d-132">Número inteiro</span><span class="sxs-lookup"><span data-stu-id="0e06d-132">integer</span></span><br/> | <span data-ttu-id="0e06d-133">não definido</span><span class="sxs-lookup"><span data-stu-id="0e06d-133">undefined</span></span><br/>       |
| <span data-ttu-id="0e06d-134">MinValue</span><span class="sxs-lookup"><span data-stu-id="0e06d-134">MinValue</span></span><br/>     | <span data-ttu-id="0e06d-135">Número inteiro</span><span class="sxs-lookup"><span data-stu-id="0e06d-135">integer</span></span><br/> | <span data-ttu-id="0e06d-136">não definido</span><span class="sxs-lookup"><span data-stu-id="0e06d-136">undefined</span></span><br/>       |
| <span data-ttu-id="0e06d-137">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="0e06d-137">Mandatory</span></span><br/>    | <span data-ttu-id="0e06d-138">string</span><span class="sxs-lookup"><span data-stu-id="0e06d-138">string</span></span><br/>  | <span data-ttu-id="0e06d-139">PSK: condicional</span><span class="sxs-lookup"><span data-stu-id="0e06d-139">psk:Conditional</span></span><br/> |
| <span data-ttu-id="0e06d-140">Vários</span><span class="sxs-lookup"><span data-stu-id="0e06d-140">Multiple</span></span><br/>     | <span data-ttu-id="0e06d-141">integer</span><span class="sxs-lookup"><span data-stu-id="0e06d-141">integer</span></span><br/> | <span data-ttu-id="0e06d-142">1</span><span class="sxs-lookup"><span data-stu-id="0e06d-142">1</span></span><br/>               |
| <span data-ttu-id="0e06d-143">UnitType</span><span class="sxs-lookup"><span data-stu-id="0e06d-143">UnitType</span></span><br/>     | <span data-ttu-id="0e06d-144">string</span><span class="sxs-lookup"><span data-stu-id="0e06d-144">string</span></span><br/>  | <span data-ttu-id="0e06d-145">mícrons</span><span class="sxs-lookup"><span data-stu-id="0e06d-145">microns</span></span><br/>         |



 

## <a name="related-topics"></a><span data-ttu-id="0e06d-146">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="0e06d-146">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0e06d-147">Especificação de esquema de impressão</span><span class="sxs-lookup"><span data-stu-id="0e06d-147">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




