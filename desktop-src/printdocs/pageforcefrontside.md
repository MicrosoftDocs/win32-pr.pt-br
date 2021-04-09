---
description: Este tópico não é atual. Para obter as informações mais atuais, consulte a especificação do esquema de impressão.
ms.assetid: 0658c808-f050-41f3-90b6-2a013b616b58
title: PageForceFrontSide
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f277e357cf59bca455102f6ca29bd66bc09455ee
ms.sourcegitcommit: 7b8f6151ebe247536304866459b2973276271d4d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/06/2021
ms.locfileid: "104172592"
---
# <a name="pageforcefrontside"></a><span data-ttu-id="ba103-104">PageForceFrontSide</span><span class="sxs-lookup"><span data-stu-id="ba103-104">PageForceFrontSide</span></span>

<span data-ttu-id="ba103-105">Este tópico não é atual.</span><span class="sxs-lookup"><span data-stu-id="ba103-105">This topic is not current.</span></span> <span data-ttu-id="ba103-106">Para obter as informações mais atuais, consulte a [especificação do esquema de impressão](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="ba103-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="ba103-107">Força a saída a aparecer na frente de uma folha de mídia.</span><span class="sxs-lookup"><span data-stu-id="ba103-107">Forces the output to appear on the front of a media sheet.</span></span> <span data-ttu-id="ba103-108">Relevante para folhas de mídia com superfícies diferentes em cada lado.</span><span class="sxs-lookup"><span data-stu-id="ba103-108">Relevant to media sheets with different surfaces on each side.</span></span> <span data-ttu-id="ba103-109">Nos casos em que esse recurso interfere nas opções de processamento (como DocumentDuplex), PageForceFrontSide tem precedência para a página específica à qual o recurso se aplica.</span><span class="sxs-lookup"><span data-stu-id="ba103-109">In cases where this feature interferes with processing options (such as DocumentDuplex), PageForceFrontSide takes precedence for the specific page to which the feature applies.</span></span>

-   [<span data-ttu-id="ba103-110">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="ba103-110">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="ba103-111">Conteúdo estrutural</span><span class="sxs-lookup"><span data-stu-id="ba103-111">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="ba103-112">Conteúdo de linguagem XML (XML)</span><span class="sxs-lookup"><span data-stu-id="ba103-112">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="ba103-113">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="ba103-113">Element Information</span></span>



| <span data-ttu-id="ba103-114">Nome</span><span class="sxs-lookup"><span data-stu-id="ba103-114">Name</span></span>                       |                    |
|----------------------------|--------------------|
| <span data-ttu-id="ba103-115">Tipo de elemento</span><span class="sxs-lookup"><span data-stu-id="ba103-115">Element Type</span></span> <br/>   | <span data-ttu-id="ba103-116">Recurso</span><span class="sxs-lookup"><span data-stu-id="ba103-116">Feature</span></span><br/> |
| <span data-ttu-id="ba103-117">Prefixo de escopo</span><span class="sxs-lookup"><span data-stu-id="ba103-117">Scoping Prefix</span></span> <br/> | <span data-ttu-id="ba103-118">?</span><span class="sxs-lookup"><span data-stu-id="ba103-118">Page</span></span><br/>    |
| <span data-ttu-id="ba103-119">Observações</span><span class="sxs-lookup"><span data-stu-id="ba103-119">Notes</span></span> <br/>          | <span data-ttu-id="ba103-120">Nenhum</span><span class="sxs-lookup"><span data-stu-id="ba103-120">None</span></span><br/>    |



 

## <a name="structural-content"></a><span data-ttu-id="ba103-121">Conteúdo estrutural</span><span class="sxs-lookup"><span data-stu-id="ba103-121">Structural Content</span></span>

<span data-ttu-id="ba103-122">A estrutura XML desse elemento é:</span><span class="sxs-lookup"><span data-stu-id="ba103-122">The XML structure of this element is:</span></span>

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

## <a name="structure-variables"></a><span data-ttu-id="ba103-123">Variáveis de estrutura</span><span class="sxs-lookup"><span data-stu-id="ba103-123">Structure Variables</span></span>

<span data-ttu-id="ba103-124">A tabela a seguir descreve as características das variáveis definidas na estrutura XML.</span><span class="sxs-lookup"><span data-stu-id="ba103-124">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="ba103-125">Nome</span><span class="sxs-lookup"><span data-stu-id="ba103-125">Name</span></span>                               | <span data-ttu-id="ba103-126">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="ba103-126">Data type</span></span>         | <span data-ttu-id="ba103-127">Unidade</span><span class="sxs-lookup"><span data-stu-id="ba103-127">Unit</span></span>                  | <span data-ttu-id="ba103-128">Valores com suporte</span><span class="sxs-lookup"><span data-stu-id="ba103-128">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="ba103-129">Resumo</span><span class="sxs-lookup"><span data-stu-id="ba103-129">Summary</span></span>                                                                      |
|------------------------------------|-------------------|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="ba103-130">\_OptionName\_</span><span class="sxs-lookup"><span data-stu-id="ba103-130">\_OptionName\_</span></span><br/>          | <span data-ttu-id="ba103-131">string</span><span class="sxs-lookup"><span data-stu-id="ba103-131">string</span></span><br/> | <span data-ttu-id="ba103-132">characters</span><span class="sxs-lookup"><span data-stu-id="ba103-132">characters</span></span><br/> | <span data-ttu-id="ba103-133">Nome totalmente qualificado válido, conforme definido pelos [namespaces em XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span><span class="sxs-lookup"><span data-stu-id="ba103-133">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="ba103-134">Se nenhum namespace for especificado, o namespace padrão será assumido.</span><span class="sxs-lookup"><span data-stu-id="ba103-134">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="ba103-135">O nome da opção.</span><span class="sxs-lookup"><span data-stu-id="ba103-135">The name of the option.</span></span><br/>                                           |
| <span data-ttu-id="ba103-136">\_IdentityOptionValue\_</span><span class="sxs-lookup"><span data-stu-id="ba103-136">\_IdentityOptionValue\_</span></span><br/> | <span data-ttu-id="ba103-137">string</span><span class="sxs-lookup"><span data-stu-id="ba103-137">string</span></span><br/> | <span data-ttu-id="ba103-138">N/D</span><span class="sxs-lookup"><span data-stu-id="ba103-138">n/a</span></span><br/>        | <span data-ttu-id="ba103-139">True, False.</span><span class="sxs-lookup"><span data-stu-id="ba103-139">True, False.</span></span><br/>                                                                                                                                                               | <span data-ttu-id="ba103-140">Define uma opção que, quando selecionada, desabilita esse recurso.</span><span class="sxs-lookup"><span data-stu-id="ba103-140">Defines an Option which when selected would disable this feature.</span></span><br/> |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="ba103-141">Conteúdo de linguagem XML (XML)</span><span class="sxs-lookup"><span data-stu-id="ba103-141">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="ba103-142">As palavras-chave do esquema de impressão pública são definidas no https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span><span class="sxs-lookup"><span data-stu-id="ba103-142">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="ba103-143">O conteúdo do linguagem XML público (XML) para essa palavra-chave é definido abaixo:</span><span class="sxs-lookup"><span data-stu-id="ba103-143">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

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

## <a name="related-topics"></a><span data-ttu-id="ba103-144">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="ba103-144">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ba103-145">Especificação de esquema de impressão</span><span class="sxs-lookup"><span data-stu-id="ba103-145">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




