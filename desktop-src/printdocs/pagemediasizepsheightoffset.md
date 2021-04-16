---
description: Este tópico não é atual. Para obter as informações mais atuais, consulte a especificação do esquema de impressão.
ms.assetid: e86d6a5d-484d-4c80-8c86-7d12d287ee21
title: PageMediaSizePSHeightOffset
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2e02129d5c8c20fceef01a9cd5cf40e5827374a7
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/05/2021
ms.locfileid: "105773051"
---
# <a name="pagemediasizepsheightoffset"></a><span data-ttu-id="f1713-104">PageMediaSizePSHeightOffset</span><span class="sxs-lookup"><span data-stu-id="f1713-104">PageMediaSizePSHeightOffset</span></span>

<span data-ttu-id="f1713-105">Este tópico não é atual.</span><span class="sxs-lookup"><span data-stu-id="f1713-105">This topic is not current.</span></span> <span data-ttu-id="f1713-106">Para obter as informações mais atuais, consulte a [especificação do esquema de impressão](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="f1713-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="f1713-107">Especifica o deslocamento, paralelo à direção da orientação do feed (referência da [especificação de formato de arquivo de descrição de impressora PostScript](https://www.adobe.com/products/postscript/pdfs/PLRM.pdf)).</span><span class="sxs-lookup"><span data-stu-id="f1713-107">Specifies the offset, parallel to the feed-orientation direction (Reference [PostScript Printer Description File Format Specification](https://www.adobe.com/products/postscript/pdfs/PLRM.pdf)).</span></span>

-   [<span data-ttu-id="f1713-108">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="f1713-108">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="f1713-109">Conteúdo da estrutura</span><span class="sxs-lookup"><span data-stu-id="f1713-109">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="f1713-110">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="f1713-110">Element Information</span></span>



| <span data-ttu-id="f1713-111">Nome</span><span class="sxs-lookup"><span data-stu-id="f1713-111">Name</span></span>                       |                                                             |
|----------------------------|-------------------------------------------------------------|
| <span data-ttu-id="f1713-112">Tipo de elemento</span><span class="sxs-lookup"><span data-stu-id="f1713-112">Element Type</span></span> <br/>   | <span data-ttu-id="f1713-113">ParameterDef</span><span class="sxs-lookup"><span data-stu-id="f1713-113">ParameterDef</span></span><br/>                                     |
| <span data-ttu-id="f1713-114">Prefixo de escopo</span><span class="sxs-lookup"><span data-stu-id="f1713-114">Scoping Prefix</span></span> <br/> | <span data-ttu-id="f1713-115">?</span><span class="sxs-lookup"><span data-stu-id="f1713-115">Page</span></span><br/>                                             |
| <span data-ttu-id="f1713-116">Observações</span><span class="sxs-lookup"><span data-stu-id="f1713-116">Notes</span></span> <br/>          | <span data-ttu-id="f1713-117">Vinculado ao elemento PageMediaSize, opção CustomPS</span><span class="sxs-lookup"><span data-stu-id="f1713-117">Linked to PageMediaSize element, CustomPS option</span></span><br/> |



 

## <a name="structure-content"></a><span data-ttu-id="f1713-118">Conteúdo da estrutura</span><span class="sxs-lookup"><span data-stu-id="f1713-118">Structure Content</span></span>

<span data-ttu-id="f1713-119">A estrutura XML desse elemento é:</span><span class="sxs-lookup"><span data-stu-id="f1713-119">The XML structure of this element is:</span></span>

``` syntax
<psf:ParameterDef name="psk:PageMediaSizePSHeightOffset">
  <psf:Property name="psf:DataType">
    <psf:Value xsi:type="xs:string">xs:integer</psf:Value>
  </psf:Property>
  <psf:Property name="psf:DefaultValue">
    <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
  </psf:Property>
  <psf:Property name="psf:MaxValue">
    <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
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

## <a name="structure-properties"></a><span data-ttu-id="f1713-120">Propriedades da estrutura</span><span class="sxs-lookup"><span data-stu-id="f1713-120">Structure Properties</span></span>

<span data-ttu-id="f1713-121">A tabela a seguir descreve as características das variáveis definidas na estrutura XML.</span><span class="sxs-lookup"><span data-stu-id="f1713-121">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="f1713-122">Propriedade</span><span class="sxs-lookup"><span data-stu-id="f1713-122">Property</span></span>                | <span data-ttu-id="f1713-123">xsi:type</span><span class="sxs-lookup"><span data-stu-id="f1713-123">xsi:type</span></span>           | <span data-ttu-id="f1713-124">Valor</span><span class="sxs-lookup"><span data-stu-id="f1713-124">Value</span></span>                      |
|-------------------------|--------------------|----------------------------|
| <span data-ttu-id="f1713-125">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="f1713-125">DataType</span></span><br/>     | <span data-ttu-id="f1713-126">string</span><span class="sxs-lookup"><span data-stu-id="f1713-126">string</span></span><br/>  | <span data-ttu-id="f1713-127">xs:integer</span><span class="sxs-lookup"><span data-stu-id="f1713-127">xs:integer</span></span><br/>      |
| <span data-ttu-id="f1713-128">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="f1713-128">DefaultValue</span></span><br/> | <span data-ttu-id="f1713-129">Número inteiro</span><span class="sxs-lookup"><span data-stu-id="f1713-129">integer</span></span><br/> | <span data-ttu-id="f1713-130">não definido</span><span class="sxs-lookup"><span data-stu-id="f1713-130">undefined</span></span><br/>       |
| <span data-ttu-id="f1713-131">MaxValue</span><span class="sxs-lookup"><span data-stu-id="f1713-131">MaxValue</span></span><br/>     | <span data-ttu-id="f1713-132">Número inteiro</span><span class="sxs-lookup"><span data-stu-id="f1713-132">integer</span></span><br/> | <span data-ttu-id="f1713-133">não definido</span><span class="sxs-lookup"><span data-stu-id="f1713-133">undefined</span></span><br/>       |
| <span data-ttu-id="f1713-134">MinValue</span><span class="sxs-lookup"><span data-stu-id="f1713-134">MinValue</span></span><br/>     | <span data-ttu-id="f1713-135">Número inteiro</span><span class="sxs-lookup"><span data-stu-id="f1713-135">integer</span></span><br/> | <span data-ttu-id="f1713-136">não definido</span><span class="sxs-lookup"><span data-stu-id="f1713-136">undefined</span></span><br/>       |
| <span data-ttu-id="f1713-137">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="f1713-137">Mandatory</span></span><br/>    | <span data-ttu-id="f1713-138">string</span><span class="sxs-lookup"><span data-stu-id="f1713-138">string</span></span><br/>  | <span data-ttu-id="f1713-139">PSK: condicional</span><span class="sxs-lookup"><span data-stu-id="f1713-139">psk:Conditional</span></span><br/> |
| <span data-ttu-id="f1713-140">Vários</span><span class="sxs-lookup"><span data-stu-id="f1713-140">Multiple</span></span><br/>     | <span data-ttu-id="f1713-141">integer</span><span class="sxs-lookup"><span data-stu-id="f1713-141">integer</span></span><br/> | <span data-ttu-id="f1713-142">1</span><span class="sxs-lookup"><span data-stu-id="f1713-142">1</span></span><br/>               |
| <span data-ttu-id="f1713-143">UnitType</span><span class="sxs-lookup"><span data-stu-id="f1713-143">UnitType</span></span><br/>     | <span data-ttu-id="f1713-144">string</span><span class="sxs-lookup"><span data-stu-id="f1713-144">string</span></span><br/>  | <span data-ttu-id="f1713-145">mícrons</span><span class="sxs-lookup"><span data-stu-id="f1713-145">microns</span></span><br/>         |



 

## <a name="related-topics"></a><span data-ttu-id="f1713-146">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="f1713-146">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f1713-147">Especificação de formato de arquivo de descrição de impressora PostScript</span><span class="sxs-lookup"><span data-stu-id="f1713-147">PostScript Printer Description File Format Specification</span></span>](https://www.adobe.com/products/postscript/pdfs/PLRM.pdf)
</dt> <dt>

[<span data-ttu-id="f1713-148">Especificação de esquema de impressão</span><span class="sxs-lookup"><span data-stu-id="f1713-148">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




