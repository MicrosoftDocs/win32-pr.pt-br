---
title: Função RWStructuredBuffer::IncrementCounter (Httpserv.h)
description: Incrementa o contador oculto do objeto.
ms.assetid: 66385d4f-6db8-49ae-a73a-49089695f5ee
keywords:
- Função IncrementCounter HLSL
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
ms.openlocfilehash: c39a857fc9a7a108cea05060caf86ce61479a382c5160f4f051c11423bc6a5d3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120095166"
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

O valor do contador pré-incrementado.

## <a name="remarks"></a>Comentários

A exibição de acesso não organizado vinculada deve ter O CONTADOR DE SINALIZADOR [**\_ \_ UAV \_ \_ de BUFFER D3D11**](/windows/desktop/api/d3d11/ne-d3d11-d3d11_buffer_uav_flag) definido durante a criação para que esse método funcione.

Um recurso estruturado pode ser indexado ainda mais com base nos nomes de componentes das estruturas.

Essa função tem suporte para os seguintes tipos de sombreadores:



| Vértice | Casco | Domínio | Geometry | Pixel | Computação |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | x     | x       |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|---------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>Httpserv.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[RWStructuredBuffer](sm5-object-rwstructuredbuffer.md)
</dt> <dt>

[Modelo de sombreador 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

