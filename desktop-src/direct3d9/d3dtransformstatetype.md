---
description: Define constantes que descrevem valores de estado de transformação.
ms.assetid: 53535d9f-246a-42cf-82a2-fb3cf6d4ebac
title: Enumeração D3DTRANSFORMSTATETYPE (D3D9Types.h)
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
ms.openlocfilehash: 299246ef890015a6d7de465ecc7c00251a52432d276a87f3d5f336b63d563737
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119986986"
---
# <a name="d3dtransformstatetype-enumeration"></a>Enumeração D3DTRANSFORMSTATETYPE

Define constantes que descrevem valores de estado de transformação.

## <a name="syntax"></a>Syntax


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

<span id="D3DTS_VIEW"></span><span id="d3dts_view"></span>**EXIBIÇÃO D3DTS \_**
</dt> <dd>

Identifica a matriz de transformação que está sendo definida como a matriz de transformação de exibição. O valor padrão é **NULL** (a matriz de identidade).

</dd> <dt>

<span id="D3DTS_PROJECTION"></span><span id="d3dts_projection"></span>**PROJEÇÃO DE D3DTS \_**
</dt> <dd>

Identifica a matriz de transformação que está sendo definida como a matriz de transformação de projeção. O valor padrão é **NULL** (a matriz de identidade).

</dd> <dt>

<span id="D3DTS_TEXTURE0"></span><span id="d3dts_texture0"></span>**TEXTURA DE \_ D3DTS0**
</dt> <dd>

Identifica a matriz de transformação que está sendo definida para o estágio de textura especificado.

</dd> <dt>

<span id="D3DTS_TEXTURE1"></span><span id="d3dts_texture1"></span>**TEXTURA DE \_ D3DTS1**
</dt> <dd>

Identifica a matriz de transformação que está sendo definida para o estágio de textura especificado.

</dd> <dt>

<span id="D3DTS_TEXTURE2"></span><span id="d3dts_texture2"></span>**TEXTURA DE \_ D3DTS2**
</dt> <dd>

Identifica a matriz de transformação que está sendo definida para o estágio de textura especificado.

</dd> <dt>

<span id="D3DTS_TEXTURE3"></span><span id="d3dts_texture3"></span>**TEXTURA DE \_ D3DTS3**
</dt> <dd>

Identifica a matriz de transformação que está sendo definida para o estágio de textura especificado.

</dd> <dt>

<span id="D3DTS_TEXTURE4"></span><span id="d3dts_texture4"></span>**TEXTURA DE \_ D3DTS4**
</dt> <dd>

Identifica a matriz de transformação que está sendo definida para o estágio de textura especificado.

</dd> <dt>

<span id="D3DTS_TEXTURE5"></span><span id="d3dts_texture5"></span>**TEXTURA D3DTS5 \_**
</dt> <dd>

Identifica a matriz de transformação que está sendo definida para o estágio de textura especificado.

</dd> <dt>

<span id="D3DTS_TEXTURE6"></span><span id="d3dts_texture6"></span>**TEXTURA DE \_ D3DTS6**
</dt> <dd>

Identifica a matriz de transformação que está sendo definida para o estágio de textura especificado.

</dd> <dt>

<span id="D3DTS_TEXTURE7"></span><span id="d3dts_texture7"></span>**TEXTURA D3DTS7 \_**
</dt> <dd>

Identifica a matriz de transformação que está sendo definida para o estágio de textura especificado.

</dd> <dt>

<span id="D3DTS_FORCE_DWORD"></span><span id="d3dts_force_dword"></span>**D3DTS \_ FORCE \_ DWORD**
</dt> <dd>

Força essa enumeração a compilar para 32 bits de tamanho. Sem esse valor, alguns compiladores permitiriam que essa enumeração fosse compilada para um tamanho diferente de 32 bits. Este valor não é usado.

</dd> </dl>

## <a name="remarks"></a>Comentários

Os estados de transformação no intervalo de 256 a 511 são reservados para armazenar até 256 matrizes do mundo que podem ser indexadas usando as macros D3DTS \_ WORLDMATRIX e D3DTS \_ WORLD.



| Macros                                                  | Descrição                                                                                                                                                                      |
|---------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**D3DTS \_ WORLD**](d3dts-world.md)                     | Equivalente a D3DTS \_ WORLDMATRIX(0).                                                                                                                                  |
| [**D3DTS \_ WORLDMATRIX**](d3dts-worldmatrix.md) (índice) | Identifica a matriz de transformação a ser definida para a matriz mundial no índice. Várias matrizes de mundo são usadas somente para mesclagem de vértices. Caso contrário, somente D3DTS \_ WORLD será usado. |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|----------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>D3D9Types.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Enumerações direct3D](dx9-graphics-reference-d3d-enums.md)
</dt> <dt>

[**IDirect3DDevice9::GetTransform**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-gettransform)
</dt> <dt>

[**IDirect3DDevice9::MultiplyTransform**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-multiplytransform)
</dt> <dt>

[**IDirect3DDevice9::SetTransform**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settransform)
</dt> <dt>

[**D3DTS \_ WORLD**](d3dts-world.md)
</dt> <dt>

[**D3DTS \_ WORLDn**](d3dts-worldn.md)
</dt> <dt>

[**D3DTS \_ WORLDMATRIX**](d3dts-worldmatrix.md)
</dt> </dl>

 

 
