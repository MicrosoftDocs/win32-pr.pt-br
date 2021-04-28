---
description: 'Método ID3DXTextureShader:: getconstant – Obtém uma constante pesquisando seu índice.'
ms.assetid: 7d3ab655-b50d-41ab-a4ca-c7b534e00e3f
title: 'Método ID3DXTextureShader:: getconstant (D3DX9Shader. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXTextureShader.GetConstant
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: edcc4b6a7f34c12be7013f2ae1e0b2e6d991a5d6
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108117664"
---
# <a name="id3dxtextureshadergetconstant-method"></a>Método ID3DXTextureShader:: getconstant

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

Um [identificador](handles.md) para a estrutura de dados pai. Se a constante for um parâmetro de nível superior (não há nenhuma estrutura de dados pai), use **NULL**.

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

Para obter uma constante de uma matriz de constantes, use [**ID3DXTextureShader:: Getconstantelement**](id3dxtextureshader--getconstantelement.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3DX9Shader. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9. lib</dt> </dl>     |



## <a name="see-also"></a>Consulte também

<dl> <dt>

[ID3DXTextureShader](id3dxtextureshader.md)
</dt> </dl>

 

 
