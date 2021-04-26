---
description: Este tópico não é atual. Para obter as informações mais atuais, consulte a especificação do esquema de impressão.
ms.assetid: 6319e8fc-787f-4bc8-8436-1b498b3882d2
title: DocumentCopiesAllPages
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 723242ddd127113b573f167e6902b27fcca9665a
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/26/2021
ms.locfileid: "107993983"
---
# <a name="documentcopiesallpages"></a><span data-ttu-id="61d0d-104">DocumentCopiesAllPages</span><span class="sxs-lookup"><span data-stu-id="61d0d-104">DocumentCopiesAllPages</span></span>

<span data-ttu-id="61d0d-105">Este tópico não é atual.</span><span class="sxs-lookup"><span data-stu-id="61d0d-105">This topic is not current.</span></span> <span data-ttu-id="61d0d-106">Para obter as informações mais atuais, consulte a [especificação do esquema de impressão](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="61d0d-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="61d0d-107">Especifica o número de cópias de um documento.</span><span class="sxs-lookup"><span data-stu-id="61d0d-107">Specifies the number of copies of a document.</span></span>

-   [<span data-ttu-id="61d0d-108">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="61d0d-108">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="61d0d-109">Conteúdo da estrutura</span><span class="sxs-lookup"><span data-stu-id="61d0d-109">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="61d0d-110">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="61d0d-110">Element Information</span></span>



| <span data-ttu-id="61d0d-111">Nome</span><span class="sxs-lookup"><span data-stu-id="61d0d-111">Name</span></span> | <span data-ttu-id="61d0d-112">Valor</span><span class="sxs-lookup"><span data-stu-id="61d0d-112">Value</span></span> |
|----------------------------|-------------------------|
| <span data-ttu-id="61d0d-113">Tipo de elemento</span><span class="sxs-lookup"><span data-stu-id="61d0d-113">Element Type</span></span> <br/>   | <span data-ttu-id="61d0d-114">ParameterDef</span><span class="sxs-lookup"><span data-stu-id="61d0d-114">ParameterDef</span></span><br/> |
| <span data-ttu-id="61d0d-115">Prefixo de escopo</span><span class="sxs-lookup"><span data-stu-id="61d0d-115">Scoping Prefix</span></span> <br/> | <span data-ttu-id="61d0d-116">Documento</span><span class="sxs-lookup"><span data-stu-id="61d0d-116">Document</span></span><br/>     |
| <span data-ttu-id="61d0d-117">Observações</span><span class="sxs-lookup"><span data-stu-id="61d0d-117">Notes</span></span> <br/>          | <span data-ttu-id="61d0d-118">Nenhum</span><span class="sxs-lookup"><span data-stu-id="61d0d-118">None</span></span><br/>         |



 

## <a name="structure-content"></a><span data-ttu-id="61d0d-119">Conteúdo da estrutura</span><span class="sxs-lookup"><span data-stu-id="61d0d-119">Structure Content</span></span>

<span data-ttu-id="61d0d-120">A estrutura XML desse elemento é:</span><span class="sxs-lookup"><span data-stu-id="61d0d-120">The XML structure of this element is:</span></span>

``` syntax
<psf:ParameterDef name="psk:DocumentCopiesAllPages">
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

## <a name="structure-properties"></a><span data-ttu-id="61d0d-121">Propriedades da estrutura</span><span class="sxs-lookup"><span data-stu-id="61d0d-121">Structure Properties</span></span>

<span data-ttu-id="61d0d-122">A tabela a seguir descreve as características das variáveis definidas na estrutura XML.</span><span class="sxs-lookup"><span data-stu-id="61d0d-122">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="61d0d-123">Propriedade</span><span class="sxs-lookup"><span data-stu-id="61d0d-123">Property</span></span>                | <span data-ttu-id="61d0d-124">xsi:type</span><span class="sxs-lookup"><span data-stu-id="61d0d-124">xsi:type</span></span>           | <span data-ttu-id="61d0d-125">Valor</span><span class="sxs-lookup"><span data-stu-id="61d0d-125">Value</span></span>                        |
|-------------------------|--------------------|------------------------------|
| <span data-ttu-id="61d0d-126">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="61d0d-126">DataType</span></span><br/>     | <span data-ttu-id="61d0d-127">string</span><span class="sxs-lookup"><span data-stu-id="61d0d-127">string</span></span><br/>  | <span data-ttu-id="61d0d-128">xs:integer</span><span class="sxs-lookup"><span data-stu-id="61d0d-128">xs:integer</span></span><br/>        |
| <span data-ttu-id="61d0d-129">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="61d0d-129">DefaultValue</span></span><br/> | <span data-ttu-id="61d0d-130">integer</span><span class="sxs-lookup"><span data-stu-id="61d0d-130">integer</span></span><br/> | <span data-ttu-id="61d0d-131">1</span><span class="sxs-lookup"><span data-stu-id="61d0d-131">1</span></span><br/>                 |
| <span data-ttu-id="61d0d-132">MaxValue</span><span class="sxs-lookup"><span data-stu-id="61d0d-132">MaxValue</span></span><br/>     | <span data-ttu-id="61d0d-133">Número inteiro</span><span class="sxs-lookup"><span data-stu-id="61d0d-133">integer</span></span><br/> | <span data-ttu-id="61d0d-134">não definido</span><span class="sxs-lookup"><span data-stu-id="61d0d-134">undefined</span></span><br/>         |
| <span data-ttu-id="61d0d-135">MinValue</span><span class="sxs-lookup"><span data-stu-id="61d0d-135">MinValue</span></span><br/>     | <span data-ttu-id="61d0d-136">integer</span><span class="sxs-lookup"><span data-stu-id="61d0d-136">integer</span></span><br/> | <span data-ttu-id="61d0d-137">1</span><span class="sxs-lookup"><span data-stu-id="61d0d-137">1</span></span><br/>                 |
| <span data-ttu-id="61d0d-138">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="61d0d-138">Mandatory</span></span><br/>    | <span data-ttu-id="61d0d-139">string</span><span class="sxs-lookup"><span data-stu-id="61d0d-139">string</span></span><br/>  | <span data-ttu-id="61d0d-140">PSK: incondicional</span><span class="sxs-lookup"><span data-stu-id="61d0d-140">psk:Unconditional</span></span><br/> |
| <span data-ttu-id="61d0d-141">Vários</span><span class="sxs-lookup"><span data-stu-id="61d0d-141">Multiple</span></span><br/>     | <span data-ttu-id="61d0d-142">integer</span><span class="sxs-lookup"><span data-stu-id="61d0d-142">integer</span></span><br/> | <span data-ttu-id="61d0d-143">1</span><span class="sxs-lookup"><span data-stu-id="61d0d-143">1</span></span><br/>                 |
| <span data-ttu-id="61d0d-144">UnitType</span><span class="sxs-lookup"><span data-stu-id="61d0d-144">UnitType</span></span><br/>     | <span data-ttu-id="61d0d-145">string</span><span class="sxs-lookup"><span data-stu-id="61d0d-145">string</span></span><br/>  | <span data-ttu-id="61d0d-146">cópia</span><span class="sxs-lookup"><span data-stu-id="61d0d-146">copies</span></span><br/>            |



 

## <a name="related-topics"></a><span data-ttu-id="61d0d-147">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="61d0d-147">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="61d0d-148">Especificação de esquema de impressão</span><span class="sxs-lookup"><span data-stu-id="61d0d-148">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




