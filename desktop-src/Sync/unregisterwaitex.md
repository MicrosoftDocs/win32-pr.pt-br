---
description: Cancela uma operação de espera registrada emitida pela função RegisterWaitForSingleObject.
ms.assetid: ea700e55-fce7-46cd-bb96-0c129b429d46
title: Função UnregisterWaitEx (Threadpoollegacyapiset. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- UnregisterWaitEx
api_type:
- DllExport
api_location:
- Kernel32.dll
- API-MS-Win-Core-threadpool-l1-1-0.dll
- KernelBase.dll
- API-MS-Win-Core-threadpool-legacy-l1-1-0.dll
- API-MS-Win-DownLevel-Kernel32-l1-1-0.dll
- MinKernelBase.dll
ms.openlocfilehash: 30f5ad5f88bec9eb7eebff5a73d8f84f633cb249
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103828532"
---
# <a name="unregisterwaitex-function"></a>Função UnregisterWaitEx

Cancela uma operação de espera registrada emitida pela função [**RegisterWaitForSingleObject**](/windows/desktop/api/WinBase/nf-winbase-registerwaitforsingleobject) .

## <a name="syntax"></a>Sintaxe


```C++
BOOL WINAPI UnregisterWaitEx(
  _In_     HANDLE WaitHandle,
  _In_opt_ HANDLE CompletionEvent
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*WaitHandle* \[ no\]
</dt> <dd>

O identificador de espera. Esse identificador é retornado pela função [**RegisterWaitForSingleObject**](/windows/desktop/api/WinBase/nf-winbase-registerwaitforsingleobject) .

</dd> <dt>

*CompletionEvent* \[ em, opcional\]
</dt> <dd>

Um identificador para o objeto de evento a ser sinalizado quando a operação de espera tiver sido cancelada. Este parâmetro pode ser **NULL**.

Se esse parâmetro for **um \_ \_ valor de identificador inválido**, a função aguardará que todas as funções de retorno de chamada sejam concluídas antes de retornar.

Se esse parâmetro for **nulo**, a função marcará o temporizador para exclusão e retornará imediatamente. No entanto, a maioria dos chamadores deve aguardar a conclusão da função de retorno de chamada para que possa executar qualquer limpeza necessária.

Se o chamador fornecer esse evento e a função for bem-sucedida ou se a função falhar com **erro e \_ /s \_ pendente**, não feche o evento até que ele seja sinalizado.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Se a função for bem-sucedida, o valor retornado será diferente de zero.

Se a função falhar, o valor retornado será zero. Para obter informações de erro estendidas, chame [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror).

## <a name="remarks"></a>Comentários

Você não pode fazer uma chamada de bloqueio para o **UnregisterWaitEx** de dentro de uma função de retorno para a mesma operação de espera. Caso contrário, o retorno de chamada estará aguardando sua conclusão. Em geral, uma chamada de bloqueio para **UnregisterWaitEx** cria uma dependência entre o thread atual e o retorno de chamada, portanto, para fazer uma chamada de cancelamento de registro em outra operação de espera, você deve garantir que as funções de retorno de chamada não dependem umas das outras e que a segunda operação de espera também não execute uma chamada de cancelamento de registro na primeira operação.

Tenha cuidado ao fazer uma chamada **UnregisterWaitEx** de bloqueio em um thread persistente. Se a operação de espera que está sendo cancelada pelo registro foi criada com **WT \_ EXECUTEINPERSISTENTTHREAD**, pode ocorrer um deadlock.

Depois de fazer uma chamada de não bloqueio para **UnregisterWaitEx**, nenhuma nova função de retorno de chamada associada a *WaitHandle* pode ser enfileirada. No entanto, pode haver funções pendentes de retorno de chamada já enfileiradas para threads de trabalho.

Em algumas condições, a função falhará com o **erro \_ e/s \_ pendente** se *CompletionEvent* for **nulo**. Isso indica que há funções de retorno de chamada pendentes. Esses retornos de chamada serão executados ou estarão no meio da execução.

Se *CompletionEvent* for um identificador para um evento fornecido pelo chamador, é possível que a função seja bem-sucedida, falhe com **erro \_ e/s \_ pendente** ou falhe com um código de erro diferente. Se a função for bem-sucedida ou se a função falhar com **erro \_ e/s \_ pendente**, o chamador sempre deverá esperar até que o evento seja sinalizado para fechar o evento. Se a função falhar com um código de erro diferente, não será necessário aguardar até que o evento seja sinalizado para fechar o evento.

**Windows XP:** Se *CompletionEvent* for um identificador para um evento fornecido pelo chamador e a função falhar com **erro e \_ /s \_ pendente**, o chamador deverá aguardar até que o evento seja sinalizado para fechar o evento. Esse comportamento mudou a partir do Windows Vista.

Para compilar um aplicativo que usa essa função, defina **\_ Win32 \_ WinNT** como 0x0500 ou posterior. Para obter mais informações, consulte [usando os cabeçalhos do Windows](../winprog/using-the-windows-headers.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows XP\]<br/>                                                                                                                                                                                                                                                                                                                    |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                                                                                                                                                                                                                                                                                           |
| parâmetro<br/>                   | <dl> <dt>Threadpoollegacyapiset. h no Windows 8 e no Windows Server 2012 (incluir Windows. h); </dt> <dt>Winbase. h no Windows 7, Windows server 2008 R2, Windows Vista, Windows Server 2008, Windows XP e Windows Server 2003 (inclua o Windows. h)</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>Kernel32.lib</dt> </dl>                                                                                                                                                                                                                                                                        |
| DLL<br/>                      | <dl> <dt>Kernel32.dll</dt> </dl>                                                                                                                                                                                                                                                                        |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**RegisterWaitForSingleObject**](/windows/desktop/api/WinBase/nf-winbase-registerwaitforsingleobject)
</dt> <dt>

[Funções de sincronização](synchronization-functions.md)
</dt> <dt>

[Pooling de Thread ](../procthread/thread-pooling.md)
</dt> </dl>

 

 
