---
description: Obtém uma descrição de parâmetro ou anotação.
ms.assetid: fd54eb08-a7e4-4106-b0ed-49a4da7fcadc
title: 'Método ID3DXBaseEffect:: GetParameterDesc (D3DX9Effect. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseEffect.GetParameterDesc
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 8c60332909ef601d58cb624201bae6e1934a84699ead1227a5d8a83c2db64dc8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118296699"
---
# <a name="id3dxbaseeffectgetparameterdesc-method"></a>Método ID3DXBaseEffect:: GetParameterDesc

Obtém uma descrição de parâmetro ou anotação.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT GetParameterDesc(
  [in]  D3DXHANDLE         hParameter,
  [out] D3DXPARAMETER_DESC *pDesc
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*hParameter* \[ no\]
</dt> <dd>

Tipo: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**

Identificador de parâmetro ou de anotação. Consulte [Handles (Direct3D 9)](handles.md).

</dd> <dt>

*pDesc* \[ fora\]
</dt> <dd>

Tipo: **[ **D3DXPARAMETER \_ desc**](d3dxparameter-desc.md)\***

Retorna uma descrição do parâmetro ou da anotação especificada. Consulte [**D3DXPARAMETER \_ desc**](d3dxparameter-desc.md).

</dd> </dl>

## <a name="return-value"></a>Retornar valor

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

 

 




