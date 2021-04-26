---
description: Este tópico não é atual. Para obter as informações mais atuais, consulte a especificação do esquema de impressão.
ms.assetid: 0592f7a4-cace-41b0-91e3-2811f72aeb3e
title: JobDigitalSignatureProcessing
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aad9dbe0ba82d219a28602178efa2e102ccf167b
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/26/2021
ms.locfileid: "107998283"
---
# <a name="jobdigitalsignatureprocessing"></a><span data-ttu-id="93be5-104">JobDigitalSignatureProcessing</span><span class="sxs-lookup"><span data-stu-id="93be5-104">JobDigitalSignatureProcessing</span></span>

<span data-ttu-id="93be5-105">Este tópico não é atual.</span><span class="sxs-lookup"><span data-stu-id="93be5-105">This topic is not current.</span></span> <span data-ttu-id="93be5-106">Para obter as informações mais atuais, consulte a [especificação do esquema de impressão](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="93be5-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="93be5-107">Descreve a configuração do processamento de assinatura digital para todo o trabalho.</span><span class="sxs-lookup"><span data-stu-id="93be5-107">Describes configuring the digital signature processing for the entire job.</span></span> <span data-ttu-id="93be5-108">Aplicável somente ao conteúdo que contém assinaturas digitais.</span><span class="sxs-lookup"><span data-stu-id="93be5-108">Applicable only to content that contains digital signatures.</span></span>

-   [<span data-ttu-id="93be5-109">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="93be5-109">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="93be5-110">Conteúdo estrutural</span><span class="sxs-lookup"><span data-stu-id="93be5-110">Structural Content</span></span>](#structural-content)

## <a name="element-information"></a><span data-ttu-id="93be5-111">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="93be5-111">Element Information</span></span>



| <span data-ttu-id="93be5-112">Nome</span><span class="sxs-lookup"><span data-stu-id="93be5-112">Name</span></span> | <span data-ttu-id="93be5-113">Valor</span><span class="sxs-lookup"><span data-stu-id="93be5-113">Value</span></span> |
|----------------------------|--------------------|
| <span data-ttu-id="93be5-114">Tipo de elemento</span><span class="sxs-lookup"><span data-stu-id="93be5-114">Element Type</span></span> <br/>   | <span data-ttu-id="93be5-115">Recurso</span><span class="sxs-lookup"><span data-stu-id="93be5-115">Feature</span></span><br/> |
| <span data-ttu-id="93be5-116">Prefixo de escopo</span><span class="sxs-lookup"><span data-stu-id="93be5-116">Scoping Prefix</span></span> <br/> | <span data-ttu-id="93be5-117">Trabalho</span><span class="sxs-lookup"><span data-stu-id="93be5-117">Job</span></span><br/>     |
| <span data-ttu-id="93be5-118">Observações</span><span class="sxs-lookup"><span data-stu-id="93be5-118">Notes</span></span> <br/>          | <span data-ttu-id="93be5-119">Nenhum</span><span class="sxs-lookup"><span data-stu-id="93be5-119">None</span></span><br/>    |



 

## <a name="structural-content"></a><span data-ttu-id="93be5-120">Conteúdo estrutural</span><span class="sxs-lookup"><span data-stu-id="93be5-120">Structural Content</span></span>

<span data-ttu-id="93be5-121">A estrutura XML desse elemento é:</span><span class="sxs-lookup"><span data-stu-id="93be5-121">The XML structure of this element is:</span></span>

``` syntax
<psf:Feature name="psk:JobDigitalSignatureProcessing">
  <psf:Property name="SelectionType">
    <psf:Value xsi:type="xs:string">PickOne</psf:Value>
  </psf:Property>
  <psf:Option name="psk:_OptionName_">
    <psf:Property name="psf:IdentityOption">
      <psf:Value xsi:type="xs:string">_IdentityOptionValue_</psf:Value>
    </psf:Property>
  </psf:Feature>
```

## <a name="structure-variables"></a><span data-ttu-id="93be5-122">Variáveis de estrutura</span><span class="sxs-lookup"><span data-stu-id="93be5-122">Structure Variables</span></span>

<span data-ttu-id="93be5-123">A tabela a seguir descreve as características das variáveis definidas na estrutura XML.</span><span class="sxs-lookup"><span data-stu-id="93be5-123">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="93be5-124">Nome</span><span class="sxs-lookup"><span data-stu-id="93be5-124">Name</span></span>                               | <span data-ttu-id="93be5-125">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="93be5-125">Data type</span></span>         | <span data-ttu-id="93be5-126">Unidade</span><span class="sxs-lookup"><span data-stu-id="93be5-126">Unit</span></span>                   | <span data-ttu-id="93be5-127">Valores com suporte</span><span class="sxs-lookup"><span data-stu-id="93be5-127">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="93be5-128">Resumo</span><span class="sxs-lookup"><span data-stu-id="93be5-128">Summary</span></span>                                                                      |
|------------------------------------|-------------------|------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="93be5-129">\_OptionName\_</span><span class="sxs-lookup"><span data-stu-id="93be5-129">\_OptionName\_</span></span><br/>          | <span data-ttu-id="93be5-130">string</span><span class="sxs-lookup"><span data-stu-id="93be5-130">string</span></span><br/> | <span data-ttu-id="93be5-131">characters</span><span class="sxs-lookup"><span data-stu-id="93be5-131">characters</span></span> <br/> | <span data-ttu-id="93be5-132">Nome totalmente qualificado válido, conforme definido pelos [namespaces em XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span><span class="sxs-lookup"><span data-stu-id="93be5-132">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="93be5-133">Se nenhum namespace for especificado, o namespace padrão será assumido.</span><span class="sxs-lookup"><span data-stu-id="93be5-133">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="93be5-134">O nome da opção</span><span class="sxs-lookup"><span data-stu-id="93be5-134">The name of the option</span></span><br/>                                            |
| <span data-ttu-id="93be5-135">\_IdentityOptionValue\_</span><span class="sxs-lookup"><span data-stu-id="93be5-135">\_IdentityOptionValue\_</span></span><br/> | <span data-ttu-id="93be5-136">string</span><span class="sxs-lookup"><span data-stu-id="93be5-136">string</span></span><br/> | <span data-ttu-id="93be5-137">N/D</span><span class="sxs-lookup"><span data-stu-id="93be5-137">n/a</span></span><br/>         | <span data-ttu-id="93be5-138">Verdadeiro, Falso</span><span class="sxs-lookup"><span data-stu-id="93be5-138">True, False</span></span><br/>                                                                                                                                                                | <span data-ttu-id="93be5-139">Define uma opção que, quando selecionada, desabilita esse recurso.</span><span class="sxs-lookup"><span data-stu-id="93be5-139">Defines an Option which when selected would disable this feature.</span></span><br/> |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="93be5-140">Conteúdo de linguagem XML (XML)</span><span class="sxs-lookup"><span data-stu-id="93be5-140">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="93be5-141">As palavras-chave do esquema de impressão pública são definidas no https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span><span class="sxs-lookup"><span data-stu-id="93be5-141">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="93be5-142">O conteúdo do linguagem XML público (XML) para essa palavra-chave é definido abaixo:</span><span class="sxs-lookup"><span data-stu-id="93be5-142">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

``` syntax
<psf:Feature name="psk:JobDigitalSignatureProcessing">
  <psf:Property name="SelectionType">
    <psf:Value xsi:type="xs:string">PickOne</psf:Value>
  </psf:Property>
  <!-- Print the job regardless of the validity of the digital signatures. Digital signatures MAY be ignored.  -->
  <psf:Option name="psk:PrintInvalidSignatures" />
  <!-- Print the job regardless of the validity of the digital signatures.  In the event an invalid signature is encountered, an error page should print at the end of the job.  Digital signatures MUST not be ignored. -->
  <psf:Option name="psk:PrintInvalidSignaturesWithErrorReport" />
  <!-- Print the job only if all digital signatures are valid.  Digital signatures MUST not be ignored. -->
  <psf:Option name="psk:PrintOnlyValidSignatures" />
</psf:Feature>
```

## <a name="related-topics"></a><span data-ttu-id="93be5-143">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="93be5-143">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="93be5-144">Especificação de esquema de impressão</span><span class="sxs-lookup"><span data-stu-id="93be5-144">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




