---
title: 'RWStructuredBuffer: função ecrementCounter do:D (Httpserv. h)'
description: Decrementa o contador oculto do objeto.
ms.assetid: 24bc0b63-a482-4fa5-9898-2d43bca20cf4
keywords:
- HLSL da função DecrementCounter
topic_type:
- apiref
api_name:
- DecrementCounter
api_location:
- httpserv.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a56641054bb4e9ed4b1865d00c662b0de2afa1a0
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104968644"
---
# <a name="decrementcounter-function"></a>Função DecrementCounter

Decrementa o contador oculto do objeto.

## <a name="syntax"></a>Sintaxe

``` syntax
uint DecrementCounter(void);
```

## <a name="parameters"></a>Parâmetros

Essa função não tem parâmetros.

## <a name="return-value"></a>Valor retornado

Tipo: **uint**

O valor do contador de pós-decrementado.

## <a name="remarks"></a>Comentários

O modo de exibição de acesso não ordenado associado deve ter o [**\_ \_ \_ \_ contador de sinalizador UAV de buffer D3D11**](/windows/desktop/api/d3d11/ne-d3d11-d3d11_buffer_uav_flag) definido durante a creationfor desse método funcionar.

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

 

