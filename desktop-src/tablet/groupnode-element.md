---
description: Contém um conjunto de elementos&\# 8212; Parágrafo, InkWord, desenho, texto, imagem ou sinalizador&\# 8212; que são agrupados juntos na nota do diário.
ms.assetid: 59ee3037-7178-41c8-84d5-d5c68fa2cf9b
title: Elemento GroupNode
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cbc4d39a592b5b6328bd31ff37761cfd3f0138c0
ms.sourcegitcommit: c3f669dc1d52278432bf75ad9fddba3257d26aa2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/04/2021
ms.locfileid: "111432561"
---
# <a name="groupnode-element"></a>Elemento GroupNode

Contém um conjunto de elementos ([**parágrafo**](paragraph-element.md), [**InkWord**](inkword-element.md), [**desenho**](drawing-element.md), [**texto**](text-element.md), [**imagem**](image-element.md)ou [**sinalizador**](flag-element.md)) que são agrupados na nota do diário.

## <a name="definition"></a>Definição

``` syntax
<xs:element name="GroupNode" type="GroupNodeType" />
```

## <a name="parent-elements"></a>Elementos pai

[**Disputa**](content-element--journal-reader.md)

## <a name="child-elements"></a>Elementos filho

[**Paragraph**](paragraph-element.md)

[**InkWord**](inkword-element.md)

[**Desenho**](drawing-element.md)

[**Text**](text-element.md)

[**Imagem**](docimage-element.md)

[**Identificar**](flag-element.md)

## <a name="attributes"></a>Atributos



| Atributo  | Type                      | Obrigatório | Descrição                                                                             | Valores possíveis           |
|------------|---------------------------|----------|-----------------------------------------------------------------------------------------|---------------------------|
| **Left**   | **xs:integer**            | Obrigatório | A distância da origem até o ponto mais à esquerda na caixa delimitadora para o elemento. | Qualquer inteiro.              |
| **Top**    | **xs:integer**            | Obrigatório | A distância da origem até o ponto superior na caixa delimitadora para o elemento.  | Qualquer inteiro.              |
| **Largura**  | **xs:nonNegativeInteger** | Obrigatório | A largura da caixa delimitadora para o elemento.                                          | Qualquer inteiro não negativo. |
| **Altura** | **xs:nonNegativeInteger** | Obrigatório | A altura da caixa delimitadora para o elemento.                                         | Qualquer inteiro não negativo. |



 

## <a name="element-information"></a>Informações do elemento



|  Elemento     | Valor                                                     |
|--------------|-----------------------------------------------------------------|
| Tipo de elemento | ComplexType [**GroupNodeType**](groupnodetype-complex-type.md) |
| Namespace    | urn: esquemas-Microsoft-com: Tablet: RichInk                      |
| Nome do esquema  | Leitor de diário                                                  |



 

 

 



