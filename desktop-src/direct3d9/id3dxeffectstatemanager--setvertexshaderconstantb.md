---
description: 'Método ID3DXEffectStateManager:: SetVertexShaderConstantB – uma função de retorno de chamada que deve ser implementada por um usuário para definir uma matriz de constantes booleanas de sombreador de vértice.'
ms.assetid: 25fd0c68-11b5-4401-a2f8-86075ba3fa54
title: 'Método ID3DXEffectStateManager:: SetVertexShaderConstantB (D3DX9Effect. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXEffectStateManager.SetVertexShaderConstantB
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 79d4972c301d7333869d68d36267186a67b37eb1
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108090404"
---
# <a name="id3dxeffectstatemanagersetvertexshaderconstantb-method"></a>Método ID3DXEffectStateManager:: SetVertexShaderConstantB

Uma função de retorno de chamada que deve ser implementada por um usuário para definir uma matriz de constantes booleanas do sombreador de vértice.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT SetVertexShaderConstantB(
  [out]       UINT StartRegister,
  [out] const BOOL *pConstantData,
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

Tipo: **const [**bool**](../winprog/windows-data-types.md) \***

Uma matriz de constantes boolianas.

</dd> <dt>

*RegisterCount* \[ fora\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

O número de registros em pConstantData.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

O método implementado pelo usuário deve retornar S \_ OK. Se o retorno de chamada falhar ao definir o estado do dispositivo, ocorrerá uma das seguintes opções:

-   O efeito falhará durante [**ID3DXEffect:: BeginPass**](id3dxeffect--beginpass.md).
-   A chamada de estado de efeito dinâmico (como [**IDirect3DDevice9:: SetVertexShaderConstantB**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setvertexshaderconstantb)) falhará.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3DX9Effect. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9. lib</dt> </dl>     |



## <a name="see-also"></a>Consulte também

<dl> <dt>

[ID3DXEffectStateManager](id3dxeffectstatemanager.md)
</dt> </dl>

 

 
