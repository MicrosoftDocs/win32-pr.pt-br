---
description: Uma função de retorno de chamada que deve ser implementada por um usuário para definir uma luz.
ms.assetid: 3b9b2cbd-79f5-4ea4-a47b-da23b091adfd
title: 'Método ID3DXEffectStateManager:: SetLight (D3DX9Effect. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXEffectStateManager.SetLight
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 1306283b098922706f39abc7ffe2514d2fba0e5c
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105781178"
---
# <a name="id3dxeffectstatemanagersetlight-method"></a>Método ID3DXEffectStateManager:: SetLight

Uma função de retorno de chamada que deve ser implementada por um usuário para definir uma luz.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT SetLight(
  [in]       DWORD     Index,
  [in] const D3DLight9 *pLight
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Índice* \[ do no\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

O índice de base zero da luz. Esse é o mesmo índice em [**IDirect3DDevice9:: SetLight**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setlight).

</dd> <dt>

*plight* \[ no\]
</dt> <dd>

Tipo: **const [**D3DLight9**](d3dlight9.md) \***

O objeto Light. Consulte [**D3DLIGHT9**](d3dlight9.md).

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

O método implementado pelo usuário deve retornar S \_ OK. Se o retorno de chamada falhar ao definir o estado do dispositivo, ocorrerá uma das seguintes opções:

-   O efeito falhará durante [**ID3DXEffect:: BeginPass**](id3dxeffect--beginpass.md).
-   A chamada de estado de efeito dinâmico (como [**IDirect3DDevice9:: SetLight**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setlight)) falhará.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3DX9Effect. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9. lib</dt> </dl>     |



## <a name="see-also"></a>Confira também

<dl> <dt>

[ID3DXEffectStateManager](id3dxeffectstatemanager.md)
</dt> </dl>

 

 
