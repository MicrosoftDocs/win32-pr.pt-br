---
description: Este tópico não é atual. Para obter as informações mais atuais, consulte a especificação do esquema de impressão.
ms.assetid: 6b81814f-2d9e-4862-8633-6ba016c11dac
title: PageImageableSize
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f1eef9012a7fda3eed6afd16add1d483c35c1111
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/26/2021
ms.locfileid: "107996103"
---
# <a name="pageimageablesize"></a>PageImageableSize

Este tópico não é atual. Para obter as informações mais atuais, consulte a [especificação do esquema de impressão](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).

Descreve a tela de imagem para layout e renderização. Isso será relatado com base em PageMediaSize e PageOrientation.

Os diagramas a seguir ilustram o uso de variáveis PageImageableSize com base em PageOrientation.

![um diagrama que mostra as medidas de página](images/local-1641910626-image.png)

-   [Informações do elemento](#element-information)
-   [Conteúdo estrutural](#structural-content)
-   [Conteúdo de linguagem XML (XML)](#extensible-markup-language-xml-content)

## <a name="element-information"></a>Informações do elemento



|                            |                     |
|----------------------------|---------------------|
| Nome | Valor |
| Tipo de elemento<br/>    | Propriedade<br/> |
| Prefixo de escopo <br/> | ?<br/>     |
| Observações <br/>          | Nenhum<br/>     |



 

## <a name="structural-content"></a>Conteúdo estrutural

A estrutura XML desse elemento é:

``` syntax
<psf:Property name="psk:PageImageableSize">
  <psf:Property name="psk:ImageableSizeWidth">
    <psf:Value xsi:type="xs:integer">_ImageableSizeWidthValue_</psf:Value>
  </psf:Property>
  <psf:Property name="psk:ImageableSizeHeight">
    <psf:Value xsi:type="xs:integer">_ImageableSizeHeightValue_</psf:Value>
  </psf:Property>
  <!--Specifies the imageable area within the logical page.  -->
  <psf:Property name="psk:ImageableArea">
    <psf:Property name="psk:OriginWidth">
      <psf:Value xsi:type="xs:integer">_OriginWidthValue_</psf:Value>
    </psf:Property>
    <psf:Property name="psk:OriginHeight">
      <psf:Value xsi:type="xs:integer">_OriginHeightValue_</psf:Value>
    </psf:Property>
    <psf:Property name="psk:ExtentWidth">
      <psf:Value xsi:type="xs:integer">_ExtentWidthValue_</psf:Value>
    </psf:Property>
    <psf:Property name="psk:ExtentHeight">
      <psf:Value xsi:type="xs:integer">_ExtentHeightValue_</psf:Value>
    </psf:Property>
  </psf:Property>
</psf:Property>
```

## <a name="structure-variables"></a>Variáveis de estrutura

A tabela a seguir descreve as características das variáveis definidas na estrutura XML.



| Nome                                    | Tipo de dados          | Unidade               | Valores com suporte                       | Resumo                                                                                                                    |
|-----------------------------------------|--------------------|--------------------|----------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| \_ImageableSizeWidthValue\_<br/>  | Número inteiro<br/> | mícrons<br/> | Maior que 0.<br/>             | Especifica a dimensão horizontal do tamanho da mídia do aplicativo em relação ao PageOrientation.<br/>               |
| \_ImageableSizeHeightValue\_<br/> | Número inteiro<br/> | mícrons<br/> | Maior que 0.<br/>             | Especifica a dimensão vertical do tamanho da mídia do aplicativo em relação ao PageOrientation.<br/>                 |
| \_OriginWidthValue\_<br/>         | Número inteiro<br/> | mícrons<br/> | Maior ou igual a 0.<br/> | Especifica a origem horizontal da área de imagem em relação ao tamanho da mídia do aplicativo.<br/>                   |
| \_OriginHeightValue\_<br/>        | Número inteiro<br/> | mícrons<br/> | Maior ou igual a 0.<br/> | Especifica a origem vertical da área de imagem em relação ao tamanho da mídia do aplicativo.<br/>                     |
| \_ExtentWidthValue\_<br/>         | Número inteiro<br/> | mícrons<br/> | Maior que 0.<br/>             | Especifica a distância horizontal entre a origem e o limite delimitador do tamanho da mídia do aplicativo.<br/>      |
| \_ExtentHeightValue\_<br/>        | Número inteiro<br/> | mícrons<br/> | Maior que 0.<br/>             | Especifica a distância vertical entre a origem e o limite delimitador do tamanho da mídia do aplicativo Canvas.<br/> |



 

## <a name="extensible-markup-language-xml-content"></a>Conteúdo de linguagem XML (XML)

As palavras-chave do esquema de impressão pública são definidas no https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace. O conteúdo do linguagem XML público (XML) para essa palavra-chave é definido abaixo:

``` syntax
<psf:Property name="psk:PageImageableSize">
  <psf:Property name="psk:ImageableSizeWidth">
    <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
  </psf:Property>
  <psf:Property name="psk:ImageableSizeHeight">
    <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
  </psf:Property>
    <psf:Property name="psk:ImageableArea">
      <psf:Property name="psk:OriginWidth">
        <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
      </psf:Property>
    <psf:Property name="psk:OriginHeight">
      <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
    </psf:Property>
    <psf:Property name="psk:ExtentWidth">
      <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
    </psf:Property>
    <psf:Property name="psk:ExtentHeight">
      <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
    </psf:Property>
  </psf:Property>
</psf:Property>
  
```

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Especificação de esquema de impressão](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




