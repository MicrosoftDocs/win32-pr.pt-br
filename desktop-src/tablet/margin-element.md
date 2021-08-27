---
description: Define as linhas de margem desenhadas na página.
ms.assetid: c3047706-affd-4feb-9d48-cfb4c7dd6fa0
title: Elemento Margin
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 78c264c2470d070353d1fd19340a161cf765bc05
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122478662"
---
# <a name="margin-element"></a>Elemento Margin

Define as linhas de margem desenhadas na página.

## <a name="definition"></a>Definição

``` syntax
<xs:complexType name="MarginType">
   <xs:attribute name="Style" use="required" type="LineLayoutStyleType" />
   <xs:attribute name="Color" type="ColorType" />
   <xs:attribute name="Type" type="MarginTypeType" />
   <xs:attribute name="Spacing" type="xs:positiveInteger" />
</xs:complexType>
```

## <a name="parent-elements"></a>Elementos pai

Nenhum.

## <a name="child-elements"></a>Elementos filho

Nenhum..

## <a name="attributes"></a>Atributos




| Atributo | Type | Obrigatório | Descrição | Valores possíveis | 
|-----------|------|----------|-------------|-----------------|
| <strong>Estilo</strong> | <a href="linelayoutstyletype-simple-type.md"><strong>LineLayoutStyleType</strong></a> simpleType | Obrigatório | Especifica o tipo de linha a ser desenhada. | <ul><li>Nenhum</li><li>Sólido</li><li>Traço</li><li>Ponto</li><li>DashDot</li><li>DashDotDot</li><li>Double</li></ul> | 
| <strong>Cor</strong> | SimpleType de <a href="colortype-simple-type.md"><strong>ColorType</strong></a> | Opcional | Cor do elemento. | Um valor RGB hexadecimal. Corresponde à seguinte expressão regular: # [0-9A-zA-Z] {6} . Por exemplo, #4a79B5.<br /> | 
| <strong>Tipo</strong> | <a href="margintypetype-simple-type.md"><strong>MarginTypeType</strong></a> simpleType | Opcional | Indica a margem esquerda ou direita. | <ul><li>Esquerda</li><li>Direita</li></ul> | 
| <strong>Espaçamento</strong> | <strong>xs:nonNegativeInteger</strong> | Opcional | Espaçamento entre a borda da página e a margem. | Qualquer inteiro não negativo. | 




 

## <a name="element-information"></a>Informações do elemento



|  Elemento     | Valor                                                     |
|--------------|-----------------------------------------------------------|
| Tipo de elemento | ComplexType de [**margintype**](margintype-complex-type.md) |
| Namespace    | urn: esquemas-Microsoft-com: Tablet: RichInk                |
| Nome do esquema  | Leitor de diário                                            |



 

 

 




