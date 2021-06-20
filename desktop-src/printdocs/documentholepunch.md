---
description: Saiba mais sobre o elemento DocumentHolePunch, que descreve as características de perfuração da saída.
ms.assetid: 46fd5e22-a2f3-424d-8c2f-2d5ac089a230
title: DocumentHolePunch
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 760559d3bb155030ff72a616096e5a860ba0d6b0
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/19/2021
ms.locfileid: "112409284"
---
# <a name="documentholepunch"></a><span data-ttu-id="b6d04-103">DocumentHolePunch</span><span class="sxs-lookup"><span data-stu-id="b6d04-103">DocumentHolePunch</span></span>

<span data-ttu-id="b6d04-104">Este tópico não é atual.</span><span class="sxs-lookup"><span data-stu-id="b6d04-104">This topic is not current.</span></span> <span data-ttu-id="b6d04-105">Para obter as informações mais atuais, consulte a [especificação do esquema de impressão](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="b6d04-105">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="b6d04-106">Descreve as características de perfuração da saída.</span><span class="sxs-lookup"><span data-stu-id="b6d04-106">Describes the hole punching characteristics of the output.</span></span> <span data-ttu-id="b6d04-107">Cada documento é perfurado separadamente.</span><span class="sxs-lookup"><span data-stu-id="b6d04-107">Each document is punched separately.</span></span> <span data-ttu-id="b6d04-108">As palavras-chave JobHolePunch e DocumentHolePunch são mutuamente exclusivas.</span><span class="sxs-lookup"><span data-stu-id="b6d04-108">The JobHolePunch and DocumentHolePunch keywords are mutually exclusive.</span></span> <span data-ttu-id="b6d04-109">Ambos não devem ser especificados simultaneamente em um documento de PrintTicket ou recursos de impressão.</span><span class="sxs-lookup"><span data-stu-id="b6d04-109">Both should not be specified simultaneously in a PrintTicket or Print Capabilities document.</span></span>

-   [<span data-ttu-id="b6d04-110">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="b6d04-110">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="b6d04-111">Conteúdo estrutural</span><span class="sxs-lookup"><span data-stu-id="b6d04-111">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="b6d04-112">Conteúdo de linguagem XML (XML)</span><span class="sxs-lookup"><span data-stu-id="b6d04-112">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="b6d04-113">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="b6d04-113">Element Information</span></span>



| <span data-ttu-id="b6d04-114">Name</span><span class="sxs-lookup"><span data-stu-id="b6d04-114">Name</span></span> | <span data-ttu-id="b6d04-115">Valor</span><span class="sxs-lookup"><span data-stu-id="b6d04-115">Value</span></span> |
|----------------------------|--------------------------------------------------------------------------------|
| <span data-ttu-id="b6d04-116">Tipo de elemento</span><span class="sxs-lookup"><span data-stu-id="b6d04-116">Element Type</span></span> <br/>   | <span data-ttu-id="b6d04-117">Recurso</span><span class="sxs-lookup"><span data-stu-id="b6d04-117">Feature</span></span><br/>                                                             |
| <span data-ttu-id="b6d04-118">Prefixo de escopo</span><span class="sxs-lookup"><span data-stu-id="b6d04-118">Scoping Prefix</span></span> <br/> | <span data-ttu-id="b6d04-119">Documento</span><span class="sxs-lookup"><span data-stu-id="b6d04-119">Document</span></span><br/>                                                            |
| <span data-ttu-id="b6d04-120">Observações</span><span class="sxs-lookup"><span data-stu-id="b6d04-120">Notes</span></span> <br/>          | <span data-ttu-id="b6d04-121">Superior, inferior, esquerda e direita são relativos ao PageImageableSize.</span><span class="sxs-lookup"><span data-stu-id="b6d04-121">Top, Bottom, Left, and Right are relative to the PageImageableSize.</span></span><br/> |



 

## <a name="structural-content"></a><span data-ttu-id="b6d04-122">Conteúdo estrutural</span><span class="sxs-lookup"><span data-stu-id="b6d04-122">Structural Content</span></span>

<span data-ttu-id="b6d04-123">A estrutura XML desse elemento é:</span><span class="sxs-lookup"><span data-stu-id="b6d04-123">The XML structure of this element is:</span></span>

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

## <a name="structure-variables"></a><span data-ttu-id="b6d04-124">Variáveis de estrutura</span><span class="sxs-lookup"><span data-stu-id="b6d04-124">Structure Variables</span></span>

<span data-ttu-id="b6d04-125">A tabela a seguir descreve as características das variáveis definidas na estrutura XML.</span><span class="sxs-lookup"><span data-stu-id="b6d04-125">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="b6d04-126">Nome</span><span class="sxs-lookup"><span data-stu-id="b6d04-126">Name</span></span>                               | <span data-ttu-id="b6d04-127">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="b6d04-127">Data type</span></span>         | <span data-ttu-id="b6d04-128">Unidade</span><span class="sxs-lookup"><span data-stu-id="b6d04-128">Unit</span></span>                  | <span data-ttu-id="b6d04-129">Valores com suporte</span><span class="sxs-lookup"><span data-stu-id="b6d04-129">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="b6d04-130">Resumo</span><span class="sxs-lookup"><span data-stu-id="b6d04-130">Summary</span></span>                                                                      |
|------------------------------------|-------------------|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="b6d04-131">\_OptionName\_</span><span class="sxs-lookup"><span data-stu-id="b6d04-131">\_OptionName\_</span></span><br/>          | <span data-ttu-id="b6d04-132">string</span><span class="sxs-lookup"><span data-stu-id="b6d04-132">string</span></span><br/> | <span data-ttu-id="b6d04-133">characters</span><span class="sxs-lookup"><span data-stu-id="b6d04-133">characters</span></span><br/> | <span data-ttu-id="b6d04-134">Nome totalmente qualificado válido, conforme definido pelos [namespaces em XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span><span class="sxs-lookup"><span data-stu-id="b6d04-134">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="b6d04-135">Se nenhum namespace for especificado, o namespace padrão será assumido.</span><span class="sxs-lookup"><span data-stu-id="b6d04-135">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="b6d04-136">O nome da opção.</span><span class="sxs-lookup"><span data-stu-id="b6d04-136">The name of the option.</span></span><br/>                                           |
| <span data-ttu-id="b6d04-137">\_IdentityOptionValue\_</span><span class="sxs-lookup"><span data-stu-id="b6d04-137">\_IdentityOptionValue\_</span></span><br/> | <span data-ttu-id="b6d04-138">string</span><span class="sxs-lookup"><span data-stu-id="b6d04-138">string</span></span><br/> | <span data-ttu-id="b6d04-139">n/d</span><span class="sxs-lookup"><span data-stu-id="b6d04-139">n/a</span></span><br/>        | <span data-ttu-id="b6d04-140">True, False.</span><span class="sxs-lookup"><span data-stu-id="b6d04-140">True, False.</span></span><br/>                                                                                                                                                               | <span data-ttu-id="b6d04-141">Define uma opção que, quando selecionada, desabilita esse recurso.</span><span class="sxs-lookup"><span data-stu-id="b6d04-141">Defines an Option which when selected would disable this feature.</span></span><br/> |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="b6d04-142">Conteúdo de linguagem XML (XML)</span><span class="sxs-lookup"><span data-stu-id="b6d04-142">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="b6d04-143">As palavras-chave do esquema de impressão pública são definidas no https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span><span class="sxs-lookup"><span data-stu-id="b6d04-143">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="b6d04-144">O conteúdo do linguagem XML público (XML) para essa palavra-chave é definido abaixo:</span><span class="sxs-lookup"><span data-stu-id="b6d04-144">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

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

## <a name="related-topics"></a><span data-ttu-id="b6d04-145">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="b6d04-145">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b6d04-146">Especificação de esquema de impressão</span><span class="sxs-lookup"><span data-stu-id="b6d04-146">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




