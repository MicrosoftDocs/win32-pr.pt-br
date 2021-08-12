---
description: Force todos os sprites em lote a serem enviados para o dispositivo. Os estados do dispositivo permanecem como estavam após a última chamada para ID3DX10Sprite::Begin. A lista de sprites em lote é limpa.
ms.assetid: ae03e17c-1a14-4a41-a9a9-8757d2f7a81d
title: Método ID3DX10Sprite::Flush (D3DX10.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10Sprite.Flush
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: d74c96ebab8b1e174a44124aaa53b714a9ea860fc9fa2ea5ae3e25c9779aae01
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118302239"
---
# <a name="id3dx10spriteflush-method"></a>Método ID3DX10Sprite::Flush

Force todos os sprites em lote a serem enviados para o dispositivo. Os estados do dispositivo permanecem como estavam após a última chamada para ID3DX10Sprite::Begin. A lista de sprites em lote é limpa.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT Flush();
```



## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Retornar valor

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se o método for bem-sucedido, o valor de retorno será S \_ OK. Se o método falhar, o seguinte valor será retornado: D3DERR \_ INVALIDCALL.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|---------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3DX10.h</dt> </dl>   |
| Biblioteca<br/> | <dl> <dt>D3DX10.lib</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[ID3DX10Sprite](id3dx10sprite.md)
</dt> <dt>

[D3DX Interfaces](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 




