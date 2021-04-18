---
description: Obter os nomes de amostra referenciados em um sombreador.
ms.assetid: fe769917-daac-43b8-bf63-fb337915ff53
title: Função D3DXGetShaderSamplers (D3DX9Shader. h)
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
ms.openlocfilehash: 2135ba36f238188c6e7817001ba89bb47e3b9998
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105793849"
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

*pFunction* \[ no\]
</dt> <dd>

Tipo: **const [**DWORD**](../winprog/windows-data-types.md) \***

Ponteiro para o fluxo DWORD da função de sombreador.

</dd> <dt>

*pSamplers* \[ entrada, saída\]
</dt> <dd>

Tipo: **[ **LPCSTR**](../winprog/windows-data-types.md)\***

Ponteiro para uma matriz de LPCSTRs. A função preencherá essa matriz com ponteiros para os nomes de amostra contidos em *pFunction*. O tamanho máximo da matriz é o número máximo de registros de amostra (16 para vs \_ 3 \_ 0 e PS \_ 3 \_ 0).

Para localizar o número de amostras usadas, verifique *pCount* depois de chamar **D3DXGetShaderSamplers** com pSamplers = **NULL**.

</dd> <dt>

*pCount* \[ fora\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)\***

Retorna o número de amostras referenciadas pelo sombreador.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se a função for bem sucedido, o valor de retorno será D3D \_ OK. Se a função falhar, o valor de retorno poderá ser um dos seguintes: D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA, E \_ OUTOFMEMORY.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3DX9Shader. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9. lib</dt> </dl>     |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Funções de sombreador](dx9-graphics-reference-d3dx-functions-shader.md)
</dt> </dl>

 

 
