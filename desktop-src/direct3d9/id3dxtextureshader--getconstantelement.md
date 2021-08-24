---
description: Obtenha uma constante da tabela de constantes.
ms.assetid: ebb05a09-af20-4c71-8594-940fce3a97e7
title: 'Método ID3DXTextureShader:: getconstantelement (D3DX9Shader. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXTextureShader.GetConstantElement
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 02d21efb3ef0ed5d4602833571b2b1a32e73df73b76f82a357cda574e93e84ce
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119747385"
---
# <a name="id3dxtextureshadergetconstantelement-method"></a>Método ID3DXTextureShader:: getconstantelement

Obtenha uma constante da tabela de constantes.

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

Um [identificador](handles.md) para a matriz de constantes. Esse valor não pode ser **nulo**.

</dd> <dt>

*Índice* \[ do no\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

Índice de base zero do elemento na tabela de constantes.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Tipo: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**

Retorna um identificador exclusivo para a constante.

## <a name="remarks"></a>Comentários

Para obter uma constante que não faz parte de uma matriz, use [**ID3DXTextureShader:: getconstant**](id3dxtextureshader--getconstant.md) ou [**ID3DXTextureShader:: GetConstantByName**](id3dxtextureshader--getconstantbyname.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3DX9Shader. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9. lib</dt> </dl>     |



## <a name="see-also"></a>Confira também

<dl> <dt>

[ID3DXTextureShader](id3dxtextureshader.md)
</dt> </dl>

 

 
