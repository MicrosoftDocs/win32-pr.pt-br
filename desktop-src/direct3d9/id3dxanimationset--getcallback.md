---
description: 'Método ID3DXAnimationSet:: getcallback – Obtém informações sobre um retorno de chamada específico no conjunto de animações.'
ms.assetid: e8388bfc-5438-4216-a98f-dd0dbca12c87
title: 'Método ID3DXAnimationSet:: getcallback (D3dx9anim. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXAnimationSet.GetCallback
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 563c1007cc471ab10a9609e776da69b7c5ed493b
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108097534"
---
# <a name="id3dxanimationsetgetcallback-method"></a>Método ID3DXAnimationSet:: getcallback

Obtém informações sobre um retorno de chamada específico no conjunto de animações.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT GetCallback(
  [in]  DOUBLE Position,
  [in]  DWORD  Flags,
  [out] DOUBLE *pCallbackPosition,
  [out] LPVOID *ppCallbackData
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Posição* \[ no\]
</dt> <dd>

Tipo: **[ **duplo**](../winprog/windows-data-types.md)**

Posição a partir da qual encontrar retornos de chamada.

</dd> <dt>

*Flags* \[in\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

Sinalizadores de pesquisa de retorno de chamada. Esse parâmetro pode ser definido como uma combinação de um ou mais sinalizadores de [**\_ \_ sinalizadores de pesquisa do D3DXCALLBACK**](./d3dxcallback-search-flags.md).

</dd> <dt>

*pCallbackPosition* \[ fora\]
</dt> <dd>

Tipo: **[ **duplo**](../winprog/windows-data-types.md)\***

Ponteiro para a posição do retorno de chamada.

</dd> <dt>

*ppCallbackData* \[ fora\]
</dt> <dd>

Tipo: **[ **LPVOID**](../winprog/windows-data-types.md)\***

Endereço do ponteiro de dados de retorno de chamada.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Os valores de retorno desse método são implementados por um programador de aplicativos. Em geral, se nenhum erro ocorrer, Programe o método para retornar o D3D \_ OK. Caso contrário, Programe o método para retornar uma mensagem de erro apropriada de [D3DERR](d3derr.md) ou [**D3DXERR**](./d3dxerr.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|----------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3dx9anim. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Consulte também

<dl> <dt>

[ID3DXAnimationSet](id3dxanimationset.md)
</dt> </dl>

 

 
