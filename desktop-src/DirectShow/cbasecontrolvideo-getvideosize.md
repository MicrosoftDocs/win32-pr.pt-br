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
ms.openlocfilehash: 4b1df6fe781f036043728050354519dfa6e28d00
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105749049"
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

## <a name="return-value"></a>Retornar valor

Retorna um valor **HRESULT** .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Ctlutil. h (incluir fluxos. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CBaseControlVideo**](cbasecontrolvideo.md)
</dt> </dl>

 

 




