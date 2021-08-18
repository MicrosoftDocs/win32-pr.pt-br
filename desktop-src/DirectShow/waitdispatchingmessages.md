---
description: A função WaitDispatchingMessages aguarda a sinalização de um objeto durante a expedição de mensagens da janela.
ms.assetid: d15f6736-d141-47a3-b767-fbf774982fb4
title: Função WaitDispatchingMessages (Wxutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WaitDispatchingMessages
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 26442633d1a4d5187b5e53ae53e0a898f759f91dc3719f09715b570108b701f1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119071900"
---
# <a name="waitdispatchingmessages-function"></a>Função WaitDispatchingMessages

A `WaitDispatchingMessages` função aguarda que um objeto seja sinalizado, ao expedir mensagens da janela.

## <a name="syntax"></a>Sintaxe


```C++
DWORD WINAPI WaitDispatchingMessages(
   HANDLE hObject,
   DWORD  dwWait,
   HWND   hwnd = NULL,
   UINT   uMsg = 0,
   HANDLE hEvent = NULL
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Hobject* 
</dt> <dd>

Identificador do objeto a ser aguardado.

</dd> <dt>

*dwWait* 
</dt> <dd>

Intervalo de tempo-fora, em milissegundos.

</dd> <dt>

*Hwnd* 
</dt> <dd>

Alça opcional para uma janela.

</dd> <dt>

*Umsg* 
</dt> <dd>

Mensagem de janela opcional, especificando uma mensagem a ser expedida.

</dd> <dt>

*Hevent* 
</dt> <dd>

Manipular opcional para um evento pelo que esperar.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retorna o valor da **função WaitForMultipleObjects.**

## <a name="remarks"></a>Comentários

Se um objeto tiver uma janela, ele deverá expedir mensagens de janela enquanto aguarda. Essa função permite que o objeto aguarde um evento, semáforo ou outro objeto de exclusão mútua ao expedir mensagens.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Wxutil.h (incluir Fluxos.h)</dt> </dl>                                                                                    |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (builds de varejo); </dt> <dt>Strmbasd.lib (builds de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Funções auxiliares diversas](miscellaneous-helper-functions.md)
</dt> </dl>

 

 




