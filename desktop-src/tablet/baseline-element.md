---
description: Fornece informações (x, y) para os pontos inicial e final da linha de base de um parágrafo no documento do diário. O espaço de coordenadas usado para esses valores é HIMETRIC.
ms.assetid: ff6a97ad-0e48-4128-8f94-24802b6ddc05
title: Elemento de linha de base
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5b64986707eaa1b382d2f88851367b9147c59c5b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104164257"
---
# <a name="baseline-element"></a>Elemento de linha de base

Fornece informações (x, y) para os pontos inicial e final da linha de base de um parágrafo no documento do diário. O espaço de coordenadas usado para esses valores é **HIMETRIC**.

## <a name="definition"></a>Definição

``` syntax
<xs:element name="Baseline" type="BaseLineType" />
```

## <a name="parent-elements"></a>Elementos pai

[**ParagraphLineMetrics**](paragraphlinemetrics-element.md)

## <a name="child-elements"></a>Elementos filho

Nenhum.

## <a name="attributes"></a>Atributos



| Atributo  | Type                      | Obrigatório | Descrição                                                      | Valores possíveis           |
|------------|---------------------------|----------|------------------------------------------------------------------|---------------------------|
| **StartX** | **xs:nonNegativeInteger** | Obrigatório | O valor X do ponto que marca o início da linha de base. | Qualquer inteiro não negativo. |
| **Inicialização** | **xs:nonNegativeInteger** | Obrigatório | O valor Y do ponto que marca o início da linha de base. | Qualquer inteiro não negativo. |
| **EndX**   | **xs:nonNegativeInteger** | Obrigatório | O valor X do ponto que marca o final da linha de base.       | Qualquer inteiro não negativo. |



 

## <a name="element-information"></a>Informações do elemento



|              |                                                               |
|--------------|---------------------------------------------------------------|
| Tipo de elemento | ComplexType de [**baselinetype**](baselinetype-complex-type.md) |
| Namespace    | urn: esquemas-Microsoft-com: Tablet: RichInk                    |
| Nome do esquema  | Leitor de diário                                                |



 

 

 



