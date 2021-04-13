---
description: Carrega na memória um buffer de PRT (transferência de radiante de computação compactada) compactado que foi salvo em disco.
ms.assetid: ea8bb0d6-f3ed-4ba0-ac87-02e9ac3ae15f
title: Função D3DXLoadPRTCompBufferFromFile (D3DX9Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXLoadPRTCompBufferFromFile
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 505fca7d8cb2426a49a2992c249ba45b5b7afd11
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104298812"
---
# <a name="d3dxloadprtcompbufferfromfile-function"></a>Função D3DXLoadPRTCompBufferFromFile

Carrega na memória um buffer de PRT (transferência de radiante de computação compactada) compactado que foi salvo em disco.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT D3DXLoadPRTCompBufferFromFile(
  _In_    LPCSTR              pFileName,
  _Inout_ LPD3DXPRTCOMPBUFFER *ppBuffer
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pFileName* \[ no\]
</dt> <dd>

Tipo: **[ **LPCSTR**](../winprog/windows-data-types.md)**

Nome do arquivo do qual carregar os dados de buffer compactados.

</dd> <dt>

*ppBuffer* \[ entrada, saída\]
</dt> <dd>

Tipo: **[ **LPD3DXPRTCOMPBUFFER**](id3dxprtcompbuffer.md)\***

Endereço de um ponteiro para o objeto [**ID3DXPRTCompBuffer**](id3dxprtcompbuffer.md) de saída.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se a função for bem sucedido, o valor de retorno será D3D \_ OK. Se a função falhar, o valor de retorno poderá ser um dos seguintes: D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.

## <a name="remarks"></a>Comentários

A configuração do compilador também determina a versão da função. Se o Unicode for definido, a chamada de função será resolvida como D3DXLoadPRTCompBufferFromFileW. Caso contrário, a chamada de função será resolvida como D3DXLoadPRTCompBufferFromFileA.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|----------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Funções de transferência radiante preputadas](dx9-graphics-reference-d3dx-functions-prt.md)
</dt> </dl>

 

 
