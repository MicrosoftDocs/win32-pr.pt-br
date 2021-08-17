---
description: Extrai os coeficientes de projeção do PCA (análise de componente principal) por exemplo de um buffer de dados compactado ID3DXPRTCompBuffer e adiciona os dados a um objeto ID3DXMesh.
ms.assetid: 0680d626-f07a-43d3-acb9-e8db82b5e933
title: 'Método ID3DXPRTCompBuffer:: ExtractToMesh (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPRTCompBuffer.ExtractToMesh
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 410ec268da89ad4033c88a90c2b37bfa8e78a7b9c229cab72c8ad07e666fce42
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117730032"
---
# <a name="id3dxprtcompbufferextracttomesh-method"></a>Método ID3DXPRTCompBuffer:: ExtractToMesh

Extrai os coeficientes de projeção do PCA (análise de componente principal) por exemplo de um buffer de dados compactado [**ID3DXPRTCompBuffer**](id3dxprtcompbuffer.md) e adiciona os dados a um objeto [**ID3DXMesh**](id3dxmesh.md) .

## <a name="syntax"></a>Sintaxe


```C++
HRESULT ExtractToMesh(
  [in] UINT         NumPCA,
  [in] D3DDECLUSAGE Usage,
  [in] UINT         UsageIndexStart,
  [in] LPD3DXMESH   pScene
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*NumPCA* \[ no\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

Número de coeficientes do PCA a serem extraídos do buffer.

</dd> <dt>

*Uso* \[ do no\]
</dt> <dd>

Tipo: **[ **D3DDECLUSAGE**](./d3ddeclusage.md)**

Descrições de uso de vértice da malha. Consulte [**D3DDECLUSAGE**](./d3ddeclusage.md).

</dd> <dt>

*UsageIndexStart* \[ no\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

Índice inicial para os coeficientes do PCA a serem armazenados na malha.

</dd> <dt>

*pScene* \[ no\]
</dt> <dd>

Tipo: **[ **LPD3DXMESH**](id3dxmesh.md)**

Ponteiro para um objeto de malha [**ID3DXMesh**](id3dxmesh.md) que armazenará os coeficientes do PCA.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se o método for bem sucedido, o valor de retorno será S \_ OK. Se o método falhar, o valor de retorno poderá ser um dos seguintes: D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|----------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Confira também

<dl> <dt>

[ID3DXPRTCompBuffer](id3dxprtcompbuffer.md)
</dt> </dl>

 

 
