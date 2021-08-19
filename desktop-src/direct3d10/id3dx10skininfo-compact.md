---
description: Limite o número de esqueletos que podem influenciar um vértice e/ou limitar a quantidade de influência que um dinossauro pode ter em um vértice.
ms.assetid: 75c4d2eb-0a43-494d-9642-4c08aa814794
title: Método ID3DX10SkinInfo::Compact (D3DX10.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10SkinInfo.Compact
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 3aab3534ea55d2f6675ef1e65b03d19f4c516562b242e284ee2865f98bc03f18
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119046904"
---
# <a name="id3dx10skininfocompact-method"></a>Método ID3DX10SkinInfo::Compact

Limite o número de esqueletos que podem influenciar um vértice e/ou limitar a quantidade de influência que um dinossauro pode ter em um vértice.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT Compact(
  [in] UINT  MaxPerVertexInfluences,
  [in] UINT  ScaleMode,
  [in] float MinWeight
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*MaxPerVertexInfluences* \[ Em\]
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

O número máximo de esqueletos que podem influenciar qualquer vértice determinado. Esse valor será ignorado se for maior que o valor retornado por [**ID3DX10SkinInfo::GetMaxBoneInfluences**](id3dx10skininfo-getmaxboneinfluences.md).

</dd> <dt>

*ScaleMode* \[ Em\]
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

Um sinalizador que descreve como dimensionar os pesos restantes em um determinado vértice depois que alguns foram cortados por MinWeight. Se D3DX10 SKININFO NO SCALING for especificado, os \_ \_ \_ pesos não serão dimensionados. Se D3DX10 SKININFO SCALE TO 1 for especificado, os pesos maiores que MinWeight serão escalados para cima para que eles adicionem até \_ \_ \_ \_ 1,0. Se D3DX10 SKININFO SCALE TO TOTAL for especificado, os pesos maiores que MinWeight serão escalados para cima para que sejam somados \_ \_ ao total \_ \_ original.

</dd> <dt>

*MinWeight* \[ Em\]
</dt> <dd>

Tipo: **float**

O percentual mínimo de influência ou peso que qualquer pau pode ter em qualquer vértice. Esse valor deve estar entre 0 e 1.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se o método for bem-sucedido, o valor de retorno será S \_ OK. Se o método falhar, o valor de retorno poderá ser: E \_ OUTOFMEMORY ou E \_ INVALIDARG.

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

 

 
