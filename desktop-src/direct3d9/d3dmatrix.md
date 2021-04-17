---
description: Descreve uma matriz.
ms.assetid: d6b98a32-e745-4724-b8ce-a81a3f5416f3
title: D3DMATRIX (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DMATRIX
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: 6b4339d2e44e1add46103bae58ad3e02c8a6509b
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105812225"
---
# <a name="d3dmatrix"></a>D3DMATRIX

Descreve uma matriz.

``` syntax
typedef struct _D3DMATRIX {
    union {
        struct {
            float        _11, _12, _13, _14;
            float        _21, _22, _23, _24;
            float        _31, _32, _33, _34;
            float        _41, _42, _43, _44;

        };
        float m[4][4];
    };
} D3DMATRIX;
```

Tipos derivados: \* LPD3DMATRIX

## <a name="members"></a>Membros



| Item                                                        | Descrição                                                                                                                                                                                                     |
|-------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="_ij"></span><span id="_IJ"></span>\_Ligatura<br/> | Uma matriz de floats que representa uma matriz 4x4, onde é o número da linha e j é o número da coluna. Por exemplo, \_ 34 significa o mesmo que \[ um ₃ ₄ \] , o componente na terceira linha e a quarta coluna.<br/> |



 

## <a name="remarks"></a>Comentários

No Direct3D, o \_ elemento 34 de uma matriz de projeção não pode ser um número negativo. Se seu aplicativo precisar usar um valor negativo nesse local, ele deverá dimensionar toda a matriz de projeção em-1 em vez disso.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|----------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>D3D9Types. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Estruturas do Direct3D](dx9-graphics-reference-d3d-structures.md)
</dt> <dt>

[**GetTransform**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-gettransform)
</dt> <dt>

[**MultiplyTransform**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-multiplytransform)
</dt> <dt>

[**SetTransform**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settransform)
</dt> <dt>

**SetTransform**
</dt> <dt>

[**D3DXMATRIX**](d3dxmatrix.md)
</dt> <dt>

[Transformações (Direct3D 9)](transforms.md)
</dt> </dl>

 

 
