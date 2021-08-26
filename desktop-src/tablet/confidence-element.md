---
description: Contém a classificação de confiança retornada pelo analisador de tinta do Diário para o InkWord.
ms.assetid: cb0ed0d0-5e2f-44a3-b72b-61cbfd22bae8
title: Elemento Confidence
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e86e4169767f3bf40d49e71e84214d50d3c0c0b4ecf5d3f7a9034ee6c8ea279d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119936976"
---
# <a name="confidence-element"></a>Elemento Confidence

Contém a classificação de confiança retornada pelo analisador de tinta do Diário para [**o InkWord.**](inkword-element.md)

## <a name="definition"></a>Definição

``` syntax
<xs:element name="Confidence" type="xs:string" minOccurs="0" />
```

## <a name="parent-elements"></a>Elementos pai

[**InkWord**](inkword-element.md)

## <a name="values"></a>Valores

Os valores válidos para esse campo incluem "0", "1" e "2". 0 indica confiança forte, 1 indica confiança intermediária e 2 indica Confiança ruim.

## <a name="child-elements"></a>Elementos filho

Nenhum.

## <a name="attributes"></a>Atributos

Nenhum.

## <a name="element-information"></a>Informações do elemento



|                  | Valor                                      |
|------------------|--------------------------------------------|
| **Tipo de elemento** | xs:string                                  |
| **Namespace**    | urn:schemas-microsoft-com:tabletpc:richink |
| **Nome do esquema**  | Leitor de Diário                             |



 

 

 



