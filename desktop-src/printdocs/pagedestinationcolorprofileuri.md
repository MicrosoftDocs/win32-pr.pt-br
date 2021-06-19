---
description: Leia sobre o parâmetro PageDestinationColorProfileURI. Este tópico não é atual. Para obter as informações mais atuais, consulte a Especificação de Esquema de Impressão.
ms.assetid: b2a4a4d2-a8bc-48dc-ad56-20380f5f91c9
title: PageDestinationColorProfileURI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0c3cf719a97f8f8086e88425c1667199815efbbb
ms.sourcegitcommit: 91530c19d26ba4c57a6af1f37b57f211f580464e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/19/2021
ms.locfileid: "112396671"
---
# <a name="pagedestinationcolorprofileuri"></a><span data-ttu-id="f5547-105">PageDestinationColorProfileURI</span><span class="sxs-lookup"><span data-stu-id="f5547-105">PageDestinationColorProfileURI</span></span>

<span data-ttu-id="f5547-106">Este tópico não é atual.</span><span class="sxs-lookup"><span data-stu-id="f5547-106">This topic is not current.</span></span> <span data-ttu-id="f5547-107">Para obter as informações mais atuais, consulte a [Especificação de Esquema de Impressão](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="f5547-107">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="f5547-108">Especifica uma referência de URI relativa a um perfil ICC contido em um documento XPS.</span><span class="sxs-lookup"><span data-stu-id="f5547-108">Specifies a relative URI reference to an ICC profile contained in an XPS Document.</span></span> <span data-ttu-id="f5547-109">O processamento dessa opção depende da configuração do recurso PageDeviceColorSpaceUsage.</span><span class="sxs-lookup"><span data-stu-id="f5547-109">The processing of this option depends of the setting of the PageDeviceColorSpaceUsage feature.</span></span> <span data-ttu-id="f5547-110">Presume-se que todos os elementos que usam esse perfil já estão no espaço de cores do dispositivo apropriado e não serão gerenciados por cores no driver ou no dispositivo.</span><span class="sxs-lookup"><span data-stu-id="f5547-110">All elements using that profile are assumed to be already in the appropriate device color space, and will not be color managed in the driver or device.</span></span>

-   [<span data-ttu-id="f5547-111">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="f5547-111">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="f5547-112">Conteúdo da estrutura</span><span class="sxs-lookup"><span data-stu-id="f5547-112">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="f5547-113">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="f5547-113">Element Information</span></span>



| <span data-ttu-id="f5547-114">Name</span><span class="sxs-lookup"><span data-stu-id="f5547-114">Name</span></span> | <span data-ttu-id="f5547-115">Valor</span><span class="sxs-lookup"><span data-stu-id="f5547-115">Value</span></span> |
|----------------------------|----------------------------------------------------------|
| <span data-ttu-id="f5547-116">Tipo de elemento</span><span class="sxs-lookup"><span data-stu-id="f5547-116">Element Type</span></span> <br/>   | <span data-ttu-id="f5547-117">ParameterDef</span><span class="sxs-lookup"><span data-stu-id="f5547-117">ParameterDef</span></span><br/>                                  |
| <span data-ttu-id="f5547-118">Prefixo de definição de scoping</span><span class="sxs-lookup"><span data-stu-id="f5547-118">Scoping Prefix</span></span> <br/> | <span data-ttu-id="f5547-119">?</span><span class="sxs-lookup"><span data-stu-id="f5547-119">Page</span></span><br/>                                          |
| <span data-ttu-id="f5547-120">Observações</span><span class="sxs-lookup"><span data-stu-id="f5547-120">Notes</span></span> <br/>          | <span data-ttu-id="f5547-121">Vinculado ao elemento PageDestinationColorProfile</span><span class="sxs-lookup"><span data-stu-id="f5547-121">Linked to PageDestinationColorProfile element</span></span><br/> |



 

## <a name="structure-content"></a><span data-ttu-id="f5547-122">Conteúdo da estrutura</span><span class="sxs-lookup"><span data-stu-id="f5547-122">Structure Content</span></span>

<span data-ttu-id="f5547-123">A estrutura XML desse elemento é:</span><span class="sxs-lookup"><span data-stu-id="f5547-123">The XML structure of this element is:</span></span>

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

## <a name="structure-properties"></a><span data-ttu-id="f5547-124">Propriedades da estrutura</span><span class="sxs-lookup"><span data-stu-id="f5547-124">Structure Properties</span></span>

<span data-ttu-id="f5547-125">A tabela a seguir descreve as características das variáveis definidas na estrutura XML.</span><span class="sxs-lookup"><span data-stu-id="f5547-125">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="f5547-126">Propriedade</span><span class="sxs-lookup"><span data-stu-id="f5547-126">Property</span></span>                | <span data-ttu-id="f5547-127">xsi:type</span><span class="sxs-lookup"><span data-stu-id="f5547-127">xsi:type</span></span>           | <span data-ttu-id="f5547-128">Valor</span><span class="sxs-lookup"><span data-stu-id="f5547-128">Value</span></span>                      |
|-------------------------|--------------------|----------------------------|
| <span data-ttu-id="f5547-129">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="f5547-129">DataType</span></span><br/>     | <span data-ttu-id="f5547-130">string</span><span class="sxs-lookup"><span data-stu-id="f5547-130">string</span></span><br/>  | <span data-ttu-id="f5547-131">xs:string</span><span class="sxs-lookup"><span data-stu-id="f5547-131">xs:string</span></span><br/>       |
| <span data-ttu-id="f5547-132">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="f5547-132">DefaultValue</span></span><br/> | <span data-ttu-id="f5547-133">string</span><span class="sxs-lookup"><span data-stu-id="f5547-133">string</span></span><br/>  | <span data-ttu-id="f5547-134">não definido</span><span class="sxs-lookup"><span data-stu-id="f5547-134">undefined</span></span><br/>       |
| <span data-ttu-id="f5547-135">MaxLength</span><span class="sxs-lookup"><span data-stu-id="f5547-135">MaxLength</span></span><br/>    | <span data-ttu-id="f5547-136">Número inteiro</span><span class="sxs-lookup"><span data-stu-id="f5547-136">integer</span></span><br/> | <span data-ttu-id="f5547-137">não definido</span><span class="sxs-lookup"><span data-stu-id="f5547-137">undefined</span></span><br/>       |
| <span data-ttu-id="f5547-138">Minlength</span><span class="sxs-lookup"><span data-stu-id="f5547-138">MinLength</span></span><br/>    | <span data-ttu-id="f5547-139">integer</span><span class="sxs-lookup"><span data-stu-id="f5547-139">integer</span></span><br/> | <span data-ttu-id="f5547-140">1</span><span class="sxs-lookup"><span data-stu-id="f5547-140">1</span></span><br/>               |
| <span data-ttu-id="f5547-141">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="f5547-141">Mandatory</span></span><br/>    | <span data-ttu-id="f5547-142">string</span><span class="sxs-lookup"><span data-stu-id="f5547-142">string</span></span><br/>  | <span data-ttu-id="f5547-143">psk:Conditional</span><span class="sxs-lookup"><span data-stu-id="f5547-143">psk:Conditional</span></span><br/> |
| <span data-ttu-id="f5547-144">Unittype</span><span class="sxs-lookup"><span data-stu-id="f5547-144">UnitType</span></span><br/>     | <span data-ttu-id="f5547-145">string</span><span class="sxs-lookup"><span data-stu-id="f5547-145">string</span></span><br/>  | <span data-ttu-id="f5547-146">characters</span><span class="sxs-lookup"><span data-stu-id="f5547-146">characters</span></span><br/>      |



 

## <a name="related-topics"></a><span data-ttu-id="f5547-147">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="f5547-147">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f5547-148">Especificação de esquema de impressão</span><span class="sxs-lookup"><span data-stu-id="f5547-148">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




