---
description: Saiba mais sobre o elemento JobDuplexAllDocumentsContiguously, que descreve as características duplex da saída.
ms.assetid: dd24166c-d5e2-420e-8a8c-e1a25728ab2f
title: JobDuplexAllDocumentsContiguously
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 20a8911a4c62644bfc073a2a9c1dcfd67dad536a
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/19/2021
ms.locfileid: "112408949"
---
# <a name="jobduplexalldocumentscontiguously"></a>JobDuplexAllDocumentsContiguously

Este tópico não é atual. Para obter as informações mais atuais, consulte a [Especificação de Esquema de Impressão](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).

Descreve as características duplex da saída. O recurso duplex permite imprimir em ambos os lados da mídia. Todos os documentos no trabalho são duplexados de forma contígua. JobDuplexAllDocumentsContiguously e DocumentDuplex são mutuamente exclusivos. O driver deve determinar o tratamento de restrição entre essas palavras-chave.

-   [Informações do elemento](#element-information)
-   [Conteúdo estrutural](#structural-content)
-   [linguagem XML conteúdo (XML)](#extensible-markup-language-xml-content)

## <a name="element-information"></a>Informações do elemento



| Name | Valor |
|----------------------------|--------------------|
| Tipo de elemento <br/>   | Recurso<br/> |
| Prefixo de definição de scoping <br/> | Trabalho<br/>     |
| Observações <br/>          | Nenhum<br/>    |



 

## <a name="structural-content"></a>Conteúdo estrutural

A estrutura XML desse elemento é:

``` syntax
<psf:Feature name="psk:JobDuplexAllDocumentsContiguously">
  <psf:Property name="psf:SelectionType">
    <psf:Value xsi:type="xs:string">psk:PickOne</psf:Value>
  </psf:Property>
  <psf:Option name="psk:_OptionName_">
    <psf:Property name="psf:IdentityOption">
      <psf:Value xsi:type="xs:string">_IdentityOptionValue_</psf:Value>
    </psf:Property>
    <psf:ScoredProperty name="psk:DuplexMode">
      <psf:Value xsi:type="xs:string">_DuplexModeValue_</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
</psf:Feature>      
```

## <a name="structure-variables"></a>Variáveis de estrutura

A tabela a seguir descreve as características das variáveis definidas na estrutura XML.



| Nome                               | Tipo de dados         | Unidade                  | Valores com suporte                                                                                                                                                             | Resumo                                                                                                                                |
|------------------------------------|-------------------|-----------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------|
| \_Optionname\_<br/>          | string<br/> | characters<br/> | Nome totalmente qualificado válido, conforme definido por https://www.w3.org/TR/1999/REC-xml-names-19990114/\#dt-qname . Se nenhum namespace for especificado, o namespace padrão será assumido.<br/> | O nome da opção.<br/>                                                                                                     |
| \_IdentityOptionValue\_<br/> | string<br/> | n/d<br/>        | True, False.<br/>                                                                                                                                                      | Define uma Opção que, quando selecionada, desabilitará esse recurso.<br/>                                                           |
| \_DuplexModeValue\_<br/>     | string<br/> | n/d<br/>        | Automático, Manual.<br/>                                                                                                                                                | Define o modo duplex. Duplex automático é executado por hardware. A duplexação manual é executada pelo software e pelo usuário.<br/> |



 

## <a name="extensible-markup-language-xml-content"></a>linguagem XML conteúdo (XML)

As palavras-chave public Print Schema são definidas no https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace . O conteúdo linguagem XML XML (public linguagem XML) para essa palavra-chave é definido abaixo:

``` syntax
<psf:Feature name="psk:JobDuplexAllDocumentsContiguously">
  <psf:Property name="psf:SelectionType">
    <psf:Value xsi:type="xs:string">psk:PickOne</psf:Value>
  </psf:Property>
  <!-- Specifies one sided printing. -->
  <psf:Option name="psk:OneSided" />
  <!-- Specifies two sided printing such that the page is flipped parallel to the MediaSizeWidth direction. -->
  <psf:Option name="psk:TwoSidedShortEdge">
    <psf:ScoredProperty name="psk:DuplexMode">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <!-- Specifies two sided printing such that the page is flipped parallel to the MediaSizeHeight direction. -->
  <psf:Option name="psk:TwoSidedLongEdge">
    <psf:ScoredProperty name="psk:DuplexMode">
      <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
</psf:Feature>    
```

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Especificação de esquema de impressão](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




