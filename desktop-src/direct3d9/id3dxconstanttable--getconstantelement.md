---
description: Obtém uma constante de uma matriz de constantes. Uma matriz é composta de elementos.
ms.assetid: 20a61207-b0e1-455d-9b65-0fade543d1cf
title: 'Método ID3DXConstantTable:: getconstantelement (D3DX9Shader. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXConstantTable.GetConstantElement
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 5396c70c1c4286223d9f45fb8ab9b73a019becb1
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105793836"
---
# <a name="id3dxconstanttablegetconstantelement-method"></a>Método ID3DXConstantTable:: getconstantelement

Obtém uma constante de uma matriz de constantes. Uma matriz é composta de elementos.

## <a name="syntax"></a>Sintaxe


```C++
D3DXHANDLE GetConstantElement(
  [in] D3DXHANDLE hConstant,
  [in] UINT       Index
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*hConstant* \[ no\]
</dt> <dd>

Tipo: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**

Identificador exclusivo para a matriz de constantes. Esse valor não pode ser **nulo**.

</dd> <dt>

*Índice* \[ do no\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

Índice de base zero do elemento na matriz.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Tipo: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**

Retorna um identificador exclusivo para a constante do elemento.

## <a name="remarks"></a>Comentários

Para obter uma constante que não faz parte de uma matriz, use [**ID3DXConstantTable:: getconstant**](id3dxconstanttable--getconstant.md) ou [**ID3DXConstantTable:: GetConstantByName**](id3dxconstanttable--getconstantbyname.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3DX9Shader. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9. lib</dt> </dl>     |



## <a name="see-also"></a>Confira também

<dl> <dt>

[ID3DXConstantTable](id3dxconstanttable.md)
</dt> </dl>

 

 
