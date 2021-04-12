---
title: Código de controle FSCTL_DFS_GET_PKT_ENTRY_STATE (LmDfs.h)
description: O código de controle de FSCTL_DFS_GET_PKT_ENTRY_STATE pode obter as mesmas informações que a função NetDfsGetClientInfo, mas pode fornecer melhor desempenho em algumas configurações com latências altas para os servidores DFS.
ms.assetid: d4eec104-128b-43b5-9fae-08ab0b977dec
topic_type:
- apiref
api_name:
- FSCTL_DFS_GET_PKT_ENTRY_STATE
api_location:
- LmDfs.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8a57fb448934908ebc1530e95a298715324aaee6
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104501045"
---
# <a name="fsctl_dfs_get_pkt_entry_state-control-code"></a>FSCTL_DFS_GET_PKT_ENTRY_STATE código de controle

O código de controle de **FSCTL_DFS_GET_PKT_ENTRY_STATE** pode obter as mesmas informações que a função [**NetDfsGetClientInfo**](/windows/desktop/api/lmdfs/nf-lmdfs-netdfsgetclientinfo) , mas pode fornecer melhor desempenho em algumas configurações com latências altas para os servidores DFS. Não é recomendável usar o código de controle de **FSCTL_DFS_GET_PKT_ENTRY_STATE** , a menos que haja problemas de desempenho.

Para executar essa operação, chame a função [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) com os parâmetros a seguir.

```C++
BOOL 
   WINAPI 
   DeviceIoControl( (HANDLE)       hDevice,            // handle to device
                    (DWORD)        FSCTL_DFS_GET_PKT_ENTRY_STATE, // dwIoControlCode(LPDWORD)      lpInBuffer,         // input buffer
                    (DWORD)        nInBufferSize,      // size of input buffer
                    (LPDWORD)      lpOutBuffer,        // output buffer
                    (DWORD)        nOutBufferSize,     // size of output buffer
                    (LPDWORD)      lpBytesReturned,    // number of bytes returned
                    (LPOVERLAPPED) lpOverlapped );     // OVERLAPPED structure
```

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*hDevice* [in]
</dt> <dd>

Um identificador para o dispositivo. Para obter um identificador de dispositivo, chame a função [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) .

</dd> <dt>

*dwIoControlCode* [in]
</dt> <dd>

O código de controle para a operação. Use **FSCTL_DFS_GET_PKT_ENTRY_STATE** para esta operação.

</dd> <dt>

*lpInBuffer* 
</dt> <dd>

Endereço de uma estrutura de [**DFS_GET_PKT_ENTRY_STATE_ARG**](/windows/win32/api/lmdfs/ns-lmdfs-dfs_get_pkt_entry_state_arg) e as cadeias de caracteres Unicode 1-3 a seguir.

</dd> <dt>

*nInBufferSize* [in]
</dt> <dd>

Tamanho, em bytes, do buffer apontado pelo parâmetro *lpInBuffer* .

</dd> <dt>

*lpOutBuffer* [saída]
</dt> <dd>

Endereço de uma estrutura de **DFS_INFO_ \#** e quaisquer cadeias de caracteres e estruturas apontadas pela estrutura de **DFS_INFO_ \#** . A estrutura específica retornada depende do membro de **nível** na estrutura de [**DFS_GET_PKT_ENTRY_STATE_ARG**](/windows/win32/api/lmdfs/ns-lmdfs-dfs_get_pkt_entry_state_arg) passada no buffer de entrada.

</dd> <dt>

*nOutBufferSize* [in]
</dt> <dd>

Tamanho, em bytes, do buffer apontado pelo parâmetro *lpOutBuffer* . Devido às cadeias de caracteres e estruturas referenciadas pela estrutura de **DFS_INFO_ \#** retornada que também estão no buffer de saída, esse buffer deve ser maior do que a estrutura de **DFS_INFO_ \#** especificada.

</dd> <dt>

*lpBytesReturned* [saída]
</dt> <dd>

Um ponteiro para uma variável que recebe o tamanho dos dados armazenados no buffer de saída, em bytes.

Se o buffer de saída for muito pequeno, mas pelo menos grande o suficiente para manter um **DWORD**, a chamada falhará, [**getlasterror**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) retornará **ERROR_MORE_DATA** e a primeira **DWORD** do buffer de saída conterá o tamanho necessário. Se o buffer de saída não puder conter um **DWORD** , a chamada falhará com **ERROR_INSUFFICIENT_BUFFER** e *lpBytesReturned* será zero.

Se *lpOverlapped* for **nulo**, *lpBytesReturned* não poderá ser **nulo**. Mesmo quando uma operação não retorna dados de saída e *lpOutBuffer* é **nula**, [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) faz uso de *lpBytesReturned*. Após tal operação, o valor de *lpBytesReturned* é inútil.

Se *lpOverlapped* não for **nulo**, *lpBytesReturned* poderá ser **nulo**. Se esse parâmetro não for **nulo** e a operação retornar dados, *lpBytesReturned* será inútil até que a operação sobreposta seja concluída. Para recuperar o número de bytes retornados, chame [**GetOverlappedResult**](/windows/desktop/api/ioapiset/nf-ioapiset-getoverlappedresult). Se o parâmetro *hDevice* estiver associado a uma porta de conclusão de e/s, você poderá recuperar o número de bytes retornados chamando [**GetQueuedCompletionStatus**](/windows/win32/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus).

</dd> <dt>

*lpOverlapped* [in]
</dt> <dd>

Um ponteiro para uma estrutura [**sobreposta**](/windows/win32/api/minwinbase/ns-minwinbase-overlapped) .

Se *hDevice* tiver sido aberto sem especificar **FILE_FLAG_OVERLAPPED**, *lpOverlapped* será ignorado.

Se *hDevice* tiver sido aberto com o sinalizador **FILE_FLAG_OVERLAPPED** , a operação será executada como uma operação sobreposta (assíncrona). Nesse caso, *lpOverlapped* deve apontar para uma estrutura [**sobreposta**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) válida que contém um identificador para um objeto de evento. Caso contrário, a função falhará de maneiras imprevisíveis.

Para operações sobrepostas, [**DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol) retorna imediatamente e o objeto de evento é sinalizado quando a operação é concluída. Caso contrário, a função não retorna até que a operação seja concluída ou um erro ocorra.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Se a operação for concluída com êxito, [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) retornará um valor diferente de zero.

Se a operação falhar ou estiver pendente, [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) retornará zero. Para obter informações de erro estendidas, chame [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror).

## <a name="requirements"></a>Requisitos

| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Vista<br/>                                                                             |
| Servidor mínimo com suporte<br/> | Windows Server 2008<br/>                                                                       |
| parâmetro<br/>                   | <dl> <dt>LmDfs. h (incluir LmDfs. h)</dt> </dl> |

## <a name="see-also"></a>Confira também

<dl> <dt>

[**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol)
</dt> <dt>

[**NetDfsGetClientInfo**](/windows/desktop/api/lmdfs/nf-lmdfs-netdfsgetclientinfo)
</dt> </dl>
