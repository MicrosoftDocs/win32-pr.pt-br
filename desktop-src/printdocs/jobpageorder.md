---
description: Saiba mais sobre o elemento JobPageOrder, que define a ordem das páginas físicas para a saída.
ms.assetid: 0c255d50-8b0e-4ecd-876d-eaaccdca7b27
title: JobPageOrder
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fa2216330034c458095af7e67ff0904100126451
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/19/2021
ms.locfileid: "112408739"
---
# <a name="jobpageorder"></a><span data-ttu-id="ff633-103">JobPageOrder</span><span class="sxs-lookup"><span data-stu-id="ff633-103">JobPageOrder</span></span>

<span data-ttu-id="ff633-104">Este tópico não é atual.</span><span class="sxs-lookup"><span data-stu-id="ff633-104">This topic is not current.</span></span> <span data-ttu-id="ff633-105">Para obter as informações mais atuais, consulte a [Especificação de Esquema de Impressão](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="ff633-105">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="ff633-106">Define a ordem das páginas físicas para a saída.</span><span class="sxs-lookup"><span data-stu-id="ff633-106">Defines the order of physical pages for the output.</span></span>

-   [<span data-ttu-id="ff633-107">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="ff633-107">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="ff633-108">Conteúdo estrutural</span><span class="sxs-lookup"><span data-stu-id="ff633-108">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="ff633-109">linguagem XML conteúdo (XML)</span><span class="sxs-lookup"><span data-stu-id="ff633-109">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="ff633-110">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="ff633-110">Element Information</span></span>



| <span data-ttu-id="ff633-111">Name</span><span class="sxs-lookup"><span data-stu-id="ff633-111">Name</span></span> | <span data-ttu-id="ff633-112">Valor</span><span class="sxs-lookup"><span data-stu-id="ff633-112">Value</span></span> |
|----------------------------|--------------------|
| <span data-ttu-id="ff633-113">Tipo de elemento</span><span class="sxs-lookup"><span data-stu-id="ff633-113">Element Type</span></span> <br/>   | <span data-ttu-id="ff633-114">Recurso</span><span class="sxs-lookup"><span data-stu-id="ff633-114">Feature</span></span><br/> |
| <span data-ttu-id="ff633-115">Prefixo de definição de scoping</span><span class="sxs-lookup"><span data-stu-id="ff633-115">Scoping Prefix</span></span> <br/> | <span data-ttu-id="ff633-116">Trabalho</span><span class="sxs-lookup"><span data-stu-id="ff633-116">Job</span></span><br/>     |
| <span data-ttu-id="ff633-117">Observações</span><span class="sxs-lookup"><span data-stu-id="ff633-117">Notes</span></span> <br/>          | <span data-ttu-id="ff633-118">Nenhum</span><span class="sxs-lookup"><span data-stu-id="ff633-118">None</span></span><br/>    |



 

## <a name="structural-content"></a><span data-ttu-id="ff633-119">Conteúdo estrutural</span><span class="sxs-lookup"><span data-stu-id="ff633-119">Structural Content</span></span>

<span data-ttu-id="ff633-120">A estrutura XML desse elemento é:</span><span class="sxs-lookup"><span data-stu-id="ff633-120">The XML structure of this element is:</span></span>

``` syntax
<psf:Feature name="psk:JobPageOrder">
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

## <a name="structure-variables"></a><span data-ttu-id="ff633-121">Variáveis de estrutura</span><span class="sxs-lookup"><span data-stu-id="ff633-121">Structure Variables</span></span>

<span data-ttu-id="ff633-122">A tabela a seguir descreve as características das variáveis definidas na estrutura XML.</span><span class="sxs-lookup"><span data-stu-id="ff633-122">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="ff633-123">Nome</span><span class="sxs-lookup"><span data-stu-id="ff633-123">Name</span></span>                               | <span data-ttu-id="ff633-124">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="ff633-124">Data type</span></span>         | <span data-ttu-id="ff633-125">Unidade</span><span class="sxs-lookup"><span data-stu-id="ff633-125">Unit</span></span>                  | <span data-ttu-id="ff633-126">Valores com suporte</span><span class="sxs-lookup"><span data-stu-id="ff633-126">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="ff633-127">Resumo</span><span class="sxs-lookup"><span data-stu-id="ff633-127">Summary</span></span>                                                                      |
|------------------------------------|-------------------|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="ff633-128">\_Optionname\_</span><span class="sxs-lookup"><span data-stu-id="ff633-128">\_OptionName\_</span></span><br/>          | <span data-ttu-id="ff633-129">string</span><span class="sxs-lookup"><span data-stu-id="ff633-129">string</span></span><br/> | <span data-ttu-id="ff633-130">characters</span><span class="sxs-lookup"><span data-stu-id="ff633-130">characters</span></span><br/> | <span data-ttu-id="ff633-131">Nome totalmente qualificado válido, conforme definido [por Namespaces em XML.](https://www.w3.org/TR/1999/REC-xml-names-19990114/)</span><span class="sxs-lookup"><span data-stu-id="ff633-131">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="ff633-132">Se nenhum namespace for especificado, o namespace padrão será assumido.</span><span class="sxs-lookup"><span data-stu-id="ff633-132">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="ff633-133">O nome da opção.</span><span class="sxs-lookup"><span data-stu-id="ff633-133">The name of the option.</span></span><br/>                                           |
| <span data-ttu-id="ff633-134">\_IdentityOptionValue\_</span><span class="sxs-lookup"><span data-stu-id="ff633-134">\_IdentityOptionValue\_</span></span><br/> | <span data-ttu-id="ff633-135">string</span><span class="sxs-lookup"><span data-stu-id="ff633-135">string</span></span><br/> | <span data-ttu-id="ff633-136">n/d</span><span class="sxs-lookup"><span data-stu-id="ff633-136">n/a</span></span><br/>        | <span data-ttu-id="ff633-137">True, False.</span><span class="sxs-lookup"><span data-stu-id="ff633-137">True, False.</span></span><br/>                                                                                                                                                               | <span data-ttu-id="ff633-138">Define uma Opção que, quando selecionada, desabilitará esse recurso.</span><span class="sxs-lookup"><span data-stu-id="ff633-138">Defines an Option which when selected would disable this feature.</span></span><br/> |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="ff633-139">linguagem XML conteúdo (XML)</span><span class="sxs-lookup"><span data-stu-id="ff633-139">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="ff633-140">As palavras-chave public Print Schema são definidas no https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace .</span><span class="sxs-lookup"><span data-stu-id="ff633-140">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="ff633-141">O conteúdo linguagem XML XML (public linguagem XML) para essa palavra-chave é definido abaixo:</span><span class="sxs-lookup"><span data-stu-id="ff633-141">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

``` syntax
<psf:Feature name="psk:JobPageOrder">
  <psf:Property name="psf:SelectionType">
   <psf:Value xsi:type="xs:string">psk:PickOne</psf:Value>
  </psf:Property>
  <!-- Specifies front to back page order. -->
  <psf:Option name="psk:Standard" />
  <!-- Specifies back to front page order. -->
  <psf:Option name="psk:Reverse" />
</psf:Feature>
```

## <a name="related-topics"></a><span data-ttu-id="ff633-142">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="ff633-142">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ff633-143">Especificação de esquema de impressão</span><span class="sxs-lookup"><span data-stu-id="ff633-143">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




