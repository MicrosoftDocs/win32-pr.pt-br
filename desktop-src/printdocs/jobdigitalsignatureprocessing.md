---
description: Saiba mais sobre o elemento JobDigitalSignatureProcessing, que descreve a configuração do processamento de assinatura digital para todo o trabalho.
ms.assetid: 0592f7a4-cace-41b0-91e3-2811f72aeb3e
title: JobDigitalSignatureProcessing
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f9491a921d9d733dd0de0a4e5133d5c6690b2b4a
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/19/2021
ms.locfileid: "112408939"
---
# <a name="jobdigitalsignatureprocessing"></a><span data-ttu-id="78aee-103">JobDigitalSignatureProcessing</span><span class="sxs-lookup"><span data-stu-id="78aee-103">JobDigitalSignatureProcessing</span></span>

<span data-ttu-id="78aee-104">Este tópico não é atual.</span><span class="sxs-lookup"><span data-stu-id="78aee-104">This topic is not current.</span></span> <span data-ttu-id="78aee-105">Para obter as informações mais atuais, consulte a [especificação do esquema de impressão](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="78aee-105">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="78aee-106">Descreve a configuração do processamento de assinatura digital para todo o trabalho.</span><span class="sxs-lookup"><span data-stu-id="78aee-106">Describes configuring the digital signature processing for the entire job.</span></span> <span data-ttu-id="78aee-107">Aplicável somente ao conteúdo que contém assinaturas digitais.</span><span class="sxs-lookup"><span data-stu-id="78aee-107">Applicable only to content that contains digital signatures.</span></span>

-   [<span data-ttu-id="78aee-108">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="78aee-108">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="78aee-109">Conteúdo estrutural</span><span class="sxs-lookup"><span data-stu-id="78aee-109">Structural Content</span></span>](#structural-content)

## <a name="element-information"></a><span data-ttu-id="78aee-110">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="78aee-110">Element Information</span></span>



| <span data-ttu-id="78aee-111">Name</span><span class="sxs-lookup"><span data-stu-id="78aee-111">Name</span></span> | <span data-ttu-id="78aee-112">Valor</span><span class="sxs-lookup"><span data-stu-id="78aee-112">Value</span></span> |
|----------------------------|--------------------|
| <span data-ttu-id="78aee-113">Tipo de elemento</span><span class="sxs-lookup"><span data-stu-id="78aee-113">Element Type</span></span> <br/>   | <span data-ttu-id="78aee-114">Recurso</span><span class="sxs-lookup"><span data-stu-id="78aee-114">Feature</span></span><br/> |
| <span data-ttu-id="78aee-115">Prefixo de escopo</span><span class="sxs-lookup"><span data-stu-id="78aee-115">Scoping Prefix</span></span> <br/> | <span data-ttu-id="78aee-116">Trabalho</span><span class="sxs-lookup"><span data-stu-id="78aee-116">Job</span></span><br/>     |
| <span data-ttu-id="78aee-117">Observações</span><span class="sxs-lookup"><span data-stu-id="78aee-117">Notes</span></span> <br/>          | <span data-ttu-id="78aee-118">Nenhum</span><span class="sxs-lookup"><span data-stu-id="78aee-118">None</span></span><br/>    |



 

## <a name="structural-content"></a><span data-ttu-id="78aee-119">Conteúdo estrutural</span><span class="sxs-lookup"><span data-stu-id="78aee-119">Structural Content</span></span>

<span data-ttu-id="78aee-120">A estrutura XML desse elemento é:</span><span class="sxs-lookup"><span data-stu-id="78aee-120">The XML structure of this element is:</span></span>

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

## <a name="structure-variables"></a><span data-ttu-id="78aee-121">Variáveis de estrutura</span><span class="sxs-lookup"><span data-stu-id="78aee-121">Structure Variables</span></span>

<span data-ttu-id="78aee-122">A tabela a seguir descreve as características das variáveis definidas na estrutura XML.</span><span class="sxs-lookup"><span data-stu-id="78aee-122">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="78aee-123">Nome</span><span class="sxs-lookup"><span data-stu-id="78aee-123">Name</span></span>                               | <span data-ttu-id="78aee-124">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="78aee-124">Data type</span></span>         | <span data-ttu-id="78aee-125">Unidade</span><span class="sxs-lookup"><span data-stu-id="78aee-125">Unit</span></span>                   | <span data-ttu-id="78aee-126">Valores com suporte</span><span class="sxs-lookup"><span data-stu-id="78aee-126">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="78aee-127">Resumo</span><span class="sxs-lookup"><span data-stu-id="78aee-127">Summary</span></span>                                                                      |
|------------------------------------|-------------------|------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="78aee-128">\_OptionName\_</span><span class="sxs-lookup"><span data-stu-id="78aee-128">\_OptionName\_</span></span><br/>          | <span data-ttu-id="78aee-129">string</span><span class="sxs-lookup"><span data-stu-id="78aee-129">string</span></span><br/> | <span data-ttu-id="78aee-130">characters</span><span class="sxs-lookup"><span data-stu-id="78aee-130">characters</span></span> <br/> | <span data-ttu-id="78aee-131">Nome totalmente qualificado válido, conforme definido pelos [namespaces em XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span><span class="sxs-lookup"><span data-stu-id="78aee-131">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="78aee-132">Se nenhum namespace for especificado, o namespace padrão será assumido.</span><span class="sxs-lookup"><span data-stu-id="78aee-132">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="78aee-133">O nome da opção</span><span class="sxs-lookup"><span data-stu-id="78aee-133">The name of the option</span></span><br/>                                            |
| <span data-ttu-id="78aee-134">\_IdentityOptionValue\_</span><span class="sxs-lookup"><span data-stu-id="78aee-134">\_IdentityOptionValue\_</span></span><br/> | <span data-ttu-id="78aee-135">string</span><span class="sxs-lookup"><span data-stu-id="78aee-135">string</span></span><br/> | <span data-ttu-id="78aee-136">n/d</span><span class="sxs-lookup"><span data-stu-id="78aee-136">n/a</span></span><br/>         | <span data-ttu-id="78aee-137">Verdadeiro, Falso</span><span class="sxs-lookup"><span data-stu-id="78aee-137">True, False</span></span><br/>                                                                                                                                                                | <span data-ttu-id="78aee-138">Define uma opção que, quando selecionada, desabilita esse recurso.</span><span class="sxs-lookup"><span data-stu-id="78aee-138">Defines an Option which when selected would disable this feature.</span></span><br/> |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="78aee-139">Conteúdo de linguagem XML (XML)</span><span class="sxs-lookup"><span data-stu-id="78aee-139">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="78aee-140">As palavras-chave do esquema de impressão pública são definidas no https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span><span class="sxs-lookup"><span data-stu-id="78aee-140">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="78aee-141">O conteúdo do linguagem XML público (XML) para essa palavra-chave é definido abaixo:</span><span class="sxs-lookup"><span data-stu-id="78aee-141">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

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

## <a name="related-topics"></a><span data-ttu-id="78aee-142">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="78aee-142">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="78aee-143">Especificação de esquema de impressão</span><span class="sxs-lookup"><span data-stu-id="78aee-143">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




