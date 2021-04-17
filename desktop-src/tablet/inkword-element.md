---
description: Contém informações sobre uma determinada palavra de tinta na nota do diário, incluindo posição, alternativas e dados reais de tinta.
ms.assetid: 1e197716-bf6c-4a28-ae66-38aa59d7371d
title: Elemento InkWord
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 179fb5e2bcce2e01f684f0b39d662e8538c7d27e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105782624"
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
| **Mantida**   | **xs:integer**            | Obrigatório | A distância da origem até o ponto mais à esquerda na caixa delimitadora para o elemento. | Qualquer inteiro.              |
| **Top**    | **xs:integer**            | Obrigatório | A distância da origem até o ponto superior na caixa delimitadora para o elemento.  | Qualquer inteiro.              |
| **Largura**  | **xs:nonNegativeInteger** | Obrigatório | A largura da caixa delimitadora para o elemento.                                          | Qualquer inteiro não negativo. |
| **Altura** | **xs:nonNegativeInteger** | Obrigatório | A altura da caixa delimitadora para o elemento.                                         | Qualquer inteiro não negativo. |



 

> [!WARNING]
> O mapeamento de coordenadas internas da palavra de tinta é a unidade de métrica em inglês e um multiplicador de 2,54 precisará ser usado pelo seu aplicativo para converter os valores de largura e altura nas unidades HIMETRIC usadas pelas APIs da plataforma do Tablet PC.

 

## <a name="element-information"></a>Informações do elemento



|              |                                                             |
|--------------|-------------------------------------------------------------|
| Tipo de elemento | ComplexType [**InkWordType**](inkwordtype-complex-type.md) |
| Namespace    | urn: esquemas-Microsoft-com: Tablet: RichInk                  |
| Nome do esquema  | Leitor de diário                                              |



 

 

 



