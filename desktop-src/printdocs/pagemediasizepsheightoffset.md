---
description: Este tópico não é atual. Para obter as informações mais atuais, consulte a especificação do esquema de impressão.
ms.assetid: e86d6a5d-484d-4c80-8c86-7d12d287ee21
title: PageMediaSizePSHeightOffset
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1e2e1e0a75c5bb6ec95a611d304d575fcf91a13e
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/26/2021
ms.locfileid: "107998053"
---
# <a name="pagemediasizepsheightoffset"></a><span data-ttu-id="8cbdd-104">PageMediaSizePSHeightOffset</span><span class="sxs-lookup"><span data-stu-id="8cbdd-104">PageMediaSizePSHeightOffset</span></span>

<span data-ttu-id="8cbdd-105">Este tópico não é atual.</span><span class="sxs-lookup"><span data-stu-id="8cbdd-105">This topic is not current.</span></span> <span data-ttu-id="8cbdd-106">Para obter as informações mais atuais, consulte a [especificação do esquema de impressão](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="8cbdd-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="8cbdd-107">Especifica o deslocamento, paralelo à direção da orientação do feed (referência da [especificação de formato de arquivo de descrição de impressora PostScript](https://www.adobe.com/products/postscript/pdfs/PLRM.pdf)).</span><span class="sxs-lookup"><span data-stu-id="8cbdd-107">Specifies the offset, parallel to the feed-orientation direction (Reference [PostScript Printer Description File Format Specification](https://www.adobe.com/products/postscript/pdfs/PLRM.pdf)).</span></span>

-   [<span data-ttu-id="8cbdd-108">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="8cbdd-108">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="8cbdd-109">Conteúdo da estrutura</span><span class="sxs-lookup"><span data-stu-id="8cbdd-109">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="8cbdd-110">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="8cbdd-110">Element Information</span></span>



| <span data-ttu-id="8cbdd-111">Nome</span><span class="sxs-lookup"><span data-stu-id="8cbdd-111">Name</span></span> | <span data-ttu-id="8cbdd-112">Valor</span><span class="sxs-lookup"><span data-stu-id="8cbdd-112">Value</span></span> |
|----------------------------|-------------------------------------------------------------|
| <span data-ttu-id="8cbdd-113">Tipo de elemento</span><span class="sxs-lookup"><span data-stu-id="8cbdd-113">Element Type</span></span> <br/>   | <span data-ttu-id="8cbdd-114">ParameterDef</span><span class="sxs-lookup"><span data-stu-id="8cbdd-114">ParameterDef</span></span><br/>                                     |
| <span data-ttu-id="8cbdd-115">Prefixo de escopo</span><span class="sxs-lookup"><span data-stu-id="8cbdd-115">Scoping Prefix</span></span> <br/> | <span data-ttu-id="8cbdd-116">?</span><span class="sxs-lookup"><span data-stu-id="8cbdd-116">Page</span></span><br/>                                             |
| <span data-ttu-id="8cbdd-117">Observações</span><span class="sxs-lookup"><span data-stu-id="8cbdd-117">Notes</span></span> <br/>          | <span data-ttu-id="8cbdd-118">Vinculado ao elemento PageMediaSize, opção CustomPS</span><span class="sxs-lookup"><span data-stu-id="8cbdd-118">Linked to PageMediaSize element, CustomPS option</span></span><br/> |



 

## <a name="structure-content"></a><span data-ttu-id="8cbdd-119">Conteúdo da estrutura</span><span class="sxs-lookup"><span data-stu-id="8cbdd-119">Structure Content</span></span>

<span data-ttu-id="8cbdd-120">A estrutura XML desse elemento é:</span><span class="sxs-lookup"><span data-stu-id="8cbdd-120">The XML structure of this element is:</span></span>

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

## <a name="structure-properties"></a><span data-ttu-id="8cbdd-121">Propriedades da estrutura</span><span class="sxs-lookup"><span data-stu-id="8cbdd-121">Structure Properties</span></span>

<span data-ttu-id="8cbdd-122">A tabela a seguir descreve as características das variáveis definidas na estrutura XML.</span><span class="sxs-lookup"><span data-stu-id="8cbdd-122">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="8cbdd-123">Propriedade</span><span class="sxs-lookup"><span data-stu-id="8cbdd-123">Property</span></span>                | <span data-ttu-id="8cbdd-124">xsi:type</span><span class="sxs-lookup"><span data-stu-id="8cbdd-124">xsi:type</span></span>           | <span data-ttu-id="8cbdd-125">Valor</span><span class="sxs-lookup"><span data-stu-id="8cbdd-125">Value</span></span>                      |
|-------------------------|--------------------|----------------------------|
| <span data-ttu-id="8cbdd-126">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="8cbdd-126">DataType</span></span><br/>     | <span data-ttu-id="8cbdd-127">string</span><span class="sxs-lookup"><span data-stu-id="8cbdd-127">string</span></span><br/>  | <span data-ttu-id="8cbdd-128">xs:integer</span><span class="sxs-lookup"><span data-stu-id="8cbdd-128">xs:integer</span></span><br/>      |
| <span data-ttu-id="8cbdd-129">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="8cbdd-129">DefaultValue</span></span><br/> | <span data-ttu-id="8cbdd-130">Número inteiro</span><span class="sxs-lookup"><span data-stu-id="8cbdd-130">integer</span></span><br/> | <span data-ttu-id="8cbdd-131">não definido</span><span class="sxs-lookup"><span data-stu-id="8cbdd-131">undefined</span></span><br/>       |
| <span data-ttu-id="8cbdd-132">MaxValue</span><span class="sxs-lookup"><span data-stu-id="8cbdd-132">MaxValue</span></span><br/>     | <span data-ttu-id="8cbdd-133">Número inteiro</span><span class="sxs-lookup"><span data-stu-id="8cbdd-133">integer</span></span><br/> | <span data-ttu-id="8cbdd-134">não definido</span><span class="sxs-lookup"><span data-stu-id="8cbdd-134">undefined</span></span><br/>       |
| <span data-ttu-id="8cbdd-135">MinValue</span><span class="sxs-lookup"><span data-stu-id="8cbdd-135">MinValue</span></span><br/>     | <span data-ttu-id="8cbdd-136">Número inteiro</span><span class="sxs-lookup"><span data-stu-id="8cbdd-136">integer</span></span><br/> | <span data-ttu-id="8cbdd-137">não definido</span><span class="sxs-lookup"><span data-stu-id="8cbdd-137">undefined</span></span><br/>       |
| <span data-ttu-id="8cbdd-138">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="8cbdd-138">Mandatory</span></span><br/>    | <span data-ttu-id="8cbdd-139">string</span><span class="sxs-lookup"><span data-stu-id="8cbdd-139">string</span></span><br/>  | <span data-ttu-id="8cbdd-140">PSK: condicional</span><span class="sxs-lookup"><span data-stu-id="8cbdd-140">psk:Conditional</span></span><br/> |
| <span data-ttu-id="8cbdd-141">Vários</span><span class="sxs-lookup"><span data-stu-id="8cbdd-141">Multiple</span></span><br/>     | <span data-ttu-id="8cbdd-142">integer</span><span class="sxs-lookup"><span data-stu-id="8cbdd-142">integer</span></span><br/> | <span data-ttu-id="8cbdd-143">1</span><span class="sxs-lookup"><span data-stu-id="8cbdd-143">1</span></span><br/>               |
| <span data-ttu-id="8cbdd-144">UnitType</span><span class="sxs-lookup"><span data-stu-id="8cbdd-144">UnitType</span></span><br/>     | <span data-ttu-id="8cbdd-145">string</span><span class="sxs-lookup"><span data-stu-id="8cbdd-145">string</span></span><br/>  | <span data-ttu-id="8cbdd-146">mícrons</span><span class="sxs-lookup"><span data-stu-id="8cbdd-146">microns</span></span><br/>         |



 

## <a name="related-topics"></a><span data-ttu-id="8cbdd-147">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="8cbdd-147">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8cbdd-148">Especificação de formato de arquivo de descrição de impressora PostScript</span><span class="sxs-lookup"><span data-stu-id="8cbdd-148">PostScript Printer Description File Format Specification</span></span>](https://www.adobe.com/products/postscript/pdfs/PLRM.pdf)
</dt> <dt>

[<span data-ttu-id="8cbdd-149">Especificação de esquema de impressão</span><span class="sxs-lookup"><span data-stu-id="8cbdd-149">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




