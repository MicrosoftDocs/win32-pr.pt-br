---
description: Obtém um ponteiro para a matriz de constantes na tabela constante.
ms.assetid: 2476344b-8433-46bb-9242-dff84e3168e7
title: Método ID3DXTextureShader::GetConstantDesc (D3DX9Shader.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXTextureShader.GetConstantDesc
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: f8c7f65c9f2096339e0131d5d54c2fd65fb7e52849219f06f6a60fd44c518751
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120095666"
---
# <a name="id3dxtextureshadergetconstantdesc-method"></a>Método ID3DXTextureShader::GetConstantDesc

Obtém um ponteiro para a matriz de constantes na tabela constante.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT GetConstantDesc(
  [in]      D3DXHANDLE        hConstant,
  [in, out] D3DXCONSTANT_DESC *pDesc,
  [in, out] UINT              *pCount
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*hConstant* \[ Em\]
</dt> <dd>

Tipo: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**

Identificador exclusivo para uma constante. Consulte [D3DXHANDLE](d3dxfx.md).

</dd> <dt>

*pDesc* \[ in, out\]
</dt> <dd>

Tipo: **[ **D3DXCONSTANT \_ DESC**](d3dxconstant-desc.md)\***

Retorna um ponteiro para uma matriz de descrições. Consulte [**D3DXCONSTANT \_ DESC**](d3dxconstant-desc.md).

</dd> <dt>

*pCount* \[ in, out\]
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)\***

A entrada fornecida deve ser o tamanho máximo da matriz. A saída é o número de elementos que são preenchidos na matriz quando a função retorna.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se o método for bem-sucedido, o valor de retorno será D3D \_ OK. Se o método falhar, o valor de retorno poderá ser um dos seguintes: D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA.

## <a name="remarks"></a>Comentários

Os exemplos podem aparecer mais de uma vez em uma tabela constante, portanto, esse método pode retornar uma matriz de descrições cada uma com um índice de registro diferente.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3DX9Shader.h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9.lib</dt> </dl>     |



## <a name="see-also"></a>Confira também

<dl> <dt>

[ID3DXTextureShader](id3dxtextureshader.md)
</dt> <dt>

[**ID3DXTextureShader::GetDesc**](id3dxtextureshader--getdesc.md)
</dt> </dl>

 

 
