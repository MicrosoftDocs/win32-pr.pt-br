---
description: Preenche uma matriz com dados de chave de retorno de chamada usados para animação de quadro chave.
ms.assetid: 2a2aa04a-a889-415b-8aa2-cc5f2bed1f9a
title: 'Método ID3DXKeyframedAnimationSet:: GetCallbackKeys (D3dx9anim. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXKeyframedAnimationSet.GetCallbackKeys
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: d3f8dbc771fcdde6d1c07a1bf810b322b0a70a30
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104172945"
---
# <a name="id3dxkeyframedanimationsetgetcallbackkeys-method"></a>Método ID3DXKeyframedAnimationSet:: GetCallbackKeys

Preenche uma matriz com dados de chave de retorno de chamada usados para animação de quadro chave.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT GetCallbackKeys(
  [out] LPD3DXKEY_CALLBACK pCallbackKeys
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pCallbackKeys* \[ fora\]
</dt> <dd>

Tipo: **[ **\_ retorno de chamada LPD3DXKEY**](d3dxkey-callback.md)**

Ponteiro para uma matriz alocada pelo usuário de estruturas de [**\_ retorno de chamada D3DXKEY**](d3dxkey-callback.md) que o método deve preencher com dados de retorno de chamada.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se o método for bem sucedido, o valor de retorno será S \_ OK. Se o método falhar, o seguinte valor será retornado: D3DERR \_ INVALIDCALL.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|----------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3dx9anim. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Confira também

<dl> <dt>

[ID3DXKeyframedAnimationSet](id3dxkeyframedanimationset.md)
</dt> <dt>

[**ID3DXKeyframedAnimationSet::GetNumCallbackKeys**](id3dxkeyframedanimationset--getnumcallbackkeys.md)
</dt> </dl>

 

 




