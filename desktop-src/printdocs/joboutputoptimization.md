---
description: Saiba mais sobre o JobOutputOptimization, que descreve o processamento do trabalho, destinado a otimizar a saída para cenários de uso específicos, conforme indicado pela opção especificada.
ms.assetid: 40925dfe-494c-49b5-ae57-de369723ba76
title: JobOutputOptimization
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cdbb65f86b5ed4fd30c056e234b88197d4ab475d
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/19/2021
ms.locfileid: "112408789"
---
# <a name="joboutputoptimization"></a><span data-ttu-id="f3b86-103">JobOutputOptimization</span><span class="sxs-lookup"><span data-stu-id="f3b86-103">JobOutputOptimization</span></span>

<span data-ttu-id="f3b86-104">Este tópico não é atual.</span><span class="sxs-lookup"><span data-stu-id="f3b86-104">This topic is not current.</span></span> <span data-ttu-id="f3b86-105">Para obter as informações mais atuais, consulte a [Especificação de Esquema de Impressão](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="f3b86-105">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="f3b86-106">Descreve o processamento do trabalho, destinado a otimizar a saída para cenários de uso específicos, conforme indicado pela opção especificada.</span><span class="sxs-lookup"><span data-stu-id="f3b86-106">Describes the job processing, intended to optimize the output for particular use scenarios as indicated by the option specified.</span></span>

-   [<span data-ttu-id="f3b86-107">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="f3b86-107">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="f3b86-108">Conteúdo estrutural</span><span class="sxs-lookup"><span data-stu-id="f3b86-108">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="f3b86-109">linguagem XML conteúdo (XML)</span><span class="sxs-lookup"><span data-stu-id="f3b86-109">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="f3b86-110">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="f3b86-110">Element Information</span></span>



| <span data-ttu-id="f3b86-111">Name</span><span class="sxs-lookup"><span data-stu-id="f3b86-111">Name</span></span> | <span data-ttu-id="f3b86-112">Valor</span><span class="sxs-lookup"><span data-stu-id="f3b86-112">Value</span></span> |
|----------------------------|--------------------|
| <span data-ttu-id="f3b86-113">Tipo de elemento</span><span class="sxs-lookup"><span data-stu-id="f3b86-113">Element Type</span></span> <br/>   | <span data-ttu-id="f3b86-114">Recurso</span><span class="sxs-lookup"><span data-stu-id="f3b86-114">Feature</span></span><br/> |
| <span data-ttu-id="f3b86-115">Prefixo de definição de scoping</span><span class="sxs-lookup"><span data-stu-id="f3b86-115">Scoping Prefix</span></span> <br/> | <span data-ttu-id="f3b86-116">Trabalho</span><span class="sxs-lookup"><span data-stu-id="f3b86-116">Job</span></span><br/>     |
| <span data-ttu-id="f3b86-117">Observações</span><span class="sxs-lookup"><span data-stu-id="f3b86-117">Notes</span></span> <br/>          | <span data-ttu-id="f3b86-118">Nenhum</span><span class="sxs-lookup"><span data-stu-id="f3b86-118">None</span></span><br/>    |



 

## <a name="structural-content"></a><span data-ttu-id="f3b86-119">Conteúdo estrutural</span><span class="sxs-lookup"><span data-stu-id="f3b86-119">Structural Content</span></span>

<span data-ttu-id="f3b86-120">A estrutura XML desse elemento é:</span><span class="sxs-lookup"><span data-stu-id="f3b86-120">The XML structure of this element is:</span></span>

``` syntax
<psf:Feature name="psk:JobOutputOptimization">
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

## <a name="structure-variables"></a><span data-ttu-id="f3b86-121">Variáveis de estrutura</span><span class="sxs-lookup"><span data-stu-id="f3b86-121">Structure Variables</span></span>

<span data-ttu-id="f3b86-122">A tabela a seguir descreve as características das variáveis definidas na estrutura XML.</span><span class="sxs-lookup"><span data-stu-id="f3b86-122">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="f3b86-123">Nome</span><span class="sxs-lookup"><span data-stu-id="f3b86-123">Name</span></span>                               | <span data-ttu-id="f3b86-124">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="f3b86-124">Data type</span></span>         | <span data-ttu-id="f3b86-125">Unidade</span><span class="sxs-lookup"><span data-stu-id="f3b86-125">Unit</span></span>                  | <span data-ttu-id="f3b86-126">Valores com suporte</span><span class="sxs-lookup"><span data-stu-id="f3b86-126">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="f3b86-127">Resumo</span><span class="sxs-lookup"><span data-stu-id="f3b86-127">Summary</span></span>                                                                      |
|------------------------------------|-------------------|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="f3b86-128">\_Optionname\_</span><span class="sxs-lookup"><span data-stu-id="f3b86-128">\_OptionName\_</span></span><br/>          | <span data-ttu-id="f3b86-129">string</span><span class="sxs-lookup"><span data-stu-id="f3b86-129">string</span></span><br/> | <span data-ttu-id="f3b86-130">characters</span><span class="sxs-lookup"><span data-stu-id="f3b86-130">characters</span></span><br/> | <span data-ttu-id="f3b86-131">Nome totalmente qualificado válido, conforme definido [por Namespaces em XML.](https://www.w3.org/TR/1999/REC-xml-names-19990114/)</span><span class="sxs-lookup"><span data-stu-id="f3b86-131">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="f3b86-132">Se nenhum namespace for especificado, o namespace padrão será assumido.</span><span class="sxs-lookup"><span data-stu-id="f3b86-132">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="f3b86-133">O nome da opção.</span><span class="sxs-lookup"><span data-stu-id="f3b86-133">The name of the option.</span></span><br/>                                           |
| <span data-ttu-id="f3b86-134">\_IdentityOptionValue\_</span><span class="sxs-lookup"><span data-stu-id="f3b86-134">\_IdentityOptionValue\_</span></span><br/> | <span data-ttu-id="f3b86-135">string</span><span class="sxs-lookup"><span data-stu-id="f3b86-135">string</span></span><br/> | <span data-ttu-id="f3b86-136">n/d</span><span class="sxs-lookup"><span data-stu-id="f3b86-136">n/a</span></span><br/>        | <span data-ttu-id="f3b86-137">True, False.</span><span class="sxs-lookup"><span data-stu-id="f3b86-137">True, False.</span></span><br/>                                                                                                                                                               | <span data-ttu-id="f3b86-138">Define uma Opção que, quando selecionada, desabilitará esse recurso.</span><span class="sxs-lookup"><span data-stu-id="f3b86-138">Defines an Option which when selected would disable this feature.</span></span><br/> |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="f3b86-139">linguagem XML conteúdo (XML)</span><span class="sxs-lookup"><span data-stu-id="f3b86-139">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="f3b86-140">As palavras-chave public Print Schema são definidas no https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace .</span><span class="sxs-lookup"><span data-stu-id="f3b86-140">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="f3b86-141">O conteúdo linguagem XML XML (public linguagem XML) para essa palavra-chave é definido abaixo:</span><span class="sxs-lookup"><span data-stu-id="f3b86-141">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

``` syntax
<psf:Feature name="psk:JobOutputOptimization">
  <psf:Property name="psf:SelectionType">
    <psf:Value xsi:type="xs:string">psk:PickOne</psf:Value>
  </psf:Property>
  <!-- Specifies the job processing be optimized for archive output. -->
  <psf:Option name="psk:ArchiveFormat" />
  <!-- Specifies the job processing be optimized for portability (cross-device) of output. -->
  <psf:Option name="psk:OptimizeForPortability" />
  <!-- Specifies the job processing be optimized for quality of output. -->
  <psf:Option name="psk:OptimizeForQuality" />
  <!-- Specifies the job processing be optimized for speed of output. -->
  <psf:Option name="psk:OptimizeForSpeed" />
  <!-- Specifies the job processing should not be optimized for a particular scenario. -->
  <psf:Option name="psk:None" />
</psf:Feature>
    
```

## <a name="related-topics"></a><span data-ttu-id="f3b86-142">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="f3b86-142">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f3b86-143">Especificação de esquema de impressão</span><span class="sxs-lookup"><span data-stu-id="f3b86-143">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




