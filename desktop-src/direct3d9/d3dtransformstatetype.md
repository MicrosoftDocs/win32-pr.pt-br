---
description: Define constantes que descrevem valores de estado de transformação.
ms.assetid: 53535d9f-246a-42cf-82a2-fb3cf6d4ebac
title: Enumeração D3DTRANSFORMSTATETYPE (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DTRANSFORMSTATETYPE
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: c618e0e19bf7dd01dec73d35436f23189f9e78a6
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105789406"
---
# <a name="d3dtransformstatetype-enumeration"></a>Enumeração D3DTRANSFORMSTATETYPE

Define constantes que descrevem valores de estado de transformação.

## <a name="syntax"></a>Sintaxe


```C++
typedef enum D3DTRANSFORMSTATETYPE { 
  D3DTS_VIEW         = 2,
  D3DTS_PROJECTION   = 3,
  D3DTS_TEXTURE0     = 16,
  D3DTS_TEXTURE1     = 17,
  D3DTS_TEXTURE2     = 18,
  D3DTS_TEXTURE3     = 19,
  D3DTS_TEXTURE4     = 20,
  D3DTS_TEXTURE5     = 21,
  D3DTS_TEXTURE6     = 22,
  D3DTS_TEXTURE7     = 23,
  D3DTS_FORCE_DWORD  = 0x7fffffff
} D3DTRANSFORMSTATETYPE, *LPD3DTRANSFORMSTATETYPE;
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="D3DTS_VIEW"></span><span id="d3dts_view"></span>**Exibição de D3DTS \_**
</dt> <dd>

Identifica a matriz de transformação que está sendo definida como a matriz de transformação View. O valor padrão é **NULL** (a matriz de identidade).

</dd> <dt>

<span id="D3DTS_PROJECTION"></span><span id="d3dts_projection"></span>**\_Projeção D3DTS**
</dt> <dd>

Identifica a matriz de transformação que está sendo definida como a matriz de transformação projeção. O valor padrão é **NULL** (a matriz de identidade).

</dd> <dt>

<span id="D3DTS_TEXTURE0"></span><span id="d3dts_texture0"></span>**D3DTS \_ TEXTURE0**
</dt> <dd>

Identifica a matriz de transformação que está sendo definida para o estágio de textura especificado.

</dd> <dt>

<span id="D3DTS_TEXTURE1"></span><span id="d3dts_texture1"></span>**D3DTS \_ TEXTURE1**
</dt> <dd>

Identifica a matriz de transformação que está sendo definida para o estágio de textura especificado.

</dd> <dt>

<span id="D3DTS_TEXTURE2"></span><span id="d3dts_texture2"></span>**D3DTS \_ TEXTURE2**
</dt> <dd>

Identifica a matriz de transformação que está sendo definida para o estágio de textura especificado.

</dd> <dt>

<span id="D3DTS_TEXTURE3"></span><span id="d3dts_texture3"></span>**D3DTS \_ TEXTURE3**
</dt> <dd>

Identifica a matriz de transformação que está sendo definida para o estágio de textura especificado.

</dd> <dt>

<span id="D3DTS_TEXTURE4"></span><span id="d3dts_texture4"></span>**D3DTS \_ TEXTURE4**
</dt> <dd>

Identifica a matriz de transformação que está sendo definida para o estágio de textura especificado.

</dd> <dt>

<span id="D3DTS_TEXTURE5"></span><span id="d3dts_texture5"></span>**D3DTS \_ TEXTURE5**
</dt> <dd>

Identifica a matriz de transformação que está sendo definida para o estágio de textura especificado.

</dd> <dt>

<span id="D3DTS_TEXTURE6"></span><span id="d3dts_texture6"></span>**D3DTS \_ TEXTURE6**
</dt> <dd>

Identifica a matriz de transformação que está sendo definida para o estágio de textura especificado.

</dd> <dt>

<span id="D3DTS_TEXTURE7"></span><span id="d3dts_texture7"></span>**D3DTS \_ TEXTURE7**
</dt> <dd>

Identifica a matriz de transformação que está sendo definida para o estágio de textura especificado.

</dd> <dt>

<span id="D3DTS_FORCE_DWORD"></span><span id="d3dts_force_dword"></span>**D3DTS \_ forçar \_ DWORD**
</dt> <dd>

Força essa enumeração a compilar a 32 bits de tamanho. Sem esse valor, alguns compiladores permitiriam que essa enumeração fosse compilada em um tamanho diferente de 32 bits. Este valor não é usado.

</dd> </dl>

## <a name="remarks"></a>Comentários

Os Estados de transformação no intervalo de 256 a 511 são reservados para armazenar até 256 matrizes mundiais que podem ser indexadas usando as \_ macros D3DTS WORLDMATRIX e D3DTS \_ World.



| Macros                                                  |                                                                                                                                                                       |
|---------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**D3DTS \_ World**](d3dts-world.md)                     | Equivalente a D3DTS \_ WORLDMATRIX (0).                                                                                                                                  |
| [**D3DTS \_ WORLDMATRIX**](d3dts-worldmatrix.md) (índice) | Identifica a matriz de transformação a ser definida para a matriz mundial no índice. Várias matrizes mundiais são usadas apenas para mesclagem de vértice. Caso contrário, somente D3DTS \_ World será usado. |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|----------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>D3D9Types. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Enumerações do Direct3D](dx9-graphics-reference-d3d-enums.md)
</dt> <dt>

[**IDirect3DDevice9:: GetTransform**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-gettransform)
</dt> <dt>

[**IDirect3DDevice9::MultiplyTransform**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-multiplytransform)
</dt> <dt>

[**IDirect3DDevice9:: SetTransform**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settransform)
</dt> <dt>

[**D3DTS \_ World**](d3dts-world.md)
</dt> <dt>

[**D3DTS \_ worldn**](d3dts-worldn.md)
</dt> <dt>

[**D3DTS \_ WORLDMATRIX**](d3dts-worldmatrix.md)
</dt> </dl>

 

 
