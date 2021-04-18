---
description: Bloqueia até que o thread saia.
ms.assetid: 1ee547b5-cd73-4ce8-8e66-c2062714d0f0
title: Método CMsgThread. WaitForThreadExit (Msgthrd. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMsgThread.WaitForThreadExit
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: c8b48573c4297a2d5d5d008eba88fd8ea437333c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105756193"
---
# <a name="cmsgthreadwaitforthreadexit-method"></a>Método CMsgThread. WaitForThreadExit

Bloqueia até que o thread saia.

## <a name="syntax"></a>Sintaxe


```C++
BOOL WaitForThreadExit(
   LPDWORD lpdwExitCode
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*lpdwExitCode* 
</dt> <dd>

Ponteiro para o código de saída retornado pelo thread.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorna **true** ou **false**, o significado do que é determinado pela classe que fornece a função de membro [**CMsgThread:: ThreadMessageProc**](cmsgthread-threadmessageproc.md) substituída e a função de membro de chamada.

## <a name="remarks"></a>Comentários

Verifique se o thread de trabalho foi encerrado completamente antes de concluir a destruição da classe derivada; caso contrário, o thread ainda poderá ser executado depois que a DLL (biblioteca de vínculo dinâmico) tiver sido descarregada do espaço de endereço do processo. Mesmo que a única instrução restante para sair seja uma instrução de retorno único, isso causaria uma exceção. A única maneira confiável de garantir que o thread foi encerrado é sinalizar o thread para sair (usando um objeto [**CMsg**](cmsg.md) negociado privadamente enviado para a função membro [**CMsgThread::P utthreadmsg**](cmsgthread-putthreadmsg.md) ) e, em seguida, chamar essa função de membro. Você deve fazer isso no destruidor para sua classe derivada.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Msgthrd. h (incluir fluxos. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CMsgThread**](cmsgthread.md)
</dt> </dl>

 

 




