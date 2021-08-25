---
description: Retorna o número de elementos na declaração de vértice.
ms.assetid: 3ce24e59-0ec3-4d53-8bc8-8a5a7cdf53b2
title: Função D3DXGetDeclLength (D3DX9Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXGetDeclLength
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: cc6a44c73d9b7127bb382cfbf18587a84d8cc179feabf48da6e29b908204b1a9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119857033"
---
# <a name="d3dxgetdecllength-function"></a>Função D3DXGetDeclLength

Retorna o número de elementos na declaração de vértice.

## <a name="syntax"></a>Sintaxe


```C++
UINT D3DXGetDeclLength(
  _In_ const D3DVERTEXELEMENT9 *pDecl
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pDecl* \[ no\]
</dt> <dd>

Tipo: **const [**D3DVERTEXELEMENT9**](d3dvertexelement9.md) \***

Um ponteiro para a declaração de vértice. Consulte [**D3DVERTEXELEMENT9**](d3dvertexelement9.md).

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

O número de elementos na declaração de vértice.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|----------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Funções de malha](dx9-graphics-reference-d3dx-functions-mesh.md)
</dt> </dl>

 

 
