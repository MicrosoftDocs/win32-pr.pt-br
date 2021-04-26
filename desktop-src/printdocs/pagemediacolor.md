---
description: Este tópico não é atual. Para obter as informações mais atuais, consulte a especificação do esquema de impressão.
ms.assetid: 3e0e2cb2-cb51-446d-a6ff-f76aa8c305f6
title: PageMediaColor
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 60c9a314bf435664d121fd35e588b62903da323e
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/26/2021
ms.locfileid: "107994503"
---
# <a name="pagemediacolor"></a><span data-ttu-id="b7435-104">PageMediaColor</span><span class="sxs-lookup"><span data-stu-id="b7435-104">PageMediaColor</span></span>

<span data-ttu-id="b7435-105">Este tópico não é atual.</span><span class="sxs-lookup"><span data-stu-id="b7435-105">This topic is not current.</span></span> <span data-ttu-id="b7435-106">Para obter as informações mais atuais, consulte a [especificação do esquema de impressão](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="b7435-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="b7435-107">Descreve as opções de cores de mídia e as características de cada opção.</span><span class="sxs-lookup"><span data-stu-id="b7435-107">Describes the Media Color options and the characteristics of each option.</span></span>

-   [<span data-ttu-id="b7435-108">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="b7435-108">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="b7435-109">Conteúdo estrutural</span><span class="sxs-lookup"><span data-stu-id="b7435-109">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="b7435-110">Conteúdo de linguagem XML (XML)</span><span class="sxs-lookup"><span data-stu-id="b7435-110">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="b7435-111">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="b7435-111">Element Information</span></span>



| <span data-ttu-id="b7435-112">Nome</span><span class="sxs-lookup"><span data-stu-id="b7435-112">Name</span></span> | <span data-ttu-id="b7435-113">Valor</span><span class="sxs-lookup"><span data-stu-id="b7435-113">Value</span></span> |
|----------------------------|--------------------|
| <span data-ttu-id="b7435-114">Tipo de elemento</span><span class="sxs-lookup"><span data-stu-id="b7435-114">Element Type</span></span> <br/>   | <span data-ttu-id="b7435-115">Recurso</span><span class="sxs-lookup"><span data-stu-id="b7435-115">Feature</span></span><br/> |
| <span data-ttu-id="b7435-116">Prefixo de escopo</span><span class="sxs-lookup"><span data-stu-id="b7435-116">Scoping Prefix</span></span> <br/> | <span data-ttu-id="b7435-117">?</span><span class="sxs-lookup"><span data-stu-id="b7435-117">Page</span></span><br/>    |
| <span data-ttu-id="b7435-118">Observações</span><span class="sxs-lookup"><span data-stu-id="b7435-118">Notes</span></span> <br/>          | <span data-ttu-id="b7435-119">Nenhum</span><span class="sxs-lookup"><span data-stu-id="b7435-119">None</span></span><br/>    |



 

## <a name="structural-content"></a><span data-ttu-id="b7435-120">Conteúdo estrutural</span><span class="sxs-lookup"><span data-stu-id="b7435-120">Structural Content</span></span>

<span data-ttu-id="b7435-121">A estrutura XML desse elemento é:</span><span class="sxs-lookup"><span data-stu-id="b7435-121">The XML structure of this element is:</span></span>

``` syntax
<psf:Feature name="psk:PageMediaColor">
  <psf:Property name="psf:SelectionType">
    <psf:Value xsi:type="xs:string">psk:PickOne</psf:Value>
  </psf:Property>
  <psf:Option name="psk:_OptionName_">
    <psf:Property name="psf:IdentityOption">
      <psf:Value xsi:type="xs:string">_IdentityOptionValue_</psf:Value>
    </psf:Property>
    <psf:ScoredProperty name="psk:MediaColorsRGB">
      <psf:Value xsi:type="xs:string">_MediaColorsRGBValue_</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
</psf:Feature>
      
```

## <a name="structure-variables"></a><span data-ttu-id="b7435-122">Variáveis de estrutura</span><span class="sxs-lookup"><span data-stu-id="b7435-122">Structure Variables</span></span>

<span data-ttu-id="b7435-123">A tabela a seguir descreve as características das variáveis definidas na estrutura XML.</span><span class="sxs-lookup"><span data-stu-id="b7435-123">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="b7435-124">Nome</span><span class="sxs-lookup"><span data-stu-id="b7435-124">Name</span></span>                               | <span data-ttu-id="b7435-125">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="b7435-125">Data type</span></span>         | <span data-ttu-id="b7435-126">Unidade</span><span class="sxs-lookup"><span data-stu-id="b7435-126">Unit</span></span>                  | <span data-ttu-id="b7435-127">Valores com suporte</span><span class="sxs-lookup"><span data-stu-id="b7435-127">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="b7435-128">Resumo</span><span class="sxs-lookup"><span data-stu-id="b7435-128">Summary</span></span>                                                                      |
|------------------------------------|-------------------|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="b7435-129">\_OptionName\_</span><span class="sxs-lookup"><span data-stu-id="b7435-129">\_OptionName\_</span></span><br/>          | <span data-ttu-id="b7435-130">string</span><span class="sxs-lookup"><span data-stu-id="b7435-130">string</span></span><br/> | <span data-ttu-id="b7435-131">characters</span><span class="sxs-lookup"><span data-stu-id="b7435-131">characters</span></span><br/> | <span data-ttu-id="b7435-132">Nome totalmente qualificado válido, conforme definido pelos [namespaces em XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span><span class="sxs-lookup"><span data-stu-id="b7435-132">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="b7435-133">Se nenhum namespace for especificado, o namespace padrão será assumido.</span><span class="sxs-lookup"><span data-stu-id="b7435-133">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="b7435-134">O nome da opção.</span><span class="sxs-lookup"><span data-stu-id="b7435-134">The name of the option.</span></span><br/>                                           |
| <span data-ttu-id="b7435-135">\_IdentityOptionValue\_</span><span class="sxs-lookup"><span data-stu-id="b7435-135">\_IdentityOptionValue\_</span></span><br/> | <span data-ttu-id="b7435-136">string</span><span class="sxs-lookup"><span data-stu-id="b7435-136">string</span></span><br/> | <span data-ttu-id="b7435-137">N/D</span><span class="sxs-lookup"><span data-stu-id="b7435-137">n/a</span></span><br/>        | <span data-ttu-id="b7435-138">True, False.</span><span class="sxs-lookup"><span data-stu-id="b7435-138">True, False.</span></span><br/>                                                                                                                                                               | <span data-ttu-id="b7435-139">Define uma opção que, quando selecionada, desabilita esse recurso.</span><span class="sxs-lookup"><span data-stu-id="b7435-139">Defines an Option which when selected would disable this feature.</span></span><br/> |
| <span data-ttu-id="b7435-140">\_MediaColorsRGBValue\_</span><span class="sxs-lookup"><span data-stu-id="b7435-140">\_MediaColorsRGBValue\_</span></span><br/> | <span data-ttu-id="b7435-141">string</span><span class="sxs-lookup"><span data-stu-id="b7435-141">string</span></span><br/> | <span data-ttu-id="b7435-142">Cor sRGB</span><span class="sxs-lookup"><span data-stu-id="b7435-142">sRGB Color</span></span><br/> | <span data-ttu-id="b7435-143">\#AARRGGBB, em que A, R, G, B representa dígitos hexadecimais.</span><span class="sxs-lookup"><span data-stu-id="b7435-143">\#AARRGGBB where A, R, G, B represent hexadecimal digits.</span></span><br/>                                                                                                                  | <span data-ttu-id="b7435-144">Define a cor sRGB para a folha de mídia física.</span><span class="sxs-lookup"><span data-stu-id="b7435-144">Defines the sRGB color for the physical media sheet.</span></span> <br/>             |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="b7435-145">Conteúdo de linguagem XML (XML)</span><span class="sxs-lookup"><span data-stu-id="b7435-145">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="b7435-146">As palavras-chave do esquema de impressão pública são definidas no `https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords` namespace.</span><span class="sxs-lookup"><span data-stu-id="b7435-146">The public Print Schema keywords are defined in the `https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords` namespace.</span></span> <span data-ttu-id="b7435-147">O conteúdo do linguagem XML público (XML) para essa palavra-chave é definido abaixo:</span><span class="sxs-lookup"><span data-stu-id="b7435-147">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

``` syntax
<psf:Feature name="psk:PageMediaColor">
  <psf:Property name="psf:SelectionType">
    <psf:Value xsi:type="xs:string">psk:PickOne</psf:Value>
  </psf:Property>
  <psf:Option name="psk:Black">
    <psf:ScoredProperty name="psk:MediaColorsRGB">
      <psf:Value xsi:type="xs:string">#FF000000</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:Blue">
    <psf:ScoredProperty name="psk:MediaColorsRGB">
      <psf:Value xsi:type="xs:string">#FF0000FF</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:Brown">
    <psf:ScoredProperty name="psk:MediaColorsRGB">
      <psf:Value xsi:type="xs:string">#FFA52A2A</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:Gold">
    <psf:ScoredProperty name="psk:MediaColorsRGB">
      <psf:Value xsi:type="xs:string">#FFFFD700</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:GoldenRod">
    <psf:ScoredProperty name="psk:MediaColorsRGB">
      <psf:Value xsi:type="xs:string">#FFDAA520</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:Gray">
    <psf:ScoredProperty name="psk:MediaColorsRGB">
      <psf:Value xsi:type="xs:string">#FF808080</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:Green">
    <psf:ScoredProperty name="psk:MediaColorsRGB">
      <psf:Value xsi:type="xs:string">#FF008000</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:Ivory">
    <psf:ScoredProperty name="psk:MediaColorsRGB">
      <psf:Value xsi:type="xs:string">#FFFFFFF0</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:NoColor">
    <psf:ScoredProperty name="psk:MediaColorsRGB">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:Orange">
    <psf:ScoredProperty name="psk:MediaColorsRGB">
      <psf:Value xsi:type="xs:string">#FFFFA500</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:Pink">
    <psf:ScoredProperty name="psk:MediaColorsRGB">
      <psf:Value xsi:type="xs:string">#FFFFC0CB</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:Red">
    <psf:ScoredProperty name="psk:MediaColorsRGB">
      <psf:Value xsi:type="xs:string">#FFFF0000</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:Silver">
    <psf:ScoredProperty name="psk:MediaColorsRGB">
      <psf:Value xsi:type="xs:string">#FFC0C0C0</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:Turquoise">
    <psf:ScoredProperty name="psk:MediaColorsRGB">
      <psf:Value xsi:type="xs:string">#FF40E0D0</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:Violet">
    <psf:ScoredProperty name="psk:MediaColorsRGB">
      <psf:Value xsi:type="xs:string">#FFEE82EE</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:White">
    <psf:ScoredProperty name="psk:MediaColorsRGB">
      <psf:Value xsi:type="xs:string">#FFFFFFFF</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:Yellow">
    <psf:ScoredProperty name="psk:MediaColorsRGB">
      <psf:Value xsi:type="xs:string">#FFFFFF00</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <!-- Specifies a custom page color. -->
  <psf:Option name="psk:Custom">
    <psf:ScoredProperty name="psk:MediaColorsRGB">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
</psf:Feature>
```

## <a name="related-topics"></a><span data-ttu-id="b7435-148">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="b7435-148">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b7435-149">Especificação de esquema de impressão</span><span class="sxs-lookup"><span data-stu-id="b7435-149">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>
