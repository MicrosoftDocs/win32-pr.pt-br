---
description: Método ID3DXTextureShader::GetConstantByName – obtém uma constante procurando seu nome.
ms.assetid: 0c57f6ce-ea81-4b34-9251-c385bfe6ebe7
title: Método ID3DXTextureShader::GetConstantByName (D3DX9Shader.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXTextureShader.GetConstantByName
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 55b3de81179c01171d7ee5ff7b845295709dfb8ead1a9bc1a7cdf615bc37c44d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117729097"
---
# <a name="id3dxtextureshadergetconstantbyname-method"></a>Método ID3DXTextureShader::GetConstantByName

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

Um [alça para](handles.md) a estrutura de dados pai. Se a constante for um parâmetro de nível superior (não há nenhuma estrutura de dados pai), use **NULL.**

</dd> <dt>

*pName* \[ Em\]
</dt> <dd>

Tipo: **[ **LPCSTR**](../winprog/windows-data-types.md)**

Uma cadeia de caracteres que contém o nome da constante.

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

[ID3DXTextureShader](id3dxtextureshader.md)
</dt> </dl>

 

 
