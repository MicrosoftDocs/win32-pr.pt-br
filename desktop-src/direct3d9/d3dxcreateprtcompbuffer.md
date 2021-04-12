---
description: Cria um buffer de PRT (transferência de radiante de computação compactada) compactado a partir de um objeto ID3DXPRTBuffer descompactado. Essa função deve ser usada com buffers por vértice ou volume.
ms.assetid: 1464d2dd-05db-4d9a-84ac-39d57b6fff4f
title: Função D3DXCreatePRTCompBuffer (D3DX9Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreatePRTCompBuffer
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 6906067c8f2b412b58c728756ecaa6415168f05a
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104298633"
---
# <a name="d3dxcreateprtcompbuffer-function"></a>Função D3DXCreatePRTCompBuffer

Cria um buffer de PRT (transferência de radiante de computação compactada) compactado a partir de um objeto [**ID3DXPRTBuffer**](id3dxprtbuffer.md) descompactado. Essa função deve ser usada com buffers por vértice ou volume.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT D3DXCreatePRTCompBuffer(
  _In_    D3DXSHCOMPRESSQUALITYTYPE Quality,
  _In_    UINT                      NumClusters,
  _In_    UINT                      NumPCA,
  _In_    LPD3DXSHPRTSIMCB          pCB,
  _In_    LPVOID                    lpUserContext,
  _In_    LPD3DXPRTBUFFER           pBuffer,
  _Inout_ LPD3DXPRTCOMPBUFFER       *ppBuffer
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Qualidade* \[ do no\]
</dt> <dd>

Tipo: **[ **D3DXSHCOMPRESSQUALITYTYPE**](./d3dxshcompressqualitytype.md)**

Qualidade da compactação de harmônica esférica (SH). Consulte [**D3DXSHCOMPRESSQUALITYTYPE**](./d3dxshcompressqualitytype.md).

</dd> <dt>

*NumClusters* \[ no\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

Número de clusters a serem usados para compactação.

</dd> <dt>

*NumPCA* \[ no\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

Número de vetores de base do PCA (análise de componente principal) a serem usados em cada cluster.

</dd> <dt>

*pCB* \[ no\]
</dt> <dd>

Tipo: **[LPD3DXSHPRTSIMCB](lpd3dxshprtsimcb.md)**

Ponteiro opcional para a função de retorno de chamada [LPD3DXSHPRTSIMCB](lpd3dxshprtsimcb.md) que é usada para calcular a porcentagem de computações de compactação de PRT concluídas. A função de retorno de chamada deve ser implementada para retornar S \_ OK para continuar executando a rotina de compactação. Qualquer outro valor irá parar a compactação. Pode ser **NULL**.

</dd> <dt>

*lpUserContext* \[ no\]
</dt> <dd>

Tipo: **[ **LPVOID**](../winprog/windows-data-types.md)**

Ponteiro opcional para um valor definido pelo usuário passado para a função de retorno de chamada [LPD3DXSHPRTSIMCB](lpd3dxshprtsimcb.md) . Normalmente usado por um aplicativo para passar um ponteiro para uma estrutura de dados que fornece informações de contexto para a função de retorno de chamada. Pode ser **NULL**.

</dd> <dt>

*pBuffer* \[ no\]
</dt> <dd>

Tipo: **[ **LPD3DXPRTBUFFER**](id3dxprtbuffer.md)**

Endereço de um ponteiro para o objeto [**ID3DXPRTBuffer**](id3dxprtbuffer.md) não compactado que será compactado.

</dd> <dt>

*ppBuffer* \[ entrada, saída\]
</dt> <dd>

Tipo: **[ **LPD3DXPRTCOMPBUFFER**](id3dxprtcompbuffer.md)\***

Endereço de um ponteiro para o objeto [**ID3DXPRTCompBuffer**](id3dxprtcompbuffer.md) de saída.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se a função for bem sucedido, o valor de retorno será D3D \_ OK. Se a função falhar, o valor de retorno poderá ser um dos seguintes: D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|----------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Funções de transferência radiante preputadas](dx9-graphics-reference-d3dx-functions-prt.md)
</dt> <dt>

[**D3DXCreatePRTBuffer**](d3dxcreateprtbuffer.md)
</dt> <dt>

[**D3DXCreatePRTBufferTex**](d3dxcreateprtbuffertex.md)
</dt> </dl>

 

 
