---
description: Este tópico não é atual. Para obter as informações mais atuais, consulte a especificação do esquema de impressão.
ms.assetid: a15fe075-6696-4c70-b658-ae62d542bb4e
title: PageCopies
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b6feef0745e3f9a86b3697b7e0ab65111fc3dfcb
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/05/2021
ms.locfileid: "104172553"
---
# <a name="pagecopies"></a><span data-ttu-id="3521c-104">PageCopies</span><span class="sxs-lookup"><span data-stu-id="3521c-104">PageCopies</span></span>

<span data-ttu-id="3521c-105">Este tópico não é atual.</span><span class="sxs-lookup"><span data-stu-id="3521c-105">This topic is not current.</span></span> <span data-ttu-id="3521c-106">Para obter as informações mais atuais, consulte a [especificação do esquema de impressão](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="3521c-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="3521c-107">Especifica o número de cópias de uma página.</span><span class="sxs-lookup"><span data-stu-id="3521c-107">Specifies the number of copies of a page.</span></span>

-   [<span data-ttu-id="3521c-108">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="3521c-108">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="3521c-109">Conteúdo da estrutura</span><span class="sxs-lookup"><span data-stu-id="3521c-109">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="3521c-110">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="3521c-110">Element Information</span></span>



| <span data-ttu-id="3521c-111">Nome</span><span class="sxs-lookup"><span data-stu-id="3521c-111">Name</span></span>                       |                         |
|----------------------------|-------------------------|
| <span data-ttu-id="3521c-112">Tipo de elemento</span><span class="sxs-lookup"><span data-stu-id="3521c-112">Element Type</span></span> <br/>   | <span data-ttu-id="3521c-113">ParameterDef</span><span class="sxs-lookup"><span data-stu-id="3521c-113">ParameterDef</span></span><br/> |
| <span data-ttu-id="3521c-114">Prefixo de escopo</span><span class="sxs-lookup"><span data-stu-id="3521c-114">Scoping Prefix</span></span> <br/> | <span data-ttu-id="3521c-115">?</span><span class="sxs-lookup"><span data-stu-id="3521c-115">Page</span></span><br/>         |
| <span data-ttu-id="3521c-116">Observações</span><span class="sxs-lookup"><span data-stu-id="3521c-116">Notes</span></span> <br/>          | <span data-ttu-id="3521c-117">Nenhum</span><span class="sxs-lookup"><span data-stu-id="3521c-117">None</span></span><br/>         |



 

## <a name="structure-content"></a><span data-ttu-id="3521c-118">Conteúdo da estrutura</span><span class="sxs-lookup"><span data-stu-id="3521c-118">Structure Content</span></span>

<span data-ttu-id="3521c-119">A estrutura XML desse elemento é:</span><span class="sxs-lookup"><span data-stu-id="3521c-119">The XML structure of this element is:</span></span>

``` syntax
<psf:ParameterDef name="psk:PageCopies">
  <psf:Property name="psf:DataType">
    <psf:Value xsi:type="xs:string">xs:integer</psf:Value>
  </psf:Property>
  <psf:Property name="psf:DefaultValue">
    <psf:Value xsi:type="xs:integer">1</psf:Value>
  </psf:Property>
  <psf:Property name="psf:MaxValue">
    <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
  </psf:Property>
  <psf:Property name="psf:MinValue">
    <psf:Value xsi:type="xs:integer">1</psf:Value>
  </psf:Property>
  <psf:Property name="psf:Multiple">
    <psf:Value xsi:type="xs:integer">1</psf:Value>
  </psf:Property>
  <psf:Property name="psf:Mandatory">
    <psf:Value xsi:type="xs:string">psk:Unconditional</psf:Value>
  </psf:Property>
  <psf:Property name="psf:UnitType">
    <psf:Value xsi:type="xs:string">copies</psf:Value>
  </psf:Property>
</psf:ParameterDef>
      
```

## <a name="structure-properties"></a><span data-ttu-id="3521c-120">Propriedades da estrutura</span><span class="sxs-lookup"><span data-stu-id="3521c-120">Structure Properties</span></span>

<span data-ttu-id="3521c-121">A tabela a seguir descreve as características das variáveis definidas na estrutura XML.</span><span class="sxs-lookup"><span data-stu-id="3521c-121">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="3521c-122">Propriedade</span><span class="sxs-lookup"><span data-stu-id="3521c-122">Property</span></span>                | <span data-ttu-id="3521c-123">xsi:type</span><span class="sxs-lookup"><span data-stu-id="3521c-123">xsi:type</span></span>           | <span data-ttu-id="3521c-124">Valor</span><span class="sxs-lookup"><span data-stu-id="3521c-124">Value</span></span>                        |
|-------------------------|--------------------|------------------------------|
| <span data-ttu-id="3521c-125">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="3521c-125">DataType</span></span><br/>     | <span data-ttu-id="3521c-126">string</span><span class="sxs-lookup"><span data-stu-id="3521c-126">string</span></span><br/>  | <span data-ttu-id="3521c-127">xs:integer</span><span class="sxs-lookup"><span data-stu-id="3521c-127">xs:integer</span></span><br/>        |
| <span data-ttu-id="3521c-128">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="3521c-128">DefaultValue</span></span><br/> | <span data-ttu-id="3521c-129">integer</span><span class="sxs-lookup"><span data-stu-id="3521c-129">integer</span></span><br/> | <span data-ttu-id="3521c-130">1</span><span class="sxs-lookup"><span data-stu-id="3521c-130">1</span></span><br/>                 |
| <span data-ttu-id="3521c-131">MaxValue</span><span class="sxs-lookup"><span data-stu-id="3521c-131">MaxValue</span></span><br/>     | <span data-ttu-id="3521c-132">Número inteiro</span><span class="sxs-lookup"><span data-stu-id="3521c-132">integer</span></span><br/> | <span data-ttu-id="3521c-133">não definido</span><span class="sxs-lookup"><span data-stu-id="3521c-133">undefined</span></span><br/>         |
| <span data-ttu-id="3521c-134">MinValue</span><span class="sxs-lookup"><span data-stu-id="3521c-134">MinValue</span></span><br/>     | <span data-ttu-id="3521c-135">integer</span><span class="sxs-lookup"><span data-stu-id="3521c-135">integer</span></span><br/> | <span data-ttu-id="3521c-136">1</span><span class="sxs-lookup"><span data-stu-id="3521c-136">1</span></span><br/>                 |
| <span data-ttu-id="3521c-137">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="3521c-137">Mandatory</span></span><br/>    | <span data-ttu-id="3521c-138">string</span><span class="sxs-lookup"><span data-stu-id="3521c-138">string</span></span><br/>  | <span data-ttu-id="3521c-139">PSK: incondicional</span><span class="sxs-lookup"><span data-stu-id="3521c-139">psk:Unconditional</span></span><br/> |
| <span data-ttu-id="3521c-140">Vários</span><span class="sxs-lookup"><span data-stu-id="3521c-140">Multiple</span></span><br/>     | <span data-ttu-id="3521c-141">integer</span><span class="sxs-lookup"><span data-stu-id="3521c-141">integer</span></span><br/> | <span data-ttu-id="3521c-142">1</span><span class="sxs-lookup"><span data-stu-id="3521c-142">1</span></span><br/>                 |
| <span data-ttu-id="3521c-143">UnitType</span><span class="sxs-lookup"><span data-stu-id="3521c-143">UnitType</span></span><br/>     | <span data-ttu-id="3521c-144">string</span><span class="sxs-lookup"><span data-stu-id="3521c-144">string</span></span><br/>  | <span data-ttu-id="3521c-145">cópia</span><span class="sxs-lookup"><span data-stu-id="3521c-145">copies</span></span><br/>            |



 

## <a name="related-topics"></a><span data-ttu-id="3521c-146">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="3521c-146">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3521c-147">Especificação de esquema de impressão</span><span class="sxs-lookup"><span data-stu-id="3521c-147">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




