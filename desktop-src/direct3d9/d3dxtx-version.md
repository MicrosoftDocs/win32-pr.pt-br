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
ms.openlocfilehash: 05b034a48635e3a5a6d1a3dbdfbabd0fe2933b5c
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105807256"
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

 

 




