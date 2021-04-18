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
ms.openlocfilehash: defef9a7ca24d6875eda508989615f308a2385b4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105752089"
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

Identificador para a janela.

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

## <a name="return-value"></a>Retornar valor

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
| parâmetro<br/>  | <dl> <dt>Winutil. h (incluir fluxos. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CBaseWindow**](cbasewindow.md)
</dt> </dl>

 

 




