---
description: Contém informações sobre uma determinada palavra de tinta na nota do diário, incluindo posição, alternativas e dados reais de tinta.
ms.assetid: 1e197716-bf6c-4a28-ae66-38aa59d7371d
title: Elemento InkWord
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 342da6688088d37065af7af8600ac2e1e7003599914b320b21e49d39235dc712
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118717314"
---
# <a name="inkword-element"></a>Elemento InkWord

Contém informações sobre uma determinada palavra de tinta na nota do diário, incluindo posição, alternativas e dados reais de tinta.

## <a name="definition"></a>Definição

``` syntax
<xs:element name="InkWord" type="InkWordType" />
```

## <a name="parent-elements"></a>Elementos pai

[**GroupNode**](groupnode-element.md)

[**Linha**](line-element.md)

## <a name="child-elements"></a>Elementos filho

[**ScalarTransform**](scalartransform-element.md)

[**Alternativolist**](alternatelist-element.md)

[**CanReClassify**](canreclassify-element.md)

[**Confiança**](confidence-element.md)

[**InkObject**](inkobject-element.md)

## <a name="attributes"></a>Atributos



| Atributo  | Type                      | Obrigatório | Descrição                                                                             | Valores possíveis           |
|------------|---------------------------|----------|-----------------------------------------------------------------------------------------|---------------------------|
| **Left**   | **xs:integer**            | Obrigatório | A distância da origem até o ponto mais à esquerda na caixa delimitadora para o elemento. | Qualquer inteiro.              |
| **Top**    | **xs:integer**            | Obrigatório | A distância da origem até o ponto superior na caixa delimitadora para o elemento.  | Qualquer inteiro.              |
| **Largura**  | **xs:nonNegativeInteger** | Obrigatório | A largura da caixa delimitadora para o elemento.                                          | Qualquer inteiro não negativo. |
| **Altura** | **xs:nonNegativeInteger** | Obrigatório | A altura da caixa delimitadora para o elemento.                                         | Qualquer inteiro não negativo. |



 

> [!WARNING]
> O mapeamento de coordenadas internas da palavra de tinta é a unidade de métrica em inglês e um multiplicador de 2,54 precisará ser usado pelo seu aplicativo para converter os valores de largura e altura nas unidades HIMETRIC usadas pelas APIs da plataforma do Tablet PC.

 

## <a name="element-information"></a>Informações do elemento



|  Elemento     | Valor                                                     |
|--------------|-------------------------------------------------------------|
| Tipo de elemento | ComplexType [**InkWordType**](inkwordtype-complex-type.md) |
| Namespace    | urn: esquemas-Microsoft-com: Tablet: RichInk                  |
| Nome do esquema  | Leitor de diário                                              |



 

 

 



