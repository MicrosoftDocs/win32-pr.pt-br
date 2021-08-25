---
description: Calcula os normais de unidade para cada vértice em uma malha. Fornecido para dar suporte a aplicativos herdado. Use D3DXComputeTangentFrameEx para melhores resultados.
ms.assetid: 7c879149-2c4c-4824-9604-e88696cc6ddc
title: Função D3DXComputeNormals (D3DX9Mesh.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXComputeNormals
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: d136e7c3d01b595273127c500ccc52cd310357df2147f3df5d97df9dbd38d38d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120069306"
---
# <a name="d3dxcomputenormals-function"></a>Função D3DXComputeNormals

Calcula os normais de unidade para cada vértice em uma malha. Fornecido para dar suporte a aplicativos herdado. Use [**D3DXComputeTangentFrameEx para**](d3dxcomputetangentframeex.md) melhores resultados.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT D3DXComputeNormals(
  _Inout_       LPD3DXBASEMESH pMesh,
  _In_    const DWORD          *pAdjacency
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pMesh* \[ in, out\]
</dt> <dd>

Tipo: **[ **LPD3DXBASEMESH**](id3dxbasemesh.md)**

Ponteiro para uma [**interface ID3DXBaseMesh,**](id3dxbasemesh.md) representando o objeto de malha normalizado.

</dd> <dt>

*pAdjacency* \[ Em\]
</dt> <dd>

Tipo: **const [**DWORD**](../winprog/windows-data-types.md) \***

Ponteiro para uma matriz de três DWORDs por face que especificam os três vizinhos para cada rosto na malha progressiva criada. Esse parâmetro é opcional e deve ser definido como **NULL** se não for usada.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se a função for bem-sucedida, o valor de retorno será S \_ OK. Se a função falhar, o valor de retorno poderá ser um dos seguintes: D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA, E \_ OUTOFMEMORY.

## <a name="remarks"></a>Comentários

A malha de entrada deve ter o [sinalizador NORMAL D3DFVF \_ especificado](d3dfvf.md) em seu FVF (formato de vértice flexível).

Um normal para um vértice é gerado pela média dos normais de todos os rostos que compartilham esse vértice.

Se a adjacency for fornecida, os vértices replicados serão ignorados e "suavizados". Se a adjacency não for fornecida, os vértices replicados terão a média normal em apenas os rostos referenciando-os explicitamente.

Essa função simplesmente chama [**D3DXComputeTangentFrameEx**](d3dxcomputetangentframeex.md) com os seguintes parâmetros de entrada:


```
D3DXComputeTangentFrameEx( pMesh,
                           D3DX_DEFAULT,
                           0,
                           D3DX_DEFAULT,
                           0,
                           D3DX_DEFAULT,
                           0,
                           D3DDECLUSAGE_NORMAL,
                           0,
                           D3DXTANGENT_GENERATE_IN_PLACE | D3DXTANGENT_CALCULATE_NORMALS,
                           pAdjacency,
                           -1.01f,
                           -0.01f,
                           -1.01f,
                           NULL,
                           NULL);
```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|----------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3DX9Mesh.h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Funções de malha](dx9-graphics-reference-d3dx-functions-mesh.md)
</dt> </dl>

 

 
