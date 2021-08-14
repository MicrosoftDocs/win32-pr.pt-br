---
description: Token de versão que cria um preenchimento de textura de procedimento em efeitos. Essa macro é usada pelas funções D3DXFillxxxTX.
ms.assetid: b11b6229-27a3-4813-9642-9e33bcd0da7a
title: D3DXTX_VERSION (D3DX9Shader. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXTX_VERSION
api_type:
- HeaderDef
api_location:
- D3DX9Shader.h
ms.openlocfilehash: 1a343930f55323016895007f858a7fe188418eeab24b16859c2d773e39c9e73b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118524097"
---
# <a name="d3dxtx_version"></a>Versão do D3DXTX \_

Token de versão que cria um preenchimento de textura de procedimento em efeitos. Essa macro é usada pelas funções D3DXFillxxxTX.

``` syntax
#define D3DXTX_VERSION (_Major, _Minor) (('T' << 24) | ('X' << 16) | ((_Major) << 8) | (_Minor))
```

## <a name="return-value"></a>Valor Retornado

A macro retorna o token de versão de textura de procedimento.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|------------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>D3DX9Shader. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Macros](dx9-graphics-reference-d3dx-macros.md)
</dt> <dt>

[**D3DXFillTextureTX**](d3dxfilltexturetx.md)
</dt> <dt>

[**D3DXFillCubeTextureTX**](d3dxfillcubetexturetx.md)
</dt> <dt>

[**D3DXFillVolumeTextureTX**](d3dxfillvolumetexturetx.md)
</dt> </dl>

 

 




