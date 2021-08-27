---
description: Estrutura D3DXVECTOR3 (D3DX10Math.h) – descreve um vetor de três componentes, incluindo sobrecargas de operador e casts de tipo.
ms.assetid: d170cd26-d705-4a31-82b3-f9ea070b6ca4
title: Estrutura D3DXVECTOR3 (D3DX10Math.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVECTOR3
api_type:
- HeaderDef
api_location:
- D3DX10Math.h
ms.openlocfilehash: 61c9791f4e97fbde77f3b42154b2855f2fc31694efd19087dd78fdced9908e56
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120120216"
---
# <a name="d3dxvector3-structure-d3dx10mathh"></a>Estrutura D3DXVECTOR3 (D3DX10Math.h)

Descreve um vetor de três componentes, incluindo sobrecargas de operador e casts de tipo.

## <a name="syntax"></a>Sintaxe


```C++
typedef struct D3DXVECTOR3 {
  FLOAT x;
  FLOAT y;
  FLOAT z;
} D3DXVECTOR3, *LPD3DXVECTOR3;
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

**D3DXVECTOR3** tem as seguintes extensões C++.

### <a name="d3dxvector3-extensions"></a>Extensões D3DXVECTOR3


```
#ifdef __cplusplus
typedef struct D3DXVECTOR3 : public D3DVECTOR
{
public:
    D3DXVECTOR3() {};
    D3DXVECTOR3( CONST FLOAT * );
    D3DXVECTOR3( CONST D3DVECTOR& );
    D3DXVECTOR3( CONST D3DXFLOAT16 * );
    D3DXVECTOR3( FLOAT x, FLOAT y, FLOAT z );

    // casting
    operator FLOAT* ();
    operator CONST FLOAT* () const;

    // assignment operators
    D3DXVECTOR3& operator += ( CONST D3DXVECTOR3& );
    D3DXVECTOR3& operator -= ( CONST D3DXVECTOR3& );
    D3DXVECTOR3& operator *= ( FLOAT );
    D3DXVECTOR3& operator /= ( FLOAT );

    // unary operators
    D3DXVECTOR3 operator + () const;
    D3DXVECTOR3 operator - () const;

    // binary operators
    D3DXVECTOR3 operator + ( CONST D3DXVECTOR3& ) const;
    D3DXVECTOR3 operator - ( CONST D3DXVECTOR3& ) const;
    D3DXVECTOR3 operator * ( FLOAT ) const;
    D3DXVECTOR3 operator / ( FLOAT ) const;

    friend D3DXVECTOR3 operator * ( FLOAT, CONST struct D3DXVECTOR3& );

    BOOL operator == ( CONST D3DXVECTOR3& ) const;
    BOOL operator != ( CONST D3DXVECTOR3& ) const;

} D3DXVECTOR3, *LPD3DXVECTOR3;

#else //!__cplusplus
typedef struct _D3DVECTOR D3DXVECTOR3, *LPD3DXVECTOR3;
#endif //!__cplusplus
        
```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|-----------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>D3DX10Math.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Estruturas D3DX](d3d10-graphics-reference-d3dx10-structures.md)
</dt> </dl>

 

 
