---
description: Contém informações de título sobre a nota do diário.
ms.assetid: efeed3a6-de5e-4698-9dc3-d0acb3d13dee
title: Elemento Title
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 05661be8566cf4136194af4e08d8f9774d3413dc
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122473132"
---
# <a name="title-element"></a>Elemento Title

Contém informações de título sobre a nota do diário.

## <a name="definition"></a>Definição

``` syntax
<xs:element name="Title" type="TitleType" minOccurs="0" />
```

## <a name="parent-elements"></a>Elementos pai

[**Telas**](stationery-element.md)

## <a name="child-elements"></a>Elementos filho

[**TitleArea**](titlearea-element.md)

## <a name="attributes"></a>Atributos




| Atributo | Type | Obrigatório | Descrição | Valores possíveis | 
|-----------|------|----------|-------------|-----------------|
| <strong>Estilo</strong> | <strong>xs:string</strong> | Obrigatório | Especifica o tipo de borda ao redor do título da nota. | <ul><li>Nenhum</li><li>SolidSquare</li><li>OutlineSquare</li><li>SolidRoundRect</li><li>OutlineRoundRect</li><li>SolidRoundRectDottedBaseline</li></ul> | 
| <strong>Datastyle</strong> | <strong>xs:string</strong> | Obrigatório | Define se o título inclui uma data ou não. | <ul><li>Nenhum</li><li>Short</li></ul> | 
| <strong>Cor</strong> | <a href="colortype-simple-type.md"><strong>SimpleType de ColorType</strong></a> | Opcional | Especifica a cor do plano de fundo. | Confira <a href="colortype-simple-type.md"><strong>simpleType de ColorType</strong></a>. | 




 

## <a name="element-information"></a>Informações do elemento



| Elemento      | Valor                                                   |
|--------------|---------------------------------------------------------|
| Tipo de elemento | ComplexType de [**títulotype**](titletype-complex-type.md) |
| Namespace    | urn: esquemas-Microsoft-com: Tablet: RichInk              |
| Nome do esquema  | Leitor de diário                                          |



 

 

 



