---
description: Este tópico não é atual. Para obter as informações mais atuais, consulte a especificação do esquema de impressão.
ms.assetid: dadc52e8-1733-4267-85aa-33d0ddd3dfa2
title: DocumentDuplex
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fb2d65ac1007b8413f9e5e6cc12802e0ac27dac3
ms.sourcegitcommit: 7b8f6151ebe247536304866459b2973276271d4d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/06/2021
ms.locfileid: "104172591"
---
# <a name="documentduplex"></a><span data-ttu-id="01b58-104">DocumentDuplex</span><span class="sxs-lookup"><span data-stu-id="01b58-104">DocumentDuplex</span></span>

<span data-ttu-id="01b58-105">Este tópico não é atual.</span><span class="sxs-lookup"><span data-stu-id="01b58-105">This topic is not current.</span></span> <span data-ttu-id="01b58-106">Para obter as informações mais atuais, consulte a [especificação do esquema de impressão](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="01b58-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="01b58-107">Descreve as características de duplex da saída.</span><span class="sxs-lookup"><span data-stu-id="01b58-107">Describes the duplex characteristics of the output.</span></span> <span data-ttu-id="01b58-108">O recurso duplex permite a impressão em ambos os lados da mídia.</span><span class="sxs-lookup"><span data-stu-id="01b58-108">The duplex feature allows for printing on both sides of the media.</span></span> <span data-ttu-id="01b58-109">Cada documento fica duplexado separadamente.</span><span class="sxs-lookup"><span data-stu-id="01b58-109">Each document is duplexed separately.</span></span> <span data-ttu-id="01b58-110">DocumentDuplex e JobDuplexAllDocumentsContiguously são mutuamente exclusivos.</span><span class="sxs-lookup"><span data-stu-id="01b58-110">DocumentDuplex and JobDuplexAllDocumentsContiguously are mutually exclusive.</span></span> <span data-ttu-id="01b58-111">Cabe ao driver determinar o tratamento de restrições entre essas palavras-chave.</span><span class="sxs-lookup"><span data-stu-id="01b58-111">It is up to the driver to determine constraint handling between these keywords.</span></span>

-   [<span data-ttu-id="01b58-112">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="01b58-112">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="01b58-113">Conteúdo estrutural</span><span class="sxs-lookup"><span data-stu-id="01b58-113">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="01b58-114">Conteúdo de linguagem XML (XML)</span><span class="sxs-lookup"><span data-stu-id="01b58-114">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="01b58-115">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="01b58-115">Element Information</span></span>



| <span data-ttu-id="01b58-116">Nome</span><span class="sxs-lookup"><span data-stu-id="01b58-116">Name</span></span>                       |                     |
|----------------------------|---------------------|
| <span data-ttu-id="01b58-117">Tipo de elemento</span><span class="sxs-lookup"><span data-stu-id="01b58-117">Element Type</span></span> <br/>   | <span data-ttu-id="01b58-118">Recurso</span><span class="sxs-lookup"><span data-stu-id="01b58-118">Feature</span></span><br/>  |
| <span data-ttu-id="01b58-119">Prefixo de escopo</span><span class="sxs-lookup"><span data-stu-id="01b58-119">Scoping Prefix</span></span> <br/> | <span data-ttu-id="01b58-120">Documento</span><span class="sxs-lookup"><span data-stu-id="01b58-120">Document</span></span><br/> |
| <span data-ttu-id="01b58-121">Observações</span><span class="sxs-lookup"><span data-stu-id="01b58-121">Notes</span></span> <br/>          | <span data-ttu-id="01b58-122">Nenhum</span><span class="sxs-lookup"><span data-stu-id="01b58-122">None</span></span><br/>     |



 

## <a name="structural-content"></a><span data-ttu-id="01b58-123">Conteúdo estrutural</span><span class="sxs-lookup"><span data-stu-id="01b58-123">Structural Content</span></span>

<span data-ttu-id="01b58-124">A estrutura XML desse elemento é a seguinte:</span><span class="sxs-lookup"><span data-stu-id="01b58-124">The XML structure of this element is as follows:</span></span>

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

## <a name="structure-variables"></a><span data-ttu-id="01b58-125">Variáveis de estrutura</span><span class="sxs-lookup"><span data-stu-id="01b58-125">Structure Variables</span></span>

<span data-ttu-id="01b58-126">A tabela a seguir descreve as características das variáveis definidas na estrutura XML.</span><span class="sxs-lookup"><span data-stu-id="01b58-126">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="01b58-127">Nome</span><span class="sxs-lookup"><span data-stu-id="01b58-127">Name</span></span>                               | <span data-ttu-id="01b58-128">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="01b58-128">Data type</span></span>         | <span data-ttu-id="01b58-129">Unidade</span><span class="sxs-lookup"><span data-stu-id="01b58-129">Unit</span></span>                  | <span data-ttu-id="01b58-130">Valores com suporte</span><span class="sxs-lookup"><span data-stu-id="01b58-130">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="01b58-131">Resumo</span><span class="sxs-lookup"><span data-stu-id="01b58-131">Summary</span></span>                                                                                                                                |
|------------------------------------|-------------------|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="01b58-132">\_OptionName\_</span><span class="sxs-lookup"><span data-stu-id="01b58-132">\_OptionName\_</span></span><br/>          | <span data-ttu-id="01b58-133">string</span><span class="sxs-lookup"><span data-stu-id="01b58-133">string</span></span><br/> | <span data-ttu-id="01b58-134">characters</span><span class="sxs-lookup"><span data-stu-id="01b58-134">characters</span></span><br/> | <span data-ttu-id="01b58-135">Nome totalmente qualificado válido, conforme definido pelos [namespaces em XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span><span class="sxs-lookup"><span data-stu-id="01b58-135">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="01b58-136">Se nenhum namespace for especificado, o namespace padrão será assumido.</span><span class="sxs-lookup"><span data-stu-id="01b58-136">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="01b58-137">O nome da opção.</span><span class="sxs-lookup"><span data-stu-id="01b58-137">The name of the option.</span></span><br/>                                                                                                     |
| <span data-ttu-id="01b58-138">\_IdentityOptionValue\_</span><span class="sxs-lookup"><span data-stu-id="01b58-138">\_IdentityOptionValue\_</span></span><br/> | <span data-ttu-id="01b58-139">string</span><span class="sxs-lookup"><span data-stu-id="01b58-139">string</span></span><br/> | <span data-ttu-id="01b58-140">N/D</span><span class="sxs-lookup"><span data-stu-id="01b58-140">n/a</span></span><br/>        | <span data-ttu-id="01b58-141">True, False.</span><span class="sxs-lookup"><span data-stu-id="01b58-141">True, False.</span></span><br/>                                                                                                                                                               | <span data-ttu-id="01b58-142">Define uma opção que, quando selecionada, desabilita esse recurso.</span><span class="sxs-lookup"><span data-stu-id="01b58-142">Defines an Option which when selected would disable this feature.</span></span><br/>                                                           |
| <span data-ttu-id="01b58-143">\_DuplexModeValue\_</span><span class="sxs-lookup"><span data-stu-id="01b58-143">\_DuplexModeValue\_</span></span><br/>     | <span data-ttu-id="01b58-144">string</span><span class="sxs-lookup"><span data-stu-id="01b58-144">string</span></span><br/> | <span data-ttu-id="01b58-145">N/D</span><span class="sxs-lookup"><span data-stu-id="01b58-145">n/a</span></span><br/>        | <span data-ttu-id="01b58-146">Automático, manual.</span><span class="sxs-lookup"><span data-stu-id="01b58-146">Automatic, Manual.</span></span><br/>                                                                                                                                                         | <span data-ttu-id="01b58-147">Define o modo duplex.</span><span class="sxs-lookup"><span data-stu-id="01b58-147">Defines the duplex mode.</span></span> <span data-ttu-id="01b58-148">O duplex automático é executado pelo hardware.</span><span class="sxs-lookup"><span data-stu-id="01b58-148">Automatic duplex is performed by hardware.</span></span> <span data-ttu-id="01b58-149">O Duplexing manual é executado pelo software e pelo usuário.</span><span class="sxs-lookup"><span data-stu-id="01b58-149">Manual duplexing is performed by software and the user.</span></span><br/> |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="01b58-150">Conteúdo de linguagem XML (XML)</span><span class="sxs-lookup"><span data-stu-id="01b58-150">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="01b58-151">As palavras-chave do esquema de impressão pública são definidas no https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span><span class="sxs-lookup"><span data-stu-id="01b58-151">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="01b58-152">O conteúdo do linguagem XML público (XML) para essa palavra-chave é definido abaixo:</span><span class="sxs-lookup"><span data-stu-id="01b58-152">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

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

## <a name="related-topics"></a><span data-ttu-id="01b58-153">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="01b58-153">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="01b58-154">Especificação de esquema de impressão</span><span class="sxs-lookup"><span data-stu-id="01b58-154">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




