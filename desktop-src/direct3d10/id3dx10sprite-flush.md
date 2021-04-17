---
description: 'Forçar a envio de todos os sprites em lotes para o dispositivo. Os Estados do dispositivo permanecem como estavam após a última chamada para ID3DX10Sprite:: Begin. A lista de sprites em lote é desmarcada.'
ms.assetid: ae03e17c-1a14-4a41-a9a9-8757d2f7a81d
title: 'Método ID3DX10Sprite:: flush (D3DX10. h)'
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
ms.openlocfilehash: 748be56a7b89223db1957b9c0144143edd90ee4c
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105791628"
---
# <a name="id3dx10spriteflush-method"></a>Método ID3DX10Sprite:: flush

Forçar a envio de todos os sprites em lotes para o dispositivo. Os Estados do dispositivo permanecem como estavam após a última chamada para ID3DX10Sprite:: Begin. A lista de sprites em lote é desmarcada.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT Flush();
```



## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Retornar valor

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se o método for bem sucedido, o valor de retorno será S \_ OK. Se o método falhar, o seguinte valor será retornado: D3DERR \_ INVALIDCALL.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|---------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3DX10. h</dt> </dl>   |
| Biblioteca<br/> | <dl> <dt>D3DX10. lib</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[ID3DX10Sprite](id3dx10sprite.md)
</dt> <dt>

[Interfaces D3DX](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 




