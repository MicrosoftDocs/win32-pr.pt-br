---
description: Este tópico não é atual. Para obter as informações mais atuais, consulte a especificação do esquema de impressão.
ms.assetid: 0658c808-f050-41f3-90b6-2a013b616b58
title: PageForceFrontSide
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e363050034137bcfb3ff2b779ecda05200865312
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/26/2021
ms.locfileid: "107996933"
---
# <a name="pageforcefrontside"></a><span data-ttu-id="64668-104">PageForceFrontSide</span><span class="sxs-lookup"><span data-stu-id="64668-104">PageForceFrontSide</span></span>

<span data-ttu-id="64668-105">Este tópico não é atual.</span><span class="sxs-lookup"><span data-stu-id="64668-105">This topic is not current.</span></span> <span data-ttu-id="64668-106">Para obter as informações mais atuais, consulte a [especificação do esquema de impressão](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="64668-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="64668-107">Força a saída a aparecer na frente de uma folha de mídia.</span><span class="sxs-lookup"><span data-stu-id="64668-107">Forces the output to appear on the front of a media sheet.</span></span> <span data-ttu-id="64668-108">Relevante para folhas de mídia com superfícies diferentes em cada lado.</span><span class="sxs-lookup"><span data-stu-id="64668-108">Relevant to media sheets with different surfaces on each side.</span></span> <span data-ttu-id="64668-109">Nos casos em que esse recurso interfere nas opções de processamento (como DocumentDuplex), PageForceFrontSide tem precedência para a página específica à qual o recurso se aplica.</span><span class="sxs-lookup"><span data-stu-id="64668-109">In cases where this feature interferes with processing options (such as DocumentDuplex), PageForceFrontSide takes precedence for the specific page to which the feature applies.</span></span>

-   [<span data-ttu-id="64668-110">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="64668-110">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="64668-111">Conteúdo estrutural</span><span class="sxs-lookup"><span data-stu-id="64668-111">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="64668-112">Conteúdo de linguagem XML (XML)</span><span class="sxs-lookup"><span data-stu-id="64668-112">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="64668-113">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="64668-113">Element Information</span></span>



| <span data-ttu-id="64668-114">Nome</span><span class="sxs-lookup"><span data-stu-id="64668-114">Name</span></span> | <span data-ttu-id="64668-115">Valor</span><span class="sxs-lookup"><span data-stu-id="64668-115">Value</span></span> |
|----------------------------|--------------------|
| <span data-ttu-id="64668-116">Tipo de elemento</span><span class="sxs-lookup"><span data-stu-id="64668-116">Element Type</span></span> <br/>   | <span data-ttu-id="64668-117">Recurso</span><span class="sxs-lookup"><span data-stu-id="64668-117">Feature</span></span><br/> |
| <span data-ttu-id="64668-118">Prefixo de escopo</span><span class="sxs-lookup"><span data-stu-id="64668-118">Scoping Prefix</span></span> <br/> | <span data-ttu-id="64668-119">?</span><span class="sxs-lookup"><span data-stu-id="64668-119">Page</span></span><br/>    |
| <span data-ttu-id="64668-120">Observações</span><span class="sxs-lookup"><span data-stu-id="64668-120">Notes</span></span> <br/>          | <span data-ttu-id="64668-121">Nenhum</span><span class="sxs-lookup"><span data-stu-id="64668-121">None</span></span><br/>    |



 

## <a name="structural-content"></a><span data-ttu-id="64668-122">Conteúdo estrutural</span><span class="sxs-lookup"><span data-stu-id="64668-122">Structural Content</span></span>

<span data-ttu-id="64668-123">A estrutura XML desse elemento é:</span><span class="sxs-lookup"><span data-stu-id="64668-123">The XML structure of this element is:</span></span>

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

## <a name="structure-variables"></a><span data-ttu-id="64668-124">Variáveis de estrutura</span><span class="sxs-lookup"><span data-stu-id="64668-124">Structure Variables</span></span>

<span data-ttu-id="64668-125">A tabela a seguir descreve as características das variáveis definidas na estrutura XML.</span><span class="sxs-lookup"><span data-stu-id="64668-125">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="64668-126">Nome</span><span class="sxs-lookup"><span data-stu-id="64668-126">Name</span></span>                               | <span data-ttu-id="64668-127">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="64668-127">Data type</span></span>         | <span data-ttu-id="64668-128">Unidade</span><span class="sxs-lookup"><span data-stu-id="64668-128">Unit</span></span>                  | <span data-ttu-id="64668-129">Valores com suporte</span><span class="sxs-lookup"><span data-stu-id="64668-129">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="64668-130">Resumo</span><span class="sxs-lookup"><span data-stu-id="64668-130">Summary</span></span>                                                                      |
|------------------------------------|-------------------|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="64668-131">\_OptionName\_</span><span class="sxs-lookup"><span data-stu-id="64668-131">\_OptionName\_</span></span><br/>          | <span data-ttu-id="64668-132">string</span><span class="sxs-lookup"><span data-stu-id="64668-132">string</span></span><br/> | <span data-ttu-id="64668-133">characters</span><span class="sxs-lookup"><span data-stu-id="64668-133">characters</span></span><br/> | <span data-ttu-id="64668-134">Nome totalmente qualificado válido, conforme definido pelos [namespaces em XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span><span class="sxs-lookup"><span data-stu-id="64668-134">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="64668-135">Se nenhum namespace for especificado, o namespace padrão será assumido.</span><span class="sxs-lookup"><span data-stu-id="64668-135">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="64668-136">O nome da opção.</span><span class="sxs-lookup"><span data-stu-id="64668-136">The name of the option.</span></span><br/>                                           |
| <span data-ttu-id="64668-137">\_IdentityOptionValue\_</span><span class="sxs-lookup"><span data-stu-id="64668-137">\_IdentityOptionValue\_</span></span><br/> | <span data-ttu-id="64668-138">string</span><span class="sxs-lookup"><span data-stu-id="64668-138">string</span></span><br/> | <span data-ttu-id="64668-139">N/D</span><span class="sxs-lookup"><span data-stu-id="64668-139">n/a</span></span><br/>        | <span data-ttu-id="64668-140">True, False.</span><span class="sxs-lookup"><span data-stu-id="64668-140">True, False.</span></span><br/>                                                                                                                                                               | <span data-ttu-id="64668-141">Define uma opção que, quando selecionada, desabilita esse recurso.</span><span class="sxs-lookup"><span data-stu-id="64668-141">Defines an Option which when selected would disable this feature.</span></span><br/> |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="64668-142">Conteúdo de linguagem XML (XML)</span><span class="sxs-lookup"><span data-stu-id="64668-142">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="64668-143">As palavras-chave do esquema de impressão pública são definidas no https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span><span class="sxs-lookup"><span data-stu-id="64668-143">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="64668-144">O conteúdo do linguagem XML público (XML) para essa palavra-chave é definido abaixo:</span><span class="sxs-lookup"><span data-stu-id="64668-144">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

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

## <a name="related-topics"></a><span data-ttu-id="64668-145">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="64668-145">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="64668-146">Especificação de esquema de impressão</span><span class="sxs-lookup"><span data-stu-id="64668-146">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




