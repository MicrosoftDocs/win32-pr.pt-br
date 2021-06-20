---
description: Saiba mais sobre o elemento DocumentPageRanges, que descreve o intervalo de saída do documento em páginas.
ms.assetid: 4cd1b0f8-7f7e-40cc-8d19-d44187822cd1
title: DocumentPageRanges
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0e854736c72b3bff5ba2e4750e0b09e0b87c2c9f
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/19/2021
ms.locfileid: "112409249"
---
# <a name="documentpageranges"></a>DocumentPageRanges

Este tópico não é atual. Para obter as informações mais atuais, consulte a [especificação do esquema de impressão](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).

Descreve o intervalo de saída do documento em páginas. O valor do parâmetro deve estar de acordo com a seguinte estrutura:

-   PageRangeText: "*PageRange*" ou "*PageRange*,*PageRange*"

-   PageRange: "*PageNumber*" ou "*PageNumber* - *PageNumber*"

-   PageNumber: 1 a N, em que N é o número de páginas no documento. Se *pagenumber* > N, *PageNumber* = N.

O espaço em branco na cadeia de caracteres deve ser ignorado.

-   [Informações do elemento](#element-information)
-   [Conteúdo estrutural](#structural-content)

## <a name="element-information"></a>Informações do elemento



| Name | Valor |
|----------------------------|-------------------------|
| Tipo de elemento <br/>   | ParameterDef<br/> |
| Prefixo de escopo <br/> | Documento<br/>     |
| Observações <br/>          | Nenhum<br/>         |



 

## <a name="structural-content"></a>Conteúdo estrutural

A estrutura XML desse elemento é:

``` syntax
<psf:ParameterDef name="psk:DocumentPageRanges">
  <psf:Property name="psf:DataType">
    <psf:Value xsi:type="xs:string">xs:string</psf:Value>
  </psf:Property>
  <psf:Property name="psf:DefaultValue">
    <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
  </psf:Property>
  <psf:Property name="psf:MaxLength">
    <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
  </psf:Property>
  <psf:Property name="psf:MinLength">
    <psf:Value xsi:type="xs:integer">1</psf:Value>
  </psf:Property>
  <psf:Property name="psf:Mandatory">
    <psf:Value xsi:type="xs:string">psk:Conditional</psf:Value>
  </psf:Property>
  <psf:Property name="psf:UnitType">
    <psf:Value xsi:type="xs:string">characters</psf:Value>
  </psf:Property>
</psf:ParameterDef>
      
```

## <a name="structure-properties"></a>Propriedades da estrutura

A tabela a seguir descreve as características das variáveis definidas na estrutura XML.



| Propriedade                | xsi:type           | Valor                      |
|-------------------------|--------------------|----------------------------|
| Tipo de dados<br/>     | string<br/>  | xs:string<br/>       |
| DefaultValue<br/> | string<br/>  | não definido<br/>       |
| MaxLength<br/>    | Número inteiro<br/> | não definido<br/>       |
| MinLength<br/>    | integer<br/> | 1<br/>               |
| Obrigatório<br/>    | string<br/>  | PSK: condicional<br/> |
| UnitType<br/>     | string<br/>  | characters<br/>      |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Especificação de esquema de impressão](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




