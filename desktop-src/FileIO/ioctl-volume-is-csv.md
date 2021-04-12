---
description: Determina se um volume é um volume CSV.
ms.assetid: 6B09B519-1E2F-4757-AAD5-1E4C81023E14
title: IOCTL_VOLUME_IS_CSV código de controle (Ntddvol. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IOCTL_VOLUME_IS_CSV
api_type:
- HeaderDef
api_location:
- Ntddvol.h
ms.openlocfilehash: 8121e1b89c88ad05a2c2be8537d7170bfabfc412
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104297357"
---
# <a name="ioctl_volume_is_csv-control-code"></a>O \_ volume do IOCTL \_ é um código de \_ controle CSV

Determina se um volume é um volume CSV.

Para executar essa operação, chame a função [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) com os parâmetros a seguir.


```C++
BOOL 
WINAPI 
DeviceIoControl( (HANDLE) hDevice,              // handle to device
                 IOCTL_VOLUME_IS_CSV,           // dwIoControlCode
                 NULL,                          // input buffer
                 0,                             // size of input buffer
                 (LPVOID) lpOutBuffer,          // lpOutBuffer
                 (DWORD) nOutBufferSize,        // nOutBufferSize
                 (LPDWORD) lpBytesReturned,     // number of bytes returned
                 (LPOVERLAPPED) lpOverlapped ); // OVERLAPPED structure
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*hDevice* 
</dt> <dd>

Um identificador para o volume. Para recuperar um identificador de volume, chame a função [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) . Somente os administradores podem abrir identificadores de volume.

</dd> <dt>

*dwIoControlCode* 
</dt> <dd>

O código de controle para a operação. Use **o \_ volume do IOCTL \_ é \_ CSV** para esta operação.

</dd> <dt>

*lpInBuffer* 
</dt> <dd>

Não usado com esta operação; Defina como **nulo**.

</dd> <dt>

*nInBufferSize* 
</dt> <dd>

Não usado com esta operação; Defina como zero (0).

</dd> <dt>

*lpOutBuffer* 
</dt> <dd>

Um ponteiro para **verdadeiro** se o volume for um volume CSV; caso contrário, a chamada de função falhará.

</dd> <dt>

*nOutBufferSize* 
</dt> <dd>

O tamanho do buffer de saída em bytes.

</dd> <dt>

*lpBytesReturned* 
</dt> <dd>

Um ponteiro para uma variável que recebe o tamanho dos dados armazenados no buffer de saída, em bytes.

Se *lpOverlapped* for **nulo**, *lpBytesReturned* não poderá ser **nulo**. Mesmo quando uma operação não retorna dados de saída e *lpOutBuffer* é **nula**, [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) faz uso de *lpBytesReturned*. Após tal operação, o valor de *lpBytesReturned* é inútil.

Se *lpOverlapped* não for **nulo**, *lpBytesReturned* poderá ser **nulo**. Se esse parâmetro não for **nulo** e a operação retornar dados, *lpBytesReturned* será inútil até que a operação sobreposta seja concluída. Para recuperar o número de bytes retornados, chame [**GetOverlappedResult**](/windows/desktop/api/ioapiset/nf-ioapiset-getoverlappedresult). Se *hDevice* estiver associado a uma porta de conclusão de e/s, você poderá recuperar o número de bytes retornados chamando [**GetQueuedCompletionStatus**](/windows/win32/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus).

</dd> <dt>

*lpOverlapped* 
</dt> <dd>

Um ponteiro para uma estrutura [**sobreposta**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) .

Se *hDevice* tiver sido aberto sem especificar o **sinalizador de arquivo \_ \_ sobreposto**, *lpOverlapped* será ignorado.

Se *hDevice* tiver sido aberto com o sinalizador de **sinalizador de arquivo \_ \_ sobreposto** , a operação será executada como uma operação sobreposta (assíncrona). Nesse caso, *lpOverlapped* deve apontar para uma estrutura [**sobreposta**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) válida que contém um identificador para um objeto de evento. Caso contrário, a função falhará de maneiras imprevisíveis.

Para operações sobrepostas, [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) retorna imediatamente e o objeto de evento é sinalizado quando a operação é concluída. Caso contrário, a função não retorna até que a operação seja concluída ou um erro ocorra.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Se a operação for concluída com êxito, [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) retornará um valor diferente de zero.

Se a operação falhar ou estiver pendente, [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) retornará zero (0). Para obter informações de erro estendidas, chame [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Nenhum compatível<br/>                                                            |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2012\]<br/>                                 |
| parâmetro<br/>                   | <dl> <dt>Ntddvol. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea)
</dt> <dt>

[**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol)
</dt> <dt>

[Códigos de controle de gerenciamento de volume](volume-management-control-codes.md)
</dt> </dl>

 

