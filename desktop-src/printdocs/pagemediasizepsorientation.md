---
description: Obtenha informações sobre o parâmetro PageMediaSizePSOrientation. Este tópico não é atual. Para obter as informações mais atuais, consulte a especificação do esquema de impressão.
ms.assetid: b091c250-66f2-47cc-a012-1526c0ed02c9
title: PageMediaSizePSOrientation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: adb1b3aff1099199a98d6c8be899824dd1a1f17c
ms.sourcegitcommit: 91530c19d26ba4c57a6af1f37b57f211f580464e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/19/2021
ms.locfileid: "112395721"
---
# <a name="pagemediasizepsorientation"></a><span data-ttu-id="1e5f1-105">PageMediaSizePSOrientation</span><span class="sxs-lookup"><span data-stu-id="1e5f1-105">PageMediaSizePSOrientation</span></span>

<span data-ttu-id="1e5f1-106">Este tópico não é atual.</span><span class="sxs-lookup"><span data-stu-id="1e5f1-106">This topic is not current.</span></span> <span data-ttu-id="1e5f1-107">Para obter as informações mais atuais, consulte a [especificação do esquema de impressão](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="1e5f1-107">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="1e5f1-108">Especifica a orientação relativa à direção da orientação do feed (referência à [especificação de formato de arquivo de descrição de impressora PostScript](https://www.adobe.com/products/postscript/pdfs/PLRM.pdf)).</span><span class="sxs-lookup"><span data-stu-id="1e5f1-108">Specifies the orientation relative to the feed-orientation direction (Reference [PostScript Printer Description File Format Specification](https://www.adobe.com/products/postscript/pdfs/PLRM.pdf)).</span></span>

-   [<span data-ttu-id="1e5f1-109">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="1e5f1-109">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="1e5f1-110">Conteúdo da estrutura</span><span class="sxs-lookup"><span data-stu-id="1e5f1-110">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="1e5f1-111">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="1e5f1-111">Element Information</span></span>



| <span data-ttu-id="1e5f1-112">Name</span><span class="sxs-lookup"><span data-stu-id="1e5f1-112">Name</span></span> | <span data-ttu-id="1e5f1-113">Valor</span><span class="sxs-lookup"><span data-stu-id="1e5f1-113">Value</span></span> |
|----------------------------|-------------------------------------------------------------|
| <span data-ttu-id="1e5f1-114">Tipo de elemento</span><span class="sxs-lookup"><span data-stu-id="1e5f1-114">Element Type</span></span> <br/>   | <span data-ttu-id="1e5f1-115">ParameterDef</span><span class="sxs-lookup"><span data-stu-id="1e5f1-115">ParameterDef</span></span><br/>                                     |
| <span data-ttu-id="1e5f1-116">Prefixo de escopo</span><span class="sxs-lookup"><span data-stu-id="1e5f1-116">Scoping Prefix</span></span> <br/> | <span data-ttu-id="1e5f1-117">?</span><span class="sxs-lookup"><span data-stu-id="1e5f1-117">Page</span></span><br/>                                             |
| <span data-ttu-id="1e5f1-118">Observações</span><span class="sxs-lookup"><span data-stu-id="1e5f1-118">Notes</span></span> <br/>          | <span data-ttu-id="1e5f1-119">Vinculado ao elemento PageMediaSize, opção CustomPS</span><span class="sxs-lookup"><span data-stu-id="1e5f1-119">Linked to PageMediaSize element, CustomPS option</span></span><br/> |



 

## <a name="structure-content"></a><span data-ttu-id="1e5f1-120">Conteúdo da estrutura</span><span class="sxs-lookup"><span data-stu-id="1e5f1-120">Structure Content</span></span>

<span data-ttu-id="1e5f1-121">A estrutura XML desse elemento é:</span><span class="sxs-lookup"><span data-stu-id="1e5f1-121">The XML structure of this element is:</span></span>

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

## <a name="structure-properties"></a><span data-ttu-id="1e5f1-122">Propriedades da estrutura</span><span class="sxs-lookup"><span data-stu-id="1e5f1-122">Structure Properties</span></span>

<span data-ttu-id="1e5f1-123">A tabela a seguir descreve as características das variáveis definidas na estrutura XML.</span><span class="sxs-lookup"><span data-stu-id="1e5f1-123">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="1e5f1-124">Propriedade</span><span class="sxs-lookup"><span data-stu-id="1e5f1-124">Property</span></span>                | <span data-ttu-id="1e5f1-125">xsi:type</span><span class="sxs-lookup"><span data-stu-id="1e5f1-125">xsi:type</span></span>           | <span data-ttu-id="1e5f1-126">Valor</span><span class="sxs-lookup"><span data-stu-id="1e5f1-126">Value</span></span>                        |
|-------------------------|--------------------|------------------------------|
| <span data-ttu-id="1e5f1-127">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="1e5f1-127">DataType</span></span><br/>     | <span data-ttu-id="1e5f1-128">string</span><span class="sxs-lookup"><span data-stu-id="1e5f1-128">string</span></span><br/>  | <span data-ttu-id="1e5f1-129">xs:integer</span><span class="sxs-lookup"><span data-stu-id="1e5f1-129">xs:integer</span></span><br/>        |
| <span data-ttu-id="1e5f1-130">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="1e5f1-130">DefaultValue</span></span><br/> | <span data-ttu-id="1e5f1-131">inteiro</span><span class="sxs-lookup"><span data-stu-id="1e5f1-131">integer</span></span><br/> | <span data-ttu-id="1e5f1-132">0</span><span class="sxs-lookup"><span data-stu-id="1e5f1-132">0</span></span><br/>                 |
| <span data-ttu-id="1e5f1-133">MaxValue</span><span class="sxs-lookup"><span data-stu-id="1e5f1-133">MaxValue</span></span><br/>     | <span data-ttu-id="1e5f1-134">Número inteiro</span><span class="sxs-lookup"><span data-stu-id="1e5f1-134">integer</span></span><br/> | <span data-ttu-id="1e5f1-135">3</span><span class="sxs-lookup"><span data-stu-id="1e5f1-135">3</span></span><br/>                 |
| <span data-ttu-id="1e5f1-136">MinValue</span><span class="sxs-lookup"><span data-stu-id="1e5f1-136">MinValue</span></span><br/>     | <span data-ttu-id="1e5f1-137">inteiro</span><span class="sxs-lookup"><span data-stu-id="1e5f1-137">integer</span></span><br/> | <span data-ttu-id="1e5f1-138">0</span><span class="sxs-lookup"><span data-stu-id="1e5f1-138">0</span></span><br/>                 |
| <span data-ttu-id="1e5f1-139">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="1e5f1-139">Mandatory</span></span><br/>    | <span data-ttu-id="1e5f1-140">string</span><span class="sxs-lookup"><span data-stu-id="1e5f1-140">string</span></span><br/>  | <span data-ttu-id="1e5f1-141">PSK: condicional</span><span class="sxs-lookup"><span data-stu-id="1e5f1-141">psk:Conditional</span></span><br/>   |
| <span data-ttu-id="1e5f1-142">Vários</span><span class="sxs-lookup"><span data-stu-id="1e5f1-142">Multiple</span></span><br/>     | <span data-ttu-id="1e5f1-143">integer</span><span class="sxs-lookup"><span data-stu-id="1e5f1-143">integer</span></span><br/> | <span data-ttu-id="1e5f1-144">1</span><span class="sxs-lookup"><span data-stu-id="1e5f1-144">1</span></span><br/>                 |
| <span data-ttu-id="1e5f1-145">UnitType</span><span class="sxs-lookup"><span data-stu-id="1e5f1-145">UnitType</span></span><br/>     | <span data-ttu-id="1e5f1-146">string</span><span class="sxs-lookup"><span data-stu-id="1e5f1-146">string</span></span><br/>  | <span data-ttu-id="1e5f1-147">PageMediaSizeEnum</span><span class="sxs-lookup"><span data-stu-id="1e5f1-147">PageMediaSizeEnum</span></span><br/> |



 

## <a name="related-topics"></a><span data-ttu-id="1e5f1-148">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="1e5f1-148">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1e5f1-149">Especificação de formato de arquivo de descrição de impressora PostScript</span><span class="sxs-lookup"><span data-stu-id="1e5f1-149">PostScript Printer Description File Format Specification</span></span>](https://www.adobe.com/products/postscript/pdfs/PLRM.pdf)
</dt> <dt>

[<span data-ttu-id="1e5f1-150">Especificação de esquema de impressão</span><span class="sxs-lookup"><span data-stu-id="1e5f1-150">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




