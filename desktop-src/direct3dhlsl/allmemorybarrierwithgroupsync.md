---
title: Função AllMemoryBaoryWithGroupSync
description: Bloqueia a execução de todos os threads em um grupo até que todos os acessos de memória tenham sido concluídos e todos os threads no grupo tenham atingido essa chamada.
ms.assetid: 831830e7-19ce-41d0-b555-44a083b67cdc
keywords:
- Função AllMemoryBaoryWithGroupSync HLSL
topic_type:
- apiref
api_name:
- AllMemoryBarrierWithGroupSync
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 69d3c146ff04597b7eca13dd5cbef93dc1c79f81709353bf5b4fa1a993a8da22
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119626686"
---
# <a name="allmemorybarrierwithgroupsync-function"></a>Função AllMemoryBaoryWithGroupSync

Bloqueia a execução de todos os threads em um grupo até que todos os acessos de memória tenham sido concluídos e todos os threads no grupo tenham atingido essa chamada.

## <a name="syntax"></a>Sintaxe

``` syntax
void AllMemoryBarrierWithGroupSync(void);
```

## <a name="parameters"></a>Parâmetros

Essa função não tem parâmetros.

## <a name="return-value"></a>Valor retornado

Essa função não retorna um valor.

## <a name="remarks"></a>Comentários

Uma barreira de memória garante que as operações de memória pendentes tenham sido concluídas. Os threads são sincronizados em barreiras groupSync. Isso pode parar um thread ou threads se as operações de memória estão em andamento.

### <a name="minimum-shader-model"></a>Modelo de sombreador mínimo

Essa função tem suporte nos modelos de sombreador a seguir.



| Modelo de Sombreador                                                                | Com suporte |
|-----------------------------------------------------------------------------|-----------|
| [Modelo de sombreador 5](d3d11-graphics-reference-sm5.md) e modelos de sombreador superior | sim       |



 

Essa função tem suporte nos seguintes tipos de sombreadores:



| Vértice | Casco | Domínio | Geometry | Pixel | Computação |
|--------|------|--------|----------|-------|---------|
|        |      |        |          |       | x       |



 

## <a name="see-also"></a>Confira também

<dl> <dt>

[Funções intrínsecas](dx-graphics-hlsl-intrinsic-functions.md)
</dt> <dt>

[Modelo de sombreador 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




