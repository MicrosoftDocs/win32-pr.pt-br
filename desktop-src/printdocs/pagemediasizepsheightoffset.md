---
description: Obter informações sobre o parâmetro PageMediaSizePSHeightOffset. Este tópico não é atual. Para obter as informações mais atuais, consulte a Especificação de Esquema de Impressão.
ms.assetid: e86d6a5d-484d-4c80-8c86-7d12d287ee21
title: PageMediaSizePSHeightOffset
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b5e2c0e3802a6c461fe2f9eec68b28677c254be9
ms.sourcegitcommit: 91530c19d26ba4c57a6af1f37b57f211f580464e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/19/2021
ms.locfileid: "112395731"
---
# <a name="pagemediasizepsheightoffset"></a><span data-ttu-id="d1def-105">PageMediaSizePSHeightOffset</span><span class="sxs-lookup"><span data-stu-id="d1def-105">PageMediaSizePSHeightOffset</span></span>

<span data-ttu-id="d1def-106">Este tópico não é atual.</span><span class="sxs-lookup"><span data-stu-id="d1def-106">This topic is not current.</span></span> <span data-ttu-id="d1def-107">Para obter as informações mais atuais, consulte a [Especificação de Esquema de Impressão](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="d1def-107">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="d1def-108">Especifica o deslocamento, paralelo à direção da orientação do feed (Referência à Especificação de Formato de Arquivo de Descrição da Impressora [PostScript](https://www.adobe.com/products/postscript/pdfs/PLRM.pdf)).</span><span class="sxs-lookup"><span data-stu-id="d1def-108">Specifies the offset, parallel to the feed-orientation direction (Reference [PostScript Printer Description File Format Specification](https://www.adobe.com/products/postscript/pdfs/PLRM.pdf)).</span></span>

-   [<span data-ttu-id="d1def-109">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="d1def-109">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="d1def-110">Conteúdo da estrutura</span><span class="sxs-lookup"><span data-stu-id="d1def-110">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="d1def-111">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="d1def-111">Element Information</span></span>



| <span data-ttu-id="d1def-112">Name</span><span class="sxs-lookup"><span data-stu-id="d1def-112">Name</span></span> | <span data-ttu-id="d1def-113">Valor</span><span class="sxs-lookup"><span data-stu-id="d1def-113">Value</span></span> |
|----------------------------|-------------------------------------------------------------|
| <span data-ttu-id="d1def-114">Tipo de elemento</span><span class="sxs-lookup"><span data-stu-id="d1def-114">Element Type</span></span> <br/>   | <span data-ttu-id="d1def-115">ParameterDef</span><span class="sxs-lookup"><span data-stu-id="d1def-115">ParameterDef</span></span><br/>                                     |
| <span data-ttu-id="d1def-116">Prefixo de definição de scoping</span><span class="sxs-lookup"><span data-stu-id="d1def-116">Scoping Prefix</span></span> <br/> | <span data-ttu-id="d1def-117">?</span><span class="sxs-lookup"><span data-stu-id="d1def-117">Page</span></span><br/>                                             |
| <span data-ttu-id="d1def-118">Observações</span><span class="sxs-lookup"><span data-stu-id="d1def-118">Notes</span></span> <br/>          | <span data-ttu-id="d1def-119">Vinculado ao elemento PageMediaSize, opção CustomPS</span><span class="sxs-lookup"><span data-stu-id="d1def-119">Linked to PageMediaSize element, CustomPS option</span></span><br/> |



 

## <a name="structure-content"></a><span data-ttu-id="d1def-120">Conteúdo da estrutura</span><span class="sxs-lookup"><span data-stu-id="d1def-120">Structure Content</span></span>

<span data-ttu-id="d1def-121">A estrutura XML desse elemento é:</span><span class="sxs-lookup"><span data-stu-id="d1def-121">The XML structure of this element is:</span></span>

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

## <a name="structure-properties"></a><span data-ttu-id="d1def-122">Propriedades da estrutura</span><span class="sxs-lookup"><span data-stu-id="d1def-122">Structure Properties</span></span>

<span data-ttu-id="d1def-123">A tabela a seguir descreve as características das variáveis definidas na estrutura XML.</span><span class="sxs-lookup"><span data-stu-id="d1def-123">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="d1def-124">Propriedade</span><span class="sxs-lookup"><span data-stu-id="d1def-124">Property</span></span>                | <span data-ttu-id="d1def-125">xsi:type</span><span class="sxs-lookup"><span data-stu-id="d1def-125">xsi:type</span></span>           | <span data-ttu-id="d1def-126">Valor</span><span class="sxs-lookup"><span data-stu-id="d1def-126">Value</span></span>                      |
|-------------------------|--------------------|----------------------------|
| <span data-ttu-id="d1def-127">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="d1def-127">DataType</span></span><br/>     | <span data-ttu-id="d1def-128">string</span><span class="sxs-lookup"><span data-stu-id="d1def-128">string</span></span><br/>  | <span data-ttu-id="d1def-129">xs:integer</span><span class="sxs-lookup"><span data-stu-id="d1def-129">xs:integer</span></span><br/>      |
| <span data-ttu-id="d1def-130">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="d1def-130">DefaultValue</span></span><br/> | <span data-ttu-id="d1def-131">Número inteiro</span><span class="sxs-lookup"><span data-stu-id="d1def-131">integer</span></span><br/> | <span data-ttu-id="d1def-132">não definido</span><span class="sxs-lookup"><span data-stu-id="d1def-132">undefined</span></span><br/>       |
| <span data-ttu-id="d1def-133">MaxValue</span><span class="sxs-lookup"><span data-stu-id="d1def-133">MaxValue</span></span><br/>     | <span data-ttu-id="d1def-134">Número inteiro</span><span class="sxs-lookup"><span data-stu-id="d1def-134">integer</span></span><br/> | <span data-ttu-id="d1def-135">não definido</span><span class="sxs-lookup"><span data-stu-id="d1def-135">undefined</span></span><br/>       |
| <span data-ttu-id="d1def-136">Minvalue</span><span class="sxs-lookup"><span data-stu-id="d1def-136">MinValue</span></span><br/>     | <span data-ttu-id="d1def-137">Número inteiro</span><span class="sxs-lookup"><span data-stu-id="d1def-137">integer</span></span><br/> | <span data-ttu-id="d1def-138">não definido</span><span class="sxs-lookup"><span data-stu-id="d1def-138">undefined</span></span><br/>       |
| <span data-ttu-id="d1def-139">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="d1def-139">Mandatory</span></span><br/>    | <span data-ttu-id="d1def-140">string</span><span class="sxs-lookup"><span data-stu-id="d1def-140">string</span></span><br/>  | <span data-ttu-id="d1def-141">psk:Conditional</span><span class="sxs-lookup"><span data-stu-id="d1def-141">psk:Conditional</span></span><br/> |
| <span data-ttu-id="d1def-142">Vários</span><span class="sxs-lookup"><span data-stu-id="d1def-142">Multiple</span></span><br/>     | <span data-ttu-id="d1def-143">integer</span><span class="sxs-lookup"><span data-stu-id="d1def-143">integer</span></span><br/> | <span data-ttu-id="d1def-144">1</span><span class="sxs-lookup"><span data-stu-id="d1def-144">1</span></span><br/>               |
| <span data-ttu-id="d1def-145">Unittype</span><span class="sxs-lookup"><span data-stu-id="d1def-145">UnitType</span></span><br/>     | <span data-ttu-id="d1def-146">string</span><span class="sxs-lookup"><span data-stu-id="d1def-146">string</span></span><br/>  | <span data-ttu-id="d1def-147">Mícrons</span><span class="sxs-lookup"><span data-stu-id="d1def-147">microns</span></span><br/>         |



 

## <a name="related-topics"></a><span data-ttu-id="d1def-148">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="d1def-148">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d1def-149">Especificação de formato de arquivo de descrição da impressora PostScript</span><span class="sxs-lookup"><span data-stu-id="d1def-149">PostScript Printer Description File Format Specification</span></span>](https://www.adobe.com/products/postscript/pdfs/PLRM.pdf)
</dt> <dt>

[<span data-ttu-id="d1def-150">Especificação de esquema de impressão</span><span class="sxs-lookup"><span data-stu-id="d1def-150">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




