---
description: Este tópico não é atual. Para obter as informações mais atuais, consulte a especificação do esquema de impressão.
ms.assetid: 8eb4e574-3209-459c-9a25-95377b2f7439
title: DocumentRollCut
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1d3a20c02c50638d532660845efc1b3894f4a7e1
ms.sourcegitcommit: 7b8f6151ebe247536304866459b2973276271d4d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/06/2021
ms.locfileid: "104172588"
---
# <a name="documentrollcut"></a><span data-ttu-id="8c72f-104">DocumentRollCut</span><span class="sxs-lookup"><span data-stu-id="8c72f-104">DocumentRollCut</span></span>

<span data-ttu-id="8c72f-105">Este tópico não é atual.</span><span class="sxs-lookup"><span data-stu-id="8c72f-105">This topic is not current.</span></span> <span data-ttu-id="8c72f-106">Para obter as informações mais atuais, consulte a [especificação do esquema de impressão](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="8c72f-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="8c72f-107">Descreve o método de recorte para o rolo de papel.</span><span class="sxs-lookup"><span data-stu-id="8c72f-107">Describes the cutting method for roll paper.</span></span> <span data-ttu-id="8c72f-108">Cada documento é tratado separadamente.</span><span class="sxs-lookup"><span data-stu-id="8c72f-108">Each document is handled separately.</span></span> <span data-ttu-id="8c72f-109">As opções especificadas descrevem os diferentes métodos para roll-Cut.</span><span class="sxs-lookup"><span data-stu-id="8c72f-109">The specified options describe the different methods for roll cut.</span></span>

-   [<span data-ttu-id="8c72f-110">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="8c72f-110">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="8c72f-111">Conteúdo estrutural</span><span class="sxs-lookup"><span data-stu-id="8c72f-111">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="8c72f-112">Conteúdo de linguagem XML (XML)</span><span class="sxs-lookup"><span data-stu-id="8c72f-112">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="8c72f-113">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="8c72f-113">Element Information</span></span>



| <span data-ttu-id="8c72f-114">Nome</span><span class="sxs-lookup"><span data-stu-id="8c72f-114">Name</span></span>                       |                     |
|----------------------------|---------------------|
| <span data-ttu-id="8c72f-115">Tipo de elemento</span><span class="sxs-lookup"><span data-stu-id="8c72f-115">Element Type</span></span> <br/>   | <span data-ttu-id="8c72f-116">Recurso</span><span class="sxs-lookup"><span data-stu-id="8c72f-116">Feature</span></span><br/>  |
| <span data-ttu-id="8c72f-117">Prefixo de escopo</span><span class="sxs-lookup"><span data-stu-id="8c72f-117">Scoping Prefix</span></span> <br/> | <span data-ttu-id="8c72f-118">Documento</span><span class="sxs-lookup"><span data-stu-id="8c72f-118">Document</span></span><br/> |
| <span data-ttu-id="8c72f-119">Observações</span><span class="sxs-lookup"><span data-stu-id="8c72f-119">Notes</span></span> <br/>          | <span data-ttu-id="8c72f-120">Nenhum</span><span class="sxs-lookup"><span data-stu-id="8c72f-120">None</span></span><br/>     |



 

## <a name="structural-content"></a><span data-ttu-id="8c72f-121">Conteúdo estrutural</span><span class="sxs-lookup"><span data-stu-id="8c72f-121">Structural Content</span></span>

<span data-ttu-id="8c72f-122">A estrutura XML desse elemento é:</span><span class="sxs-lookup"><span data-stu-id="8c72f-122">The XML structure of this element is:</span></span>

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

## <a name="structure-variables"></a><span data-ttu-id="8c72f-123">Variáveis de estrutura</span><span class="sxs-lookup"><span data-stu-id="8c72f-123">Structure Variables</span></span>

<span data-ttu-id="8c72f-124">A tabela a seguir descreve as características das variáveis definidas na estrutura XML.</span><span class="sxs-lookup"><span data-stu-id="8c72f-124">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="8c72f-125">Nome</span><span class="sxs-lookup"><span data-stu-id="8c72f-125">Name</span></span>                               | <span data-ttu-id="8c72f-126">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="8c72f-126">Data type</span></span>         | <span data-ttu-id="8c72f-127">Unidade</span><span class="sxs-lookup"><span data-stu-id="8c72f-127">Unit</span></span>                  | <span data-ttu-id="8c72f-128">Valores com suporte</span><span class="sxs-lookup"><span data-stu-id="8c72f-128">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="8c72f-129">Resumo</span><span class="sxs-lookup"><span data-stu-id="8c72f-129">Summary</span></span>                                                                      |
|------------------------------------|-------------------|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="8c72f-130">\_OptionName\_</span><span class="sxs-lookup"><span data-stu-id="8c72f-130">\_OptionName\_</span></span><br/>          | <span data-ttu-id="8c72f-131">string</span><span class="sxs-lookup"><span data-stu-id="8c72f-131">string</span></span><br/> | <span data-ttu-id="8c72f-132">characters</span><span class="sxs-lookup"><span data-stu-id="8c72f-132">characters</span></span><br/> | <span data-ttu-id="8c72f-133">Nome totalmente qualificado válido, conforme definido pelos [namespaces em XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span><span class="sxs-lookup"><span data-stu-id="8c72f-133">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="8c72f-134">Se nenhum namespace for especificado, o namespace padrão será assumido.</span><span class="sxs-lookup"><span data-stu-id="8c72f-134">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="8c72f-135">O nome da opção.</span><span class="sxs-lookup"><span data-stu-id="8c72f-135">The name of the option.</span></span><br/>                                           |
| <span data-ttu-id="8c72f-136">\_IdentityOptionValue\_</span><span class="sxs-lookup"><span data-stu-id="8c72f-136">\_IdentityOptionValue\_</span></span><br/> | <span data-ttu-id="8c72f-137">string</span><span class="sxs-lookup"><span data-stu-id="8c72f-137">string</span></span><br/> | <span data-ttu-id="8c72f-138">N/D</span><span class="sxs-lookup"><span data-stu-id="8c72f-138">n/a</span></span><br/>        | <span data-ttu-id="8c72f-139">True, False.</span><span class="sxs-lookup"><span data-stu-id="8c72f-139">True, False.</span></span><br/>                                                                                                                                                               | <span data-ttu-id="8c72f-140">Define uma opção que, quando selecionada, desabilita esse recurso.</span><span class="sxs-lookup"><span data-stu-id="8c72f-140">Defines an Option which when selected would disable this feature.</span></span><br/> |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="8c72f-141">Conteúdo de linguagem XML (XML)</span><span class="sxs-lookup"><span data-stu-id="8c72f-141">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="8c72f-142">As palavras-chave do esquema de impressão pública são definidas no https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span><span class="sxs-lookup"><span data-stu-id="8c72f-142">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="8c72f-143">O conteúdo do linguagem XML público (XML) para essa palavra-chave é definido abaixo:</span><span class="sxs-lookup"><span data-stu-id="8c72f-143">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

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

## <a name="related-topics"></a><span data-ttu-id="8c72f-144">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="8c72f-144">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8c72f-145">Especificação de esquema de impressão</span><span class="sxs-lookup"><span data-stu-id="8c72f-145">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




