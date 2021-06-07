---
description: Contém informações sobre uma determinada palavra de tinta na nota Do diário, incluindo posição, alternativas e os dados reais de tinta.
ms.assetid: 1e197716-bf6c-4a28-ae66-38aa59d7371d
title: Elemento InkWord
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e8dc9baea7cda0346e82c11331c45f453e61f192
ms.sourcegitcommit: c3f669dc1d52278432bf75ad9fddba3257d26aa2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/04/2021
ms.locfileid: "111432388"
---
# <a name="inkword-element"></a>Elemento InkWord

Contém informações sobre uma determinada palavra de tinta na nota Do diário, incluindo posição, alternativas e os dados reais de tinta.

## <a name="definition"></a>Definição

``` syntax
<xs:element name="InkWord" type="InkWordType" />
```

## <a name="parent-elements"></a>Elementos pai

[**GroupNode**](groupnode-element.md)

[**Linha**](line-element.md)

## <a name="child-elements"></a>Elementos filho

[**ScalarTransform**](scalartransform-element.md)

[**AlternateList**](alternatelist-element.md)

[**CanReClassify**](canreclassify-element.md)

[**Confiança**](confidence-element.md)

[**InkObject**](inkobject-element.md)

## <a name="attributes"></a>Atributos



| Atributo  | Type                      | Obrigatório | Descrição                                                                             | Valores possíveis           |
|------------|---------------------------|----------|-----------------------------------------------------------------------------------------|---------------------------|
| **Left**   | **xs:integer**            | Obrigatório | A distância da origem até o ponto mais à esquerda na caixa delimitante do elemento. | Qualquer inteiro.              |
| **Top**    | **xs:integer**            | Obrigatório | A distância da origem até o ponto mais alto na caixa delimitada do elemento.  | Qualquer inteiro.              |
| **Largura**  | **xs:nonNegativeInteger** | Obrigatório | A largura da caixa delimitada para o elemento.                                          | Qualquer inteiro não negativo. |
| **Altura** | **xs:nonNegativeInteger** | Obrigatório | A altura da caixa delimitada para o elemento.                                         | Qualquer inteiro não negativo. |



 

> [!WARNING]
> O mapeamento de coordenadas interno da palavra de tinta é Unidades de Métrica em Inglês e um multiplicador de 2,54 precisará ser usado pelo seu aplicativo para converter os valores de Largura e Altura nas unidades HIMETRIC usadas pelas APIs da plataforma tablet PC.

 

## <a name="element-information"></a>Informações do elemento



|  Elemento     | Valor                                                     |
|--------------|-------------------------------------------------------------|
| Tipo de elemento | [**ComplexType InkWordType**](inkwordtype-complex-type.md) |
| Namespace    | urn:schemas-microsoft-com:tabletpc:richink                  |
| Nome do esquema  | Leitor de Diário                                              |



 

 

 



