---
description: Bloqueia até que o thread saia.
ms.assetid: 1ee547b5-cd73-4ce8-8e66-c2062714d0f0
title: Método CMsgThread.WaitForThreadExit (Msgthrd.h)
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
ms.openlocfilehash: de9861a1c7cae3055be288c4624b9e0b98c7b719e1534c1841ddb17770d91cf3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119915706"
---
# <a name="cmsgthreadwaitforthreadexit-method"></a>Método CMsgThread.WaitForThreadExit

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

## <a name="return-value"></a>Valor retornado

Retorna **TRUE** ou **FALSE**, o significado do qual é determinado pela classe que fornece a função de membro [**CMsgThread::ThreadMessageProc**](cmsgthread-threadmessageproc.md) e a função membro de chamada.

## <a name="remarks"></a>Comentários

Verifique se o thread de trabalho foi completamente concluído antes de concluir a destruição da classe derivada; caso contrário, o thread ainda poderá ser executado depois que sua DLL (biblioteca de vínculo dinâmico) tiver sido descarregada do espaço de endereço do processo. Mesmo que a única instrução deixada para sair seja uma instrução de retorno único, isso causaria uma exceção. A única maneira confiável de garantir que o thread tenha sido exitado é sinalizar o thread para sair (usando um objeto [**CMsg**](cmsg.md) negociado de forma privada enviado para a função de membro [**CMsgThread::P utThreadMsg)**](cmsgthread-putthreadmsg.md) e, em seguida, chamar essa função de membro. Você deve fazer isso no destruidor da classe derivada.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Msgthrd.h (incluir Fluxos.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (builds de varejo); </dt> <dt>Strmbasd.lib (builds de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CMsgThread**](cmsgthread.md)
</dt> </dl>

 

 




