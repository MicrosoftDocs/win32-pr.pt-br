---
description: Carrega na memória um buffer de PRT (transferência de radiance) compactado que foi salvo no disco.
ms.assetid: ea8bb0d6-f3ed-4ba0-ac87-02e9ac3ae15f
title: Função D3DXLoadPRTCompBufferFromFile (D3DX9Mesh.h)
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
ms.openlocfilehash: a05a5712961e8bf72f4eb67f7e644d0f41150b812800fc1c0bd9bca464e3f54f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120027376"
---
# <a name="d3dxloadprtcompbufferfromfile-function"></a>Função D3DXLoadPRTCompBufferFromFile

Carrega na memória um buffer de PRT (transferência de radiance) compactado que foi salvo no disco.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT D3DXLoadPRTCompBufferFromFile(
  _In_    LPCSTR              pFileName,
  _Inout_ LPD3DXPRTCOMPBUFFER *ppBuffer
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pFileName* \[ Em\]
</dt> <dd>

Tipo: **[ **LPCSTR**](../winprog/windows-data-types.md)**

Nome do arquivo do qual carregar os dados de buffer compactados.

</dd> <dt>

*ppBuffer* \[ in, out\]
</dt> <dd>

Tipo: **[ **LPD3DXPRTCOMPBUFFER**](id3dxprtcompbuffer.md)\***

Endereço de um ponteiro para o objeto [**ID3DXPRTCompBuffer de**](id3dxprtcompbuffer.md) saída.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se a função for bem-sucedida, o valor de retorno será D3D \_ OK. Se a função falhar, o valor de retorno poderá ser um dos seguintes: D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.

## <a name="remarks"></a>Comentários

A configuração do compilador também determina a versão da função. Se Unicode for definido, a chamada de função será resolvida para D3DXLoadPRTCompBufferFromFileW. Caso contrário, a chamada de função será resolvida para D3DXLoadPRTCompBufferFromFileA.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|----------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3DX9Mesh.h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Funções de transferência de Radiance pré-comutadas](dx9-graphics-reference-d3dx-functions-prt.md)
</dt> </dl>

 

 
