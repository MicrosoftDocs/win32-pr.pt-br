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
ms.openlocfilehash: 44b5089b6e539a8104586e27b58388a324462b37
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104173029"
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

## <a name="return-value"></a>Retornar valor

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

 

 
