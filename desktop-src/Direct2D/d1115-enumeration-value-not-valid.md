---
title: Valor de enumeração D1115 inválido
description: Valor de enumeração D1115 inválido
ms.assetid: cfffd2b8-a7d3-4a60-8586-81d8435936a6
keywords:
- O valor de enumeração D1115 não é válido Direct2D
topic_type:
- apiref
api_name:
- D1115 Enumeration Value Not Valid
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: edcfe70c67e61a3b8bfc435adfdaa017a1c62b22
ms.sourcegitcommit: 80ee822f6ebcbcc8f60042e0d14a39ef6989c731
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/27/2021
ms.locfileid: "105752369"
---
# <a name="d1115-enumeration-value-not-valid"></a>D1115: valor de enumeração inválido

O parâmetro de parâmetro \[  \] com \[ *valor* \] de valor para *interface*::*Method* não é um valor de enumeração válido.

## <a name="placeholders"></a>Espaços reservados

<dl> <dt>

<span id="parameter"></span><span id="PARAMETER"></span>*meter*
</dt> <dd>

O nome do parâmetro que recebeu o tipo inesperado.

</dd> <dt>

<span id="value"></span><span id="VALUE"></span>*valor*
</dt> <dd>

O valor de enumeração inválido.

</dd> <dt>

<span id="interface"></span><span id="INTERFACE"></span>*interface*
</dt> <dd>

O nome da interface à qual o *método* pertence.

</dd> <dt>

<span id="method"></span><span id="METHOD"></span>*forma*
</dt> <dd>

O nome do método que recebeu o valor de enumeração inválido.

</dd> </dl> 




 

## <a name="examples"></a>Exemplos

O exemplo a seguir especifica um valor de enumeração de [**\_ tipo de \_ destino \_ de renderização d2d1**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_render_target_type) de 30, que está fora do intervalo esperado.


```C++
        hr = m_pD2DFactory->CreateHwndRenderTarget(
            D2D1::RenderTargetProperties((D2D1_RENDER_TARGET_TYPE)(30)),
            D2D1::HwndRenderTargetProperties(m_hwnd, size),
            &m_pRenderTarget
            );
```



Este exemplo produz a seguinte mensagem de depuração:

``` syntax
D2D DEBUG ERROR - The parameter [renderTargetProperties->type] with value [30] 
for ID2D1Factory::CreateHwndRenderTarget is not a valid enumeration value.
```

## <a name="possible-causes"></a>Possíveis causas

Um parâmetro usou um valor de enumeração inválido.

## <a name="fixes"></a>Correções

Use um valor de enumeração válido.

> [!Note]  
> A camada de depuração atualmente verifica apenas os valores individuais de enumeração; Ele não verifica se uma combinação bit-de-bits é válida.

 

 

 
