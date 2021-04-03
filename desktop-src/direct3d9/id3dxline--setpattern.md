---
description: Aplica um padrão Stipple à linha.
ms.assetid: 53548a9f-cf09-4ab9-9327-d5053645fc1b
title: 'Método ID3DXLine:: setpattern (D3dx9core. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXLine.SetPattern
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 80a0485991bc06bdb9fcd3280017d4cc60b492ca
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104091991"
---
# <a name="id3dxlinesetpattern-method"></a>Método ID3DXLine:: setpattern

Aplica um padrão Stipple à linha.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT SetPattern(
  [in] DWORD dwPattern
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*dwPattern* \[ no\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

Descreve o padrão Stipple: 1 é opaco, 0 é transparente.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se o método for bem sucedido, o valor de retorno será D3D \_ OK. Se o método falhar, o valor de retorno poderá ser um dos seguintes: D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|----------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3dx9core. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Confira também

<dl> <dt>

[ID3DXLine](id3dxline.md)
</dt> </dl>

 

 
