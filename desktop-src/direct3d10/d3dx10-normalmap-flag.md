---
description: Esses sinalizadores são usados para controlar como o D3DX10ComputeNormalMap gera mapas normais. Qualquer número desses sinalizadores pode estar ou juntos em qualquer combinação.
ms.assetid: 307936c1-3137-41fe-8bea-7a82e6db0867
title: Enumeração de D3DX10_NORMALMAP_FLAG (D3DX10Tex. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10_NORMALMAP_FLAG
api_type:
- HeaderDef
api_location:
- D3DX10Tex.h
ms.openlocfilehash: c4b6962561007fbc3e64b471c045e98b2f8328b4
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105812130"
---
# <a name="d3dx10_normalmap_flag-enumeration"></a>\_Enumeração de \_ sinalizador D3DX10 NormalMap

Esses sinalizadores são usados para controlar como o [**D3DX10ComputeNormalMap**](d3dx10computenormalmap.md) gera mapas normais. Qualquer número desses sinalizadores pode estar ou juntos em qualquer combinação.

## <a name="syntax"></a>Syntax


```C++
typedef enum D3DX10_NORMALMAP_FLAG { 
  D3DX10_NORMALMAP_MIRROR_U           = (1 << 16),
  D3DX10_NORMALMAP_MIRROR_V           = (2 << 16),
  D3DX10_NORMALMAP_MIRROR             = (3 << 16),
  D3DX10_NORMALMAP_INVERTSIGN         = (8 << 16),
  D3DX10_NORMALMAP_COMPUTE_OCCLUSION  = (16 << 16)
} D3DX10_NORMALMAP_FLAG, *LPD3DX10_NORMALMAP_FLAG;
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="D3DX10_NORMALMAP_MIRROR_U"></span><span id="d3dx10_normalmap_mirror_u"></span>**D3DX10 \_ NormalMap \_ Mirror \_ U**
</dt> <dd>

Indica que os pixels da borda da textura no eixo U devem ser espelhados, não encapsulados.

</dd> <dt>

<span id="D3DX10_NORMALMAP_MIRROR_V"></span><span id="d3dx10_normalmap_mirror_v"></span>**D3DX10 \_ NormalMap \_ Mirror \_ V**
</dt> <dd>

Indica que os pixels da borda da textura no eixo V devem ser espelhados, não encapsulados.

</dd> <dt>

<span id="D3DX10_NORMALMAP_MIRROR"></span><span id="d3dx10_normalmap_mirror"></span>**D3DX10 \_ NormalMap \_ Mirror**
</dt> <dd>

O mesmo que D3DX10 \_ NormalMap \_ espelho \_ U \| D3DX10 \_ NormalMap \_ Mirror \_ V.

</dd> <dt>

<span id="D3DX10_NORMALMAP_INVERTSIGN"></span><span id="d3dx10_normalmap_invertsign"></span>**D3DX10 \_ NormalMap \_ INVERTSIGN**
</dt> <dd>

Inverte a direção de cada normal.

</dd> <dt>

<span id="D3DX10_NORMALMAP_COMPUTE_OCCLUSION"></span><span id="d3dx10_normalmap_compute_occlusion"></span>**D3DX10 \_ NormalMap \_ \_ oclusão Compute**
</dt> <dd>

Computa o termo por pixel oclusão e o codifica no Alpha. Um alfa de 1 significa que o pixel não é obscurecido de nenhuma forma e um alfa de 0 significaria que o pixel fosse completamente obscurecido.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|----------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>D3DX10Tex. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Enumerações D3DX](d3d10-graphics-reference-d3dx10-enums.md)
</dt> </dl>

 

 




