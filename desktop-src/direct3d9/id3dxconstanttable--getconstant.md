---
description: Método ID3DXConstantTable::GetConstant – obtém uma constante procurando seu índice.
ms.assetid: 7db25171-9bda-4db8-b6a8-8a4d60a842f7
title: Método ID3DXConstantTable::GetConstant (D3DX9Shader.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXConstantTable.GetConstant
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 2d4c2e268e456f1e4462b033a046ce71f10a8e854e377e4d4104ee5abde3accc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119748876"
---
# <a name="id3dxconstanttablegetconstant-method"></a>Método ID3DXConstantTable::GetConstant

Obtém uma constante procurando seu índice.

## <a name="syntax"></a>Sintaxe


```C++
D3DXHANDLE GetConstant(
  [in] D3DXHANDLE hConstant,
  [in] UINT       Index
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*hConstant* \[ Em\]
</dt> <dd>

Tipo: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**

Identificador exclusivo para a estrutura de dados pai. Se a constante for um parâmetro de nível superior (não há nenhuma estrutura de dados pai), use **NULL.**

</dd> <dt>

*Índice* \[ Em\]
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

Índice baseado em zero da constante.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Tipo: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**

Retorna um identificador exclusivo para a constante.

## <a name="remarks"></a>Comentários

Para obter uma constante de uma matriz de constantes, use [**ID3DXConstantTable::GetConstantElement**](id3dxconstanttable--getconstantelement.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3DX9Shader.h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9.lib</dt> </dl>     |



## <a name="see-also"></a>Confira também

<dl> <dt>

[ID3DXConstantTable](id3dxconstanttable.md)
</dt> </dl>

 

 
