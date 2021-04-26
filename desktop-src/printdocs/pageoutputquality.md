---
description: Este tópico não é atual. Para obter as informações mais atuais, consulte a especificação do esquema de impressão.
ms.assetid: 4720f812-a71a-458f-85fa-7885cca0dbbb
title: PageOutputQuality
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2c63238c290d6b8f0bb208e94e52dc66c8d2e6be
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/26/2021
ms.locfileid: "107994473"
---
# <a name="pageoutputquality"></a><span data-ttu-id="c9695-104">PageOutputQuality</span><span class="sxs-lookup"><span data-stu-id="c9695-104">PageOutputQuality</span></span>

<span data-ttu-id="c9695-105">Este tópico não é atual.</span><span class="sxs-lookup"><span data-stu-id="c9695-105">This topic is not current.</span></span> <span data-ttu-id="c9695-106">Para obter as informações mais atuais, consulte a [especificação do esquema de impressão](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="c9695-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="c9695-107">Descreve o nível de qualidade da saída.</span><span class="sxs-lookup"><span data-stu-id="c9695-107">Describes the quality level of the output.</span></span>

-   [<span data-ttu-id="c9695-108">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="c9695-108">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="c9695-109">Conteúdo estrutural</span><span class="sxs-lookup"><span data-stu-id="c9695-109">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="c9695-110">Conteúdo de linguagem XML (XML)</span><span class="sxs-lookup"><span data-stu-id="c9695-110">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="c9695-111">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="c9695-111">Element Information</span></span>



| <span data-ttu-id="c9695-112">Nome</span><span class="sxs-lookup"><span data-stu-id="c9695-112">Name</span></span> | <span data-ttu-id="c9695-113">Valor</span><span class="sxs-lookup"><span data-stu-id="c9695-113">Value</span></span> |
|----------------------------|--------------------|
| <span data-ttu-id="c9695-114">Tipo de elemento</span><span class="sxs-lookup"><span data-stu-id="c9695-114">Element Type</span></span> <br/>   | <span data-ttu-id="c9695-115">Recurso</span><span class="sxs-lookup"><span data-stu-id="c9695-115">Feature</span></span><br/> |
| <span data-ttu-id="c9695-116">Prefixo de escopo</span><span class="sxs-lookup"><span data-stu-id="c9695-116">Scoping Prefix</span></span> <br/> | <span data-ttu-id="c9695-117">?</span><span class="sxs-lookup"><span data-stu-id="c9695-117">Page</span></span><br/>    |
| <span data-ttu-id="c9695-118">Observações</span><span class="sxs-lookup"><span data-stu-id="c9695-118">Notes</span></span> <br/>          | <span data-ttu-id="c9695-119">Nenhum</span><span class="sxs-lookup"><span data-stu-id="c9695-119">None</span></span><br/>    |



 

## <a name="structural-content"></a><span data-ttu-id="c9695-120">Conteúdo estrutural</span><span class="sxs-lookup"><span data-stu-id="c9695-120">Structural Content</span></span>

<span data-ttu-id="c9695-121">A estrutura XML desse elemento é:</span><span class="sxs-lookup"><span data-stu-id="c9695-121">The XML structure of this element is:</span></span>

``` syntax
<psf:Feature name="psk:PageOutputQuality">
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

## <a name="structure-variables"></a><span data-ttu-id="c9695-122">Variáveis de estrutura</span><span class="sxs-lookup"><span data-stu-id="c9695-122">Structure Variables</span></span>

<span data-ttu-id="c9695-123">A tabela a seguir descreve as características das variáveis definidas na estrutura XML.</span><span class="sxs-lookup"><span data-stu-id="c9695-123">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="c9695-124">Nome</span><span class="sxs-lookup"><span data-stu-id="c9695-124">Name</span></span>                               | <span data-ttu-id="c9695-125">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="c9695-125">Data type</span></span>         | <span data-ttu-id="c9695-126">Unidade</span><span class="sxs-lookup"><span data-stu-id="c9695-126">Unit</span></span>                  | <span data-ttu-id="c9695-127">Valores com suporte</span><span class="sxs-lookup"><span data-stu-id="c9695-127">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="c9695-128">Resumo</span><span class="sxs-lookup"><span data-stu-id="c9695-128">Summary</span></span>                                                                      |
|------------------------------------|-------------------|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="c9695-129">\_OptionName\_</span><span class="sxs-lookup"><span data-stu-id="c9695-129">\_OptionName\_</span></span><br/>          | <span data-ttu-id="c9695-130">string</span><span class="sxs-lookup"><span data-stu-id="c9695-130">string</span></span><br/> | <span data-ttu-id="c9695-131">characters</span><span class="sxs-lookup"><span data-stu-id="c9695-131">characters</span></span><br/> | <span data-ttu-id="c9695-132">Nome totalmente qualificado válido, conforme definido pelos [namespaces em XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span><span class="sxs-lookup"><span data-stu-id="c9695-132">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="c9695-133">Se nenhum namespace for especificado, o namespace padrão será assumido.</span><span class="sxs-lookup"><span data-stu-id="c9695-133">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="c9695-134">O nome da opção</span><span class="sxs-lookup"><span data-stu-id="c9695-134">The name of the option</span></span><br/>                                            |
| <span data-ttu-id="c9695-135">\_IdentityOptionValue\_</span><span class="sxs-lookup"><span data-stu-id="c9695-135">\_IdentityOptionValue\_</span></span><br/> | <span data-ttu-id="c9695-136">string</span><span class="sxs-lookup"><span data-stu-id="c9695-136">string</span></span><br/> | <span data-ttu-id="c9695-137">N/D</span><span class="sxs-lookup"><span data-stu-id="c9695-137">n/a</span></span><br/>        | <span data-ttu-id="c9695-138">Verdadeiro, Falso</span><span class="sxs-lookup"><span data-stu-id="c9695-138">True, False</span></span><br/>                                                                                                                                                                | <span data-ttu-id="c9695-139">Define uma opção que, quando selecionada, desabilita esse recurso.</span><span class="sxs-lookup"><span data-stu-id="c9695-139">Defines an Option which when selected would disable this feature.</span></span><br/> |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="c9695-140">Conteúdo de linguagem XML (XML)</span><span class="sxs-lookup"><span data-stu-id="c9695-140">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="c9695-141">As palavras-chave do esquema de impressão pública são definidas no https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span><span class="sxs-lookup"><span data-stu-id="c9695-141">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="c9695-142">O conteúdo do linguagem XML público (XML) para essa palavra-chave é definido abaixo:</span><span class="sxs-lookup"><span data-stu-id="c9695-142">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

``` syntax
<psf:Feature name="psk:PageOutputQuality">
  <psf:Property name="psf:SelectionType">
    <psf:Value xsi:type="xs:string">psk:PickOne</psf:Value>
  </psf:Property>
  <!-- Specifies the intent for automatic output (allow the client to automatically choose the best settings). -->
  <psf:Option name="psk:Automatic" />
  <!-- Specifies the intent for draft output (balanced for draft quality text and graphics). -->
  <psf:Option name="psk:Draft" />
  <!-- Specifies the intent for fax output (balanced for standard fax quality). -->
  <psf:Option name="psk:Fax" />
  <!-- Specifies the intent for high quality output (balanced for high quality text and graphics). -->
  <psf:Option name="psk:High" />
  <!-- Specifies the intent for normal output (balanced for good quality text and graphics). -->
  <psf:Option name="psk:Normal" />
  <!-- Specifies the intent for photographic output (images should have the highest quality). -->
  <psf:Option name="psk:Photographic" />
  <!-- Specifies the intent for text only output (graphics may output poorly or not at all). -->
  <psf:Option name="psk:Text" />
</psf:Feature>
    
```

## <a name="related-topics"></a><span data-ttu-id="c9695-143">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="c9695-143">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c9695-144">Especificação de esquema de impressão</span><span class="sxs-lookup"><span data-stu-id="c9695-144">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




