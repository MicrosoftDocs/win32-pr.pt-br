---
description: Leia sobre o elemento pageICMRenderingIntent configurável pelo usuário. Este tópico não é atual. Para obter as informações mais atuais, consulte a Especificação de Esquema de Impressão.
ms.assetid: df11ee89-fe62-4fe5-a1d6-0f925360ca39
title: PageICMRenderingIntent
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ab595bac5a7136510335167c37bc36d8a7e44056
ms.sourcegitcommit: 998d50f6def8a25850fc113fc8a2df903c829c5e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/09/2021
ms.locfileid: "113549174"
---
# <a name="pageicmrenderingintent"></a><span data-ttu-id="b0f8e-105">PageICMRenderingIntent</span><span class="sxs-lookup"><span data-stu-id="b0f8e-105">PageICMRenderingIntent</span></span>

<span data-ttu-id="b0f8e-106">Este tópico não é atual.</span><span class="sxs-lookup"><span data-stu-id="b0f8e-106">This topic is not current.</span></span> <span data-ttu-id="b0f8e-107">Para obter as informações mais atuais, consulte a [Especificação de Esquema de Impressão](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="b0f8e-107">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="b0f8e-108">Descreve a intenção de renderização conforme definido pela Especificação ICC v2.</span><span class="sxs-lookup"><span data-stu-id="b0f8e-108">Describes the rendering intent as defined by the ICC v2 Specification.</span></span> <span data-ttu-id="b0f8e-109">Esse valor deverá ser ignorado se uma imagem ou elemento gráfico tiver um perfil inserido que especifique a intenção rendering.</span><span class="sxs-lookup"><span data-stu-id="b0f8e-109">This value should be ignored if an image or graphical element has an embedded profile that specifies the Rendering intent.</span></span>

-   [<span data-ttu-id="b0f8e-110">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="b0f8e-110">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="b0f8e-111">Conteúdo estrutural</span><span class="sxs-lookup"><span data-stu-id="b0f8e-111">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="b0f8e-112">linguagem XML conteúdo (XML)</span><span class="sxs-lookup"><span data-stu-id="b0f8e-112">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="b0f8e-113">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="b0f8e-113">Element Information</span></span>



| <span data-ttu-id="b0f8e-114">Nome</span><span class="sxs-lookup"><span data-stu-id="b0f8e-114">Name</span></span> | <span data-ttu-id="b0f8e-115">Valor</span><span class="sxs-lookup"><span data-stu-id="b0f8e-115">Value</span></span> |
|----------------------------|--------------------|
| <span data-ttu-id="b0f8e-116">Tipo de elemento</span><span class="sxs-lookup"><span data-stu-id="b0f8e-116">Element Type</span></span> <br/>   | <span data-ttu-id="b0f8e-117">Recurso</span><span class="sxs-lookup"><span data-stu-id="b0f8e-117">Feature</span></span><br/> |
| <span data-ttu-id="b0f8e-118">Prefixo de definição de scoping</span><span class="sxs-lookup"><span data-stu-id="b0f8e-118">Scoping Prefix</span></span> <br/> | <span data-ttu-id="b0f8e-119">Página</span><span class="sxs-lookup"><span data-stu-id="b0f8e-119">Page</span></span><br/>    |
| <span data-ttu-id="b0f8e-120">Observações</span><span class="sxs-lookup"><span data-stu-id="b0f8e-120">Notes</span></span> <br/>          | <span data-ttu-id="b0f8e-121">Nenhum</span><span class="sxs-lookup"><span data-stu-id="b0f8e-121">None</span></span> <br/>   |



 

## <a name="structural-content"></a><span data-ttu-id="b0f8e-122">Conteúdo estrutural</span><span class="sxs-lookup"><span data-stu-id="b0f8e-122">Structural Content</span></span>

<span data-ttu-id="b0f8e-123">A estrutura XML desse elemento é:</span><span class="sxs-lookup"><span data-stu-id="b0f8e-123">The XML structure of this element is:</span></span>

``` syntax
<psf:Feature name="psk:PageICMRenderingIntent">
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

## <a name="structure-variables"></a><span data-ttu-id="b0f8e-124">Variáveis de estrutura</span><span class="sxs-lookup"><span data-stu-id="b0f8e-124">Structure Variables</span></span>

<span data-ttu-id="b0f8e-125">A tabela a seguir descreve as características das variáveis definidas na estrutura XML.</span><span class="sxs-lookup"><span data-stu-id="b0f8e-125">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="b0f8e-126">Nome</span><span class="sxs-lookup"><span data-stu-id="b0f8e-126">Name</span></span>                               | <span data-ttu-id="b0f8e-127">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="b0f8e-127">Data type</span></span>         | <span data-ttu-id="b0f8e-128">Unidade</span><span class="sxs-lookup"><span data-stu-id="b0f8e-128">Unit</span></span>                  | <span data-ttu-id="b0f8e-129">Valores com suporte</span><span class="sxs-lookup"><span data-stu-id="b0f8e-129">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="b0f8e-130">Resumo</span><span class="sxs-lookup"><span data-stu-id="b0f8e-130">Summary</span></span>                                                                      |
|------------------------------------|-------------------|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="b0f8e-131">\_Optionname\_</span><span class="sxs-lookup"><span data-stu-id="b0f8e-131">\_OptionName\_</span></span><br/>          | <span data-ttu-id="b0f8e-132">string</span><span class="sxs-lookup"><span data-stu-id="b0f8e-132">string</span></span><br/> | <span data-ttu-id="b0f8e-133">characters</span><span class="sxs-lookup"><span data-stu-id="b0f8e-133">characters</span></span><br/> | <span data-ttu-id="b0f8e-134">Nome totalmente qualificado válido, conforme definido [por Namespaces em XML.](https://www.w3.org/TR/1999/REC-xml-names-19990114/)</span><span class="sxs-lookup"><span data-stu-id="b0f8e-134">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="b0f8e-135">Se nenhum namespace for especificado, o namespace padrão será assumido.</span><span class="sxs-lookup"><span data-stu-id="b0f8e-135">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="b0f8e-136">O nome da opção.</span><span class="sxs-lookup"><span data-stu-id="b0f8e-136">The name of the option.</span></span><br/>                                           |
| <span data-ttu-id="b0f8e-137">\_IdentityOptionValue\_</span><span class="sxs-lookup"><span data-stu-id="b0f8e-137">\_IdentityOptionValue\_</span></span><br/> | <span data-ttu-id="b0f8e-138">string</span><span class="sxs-lookup"><span data-stu-id="b0f8e-138">string</span></span><br/> | <span data-ttu-id="b0f8e-139">n/d</span><span class="sxs-lookup"><span data-stu-id="b0f8e-139">n/a</span></span><br/>        | <span data-ttu-id="b0f8e-140">True, False.</span><span class="sxs-lookup"><span data-stu-id="b0f8e-140">True, False.</span></span><br/>                                                                                                                                                               | <span data-ttu-id="b0f8e-141">Define uma Opção que, quando selecionada, desabilitará esse recurso.</span><span class="sxs-lookup"><span data-stu-id="b0f8e-141">Defines an Option which when selected would disable this feature.</span></span><br/> |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="b0f8e-142">linguagem XML conteúdo (XML)</span><span class="sxs-lookup"><span data-stu-id="b0f8e-142">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="b0f8e-143">As palavras-chave public Print Schema são definidas no https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace .</span><span class="sxs-lookup"><span data-stu-id="b0f8e-143">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="b0f8e-144">O conteúdo linguagem XML XML (public linguagem XML) para essa palavra-chave é definido abaixo:</span><span class="sxs-lookup"><span data-stu-id="b0f8e-144">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

``` syntax
<psf:Feature name="psk:PageICMRenderingIntent">
  <psf:Property name="SelectionType">
    <psf:Value xsi:type="xs:string">PickOne</psf:Value>
  </psf:Property>
  <!--Absolute Colorimetric Rendering intent-->
  <psf:Option name="psk:AbsoluteColorimetric" />
  <!--Relative Colorimetric Rendering intent -->
  <psf:Option name="psk:RelativeColorimetric" />
  <!--Photographs Rendering intent -->
  <psf:Option name="psk:Photographs" />
  <!--Business Graphics Rendering intent -->
  <psf:Option name="psk:BusinessGraphics" />
</psf:Feature>
```

## <a name="related-topics"></a><span data-ttu-id="b0f8e-145">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="b0f8e-145">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b0f8e-146">Especificação de esquema de impressão</span><span class="sxs-lookup"><span data-stu-id="b0f8e-146">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




