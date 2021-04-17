---
description: Identifica a matriz de transformação que está sendo definida como a matriz de transformação mundial.
ms.assetid: 2bf7ac8a-43d8-460e-a400-3b33e96441db
title: Macro D3DTS_WORLD (D3d9types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DTS_WORLD
api_type:
- HeaderDef
api_location:
- D3d9types.h
ms.openlocfilehash: c3c8f0ac30230a747fba34d9962791b4b331d647
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105813272"
---
# <a name="d3dts_world-macro"></a>\_Macro do mundo D3DTS

Identifica a matriz de transformação que está sendo definida como a matriz de transformação mundial.

## <a name="syntax"></a>Sintaxe


```C++
D3DTRANSFORMSTATETYPE D3DTS_WORLD(void);
```



## <a name="parameters"></a>Parâmetros

Esta macro não tem parâmetros.

## <a name="return-value"></a>Retornar valor

Um [**D3DTRANSFORMSTATETYPE**](./d3dtransformstatetype.md) equivalente a [**D3DTS \_ WORLDMATRIX (0)**](./d3dts-worldmatrix.md).

## <a name="remarks"></a>Comentários

Essa macro é fornecida para facilitar a portabilidade de aplicativos existentes para o Direct3D 9.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|----------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>D3d9types. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Macros](dx9-graphics-reference-d3d-macros.md)
</dt> <dt>

[**SetTransform**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settransform)
</dt> <dt>

[**D3DTS \_ WORLDMATRIX**](d3dts-worldmatrix.md)
</dt> </dl>

 

 
