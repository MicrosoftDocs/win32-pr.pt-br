---
title: 'Função Texture2DMS:: Load (int, int)'
description: 'Obtém um valor. | Função Texture2DMS:: Load (int, int)'
ms.assetid: b49b94e0-5c49-4901-b49d-3e652d4fd2d1
keywords:
- Carregar função DXGI
topic_type:
- apiref
api_name:
- Load
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 7d9c86bea7d914dd5975105a00a64789864a1fbd
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104968410"
---
# <a name="texture2dmsloadintint-function"></a>Função Texture2DMS:: Load (int, int)

Obtém um valor.

## <a name="syntax"></a>Sintaxe

``` syntax
T Load(
  in int2 coord,
  in int sampleindex
);
```

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*coord* \[ no\]
</dt> <dd>

Tipo: **Int2**

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
void Load(in int2 coord,
  in int sampleindex,
  in int2 offset);
```



Essa função tem suporte para os seguintes tipos de sombreadores:



| Vértice | Envoltória | Domínio | Geometria | 16x16 | Computação |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | x     | x       |



 

## <a name="see-also"></a>Confira também

<dl> <dt>

[Métodos de carregamento](texture2dms-load.md)
</dt> <dt>

[Modelo de sombreador 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 
