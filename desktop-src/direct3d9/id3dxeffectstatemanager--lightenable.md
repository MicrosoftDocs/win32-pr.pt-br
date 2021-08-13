---
description: Uma função de retorno de chamada que deve ser implementada por um usuário para habilitar/desabilitar uma luz.
ms.assetid: 11522ca3-8a2f-4767-a6e6-4186cb4f3115
title: Método ID3DXEffectStateManager::LightEnable (D3DX9Effect.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXEffectStateManager.LightEnable
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 0a7ce5a4fe90e911faaf8927fe584004eec7a68eae7b5c75f1c3a92f017fd4bd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118295781"
---
# <a name="id3dxeffectstatemanagerlightenable-method"></a>Método ID3DXEffectStateManager::LightEnable

Uma função de retorno de chamada que deve ser implementada por um usuário para habilitar/desabilitar uma luz.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT LightEnable(
  [in] DWORD Index,
  [in] BOOL  Enable
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Índice* \[ Em\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

O índice baseado em zero da luz. Esse é o mesmo índice em [**IDirect3DDevice9::SetLight.**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setlight)

</dd> <dt>

*Habilitar* \[ Em\]
</dt> <dd>

Tipo: **[ **BOOL**](../winprog/windows-data-types.md)**

True para habilitar a luz; caso contrário, false.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

O método implementado pelo usuário deve retornar S \_ OK. Se o retorno de chamada falhar ao definir o estado do dispositivo, ocorrerá um dos seguintes:

-   O efeito falhará durante [**ID3DXEffect::BeginPass.**](id3dxeffect--beginpass.md)
-   A chamada de estado de efeito dinâmico (como [**IDirect3DDevice9::LightEnable**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-lightenable)) falhará.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3DX9Effect.h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9.lib</dt> </dl>     |



## <a name="see-also"></a>Confira também

<dl> <dt>

[ID3DXEffectStateManager](id3dxeffectstatemanager.md)
</dt> </dl>

 

 
