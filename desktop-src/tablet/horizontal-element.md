---
description: Contém informações de formatação para as linhas horizontais usadas para a papelaria em uma nota de Diário.
ms.assetid: e3c9e7a8-8de6-4871-b386-2186883f2ee7
title: Elemento Horizontal
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 97b66e8557d73570ce1a0b7eb7217c02435c51a6
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122482682"
---
# <a name="horizontal-element"></a>Elemento Horizontal

Contém informações de formatação para as linhas horizontais usadas para a papelaria em uma nota de Diário.

## <a name="definition"></a>Definição

``` syntax
<xs:element name="Horizontal" type="HorizontalType" minOccurs="0" />
```

## <a name="parent-elements"></a>Elementos pai

[**LineLayout**](linelayout-element.md)

## <a name="child-elements"></a>Elementos filho

Nenhum.

## <a name="attributes"></a>Atributos




| Atributo | Type | Obrigatório | Descrição | Valores possíveis | 
|-----------|------|----------|-------------|-----------------|
| <strong>Estilo</strong> | <a href="linelayoutstyletype-simple-type.md"><strong>SimpleType LineLayoutStyleType</strong></a> | Obrigatório | Especifica o tipo de linha a ser desenhada. | <ul><li>Nenhum</li><li>Sólido</li><li>Traço</li><li>Ponto</li><li>DashDot</li><li>DashDotDot</li><li>Double</li></ul> | 
| <strong>Cor</strong> | <a href="colortype-simple-type.md"><strong>ColorType</strong></a> simpleType | Opcional | Cor do elemento. | Um valor RGB hexadecimal. Corresponde à seguinte expressão regular: #[0-9a-zA-Z] {6} . Por exemplo, #4a79B5.<br /> | 
| <strong>SpacingBefore</strong> | <strong>xs:nonNegativeInteger</strong> | Opcional | Espaçamento antes do elemento . | Qualquer inteiro não negativo. | 
| <strong>SpacingBetween</strong> | <strong>xs:nonNegativeInteger</strong> | Opcional | Espaçamento entre esse elemento e elementos ao redor. | Qualquer inteiro não negativo. | 




 

## <a name="element-information"></a>Informações do elemento



|  Elemento     | Valor                                                     |
|--------------|-------------------------------------------------------------------|
| Tipo de elemento | [**ComplexType HorizontalType**](horizontaltype-complex-type.md) |
| Namespace    | urn:schemas-microsoft-com:tabletpc:richink                        |
| Nome do esquema  | Leitor de Diário                                                    |



 

 

 




