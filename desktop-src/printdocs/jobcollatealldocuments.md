---
description: Este tópico não é atual. Para obter as informações mais atuais, consulte a especificação do esquema de impressão.
ms.assetid: 64fcd03f-8e0a-498d-82ea-0c69be0a3886
title: JobCollateAllDocuments
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0406a5f9106cbe4cd2a8ccb0986a1bfacc95b916
ms.sourcegitcommit: 7b8f6151ebe247536304866459b2973276271d4d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/06/2021
ms.locfileid: "104298031"
---
# <a name="jobcollatealldocuments"></a><span data-ttu-id="850ce-104">JobCollateAllDocuments</span><span class="sxs-lookup"><span data-stu-id="850ce-104">JobCollateAllDocuments</span></span>

<span data-ttu-id="850ce-105">Este tópico não é atual.</span><span class="sxs-lookup"><span data-stu-id="850ce-105">This topic is not current.</span></span> <span data-ttu-id="850ce-106">Para obter as informações mais atuais, consulte a [especificação do esquema de impressão](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="850ce-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="850ce-107">Descreve as características de agrupamento da saída.</span><span class="sxs-lookup"><span data-stu-id="850ce-107">Describes the collating characteristics of the output.</span></span> <span data-ttu-id="850ce-108">Todos os documentos em cada trabalho individual são agrupados.</span><span class="sxs-lookup"><span data-stu-id="850ce-108">All documents in each individual job are collated.</span></span> <span data-ttu-id="850ce-109">DocumentCollate e JobCollateAlldocuments são mutuamente exclusivos.</span><span class="sxs-lookup"><span data-stu-id="850ce-109">DocumentCollate and JobCollateAlldocuments are mutually exclusive.</span></span> <span data-ttu-id="850ce-110">O comportamento e a implementação de se ambas ou apenas uma dessas palavras-chave são implementadas são deixados para o driver.</span><span class="sxs-lookup"><span data-stu-id="850ce-110">The behavior and implementation of whether both or only one of these keywords is implemented is left to the driver.</span></span>

<span data-ttu-id="850ce-111">A seguir estão as regras que devem ser seguidas para implementação de agrupamento.</span><span class="sxs-lookup"><span data-stu-id="850ce-111">The following are the rules that should be followed for Collate implementation.</span></span>

## <a name="element-definition-and-rules"></a><span data-ttu-id="850ce-112">Definição de elemento e regras</span><span class="sxs-lookup"><span data-stu-id="850ce-112">Element Definition and Rules</span></span>

<span data-ttu-id="850ce-113">Você deve primeiro seguir as regras para JobCollateAllDocument e, em seguida, aplicar regras para DocumentCollate para que os cenários funcionem.</span><span class="sxs-lookup"><span data-stu-id="850ce-113">You must first follow the rules for JobCollateAllDocument, and then apply rules for DocumentCollate for the scenarios to work.</span></span> <span data-ttu-id="850ce-114">Observe que, em uma configuração de conversão de PrintTicket para DEVMODE, em que JobCollateAllDocuments não é suportado pelo driver, cabe ao driver escolher o comportamento apropriado a ser adotado (JobCollateAllDocuments = ON ou OFF).</span><span class="sxs-lookup"><span data-stu-id="850ce-114">Note that in a PrintTicket to Devmode conversion setting, where JobCollateAllDocuments is not supported by the driver, it is up to the driver to choose the appropriate behavior to take (JobCollateAllDocuments = ON or OFF).</span></span> <span data-ttu-id="850ce-115">Além disso, a escolha pode ser alterada dependendo de outras configurações do PrintTicket.</span><span class="sxs-lookup"><span data-stu-id="850ce-115">Also, the choice can be changed depending on other PrintTicket settings.</span></span>

### <a name="jobcollatealldocuments"></a><span data-ttu-id="850ce-116">JobCollateAllDocuments</span><span class="sxs-lookup"><span data-stu-id="850ce-116">JobCollateAllDocuments</span></span>

<span data-ttu-id="850ce-117">EM: imprimir (DocumentCopiesAllPages) cópias de cada documento, repetir JobCopiesAllDocuments vezes.</span><span class="sxs-lookup"><span data-stu-id="850ce-117">ON: Print (DocumentCopiesAllPages) copies of each document, repeat JobCopiesAllDocuments times.</span></span>

<span data-ttu-id="850ce-118">OFF: para cada documento, Print (JobCopiesAllDocuments x DocumentCopiesAllPages) copia juntos.</span><span class="sxs-lookup"><span data-stu-id="850ce-118">OFF: For each document, print (JobCopiesAllDocuments x DocumentCopiesAllPages) copies together.</span></span>

### <a name="documentcollate"></a><span data-ttu-id="850ce-119">DocumentCollate</span><span class="sxs-lookup"><span data-stu-id="850ce-119">DocumentCollate</span></span>

<span data-ttu-id="850ce-120">EM: para todas as cópias (JobCopiesAllDocuments x DocumentCopiesAllPages) de um documento impresso de forma contígua, você agrupa as planilhas nesse documento.</span><span class="sxs-lookup"><span data-stu-id="850ce-120">ON: For all copies (JobCopiesAllDocuments x DocumentCopiesAllPages) of a document printed contiguously, collate sheets in that document.</span></span>

<span data-ttu-id="850ce-121">DESATIVADO: para todas as cópias (JobCopiesAllDocuments x DocumentCopiesAllPages) são impressas de forma contígua, imprima todas as cópias (JobCopiesAllDocuments x DocumentCopiesAllPages) de cada folha juntas.</span><span class="sxs-lookup"><span data-stu-id="850ce-121">OFF: For all copies (JobCopiesAllDocuments x DocumentCopiesAllPages) printed contiguously, print all copies (JobCopiesAllDocuments x DocumentCopiesAllPages) of each sheet together.</span></span>

-   [<span data-ttu-id="850ce-122">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="850ce-122">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="850ce-123">Conteúdo estrutural</span><span class="sxs-lookup"><span data-stu-id="850ce-123">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="850ce-124">Conteúdo de linguagem XML (XML)</span><span class="sxs-lookup"><span data-stu-id="850ce-124">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

### <a name="element-information"></a><span data-ttu-id="850ce-125">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="850ce-125">Element Information</span></span>



| <span data-ttu-id="850ce-126">Nome</span><span class="sxs-lookup"><span data-stu-id="850ce-126">Name</span></span>                       |                    |
|----------------------------|--------------------|
| <span data-ttu-id="850ce-127">Tipo de elemento</span><span class="sxs-lookup"><span data-stu-id="850ce-127">Element Type</span></span> <br/>   | <span data-ttu-id="850ce-128">Recurso</span><span class="sxs-lookup"><span data-stu-id="850ce-128">Feature</span></span><br/> |
| <span data-ttu-id="850ce-129">Prefixo de escopo</span><span class="sxs-lookup"><span data-stu-id="850ce-129">Scoping Prefix</span></span> <br/> | <span data-ttu-id="850ce-130">Trabalho</span><span class="sxs-lookup"><span data-stu-id="850ce-130">Job</span></span><br/>     |
| <span data-ttu-id="850ce-131">Observações</span><span class="sxs-lookup"><span data-stu-id="850ce-131">Notes</span></span> <br/>          | <span data-ttu-id="850ce-132">Nenhum</span><span class="sxs-lookup"><span data-stu-id="850ce-132">None</span></span><br/>    |



 

### <a name="structural-content"></a><span data-ttu-id="850ce-133">Conteúdo estrutural</span><span class="sxs-lookup"><span data-stu-id="850ce-133">Structural Content</span></span>

<span data-ttu-id="850ce-134">A estrutura XML desse elemento é:</span><span class="sxs-lookup"><span data-stu-id="850ce-134">The XML structure of this element is:</span></span>

``` syntax
<psf:Feature name="psk:JobCollateAllDocuments">
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

### <a name="structure-variables"></a><span data-ttu-id="850ce-135">Variáveis de estrutura</span><span class="sxs-lookup"><span data-stu-id="850ce-135">Structure Variables</span></span>

<span data-ttu-id="850ce-136">A tabela a seguir descreve as características das variáveis definidas na estrutura XML.</span><span class="sxs-lookup"><span data-stu-id="850ce-136">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="850ce-137">Nome</span><span class="sxs-lookup"><span data-stu-id="850ce-137">Name</span></span>                               | <span data-ttu-id="850ce-138">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="850ce-138">Data type</span></span>         | <span data-ttu-id="850ce-139">Unidade</span><span class="sxs-lookup"><span data-stu-id="850ce-139">Unit</span></span>                  | <span data-ttu-id="850ce-140">Valores com suporte</span><span class="sxs-lookup"><span data-stu-id="850ce-140">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="850ce-141">Resumo</span><span class="sxs-lookup"><span data-stu-id="850ce-141">Summary</span></span>                                                                      |
|------------------------------------|-------------------|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="850ce-142">\_OptionName\_</span><span class="sxs-lookup"><span data-stu-id="850ce-142">\_OptionName\_</span></span><br/>          | <span data-ttu-id="850ce-143">string</span><span class="sxs-lookup"><span data-stu-id="850ce-143">string</span></span><br/> | <span data-ttu-id="850ce-144">characters</span><span class="sxs-lookup"><span data-stu-id="850ce-144">characters</span></span><br/> | <span data-ttu-id="850ce-145">Nome totalmente qualificado válido, conforme definido pelos [namespaces em XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span><span class="sxs-lookup"><span data-stu-id="850ce-145">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="850ce-146">Se nenhum namespace for especificado, o namespace padrão será assumido.</span><span class="sxs-lookup"><span data-stu-id="850ce-146">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="850ce-147">O nome da opção.</span><span class="sxs-lookup"><span data-stu-id="850ce-147">The name of the option.</span></span><br/>                                           |
| <span data-ttu-id="850ce-148">\_IdentityOptionValue\_</span><span class="sxs-lookup"><span data-stu-id="850ce-148">\_IdentityOptionValue\_</span></span><br/> | <span data-ttu-id="850ce-149">string</span><span class="sxs-lookup"><span data-stu-id="850ce-149">string</span></span><br/> | <span data-ttu-id="850ce-150">N/D</span><span class="sxs-lookup"><span data-stu-id="850ce-150">n/a</span></span><br/>        | <span data-ttu-id="850ce-151">True, False.</span><span class="sxs-lookup"><span data-stu-id="850ce-151">True, False.</span></span><br/>                                                                                                                                                               | <span data-ttu-id="850ce-152">Define uma opção que, quando selecionada, desabilita esse recurso.</span><span class="sxs-lookup"><span data-stu-id="850ce-152">Defines an Option which when selected would disable this feature.</span></span><br/> |



 

### <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="850ce-153">Conteúdo de linguagem XML (XML)</span><span class="sxs-lookup"><span data-stu-id="850ce-153">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="850ce-154">As palavras-chave do esquema de impressão pública são definidas no https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span><span class="sxs-lookup"><span data-stu-id="850ce-154">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="850ce-155">O conteúdo do linguagem XML público (XML) para essa palavra-chave é definido abaixo:</span><span class="sxs-lookup"><span data-stu-id="850ce-155">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

``` syntax
<psf:Feature name="psk:JobCollateAllDocuments">
  <psf:Property name="psf:SelectionType">
    <psf:Value xsi:type="xs:string">psk:PickOne</psf:Value>
  </psf:Property>
  <!-- Specifies collating.  -->
  <psf:Option name="psk:Collated" />
  <!-- Specifies no collating. -->
  <psf:Option name="psk:Uncollated" />
</psf:Feature>
```

 

 




