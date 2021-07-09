---
description: Saiba mais sobre o elemento PageMediaColor configurável pelo usuário. Este tópico não é atual. Para obter as informações mais atuais, consulte a especificação do esquema de impressão.
ms.assetid: 3e0e2cb2-cb51-446d-a6ff-f76aa8c305f6
title: PageMediaColor
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3041c8954048f60f52e9324f0c6565396d7fafe2
ms.sourcegitcommit: 998d50f6def8a25850fc113fc8a2df903c829c5e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/09/2021
ms.locfileid: "113549154"
---
# <a name="pagemediacolor"></a><span data-ttu-id="0a1c5-105">PageMediaColor</span><span class="sxs-lookup"><span data-stu-id="0a1c5-105">PageMediaColor</span></span>

<span data-ttu-id="0a1c5-106">Este tópico não é atual.</span><span class="sxs-lookup"><span data-stu-id="0a1c5-106">This topic is not current.</span></span> <span data-ttu-id="0a1c5-107">Para obter as informações mais atuais, consulte a [especificação do esquema de impressão](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="0a1c5-107">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="0a1c5-108">Descreve as opções de cores de mídia e as características de cada opção.</span><span class="sxs-lookup"><span data-stu-id="0a1c5-108">Describes the Media Color options and the characteristics of each option.</span></span>

-   [<span data-ttu-id="0a1c5-109">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="0a1c5-109">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="0a1c5-110">Conteúdo estrutural</span><span class="sxs-lookup"><span data-stu-id="0a1c5-110">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="0a1c5-111">Conteúdo de linguagem XML (XML)</span><span class="sxs-lookup"><span data-stu-id="0a1c5-111">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="0a1c5-112">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="0a1c5-112">Element Information</span></span>



| <span data-ttu-id="0a1c5-113">Nome</span><span class="sxs-lookup"><span data-stu-id="0a1c5-113">Name</span></span> | <span data-ttu-id="0a1c5-114">Valor</span><span class="sxs-lookup"><span data-stu-id="0a1c5-114">Value</span></span> |
|----------------------------|--------------------|
| <span data-ttu-id="0a1c5-115">Tipo de elemento</span><span class="sxs-lookup"><span data-stu-id="0a1c5-115">Element Type</span></span> <br/>   | <span data-ttu-id="0a1c5-116">Recurso</span><span class="sxs-lookup"><span data-stu-id="0a1c5-116">Feature</span></span><br/> |
| <span data-ttu-id="0a1c5-117">Prefixo de escopo</span><span class="sxs-lookup"><span data-stu-id="0a1c5-117">Scoping Prefix</span></span> <br/> | <span data-ttu-id="0a1c5-118">Página</span><span class="sxs-lookup"><span data-stu-id="0a1c5-118">Page</span></span><br/>    |
| <span data-ttu-id="0a1c5-119">Observações</span><span class="sxs-lookup"><span data-stu-id="0a1c5-119">Notes</span></span> <br/>          | <span data-ttu-id="0a1c5-120">Nenhum</span><span class="sxs-lookup"><span data-stu-id="0a1c5-120">None</span></span><br/>    |



 

## <a name="structural-content"></a><span data-ttu-id="0a1c5-121">Conteúdo estrutural</span><span class="sxs-lookup"><span data-stu-id="0a1c5-121">Structural Content</span></span>

<span data-ttu-id="0a1c5-122">A estrutura XML desse elemento é:</span><span class="sxs-lookup"><span data-stu-id="0a1c5-122">The XML structure of this element is:</span></span>

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

## <a name="structure-variables"></a><span data-ttu-id="0a1c5-123">Variáveis de estrutura</span><span class="sxs-lookup"><span data-stu-id="0a1c5-123">Structure Variables</span></span>

<span data-ttu-id="0a1c5-124">A tabela a seguir descreve as características das variáveis definidas na estrutura XML.</span><span class="sxs-lookup"><span data-stu-id="0a1c5-124">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="0a1c5-125">Nome</span><span class="sxs-lookup"><span data-stu-id="0a1c5-125">Name</span></span>                               | <span data-ttu-id="0a1c5-126">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="0a1c5-126">Data type</span></span>         | <span data-ttu-id="0a1c5-127">Unidade</span><span class="sxs-lookup"><span data-stu-id="0a1c5-127">Unit</span></span>                  | <span data-ttu-id="0a1c5-128">Valores com suporte</span><span class="sxs-lookup"><span data-stu-id="0a1c5-128">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="0a1c5-129">Resumo</span><span class="sxs-lookup"><span data-stu-id="0a1c5-129">Summary</span></span>                                                                      |
|------------------------------------|-------------------|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="0a1c5-130">\_OptionName\_</span><span class="sxs-lookup"><span data-stu-id="0a1c5-130">\_OptionName\_</span></span><br/>          | <span data-ttu-id="0a1c5-131">string</span><span class="sxs-lookup"><span data-stu-id="0a1c5-131">string</span></span><br/> | <span data-ttu-id="0a1c5-132">characters</span><span class="sxs-lookup"><span data-stu-id="0a1c5-132">characters</span></span><br/> | <span data-ttu-id="0a1c5-133">Nome totalmente qualificado válido, conforme definido pelos [namespaces em XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span><span class="sxs-lookup"><span data-stu-id="0a1c5-133">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="0a1c5-134">Se nenhum namespace for especificado, o namespace padrão será assumido.</span><span class="sxs-lookup"><span data-stu-id="0a1c5-134">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="0a1c5-135">O nome da opção.</span><span class="sxs-lookup"><span data-stu-id="0a1c5-135">The name of the option.</span></span><br/>                                           |
| <span data-ttu-id="0a1c5-136">\_IdentityOptionValue\_</span><span class="sxs-lookup"><span data-stu-id="0a1c5-136">\_IdentityOptionValue\_</span></span><br/> | <span data-ttu-id="0a1c5-137">string</span><span class="sxs-lookup"><span data-stu-id="0a1c5-137">string</span></span><br/> | <span data-ttu-id="0a1c5-138">n/d</span><span class="sxs-lookup"><span data-stu-id="0a1c5-138">n/a</span></span><br/>        | <span data-ttu-id="0a1c5-139">True, False.</span><span class="sxs-lookup"><span data-stu-id="0a1c5-139">True, False.</span></span><br/>                                                                                                                                                               | <span data-ttu-id="0a1c5-140">Define uma opção que, quando selecionada, desabilita esse recurso.</span><span class="sxs-lookup"><span data-stu-id="0a1c5-140">Defines an Option which when selected would disable this feature.</span></span><br/> |
| <span data-ttu-id="0a1c5-141">\_MediaColorsRGBValue\_</span><span class="sxs-lookup"><span data-stu-id="0a1c5-141">\_MediaColorsRGBValue\_</span></span><br/> | <span data-ttu-id="0a1c5-142">string</span><span class="sxs-lookup"><span data-stu-id="0a1c5-142">string</span></span><br/> | <span data-ttu-id="0a1c5-143">Cor sRGB</span><span class="sxs-lookup"><span data-stu-id="0a1c5-143">sRGB Color</span></span><br/> | <span data-ttu-id="0a1c5-144">\#AARRGGBB, em que A, R, G, B representa dígitos hexadecimais.</span><span class="sxs-lookup"><span data-stu-id="0a1c5-144">\#AARRGGBB where A, R, G, B represent hexadecimal digits.</span></span><br/>                                                                                                                  | <span data-ttu-id="0a1c5-145">Define a cor sRGB para a folha de mídia física.</span><span class="sxs-lookup"><span data-stu-id="0a1c5-145">Defines the sRGB color for the physical media sheet.</span></span> <br/>             |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="0a1c5-146">Conteúdo de linguagem XML (XML)</span><span class="sxs-lookup"><span data-stu-id="0a1c5-146">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="0a1c5-147">As palavras-chave do esquema de impressão pública são definidas no `https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords` namespace.</span><span class="sxs-lookup"><span data-stu-id="0a1c5-147">The public Print Schema keywords are defined in the `https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords` namespace.</span></span> <span data-ttu-id="0a1c5-148">O conteúdo do linguagem XML público (XML) para essa palavra-chave é definido abaixo:</span><span class="sxs-lookup"><span data-stu-id="0a1c5-148">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

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

## <a name="related-topics"></a><span data-ttu-id="0a1c5-149">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="0a1c5-149">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0a1c5-150">Especificação de esquema de impressão</span><span class="sxs-lookup"><span data-stu-id="0a1c5-150">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>
