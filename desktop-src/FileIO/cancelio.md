---
description: Cancela todas as operações de E/S (entrada e saída) pendentes emitidas pelo thread de chamada para o arquivo especificado.
ms.assetid: b28162dc-0da8-41c6-9901-29381d2d72c4
title: Função CancelIo (IoAPI.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CancelIo
api_type:
- DllExport
api_location:
- Kernel32.dll
- API-MS-Win-Core-io-l1-1-1.dll
- KernelBase.dll
- MinKernelBase.dll
- api-ms-win-downlevel-kernel32-l1-1-0.dll
ms.openlocfilehash: 900a47d51df882ce1f2931489ea93b5e3b4c498b8d5cc0f35e521e015e12c1d3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120075336"
---
# <a name="cancelio-function"></a>Função CancelIo

Cancela todas as operações de E/S (entrada e saída) pendentes emitidas pelo thread de chamada para o arquivo especificado. A função não cancela as operações de E/S que outros threads emem para um manipular arquivo.

Para cancelar operações de E/S de outro thread, use a [**função CancelIoEx.**](cancelioex-func.md)

## <a name="syntax"></a>Sintaxe


```C++
BOOL WINAPI CancelIo(
  _In_ HANDLE hFile
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*hFile* \[ Em\]
</dt> <dd>

Um alça para o arquivo.

A função cancela todas as operações de E/S pendentes para esse manipular arquivo.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Se a função for bem-sucedida, o valor retornado será diferente de zero. A operação de cancelamento para todas as operações de E/S pendentes emitidas pelo thread de chamada para o alçamento de arquivo especificado foi solicitada com êxito. O thread pode usar a [**função GetOverlappedResult**](/windows/desktop/api/ioapiset/nf-ioapiset-getoverlappedresult) para determinar quando as próprias operações de E/S foram concluídas.

Se a função falhar, o valor de retorno será zero (0). Para obter informações de erro estendidas, chame a [**função GetLastError.**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror)

## <a name="remarks"></a>Comentários

Se houver operações de E/S pendentes em andamento para o alçamento de arquivo especificado e elas são emitidas pelo thread de chamada, a **função CancelIo** os cancela. **CancelIo** cancela apenas a E/S pendente no handle, ele não altera o estado do handle; isso significa que você não pode contar com o estado do handle porque não pode saber se a operação foi concluída com êxito ou cancelada.

As operações de E/S devem ser emitidas como E/S sobressalo. Caso não sejam, as operações de E/S não retornam para permitir que o thread chame a **função CancelIo.** Chamar a **função CancelIo** com um alça de arquivo que não é aberto com **FILE FLAG \_ \_ OVERLAPPED** não faz nada.

Todas as operações de E/S canceladas são concluídas com o erro OPERAÇÃO DE ERRO **\_ \_ ANULADA** e todas as notificações de conclusão para as operações de E/S ocorrem normalmente.

No Windows 8 e Windows Server 2012, essa função é suportada pelas tecnologias a seguir.



| Tecnologia                                           | Com suporte      |
|------------------------------------------------------|----------------|
| Protocolo SMB 3.0<br/>   | Sim<br/> |
| TFO (Failover Transparente) do SMB 3.0<br/>        | Sim<br/> |
| SMB 3.0 com SO (Compartilhamentos de Arquivos de Escalação Out)<br/>   | Sim<br/> |
| Volume Compartilhado Clusterizado sistema de arquivos (CsvFS)<br/> | Sim<br/> |
| ReFS (Sistema de Arquivos Resiliente)<br/>              | Sim<br/> |



 

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

[**CancelIoEx**](cancelioex-func.md)
</dt> <dt>

[**CancelSynchronousIo**](cancelsynchronousio-func.md)
</dt> <dt>

[**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea)
</dt> <dt>

[**Deviceiocontrol**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol)
</dt> <dt>

[Funções de gerenciamento de arquivos](file-management-functions.md)
</dt> <dt>

[**LockFileEx**](/windows/desktop/api/FileAPI/nf-fileapi-lockfileex)
</dt> <dt>

[**ReadDirectoryChangesW**](/windows/desktop/api/WinBase/nf-winbase-readdirectorychangesw)
</dt> <dt>

[**ReadFile**](/windows/desktop/api/FileAPI/nf-fileapi-readfile)
</dt> <dt>

[**ReadFileEx**](/windows/desktop/api/FileAPI/nf-fileapi-readfileex)
</dt> <dt>

[E/S síncrona e assíncrona](synchronous-and-asynchronous-i-o.md)
</dt> <dt>

[**WriteFile**](/windows/desktop/api/FileAPI/nf-fileapi-writefile)
</dt> <dt>

[**WriteFileEx**](/windows/desktop/api/FileAPI/nf-fileapi-writefileex)
</dt> </dl>

 

