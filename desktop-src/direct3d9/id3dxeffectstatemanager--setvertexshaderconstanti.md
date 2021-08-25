---
description: Método ID3DXEffectStateManager::SetVertexShaderConstantI – uma função de retorno de chamada que deve ser implementada por um usuário para definir uma matriz de constantes de inteiro do sombreador de vértice.
ms.assetid: 0035c97a-1b17-4665-9032-7b3b9a9d2cff
title: Método ID3DXEffectStateManager::SetVertexShaderConstantI (D3DX9Effect.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXEffectStateManager.SetVertexShaderConstantI
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 949f2cb23e15e3cfb99fcb6880795cfbd6019a8c858198b23bb9db6508714d44
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119856686"
---
# <a name="id3dxeffectstatemanagersetvertexshaderconstanti-method"></a>Método ID3DXEffectStateManager::SetVertexShaderConstantI

Uma função de retorno de chamada que deve ser implementada por um usuário para definir uma matriz de constantes de inteiro do sombreador de vértice.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT SetVertexShaderConstantI(
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
-   A chamada de estado de efeito dinâmico (como [**IDirect3DDevice9::SetVertexShaderConstantI**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setvertexshaderconstanti)) falhará.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3DX9Effect.h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9.lib</dt> </dl>     |



## <a name="see-also"></a>Confira também

<dl> <dt>

[ID3DXEffectStateManager](id3dxeffectstatemanager.md)
</dt> </dl>

 

 
