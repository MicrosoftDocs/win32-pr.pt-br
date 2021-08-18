---
description: Faça o software em uma matriz de vértices.
ms.assetid: 6c1a713f-4ae7-4ee2-afa6-079dd8354fe7
title: Método ID3DX10SkinInfo::D oSoftwareSkinning (D3DX10.h)
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
ms.openlocfilehash: 20f68f51d6886d53d74cd31691e52c362c60d2bf9be2beb0656564cb20fcb80a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119729806"
---
# <a name="id3dx10skininfodosoftwareskinning-method"></a>Método ID3DX10SkinInfo::D oSoftwareSkinning

Faça o software em uma matriz de vértices.

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

*StartVertex* \[ Em\]
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

Um índice baseado em 0 em pSrcVertices.

</dd> <dt>

*VertexCount* \[ Em\]
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

Número de vértices a transformar.

</dd> <dt>

*pSrcVertices* \[ Em\]
</dt> <dd>

Tipo: **\* void**

Ponteiro para uma matriz de vértices a transformar.

</dd> <dt>

*SrcStride* \[ Em\]
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

O tamanho, em bytes, de um vértice em pSrcVertices.

</dd> <dt>

*pDestVertices* \[ in, out\]
</dt> <dd>

Tipo: **\* void**

Ponteiro para uma matriz de vértices, que será preenchida com os vértices transformados.

</dd> <dt>

*DestStride* \[ Em\]
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

O tamanho, em bytes, de um vértice em pDestVertices.

</dd> <dt>

*pBoneMatrices* \[ Em\]
</dt> <dd>

Tipo: **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***

Uma matriz de matrizes que será usada para transformar os pontos mapeados para cada olho, de modo que os vértices mapeados para o i serão transformados por \[ \] pBoneMatrices \[ i \] . Essa matriz será usada para transformar as matrizes somente se o valor IsNormal em pChannelDescs for definido como **FALSE,** caso contrário, pInverseTransposeBoneMatrices será usado.

</dd> <dt>

*pInverseTransposeBoneMatrices* \[ Em\]
</dt> <dd>

Tipo: **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***

Se esse valor for **NULL,** ele será definido como pBoneMatrices. Essa matriz de matrizes será usada para transformar os vértices somente se o valor IsNormal em pChannelDescs for definido como **TRUE,** caso contrário, pBoneMatrices será usado.

</dd> <dt>

*pChannelDescs* \[ Em\]
</dt> <dd>

Tipo: **[ **CANAL DE REAÇÃO \_ \_ D3DX10**](d3dx10-skinning-channel.md)\***

Ponteiro para uma estrutura D3DX10 CANAL DE PARTIDA, que determina o membro da decl de vértice em que a distribuição de \_ \_ software será feita.

</dd> <dt>

*NumChannels* \[ Em\]
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

O número de estruturas D3DX10 \_ CANAL DE PARTIDA EM \_ PChannelDescs.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se o método for bem-sucedido, o valor de retorno será S \_ OK. Se o método falhar, o valor de retorno poderá ser: E \_ INVALIDARG.

## <a name="remarks"></a>Comentários

Aqui está um exemplo de como usar o software de programação:


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
| parâmetro<br/>  | <dl> <dt>D3DX10.h</dt> </dl>   |
| Biblioteca<br/> | <dl> <dt>D3DX10.lib</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[ID3DX10SkinInfo](id3dx10skininfo.md)
</dt> <dt>

[D3DX Interfaces](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
