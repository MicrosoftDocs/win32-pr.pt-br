---
description: Obter os nomes de amostra referenciados em um sombreador.
ms.assetid: fe769917-daac-43b8-bf63-fb337915ff53
title: Função D3DXGetShaderSamplers (D3DX9Shader.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXGetShaderSamplers
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: da4c7381b0fe058e18dd2edfd86ef49f434cd1b57bff18303fce0ba939c5d299
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119044994"
---
# <a name="d3dxgetshadersamplers-function"></a>Função D3DXGetShaderSamplers

Obter os nomes de amostra referenciados em um sombreador.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT D3DXGetShaderSamplers(
  _In_    const DWORD  *pFunction,
  _Inout_       LPCSTR *pSamplers,
  _Out_         UINT   *pCount
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pFunction* \[ Em\]
</dt> <dd>

Tipo: **const [**DWORD**](../winprog/windows-data-types.md) \***

Ponteiro para o fluxo DWORD da função de sombreador.

</dd> <dt>

*pSamplers* \[ in, out\]
</dt> <dd>

Tipo: **[ **LPCSTR**](../winprog/windows-data-types.md)\***

Ponteiro para uma matriz de LPCSTRs. A função preencherá essa matriz com ponteiros para os nomes de amostra contidos em *pFunction*. O tamanho máximo da matriz é o número máximo de registros de amostra (16 para \_ versus 3 \_ 0 e ps \_ 3 \_ 0).

Para encontrar o número de exemplos usados, verifique *pCount depois* de chamar **D3DXGetShaderSamplers** com pSamplers = **NULL**.

</dd> <dt>

*pCount* \[ out\]
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)\***

Retorna o número de amostras referenciados pelo sombreador.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se a função for bem-sucedida, o valor de retorno será D3D \_ OK. Se a função falhar, o valor de retorno poderá ser um dos seguintes: D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA, E \_ OUTOFMEMORY.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3DX9Shader.h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9.lib</dt> </dl>     |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Funções de sombreador](dx9-graphics-reference-d3dx-functions-shader.md)
</dt> </dl>

 

 
