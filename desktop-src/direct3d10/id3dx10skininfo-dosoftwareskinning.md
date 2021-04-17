---
description: Faça a subaparência do software em uma matriz de vértices.
ms.assetid: 6c1a713f-4ae7-4ee2-afa6-079dd8354fe7
title: 'ID3DX10SkinInfo: método oSoftwareSkinning de:D (D3DX10. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10SkinInfo.DoSoftwareSkinning
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 54dfe909e36be0273e0679a824ff0674b0e3b38c
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105761199"
---
# <a name="id3dx10skininfodosoftwareskinning-method"></a>ID3DX10SkinInfo: método oSoftwareSkinning de:D

Faça a subaparência do software em uma matriz de vértices.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT DoSoftwareSkinning(
  [in]      UINT                    StartVertex,
  [in]      UINT                    VertexCount,
  [in]      void                    *pSrcVertices,
  [in]      UINT                    SrcStride,
  [in, out] void                    *pDestVertices,
  [in]      UINT                    DestStride,
  [in]      D3DXMATRIX              *pBoneMatrices,
  [in]      D3DXMATRIX              *pInverseTransposeBoneMatrices,
  [in]      D3DX10_SKINNING_CHANNEL *pChannelDescs,
  [in]      UINT                    NumChannels
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*StartVertex* \[ no\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

Um índice baseado em 0 em pSrcVertices.

</dd> <dt>

*Contagemdevértice* \[ no\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

Número de vértices para transformar.

</dd> <dt>

*pSrcVertices* \[ no\]
</dt> <dd>

Tipo: **void \***

Ponteiro para uma matriz de vértices para transformar.

</dd> <dt>

*SrcStride* \[ no\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

O tamanho, em bytes, de um vértice em pSrcVertices.

</dd> <dt>

*pDestVertices* \[ entrada, saída\]
</dt> <dd>

Tipo: **void \***

Ponteiro para uma matriz de vértices, que será preenchida com os vértices transformados.

</dd> <dt>

*DestStride* \[ no\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

O tamanho, em bytes, de um vértice em pDestVertices.

</dd> <dt>

*pBoneMatrices* \[ no\]
</dt> <dd>

Tipo: **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***

Uma matriz de matrizes que será usada para transformar os pontos mapeados para cada Bone, de modo que os vértices mapeados para Bone \[ i serão \] transformados por pBoneMatrices \[ i \] . Essa matriz será usada para transformar as matrizes somente se o valor IsNormal em pChannelDescs for definido como **false**; caso contrário, pInverseTransposeBoneMatrices será usado.

</dd> <dt>

*pInverseTransposeBoneMatrices* \[ no\]
</dt> <dd>

Tipo: **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***

Se esse valor for **NULL**, ele será definido como igual a pBoneMatrices. Essa matriz de matrizes será usada para transformar os vértices somente se o valor IsNormal em pChannelDescs for definido como **true**; caso contrário, pBoneMatrices será usado.

</dd> <dt>

*pChannelDescs* \[ no\]
</dt> <dd>

Tipo: **[ **\_ \_ canal de revestimento D3DX10**](d3dx10-skinning-channel.md)\***

Ponteiro para uma \_ estrutura de canal de casca de D3DX10 \_ , que determina o membro da decl Vertex que a subcapa de software será feita em.

</dd> <dt>

*NumChannels* \[ no\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

O número de estruturas de canal de D3DX10 \_ \_ de aparência em pChannelDescs.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se o método for bem sucedido, o valor de retorno será S \_ OK. Se o método falhar, o valor de retorno poderá ser: E \_ INVALIDARG.

## <a name="remarks"></a>Comentários

Aqui está um exemplo de como usar a dicapação de software:


```
//vertex definition
struct MyVertex
{
    D3DXVECTOR3 Position;
    D3DXVECTOR2 Weight;
    D3DXVECTOR2 TexCoord;
};

//create vertex data
const UINT numVertices = 16;
MyVertex vertices[numVertices] = {...};
MyVertex destVertices[numVertices];

//create bone matrices
D3DXMATRIX boneMatrices[2];
D3DXMatrixIdentity(&boneMatrices[0]);
D3DXMatrixRotationX(&boneMatrices[1], 3.14159f / 180.0f);

//create bone indices and weights
UINT boneIndices[numVertices] = {...};
float boneWeights[2][numVertices] = {...};

//create skin info, populate it with bones and vertices, and then map them to each other
ID3DX10SkinInfo *pSkinInfo = NULL;
D3DX10CreateSkinInfo(&pSkinInfo);
pSkinInfo->AddBones(2);
pSkinInfo->AddVertices(numVertices);
pSkinInfo->AddBoneInfluences(0, numVertices, boneIndices, boneWeights[0]);
pSkinInfo->AddBoneInfluences(1, numVertices, boneIndices, boneWeights[1]);

//create channel desc
D3DX10_SKINNING_CHANNEL channelDesc;
channelDesc.SrcOffset = 0;
channelDesc.DestOffset = 0;
channelDesc.IsNormal = FALSE;

//do the skinning
pSkinInfo->DoSoftwareSkinning(0, numVertices,
                              vertices, sizeof(MyVertex), 
                              destVertices, sizeof(MyVertex), 
                              boneMatrices, NULL, 
                              &channelDesc, 1);
```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|---------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3DX10. h</dt> </dl>   |
| Biblioteca<br/> | <dl> <dt>D3DX10. lib</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[ID3DX10SkinInfo](id3dx10skininfo.md)
</dt> <dt>

[Interfaces D3DX](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
