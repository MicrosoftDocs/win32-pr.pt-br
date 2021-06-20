---
description: Saiba mais sobre o elemento DocumentSeparatorSheet, que descreve o uso de folha de separador para um documento.
ms.assetid: f0b2192d-4bb7-4ba2-8dd0-35a20183ea31
title: DocumentSeparatorSheet
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 38195c2d1c52e5c02d9da4844b5fa981866a61bc
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/19/2021
ms.locfileid: "112409159"
---
# <a name="documentseparatorsheet"></a><span data-ttu-id="3d081-103">DocumentSeparatorSheet</span><span class="sxs-lookup"><span data-stu-id="3d081-103">DocumentSeparatorSheet</span></span>

<span data-ttu-id="3d081-104">Este tópico não é atual.</span><span class="sxs-lookup"><span data-stu-id="3d081-104">This topic is not current.</span></span> <span data-ttu-id="3d081-105">Para obter as informações mais atuais, consulte a [Especificação de Esquema de Impressão](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="3d081-105">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="3d081-106">Descreve o uso de folha de separador para um documento.</span><span class="sxs-lookup"><span data-stu-id="3d081-106">Describes the separator sheet usage for a document.</span></span> <span data-ttu-id="3d081-107">As folhas separadores devem aparecer na saída, conforme indicado pela Opção especificada abaixo.</span><span class="sxs-lookup"><span data-stu-id="3d081-107">Separator sheets should appear in the output as indicated by the Option specified below.</span></span>

-   [<span data-ttu-id="3d081-108">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="3d081-108">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="3d081-109">Conteúdo estrutural</span><span class="sxs-lookup"><span data-stu-id="3d081-109">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="3d081-110">linguagem XML conteúdo (XML)</span><span class="sxs-lookup"><span data-stu-id="3d081-110">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="3d081-111">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="3d081-111">Element Information</span></span>



| <span data-ttu-id="3d081-112">Name</span><span class="sxs-lookup"><span data-stu-id="3d081-112">Name</span></span> | <span data-ttu-id="3d081-113">Valor</span><span class="sxs-lookup"><span data-stu-id="3d081-113">Value</span></span> |
|----------------------------|---------------------|
| <span data-ttu-id="3d081-114">Tipo de elemento</span><span class="sxs-lookup"><span data-stu-id="3d081-114">Element Type</span></span> <br/>   | <span data-ttu-id="3d081-115">Recurso</span><span class="sxs-lookup"><span data-stu-id="3d081-115">Feature</span></span><br/>  |
| <span data-ttu-id="3d081-116">Prefixo de definição de scoping</span><span class="sxs-lookup"><span data-stu-id="3d081-116">Scoping Prefix</span></span> <br/> | <span data-ttu-id="3d081-117">Documento</span><span class="sxs-lookup"><span data-stu-id="3d081-117">Document</span></span><br/> |
| <span data-ttu-id="3d081-118">Observações</span><span class="sxs-lookup"><span data-stu-id="3d081-118">Notes</span></span> <br/>          | <span data-ttu-id="3d081-119">Nenhum</span><span class="sxs-lookup"><span data-stu-id="3d081-119">None</span></span><br/>     |



 

## <a name="structural-content"></a><span data-ttu-id="3d081-120">Conteúdo estrutural</span><span class="sxs-lookup"><span data-stu-id="3d081-120">Structural Content</span></span>

<span data-ttu-id="3d081-121">A estrutura XML desse elemento é:</span><span class="sxs-lookup"><span data-stu-id="3d081-121">The XML structure of this element is:</span></span>

``` syntax
<psf:Feature name="psk:DocumentSeparatorSheet">
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

## <a name="structure-variables"></a><span data-ttu-id="3d081-122">Variáveis de estrutura</span><span class="sxs-lookup"><span data-stu-id="3d081-122">Structure Variables</span></span>

<span data-ttu-id="3d081-123">A tabela a seguir descreve as características das variáveis definidas na estrutura XML.</span><span class="sxs-lookup"><span data-stu-id="3d081-123">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="3d081-124">Nome</span><span class="sxs-lookup"><span data-stu-id="3d081-124">Name</span></span>                               | <span data-ttu-id="3d081-125">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="3d081-125">Data type</span></span>         | <span data-ttu-id="3d081-126">Unidade</span><span class="sxs-lookup"><span data-stu-id="3d081-126">Unit</span></span>                  | <span data-ttu-id="3d081-127">Valores com suporte</span><span class="sxs-lookup"><span data-stu-id="3d081-127">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="3d081-128">Resumo</span><span class="sxs-lookup"><span data-stu-id="3d081-128">Summary</span></span>                                                                      |
|------------------------------------|-------------------|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="3d081-129">\_Optionname\_</span><span class="sxs-lookup"><span data-stu-id="3d081-129">\_OptionName\_</span></span><br/>          | <span data-ttu-id="3d081-130">string</span><span class="sxs-lookup"><span data-stu-id="3d081-130">string</span></span><br/> | <span data-ttu-id="3d081-131">characters</span><span class="sxs-lookup"><span data-stu-id="3d081-131">characters</span></span><br/> | <span data-ttu-id="3d081-132">Nome totalmente qualificado válido, conforme definido [por Namespaces em XML.](https://www.w3.org/TR/1999/REC-xml-names-19990114/)</span><span class="sxs-lookup"><span data-stu-id="3d081-132">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="3d081-133">Se nenhum namespace for especificado, o namespace padrão será assumido.</span><span class="sxs-lookup"><span data-stu-id="3d081-133">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="3d081-134">O nome da opção.</span><span class="sxs-lookup"><span data-stu-id="3d081-134">The name of the option.</span></span><br/>                                           |
| <span data-ttu-id="3d081-135">\_IdentityOptionValue\_</span><span class="sxs-lookup"><span data-stu-id="3d081-135">\_IdentityOptionValue\_</span></span><br/> | <span data-ttu-id="3d081-136">string</span><span class="sxs-lookup"><span data-stu-id="3d081-136">string</span></span><br/> | <span data-ttu-id="3d081-137">n/d</span><span class="sxs-lookup"><span data-stu-id="3d081-137">n/a</span></span><br/>        | <span data-ttu-id="3d081-138">True, False.</span><span class="sxs-lookup"><span data-stu-id="3d081-138">True, False.</span></span><br/>                                                                                                                                                               | <span data-ttu-id="3d081-139">Define uma Opção que, quando selecionada, desabilitará esse recurso.</span><span class="sxs-lookup"><span data-stu-id="3d081-139">Defines an Option which when selected would disable this feature.</span></span><br/> |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="3d081-140">linguagem XML conteúdo (XML)</span><span class="sxs-lookup"><span data-stu-id="3d081-140">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="3d081-141">As palavras-chave public Print Schema são definidas no https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace .</span><span class="sxs-lookup"><span data-stu-id="3d081-141">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="3d081-142">O conteúdo linguagem XML XML (public linguagem XML) para essa palavra-chave é definido abaixo:</span><span class="sxs-lookup"><span data-stu-id="3d081-142">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

``` syntax
<psf:Feature name="psk:DocumentSeparatorSheet">
  <psf:Property name="psf:SelectionType">
    <psf:Value xsi:type="xs:string">psk:PickOne</psf:Value>
  </psf:Property>
  <!-- Specifies a separator sheet at the start and end of the document. -->
  <psf:Option name="psk:BothSheets" />
  <!-- Specifies a separator sheet at the end of the document. -->
  <psf:Option name="psk:EndSheet" />
  <!-- Specifies no separator sheet(s). -->
  <psf:Option name="psk:None" />
  <!-- Specifies a separator sheet at the start of the document. -->
  <psf:Option name="psk:StartSheet" />
</psf:Feature>
    
```

## <a name="related-topics"></a><span data-ttu-id="3d081-143">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="3d081-143">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3d081-144">Especificação de esquema de impressão</span><span class="sxs-lookup"><span data-stu-id="3d081-144">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




