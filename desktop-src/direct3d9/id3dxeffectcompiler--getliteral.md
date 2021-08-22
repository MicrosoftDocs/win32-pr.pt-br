---
description: Obtém um status literal de um parâmetro. Um parâmetro literal tem um valor que não muda durante o tempo de vida de um efeito.
ms.assetid: 417abbee-5193-462e-b0d1-b4928ad0a041
title: Método ID3DXEffectCompiler::GetLiteral (D3DX9Shader.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXEffectCompiler.GetLiteral
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: d5c4fcb9b4eb3ee102d4e0676985945cfa227aa35cbd939c8dcd5b8d51da4826
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119493936"
---
# <a name="id3dxeffectcompilergetliteral-method"></a>Método ID3DXEffectCompiler::GetLiteral

Obtém um status literal de um parâmetro. Um parâmetro literal tem um valor que não muda durante o tempo de vida de um efeito.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT GetLiteral(
  [in]  D3DXHANDLE hParameter,
  [out] BOOL       *pLiteral
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*hParameter* \[ Em\]
</dt> <dd>

Tipo: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**

Identificador exclusivo para um parâmetro. Consulte [Handles (Direct3D 9)](handles.md).

</dd> <dt>

*pLiteral* \[ out\]
</dt> <dd>

Tipo: **[ **BOOL**](../winprog/windows-data-types.md)\***

Retornará True se o parâmetro for um literal e False caso contrário.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se o método for bem-sucedido, o valor de retorno será D3D \_ OK. Se o método falhar, o valor de retorno poderá ser D3DERR \_ INVALIDCALL.

## <a name="remarks"></a>Comentários

Esses métodos só mudam se o parâmetro é um literal ou não. Para alterar o valor de um parâmetro, use um método como [**ID3DXBaseEffect::SetBool**](id3dxbaseeffect--setbool.md) ou [**ID3DXBaseEffect::SetValue**](id3dxbaseeffect--setvalue.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3DX9Shader.h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9.lib</dt> </dl>     |



## <a name="see-also"></a>Confira também

<dl> <dt>

[ID3DXEffectCompiler](id3dxeffectcompiler.md)
</dt> <dt>

[Usos e literais (Direct3D 9)](usages-and-literals.md)
</dt> <dt>

[**ID3DXEffectCompiler::SetLiteral**](id3dxeffectcompiler--setliteral.md)
</dt> </dl>

 

 
