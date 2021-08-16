---
title: Função Texture2DMSArray::GetSamplePosition
description: Obtém a posição do exemplo especificado. | Função Texture2DMSArray::GetSamplePosition
ms.assetid: e04717be-58b0-4242-87dd-d769834ae1c2
keywords:
- Função GetSamplePosition HLSL
topic_type:
- apiref
api_name:
- GetSamplePosition
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 9da6727120dcb19d9dd51c83d62f85d842036edb2197d33e298259480b248642
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118508412"
---
# <a name="texture2dmsarraygetsampleposition-function"></a>Função Texture2DMSArray::GetSamplePosition

Obtém a posição do exemplo especificado.

## <a name="syntax"></a>Sintaxe

``` syntax
float2 GetSamplePosition(
  in int sampleindex
);
```

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*sampleindex* \[ Em\]
</dt> <dd>

Tipo: **[ **int**](/windows/desktop/WinProg/windows-data-types)**

O índice baseado em zero de um local de exemplo.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Tipo: **float2**

Um local de exemplo.

## <a name="remarks"></a>Comentários

Essa função tem suporte para os seguintes tipos de sombreadores:



| Vértice | Casco | Domínio | Geometry | Pixel | Computação |
|--------|------|--------|----------|-------|---------|
| x      | x    | x      | x        | x     | x       |



 

## <a name="see-also"></a>Confira também

<dl> <dt>

[Texture2DMSArray](sm5-object-texture2dmsarray.md)
</dt> <dt>

[Modelo de sombreador 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 
