---
description: Este tópico não é atual. Para obter as informações mais atuais, consulte a especificação do esquema de impressão.
ms.assetid: b091c250-66f2-47cc-a012-1526c0ed02c9
title: PageMediaSizePSOrientation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a188c61d3bb3c47286b887406174a3fc41f3c58a
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/05/2021
ms.locfileid: "105786194"
---
# <a name="pagemediasizepsorientation"></a><span data-ttu-id="e3803-104">PageMediaSizePSOrientation</span><span class="sxs-lookup"><span data-stu-id="e3803-104">PageMediaSizePSOrientation</span></span>

<span data-ttu-id="e3803-105">Este tópico não é atual.</span><span class="sxs-lookup"><span data-stu-id="e3803-105">This topic is not current.</span></span> <span data-ttu-id="e3803-106">Para obter as informações mais atuais, consulte a [especificação do esquema de impressão](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="e3803-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="e3803-107">Especifica a orientação relativa à direção da orientação do feed (referência à [especificação de formato de arquivo de descrição de impressora PostScript](https://www.adobe.com/products/postscript/pdfs/PLRM.pdf)).</span><span class="sxs-lookup"><span data-stu-id="e3803-107">Specifies the orientation relative to the feed-orientation direction (Reference [PostScript Printer Description File Format Specification](https://www.adobe.com/products/postscript/pdfs/PLRM.pdf)).</span></span>

-   [<span data-ttu-id="e3803-108">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="e3803-108">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="e3803-109">Conteúdo da estrutura</span><span class="sxs-lookup"><span data-stu-id="e3803-109">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="e3803-110">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="e3803-110">Element Information</span></span>



| <span data-ttu-id="e3803-111">Nome</span><span class="sxs-lookup"><span data-stu-id="e3803-111">Name</span></span>                       |                                                             |
|----------------------------|-------------------------------------------------------------|
| <span data-ttu-id="e3803-112">Tipo de elemento</span><span class="sxs-lookup"><span data-stu-id="e3803-112">Element Type</span></span> <br/>   | <span data-ttu-id="e3803-113">ParameterDef</span><span class="sxs-lookup"><span data-stu-id="e3803-113">ParameterDef</span></span><br/>                                     |
| <span data-ttu-id="e3803-114">Prefixo de escopo</span><span class="sxs-lookup"><span data-stu-id="e3803-114">Scoping Prefix</span></span> <br/> | <span data-ttu-id="e3803-115">?</span><span class="sxs-lookup"><span data-stu-id="e3803-115">Page</span></span><br/>                                             |
| <span data-ttu-id="e3803-116">Observações</span><span class="sxs-lookup"><span data-stu-id="e3803-116">Notes</span></span> <br/>          | <span data-ttu-id="e3803-117">Vinculado ao elemento PageMediaSize, opção CustomPS</span><span class="sxs-lookup"><span data-stu-id="e3803-117">Linked to PageMediaSize element, CustomPS option</span></span><br/> |



 

## <a name="structure-content"></a><span data-ttu-id="e3803-118">Conteúdo da estrutura</span><span class="sxs-lookup"><span data-stu-id="e3803-118">Structure Content</span></span>

<span data-ttu-id="e3803-119">A estrutura XML desse elemento é:</span><span class="sxs-lookup"><span data-stu-id="e3803-119">The XML structure of this element is:</span></span>

``` syntax
<psf:ParameterDef name="psk:PageMediaSizePSOrientation">
  <psf:Property name="psf:DataType">
    <psf:Value xsi:type="xs:string">xs:integer</psf:Value>
  </psf:Property>
  <psf:Property name="psf:DefaultValue">
    <psf:Value xsi:type="xs:integer">0</psf:Value>
  </psf:Property>
  <psf:Property name="psf:MaxValue">
    <psf:Value xsi:type="xs:integer">3</psf:Value>
  </psf:Property>
  <psf:Property name="psf:MinValue">
    <psf:Value xsi:type="xs:integer">0</psf:Value>
  </psf:Property>
  <psf:Property name="psf:Multiple">
    <psf:Value xsi:type="xs:integer">1</psf:Value>
  </psf:Property>
  <psf:Property name="psf:Mandatory">
    <psf:Value xsi:type="xs:string">psk:Conditional</psf:Value>
  </psf:Property>
  <psf:Property name="psf:UnitType">
    <psf:Value xsi:type="xs:string">PageMediaSizeEnum</psf:Value>
  </psf:Property>
</psf:ParameterDef>
      
```

## <a name="structure-properties"></a><span data-ttu-id="e3803-120">Propriedades da estrutura</span><span class="sxs-lookup"><span data-stu-id="e3803-120">Structure Properties</span></span>

<span data-ttu-id="e3803-121">A tabela a seguir descreve as características das variáveis definidas na estrutura XML.</span><span class="sxs-lookup"><span data-stu-id="e3803-121">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="e3803-122">Propriedade</span><span class="sxs-lookup"><span data-stu-id="e3803-122">Property</span></span>                | <span data-ttu-id="e3803-123">xsi:type</span><span class="sxs-lookup"><span data-stu-id="e3803-123">xsi:type</span></span>           | <span data-ttu-id="e3803-124">Valor</span><span class="sxs-lookup"><span data-stu-id="e3803-124">Value</span></span>                        |
|-------------------------|--------------------|------------------------------|
| <span data-ttu-id="e3803-125">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="e3803-125">DataType</span></span><br/>     | <span data-ttu-id="e3803-126">string</span><span class="sxs-lookup"><span data-stu-id="e3803-126">string</span></span><br/>  | <span data-ttu-id="e3803-127">xs:integer</span><span class="sxs-lookup"><span data-stu-id="e3803-127">xs:integer</span></span><br/>        |
| <span data-ttu-id="e3803-128">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="e3803-128">DefaultValue</span></span><br/> | <span data-ttu-id="e3803-129">integer</span><span class="sxs-lookup"><span data-stu-id="e3803-129">integer</span></span><br/> | <span data-ttu-id="e3803-130">0</span><span class="sxs-lookup"><span data-stu-id="e3803-130">0</span></span><br/>                 |
| <span data-ttu-id="e3803-131">MaxValue</span><span class="sxs-lookup"><span data-stu-id="e3803-131">MaxValue</span></span><br/>     | <span data-ttu-id="e3803-132">Número inteiro</span><span class="sxs-lookup"><span data-stu-id="e3803-132">integer</span></span><br/> | <span data-ttu-id="e3803-133">3</span><span class="sxs-lookup"><span data-stu-id="e3803-133">3</span></span><br/>                 |
| <span data-ttu-id="e3803-134">MinValue</span><span class="sxs-lookup"><span data-stu-id="e3803-134">MinValue</span></span><br/>     | <span data-ttu-id="e3803-135">integer</span><span class="sxs-lookup"><span data-stu-id="e3803-135">integer</span></span><br/> | <span data-ttu-id="e3803-136">0</span><span class="sxs-lookup"><span data-stu-id="e3803-136">0</span></span><br/>                 |
| <span data-ttu-id="e3803-137">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="e3803-137">Mandatory</span></span><br/>    | <span data-ttu-id="e3803-138">string</span><span class="sxs-lookup"><span data-stu-id="e3803-138">string</span></span><br/>  | <span data-ttu-id="e3803-139">PSK: condicional</span><span class="sxs-lookup"><span data-stu-id="e3803-139">psk:Conditional</span></span><br/>   |
| <span data-ttu-id="e3803-140">Vários</span><span class="sxs-lookup"><span data-stu-id="e3803-140">Multiple</span></span><br/>     | <span data-ttu-id="e3803-141">integer</span><span class="sxs-lookup"><span data-stu-id="e3803-141">integer</span></span><br/> | <span data-ttu-id="e3803-142">1</span><span class="sxs-lookup"><span data-stu-id="e3803-142">1</span></span><br/>                 |
| <span data-ttu-id="e3803-143">UnitType</span><span class="sxs-lookup"><span data-stu-id="e3803-143">UnitType</span></span><br/>     | <span data-ttu-id="e3803-144">string</span><span class="sxs-lookup"><span data-stu-id="e3803-144">string</span></span><br/>  | <span data-ttu-id="e3803-145">PageMediaSizeEnum</span><span class="sxs-lookup"><span data-stu-id="e3803-145">PageMediaSizeEnum</span></span><br/> |



 

## <a name="related-topics"></a><span data-ttu-id="e3803-146">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="e3803-146">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e3803-147">Especificação de formato de arquivo de descrição de impressora PostScript</span><span class="sxs-lookup"><span data-stu-id="e3803-147">PostScript Printer Description File Format Specification</span></span>](https://www.adobe.com/products/postscript/pdfs/PLRM.pdf)
</dt> <dt>

[<span data-ttu-id="e3803-148">Especificação de esquema de impressão</span><span class="sxs-lookup"><span data-stu-id="e3803-148">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




