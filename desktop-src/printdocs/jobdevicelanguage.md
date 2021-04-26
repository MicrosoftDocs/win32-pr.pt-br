---
description: Este tópico não é atual. Para obter as informações mais atuais, consulte a especificação do esquema de impressão.
ms.assetid: 3894d9fa-2bf7-447a-bac3-e72a0fdb7187
title: JobDeviceLanguage
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 66b9f85b44ae9fdc6efb66ce5b72bb68c5187790
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/26/2021
ms.locfileid: "107998293"
---
# <a name="jobdevicelanguage"></a><span data-ttu-id="b007d-104">JobDeviceLanguage</span><span class="sxs-lookup"><span data-stu-id="b007d-104">JobDeviceLanguage</span></span>

<span data-ttu-id="b007d-105">Este tópico não é atual.</span><span class="sxs-lookup"><span data-stu-id="b007d-105">This topic is not current.</span></span> <span data-ttu-id="b007d-106">Para obter as informações mais atuais, consulte a [especificação do esquema de impressão](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="b007d-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="b007d-107">Descreve os idiomas de dispositivo com suporte para enviar dados do driver para o dispositivo físico.</span><span class="sxs-lookup"><span data-stu-id="b007d-107">Describes the device languages supported for sending data from driver to physical device.</span></span> <span data-ttu-id="b007d-108">Isso geralmente é chamado de "linguagem de descrição de página".</span><span class="sxs-lookup"><span data-stu-id="b007d-108">This is often called "Page Description Language".</span></span> <span data-ttu-id="b007d-109">Essa palavra-chave define qual linguagem de descrição de página é suportada pelo driver e pelo dispositivo físico.</span><span class="sxs-lookup"><span data-stu-id="b007d-109">This keyword defines what page description language is supported by the driver and physical device.</span></span>

-   [<span data-ttu-id="b007d-110">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="b007d-110">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="b007d-111">Conteúdo estrutural</span><span class="sxs-lookup"><span data-stu-id="b007d-111">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="b007d-112">Conteúdo de linguagem XML (XML)</span><span class="sxs-lookup"><span data-stu-id="b007d-112">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="b007d-113">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="b007d-113">Element Information</span></span>



| <span data-ttu-id="b007d-114">Nome</span><span class="sxs-lookup"><span data-stu-id="b007d-114">Name</span></span> | <span data-ttu-id="b007d-115">Valor</span><span class="sxs-lookup"><span data-stu-id="b007d-115">Value</span></span> |
|----------------------------|--------------------|
| <span data-ttu-id="b007d-116">Tipo de elemento</span><span class="sxs-lookup"><span data-stu-id="b007d-116">Element Type</span></span> <br/>   | <span data-ttu-id="b007d-117">Recurso</span><span class="sxs-lookup"><span data-stu-id="b007d-117">Feature</span></span><br/> |
| <span data-ttu-id="b007d-118">Prefixo de escopo</span><span class="sxs-lookup"><span data-stu-id="b007d-118">Scoping Prefix</span></span> <br/> | <span data-ttu-id="b007d-119">Trabalho</span><span class="sxs-lookup"><span data-stu-id="b007d-119">Job</span></span><br/>     |
| <span data-ttu-id="b007d-120">Observações</span><span class="sxs-lookup"><span data-stu-id="b007d-120">Notes</span></span> <br/>          | <span data-ttu-id="b007d-121">Nenhum</span><span class="sxs-lookup"><span data-stu-id="b007d-121">None</span></span><br/>    |



 

## <a name="structural-content"></a><span data-ttu-id="b007d-122">Conteúdo estrutural</span><span class="sxs-lookup"><span data-stu-id="b007d-122">Structural Content</span></span>

<span data-ttu-id="b007d-123">A estrutura XML desse elemento é:</span><span class="sxs-lookup"><span data-stu-id="b007d-123">The XML structure of this element is:</span></span>

``` syntax
<psf:Feature name="psk:JobDeviceLanguage">
  <psf:Property name="psf:SelectionType">
    <psf:Value xsi:type="xs:string">psk:PickOne</psf:Value>
  </psf:Property>
  <psf:Option name="psk:_OptionName_">
    <psf:Property name="psf:IdentityOption">
      <psf:Value xsi:type="xs:string">_IdentityOptionValue_</psf:Value>
    </psf:Property>
    <psf:ScoredProperty name="psk:LanguageLevel">
      <psf:Value xsi:type="xs:string">_value_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:LanguageEncoding">
      <psf:Value xsi:type="xs:string">_LanguageEncodingValue_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:LanguageVersion">
      <psf:Value xsi:type="xs:string">_LanguageVersionValue_</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
</psf:Feature>
      
```

## <a name="structure-variables"></a><span data-ttu-id="b007d-124">Variáveis de estrutura</span><span class="sxs-lookup"><span data-stu-id="b007d-124">Structure Variables</span></span>

<span data-ttu-id="b007d-125">A tabela a seguir descreve as características das variáveis definidas na estrutura XML.</span><span class="sxs-lookup"><span data-stu-id="b007d-125">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="b007d-126">Nome</span><span class="sxs-lookup"><span data-stu-id="b007d-126">Name</span></span>                                 | <span data-ttu-id="b007d-127">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="b007d-127">Data type</span></span>         | <span data-ttu-id="b007d-128">Unidade</span><span class="sxs-lookup"><span data-stu-id="b007d-128">Unit</span></span>                  | <span data-ttu-id="b007d-129">Valores com suporte</span><span class="sxs-lookup"><span data-stu-id="b007d-129">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="b007d-130">Resumo</span><span class="sxs-lookup"><span data-stu-id="b007d-130">Summary</span></span>                                                                      |
|--------------------------------------|-------------------|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="b007d-131">\_OptionName\_</span><span class="sxs-lookup"><span data-stu-id="b007d-131">\_OptionName\_</span></span><br/>            | <span data-ttu-id="b007d-132">string</span><span class="sxs-lookup"><span data-stu-id="b007d-132">string</span></span><br/> | <span data-ttu-id="b007d-133">characters</span><span class="sxs-lookup"><span data-stu-id="b007d-133">characters</span></span><br/> | <span data-ttu-id="b007d-134">Nome totalmente qualificado válido, conforme definido pelos [namespaces em XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span><span class="sxs-lookup"><span data-stu-id="b007d-134">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="b007d-135">Se nenhum namespace for especificado, o namespace padrão será assumido.</span><span class="sxs-lookup"><span data-stu-id="b007d-135">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="b007d-136">O nome da opção.</span><span class="sxs-lookup"><span data-stu-id="b007d-136">The name of the option.</span></span><br/>                                           |
| <span data-ttu-id="b007d-137">\_IdentityOptionValue\_</span><span class="sxs-lookup"><span data-stu-id="b007d-137">\_IdentityOptionValue\_</span></span><br/>   | <span data-ttu-id="b007d-138">string</span><span class="sxs-lookup"><span data-stu-id="b007d-138">string</span></span><br/> | <span data-ttu-id="b007d-139">N/D</span><span class="sxs-lookup"><span data-stu-id="b007d-139">n/a</span></span><br/>        | <span data-ttu-id="b007d-140">True, False.</span><span class="sxs-lookup"><span data-stu-id="b007d-140">True, False.</span></span><br/>                                                                                                                                                               | <span data-ttu-id="b007d-141">Define uma opção que, quando selecionada, desabilita esse recurso.</span><span class="sxs-lookup"><span data-stu-id="b007d-141">Defines an Option which when selected would disable this feature.</span></span><br/> |
| <span data-ttu-id="b007d-142">\_LanguageLevelValue\_</span><span class="sxs-lookup"><span data-stu-id="b007d-142">\_LanguageLevelValue\_</span></span><br/>    | <span data-ttu-id="b007d-143">string</span><span class="sxs-lookup"><span data-stu-id="b007d-143">string</span></span><br/> | <span data-ttu-id="b007d-144">N/D</span><span class="sxs-lookup"><span data-stu-id="b007d-144">n/a</span></span><br/>        | <span data-ttu-id="b007d-145">Nenhum.</span><span class="sxs-lookup"><span data-stu-id="b007d-145">None.</span></span><br/>                                                                                                                                                                      | <span data-ttu-id="b007d-146">Especifica o nível de linguagem (por exemplo, PS nível 2).</span><span class="sxs-lookup"><span data-stu-id="b007d-146">Specifies the language level (for example, PS Level 2).</span></span><br/>           |
| <span data-ttu-id="b007d-147">\_LanguageEncodingValue\_</span><span class="sxs-lookup"><span data-stu-id="b007d-147">\_LanguageEncodingValue\_</span></span><br/> | <span data-ttu-id="b007d-148">string</span><span class="sxs-lookup"><span data-stu-id="b007d-148">string</span></span><br/> | <span data-ttu-id="b007d-149">N/D</span><span class="sxs-lookup"><span data-stu-id="b007d-149">n/a</span></span><br/>        | <span data-ttu-id="b007d-150">Nenhum.</span><span class="sxs-lookup"><span data-stu-id="b007d-150">None.</span></span><br/>                                                                                                                                                                      | <span data-ttu-id="b007d-151">Especifica a codificação de idioma (por exemplo, ISOLatin1).</span><span class="sxs-lookup"><span data-stu-id="b007d-151">Specifies the language encoding (for example, ISOLatin1).</span></span><br/>         |
| <span data-ttu-id="b007d-152">\_LanguageVersionValue\_</span><span class="sxs-lookup"><span data-stu-id="b007d-152">\_LanguageVersionValue\_</span></span><br/>  | <span data-ttu-id="b007d-153">string</span><span class="sxs-lookup"><span data-stu-id="b007d-153">string</span></span><br/> | <span data-ttu-id="b007d-154">N/D</span><span class="sxs-lookup"><span data-stu-id="b007d-154">n/a</span></span><br/>        | <span data-ttu-id="b007d-155">Nenhum.</span><span class="sxs-lookup"><span data-stu-id="b007d-155">None.</span></span><br/>                                                                                                                                                                      | <span data-ttu-id="b007d-156">Especifica a versão do idioma.</span><span class="sxs-lookup"><span data-stu-id="b007d-156">Specifies the language version.</span></span><br/>                                   |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="b007d-157">Conteúdo de linguagem XML (XML)</span><span class="sxs-lookup"><span data-stu-id="b007d-157">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="b007d-158">As palavras-chave do esquema de impressão pública são definidas no https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span><span class="sxs-lookup"><span data-stu-id="b007d-158">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="b007d-159">O conteúdo do linguagem XML público (XML) para essa palavra-chave é definido abaixo:</span><span class="sxs-lookup"><span data-stu-id="b007d-159">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

``` syntax
<psf:Feature name="psk:JobDeviceLanguage">
  <psf:Property name="psf:SelectionType">
    <psf:Value xsi:type="xs:string">psk:PickOne</psf:Value>
  </psf:Property>
  <!--Specifies device language is XPS-->
  <psf:Option name="psk:XPS">
    <psf:ScoredProperty name="psk:LanguageLevel">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:LanguageEncoding">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:LanguageVersion">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <!--Specifies device language is PC-PR201 -->
  <psf:Option name="psk:_201PL">
    <psf:ScoredProperty name="psk:LanguageLevel">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:LanguageEncoding">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:LanguageVersion">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <!--Specified device language is ART -->
  <psf:Option name="psk:ART">
    <psf:ScoredProperty name="psk:LanguageLevel">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:LanguageEncoding">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:LanguageVersion">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <!--Specified device language is ASCII -->
  <psf:Option name="psk:ASCII">
    <psf:ScoredProperty name="psk:LanguageLevel">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:LanguageEncoding">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:LanguageVersion">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <!--Specified device language is CaPSL-->
  <psf:Option name="psk:CaPSL">
    <psf:ScoredProperty name="psk:LanguageLevel">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:LanguageEncoding">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:LanguageVersion">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <!--Specified device language is ESC/P2-->
  <psf:Option name="psk:ESCP2">
    <psf:ScoredProperty name="psk:LanguageLevel">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:LanguageEncoding">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:LanguageVersion">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <!--Specified device language is ESC/Page-->
  <psf:Option name="psk:ESCPage">
    <psf:ScoredProperty name="psk:LanguageLevel">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:LanguageEncoding">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:LanguageVersion">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <!--Specified device language is HP-GL/2-->
  <psf:Option name="psk:HPGL2">
    <psf:ScoredProperty name="psk:LanguageLevel">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:LanguageEncoding">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:LanguageVersion">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <!--Specified device language is KPDL -->
  <psf:Option name="psk:KPDL">
    <psf:ScoredProperty name="psk:LanguageLevel">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:LanguageEncoding">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:LanguageVersion">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <!--Specified device language is KS -->
  <psf:Option name="psk:KS">
    <psf:ScoredProperty name="psk:LanguageLevel">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:LanguageEncoding">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:LanguageVersion">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <!--Specified device language is KSSM -->
  <psf:Option name="psk:KSSM">
    <psf:ScoredProperty name="psk:LanguageLevel">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:LanguageEncoding">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:LanguageVersion">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <!--Specified device language is PCL -->
  <psf:Option name="psk:PCL">
    <psf:ScoredProperty name="psk:LanguageLevel">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:LanguageEncoding">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:LanguageVersion">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <!--Specified device language is PCL5c -->
  <psf:Option name="psk:PCL5c">
    <psf:ScoredProperty name="LanguageLevel">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:LanguageEncoding">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:LanguageVersion">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <!--Specified device language is PCL5e -->
  <psf:Option name="psk:PCL5e">
    <psf:ScoredProperty name="psk:LanguageLevel">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:LanguageEncoding">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:LanguageVersion">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <!--Specified device language is PCL-XL -->
  <psf:Option name="psk:PCL-XL">
    <psf:ScoredProperty name="psk:LanguageLevel">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:LanguageEncoding">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:LanguageVersion">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <!--Specified device language is PostScript -->
  <psf:Option name="psk:PostScript">
    <psf:ScoredProperty name="psk:LanguageLevel">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:LanguageEncoding">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:LanguageVersion">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <!--Specified device language is PPDS -->
  <psf:Option name="psk:PPDS">
    <psf:ScoredProperty name="psk:LanguageLevel">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:LanguageEncoding">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:LanguageVersion">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <!--Specified device language is RPDL -->
  <psf:Option name="psk:RPDL">
    <psf:ScoredProperty name="psk:LanguageLevel">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:LanguageEncoding">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:LanguageVersion">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <!--Specified device language is RTL -->
  <psf:Option name="psk:RTL">
    <psf:ScoredProperty name="psk:LanguageLevel">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:LanguageEncoding">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:LanguageVersion">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
</psf:Feature>    
```

## <a name="related-topics"></a><span data-ttu-id="b007d-160">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="b007d-160">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b007d-161">Especificação de esquema de impressão</span><span class="sxs-lookup"><span data-stu-id="b007d-161">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




