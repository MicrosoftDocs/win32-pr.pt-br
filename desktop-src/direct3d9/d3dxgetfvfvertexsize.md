---
description: Retorna o tamanho de um vértice para um FVF (formato de vértice flexível).
ms.assetid: 9d8e2b1f-0ec8-46ab-8492-2cadd700225e
title: Função D3DXGetFVFVertexSize (D3dx9mesh.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXGetFVFVertexSize
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: f00faa489481faf436a30fe6e6313429d446cd8000173131d823442e960b5a08
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120119206"
---
# <a name="d3dxgetfvfvertexsize-function"></a>Função D3DXGetFVFVertexSize

Retorna o tamanho de um vértice para um FVF (formato de vértice flexível).

## <a name="syntax"></a>Sintaxe


```C++
UINT D3DXGetFVFVertexSize(
  _In_ DWORD FVF
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*FVF* \[ Em\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

FVF a ser consultado. Uma combinação de [D3DFVF.](d3dfvf.md)

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

O tamanho do vértice FVF, em bytes.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|----------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3dx9mesh.h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Funções de malha](dx9-graphics-reference-d3dx-functions-mesh.md)
</dt> </dl>

 

 
