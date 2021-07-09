---
description: Saiba mais sobre o elemento PageForceFrontSide configurável pelo usuário. Este tópico não é atual. Para obter as informações mais atuais, consulte a especificação do esquema de impressão.
ms.assetid: 0658c808-f050-41f3-90b6-2a013b616b58
title: PageForceFrontSide
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 79f22e9ec52b7cee72e8f3a479d161e9abb765c4
ms.sourcegitcommit: 998d50f6def8a25850fc113fc8a2df903c829c5e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/09/2021
ms.locfileid: "113549184"
---
# <a name="pageforcefrontside"></a><span data-ttu-id="cd5de-105">PageForceFrontSide</span><span class="sxs-lookup"><span data-stu-id="cd5de-105">PageForceFrontSide</span></span>

<span data-ttu-id="cd5de-106">Este tópico não é atual.</span><span class="sxs-lookup"><span data-stu-id="cd5de-106">This topic is not current.</span></span> <span data-ttu-id="cd5de-107">Para obter as informações mais atuais, consulte a [especificação do esquema de impressão](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="cd5de-107">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="cd5de-108">Força a saída a aparecer na frente de uma folha de mídia.</span><span class="sxs-lookup"><span data-stu-id="cd5de-108">Forces the output to appear on the front of a media sheet.</span></span> <span data-ttu-id="cd5de-109">Relevante para folhas de mídia com superfícies diferentes em cada lado.</span><span class="sxs-lookup"><span data-stu-id="cd5de-109">Relevant to media sheets with different surfaces on each side.</span></span> <span data-ttu-id="cd5de-110">Nos casos em que esse recurso interfere nas opções de processamento (como DocumentDuplex), PageForceFrontSide tem precedência para a página específica à qual o recurso se aplica.</span><span class="sxs-lookup"><span data-stu-id="cd5de-110">In cases where this feature interferes with processing options (such as DocumentDuplex), PageForceFrontSide takes precedence for the specific page to which the feature applies.</span></span>

-   [<span data-ttu-id="cd5de-111">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="cd5de-111">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="cd5de-112">Conteúdo estrutural</span><span class="sxs-lookup"><span data-stu-id="cd5de-112">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="cd5de-113">Conteúdo de linguagem XML (XML)</span><span class="sxs-lookup"><span data-stu-id="cd5de-113">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="cd5de-114">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="cd5de-114">Element Information</span></span>



| <span data-ttu-id="cd5de-115">Nome</span><span class="sxs-lookup"><span data-stu-id="cd5de-115">Name</span></span> | <span data-ttu-id="cd5de-116">Valor</span><span class="sxs-lookup"><span data-stu-id="cd5de-116">Value</span></span> |
|----------------------------|--------------------|
| <span data-ttu-id="cd5de-117">Tipo de elemento</span><span class="sxs-lookup"><span data-stu-id="cd5de-117">Element Type</span></span> <br/>   | <span data-ttu-id="cd5de-118">Recurso</span><span class="sxs-lookup"><span data-stu-id="cd5de-118">Feature</span></span><br/> |
| <span data-ttu-id="cd5de-119">Prefixo de escopo</span><span class="sxs-lookup"><span data-stu-id="cd5de-119">Scoping Prefix</span></span> <br/> | <span data-ttu-id="cd5de-120">Página</span><span class="sxs-lookup"><span data-stu-id="cd5de-120">Page</span></span><br/>    |
| <span data-ttu-id="cd5de-121">Observações</span><span class="sxs-lookup"><span data-stu-id="cd5de-121">Notes</span></span> <br/>          | <span data-ttu-id="cd5de-122">Nenhum</span><span class="sxs-lookup"><span data-stu-id="cd5de-122">None</span></span><br/>    |



 

## <a name="structural-content"></a><span data-ttu-id="cd5de-123">Conteúdo estrutural</span><span class="sxs-lookup"><span data-stu-id="cd5de-123">Structural Content</span></span>

<span data-ttu-id="cd5de-124">A estrutura XML desse elemento é:</span><span class="sxs-lookup"><span data-stu-id="cd5de-124">The XML structure of this element is:</span></span>

``` syntax
<psf:Feature name="psk:PageForceFrontSide">
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

## <a name="structure-variables"></a><span data-ttu-id="cd5de-125">Variáveis de estrutura</span><span class="sxs-lookup"><span data-stu-id="cd5de-125">Structure Variables</span></span>

<span data-ttu-id="cd5de-126">A tabela a seguir descreve as características das variáveis definidas na estrutura XML.</span><span class="sxs-lookup"><span data-stu-id="cd5de-126">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="cd5de-127">Nome</span><span class="sxs-lookup"><span data-stu-id="cd5de-127">Name</span></span>                               | <span data-ttu-id="cd5de-128">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="cd5de-128">Data type</span></span>         | <span data-ttu-id="cd5de-129">Unidade</span><span class="sxs-lookup"><span data-stu-id="cd5de-129">Unit</span></span>                  | <span data-ttu-id="cd5de-130">Valores com suporte</span><span class="sxs-lookup"><span data-stu-id="cd5de-130">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="cd5de-131">Resumo</span><span class="sxs-lookup"><span data-stu-id="cd5de-131">Summary</span></span>                                                                      |
|------------------------------------|-------------------|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="cd5de-132">\_OptionName\_</span><span class="sxs-lookup"><span data-stu-id="cd5de-132">\_OptionName\_</span></span><br/>          | <span data-ttu-id="cd5de-133">string</span><span class="sxs-lookup"><span data-stu-id="cd5de-133">string</span></span><br/> | <span data-ttu-id="cd5de-134">characters</span><span class="sxs-lookup"><span data-stu-id="cd5de-134">characters</span></span><br/> | <span data-ttu-id="cd5de-135">Nome totalmente qualificado válido, conforme definido pelos [namespaces em XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span><span class="sxs-lookup"><span data-stu-id="cd5de-135">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="cd5de-136">Se nenhum namespace for especificado, o namespace padrão será assumido.</span><span class="sxs-lookup"><span data-stu-id="cd5de-136">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="cd5de-137">O nome da opção.</span><span class="sxs-lookup"><span data-stu-id="cd5de-137">The name of the option.</span></span><br/>                                           |
| <span data-ttu-id="cd5de-138">\_IdentityOptionValue\_</span><span class="sxs-lookup"><span data-stu-id="cd5de-138">\_IdentityOptionValue\_</span></span><br/> | <span data-ttu-id="cd5de-139">string</span><span class="sxs-lookup"><span data-stu-id="cd5de-139">string</span></span><br/> | <span data-ttu-id="cd5de-140">n/d</span><span class="sxs-lookup"><span data-stu-id="cd5de-140">n/a</span></span><br/>        | <span data-ttu-id="cd5de-141">True, False.</span><span class="sxs-lookup"><span data-stu-id="cd5de-141">True, False.</span></span><br/>                                                                                                                                                               | <span data-ttu-id="cd5de-142">Define uma opção que, quando selecionada, desabilita esse recurso.</span><span class="sxs-lookup"><span data-stu-id="cd5de-142">Defines an Option which when selected would disable this feature.</span></span><br/> |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="cd5de-143">Conteúdo de linguagem XML (XML)</span><span class="sxs-lookup"><span data-stu-id="cd5de-143">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="cd5de-144">As palavras-chave do esquema de impressão pública são definidas no https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span><span class="sxs-lookup"><span data-stu-id="cd5de-144">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="cd5de-145">O conteúdo do linguagem XML público (XML) para essa palavra-chave é definido abaixo:</span><span class="sxs-lookup"><span data-stu-id="cd5de-145">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

``` syntax
<psf:Feature name="psk:PageForceFrontSide">
  <psf:Property name="psf:SelectionType">
    <psf:Value xsi:type="xs:string">psk:PickOne</psf:Value>
  </psf:Property>
  <!-- Specifies output is restricted to the front side of the sheet. -->
  <psf:Option name="psk:ForceFrontSide" />
  <!-- Specifies no output restrictions.  -->
  <psf:Option name="psk:None" />
</psf:Feature>    
```

## <a name="related-topics"></a><span data-ttu-id="cd5de-146">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="cd5de-146">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="cd5de-147">Especificação de esquema de impressão</span><span class="sxs-lookup"><span data-stu-id="cd5de-147">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




