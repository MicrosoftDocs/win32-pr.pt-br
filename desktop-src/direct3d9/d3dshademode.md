---
description: Define constantes que descrevem os modos de sombreamento com suporte.
ms.assetid: ba4e0c62-b496-427b-a324-2fb560d153ba
title: Enumeração D3DSHADEMODE (D3d9types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DSHADEMODE
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: 9950e0074bef7a7b0c211177b3902cd69e2e112c
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104298557"
---
# <a name="d3dshademode-enumeration"></a>Enumeração D3DSHADEMODE

Define constantes que descrevem os modos de sombreamento com suporte.

## <a name="syntax"></a>Syntax


```C++
typedef enum D3DSHADEMODE { 
  D3DSHADE_FLAT         = 1,
  D3DSHADE_GOURAUD      = 2,
  D3DSHADE_PHONG        = 3,
  D3DSHADE_FORCE_DWORD  = 0x7fffffff
} D3DSHADEMODE, *LPD3DSHADEMODE;
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="D3DSHADE_FLAT"></span><span id="d3dshade_flat"></span>**D3DSHADE \_ simples**
</dt> <dd>

Modo de sombreamento simples. A cor e o componente especular do primeiro vértice no triângulo são usados para determinar a cor e o componente especular da face. Essas cores permanecem constantes em todo o triângulo; ou seja, eles não são interpolados. O alfa especular é interpolado. Consulte Observações.

</dd> <dt>

<span id="D3DSHADE_GOURAUD"></span><span id="d3dshade_gouraud"></span>**D3DSHADE \_ GOURAUD**
</dt> <dd>

Modo de sombreamento Gouraud. Os componentes de cor e especulação da face são determinados por uma interpolação linear entre os três vértices do triângulo.

</dd> <dt>

<span id="D3DSHADE_PHONG"></span><span id="d3dshade_phong"></span>**D3DSHADE \_ PHONG**
</dt> <dd>

Não há suporte.

</dd> <dt>

<span id="D3DSHADE_FORCE_DWORD"></span><span id="d3dshade_force_dword"></span>**D3DSHADE \_ forçar \_ DWORD**
</dt> <dd>

Força essa enumeração a compilar a 32 bits de tamanho. Sem esse valor, alguns compiladores permitiriam que essa enumeração fosse compilada em um tamanho diferente de 32 bits. Este valor não é usado.

</dd> </dl>

## <a name="remarks"></a>Comentários

O primeiro vértice de um triângulo para o modo de sombreamento simples é definido da maneira a seguir.

-   Para uma lista de triângulos, o primeiro vértice do triângulo i é \* 3.
-   Para uma faixa de triângulo, o primeiro vértice do triângulo i é o vértice i.
-   Para um ventilador de triângulo, o primeiro vértice do triângulo i é o vértice i + 1.

Os membros desse tipo enumerado definem o valores para o \_ estado de RENDERIZAÇÃO D3DRS shadmode.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|----------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>D3d9types. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Enumerações do Direct3D](dx9-graphics-reference-d3d-enums.md)
</dt> <dt>

[**D3DRENDERSTATETYPE**](./d3drenderstatetype.md)
</dt> </dl>

 

 
