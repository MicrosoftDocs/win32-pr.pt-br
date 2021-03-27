---
title: 'Função RWStructuredBuffer:: IncrementCounter (Httpserv. h)'
description: Incrementa o contador oculto do objeto.
ms.assetid: 66385d4f-6db8-49ae-a73a-49089695f5ee
keywords:
- HLSL da função IncrementCounter
topic_type:
- apiref
api_name:
- IncrementCounter
api_location:
- httpserv.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c0002f82873de1c56ce5a7d79c9adb13bdf7ebc0
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104298748"
---
# <a name="incrementcounter-function"></a>Função IncrementCounter

Incrementa o contador oculto do objeto.

## <a name="syntax"></a>Sintaxe

``` syntax
uint IncrementCounter(void);
```

## <a name="parameters"></a>Parâmetros

Essa função não tem parâmetros.

## <a name="return-value"></a>Valor retornado

Tipo: **uint**

O valor do contador incrementado previamente.

## <a name="remarks"></a>Comentários

O modo de exibição de acesso não ordenado associado deve ter o [**\_ \_ \_ \_ contador de sinalizador UAV de buffer de D3D11**](/windows/desktop/api/d3d11/ne-d3d11-d3d11_buffer_uav_flag) definido durante a criação para que esse método funcione.

Um recurso estruturado pode ser indexado ainda mais com base nos nomes de componentes das estruturas.

Essa função tem suporte para os seguintes tipos de sombreadores:



| Vértice | Envoltória | Domínio | Geometria | 16x16 | Computação |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | x     | x       |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|---------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>Httpserv. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[RWStructuredBuffer](sm5-object-rwstructuredbuffer.md)
</dt> <dt>

[Modelo de sombreador 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

