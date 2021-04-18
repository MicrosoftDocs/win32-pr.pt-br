---
description: Cancela todas as operações de entrada e saída (e/s) pendentes emitidas pelo thread de chamada para o arquivo especificado.
ms.assetid: b28162dc-0da8-41c6-9901-29381d2d72c4
title: Função CancelIo (IoAPI. h)
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
ms.openlocfilehash: adb1ab95b30b31670a6ff5a4cc0e0205943f7683
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105753301"
---
# <a name="cancelio-function"></a>Função CancelIo

Cancela todas as operações de entrada e saída (e/s) pendentes emitidas pelo thread de chamada para o arquivo especificado. A função não cancela as operações de e/s que outros threads emitem para um identificador de arquivo.

Para cancelar as operações de e/s de outro thread, use a função [**CancelIoEx**](cancelioex-func.md) .

## <a name="syntax"></a>Sintaxe


```C++
BOOL WINAPI CancelIo(
  _In_ HANDLE hFile
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*hFile* \[ no\]
</dt> <dd>

Um identificador para o arquivo.

A função cancela todas as operações de e/s pendentes para este identificador de arquivo.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Se a função for bem-sucedida, o valor retornado será diferente de zero. A operação de cancelamento para todas as operações de e/s pendentes emitidas pelo thread de chamada para o identificador de arquivo especificado foi solicitada com êxito. O thread pode usar a função [**GetOverlappedResult**](/windows/desktop/api/ioapiset/nf-ioapiset-getoverlappedresult) para determinar quando as operações de e/s propriamente ditas foram concluídas.

Se a função falhar, o valor de retorno será zero (0). Para obter informações de erro estendidas, chame a função [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) .

## <a name="remarks"></a>Comentários

Se houver alguma operação de e/s pendente em andamento para o identificador de arquivo especificado e elas forem emitidas pelo thread de chamada, a função **CancelIo** as cancelará. **CancelIo** cancela apenas e/s pendentes no identificador, ele não altera o estado do identificador; Isso significa que você não pode contar com o estado do identificador porque não é possível saber se a operação foi concluída com êxito ou cancelada.

As operações de e/s devem ser emitidas como e/s sobreposta. Se não forem, as operações de e/s não retornarão para permitir que o thread chame a função **CancelIo** . Chamar a função **CancelIo** com um identificador de arquivo que não está aberto com o **sinalizador de arquivo \_ \_ sobreposto** não faz nada.

Todas as operações de e/s que foram canceladas com a operação de erro de erro foram **\_ \_ anuladas** e todas as notificações de conclusão para as operações de e/s ocorrem normalmente.

No Windows 8 e no Windows Server 2012, essa função é suportada pelas seguintes tecnologias.



| Tecnologia                                           | Com suporte      |
|------------------------------------------------------|----------------|
| Protocolo SMB (Server Message Block) 3,0<br/>   | Yes<br/> |
| Failover transparente SMB 3,0 (TFO)<br/>        | Yes<br/> |
| SMB 3,0 com compartilhamentos de arquivos de escalabilidade horizontal (SO)<br/>   | Yes<br/> |
| Sistema de arquivos Volume Compartilhado Clusterizado (CsvFS)<br/> | Yes<br/> |
| ReFS (Sistema de Arquivos Resiliente)<br/>              | Yes<br/> |



 

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

[**CancelIoEx**](cancelioex-func.md)
</dt> <dt>

[**CancelSynchronousIo**](cancelsynchronousio-func.md)
</dt> <dt>

[**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea)
</dt> <dt>

[**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol)
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

[E/s síncrona e síncrona](synchronous-and-asynchronous-i-o.md)
</dt> <dt>

[**WriteFile**](/windows/desktop/api/FileAPI/nf-fileapi-writefile)
</dt> <dt>

[**WriteFileEx**](/windows/desktop/api/FileAPI/nf-fileapi-writefileex)
</dt> </dl>

 

