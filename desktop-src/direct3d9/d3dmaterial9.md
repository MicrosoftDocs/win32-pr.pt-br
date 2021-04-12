---
description: Especifica as propriedades do material.
ms.assetid: 943e6f6d-8091-462f-8c44-e0c27686934a
title: Estrutura D3DMATERIAL9 (D3D9Types. h)
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
ms.openlocfilehash: b9c3ad93fe2cb80fe758e2e66da37cce9d4267ad
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104370969"
---
# <a name="d3dmaterial9-structure"></a>Estrutura D3DMATERIAL9

Especifica as propriedades do material.

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

**Alimentar**
</dt> <dd>

Tipo: **float**

</dd> <dd>

Valor de ponto flutuante especificando a nitidez dos realces especulares. Quanto maior o valor, mais nítido o realce.

</dd> </dl>

## <a name="remarks"></a>Comentários

Para desativar os realces especulares, defina D3DRS \_ SPECULARENABLE como **false**, usando [**D3DRENDERSTATETYPE**](./d3drenderstatetype.md). Essa é a opção mais rápida porque nenhum realce especular será calculado.

Para obter mais informações sobre como usar o mecanismo de iluminação para calcular a iluminação especular, consulte [Iluminação especular (Direct3D 9)](specular-lighting.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|----------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>D3D9Types. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Estruturas do Direct3D](dx9-graphics-reference-d3d-structures.md)
</dt> <dt>

[**IDirect3DDevice9:: GetMaterial**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-getmaterial)
</dt> <dt>

[**IDirect3DDevice9:: SetMaterial**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setmaterial)
</dt> </dl>

 

 
