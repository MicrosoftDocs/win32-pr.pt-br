---
title: Estrutura de D3DX11_EFFECT_TYPE_DESC (D3dx11effect. h)
description: Descreve um tipo de variável de efeito.
ms.assetid: bf2aa5b7-c68c-42bb-ae70-2fe16f8669a4
keywords:
- Estrutura D3DX11_EFFECT_TYPE_DESC Direct3D 11
topic_type:
- apiref
api_name:
- D3DX11_EFFECT_TYPE_DESC
api_location:
- d3dx11effect.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cc045b40105a698c9d051de791991c49d2b6d0dd4672d50f344e8781999dd5c5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118989956"
---
# <a name="d3dx11_effect_type_desc-structure"></a>\_ \_ Estrutura desc de tipo de efeito D3DX11 \_

Descreve um tipo de variável de efeito.

## <a name="syntax"></a>Sintaxe


```C++
typedef struct _D3DX11_EFFECT_TYPE_DESC {
  LPCSTR                      TypeName;
  D3D10_SHADER_VARIABLE_CLASS Class;
  D3D10_SHADER_VARIABLE_TYPE  Type;
  UINT                        Elements;
  UINT                        Members;
  UINT                        Rows;
  UINT                        Columns;
  UINT                        PackedSize;
  UINT                        UnpackedSize;
  UINT                        Stride;
} D3DX11_EFFECT_TYPE_DESC;
```



## <a name="members"></a>Membros

<dl> <dt>

**TypeName**
</dt> <dd>

Tipo: **[ **LPCSTR**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Nome do tipo, por exemplo, "FLOAT4" ou "MyStruct".

</dd> <dt>

**Classe**
</dt> <dd>

Tipo: **[ **\_ classe de \_ variável \_ d3d10 Shader**](/windows/desktop/api/d3dcommon/ne-d3dcommon-d3d_shader_variable_class)**

</dd> <dd>

A classe Variable (consulte [**a \_ \_ \_ classe da variável d3d10 Shader**](/windows/desktop/api/d3dcommon/ne-d3dcommon-d3d_shader_variable_class)).

</dd> <dt>

**Tipo**
</dt> <dd>

Tipo: **[ **\_ tipo de \_ variável \_ de sombreador d3d10**](/windows/desktop/api/d3dcommon/ne-d3dcommon-d3d_shader_variable_type)**

</dd> <dd>

O tipo de variável ( [**consulte \_ \_ \_ tipo de variável de sombreador d3d10**](/windows/desktop/api/d3dcommon/ne-d3dcommon-d3d_shader_variable_type)).

</dd> <dt>

**Elementos**
</dt> <dd>

Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Número de elementos neste tipo (0 se não for uma matriz).

</dd> <dt>

**Membros**
</dt> <dd>

Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Número de Membros (0 se não for uma estrutura).

</dd> <dt>

**Linhas**
</dt> <dd>

Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Número de linhas neste tipo (0 se não for um primitivo numérico).

</dd> <dt>

**Colunas**
</dt> <dd>

Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Número de colunas neste tipo (0 se não for um primitivo numérico).

</dd> <dt>

**PackedSize**
</dt> <dd>

Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Número de bytes necessários para representar esse tipo de dados, quando compactados rigidamente.

</dd> <dt>

**UnpackedSize**
</dt> <dd>

Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Número de bytes ocupados por esse tipo de dados, quando dispostos em um buffer de constantes.

</dd> <dt>

**Passo**
</dt> <dd>

Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Número de bytes a serem buscados entre os elementos, quando dispostos em um buffer de constantes.

</dd> </dl>

## <a name="remarks"></a>Comentários

O \_ \_ tipo de efeito D3DX11 \_ DESC é usado com [ **ID3DX11EffectType:: GetDesc**](id3dx11effecttype-getdesc.md)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|-------------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>D3dx11effect. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Efeitos 11 estruturas](d3d11-graphics-reference-effects11-structures.md)
</dt> </dl>

 

