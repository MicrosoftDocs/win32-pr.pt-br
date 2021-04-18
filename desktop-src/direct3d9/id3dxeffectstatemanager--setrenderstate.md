---
description: Uma função de retorno de chamada que deve ser implementada por um usuário para definir o estado de renderização.
ms.assetid: a5a27e30-c141-44a4-b8d4-38c1d6076b2a
title: 'Método ID3DXEffectStateManager:: setrenderingstate (D3DX9Effect. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXEffectStateManager.SetRenderState
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 111ab8ff379d5b095500101674fc45b6a2b31bc1
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105815507"
---
# <a name="id3dxeffectstatemanagersetrenderstate-method"></a>Método ID3DXEffectStateManager:: setrenderingstate

Uma função de retorno de chamada que deve ser implementada por um usuário para definir o estado de renderização.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT SetRenderState(
  [in] D3DRENDERSTATETYPE State,
  [in] DWORD              Value
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Estado* \[ no\]
</dt> <dd>

Tipo: **[ **D3DRENDERSTATETYPE**](./d3drenderstatetype.md)**

O estado de renderização a ser definido. [**D3DRENDERSTATETYPE**](./d3drenderstatetype.md)

</dd> <dt>

*Valor* \[ do no\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

O valor do estado de renderização. Consulte [Estados de efeito (Direct3D 9)](effect-states.md).

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

O método implementado pelo usuário deve retornar S \_ OK. Se o retorno de chamada falhar ao definir o estado do dispositivo, ocorrerá uma das seguintes opções:

-   O efeito falhará durante [**ID3DXEffect:: BeginPass**](id3dxeffect--beginpass.md).
-   A chamada de estado de efeito dinâmico (como [**IDirect3DDevice9:: Setrenderingstate**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate)) falhará.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3DX9Effect. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9. lib</dt> </dl>     |



## <a name="see-also"></a>Confira também

<dl> <dt>

[ID3DXEffectStateManager](id3dxeffectstatemanager.md)
</dt> </dl>

 

 
