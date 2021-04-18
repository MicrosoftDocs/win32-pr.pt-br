---
description: Desenha uma faixa de linha no espaço da tela com uma matriz de transformação de entrada especificada.
ms.assetid: 869dc705-8162-4cd9-ac6a-c0ce32f430c3
title: 'ID3DXLine: método rawTransform de:D (D3dx9core. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXLine.DrawTransform
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 52407a8c92e626f8fe4d2df817017f81806cbae9
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105763980"
---
# <a name="id3dxlinedrawtransform-method"></a>ID3DXLine: método rawTransform de:D

Desenha uma faixa de linha no espaço da tela com uma matriz de transformação de entrada especificada.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT DrawTransform(
  [in] const D3DXVECTOR3 *pVertexList,
  [in]       DWORD       dwVertexListCount,
  [in] const D3DXMATRIX  *pTransform,
  [in]       D3DCOLOR    Color
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pVertexList* \[ no\]
</dt> <dd>

Tipo: **const [**D3DXVECTOR3**](d3dxvector3.md) \***

Matriz de vértices que compõem a linha. Consulte [**D3DXVECTOR3**](d3dxvector3.md).

</dd> <dt>

*dwVertexListCount* \[ no\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

Número de vértices na lista de vértices.

</dd> <dt>

*pTransform* \[ no\]
</dt> <dd>

Tipo: **const [**D3DXMATRIX**](d3dxmatrix.md) \***

Uma matriz de tamanho, rotação e conversão (SRT) para transformar os pontos. Consulte [**D3DXMATRIX**](d3dxmatrix.md). Se essa matriz for uma matriz de projeção, todas as linhas stippled serão desenhadas com um padrão stippling de perspectiva correta. Ou, você pode transformar os vértices e usar [**ID3DXLine::D RAW**](id3dxline--draw.md) para desenhar a linha com um padrão de Stipple que não seja de perspectiva correta.

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

 

 
