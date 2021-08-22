---
title: Função AllMemoryBarrier
description: Bloqueia a execução de todos os threads em um grupo até que todos os acessos à memória tenham sido concluídos.
ms.assetid: 63593de6-7b92-4f29-bcd9-21c69b9defcb
keywords:
- HLSL da função AllMemoryBarrier
topic_type:
- apiref
api_name:
- AllMemoryBarrier
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 4fc5d22c36d67aa0e8df8352ba8fa6f2d579ddabd4825e6508499420a56bd0ac
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119626746"
---
# <a name="allmemorybarrier-function"></a>Função AllMemoryBarrier

Bloqueia a execução de todos os threads em um grupo até que todos os acessos à memória tenham sido concluídos.

## <a name="syntax"></a>Sintaxe

``` syntax
void AllMemoryBarrier(void);
```

## <a name="parameters"></a>Parâmetros

Essa função não tem parâmetros.

## <a name="return-value"></a>Valor retornado

Essa função não retorna um valor.

## <a name="remarks"></a>Comentários

Uma barreira de memória garante que as operações de memória pendentes tenham sido concluídas. Os threads são sincronizados em barreiras de GroupSync. Isso pode paralisar um thread ou threads se as operações de memória estiverem em andamento.

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

 

 




