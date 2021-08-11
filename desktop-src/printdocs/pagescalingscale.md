---
description: Obter informações sobre o parâmetro PageScalingScale. Este tópico não é atual. Para obter as informações mais atuais, consulte a Especificação de Esquema de Impressão.
ms.assetid: 49a60a94-fb65-4439-bebf-3f77ea0861fe
title: PageScalingScale
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 01b8a46c0c0055e48f5feb536295ffc1045a4e71df2ae353506ea6ed9f592e7b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118234386"
---
# <a name="pagescalingscale"></a>PageScalingScale

Este tópico não é atual. Para obter as informações mais atuais, consulte a [Especificação de Esquema de Impressão](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).

Especifica o fator de dimensionamento para dimensionamento quadrado personalizado.

-   [Informações do elemento](#element-information)
-   [Conteúdo da estrutura](#structure-content)

## <a name="element-information"></a>Informações do elemento



| Name | Valor |
|----------------------------|---------------------------------------------------------|
| Tipo de elemento <br/>   | ParameterDef<br/>                                 |
| Prefixo de definição de scoping <br/> | ?<br/>                                         |
| Observações <br/>          | Vinculado ao elemento PageScaling, opção Personalizada<br/> |



 

## <a name="structure-content"></a>Conteúdo da estrutura

A estrutura XML desse elemento é:

``` syntax
<psf:ParameterDef name="psk:PageScalingScale">
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
    <psf:Value xsi:type="xs:integer">1</psf:Value>
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
| DefaultValue<br/> | Número inteiro<br/> | não definido<br/>       |
| MaxValue<br/>     | Número inteiro<br/> | não definido<br/>       |
| Minvalue<br/>     | integer<br/> | 1<br/>               |
| Obrigatório<br/>    | string<br/>  | psk:Conditional<br/> |
| Vários<br/>     | integer<br/> | 1<br/>               |
| Unittype<br/>     | string<br/>  | {1&gt;percent&lt;1}<br/>         |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Especificação de esquema de impressão](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




