---
description: Marca todas as operações de e/s pendentes para o identificador de arquivo especificado. A função cancela apenas as operações de e/s no processo atual, independentemente de qual thread criou a operação de e/s.
ms.assetid: a2ce13b8-7da6-4848-848d-901d9667c2e3
title: Função CancelIoEx (IoAPI. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CancelIoEx
api_type:
- DllExport
api_location:
- Kernel32.dll
- API-MS-Win-Core-io-l1-1-0.dll
- KernelBase.dll
- MinKernelBase.dll
- API-MS-Win-Core-io-l1-1-1.dll
- api-ms-win-downlevel-kernel32-l1-1-0.dll
ms.openlocfilehash: 3de44762ad9a230a9d8cc410c4ba3ae7c2d9964e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105810922"
---
# <a name="cancelioex-function"></a>Função CancelIoEx

Marca todas as operações de e/s pendentes para o identificador de arquivo especificado. A função cancela apenas as operações de e/s no processo atual, independentemente de qual thread criou a operação de e/s.

## <a name="syntax"></a>Sintaxe


```C++
BOOL WINAPI CancelIoEx(
  _In_     HANDLE       hFile,
  _In_opt_ LPOVERLAPPED lpOverlapped
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*hFile* \[ no\]
</dt> <dd>

Um identificador para o arquivo.

</dd> <dt>

*lpOverlapped* \[ em, opcional\]
</dt> <dd>

Um ponteiro para uma estrutura de dados [**sobreposta**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) que contém os dados usados para e/s assíncrona.

Se esse parâmetro for **nulo**, todas as solicitações de e/s para o parâmetro *hFile* serão canceladas.

Se esse parâmetro não for **nulo**, somente as solicitações de e/s específicas emitidas para o arquivo com a estrutura sobreposta *lpOverlapped* especificada serão marcadas como canceladas, o que significa que você pode cancelar uma ou mais solicitações, enquanto a função [**CancelIo**](cancelio.md) cancela todas as solicitações pendentes em um identificador de arquivo.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Se a função for bem-sucedida, o valor retornado será diferente de zero. A operação de cancelamento para todas as operações de e/s pendentes emitidas pelo processo de chamada para o identificador de arquivo especificado foi solicitada com êxito. O aplicativo não deve liberar ou reutilizar a estrutura [**sobreposta**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) associada às operações de e/s canceladas até que elas sejam concluídas. O thread pode usar a função [**GetOverlappedResult**](/windows/desktop/api/ioapiset/nf-ioapiset-getoverlappedresult) para determinar quando as operações de e/s propriamente ditas foram concluídas.

Se a função falhar, o valor de retorno será 0 (zero). Para obter informações de erro estendidas, chame a função [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) .

Se essa função não puder localizar uma solicitação para cancelar, o valor de retorno será 0 (zero) e [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) retornará o **erro \_ não \_ encontrado**.

## <a name="remarks"></a>Comentários

A função **CancelIoEx** permite que você cancele solicitações em threads diferentes do thread de chamada. A função [**CancelIo**](cancelio.md) cancela apenas as solicitações no mesmo thread que chamou a função **CancelIo** . **CancelIoEx** cancela apenas e/s pendentes no identificador, ele não altera o estado do identificador; Isso significa que você não pode contar com o estado do identificador porque não é possível saber se a operação foi concluída com êxito ou cancelada.

Se houver alguma operação de e/s pendente em andamento para o identificador de arquivo especificado, a função **CancelIoEx** as marcará para cancelamento. A maioria dos tipos de operações pode ser cancelada imediatamente; outras operações podem continuar na conclusão antes de serem realmente canceladas e o chamador é notificado. A função **CancelIoEx** não aguarda a conclusão de todas as operações canceladas.

Se o identificador de arquivo estiver associado a uma porta de conclusão, um pacote de conclusão de e/s não será enfileirado para a porta se uma operação síncrona for cancelada com êxito. Para operações assíncronas ainda pendentes, a operação de cancelamento colocará em fila um pacote de conclusão de e/s.

A operação que está sendo cancelada é concluída com um dos três status; Você deve verificar o status de conclusão para determinar o estado de conclusão. Os três status são:

-   A operação foi concluída normalmente. Isso pode ocorrer mesmo que a operação tenha sido cancelada, porque a solicitação de cancelamento pode não ter sido enviada a tempo para cancelar a operação.
-   A operação foi cancelada. A função [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) retorna a **operação de erro \_ \_ anulada**.
-   A operação falhou com outro erro. A função [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) retorna o código de erro relevante.

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
|-------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Aplicativos de \[ aplicativos \| UWP do Windows Vista desktop\]<br/>                                                                                                                                                                                                                   |
| Servidor mínimo com suporte<br/> | Aplicativos do Windows Server 2008 \[ Desktop aplicativos \| UWP\]<br/>                                                                                                                                                                                                             |
| parâmetro<br/>                   | <dl> <dt>IoAPI. h (incluir Windows. h); </dt> <dt>Winbase. h no Windows server 2008 R2, Windows 7, Windows server 2008 e Windows Vista (incluir Windows. h)</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>Kernel32.lib</dt> </dl>                                                                                                                                                                                 |
| DLL<br/>                      | <dl> <dt>Kernel32.dll</dt> </dl>                                                                                                                                                                                 |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**CancelIo**](cancelio.md)
</dt> <dt>

[**CancelSynchronousIo**](cancelsynchronousio-func.md)
</dt> <dt>

[Cancelando operações de e/s pendentes](canceling-pending-i-o-operations.md)
</dt> <dt>

[Funções de gerenciamento de arquivos](file-management-functions.md)
</dt> <dt>

[E/s síncrona e síncrona](synchronous-and-asynchronous-i-o.md)
</dt> </dl>

 

