---
description: Cria uma superfície de renderização.
ms.assetid: 35e0007e-c405-46e1-a52b-625adc84732b
title: Função D3DXCreateRenderToSurface (D3dx9core. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreateRenderToSurface
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 632225dcad44324f88d8c126eb3f74d7779ff5ec698581514717dc1e0c54d3f7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118988626"
---
# <a name="d3dxcreaterendertosurface-function"></a>Função D3DXCreateRenderToSurface

Cria uma superfície de renderização.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT D3DXCreateRenderToSurface(
  _In_  LPDIRECT3DDEVICE9     pDevice,
  _In_  UINT                  Width,
  _In_  UINT                  Height,
  _In_  D3DFORMAT             Format,
  _In_  BOOL                  DepthStencil,
  _In_  D3DFORMAT             DepthStencilFormat,
  _Out_ LPD3DXRENDERTOSURFACE *ppRenderToSurface
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pDevice* \[ no\]
</dt> <dd>

Tipo: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**

Ponteiro para uma interface [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) , o dispositivo a ser associado à superfície de renderização.

</dd> <dt>

*Largura* \[ no\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

Largura da superfície de renderização, em pixels.

</dd> <dt>

*Altura* \[ no\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

Altura da superfície de renderização, em pixels.

</dd> <dt>

*Formato* \[ no\]
</dt> <dd>

Tipo: **[D3DFORMAT](d3dformat.md)**

Membro do tipo enumerado [D3DFORMAT](d3dformat.md) , que descreve o formato de pixel da superfície de renderização.

</dd> <dt>

*DepthStencil* \[ no\]
</dt> <dd>

Tipo: **[ **bool**](../winprog/windows-data-types.md)**

Se **for true**, a superfície de renderização dará suporte a uma superfície de estêncil de profundidade. Caso contrário, esse membro será definido como **false**. Essa função criará um novo buffer de profundidade.

</dd> <dt>

*DepthStencilFormat* \[ no\]
</dt> <dd>

Tipo: **[D3DFORMAT](d3dformat.md)**

Se *DepthStencil* for definido como **true**, esse parâmetro será um membro do tipo enumerado [D3DFORMAT](d3dformat.md) , descrevendo o formato de estêncil de profundidade da superfície de renderização.

</dd> <dt>

*ppRenderToSurface* \[ fora\]
</dt> <dd>

Tipo: **[ **LPD3DXRENDERTOSURFACE**](id3dxrendertosurface.md)\***

Endereço de um ponteiro para uma interface [**ID3DXRenderToSurface**](id3dxrendertosurface.md) , que representa a superfície de renderização criada.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se a função for bem sucedido, o valor de retorno será D3D \_ OK. Se a função falhar, o valor de retorno poderá ser um dos seguintes: D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|----------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3dx9core. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Funções de Uso Geral](dx9-graphics-reference-d3dx-functions-general-purpose.md)
</dt> </dl>

 

 
