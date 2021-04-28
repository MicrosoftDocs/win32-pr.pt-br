---
description: 'Método ID3DXConstantTable:: getconstant – Obtém uma constante pesquisando seu índice.'
ms.assetid: 7db25171-9bda-4db8-b6a8-8a4d60a842f7
title: 'Método ID3DXConstantTable:: getconstant (D3DX9Shader. h)'
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
ms.openlocfilehash: 664a1b1a214b49eb731a3a0766a255e5f5acadd9
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108115264"
---
# <a name="id3dxconstanttablegetconstant-method"></a>Método ID3DXConstantTable:: getconstant

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

*hConstant* \[ no\]
</dt> <dd>

Tipo: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**

Identificador exclusivo para a estrutura de dados pai. Se a constante for um parâmetro de nível superior (não há nenhuma estrutura de dados pai), use **NULL**.

</dd> <dt>

*Índice* \[ do no\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

Índice de base zero da constante.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Tipo: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**

Retorna um identificador exclusivo para a constante.

## <a name="remarks"></a>Comentários

Para obter uma constante de uma matriz de constantes, use [**ID3DXConstantTable:: Getconstantelement**](id3dxconstanttable--getconstantelement.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3DX9Shader. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9. lib</dt> </dl>     |



## <a name="see-also"></a>Consulte também

<dl> <dt>

[ID3DXConstantTable](id3dxconstanttable.md)
</dt> </dl>

 

 
