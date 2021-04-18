---
description: Este tópico não é atual. Para obter as informações mais atuais, consulte a especificação do esquema de impressão.
ms.assetid: a1a684ce-5615-4ff7-a7aa-5c9f786f84ed
title: PageMediaSizePSWidth
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a7fef8b9e3740c5f12045e449f2a6b8100d7fc1d
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/05/2021
ms.locfileid: "105807292"
---
# <a name="pagemediasizepswidth"></a><span data-ttu-id="a8ffc-104">PageMediaSizePSWidth</span><span class="sxs-lookup"><span data-stu-id="a8ffc-104">PageMediaSizePSWidth</span></span>

<span data-ttu-id="a8ffc-105">Este tópico não é atual.</span><span class="sxs-lookup"><span data-stu-id="a8ffc-105">This topic is not current.</span></span> <span data-ttu-id="a8ffc-106">Para obter as informações mais atuais, consulte a [especificação do esquema de impressão](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="a8ffc-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="a8ffc-107">Especifica a largura da página perpendicular à direção da orientação do feed (referência à [especificação de formato de arquivo de descrição de impressora PostScript](https://www.adobe.com/products/postscript/pdfs/PLRM.pdf)).</span><span class="sxs-lookup"><span data-stu-id="a8ffc-107">Specifies the width of the page perpendicular to the feed-orientation direction (Reference [PostScript Printer Description File Format Specification](https://www.adobe.com/products/postscript/pdfs/PLRM.pdf)).</span></span>

-   [<span data-ttu-id="a8ffc-108">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="a8ffc-108">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="a8ffc-109">Conteúdo da estrutura</span><span class="sxs-lookup"><span data-stu-id="a8ffc-109">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="a8ffc-110">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="a8ffc-110">Element Information</span></span>



| <span data-ttu-id="a8ffc-111">Nome</span><span class="sxs-lookup"><span data-stu-id="a8ffc-111">Name</span></span>                       |                                                             |
|----------------------------|-------------------------------------------------------------|
| <span data-ttu-id="a8ffc-112">Tipo de elemento</span><span class="sxs-lookup"><span data-stu-id="a8ffc-112">Element Type</span></span> <br/>   | <span data-ttu-id="a8ffc-113">ParameterDef</span><span class="sxs-lookup"><span data-stu-id="a8ffc-113">ParameterDef</span></span><br/>                                     |
| <span data-ttu-id="a8ffc-114">Prefixo de escopo</span><span class="sxs-lookup"><span data-stu-id="a8ffc-114">Scoping Prefix</span></span> <br/> | <span data-ttu-id="a8ffc-115">?</span><span class="sxs-lookup"><span data-stu-id="a8ffc-115">Page</span></span><br/>                                             |
| <span data-ttu-id="a8ffc-116">Observações</span><span class="sxs-lookup"><span data-stu-id="a8ffc-116">Notes</span></span> <br/>          | <span data-ttu-id="a8ffc-117">Vinculado ao elemento PageMediaSize, opção CustomPS</span><span class="sxs-lookup"><span data-stu-id="a8ffc-117">Linked to PageMediaSize element, CustomPS option</span></span><br/> |



 

## <a name="structure-content"></a><span data-ttu-id="a8ffc-118">Conteúdo da estrutura</span><span class="sxs-lookup"><span data-stu-id="a8ffc-118">Structure Content</span></span>

<span data-ttu-id="a8ffc-119">A estrutura XML desse elemento é:</span><span class="sxs-lookup"><span data-stu-id="a8ffc-119">The XML structure of this element is:</span></span>

``` syntax
<psf:ParameterDef name="psk:PageMediaSizePSWidth">
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

## <a name="structure-properties"></a><span data-ttu-id="a8ffc-120">Propriedades da estrutura</span><span class="sxs-lookup"><span data-stu-id="a8ffc-120">Structure Properties</span></span>

<span data-ttu-id="a8ffc-121">A tabela a seguir descreve as características das variáveis definidas na estrutura XML.</span><span class="sxs-lookup"><span data-stu-id="a8ffc-121">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="a8ffc-122">Propriedade</span><span class="sxs-lookup"><span data-stu-id="a8ffc-122">Property</span></span>                | <span data-ttu-id="a8ffc-123">xsi:type</span><span class="sxs-lookup"><span data-stu-id="a8ffc-123">xsi:type</span></span>           | <span data-ttu-id="a8ffc-124">Valor</span><span class="sxs-lookup"><span data-stu-id="a8ffc-124">Value</span></span>                      |
|-------------------------|--------------------|----------------------------|
| <span data-ttu-id="a8ffc-125">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="a8ffc-125">DataType</span></span><br/>     | <span data-ttu-id="a8ffc-126">string</span><span class="sxs-lookup"><span data-stu-id="a8ffc-126">string</span></span><br/>  | <span data-ttu-id="a8ffc-127">xs:integer</span><span class="sxs-lookup"><span data-stu-id="a8ffc-127">xs:integer</span></span><br/>      |
| <span data-ttu-id="a8ffc-128">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="a8ffc-128">DefaultValue</span></span><br/> | <span data-ttu-id="a8ffc-129">Número inteiro</span><span class="sxs-lookup"><span data-stu-id="a8ffc-129">integer</span></span><br/> | <span data-ttu-id="a8ffc-130">não definido</span><span class="sxs-lookup"><span data-stu-id="a8ffc-130">undefined</span></span><br/>       |
| <span data-ttu-id="a8ffc-131">MaxValue</span><span class="sxs-lookup"><span data-stu-id="a8ffc-131">MaxValue</span></span><br/>     | <span data-ttu-id="a8ffc-132">Número inteiro</span><span class="sxs-lookup"><span data-stu-id="a8ffc-132">integer</span></span><br/> | <span data-ttu-id="a8ffc-133">não definido</span><span class="sxs-lookup"><span data-stu-id="a8ffc-133">undefined</span></span><br/>       |
| <span data-ttu-id="a8ffc-134">MinValue</span><span class="sxs-lookup"><span data-stu-id="a8ffc-134">MinValue</span></span><br/>     | <span data-ttu-id="a8ffc-135">Número inteiro</span><span class="sxs-lookup"><span data-stu-id="a8ffc-135">integer</span></span><br/> | <span data-ttu-id="a8ffc-136">não definido</span><span class="sxs-lookup"><span data-stu-id="a8ffc-136">undefined</span></span><br/>       |
| <span data-ttu-id="a8ffc-137">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="a8ffc-137">Mandatory</span></span><br/>    | <span data-ttu-id="a8ffc-138">string</span><span class="sxs-lookup"><span data-stu-id="a8ffc-138">string</span></span><br/>  | <span data-ttu-id="a8ffc-139">PSK: condicional</span><span class="sxs-lookup"><span data-stu-id="a8ffc-139">psk:Conditional</span></span><br/> |
| <span data-ttu-id="a8ffc-140">Vários</span><span class="sxs-lookup"><span data-stu-id="a8ffc-140">Multiple</span></span><br/>     | <span data-ttu-id="a8ffc-141">integer</span><span class="sxs-lookup"><span data-stu-id="a8ffc-141">integer</span></span><br/> | <span data-ttu-id="a8ffc-142">1</span><span class="sxs-lookup"><span data-stu-id="a8ffc-142">1</span></span><br/>               |
| <span data-ttu-id="a8ffc-143">UnitType</span><span class="sxs-lookup"><span data-stu-id="a8ffc-143">UnitType</span></span><br/>     | <span data-ttu-id="a8ffc-144">string</span><span class="sxs-lookup"><span data-stu-id="a8ffc-144">string</span></span><br/>  | <span data-ttu-id="a8ffc-145">mícrons</span><span class="sxs-lookup"><span data-stu-id="a8ffc-145">microns</span></span><br/>         |



 

## <a name="related-topics"></a><span data-ttu-id="a8ffc-146">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="a8ffc-146">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a8ffc-147">Especificação de formato de arquivo de descrição de impressora PostScript</span><span class="sxs-lookup"><span data-stu-id="a8ffc-147">PostScript Printer Description File Format Specification</span></span>](https://www.adobe.com/products/postscript/pdfs/PLRM.pdf)
</dt> <dt>

[<span data-ttu-id="a8ffc-148">Especificação de esquema de impressão</span><span class="sxs-lookup"><span data-stu-id="a8ffc-148">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




