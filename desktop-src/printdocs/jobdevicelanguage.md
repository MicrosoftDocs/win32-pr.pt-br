---
description: Este tópico não é atual. Para obter as informações mais atuais, consulte a especificação do esquema de impressão.
ms.assetid: 3894d9fa-2bf7-447a-bac3-e72a0fdb7187
title: JobDeviceLanguage
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: da5b128cd8a0bd06cc259d3da0daf834f3c2aebf
ms.sourcegitcommit: 7b8f6151ebe247536304866459b2973276271d4d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/06/2021
ms.locfileid: "104298044"
---
# <a name="jobdevicelanguage"></a><span data-ttu-id="699a2-104">JobDeviceLanguage</span><span class="sxs-lookup"><span data-stu-id="699a2-104">JobDeviceLanguage</span></span>

<span data-ttu-id="699a2-105">Este tópico não é atual.</span><span class="sxs-lookup"><span data-stu-id="699a2-105">This topic is not current.</span></span> <span data-ttu-id="699a2-106">Para obter as informações mais atuais, consulte a [especificação do esquema de impressão](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="699a2-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="699a2-107">Descreve os idiomas de dispositivo com suporte para enviar dados do driver para o dispositivo físico.</span><span class="sxs-lookup"><span data-stu-id="699a2-107">Describes the device languages supported for sending data from driver to physical device.</span></span> <span data-ttu-id="699a2-108">Isso geralmente é chamado de "linguagem de descrição de página".</span><span class="sxs-lookup"><span data-stu-id="699a2-108">This is often called "Page Description Language".</span></span> <span data-ttu-id="699a2-109">Essa palavra-chave define qual linguagem de descrição de página é suportada pelo driver e pelo dispositivo físico.</span><span class="sxs-lookup"><span data-stu-id="699a2-109">This keyword defines what page description language is supported by the driver and physical device.</span></span>

-   [<span data-ttu-id="699a2-110">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="699a2-110">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="699a2-111">Conteúdo estrutural</span><span class="sxs-lookup"><span data-stu-id="699a2-111">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="699a2-112">Conteúdo de linguagem XML (XML)</span><span class="sxs-lookup"><span data-stu-id="699a2-112">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="699a2-113">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="699a2-113">Element Information</span></span>



| <span data-ttu-id="699a2-114">Nome</span><span class="sxs-lookup"><span data-stu-id="699a2-114">Name</span></span>                       |                    |
|----------------------------|--------------------|
| <span data-ttu-id="699a2-115">Tipo de elemento</span><span class="sxs-lookup"><span data-stu-id="699a2-115">Element Type</span></span> <br/>   | <span data-ttu-id="699a2-116">Recurso</span><span class="sxs-lookup"><span data-stu-id="699a2-116">Feature</span></span><br/> |
| <span data-ttu-id="699a2-117">Prefixo de escopo</span><span class="sxs-lookup"><span data-stu-id="699a2-117">Scoping Prefix</span></span> <br/> | <span data-ttu-id="699a2-118">Trabalho</span><span class="sxs-lookup"><span data-stu-id="699a2-118">Job</span></span><br/>     |
| <span data-ttu-id="699a2-119">Observações</span><span class="sxs-lookup"><span data-stu-id="699a2-119">Notes</span></span> <br/>          | <span data-ttu-id="699a2-120">Nenhum</span><span class="sxs-lookup"><span data-stu-id="699a2-120">None</span></span><br/>    |



 

## <a name="structural-content"></a><span data-ttu-id="699a2-121">Conteúdo estrutural</span><span class="sxs-lookup"><span data-stu-id="699a2-121">Structural Content</span></span>

<span data-ttu-id="699a2-122">A estrutura XML desse elemento é:</span><span class="sxs-lookup"><span data-stu-id="699a2-122">The XML structure of this element is:</span></span>

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

## <a name="structure-variables"></a><span data-ttu-id="699a2-123">Variáveis de estrutura</span><span class="sxs-lookup"><span data-stu-id="699a2-123">Structure Variables</span></span>

<span data-ttu-id="699a2-124">A tabela a seguir descreve as características das variáveis definidas na estrutura XML.</span><span class="sxs-lookup"><span data-stu-id="699a2-124">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="699a2-125">Nome</span><span class="sxs-lookup"><span data-stu-id="699a2-125">Name</span></span>                                 | <span data-ttu-id="699a2-126">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="699a2-126">Data type</span></span>         | <span data-ttu-id="699a2-127">Unidade</span><span class="sxs-lookup"><span data-stu-id="699a2-127">Unit</span></span>                  | <span data-ttu-id="699a2-128">Valores com suporte</span><span class="sxs-lookup"><span data-stu-id="699a2-128">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="699a2-129">Resumo</span><span class="sxs-lookup"><span data-stu-id="699a2-129">Summary</span></span>                                                                      |
|--------------------------------------|-------------------|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="699a2-130">\_OptionName\_</span><span class="sxs-lookup"><span data-stu-id="699a2-130">\_OptionName\_</span></span><br/>            | <span data-ttu-id="699a2-131">string</span><span class="sxs-lookup"><span data-stu-id="699a2-131">string</span></span><br/> | <span data-ttu-id="699a2-132">characters</span><span class="sxs-lookup"><span data-stu-id="699a2-132">characters</span></span><br/> | <span data-ttu-id="699a2-133">Nome totalmente qualificado válido, conforme definido pelos [namespaces em XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span><span class="sxs-lookup"><span data-stu-id="699a2-133">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="699a2-134">Se nenhum namespace for especificado, o namespace padrão será assumido.</span><span class="sxs-lookup"><span data-stu-id="699a2-134">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="699a2-135">O nome da opção.</span><span class="sxs-lookup"><span data-stu-id="699a2-135">The name of the option.</span></span><br/>                                           |
| <span data-ttu-id="699a2-136">\_IdentityOptionValue\_</span><span class="sxs-lookup"><span data-stu-id="699a2-136">\_IdentityOptionValue\_</span></span><br/>   | <span data-ttu-id="699a2-137">string</span><span class="sxs-lookup"><span data-stu-id="699a2-137">string</span></span><br/> | <span data-ttu-id="699a2-138">N/D</span><span class="sxs-lookup"><span data-stu-id="699a2-138">n/a</span></span><br/>        | <span data-ttu-id="699a2-139">True, False.</span><span class="sxs-lookup"><span data-stu-id="699a2-139">True, False.</span></span><br/>                                                                                                                                                               | <span data-ttu-id="699a2-140">Define uma opção que, quando selecionada, desabilita esse recurso.</span><span class="sxs-lookup"><span data-stu-id="699a2-140">Defines an Option which when selected would disable this feature.</span></span><br/> |
| <span data-ttu-id="699a2-141">\_LanguageLevelValue\_</span><span class="sxs-lookup"><span data-stu-id="699a2-141">\_LanguageLevelValue\_</span></span><br/>    | <span data-ttu-id="699a2-142">string</span><span class="sxs-lookup"><span data-stu-id="699a2-142">string</span></span><br/> | <span data-ttu-id="699a2-143">N/D</span><span class="sxs-lookup"><span data-stu-id="699a2-143">n/a</span></span><br/>        | <span data-ttu-id="699a2-144">Nenhum.</span><span class="sxs-lookup"><span data-stu-id="699a2-144">None.</span></span><br/>                                                                                                                                                                      | <span data-ttu-id="699a2-145">Especifica o nível de linguagem (por exemplo, PS nível 2).</span><span class="sxs-lookup"><span data-stu-id="699a2-145">Specifies the language level (for example, PS Level 2).</span></span><br/>           |
| <span data-ttu-id="699a2-146">\_LanguageEncodingValue\_</span><span class="sxs-lookup"><span data-stu-id="699a2-146">\_LanguageEncodingValue\_</span></span><br/> | <span data-ttu-id="699a2-147">string</span><span class="sxs-lookup"><span data-stu-id="699a2-147">string</span></span><br/> | <span data-ttu-id="699a2-148">N/D</span><span class="sxs-lookup"><span data-stu-id="699a2-148">n/a</span></span><br/>        | <span data-ttu-id="699a2-149">Nenhum.</span><span class="sxs-lookup"><span data-stu-id="699a2-149">None.</span></span><br/>                                                                                                                                                                      | <span data-ttu-id="699a2-150">Especifica a codificação de idioma (por exemplo, ISOLatin1).</span><span class="sxs-lookup"><span data-stu-id="699a2-150">Specifies the language encoding (for example, ISOLatin1).</span></span><br/>         |
| <span data-ttu-id="699a2-151">\_LanguageVersionValue\_</span><span class="sxs-lookup"><span data-stu-id="699a2-151">\_LanguageVersionValue\_</span></span><br/>  | <span data-ttu-id="699a2-152">string</span><span class="sxs-lookup"><span data-stu-id="699a2-152">string</span></span><br/> | <span data-ttu-id="699a2-153">N/D</span><span class="sxs-lookup"><span data-stu-id="699a2-153">n/a</span></span><br/>        | <span data-ttu-id="699a2-154">Nenhum.</span><span class="sxs-lookup"><span data-stu-id="699a2-154">None.</span></span><br/>                                                                                                                                                                      | <span data-ttu-id="699a2-155">Especifica a versão do idioma.</span><span class="sxs-lookup"><span data-stu-id="699a2-155">Specifies the language version.</span></span><br/>                                   |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="699a2-156">Conteúdo de linguagem XML (XML)</span><span class="sxs-lookup"><span data-stu-id="699a2-156">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="699a2-157">As palavras-chave do esquema de impressão pública são definidas no https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span><span class="sxs-lookup"><span data-stu-id="699a2-157">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="699a2-158">O conteúdo do linguagem XML público (XML) para essa palavra-chave é definido abaixo:</span><span class="sxs-lookup"><span data-stu-id="699a2-158">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

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

## <a name="related-topics"></a><span data-ttu-id="699a2-159">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="699a2-159">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="699a2-160">Especificação de esquema de impressão</span><span class="sxs-lookup"><span data-stu-id="699a2-160">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




