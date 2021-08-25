---
description: Uma função de retorno de chamada que deve ser implementada por um usuário para definir um código FVF.
ms.assetid: 701a4333-a71e-4d84-a06c-1c86312ee4ff
title: 'Método ID3DXEffectStateManager:: SetFVF (D3DX9Effect. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXEffectStateManager.SetFVF
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 828f6873ed9bf48de6a02d4195fdd1fa9d2bc39f99da1f8906fd8a2c53075cf5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120026406"
---
# <a name="id3dxeffectstatemanagersetfvf-method"></a>Método ID3DXEffectStateManager:: SetFVF

Uma função de retorno de chamada que deve ser implementada por um usuário para definir um código FVF.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT SetFVF(
  [in] DWORD FVF
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*FVF* \[ no\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

A constante FVF, que determina como interpretar os dados de vértice. Consulte [D3DFVF](d3dfvf.md).

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

O método implementado pelo usuário deve retornar S \_ OK. Se o retorno de chamada falhar ao definir o estado do dispositivo, ocorrerá uma das seguintes opções:

-   O efeito falhará durante [**ID3DXEffect:: BeginPass**](id3dxeffect--beginpass.md).
-   A chamada de estado de efeito dinâmico (como [**IDirect3DDevice9:: SetFVF**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setfvf)) falhará.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3DX9Effect. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9. lib</dt> </dl>     |



## <a name="see-also"></a>Confira também

<dl> <dt>

[ID3DXEffectStateManager](id3dxeffectstatemanager.md)
</dt> </dl>

 

 
