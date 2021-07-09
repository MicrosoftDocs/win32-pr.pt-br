---
description: Obter informações sobre o elemento configurável pelo usuário JobHolePunch. Este tópico não é atual. Para obter as informações mais atuais, consulte a Especificação de Esquema de Impressão.
ms.assetid: 26e9e7d6-7c01-4687-aa64-7aea867b4e58
title: JobHolePunch
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7c82a36784ab6a1fb5eb0c8d682c45cce574ee9e
ms.sourcegitcommit: 998d50f6def8a25850fc113fc8a2df903c829c5e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/09/2021
ms.locfileid: "113549354"
---
# <a name="jobholepunch"></a><span data-ttu-id="a0061-105">JobHolePunch</span><span class="sxs-lookup"><span data-stu-id="a0061-105">JobHolePunch</span></span>

<span data-ttu-id="a0061-106">Este tópico não é atual.</span><span class="sxs-lookup"><span data-stu-id="a0061-106">This topic is not current.</span></span> <span data-ttu-id="a0061-107">Para obter as informações mais atuais, consulte a [Especificação de Esquema de Impressão](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="a0061-107">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="a0061-108">Descreve as características de ressarção de orifício da saída.</span><span class="sxs-lookup"><span data-stu-id="a0061-108">Describes the hole punching characteristics of the output.</span></span> <span data-ttu-id="a0061-109">Todos os documentos são organizados juntos.</span><span class="sxs-lookup"><span data-stu-id="a0061-109">All documents are punched together.</span></span> <span data-ttu-id="a0061-110">As palavras-chave JobHolePunch e DocumentHolePunch são mutuamente exclusivas.</span><span class="sxs-lookup"><span data-stu-id="a0061-110">The JobHolePunch and DocumentHolePunch keywords are mutually exclusive.</span></span> <span data-ttu-id="a0061-111">Ambos não devem ser especificados simultaneamente em um documento PrintTicket ou Recursos de Impressão.</span><span class="sxs-lookup"><span data-stu-id="a0061-111">Both should not be specified simultaneously in a PrintTicket or Print Capabilities document.</span></span>

-   [<span data-ttu-id="a0061-112">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="a0061-112">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="a0061-113">Conteúdo estrutural</span><span class="sxs-lookup"><span data-stu-id="a0061-113">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="a0061-114">linguagem XML conteúdo (XML)</span><span class="sxs-lookup"><span data-stu-id="a0061-114">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="a0061-115">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="a0061-115">Element Information</span></span>



| <span data-ttu-id="a0061-116">Nome</span><span class="sxs-lookup"><span data-stu-id="a0061-116">Name</span></span> | <span data-ttu-id="a0061-117">Valor</span><span class="sxs-lookup"><span data-stu-id="a0061-117">Value</span></span> |
|----------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a0061-118">Tipo de elemento</span><span class="sxs-lookup"><span data-stu-id="a0061-118">Element Type</span></span> <br/>   | <span data-ttu-id="a0061-119">Recurso</span><span class="sxs-lookup"><span data-stu-id="a0061-119">Feature</span></span><br/>                                                                                                                              |
| <span data-ttu-id="a0061-120">Prefixo de definição de scoping</span><span class="sxs-lookup"><span data-stu-id="a0061-120">Scoping Prefix</span></span> <br/> | <span data-ttu-id="a0061-121">Trabalho</span><span class="sxs-lookup"><span data-stu-id="a0061-121">Job</span></span><br/>                                                                                                                                  |
| <span data-ttu-id="a0061-122">Observações</span><span class="sxs-lookup"><span data-stu-id="a0061-122">Notes</span></span> <br/>          | <span data-ttu-id="a0061-123">Top, Bottom, Left e Right são relativos ao PageImageableSize, em que TopLeft é anotado pela origem do eixo x e do eixo y.</span><span class="sxs-lookup"><span data-stu-id="a0061-123">Top, Bottom, Left, and Right are relative to the PageImageableSize, where TopLeft is denoted by the origin of the x-axis and y-axis.</span></span><br/> |



 

## <a name="structural-content"></a><span data-ttu-id="a0061-124">Conteúdo estrutural</span><span class="sxs-lookup"><span data-stu-id="a0061-124">Structural Content</span></span>

<span data-ttu-id="a0061-125">A estrutura XML desse elemento é:</span><span class="sxs-lookup"><span data-stu-id="a0061-125">The XML structure of this element is:</span></span>

``` syntax
<psf:Feature name="psk:JobHolePunch">
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

## <a name="structure-variables"></a><span data-ttu-id="a0061-126">Variáveis de estrutura</span><span class="sxs-lookup"><span data-stu-id="a0061-126">Structure Variables</span></span>

<span data-ttu-id="a0061-127">A tabela a seguir descreve as características das variáveis definidas na estrutura XML.</span><span class="sxs-lookup"><span data-stu-id="a0061-127">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="a0061-128">Nome</span><span class="sxs-lookup"><span data-stu-id="a0061-128">Name</span></span>                               | <span data-ttu-id="a0061-129">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="a0061-129">Data type</span></span>         | <span data-ttu-id="a0061-130">Unidade</span><span class="sxs-lookup"><span data-stu-id="a0061-130">Unit</span></span>                  | <span data-ttu-id="a0061-131">Valores com suporte</span><span class="sxs-lookup"><span data-stu-id="a0061-131">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="a0061-132">Resumo</span><span class="sxs-lookup"><span data-stu-id="a0061-132">Summary</span></span>                                                                      |
|------------------------------------|-------------------|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="a0061-133">\_Optionname\_</span><span class="sxs-lookup"><span data-stu-id="a0061-133">\_OptionName\_</span></span><br/>          | <span data-ttu-id="a0061-134">string</span><span class="sxs-lookup"><span data-stu-id="a0061-134">string</span></span><br/> | <span data-ttu-id="a0061-135">characters</span><span class="sxs-lookup"><span data-stu-id="a0061-135">characters</span></span><br/> | <span data-ttu-id="a0061-136">Nome totalmente qualificado válido, conforme definido [por Namespaces em XML.](https://www.w3.org/TR/1999/REC-xml-names-19990114/)</span><span class="sxs-lookup"><span data-stu-id="a0061-136">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="a0061-137">Se nenhum namespace for especificado, o namespace padrão será assumido.</span><span class="sxs-lookup"><span data-stu-id="a0061-137">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="a0061-138">O nome da opção.</span><span class="sxs-lookup"><span data-stu-id="a0061-138">The name of the option.</span></span><br/>                                           |
| <span data-ttu-id="a0061-139">\_IdentityOptionValue\_</span><span class="sxs-lookup"><span data-stu-id="a0061-139">\_IdentityOptionValue\_</span></span><br/> | <span data-ttu-id="a0061-140">string</span><span class="sxs-lookup"><span data-stu-id="a0061-140">string</span></span><br/> | <span data-ttu-id="a0061-141">n/d</span><span class="sxs-lookup"><span data-stu-id="a0061-141">n/a</span></span><br/>        | <span data-ttu-id="a0061-142">True, False.</span><span class="sxs-lookup"><span data-stu-id="a0061-142">True, False.</span></span><br/>                                                                                                                                                               | <span data-ttu-id="a0061-143">Define uma Opção que, quando selecionada, desabilitará esse recurso.</span><span class="sxs-lookup"><span data-stu-id="a0061-143">Defines an Option which when selected would disable this feature.</span></span><br/> |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="a0061-144">linguagem XML conteúdo (XML)</span><span class="sxs-lookup"><span data-stu-id="a0061-144">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="a0061-145">As palavras-chave public Print Schema são definidas no https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace .</span><span class="sxs-lookup"><span data-stu-id="a0061-145">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="a0061-146">O conteúdo linguagem XML XML (public linguagem XML) para essa palavra-chave é definido abaixo:</span><span class="sxs-lookup"><span data-stu-id="a0061-146">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

``` syntax
<psf:Feature name="psk:JobHolePunch">
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

## <a name="related-topics"></a><span data-ttu-id="a0061-147">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="a0061-147">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a0061-148">Especificação de esquema de impressão</span><span class="sxs-lookup"><span data-stu-id="a0061-148">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




