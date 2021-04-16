---
title: O recurso D1106 é do tipo incorreto
ms.assetid: 79a618cb-1d05-4895-b801-7663890b456a
description: O recurso fornecido não é de um tipo esperado.
keywords:
- O recurso D1106 está errado no tipo Direct2D
topic_type:
- apiref
api_name:
- D1106 Resource Is Wrong Type
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.custom: seodec18
ms.openlocfilehash: 5c38ef36319b8021de918a798c94a3be0683a7b7
ms.sourcegitcommit: 80ee822f6ebcbcc8f60042e0d14a39ef6989c731
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/27/2021
ms.locfileid: "105747673"
---
# <a name="d1106-resource-is-wrong-type"></a>D1106: tipo de recurso incorreto

O recurso de recurso fornecido \[  \] não é de um tipo esperado.

## <a name="placeholders"></a>Espaços reservados

<dl> <dt>

<span id="resource"></span><span id="RESOURCE"></span>*Kit*
</dt> <dd>

O endereço do recurso.

</dd> </dl> 




 

## <a name="possible-causes"></a>Possíveis causas

Uma interface foi convertida de forma inadequada e usada como parâmetro para um método ou função.

## <a name="examples"></a>Exemplos

O exemplo a seguir passa um [**ID2D1SolidColorBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1solidcolorbrush) quando um [**ID2D1Geometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1geometry) é esperado.


```C++
        m_pRenderTarget->FillGeometry(
            (ID2D1Geometry*)m_pYellowGreenBrush,
            m_pYellowGreenBrush
            );
```



Este exemplo produz a seguinte mensagem de depuração:

``` syntax
DEBUG ERROR - The given resource[003A2C98] is not of an expected type
```

## <a name="fixes"></a>Correções

Use o tipo exigido pelo método.

 

 
