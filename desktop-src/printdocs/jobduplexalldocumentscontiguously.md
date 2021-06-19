---
description: Saiba mais sobre o elemento JobDuplexAllDocumentsContiguously, que descreve as características duplex da saída.
ms.assetid: dd24166c-d5e2-420e-8a8c-e1a25728ab2f
title: JobDuplexAllDocumentsContiguously
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 20a8911a4c62644bfc073a2a9c1dcfd67dad536a
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/19/2021
ms.locfileid: "112408949"
---
# <a name="jobduplexalldocumentscontiguously"></a><span data-ttu-id="98e64-103">JobDuplexAllDocumentsContiguously</span><span class="sxs-lookup"><span data-stu-id="98e64-103">JobDuplexAllDocumentsContiguously</span></span>

<span data-ttu-id="98e64-104">Este tópico não é atual.</span><span class="sxs-lookup"><span data-stu-id="98e64-104">This topic is not current.</span></span> <span data-ttu-id="98e64-105">Para obter as informações mais atuais, consulte a [Especificação de Esquema de Impressão](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="98e64-105">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="98e64-106">Descreve as características duplex da saída.</span><span class="sxs-lookup"><span data-stu-id="98e64-106">Describes the duplex characteristics of the output.</span></span> <span data-ttu-id="98e64-107">O recurso duplex permite imprimir em ambos os lados da mídia.</span><span class="sxs-lookup"><span data-stu-id="98e64-107">The duplex feature allows for printing on both sides of the media.</span></span> <span data-ttu-id="98e64-108">Todos os documentos no trabalho são duplexados de forma contígua.</span><span class="sxs-lookup"><span data-stu-id="98e64-108">All Documents in the job are duplexed together contiguously.</span></span> <span data-ttu-id="98e64-109">JobDuplexAllDocumentsContiguously e DocumentDuplex são mutuamente exclusivos.</span><span class="sxs-lookup"><span data-stu-id="98e64-109">JobDuplexAllDocumentsContiguously and DocumentDuplex are mutually exclusive.</span></span> <span data-ttu-id="98e64-110">O driver deve determinar o tratamento de restrição entre essas palavras-chave.</span><span class="sxs-lookup"><span data-stu-id="98e64-110">It is up to the driver to determine constraint handling between these keywords.</span></span>

-   [<span data-ttu-id="98e64-111">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="98e64-111">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="98e64-112">Conteúdo estrutural</span><span class="sxs-lookup"><span data-stu-id="98e64-112">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="98e64-113">linguagem XML conteúdo (XML)</span><span class="sxs-lookup"><span data-stu-id="98e64-113">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="98e64-114">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="98e64-114">Element Information</span></span>



| <span data-ttu-id="98e64-115">Name</span><span class="sxs-lookup"><span data-stu-id="98e64-115">Name</span></span> | <span data-ttu-id="98e64-116">Valor</span><span class="sxs-lookup"><span data-stu-id="98e64-116">Value</span></span> |
|----------------------------|--------------------|
| <span data-ttu-id="98e64-117">Tipo de elemento</span><span class="sxs-lookup"><span data-stu-id="98e64-117">Element Type</span></span> <br/>   | <span data-ttu-id="98e64-118">Recurso</span><span class="sxs-lookup"><span data-stu-id="98e64-118">Feature</span></span><br/> |
| <span data-ttu-id="98e64-119">Prefixo de definição de scoping</span><span class="sxs-lookup"><span data-stu-id="98e64-119">Scoping Prefix</span></span> <br/> | <span data-ttu-id="98e64-120">Trabalho</span><span class="sxs-lookup"><span data-stu-id="98e64-120">Job</span></span><br/>     |
| <span data-ttu-id="98e64-121">Observações</span><span class="sxs-lookup"><span data-stu-id="98e64-121">Notes</span></span> <br/>          | <span data-ttu-id="98e64-122">Nenhum</span><span class="sxs-lookup"><span data-stu-id="98e64-122">None</span></span><br/>    |



 

## <a name="structural-content"></a><span data-ttu-id="98e64-123">Conteúdo estrutural</span><span class="sxs-lookup"><span data-stu-id="98e64-123">Structural Content</span></span>

<span data-ttu-id="98e64-124">A estrutura XML desse elemento é:</span><span class="sxs-lookup"><span data-stu-id="98e64-124">The XML structure of this element is:</span></span>

``` syntax
<psf:Feature name="psk:JobDuplexAllDocumentsContiguously">
  <psf:Property name="psf:SelectionType">
    <psf:Value xsi:type="xs:string">psk:PickOne</psf:Value>
  </psf:Property>
  <psf:Option name="psk:_OptionName_">
    <psf:Property name="psf:IdentityOption">
      <psf:Value xsi:type="xs:string">_IdentityOptionValue_</psf:Value>
    </psf:Property>
    <psf:ScoredProperty name="psk:DuplexMode">
      <psf:Value xsi:type="xs:string">_DuplexModeValue_</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
</psf:Feature>      
```

## <a name="structure-variables"></a><span data-ttu-id="98e64-125">Variáveis de estrutura</span><span class="sxs-lookup"><span data-stu-id="98e64-125">Structure Variables</span></span>

<span data-ttu-id="98e64-126">A tabela a seguir descreve as características das variáveis definidas na estrutura XML.</span><span class="sxs-lookup"><span data-stu-id="98e64-126">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="98e64-127">Nome</span><span class="sxs-lookup"><span data-stu-id="98e64-127">Name</span></span>                               | <span data-ttu-id="98e64-128">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="98e64-128">Data type</span></span>         | <span data-ttu-id="98e64-129">Unidade</span><span class="sxs-lookup"><span data-stu-id="98e64-129">Unit</span></span>                  | <span data-ttu-id="98e64-130">Valores com suporte</span><span class="sxs-lookup"><span data-stu-id="98e64-130">Supported values</span></span>                                                                                                                                                             | <span data-ttu-id="98e64-131">Resumo</span><span class="sxs-lookup"><span data-stu-id="98e64-131">Summary</span></span>                                                                                                                                |
|------------------------------------|-------------------|-----------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="98e64-132">\_Optionname\_</span><span class="sxs-lookup"><span data-stu-id="98e64-132">\_OptionName\_</span></span><br/>          | <span data-ttu-id="98e64-133">string</span><span class="sxs-lookup"><span data-stu-id="98e64-133">string</span></span><br/> | <span data-ttu-id="98e64-134">characters</span><span class="sxs-lookup"><span data-stu-id="98e64-134">characters</span></span><br/> | <span data-ttu-id="98e64-135">Nome totalmente qualificado válido, conforme definido por https://www.w3.org/TR/1999/REC-xml-names-19990114/\#dt-qname .</span><span class="sxs-lookup"><span data-stu-id="98e64-135">Valid fully qualified name as defined by https://www.w3.org/TR/1999/REC-xml-names-19990114/\#dt-qname.</span></span> <span data-ttu-id="98e64-136">Se nenhum namespace for especificado, o namespace padrão será assumido.</span><span class="sxs-lookup"><span data-stu-id="98e64-136">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="98e64-137">O nome da opção.</span><span class="sxs-lookup"><span data-stu-id="98e64-137">The name of the option.</span></span><br/>                                                                                                     |
| <span data-ttu-id="98e64-138">\_IdentityOptionValue\_</span><span class="sxs-lookup"><span data-stu-id="98e64-138">\_IdentityOptionValue\_</span></span><br/> | <span data-ttu-id="98e64-139">string</span><span class="sxs-lookup"><span data-stu-id="98e64-139">string</span></span><br/> | <span data-ttu-id="98e64-140">n/d</span><span class="sxs-lookup"><span data-stu-id="98e64-140">n/a</span></span><br/>        | <span data-ttu-id="98e64-141">True, False.</span><span class="sxs-lookup"><span data-stu-id="98e64-141">True, False.</span></span><br/>                                                                                                                                                      | <span data-ttu-id="98e64-142">Define uma Opção que, quando selecionada, desabilitará esse recurso.</span><span class="sxs-lookup"><span data-stu-id="98e64-142">Defines an Option which when selected would disable this feature.</span></span><br/>                                                           |
| <span data-ttu-id="98e64-143">\_DuplexModeValue\_</span><span class="sxs-lookup"><span data-stu-id="98e64-143">\_DuplexModeValue\_</span></span><br/>     | <span data-ttu-id="98e64-144">string</span><span class="sxs-lookup"><span data-stu-id="98e64-144">string</span></span><br/> | <span data-ttu-id="98e64-145">n/d</span><span class="sxs-lookup"><span data-stu-id="98e64-145">n/a</span></span><br/>        | <span data-ttu-id="98e64-146">Automático, Manual.</span><span class="sxs-lookup"><span data-stu-id="98e64-146">Automatic, Manual.</span></span><br/>                                                                                                                                                | <span data-ttu-id="98e64-147">Define o modo duplex.</span><span class="sxs-lookup"><span data-stu-id="98e64-147">Defines the duplex mode.</span></span> <span data-ttu-id="98e64-148">Duplex automático é executado por hardware.</span><span class="sxs-lookup"><span data-stu-id="98e64-148">Automatic duplex is performed by hardware.</span></span> <span data-ttu-id="98e64-149">A duplexação manual é executada pelo software e pelo usuário.</span><span class="sxs-lookup"><span data-stu-id="98e64-149">Manual duplexing is performed by software and the user.</span></span><br/> |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="98e64-150">linguagem XML conteúdo (XML)</span><span class="sxs-lookup"><span data-stu-id="98e64-150">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="98e64-151">As palavras-chave public Print Schema são definidas no https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace .</span><span class="sxs-lookup"><span data-stu-id="98e64-151">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="98e64-152">O conteúdo linguagem XML XML (public linguagem XML) para essa palavra-chave é definido abaixo:</span><span class="sxs-lookup"><span data-stu-id="98e64-152">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

``` syntax
<psf:Feature name="psk:JobDuplexAllDocumentsContiguously">
  <psf:Property name="psf:SelectionType">
    <psf:Value xsi:type="xs:string">psk:PickOne</psf:Value>
  </psf:Property>
  <!-- Specifies one sided printing. -->
  <psf:Option name="psk:OneSided" />
  <!-- Specifies two sided printing such that the page is flipped parallel to the MediaSizeWidth direction. -->
  <psf:Option name="psk:TwoSidedShortEdge">
    <psf:ScoredProperty name="psk:DuplexMode">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <!-- Specifies two sided printing such that the page is flipped parallel to the MediaSizeHeight direction. -->
  <psf:Option name="psk:TwoSidedLongEdge">
    <psf:ScoredProperty name="psk:DuplexMode">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
</psf:Feature>    
```

## <a name="related-topics"></a><span data-ttu-id="98e64-153">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="98e64-153">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="98e64-154">Especificação de esquema de impressão</span><span class="sxs-lookup"><span data-stu-id="98e64-154">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




