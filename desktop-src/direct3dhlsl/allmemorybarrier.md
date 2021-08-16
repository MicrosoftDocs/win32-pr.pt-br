---
title: Função AllMemoryBaory
description: Bloqueia a execução de todos os threads em um grupo até que todos os acessos de memória tenham sido concluídos.
ms.assetid: 63593de6-7b92-4f29-bcd9-21c69b9defcb
keywords:
- Função AllMemoryBaory HLSL
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
# <a name="allmemorybarrier-function"></a>Função AllMemoryBaory

Bloqueia a execução de todos os threads em um grupo até que todos os acessos de memória tenham sido concluídos.

## <a name="syntax"></a>Sintaxe

``` syntax
void AllMemoryBarrier(void);
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

 

 




