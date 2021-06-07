---
description: Contém informações de localização e limite para o título da nota, se presente.
ms.assetid: b193f6c2-5f26-41f9-acc8-d734c426b069
title: Elemento TitleArea
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 88d563e8d7f6fc0107bc3302d3f8d94d29dfbfb8
ms.sourcegitcommit: c3f669dc1d52278432bf75ad9fddba3257d26aa2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/04/2021
ms.locfileid: "111432188"
---
# <a name="titlearea-element"></a>Elemento TitleArea

Contém informações de localização e limite para o título da nota, se presente.

## <a name="definition"></a>Definição

``` syntax
<xs:element name="TitleArea" type="TitleAreaType" minOccurs="0" />
```

## <a name="parent-elements"></a>Elementos pai

[**Título**](title-element.md)

## <a name="child-elements"></a>Elementos filho

Nenhum.

## <a name="attributes"></a>Atributos



| Atributo  | Type                      | Obrigatório | Descrição                                                                             | Valores possíveis           |
|------------|---------------------------|----------|-----------------------------------------------------------------------------------------|---------------------------|
| **Left**   | **xs:integer**            | Obrigatório | A distância da origem até o ponto mais à esquerda na caixa delimitadora para o elemento. | Qualquer inteiro.              |
| **Top**    | **xs:integer**            | Obrigatório | A distância da origem até o ponto superior na caixa delimitadora para o elemento.  | Qualquer inteiro.              |
| **Largura**  | **xs:nonNegativeInteger** | Obrigatório | A largura da caixa delimitadora para o elemento.                                          | Qualquer inteiro não negativo. |
| **Altura** | **xs:nonNegativeInteger** | Obrigatório | A altura da caixa delimitadora para o elemento.                                         | Qualquer inteiro não negativo. |



 

## <a name="element-information"></a>Informações do elemento



|   Elemento    | Valor                                                           |
|--------------|-----------------------------------------------------------------|
| Tipo de elemento | ComplexType [**TitleAreaType**](titleareatype-complex-type.md) |
| Namespace    | urn: esquemas-Microsoft-com: Tablet: RichInk                      |
| Nome do esquema  | Leitor de diário                                                  |



 

 

 



