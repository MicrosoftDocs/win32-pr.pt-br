---
description: Contém um conjunto de elementos&\# 8212; Parágrafo, InkWord, desenho, texto, imagem ou sinalizador&\# 8212; que são agrupados juntos na nota do diário.
ms.assetid: 59ee3037-7178-41c8-84d5-d5c68fa2cf9b
title: Elemento GroupNode
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6ee141691ef58d14e6c08a49544e9cf3ecf7540b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105747473"
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

[**Senha**](drawing-element.md)

[**Texto**](text-element.md)

[**Imagem**](docimage-element.md)

[**Sinalizador**](flag-element.md)

## <a name="attributes"></a>Atributos



| Atributo  | Type                      | Obrigatório | Descrição                                                                             | Valores possíveis           |
|------------|---------------------------|----------|-----------------------------------------------------------------------------------------|---------------------------|
| **Mantida**   | **xs:integer**            | Obrigatório | A distância da origem até o ponto mais à esquerda na caixa delimitadora para o elemento. | Qualquer inteiro.              |
| **Top**    | **xs:integer**            | Obrigatório | A distância da origem até o ponto superior na caixa delimitadora para o elemento.  | Qualquer inteiro.              |
| **Largura**  | **xs:nonNegativeInteger** | Obrigatório | A largura da caixa delimitadora para o elemento.                                          | Qualquer inteiro não negativo. |
| **Altura** | **xs:nonNegativeInteger** | Obrigatório | A altura da caixa delimitadora para o elemento.                                         | Qualquer inteiro não negativo. |



 

## <a name="element-information"></a>Informações do elemento



|              |                                                                 |
|--------------|-----------------------------------------------------------------|
| Tipo de elemento | ComplexType [**GroupNodeType**](groupnodetype-complex-type.md) |
| Namespace    | urn: esquemas-Microsoft-com: Tablet: RichInk                      |
| Nome do esquema  | Leitor de diário                                                  |



 

 

 



