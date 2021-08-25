---
description: Obtém uma descrição da função.
ms.assetid: a1a0ccf4-2428-4e60-9af0-07dc2132a367
title: 'Método ID3DXBaseEffect:: GetFunctionDesc (D3DX9Effect. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseEffect.GetFunctionDesc
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: b8f74715b163b3d197f62274c6aa6bf52ae872254db9df8225e061dc54900964
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119893716"
---
# <a name="id3dxbaseeffectgetfunctiondesc-method"></a>Método ID3DXBaseEffect:: GetFunctionDesc

Obtém uma descrição da função.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT GetFunctionDesc(
  [in]  D3DXHANDLE        hFunction,
  [out] D3DXFUNCTION_DESC *pDesc
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*hFunction* \[ no\]
</dt> <dd>

Tipo: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**

Identificador de função. Consulte [Handles (Direct3D 9)](handles.md).

</dd> <dt>

*pDesc* \[ fora\]
</dt> <dd>

Tipo: **[ **D3DXFUNCTION \_ desc**](d3dxfunction-desc.md)\***

Retorna uma descrição da função. Consulte [**D3DXFUNCTION \_ desc**](d3dxfunction-desc.md).

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se o método for bem sucedido, o valor de retorno será S \_ OK. Se o método falhar, o valor de retorno poderá ser D3DERR \_ INVALIDCALL.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3DX9Effect. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9. lib</dt> </dl>     |



## <a name="see-also"></a>Confira também

<dl> <dt>

[ID3DXBaseEffect](id3dxbaseeffect.md)
</dt> </dl>

 

 




