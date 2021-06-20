---
description: Saiba como o elemento DocumentCopiesAllPages, que especifica o número de cópias de um documento.
ms.assetid: 6319e8fc-787f-4bc8-8436-1b498b3882d2
title: DocumentCopiesAllPages
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 05bf82c23b764f3fe1f8257f4cdb2e7fa03374bd
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/19/2021
ms.locfileid: "112409439"
---
# <a name="documentcopiesallpages"></a>DocumentCopiesAllPages

Este tópico não é atual. Para obter as informações mais atuais, consulte a [especificação do esquema de impressão](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).

Especifica o número de cópias de um documento.

-   [Informações do elemento](#element-information)
-   [Conteúdo da estrutura](#structure-content)

## <a name="element-information"></a>Informações do elemento



| Name | Valor |
|----------------------------|-------------------------|
| Tipo de elemento <br/>   | ParameterDef<br/> |
| Prefixo de escopo <br/> | Documento<br/>     |
| Observações <br/>          | Nenhum<br/>         |



 

## <a name="structure-content"></a>Conteúdo da estrutura

A estrutura XML desse elemento é:

``` syntax
<psf:ParameterDef name="psk:DocumentCopiesAllPages">
  <psf:Property name="psf:DataType">
    <psf:Value xsi:type="xs:string">xs:integer</psf:Value>
  </psf:Property>
  <psf:Property name="psf:DefaultValue">
    <psf:Value xsi:type="xs:integer">1</psf:Value>
  </psf:Property>
  <psf:Property name="psf:MaxValue">
    <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
  </psf:Property>
  <psf:Property name="psf:MinValue">
    <psf:Value xsi:type="xs:integer">1</psf:Value>
  </psf:Property>
  <psf:Property name="psf:Multiple">
    <psf:Value xsi:type="xs:integer">1</psf:Value>
  </psf:Property>
  <psf:Property name="psf:Mandatory">
    <psf:Value xsi:type="xs:string">psk:Unconditional</psf:Value>
  </psf:Property>
  <psf:Property name="psf:UnitType">
    <psf:Value xsi:type="xs:string">copies</psf:Value>
  </psf:Property>
</psf:ParameterDef>
      
```

## <a name="structure-properties"></a>Propriedades da estrutura

A tabela a seguir descreve as características das variáveis definidas na estrutura XML.



| Propriedade                | xsi:type           | Valor                        |
|-------------------------|--------------------|------------------------------|
| Tipo de dados<br/>     | string<br/>  | xs:integer<br/>        |
| DefaultValue<br/> | integer<br/> | 1<br/>                 |
| MaxValue<br/>     | Número inteiro<br/> | não definido<br/>         |
| MinValue<br/>     | integer<br/> | 1<br/>                 |
| Obrigatório<br/>    | string<br/>  | PSK: incondicional<br/> |
| Vários<br/>     | integer<br/> | 1<br/>                 |
| UnitType<br/>     | string<br/>  | cópia<br/>            |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Especificação de esquema de impressão](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




