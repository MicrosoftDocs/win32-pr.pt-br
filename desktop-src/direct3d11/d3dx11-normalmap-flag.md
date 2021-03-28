---
title: Enumeração de D3DX11_NORMALMAP_FLAG (D3DX11tex. h)
description: Observe que a biblioteca de utilitários D3DX (D3DX 9, D3DX 10 e D3DX 11) foi preterida para o Windows 8 e não tem suporte para aplicativos da Windows Store. Opções de mapa normais. Você pode combinar qualquer número desses sinalizadores usando uma operação OR bit a bit.
ms.assetid: cc9c8a54-be1e-4594-8274-9955562a6fa8
keywords:
- Enumeração D3DX11_NORMALMAP_FLAG Direct3D 11
- Ponteiro de enumeração LPD3DX11_NORMALMAP_FLAG Direct3D 11
topic_type:
- apiref
api_name:
- D3DX11_NORMALMAP_FLAG
api_location:
- D3DX11tex.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 37f5d9669370e6df03d783ae1cb82a5eeb5a9142
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104173188"
---
# <a name="d3dx11_normalmap_flag-enumeration"></a>\_Enumeração de \_ sinalizador D3DX11 NormalMap

> [!Note]  
> A biblioteca de utilitários D3DX (D3DX 9, D3DX 10 e D3DX 11) foi preterida para o Windows 8 e não tem suporte para aplicativos da Windows Store.

 

Opções de mapa normais. Você pode combinar qualquer número desses sinalizadores usando uma operação OR bit a bit.

## <a name="syntax"></a>Syntax


```C++
typedef enum D3DX11_NORMALMAP_FLAG { 
  D3DX11_NORMALMAP_MIRROR_U           = (1 << 16),
  D3DX11_NORMALMAP_MIRROR_V           = (2 << 16),
  D3DX11_NORMALMAP_MIRROR             = (3 << 16),
  D3DX11_NORMALMAP_INVERTSIGN         = (8 << 16),
  D3DX11_NORMALMAP_COMPUTE_OCCLUSION  = (16 << 16)
} D3DX11_NORMALMAP_FLAG, *LPD3DX11_NORMALMAP_FLAG;
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="D3DX11_NORMALMAP_MIRROR_U"></span><span id="d3dx11_normalmap_mirror_u"></span>**D3DX11 \_ NormalMap \_ Mirror \_ U**
</dt> <dd>

Indica que os pixels da borda da textura no eixo U devem ser espelhados, não encapsulados.

</dd> <dt>

<span id="D3DX11_NORMALMAP_MIRROR_V"></span><span id="d3dx11_normalmap_mirror_v"></span>**D3DX11 \_ NormalMap \_ Mirror \_ V**
</dt> <dd>

Indica que os pixels da borda da textura no eixo V devem ser espelhados, não encapsulados.

</dd> <dt>

<span id="D3DX11_NORMALMAP_MIRROR"></span><span id="d3dx11_normalmap_mirror"></span>**D3DX11 \_ NormalMap \_ Mirror**
</dt> <dd>

O mesmo que D3DX11 \_ NormalMap \_ espelho \_ U \| D3DX11 \_ NormalMap \_ Mirror \_ V.

</dd> <dt>

<span id="D3DX11_NORMALMAP_INVERTSIGN"></span><span id="d3dx11_normalmap_invertsign"></span>**D3DX11 \_ NormalMap \_ INVERTSIGN**
</dt> <dd>

Inverte a direção de cada normal.

</dd> <dt>

<span id="D3DX11_NORMALMAP_COMPUTE_OCCLUSION"></span><span id="d3dx11_normalmap_compute_occlusion"></span>**D3DX11 \_ NormalMap \_ \_ oclusão Compute**
</dt> <dd>

Computa o termo por pixel oclusão e o codifica no Alpha. Um alfa de 1 significa que o pixel não é obscurecido de nenhuma forma e um alfa de 0 significaria que o pixel fosse completamente obscurecido.

</dd> </dl>

## <a name="remarks"></a>Comentários

Esses sinalizadores são usados pelo [**D3DX11ComputeNormalMap**](d3dx11computenormalmap.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|----------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>D3DX11tex. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Enumerações D3DX](d3d11-graphics-reference-d3dx11-enums.md)
</dt> </dl>

 

 





