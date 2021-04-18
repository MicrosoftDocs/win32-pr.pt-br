---
description: Posta um pacote de conclusão de e/s em uma porta de conclusão de e/s.
ms.assetid: 69a9b1e5-2d40-42de-a14a-f7b6f29bf571
title: Função PostQueuedCompletionStatus (IoAPI. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PostQueuedCompletionStatus
api_type:
- DllExport
api_location:
- Kernel32.dll
- API-MS-Win-Core-io-l1-1-0.dll
- KernelBase.dll
- MinKernelBase.dll
- API-MS-Win-Core-io-l1-1-1.dll
- api-ms-win-downlevel-kernel32-l1-1-0.dll
ms.openlocfilehash: f12de10032df7fec32dd9a577353dd20c0f4eaa5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105756939"
---
# <a name="postqueuedcompletionstatus-function"></a>Função PostQueuedCompletionStatus

Posta um pacote de conclusão de e/s em uma porta de conclusão de e/s.

## <a name="syntax"></a>Sintaxe


```C++
BOOL WINAPI PostQueuedCompletionStatus(
  _In_     HANDLE       CompletionPort,
  _In_     DWORD        dwNumberOfBytesTransferred,
  _In_     ULONG_PTR    dwCompletionKey,
  _In_opt_ LPOVERLAPPED lpOverlapped
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*CompletionPort* \[ no\]
</dt> <dd>

Um identificador para uma porta de conclusão de e/s na qual o pacote de conclusão de e/s deve ser lançado.

</dd> <dt>

*dwNumberOfBytesTransferred* \[ no\]
</dt> <dd>

O valor a ser retornado por meio do parâmetro *lpNumberOfBytesTransferred* da função [**GetQueuedCompletionStatus**](/windows/win32/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus) .

</dd> <dt>

*dwCompletionKey* \[ no\]
</dt> <dd>

O valor a ser retornado por meio do parâmetro *lpCompletionKey* da função [**GetQueuedCompletionStatus**](/windows/win32/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus) .

</dd> <dt>

*lpOverlapped* \[ em, opcional\]
</dt> <dd>

O valor a ser retornado por meio do parâmetro *lpOverlapped* da função [**GetQueuedCompletionStatus**](/windows/win32/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus) .

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Se a função for bem-sucedida, o valor retornado será diferente de zero.

Se a função falhar, o valor retornado será zero. Para obter informações de erro estendidas, chame [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) .

## <a name="remarks"></a>Comentários

O pacote de conclusão de e/s atenderá a uma chamada pendente para a função [**GetQueuedCompletionStatus**](/windows/win32/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus) . Essa função retorna com os três valores passados como segundo, terceiro e quarto parâmetros da chamada para **PostQueuedCompletionStatus**. O sistema não usa nem valida esses valores. Em particular, o parâmetro *lpOverlapped* não precisa apontar para uma estrutura [**sobreposta**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) .

No Windows 8 e no Windows Server 2012, essa função é suportada pelas seguintes tecnologias.



| Tecnologia                                           | Com suporte      |
|------------------------------------------------------|----------------|
| Protocolo SMB (Server Message Block) 3,0<br/>   | Yes<br/> |
| Failover transparente SMB 3,0 (TFO)<br/>        | Yes<br/> |
| SMB 3,0 com compartilhamentos de arquivos de escalabilidade horizontal (SO)<br/>   | Yes<br/> |
| Sistema de arquivos Volume Compartilhado Clusterizado (CsvFS)<br/> | Yes<br/> |
| ReFS (Sistema de Arquivos Resiliente)<br/>              | Yes<br/> |



 

O CsvFs fará e/s redirecionada para arquivos compactados.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Aplicativos de \[ aplicativos \| UWP do Windows XP desktop\]<br/>                                                                                                                                                                                                                                                       |
| Servidor mínimo com suporte<br/> | Aplicativos do Windows Server 2003 \[ Desktop aplicativos \| UWP\]<br/>                                                                                                                                                                                                                                              |
| parâmetro<br/>                   | <dl> <dt>IoAPI. h (incluir Windows. h); </dt> <dt>Winbase. h no Windows server 2008 R2, Windows 7, Windows Server 2008, Windows Vista, Windows Server 2003 e Windows XP (incluir Windows. h)</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>Kernel32.lib</dt> </dl>                                                                                                                                                                                                                  |
| DLL<br/>                      | <dl> <dt>Kernel32.dll</dt> </dl>                                                                                                                                                                                                                  |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**CreateIoCompletionPort**](createiocompletionport.md)
</dt> <dt>

[Funções de gerenciamento de arquivos](file-management-functions.md)
</dt> <dt>

[**GetQueuedCompletionStatus**](/windows/win32/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus)
</dt> <dt>

[**SOBREPÕE**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped)
</dt> </dl>

 

