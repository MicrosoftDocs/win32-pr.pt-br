---
description: Saiba mais sobre o elemento JobAccountingSheet, que descreve a planilha de contabilidade a ser saída para o trabalho.
ms.assetid: fd16bd46-32e3-4896-ac5c-03c1bf6ad515
title: JobAccountingSheet
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 499d78db7a967e256ee79cd6e0c35d2f7d59dff4
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/19/2021
ms.locfileid: "112409090"
---
# <a name="jobaccountingsheet"></a><span data-ttu-id="ecdb9-103">JobAccountingSheet</span><span class="sxs-lookup"><span data-stu-id="ecdb9-103">JobAccountingSheet</span></span>

<span data-ttu-id="ecdb9-104">Este tópico não é atual.</span><span class="sxs-lookup"><span data-stu-id="ecdb9-104">This topic is not current.</span></span> <span data-ttu-id="ecdb9-105">Para obter as informações mais atuais, consulte a [Especificação de Esquema de Impressão](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="ecdb9-105">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="ecdb9-106">Descreve a planilha de contabilidade a ser saída para o trabalho.</span><span class="sxs-lookup"><span data-stu-id="ecdb9-106">Describes the accounting sheet to be output for the job.</span></span> <span data-ttu-id="ecdb9-107">A planilha de contabilidade deve ser saída no PageMediaSize padrão e usando o PageMediaType padrão.</span><span class="sxs-lookup"><span data-stu-id="ecdb9-107">The accounting sheet should be output on the default PageMediaSize and using the default PageMediaType.</span></span> <span data-ttu-id="ecdb9-108">A planilha de contabilidade deve ser isolada do restante do trabalho.</span><span class="sxs-lookup"><span data-stu-id="ecdb9-108">The accounting sheet should to be isolated from the remainder of the job.</span></span> <span data-ttu-id="ecdb9-109">Isso significa que todas as opções de conclusão ou processamento (como JobDuplex, JobStaple ou JobBinding) não devem incluir a planilha de contabilidade.</span><span class="sxs-lookup"><span data-stu-id="ecdb9-109">This means that any finishing or processing options (such as JobDuplex, JobStaple, or JobBinding) should not include the accounting sheet.</span></span> <span data-ttu-id="ecdb9-110">A planilha de contabilidade pode ocorrer como a primeira ou a última página do trabalho a critério do implementador.</span><span class="sxs-lookup"><span data-stu-id="ecdb9-110">The accounting sheet may occur as the first or last page of the job at the implementer's discretion.</span></span>

-   [<span data-ttu-id="ecdb9-111">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="ecdb9-111">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="ecdb9-112">Conteúdo estrutural</span><span class="sxs-lookup"><span data-stu-id="ecdb9-112">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="ecdb9-113">linguagem XML conteúdo (XML)</span><span class="sxs-lookup"><span data-stu-id="ecdb9-113">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="ecdb9-114">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="ecdb9-114">Element Information</span></span>



| <span data-ttu-id="ecdb9-115">Name</span><span class="sxs-lookup"><span data-stu-id="ecdb9-115">Name</span></span> | <span data-ttu-id="ecdb9-116">Valor</span><span class="sxs-lookup"><span data-stu-id="ecdb9-116">Value</span></span> |
|----------------------------|--------------------|
| <span data-ttu-id="ecdb9-117">Tipo de elemento</span><span class="sxs-lookup"><span data-stu-id="ecdb9-117">Element Type</span></span> <br/>   | <span data-ttu-id="ecdb9-118">Recurso</span><span class="sxs-lookup"><span data-stu-id="ecdb9-118">Feature</span></span><br/> |
| <span data-ttu-id="ecdb9-119">Prefixo de definição de scoping</span><span class="sxs-lookup"><span data-stu-id="ecdb9-119">Scoping Prefix</span></span> <br/> | <span data-ttu-id="ecdb9-120">Trabalho</span><span class="sxs-lookup"><span data-stu-id="ecdb9-120">Job</span></span><br/>     |
| <span data-ttu-id="ecdb9-121">Observações</span><span class="sxs-lookup"><span data-stu-id="ecdb9-121">Notes</span></span> <br/>          | <span data-ttu-id="ecdb9-122">Nenhum</span><span class="sxs-lookup"><span data-stu-id="ecdb9-122">None</span></span><br/>    |



 

## <a name="structural-content"></a><span data-ttu-id="ecdb9-123">Conteúdo estrutural</span><span class="sxs-lookup"><span data-stu-id="ecdb9-123">Structural Content</span></span>

<span data-ttu-id="ecdb9-124">A estrutura XML desse elemento é:</span><span class="sxs-lookup"><span data-stu-id="ecdb9-124">The XML structure of this element is:</span></span>

``` syntax
<psf:Feature name="psk:JobAccountingSheet">
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

## <a name="structure-variables"></a><span data-ttu-id="ecdb9-125">Variáveis de estrutura</span><span class="sxs-lookup"><span data-stu-id="ecdb9-125">Structure Variables</span></span>

<span data-ttu-id="ecdb9-126">A tabela a seguir descreve as características das variáveis definidas na estrutura XML.</span><span class="sxs-lookup"><span data-stu-id="ecdb9-126">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="ecdb9-127">Nome</span><span class="sxs-lookup"><span data-stu-id="ecdb9-127">Name</span></span>                               | <span data-ttu-id="ecdb9-128">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="ecdb9-128">Data type</span></span>         | <span data-ttu-id="ecdb9-129">Unidade</span><span class="sxs-lookup"><span data-stu-id="ecdb9-129">Unit</span></span>                  | <span data-ttu-id="ecdb9-130">Valores com suporte</span><span class="sxs-lookup"><span data-stu-id="ecdb9-130">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="ecdb9-131">Resumo</span><span class="sxs-lookup"><span data-stu-id="ecdb9-131">Summary</span></span>                                                                      |
|------------------------------------|-------------------|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="ecdb9-132">\_Optionname\_</span><span class="sxs-lookup"><span data-stu-id="ecdb9-132">\_OptionName\_</span></span><br/>          | <span data-ttu-id="ecdb9-133">string</span><span class="sxs-lookup"><span data-stu-id="ecdb9-133">string</span></span><br/> | <span data-ttu-id="ecdb9-134">characters</span><span class="sxs-lookup"><span data-stu-id="ecdb9-134">characters</span></span><br/> | <span data-ttu-id="ecdb9-135">Nome totalmente qualificado válido, conforme definido [por Namespaces em XML.](https://www.w3.org/TR/1999/REC-xml-names-19990114/)</span><span class="sxs-lookup"><span data-stu-id="ecdb9-135">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="ecdb9-136">Se nenhum namespace for especificado, o namespace padrão será assumido.</span><span class="sxs-lookup"><span data-stu-id="ecdb9-136">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="ecdb9-137">O nome da opção.</span><span class="sxs-lookup"><span data-stu-id="ecdb9-137">The name of the option.</span></span><br/>                                           |
| <span data-ttu-id="ecdb9-138">\_IdentityOptionValue\_</span><span class="sxs-lookup"><span data-stu-id="ecdb9-138">\_IdentityOptionValue\_</span></span><br/> | <span data-ttu-id="ecdb9-139">string</span><span class="sxs-lookup"><span data-stu-id="ecdb9-139">string</span></span><br/> | <span data-ttu-id="ecdb9-140">n/d</span><span class="sxs-lookup"><span data-stu-id="ecdb9-140">n/a</span></span><br/>        | <span data-ttu-id="ecdb9-141">True, False.</span><span class="sxs-lookup"><span data-stu-id="ecdb9-141">True, False.</span></span><br/>                                                                                                                                                               | <span data-ttu-id="ecdb9-142">Define uma Opção que, quando selecionada, desabilitará esse recurso.</span><span class="sxs-lookup"><span data-stu-id="ecdb9-142">Defines an Option which when selected would disable this feature.</span></span><br/> |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="ecdb9-143">linguagem XML conteúdo (XML)</span><span class="sxs-lookup"><span data-stu-id="ecdb9-143">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="ecdb9-144">As palavras-chave public Print Schema são definidas no https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace .</span><span class="sxs-lookup"><span data-stu-id="ecdb9-144">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="ecdb9-145">O conteúdo linguagem XML XML (public linguagem XML) para essa palavra-chave é definido abaixo:</span><span class="sxs-lookup"><span data-stu-id="ecdb9-145">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

``` syntax
<psf:Feature name="psk:JobAccountingSheet">
  <psf:Property name="psf:SelectionType">
    <psf:Value xsi:type="xs:string">psk:PickOne</psf:Value>
  </psf:Property>
  <!-- Specifies no accounting sheet will be output. -->
  <psf:Option name="psk:None" />
  <!-- Specifies the standard (device defined) accounting sheet should be output. -->
  <psf:Option name="psk:Standard" />
</psf:Feature>
        
```

## <a name="related-topics"></a><span data-ttu-id="ecdb9-146">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="ecdb9-146">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ecdb9-147">Especificação de esquema de impressão</span><span class="sxs-lookup"><span data-stu-id="ecdb9-147">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




