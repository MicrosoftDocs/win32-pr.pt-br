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
ms.openlocfilehash: 8302f31cd07b81f4f78abe6a0a1fbcb2e6a1028f6153da69e55e0fb34977b585
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119671386"
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



| Vértice | Envoltória | Domínio | Geometry | 16x16 | Computação |
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

 

