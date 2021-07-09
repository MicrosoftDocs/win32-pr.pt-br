---
description: Leia sobre o parâmetro PageDestinationColorProfileEmbedded. Este tópico não é atual. Para obter as informações mais atuais, consulte a especificação do esquema de impressão.
ms.assetid: b360f870-bfaa-4d4d-adce-17fcfc48b6a6
title: PageDestinationColorProfileEmbedded
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 05865636b6554873844a99b523f8c21fe2bfc1c7
ms.sourcegitcommit: 998d50f6def8a25850fc113fc8a2df903c829c5e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/09/2021
ms.locfileid: "113549204"
---
# <a name="pagedestinationcolorprofileembedded"></a><span data-ttu-id="680be-105">PageDestinationColorProfileEmbedded</span><span class="sxs-lookup"><span data-stu-id="680be-105">PageDestinationColorProfileEmbedded</span></span>

<span data-ttu-id="680be-106">Este tópico não é atual.</span><span class="sxs-lookup"><span data-stu-id="680be-106">This topic is not current.</span></span> <span data-ttu-id="680be-107">Para obter as informações mais atuais, consulte a [especificação do esquema de impressão](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="680be-107">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="680be-108">Especifica o perfil de cor de destino inserido.</span><span class="sxs-lookup"><span data-stu-id="680be-108">Specifies the embedded destination color profile.</span></span>

-   [<span data-ttu-id="680be-109">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="680be-109">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="680be-110">Conteúdo da estrutura</span><span class="sxs-lookup"><span data-stu-id="680be-110">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="680be-111">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="680be-111">Element Information</span></span>



| <span data-ttu-id="680be-112">Nome</span><span class="sxs-lookup"><span data-stu-id="680be-112">Name</span></span> | <span data-ttu-id="680be-113">Valor</span><span class="sxs-lookup"><span data-stu-id="680be-113">Value</span></span> |
|----------------------------|----------------------------------------------------------|
| <span data-ttu-id="680be-114">Tipo de elemento</span><span class="sxs-lookup"><span data-stu-id="680be-114">Element Type</span></span> <br/>   | <span data-ttu-id="680be-115">ParameterDef</span><span class="sxs-lookup"><span data-stu-id="680be-115">ParameterDef</span></span><br/>                                  |
| <span data-ttu-id="680be-116">Prefixo de escopo</span><span class="sxs-lookup"><span data-stu-id="680be-116">Scoping Prefix</span></span> <br/> | <span data-ttu-id="680be-117">Página</span><span class="sxs-lookup"><span data-stu-id="680be-117">Page</span></span><br/>                                          |
| <span data-ttu-id="680be-118">Observações</span><span class="sxs-lookup"><span data-stu-id="680be-118">Notes</span></span> <br/>          | <span data-ttu-id="680be-119">Vinculado ao elemento PageDestinationColorProfile</span><span class="sxs-lookup"><span data-stu-id="680be-119">Linked to PageDestinationColorProfile element</span></span><br/> |



 

## <a name="structure-content"></a><span data-ttu-id="680be-120">Conteúdo da estrutura</span><span class="sxs-lookup"><span data-stu-id="680be-120">Structure Content</span></span>

<span data-ttu-id="680be-121">A estrutura XML desse elemento é:</span><span class="sxs-lookup"><span data-stu-id="680be-121">The XML structure of this element is:</span></span>

``` syntax
<psf:ParameterDef name="psk:PageDestinationColorProfileEmbedded">
  <psf:Property name="psf:DataType">
    <psf:Value xsi:type="xs:string">xs:string</psf:Value>
  </psf:Property>
  <psf:Property name="psf:DefaultValue">
    <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
  </psf:Property>
  <psf:Property name="psf:MaxLength">
    <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
  </psf:Property>
  <psf:Property name="psf:MinLength">
    <psf:Value xsi:type="xs:integer">1</psf:Value>
  </psf:Property>
  <psf:Property name="psf:Mandatory">
    <psf:Value xsi:type="xs:string">psk:Conditional</psf:Value>
  </psf:Property>
  <psf:Property name="psf:UnitType">
    <psf:Value xsi:type="xs:string">characters</psf:Value>
  </psf:Property>
</psf:ParameterDef>
      
```

## <a name="structure-properties"></a><span data-ttu-id="680be-122">Propriedades da estrutura</span><span class="sxs-lookup"><span data-stu-id="680be-122">Structure Properties</span></span>

<span data-ttu-id="680be-123">A tabela a seguir descreve as características das variáveis definidas na estrutura XML.</span><span class="sxs-lookup"><span data-stu-id="680be-123">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="680be-124">Propriedade</span><span class="sxs-lookup"><span data-stu-id="680be-124">Property</span></span>                | <span data-ttu-id="680be-125">xsi:type</span><span class="sxs-lookup"><span data-stu-id="680be-125">xsi:type</span></span>           | <span data-ttu-id="680be-126">Valor</span><span class="sxs-lookup"><span data-stu-id="680be-126">Value</span></span>                      |
|-------------------------|--------------------|----------------------------|
| <span data-ttu-id="680be-127">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="680be-127">DataType</span></span><br/>     | <span data-ttu-id="680be-128">string</span><span class="sxs-lookup"><span data-stu-id="680be-128">string</span></span><br/>  | <span data-ttu-id="680be-129">xs:string</span><span class="sxs-lookup"><span data-stu-id="680be-129">xs:string</span></span><br/>       |
| <span data-ttu-id="680be-130">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="680be-130">DefaultValue</span></span><br/> | <span data-ttu-id="680be-131">string</span><span class="sxs-lookup"><span data-stu-id="680be-131">string</span></span><br/>  | <span data-ttu-id="680be-132">não definido</span><span class="sxs-lookup"><span data-stu-id="680be-132">undefined</span></span><br/>       |
| <span data-ttu-id="680be-133">MaxLength</span><span class="sxs-lookup"><span data-stu-id="680be-133">MaxLength</span></span><br/>    | <span data-ttu-id="680be-134">Número inteiro</span><span class="sxs-lookup"><span data-stu-id="680be-134">integer</span></span><br/> | <span data-ttu-id="680be-135">não definido</span><span class="sxs-lookup"><span data-stu-id="680be-135">undefined</span></span><br/>       |
| <span data-ttu-id="680be-136">MinLength</span><span class="sxs-lookup"><span data-stu-id="680be-136">MinLength</span></span><br/>    | <span data-ttu-id="680be-137">integer</span><span class="sxs-lookup"><span data-stu-id="680be-137">integer</span></span><br/> | <span data-ttu-id="680be-138">1</span><span class="sxs-lookup"><span data-stu-id="680be-138">1</span></span><br/>               |
| <span data-ttu-id="680be-139">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="680be-139">Mandatory</span></span><br/>    | <span data-ttu-id="680be-140">string</span><span class="sxs-lookup"><span data-stu-id="680be-140">string</span></span><br/>  | <span data-ttu-id="680be-141">PSK: condicional</span><span class="sxs-lookup"><span data-stu-id="680be-141">psk:Conditional</span></span><br/> |
| <span data-ttu-id="680be-142">UnitType</span><span class="sxs-lookup"><span data-stu-id="680be-142">UnitType</span></span><br/>     | <span data-ttu-id="680be-143">string</span><span class="sxs-lookup"><span data-stu-id="680be-143">string</span></span><br/>  | <span data-ttu-id="680be-144">characters</span><span class="sxs-lookup"><span data-stu-id="680be-144">characters</span></span><br/>      |



 

## <a name="related-topics"></a><span data-ttu-id="680be-145">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="680be-145">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="680be-146">Especificação de esquema de impressão</span><span class="sxs-lookup"><span data-stu-id="680be-146">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




