---
description: Converte informações de adjacência de malha em uma matriz de representantes de ponto.
ms.assetid: b8914f9c-8550-498d-813d-bb1afe0fb5b2
title: 'Método ID3DXBaseMesh:: ConvertAdjacencyToPointReps (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseMesh.ConvertAdjacencyToPointReps
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 3a4827473cce115f742a85b99732d09a2c5efa4e
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104172977"
---
# <a name="id3dxbasemeshconvertadjacencytopointreps-method"></a>Método ID3DXBaseMesh:: ConvertAdjacencyToPointReps

Converte informações de adjacência de malha em uma matriz de representantes de ponto.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT ConvertAdjacencyToPointReps(
  [in]      const DWORD *pAdjacency,
  [in, out]       DWORD *pPRep
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pAdjacency* \[ no\]
</dt> <dd>

Tipo: **const [**DWORD**](../winprog/windows-data-types.md) \***

Ponteiro para uma matriz de três DWORDs por face que especificam os três vizinhos para cada face na malha. O número de bytes nessa matriz deve ser pelo menos 3 \* [**ID3DXBaseMesh:: GetNumFaces**](id3dxbasemesh--getnumfaces.md) \* sizeof (DWORD).

</dd> <dt>

*pPRep* \[ entrada, saída\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)\***

Ponteiro para uma matriz de um DWORD por vértice da malha que será preenchida com dados representativos de ponto.

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

 

 
