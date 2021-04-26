---
description: Este tópico não é atual. Para obter as informações mais atuais, consulte a especificação do esquema de impressão.
ms.assetid: df11ee89-fe62-4fe5-a1d6-0f925360ca39
title: PageICMRenderingIntent
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d17eea84ba45ea7c121080f7649b03492c6f3409
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/26/2021
ms.locfileid: "107995553"
---
# <a name="pageicmrenderingintent"></a><span data-ttu-id="876f8-104">PageICMRenderingIntent</span><span class="sxs-lookup"><span data-stu-id="876f8-104">PageICMRenderingIntent</span></span>

<span data-ttu-id="876f8-105">Este tópico não é atual.</span><span class="sxs-lookup"><span data-stu-id="876f8-105">This topic is not current.</span></span> <span data-ttu-id="876f8-106">Para obter as informações mais atuais, consulte a [especificação do esquema de impressão](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="876f8-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="876f8-107">Descreve a tentativa de renderização conforme definido pela especificação ICC v2.</span><span class="sxs-lookup"><span data-stu-id="876f8-107">Describes the rendering intent as defined by the ICC v2 Specification.</span></span> <span data-ttu-id="876f8-108">Esse valor deve ser ignorado se uma imagem ou elemento gráfico tiver um perfil inserido que especifica a tentativa de renderização.</span><span class="sxs-lookup"><span data-stu-id="876f8-108">This value should be ignored if an image or graphical element has an embedded profile that specifies the Rendering intent.</span></span>

-   [<span data-ttu-id="876f8-109">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="876f8-109">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="876f8-110">Conteúdo estrutural</span><span class="sxs-lookup"><span data-stu-id="876f8-110">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="876f8-111">Conteúdo de linguagem XML (XML)</span><span class="sxs-lookup"><span data-stu-id="876f8-111">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="876f8-112">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="876f8-112">Element Information</span></span>



| <span data-ttu-id="876f8-113">Nome</span><span class="sxs-lookup"><span data-stu-id="876f8-113">Name</span></span> | <span data-ttu-id="876f8-114">Valor</span><span class="sxs-lookup"><span data-stu-id="876f8-114">Value</span></span> |
|----------------------------|--------------------|
| <span data-ttu-id="876f8-115">Tipo de elemento</span><span class="sxs-lookup"><span data-stu-id="876f8-115">Element Type</span></span> <br/>   | <span data-ttu-id="876f8-116">Recurso</span><span class="sxs-lookup"><span data-stu-id="876f8-116">Feature</span></span><br/> |
| <span data-ttu-id="876f8-117">Prefixo de escopo</span><span class="sxs-lookup"><span data-stu-id="876f8-117">Scoping Prefix</span></span> <br/> | <span data-ttu-id="876f8-118">?</span><span class="sxs-lookup"><span data-stu-id="876f8-118">Page</span></span><br/>    |
| <span data-ttu-id="876f8-119">Observações</span><span class="sxs-lookup"><span data-stu-id="876f8-119">Notes</span></span> <br/>          | <span data-ttu-id="876f8-120">Nenhum</span><span class="sxs-lookup"><span data-stu-id="876f8-120">None</span></span> <br/>   |



 

## <a name="structural-content"></a><span data-ttu-id="876f8-121">Conteúdo estrutural</span><span class="sxs-lookup"><span data-stu-id="876f8-121">Structural Content</span></span>

<span data-ttu-id="876f8-122">A estrutura XML desse elemento é:</span><span class="sxs-lookup"><span data-stu-id="876f8-122">The XML structure of this element is:</span></span>

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

## <a name="structure-variables"></a><span data-ttu-id="876f8-123">Variáveis de estrutura</span><span class="sxs-lookup"><span data-stu-id="876f8-123">Structure Variables</span></span>

<span data-ttu-id="876f8-124">A tabela a seguir descreve as características das variáveis definidas na estrutura XML.</span><span class="sxs-lookup"><span data-stu-id="876f8-124">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="876f8-125">Nome</span><span class="sxs-lookup"><span data-stu-id="876f8-125">Name</span></span>                               | <span data-ttu-id="876f8-126">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="876f8-126">Data type</span></span>         | <span data-ttu-id="876f8-127">Unidade</span><span class="sxs-lookup"><span data-stu-id="876f8-127">Unit</span></span>                  | <span data-ttu-id="876f8-128">Valores com suporte</span><span class="sxs-lookup"><span data-stu-id="876f8-128">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="876f8-129">Resumo</span><span class="sxs-lookup"><span data-stu-id="876f8-129">Summary</span></span>                                                                      |
|------------------------------------|-------------------|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="876f8-130">\_OptionName\_</span><span class="sxs-lookup"><span data-stu-id="876f8-130">\_OptionName\_</span></span><br/>          | <span data-ttu-id="876f8-131">string</span><span class="sxs-lookup"><span data-stu-id="876f8-131">string</span></span><br/> | <span data-ttu-id="876f8-132">characters</span><span class="sxs-lookup"><span data-stu-id="876f8-132">characters</span></span><br/> | <span data-ttu-id="876f8-133">Nome totalmente qualificado válido, conforme definido pelos [namespaces em XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span><span class="sxs-lookup"><span data-stu-id="876f8-133">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="876f8-134">Se nenhum namespace for especificado, o namespace padrão será assumido.</span><span class="sxs-lookup"><span data-stu-id="876f8-134">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="876f8-135">O nome da opção.</span><span class="sxs-lookup"><span data-stu-id="876f8-135">The name of the option.</span></span><br/>                                           |
| <span data-ttu-id="876f8-136">\_IdentityOptionValue\_</span><span class="sxs-lookup"><span data-stu-id="876f8-136">\_IdentityOptionValue\_</span></span><br/> | <span data-ttu-id="876f8-137">string</span><span class="sxs-lookup"><span data-stu-id="876f8-137">string</span></span><br/> | <span data-ttu-id="876f8-138">N/D</span><span class="sxs-lookup"><span data-stu-id="876f8-138">n/a</span></span><br/>        | <span data-ttu-id="876f8-139">True, False.</span><span class="sxs-lookup"><span data-stu-id="876f8-139">True, False.</span></span><br/>                                                                                                                                                               | <span data-ttu-id="876f8-140">Define uma opção que, quando selecionada, desabilita esse recurso.</span><span class="sxs-lookup"><span data-stu-id="876f8-140">Defines an Option which when selected would disable this feature.</span></span><br/> |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="876f8-141">Conteúdo de linguagem XML (XML)</span><span class="sxs-lookup"><span data-stu-id="876f8-141">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="876f8-142">As palavras-chave do esquema de impressão pública são definidas no https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span><span class="sxs-lookup"><span data-stu-id="876f8-142">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="876f8-143">O conteúdo do linguagem XML público (XML) para essa palavra-chave é definido abaixo:</span><span class="sxs-lookup"><span data-stu-id="876f8-143">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

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

## <a name="related-topics"></a><span data-ttu-id="876f8-144">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="876f8-144">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="876f8-145">Especificação de esquema de impressão</span><span class="sxs-lookup"><span data-stu-id="876f8-145">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




