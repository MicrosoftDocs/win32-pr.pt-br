---
title: 'Função Texture2DMSArray:: Load (int, int)'
description: 'Obtém um valor. | Função Texture2DMSArray:: Load (int, int)'
ms.assetid: 955135cf-1bac-4d0c-9870-2b6d59d9dd88
keywords:
- Carregar função HLSL
topic_type:
- apiref
api_name:
- Load
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 83da1a2af6ffc7e990ba1fd4c7f220387304c770
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "103930489"
---
# <a name="texture2dmsarrayloadintint-function"></a>Função Texture2DMSArray:: Load (int, int)

Obtém um valor.

## <a name="syntax"></a>Sintaxe

``` syntax
T Load(
  in int3 coord,
  in int sampleindex
);
```

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*coord* \[ no\]
</dt> <dd>

Tipo: **Int3**

O local de entrada.

</dd> <dt>

*sampleindex* \[ no\]
</dt> <dd>

Tipo: **[ **int**](/windows/desktop/WinProg/windows-data-types)**

O índice de exemplo.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Tipo: **T**

Um valor, cujo tipo corresponde ao tipo de modelo de textura.

## <a name="remarks"></a>Comentários

Esta é uma lista das versões sobrecarregadas desse método.


```
void Load(in int3 coord,
  in int sampleindex,
  in int2 offset);
```



Essa função tem suporte para os seguintes tipos de sombreadores:



| Vértice | Envoltória | Domínio | Geometria | 16x16 | Computação |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | x     | x       |



 

## <a name="see-also"></a>Confira também

<dl> <dt>

[Métodos de carregamento](texture2dmsarray-load.md)
</dt> <dt>

[Modelo de sombreador 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 
