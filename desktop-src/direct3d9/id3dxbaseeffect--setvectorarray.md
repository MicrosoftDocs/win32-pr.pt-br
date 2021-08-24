---
description: Define uma matriz de vetores.
ms.assetid: 7a9c61b4-7bfc-4879-abd2-a42d40e9b2a7
title: Método ID3DXBaseEffect::SetVectorArray (D3DX9Shader.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseEffect.SetVectorArray
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 79018873b512b54277f2b63da23a9360389e10b32672be59807e7ef47c9884f2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119790636"
---
# <a name="id3dxbaseeffectsetvectorarray-method"></a>Método ID3DXBaseEffect::SetVectorArray

Define uma matriz de vetores.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT SetVectorArray(
  [in]       D3DXHANDLE  hParameter,
  [in] const D3DXVECTOR4 *pVector,
  [in]       UINT        Count
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*hParameter* \[ Em\]
</dt> <dd>

Tipo: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**

Identificador exclusivo. Consulte [Handles (Direct3D 9)](handles.md).

</dd> <dt>

*pVector* \[ Em\]
</dt> <dd>

Tipo: **const [**D3DXVECTOR4**](d3dxvector4.md) \***

Matriz de vetores de ponto flutuante 4D.

</dd> <dt>

*Contagem* \[ Em\]
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

Número de vetores na matriz.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se o método for bem-sucedido, o valor de retorno será D3D \_ OK. Se o método falhar, o valor de retorno poderá ser D3DERR \_ INVALIDCALL.

## <a name="remarks"></a>Comentários

Se os vetores de destino são menores que os vetores de origem, os componentes adicionais dos vetores de origem serão ignorados.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3DX9Shader.h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9.lib</dt> </dl>     |



## <a name="see-also"></a>Confira também

<dl> <dt>

[ID3DXBaseEffect](id3dxbaseeffect.md)
</dt> <dt>

[**GetVectorArray**](id3dxbaseeffect--getvectorarray.md)
</dt> </dl>

 

 
