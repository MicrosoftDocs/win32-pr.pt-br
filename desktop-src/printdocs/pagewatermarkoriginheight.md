---
description: Obter informações sobre o parâmetro PageWatermarkOriginHeight. Este tópico não é atual. Para obter as informações mais atuais, consulte a Especificação de Esquema de Impressão.
ms.assetid: ef429727-d881-408b-95ce-2acce667654a
title: PageWatermarkOriginHeight
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 25af5aa849cbf6d849afef2b11d2a39012818c8eabeccaeae8d77aa9e1925c84
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119034084"
---
# <a name="pagewatermarkoriginheight"></a>PageWatermarkOriginHeight

Este tópico não é atual. Para obter as informações mais atuais, consulte a [Especificação de Esquema de Impressão](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).

Especifica a origem de uma marca-d'água em relação à origem de PageImageableSize.

-   [Informações do elemento](#element-information)
-   [Conteúdo da estrutura](#structure-content)

## <a name="element-information"></a>Informações do elemento



| Nome | Valor |
|----------------------------|--------------------------------------------|
| Tipo de elemento <br/>   | ParameterDef<br/>                    |
| Prefixo de definição de scoping <br/> | ?<br/>                            |
| Observações <br/>          | Vinculado ao elemento PageWatermark<br/> |



 

## <a name="structure-content"></a>Conteúdo da estrutura

A estrutura XML desse elemento é a seguinte:

``` syntax
<psf:ParameterDef name="psk:PageWatermarkOriginHeight">
  <psf:Property name="psf:DataType">
    <psf:Value xsi:type="xs:string">xs:integer</psf:Value>
  </psf:Property>
  <psf:Property name="psf:DefaultValue">
    <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
  </psf:Property>
  <psf:Property name="psf:MaxValue">
    <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
  </psf:Property>
  <psf:Property name="psf:MinValue">
    <psf:Value xsi:type="xs:integer">0</psf:Value>
  </psf:Property>
  <psf:Property name="psf:Multiple">
    <psf:Value xsi:type="xs:integer">1</psf:Value>
  </psf:Property>
  <psf:Property name="psf:Mandatory">
    <psf:Value xsi:type="xs:string">psk:Conditional</psf:Value>
  </psf:Property>
  <psf:Property name="psf:UnitType">
    <psf:Value xsi:type="xs:string">microns</psf:Value>
  </psf:Property>
</psf:ParameterDef>
      
```

## <a name="structure-properties"></a>Propriedades da estrutura

A tabela a seguir descreve as características das variáveis definidas na estrutura XML.



| Propriedade                | xsi:type           | Valor                                                                   |
|-------------------------|--------------------|-------------------------------------------------------------------------|
| Tipo de dados<br/>     | string<br/>  | xs:integer<br/>                                                   |
| DefaultValue<br/> | Número inteiro<br/> | não definido<br/>                                                    |
| MaxValue<br/>     | Número inteiro<br/> | Menor ou igual a PageImageableSize – valor ExtentHeight<br/> |
| Minvalue<br/>     | inteiro<br/> | 0<br/>                                                            |
| Vários<br/>     | integer<br/> | 1<br/>                                                            |
| Obrigatório<br/>    | string<br/>  | psk:Conditional<br/>                                              |
| Unittype<br/>     | string<br/>  | Mícrons<br/>                                                      |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Especificação de esquema de impressão](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




