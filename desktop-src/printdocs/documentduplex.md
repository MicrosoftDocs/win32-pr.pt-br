---
description: Saiba mais sobre o elemento DocumentDuplex, que descreve as características de duplex da saída. O recurso duplex permite a impressão em ambos os lados da mídia.
ms.assetid: dadc52e8-1733-4267-85aa-33d0ddd3dfa2
title: DocumentDuplex
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5c2ad8521835213594f10507ab6fd4b9cca24040
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/19/2021
ms.locfileid: "112409339"
---
# <a name="documentduplex"></a><span data-ttu-id="c42e6-104">DocumentDuplex</span><span class="sxs-lookup"><span data-stu-id="c42e6-104">DocumentDuplex</span></span>

<span data-ttu-id="c42e6-105">Este tópico não é atual.</span><span class="sxs-lookup"><span data-stu-id="c42e6-105">This topic is not current.</span></span> <span data-ttu-id="c42e6-106">Para obter as informações mais atuais, consulte a [especificação do esquema de impressão](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="c42e6-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="c42e6-107">Descreve as características de duplex da saída.</span><span class="sxs-lookup"><span data-stu-id="c42e6-107">Describes the duplex characteristics of the output.</span></span> <span data-ttu-id="c42e6-108">O recurso duplex permite a impressão em ambos os lados da mídia.</span><span class="sxs-lookup"><span data-stu-id="c42e6-108">The duplex feature allows for printing on both sides of the media.</span></span> <span data-ttu-id="c42e6-109">Cada documento fica duplexado separadamente.</span><span class="sxs-lookup"><span data-stu-id="c42e6-109">Each document is duplexed separately.</span></span> <span data-ttu-id="c42e6-110">DocumentDuplex e JobDuplexAllDocumentsContiguously são mutuamente exclusivos.</span><span class="sxs-lookup"><span data-stu-id="c42e6-110">DocumentDuplex and JobDuplexAllDocumentsContiguously are mutually exclusive.</span></span> <span data-ttu-id="c42e6-111">Cabe ao driver determinar o tratamento de restrições entre essas palavras-chave.</span><span class="sxs-lookup"><span data-stu-id="c42e6-111">It is up to the driver to determine constraint handling between these keywords.</span></span>

-   [<span data-ttu-id="c42e6-112">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="c42e6-112">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="c42e6-113">Conteúdo estrutural</span><span class="sxs-lookup"><span data-stu-id="c42e6-113">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="c42e6-114">Conteúdo de linguagem XML (XML)</span><span class="sxs-lookup"><span data-stu-id="c42e6-114">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="c42e6-115">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="c42e6-115">Element Information</span></span>



| <span data-ttu-id="c42e6-116">Name</span><span class="sxs-lookup"><span data-stu-id="c42e6-116">Name</span></span> | <span data-ttu-id="c42e6-117">Valor</span><span class="sxs-lookup"><span data-stu-id="c42e6-117">Value</span></span> |
|----------------------------|---------------------|
| <span data-ttu-id="c42e6-118">Tipo de elemento</span><span class="sxs-lookup"><span data-stu-id="c42e6-118">Element Type</span></span> <br/>   | <span data-ttu-id="c42e6-119">Recurso</span><span class="sxs-lookup"><span data-stu-id="c42e6-119">Feature</span></span><br/>  |
| <span data-ttu-id="c42e6-120">Prefixo de escopo</span><span class="sxs-lookup"><span data-stu-id="c42e6-120">Scoping Prefix</span></span> <br/> | <span data-ttu-id="c42e6-121">Documento</span><span class="sxs-lookup"><span data-stu-id="c42e6-121">Document</span></span><br/> |
| <span data-ttu-id="c42e6-122">Observações</span><span class="sxs-lookup"><span data-stu-id="c42e6-122">Notes</span></span> <br/>          | <span data-ttu-id="c42e6-123">Nenhum</span><span class="sxs-lookup"><span data-stu-id="c42e6-123">None</span></span><br/>     |



 

## <a name="structural-content"></a><span data-ttu-id="c42e6-124">Conteúdo estrutural</span><span class="sxs-lookup"><span data-stu-id="c42e6-124">Structural Content</span></span>

<span data-ttu-id="c42e6-125">A estrutura XML desse elemento é a seguinte:</span><span class="sxs-lookup"><span data-stu-id="c42e6-125">The XML structure of this element is as follows:</span></span>

``` syntax
<psf:Feature name="psk:DocumentDuplex">
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

## <a name="structure-variables"></a><span data-ttu-id="c42e6-126">Variáveis de estrutura</span><span class="sxs-lookup"><span data-stu-id="c42e6-126">Structure Variables</span></span>

<span data-ttu-id="c42e6-127">A tabela a seguir descreve as características das variáveis definidas na estrutura XML.</span><span class="sxs-lookup"><span data-stu-id="c42e6-127">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="c42e6-128">Nome</span><span class="sxs-lookup"><span data-stu-id="c42e6-128">Name</span></span>                               | <span data-ttu-id="c42e6-129">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="c42e6-129">Data type</span></span>         | <span data-ttu-id="c42e6-130">Unidade</span><span class="sxs-lookup"><span data-stu-id="c42e6-130">Unit</span></span>                  | <span data-ttu-id="c42e6-131">Valores com suporte</span><span class="sxs-lookup"><span data-stu-id="c42e6-131">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="c42e6-132">Resumo</span><span class="sxs-lookup"><span data-stu-id="c42e6-132">Summary</span></span>                                                                                                                                |
|------------------------------------|-------------------|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c42e6-133">\_OptionName\_</span><span class="sxs-lookup"><span data-stu-id="c42e6-133">\_OptionName\_</span></span><br/>          | <span data-ttu-id="c42e6-134">string</span><span class="sxs-lookup"><span data-stu-id="c42e6-134">string</span></span><br/> | <span data-ttu-id="c42e6-135">characters</span><span class="sxs-lookup"><span data-stu-id="c42e6-135">characters</span></span><br/> | <span data-ttu-id="c42e6-136">Nome totalmente qualificado válido, conforme definido pelos [namespaces em XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span><span class="sxs-lookup"><span data-stu-id="c42e6-136">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="c42e6-137">Se nenhum namespace for especificado, o namespace padrão será assumido.</span><span class="sxs-lookup"><span data-stu-id="c42e6-137">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="c42e6-138">O nome da opção.</span><span class="sxs-lookup"><span data-stu-id="c42e6-138">The name of the option.</span></span><br/>                                                                                                     |
| <span data-ttu-id="c42e6-139">\_IdentityOptionValue\_</span><span class="sxs-lookup"><span data-stu-id="c42e6-139">\_IdentityOptionValue\_</span></span><br/> | <span data-ttu-id="c42e6-140">string</span><span class="sxs-lookup"><span data-stu-id="c42e6-140">string</span></span><br/> | <span data-ttu-id="c42e6-141">n/d</span><span class="sxs-lookup"><span data-stu-id="c42e6-141">n/a</span></span><br/>        | <span data-ttu-id="c42e6-142">True, False.</span><span class="sxs-lookup"><span data-stu-id="c42e6-142">True, False.</span></span><br/>                                                                                                                                                               | <span data-ttu-id="c42e6-143">Define uma opção que, quando selecionada, desabilita esse recurso.</span><span class="sxs-lookup"><span data-stu-id="c42e6-143">Defines an Option which when selected would disable this feature.</span></span><br/>                                                           |
| <span data-ttu-id="c42e6-144">\_DuplexModeValue\_</span><span class="sxs-lookup"><span data-stu-id="c42e6-144">\_DuplexModeValue\_</span></span><br/>     | <span data-ttu-id="c42e6-145">string</span><span class="sxs-lookup"><span data-stu-id="c42e6-145">string</span></span><br/> | <span data-ttu-id="c42e6-146">n/d</span><span class="sxs-lookup"><span data-stu-id="c42e6-146">n/a</span></span><br/>        | <span data-ttu-id="c42e6-147">Automático, manual.</span><span class="sxs-lookup"><span data-stu-id="c42e6-147">Automatic, Manual.</span></span><br/>                                                                                                                                                         | <span data-ttu-id="c42e6-148">Define o modo duplex.</span><span class="sxs-lookup"><span data-stu-id="c42e6-148">Defines the duplex mode.</span></span> <span data-ttu-id="c42e6-149">O duplex automático é executado pelo hardware.</span><span class="sxs-lookup"><span data-stu-id="c42e6-149">Automatic duplex is performed by hardware.</span></span> <span data-ttu-id="c42e6-150">O Duplexing manual é executado pelo software e pelo usuário.</span><span class="sxs-lookup"><span data-stu-id="c42e6-150">Manual duplexing is performed by software and the user.</span></span><br/> |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="c42e6-151">Conteúdo de linguagem XML (XML)</span><span class="sxs-lookup"><span data-stu-id="c42e6-151">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="c42e6-152">As palavras-chave do esquema de impressão pública são definidas no https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span><span class="sxs-lookup"><span data-stu-id="c42e6-152">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="c42e6-153">O conteúdo do linguagem XML público (XML) para essa palavra-chave é definido abaixo:</span><span class="sxs-lookup"><span data-stu-id="c42e6-153">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

``` syntax
<psf:Feature name="psk:DocumentDuplex">
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

## <a name="related-topics"></a><span data-ttu-id="c42e6-154">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="c42e6-154">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c42e6-155">Especificação de esquema de impressão</span><span class="sxs-lookup"><span data-stu-id="c42e6-155">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




