---
description: Este tópico não é atual. Para obter as informações mais atuais, consulte a especificação do esquema de impressão.
ms.assetid: e73e1736-9be5-4831-8277-23a62658b7b5
title: JobNUpAllDocumentsContiguously
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 90e307883a25fc977b9086259789c04f4b3a7cbf
ms.sourcegitcommit: 7b8f6151ebe247536304866459b2973276271d4d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/06/2021
ms.locfileid: "104298048"
---
# <a name="jobnupalldocumentscontiguously"></a>JobNUpAllDocumentsContiguously

Este tópico não é atual. Para obter as informações mais atuais, consulte a [especificação do esquema de impressão](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).

Descreve a saída de várias páginas lógicas para uma única folha física. Todos os documentos no trabalho são compilados em conjunto de forma contígua. JobNUpAllDocumentsContiguously e DocumentNUp são mutuamente exclusivos. Cabe ao driver determinar o tratamento de restrições entre essas palavras-chave.

O diagrama a seguir ilustra um exemplo com o documento 1 contendo 3 páginas e o documento 2 contendo 2 páginas. Cada documento no trabalho fica duplexado de forma contígua. As instruções de apresentação mostradas no exemplo são a opção RightBottom.

![um diagrama que mostra como as páginas do documento são colocadas em uma única planilha com base na configuração DocumentNUp](images/local-1242234459-jobduplexpics.gif)

-   [Informações do elemento](#element-information)
-   [Conteúdo estrutural](#structural-content)
-   [Conteúdo de linguagem XML (XML)](#extensible-markup-language-xml-content)

## <a name="element-information"></a>Informações do elemento



| Nome                       |                                                                                                                                                |
|----------------------------|------------------------------------------------------------------------------------------------------------------------------------------------|
| Tipo de elemento <br/>   | Recurso<br/>                                                                                                                             |
| Prefixo de escopo <br/> | Trabalho<br/>                                                                                                                                 |
| Observações <br/>          | As partes superior, inferior, esquerda e direita são relativas ao PageImageableSize, em que TopLeft é indicado pela origem da altura e da largura.<br/> |



 

## <a name="structural-content"></a>Conteúdo estrutural

A estrutura XML desse elemento é:

``` syntax
<psf:Feature name="psk:JobNUpAllDocumentsContiguously">
  <psf:Property name="psf:SelectionType">
    <psf:Value xsi:type="xs:string">psk:PickOne</psf:Value>
  </psf:Property>
  <psf:Option name="psk:_OptionName_">
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
| \_OptionName\_<br/>                      | string<br/>  | characters<br/>    | Nome totalmente qualificado válido, conforme definido pelos [namespaces em XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/). Se nenhum namespace for especificado, o namespace padrão será assumido.<br/> | O nome da opção.<br/>                                                                                                   |
| \_IdentityOptionValue\_<br/>             | string<br/>  | N/D<br/>           | True, False.<br/>                                                                                                                                                               | Define uma opção que, quando selecionada, desabilita esse recurso.<br/>                                                         |
| \_PagesPerSheetValue\_<br/>              | Número inteiro<br/> | Páginas lógicas<br/> | Todos os inteiros (maiores que zero).<br/>                                                                                                                                          | Especifica o número de páginas lógicas por folha física. O conjunto com suporte pode ser qualquer conjunto de inteiros, por exemplo, {1,2,4,6,8,9,16}.<br/> |
| \_PresentationDirectionOptionName\_<br/> | string<br/>  | characters<br/>    | Nome totalmente qualificado válido, conforme definido pelos [namespaces em XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/). Se nenhum namespace for especificado, o namespace padrão será assumido.<br/> | O nome da opção.<br/>                                                                                                   |



 

## <a name="extensible-markup-language-xml-content"></a>Conteúdo de linguagem XML (XML)

As palavras-chave do esquema de impressão pública são definidas no https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace. O conteúdo do linguagem XML público (XML) para essa palavra-chave é definido abaixo:

``` syntax
<psf:Feature name="psk:JobNUpAllDocumentsContiguously">
  <psf:Property name="psf:SelectionType">
    <psf:Value xsi:type="xs:string">psk:PickOne</psf:Value>
  </psf:Property>
  <psf:Option>
    <psf:ScoredProperty name="psk:PagesPerSheet">
      <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <psf:Feature name="psk:PresentationDirection">
    <!-- Specifies left to right, top to bottom. -->
    <psf:Option name="psk:RightBottom" />
    <!-- Specifies top to bottom, left to right. -->
    <psf:Option name="psk:BottomRight" />
    <!-- Specifies right to left, top to bottom. -->
    <psf:Option name="psk:LeftBottom" />
    <!-- Specifies top to bottom, right to left. -->
    <psf:Option name="psk:BottomLeft" />
    <!-- Specifies left to right, bottom to top. -->
    <psf:Option name="psk:RightTop" />
    <!-- Specifies bottom to top, left to right. -->
    <psf:Option name="psk:TopRight" />
    <!-- Specifies right to left, bottom to top. -->
    <psf:Option name="psk:LeftTop" />
    <!-- Specifies bottom to top, right to left. -->
    <psf:Option name="psk:TopLeft" />
  </psf:Feature>
</psf:Feature>
    
```

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Especificação de esquema de impressão](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




