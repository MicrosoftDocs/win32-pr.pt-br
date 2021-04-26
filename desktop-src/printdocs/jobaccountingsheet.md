---
description: Este tópico não é atual. Para obter as informações mais atuais, consulte a especificação do esquema de impressão.
ms.assetid: fd16bd46-32e3-4896-ac5c-03c1bf6ad515
title: JobAccountingSheet
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 30ffb70ba0ac1a78eefc1024d8e93dc642439aed
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/26/2021
ms.locfileid: "107998423"
---
# <a name="jobaccountingsheet"></a><span data-ttu-id="5b05a-104">JobAccountingSheet</span><span class="sxs-lookup"><span data-stu-id="5b05a-104">JobAccountingSheet</span></span>

<span data-ttu-id="5b05a-105">Este tópico não é atual.</span><span class="sxs-lookup"><span data-stu-id="5b05a-105">This topic is not current.</span></span> <span data-ttu-id="5b05a-106">Para obter as informações mais atuais, consulte a [especificação do esquema de impressão](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="5b05a-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="5b05a-107">Descreve a planilha de contabilidade a ser impressa para o trabalho.</span><span class="sxs-lookup"><span data-stu-id="5b05a-107">Describes the accounting sheet to be output for the job.</span></span> <span data-ttu-id="5b05a-108">A folha contábil deve ser saída no PageMediaSize padrão e usando o PageMediaType padrão.</span><span class="sxs-lookup"><span data-stu-id="5b05a-108">The accounting sheet should be output on the default PageMediaSize and using the default PageMediaType.</span></span> <span data-ttu-id="5b05a-109">A folha de contabilidade deve ser isolada do restante do trabalho.</span><span class="sxs-lookup"><span data-stu-id="5b05a-109">The accounting sheet should to be isolated from the remainder of the job.</span></span> <span data-ttu-id="5b05a-110">Isso significa que qualquer opção de acabamento ou de processamento (como JobDuplex, JobStaple ou JobBinding) não deve incluir a planilha de contabilidade.</span><span class="sxs-lookup"><span data-stu-id="5b05a-110">This means that any finishing or processing options (such as JobDuplex, JobStaple, or JobBinding) should not include the accounting sheet.</span></span> <span data-ttu-id="5b05a-111">A folha contábil pode ocorrer como a primeira ou última página do trabalho na critério do implementador.</span><span class="sxs-lookup"><span data-stu-id="5b05a-111">The accounting sheet may occur as the first or last page of the job at the implementer's discretion.</span></span>

-   [<span data-ttu-id="5b05a-112">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="5b05a-112">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="5b05a-113">Conteúdo estrutural</span><span class="sxs-lookup"><span data-stu-id="5b05a-113">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="5b05a-114">Conteúdo de linguagem XML (XML)</span><span class="sxs-lookup"><span data-stu-id="5b05a-114">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="5b05a-115">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="5b05a-115">Element Information</span></span>



| <span data-ttu-id="5b05a-116">Nome</span><span class="sxs-lookup"><span data-stu-id="5b05a-116">Name</span></span> | <span data-ttu-id="5b05a-117">Valor</span><span class="sxs-lookup"><span data-stu-id="5b05a-117">Value</span></span> |
|----------------------------|--------------------|
| <span data-ttu-id="5b05a-118">Tipo de elemento</span><span class="sxs-lookup"><span data-stu-id="5b05a-118">Element Type</span></span> <br/>   | <span data-ttu-id="5b05a-119">Recurso</span><span class="sxs-lookup"><span data-stu-id="5b05a-119">Feature</span></span><br/> |
| <span data-ttu-id="5b05a-120">Prefixo de escopo</span><span class="sxs-lookup"><span data-stu-id="5b05a-120">Scoping Prefix</span></span> <br/> | <span data-ttu-id="5b05a-121">Trabalho</span><span class="sxs-lookup"><span data-stu-id="5b05a-121">Job</span></span><br/>     |
| <span data-ttu-id="5b05a-122">Observações</span><span class="sxs-lookup"><span data-stu-id="5b05a-122">Notes</span></span> <br/>          | <span data-ttu-id="5b05a-123">Nenhum</span><span class="sxs-lookup"><span data-stu-id="5b05a-123">None</span></span><br/>    |



 

## <a name="structural-content"></a><span data-ttu-id="5b05a-124">Conteúdo estrutural</span><span class="sxs-lookup"><span data-stu-id="5b05a-124">Structural Content</span></span>

<span data-ttu-id="5b05a-125">A estrutura XML desse elemento é:</span><span class="sxs-lookup"><span data-stu-id="5b05a-125">The XML structure of this element is:</span></span>

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

## <a name="structure-variables"></a><span data-ttu-id="5b05a-126">Variáveis de estrutura</span><span class="sxs-lookup"><span data-stu-id="5b05a-126">Structure Variables</span></span>

<span data-ttu-id="5b05a-127">A tabela a seguir descreve as características das variáveis definidas na estrutura XML.</span><span class="sxs-lookup"><span data-stu-id="5b05a-127">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="5b05a-128">Nome</span><span class="sxs-lookup"><span data-stu-id="5b05a-128">Name</span></span>                               | <span data-ttu-id="5b05a-129">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="5b05a-129">Data type</span></span>         | <span data-ttu-id="5b05a-130">Unidade</span><span class="sxs-lookup"><span data-stu-id="5b05a-130">Unit</span></span>                  | <span data-ttu-id="5b05a-131">Valores com suporte</span><span class="sxs-lookup"><span data-stu-id="5b05a-131">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="5b05a-132">Resumo</span><span class="sxs-lookup"><span data-stu-id="5b05a-132">Summary</span></span>                                                                      |
|------------------------------------|-------------------|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="5b05a-133">\_OptionName\_</span><span class="sxs-lookup"><span data-stu-id="5b05a-133">\_OptionName\_</span></span><br/>          | <span data-ttu-id="5b05a-134">string</span><span class="sxs-lookup"><span data-stu-id="5b05a-134">string</span></span><br/> | <span data-ttu-id="5b05a-135">characters</span><span class="sxs-lookup"><span data-stu-id="5b05a-135">characters</span></span><br/> | <span data-ttu-id="5b05a-136">Nome totalmente qualificado válido, conforme definido pelos [namespaces em XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span><span class="sxs-lookup"><span data-stu-id="5b05a-136">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="5b05a-137">Se nenhum namespace for especificado, o namespace padrão será assumido.</span><span class="sxs-lookup"><span data-stu-id="5b05a-137">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="5b05a-138">O nome da opção.</span><span class="sxs-lookup"><span data-stu-id="5b05a-138">The name of the option.</span></span><br/>                                           |
| <span data-ttu-id="5b05a-139">\_IdentityOptionValue\_</span><span class="sxs-lookup"><span data-stu-id="5b05a-139">\_IdentityOptionValue\_</span></span><br/> | <span data-ttu-id="5b05a-140">string</span><span class="sxs-lookup"><span data-stu-id="5b05a-140">string</span></span><br/> | <span data-ttu-id="5b05a-141">N/D</span><span class="sxs-lookup"><span data-stu-id="5b05a-141">n/a</span></span><br/>        | <span data-ttu-id="5b05a-142">True, False.</span><span class="sxs-lookup"><span data-stu-id="5b05a-142">True, False.</span></span><br/>                                                                                                                                                               | <span data-ttu-id="5b05a-143">Define uma opção que, quando selecionada, desabilita esse recurso.</span><span class="sxs-lookup"><span data-stu-id="5b05a-143">Defines an Option which when selected would disable this feature.</span></span><br/> |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="5b05a-144">Conteúdo de linguagem XML (XML)</span><span class="sxs-lookup"><span data-stu-id="5b05a-144">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="5b05a-145">As palavras-chave do esquema de impressão pública são definidas no https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span><span class="sxs-lookup"><span data-stu-id="5b05a-145">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="5b05a-146">O conteúdo do linguagem XML público (XML) para essa palavra-chave é definido abaixo:</span><span class="sxs-lookup"><span data-stu-id="5b05a-146">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

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

## <a name="related-topics"></a><span data-ttu-id="5b05a-147">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="5b05a-147">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5b05a-148">Especificação de esquema de impressão</span><span class="sxs-lookup"><span data-stu-id="5b05a-148">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




