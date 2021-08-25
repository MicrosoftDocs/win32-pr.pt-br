---
title: Função GroupMemoryBaory
description: Bloqueia a execução de todos os threads em um grupo até que todos os acessos compartilhados de grupo tenham sido concluídos.
ms.assetid: cebd4277-47a0-401a-bfbe-8d956412f254
keywords:
- Função GroupMemoryBaory HLSL
topic_type:
- apiref
api_name:
- GroupMemoryBarrier
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: e9889be841df54f6ae18b7ac52d7117f780af37662c5a1d4f6c29af858350345
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119743856"
---
# <a name="groupmemorybarrier-function"></a>Função GroupMemoryBaory

Bloqueia a execução de todos os threads em um grupo até que todos os acessos compartilhados de grupo tenham sido concluídos.

## <a name="syntax"></a>Sintaxe

``` syntax
void GroupMemoryBarrier(void);
```

## <a name="parameters"></a>Parâmetros

Essa função não tem parâmetros.

## <a name="return-value"></a>Valor retornado

Essa função não retorna um valor.

## <a name="remarks"></a>Comentários

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

 

 




