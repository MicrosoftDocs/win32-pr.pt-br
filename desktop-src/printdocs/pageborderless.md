---
description: Este tópico não é atual. Para obter as informações mais atuais, consulte a especificação do esquema de impressão.
ms.assetid: c5e75f57-7426-41fa-88f4-789153fcd0c5
title: PageBorderless
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b20eb3379c76bfef3cd7ce6bb75dcf71479f0449
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/26/2021
ms.locfileid: "107997683"
---
# <a name="pageborderless"></a><span data-ttu-id="19a2a-104">PageBorderless</span><span class="sxs-lookup"><span data-stu-id="19a2a-104">PageBorderless</span></span>

<span data-ttu-id="19a2a-105">Este tópico não é atual.</span><span class="sxs-lookup"><span data-stu-id="19a2a-105">This topic is not current.</span></span> <span data-ttu-id="19a2a-106">Para obter as informações mais atuais, consulte a [especificação do esquema de impressão](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="19a2a-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="19a2a-107">Descreve quando o conteúdo da imagem deve ser impresso nas bordas físicas da mídia.</span><span class="sxs-lookup"><span data-stu-id="19a2a-107">Describes when image content should be printed to the physical edges of the media.</span></span>

-   [<span data-ttu-id="19a2a-108">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="19a2a-108">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="19a2a-109">Conteúdo estrutural</span><span class="sxs-lookup"><span data-stu-id="19a2a-109">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="19a2a-110">Conteúdo de linguagem XML (XML)</span><span class="sxs-lookup"><span data-stu-id="19a2a-110">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="19a2a-111">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="19a2a-111">Element Information</span></span>



| <span data-ttu-id="19a2a-112">Nome</span><span class="sxs-lookup"><span data-stu-id="19a2a-112">Name</span></span> | <span data-ttu-id="19a2a-113">Valor</span><span class="sxs-lookup"><span data-stu-id="19a2a-113">Value</span></span> |
|----------------------------|--------------------|
| <span data-ttu-id="19a2a-114">Tipo de elemento</span><span class="sxs-lookup"><span data-stu-id="19a2a-114">Element Type</span></span> <br/>   | <span data-ttu-id="19a2a-115">Recurso</span><span class="sxs-lookup"><span data-stu-id="19a2a-115">Feature</span></span><br/> |
| <span data-ttu-id="19a2a-116">Prefixo de escopo</span><span class="sxs-lookup"><span data-stu-id="19a2a-116">Scoping Prefix</span></span> <br/> | <span data-ttu-id="19a2a-117">?</span><span class="sxs-lookup"><span data-stu-id="19a2a-117">Page</span></span><br/>    |
| <span data-ttu-id="19a2a-118">Observações</span><span class="sxs-lookup"><span data-stu-id="19a2a-118">Notes</span></span> <br/>          | <span data-ttu-id="19a2a-119">Nenhum</span><span class="sxs-lookup"><span data-stu-id="19a2a-119">None</span></span><br/>    |



 

## <a name="structural-content"></a><span data-ttu-id="19a2a-120">Conteúdo estrutural</span><span class="sxs-lookup"><span data-stu-id="19a2a-120">Structural Content</span></span>

<span data-ttu-id="19a2a-121">A estrutura XML desse elemento é:</span><span class="sxs-lookup"><span data-stu-id="19a2a-121">The XML structure of this element is:</span></span>

``` syntax
<psf:Feature name="psk:PageBorderless">
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

## <a name="structure-variables"></a><span data-ttu-id="19a2a-122">Variáveis de estrutura</span><span class="sxs-lookup"><span data-stu-id="19a2a-122">Structure Variables</span></span>

<span data-ttu-id="19a2a-123">A tabela a seguir descreve as características das variáveis definidas na estrutura XML.</span><span class="sxs-lookup"><span data-stu-id="19a2a-123">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="19a2a-124">Nome</span><span class="sxs-lookup"><span data-stu-id="19a2a-124">Name</span></span>                               | <span data-ttu-id="19a2a-125">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="19a2a-125">Data type</span></span>         | <span data-ttu-id="19a2a-126">Unidade</span><span class="sxs-lookup"><span data-stu-id="19a2a-126">Unit</span></span>                  | <span data-ttu-id="19a2a-127">Valores com suporte</span><span class="sxs-lookup"><span data-stu-id="19a2a-127">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="19a2a-128">Resumo</span><span class="sxs-lookup"><span data-stu-id="19a2a-128">Summary</span></span>                                                                      |
|------------------------------------|-------------------|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="19a2a-129">\_OptionName\_</span><span class="sxs-lookup"><span data-stu-id="19a2a-129">\_OptionName\_</span></span><br/>          | <span data-ttu-id="19a2a-130">string</span><span class="sxs-lookup"><span data-stu-id="19a2a-130">string</span></span><br/> | <span data-ttu-id="19a2a-131">characters</span><span class="sxs-lookup"><span data-stu-id="19a2a-131">characters</span></span><br/> | <span data-ttu-id="19a2a-132">Nome totalmente qualificado válido, conforme definido pelos [namespaces em XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span><span class="sxs-lookup"><span data-stu-id="19a2a-132">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="19a2a-133">Se nenhum namespace for especificado, o namespace padrão será assumido.</span><span class="sxs-lookup"><span data-stu-id="19a2a-133">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="19a2a-134">O nome da opção.</span><span class="sxs-lookup"><span data-stu-id="19a2a-134">The name of the option.</span></span><br/>                                           |
| <span data-ttu-id="19a2a-135">\_IdentityOptionValue\_</span><span class="sxs-lookup"><span data-stu-id="19a2a-135">\_IdentityOptionValue\_</span></span><br/> | <span data-ttu-id="19a2a-136">string</span><span class="sxs-lookup"><span data-stu-id="19a2a-136">string</span></span><br/> | <span data-ttu-id="19a2a-137">N/D</span><span class="sxs-lookup"><span data-stu-id="19a2a-137">n/a</span></span><br/>        | <span data-ttu-id="19a2a-138">True, False.</span><span class="sxs-lookup"><span data-stu-id="19a2a-138">True, False.</span></span><br/>                                                                                                                                                               | <span data-ttu-id="19a2a-139">Define uma opção que, quando selecionada, desabilita esse recurso.</span><span class="sxs-lookup"><span data-stu-id="19a2a-139">Defines an Option which when selected would disable this feature.</span></span><br/> |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="19a2a-140">Conteúdo de linguagem XML (XML)</span><span class="sxs-lookup"><span data-stu-id="19a2a-140">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="19a2a-141">As palavras-chave do esquema de impressão pública são definidas no https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span><span class="sxs-lookup"><span data-stu-id="19a2a-141">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="19a2a-142">O conteúdo do linguagem XML público (XML) para essa palavra-chave é definido abaixo:</span><span class="sxs-lookup"><span data-stu-id="19a2a-142">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

``` syntax
<psf:Feature name="psk:PageBorderless">
  <psf:Property name="psf:SelectionType">
    <psf:Value xsi:type="xs:string">psk:PickOne</psf:Value>
  </psf:Property>
  <!-- Specifies borderless printing. -->
  <psf:Option name="psk:Borderless" />
  <!-- Specifies no borderless printing. -->
  <psf:Option name="psk:None" />
</psf:Feature>
```

## <a name="related-topics"></a><span data-ttu-id="19a2a-143">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="19a2a-143">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="19a2a-144">Especificação de esquema de impressão</span><span class="sxs-lookup"><span data-stu-id="19a2a-144">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




