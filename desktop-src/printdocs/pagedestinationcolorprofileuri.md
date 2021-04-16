---
description: Este tópico não é atual. Para obter as informações mais atuais, consulte a especificação do esquema de impressão.
ms.assetid: b2a4a4d2-a8bc-48dc-ad56-20380f5f91c9
title: PageDestinationColorProfileURI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8fff2ca269eaed9331f6c2077e6b396cca5a01c4
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/05/2021
ms.locfileid: "105773052"
---
# <a name="pagedestinationcolorprofileuri"></a><span data-ttu-id="ac1e4-104">PageDestinationColorProfileURI</span><span class="sxs-lookup"><span data-stu-id="ac1e4-104">PageDestinationColorProfileURI</span></span>

<span data-ttu-id="ac1e4-105">Este tópico não é atual.</span><span class="sxs-lookup"><span data-stu-id="ac1e4-105">This topic is not current.</span></span> <span data-ttu-id="ac1e4-106">Para obter as informações mais atuais, consulte a [especificação do esquema de impressão](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="ac1e4-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="ac1e4-107">Especifica uma referência de URI relativa a um perfil ICC contido em um documento XPS.</span><span class="sxs-lookup"><span data-stu-id="ac1e4-107">Specifies a relative URI reference to an ICC profile contained in an XPS Document.</span></span> <span data-ttu-id="ac1e4-108">O processamento dessa opção depende da configuração do recurso PageDeviceColorSpaceUsage.</span><span class="sxs-lookup"><span data-stu-id="ac1e4-108">The processing of this option depends of the setting of the PageDeviceColorSpaceUsage feature.</span></span> <span data-ttu-id="ac1e4-109">Todos os elementos que usam esse perfil já estão no espaço de cores do dispositivo apropriado e não serão gerenciados por cores no driver ou no dispositivo.</span><span class="sxs-lookup"><span data-stu-id="ac1e4-109">All elements using that profile are assumed to be already in the appropriate device color space, and will not be color managed in the driver or device.</span></span>

-   [<span data-ttu-id="ac1e4-110">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="ac1e4-110">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="ac1e4-111">Conteúdo da estrutura</span><span class="sxs-lookup"><span data-stu-id="ac1e4-111">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="ac1e4-112">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="ac1e4-112">Element Information</span></span>



| <span data-ttu-id="ac1e4-113">Nome</span><span class="sxs-lookup"><span data-stu-id="ac1e4-113">Name</span></span>                       |                                                          |
|----------------------------|----------------------------------------------------------|
| <span data-ttu-id="ac1e4-114">Tipo de elemento</span><span class="sxs-lookup"><span data-stu-id="ac1e4-114">Element Type</span></span> <br/>   | <span data-ttu-id="ac1e4-115">ParameterDef</span><span class="sxs-lookup"><span data-stu-id="ac1e4-115">ParameterDef</span></span><br/>                                  |
| <span data-ttu-id="ac1e4-116">Prefixo de escopo</span><span class="sxs-lookup"><span data-stu-id="ac1e4-116">Scoping Prefix</span></span> <br/> | <span data-ttu-id="ac1e4-117">?</span><span class="sxs-lookup"><span data-stu-id="ac1e4-117">Page</span></span><br/>                                          |
| <span data-ttu-id="ac1e4-118">Observações</span><span class="sxs-lookup"><span data-stu-id="ac1e4-118">Notes</span></span> <br/>          | <span data-ttu-id="ac1e4-119">Vinculado ao elemento PageDestinationColorProfile</span><span class="sxs-lookup"><span data-stu-id="ac1e4-119">Linked to PageDestinationColorProfile element</span></span><br/> |



 

## <a name="structure-content"></a><span data-ttu-id="ac1e4-120">Conteúdo da estrutura</span><span class="sxs-lookup"><span data-stu-id="ac1e4-120">Structure Content</span></span>

<span data-ttu-id="ac1e4-121">A estrutura XML desse elemento é:</span><span class="sxs-lookup"><span data-stu-id="ac1e4-121">The XML structure of this element is:</span></span>

``` syntax
<psf:ParameterDef name="psk:PageDestinationColorProfileURI">
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

## <a name="structure-properties"></a><span data-ttu-id="ac1e4-122">Propriedades da estrutura</span><span class="sxs-lookup"><span data-stu-id="ac1e4-122">Structure Properties</span></span>

<span data-ttu-id="ac1e4-123">A tabela a seguir descreve as características das variáveis definidas na estrutura XML.</span><span class="sxs-lookup"><span data-stu-id="ac1e4-123">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="ac1e4-124">Propriedade</span><span class="sxs-lookup"><span data-stu-id="ac1e4-124">Property</span></span>                | <span data-ttu-id="ac1e4-125">xsi:type</span><span class="sxs-lookup"><span data-stu-id="ac1e4-125">xsi:type</span></span>           | <span data-ttu-id="ac1e4-126">Valor</span><span class="sxs-lookup"><span data-stu-id="ac1e4-126">Value</span></span>                      |
|-------------------------|--------------------|----------------------------|
| <span data-ttu-id="ac1e4-127">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="ac1e4-127">DataType</span></span><br/>     | <span data-ttu-id="ac1e4-128">string</span><span class="sxs-lookup"><span data-stu-id="ac1e4-128">string</span></span><br/>  | <span data-ttu-id="ac1e4-129">xs:string</span><span class="sxs-lookup"><span data-stu-id="ac1e4-129">xs:string</span></span><br/>       |
| <span data-ttu-id="ac1e4-130">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="ac1e4-130">DefaultValue</span></span><br/> | <span data-ttu-id="ac1e4-131">string</span><span class="sxs-lookup"><span data-stu-id="ac1e4-131">string</span></span><br/>  | <span data-ttu-id="ac1e4-132">não definido</span><span class="sxs-lookup"><span data-stu-id="ac1e4-132">undefined</span></span><br/>       |
| <span data-ttu-id="ac1e4-133">MaxLength</span><span class="sxs-lookup"><span data-stu-id="ac1e4-133">MaxLength</span></span><br/>    | <span data-ttu-id="ac1e4-134">Número inteiro</span><span class="sxs-lookup"><span data-stu-id="ac1e4-134">integer</span></span><br/> | <span data-ttu-id="ac1e4-135">não definido</span><span class="sxs-lookup"><span data-stu-id="ac1e4-135">undefined</span></span><br/>       |
| <span data-ttu-id="ac1e4-136">MinLength</span><span class="sxs-lookup"><span data-stu-id="ac1e4-136">MinLength</span></span><br/>    | <span data-ttu-id="ac1e4-137">integer</span><span class="sxs-lookup"><span data-stu-id="ac1e4-137">integer</span></span><br/> | <span data-ttu-id="ac1e4-138">1</span><span class="sxs-lookup"><span data-stu-id="ac1e4-138">1</span></span><br/>               |
| <span data-ttu-id="ac1e4-139">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="ac1e4-139">Mandatory</span></span><br/>    | <span data-ttu-id="ac1e4-140">string</span><span class="sxs-lookup"><span data-stu-id="ac1e4-140">string</span></span><br/>  | <span data-ttu-id="ac1e4-141">PSK: condicional</span><span class="sxs-lookup"><span data-stu-id="ac1e4-141">psk:Conditional</span></span><br/> |
| <span data-ttu-id="ac1e4-142">UnitType</span><span class="sxs-lookup"><span data-stu-id="ac1e4-142">UnitType</span></span><br/>     | <span data-ttu-id="ac1e4-143">string</span><span class="sxs-lookup"><span data-stu-id="ac1e4-143">string</span></span><br/>  | <span data-ttu-id="ac1e4-144">characters</span><span class="sxs-lookup"><span data-stu-id="ac1e4-144">characters</span></span><br/>      |



 

## <a name="related-topics"></a><span data-ttu-id="ac1e4-145">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="ac1e4-145">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ac1e4-146">Especificação de esquema de impressão</span><span class="sxs-lookup"><span data-stu-id="ac1e4-146">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




