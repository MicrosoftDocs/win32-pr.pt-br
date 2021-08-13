---
title: Função Texture2DMS::Load(int,int)
description: Obtém um valor. | Função Texture2DMS::Load(int,int)
ms.assetid: b49b94e0-5c49-4901-b49d-3e652d4fd2d1
keywords:
- Função de carregamento DXGI
topic_type:
- apiref
api_name:
- Load
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 0997a1bd30b4912864674015057fcafec227d90ad05b16b88fd3f05b671f155c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118285724"
---
# <a name="texture2dmsloadintint-function"></a>Função Texture2DMS::Load(int,int)

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

*coord* \[ Em\]
</dt> <dd>

Tipo: **int2**

O local de entrada.

</dd> <dt>

*sampleindex* \[ Em\]
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



| Vértice | Casco | Domínio | Geometry | Pixel | Computação |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | x     | x       |



 

## <a name="see-also"></a>Confira também

<dl> <dt>

[Métodos de carregamento](texture2dms-load.md)
</dt> <dt>

[Modelo de sombreador 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 
