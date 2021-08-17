---
description: Método ID3DXEffectStateManager::SetPixelShaderConstantI – uma função de retorno de chamada que deve ser implementada por um usuário para definir uma matriz de constantes de inteiro do sombreador de vértice.
ms.assetid: 55f5747d-b7f8-4d13-ac2c-df2dcb160091
title: Método ID3DXEffectStateManager::SetPixelShaderConstantI (D3DX9Effect.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXEffectStateManager.SetPixelShaderConstantI
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: a817ac4e092eb9d8be2e4e2da02af051ae957dc97655b45e4e48dbe85b115ca3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119121499"
---
# <a name="id3dxeffectstatemanagersetpixelshaderconstanti-method"></a>Método ID3DXEffectStateManager::SetPixelShaderConstantI

Uma função de retorno de chamada que deve ser implementada por um usuário para definir uma matriz de constantes de inteiro do sombreador de vértice.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT SetPixelShaderConstantI(
  [out]       UINT StartRegister,
  [out] const INT  *pConstantData,
  [out]       UINT RegisterCount
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*StartRegister* \[ out\]
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

O índice baseado em zero do primeiro registro constante.

</dd> <dt>

*pConstantData* \[ out\]
</dt> <dd>

Tipo: **const [**INT**](../winprog/windows-data-types.md) \***

Uma matriz de constantes de inteiro.

</dd> <dt>

*RegisterCount* \[ out\]
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

O número de registros em pConstantData.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

O método implementado pelo usuário deve retornar S \_ OK. Se o retorno de chamada falhar ao definir o estado do dispositivo, ocorrerá um dos seguintes:

-   O efeito falhará durante [**ID3DXEffect::BeginPass.**](id3dxeffect--beginpass.md)
-   A chamada de estado de efeito dinâmico (como [**IDirect3DDevice9::SetPixelShaderConstantI**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setpixelshaderconstanti)) falhará.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3DX9Effect.h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9.lib</dt> </dl>     |



## <a name="see-also"></a>Confira também

<dl> <dt>

[ID3DXEffectStateManager](id3dxeffectstatemanager.md)
</dt> </dl>

 

 
