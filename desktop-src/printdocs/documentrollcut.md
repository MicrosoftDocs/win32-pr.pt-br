---
description: Saiba mais sobre o elemento DocumentRollCut, que descreve o método de recorte para o rolo de papel. Cada documento é tratado separadamente.
ms.assetid: 8eb4e574-3209-459c-9a25-95377b2f7439
title: DocumentRollCut
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 92f7232cbe9dafce25aa2ee482ca40bf99145841
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/19/2021
ms.locfileid: "112409179"
---
# <a name="documentrollcut"></a><span data-ttu-id="c111c-104">DocumentRollCut</span><span class="sxs-lookup"><span data-stu-id="c111c-104">DocumentRollCut</span></span>

<span data-ttu-id="c111c-105">Este tópico não é atual.</span><span class="sxs-lookup"><span data-stu-id="c111c-105">This topic is not current.</span></span> <span data-ttu-id="c111c-106">Para obter as informações mais atuais, consulte a [especificação do esquema de impressão](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="c111c-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="c111c-107">Descreve o método de recorte para o rolo de papel.</span><span class="sxs-lookup"><span data-stu-id="c111c-107">Describes the cutting method for roll paper.</span></span> <span data-ttu-id="c111c-108">Cada documento é tratado separadamente.</span><span class="sxs-lookup"><span data-stu-id="c111c-108">Each document is handled separately.</span></span> <span data-ttu-id="c111c-109">As opções especificadas descrevem os diferentes métodos para roll-Cut.</span><span class="sxs-lookup"><span data-stu-id="c111c-109">The specified options describe the different methods for roll cut.</span></span>

-   [<span data-ttu-id="c111c-110">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="c111c-110">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="c111c-111">Conteúdo estrutural</span><span class="sxs-lookup"><span data-stu-id="c111c-111">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="c111c-112">Conteúdo de linguagem XML (XML)</span><span class="sxs-lookup"><span data-stu-id="c111c-112">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="c111c-113">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="c111c-113">Element Information</span></span>



| <span data-ttu-id="c111c-114">Name</span><span class="sxs-lookup"><span data-stu-id="c111c-114">Name</span></span> | <span data-ttu-id="c111c-115">Valor</span><span class="sxs-lookup"><span data-stu-id="c111c-115">Value</span></span> |
|----------------------------|---------------------|
| <span data-ttu-id="c111c-116">Tipo de elemento</span><span class="sxs-lookup"><span data-stu-id="c111c-116">Element Type</span></span> <br/>   | <span data-ttu-id="c111c-117">Recurso</span><span class="sxs-lookup"><span data-stu-id="c111c-117">Feature</span></span><br/>  |
| <span data-ttu-id="c111c-118">Prefixo de escopo</span><span class="sxs-lookup"><span data-stu-id="c111c-118">Scoping Prefix</span></span> <br/> | <span data-ttu-id="c111c-119">Documento</span><span class="sxs-lookup"><span data-stu-id="c111c-119">Document</span></span><br/> |
| <span data-ttu-id="c111c-120">Observações</span><span class="sxs-lookup"><span data-stu-id="c111c-120">Notes</span></span> <br/>          | <span data-ttu-id="c111c-121">Nenhum</span><span class="sxs-lookup"><span data-stu-id="c111c-121">None</span></span><br/>     |



 

## <a name="structural-content"></a><span data-ttu-id="c111c-122">Conteúdo estrutural</span><span class="sxs-lookup"><span data-stu-id="c111c-122">Structural Content</span></span>

<span data-ttu-id="c111c-123">A estrutura XML desse elemento é:</span><span class="sxs-lookup"><span data-stu-id="c111c-123">The XML structure of this element is:</span></span>

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

## <a name="structure-variables"></a><span data-ttu-id="c111c-124">Variáveis de estrutura</span><span class="sxs-lookup"><span data-stu-id="c111c-124">Structure Variables</span></span>

<span data-ttu-id="c111c-125">A tabela a seguir descreve as características das variáveis definidas na estrutura XML.</span><span class="sxs-lookup"><span data-stu-id="c111c-125">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="c111c-126">Nome</span><span class="sxs-lookup"><span data-stu-id="c111c-126">Name</span></span>                               | <span data-ttu-id="c111c-127">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="c111c-127">Data type</span></span>         | <span data-ttu-id="c111c-128">Unidade</span><span class="sxs-lookup"><span data-stu-id="c111c-128">Unit</span></span>                  | <span data-ttu-id="c111c-129">Valores com suporte</span><span class="sxs-lookup"><span data-stu-id="c111c-129">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="c111c-130">Resumo</span><span class="sxs-lookup"><span data-stu-id="c111c-130">Summary</span></span>                                                                      |
|------------------------------------|-------------------|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="c111c-131">\_OptionName\_</span><span class="sxs-lookup"><span data-stu-id="c111c-131">\_OptionName\_</span></span><br/>          | <span data-ttu-id="c111c-132">string</span><span class="sxs-lookup"><span data-stu-id="c111c-132">string</span></span><br/> | <span data-ttu-id="c111c-133">characters</span><span class="sxs-lookup"><span data-stu-id="c111c-133">characters</span></span><br/> | <span data-ttu-id="c111c-134">Nome totalmente qualificado válido, conforme definido pelos [namespaces em XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span><span class="sxs-lookup"><span data-stu-id="c111c-134">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="c111c-135">Se nenhum namespace for especificado, o namespace padrão será assumido.</span><span class="sxs-lookup"><span data-stu-id="c111c-135">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="c111c-136">O nome da opção.</span><span class="sxs-lookup"><span data-stu-id="c111c-136">The name of the option.</span></span><br/>                                           |
| <span data-ttu-id="c111c-137">\_IdentityOptionValue\_</span><span class="sxs-lookup"><span data-stu-id="c111c-137">\_IdentityOptionValue\_</span></span><br/> | <span data-ttu-id="c111c-138">string</span><span class="sxs-lookup"><span data-stu-id="c111c-138">string</span></span><br/> | <span data-ttu-id="c111c-139">n/d</span><span class="sxs-lookup"><span data-stu-id="c111c-139">n/a</span></span><br/>        | <span data-ttu-id="c111c-140">True, False.</span><span class="sxs-lookup"><span data-stu-id="c111c-140">True, False.</span></span><br/>                                                                                                                                                               | <span data-ttu-id="c111c-141">Define uma opção que, quando selecionada, desabilita esse recurso.</span><span class="sxs-lookup"><span data-stu-id="c111c-141">Defines an Option which when selected would disable this feature.</span></span><br/> |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="c111c-142">Conteúdo de linguagem XML (XML)</span><span class="sxs-lookup"><span data-stu-id="c111c-142">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="c111c-143">As palavras-chave do esquema de impressão pública são definidas no https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span><span class="sxs-lookup"><span data-stu-id="c111c-143">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="c111c-144">O conteúdo do linguagem XML público (XML) para essa palavra-chave é definido abaixo:</span><span class="sxs-lookup"><span data-stu-id="c111c-144">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

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

## <a name="related-topics"></a><span data-ttu-id="c111c-145">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="c111c-145">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c111c-146">Especificação de esquema de impressão</span><span class="sxs-lookup"><span data-stu-id="c111c-146">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




