---
description: Contém as informações que descrevem o componente vertical das linhas na papelaria usada pela observação Do diário. Usado, por exemplo, quando a nota tem linhas de grade.
ms.assetid: af6f485e-13df-41bb-b57a-10d8393b83e7
title: Elemento Vertical
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f6f05ab8a2160dbf6b987177957e8285385fe4db
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122479502"
---
# <a name="vertical-element"></a>Elemento Vertical

Contém as informações que descrevem o componente vertical das linhas na papelaria usada pela observação Do diário. Usado, por exemplo, quando a nota tem linhas de grade.

## <a name="definition"></a>Definição

``` syntax
<xs:element name="Vertical" type="VerticalType" minOccurs="0" />
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



|  Elemento     | Valor                                                         |
|--------------|---------------------------------------------------------------|
| Tipo de elemento | [**ComplexType VerticalType**](verticaltype-complex-type.md) |
| Namespace    | urn:schemas-microsoft-com:tabletpc:richink                    |
| Nome do esquema  | Leitor de Diário                                                |



 

 

 




