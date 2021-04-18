---
description: Enfileira uma solicitação de execução pelo thread de trabalho.
ms.assetid: a854f962-143d-4776-bf98-119d003867df
title: Método CMsgThread. PutThreadMsg (Msgthrd. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMsgThread.PutThreadMsg
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 3445d9af4ec9c7abe6a4401e219fc305e254d555
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105770282"
---
# <a name="cmsgthreadputthreadmsg-method"></a>Método CMsgThread. PutThreadMsg

Enfileira uma solicitação de execução pelo thread de trabalho.

## <a name="syntax"></a>Sintaxe


```C++
void PutThreadMsg(
   UINT     uMsg,
   DWORD    dwMsgFlags,
   LPVOID   lpMsgParam,
   CAMEvent *pEvent = NULL
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*uMsg* 
</dt> <dd>

Código de solicitação.

</dd> <dt>

*dwMsgFlags* 
</dt> <dd>

Parâmetro de sinalizadores opcionais.

</dd> <dt>

*lpMsgParam* 
</dt> <dd>

Ponteiro opcional para um bloco de dados que contém parâmetros adicionais ou valores de retorno. Deve ser estático ou alocado para heap e não automático.

</dd> <dt>

*pEvent* 
</dt> <dd>

Ponteiro opcional para um objeto de evento a ser sinalizado após a conclusão.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Esse método não retorna um valor.

## <a name="remarks"></a>Comentários

Essa função de membro enfileira uma solicitação de execução pelo thread de trabalho. Os parâmetros dessa função de membro serão enfileirados (em um objeto [**CMsg**](cmsg.md) ) e passados para a função membro [**CMsgThread:: ThreadMessageProc**](cmsgthread-threadmessageproc.md) do thread de trabalho. Essa função de membro retorna imediatamente após o enfileiramento da solicitação e não aguarda o thread atender à solicitação. A função membro **CMsgThread:: ThreadMessageProc** da classe derivada define os quatro parâmetros.

Essa função de membro usa uma lista multithread segura, portanto, várias chamadas para essa função de membro de threads diferentes podem ser feitas com segurança.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Msgthrd. h (incluir fluxos. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CMsgThread**](cmsgthread.md)
</dt> </dl>

 

 




