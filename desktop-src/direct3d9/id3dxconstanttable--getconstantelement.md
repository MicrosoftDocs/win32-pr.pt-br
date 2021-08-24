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
ms.openlocfilehash: 9cb1adacadb92cf3a2f9a3e041e4a94a840994db3244233509350448008bd675
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119748776"
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

## <a name="return-value"></a>Valor retornado

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

 

 
