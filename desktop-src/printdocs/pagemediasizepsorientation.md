---
description: Este tópico não é atual. Para obter as informações mais atuais, consulte a especificação do esquema de impressão.
ms.assetid: b091c250-66f2-47cc-a012-1526c0ed02c9
title: PageMediaSizePSOrientation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d16a9a2e59ebffb41ad7c9a9c16eaf41497ade62
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/26/2021
ms.locfileid: "107997553"
---
# <a name="pagemediasizepsorientation"></a><span data-ttu-id="0f2e7-104">PageMediaSizePSOrientation</span><span class="sxs-lookup"><span data-stu-id="0f2e7-104">PageMediaSizePSOrientation</span></span>

<span data-ttu-id="0f2e7-105">Este tópico não é atual.</span><span class="sxs-lookup"><span data-stu-id="0f2e7-105">This topic is not current.</span></span> <span data-ttu-id="0f2e7-106">Para obter as informações mais atuais, consulte a [especificação do esquema de impressão](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="0f2e7-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="0f2e7-107">Especifica a orientação relativa à direção da orientação do feed (referência à [especificação de formato de arquivo de descrição de impressora PostScript](https://www.adobe.com/products/postscript/pdfs/PLRM.pdf)).</span><span class="sxs-lookup"><span data-stu-id="0f2e7-107">Specifies the orientation relative to the feed-orientation direction (Reference [PostScript Printer Description File Format Specification](https://www.adobe.com/products/postscript/pdfs/PLRM.pdf)).</span></span>

-   [<span data-ttu-id="0f2e7-108">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="0f2e7-108">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="0f2e7-109">Conteúdo da estrutura</span><span class="sxs-lookup"><span data-stu-id="0f2e7-109">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="0f2e7-110">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="0f2e7-110">Element Information</span></span>



| <span data-ttu-id="0f2e7-111">Nome</span><span class="sxs-lookup"><span data-stu-id="0f2e7-111">Name</span></span> | <span data-ttu-id="0f2e7-112">Valor</span><span class="sxs-lookup"><span data-stu-id="0f2e7-112">Value</span></span> |
|----------------------------|-------------------------------------------------------------|
| <span data-ttu-id="0f2e7-113">Tipo de elemento</span><span class="sxs-lookup"><span data-stu-id="0f2e7-113">Element Type</span></span> <br/>   | <span data-ttu-id="0f2e7-114">ParameterDef</span><span class="sxs-lookup"><span data-stu-id="0f2e7-114">ParameterDef</span></span><br/>                                     |
| <span data-ttu-id="0f2e7-115">Prefixo de escopo</span><span class="sxs-lookup"><span data-stu-id="0f2e7-115">Scoping Prefix</span></span> <br/> | <span data-ttu-id="0f2e7-116">?</span><span class="sxs-lookup"><span data-stu-id="0f2e7-116">Page</span></span><br/>                                             |
| <span data-ttu-id="0f2e7-117">Observações</span><span class="sxs-lookup"><span data-stu-id="0f2e7-117">Notes</span></span> <br/>          | <span data-ttu-id="0f2e7-118">Vinculado ao elemento PageMediaSize, opção CustomPS</span><span class="sxs-lookup"><span data-stu-id="0f2e7-118">Linked to PageMediaSize element, CustomPS option</span></span><br/> |



 

## <a name="structure-content"></a><span data-ttu-id="0f2e7-119">Conteúdo da estrutura</span><span class="sxs-lookup"><span data-stu-id="0f2e7-119">Structure Content</span></span>

<span data-ttu-id="0f2e7-120">A estrutura XML desse elemento é:</span><span class="sxs-lookup"><span data-stu-id="0f2e7-120">The XML structure of this element is:</span></span>

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

## <a name="structure-properties"></a><span data-ttu-id="0f2e7-121">Propriedades da estrutura</span><span class="sxs-lookup"><span data-stu-id="0f2e7-121">Structure Properties</span></span>

<span data-ttu-id="0f2e7-122">A tabela a seguir descreve as características das variáveis definidas na estrutura XML.</span><span class="sxs-lookup"><span data-stu-id="0f2e7-122">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="0f2e7-123">Propriedade</span><span class="sxs-lookup"><span data-stu-id="0f2e7-123">Property</span></span>                | <span data-ttu-id="0f2e7-124">xsi:type</span><span class="sxs-lookup"><span data-stu-id="0f2e7-124">xsi:type</span></span>           | <span data-ttu-id="0f2e7-125">Valor</span><span class="sxs-lookup"><span data-stu-id="0f2e7-125">Value</span></span>                        |
|-------------------------|--------------------|------------------------------|
| <span data-ttu-id="0f2e7-126">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="0f2e7-126">DataType</span></span><br/>     | <span data-ttu-id="0f2e7-127">string</span><span class="sxs-lookup"><span data-stu-id="0f2e7-127">string</span></span><br/>  | <span data-ttu-id="0f2e7-128">xs:integer</span><span class="sxs-lookup"><span data-stu-id="0f2e7-128">xs:integer</span></span><br/>        |
| <span data-ttu-id="0f2e7-129">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="0f2e7-129">DefaultValue</span></span><br/> | <span data-ttu-id="0f2e7-130">integer</span><span class="sxs-lookup"><span data-stu-id="0f2e7-130">integer</span></span><br/> | <span data-ttu-id="0f2e7-131">0</span><span class="sxs-lookup"><span data-stu-id="0f2e7-131">0</span></span><br/>                 |
| <span data-ttu-id="0f2e7-132">MaxValue</span><span class="sxs-lookup"><span data-stu-id="0f2e7-132">MaxValue</span></span><br/>     | <span data-ttu-id="0f2e7-133">Número inteiro</span><span class="sxs-lookup"><span data-stu-id="0f2e7-133">integer</span></span><br/> | <span data-ttu-id="0f2e7-134">3</span><span class="sxs-lookup"><span data-stu-id="0f2e7-134">3</span></span><br/>                 |
| <span data-ttu-id="0f2e7-135">MinValue</span><span class="sxs-lookup"><span data-stu-id="0f2e7-135">MinValue</span></span><br/>     | <span data-ttu-id="0f2e7-136">integer</span><span class="sxs-lookup"><span data-stu-id="0f2e7-136">integer</span></span><br/> | <span data-ttu-id="0f2e7-137">0</span><span class="sxs-lookup"><span data-stu-id="0f2e7-137">0</span></span><br/>                 |
| <span data-ttu-id="0f2e7-138">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="0f2e7-138">Mandatory</span></span><br/>    | <span data-ttu-id="0f2e7-139">string</span><span class="sxs-lookup"><span data-stu-id="0f2e7-139">string</span></span><br/>  | <span data-ttu-id="0f2e7-140">PSK: condicional</span><span class="sxs-lookup"><span data-stu-id="0f2e7-140">psk:Conditional</span></span><br/>   |
| <span data-ttu-id="0f2e7-141">Vários</span><span class="sxs-lookup"><span data-stu-id="0f2e7-141">Multiple</span></span><br/>     | <span data-ttu-id="0f2e7-142">integer</span><span class="sxs-lookup"><span data-stu-id="0f2e7-142">integer</span></span><br/> | <span data-ttu-id="0f2e7-143">1</span><span class="sxs-lookup"><span data-stu-id="0f2e7-143">1</span></span><br/>                 |
| <span data-ttu-id="0f2e7-144">UnitType</span><span class="sxs-lookup"><span data-stu-id="0f2e7-144">UnitType</span></span><br/>     | <span data-ttu-id="0f2e7-145">string</span><span class="sxs-lookup"><span data-stu-id="0f2e7-145">string</span></span><br/>  | <span data-ttu-id="0f2e7-146">PageMediaSizeEnum</span><span class="sxs-lookup"><span data-stu-id="0f2e7-146">PageMediaSizeEnum</span></span><br/> |



 

## <a name="related-topics"></a><span data-ttu-id="0f2e7-147">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="0f2e7-147">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0f2e7-148">Especificação de formato de arquivo de descrição de impressora PostScript</span><span class="sxs-lookup"><span data-stu-id="0f2e7-148">PostScript Printer Description File Format Specification</span></span>](https://www.adobe.com/products/postscript/pdfs/PLRM.pdf)
</dt> <dt>

[<span data-ttu-id="0f2e7-149">Especificação de esquema de impressão</span><span class="sxs-lookup"><span data-stu-id="0f2e7-149">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




