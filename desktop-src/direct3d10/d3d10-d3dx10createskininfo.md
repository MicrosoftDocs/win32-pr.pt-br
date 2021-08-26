---
description: Função D3DX10CreateSkinInfo – cria um objeto de malha de capa vazia usando um declarador.
ms.assetid: 5356cfe5-de90-462d-9722-72f3618decfb
title: Função D3DX10CreateSkinInfo (D3DX10Mesh.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10CreateSkinInfo
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 52a6d1116e46771c4c092fb08f3d59f43277d2437db1bd2c5b750f4a381043fe
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120070186"
---
# <a name="d3dx10createskininfo-function"></a>Função D3DX10CreateSkinInfo

Cria um objeto de malha de capa vazia usando um declarador.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT D3DX10CreateSkinInfo(
  _Out_ LPD3DX10SKININFO *ppSkinInfo
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*ppSkinInfo* \[ out\]
</dt> <dd>

Tipo: **[ **LPD3DX10SKININFO**](id3dx10skininfo.md)\***

Endereço de um ponteiro para uma [**Interface ID3DX10SkinInfo**](id3dx10skininfo.md), que representa o objeto de malha de capa criado.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se a função for bem-sucedida, o valor de retorno será D3D \_ OK. Se a função falhar, o valor de retorno poderá ser: E \_ OUTOFMEMORY.

## <a name="remarks"></a>Comentários

Use [**o ID3DX10SkinInfo::SetBoneInfluence**](id3dx10skininfo-setboneinfluence.md) para preencher o objeto de malha de capa vazia retornado por esse método.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|-----------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3DX10Mesh.h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3DX10.lib</dt> </dl>   |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Funções de malha](d3d10-graphics-reference-d3dx10-functions-mesh.md)
</dt> <dt>

[Funções D3DX](d3d10-graphics-reference-d3dx10-functions.md)
</dt> </dl>

 

 




