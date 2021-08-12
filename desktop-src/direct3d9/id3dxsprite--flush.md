---
description: Força todos os sprites em lote a serem enviados para o dispositivo. Os estados do dispositivo permanecem como estavam após a última chamada para ID3DXSprite::Begin. A lista de sprites em lote é limpa.
ms.assetid: e5717bde-e339-4344-8ce7-b0c3fe118887
title: Método ID3DXSprite::Flush (D3dx9core.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXSprite.Flush
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 766fbe41491fc6861ac3eaf366c3a858870c560139f1048d405184b580e72229
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118292688"
---
# <a name="id3dxspriteflush-method"></a>Método ID3DXSprite::Flush

Força todos os sprites em lote a serem enviados para o dispositivo. Os estados do dispositivo permanecem como estavam após a última chamada para [**ID3DXSprite::Begin.**](id3dxsprite--begin.md) A lista de sprites em lote é limpa.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT Flush();
```



## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Retornar valor

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se o método for bem-sucedido, o valor de retorno será S \_ OK. Se o método falhar, o valor a seguir será retornado. D3DERR \_ INVALIDCALL

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|----------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3dx9core.h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Confira também

<dl> <dt>

[ID3DXSprite](id3dxsprite.md)
</dt> <dt>

[**ID3DXSprite::End**](id3dxsprite--end.md)
</dt> </dl>

 

 




