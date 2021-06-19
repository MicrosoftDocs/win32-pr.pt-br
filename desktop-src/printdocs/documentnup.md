---
description: Saiba mais sobre o elemento DocumentNUp, que descreve a saída e o formato de várias páginas lógicas para uma única planilha física.
ms.assetid: 941515a8-ba3f-47b9-9f3f-08a48122661a
title: DocumentNUp
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8b49bd4fa3eb9f2b3b0083fc8022dbd6f41d090e
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/19/2021
ms.locfileid: "112409259"
---
# <a name="documentnup"></a>DocumentNUp

Este tópico não é atual. Para obter as informações mais atuais, consulte a [Especificação de Esquema de Impressão](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).

Descreve a saída e o formato de várias páginas lógicas para uma única planilha física. Cada documento é compilado separadamente. DocumentNUp e JobNUpAllDocumentsContiguously são mutuamente exclusivos. O driver deve determinar o tratamento de restrição entre essas palavras-chave.

O diagrama a seguir ilustra um exemplo com o Documento 1 contendo 3 páginas e o Documento 2 contendo duas páginas. Cada documento é duplexado separadamente. A direção da apresentação mostrada abaixo é a opção RightBottom.

![um diagrama que mostra como as páginas de documento são colocadas em uma única planilha com base na configuração de documentnup](images/local-1663869164-docduplex1.gif)

-   [Informações do elemento](#element-information)
-   [Conteúdo estrutural](#structural-content)
-   [linguagem XML conteúdo (XML)](#extensible-markup-language-xml-content)

## <a name="element-information"></a>Informações do elemento



| Name | Valor |
|----------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------|
| Tipo de elemento <br/>   | Recurso<br/>                                                                                                                              |
| Prefixo de definição de scoping <br/> | Documento<br/>                                                                                                                             |
| Observações <br/>          | Top, Bottom, Left e Right são relativos ao PageImageableSize, em que TopLeft é anotado pela origem do eixo x e do eixo y.<br/> |



 

## <a name="structural-content"></a>Conteúdo estrutural

A estrutura XML desse elemento é a seguinte:

``` syntax
<psf:Feature name="psk:DocumentNUp">
  <psf:Property name="psf:SelectionType">
    <psf:Value xsi:type="xs:string">psk:PickOne</psf:Value>
  </psf:Property>
  <psf:Option>
    <psf:Property name="psf:IdentityOption">
      <psf:Value xsi:type="xs:string">_IdentityOptionValue_</psf:Value>
    </psf:Property>
    <psf:ScoredProperty name="psk:PagesPerSheet">
      <psf:Value xsi:type="xs:integer">_PagesPerSheetValue_</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <!-- Specifies the ordering direction of the pages.  First direction followed by second direction. -->
  <psf:Feature name="psk:PresentationDirection">
    <psf:Option name="psk:_PresentationDirectionOptionName_" />
  </psf:Feature>
</psf:Feature>
```

## <a name="structure-variables"></a>Variáveis de estrutura

A tabela a seguir descreve as características das variáveis definidas na estrutura XML.



| Nome                                           | Tipo de dados          | Unidade                     | Valores com suporte                                                                                                                                                                      | Resumo                                                                                                                              |
|------------------------------------------------|--------------------|--------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------|
| \_Optionname\_<br/>                      | string<br/>  | characters<br/>    | Nome totalmente qualificado válido, conforme definido [por Namespaces em XML.](https://www.w3.org/TR/1999/REC-xml-names-19990114/) Se nenhum namespace for especificado, o namespace padrão será assumido.<br/> | O nome da opção.<br/>                                                                                                   |
| \_IdentityOptionValue\_<br/>             | string<br/>  | n/d<br/>           | True, False.<br/>                                                                                                                                                               | Define uma Opção que, quando selecionada, desabilitará esse recurso.<br/>                                                         |
| \_PagesPerSheetValue\_<br/>              | Número inteiro<br/> | Páginas lógicas<br/> | Todos os inteiros (Maior que Zero).<br/>                                                                                                                                          | Especifica o número de páginas lógicas por planilha física. O conjunto com suporte pode ser qualquer conjunto de inteiros, por exemplo, {1,2,4,6,8,9,16}.<br/> |
| \_PresentationDirectionOptionName\_<br/> | string<br/>  | characters<br/>    | Nome totalmente qualificado válido, conforme definido [por Namespaces em XML.](https://www.w3.org/TR/1999/REC-xml-names-19990114/) Se nenhum namespace for especificado, o namespace padrão será assumido.<br/> | O nome da opção.<br/>                                                                                                   |



 

## <a name="extensible-markup-language-xml-content"></a>linguagem XML conteúdo (XML)

As palavras-chave public Print Schema são definidas no https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace . O conteúdo linguagem XML XML (public linguagem XML) para essa palavra-chave é definido abaixo:

``` syntax
<psf:Feature name="psk:DocumentNUp">
  <psf:Property name="psf:SelectionType">
    <psf:Value xsi:type="xs:string">psk:PickOne</psf:Value>
  </psf:Property>
  <psf:Option>
    <psf:ScoredProperty name="psk:PagesPerSheet">
      <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Feature name="psk:PresentationDirection">
    <!-- Specifies format left to right, top to bottom. -->
    <psf:Option name="psk:RightBottom" />
    <!-- Specifies format top to bottom, left to right. -->
    <psf:Option name="psk:BottomRight" />
    <!-- Specifies format right to left, top to bottom. -->
    <psf:Option name="psk:LeftBottom" />
    <!-- Specifies format top to bottom, right to left. -->
    <psf:Option name="psk:BottomLeft" />
    <!-- Specifies format left to right, bottom to top. -->
    <psf:Option name="psk:RightTop" />
    <!-- Specifies format bottom to top, left to right. -->
    <psf:Option name="psk:TopRight" />
    <!-- Specifies format right to left, bottom to top. -->
    <psf:Option name="psk:LeftTop" />
    <!-- Specifies format bottom to top, right to left. -->
    <psf:Option name="psk:TopLeft" />
  </psf:Feature>
</psf:Feature>
    
```

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Especificação de esquema de impressão](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




