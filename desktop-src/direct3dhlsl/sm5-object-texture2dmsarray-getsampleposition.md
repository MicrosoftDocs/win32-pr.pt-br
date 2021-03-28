---
title: 'Função Texture2DMSArray:: GetSamplePosition'
description: 'Obtém a posição do exemplo especificado. | Função Texture2DMSArray:: GetSamplePosition'
ms.assetid: e04717be-58b0-4242-87dd-d769834ae1c2
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
ms.openlocfilehash: ea4d45ef5523c5fa4c9ef080bba6286a050aa12c
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104172868"
---
# <a name="texture2dmsarraygetsampleposition-function"></a>Função Texture2DMSArray:: GetSamplePosition

Obtém a posição do exemplo especificado.

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

[Texture2DMSArray](sm5-object-texture2dmsarray.md)
</dt> <dt>

[Modelo de sombreador 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 
