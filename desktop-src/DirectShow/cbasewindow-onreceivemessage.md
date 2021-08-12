---
description: O método OnReceiveMessage manipula mensagens de janela.
ms.assetid: 0f074f9b-00e5-42ff-a491-020d441acad1
title: Método CBaseWindow. OnReceiveMessage (Winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseWindow.OnReceiveMessage
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 1a5dbfb84edef1f5257cfda8cae08d27b219909f47a7d88fd29580ae12e48b3d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118657959"
---
# <a name="cbasewindowonreceivemessage-method"></a>Método CBaseWindow. OnReceiveMessage

O `OnReceiveMessage` método manipula mensagens de janela.

## <a name="syntax"></a>Sintaxe


```C++
virtual LRESULT OnReceiveMessage(
   HWND   hwnd,
   INT    uMsg,
   WPARAM wParam,
   LPARAM lParam
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*HWND* 
</dt> <dd>

Identificador da janela.

</dd> <dt>

*uMsg* 
</dt> <dd>

Identificador de mensagem.

</dd> <dt>

*wParam* 
</dt> <dd>

Primeiro parâmetro de mensagem.

</dd> <dt>

*lParam* 
</dt> <dd>

Segundo parâmetro de mensagem.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retornará 0 se a mensagem tiver sido processada ou 1 se a mensagem não tiver sido processada.

## <a name="remarks"></a>Comentários

A classe base manipula as seguintes mensagens:

-   fechar o WM \_
-   movimentação do WM \_
-   paleta do WMchanged \_
-   QUERYNEWPALETTE do WM \_
-   tamanho do WM \_
-   SYSCOLORCHANGE do WM \_

Uma classe derivada pode substituir esse método para lidar com outras mensagens. A classe derivada deve chamar o método de classe base para manipular todas as mensagens que a classe derivada ignora.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Winutil. h (incluir Fluxos. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CBaseWindow**](cbasewindow.md)
</dt> </dl>

 

 




