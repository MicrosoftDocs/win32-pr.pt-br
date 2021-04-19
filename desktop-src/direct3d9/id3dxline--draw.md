---
description: Desenha uma faixa de linha no espaço da tela. A entrada está na forma de uma matriz que define pontos (de D3DXVECTOR2) na faixa de linha.
ms.assetid: 10ad5af5-fb57-46ef-a89f-7a05dcf58826
title: 'ID3DXLine: método RAW de:D (D3dx9core. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXLine.Draw
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 0a7492fb2128e0d9ec402d5211c20d5569ceb506
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105813438"
---
# <a name="id3dxlinedraw-method"></a>ID3DXLine: método RAW de:D

Desenha uma faixa de linha no espaço da tela. A entrada está na forma de uma matriz que define pontos (de [**D3DXVECTOR2**](d3dxvector2.md)) na faixa de linha.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT Draw(
  [in] const D3DXVECTOR2 *pVertexList,
  [in]       DWORD       dwVertexListCount,
  [in]       D3DCOLOR    Color
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pVertexList* \[ no\]
</dt> <dd>

Tipo: **const [**D3DXVECTOR2**](d3dxvector2.md) \***

Matriz de vértices que compõem a linha. Consulte [**D3DXVECTOR2**](d3dxvector2.md).

</dd> <dt>

*dwVertexListCount* \[ no\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

Número de vértices na lista de vértices.

</dd> <dt>

*Cor* \[ do no\]
</dt> <dd>

Tipo: **[ **D3DCOLOR**](d3dcolor.md)**

Cor da linha. Consulte [**D3DCOLOR**](d3dcolor.md).

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

 

 
