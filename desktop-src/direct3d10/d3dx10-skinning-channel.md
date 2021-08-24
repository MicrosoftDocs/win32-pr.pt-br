---
description: O membro da decl de vértice para fazer a criação de software. Isso é usado com a API ID3DX10SkinInfo::D oSoftwareSkinning.
ms.assetid: 67c817cd-ce78-4e8b-bdc3-7c4d6670dee1
title: D3DX10_SKINNING_CHANNEL (D3DX10.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10_SKINNING_CHANNEL
api_type:
- HeaderDef
api_location:
- D3DX10.h
ms.openlocfilehash: b8e976ba1aecdeb792ba45fc4f60f25e7feb5a7dde3f7fc845a22962e441bf2b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119753526"
---
# <a name="d3dx10_skinning_channel-structure"></a>Estrutura D3DX10 \_ CANAL DE PARTIDA \_

O membro da decl de vértice para fazer a criação de software. Isso é usado com a API [**ID3DX10SkinInfo::D oSoftwareSkinning.**](id3dx10skininfo-dosoftwareskinning.md)

## <a name="syntax"></a>Sintaxe


```C++
typedef struct D3DX10_SKINNING_CHANNEL {
  UINT SrcOffset;
  UINT DestOffset;
  BOOL IsNormal;
} D3DX10_SKINNING_CHANNEL, *LPD3DX10_SKINNING_CHANNEL;
```



## <a name="members"></a>Membros

<dl> <dt>

**Srcoffset**
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

</dd> <dd>

Deslocamento do início de cada vértice de origem.

</dd> <dt>

**DestOffset**
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

</dd> <dd>

Deslocamento do início de cada vértice de destino.

</dd> <dt>

**IsNormal**
</dt> <dd>

Tipo: **[ **BOOL**](../winprog/windows-data-types.md)**

</dd> <dd>

Determina qual matriz de matrizes usar na API [**ID3DX10SkinInfo::D oSoftwareSkinning.**](id3dx10skininfo-dosoftwareskinning.md) Se isso for verdadeiro, *o pInverseTransposeBoneMatrices* será usado, caso *contrário, pBoneMatrices* será usado.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|-------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>D3DX10.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Estruturas D3DX](d3d10-graphics-reference-d3dx10-structures.md)
</dt> </dl>

 

 
