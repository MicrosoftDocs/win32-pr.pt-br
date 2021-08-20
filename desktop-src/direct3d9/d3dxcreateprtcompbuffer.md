---
description: Cria um buffer de PRT (transferência de radiance pré-compactado) compactado de um objeto ID3DXPRTBuffer não compactado. Essa função deve ser usada com buffers por vértice ou volume.
ms.assetid: 1464d2dd-05db-4d9a-84ac-39d57b6fff4f
title: Função D3DXCreatePRTCompBuffer (D3DX9Mesh.h)
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
ms.openlocfilehash: cba1f4106a4dd04c3265bcb5cc5b19fe6a81b9ef7bd8824673e89918f9baeec4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118096581"
---
# <a name="d3dxcreateprtcompbuffer-function"></a>Função D3DXCreatePRTCompBuffer

Cria um buffer de PRT (transferência de radiance pré-compactado) compactado de um objeto [**ID3DXPRTBuffer**](id3dxprtbuffer.md) não compactado. Essa função deve ser usada com buffers por vértice ou volume.

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

*Qualidade* \[ Em\]
</dt> <dd>

Tipo: **[ **D3DXSHCOMPRESSQUALITYTYPE**](./d3dxshcompressqualitytype.md)**

Qualidade da compactação sh (spherical) . Consulte [**D3DXSHCOMPRESSQUALITYTYPE**](./d3dxshcompressqualitytype.md).

</dd> <dt>

*NumClusters* \[ Em\]
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

Número de clusters a ser usado para compactação.

</dd> <dt>

*NumPCA* \[ Em\]
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

Número de vetores base de PCA (análise de componente principal) a ser usado em cada cluster.

</dd> <dt>

*pCB* \[ Em\]
</dt> <dd>

Tipo: **[LPD3DXSHPRTSIMCB](lpd3dxshprtsimcb.md)**

Ponteiro opcional para a função de retorno de chamada [LPD3DXSHPRTSIMCB](lpd3dxshprtsimcb.md) usada para calcular o percentual de cálculos de compactação PRT concluídos. A função de retorno de chamada deve ser implementada para retornar S \_ OK para continuar executando a rotina de compactação. Qualquer outro valor interromperá a compactação. Pode ser **NULL.**

</dd> <dt>

*lpUserContext* \[ Em\]
</dt> <dd>

Tipo: **[ **LPVOID**](../winprog/windows-data-types.md)**

Ponteiro opcional para um valor definido pelo usuário passado para a função de retorno de chamada [LPD3DXSHPRTSIMCB.](lpd3dxshprtsimcb.md) Normalmente usado por um aplicativo para passar um ponteiro para uma estrutura de dados que fornece informações de contexto para a função de retorno de chamada. Pode ser **NULL.**

</dd> <dt>

*pBuffer* \[ Em\]
</dt> <dd>

Tipo: **[ **LPD3DXPRTBUFFER**](id3dxprtbuffer.md)**

Endereço de um ponteiro para o objeto [**ID3DXPRTBuffer**](id3dxprtbuffer.md) não compactado que será compactado.

</dd> <dt>

*ppBuffer* \[ in, out\]
</dt> <dd>

Tipo: **[ **LPD3DXPRTCOMPBUFFER**](id3dxprtcompbuffer.md)\***

Endereço de um ponteiro para o objeto [**ID3DXPRTCompBuffer de**](id3dxprtcompbuffer.md) saída.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se a função for bem-sucedida, o valor de retorno será D3D \_ OK. Se a função falhar, o valor de retorno poderá ser um dos seguintes: D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|----------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3DX9Mesh.h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Funções de transferência de Radiance pré-comutadas](dx9-graphics-reference-d3dx-functions-prt.md)
</dt> <dt>

[**D3DXCreatePRTBuffer**](d3dxcreateprtbuffer.md)
</dt> <dt>

[**D3DXCreatePRTBufferTex**](d3dxcreateprtbuffertex.md)
</dt> </dl>

 

 
