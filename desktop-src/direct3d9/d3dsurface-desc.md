---
description: Descreve uma superfície.
ms.assetid: fad8ffdb-36e5-4695-b343-e1315357c31a
title: Estrutura de D3DSURFACE_DESC (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DSURFACE_DESC
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: 6424bbe9b78532657670bc5cd9ad0705de89a3b0
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105768379"
---
# <a name="d3dsurface_desc-structure"></a>\_Estrutura desc de D3DSURFACE

Descreve uma superfície.

## <a name="syntax"></a>Sintaxe


```C++
typedef struct D3DSURFACE_DESC {
  D3DFORMAT           Format;
  D3DRESOURCETYPE     Type;
  DWORD               Usage;
  D3DPOOL             Pool;
  D3DMULTISAMPLE_TYPE MultiSampleType;
  DWORD               MultiSampleQuality;
  UINT                Width;
  UINT                Height;
} D3DSURFACE_DESC, *LPD3DSURFACE_DESC;
```



## <a name="members"></a>Membros

<dl> <dt>

**Formato**
</dt> <dd>

Tipo: **[D3DFORMAT](d3dformat.md)**

</dd> <dd>

Membro do tipo enumerado [D3DFORMAT](d3dformat.md) , que descreve o formato da superfície.

</dd> <dt>

**Tipo**
</dt> <dd>

Tipo: **[ **D3DRESOURCETYPE**](./d3dresourcetype.md)**

</dd> <dd>

Membro do tipo enumerado [**D3DRESOURCETYPE**](./d3dresourcetype.md) , identificando esse recurso como uma superfície.

</dd> <dt>

**Usage**
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

</dd> <dd>

Os valores D3DUSAGE \_ DEPTHSTENCIL ou D3DUSAGE \_ RENDERTARGET. Para obter mais informações, consulte [**D3DUSAGE**](d3dusage.md).

</dd> <dt>

**Pool**
</dt> <dd>

Tipo: **[ **D3DPOOL**](./d3dpool.md)**

</dd> <dd>

Membro do tipo enumerado [**D3DPOOL**](./d3dpool.md) , especificando a classe de memória alocada para essa superfície.

</dd> <dt>

**Multiamostratype**
</dt> <dd>

Tipo: **[ **\_ tipo de D3DMULTISAMPLE**](./d3dmultisample-type.md)**

</dd> <dd>

Membro do tipo [**\_ enumerado D3DMULTISAMPLE**](./d3dmultisample-type.md) , especificando os níveis de multiamostragens de cena completa com suporte na superfície.

</dd> <dt>

**MultiSampleQuality**
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

</dd> <dd>

Nível de qualidade. O intervalo válido é entre zero e um menor que o nível retornado por pQualityLevels usado pelo [**CheckDeviceMultiSampleType**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-checkdevicemultisampletype). Passar um valor maior retorna o erro D3DERR \_ INVALIDCALL. Os valores MultisampleQuality de destinos de renderização emparelhados, superfícies de estêncil de profundidade e o tipo multiamostral devem corresponder a todos.

</dd> <dt>

**Largura**
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

</dd> <dd>

Largura da superfície, em pixels.

</dd> <dt>

**Altura**
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

</dd> <dd>

Altura da superfície, em pixels.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|----------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>D3D9Types. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Estruturas do Direct3D](dx9-graphics-reference-d3d-structures.md)
</dt> <dt>

[**GetLevelDesc**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dcubetexture9-getleveldesc)
</dt> <dt>

[**GetDesc**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dsurface9-getdesc)
</dt> <dt>

[**GetLevelDesc**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dcubetexture9-getleveldesc)
</dt> </dl>

 

 
