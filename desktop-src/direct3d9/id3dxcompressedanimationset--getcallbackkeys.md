---
description: 'Método ID3DXCompressedAnimationSet:: GetCallbackKeys – preenche uma matriz com dados de chave de retorno de chamada usados para a animação do quadro chave.'
ms.assetid: 0dc30c1f-9ffb-42ec-8074-84293f16c344
title: 'Método ID3DXCompressedAnimationSet:: GetCallbackKeys (D3dx9anim. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXCompressedAnimationSet.GetCallbackKeys
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: d7c430358b5ba7f66c5a79b08ae01925141e659f
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108115324"
---
# <a name="id3dxcompressedanimationsetgetcallbackkeys-method"></a>Método ID3DXCompressedAnimationSet:: GetCallbackKeys

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

## <a name="return-value"></a>Valor retornado

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se o método for bem sucedido, o valor de retorno será S \_ OK. Se o método falhar, o seguinte valor será retornado: D3DERR \_ INVALIDCALL.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|----------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3dx9anim. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Consulte também

<dl> <dt>

[ID3DXCompressedAnimationSet](id3dxcompressedanimationset.md)
</dt> <dt>

[**ID3DXCompressedAnimationSet::GetNumCallbackKeys**](id3dxcompressedanimationset--getnumcallbackkeys.md)
</dt> </dl>

 

 




