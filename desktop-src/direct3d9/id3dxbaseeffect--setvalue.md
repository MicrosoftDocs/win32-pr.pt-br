---
description: Defina o valor de um parâmetro ou anotação arbitrária, incluindo tipos simples, structs, matrizes, cadeias de caracteres, sombreadores e texturas.
ms.assetid: ab71f1a1-3e10-4883-99b4-607e0b5751c2
title: 'Método ID3DXBaseEffect:: SetValue (D3DX9Shader. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseEffect.SetValue
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 3281306240cefc0312ff9a2af7e056dab74a085b
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104091981"
---
# <a name="id3dxbaseeffectsetvalue-method"></a>Método ID3DXBaseEffect:: SetValue

Defina o valor de um parâmetro ou anotação arbitrária, incluindo tipos simples, structs, matrizes, cadeias de caracteres, sombreadores e texturas.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT SetValue(
  [in] D3DXHANDLE hParameter,
  [in] LPCVOID    pData,
  [in] UINT       Bytes
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*hParameter* \[ no\]
</dt> <dd>

Tipo: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**

Identificador exclusivo. Consulte [Handles (Direct3D 9)](handles.md).

</dd> <dt>

*pData* \[ no\]
</dt> <dd>

Tipo: **[ **LPCVOID**](../winprog/windows-data-types.md)**

Ponteiro para um buffer que contém dados.

</dd> <dt>

*Bytes* \[ no\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

\[em \] número de bytes no buffer. Passe D3DX \_ padrão se souber que o buffer é grande o suficiente para conter o parâmetro inteiro e você deseja ignorar a validação de tamanho.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se o método for bem sucedido, o valor de retorno será D3D \_ OK. Se o método falhar, o valor de retorno poderá ser D3DERR \_ INVALIDCALL.

## <a name="remarks"></a>Comentários

Esse método pode ser usado em vez de quase todas as chamadas de API de conjunto de efeitos.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3DX9Shader. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9. lib</dt> </dl>     |



## <a name="see-also"></a>Confira também

<dl> <dt>

[ID3DXBaseEffect](id3dxbaseeffect.md)
</dt> <dt>

[**GetValue**](id3dxbaseeffect--getvalue.md)
</dt> </dl>

 

 
