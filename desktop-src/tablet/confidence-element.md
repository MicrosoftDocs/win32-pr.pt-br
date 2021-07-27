---
description: Contém a classificação de confiança retornada pelo analisador de tinta do Diário para o InkWord.
ms.assetid: cb0ed0d0-5e2f-44a3-b72b-61cbfd22bae8
title: Elemento Confidence
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a5fdaaed8d9c57822ad94ec49183a399ed317917
ms.sourcegitcommit: 5a78723ad484955ac91a23cf282cf9c176c1eab6
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/22/2021
ms.locfileid: "114436490"
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



 

 

 



