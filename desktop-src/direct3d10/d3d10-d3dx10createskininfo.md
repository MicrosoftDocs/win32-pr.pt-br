---
description: Função D3DX10CreateSkinInfo – cria um objeto de malha de capa vazio usando um Declarador.
ms.assetid: 5356cfe5-de90-462d-9722-72f3618decfb
title: Função D3DX10CreateSkinInfo (D3DX10Mesh. h)
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
ms.openlocfilehash: 17d6ec99d3f43c41d56deebef81a021c81ec1d69
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108103594"
---
# <a name="d3dx10createskininfo-function"></a>Função D3DX10CreateSkinInfo

Cria um objeto de malha de capa vazio usando um Declarador.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT D3DX10CreateSkinInfo(
  _Out_ LPD3DX10SKININFO *ppSkinInfo
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*ppSkinInfo* \[ fora\]
</dt> <dd>

Tipo: **[ **LPD3DX10SKININFO**](id3dx10skininfo.md)\***

Endereço de um ponteiro para uma [**interface ID3DX10SkinInfo**](id3dx10skininfo.md), que representa o objeto de malha de capa criado.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se a função for bem sucedido, o valor de retorno será D3D \_ OK. Se a função falhar, o valor de retorno poderá ser: E \_ OUTOFMEMORY.

## <a name="remarks"></a>Comentários

Use o [**ID3DX10SkinInfo:: SetBoneInfluence**](id3dx10skininfo-setboneinfluence.md) para preencher o objeto de malha de capa vazio retornado por esse método.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|-----------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3DX10Mesh. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3DX10. lib</dt> </dl>   |



## <a name="see-also"></a>Consulte também

<dl> <dt>

[Funções de malha](d3d10-graphics-reference-d3dx10-functions-mesh.md)
</dt> <dt>

[Funções D3DX](d3d10-graphics-reference-d3dx10-functions.md)
</dt> </dl>

 

 




