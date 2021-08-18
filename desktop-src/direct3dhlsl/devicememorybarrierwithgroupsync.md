---
title: Função DeviceMemoryBarrierWithGroupSync
description: Bloqueia a execução de todos os threads em um grupo até que todos os acessos à memória do dispositivo tenham sido concluídos e que todos os threads do grupo tenham atingido essa chamada.
ms.assetid: 77c54064-a996-4c51-84b5-7da60e884c4f
keywords:
- HLSL da função DeviceMemoryBarrierWithGroupSync
topic_type:
- apiref
api_name:
- DeviceMemoryBarrierWithGroupSync
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 2567a209b86481cd0f25922e8e3b1cf947196a2c799344089591cf70fa3624fd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119625816"
---
# <a name="devicememorybarrierwithgroupsync-function"></a>Função DeviceMemoryBarrierWithGroupSync

Bloqueia a execução de todos os threads em um grupo até que todos os acessos à memória do dispositivo tenham sido concluídos e que todos os threads do grupo tenham atingido essa chamada.

## <a name="syntax"></a>Sintaxe

``` syntax
void DeviceMemoryBarrierWithGroupSync(void);
```

## <a name="parameters"></a>Parâmetros

Essa função não tem parâmetros.

## <a name="return-value"></a>Valor retornado

Essa função não retorna um valor.

## <a name="remarks"></a>Comentários

### <a name="minimum-shader-model"></a>Modelo de sombreamento mínimo

Essa função tem suporte nos seguintes modelos de sombreador.



| Modelo de Sombreador                                                                | Com suporte |
|-----------------------------------------------------------------------------|-----------|
| [Modelo](d3d11-graphics-reference-sm5.md) de sombreador 5 e modelos de sombreador mais altos | sim       |



 

Essa função tem suporte nos seguintes tipos de sombreadores:



| Vértice | Envoltória | Domínio | Geometry | 16x16 | Computação |
|--------|------|--------|----------|-------|---------|
|        |      |        |          |       | x       |



 

## <a name="see-also"></a>Confira também

<dl> <dt>

[Funções intrínsecas](dx-graphics-hlsl-intrinsic-functions.md)
</dt> <dt>

[Modelo de sombreador 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




