---
description: Este tópico não é atual. Para obter as informações mais atuais, consulte a especificação do esquema de impressão.
ms.assetid: a05357c0-6a82-42ff-b4f8-d3e0ee089055
title: PageMirrorImage
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a59b34a836fe356714f7323b32cb9efbf16317bb
ms.sourcegitcommit: 7b8f6151ebe247536304866459b2973276271d4d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/06/2021
ms.locfileid: "105796156"
---
# <a name="pagemirrorimage"></a><span data-ttu-id="d07b4-104">PageMirrorImage</span><span class="sxs-lookup"><span data-stu-id="d07b4-104">PageMirrorImage</span></span>

<span data-ttu-id="d07b4-105">Este tópico não é atual.</span><span class="sxs-lookup"><span data-stu-id="d07b4-105">This topic is not current.</span></span> <span data-ttu-id="d07b4-106">Para obter as informações mais atuais, consulte a [especificação do esquema de impressão](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="d07b4-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="d07b4-107">Descreve a configuração de espelhamento da saída.</span><span class="sxs-lookup"><span data-stu-id="d07b4-107">Describes the mirroring setting of the output.</span></span>

-   [<span data-ttu-id="d07b4-108">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="d07b4-108">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="d07b4-109">Conteúdo estrutural</span><span class="sxs-lookup"><span data-stu-id="d07b4-109">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="d07b4-110">Conteúdo de linguagem XML (XML)</span><span class="sxs-lookup"><span data-stu-id="d07b4-110">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="d07b4-111">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="d07b4-111">Element Information</span></span>



| <span data-ttu-id="d07b4-112">Nome</span><span class="sxs-lookup"><span data-stu-id="d07b4-112">Name</span></span>                       |                    |
|----------------------------|--------------------|
| <span data-ttu-id="d07b4-113">Tipo de elemento</span><span class="sxs-lookup"><span data-stu-id="d07b4-113">Element Type</span></span> <br/>   | <span data-ttu-id="d07b4-114">Recurso</span><span class="sxs-lookup"><span data-stu-id="d07b4-114">Feature</span></span><br/> |
| <span data-ttu-id="d07b4-115">Prefixo de escopo</span><span class="sxs-lookup"><span data-stu-id="d07b4-115">Scoping Prefix</span></span> <br/> | <span data-ttu-id="d07b4-116">?</span><span class="sxs-lookup"><span data-stu-id="d07b4-116">Page</span></span><br/>    |
| <span data-ttu-id="d07b4-117">Observações</span><span class="sxs-lookup"><span data-stu-id="d07b4-117">Notes</span></span> <br/>          | <span data-ttu-id="d07b4-118">Nenhum</span><span class="sxs-lookup"><span data-stu-id="d07b4-118">None</span></span><br/>    |



 

## <a name="structural-content"></a><span data-ttu-id="d07b4-119">Conteúdo estrutural</span><span class="sxs-lookup"><span data-stu-id="d07b4-119">Structural Content</span></span>

<span data-ttu-id="d07b4-120">A estrutura XML desse elemento é:</span><span class="sxs-lookup"><span data-stu-id="d07b4-120">The XML structure of this element is:</span></span>

``` syntax
<psf:Feature name="psk:PageMirrorImage">
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

## <a name="structure-variables"></a><span data-ttu-id="d07b4-121">Variáveis de estrutura</span><span class="sxs-lookup"><span data-stu-id="d07b4-121">Structure Variables</span></span>

<span data-ttu-id="d07b4-122">A tabela a seguir descreve as características das variáveis definidas na estrutura XML.</span><span class="sxs-lookup"><span data-stu-id="d07b4-122">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="d07b4-123">Nome</span><span class="sxs-lookup"><span data-stu-id="d07b4-123">Name</span></span>                               | <span data-ttu-id="d07b4-124">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="d07b4-124">Data type</span></span>         | <span data-ttu-id="d07b4-125">Unidade</span><span class="sxs-lookup"><span data-stu-id="d07b4-125">Unit</span></span>                  | <span data-ttu-id="d07b4-126">Valores com suporte</span><span class="sxs-lookup"><span data-stu-id="d07b4-126">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="d07b4-127">Resumo</span><span class="sxs-lookup"><span data-stu-id="d07b4-127">Summary</span></span>                                                                      |
|------------------------------------|-------------------|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="d07b4-128">\_OptionName\_</span><span class="sxs-lookup"><span data-stu-id="d07b4-128">\_OptionName\_</span></span><br/>          | <span data-ttu-id="d07b4-129">string</span><span class="sxs-lookup"><span data-stu-id="d07b4-129">string</span></span><br/> | <span data-ttu-id="d07b4-130">characters</span><span class="sxs-lookup"><span data-stu-id="d07b4-130">characters</span></span><br/> | <span data-ttu-id="d07b4-131">Nome totalmente qualificado válido, conforme definido pelos [namespaces em XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span><span class="sxs-lookup"><span data-stu-id="d07b4-131">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="d07b4-132">Se nenhum namespace for especificado, o namespace padrão será assumido.</span><span class="sxs-lookup"><span data-stu-id="d07b4-132">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="d07b4-133">O nome da opção.</span><span class="sxs-lookup"><span data-stu-id="d07b4-133">The name of the option.</span></span><br/>                                           |
| <span data-ttu-id="d07b4-134">\_IdentityOptionValue\_</span><span class="sxs-lookup"><span data-stu-id="d07b4-134">\_IdentityOptionValue\_</span></span><br/> | <span data-ttu-id="d07b4-135">string</span><span class="sxs-lookup"><span data-stu-id="d07b4-135">string</span></span><br/> | <span data-ttu-id="d07b4-136">N/D</span><span class="sxs-lookup"><span data-stu-id="d07b4-136">n/a</span></span><br/>        | <span data-ttu-id="d07b4-137">True, False.</span><span class="sxs-lookup"><span data-stu-id="d07b4-137">True, False.</span></span><br/>                                                                                                                                                               | <span data-ttu-id="d07b4-138">Define uma opção que, quando selecionada, desabilita esse recurso.</span><span class="sxs-lookup"><span data-stu-id="d07b4-138">Defines an Option which when selected would disable this feature.</span></span><br/> |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="d07b4-139">Conteúdo de linguagem XML (XML)</span><span class="sxs-lookup"><span data-stu-id="d07b4-139">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="d07b4-140">As palavras-chave do esquema de impressão pública são definidas no https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span><span class="sxs-lookup"><span data-stu-id="d07b4-140">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="d07b4-141">O conteúdo do linguagem XML público (XML) para essa palavra-chave é definido abaixo:</span><span class="sxs-lookup"><span data-stu-id="d07b4-141">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

``` syntax
<psf:Feature name="psk:PageMirrorImage">
  <psf:Property name="psf:SelectionType">
    <psf:Value xsi:type="xs:string">psk:PickOne</psf:Value>
  </psf:Property>
  <!-- Specifies the output should be mirrored parallel to the MediaSizeWidth direction. -->
  <psf:Option name="psk:MirrorImageWidth" />
  <!-- Specifies the output should be mirrored parallel to the MediaSizeHeight direction. -->
  <psf:Option name="psk:MirrorImageHeight" />
  <!-- Specifies the output should not be mirrored. -->
  <psf:Option name="psk:None" />
</psf:Feature>
    
```

## <a name="related-topics"></a><span data-ttu-id="d07b4-142">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="d07b4-142">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d07b4-143">Especificação de esquema de impressão</span><span class="sxs-lookup"><span data-stu-id="d07b4-143">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




