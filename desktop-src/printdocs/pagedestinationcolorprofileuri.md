---
description: Este tópico não é atual. Para obter as informações mais atuais, consulte a especificação do esquema de impressão.
ms.assetid: b2a4a4d2-a8bc-48dc-ad56-20380f5f91c9
title: PageDestinationColorProfileURI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b321cba1608b1098dcc91f3800ef11f4968fb3f2
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/26/2021
ms.locfileid: "107996093"
---
# <a name="pagedestinationcolorprofileuri"></a><span data-ttu-id="1f9fc-104">PageDestinationColorProfileURI</span><span class="sxs-lookup"><span data-stu-id="1f9fc-104">PageDestinationColorProfileURI</span></span>

<span data-ttu-id="1f9fc-105">Este tópico não é atual.</span><span class="sxs-lookup"><span data-stu-id="1f9fc-105">This topic is not current.</span></span> <span data-ttu-id="1f9fc-106">Para obter as informações mais atuais, consulte a [especificação do esquema de impressão](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="1f9fc-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="1f9fc-107">Especifica uma referência de URI relativa a um perfil ICC contido em um documento XPS.</span><span class="sxs-lookup"><span data-stu-id="1f9fc-107">Specifies a relative URI reference to an ICC profile contained in an XPS Document.</span></span> <span data-ttu-id="1f9fc-108">O processamento dessa opção depende da configuração do recurso PageDeviceColorSpaceUsage.</span><span class="sxs-lookup"><span data-stu-id="1f9fc-108">The processing of this option depends of the setting of the PageDeviceColorSpaceUsage feature.</span></span> <span data-ttu-id="1f9fc-109">Todos os elementos que usam esse perfil já estão no espaço de cores do dispositivo apropriado e não serão gerenciados por cores no driver ou no dispositivo.</span><span class="sxs-lookup"><span data-stu-id="1f9fc-109">All elements using that profile are assumed to be already in the appropriate device color space, and will not be color managed in the driver or device.</span></span>

-   [<span data-ttu-id="1f9fc-110">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="1f9fc-110">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="1f9fc-111">Conteúdo da estrutura</span><span class="sxs-lookup"><span data-stu-id="1f9fc-111">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="1f9fc-112">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="1f9fc-112">Element Information</span></span>



| <span data-ttu-id="1f9fc-113">Nome</span><span class="sxs-lookup"><span data-stu-id="1f9fc-113">Name</span></span> | <span data-ttu-id="1f9fc-114">Valor</span><span class="sxs-lookup"><span data-stu-id="1f9fc-114">Value</span></span> |
|----------------------------|----------------------------------------------------------|
| <span data-ttu-id="1f9fc-115">Tipo de elemento</span><span class="sxs-lookup"><span data-stu-id="1f9fc-115">Element Type</span></span> <br/>   | <span data-ttu-id="1f9fc-116">ParameterDef</span><span class="sxs-lookup"><span data-stu-id="1f9fc-116">ParameterDef</span></span><br/>                                  |
| <span data-ttu-id="1f9fc-117">Prefixo de escopo</span><span class="sxs-lookup"><span data-stu-id="1f9fc-117">Scoping Prefix</span></span> <br/> | <span data-ttu-id="1f9fc-118">?</span><span class="sxs-lookup"><span data-stu-id="1f9fc-118">Page</span></span><br/>                                          |
| <span data-ttu-id="1f9fc-119">Observações</span><span class="sxs-lookup"><span data-stu-id="1f9fc-119">Notes</span></span> <br/>          | <span data-ttu-id="1f9fc-120">Vinculado ao elemento PageDestinationColorProfile</span><span class="sxs-lookup"><span data-stu-id="1f9fc-120">Linked to PageDestinationColorProfile element</span></span><br/> |



 

## <a name="structure-content"></a><span data-ttu-id="1f9fc-121">Conteúdo da estrutura</span><span class="sxs-lookup"><span data-stu-id="1f9fc-121">Structure Content</span></span>

<span data-ttu-id="1f9fc-122">A estrutura XML desse elemento é:</span><span class="sxs-lookup"><span data-stu-id="1f9fc-122">The XML structure of this element is:</span></span>

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

## <a name="structure-properties"></a><span data-ttu-id="1f9fc-123">Propriedades da estrutura</span><span class="sxs-lookup"><span data-stu-id="1f9fc-123">Structure Properties</span></span>

<span data-ttu-id="1f9fc-124">A tabela a seguir descreve as características das variáveis definidas na estrutura XML.</span><span class="sxs-lookup"><span data-stu-id="1f9fc-124">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="1f9fc-125">Propriedade</span><span class="sxs-lookup"><span data-stu-id="1f9fc-125">Property</span></span>                | <span data-ttu-id="1f9fc-126">xsi:type</span><span class="sxs-lookup"><span data-stu-id="1f9fc-126">xsi:type</span></span>           | <span data-ttu-id="1f9fc-127">Valor</span><span class="sxs-lookup"><span data-stu-id="1f9fc-127">Value</span></span>                      |
|-------------------------|--------------------|----------------------------|
| <span data-ttu-id="1f9fc-128">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="1f9fc-128">DataType</span></span><br/>     | <span data-ttu-id="1f9fc-129">string</span><span class="sxs-lookup"><span data-stu-id="1f9fc-129">string</span></span><br/>  | <span data-ttu-id="1f9fc-130">xs:string</span><span class="sxs-lookup"><span data-stu-id="1f9fc-130">xs:string</span></span><br/>       |
| <span data-ttu-id="1f9fc-131">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="1f9fc-131">DefaultValue</span></span><br/> | <span data-ttu-id="1f9fc-132">string</span><span class="sxs-lookup"><span data-stu-id="1f9fc-132">string</span></span><br/>  | <span data-ttu-id="1f9fc-133">não definido</span><span class="sxs-lookup"><span data-stu-id="1f9fc-133">undefined</span></span><br/>       |
| <span data-ttu-id="1f9fc-134">MaxLength</span><span class="sxs-lookup"><span data-stu-id="1f9fc-134">MaxLength</span></span><br/>    | <span data-ttu-id="1f9fc-135">Número inteiro</span><span class="sxs-lookup"><span data-stu-id="1f9fc-135">integer</span></span><br/> | <span data-ttu-id="1f9fc-136">não definido</span><span class="sxs-lookup"><span data-stu-id="1f9fc-136">undefined</span></span><br/>       |
| <span data-ttu-id="1f9fc-137">MinLength</span><span class="sxs-lookup"><span data-stu-id="1f9fc-137">MinLength</span></span><br/>    | <span data-ttu-id="1f9fc-138">integer</span><span class="sxs-lookup"><span data-stu-id="1f9fc-138">integer</span></span><br/> | <span data-ttu-id="1f9fc-139">1</span><span class="sxs-lookup"><span data-stu-id="1f9fc-139">1</span></span><br/>               |
| <span data-ttu-id="1f9fc-140">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="1f9fc-140">Mandatory</span></span><br/>    | <span data-ttu-id="1f9fc-141">string</span><span class="sxs-lookup"><span data-stu-id="1f9fc-141">string</span></span><br/>  | <span data-ttu-id="1f9fc-142">PSK: condicional</span><span class="sxs-lookup"><span data-stu-id="1f9fc-142">psk:Conditional</span></span><br/> |
| <span data-ttu-id="1f9fc-143">UnitType</span><span class="sxs-lookup"><span data-stu-id="1f9fc-143">UnitType</span></span><br/>     | <span data-ttu-id="1f9fc-144">string</span><span class="sxs-lookup"><span data-stu-id="1f9fc-144">string</span></span><br/>  | <span data-ttu-id="1f9fc-145">characters</span><span class="sxs-lookup"><span data-stu-id="1f9fc-145">characters</span></span><br/>      |



 

## <a name="related-topics"></a><span data-ttu-id="1f9fc-146">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="1f9fc-146">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1f9fc-147">Especificação de esquema de impressão</span><span class="sxs-lookup"><span data-stu-id="1f9fc-147">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




