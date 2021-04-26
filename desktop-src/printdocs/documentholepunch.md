---
description: Este tópico não é atual. Para obter as informações mais atuais, consulte a especificação do esquema de impressão.
ms.assetid: 46fd5e22-a2f3-424d-8c2f-2d5ac089a230
title: DocumentHolePunch
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 825120996d0d488af347ed871386a12d7f8014a7
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/26/2021
ms.locfileid: "107997883"
---
# <a name="documentholepunch"></a><span data-ttu-id="a167d-104">DocumentHolePunch</span><span class="sxs-lookup"><span data-stu-id="a167d-104">DocumentHolePunch</span></span>

<span data-ttu-id="a167d-105">Este tópico não é atual.</span><span class="sxs-lookup"><span data-stu-id="a167d-105">This topic is not current.</span></span> <span data-ttu-id="a167d-106">Para obter as informações mais atuais, consulte a [especificação do esquema de impressão](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="a167d-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="a167d-107">Descreve as características de perfuração da saída.</span><span class="sxs-lookup"><span data-stu-id="a167d-107">Describes the hole punching characteristics of the output.</span></span> <span data-ttu-id="a167d-108">Cada documento é perfurado separadamente.</span><span class="sxs-lookup"><span data-stu-id="a167d-108">Each document is punched separately.</span></span> <span data-ttu-id="a167d-109">As palavras-chave JobHolePunch e DocumentHolePunch são mutuamente exclusivas.</span><span class="sxs-lookup"><span data-stu-id="a167d-109">The JobHolePunch and DocumentHolePunch keywords are mutually exclusive.</span></span> <span data-ttu-id="a167d-110">Ambos não devem ser especificados simultaneamente em um documento de PrintTicket ou recursos de impressão.</span><span class="sxs-lookup"><span data-stu-id="a167d-110">Both should not be specified simultaneously in a PrintTicket or Print Capabilities document.</span></span>

-   [<span data-ttu-id="a167d-111">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="a167d-111">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="a167d-112">Conteúdo estrutural</span><span class="sxs-lookup"><span data-stu-id="a167d-112">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="a167d-113">Conteúdo de linguagem XML (XML)</span><span class="sxs-lookup"><span data-stu-id="a167d-113">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="a167d-114">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="a167d-114">Element Information</span></span>



| <span data-ttu-id="a167d-115">Nome</span><span class="sxs-lookup"><span data-stu-id="a167d-115">Name</span></span> | <span data-ttu-id="a167d-116">Valor</span><span class="sxs-lookup"><span data-stu-id="a167d-116">Value</span></span> |
|----------------------------|--------------------------------------------------------------------------------|
| <span data-ttu-id="a167d-117">Tipo de elemento</span><span class="sxs-lookup"><span data-stu-id="a167d-117">Element Type</span></span> <br/>   | <span data-ttu-id="a167d-118">Recurso</span><span class="sxs-lookup"><span data-stu-id="a167d-118">Feature</span></span><br/>                                                             |
| <span data-ttu-id="a167d-119">Prefixo de escopo</span><span class="sxs-lookup"><span data-stu-id="a167d-119">Scoping Prefix</span></span> <br/> | <span data-ttu-id="a167d-120">Documento</span><span class="sxs-lookup"><span data-stu-id="a167d-120">Document</span></span><br/>                                                            |
| <span data-ttu-id="a167d-121">Observações</span><span class="sxs-lookup"><span data-stu-id="a167d-121">Notes</span></span> <br/>          | <span data-ttu-id="a167d-122">Superior, inferior, esquerda e direita são relativos ao PageImageableSize.</span><span class="sxs-lookup"><span data-stu-id="a167d-122">Top, Bottom, Left, and Right are relative to the PageImageableSize.</span></span><br/> |



 

## <a name="structural-content"></a><span data-ttu-id="a167d-123">Conteúdo estrutural</span><span class="sxs-lookup"><span data-stu-id="a167d-123">Structural Content</span></span>

<span data-ttu-id="a167d-124">A estrutura XML desse elemento é:</span><span class="sxs-lookup"><span data-stu-id="a167d-124">The XML structure of this element is:</span></span>

``` syntax
<psf:Feature name="psk:DocumentHolePunch">
  <psf:Property name="psf:SelectionType">
    <psf:Value xsi:type="xs:string">psk:PickOne</psf:Value>
  </psf:Property>
  <psf:Option name="psk:_OptionName_">
    <psf:Property name="psf:IdentityOption">
      <psf:Value xsi:type="xs:string">_IdentityOptionValue_</psf:Value>
    </psf:Property>
  </psf:Option>
</psf:Feature>
```

## <a name="structure-variables"></a><span data-ttu-id="a167d-125">Variáveis de estrutura</span><span class="sxs-lookup"><span data-stu-id="a167d-125">Structure Variables</span></span>

<span data-ttu-id="a167d-126">A tabela a seguir descreve as características das variáveis definidas na estrutura XML.</span><span class="sxs-lookup"><span data-stu-id="a167d-126">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="a167d-127">Nome</span><span class="sxs-lookup"><span data-stu-id="a167d-127">Name</span></span>                               | <span data-ttu-id="a167d-128">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="a167d-128">Data type</span></span>         | <span data-ttu-id="a167d-129">Unidade</span><span class="sxs-lookup"><span data-stu-id="a167d-129">Unit</span></span>                  | <span data-ttu-id="a167d-130">Valores com suporte</span><span class="sxs-lookup"><span data-stu-id="a167d-130">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="a167d-131">Resumo</span><span class="sxs-lookup"><span data-stu-id="a167d-131">Summary</span></span>                                                                      |
|------------------------------------|-------------------|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="a167d-132">\_OptionName\_</span><span class="sxs-lookup"><span data-stu-id="a167d-132">\_OptionName\_</span></span><br/>          | <span data-ttu-id="a167d-133">string</span><span class="sxs-lookup"><span data-stu-id="a167d-133">string</span></span><br/> | <span data-ttu-id="a167d-134">characters</span><span class="sxs-lookup"><span data-stu-id="a167d-134">characters</span></span><br/> | <span data-ttu-id="a167d-135">Nome totalmente qualificado válido, conforme definido pelos [namespaces em XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span><span class="sxs-lookup"><span data-stu-id="a167d-135">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="a167d-136">Se nenhum namespace for especificado, o namespace padrão será assumido.</span><span class="sxs-lookup"><span data-stu-id="a167d-136">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="a167d-137">O nome da opção.</span><span class="sxs-lookup"><span data-stu-id="a167d-137">The name of the option.</span></span><br/>                                           |
| <span data-ttu-id="a167d-138">\_IdentityOptionValue\_</span><span class="sxs-lookup"><span data-stu-id="a167d-138">\_IdentityOptionValue\_</span></span><br/> | <span data-ttu-id="a167d-139">string</span><span class="sxs-lookup"><span data-stu-id="a167d-139">string</span></span><br/> | <span data-ttu-id="a167d-140">N/D</span><span class="sxs-lookup"><span data-stu-id="a167d-140">n/a</span></span><br/>        | <span data-ttu-id="a167d-141">True, False.</span><span class="sxs-lookup"><span data-stu-id="a167d-141">True, False.</span></span><br/>                                                                                                                                                               | <span data-ttu-id="a167d-142">Define uma opção que, quando selecionada, desabilita esse recurso.</span><span class="sxs-lookup"><span data-stu-id="a167d-142">Defines an Option which when selected would disable this feature.</span></span><br/> |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="a167d-143">Conteúdo de linguagem XML (XML)</span><span class="sxs-lookup"><span data-stu-id="a167d-143">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="a167d-144">As palavras-chave do esquema de impressão pública são definidas no https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span><span class="sxs-lookup"><span data-stu-id="a167d-144">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="a167d-145">O conteúdo do linguagem XML público (XML) para essa palavra-chave é definido abaixo:</span><span class="sxs-lookup"><span data-stu-id="a167d-145">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

``` syntax
<psf:Feature name="psk:DocumentHolePunch">
  <psf:Property name="psf:SelectionType">
    <psf:Value xsi:type="xs:string">psk:PickOne</psf:Value>
  </psf:Property>
  <!-- Specifies hole(s) along the bottom edge. -->
  <psf:Option name="psk:BottomEdge" />
  <!-- Specifies hole(s) along the left edge. -->
  <psf:Option name="psk:LeftEdge" />
  <!-- Specifies no hole punching. -->
  <psf:Option name="psk:None" />
  <!-- Specifies hole(s) along the right edge. -->
  <psf:Option name="psk:RightEdge" />
  <!-- Specifies hole(s) along the top edge. -->
  <psf:Option name="psk:TopEdge" />
</psf:Feature>    
```

## <a name="related-topics"></a><span data-ttu-id="a167d-146">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="a167d-146">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a167d-147">Especificação de esquema de impressão</span><span class="sxs-lookup"><span data-stu-id="a167d-147">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




