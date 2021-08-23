---
description: Posta um pacote de conclusão de E/S em uma porta de conclusão de E/S.
ms.assetid: 69a9b1e5-2d40-42de-a14a-f7b6f29bf571
title: Função PostQueuedCompletionStatus (IoAPI.h)
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
ms.openlocfilehash: e56bad8b9de85f22836f9446b67340d22e71fe83552da6796e7864d3baddae4b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119683356"
---
# <a name="postqueuedcompletionstatus-function"></a>Função PostQueuedCompletionStatus

Posta um pacote de conclusão de E/S em uma porta de conclusão de E/S.

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

*CompletionPort* \[ Em\]
</dt> <dd>

Um lidar com uma porta de conclusão de E/S na qual o pacote de conclusão de E/S deve ser postado.

</dd> <dt>

*dwNumberOfBytesTransferred* \[ Em\]
</dt> <dd>

O valor a ser retornado por *meio do parâmetro lpNumberOfBytesTransferred* da [**função GetQueuedCompletionStatus.**](/windows/win32/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus)

</dd> <dt>

*dwCompletionKey* \[ Em\]
</dt> <dd>

O valor a ser retornado por *meio do parâmetro lpCompletionKey* da [**função GetQueuedCompletionStatus.**](/windows/win32/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus)

</dd> <dt>

*lpOverlapped* \[ in, opcional\]
</dt> <dd>

O valor a ser retornado por *meio do parâmetro lpOverlapped* da [**função GetQueuedCompletionStatus.**](/windows/win32/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus)

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Se a função for bem-sucedida, o valor retornado será diferente de zero.

Se a função falhar, o valor retornado será zero. Para obter informações de erro estendidas, [**chame GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) .

## <a name="remarks"></a>Comentários

O pacote de conclusão de E/S atenderá a uma chamada pendente para a [**função GetQueuedCompletionStatus.**](/windows/win32/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus) Essa função retorna com os três valores passados como o segundo, o terceiro e o quarto parâmetros da chamada para **PostQueuedCompletionStatus**. O sistema não usa nem valida esses valores. Em particular, o *parâmetro lpOverlapped* não precisa apontar para uma [**estrutura OVERLAPPED.**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped)

No Windows 8 e Windows Server 2012, essa função é suportada pelas tecnologias a seguir.



| Tecnologia                                           | Com suporte      |
|------------------------------------------------------|----------------|
| Protocolo SMB 3.0<br/>   | Sim<br/> |
| TFO (Failover Transparente) do SMB 3.0<br/>        | Sim<br/> |
| SMB 3.0 com SO (Compartilhamentos de Arquivos de Escalação Out)<br/>   | Sim<br/> |
| Volume Compartilhado Clusterizado de Arquivos do Volume Compartilhado Clusterizado (CsvFS)<br/> | Sim<br/> |
| ReFS (Sistema de Arquivos Resiliente)<br/>              | Sim<br/> |



 

CsvFs fará E/S redirecionada para arquivos compactados.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Aplicativos \| UWP de aplicativos da área de trabalho XP\]<br/>                                                                                                                                                                                                                                                       |
| Servidor mínimo com suporte<br/> | Windows Aplicativos \[ UWP de aplicativos da área de trabalho do Server 2003 \|\]<br/>                                                                                                                                                                                                                                              |
| Cabeçalho<br/>                   | <dl> <dt>IoAPI.h (incluir Windows.h);</dt> <dt>WinBase.h no Windows Server 2008 R2, Windows 7, Windows Server 2008, Windows Vista, Windows Server 2003 e Windows XP (inclua Windows.h)</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>Kernel32.lib</dt> </dl>                                                                                                                                                                                                                  |
| DLL<br/>                      | <dl> <dt>Kernel32.dll</dt> </dl>                                                                                                                                                                                                                  |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Createiocompletionport**](createiocompletionport.md)
</dt> <dt>

[Funções de gerenciamento de arquivos](file-management-functions.md)
</dt> <dt>

[**GetQueuedCompletionStatus**](/windows/win32/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus)
</dt> <dt>

[**Sobreposta**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped)
</dt> </dl>

 

