---
description: Esta constante é o número máximo de declaradores de vértice para uma malha.
ms.assetid: 234e99a2-1907-4065-b03b-fb9e8d6812ab
title: Enumeração de MAX_FVF_DECL_SIZE (D3dx9mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MAX_FVF_DECL_SIZE
api_type:
- HeaderDef
api_location:
- d3dx9mesh.h
ms.openlocfilehash: 7204308e6b9355b416218f31af301b5ea6d8fff5
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105761908"
---
# <a name="max_fvf_decl_size-enumeration"></a>Enumeração de tamanho máximo de \_ \_ DECL FVF \_

Esta constante é o número máximo de declaradores de vértice para uma malha.

## <a name="syntax"></a>Syntax


```C++
typedef enum  { 
  MAX_FVF_DECL_SIZE  = MAXD3DDECLLENGTH + 1
} MAX_FVF_DECL_SIZE;
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="MAX_FVF_DECL_SIZE"></span><span id="max_fvf_decl_size"></span>**tamanho máximo de \_ \_ DECL FVF \_**
</dt> <dd>

O número máximo de elementos na declaração de vértice. O adicional (+ 1) é para [**D3DDECL \_ end**](d3ddecl-end.md).

</dd> </dl>

## <a name="remarks"></a>Comentários

MAXD3DDECLLENGTH é definido como um máximo de 64 (consulte d3d9types. h). Isso não inclui o elemento vértice do marcador "End".

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|----------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>D3dx9mesh. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Enumerações D3DX](dx9-graphics-reference-d3dx-enums.md)
</dt> <dt>

[**ID3DXBaseMesh**](id3dxbasemesh.md)
</dt> <dt>

[**Getdeclaration**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dvertexdeclaration9-getdeclaration)
</dt> <dt>

[**D3DXDeclaratorFromFVF**](d3dxdeclaratorfromfvf.md)
</dt> <dt>

[**ID3DXSkinInfo**](id3dxskininfo.md)
</dt> </dl>

 

 
