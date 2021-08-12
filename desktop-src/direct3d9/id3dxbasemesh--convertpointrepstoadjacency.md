---
description: Converte dados representativos de ponto em informações de adjacência de malha.
ms.assetid: 6ae40486-74be-45a8-9971-f20517c8dcf0
title: 'Método ID3DXBaseMesh:: ConvertPointRepsToAdjacency (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseMesh.ConvertPointRepsToAdjacency
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: b888bc7fe8be0aa8bbac1150717ff90440bb797d84d910f7bcb6ee4f35f49345
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118296204"
---
# <a name="id3dxbasemeshconvertpointrepstoadjacency-method"></a>Método ID3DXBaseMesh:: ConvertPointRepsToAdjacency

Converte dados representativos de ponto em informações de adjacência de malha.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT ConvertPointRepsToAdjacency(
  [in]      const DWORD *pPRep,
  [in, out]       DWORD *pAdjacency
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pPRep* \[ no\]
</dt> <dd>

Tipo: **const [**DWORD**](../winprog/windows-data-types.md) \***

Ponteiro para uma matriz de um DWORD por vértice da malha que contém dados representativos de ponto. Esse parâmetro é opcional. O fornecimento de um valor **nulo** fará com que esse parâmetro seja interpretado como uma matriz de "identidade".

</dd> <dt>

*pAdjacency* \[ entrada, saída\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)\***

Ponteiro para uma matriz de três DWORDs por face que especificam os três vizinhos para cada face na malha. O número de bytes nessa matriz deve ser pelo menos 3 \* [**ID3DXBaseMesh:: GetNumFaces**](id3dxbasemesh--getnumfaces.md) \* sizeof (DWORD).

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se o método for bem sucedido, o valor de retorno será D3D \_ OK. Se o método falhar, o valor de retorno poderá ser um dos seguintes: D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|----------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Confira também

<dl> <dt>

[ID3DXBaseMesh](id3dxbasemesh.md)
</dt> </dl>

 

 
