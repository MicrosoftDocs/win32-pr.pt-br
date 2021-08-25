---
description: Conjuntos predefinidos de estado de pipeline usados por blocos de estado (consulte Estado de salvar e restaurar blocos de estado (Direct3D 9)).
ms.assetid: 60b94d45-aab6-4dbe-ab48-65dfe9861d82
title: Enumeração D3DSTATEBLOCKTYPE (D3D9Types.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DSTATEBLOCKTYPE
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: 7780b7ded37ba976f32f4439ab793ae711be2f5790d03555a6a8be4f031571e2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119850177"
---
# <a name="d3dstateblocktype-enumeration"></a>Enumeração D3DSTATEBLOCKTYPE

Conjuntos predefinidos de estado de pipeline usados por blocos de estado (consulte Estado de salvar e restaurar blocos de estado [(Direct3D 9)](state-blocks-save-and-restore-state.md)).

## <a name="syntax"></a>Syntax


```C++
typedef enum _D3DSTATEBLOCKTYPE { 
  D3DSBT_ALL          = 1,
  D3DSBT_PIXELSTATE   = 2,
  D3DSBT_VERTEXSTATE  = 3,
  D3DSBT_FORCE_DWORD  = 0x7fffffff
} D3DSTATEBLOCKTYPE;
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="D3DSBT_ALL"></span><span id="d3dsbt_all"></span>**D3DSBT \_ ALL**
</dt> <dd>

Capture o estado [atual do dispositivo](saving-all-device-states-with-a-stateblock.md).

</dd> <dt>

<span id="D3DSBT_PIXELSTATE"></span><span id="d3dsbt_pixelstate"></span>**D3DSBT \_ PIXELSTATE**
</dt> <dd>

Capture o estado [de pixel atual.](saving-pixel-states-with-a-stateblock.md)

</dd> <dt>

<span id="D3DSBT_VERTEXSTATE"></span><span id="d3dsbt_vertexstate"></span>**D3DSBT \_ VERTEXSTATE**
</dt> <dd>

Capture o estado [atual do vértice](saving-vertex-states-with-a-stateblock.md).

</dd> <dt>

<span id="D3DSBT_FORCE_DWORD"></span><span id="d3dsbt_force_dword"></span>**D3DSBT \_ FORCE \_ DWORD**
</dt> <dd>

Força essa enumeração a compilar para 32 bits de tamanho. Sem esse valor, alguns compiladores permitiriam que essa enumeração fosse compilada para um tamanho diferente de 32 bits. Não use esse valor.

</dd> </dl>

## <a name="remarks"></a>Comentários

Como mostra o diagrama a seguir, o vértice e o estado de pixel são ambos subconjunto do estado do dispositivo.

![diagrama do estado do dispositivo, com estado de vértice e estado de pixel como subconjunto](images/statesets.png)

Há apenas alguns estados que são considerados estado de vértice e pixel. Esses estados são:

-   Estado de renderização: D3DRS \_ DRADENSITY
-   Estado de renderização: D3DRSSTART \_
-   Estado de renderização: D3DRS \_ REFEREND
-   Estado da textura: D3DTSS \_ TEXCOORDINDEX
-   Estado da textura: \_ TEXTURETRANSFORMFLAGS D3DTSS

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|----------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>D3D9Types.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Enumerações direct3D](dx9-graphics-reference-d3d-enums.md)
</dt> <dt>

[**IDirect3DDevice9::CreateStateBlock**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createstateblock)
</dt> <dt>

**IDirect3DDevice9::CreateStateBlock**
</dt> </dl>

 

 
