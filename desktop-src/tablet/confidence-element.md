---
description: Contém a classificação de confiança retornada pelo analisador de tinta do diário para o InkWord.
ms.assetid: cb0ed0d0-5e2f-44a3-b72b-61cbfd22bae8
title: Elemento de confiança
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3cef4869776a6cafc4e6ef4758649b918e0b5988
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104089862"
---
# <a name="confidence-element"></a>Elemento de confiança

Contém a classificação de confiança retornada pelo analisador de tinta do diário para o [**InkWord**](inkword-element.md).

## <a name="definition"></a>Definição

``` syntax
<xs:element name="Confidence" type="xs:string" minOccurs="0" />
```

## <a name="parent-elements"></a>Elementos pai

[**InkWord**](inkword-element.md)

## <a name="values"></a>Valores

Os valores válidos para esse campo incluem "0", "1" e "2". 0 indica forte confiança, 1 indica confiança intermediária e 2 indica má confiança.

## <a name="child-elements"></a>Elementos filho

Nenhum.

## <a name="attributes"></a>Atributos

Nenhum.

## <a name="element-information"></a>Informações do elemento



|              |                                            |
|--------------|--------------------------------------------|
| Tipo de elemento | **xs:string**                              |
| Namespace    | urn: esquemas-Microsoft-com: Tablet: RichInk |
| Nome do esquema  | Leitor de diário                             |



 

 

 



