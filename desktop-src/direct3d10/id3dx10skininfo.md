---
description: O ID3DX10SkinInfo permite otimizar, processar e definir manualmente a relação entre os Bones e os vértices em suas malhas (consulte a animação estrutural na Wikipédia).
ms.assetid: bea0fe71-c201-45c6-8036-d0d76d5851fd
title: Interface ID3DX10SkinInfo (D3DX10. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10SkinInfo
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 3216765ab9ef2ba9f2b0883c31a878a7eae6861f
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104298635"
---
# <a name="id3dx10skininfo-interface"></a>Interface ID3DX10SkinInfo

O ID3DX10SkinInfo permite otimizar, processar e definir manualmente a relação entre os Bones e os vértices em suas malhas (consulte a [animação estrutural na Wikipédia](https://en.wikipedia.org/wiki/Skeletal_animation)). Ele é mais útil para fazer arquivos. x exportados por aplicativos DCC (como 3DS Max e Maya) mais amigáveis para hardware e para melhorar a velocidade de renderização de suas malhas subcapadas no modo de processamento de software.

## <a name="members"></a>Membros

A interface **ID3DX10SkinInfo** herda da interface [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) . **ID3DX10SkinInfo** também tem estes tipos de membros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

A interface **ID3DX10SkinInfo** tem esses métodos.



| Método                                                                   | Descrição                                                                                                                        |
|:-------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------|
| [**AddBoneInfluences**](id3dx10skininfo-addboneinfluences.md)           | Habilite um Bone existente para influenciar um grupo de vértices e definir quanto influência o Bone tem em cada vértice.<br/>     |
| [**Addbones**](id3dx10skininfo-addbones.md)                             | Aloque espaço para mais Bones.<br/>                                                                                          |
| [**Addvértices**](id3dx10skininfo-addvertices.md)                       | Aloque espaço para vértices adicionais.<br/>                                                                                 |
| [**ClearBoneInfluences**](id3dx10skininfo-clearboneinfluences.md)       | Desmarque a lista de vértices de um Bone que ele influencia.<br/>                                                                     |
| [**Compacto**](id3dx10skininfo-compact.md)                               | Limitar o número de Bones que podem influenciar um vértice e/ou limitar a quantidade de influência que um Bone pode ter em um vértice.<br/> |
| [**DoSoftwareSkinning**](id3dx10skininfo-dosoftwareskinning.md)         | Faça a subaparência do software em uma matriz de vértices.<br/>                                                                           |
| [**FindBoneInfluenceIndex**](id3dx10skininfo-findboneinfluenceindex.md) | Localize o índice que indica onde um determinado vértice está em uma determinada lista de vértices influenciados.<br/>                    |
| [**GetBoneInfluence**](id3dx10skininfo-getboneinfluence.md)             | Obter a quantidade de influência que um determinado Bone tem sobre um determinado vértice.<br/>                                                       |
| [**GetBoneInfluenceCount**](id3dx10skininfo-getboneinfluencecount.md)   | Obter o número de vértices que um determinado Bone influencia.<br/>                                                                |
| [**GetBoneInfluences**](id3dx10skininfo-getboneinfluences.md)           | Obtenha uma lista de vértices que um determinado Bone influencia e uma lista da quantidade de influência que o Bone tem em cada vértice.<br/> |
| [**GetMaxBoneInfluences**](id3dx10skininfo-getmaxboneinfluences.md)     | Obter o número de vértices que um Bone pode influenciar de uma influência.<br/>                                                              |
| [**GetNumBones**](id3dx10skininfo-getnumbones.md)                       | Obtenha o número de Bones em ID3DX10SkinInfo.<br/>                                                                             |
| [**GetNumVertices**](id3dx10skininfo-getnumvertices.md)                 | Obtenha o número de vértices em ID3DX10SkinInfo.<br/>                                                                          |
| [**RemapBones**](id3dx10skininfo-remapbones.md)                         | Altere quais Bones influenciam quais vértices.<br/>                                                                            |
| [**RemapVertices**](id3dx10skininfo-remapvertices.md)                   | Altere quais vértices são influenciados por quais Bones.<br/>                                                                    |
| [**RemoveBone**](id3dx10skininfo-removebone.md)                         | Remover um Bone.<br/>                                                                                                          |
| [**SetBoneInfluence**](id3dx10skininfo-setboneinfluence.md)             | Defina a quantidade de influência que um determinado Bone tem sobre um determinado vértice.<br/>                                                       |



 

## <a name="remarks"></a>Comentários

Crie uma interface ID3DX10SkinInfo com [**D3DX10CreateSkinInfo**](d3d10-d3dx10createskininfo.md), **D3DX10CreateSkinInfoFromBlendedMesh** ou **D3DX10CreateSkinInfoFVF**.

O tipo LPD3DX10SKININFO é definido como um ponteiro para a interface **ID3DX10SkinInfo** .


```
typedef struct ID3DX10SkinInfo *LPD3DX10SKININFO;
```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|---------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3DX10. h</dt> </dl>   |
| Biblioteca<br/> | <dl> <dt>D3DX10. lib</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Interfaces D3DX](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
