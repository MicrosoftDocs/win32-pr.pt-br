---
description: Este tópico não é atual. Para obter as informações mais atuais, consulte a especificação do esquema de impressão.
ms.assetid: 38411802-2b2e-441c-b3a6-334d87b11b5d
title: PageSourceColorProfileEmbedded
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 409b101d944152fa28c8972da4d8515e8cdfb05b
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/05/2021
ms.locfileid: "105781110"
---
# <a name="pagesourcecolorprofileembedded"></a>PageSourceColorProfileEmbedded

Este tópico não é atual. Para obter as informações mais atuais, consulte a [especificação do esquema de impressão](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).

Especifica o perfil de cor de origem inserido.

-   [Informações do elemento](#element-information)
-   [Conteúdo da estrutura](#structure-content)

## <a name="element-information"></a>Informações do elemento



| Nome                       |                                                     |
|----------------------------|-----------------------------------------------------|
| Tipo de elemento <br/>   | ParameterDef<br/>                             |
| Prefixo de escopo <br/> | ?<br/>                                     |
| Observações <br/>          | Vinculado ao elemento PageSourceColorProfile<br/> |



 

## <a name="structure-content"></a>Conteúdo da estrutura

A estrutura XML desse elemento é:

``` syntax
<psf:ParameterDef name="psk:PageSourceColorProfileEmbedded">
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

 

 




