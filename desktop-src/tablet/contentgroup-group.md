---
description: Define um grupo que contém um conjunto de conteúdo agrupado em uma nota de Diário.
ms.assetid: e2561be1-03ce-41f7-9ad4-197d75411c48
title: Grupo ContentGroup
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 02e4291da1912c43674871c06fb803e1936f7178
ms.sourcegitcommit: c3f669dc1d52278432bf75ad9fddba3257d26aa2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/04/2021
ms.locfileid: "111432608"
---
# <a name="contentgroup-group"></a>Grupo ContentGroup

Define um grupo que contém um conjunto de conteúdo agrupado em uma nota de Diário.

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

[**Text**](text-element.md)

[**Imagem**](docimage-element.md)

[**Bandeira**](flag-element.md)

## <a name="attributes"></a>Atributos



| Atributo  | Type                      | Obrigatório | Descrição                                                                                        | PossibleValues                       |
|------------|---------------------------|----------|----------------------------------------------------------------------------------------------------|--------------------------------------|
| **Left**   | **xs:integer**            | Obrigatório | A distância da origem até o ponto mais à esquerda na caixa delimitante do elemento.<br/> | Qualquer inteiro.<br/>              |
| **Top**    | **xs:integer**            | Obrigatório | A distância da origem até o ponto mais alto na caixa delimitada do elemento.<br/>  | Qualquer inteiro.<br/>              |
| **Largura**  | **xs:nonNegativeInteger** | Obrigatório | A largura da caixa delimitada para o elemento.<br/>                                          | Qualquer inteiro não negativo.<br/> |
| **Altura** | **xs:nonNegativeInteger** | Obrigatório | A altura da caixa delimitada para o elemento.<br/>                                         | Qualquer inteiro não negativo.<br/> |



 

## <a name="type-information"></a>Informações do Tipo



|  Elemento     | Valor                                                     |
|-------------|--------------------------------------------|
| Namespace   | urn:schemas-microsoft-com:tabletpc:richink |
| Nome do esquema | Leitor de Diário                             |



 

 

 




