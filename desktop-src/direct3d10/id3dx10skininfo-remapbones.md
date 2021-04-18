---
description: Altere quais Bones influenciam quais vértices.
ms.assetid: 0955e0ba-ffc5-408b-ab38-2abd39e1c429
title: 'Método ID3DX10SkinInfo:: RemapBones (D3DX10. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10SkinInfo.RemapBones
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 238e4628740fa74e055312c82de2635316f5bde5
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105793691"
---
# <a name="id3dx10skininforemapbones-method"></a>Método ID3DX10SkinInfo:: RemapBones

Altere quais Bones influenciam quais vértices.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT RemapBones(
  [in] UINT NewBoneCount,
  [in] UINT *pBoneRemap
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*NewBoneCount* \[ no\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

O novo número de Bones.

</dd> <dt>

*pBoneRemap* \[ no\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)\***

Um ponteiro para uma matriz de índices Bone, que descrevem o remapeamento. Por exemplo, digamos que SkinInfo contenha alguns Bones de modo que bone0 seja mapeado para V0, bone1 para v1 e bone2 para v2, e matriz com 2, 1, 0 seja especificado para pBoneRemap. Isso fará com que bone0 seja mapeado para v2, bone1 para v1 e bone2 para V0.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se o método for bem sucedido, o valor de retorno será S \_ OK. Se o método falhar, o valor de retorno poderá ser: E \_ OUTOFMEMORY ou E \_ INVALIDARG.

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

 

 
