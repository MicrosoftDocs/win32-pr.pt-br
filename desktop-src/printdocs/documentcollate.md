---
description: Este tópico não é atual. Para obter as informações mais atuais, consulte a especificação do esquema de impressão.
ms.assetid: 752cccf7-1f95-4597-b0e2-a96fd22ffeef
title: DocumentCollate
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 959613299c53996ce7d66171d2da1518f28b9298
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/26/2021
ms.locfileid: "107993993"
---
# <a name="documentcollate"></a><span data-ttu-id="8e410-104">DocumentCollate</span><span class="sxs-lookup"><span data-stu-id="8e410-104">DocumentCollate</span></span>

<span data-ttu-id="8e410-105">Este tópico não é atual.</span><span class="sxs-lookup"><span data-stu-id="8e410-105">This topic is not current.</span></span> <span data-ttu-id="8e410-106">Para obter as informações mais atuais, consulte a [especificação do esquema de impressão](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="8e410-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="8e410-107">Descreve as características de agrupamento da saída.</span><span class="sxs-lookup"><span data-stu-id="8e410-107">Describes the collating characteristics of the output.</span></span> <span data-ttu-id="8e410-108">Todas as páginas em cada documento individual são agrupadas.</span><span class="sxs-lookup"><span data-stu-id="8e410-108">All pages in each individual document are collated.</span></span> <span data-ttu-id="8e410-109">DocumentCollate e JobCollateAlldocuments são mutuamente exclusivos.</span><span class="sxs-lookup"><span data-stu-id="8e410-109">DocumentCollate and JobCollateAlldocuments are mutually exclusive.</span></span> <span data-ttu-id="8e410-110">O comportamento e a implementação de se ambas ou apenas uma dessas palavras-chave são implementadas são deixados para o driver.</span><span class="sxs-lookup"><span data-stu-id="8e410-110">The behavior and implementation of whether both or only one of these keywords is implemented is left to the driver.</span></span>

<span data-ttu-id="8e410-111">A seguir estão as regras que devem ser seguidas para implementação de agrupamento</span><span class="sxs-lookup"><span data-stu-id="8e410-111">The following are the rules which should be followed for Collate implementation</span></span>

## <a name="element-definition-and-rules"></a><span data-ttu-id="8e410-112">Definição de elemento e regras</span><span class="sxs-lookup"><span data-stu-id="8e410-112">Element Definition and Rules</span></span>

<span data-ttu-id="8e410-113">Você deve primeiro seguir as regras para JobCollateAllDocument e, em seguida, aplicar regras para DocumentCollate para que os cenários funcionem.</span><span class="sxs-lookup"><span data-stu-id="8e410-113">You must first follow the rules for JobCollateAllDocument, and then apply rules for DocumentCollate for the scenarios to work.</span></span> <span data-ttu-id="8e410-114">Observe que, em uma configuração de conversão de PrintTicket para DEVMODE, em que JobCollateAllDocuments não é suportado pelo driver, cabe ao driver escolher o comportamento apropriado a ser adotado (JobCollateAllDocuments = ON ou OFF).</span><span class="sxs-lookup"><span data-stu-id="8e410-114">Note that in a PrintTicket to Devmode conversion setting, where JobCollateAllDocuments is not supported by the driver, it is up to the driver to choose the appropriate behavior to take (JobCollateAllDocuments = ON or OFF).</span></span> <span data-ttu-id="8e410-115">Além disso, a escolha pode ser alterada dependendo de outras configurações do PrintTicket.</span><span class="sxs-lookup"><span data-stu-id="8e410-115">Also, the choice can be changed depending on other PrintTicket settings.</span></span>

### <a name="jobcollatealldocuments"></a><span data-ttu-id="8e410-116">JobCollateAllDocuments</span><span class="sxs-lookup"><span data-stu-id="8e410-116">JobCollateAllDocuments</span></span>

<span data-ttu-id="8e410-117">EM: imprimir (DocumentCopiesAllPages) cópias de cada documento, repetir JobCopiesAllDocuments vezes.</span><span class="sxs-lookup"><span data-stu-id="8e410-117">ON: Print (DocumentCopiesAllPages) copies of each document, repeat JobCopiesAllDocuments times.</span></span>

<span data-ttu-id="8e410-118">OFF: para cada documento, Print (JobCopiesAllDocuments x DocumentCopiesAllPages) copia juntos.</span><span class="sxs-lookup"><span data-stu-id="8e410-118">OFF: For each document, print (JobCopiesAllDocuments x DocumentCopiesAllPages) copies together.</span></span>

### <a name="documentcollate"></a><span data-ttu-id="8e410-119">DocumentCollate</span><span class="sxs-lookup"><span data-stu-id="8e410-119">DocumentCollate</span></span>

<span data-ttu-id="8e410-120">EM: para todas as cópias (JobCopiesAllDocuments x DocumentCopiesAllPages) de um documento impresso de forma contígua, você agrupa as planilhas nesse documento.</span><span class="sxs-lookup"><span data-stu-id="8e410-120">ON: For all copies (JobCopiesAllDocuments x DocumentCopiesAllPages) of a document printed contiguously, collate sheets in that document.</span></span>

<span data-ttu-id="8e410-121">DESATIVADO: para todas as cópias (JobCopiesAllDocuments x DocumentCopiesAllPages) são impressas de forma contígua, imprima todas as cópias (JobCopiesAllDocuments x DocumentCopiesAllPages) de cada folha juntas.</span><span class="sxs-lookup"><span data-stu-id="8e410-121">OFF: For all copies (JobCopiesAllDocuments x DocumentCopiesAllPages) printed contiguously, print all copies (JobCopiesAllDocuments x DocumentCopiesAllPages) of each sheet together.</span></span>

-   [<span data-ttu-id="8e410-122">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="8e410-122">Element Information</span></span>](#element-information)

-   [<span data-ttu-id="8e410-123">Conteúdo estrutural</span><span class="sxs-lookup"><span data-stu-id="8e410-123">Structural Content</span></span>](#structural-content)

-   [<span data-ttu-id="8e410-124">Conteúdo XML</span><span class="sxs-lookup"><span data-stu-id="8e410-124">XML Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="8e410-125">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="8e410-125">Element Information</span></span>



| <span data-ttu-id="8e410-126">Nome</span><span class="sxs-lookup"><span data-stu-id="8e410-126">Name</span></span> | <span data-ttu-id="8e410-127">Valor</span><span class="sxs-lookup"><span data-stu-id="8e410-127">Value</span></span> |
|----------------------------|---------------------|
| <span data-ttu-id="8e410-128">Tipo de elemento</span><span class="sxs-lookup"><span data-stu-id="8e410-128">Element Type</span></span> <br/>   | <span data-ttu-id="8e410-129">Recurso</span><span class="sxs-lookup"><span data-stu-id="8e410-129">Feature</span></span><br/>  |
| <span data-ttu-id="8e410-130">Prefixo de escopo</span><span class="sxs-lookup"><span data-stu-id="8e410-130">Scoping Prefix</span></span> <br/> | <span data-ttu-id="8e410-131">Documento</span><span class="sxs-lookup"><span data-stu-id="8e410-131">Document</span></span><br/> |
| <span data-ttu-id="8e410-132">Observações</span><span class="sxs-lookup"><span data-stu-id="8e410-132">Notes</span></span> <br/>          | <span data-ttu-id="8e410-133">Nenhum</span><span class="sxs-lookup"><span data-stu-id="8e410-133">None</span></span><br/>     |



 

## <a name="structural-content"></a><span data-ttu-id="8e410-134">Conteúdo estrutural</span><span class="sxs-lookup"><span data-stu-id="8e410-134">Structural Content</span></span>

<span data-ttu-id="8e410-135">A estrutura XML desse elemento é:</span><span class="sxs-lookup"><span data-stu-id="8e410-135">The XML structure of this element is:</span></span>

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

## <a name="structure-variables"></a><span data-ttu-id="8e410-136">Variáveis de estrutura</span><span class="sxs-lookup"><span data-stu-id="8e410-136">Structure Variables</span></span>

<span data-ttu-id="8e410-137">A tabela a seguir descreve as características das variáveis definidas na estrutura XML.</span><span class="sxs-lookup"><span data-stu-id="8e410-137">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="8e410-138">Nome</span><span class="sxs-lookup"><span data-stu-id="8e410-138">Name</span></span>                               | <span data-ttu-id="8e410-139">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="8e410-139">Data type</span></span>         | <span data-ttu-id="8e410-140">Unidade</span><span class="sxs-lookup"><span data-stu-id="8e410-140">Unit</span></span>                  | <span data-ttu-id="8e410-141">Valores com suporte</span><span class="sxs-lookup"><span data-stu-id="8e410-141">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="8e410-142">Resumo</span><span class="sxs-lookup"><span data-stu-id="8e410-142">Summary</span></span>                                                                      |
|------------------------------------|-------------------|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="8e410-143">\_OptionName\_</span><span class="sxs-lookup"><span data-stu-id="8e410-143">\_OptionName\_</span></span><br/>          | <span data-ttu-id="8e410-144">string</span><span class="sxs-lookup"><span data-stu-id="8e410-144">string</span></span><br/> | <span data-ttu-id="8e410-145">characters</span><span class="sxs-lookup"><span data-stu-id="8e410-145">characters</span></span><br/> | <span data-ttu-id="8e410-146">Nome totalmente qualificado válido, conforme definido pelos [namespaces em XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span><span class="sxs-lookup"><span data-stu-id="8e410-146">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="8e410-147">Se nenhum namespace for especificado, o namespace padrão será assumido.</span><span class="sxs-lookup"><span data-stu-id="8e410-147">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="8e410-148">O nome da opção.</span><span class="sxs-lookup"><span data-stu-id="8e410-148">The name of the option.</span></span><br/>                                           |
| <span data-ttu-id="8e410-149">\_IdentityOptionValue\_</span><span class="sxs-lookup"><span data-stu-id="8e410-149">\_IdentityOptionValue\_</span></span><br/> | <span data-ttu-id="8e410-150">string</span><span class="sxs-lookup"><span data-stu-id="8e410-150">string</span></span><br/> | <span data-ttu-id="8e410-151">N/D</span><span class="sxs-lookup"><span data-stu-id="8e410-151">n/a</span></span><br/>        | <span data-ttu-id="8e410-152">True, False.</span><span class="sxs-lookup"><span data-stu-id="8e410-152">True, False.</span></span><br/>                                                                                                                                                               | <span data-ttu-id="8e410-153">Define uma opção que, quando selecionada, desabilita esse recurso.</span><span class="sxs-lookup"><span data-stu-id="8e410-153">Defines an Option which when selected would disable this feature.</span></span><br/> |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="8e410-154">Conteúdo de linguagem XML (XML)</span><span class="sxs-lookup"><span data-stu-id="8e410-154">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="8e410-155">As palavras-chave do esquema de impressão pública são definidas no https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span><span class="sxs-lookup"><span data-stu-id="8e410-155">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="8e410-156">O conteúdo do linguagem XML público (XML) para essa palavra-chave é definido abaixo:</span><span class="sxs-lookup"><span data-stu-id="8e410-156">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

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

## <a name="related-topics"></a><span data-ttu-id="8e410-157">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="8e410-157">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8e410-158">Especificação de esquema de impressão</span><span class="sxs-lookup"><span data-stu-id="8e410-158">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




