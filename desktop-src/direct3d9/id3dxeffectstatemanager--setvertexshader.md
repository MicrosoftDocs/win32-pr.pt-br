---
description: Uma função de retorno de chamada que deve ser implementada por um usuário para definir um sombreador de vértice.
ms.assetid: 8f3d3be3-c073-441d-a318-6d2cd5e7aca5
title: Método ID3DXEffectStateManager::SetVertexShader (D3DX9Effect.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXEffectStateManager.SetVertexShader
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 5f52daf5174608985b18140d2e6efde849f0bd6292c00584ece3453cca33ebf0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118520918"
---
# <a name="id3dxeffectstatemanagersetvertexshader-method"></a>Método ID3DXEffectStateManager::SetVertexShader

Uma função de retorno de chamada que deve ser implementada por um usuário para definir um sombreador de vértice.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT SetVertexShader(
  [in] LPDIRECT3DVERTEXSHADER9 pShader
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pShader* \[ Em\]
</dt> <dd>

Tipo: **[ **LPDIRECT3DVERTEXSHADER9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvertexshader9)**

Um ponteiro para um objeto de sombreador de vértice. Consulte [**IDirect3DVertexShader9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvertexshader9).

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

O método implementado pelo usuário deve retornar S \_ OK. Se o retorno de chamada falhar ao definir o estado do dispositivo, ocorrerá um dos seguintes:

-   O efeito falhará durante [**ID3DXEffect::BeginPass.**](id3dxeffect--beginpass.md)
-   A chamada de estado de efeito dinâmico (como [**IDirect3DDevice9::SetVertexShader**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setvertexshader)) falhará.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3DX9Effect.h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9.lib</dt> </dl>     |



## <a name="see-also"></a>Confira também

<dl> <dt>

[ID3DXEffectStateManager](id3dxeffectstatemanager.md)
</dt> </dl>

 

 
