---
description: Define um grupo que contém um conjunto de conteúdo agrupado em uma nota do diário.
ms.assetid: e2561be1-03ce-41f7-9ad4-197d75411c48
title: Grupo de grupos de conteúdo
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c0085cc52a8fc29d3a51f4d1e1c8f42128b63db9e166a7a1c436dc15bff70a36
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120009006"
---
# <a name="contentgroup-group"></a>Grupo de grupos de conteúdo

Define um grupo que contém um conjunto de conteúdo agrupado em uma nota do diário.

## <a name="definition"></a>Definição

``` syntax
<xs:group name="ContentGroup" >
  <xs:choice>
    <xs:element name="GroupNode" type="GroupNodeType" />
    <xs:element name="Paragraph" type="ParagraphType" />
    <xs:element name="InkWord" type="InkWordType" />
    <xs:element name="Drawing" type="DrawingType" />
    <xs:element name="Text" type="TextType" />
    <xs:element name="Image" type="ImageType" />
    <xs:element name="Flag" type="FlagType" />
    <xs:element name="Reflow" type="ReflowType" />
  </xs:choice>
</xs:group>
```

## <a name="child-elements"></a>Elementos filho

[**GroupNode**](groupnode-element.md)

[**Paragraph**](paragraph-element.md)

[**InkWord**](inkword-element.md)

[**Desenho**](drawing-element.md)

[**Texto**](text-element.md)

[**Imagem**](docimage-element.md)

[**Sinalizador**](flag-element.md)

## <a name="attributes"></a>Atributos



| Atributo  | Type                      | Obrigatório | Descrição                                                                                        | PossibleValues                       |
|------------|---------------------------|----------|----------------------------------------------------------------------------------------------------|--------------------------------------|
| **Left**   | **xs:integer**            | Obrigatório | A distância da origem até o ponto mais à esquerda na caixa delimitadora para o elemento.<br/> | Qualquer inteiro.<br/>              |
| **Top**    | **xs:integer**            | Obrigatório | A distância da origem até o ponto superior na caixa delimitadora para o elemento.<br/>  | Qualquer inteiro.<br/>              |
| **Largura**  | **xs:nonNegativeInteger** | Obrigatório | A largura da caixa delimitadora para o elemento.<br/>                                          | Qualquer inteiro não negativo.<br/> |
| **Altura** | **xs:nonNegativeInteger** | Obrigatório | A altura da caixa delimitadora para o elemento.<br/>                                         | Qualquer inteiro não negativo.<br/> |



 

## <a name="type-information"></a>Informações do Tipo



|  Elemento     | Valor                                                     |
|-------------|--------------------------------------------|
| Namespace   | urn: esquemas-Microsoft-com: Tablet: RichInk |
| Nome do esquema | Leitor de diário                             |



 

 

 




