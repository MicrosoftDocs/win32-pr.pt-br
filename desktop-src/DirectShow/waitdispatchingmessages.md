---
description: A função WaitDispatchingMessages aguarda que um objeto seja sinalizado, ao mesmo tempo que distribui mensagens de janela.
ms.assetid: d15f6736-d141-47a3-b767-fbf774982fb4
title: Função WaitDispatchingMessages (Wxutil. h)
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
ms.openlocfilehash: 9e509a081243f28293dc2d8abf8311f69eaf9a44
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105784013"
---
# <a name="waitdispatchingmessages-function"></a>Função WaitDispatchingMessages

A `WaitDispatchingMessages` função espera que um objeto seja sinalizado, ao mesmo tempo em que distribui mensagens de janela.

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

*hObject* 
</dt> <dd>

Identificador do objeto a ser aguardado.

</dd> <dt>

*dwWait* 
</dt> <dd>

Intervalo de tempo limite, em milissegundos.

</dd> <dt>

*HWND* 
</dt> <dd>

Identificador opcional para uma janela.

</dd> <dt>

*uMsg* 
</dt> <dd>

Mensagem de janela opcional, especificando uma mensagem a ser expedida.

</dd> <dt>

*hEvent* 
</dt> <dd>

Identificador opcional para um evento a ser aguardado.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorna o valor da função **WaitForMultipleObjects** .

## <a name="remarks"></a>Comentários

Se um objeto possuir uma janela, ele deverá enviar mensagens da janela enquanto aguarda. Essa função permite que o objeto Aguarde um evento, um semáforo ou outro objeto de exclusão mútua ao expedir mensagens.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Wxutil. h (incluir fluxos. h)</dt> </dl>                                                                                    |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Funções auxiliares diversas](miscellaneous-helper-functions.md)
</dt> </dl>

 

 




