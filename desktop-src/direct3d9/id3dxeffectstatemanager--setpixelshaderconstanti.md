---
description: Uma função de retorno de chamada que deve ser implementada por um usuário para definir uma matriz de constantes de inteiro de sombreador de vértice.
ms.assetid: 55f5747d-b7f8-4d13-ac2c-df2dcb160091
title: 'Método ID3DXEffectStateManager:: SetPixelShaderConstantI (D3DX9Effect. h)'
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
ms.openlocfilehash: 2e84d883370038435dc59bb948ef94fcd82223db
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105798190"
---
# <a name="id3dxeffectstatemanagersetpixelshaderconstanti-method"></a>Método ID3DXEffectStateManager:: SetPixelShaderConstantI

Uma função de retorno de chamada que deve ser implementada por um usuário para definir uma matriz de constantes de inteiro de sombreador de vértice.

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

*StartRegister* \[ fora\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

O índice de base zero da primeira constante registrada.

</dd> <dt>

*pConstantData* \[ fora\]
</dt> <dd>

Tipo: **const [**int**](../winprog/windows-data-types.md) \***

Uma matriz de constantes de inteiro.

</dd> <dt>

*RegisterCount* \[ fora\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

O número de registros em pConstantData.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

O método implementado pelo usuário deve retornar S \_ OK. Se o retorno de chamada falhar ao definir o estado do dispositivo, ocorrerá uma das seguintes opções:

-   O efeito falhará durante [**ID3DXEffect:: BeginPass**](id3dxeffect--beginpass.md).
-   A chamada de estado de efeito dinâmico (como [**IDirect3DDevice9:: SetPixelShaderConstantI**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setpixelshaderconstanti)) falhará.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3DX9Effect. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9. lib</dt> </dl>     |



## <a name="see-also"></a>Confira também

<dl> <dt>

[ID3DXEffectStateManager](id3dxeffectstatemanager.md)
</dt> </dl>

 

 
