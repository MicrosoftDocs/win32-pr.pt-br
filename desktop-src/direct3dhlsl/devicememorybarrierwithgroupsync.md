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
ms.openlocfilehash: 6a7a4a27b3256fb78c7b60b960fc5383cfd5b5d4
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/25/2019
ms.locfileid: "104293290"
---
# <a name="devicememorybarrierwithgroupsync-function"></a>Função DeviceMemoryBarrierWithGroupSync

Bloqueia a execução de todos os threads em um grupo até que todos os acessos à memória do dispositivo tenham sido concluídos e que todos os threads do grupo tenham atingido essa chamada.

## <a name="syntax"></a>Sintaxe

``` syntax
void DeviceMemoryBarrierWithGroupSync(void);
```

## <a name="parameters"></a>Parâmetros

Essa função não tem parâmetros.

## <a name="return-value"></a>Retornar valor

Essa função não retorna um valor.

## <a name="remarks"></a>Comentários

### <a name="minimum-shader-model"></a>Modelo de sombreamento mínimo

Essa função tem suporte nos seguintes modelos de sombreador.



| Modelo de Sombreador                                                                | Com suporte |
|-----------------------------------------------------------------------------|-----------|
| [Modelo](d3d11-graphics-reference-sm5.md) de sombreador 5 e modelos de sombreador mais altos | sim       |



 

Essa função tem suporte nos seguintes tipos de sombreadores:



| Vértice | Envoltória | Domínio | Geometria | 16x16 | Computação |
|--------|------|--------|----------|-------|---------|
|        |      |        |          |       | x       |



 

## <a name="see-also"></a>Confira também

<dl> <dt>

[Funções intrínsecas](dx-graphics-hlsl-intrinsic-functions.md)
</dt> <dt>

[Modelo de sombreador 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




