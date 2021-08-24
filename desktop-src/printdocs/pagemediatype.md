---
description: Obtenha informações sobre o elemento PageMediaType configurável pelo usuário. Este tópico não é atual. Para obter as informações mais atuais, consulte a especificação do esquema de impressão.
ms.assetid: 29d7ae65-9dd3-4a29-8e5e-79708638a3bb
title: PageMediaType
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 50e7da5d4cdad5b17324e5e628b5b9e8d0cac1c0ebfaded11379c836d5245a0a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119098840"
---
# <a name="pagemediatype"></a>PageMediaType

Este tópico não é atual. Para obter as informações mais atuais, consulte a [especificação do esquema de impressão](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).

Descreve as opções de MediaType e as características de cada opção.

-   [Informações do elemento](#element-information)
-   [Conteúdo estrutural](#structural-content)
-   [Conteúdo de linguagem XML (XML)](#extensible-markup-language-xml-content)

## <a name="element-information"></a>Informações do elemento



| Nome | Valor |
|----------------------------|--------------------|
| Tipo de elemento <br/>   | Recurso<br/> |
| Prefixo de escopo <br/> | ?<br/>    |
| Observações <br/>          | Nenhum<br/>    |



 

## <a name="structural-content"></a>Conteúdo estrutural

A estrutura XML desse elemento é:

``` syntax
<psf:Feature name="psk:PageMediaType">
  <psf:Property name="psf:SelectionType">
    <psf:Value xsi:type="xs:string">psk:PickOne</psf:Value>
  </psf:Property>
  <psf:Option name="psk:_OptionName_">
    <psf:Property name="psf:IdentityOption">
      <psf:Value xsi:type="xs:string">_IdentityOptionValue_</psf:Value>
    </psf:Property>
    <psf:ScoredProperty name="psk:BackCoating">
      <psf:Value xsi:type="xs:string">_BackCoatingValue_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:FrontCoating">
      <psf:Value xsi:type="xs:string">_FrontCoatingValue_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:Material">
      <psf:Value xsi:type="xs:string">_MaterialValue_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:PrePrinted">
      <psf:Value xsi:type="xs:string">_PrePrintedValue_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:PrePunched">
      <psf:Value xsi:type="xs:string">_PrePunchedValue_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:Recycled">
      <psf:Value xsi:type="xs:string">_RecycledValue_</psf:Value>
    </psf:ScoredProperty>     
    <psf:ScoredProperty name="psk:Weight">
      <psf:Value xsi:type="xs:integer">_WeightValue_</psf:Value>
    </psf:ScoredProperty> 
  </psf:Option>
</psf:Feature>
      
```

## <a name="structure-variables"></a>Variáveis de estrutura

A tabela a seguir descreve as características das variáveis definidas na estrutura XML.



| Nome                               | Tipo de dados          | Unidade                              | Valores com suporte                                                                                                                                                                      | Resumo                                                                      |
|------------------------------------|--------------------|-----------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| \_OptionName\_<br/>          | string<br/>  | characters<br/>             | Nome totalmente qualificado válido, conforme definido pelos [namespaces em XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/). Se nenhum namespace for especificado, o namespace padrão será assumido.<br/> | O nome da opção.<br/>                                           |
| \_IdentityOptionValue\_<br/> | string<br/>  | n/d<br/>                    | True, False.<br/>                                                                                                                                                               | Define uma opção que, quando selecionada, desabilita esse recurso.<br/> |
| \_Backrevestimentovalue\_<br/>    | string<br/>  | n/d<br/>                    | Glossa, HighGloss, fosco, None, acetinado, SemiGloss.<br/>                                                                                                                          | Especifica o revestimento do lado do verso da mídia.<br/>              |
| \_FrontCoatingValue\_<br/>   | string<br/>  | n/d<br/>                    | Glossa, HighGloss, fosco, None, acetinado, SemiGloss.<br/>                                                                                                                          | Especifica o revestimento do lado frontal da mídia.<br/>             |
| \_Materialvalue\_<br/>       | string<br/>  | n/d<br/>                    | Alumínio, exibição, DryFilm, papel, polyester, transparência, WetFilm.<br/>                                                                                                       | Especifica o material do qual a mídia é desfeita.<br/>                  |
| \_Pré-impresso\_<br/>     | string<br/>  | n/d<br/>                    | Nenhum, pré-impresso, papel timbrado.<br/>                                                                                                                                              | Especifica as características da mídia impressa.<br/>                       |
| \_PrePunchedValue\_<br/>     | string<br/>  | n/d<br/>                    | Nenhum, perfurado.<br/>                                                                                                                                                          | Especifica as características de mídias prefuradas.<br/>                       |
| \_Reciclador\_<br/>       | string<br/>  | n/d<br/>                    | Nenhum, padrão.<br/>                                                                                                                                                            | Especifica as características de mídia reciclada.<br/>                         |
| \_Pesovalue\_<br/>         | Número inteiro<br/> | gramas por metro quadrado<br/> | Maior que 0.<br/>                                                                                                                                                            | Especifica características de peso de mídia.<br/>                           |



 

## <a name="extensible-markup-language-xml-content"></a>Conteúdo de linguagem XML (XML)

As palavras-chave do esquema de impressão pública são definidas no `https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords` namespace. O conteúdo do linguagem XML público (XML) para essa palavra-chave é definido abaixo:

``` syntax
<psf:Feature name="psk:PageMediaType">
  <psf:Property name="psf:SelectionType">
    <psf:Value xsi:type="xs:string">psk:PickOne</psf:Value>
  </psf:Property>
  <!-- Specifies Media would be Automatically selected. -->
  <psf:Option name="psk:AutoSelect"/>
  <!-- Specifies archival quality media. -->
  <psf:Option name="psk:Archival">
    <psf:ScoredProperty name="psk:BackCoating">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:FrontCoating">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:Material">
      <psf:Value xsi:type="xs:string">Paper</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:PrePrinted">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:PrePunched">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:Recycled">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:Weight">
      <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <!-- Specifies specialty back printing film media. -->
  <psf:Option name="psk:BackPrintFilm">
    <psf:ScoredProperty name="psk:BackCoating">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:FrontCoating">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:Material">
      <psf:Value xsi:type="xs:string">DryFilm</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:PrePrinted">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:PrePunched">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:Recycled">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:Weight">
      <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <!-- Specifies standard bond media. -->
  <psf:Option name="psk:Bond">
    <psf:ScoredProperty name="psk:BackCoating">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:FrontCoating">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:Material">
      <psf:Value xsi:type="xs:string">Paper</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:PrePrinted">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:PrePunched">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:Recycled">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:Weight">
      <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <!-- Specifies standard card stock media. -->
  <psf:Option name="psk:CardStock">
    <psf:ScoredProperty name="psk:BackCoating">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:FrontCoating">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:Material">
      <psf:Value xsi:type="xs:string">Paper</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:PrePrinted">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:PrePunched">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:Recycled">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:Weight">
      <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <!-- Specifies continuous feed media. -->
  <psf:Option name="psk:Continous">
    <psf:ScoredProperty name="psk:BackCoating">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:FrontCoating">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:Material">
      <psf:Value xsi:type="xs:string">Paper</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:PrePrinted">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:PrePunched">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:Recycled">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:Weight">
      <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <!-- Specifies standard envelope media. -->
  <psf:Option name="psk:EnvelopePlain">
    <psf:ScoredProperty name="psk:BackCoating">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:FrontCoating">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:Material">
      <psf:Value xsi:type="xs:string">Paper</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:PrePrinted">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:PrePunched">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:Recycled">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:Weight">
      <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <!-- Specifies windowed envelope media. -->
  <psf:Option name="psk:EnvelopeWindow">
    <psf:ScoredProperty name="psk:BackCoating">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:FrontCoating">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:Material">
      <psf:Value xsi:type="xs:string">Paper</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:PrePrinted">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:PrePunched">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:Recycled">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:Weight">
      <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <!-- Specifies fabric media. -->
  <psf:Option name="psk:Fabric">
    <psf:ScoredProperty name="psk:BackCoating">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:FrontCoating">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:Material">
      <psf:Value xsi:type="xs:string">Polyester</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:PrePrinted">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:PrePunched">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:Recycled">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:Weight">
      <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <!-- Specifies specialty high resolution media. -->
  <psf:Option name="psk:HighResolution">
    <psf:ScoredProperty name="psk:BackCoating">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:FrontCoating">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:Material">
      <psf:Value xsi:type="xs:string">Paper</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:PrePrinted">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:PrePunched">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:Recycled">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:Weight">
      <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <!-- Specifies label media. -->
  <psf:Option name="psk:Label">
    <psf:ScoredProperty name="psk:BackCoating">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:FrontCoating">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:Material">
      <psf:Value xsi:type="xs:string">Paper</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:PrePrinted">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:PrePunched">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:Recycled">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:Weight">
      <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <!-- Specifies attached multi-part forms media. -->
  <psf:Option name="psk:MultiLayerForm">
    <psf:ScoredProperty name="psk:BackCoating">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:FrontCoating">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:Material">
      <psf:Value xsi:type="xs:string">Paper</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:PrePrinted">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:PrePunched">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:Recycled">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:Weight">
      <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <!-- Specifies separate multi-part forms media. -->
  <psf:Option name="psk:MultiPartForm">
    <psf:ScoredProperty name="psk:BackCoating">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:FrontCoating">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:Material">
      <psf:Value xsi:type="xs:string">Paper</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:PrePrinted">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:PrePunched">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:Recycled">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:Weight">
      <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <!-- Specifies standard photographic media. -->
  <psf:Option name="psk:Photographic">
    <psf:ScoredProperty name="psk:BackCoating">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:FrontCoating">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:Material">
      <psf:Value xsi:type="xs:string">Paper</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:PrePrinted">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:PrePunched">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:Recycled">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:Weight">
      <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <!-- Specifies film photographic media. -->
  <psf:Option name="psk:PhotographicFilm">
    <psf:ScoredProperty name="psk:BackCoating">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:FrontCoating">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:Material">
      <psf:Value xsi:type="xs:string">DryFilm</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:PrePrinted">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:PrePunched">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:Recycled">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:Weight">
      <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <!-- Specifies glossy photographic media. -->
  <psf:Option name="psk:PhotographicGlossy">
    <psf:ScoredProperty name="psk:BackCoating">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:FrontCoating">
      <psf:Value xsi:type="xs:string">Glossy</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:Material">
      <psf:Value xsi:type="xs:string">Paper</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:PrePrinted">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:PrePunched">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:Recycled">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:Weight">
      <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <!-- Specifies high gloss photographic media. -->
  <psf:Option name="psk:PhotographicHighGloss">
    <psf:ScoredProperty name="psk:BackCoating">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:FrontCoating">
      <psf:Value xsi:type="xs:string">HighGloss</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:Material">
      <psf:Value xsi:type="xs:string">Paper</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:PrePrinted">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:PrePunched">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:Recycled">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:Weight">
      <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <!-- Specifies matte photographic media. -->
  <psf:Option name="psk:PhotographicMatte">
    <psf:ScoredProperty name="psk:BackCoating">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:FrontCoating">
      <psf:Value xsi:type="xs:string">Matte</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:Material">
      <psf:Value xsi:type="xs:string">Paper</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:PrePrinted">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:PrePunched">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:Recycled">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:Weight">
      <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <!-- Specifies satin photographic media. -->
  <psf:Option name="psk:PhotographicSatin">
    <psf:ScoredProperty name="psk:BackCoating">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:FrontCoating">
      <psf:Value xsi:type="xs:string">Satin</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:Material">
      <psf:Value xsi:type="xs:string">Paper</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:PrePrinted">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:PrePunched">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:Recycled">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:Weight">
      <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <!-- Specifies semi-gloss photographic media. -->
  <psf:Option name="psk:PhotographicSemiGloss">
    <psf:ScoredProperty name="psk:BackCoating">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:FrontCoating">
      <psf:Value xsi:type="xs:string">SemiGloss</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:Material">
      <psf:Value xsi:type="xs:string">Paper</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:PrePrinted">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:PrePunched">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:Recycled">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:Weight">
      <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <!-- Specifies standard paper media. -->
  <psf:Option name="psk:Plain">
    <psf:ScoredProperty name="psk:BackCoating">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:FrontCoating">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:Material">
      <psf:Value xsi:type="xs:string">Paper</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:PrePrinted">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:PrePunched">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:Recycled">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:Weight">
      <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <!-- Specifies output to an output display in continuous form. -->
  <psf:Option name="psk:Screen">
    <psf:ScoredProperty name="psk:BackCoating">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:FrontCoating">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:Material">
      <psf:Value xsi:type="xs:string">Display</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:PrePrinted">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:PrePunched">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:Recycled">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:Weight">
      <psf:Value xsi:type="xs:integer">0</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <!-- Specifies output to an output display in paged form. -->
  <psf:Option name="psk:ScreenPaged">
    <psf:ScoredProperty name="psk:BackCoating">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:FrontCoating">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:Material">
      <psf:Value xsi:type="xs:string">Display</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:PrePrinted">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:PrePunched">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:Recycled">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:Weight">
      <psf:Value xsi:type="xs:integer">0</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <!-- Specifies specialty stationery media. -->
  <psf:Option name="psk:Stationery">
    <psf:ScoredProperty name="psk:BackCoating">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:FrontCoating">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:Material">
      <psf:Value xsi:type="xs:string">Display</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:PrePrinted">
      <psf:Value xsi:type="xs:string">Letterhead</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:PrePunched">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:Recycled">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:Weight">
      <psf:Value xsi:type="xs:integer">0</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <!-- Specifies tab stock media that is not pre-cut (single tabs). -->
  <psf:Option name="psk:TabStockFull">
    <psf:ScoredProperty name="psk:BackCoating">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:FrontCoating">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:Material">
      <psf:Value xsi:type="xs:string">Paper</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:PrePrinted">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:PrePunched">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:Recycled">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:Weight">
      <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <!-- Specifies tab stock media that is pre-cut (multiple tabs). -->
  <psf:Option name="psk:TabStockPreCut">
    <psf:ScoredProperty name="psk:BackCoating">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:FrontCoating">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:Material">
      <psf:Value xsi:type="xs:string">Paper</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:PrePrinted">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:PrePunched">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:Recycled">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:Weight">
      <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <!-- Specifies transparency media. -->
  <psf:Option name="psk:Transparency">
    <psf:ScoredProperty name="psk:BackCoating">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:FrontCoating">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:Material">
      <psf:Value xsi:type="xs:string">Transparency</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:PrePrinted">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:PrePunched">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:Recycled">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:Weight">
      <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <!-- Specifies specialty T-shirt transfer media. -->
  <psf:Option name="psk:TShirtTransfer">
    <psf:ScoredProperty name="psk:BackCoating">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:FrontCoating">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:Material">
      <psf:Value xsi:type="xs:string">Paper</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:PrePrinted">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:PrePunched">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:Recycled">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:Weight">
      <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <!-- Specifies unknown or unlisted media. -->
  <psf:Option name="psk:None">
    <psf:ScoredProperty name="psk:BackCoating">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:FrontCoating">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:Material">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:PrePrinted">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:PrePunched">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:Recycled">
      <psf:Value xsi:type="xs:string">None</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:Weight">
      <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
</psf:Feature>    
```

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Especificação de esquema de impressão](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>
