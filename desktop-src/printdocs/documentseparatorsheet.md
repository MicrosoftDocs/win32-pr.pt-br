---
description: Este tópico não é atual. Para obter as informações mais atuais, consulte a especificação do esquema de impressão.
ms.assetid: f0b2192d-4bb7-4ba2-8dd0-35a20183ea31
title: DocumentSeparatorSheet
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cb6bd0d58c5b361b167d22c672b7e080e4498d3e
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/26/2021
ms.locfileid: "107997053"
---
# <a name="documentseparatorsheet"></a><span data-ttu-id="adf07-104">DocumentSeparatorSheet</span><span class="sxs-lookup"><span data-stu-id="adf07-104">DocumentSeparatorSheet</span></span>

<span data-ttu-id="adf07-105">Este tópico não é atual.</span><span class="sxs-lookup"><span data-stu-id="adf07-105">This topic is not current.</span></span> <span data-ttu-id="adf07-106">Para obter as informações mais atuais, consulte a [especificação do esquema de impressão](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="adf07-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="adf07-107">Descreve o uso da folha separadora de um documento.</span><span class="sxs-lookup"><span data-stu-id="adf07-107">Describes the separator sheet usage for a document.</span></span> <span data-ttu-id="adf07-108">As folhas separadoras devem aparecer na saída, conforme indicado pela opção especificada abaixo.</span><span class="sxs-lookup"><span data-stu-id="adf07-108">Separator sheets should appear in the output as indicated by the Option specified below.</span></span>

-   [<span data-ttu-id="adf07-109">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="adf07-109">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="adf07-110">Conteúdo estrutural</span><span class="sxs-lookup"><span data-stu-id="adf07-110">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="adf07-111">Conteúdo de linguagem XML (XML)</span><span class="sxs-lookup"><span data-stu-id="adf07-111">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="adf07-112">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="adf07-112">Element Information</span></span>



| <span data-ttu-id="adf07-113">Nome</span><span class="sxs-lookup"><span data-stu-id="adf07-113">Name</span></span> | <span data-ttu-id="adf07-114">Valor</span><span class="sxs-lookup"><span data-stu-id="adf07-114">Value</span></span> |
|----------------------------|---------------------|
| <span data-ttu-id="adf07-115">Tipo de elemento</span><span class="sxs-lookup"><span data-stu-id="adf07-115">Element Type</span></span> <br/>   | <span data-ttu-id="adf07-116">Recurso</span><span class="sxs-lookup"><span data-stu-id="adf07-116">Feature</span></span><br/>  |
| <span data-ttu-id="adf07-117">Prefixo de escopo</span><span class="sxs-lookup"><span data-stu-id="adf07-117">Scoping Prefix</span></span> <br/> | <span data-ttu-id="adf07-118">Documento</span><span class="sxs-lookup"><span data-stu-id="adf07-118">Document</span></span><br/> |
| <span data-ttu-id="adf07-119">Observações</span><span class="sxs-lookup"><span data-stu-id="adf07-119">Notes</span></span> <br/>          | <span data-ttu-id="adf07-120">Nenhum</span><span class="sxs-lookup"><span data-stu-id="adf07-120">None</span></span><br/>     |



 

## <a name="structural-content"></a><span data-ttu-id="adf07-121">Conteúdo estrutural</span><span class="sxs-lookup"><span data-stu-id="adf07-121">Structural Content</span></span>

<span data-ttu-id="adf07-122">A estrutura XML desse elemento é:</span><span class="sxs-lookup"><span data-stu-id="adf07-122">The XML structure of this element is:</span></span>

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

## <a name="structure-variables"></a><span data-ttu-id="adf07-123">Variáveis de estrutura</span><span class="sxs-lookup"><span data-stu-id="adf07-123">Structure Variables</span></span>

<span data-ttu-id="adf07-124">A tabela a seguir descreve as características das variáveis definidas na estrutura XML.</span><span class="sxs-lookup"><span data-stu-id="adf07-124">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="adf07-125">Nome</span><span class="sxs-lookup"><span data-stu-id="adf07-125">Name</span></span>                               | <span data-ttu-id="adf07-126">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="adf07-126">Data type</span></span>         | <span data-ttu-id="adf07-127">Unidade</span><span class="sxs-lookup"><span data-stu-id="adf07-127">Unit</span></span>                  | <span data-ttu-id="adf07-128">Valores com suporte</span><span class="sxs-lookup"><span data-stu-id="adf07-128">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="adf07-129">Resumo</span><span class="sxs-lookup"><span data-stu-id="adf07-129">Summary</span></span>                                                                      |
|------------------------------------|-------------------|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="adf07-130">\_OptionName\_</span><span class="sxs-lookup"><span data-stu-id="adf07-130">\_OptionName\_</span></span><br/>          | <span data-ttu-id="adf07-131">string</span><span class="sxs-lookup"><span data-stu-id="adf07-131">string</span></span><br/> | <span data-ttu-id="adf07-132">characters</span><span class="sxs-lookup"><span data-stu-id="adf07-132">characters</span></span><br/> | <span data-ttu-id="adf07-133">Nome totalmente qualificado válido, conforme definido pelos [namespaces em XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span><span class="sxs-lookup"><span data-stu-id="adf07-133">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="adf07-134">Se nenhum namespace for especificado, o namespace padrão será assumido.</span><span class="sxs-lookup"><span data-stu-id="adf07-134">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="adf07-135">O nome da opção.</span><span class="sxs-lookup"><span data-stu-id="adf07-135">The name of the option.</span></span><br/>                                           |
| <span data-ttu-id="adf07-136">\_IdentityOptionValue\_</span><span class="sxs-lookup"><span data-stu-id="adf07-136">\_IdentityOptionValue\_</span></span><br/> | <span data-ttu-id="adf07-137">string</span><span class="sxs-lookup"><span data-stu-id="adf07-137">string</span></span><br/> | <span data-ttu-id="adf07-138">N/D</span><span class="sxs-lookup"><span data-stu-id="adf07-138">n/a</span></span><br/>        | <span data-ttu-id="adf07-139">True, False.</span><span class="sxs-lookup"><span data-stu-id="adf07-139">True, False.</span></span><br/>                                                                                                                                                               | <span data-ttu-id="adf07-140">Define uma opção que, quando selecionada, desabilita esse recurso.</span><span class="sxs-lookup"><span data-stu-id="adf07-140">Defines an Option which when selected would disable this feature.</span></span><br/> |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="adf07-141">Conteúdo de linguagem XML (XML)</span><span class="sxs-lookup"><span data-stu-id="adf07-141">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="adf07-142">As palavras-chave do esquema de impressão pública são definidas no https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span><span class="sxs-lookup"><span data-stu-id="adf07-142">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="adf07-143">O conteúdo do linguagem XML público (XML) para essa palavra-chave é definido abaixo:</span><span class="sxs-lookup"><span data-stu-id="adf07-143">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

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

## <a name="related-topics"></a><span data-ttu-id="adf07-144">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="adf07-144">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="adf07-145">Especificação de esquema de impressão</span><span class="sxs-lookup"><span data-stu-id="adf07-145">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




