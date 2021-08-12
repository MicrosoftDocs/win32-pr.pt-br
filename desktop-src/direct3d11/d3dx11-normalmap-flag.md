---
title: D3DX11_NORMALMAP_FLAG enumeração (D3DX11tex.h)
description: Observação A biblioteca de utilitários D3DX (D3DX 9, D3DX 10 e D3DX 11) foi preterida para Windows 8 e não tem suporte para aplicativos da Windows Store. Opções normais de mapa. Você pode combinar qualquer número desses sinalizadores usando uma operação OR bit a bit.
ms.assetid: cc9c8a54-be1e-4594-8274-9955562a6fa8
keywords:
- D3DX11_NORMALMAP_FLAG enumeração Direct3D 11
- LPD3DX11_NORMALMAP_FLAG ponteiro de enumeração Direct3D 11
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
ms.openlocfilehash: dbea7c787ac2e2aa7d988e052e2ca548a49a338c9b9f981ce73d51c40e0b4edd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118300645"
---
# <a name="d3dx11_normalmap_flag-enumeration"></a>Enumeração DE SINALIZADOR D3DX11 \_ NORMALMAP \_

> [!Note]  
> A biblioteca de utilitários D3DX (D3DX 9, D3DX 10 e D3DX 11) foi preterida para Windows 8 e não tem suporte para aplicativos Windows Store.

 

Opções normais de mapa. Você pode combinar qualquer número desses sinalizadores usando uma operação OR bit a bit.

## <a name="syntax"></a>Sintaxe


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

<span id="D3DX11_NORMALMAP_MIRROR_U"></span><span id="d3dx11_normalmap_mirror_u"></span>**D3DX11 \_ NORMALMAP \_ MIRROR \_ U**
</dt> <dd>

Indica que os pixels fora da borda da textura no eixo U devem ser espelhados, não wraped.

</dd> <dt>

<span id="D3DX11_NORMALMAP_MIRROR_V"></span><span id="d3dx11_normalmap_mirror_v"></span>**D3DX11 \_ NORMALMAP \_ MIRROR \_ V**
</dt> <dd>

Indica que os pixels fora da borda da textura no eixo V devem ser espelhados, não wraped.

</dd> <dt>

<span id="D3DX11_NORMALMAP_MIRROR"></span><span id="d3dx11_normalmap_mirror"></span>**D3DX11 \_ NORMALMAP \_ MIRROR**
</dt> <dd>

O mesmo que D3DX11 \_ NORMALMAP \_ MIRROR U \_ \| D3DX11 \_ NORMALMAP MIRROR \_ \_ V.

</dd> <dt>

<span id="D3DX11_NORMALMAP_INVERTSIGN"></span><span id="d3dx11_normalmap_invertsign"></span>**D3DX11 \_ NORMALMAP \_ INVERTSIGN**
</dt> <dd>

Inverte a direção de cada normal.

</dd> <dt>

<span id="D3DX11_NORMALMAP_COMPUTE_OCCLUSION"></span><span id="d3dx11_normalmap_compute_occlusion"></span>**OCLUSÃO DE COMPUTAÇÃO DE D3DX11 \_ NORMALMAP \_ \_**
</dt> <dd>

Calcula o termo de oclusão por pixel e o codifica no alfa. Um Alfa de 1 significa que o pixel não é obscurecido de nenhuma maneira, e um alfa de 0 significa que o pixel está completamente obscurecido.

</dd> </dl>

## <a name="remarks"></a>Comentários

Esses sinalizadores são usados por [**D3DX11ComputeNormalMap**](d3dx11computenormalmap.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|----------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>D3DX11tex.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Enumerações D3DX](d3d11-graphics-reference-d3dx11-enums.md)
</dt> </dl>

 

 





