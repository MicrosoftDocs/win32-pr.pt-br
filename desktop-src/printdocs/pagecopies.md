---
description: Leia informações de referência sobre o parâmetro PageCopies. Este tópico não é atual. Para obter as informações mais atuais, consulte a especificação do esquema de impressão.
ms.assetid: a15fe075-6696-4c70-b658-ae62d542bb4e
title: PageCopies
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5002850fa1df5a86b0022a941e3b2a1f7e414a44
ms.sourcegitcommit: 91530c19d26ba4c57a6af1f37b57f211f580464e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/19/2021
ms.locfileid: "112396681"
---
# <a name="pagecopies"></a><span data-ttu-id="e8098-105">PageCopies</span><span class="sxs-lookup"><span data-stu-id="e8098-105">PageCopies</span></span>

<span data-ttu-id="e8098-106">Este tópico não é atual.</span><span class="sxs-lookup"><span data-stu-id="e8098-106">This topic is not current.</span></span> <span data-ttu-id="e8098-107">Para obter as informações mais atuais, consulte a [especificação do esquema de impressão](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="e8098-107">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="e8098-108">Especifica o número de cópias de uma página.</span><span class="sxs-lookup"><span data-stu-id="e8098-108">Specifies the number of copies of a page.</span></span>

-   [<span data-ttu-id="e8098-109">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="e8098-109">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="e8098-110">Conteúdo da estrutura</span><span class="sxs-lookup"><span data-stu-id="e8098-110">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="e8098-111">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="e8098-111">Element Information</span></span>



| <span data-ttu-id="e8098-112">Name</span><span class="sxs-lookup"><span data-stu-id="e8098-112">Name</span></span> | <span data-ttu-id="e8098-113">Valor</span><span class="sxs-lookup"><span data-stu-id="e8098-113">Value</span></span> |
|----------------------------|-------------------------|
| <span data-ttu-id="e8098-114">Tipo de elemento</span><span class="sxs-lookup"><span data-stu-id="e8098-114">Element Type</span></span> <br/>   | <span data-ttu-id="e8098-115">ParameterDef</span><span class="sxs-lookup"><span data-stu-id="e8098-115">ParameterDef</span></span><br/> |
| <span data-ttu-id="e8098-116">Prefixo de escopo</span><span class="sxs-lookup"><span data-stu-id="e8098-116">Scoping Prefix</span></span> <br/> | <span data-ttu-id="e8098-117">?</span><span class="sxs-lookup"><span data-stu-id="e8098-117">Page</span></span><br/>         |
| <span data-ttu-id="e8098-118">Observações</span><span class="sxs-lookup"><span data-stu-id="e8098-118">Notes</span></span> <br/>          | <span data-ttu-id="e8098-119">Nenhum</span><span class="sxs-lookup"><span data-stu-id="e8098-119">None</span></span><br/>         |



 

## <a name="structure-content"></a><span data-ttu-id="e8098-120">Conteúdo da estrutura</span><span class="sxs-lookup"><span data-stu-id="e8098-120">Structure Content</span></span>

<span data-ttu-id="e8098-121">A estrutura XML desse elemento é:</span><span class="sxs-lookup"><span data-stu-id="e8098-121">The XML structure of this element is:</span></span>

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

## <a name="structure-properties"></a><span data-ttu-id="e8098-122">Propriedades da estrutura</span><span class="sxs-lookup"><span data-stu-id="e8098-122">Structure Properties</span></span>

<span data-ttu-id="e8098-123">A tabela a seguir descreve as características das variáveis definidas na estrutura XML.</span><span class="sxs-lookup"><span data-stu-id="e8098-123">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="e8098-124">Propriedade</span><span class="sxs-lookup"><span data-stu-id="e8098-124">Property</span></span>                | <span data-ttu-id="e8098-125">xsi:type</span><span class="sxs-lookup"><span data-stu-id="e8098-125">xsi:type</span></span>           | <span data-ttu-id="e8098-126">Valor</span><span class="sxs-lookup"><span data-stu-id="e8098-126">Value</span></span>                        |
|-------------------------|--------------------|------------------------------|
| <span data-ttu-id="e8098-127">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="e8098-127">DataType</span></span><br/>     | <span data-ttu-id="e8098-128">string</span><span class="sxs-lookup"><span data-stu-id="e8098-128">string</span></span><br/>  | <span data-ttu-id="e8098-129">xs:integer</span><span class="sxs-lookup"><span data-stu-id="e8098-129">xs:integer</span></span><br/>        |
| <span data-ttu-id="e8098-130">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="e8098-130">DefaultValue</span></span><br/> | <span data-ttu-id="e8098-131">integer</span><span class="sxs-lookup"><span data-stu-id="e8098-131">integer</span></span><br/> | <span data-ttu-id="e8098-132">1</span><span class="sxs-lookup"><span data-stu-id="e8098-132">1</span></span><br/>                 |
| <span data-ttu-id="e8098-133">MaxValue</span><span class="sxs-lookup"><span data-stu-id="e8098-133">MaxValue</span></span><br/>     | <span data-ttu-id="e8098-134">Número inteiro</span><span class="sxs-lookup"><span data-stu-id="e8098-134">integer</span></span><br/> | <span data-ttu-id="e8098-135">não definido</span><span class="sxs-lookup"><span data-stu-id="e8098-135">undefined</span></span><br/>         |
| <span data-ttu-id="e8098-136">MinValue</span><span class="sxs-lookup"><span data-stu-id="e8098-136">MinValue</span></span><br/>     | <span data-ttu-id="e8098-137">integer</span><span class="sxs-lookup"><span data-stu-id="e8098-137">integer</span></span><br/> | <span data-ttu-id="e8098-138">1</span><span class="sxs-lookup"><span data-stu-id="e8098-138">1</span></span><br/>                 |
| <span data-ttu-id="e8098-139">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="e8098-139">Mandatory</span></span><br/>    | <span data-ttu-id="e8098-140">string</span><span class="sxs-lookup"><span data-stu-id="e8098-140">string</span></span><br/>  | <span data-ttu-id="e8098-141">PSK: incondicional</span><span class="sxs-lookup"><span data-stu-id="e8098-141">psk:Unconditional</span></span><br/> |
| <span data-ttu-id="e8098-142">Vários</span><span class="sxs-lookup"><span data-stu-id="e8098-142">Multiple</span></span><br/>     | <span data-ttu-id="e8098-143">integer</span><span class="sxs-lookup"><span data-stu-id="e8098-143">integer</span></span><br/> | <span data-ttu-id="e8098-144">1</span><span class="sxs-lookup"><span data-stu-id="e8098-144">1</span></span><br/>                 |
| <span data-ttu-id="e8098-145">UnitType</span><span class="sxs-lookup"><span data-stu-id="e8098-145">UnitType</span></span><br/>     | <span data-ttu-id="e8098-146">string</span><span class="sxs-lookup"><span data-stu-id="e8098-146">string</span></span><br/>  | <span data-ttu-id="e8098-147">cópia</span><span class="sxs-lookup"><span data-stu-id="e8098-147">copies</span></span><br/>            |



 

## <a name="related-topics"></a><span data-ttu-id="e8098-148">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="e8098-148">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e8098-149">Especificação de esquema de impressão</span><span class="sxs-lookup"><span data-stu-id="e8098-149">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




