---
description: Este tópico não é atual. Para obter as informações mais atuais, consulte a especificação do esquema de impressão.
ms.assetid: 857caf51-ccf6-415c-aab3-1fed50fa7b34
title: PageMediaSizePSHeight
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1cb576ce7d623f4d036db1332b0339e6cef518d3
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/05/2021
ms.locfileid: "105815443"
---
# <a name="pagemediasizepsheight"></a><span data-ttu-id="d5f84-104">PageMediaSizePSHeight</span><span class="sxs-lookup"><span data-stu-id="d5f84-104">PageMediaSizePSHeight</span></span>

<span data-ttu-id="d5f84-105">Este tópico não é atual.</span><span class="sxs-lookup"><span data-stu-id="d5f84-105">This topic is not current.</span></span> <span data-ttu-id="d5f84-106">Para obter as informações mais atuais, consulte a [especificação do esquema de impressão](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="d5f84-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="d5f84-107">Especifica a altura da página, paralela à direção da orientação do feed (referência da [especificação de formato de arquivo de descrição de impressora PostScript](https://www.adobe.com/products/postscript/pdfs/PLRM.pdf)).</span><span class="sxs-lookup"><span data-stu-id="d5f84-107">Specifies the height of the page, parallel to the feed-orientation direction (Reference [PostScript Printer Description File Format Specification](https://www.adobe.com/products/postscript/pdfs/PLRM.pdf)).</span></span>

-   [<span data-ttu-id="d5f84-108">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="d5f84-108">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="d5f84-109">Conteúdo da estrutura</span><span class="sxs-lookup"><span data-stu-id="d5f84-109">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="d5f84-110">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="d5f84-110">Element Information</span></span>



| <span data-ttu-id="d5f84-111">Nome</span><span class="sxs-lookup"><span data-stu-id="d5f84-111">Name</span></span>                       |                                                             |
|----------------------------|-------------------------------------------------------------|
| <span data-ttu-id="d5f84-112">Tipo de elemento</span><span class="sxs-lookup"><span data-stu-id="d5f84-112">Element Type</span></span> <br/>   | <span data-ttu-id="d5f84-113">ParameterDef</span><span class="sxs-lookup"><span data-stu-id="d5f84-113">ParameterDef</span></span><br/>                                     |
| <span data-ttu-id="d5f84-114">Prefixo de escopo</span><span class="sxs-lookup"><span data-stu-id="d5f84-114">Scoping Prefix</span></span> <br/> | <span data-ttu-id="d5f84-115">?</span><span class="sxs-lookup"><span data-stu-id="d5f84-115">Page</span></span><br/>                                             |
| <span data-ttu-id="d5f84-116">Observações</span><span class="sxs-lookup"><span data-stu-id="d5f84-116">Notes</span></span> <br/>          | <span data-ttu-id="d5f84-117">Vinculado ao elemento PageMediaSize, opção CustomPS</span><span class="sxs-lookup"><span data-stu-id="d5f84-117">Linked to PageMediaSize element, CustomPS option</span></span><br/> |



 

## <a name="structure-content"></a><span data-ttu-id="d5f84-118">Conteúdo da estrutura</span><span class="sxs-lookup"><span data-stu-id="d5f84-118">Structure Content</span></span>

<span data-ttu-id="d5f84-119">A estrutura XML desse elemento é:</span><span class="sxs-lookup"><span data-stu-id="d5f84-119">The XML structure of this element is:</span></span>

``` syntax
<psf:ParameterDef name="psk:PageMediaSizePSHeight">
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

## <a name="structure-properties"></a><span data-ttu-id="d5f84-120">Propriedades da estrutura</span><span class="sxs-lookup"><span data-stu-id="d5f84-120">Structure Properties</span></span>

<span data-ttu-id="d5f84-121">A tabela a seguir descreve as características das variáveis definidas na estrutura XML.</span><span class="sxs-lookup"><span data-stu-id="d5f84-121">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="d5f84-122">Propriedade</span><span class="sxs-lookup"><span data-stu-id="d5f84-122">Property</span></span>                | <span data-ttu-id="d5f84-123">xsi:type</span><span class="sxs-lookup"><span data-stu-id="d5f84-123">xsi:type</span></span>           | <span data-ttu-id="d5f84-124">Valor</span><span class="sxs-lookup"><span data-stu-id="d5f84-124">Value</span></span>                      |
|-------------------------|--------------------|----------------------------|
| <span data-ttu-id="d5f84-125">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="d5f84-125">DataType</span></span><br/>     | <span data-ttu-id="d5f84-126">string</span><span class="sxs-lookup"><span data-stu-id="d5f84-126">string</span></span><br/>  | <span data-ttu-id="d5f84-127">xs:integer</span><span class="sxs-lookup"><span data-stu-id="d5f84-127">xs:integer</span></span><br/>      |
| <span data-ttu-id="d5f84-128">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="d5f84-128">DefaultValue</span></span><br/> | <span data-ttu-id="d5f84-129">Número inteiro</span><span class="sxs-lookup"><span data-stu-id="d5f84-129">integer</span></span><br/> | <span data-ttu-id="d5f84-130">não definido</span><span class="sxs-lookup"><span data-stu-id="d5f84-130">undefined</span></span><br/>       |
| <span data-ttu-id="d5f84-131">MaxValue</span><span class="sxs-lookup"><span data-stu-id="d5f84-131">MaxValue</span></span><br/>     | <span data-ttu-id="d5f84-132">Número inteiro</span><span class="sxs-lookup"><span data-stu-id="d5f84-132">integer</span></span><br/> | <span data-ttu-id="d5f84-133">não definido</span><span class="sxs-lookup"><span data-stu-id="d5f84-133">undefined</span></span><br/>       |
| <span data-ttu-id="d5f84-134">MinValue</span><span class="sxs-lookup"><span data-stu-id="d5f84-134">MinValue</span></span><br/>     | <span data-ttu-id="d5f84-135">Número inteiro</span><span class="sxs-lookup"><span data-stu-id="d5f84-135">integer</span></span><br/> | <span data-ttu-id="d5f84-136">não definido</span><span class="sxs-lookup"><span data-stu-id="d5f84-136">undefined</span></span><br/>       |
| <span data-ttu-id="d5f84-137">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="d5f84-137">Mandatory</span></span><br/>    | <span data-ttu-id="d5f84-138">string</span><span class="sxs-lookup"><span data-stu-id="d5f84-138">string</span></span><br/>  | <span data-ttu-id="d5f84-139">PSK: condicional</span><span class="sxs-lookup"><span data-stu-id="d5f84-139">psk:Conditional</span></span><br/> |
| <span data-ttu-id="d5f84-140">Vários</span><span class="sxs-lookup"><span data-stu-id="d5f84-140">Multiple</span></span><br/>     | <span data-ttu-id="d5f84-141">integer</span><span class="sxs-lookup"><span data-stu-id="d5f84-141">integer</span></span><br/> | <span data-ttu-id="d5f84-142">1</span><span class="sxs-lookup"><span data-stu-id="d5f84-142">1</span></span><br/>               |
| <span data-ttu-id="d5f84-143">UnitType</span><span class="sxs-lookup"><span data-stu-id="d5f84-143">UnitType</span></span><br/>     | <span data-ttu-id="d5f84-144">string</span><span class="sxs-lookup"><span data-stu-id="d5f84-144">string</span></span><br/>  | <span data-ttu-id="d5f84-145">mícrons</span><span class="sxs-lookup"><span data-stu-id="d5f84-145">microns</span></span><br/>         |



 

## <a name="related-topics"></a><span data-ttu-id="d5f84-146">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="d5f84-146">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d5f84-147">Especificação de formato de arquivo de descrição de impressora PostScript</span><span class="sxs-lookup"><span data-stu-id="d5f84-147">PostScript Printer Description File Format Specification</span></span>](https://www.adobe.com/products/postscript/pdfs/PLRM.pdf)
</dt> <dt>

[<span data-ttu-id="d5f84-148">Especificação de esquema de impressão</span><span class="sxs-lookup"><span data-stu-id="d5f84-148">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




