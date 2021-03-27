---
title: 'Função Texture2DMS:: GetSamplePosition'
description: Retorna a posição de exemplo do índice de exemplo fornecido.
ms.assetid: b7821112-9b40-4302-b5c1-03bab531a0ab
keywords:
- HLSL da função GetSamplePosition
topic_type:
- apiref
api_name:
- GetSamplePosition
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 532411e333023ff61df0b7f9fbf0336dc11d1586
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/10/2020
ms.locfileid: "104499223"
---
# <a name="texture2dmsgetsampleposition-function"></a>Função Texture2DMS:: GetSamplePosition

Retorna a posição de exemplo do índice de exemplo fornecido.

## <a name="syntax"></a>Sintaxe

``` syntax
float2 GetSamplePosition(
  in int sampleindex
);
```

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*sampleindex* \[ no\]
</dt> <dd>

Tipo: **[ **int**](/windows/desktop/WinProg/windows-data-types)**

O índice de base zero de um local de exemplo.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Tipo: **float2**

Um local de exemplo.

## <a name="remarks"></a>Comentários

Essa função tem suporte para os seguintes tipos de sombreadores:



| Vértice | Envoltória | Domínio | Geometria | 16x16 | Computação |
|--------|------|--------|----------|-------|---------|
| x      | x    | x      | x        | x     | x       |



 

## <a name="see-also"></a>Confira também

<dl> <dt>

[Texture2DMS](sm5-object-texture2dms.md)
</dt> <dt>

[Modelo de sombreador 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 
