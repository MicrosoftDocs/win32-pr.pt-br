---
description: Marca as operações de E/S pendentes para o alça de arquivo especificado. A função cancela apenas as operações de E/S no processo atual, independentemente de qual thread criou a operação de E/S.
ms.assetid: a2ce13b8-7da6-4848-848d-901d9667c2e3
title: Função CancelIoEx (IoAPI.h)
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
ms.openlocfilehash: 3726bf221073f33d87481d7a6bb6f2f4fd459812616975fba38d9a9a8f0334ec
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119582606"
---
# <a name="cancelioex-function"></a>Função CancelIoEx

Marca as operações de E/S pendentes para o alça de arquivo especificado. A função cancela apenas as operações de E/S no processo atual, independentemente de qual thread criou a operação de E/S.

## <a name="syntax"></a>Sintaxe


```C++
BOOL WINAPI CancelIoEx(
  _In_     HANDLE       hFile,
  _In_opt_ LPOVERLAPPED lpOverlapped
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*hFile* \[ Em\]
</dt> <dd>

Um alça para o arquivo.

</dd> <dt>

*lpOverlapped* \[ in, opcional\]
</dt> <dd>

Um ponteiro para uma [**estrutura de dados OVERLAPPED**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) que contém os dados usados para E/S assíncrona.

Se esse parâmetro for **NULL,** todas as solicitações de E/S para o *parâmetro hFile* serão canceladas.

Se esse parâmetro não for **NULL,** somente as solicitações de E/S específicas que foram emitidas para o arquivo com a estrutura sobrecarrada *lpOverlapped* especificada serão marcadas como canceladas, o que significa que você pode cancelar uma ou mais solicitações, enquanto a [**função CancelIo**](cancelio.md) cancela todas as solicitações pendentes em um manipular arquivo.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Se a função for bem-sucedida, o valor retornado será diferente de zero. A operação de cancelamento para todas as operações de E/S pendentes emitidas pelo processo de chamada para o alçamento de arquivo especificado foi solicitada com êxito. O aplicativo não deve liberar ou reutilizar a estrutura [**OVERLAPPED**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) associada às operações de E/S canceladas até que elas tenham sido concluídas. O thread pode usar a [**função GetOverlappedResult**](/windows/desktop/api/ioapiset/nf-ioapiset-getoverlappedresult) para determinar quando as próprias operações de E/S foram concluídas.

Se a função falhar, o valor de retorno será 0 (zero). Para obter informações de erro estendidas, chame a [**função GetLastError.**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror)

Se essa função não puder encontrar uma solicitação para cancelar, o valor de retorno será 0 (zero) e [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) **retornará ERROR \_ NOT \_ FOUND**.

## <a name="remarks"></a>Comentários

A **função CancelIoEx** permite que você cancele solicitações em threads diferentes do thread de chamada. A [**função CancelIo**](cancelio.md) apenas cancela solicitações no mesmo thread que chamou a **função CancelIo.** **CancelIoEx** cancela apenas a E/S pendente no handle, ele não altera o estado do handle; isso significa que você não pode contar com o estado do handle porque não pode saber se a operação foi concluída com êxito ou cancelada.

Se houver operações de E/S pendentes em andamento para o handle de arquivo especificado, a função **CancelIoEx** as marcará para cancelamento. A maioria dos tipos de operações pode ser cancelada imediatamente; outras operações podem continuar até a conclusão antes que elas sejam realmente canceladas e o chamador seja notificado. A **função CancelIoEx** não aguarda a conclusão de todas as operações canceladas.

Se o alça de arquivo estiver associado a uma porta de conclusão, um pacote de conclusão de E/S não será enxuado para a porta se uma operação síncrona for cancelada com êxito. Para operações assíncronas ainda pendentes, a operação de cancelamento enfileira um pacote de conclusão de E/S.

A operação que está sendo cancelada é concluída com um dos três status; você deve verificar o status de conclusão para determinar o estado de conclusão. Os três status são:

-   A operação foi concluída normalmente. Isso pode ocorrer mesmo que a operação tenha sido cancelada, porque a solicitação de cancelamento pode não ter sido enviada a tempo de cancelar a operação.
-   A operação foi cancelada. A [**função GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) retorna **ERROR OPERATION \_ \_ ABORTED**.
-   A operação falhou com outro erro. A [**função GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) retorna o código de erro relevante.

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
|-------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Aplicativos \| UWP de aplicativos da área de trabalho do Vista\]<br/>                                                                                                                                                                                                                   |
| Servidor mínimo com suporte<br/> | Windows Aplicativos \[ UWP do Server 2008 Desktop \|\]<br/>                                                                                                                                                                                                             |
| Cabeçalho<br/>                   | <dl> <dt>IoAPI.h (incluir Windows.h);</dt> <dt>WinBase.h no Windows Server 2008 R2, Windows 7, Windows Server 2008 e Windows Vista (inclua Windows.h)</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>Kernel32.lib</dt> </dl>                                                                                                                                                                                 |
| DLL<br/>                      | <dl> <dt>Kernel32.dll</dt> </dl>                                                                                                                                                                                 |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**CancelIo**](cancelio.md)
</dt> <dt>

[**CancelSynchronousIo**](cancelsynchronousio-func.md)
</dt> <dt>

[Cancelando operações de E/S pendentes](canceling-pending-i-o-operations.md)
</dt> <dt>

[Funções de gerenciamento de arquivos](file-management-functions.md)
</dt> <dt>

[E/S síncrona e assíncrona](synchronous-and-asynchronous-i-o.md)
</dt> </dl>

 

