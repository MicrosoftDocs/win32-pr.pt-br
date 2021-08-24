---
description: Os aplicativos usam os métodos da interface ID3DXSkinInfo para manipular matrizes Bone, que são usadas para a capa de dados de vértice para animação. Essa interface não está mais estritamente ligada a ID3DXMesh e pode ser usada para aplicar uma capa a qualquer conjunto de dados de vértice.
ms.assetid: 4ccf88b0-2cc7-4e91-a0f2-fb8eea66a3ce
title: Interface ID3DXSkinInfo (D3DX9Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXSkinInfo
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 0d7bfeddb5cb34bb9b5d0372f424c40248f06e55fa7263e1e884e71fb82dafcb
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119727756"
---
# <a name="id3dxskininfo-interface"></a>Interface ID3DXSkinInfo

Os aplicativos usam os métodos da interface ID3DXSkinInfo para manipular matrizes Bone, que são usadas para a capa de dados de vértice para animação. Essa interface não está mais estritamente ligada a [**ID3DXMesh**](id3dxmesh.md) e pode ser usada para aplicar uma capa a qualquer conjunto de dados de vértice.

## <a name="members"></a>Membros

A interface **ID3DXSkinInfo** herda da interface [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) . **ID3DXSkinInfo** também tem estes tipos de membros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

A interface **ID3DXSkinInfo** tem esses métodos.



| Método                                                                              | Descrição                                                                                                                                                                                    |
|:------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Clone**](id3dxskininfo--clone.md)                                               | Clona um objeto de informações de capa.<br/>                                                                                                                                                          |
| [**ConvertToBlendedMesh**](id3dxskininfo--converttoblendedmesh.md)                 | Usa uma malha e retorna uma nova malha com pesos de mistura por vértice e uma tabela de combinação de Bone. A tabela descreve quais Bones afetam quais subconjuntos da malha.<br/>                   |
| [**ConvertToIndexedBlendedMesh**](id3dxskininfo--converttoindexedblendedmesh.md)   | Usa uma malha e retorna uma nova malha com pesos de mistura por vértice, índices e uma tabela de combinação de Bone. A tabela descreve quais paletas de Bone afetam quais subconjuntos da malha.<br/> |
| [**FindBoneVertexInfluenceIndex**](id3dxskininfo--findbonevertexinfluenceindex.md) | Recupera o índice da influência do Bone que afeta um único vértice.<br/>                                                                                                                |
| [**GetBoneInfluence**](id3dxskininfo--getboneinfluence.md)                         | Obtém os vértices e os pesos que um Bone influencia.<br/>                                                                                                                               |
| [**Getbonename**](id3dxskininfo--getbonename.md)                                   | Obtém o nome do Bone, do índice Bone.<br/>                                                                                                                                            |
| [**GetBoneOffsetMatrix**](id3dxskininfo--getboneoffsetmatrix.md)                   | Obtém a matriz de deslocamento do Bone.<br/>                                                                                                                                                        |
| [**GetBoneVertexInfluence**](id3dxskininfo--getbonevertexinfluence.md)             | Recupera o fator de mistura e o vértice afetados por uma influência de Bone especificada.<br/>                                                                                                       |
| [**Getdeclaration**](id3dxskininfo--getdeclaration.md)                             | Obtém a declaração de vértice.<br/>                                                                                                                                                        |
| [**GetFVF**](id3dxskininfo--getfvf.md)                                             | Obtém o valor de vértice da função fixa.<br/>                                                                                                                                               |
| [**GetMaxFaceInfluences**](id3dxskininfo--getmaxfaceinfluences.md)                 | Obtém o número máximo de influências em uma malha de triângulos com o buffer de índice especificado.<br/>                                                                                                |
| [**GetMaxVertexInfluences**](id3dxskininfo--getmaxvertexinfluences.md)             | Obtém o número máximo de influências para qualquer vértice na malha.<br/>                                                                                                                   |
| [**GetMinBoneInfluence**](id3dxskininfo--getminboneinfluence.md)                   | Obtém a influência mínima do Bone. Influenciar valores menores do que isso é ignorado.<br/>                                                                                                    |
| [**GetNumBoneInfluences**](id3dxskininfo--getnumboneinfluences.md)                 | Obtém o número de influências para um Bone.<br/>                                                                                                                                           |
| [**GetNumBones**](id3dxskininfo--getnumbones.md)                                   | Obtém o número de Bones.<br/>                                                                                                                                                           |
| [**Conseguem**](id3dxskininfo--remap.md)                                               | Atualiza informações de influência de Bone para corresponder os vértices depois que eles são reordenados. Esse método deve ser chamado se o buffer de vértice de destino tiver sido reordenado externamente.<br/>              |
| [**SetBoneInfluence**](id3dxskininfo--setboneinfluence.md)                         | Define o valor de influência para um Bone.<br/>                                                                                                                                                |
| [**Setbonename**](id3dxskininfo--setbonename.md)                                   | Define o nome do Bone.<br/>                                                                                                                                                                 |
| [**SetBoneOffsetMatrix**](id3dxskininfo--setboneoffsetmatrix.md)                   | Define a matriz de deslocamento do Bone.<br/>                                                                                                                                                        |
| [**SetBoneVertexInfluence**](id3dxskininfo--setbonevertexinfluence.md)             | Define um valor de influência de um Bone em um único vértice.<br/>                                                                                                                               |
| [**Setdeclaration**](id3dxskininfo--setdeclaration.md)                             | Define a declaração de vértice.<br/>                                                                                                                                                        |
| [**SetFVF**](id3dxskininfo--setfvf.md)                                             | Define o tipo de formato de vértice flexível (FVF).<br/>                                                                                                                                         |
| [**SetMinBoneInfluence**](id3dxskininfo--setminboneinfluence.md)                   | Define a influência mínima do Bone. Influenciar valores menores do que isso é ignorado.<br/>                                                                                                    |
| [**UpdateSkinnedMesh**](id3dxskininfo--updateskinnedmesh.md)                       | Aplica a procapação de software aos vértices de destino com base nas matrizes atuais.<br/>                                                                                                     |



 

## <a name="remarks"></a>Comentários

Crie uma interface **ID3DXSkinInfo** com [**D3DXCreateSkinInfo**](d3dxcreateskininfo.md), [**D3DXCreateSkinInfoFromBlendedMesh**](d3dxcreateskininfofromblendedmesh.md)ou [**D3DXCreateSkinInfoFVF**](d3dxcreateskininfofvf.md).

O tipo LPD3DXSKININFO é definido como um ponteiro para a interface **ID3DXSkinInfo** .


```
typedef struct ID3DXSkinInfo *LPD3DXSKININFO;
```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|----------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Interfaces D3DX](dx9-graphics-reference-d3dx-interfaces.md)
</dt> </dl>

 

 
