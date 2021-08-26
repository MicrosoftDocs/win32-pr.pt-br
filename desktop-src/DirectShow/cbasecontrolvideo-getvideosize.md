---
description: O método getvideoclipize recupera a largura e a altura do vídeo nativo.
ms.assetid: b3461a56-705b-465a-9cfc-e86fd52a07c5
title: Método CBaseControlVideo. (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlVideo.GetVideoSize
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: b49f58901ac362b5a03d069485ec4dbf74e22d4549dc628f26baa5c2bfa85234
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120056936"
---
# <a name="cbasecontrolvideogetvideosize-method"></a>Método CBaseControlVideo.

O `GetVideoSize` método recupera a largura e a altura do vídeo nativo.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT GetVideoSize(
   long *pWidth,
   long *pHeight
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pWidth* 
</dt> <dd>

Ponteiro para a largura do vídeo.

</dd> <dt>

*pHeight* 
</dt> <dd>

Ponteiro para a altura do vídeo.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retorna um valor **HRESULT** .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Ctlutil. h (incluir Fluxos. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CBaseControlVideo**](cbasecontrolvideo.md)
</dt> </dl>

 

 




