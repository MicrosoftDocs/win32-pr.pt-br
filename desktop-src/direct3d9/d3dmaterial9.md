---
description: Especifica propriedades de material.
ms.assetid: 943e6f6d-8091-462f-8c44-e0c27686934a
title: Estrutura D3DMATERIAL9 (D3D9Types.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DMATERIAL9
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: 640fd4ce0110f47aa20a04d0df595b0ae8bf5052c229825dd93e1066150c6306
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118527576"
---
# <a name="d3dmaterial9-structure"></a>Estrutura D3DMATERIAL9

Especifica propriedades de material.

## <a name="syntax"></a>Sintaxe


```C++
typedef struct D3DMATERIAL9 {
  D3DCOLORVALUE Diffuse;
  D3DCOLORVALUE Ambient;
  D3DCOLORVALUE Specular;
  D3DCOLORVALUE Emissive;
  float         Power;
} D3DMATERIAL9, *LPD3DMATERIAL9;
```



## <a name="members"></a>Membros

<dl> <dt>

**Difusa**
</dt> <dd>

Tipo: **[ **D3DCOLORVALUE**](d3dcolorvalue.md)**

</dd> <dd>

Valor que especifica a cor difusa do material. Consulte [**D3DCOLORVALUE**](d3dcolorvalue.md).

</dd> <dt>

**Ambiente**
</dt> <dd>

Tipo: **[ **D3DCOLORVALUE**](d3dcolorvalue.md)**

</dd> <dd>

Valor que especifica a cor do ambiente do material. Consulte [**D3DCOLORVALUE**](d3dcolorvalue.md).

</dd> <dt>

**Especular**
</dt> <dd>

Tipo: **[ **D3DCOLORVALUE**](d3dcolorvalue.md)**

</dd> <dd>

Valor que especifica a cor especular do material. Consulte [**D3DCOLORVALUE**](d3dcolorvalue.md).

</dd> <dt>

**Emissiva**
</dt> <dd>

Tipo: **[ **D3DCOLORVALUE**](d3dcolorvalue.md)**

</dd> <dd>

Valor que especifica a cor emissiva do material. Consulte [**D3DCOLORVALUE**](d3dcolorvalue.md).

</dd> <dt>

**Poder**
</dt> <dd>

Tipo: **float**

</dd> <dd>

Valor de ponto flutuante que especifica a sharpness de realçamentos especular. Quanto maior o valor, mais nítido o realçador.

</dd> </dl>

## <a name="remarks"></a>Comentários

Para desativar os destaques especular, de conjunto D3DRS \_ SPECUABLE como **FALSE,** usando [**D3DRENDERSTATETYPE**](./d3drenderstatetype.md). Essa é a opção mais rápida porque nenhum realçando especular será calculado.

Para obter mais informações sobre como usar o mecanismo de iluminação para calcular a iluminação especular, consulte [Iluminação especular (Direct3D 9)](specular-lighting.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|----------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>D3D9Types.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Estruturas Direct3D](dx9-graphics-reference-d3d-structures.md)
</dt> <dt>

[**IDirect3DDevice9::GetMaterial**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-getmaterial)
</dt> <dt>

[**IDirect3DDevice9::SetMaterial**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setmaterial)
</dt> </dl>

 

 
