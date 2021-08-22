---
description: Uma função de retorno de chamada que deve ser implementada por um usuário para definir o estado do material.
ms.assetid: 4c5e903f-551b-4346-a5eb-301a3a5b9b44
title: Método ID3DXEffectStateManager::SetMaterial (D3DX9Effect.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXEffectStateManager.SetMaterial
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 67e8b1ad498b5aacbae7aaad2d6b63fa406d54d6315a4e75b3028efe3107eaf8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118802870"
---
# <a name="id3dxeffectstatemanagersetmaterial-method"></a>Método ID3DXEffectStateManager::SetMaterial

Uma função de retorno de chamada que deve ser implementada por um usuário para definir o estado do material.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT SetMaterial(
  [in] const D3DMATERIAL9 *pMaterial
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pMaterial* \[ Em\]
</dt> <dd>

Tipo: **const [**D3DMATERIAL9**](d3dmaterial9.md) \***

Um ponteiro para o estado do material. Consulte [**D3DMATERIAL9**](d3dmaterial9.md).

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

O método implementado pelo usuário deve retornar S \_ OK. Se o retorno de chamada falhar ao definir o estado do dispositivo, ocorrerá um dos seguintes:

-   O efeito falhará durante [**ID3DXEffect::BeginPass.**](id3dxeffect--beginpass.md)
-   A chamada de estado de efeito dinâmico (como [**IDirect3DDevice9::SetMaterial**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setmaterial)) falhará.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3DX9Effect.h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9.lib</dt> </dl>     |



## <a name="see-also"></a>Confira também

<dl> <dt>

[ID3DXEffectStateManager](id3dxeffectstatemanager.md)
</dt> </dl>

 

 
