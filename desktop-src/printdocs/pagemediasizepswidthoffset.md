---
description: Obter informações sobre o parâmetro PageMediaSizePSWidthOffset. Este tópico não é atual. Para obter as informações mais atuais, consulte a Especificação de Esquema de Impressão.
ms.assetid: b93ad6e6-ab27-4fab-b488-6f402b6ee857
title: PageMediaSizePSWidthOffset
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 265acad803dbc334be115440e195967465b3ef50
ms.sourcegitcommit: 998d50f6def8a25850fc113fc8a2df903c829c5e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/09/2021
ms.locfileid: "113549086"
---
# <a name="pagemediasizepswidthoffset"></a><span data-ttu-id="4cc85-105">PageMediaSizePSWidthOffset</span><span class="sxs-lookup"><span data-stu-id="4cc85-105">PageMediaSizePSWidthOffset</span></span>

<span data-ttu-id="4cc85-106">Este tópico não é atual.</span><span class="sxs-lookup"><span data-stu-id="4cc85-106">This topic is not current.</span></span> <span data-ttu-id="4cc85-107">Para obter as informações mais atuais, consulte a [Especificação de Esquema de Impressão](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="4cc85-107">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="4cc85-108">Especifica a direção de deslocamento para a orientação do feed (Referência PostScript especificação de formato de arquivo de descrição [da impressora).](https://www.adobe.com/products/postscript/pdfs/PLRM.pdf)</span><span class="sxs-lookup"><span data-stu-id="4cc85-108">Specifies the offset perpendicular to the feed-orientation direction (Reference [PostScript Printer Description File Format Specification](https://www.adobe.com/products/postscript/pdfs/PLRM.pdf)).</span></span>

-   [<span data-ttu-id="4cc85-109">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="4cc85-109">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="4cc85-110">Conteúdo da estrutura</span><span class="sxs-lookup"><span data-stu-id="4cc85-110">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="4cc85-111">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="4cc85-111">Element Information</span></span>



| <span data-ttu-id="4cc85-112">Nome</span><span class="sxs-lookup"><span data-stu-id="4cc85-112">Name</span></span> | <span data-ttu-id="4cc85-113">Valor</span><span class="sxs-lookup"><span data-stu-id="4cc85-113">Value</span></span> |
|----------------------------|-------------------------------------------------------------|
| <span data-ttu-id="4cc85-114">Tipo de elemento</span><span class="sxs-lookup"><span data-stu-id="4cc85-114">Element Type</span></span> <br/>   | <span data-ttu-id="4cc85-115">ParameterDef</span><span class="sxs-lookup"><span data-stu-id="4cc85-115">ParameterDef</span></span><br/>                                     |
| <span data-ttu-id="4cc85-116">Prefixo de definição de scoping</span><span class="sxs-lookup"><span data-stu-id="4cc85-116">Scoping Prefix</span></span> <br/> | <span data-ttu-id="4cc85-117">Página</span><span class="sxs-lookup"><span data-stu-id="4cc85-117">Page</span></span><br/>                                             |
| <span data-ttu-id="4cc85-118">Observações</span><span class="sxs-lookup"><span data-stu-id="4cc85-118">Notes</span></span> <br/>          | <span data-ttu-id="4cc85-119">Vinculado ao elemento PageMediaSize, opção CustomPS</span><span class="sxs-lookup"><span data-stu-id="4cc85-119">Linked to PageMediaSize element, CustomPS option</span></span><br/> |



 

## <a name="structure-content"></a><span data-ttu-id="4cc85-120">Conteúdo da estrutura</span><span class="sxs-lookup"><span data-stu-id="4cc85-120">Structure Content</span></span>

<span data-ttu-id="4cc85-121">A estrutura XML desse elemento é:</span><span class="sxs-lookup"><span data-stu-id="4cc85-121">The XML structure of this element is:</span></span>

``` syntax
<psf:ParameterDef name="psk:PageMediaSizePSWidthOffset">
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

## <a name="structure-properties"></a><span data-ttu-id="4cc85-122">Propriedades da estrutura</span><span class="sxs-lookup"><span data-stu-id="4cc85-122">Structure Properties</span></span>

<span data-ttu-id="4cc85-123">A tabela a seguir descreve as características das variáveis definidas na estrutura XML.</span><span class="sxs-lookup"><span data-stu-id="4cc85-123">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="4cc85-124">Propriedade</span><span class="sxs-lookup"><span data-stu-id="4cc85-124">Property</span></span>                | <span data-ttu-id="4cc85-125">xsi:type</span><span class="sxs-lookup"><span data-stu-id="4cc85-125">xsi:type</span></span>           | <span data-ttu-id="4cc85-126">Valor</span><span class="sxs-lookup"><span data-stu-id="4cc85-126">Value</span></span>                      |
|-------------------------|--------------------|----------------------------|
| <span data-ttu-id="4cc85-127">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="4cc85-127">DataType</span></span><br/>     | <span data-ttu-id="4cc85-128">string</span><span class="sxs-lookup"><span data-stu-id="4cc85-128">string</span></span><br/>  | <span data-ttu-id="4cc85-129">xs:integer</span><span class="sxs-lookup"><span data-stu-id="4cc85-129">xs:integer</span></span><br/>      |
| <span data-ttu-id="4cc85-130">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="4cc85-130">DefaultValue</span></span><br/> | <span data-ttu-id="4cc85-131">Número inteiro</span><span class="sxs-lookup"><span data-stu-id="4cc85-131">integer</span></span><br/> | <span data-ttu-id="4cc85-132">não definido</span><span class="sxs-lookup"><span data-stu-id="4cc85-132">undefined</span></span><br/>       |
| <span data-ttu-id="4cc85-133">MaxValue</span><span class="sxs-lookup"><span data-stu-id="4cc85-133">MaxValue</span></span><br/>     | <span data-ttu-id="4cc85-134">Número inteiro</span><span class="sxs-lookup"><span data-stu-id="4cc85-134">integer</span></span><br/> | <span data-ttu-id="4cc85-135">não definido</span><span class="sxs-lookup"><span data-stu-id="4cc85-135">undefined</span></span><br/>       |
| <span data-ttu-id="4cc85-136">Minvalue</span><span class="sxs-lookup"><span data-stu-id="4cc85-136">MinValue</span></span><br/>     | <span data-ttu-id="4cc85-137">Número inteiro</span><span class="sxs-lookup"><span data-stu-id="4cc85-137">integer</span></span><br/> | <span data-ttu-id="4cc85-138">não definido</span><span class="sxs-lookup"><span data-stu-id="4cc85-138">undefined</span></span><br/>       |
| <span data-ttu-id="4cc85-139">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="4cc85-139">Mandatory</span></span><br/>    | <span data-ttu-id="4cc85-140">string</span><span class="sxs-lookup"><span data-stu-id="4cc85-140">string</span></span><br/>  | <span data-ttu-id="4cc85-141">psk:Conditional</span><span class="sxs-lookup"><span data-stu-id="4cc85-141">psk:Conditional</span></span><br/> |
| <span data-ttu-id="4cc85-142">Vários</span><span class="sxs-lookup"><span data-stu-id="4cc85-142">Multiple</span></span><br/>     | <span data-ttu-id="4cc85-143">integer</span><span class="sxs-lookup"><span data-stu-id="4cc85-143">integer</span></span><br/> | <span data-ttu-id="4cc85-144">1</span><span class="sxs-lookup"><span data-stu-id="4cc85-144">1</span></span><br/>               |
| <span data-ttu-id="4cc85-145">Unittype</span><span class="sxs-lookup"><span data-stu-id="4cc85-145">UnitType</span></span><br/>     | <span data-ttu-id="4cc85-146">string</span><span class="sxs-lookup"><span data-stu-id="4cc85-146">string</span></span><br/>  | <span data-ttu-id="4cc85-147">Mícrons</span><span class="sxs-lookup"><span data-stu-id="4cc85-147">microns</span></span><br/>         |



 

## <a name="related-topics"></a><span data-ttu-id="4cc85-148">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="4cc85-148">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4cc85-149">PostScript Especificação de formato de arquivo de descrição da impressora</span><span class="sxs-lookup"><span data-stu-id="4cc85-149">PostScript Printer Description File Format Specification</span></span>](https://www.adobe.com/products/postscript/pdfs/PLRM.pdf)
</dt> <dt>

[<span data-ttu-id="4cc85-150">Especificação de esquema de impressão</span><span class="sxs-lookup"><span data-stu-id="4cc85-150">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




