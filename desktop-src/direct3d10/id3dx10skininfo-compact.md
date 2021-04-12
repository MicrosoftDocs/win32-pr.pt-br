---
description: Limitar o número de Bones que podem influenciar um vértice e/ou limitar a quantidade de influência que um Bone pode ter em um vértice.
ms.assetid: 75c4d2eb-0a43-494d-9642-4c08aa814794
title: 'Método ID3DX10SkinInfo:: Compact (D3DX10. h)'
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
ms.openlocfilehash: 379343688a1fd2ffe5ebd968dc984fa09faada7d
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104370936"
---
# <a name="id3dx10skininfocompact-method"></a>Método ID3DX10SkinInfo:: Compact

Limitar o número de Bones que podem influenciar um vértice e/ou limitar a quantidade de influência que um Bone pode ter em um vértice.

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

*MaxPerVertexInfluences* \[ no\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

O número máximo de Bones que podem influenciar qualquer vértice determinado. Esse valor será ignorado se for maior que o valor retornado por [**ID3DX10SkinInfo:: GetMaxBoneInfluences**](id3dx10skininfo-getmaxboneinfluences.md).

</dd> <dt>

*ScaleMode* \[ no\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

Um sinalizador que descreve como dimensionar os pesos restantes em um determinado vértice depois que alguns foram descortadosdos pelo MinWeight. Se D3DX10 \_ SKININFO \_ nenhum \_ dimensionamento for especificado, os pesos não serão dimensionados. Se D3DX10 \_ SKININFO \_ dimensionar \_ para \_ 1 for especificado, os pesos maiores que MinWeight serão escalados verticalmente para que eles se adicionem até 1,0. Se D3DX10 \_ SKININFO \_ dimensionar \_ para \_ total for especificado, os pesos maiores que MinWeight serão dimensionados para que eles se adicionem ao total original.

</dd> <dt>

*MinWeight* \[ no\]
</dt> <dd>

Tipo: **float**

O percentual mínimo de influência, ou peso, que qualquer Bone pode ter em qualquer vértice. Esse valor deve estar entre 0 e 1.

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

 

 
