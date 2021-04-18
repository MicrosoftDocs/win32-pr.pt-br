---
description: Recupera os valores de albedo dos vértices de malha.
ms.assetid: 12b8d6d1-c806-4dcd-80ac-f3963215dcf4
title: 'Método ID3DXPRTEngine:: GetVertexAlbedo (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPRTEngine.GetVertexAlbedo
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 7926f6393221552107667c9209ef2b4c51945ab8
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105760616"
---
# <a name="id3dxprtenginegetvertexalbedo-method"></a>Método ID3DXPRTEngine:: GetVertexAlbedo

Recupera os valores de albedo dos vértices de malha.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT GetVertexAlbedo(
  [in, out] D3DXCOLOR *pVertColors,
  [in]      UINT      NumVerts
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pVertColors* \[ entrada, saída\]
</dt> <dd>

Tipo: **[ **D3DXCOLOR**](d3dxcolor.md)\***

Ponteiro para uma matriz de destino de valores albedo dos vértices de malha. Consulte [**D3DXCOLOR**](d3dxcolor.md).

</dd> <dt>

*NumVerts* \[ no\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

Número de vértices na malha.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se o método for bem sucedido, o valor de retorno será S \_ OK. Se o método falhar, o valor de retorno poderá ser um dos seguintes: D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|----------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Confira também

<dl> <dt>

[ID3DXPRTEngine](id3dxprtengine.md)
</dt> </dl>

 

 
