---
title: D1114 de ponteiro nulo não opcional
ms.assetid: 62f0f247-8359-4f75-b3ce-195202d491d5
description: 'O parâmetro do método interface:: não é opcional. Um ponteiro nulo foi passado. isso fará com que o Direct2D falhe.'
keywords:
- D1114 nulo de ponteiro não opcional Direct2D
topic_type:
- apiref
api_name:
- D1114 Non Optional Pointer NULL
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.custom: seodec18
ms.openlocfilehash: fa5213eabfb4b22b9a37927495f5058cbfeb0b86b0f1f8b8f3a4ba1a2a2bdbb6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118666205"
---
# <a name="d1114-non-optional-pointer-null"></a>D1114: ponteiro não opcional nulo

O \[ *parâmetro* \] de parâmetro para o *método* *interface*:: não é opcional. Um ponteiro **nulo** foi passado. isso fará com que o Direct2D falhe.

### <a name="placeholders"></a>Espaços reservados

<dl> <dt>

<span id="parameter"></span><span id="PARAMETER"></span>*meter*
</dt> <dd>

O nome do parâmetro que contém o ponteiro **nulo** .

</dd> <dt>

<span id="interface"></span><span id="INTERFACE"></span>*interface*
</dt> <dd>

O nome da interface à qual o *método* pertence.

</dd> <dt>

<span id="method"></span><span id="METHOD"></span>*forma*
</dt> <dd>

O nome do método que recebeu o parâmetro inválido.

</dd> </dl> 




 

### <a name="examples"></a>Exemplos

O exemplo a seguir mostra que o método [**FillGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillgeometry) recebe um ponteiro nulo para o parâmetro *Geometry* não opcional.


```C++
        m_pRenderTarget->FillGeometry(NULL, m_pYellowGreenBrush);
```



Este exemplo produz a seguinte mensagem de depuração:

``` syntax
D2D DEBUG ERROR - The parameter [geometry] for ID2D1RenderTarget::FillGeometry is not optional. 
A NULL pointer was passed. This will cause Direct2D to crash.
```

## <a name="possible-causes"></a>Possíveis causas

Um ponteiro nulo foi passado para um parâmetro não opcional.

## <a name="fixes"></a>Correções

Certifique-se de que um parâmetro não opcional não tenha um ponteiro nulo.

 

 
