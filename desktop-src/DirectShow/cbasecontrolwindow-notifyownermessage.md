---
description: O método NotifyOwnerMessage passa mensagens específicas para a janela de vídeo.
ms.assetid: 8b27281a-5b8a-46c3-aa66-390d4496f30e
title: Método CBaseControlWindow. NotifyOwnerMessage (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlWindow.NotifyOwnerMessage
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 9073d37987404849ba8aa3acbda9919df840b410
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105752306"
---
# <a name="cbasecontrolwindownotifyownermessage-method"></a>Método CBaseControlWindow. NotifyOwnerMessage

O `NotifyOwnerMessage` método passa mensagens específicas para a janela de vídeo.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT NotifyOwnerMessage(
   long     hwnd,
   long     uMsg,
   LONG_PTR wParam,
   LONG_PTR lParam
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*HWND* 
</dt> <dd>

Identificador para a janela de vídeo.

</dd> <dt>

*uMsg* 
</dt> <dd>

Detalhes da mensagem.

</dd> <dt>

*wParam* 
</dt> <dd>

Primeiro parâmetro de mensagem.

</dd> <dt>

*lParam* 
</dt> <dd>

Segundo parâmetro de mensagem.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Não retorna nenhum \_ erro.

## <a name="remarks"></a>Comentários

Quando a janela de vídeo é um filho de outra janela, ela não recebe determinadas mensagens de janela de nível superior. Essas mensagens podem ser valiosas para um processador, pois podem afetar seu comportamento. `NotifyOwnerMessage` passa qualquer uma das mensagens a seguir para a janela de vídeo.

-   ACTIVATEAPP do WM \_
-   DEVMODECHANGE do WM \_
-   DISPLAYCHANGE do WM \_
-   paleta do WMchanged \_
-   PALETTEISCHANGING do WM \_
-   QUERYNEWPALETTE do WM \_
-   SYSCOLORCHANGE do WM \_

Você pode solicitar que o [**IVideoWindow**](/windows/desktop/api/Control/nn-control-ivideowindow) de plug-in (PID) de um Windows faça uma janela se torne um filho de outra janela. Quando isso ocorrer, o PID procurará determinadas mensagens que podem ser enviadas para a janela proprietária. Em seguida, o PID encaminhará essas mensagens para a janela de propriedade. O processamento padrão para as mensagens é enviá-las ao procedimento de janela de propriedade de forma síncrona chamando a função **SendMessage** do Win32.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Ctlutil. h (incluir fluxos. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CBaseControlWindow**](cbasecontrolwindow.md)
</dt> </dl>

 

 




