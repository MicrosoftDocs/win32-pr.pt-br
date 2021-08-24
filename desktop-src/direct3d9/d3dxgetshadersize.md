---
description: Retorna o tamanho do código de byte do sombreador, em bytes.
ms.assetid: 7dd091f7-fda9-49e1-982d-2eb57d9ecb23
title: Função D3DXGetShaderSize (D3DX9Shader.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXGetShaderSize
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 7354431fa8f9e8a177b8ccc63ef434a3f0a88add8e9e4736e3fd5fffb0cea811
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119564816"
---
# <a name="d3dxgetshadersize-function"></a>Função D3DXGetShaderSize

Retorna o tamanho do código de byte do sombreador, em bytes.

## <a name="syntax"></a>Sintaxe


```C++
UINT D3DXGetShaderSize(
  _In_ const DWORD *pFunction
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pFunction* \[ Em\]
</dt> <dd>

Tipo: **const [**DWORD**](../winprog/windows-data-types.md) \***

Ponteiro para o fluxo DWORD da função.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

Retorna o tamanho do código de byte do sombreador, em bytes.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3DX9Shader.h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9.lib</dt> </dl>     |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Funções de sombreador](dx9-graphics-reference-d3dx-functions-shader.md)
</dt> </dl>

 

 
