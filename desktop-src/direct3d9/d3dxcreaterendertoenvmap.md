---
description: Cria um mapa de ambiente de renderização.
ms.assetid: 5ca10602-5ab1-4766-a350-706c46c55df2
title: Função D3DXCreateRenderToEnvMap (D3dx9core. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreateRenderToEnvMap
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 6829d53f53bd6a4783f5873eeed614e48bbe1088
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104012096"
---
# <a name="d3dxcreaterendertoenvmap-function"></a>Função D3DXCreateRenderToEnvMap

Cria um mapa de ambiente de renderização.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT D3DXCreateRenderToEnvMap(
  _In_  LPDIRECT3DDEVICE9    pDevice,
  _In_  UINT                 Size,
  _In_  UINT                 MipLevels,
  _In_  D3DFORMAT            Format,
  _In_  BOOL                 DepthStencil,
  _In_  D3DFORMAT            DepthStencilFormat,
  _Out_ LPD3DXRENDERTOENVMAP *ppRenderToEnvMap
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pDevice* \[ no\]
</dt> <dd>

Tipo: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**

Ponteiro para uma interface [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) , que é o dispositivo a ser associado à superfície de renderização.

</dd> <dt>

*Tamanho* \[ no\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

Tamanho da superfície de renderização.

</dd> <dt>

*MipLevels* \[ no\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

O número de níveis de mipmap.

</dd> <dt>

*Formato* \[ no\]
</dt> <dd>

Tipo: **[D3DFORMAT](d3dformat.md)**

Membro do tipo enumerado [D3DFORMAT](d3dformat.md) que descreve o formato de pixel do mapa de ambiente.

</dd> <dt>

*DepthStencil* \[ no\]
</dt> <dd>

Tipo: **[ **bool**](../winprog/windows-data-types.md)**

Se **for true**, a superfície de renderização dará suporte a uma superfície de estêncil de profundidade. Caso contrário, esse membro será definido como **false**.

</dd> <dt>

*DepthStencilFormat* \[ no\]
</dt> <dd>

Tipo: **[D3DFORMAT](d3dformat.md)**

Se DepthStencil for definido como **true**, esse parâmetro será um membro do tipo enumerado [D3DFORMAT](d3dformat.md) que descreve o formato de estêncil de profundidade do mapa de ambiente.

</dd> <dt>

*ppRenderToEnvMap* \[ fora\]
</dt> <dd>

Tipo: **[ **LPD3DXRENDERTOENVMAP**](id3dxrendertoenvmap.md)\***

Endereço de um ponteiro para uma interface [**ID3DXRenderToEnvMap**](id3dxrendertoenvmap.md) que representa o mapa de ambiente de renderização criado.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

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

 

 
