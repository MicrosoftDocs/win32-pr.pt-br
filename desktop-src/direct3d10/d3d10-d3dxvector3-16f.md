---
description: O mesmo que um D3DXVECTOR3, mas usa valores de ponto flutuante de 16 bits para x, y e z.
ms.assetid: b21676f1-5cff-4eef-bd60-5c09882283dc
title: D3DXVECTOR3_16F (D3DX10Math.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVECTOR3_16F
api_type:
- HeaderDef
api_location:
- D3DX10Math.h
ms.openlocfilehash: afb5e12d19655ddf6f2d31d23a21cbac2347ba05a9d7900c1bc2a90977a9fd88
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119729856"
---
# <a name="d3dxvector3_16f-structure"></a>Estrutura D3DXVECTOR3 \_ 16F

O mesmo que [**um D3DXVECTOR3**](d3d10-d3dxvector3.md), mas usa valores de ponto flutuante de 16 bits para x, y e z.

## <a name="syntax"></a>Sintaxe


```C++
typedef struct D3DXVECTOR3_16F {
  FLOAT x;
  FLOAT y;
  FLOAT z;
} D3DXVECTOR3_16F, *LPD3DXVECTOR3_16F;
```



## <a name="members"></a>Membros

<dl> <dt>

**x**
</dt> <dd>

Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**

</dd> <dd>

O componente x.

</dd> <dt>

**y**
</dt> <dd>

Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**

</dd> <dd>

O componente y.

</dd> <dt>

**Z**
</dt> <dd>

Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**

</dd> <dd>

O componente z.

</dd> </dl>

## <a name="remarks"></a>Comentários

**D3DXVECTOR3 \_ 16F** tem as seguintes extensões C++.

### <a name="d3dxvector3_16f-extensions"></a>Extensões D3DXVECTOR3 \_ 16F


```

typedef struct D3DXVECTOR3_16F
{
#ifdef __cplusplus
public:
    D3DXVECTOR3_16F() {};
    D3DXVECTOR3_16F( CONST FLOAT * );
    D3DXVECTOR3_16F( CONST D3DVECTOR& );
    D3DXVECTOR3_16F( CONST D3DXFLOAT16 * );
    D3DXVECTOR3_16F( CONST D3DXFLOAT16 &x, CONST D3DXFLOAT16 &y, CONST D3DXFLOAT16 &z );

    // casting
    operator D3DXFLOAT16* ();
    operator CONST D3DXFLOAT16* () const;

    // binary operators
    BOOL operator == ( CONST D3DXVECTOR3_16F& ) const;
    BOOL operator != ( CONST D3DXVECTOR3_16F& ) const;

public:
#endif //__cplusplus
    D3DXFLOAT16 x, y, z;

} D3DXVECTOR3_16F, *LPD3DXVECTOR3_16F;
```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|-----------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>D3DX10Math.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Estruturas D3DX](d3d10-graphics-reference-d3dx10-structures.md)
</dt> </dl>

 

 
