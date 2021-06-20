---
description: Saiba mais sobre o elemento DocumentCollate, que descreve as características de colagem da saída.
ms.assetid: 752cccf7-1f95-4597-b0e2-a96fd22ffeef
title: DocumentCollate
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e4c3036cc64265ea8f88bfcc46aea0149f8af5ad
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/19/2021
ms.locfileid: "112409449"
---
# <a name="documentcollate"></a><span data-ttu-id="7890a-103">DocumentCollate</span><span class="sxs-lookup"><span data-stu-id="7890a-103">DocumentCollate</span></span>

<span data-ttu-id="7890a-104">Este tópico não é atual.</span><span class="sxs-lookup"><span data-stu-id="7890a-104">This topic is not current.</span></span> <span data-ttu-id="7890a-105">Para obter as informações mais atuais, consulte a [Especificação de Esquema de Impressão](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="7890a-105">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="7890a-106">Descreve as características de colagem da saída.</span><span class="sxs-lookup"><span data-stu-id="7890a-106">Describes the collating characteristics of the output.</span></span> <span data-ttu-id="7890a-107">Todas as páginas em cada documento individual são colladas.</span><span class="sxs-lookup"><span data-stu-id="7890a-107">All pages in each individual document are collated.</span></span> <span data-ttu-id="7890a-108">DocumentCollate e JobCollateAlldocuments são mutuamente exclusivos.</span><span class="sxs-lookup"><span data-stu-id="7890a-108">DocumentCollate and JobCollateAlldocuments are mutually exclusive.</span></span> <span data-ttu-id="7890a-109">O comportamento e a implementação de se ambas ou apenas uma dessas palavras-chave é implementada são deixadas para o driver.</span><span class="sxs-lookup"><span data-stu-id="7890a-109">The behavior and implementation of whether both or only one of these keywords is implemented is left to the driver.</span></span>

<span data-ttu-id="7890a-110">A seguir estão as regras que devem ser seguidas para a implementação de Collate</span><span class="sxs-lookup"><span data-stu-id="7890a-110">The following are the rules which should be followed for Collate implementation</span></span>

## <a name="element-definition-and-rules"></a><span data-ttu-id="7890a-111">Definição de elemento e regras</span><span class="sxs-lookup"><span data-stu-id="7890a-111">Element Definition and Rules</span></span>

<span data-ttu-id="7890a-112">Primeiro, você deve seguir as regras para JobCollateAllDocument e, em seguida, aplicar regras para DocumentCollate para que os cenários funcionem.</span><span class="sxs-lookup"><span data-stu-id="7890a-112">You must first follow the rules for JobCollateAllDocument, and then apply rules for DocumentCollate for the scenarios to work.</span></span> <span data-ttu-id="7890a-113">Observe que, em uma configuração de conversão PrintTicket para Devmode, em que JobCollateAllDocuments não é suportado pelo driver, cabe ao driver escolher o comportamento apropriado a ser tomada (JobCollateAllDocuments = ON ou OFF).</span><span class="sxs-lookup"><span data-stu-id="7890a-113">Note that in a PrintTicket to Devmode conversion setting, where JobCollateAllDocuments is not supported by the driver, it is up to the driver to choose the appropriate behavior to take (JobCollateAllDocuments = ON or OFF).</span></span> <span data-ttu-id="7890a-114">Além disso, a escolha pode ser alterada dependendo de outras configurações printTicket.</span><span class="sxs-lookup"><span data-stu-id="7890a-114">Also, the choice can be changed depending on other PrintTicket settings.</span></span>

### <a name="jobcollatealldocuments"></a><span data-ttu-id="7890a-115">JobCollateAllDocuments</span><span class="sxs-lookup"><span data-stu-id="7890a-115">JobCollateAllDocuments</span></span>

<span data-ttu-id="7890a-116">ON: imprima (DocumentCopiesAllPages) cópias de cada documento, repita JobCopiesAllDocuments vezes.</span><span class="sxs-lookup"><span data-stu-id="7890a-116">ON: Print (DocumentCopiesAllPages) copies of each document, repeat JobCopiesAllDocuments times.</span></span>

<span data-ttu-id="7890a-117">OFF: para cada documento, imprimir (JobCopiesAllDocuments x DocumentCopiesAllPages) copia juntas.</span><span class="sxs-lookup"><span data-stu-id="7890a-117">OFF: For each document, print (JobCopiesAllDocuments x DocumentCopiesAllPages) copies together.</span></span>

### <a name="documentcollate"></a><span data-ttu-id="7890a-118">DocumentCollate</span><span class="sxs-lookup"><span data-stu-id="7890a-118">DocumentCollate</span></span>

<span data-ttu-id="7890a-119">ON: para todas as cópias (JobCopiesAllDocuments x DocumentCopiesAllPages) de um documento impresso de forma contígua, cole planilhas nesse documento.</span><span class="sxs-lookup"><span data-stu-id="7890a-119">ON: For all copies (JobCopiesAllDocuments x DocumentCopiesAllPages) of a document printed contiguously, collate sheets in that document.</span></span>

<span data-ttu-id="7890a-120">OFF: para todas as cópias (JobCopiesAllDocuments x DocumentCopiesAllPages) impressas de forma contígua, imprima todas as cópias (JobCopiesAllDocuments x DocumentCopiesAllPages) de cada planilha juntas.</span><span class="sxs-lookup"><span data-stu-id="7890a-120">OFF: For all copies (JobCopiesAllDocuments x DocumentCopiesAllPages) printed contiguously, print all copies (JobCopiesAllDocuments x DocumentCopiesAllPages) of each sheet together.</span></span>

-   [<span data-ttu-id="7890a-121">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="7890a-121">Element Information</span></span>](#element-information)

-   [<span data-ttu-id="7890a-122">Conteúdo estrutural</span><span class="sxs-lookup"><span data-stu-id="7890a-122">Structural Content</span></span>](#structural-content)

-   [<span data-ttu-id="7890a-123">Conteúdo XML</span><span class="sxs-lookup"><span data-stu-id="7890a-123">XML Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="7890a-124">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="7890a-124">Element Information</span></span>



| <span data-ttu-id="7890a-125">Name</span><span class="sxs-lookup"><span data-stu-id="7890a-125">Name</span></span> | <span data-ttu-id="7890a-126">Valor</span><span class="sxs-lookup"><span data-stu-id="7890a-126">Value</span></span> |
|----------------------------|---------------------|
| <span data-ttu-id="7890a-127">Tipo de elemento</span><span class="sxs-lookup"><span data-stu-id="7890a-127">Element Type</span></span> <br/>   | <span data-ttu-id="7890a-128">Recurso</span><span class="sxs-lookup"><span data-stu-id="7890a-128">Feature</span></span><br/>  |
| <span data-ttu-id="7890a-129">Prefixo de definição de scoping</span><span class="sxs-lookup"><span data-stu-id="7890a-129">Scoping Prefix</span></span> <br/> | <span data-ttu-id="7890a-130">Documento</span><span class="sxs-lookup"><span data-stu-id="7890a-130">Document</span></span><br/> |
| <span data-ttu-id="7890a-131">Observações</span><span class="sxs-lookup"><span data-stu-id="7890a-131">Notes</span></span> <br/>          | <span data-ttu-id="7890a-132">Nenhum</span><span class="sxs-lookup"><span data-stu-id="7890a-132">None</span></span><br/>     |



 

## <a name="structural-content"></a><span data-ttu-id="7890a-133">Conteúdo estrutural</span><span class="sxs-lookup"><span data-stu-id="7890a-133">Structural Content</span></span>

<span data-ttu-id="7890a-134">A estrutura XML desse elemento é:</span><span class="sxs-lookup"><span data-stu-id="7890a-134">The XML structure of this element is:</span></span>

``` syntax
<psf:Feature name="psk:DocumentCollate">
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

## <a name="structure-variables"></a><span data-ttu-id="7890a-135">Variáveis de estrutura</span><span class="sxs-lookup"><span data-stu-id="7890a-135">Structure Variables</span></span>

<span data-ttu-id="7890a-136">A tabela a seguir descreve as características das variáveis definidas na estrutura XML.</span><span class="sxs-lookup"><span data-stu-id="7890a-136">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="7890a-137">Nome</span><span class="sxs-lookup"><span data-stu-id="7890a-137">Name</span></span>                               | <span data-ttu-id="7890a-138">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="7890a-138">Data type</span></span>         | <span data-ttu-id="7890a-139">Unidade</span><span class="sxs-lookup"><span data-stu-id="7890a-139">Unit</span></span>                  | <span data-ttu-id="7890a-140">Valores com suporte</span><span class="sxs-lookup"><span data-stu-id="7890a-140">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="7890a-141">Resumo</span><span class="sxs-lookup"><span data-stu-id="7890a-141">Summary</span></span>                                                                      |
|------------------------------------|-------------------|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="7890a-142">\_Optionname\_</span><span class="sxs-lookup"><span data-stu-id="7890a-142">\_OptionName\_</span></span><br/>          | <span data-ttu-id="7890a-143">string</span><span class="sxs-lookup"><span data-stu-id="7890a-143">string</span></span><br/> | <span data-ttu-id="7890a-144">characters</span><span class="sxs-lookup"><span data-stu-id="7890a-144">characters</span></span><br/> | <span data-ttu-id="7890a-145">Nome totalmente qualificado válido, conforme definido [por Namespaces em XML.](https://www.w3.org/TR/1999/REC-xml-names-19990114/)</span><span class="sxs-lookup"><span data-stu-id="7890a-145">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="7890a-146">Se nenhum namespace for especificado, o namespace padrão será assumido.</span><span class="sxs-lookup"><span data-stu-id="7890a-146">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="7890a-147">O nome da opção.</span><span class="sxs-lookup"><span data-stu-id="7890a-147">The name of the option.</span></span><br/>                                           |
| <span data-ttu-id="7890a-148">\_IdentityOptionValue\_</span><span class="sxs-lookup"><span data-stu-id="7890a-148">\_IdentityOptionValue\_</span></span><br/> | <span data-ttu-id="7890a-149">string</span><span class="sxs-lookup"><span data-stu-id="7890a-149">string</span></span><br/> | <span data-ttu-id="7890a-150">n/d</span><span class="sxs-lookup"><span data-stu-id="7890a-150">n/a</span></span><br/>        | <span data-ttu-id="7890a-151">True, False.</span><span class="sxs-lookup"><span data-stu-id="7890a-151">True, False.</span></span><br/>                                                                                                                                                               | <span data-ttu-id="7890a-152">Define uma Opção que, quando selecionada, desabilitará esse recurso.</span><span class="sxs-lookup"><span data-stu-id="7890a-152">Defines an Option which when selected would disable this feature.</span></span><br/> |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="7890a-153">linguagem XML conteúdo (XML)</span><span class="sxs-lookup"><span data-stu-id="7890a-153">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="7890a-154">As palavras-chave public Print Schema são definidas no https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace .</span><span class="sxs-lookup"><span data-stu-id="7890a-154">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="7890a-155">O conteúdo linguagem XML XML (public linguagem XML) para essa palavra-chave é definido abaixo:</span><span class="sxs-lookup"><span data-stu-id="7890a-155">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

``` syntax
<psf:Feature name="psk:DocumentCollate">
  <psf:Property name="psf:SelectionType">
    <psf:Value xsi:type="xs:string">psk:PickOne</psf:Value>
  </psf:Property>
  <!-- Specifies collating.  -->
  <psf:Option name="psk:Collated" />
  <!-- Specifies no collating. -->
  <psf:Option name="psk:Uncollated" />
</psf:Feature>
```

## <a name="related-topics"></a><span data-ttu-id="7890a-156">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="7890a-156">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7890a-157">Especificação de esquema de impressão</span><span class="sxs-lookup"><span data-stu-id="7890a-157">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




