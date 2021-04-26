---
description: Este tópico não é atual. Para obter as informações mais atuais, consulte a especificação do esquema de impressão.
ms.assetid: 22e4a6e9-4d18-4fff-873c-27ba59a79222
title: PageMediaSizeMediaSizeWidth
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 50df088fd25a69ee566e1406d3f1b833aa6131f5
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/26/2021
ms.locfileid: "107997563"
---
# <a name="pagemediasizemediasizewidth"></a><span data-ttu-id="f11eb-104">PageMediaSizeMediaSizeWidth</span><span class="sxs-lookup"><span data-stu-id="f11eb-104">PageMediaSizeMediaSizeWidth</span></span>

<span data-ttu-id="f11eb-105">Este tópico não é atual.</span><span class="sxs-lookup"><span data-stu-id="f11eb-105">This topic is not current.</span></span> <span data-ttu-id="f11eb-106">Para obter as informações mais atuais, consulte a [especificação do esquema de impressão](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="f11eb-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="f11eb-107">Especifica a direção da dimensão MediaSizeWidth para a opção MediaSize personalizada.</span><span class="sxs-lookup"><span data-stu-id="f11eb-107">Specifies the dimension MediaSizeWidth direction for the Custom MediaSize option.</span></span>

-   [<span data-ttu-id="f11eb-108">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="f11eb-108">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="f11eb-109">Conteúdo da estrutura</span><span class="sxs-lookup"><span data-stu-id="f11eb-109">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="f11eb-110">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="f11eb-110">Element Information</span></span>



| <span data-ttu-id="f11eb-111">Nome</span><span class="sxs-lookup"><span data-stu-id="f11eb-111">Name</span></span> | <span data-ttu-id="f11eb-112">Valor</span><span class="sxs-lookup"><span data-stu-id="f11eb-112">Value</span></span> |
|----------------------------|-----------------------------------------------------------|
| <span data-ttu-id="f11eb-113">Tipo de elemento</span><span class="sxs-lookup"><span data-stu-id="f11eb-113">Element Type</span></span> <br/>   | <span data-ttu-id="f11eb-114">ParameterDef</span><span class="sxs-lookup"><span data-stu-id="f11eb-114">ParameterDef</span></span><br/>                                   |
| <span data-ttu-id="f11eb-115">Prefixo de escopo</span><span class="sxs-lookup"><span data-stu-id="f11eb-115">Scoping Prefix</span></span> <br/> | <span data-ttu-id="f11eb-116">?</span><span class="sxs-lookup"><span data-stu-id="f11eb-116">Page</span></span><br/>                                           |
| <span data-ttu-id="f11eb-117">Observações</span><span class="sxs-lookup"><span data-stu-id="f11eb-117">Notes</span></span> <br/>          | <span data-ttu-id="f11eb-118">Vinculado ao elemento PageMediaSize, opção personalizada</span><span class="sxs-lookup"><span data-stu-id="f11eb-118">Linked to PageMediaSize element, Custom option</span></span><br/> |



 

## <a name="structure-content"></a><span data-ttu-id="f11eb-119">Conteúdo da estrutura</span><span class="sxs-lookup"><span data-stu-id="f11eb-119">Structure Content</span></span>

<span data-ttu-id="f11eb-120">A estrutura XML desse elemento é:</span><span class="sxs-lookup"><span data-stu-id="f11eb-120">The XML structure of this element is:</span></span>

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

## <a name="structure-properties"></a><span data-ttu-id="f11eb-121">Propriedades da estrutura</span><span class="sxs-lookup"><span data-stu-id="f11eb-121">Structure Properties</span></span>

<span data-ttu-id="f11eb-122">A tabela a seguir descreve as características das variáveis definidas na estrutura XML.</span><span class="sxs-lookup"><span data-stu-id="f11eb-122">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="f11eb-123">Propriedade</span><span class="sxs-lookup"><span data-stu-id="f11eb-123">Property</span></span>                | <span data-ttu-id="f11eb-124">xsi:type</span><span class="sxs-lookup"><span data-stu-id="f11eb-124">xsi:type</span></span>           | <span data-ttu-id="f11eb-125">Valor</span><span class="sxs-lookup"><span data-stu-id="f11eb-125">Value</span></span>                      |
|-------------------------|--------------------|----------------------------|
| <span data-ttu-id="f11eb-126">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="f11eb-126">DataType</span></span><br/>     | <span data-ttu-id="f11eb-127">string</span><span class="sxs-lookup"><span data-stu-id="f11eb-127">string</span></span><br/>  | <span data-ttu-id="f11eb-128">xs:integer</span><span class="sxs-lookup"><span data-stu-id="f11eb-128">xs:integer</span></span><br/>      |
| <span data-ttu-id="f11eb-129">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="f11eb-129">DefaultValue</span></span><br/> | <span data-ttu-id="f11eb-130">Número inteiro</span><span class="sxs-lookup"><span data-stu-id="f11eb-130">integer</span></span><br/> | <span data-ttu-id="f11eb-131">não definido</span><span class="sxs-lookup"><span data-stu-id="f11eb-131">undefined</span></span><br/>       |
| <span data-ttu-id="f11eb-132">MaxValue</span><span class="sxs-lookup"><span data-stu-id="f11eb-132">MaxValue</span></span><br/>     | <span data-ttu-id="f11eb-133">Número inteiro</span><span class="sxs-lookup"><span data-stu-id="f11eb-133">integer</span></span><br/> | <span data-ttu-id="f11eb-134">não definido</span><span class="sxs-lookup"><span data-stu-id="f11eb-134">undefined</span></span><br/>       |
| <span data-ttu-id="f11eb-135">MinValue</span><span class="sxs-lookup"><span data-stu-id="f11eb-135">MinValue</span></span><br/>     | <span data-ttu-id="f11eb-136">Número inteiro</span><span class="sxs-lookup"><span data-stu-id="f11eb-136">integer</span></span><br/> | <span data-ttu-id="f11eb-137">não definido</span><span class="sxs-lookup"><span data-stu-id="f11eb-137">undefined</span></span><br/>       |
| <span data-ttu-id="f11eb-138">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="f11eb-138">Mandatory</span></span><br/>    | <span data-ttu-id="f11eb-139">string</span><span class="sxs-lookup"><span data-stu-id="f11eb-139">string</span></span><br/>  | <span data-ttu-id="f11eb-140">PSK: condicional</span><span class="sxs-lookup"><span data-stu-id="f11eb-140">psk:Conditional</span></span><br/> |
| <span data-ttu-id="f11eb-141">Vários</span><span class="sxs-lookup"><span data-stu-id="f11eb-141">Multiple</span></span><br/>     | <span data-ttu-id="f11eb-142">integer</span><span class="sxs-lookup"><span data-stu-id="f11eb-142">integer</span></span><br/> | <span data-ttu-id="f11eb-143">1</span><span class="sxs-lookup"><span data-stu-id="f11eb-143">1</span></span><br/>               |
| <span data-ttu-id="f11eb-144">UnitType</span><span class="sxs-lookup"><span data-stu-id="f11eb-144">UnitType</span></span><br/>     | <span data-ttu-id="f11eb-145">string</span><span class="sxs-lookup"><span data-stu-id="f11eb-145">string</span></span><br/>  | <span data-ttu-id="f11eb-146">mícrons</span><span class="sxs-lookup"><span data-stu-id="f11eb-146">microns</span></span><br/>         |



 

## <a name="related-topics"></a><span data-ttu-id="f11eb-147">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="f11eb-147">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f11eb-148">Especificação de esquema de impressão</span><span class="sxs-lookup"><span data-stu-id="f11eb-148">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




