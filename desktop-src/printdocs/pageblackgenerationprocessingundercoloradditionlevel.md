---
description: Este tópico não é atual. Para obter as informações mais atuais, consulte a especificação do esquema de impressão.
ms.assetid: da957aca-1655-4e8d-9e7b-4da0f253293b
title: PageBlackGenerationProcessingUnderColorAdditionLevel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e1fb6866dae4eb4a39de5c2b3b5d678a7388d703
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/05/2021
ms.locfileid: "104172567"
---
# <a name="pageblackgenerationprocessingundercoloradditionlevel"></a>PageBlackGenerationProcessingUnderColorAdditionLevel

Este tópico não é atual. Para obter as informações mais atuais, consulte a [especificação do esquema de impressão](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).

Descreve a quantidade de tinta de desvio (em proporção de componente cinza) para adicionar a áreas em que o GCR/UCR gerou "BlackInkLimit" (ou UCAStart, se especificado) nas áreas neutras escuras e quase neutros.

-   [Informações do elemento](#element-information)
-   [Conteúdo da estrutura](#structure-content)

## <a name="element-information"></a>Informações do elemento



| Nome                       |                                                            |
|----------------------------|------------------------------------------------------------|
| Tipo de elemento <br/>   | ParameterDef<br/>                                    |
| Prefixo de escopo <br/> | ?<br/>                                            |
| Observações <br/>          | Vinculado ao elemento PageBlackGenerationProcessing<br/> |



 

## <a name="structure-content"></a>Conteúdo da estrutura

A estrutura XML desse elemento é:

``` syntax
<psf:ParameterDef name="psk:PageBlackGenerationProcessingUnderColorAdditionLevel">
  <psf:Property name="psf:DataType">
    <psf:Value xsi:type="xs:string">xs:integer</psf:Value>
  </psf:Property>
  <psf:Property name="psf:DefaultValue">
    <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
  </psf:Property>
  <psf:Property name="psf:MaxValue">
    <psf:Value xsi:type="xs:integer">100</psf:Value>
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
    <psf:Value xsi:type="xs:string">percent</psf:Value>
  </psf:Property>
</psf:ParameterDef>
```

## <a name="structure-properties"></a>Propriedades da estrutura

A tabela a seguir descreve as características das variáveis definidas na estrutura XML.



| Propriedade                | xsi:type           | Valor                      |
|-------------------------|--------------------|----------------------------|
| Tipo de dados<br/>     | string<br/>  | xs:integer<br/>      |
| DefaultValue<br/> | string<br/>  | não definido<br/>       |
| MaxValue<br/>     | Número inteiro<br/> | 100<br/>             |
| MinValue<br/>     | integer<br/> | 0<br/>               |
| Vários<br/>     | integer<br/> | 1<br/>               |
| Obrigatório<br/>    | string<br/>  | PSK: condicional<br/> |
| UnitType<br/>     | string<br/>  | {1&gt;percent&lt;1}<br/>         |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Especificação de esquema de impressão](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




