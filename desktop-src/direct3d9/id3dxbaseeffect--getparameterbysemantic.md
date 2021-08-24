---
description: Obtém o identificador de um parâmetro de nível superior ou um parâmetro de membro de estrutura pesquisando sua semântica com uma pesquisa que não diferencia maiúsculas de minúsculas.
ms.assetid: 3de3791a-fe09-4a39-bd6f-0e20a641dd32
title: 'Método ID3DXBaseEffect:: GetParameterBySemantic (D3DX9Shader. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseEffect.GetParameterBySemantic
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: fa00ef4585462f068e95fcefca8332acd46930efaf1bb1c108a471511ab63eb4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119791006"
---
# <a name="id3dxbaseeffectgetparameterbysemantic-method"></a>Método ID3DXBaseEffect:: GetParameterBySemantic

Obtém o identificador de um parâmetro de nível superior ou um parâmetro de membro de estrutura pesquisando sua semântica com uma pesquisa que não diferencia maiúsculas de minúsculas.

## <a name="syntax"></a>Sintaxe


```C++
D3DXHANDLE GetParameterBySemantic(
  [in] D3DXHANDLE hParameter,
  [in] LPCSTR     pSemantic
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*hParameter* \[ no\]
</dt> <dd>

Tipo: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**

Identificador do parâmetro ou **nulo** para parâmetros de nível superior. Consulte [Handles (Direct3D 9)](handles.md).

</dd> <dt>

*pSemantic* \[ no\]
</dt> <dd>

Tipo: **[ **LPCSTR**](../winprog/windows-data-types.md)**

Cadeia de caracteres que contém o nome semântico.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Tipo: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**

Retorna o identificador do primeiro parâmetro que corresponde à semântica especificada ou **NULL** se a semântica não foi encontrada. Consulte [Handles (Direct3D 9)](handles.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3DX9Shader. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9. lib</dt> </dl>     |



## <a name="see-also"></a>Confira também

<dl> <dt>

[ID3DXBaseEffect](id3dxbaseeffect.md)
</dt> </dl>

 

 
