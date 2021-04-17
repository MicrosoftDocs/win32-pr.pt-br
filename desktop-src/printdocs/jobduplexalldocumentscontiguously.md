---
description: Este tópico não é atual. Para obter as informações mais atuais, consulte a especificação do esquema de impressão.
ms.assetid: dd24166c-d5e2-420e-8a8c-e1a25728ab2f
title: JobDuplexAllDocumentsContiguously
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 92c14e9c536d0ab24fafe308a8b11fa769842aab
ms.sourcegitcommit: 7b8f6151ebe247536304866459b2973276271d4d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/06/2021
ms.locfileid: "105790561"
---
# <a name="jobduplexalldocumentscontiguously"></a><span data-ttu-id="773e7-104">JobDuplexAllDocumentsContiguously</span><span class="sxs-lookup"><span data-stu-id="773e7-104">JobDuplexAllDocumentsContiguously</span></span>

<span data-ttu-id="773e7-105">Este tópico não é atual.</span><span class="sxs-lookup"><span data-stu-id="773e7-105">This topic is not current.</span></span> <span data-ttu-id="773e7-106">Para obter as informações mais atuais, consulte a [especificação do esquema de impressão](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="773e7-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="773e7-107">Descreve as características de duplex da saída.</span><span class="sxs-lookup"><span data-stu-id="773e7-107">Describes the duplex characteristics of the output.</span></span> <span data-ttu-id="773e7-108">O recurso duplex permite a impressão em ambos os lados da mídia.</span><span class="sxs-lookup"><span data-stu-id="773e7-108">The duplex feature allows for printing on both sides of the media.</span></span> <span data-ttu-id="773e7-109">Todos os documentos no trabalho são bidirecionados em conjunto de forma contígua.</span><span class="sxs-lookup"><span data-stu-id="773e7-109">All Documents in the job are duplexed together contiguously.</span></span> <span data-ttu-id="773e7-110">JobDuplexAllDocumentsContiguously e DocumentDuplex são mutuamente exclusivos.</span><span class="sxs-lookup"><span data-stu-id="773e7-110">JobDuplexAllDocumentsContiguously and DocumentDuplex are mutually exclusive.</span></span> <span data-ttu-id="773e7-111">Cabe ao driver determinar o tratamento de restrições entre essas palavras-chave.</span><span class="sxs-lookup"><span data-stu-id="773e7-111">It is up to the driver to determine constraint handling between these keywords.</span></span>

-   [<span data-ttu-id="773e7-112">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="773e7-112">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="773e7-113">Conteúdo estrutural</span><span class="sxs-lookup"><span data-stu-id="773e7-113">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="773e7-114">Conteúdo de linguagem XML (XML)</span><span class="sxs-lookup"><span data-stu-id="773e7-114">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="773e7-115">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="773e7-115">Element Information</span></span>



| <span data-ttu-id="773e7-116">Nome</span><span class="sxs-lookup"><span data-stu-id="773e7-116">Name</span></span>                       |                    |
|----------------------------|--------------------|
| <span data-ttu-id="773e7-117">Tipo de elemento</span><span class="sxs-lookup"><span data-stu-id="773e7-117">Element Type</span></span> <br/>   | <span data-ttu-id="773e7-118">Recurso</span><span class="sxs-lookup"><span data-stu-id="773e7-118">Feature</span></span><br/> |
| <span data-ttu-id="773e7-119">Prefixo de escopo</span><span class="sxs-lookup"><span data-stu-id="773e7-119">Scoping Prefix</span></span> <br/> | <span data-ttu-id="773e7-120">Trabalho</span><span class="sxs-lookup"><span data-stu-id="773e7-120">Job</span></span><br/>     |
| <span data-ttu-id="773e7-121">Observações</span><span class="sxs-lookup"><span data-stu-id="773e7-121">Notes</span></span> <br/>          | <span data-ttu-id="773e7-122">Nenhum</span><span class="sxs-lookup"><span data-stu-id="773e7-122">None</span></span><br/>    |



 

## <a name="structural-content"></a><span data-ttu-id="773e7-123">Conteúdo estrutural</span><span class="sxs-lookup"><span data-stu-id="773e7-123">Structural Content</span></span>

<span data-ttu-id="773e7-124">A estrutura XML desse elemento é:</span><span class="sxs-lookup"><span data-stu-id="773e7-124">The XML structure of this element is:</span></span>

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

## <a name="structure-variables"></a><span data-ttu-id="773e7-125">Variáveis de estrutura</span><span class="sxs-lookup"><span data-stu-id="773e7-125">Structure Variables</span></span>

<span data-ttu-id="773e7-126">A tabela a seguir descreve as características das variáveis definidas na estrutura XML.</span><span class="sxs-lookup"><span data-stu-id="773e7-126">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="773e7-127">Nome</span><span class="sxs-lookup"><span data-stu-id="773e7-127">Name</span></span>                               | <span data-ttu-id="773e7-128">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="773e7-128">Data type</span></span>         | <span data-ttu-id="773e7-129">Unidade</span><span class="sxs-lookup"><span data-stu-id="773e7-129">Unit</span></span>                  | <span data-ttu-id="773e7-130">Valores com suporte</span><span class="sxs-lookup"><span data-stu-id="773e7-130">Supported values</span></span>                                                                                                                                                             | <span data-ttu-id="773e7-131">Resumo</span><span class="sxs-lookup"><span data-stu-id="773e7-131">Summary</span></span>                                                                                                                                |
|------------------------------------|-------------------|-----------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="773e7-132">\_OptionName\_</span><span class="sxs-lookup"><span data-stu-id="773e7-132">\_OptionName\_</span></span><br/>          | <span data-ttu-id="773e7-133">string</span><span class="sxs-lookup"><span data-stu-id="773e7-133">string</span></span><br/> | <span data-ttu-id="773e7-134">characters</span><span class="sxs-lookup"><span data-stu-id="773e7-134">characters</span></span><br/> | <span data-ttu-id="773e7-135">Nome totalmente qualificado válido, conforme definido pelo https://www.w3.org/TR/1999/REC-xml-names-19990114/\#dt-qname .</span><span class="sxs-lookup"><span data-stu-id="773e7-135">Valid fully qualified name as defined by https://www.w3.org/TR/1999/REC-xml-names-19990114/\#dt-qname.</span></span> <span data-ttu-id="773e7-136">Se nenhum namespace for especificado, o namespace padrão será assumido.</span><span class="sxs-lookup"><span data-stu-id="773e7-136">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="773e7-137">O nome da opção.</span><span class="sxs-lookup"><span data-stu-id="773e7-137">The name of the option.</span></span><br/>                                                                                                     |
| <span data-ttu-id="773e7-138">\_IdentityOptionValue\_</span><span class="sxs-lookup"><span data-stu-id="773e7-138">\_IdentityOptionValue\_</span></span><br/> | <span data-ttu-id="773e7-139">string</span><span class="sxs-lookup"><span data-stu-id="773e7-139">string</span></span><br/> | <span data-ttu-id="773e7-140">N/D</span><span class="sxs-lookup"><span data-stu-id="773e7-140">n/a</span></span><br/>        | <span data-ttu-id="773e7-141">True, False.</span><span class="sxs-lookup"><span data-stu-id="773e7-141">True, False.</span></span><br/>                                                                                                                                                      | <span data-ttu-id="773e7-142">Define uma opção que, quando selecionada, desabilita esse recurso.</span><span class="sxs-lookup"><span data-stu-id="773e7-142">Defines an Option which when selected would disable this feature.</span></span><br/>                                                           |
| <span data-ttu-id="773e7-143">\_DuplexModeValue\_</span><span class="sxs-lookup"><span data-stu-id="773e7-143">\_DuplexModeValue\_</span></span><br/>     | <span data-ttu-id="773e7-144">string</span><span class="sxs-lookup"><span data-stu-id="773e7-144">string</span></span><br/> | <span data-ttu-id="773e7-145">N/D</span><span class="sxs-lookup"><span data-stu-id="773e7-145">n/a</span></span><br/>        | <span data-ttu-id="773e7-146">Automático, manual.</span><span class="sxs-lookup"><span data-stu-id="773e7-146">Automatic, Manual.</span></span><br/>                                                                                                                                                | <span data-ttu-id="773e7-147">Define o modo duplex.</span><span class="sxs-lookup"><span data-stu-id="773e7-147">Defines the duplex mode.</span></span> <span data-ttu-id="773e7-148">O duplex automático é executado pelo hardware.</span><span class="sxs-lookup"><span data-stu-id="773e7-148">Automatic duplex is performed by hardware.</span></span> <span data-ttu-id="773e7-149">O Duplexing manual é executado pelo software e pelo usuário.</span><span class="sxs-lookup"><span data-stu-id="773e7-149">Manual duplexing is performed by software and the user.</span></span><br/> |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="773e7-150">Conteúdo de linguagem XML (XML)</span><span class="sxs-lookup"><span data-stu-id="773e7-150">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="773e7-151">As palavras-chave do esquema de impressão pública são definidas no https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span><span class="sxs-lookup"><span data-stu-id="773e7-151">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="773e7-152">O conteúdo do linguagem XML público (XML) para essa palavra-chave é definido abaixo:</span><span class="sxs-lookup"><span data-stu-id="773e7-152">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

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

## <a name="related-topics"></a><span data-ttu-id="773e7-153">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="773e7-153">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="773e7-154">Especificação de esquema de impressão</span><span class="sxs-lookup"><span data-stu-id="773e7-154">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




