---
description: Este tópico não é atual. Para obter as informações mais atuais, consulte a especificação do esquema de impressão.
ms.assetid: 6f99f54b-c401-42ea-8715-95a2aad73042
title: PageMediaSize
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b549d7bd81579424125908fc71c9b81e839aff05
ms.sourcegitcommit: 7b8f6151ebe247536304866459b2973276271d4d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/06/2021
ms.locfileid: "104552872"
---
# <a name="pagemediasize"></a>PageMediaSize

Este tópico não é atual. Para obter as informações mais atuais, consulte a [especificação do esquema de impressão](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).

Descreve as dimensões de mídia física usadas para a saída.

O diagrama a seguir ilustra o uso da variável PageMediaSize (a opção ISOA4 é usada como um exemplo).

![um diagrama que mostra as dimensões da página](images/local-1594393517-pagemediasizepic.gif)

-   [Informações do elemento](#element-information)
-   [Conteúdo estrutural](#structural-content)
-   [Conteúdo de linguagem XML (XML)](#extensible-markup-language-xml-content)

## <a name="element-information"></a>Informações do elemento



|                            |                    |
|----------------------------|--------------------|
| Nome                       |                    |
| Tipo de elemento <br/>   | Recurso<br/> |
| Prefixo de escopo <br/> | ?<br/>    |
| Observações <br/>          | Nenhum<br/>    |



 

## <a name="structural-content"></a>Conteúdo estrutural

A estrutura XML desse elemento é:

``` syntax
<psf:Feature name="psk:PageMediaSize">
  <psf:Property name="psf:SelectionType">
    <psf:Value xsi:type="xs:string">psk:PickOne</psf:Value>
  </psf:Property>
  <psf:Option name="psk:_OptionName_">
    <psf:Property name="psf:IdentityOption">
      <psf:Value xsi:type="xs:string">_IdentityOptionValue_</psf:Value>
    </psf:Property>
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xs:integer">_MediaSizeWidth_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xs:integer">_MediaSizeHeight_</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
</psf:Feature>
      
```

## <a name="structure-variables"></a>Variáveis de estrutura

A tabela a seguir descreve as características das variáveis definidas na estrutura XML.



| Nome                                | Tipo de dados          | Unidade                  | Valores com suporte                                                                                                                                                                      | Resumo                                                                                                                                                                   |
|-------------------------------------|--------------------|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \_OptionName\_<br/>           | string<br/>  | characters<br/> | Nome totalmente qualificado válido, conforme definido pelos [namespaces em XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/). Se nenhum namespace for especificado, o namespace padrão será assumido.<br/> | Especifica o nome da mídia. A nomenclatura deve usar a seguinte convenção: " \_ OptionNameStandard \_ " " \_ OptionNameCommonName \_ " " \_ OptionNameDescriptor \_ ".<br/> |
| \_IdentityOptionValue\_<br/>  | string<br/>  | N/D<br/>        | True, False.<br/>                                                                                                                                                               | Define uma opção que, quando selecionada, desabilita esse recurso.<br/>                                                                                              |
| \_OptionNameStandard\_<br/>   | string<br/>  | characters<br/> | ' ISO ', ' JIS ', ' Japão ', ' América do, ' OtherMetric ', ' PRC ', nenhum.<br/>                                                                                                         | Indica se o tamanho da mídia está definido por um padrão específico.<br/>                                                                                               |
| \_OptionNameCommonName\_<br/> | string<br/>  | characters<br/> | Nome totalmente qualificado válido, conforme definido pelos [namespaces em XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/). Se nenhum namespace for especificado, o namespace padrão será assumido.<br/> | Nome comum para o tamanho da mídia.<br/>                                                                                                                                |
| \_OptionNameDescriptor\_<br/> | string<br/>  | characters<br/> | Big, envelope, extra, mais, cartão-postal, girado, planilha, ' nenhum '.<br/>                                                                                                              | Big, envelope, extra, mais, cartão-postal, girado, planilha, ' nenhum '.<br/>                                                                                                  |
| \_MediaSizeWidth\_<br/>       | Número inteiro<br/> | mícrons<br/>    | Maior que 0, menor que o tamanho máximo de mídia de suporte para o dispositivo.<br/>                                                                                                           | Especifica a largura da mídia física.<br/>                                                                                                                     |
| \_MediaSizeHeight\_<br/>      | Número inteiro<br/> | mícrons<br/>    | Maior que 0, menor que o tamanho máximo de mídia de suporte para o dispositivo.<br/>                                                                                                           | Especifica a altura da mídia física.<br/>                                                                                                                    |



 

## <a name="extensible-markup-language-xml-content"></a>Conteúdo de linguagem XML (XML)

As palavras-chave do esquema de impressão pública são definidas no `https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords` namespace. O conteúdo do linguagem XML público (XML) para essa palavra-chave é definido abaixo:

``` syntax
<psf:Feature name="psk:PageMediaSize">
  <psf:Property name="psf:SelectionType">
    <psf:Value xsi:type="xs:string">psk:PickOne</psf:Value>
  </psf:Property>
  <!-- Specifies a custom media size.  Must be validated again DeviceMediaSize. -->
  <psf:Option name="psk:CustomMediaSize">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:ParameterRef name="psk:PageMediaSizeMediaSizeWidth" />
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:ParameterRef name="psk:PageMediaSizeMediaSizeHeight" />
    </psf:ScoredProperty>
  </psf:Option>
  <!-- Specifies a custom media size (PostScript specific).  Must be validated again DeviceMediaSize. -->
  <psf:Option name="psk:PSCustomMediaSize">
    <!-- Specifies the height of the page parallel to the feed orientation direction.  (Reference PPD Spec). -->
    <psf:ScoredProperty name="psk:PSHeight">
      <psf:ParameterRef name="psk:PageMediaSizePSHeight" />
    </psf:ScoredProperty>
    <!-- Specifies the offset parallel to the feed orientation direction.  (Reference PPD Spec). -->
    <psf:ScoredProperty name="psk:PSHeightOffset">
      <psf:ParameterRef name="psk:PageMediaSizePSHeightOffset" />
    </psf:ScoredProperty>
    <!-- Specifies the orientation relative to the feed orientation direction.  (Reference PPD Spec). -->
    <psf:ScoredProperty name="psk:PSOrientation">
      <psf:ParameterRef name="psk:PageMediaSizePSOrientation" />
    </psf:ScoredProperty>
    <!-- Specifies the width of the page perpendicular to the feed orientation direction.  (Reference PPD Spec). -->
    <psf:ScoredProperty name="psk:PSWidth">
      <psf:ParameterRef name="psk:PageMediaSizePSWidth" />
    </psf:ScoredProperty>
    <!-- Specifies the offset perpendicular to the feed orientation direction.  (Reference PPD Spec). -->
    <psf:ScoredProperty name="psk:PSWidthOffset">
      <psf:ParameterRef name="psk:PageMediaSizePSWidthOffset" />
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:ISOA0">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xs:integer">841000</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xs:integer">1189000</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:ISOA1">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xs:integer">594000</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xs:integer">841000</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:ISOA10">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xs:integer">26000</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xs:integer">37000</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:ISOA2">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xs:integer">420000</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xs:integer">594000</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:ISOA3">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xs:integer">297000</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xs:integer">420000</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:ISOA3Rotated">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xs:integer">420000</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xs:integer">297000</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:ISOA3Extra">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xs:integer">322000</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xs:integer">445000</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:ISOA4">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xs:integer">210000</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xs:integer">297000</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:ISOA4Rotated">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xs:integer">297000</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xs:integer">210000</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:ISOA4Extra">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xs:integer">235500</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xs:integer">322300</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:ISOA5">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xs:integer">148000</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xs:integer">210000</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:ISOA5Rotated">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xs:integer">210000</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xs:integer">148000</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:ISOA5Extra">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xs:integer">174000</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xs:integer">235000</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:ISOA6">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xs:integer">105000</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xs:integer">148000</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:ISOA6Rotated">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xs:integer">148000</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xs:integer">105000</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:ISOA7">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xs:integer">74000</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xs:integer">105000</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:ISOA8">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xs:integer">52000</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xs:integer">74000</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:ISOA9">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xs:integer">37000</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xs:integer">52000</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:ISOB0">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xs:integer">1000000</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xs:integer">1414000</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:ISOB1">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xs:integer">707000</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xs:integer">1000000</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:ISOB10">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xs:integer">31000</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xs:integer">44000</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:ISOB2">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xs:integer">500000</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xs:integer">707000</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:ISOB3">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xs:integer">353000</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xs:integer">500000</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:ISOB4">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xs:integer">250000</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xs:integer">353000</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:ISOB4Envelope">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xs:integer">250000</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xs:integer">353000</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:ISOB5Envelope">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xs:integer">176000</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xs:integer">250000</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:ISOB5Extra">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xs:integer">201000</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xs:integer">276000</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:ISOB7">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xs:integer">88000</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xs:integer">125000</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:ISOB8">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xs:integer">62000</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xs:integer">88000</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:ISOB9">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xs:integer">44000</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xs:integer">62000</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:ISOC0">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xs:integer">917000</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xs:integer">1297000</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:ISOC1">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xs:integer">648000</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xs:integer">917000</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:ISOC10">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xs:integer">28000</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xs:integer">40000</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:ISOC2">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xs:integer">458000</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xs:integer">648000</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:ISOC3">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xs:integer">324000</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xs:integer">458000</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:ISOC3Envelope">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xs:integer">324000</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xs:integer">458000</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:ISOC4">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xs:integer">229000</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xs:integer">324000</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:ISOC4Envelope">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xs:integer">229000</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xs:integer">324000</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:ISOC5">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xs:integer">162000</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xs:integer">229000</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:ISOC5Envelope">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xs:integer">162000</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xs:integer">229000</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:ISOC6">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xs:integer">114000</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xs:integer">162000</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:ISOC6Envelope">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xs:integer">114000</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xs:integer">162000</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:ISOC6C5Envelope">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xs:integer">114000</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xs:integer">229000</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:ISOC7">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xs:integer">81000</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xs:integer">114000</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:ISOC8">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xs:integer">57000</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xs:integer">81000</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:ISOC9">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xs:integer">40000</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xs:integer">57000</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:ISODLEnvelope">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xs:integer">110000</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xs:integer">220000</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:ISODLEnvelopeRotated">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xs:integer">220000</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xs:integer">110000</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:ISOSRA3">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xs:integer">320000</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xs:integer">450000</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:JapanQuadrupleHagakiPostcard">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xs:integer">200000</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xs:integer">296000</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:JISB0">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xs:integer">1030000</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xs:integer">1456000</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:JISB1">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xs:integer">728000</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xs:integer">1030000</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:JISB10">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xs:integer">32000</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xs:integer">45000</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:JISB2">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xs:integer">515000</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xs:integer">728000</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:JISB3">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xs:integer">364000</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xs:integer">515000</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:JISB4">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xs:integer">257000</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xs:integer">364000</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:JISB4Rotated">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xs:integer">364000</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xs:integer">257000</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:JISB5">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xs:integer">182000</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xs:integer">257000</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:JISB5Rotated">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xs:integer">257000</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xs:integer">182000</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:JISB6">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xs:integer">128000</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xs:integer">182000</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:JISB6Rotated">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xs:integer">182000</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xs:integer">128000</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:JISB7">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xs:integer">91000</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xs:integer">128000</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:JISB8">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xs:integer">64000</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xs:integer">91000</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:JISB9">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xs:integer">45000</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xs:integer">64000</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:JapanChou3Envelope">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xs:integer">120000</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xs:integer">235000</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:JapanChou3EnvelopeRotated">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xs:integer">235000</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xs:integer">120000</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:JapanChou4Envelope">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xs:integer">90000</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xs:integer">205000</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:JapanChou4EnvelopeRotated">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xs:integer">205000</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xs:integer">90000</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:JapanHagakiPostcard">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xs:integer">100000</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xs:integer">148000</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:JapanHagakiPostcardRotated">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xs:integer">148000</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xs:integer">100000</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:JapanKaku2Envelope">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xs:integer">240000</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xs:integer">332000</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:JapanKaku2EnvelopeRotated">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xs:integer">332000</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xs:integer">240000</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:JapanKaku3Envelope">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xs:integer">216000</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xs:integer">277000</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:JapanKaku3EnvelopeRotated">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xs:integer">277000</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xs:integer">216000</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:JapanYou4Envelope">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xs:integer">105000</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xs:integer">235000</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:NorthAmerica10x11">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xs:integer">254000</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xs:integer">279400</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:NorthAmerica10x14">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xs:integer">254000</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xs:integer">355600</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:NorthAmerica11x17">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xs:integer">279400</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xs:integer">431800</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:NorthAmerica9x11">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xs:integer">228600</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xs:integer">279400</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:NorthAmericaArchitectureASheet">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xs:integer">228600</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xs:integer">304800</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:NorthAmericaArchitectureBSheet">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xs:integer">304800</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xs:integer">457200</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:NorthAmericaArchitectureCSheet">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xs:integer">457200</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xs:integer">609600</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:NorthAmericaArchitectureDSheet">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xs:integer">609600</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xs:integer">914400</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:NorthAmericaArchitectureESheet">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xs:integer">914400</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xs:integer">1219200</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:NorthAmericaCSheet">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xs:integer">431800</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xs:integer">558800</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:NorthAmericaDSheet">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xs:integer">558800</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xs:integer">863600</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:NorthAmericaESheet">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xs:integer">863600</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xs:integer">1117600</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:NorthAmericaExecutive">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xs:integer">184150</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xs:integer">266700</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:NorthAmericaGermanLegalFanfold">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xs:integer">215900</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xs:integer">330200</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:NorthAmericaGermanStandardFanfold">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xs:integer">215900</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xs:integer">304800</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:NorthAmericaLegal">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xs:integer">215900</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xs:integer">355600</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:NorthAmericaLegalExtra">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xs:integer">241300</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xs:integer">381000</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:NorthAmericaLetter">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xs:integer">215900</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xs:integer">279400</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:NorthAmericaLetterRotated">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xs:integer">279400</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xs:integer">215900</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:NorthAmericaLetterExtra">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xs:integer">241300</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xs:integer">304800</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:NorthAmericaLetterPlus">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xs:integer">215900</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xs:integer">322326</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:NorthAmericaMonarchEnvelope">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xs:integer">98425</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xs:integer">177800</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:NorthAmericaNote">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xs:integer">215900</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xs:integer">279400</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:NorthAmericaNumber10Envelope">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xs:integer">104775</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xs:integer">241300</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:NorthAmericaNumber10EnvelopeRotated">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xs:integer">241300</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xs:integer">104775</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:NorthAmericaNumber9Envelope">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xs:integer">98425</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xs:integer">225425</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:NorthAmericaNumber11Envelope">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xs:integer">114300</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xs:integer">263525</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:NorthAmericaNumber12Envelope">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xs:integer">120650</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xs:integer">279400</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:NorthAmericaNumber14Envelope">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xs:integer">127000</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xs:integer">292100</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:NorthAmericaPersonalEnvelope">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xs:integer">92075</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xs:integer">165100</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:NorthAmericaQuarto">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xs:integer">215000</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xs:integer">275000</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:NorthAmericaStatement">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xs:integer">139700</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xs:integer">215900</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:NorthAmericaSuperA">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xs:integer">227000</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xs:integer">356000</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:NorthAmericaSuperB">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xs:integer">305000</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xs:integer">487000</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:NorthAmericaTabloid">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xs:integer">279400</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xs:integer">431800</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:NorthAmericaTabloidExtra">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xs:integer">296926</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xs:integer">457200</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:OtherMetricA4Plus">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xs:integer">210000</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xs:integer">330000</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:OtherMetricA3Plus">
    - <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xsd:integer">329000</psf:Value>
    </psf:ScoredProperty>
    - <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xsd:integer">483000</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:OtherMetricFolio">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xs:integer">215900</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xs:integer">330200</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:OtherMetricInviteEnvelope">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xs:integer">220000</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xs:integer">220000</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:OtherMetricItalianEnvelope">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xs:integer">110000</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xs:integer">230000</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:PRC1Envelope">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xs:integer">102000</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xs:integer">165000</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:PRC1EnvelopeRotated">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xs:integer">165000</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xs:integer">102000</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:PRC10Envelope">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xs:integer">324000</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xs:integer">458000</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:PRC10EnvelopeRotated">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xs:integer">458000</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xs:integer">324000</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:PRC16K">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xs:integer">146000</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xs:integer">215000</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:PRC16KRotated">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xs:integer">215000</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xs:integer">146000</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:PRC2Envelope">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xs:integer">102000</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xs:integer">176000</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:PRC2EnvelopeRotated">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xs:integer">176000</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xs:integer">102000</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:PRC32K">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xs:integer">97000</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xs:integer">151000</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:PRC32KRotated">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xs:integer">151000</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xs:integer">97000</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:PRC32KBig">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xs:integer">97000</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xs:integer">151000</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:PRC3Envelope">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xs:integer">125000</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xs:integer">176000</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:PRC3EnvelopeRotated">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xs:integer">176000</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xs:integer">125000</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:PRC4Envelope">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xs:integer">110000</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xs:integer">208000</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:PRC4EnvelopeRotated">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xs:integer">208000</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xs:integer">110000</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:PRC5Envelope">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xs:integer">110000</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xs:integer">220000</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:PRC5EnvelopeRotated">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xs:integer">220000</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xs:integer">110000</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:PRC6Envelope">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xs:integer">120000</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xs:integer">230000</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:PRC6EnvelopeRotated">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xs:integer">230000</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xs:integer">120000</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:PRC7Envelope">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xs:integer">160000</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xs:integer">230000</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:PRC7EnvelopeRotated">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xs:integer">230000</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xs:integer">160000</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:PRC8Envelope">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xs:integer">120000</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xs:integer">309000</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:PRC8EnvelopeRotated">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xs:integer">309000</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xs:integer">120000</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:PRC9Envelope">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xs:integer">229000</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xs:integer">324000</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:PRC9EnvelopeRotated">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xs:integer">324000</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xs:integer">229000</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:Roll04Inch">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xs:integer">101600</psf:Value>
    </psf:ScoredProperty>
    <!-- MediaSizeHeight not applicable for Roll media -->
  </psf:Option>
  <psf:Option name="psk:Roll06Inch">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xs:integer">152400</psf:Value>
    </psf:ScoredProperty>
    <!-- MediaSizeHeight not applicable for Roll media -->
  </psf:Option>
  <psf:Option name="psk:Roll08Inch">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xs:integer">203200</psf:Value>
    </psf:ScoredProperty>
    <!-- MediaSizeHeight not applicable for Roll media -->
  </psf:Option>
  <psf:Option name="psk:Roll12Inch">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xs:integer">304800</psf:Value>
    </psf:ScoredProperty>
    <!-- MediaSizeHeight not applicable for Roll media -->
  </psf:Option>
  <psf:Option name="psk:Roll15Inch">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xs:integer">381000</psf:Value>
    </psf:ScoredProperty>
    <!-- MediaSizeHeight not applicable for Roll media -->
  </psf:Option>
  <psf:Option name="psk:Roll18Inch">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xs:integer">457200</psf:Value>
    </psf:ScoredProperty>
    <!-- MediaSizeHeight not applicable for Roll media -->
  </psf:Option>
  <psf:Option name="psk:Roll22Inch">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xs:integer">558800</psf:Value>
    </psf:ScoredProperty>
    <!-- MediaSizeHeight not applicable for Roll media -->
  </psf:Option>
  <psf:Option name="psk:Roll24Inch">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xs:integer">609600</psf:Value>
    </psf:ScoredProperty>
    <!-- MediaSizeHeight not applicable for Roll media -->
  </psf:Option>
  <psf:Option name="psk:Roll30Inch">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xs:integer">762000</psf:Value>
    </psf:ScoredProperty>
    <!-- MediaSizeHeight not applicable for Roll media -->
  </psf:Option>
  <psf:Option name="psk:Roll36Inch">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xs:integer">914400</psf:Value>
    </psf:ScoredProperty>
    <!-- MediaSizeHeight not applicable for Roll media -->
  </psf:Option>
  <psf:Option name="psk:Roll54Inch">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xs:integer">1371600</psf:Value>
    </psf:ScoredProperty>
    <!-- MediaSizeHeight not applicable for Roll media -->
  </psf:Option>
  <psf:Option name="psk:JapanDoubleHagakiPostcard">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xsd:integer">200000</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xsd:integer">148000</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:JapanDoubleHagakiPostcardRotated">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xsd:integer">148000</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xsd:integer">200000</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:JapanLPhoto">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xsd:integer">89000</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xsd:integer">127000</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:Japan2LPhoto">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xsd:integer">127000</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xsd:integer">178000</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:JapanYou1Envelope">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xsd:integer">120000</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xsd:integer">176000</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:JapanYou2Envelope">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xsd:integer">114000</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xsd:integer">162000</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:JapanYou3Envelope">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xsd:integer">98000</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xsd:integer">148000</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:JapanYou4EnvelopeRotated">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xsd:integer">235000</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xsd:integer">105000</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:JapanYou6Envelope">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xsd:integer">98000</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xsd:integer">190000</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:JapanYou6EnvelopeRotated">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xsd:integer">190000</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xsd:integer">98000</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:NorthAmerica4x6">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xsd:integer">101600</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xsd:integer">152400</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:NorthAmerica4x8">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xsd:integer">101600</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xsd:integer">203200</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:NorthAmerica5x7">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xsd:integer">127000</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xsd:integer">177800</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:NorthAmerica8x10">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xsd:integer">203200</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xsd:integer">254000</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:NorthAmerica10x12">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xsd:integer">254000</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xsd:integer">304800</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:NorthAmerica14x17">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xsd:integer">355600</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xsd:integer">431800</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:BusinessCard">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xsd:integer">55000</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xsd:integer">91000</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Option name="psk:CreditCard">
    <psf:ScoredProperty name="psk:MediaSizeWidth">
      <psf:Value xsi:type="xsd:integer">54000</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSizeHeight">
      <psf:Value xsi:type="xsd:integer">86000</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
</psf:Feature>   
```

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Especificação de esquema de impressão](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>
