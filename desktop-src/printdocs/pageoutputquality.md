---
description: Saiba mais sobre o elemento configurável pelo usuário PageOutputQuality. Este tópico não é atual. Para obter as informações mais atuais, consulte a Especificação de Esquema de Impressão.
ms.assetid: 4720f812-a71a-458f-85fa-7885cca0dbbb
title: PageOutputQuality
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8001d8ffd6bb3ead50a27b9ea36c9849c475576f
ms.sourcegitcommit: 91530c19d26ba4c57a6af1f37b57f211f580464e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/19/2021
ms.locfileid: "112395581"
---
# <a name="pageoutputquality"></a><span data-ttu-id="f7361-105">PageOutputQuality</span><span class="sxs-lookup"><span data-stu-id="f7361-105">PageOutputQuality</span></span>

<span data-ttu-id="f7361-106">Este tópico não é atual.</span><span class="sxs-lookup"><span data-stu-id="f7361-106">This topic is not current.</span></span> <span data-ttu-id="f7361-107">Para obter as informações mais atuais, consulte a [Especificação de Esquema de Impressão](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="f7361-107">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="f7361-108">Descreve o nível de qualidade da saída.</span><span class="sxs-lookup"><span data-stu-id="f7361-108">Describes the quality level of the output.</span></span>

-   [<span data-ttu-id="f7361-109">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="f7361-109">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="f7361-110">Conteúdo estrutural</span><span class="sxs-lookup"><span data-stu-id="f7361-110">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="f7361-111">linguagem XML conteúdo (XML)</span><span class="sxs-lookup"><span data-stu-id="f7361-111">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="f7361-112">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="f7361-112">Element Information</span></span>



| <span data-ttu-id="f7361-113">Name</span><span class="sxs-lookup"><span data-stu-id="f7361-113">Name</span></span> | <span data-ttu-id="f7361-114">Valor</span><span class="sxs-lookup"><span data-stu-id="f7361-114">Value</span></span> |
|----------------------------|--------------------|
| <span data-ttu-id="f7361-115">Tipo de elemento</span><span class="sxs-lookup"><span data-stu-id="f7361-115">Element Type</span></span> <br/>   | <span data-ttu-id="f7361-116">Recurso</span><span class="sxs-lookup"><span data-stu-id="f7361-116">Feature</span></span><br/> |
| <span data-ttu-id="f7361-117">Prefixo de definição de scoping</span><span class="sxs-lookup"><span data-stu-id="f7361-117">Scoping Prefix</span></span> <br/> | <span data-ttu-id="f7361-118">?</span><span class="sxs-lookup"><span data-stu-id="f7361-118">Page</span></span><br/>    |
| <span data-ttu-id="f7361-119">Observações</span><span class="sxs-lookup"><span data-stu-id="f7361-119">Notes</span></span> <br/>          | <span data-ttu-id="f7361-120">Nenhum</span><span class="sxs-lookup"><span data-stu-id="f7361-120">None</span></span><br/>    |



 

## <a name="structural-content"></a><span data-ttu-id="f7361-121">Conteúdo estrutural</span><span class="sxs-lookup"><span data-stu-id="f7361-121">Structural Content</span></span>

<span data-ttu-id="f7361-122">A estrutura XML desse elemento é:</span><span class="sxs-lookup"><span data-stu-id="f7361-122">The XML structure of this element is:</span></span>

``` syntax
<psf:Feature name="psk:PageOutputQuality">
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

## <a name="structure-variables"></a><span data-ttu-id="f7361-123">Variáveis de estrutura</span><span class="sxs-lookup"><span data-stu-id="f7361-123">Structure Variables</span></span>

<span data-ttu-id="f7361-124">A tabela a seguir descreve as características das variáveis definidas na estrutura XML.</span><span class="sxs-lookup"><span data-stu-id="f7361-124">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="f7361-125">Nome</span><span class="sxs-lookup"><span data-stu-id="f7361-125">Name</span></span>                               | <span data-ttu-id="f7361-126">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="f7361-126">Data type</span></span>         | <span data-ttu-id="f7361-127">Unidade</span><span class="sxs-lookup"><span data-stu-id="f7361-127">Unit</span></span>                  | <span data-ttu-id="f7361-128">Valores com suporte</span><span class="sxs-lookup"><span data-stu-id="f7361-128">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="f7361-129">Resumo</span><span class="sxs-lookup"><span data-stu-id="f7361-129">Summary</span></span>                                                                      |
|------------------------------------|-------------------|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="f7361-130">\_Optionname\_</span><span class="sxs-lookup"><span data-stu-id="f7361-130">\_OptionName\_</span></span><br/>          | <span data-ttu-id="f7361-131">string</span><span class="sxs-lookup"><span data-stu-id="f7361-131">string</span></span><br/> | <span data-ttu-id="f7361-132">characters</span><span class="sxs-lookup"><span data-stu-id="f7361-132">characters</span></span><br/> | <span data-ttu-id="f7361-133">Nome totalmente qualificado válido, conforme definido [por Namespaces em XML.](https://www.w3.org/TR/1999/REC-xml-names-19990114/)</span><span class="sxs-lookup"><span data-stu-id="f7361-133">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="f7361-134">Se nenhum namespace for especificado, o namespace padrão será assumido.</span><span class="sxs-lookup"><span data-stu-id="f7361-134">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="f7361-135">O nome da opção</span><span class="sxs-lookup"><span data-stu-id="f7361-135">The name of the option</span></span><br/>                                            |
| <span data-ttu-id="f7361-136">\_IdentityOptionValue\_</span><span class="sxs-lookup"><span data-stu-id="f7361-136">\_IdentityOptionValue\_</span></span><br/> | <span data-ttu-id="f7361-137">string</span><span class="sxs-lookup"><span data-stu-id="f7361-137">string</span></span><br/> | <span data-ttu-id="f7361-138">n/d</span><span class="sxs-lookup"><span data-stu-id="f7361-138">n/a</span></span><br/>        | <span data-ttu-id="f7361-139">Verdadeiro, Falso</span><span class="sxs-lookup"><span data-stu-id="f7361-139">True, False</span></span><br/>                                                                                                                                                                | <span data-ttu-id="f7361-140">Define uma Opção que, quando selecionada, desabilitará esse recurso.</span><span class="sxs-lookup"><span data-stu-id="f7361-140">Defines an Option which when selected would disable this feature.</span></span><br/> |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="f7361-141">linguagem XML conteúdo (XML)</span><span class="sxs-lookup"><span data-stu-id="f7361-141">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="f7361-142">As palavras-chave public Print Schema são definidas no https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace .</span><span class="sxs-lookup"><span data-stu-id="f7361-142">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="f7361-143">O conteúdo linguagem XML XML (public linguagem XML) para essa palavra-chave é definido abaixo:</span><span class="sxs-lookup"><span data-stu-id="f7361-143">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

``` syntax
<psf:Feature name="psk:PageOutputQuality">
  <psf:Property name="psf:SelectionType">
    <psf:Value xsi:type="xs:string">psk:PickOne</psf:Value>
  </psf:Property>
  <!-- Specifies the intent for automatic output (allow the client to automatically choose the best settings). -->
  <psf:Option name="psk:Automatic" />
  <!-- Specifies the intent for draft output (balanced for draft quality text and graphics). -->
  <psf:Option name="psk:Draft" />
  <!-- Specifies the intent for fax output (balanced for standard fax quality). -->
  <psf:Option name="psk:Fax" />
  <!-- Specifies the intent for high quality output (balanced for high quality text and graphics). -->
  <psf:Option name="psk:High" />
  <!-- Specifies the intent for normal output (balanced for good quality text and graphics). -->
  <psf:Option name="psk:Normal" />
  <!-- Specifies the intent for photographic output (images should have the highest quality). -->
  <psf:Option name="psk:Photographic" />
  <!-- Specifies the intent for text only output (graphics may output poorly or not at all). -->
  <psf:Option name="psk:Text" />
</psf:Feature>
    
```

## <a name="related-topics"></a><span data-ttu-id="f7361-144">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="f7361-144">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f7361-145">Especificação de esquema de impressão</span><span class="sxs-lookup"><span data-stu-id="f7361-145">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




