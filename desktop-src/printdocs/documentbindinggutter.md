---
description: Encontre informações sobre o parâmetro DocumentBindingGutter. Este tópico não é atual. Para obter as informações mais atuais, consulte a especificação do esquema de impressão.
ms.assetid: 903ad358-a060-4c8f-b72e-5ec2eb898248
title: DocumentBindingGutter
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 45839aa07d740d8498e477809b45aa823460b23f
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/30/2021
ms.locfileid: "113118461"
---
# <a name="documentbindinggutter"></a><span data-ttu-id="4b7df-105">DocumentBindingGutter</span><span class="sxs-lookup"><span data-stu-id="4b7df-105">DocumentBindingGutter</span></span>

<span data-ttu-id="4b7df-106">Este tópico não é atual.</span><span class="sxs-lookup"><span data-stu-id="4b7df-106">This topic is not current.</span></span> <span data-ttu-id="4b7df-107">Para obter as informações mais atuais, consulte a [especificação do esquema de impressão](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="4b7df-107">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="4b7df-108">Especifica a largura da medianiz de associação.</span><span class="sxs-lookup"><span data-stu-id="4b7df-108">Specifies the width of the binding gutter.</span></span>

-   [<span data-ttu-id="4b7df-109">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="4b7df-109">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="4b7df-110">Conteúdo da estrutura</span><span class="sxs-lookup"><span data-stu-id="4b7df-110">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="4b7df-111">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="4b7df-111">Element Information</span></span>



| <span data-ttu-id="4b7df-112">Nome</span><span class="sxs-lookup"><span data-stu-id="4b7df-112">Name</span></span> | <span data-ttu-id="4b7df-113">Valor</span><span class="sxs-lookup"><span data-stu-id="4b7df-113">Value</span></span> |
|----------------------------|----------------------------------------------|
| <span data-ttu-id="4b7df-114">Tipo de elemento</span><span class="sxs-lookup"><span data-stu-id="4b7df-114">Element Type</span></span> <br/>   | <span data-ttu-id="4b7df-115">ParameterDef</span><span class="sxs-lookup"><span data-stu-id="4b7df-115">ParameterDef</span></span><br/>                      |
| <span data-ttu-id="4b7df-116">Prefixo de escopo</span><span class="sxs-lookup"><span data-stu-id="4b7df-116">Scoping Prefix</span></span> <br/> | <span data-ttu-id="4b7df-117">Documento</span><span class="sxs-lookup"><span data-stu-id="4b7df-117">Document</span></span><br/>                          |
| <span data-ttu-id="4b7df-118">Observações</span><span class="sxs-lookup"><span data-stu-id="4b7df-118">Notes</span></span> <br/>          | <span data-ttu-id="4b7df-119">Vinculado ao elemento Documentbinding</span><span class="sxs-lookup"><span data-stu-id="4b7df-119">Linked to DocumentBinding element</span></span><br/> |



 

## <a name="structure-content"></a><span data-ttu-id="4b7df-120">Conteúdo da estrutura</span><span class="sxs-lookup"><span data-stu-id="4b7df-120">Structure Content</span></span>

<span data-ttu-id="4b7df-121">A estrutura XML desse elemento é:</span><span class="sxs-lookup"><span data-stu-id="4b7df-121">The XML structure of this element is:</span></span>

``` syntax
<psf:ParameterDef name="psk:DocumentBindingGutter">
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

## <a name="structure-properties"></a><span data-ttu-id="4b7df-122">Propriedades da estrutura</span><span class="sxs-lookup"><span data-stu-id="4b7df-122">Structure Properties</span></span>

<span data-ttu-id="4b7df-123">A tabela a seguir descreve as características das variáveis definidas na estrutura XML.</span><span class="sxs-lookup"><span data-stu-id="4b7df-123">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="4b7df-124">Propriedade</span><span class="sxs-lookup"><span data-stu-id="4b7df-124">Property</span></span>                | <span data-ttu-id="4b7df-125">xsi:type</span><span class="sxs-lookup"><span data-stu-id="4b7df-125">xsi:type</span></span>           | <span data-ttu-id="4b7df-126">Valor</span><span class="sxs-lookup"><span data-stu-id="4b7df-126">Value</span></span>                      |
|-------------------------|--------------------|----------------------------|
| <span data-ttu-id="4b7df-127">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="4b7df-127">DataType</span></span><br/>     | <span data-ttu-id="4b7df-128">string</span><span class="sxs-lookup"><span data-stu-id="4b7df-128">string</span></span><br/>  | <span data-ttu-id="4b7df-129">xs:integer</span><span class="sxs-lookup"><span data-stu-id="4b7df-129">xs:integer</span></span><br/>      |
| <span data-ttu-id="4b7df-130">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="4b7df-130">DefaultValue</span></span><br/> | <span data-ttu-id="4b7df-131">Número inteiro</span><span class="sxs-lookup"><span data-stu-id="4b7df-131">integer</span></span><br/> | <span data-ttu-id="4b7df-132">não definido</span><span class="sxs-lookup"><span data-stu-id="4b7df-132">undefined</span></span><br/>       |
| <span data-ttu-id="4b7df-133">MaxValue</span><span class="sxs-lookup"><span data-stu-id="4b7df-133">MaxValue</span></span><br/>     | <span data-ttu-id="4b7df-134">Número inteiro</span><span class="sxs-lookup"><span data-stu-id="4b7df-134">integer</span></span><br/> | <span data-ttu-id="4b7df-135">não definido</span><span class="sxs-lookup"><span data-stu-id="4b7df-135">undefined</span></span><br/>       |
| <span data-ttu-id="4b7df-136">MinValue</span><span class="sxs-lookup"><span data-stu-id="4b7df-136">MinValue</span></span><br/>     | <span data-ttu-id="4b7df-137">Número inteiro</span><span class="sxs-lookup"><span data-stu-id="4b7df-137">integer</span></span><br/> | <span data-ttu-id="4b7df-138">não definido</span><span class="sxs-lookup"><span data-stu-id="4b7df-138">undefined</span></span><br/>       |
| <span data-ttu-id="4b7df-139">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="4b7df-139">Mandatory</span></span><br/>    | <span data-ttu-id="4b7df-140">String</span><span class="sxs-lookup"><span data-stu-id="4b7df-140">String</span></span><br/>  | <span data-ttu-id="4b7df-141">PSK: condicional</span><span class="sxs-lookup"><span data-stu-id="4b7df-141">psk:Conditional</span></span><br/> |
| <span data-ttu-id="4b7df-142">Vários</span><span class="sxs-lookup"><span data-stu-id="4b7df-142">Multiple</span></span><br/>     | <span data-ttu-id="4b7df-143">integer</span><span class="sxs-lookup"><span data-stu-id="4b7df-143">integer</span></span><br/> | <span data-ttu-id="4b7df-144">1</span><span class="sxs-lookup"><span data-stu-id="4b7df-144">1</span></span><br/>               |
| <span data-ttu-id="4b7df-145">UnitType</span><span class="sxs-lookup"><span data-stu-id="4b7df-145">UnitType</span></span><br/>     | <span data-ttu-id="4b7df-146">string</span><span class="sxs-lookup"><span data-stu-id="4b7df-146">string</span></span><br/>  | <span data-ttu-id="4b7df-147">mícrons</span><span class="sxs-lookup"><span data-stu-id="4b7df-147">microns</span></span><br/>         |



 

## <a name="related-topics"></a><span data-ttu-id="4b7df-148">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="4b7df-148">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4b7df-149">Especificação de esquema de impressão</span><span class="sxs-lookup"><span data-stu-id="4b7df-149">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




