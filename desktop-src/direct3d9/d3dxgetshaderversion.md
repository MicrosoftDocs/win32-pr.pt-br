---
description: Retorna a versão do sombreador compilado.
ms.assetid: 6cc6c654-e8d1-4225-b5d0-6bc2434a16bd
title: Função D3DXGetShaderVersion (D3DX9Shader. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXGetShaderVersion
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 2c4a65db8706f6d8648096cf0822654e562687a2
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104091965"
---
# <a name="d3dxgetshaderversion-function"></a>Função D3DXGetShaderVersion

Retorna a versão do sombreador compilado.

## <a name="syntax"></a>Sintaxe


```C++
DWORD D3DXGetShaderVersion(
  _In_ const DWORD *pFunction
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pFunction* \[ no\]
</dt> <dd>

Tipo: **const [**DWORD**](../winprog/windows-data-types.md) \***

Ponteiro para a função de fluxo DWORD.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

Retorna a versão do sombreador fornecido ou zero se a função de sombreador for **nula**.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3DX9Shader. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9. lib</dt> </dl>     |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Funções de sombreador](dx9-graphics-reference-d3dx-functions-shader.md)
</dt> </dl>

 

 
