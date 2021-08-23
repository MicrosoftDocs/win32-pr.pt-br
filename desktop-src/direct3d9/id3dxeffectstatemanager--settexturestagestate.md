---
description: Uma função de retorno de chamada que deve ser implementada por um usuário para definir o estado do estágio de textura.
ms.assetid: cc86a483-ccf0-400d-b14d-ab55a3cf4b98
title: 'Método ID3DXEffectStateManager:: SetTextureStageState (D3DX9Effect. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXEffectStateManager.SetTextureStageState
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 5a74642d97532020679749d54924f4ab4052100d638d2bbd902b7b721fc75610
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118520981"
---
# <a name="id3dxeffectstatemanagersettexturestagestate-method"></a>Método ID3DXEffectStateManager:: SetTextureStageState

Uma função de retorno de chamada que deve ser implementada por um usuário para definir o estado do estágio de textura.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT SetTextureStageState(
  [in] DWORD                    Stage,
  [in] D3DTEXTURESTAGESTATETYPE Type,
  [in] DWORD                    Value
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Estágio* \[ no\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

O estágio ao qual a textura está atribuída. Este é o valor de índice em [**IDirect3DDevice9:: SetTexture**](/windows/desktop/api) ou [**IDirect3DDevice9:: SetTextureStageState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexturestagestate).

</dd> <dt>

*Tipo* \[ de no\]
</dt> <dd>

Tipo: **[ **D3DTEXTURESTAGESTATETYPE**](./d3dtexturestagestatetype.md)**

Define o tipo de operação que um estágio de textura executará. Consulte [**D3DTEXTURESTAGESTATETYPE**](./d3dtexturestagestatetype.md).

</dd> <dt>

*Valor* \[ do no\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

Pode ser uma operação ([**D3DTEXTUREOP**](./d3dtextureop.md)) ou um valor de argumento ([D3DTA](d3dta.md)), dependendo do que é escolhido para o tipo.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

O método implementado pelo usuário deve retornar S \_ OK. Se o retorno de chamada falhar ao definir o estado do dispositivo, ocorrerá uma das seguintes opções:

-   O efeito falhará durante [**ID3DXEffect:: BeginPass**](id3dxeffect--beginpass.md).
-   A chamada de estado de efeito dinâmico (como [**IDirect3DDevice9:: SetTextureStageState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexturestagestate)) falhará.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3DX9Effect. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9. lib</dt> </dl>     |



## <a name="see-also"></a>Confira também

<dl> <dt>

[ID3DXEffectStateManager](id3dxeffectstatemanager.md)
</dt> </dl>

 

 
