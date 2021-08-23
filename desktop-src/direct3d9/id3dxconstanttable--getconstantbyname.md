---
description: Método ID3DXConstantTable::GetConstantByName – obtém uma constante procurando seu nome.
ms.assetid: 785a2d4f-6391-4419-a0b8-d8244a03ceae
title: Método ID3DXConstantTable::GetConstantByName (D3DX9Shader.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXConstantTable.GetConstantByName
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 25458c14ee4d1d78388edb072fd80061778902e8cca476beaf7071c5f59aea9c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119675576"
---
# <a name="id3dxconstanttablegetconstantbyname-method"></a>Método ID3DXConstantTable::GetConstantByName

Obtém uma constante procurando seu nome.

## <a name="syntax"></a>Sintaxe


```C++
D3DXHANDLE GetConstantByName(
  [in] D3DXHANDLE hConstant,
  [in] LPCSTR     pName
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*hConstant* \[ Em\]
</dt> <dd>

Tipo: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**

Identificador exclusivo para a estrutura de dados pai. Se a constante for um parâmetro de nível superior (não há nenhuma estrutura de dados pai), use **NULL.**

</dd> <dt>

*pName* \[ Em\]
</dt> <dd>

Tipo: **[ **LPCSTR**](../winprog/windows-data-types.md)**

Nome da constante.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Tipo: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**

Retorna um identificador exclusivo para a constante.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3DX9Shader.h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9.lib</dt> </dl>     |



## <a name="see-also"></a>Confira também

<dl> <dt>

[ID3DXConstantTable](id3dxconstanttable.md)
</dt> </dl>

 

 
