---
description: Descreve um destino de renderização fora da tela usado por uma instância de ID3DXRenderToEnvMap.
ms.assetid: 805df4da-e882-4d54-bf2c-49cfcbc59ac6
title: Estrutura de D3DXRTE_DESC (D3dx9core. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXRTE_DESC
api_type:
- HeaderDef
api_location:
- d3dx9core.h
ms.openlocfilehash: 91efe4dff2b392310ed2fd6bdc30db12c883c5d08e6b2cf110c2cb29d73c54ce
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120027276"
---
# <a name="d3dxrte_desc-structure"></a>\_Estrutura desc de D3DXRTE

Descreve um destino de renderização fora da tela usado por uma instância de [**ID3DXRenderToEnvMap**](id3dxrendertoenvmap.md).

## <a name="syntax"></a>Sintaxe


```C++
typedef struct D3DXRTE_DESC {
  UINT      Size;
  UINT      MipLevels;
  D3DFORMAT Format;
  BOOL      DepthStencil;
  D3DFORMAT DepthStencilFormat;
} D3DXRTE_DESC, *LPD3DXRTE_DESC;
```



## <a name="members"></a>Membros

<dl> <dt>

**Tamanho**
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

</dd> <dd>

Largura e altura em pixels.

</dd> <dt>

**MipLevels**
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

</dd> <dd>

Número máximo de detalhes (LOD).

</dd> <dt>

**Formato**
</dt> <dd>

Tipo: **[D3DFORMAT](d3dformat.md)**

</dd> <dd>

Formato de buffer de cores.

</dd> <dt>

**DepthStencil**
</dt> <dd>

Tipo: **[ **bool**](../winprog/windows-data-types.md)**

</dd> <dd>

Indica se o z-buffer é necessário.

</dd> <dt>

**DepthStencilFormat**
</dt> <dd>

Tipo: **[D3DFORMAT](d3dformat.md)**

</dd> <dd>

Formato do buffer de profundidade.

</dd> </dl>

## <a name="remarks"></a>Comentários

Esse método é usado para retornar os parâmetros de criação usados ao criar um objeto [**ID3DXRenderToEnvMap**](id3dxrendertoenvmap.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|----------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>D3dx9core. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Estruturas D3DX](dx9-graphics-reference-d3dx-structures.md)
</dt> </dl>

 

 
