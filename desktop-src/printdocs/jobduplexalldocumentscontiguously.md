---
description: Este tópico não é atual. Para obter as informações mais atuais, consulte a especificação do esquema de impressão.
ms.assetid: dd24166c-d5e2-420e-8a8c-e1a25728ab2f
title: JobDuplexAllDocumentsContiguously
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6e5ae88213af15b53f71e406b4caf791b80f286f
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/26/2021
ms.locfileid: "107998213"
---
# <a name="jobduplexalldocumentscontiguously"></a><span data-ttu-id="f85c3-104">JobDuplexAllDocumentsContiguously</span><span class="sxs-lookup"><span data-stu-id="f85c3-104">JobDuplexAllDocumentsContiguously</span></span>

<span data-ttu-id="f85c3-105">Este tópico não é atual.</span><span class="sxs-lookup"><span data-stu-id="f85c3-105">This topic is not current.</span></span> <span data-ttu-id="f85c3-106">Para obter as informações mais atuais, consulte a [especificação do esquema de impressão](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="f85c3-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="f85c3-107">Descreve as características de duplex da saída.</span><span class="sxs-lookup"><span data-stu-id="f85c3-107">Describes the duplex characteristics of the output.</span></span> <span data-ttu-id="f85c3-108">O recurso duplex permite a impressão em ambos os lados da mídia.</span><span class="sxs-lookup"><span data-stu-id="f85c3-108">The duplex feature allows for printing on both sides of the media.</span></span> <span data-ttu-id="f85c3-109">Todos os documentos no trabalho são bidirecionados em conjunto de forma contígua.</span><span class="sxs-lookup"><span data-stu-id="f85c3-109">All Documents in the job are duplexed together contiguously.</span></span> <span data-ttu-id="f85c3-110">JobDuplexAllDocumentsContiguously e DocumentDuplex são mutuamente exclusivos.</span><span class="sxs-lookup"><span data-stu-id="f85c3-110">JobDuplexAllDocumentsContiguously and DocumentDuplex are mutually exclusive.</span></span> <span data-ttu-id="f85c3-111">Cabe ao driver determinar o tratamento de restrições entre essas palavras-chave.</span><span class="sxs-lookup"><span data-stu-id="f85c3-111">It is up to the driver to determine constraint handling between these keywords.</span></span>

-   [<span data-ttu-id="f85c3-112">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="f85c3-112">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="f85c3-113">Conteúdo estrutural</span><span class="sxs-lookup"><span data-stu-id="f85c3-113">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="f85c3-114">Conteúdo de linguagem XML (XML)</span><span class="sxs-lookup"><span data-stu-id="f85c3-114">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="f85c3-115">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="f85c3-115">Element Information</span></span>



| <span data-ttu-id="f85c3-116">Nome</span><span class="sxs-lookup"><span data-stu-id="f85c3-116">Name</span></span> | <span data-ttu-id="f85c3-117">Valor</span><span class="sxs-lookup"><span data-stu-id="f85c3-117">Value</span></span> |
|----------------------------|--------------------|
| <span data-ttu-id="f85c3-118">Tipo de elemento</span><span class="sxs-lookup"><span data-stu-id="f85c3-118">Element Type</span></span> <br/>   | <span data-ttu-id="f85c3-119">Recurso</span><span class="sxs-lookup"><span data-stu-id="f85c3-119">Feature</span></span><br/> |
| <span data-ttu-id="f85c3-120">Prefixo de escopo</span><span class="sxs-lookup"><span data-stu-id="f85c3-120">Scoping Prefix</span></span> <br/> | <span data-ttu-id="f85c3-121">Trabalho</span><span class="sxs-lookup"><span data-stu-id="f85c3-121">Job</span></span><br/>     |
| <span data-ttu-id="f85c3-122">Observações</span><span class="sxs-lookup"><span data-stu-id="f85c3-122">Notes</span></span> <br/>          | <span data-ttu-id="f85c3-123">Nenhum</span><span class="sxs-lookup"><span data-stu-id="f85c3-123">None</span></span><br/>    |



 

## <a name="structural-content"></a><span data-ttu-id="f85c3-124">Conteúdo estrutural</span><span class="sxs-lookup"><span data-stu-id="f85c3-124">Structural Content</span></span>

<span data-ttu-id="f85c3-125">A estrutura XML desse elemento é:</span><span class="sxs-lookup"><span data-stu-id="f85c3-125">The XML structure of this element is:</span></span>

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

## <a name="structure-variables"></a><span data-ttu-id="f85c3-126">Variáveis de estrutura</span><span class="sxs-lookup"><span data-stu-id="f85c3-126">Structure Variables</span></span>

<span data-ttu-id="f85c3-127">A tabela a seguir descreve as características das variáveis definidas na estrutura XML.</span><span class="sxs-lookup"><span data-stu-id="f85c3-127">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="f85c3-128">Nome</span><span class="sxs-lookup"><span data-stu-id="f85c3-128">Name</span></span>                               | <span data-ttu-id="f85c3-129">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="f85c3-129">Data type</span></span>         | <span data-ttu-id="f85c3-130">Unidade</span><span class="sxs-lookup"><span data-stu-id="f85c3-130">Unit</span></span>                  | <span data-ttu-id="f85c3-131">Valores com suporte</span><span class="sxs-lookup"><span data-stu-id="f85c3-131">Supported values</span></span>                                                                                                                                                             | <span data-ttu-id="f85c3-132">Resumo</span><span class="sxs-lookup"><span data-stu-id="f85c3-132">Summary</span></span>                                                                                                                                |
|------------------------------------|-------------------|-----------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f85c3-133">\_OptionName\_</span><span class="sxs-lookup"><span data-stu-id="f85c3-133">\_OptionName\_</span></span><br/>          | <span data-ttu-id="f85c3-134">string</span><span class="sxs-lookup"><span data-stu-id="f85c3-134">string</span></span><br/> | <span data-ttu-id="f85c3-135">characters</span><span class="sxs-lookup"><span data-stu-id="f85c3-135">characters</span></span><br/> | <span data-ttu-id="f85c3-136">Nome totalmente qualificado válido, conforme definido pelo https://www.w3.org/TR/1999/REC-xml-names-19990114/\#dt-qname .</span><span class="sxs-lookup"><span data-stu-id="f85c3-136">Valid fully qualified name as defined by https://www.w3.org/TR/1999/REC-xml-names-19990114/\#dt-qname.</span></span> <span data-ttu-id="f85c3-137">Se nenhum namespace for especificado, o namespace padrão será assumido.</span><span class="sxs-lookup"><span data-stu-id="f85c3-137">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="f85c3-138">O nome da opção.</span><span class="sxs-lookup"><span data-stu-id="f85c3-138">The name of the option.</span></span><br/>                                                                                                     |
| <span data-ttu-id="f85c3-139">\_IdentityOptionValue\_</span><span class="sxs-lookup"><span data-stu-id="f85c3-139">\_IdentityOptionValue\_</span></span><br/> | <span data-ttu-id="f85c3-140">string</span><span class="sxs-lookup"><span data-stu-id="f85c3-140">string</span></span><br/> | <span data-ttu-id="f85c3-141">N/D</span><span class="sxs-lookup"><span data-stu-id="f85c3-141">n/a</span></span><br/>        | <span data-ttu-id="f85c3-142">True, False.</span><span class="sxs-lookup"><span data-stu-id="f85c3-142">True, False.</span></span><br/>                                                                                                                                                      | <span data-ttu-id="f85c3-143">Define uma opção que, quando selecionada, desabilita esse recurso.</span><span class="sxs-lookup"><span data-stu-id="f85c3-143">Defines an Option which when selected would disable this feature.</span></span><br/>                                                           |
| <span data-ttu-id="f85c3-144">\_DuplexModeValue\_</span><span class="sxs-lookup"><span data-stu-id="f85c3-144">\_DuplexModeValue\_</span></span><br/>     | <span data-ttu-id="f85c3-145">string</span><span class="sxs-lookup"><span data-stu-id="f85c3-145">string</span></span><br/> | <span data-ttu-id="f85c3-146">N/D</span><span class="sxs-lookup"><span data-stu-id="f85c3-146">n/a</span></span><br/>        | <span data-ttu-id="f85c3-147">Automático, manual.</span><span class="sxs-lookup"><span data-stu-id="f85c3-147">Automatic, Manual.</span></span><br/>                                                                                                                                                | <span data-ttu-id="f85c3-148">Define o modo duplex.</span><span class="sxs-lookup"><span data-stu-id="f85c3-148">Defines the duplex mode.</span></span> <span data-ttu-id="f85c3-149">O duplex automático é executado pelo hardware.</span><span class="sxs-lookup"><span data-stu-id="f85c3-149">Automatic duplex is performed by hardware.</span></span> <span data-ttu-id="f85c3-150">O Duplexing manual é executado pelo software e pelo usuário.</span><span class="sxs-lookup"><span data-stu-id="f85c3-150">Manual duplexing is performed by software and the user.</span></span><br/> |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="f85c3-151">Conteúdo de linguagem XML (XML)</span><span class="sxs-lookup"><span data-stu-id="f85c3-151">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="f85c3-152">As palavras-chave do esquema de impressão pública são definidas no https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span><span class="sxs-lookup"><span data-stu-id="f85c3-152">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="f85c3-153">O conteúdo do linguagem XML público (XML) para essa palavra-chave é definido abaixo:</span><span class="sxs-lookup"><span data-stu-id="f85c3-153">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

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

## <a name="related-topics"></a><span data-ttu-id="f85c3-154">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="f85c3-154">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f85c3-155">Especificação de esquema de impressão</span><span class="sxs-lookup"><span data-stu-id="f85c3-155">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




