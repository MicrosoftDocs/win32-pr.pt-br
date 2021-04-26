---
description: Este tópico não é atual. Para obter as informações mais atuais, consulte a especificação do esquema de impressão.
ms.assetid: 8eb4e574-3209-459c-9a25-95377b2f7439
title: DocumentRollCut
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d3d4bfb09a1c3f6f43f11886685a0edfcf2bbd92
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/26/2021
ms.locfileid: "107997043"
---
# <a name="documentrollcut"></a><span data-ttu-id="3c8e8-104">DocumentRollCut</span><span class="sxs-lookup"><span data-stu-id="3c8e8-104">DocumentRollCut</span></span>

<span data-ttu-id="3c8e8-105">Este tópico não é atual.</span><span class="sxs-lookup"><span data-stu-id="3c8e8-105">This topic is not current.</span></span> <span data-ttu-id="3c8e8-106">Para obter as informações mais atuais, consulte a [especificação do esquema de impressão](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="3c8e8-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="3c8e8-107">Descreve o método de recorte para o rolo de papel.</span><span class="sxs-lookup"><span data-stu-id="3c8e8-107">Describes the cutting method for roll paper.</span></span> <span data-ttu-id="3c8e8-108">Cada documento é tratado separadamente.</span><span class="sxs-lookup"><span data-stu-id="3c8e8-108">Each document is handled separately.</span></span> <span data-ttu-id="3c8e8-109">As opções especificadas descrevem os diferentes métodos para roll-Cut.</span><span class="sxs-lookup"><span data-stu-id="3c8e8-109">The specified options describe the different methods for roll cut.</span></span>

-   [<span data-ttu-id="3c8e8-110">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="3c8e8-110">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="3c8e8-111">Conteúdo estrutural</span><span class="sxs-lookup"><span data-stu-id="3c8e8-111">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="3c8e8-112">Conteúdo de linguagem XML (XML)</span><span class="sxs-lookup"><span data-stu-id="3c8e8-112">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="3c8e8-113">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="3c8e8-113">Element Information</span></span>



| <span data-ttu-id="3c8e8-114">Nome</span><span class="sxs-lookup"><span data-stu-id="3c8e8-114">Name</span></span> | <span data-ttu-id="3c8e8-115">Valor</span><span class="sxs-lookup"><span data-stu-id="3c8e8-115">Value</span></span> |
|----------------------------|---------------------|
| <span data-ttu-id="3c8e8-116">Tipo de elemento</span><span class="sxs-lookup"><span data-stu-id="3c8e8-116">Element Type</span></span> <br/>   | <span data-ttu-id="3c8e8-117">Recurso</span><span class="sxs-lookup"><span data-stu-id="3c8e8-117">Feature</span></span><br/>  |
| <span data-ttu-id="3c8e8-118">Prefixo de escopo</span><span class="sxs-lookup"><span data-stu-id="3c8e8-118">Scoping Prefix</span></span> <br/> | <span data-ttu-id="3c8e8-119">Documento</span><span class="sxs-lookup"><span data-stu-id="3c8e8-119">Document</span></span><br/> |
| <span data-ttu-id="3c8e8-120">Observações</span><span class="sxs-lookup"><span data-stu-id="3c8e8-120">Notes</span></span> <br/>          | <span data-ttu-id="3c8e8-121">Nenhum</span><span class="sxs-lookup"><span data-stu-id="3c8e8-121">None</span></span><br/>     |



 

## <a name="structural-content"></a><span data-ttu-id="3c8e8-122">Conteúdo estrutural</span><span class="sxs-lookup"><span data-stu-id="3c8e8-122">Structural Content</span></span>

<span data-ttu-id="3c8e8-123">A estrutura XML desse elemento é:</span><span class="sxs-lookup"><span data-stu-id="3c8e8-123">The XML structure of this element is:</span></span>

``` syntax
<psf:Feature name="psk:DocumentRollCut">
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

## <a name="structure-variables"></a><span data-ttu-id="3c8e8-124">Variáveis de estrutura</span><span class="sxs-lookup"><span data-stu-id="3c8e8-124">Structure Variables</span></span>

<span data-ttu-id="3c8e8-125">A tabela a seguir descreve as características das variáveis definidas na estrutura XML.</span><span class="sxs-lookup"><span data-stu-id="3c8e8-125">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="3c8e8-126">Nome</span><span class="sxs-lookup"><span data-stu-id="3c8e8-126">Name</span></span>                               | <span data-ttu-id="3c8e8-127">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="3c8e8-127">Data type</span></span>         | <span data-ttu-id="3c8e8-128">Unidade</span><span class="sxs-lookup"><span data-stu-id="3c8e8-128">Unit</span></span>                  | <span data-ttu-id="3c8e8-129">Valores com suporte</span><span class="sxs-lookup"><span data-stu-id="3c8e8-129">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="3c8e8-130">Resumo</span><span class="sxs-lookup"><span data-stu-id="3c8e8-130">Summary</span></span>                                                                      |
|------------------------------------|-------------------|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="3c8e8-131">\_OptionName\_</span><span class="sxs-lookup"><span data-stu-id="3c8e8-131">\_OptionName\_</span></span><br/>          | <span data-ttu-id="3c8e8-132">string</span><span class="sxs-lookup"><span data-stu-id="3c8e8-132">string</span></span><br/> | <span data-ttu-id="3c8e8-133">characters</span><span class="sxs-lookup"><span data-stu-id="3c8e8-133">characters</span></span><br/> | <span data-ttu-id="3c8e8-134">Nome totalmente qualificado válido, conforme definido pelos [namespaces em XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span><span class="sxs-lookup"><span data-stu-id="3c8e8-134">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="3c8e8-135">Se nenhum namespace for especificado, o namespace padrão será assumido.</span><span class="sxs-lookup"><span data-stu-id="3c8e8-135">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="3c8e8-136">O nome da opção.</span><span class="sxs-lookup"><span data-stu-id="3c8e8-136">The name of the option.</span></span><br/>                                           |
| <span data-ttu-id="3c8e8-137">\_IdentityOptionValue\_</span><span class="sxs-lookup"><span data-stu-id="3c8e8-137">\_IdentityOptionValue\_</span></span><br/> | <span data-ttu-id="3c8e8-138">string</span><span class="sxs-lookup"><span data-stu-id="3c8e8-138">string</span></span><br/> | <span data-ttu-id="3c8e8-139">N/D</span><span class="sxs-lookup"><span data-stu-id="3c8e8-139">n/a</span></span><br/>        | <span data-ttu-id="3c8e8-140">True, False.</span><span class="sxs-lookup"><span data-stu-id="3c8e8-140">True, False.</span></span><br/>                                                                                                                                                               | <span data-ttu-id="3c8e8-141">Define uma opção que, quando selecionada, desabilita esse recurso.</span><span class="sxs-lookup"><span data-stu-id="3c8e8-141">Defines an Option which when selected would disable this feature.</span></span><br/> |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="3c8e8-142">Conteúdo de linguagem XML (XML)</span><span class="sxs-lookup"><span data-stu-id="3c8e8-142">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="3c8e8-143">As palavras-chave do esquema de impressão pública são definidas no https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span><span class="sxs-lookup"><span data-stu-id="3c8e8-143">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="3c8e8-144">O conteúdo do linguagem XML público (XML) para essa palavra-chave é definido abaixo:</span><span class="sxs-lookup"><span data-stu-id="3c8e8-144">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

``` syntax
<psf:Feature name="psk:DocumentRollCut">
  <psf:Property name="psf:SelectionType">
    <psf:Value xsi:type="xs:string">psk:PickOne</psf:Value>
  </psf:Property>
  <!-- Specifies cutting method for banner -->
  <psf:Option name="psk:Banner" />
  <!-- Specifies cutting at the edge of the image --> 
  <psf:Option name="psk:CutSheetAtImageEdge" />
  <!-- Specifies cutting for media size selected for PageMediaSize -->
  <psf:Option name="psk:CutSheetAtStandardMediaSize" />
  <!-- Specifies no document roll cut -->
  <psf:Option name="psk:None" />
</psf:Feature>
    
```

## <a name="related-topics"></a><span data-ttu-id="3c8e8-145">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="3c8e8-145">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3c8e8-146">Especificação de esquema de impressão</span><span class="sxs-lookup"><span data-stu-id="3c8e8-146">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




