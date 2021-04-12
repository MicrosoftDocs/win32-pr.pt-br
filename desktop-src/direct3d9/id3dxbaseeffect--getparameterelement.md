---
description: Obtenha o identificador de um parâmetro de elemento de matriz.
ms.assetid: fe8edbc5-dc1d-4386-8149-489541d55bde
title: 'Método ID3DXBaseEffect:: ParameterElement (D3DX9Shader. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseEffect.GetParameterElement
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 5130ccf57634f9b1a569a1dd70833fe2014e1a74
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104298824"
---
# <a name="id3dxbaseeffectgetparameterelement-method"></a>Método ID3DXBaseEffect:: ParameterElement

Obtenha o identificador de um parâmetro de elemento de matriz.

## <a name="syntax"></a>Sintaxe


```C++
D3DXHANDLE GetParameterElement(
  [in] D3DXHANDLE hParameter,
  [in] UINT       ElementIndex
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*hParameter* \[ no\]
</dt> <dd>

Tipo: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**

Identificador da matriz. Consulte [Handles (Direct3D 9)](handles.md).

</dd> <dt>

*ElementIndex* \[ no\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

Índice de elemento de matriz.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Tipo: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**

Retorna o identificador do parâmetro especificado ou **NULL** se HParameter ou ElementIndex for inválido. Consulte [Handles (Direct3D 9)](handles.md).

## <a name="remarks"></a>Comentários

Esse método é usado para obter um elemento de um parâmetro que é uma matriz.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3DX9Shader. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9. lib</dt> </dl>     |



## <a name="see-also"></a>Confira também

<dl> <dt>

[ID3DXBaseEffect](id3dxbaseeffect.md)
</dt> </dl>

 

 
