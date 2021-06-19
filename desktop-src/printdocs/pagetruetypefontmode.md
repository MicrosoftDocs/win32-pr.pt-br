---
description: Saiba mais sobre o elemento configurável pelo usuário PageTrueTypeFontMode. Este tópico não é atual. Para obter as informações mais atuais, consulte a Especificação de Esquema de Impressão.
ms.assetid: 36b1de5d-8575-42cf-b158-dcf7705ec157
title: PageTrueTypeFontMode
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bf30af3684693f594f497dbad95d4f9a7743d624
ms.sourcegitcommit: 91530c19d26ba4c57a6af1f37b57f211f580464e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/19/2021
ms.locfileid: "112395611"
---
# <a name="pagetruetypefontmode"></a><span data-ttu-id="b76c6-105">PageTrueTypeFontMode</span><span class="sxs-lookup"><span data-stu-id="b76c6-105">PageTrueTypeFontMode</span></span>

<span data-ttu-id="b76c6-106">Este tópico não é atual.</span><span class="sxs-lookup"><span data-stu-id="b76c6-106">This topic is not current.</span></span> <span data-ttu-id="b76c6-107">Para obter as informações mais atuais, consulte a [Especificação de Esquema de Impressão](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="b76c6-107">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="b76c6-108">Descreve o método de manipulação de fonte TrueType a ser usado.</span><span class="sxs-lookup"><span data-stu-id="b76c6-108">Describes the method of TrueType font handling to be used.</span></span>

-   [<span data-ttu-id="b76c6-109">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="b76c6-109">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="b76c6-110">Conteúdo estrutural</span><span class="sxs-lookup"><span data-stu-id="b76c6-110">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="b76c6-111">linguagem XML conteúdo (XML)</span><span class="sxs-lookup"><span data-stu-id="b76c6-111">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="b76c6-112">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="b76c6-112">Element Information</span></span>



| <span data-ttu-id="b76c6-113">Name</span><span class="sxs-lookup"><span data-stu-id="b76c6-113">Name</span></span> | <span data-ttu-id="b76c6-114">Valor</span><span class="sxs-lookup"><span data-stu-id="b76c6-114">Value</span></span> |
|----------------------------|--------------------|
| <span data-ttu-id="b76c6-115">Tipo de elemento</span><span class="sxs-lookup"><span data-stu-id="b76c6-115">Element Type</span></span> <br/>   | <span data-ttu-id="b76c6-116">Recurso</span><span class="sxs-lookup"><span data-stu-id="b76c6-116">Feature</span></span><br/> |
| <span data-ttu-id="b76c6-117">Prefixo de definição de scoping</span><span class="sxs-lookup"><span data-stu-id="b76c6-117">Scoping Prefix</span></span> <br/> | <span data-ttu-id="b76c6-118">?</span><span class="sxs-lookup"><span data-stu-id="b76c6-118">Page</span></span><br/>    |
| <span data-ttu-id="b76c6-119">Observações</span><span class="sxs-lookup"><span data-stu-id="b76c6-119">Notes</span></span> <br/>          | <span data-ttu-id="b76c6-120">Nenhum</span><span class="sxs-lookup"><span data-stu-id="b76c6-120">None</span></span><br/>    |



 

## <a name="structural-content"></a><span data-ttu-id="b76c6-121">Conteúdo estrutural</span><span class="sxs-lookup"><span data-stu-id="b76c6-121">Structural Content</span></span>

<span data-ttu-id="b76c6-122">A estrutura XML desse elemento é:</span><span class="sxs-lookup"><span data-stu-id="b76c6-122">The XML structure of this element is:</span></span>

``` syntax
<psf:Feature name="psk:PageTrueTypeFontMode">
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

## <a name="structure-variables"></a><span data-ttu-id="b76c6-123">Variáveis de estrutura</span><span class="sxs-lookup"><span data-stu-id="b76c6-123">Structure Variables</span></span>

<span data-ttu-id="b76c6-124">A tabela a seguir descreve as características das variáveis definidas na estrutura XML.</span><span class="sxs-lookup"><span data-stu-id="b76c6-124">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="b76c6-125">Nome</span><span class="sxs-lookup"><span data-stu-id="b76c6-125">Name</span></span>                               | <span data-ttu-id="b76c6-126">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="b76c6-126">Data type</span></span>         | <span data-ttu-id="b76c6-127">Unidade</span><span class="sxs-lookup"><span data-stu-id="b76c6-127">Unit</span></span>                  | <span data-ttu-id="b76c6-128">Valores com suporte</span><span class="sxs-lookup"><span data-stu-id="b76c6-128">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="b76c6-129">Resumo</span><span class="sxs-lookup"><span data-stu-id="b76c6-129">Summary</span></span>                                                                      |
|------------------------------------|-------------------|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="b76c6-130">\_Optionname\_</span><span class="sxs-lookup"><span data-stu-id="b76c6-130">\_OptionName\_</span></span><br/>          | <span data-ttu-id="b76c6-131">string</span><span class="sxs-lookup"><span data-stu-id="b76c6-131">string</span></span><br/> | <span data-ttu-id="b76c6-132">characters</span><span class="sxs-lookup"><span data-stu-id="b76c6-132">characters</span></span><br/> | <span data-ttu-id="b76c6-133">Nome totalmente qualificado válido, conforme definido [por Namespaces em XML.](https://www.w3.org/TR/1999/REC-xml-names-19990114/)</span><span class="sxs-lookup"><span data-stu-id="b76c6-133">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="b76c6-134">Se nenhum namespace for especificado, o namespace padrão será assumido.</span><span class="sxs-lookup"><span data-stu-id="b76c6-134">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="b76c6-135">O nome da opção.</span><span class="sxs-lookup"><span data-stu-id="b76c6-135">The name of the option.</span></span><br/>                                           |
| <span data-ttu-id="b76c6-136">\_IdentityOptionValue\_</span><span class="sxs-lookup"><span data-stu-id="b76c6-136">\_IdentityOptionValue\_</span></span><br/> | <span data-ttu-id="b76c6-137">string</span><span class="sxs-lookup"><span data-stu-id="b76c6-137">string</span></span><br/> | <span data-ttu-id="b76c6-138">n/d</span><span class="sxs-lookup"><span data-stu-id="b76c6-138">n/a</span></span><br/>        | <span data-ttu-id="b76c6-139">True, False.</span><span class="sxs-lookup"><span data-stu-id="b76c6-139">True, False.</span></span><br/>                                                                                                                                                               | <span data-ttu-id="b76c6-140">Define uma Opção que, quando selecionada, desabilitará esse recurso.</span><span class="sxs-lookup"><span data-stu-id="b76c6-140">Defines an Option which when selected would disable this feature.</span></span><br/> |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="b76c6-141">linguagem XML conteúdo (XML)</span><span class="sxs-lookup"><span data-stu-id="b76c6-141">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="b76c6-142">As palavras-chave public Print Schema são definidas no https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace .</span><span class="sxs-lookup"><span data-stu-id="b76c6-142">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="b76c6-143">O conteúdo linguagem XML XML (public linguagem XML) para essa palavra-chave é definido abaixo:</span><span class="sxs-lookup"><span data-stu-id="b76c6-143">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

``` syntax
<psf:Feature name="psk:PageTrueTypeFontMode">
  <psf:Property name="psf:SelectionType">
    <psf:Value xsi:type="xs:string">psk:PickOne</psf:Value>
  </psf:Property>
  <!--Automatic handling of TrueType font-->
  <psf:Option name="psk:Automatic" />
  <!--TrueType font is downloaded as outline font-->
  <psf:Option name="psk:DownloadAsOutlineFont" />
  <!--TrueType font is downloaded as raster font-->
  <psf:Option name="psk:DownloadAsRasterFont" />
  <!--TrueType font is downloaded as native true type font-->
  <psf:Option name="psk:DownloadAsNativeTrueTypeFont" />
  <!--TrueType font is rendered as a bitmap-->
  <psf:Option name="psk:RenderAsBitmap" />
</psf:Feature>    
```

## <a name="related-topics"></a><span data-ttu-id="b76c6-144">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="b76c6-144">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b76c6-145">Especificação de esquema de impressão</span><span class="sxs-lookup"><span data-stu-id="b76c6-145">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




