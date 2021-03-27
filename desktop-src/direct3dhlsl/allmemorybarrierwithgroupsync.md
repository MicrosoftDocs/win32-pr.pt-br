---
title: Função AllMemoryBarrierWithGroupSync
description: Bloqueia a execução de todos os threads em um grupo até que todos os acessos à memória tenham sido concluídos e que todos os threads do grupo tenham atingido essa chamada.
ms.assetid: 831830e7-19ce-41d0-b555-44a083b67cdc
keywords:
- HLSL da função AllMemoryBarrierWithGroupSync
topic_type:
- apiref
api_name:
- AllMemoryBarrierWithGroupSync
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 1fc005545485b7f894729ab6c7d7975acfd5b6d4
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/25/2019
ms.locfileid: "104006698"
---
# <a name="allmemorybarrierwithgroupsync-function"></a>Função AllMemoryBarrierWithGroupSync

Bloqueia a execução de todos os threads em um grupo até que todos os acessos à memória tenham sido concluídos e que todos os threads do grupo tenham atingido essa chamada.

## <a name="syntax"></a>Sintaxe

``` syntax
void AllMemoryBarrierWithGroupSync(void);
```

## <a name="parameters"></a>Parâmetros

Essa função não tem parâmetros.

## <a name="return-value"></a>Retornar valor

Essa função não retorna um valor.

## <a name="remarks"></a>Comentários

Uma barreira de memória garante que as operações de memória pendentes tenham sido concluídas. Os threads são sincronizados em barreiras de GroupSync. Isso pode paralisar um thread ou threads se as operações de memória estiverem em andamento.

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

 

 




