---
description: O membro da decl de vértice para fazer a subaparência do software. Isso é usado com a API ID3DX10SkinInfo::D oSoftwareSkinning.
ms.assetid: 67c817cd-ce78-4e8b-bdc3-7c4d6670dee1
title: Estrutura de D3DX10_SKINNING_CHANNEL (D3DX10. h)
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
ms.openlocfilehash: 79f5807dc2539d770d3caa41bddf7aa4960ce682
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104173062"
---
# <a name="d3dx10_skinning_channel-structure"></a>Estrutura de canal de D3DX10 de \_ aparência \_

O membro da decl de vértice para fazer a subaparência do software. Isso é usado com a API [**ID3DX10SkinInfo::D osoftwareskinning**](id3dx10skininfo-dosoftwareskinning.md) .

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

**SrcOffset**
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

</dd> <dd>

Deslocamento do início de cada vértice de origem.

</dd> <dt>

**DestOffset**
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

</dd> <dd>

Deslocamento do início de cada vértice de destino.

</dd> <dt>

**IsNormal**
</dt> <dd>

Tipo: **[ **bool**](../winprog/windows-data-types.md)**

</dd> <dd>

Determina qual matriz de matrizes usar na API [**ID3DX10SkinInfo::D osoftwareskinning**](id3dx10skininfo-dosoftwareskinning.md) . Se for true, o *pInverseTransposeBoneMatrices* será usado; caso contrário, *pBoneMatrices* será usado.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|-------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>D3DX10. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Estruturas D3DX](d3d10-graphics-reference-d3dx10-structures.md)
</dt> </dl>

 

 
