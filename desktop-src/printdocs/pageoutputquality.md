---
description: Este tópico não é atual. Para obter as informações mais atuais, consulte a especificação do esquema de impressão.
ms.assetid: 4720f812-a71a-458f-85fa-7885cca0dbbb
title: PageOutputQuality
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 09ae5bdcf7e1742ae15b0b6d832b3d15d47718b7
ms.sourcegitcommit: 7b8f6151ebe247536304866459b2973276271d4d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/06/2021
ms.locfileid: "104298052"
---
# <a name="pageoutputquality"></a><span data-ttu-id="4dbd6-104">PageOutputQuality</span><span class="sxs-lookup"><span data-stu-id="4dbd6-104">PageOutputQuality</span></span>

<span data-ttu-id="4dbd6-105">Este tópico não é atual.</span><span class="sxs-lookup"><span data-stu-id="4dbd6-105">This topic is not current.</span></span> <span data-ttu-id="4dbd6-106">Para obter as informações mais atuais, consulte a [especificação do esquema de impressão](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="4dbd6-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="4dbd6-107">Descreve o nível de qualidade da saída.</span><span class="sxs-lookup"><span data-stu-id="4dbd6-107">Describes the quality level of the output.</span></span>

-   [<span data-ttu-id="4dbd6-108">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="4dbd6-108">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="4dbd6-109">Conteúdo estrutural</span><span class="sxs-lookup"><span data-stu-id="4dbd6-109">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="4dbd6-110">Conteúdo de linguagem XML (XML)</span><span class="sxs-lookup"><span data-stu-id="4dbd6-110">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="4dbd6-111">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="4dbd6-111">Element Information</span></span>



| <span data-ttu-id="4dbd6-112">Nome</span><span class="sxs-lookup"><span data-stu-id="4dbd6-112">Name</span></span>                       |                    |
|----------------------------|--------------------|
| <span data-ttu-id="4dbd6-113">Tipo de elemento</span><span class="sxs-lookup"><span data-stu-id="4dbd6-113">Element Type</span></span> <br/>   | <span data-ttu-id="4dbd6-114">Recurso</span><span class="sxs-lookup"><span data-stu-id="4dbd6-114">Feature</span></span><br/> |
| <span data-ttu-id="4dbd6-115">Prefixo de escopo</span><span class="sxs-lookup"><span data-stu-id="4dbd6-115">Scoping Prefix</span></span> <br/> | <span data-ttu-id="4dbd6-116">?</span><span class="sxs-lookup"><span data-stu-id="4dbd6-116">Page</span></span><br/>    |
| <span data-ttu-id="4dbd6-117">Observações</span><span class="sxs-lookup"><span data-stu-id="4dbd6-117">Notes</span></span> <br/>          | <span data-ttu-id="4dbd6-118">Nenhum</span><span class="sxs-lookup"><span data-stu-id="4dbd6-118">None</span></span><br/>    |



 

## <a name="structural-content"></a><span data-ttu-id="4dbd6-119">Conteúdo estrutural</span><span class="sxs-lookup"><span data-stu-id="4dbd6-119">Structural Content</span></span>

<span data-ttu-id="4dbd6-120">A estrutura XML desse elemento é:</span><span class="sxs-lookup"><span data-stu-id="4dbd6-120">The XML structure of this element is:</span></span>

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

## <a name="structure-variables"></a><span data-ttu-id="4dbd6-121">Variáveis de estrutura</span><span class="sxs-lookup"><span data-stu-id="4dbd6-121">Structure Variables</span></span>

<span data-ttu-id="4dbd6-122">A tabela a seguir descreve as características das variáveis definidas na estrutura XML.</span><span class="sxs-lookup"><span data-stu-id="4dbd6-122">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="4dbd6-123">Nome</span><span class="sxs-lookup"><span data-stu-id="4dbd6-123">Name</span></span>                               | <span data-ttu-id="4dbd6-124">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="4dbd6-124">Data type</span></span>         | <span data-ttu-id="4dbd6-125">Unidade</span><span class="sxs-lookup"><span data-stu-id="4dbd6-125">Unit</span></span>                  | <span data-ttu-id="4dbd6-126">Valores com suporte</span><span class="sxs-lookup"><span data-stu-id="4dbd6-126">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="4dbd6-127">Resumo</span><span class="sxs-lookup"><span data-stu-id="4dbd6-127">Summary</span></span>                                                                      |
|------------------------------------|-------------------|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="4dbd6-128">\_OptionName\_</span><span class="sxs-lookup"><span data-stu-id="4dbd6-128">\_OptionName\_</span></span><br/>          | <span data-ttu-id="4dbd6-129">string</span><span class="sxs-lookup"><span data-stu-id="4dbd6-129">string</span></span><br/> | <span data-ttu-id="4dbd6-130">characters</span><span class="sxs-lookup"><span data-stu-id="4dbd6-130">characters</span></span><br/> | <span data-ttu-id="4dbd6-131">Nome totalmente qualificado válido, conforme definido pelos [namespaces em XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span><span class="sxs-lookup"><span data-stu-id="4dbd6-131">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="4dbd6-132">Se nenhum namespace for especificado, o namespace padrão será assumido.</span><span class="sxs-lookup"><span data-stu-id="4dbd6-132">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="4dbd6-133">O nome da opção</span><span class="sxs-lookup"><span data-stu-id="4dbd6-133">The name of the option</span></span><br/>                                            |
| <span data-ttu-id="4dbd6-134">\_IdentityOptionValue\_</span><span class="sxs-lookup"><span data-stu-id="4dbd6-134">\_IdentityOptionValue\_</span></span><br/> | <span data-ttu-id="4dbd6-135">string</span><span class="sxs-lookup"><span data-stu-id="4dbd6-135">string</span></span><br/> | <span data-ttu-id="4dbd6-136">N/D</span><span class="sxs-lookup"><span data-stu-id="4dbd6-136">n/a</span></span><br/>        | <span data-ttu-id="4dbd6-137">Verdadeiro, Falso</span><span class="sxs-lookup"><span data-stu-id="4dbd6-137">True, False</span></span><br/>                                                                                                                                                                | <span data-ttu-id="4dbd6-138">Define uma opção que, quando selecionada, desabilita esse recurso.</span><span class="sxs-lookup"><span data-stu-id="4dbd6-138">Defines an Option which when selected would disable this feature.</span></span><br/> |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="4dbd6-139">Conteúdo de linguagem XML (XML)</span><span class="sxs-lookup"><span data-stu-id="4dbd6-139">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="4dbd6-140">As palavras-chave do esquema de impressão pública são definidas no https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span><span class="sxs-lookup"><span data-stu-id="4dbd6-140">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="4dbd6-141">O conteúdo do linguagem XML público (XML) para essa palavra-chave é definido abaixo:</span><span class="sxs-lookup"><span data-stu-id="4dbd6-141">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

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

## <a name="related-topics"></a><span data-ttu-id="4dbd6-142">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="4dbd6-142">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4dbd6-143">Especificação de esquema de impressão</span><span class="sxs-lookup"><span data-stu-id="4dbd6-143">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




