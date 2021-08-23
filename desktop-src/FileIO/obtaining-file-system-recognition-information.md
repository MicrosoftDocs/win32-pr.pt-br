---
description: O reconhecimento do sistema de arquivos é a capacidade de reconhecer a mídia de armazenamento que contém um layout válido do sistema de arquivos/volume que ainda não foi definido, mas a mídia é capaz de se identificar por meio da presença da estrutura de reconhecimento definida internamente pelo Windows.
ms.assetid: 23ed6de0-25ff-4841-91f6-94b487dee613
title: Obtendo informações de reconhecimento do sistema de arquivos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2c10b538f9e98ecab3f8f8f72784ef658c068f780388dc7b600be68b76380757
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119148499"
---
# <a name="obtaining-file-system-recognition-information"></a>Obtendo informações de reconhecimento do sistema de arquivos

[](file-system-recognition.md) O reconhecimento do sistema de arquivos é a capacidade de reconhecer a mídia de armazenamento que contém um layout válido do sistema de arquivos/volume que ainda não foi definido, mas a mídia é capaz de se identificar por meio da presença da estrutura de reconhecimento definida internamente pelo Windows.

Como nenhum sistema de arquivos existente reconhecerá um novo layout de disco, o sistema de arquivos "RAW" montará o volume e fornecerá acesso direto no nível do bloco. O sistema de arquivos "RAW", incorporado em *NtosKrnl,* terá a capacidade de ler a estrutura de reconhecimento do sistema de arquivos e fornecer aos aplicativos acesso a essas estruturas por meio da solicitação de controle do sistema de arquivos [**FSCTL \_ QUERY \_ FILE SYSTEM \_ \_ RECOGNITION**](/windows/win32/api/winioctl/ni-winioctl-fsctl_query_file_system_recognition), mostrada no exemplo a seguir.


```C++
STDMETHODIMP CheckFileSystem(
    PCWSTR pcwszDrive
    ) 
{
    HRESULT hr = S_OK;
    HANDLE  hDisk = INVALID_HANDLE_VALUE;
    BOOL    fResult = FALSE;    
    ULONG   BytesReturned = 0;    
    FILE_SYSTEM_RECOGNITION_INFORMATION     FsRi = {0};
    
    //
    // Open the target, for example "\\.\C:"
    //
    wprintf( L"CreateFile on %s...", pcwszDrive );
    hDisk = CreateFile( pcwszDrive, 
                        FILE_READ_ATTRIBUTES|SYNCHRONIZE|FILE_TRAVERSE,                        
                        FILE_SHARE_READ|FILE_SHARE_WRITE,
                        NULL, OPEN_EXISTING, 0, NULL );    
    if( hDisk == INVALID_HANDLE_VALUE ) 
    {
        hr = HRESULT_FROM_WIN32( GetLastError() );
        wprintf( L"CreateFile failed on %s, GLE = 0x%x\n", pcwszDrive, GetLastError() );
        goto exit;
    }
    wprintf( L"succeeded.\n\n" );

    wprintf( L"\nPress Any Key to send down the FSCTL\n" );
    _getwch();

    //
    // Send down the FSCTL
    //
    wprintf( L"Calling DeviceIoControl( FSCTL_QUERY_FILE_SYSTEM_RECOGNITION ) " );
    
    fResult = DeviceIoControl( hDisk, 
                               FSCTL_QUERY_FILE_SYSTEM_RECOGNITION, 
                               NULL, 
                               0, 
                               &FsRi, 
                               sizeof(FsRi), 
                               &BytesReturned, 
                               NULL );
    if( !fResult ) 
    {
        hr = HRESULT_FROM_WIN32( GetLastError() );
        wprintf( L"failed GLE = 0x%x\n", GetLastError() );
        goto exit;
    }
    wprintf( L"succeeded.\n\n" );

    wprintf( L"FSCTL_QUERY_FILE_SYSTEM_RECOGNITION returned success.\n" );

    wprintf( L"FSCTL_QUERY_FILE_SYSTEM_RECOGNITION retrieved \"%S\".\n",
              FsRi.FileSystem );

exit:

    if( hDisk != INVALID_HANDLE_VALUE ) 
    {
        CloseHandle( hDisk );
        hDisk = INVALID_HANDLE_VALUE;
    }

    return hr;
}
```



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Reconhecimento do sistema de arquivos](file-system-recognition.md)
</dt> <dt>

[**ESTRUTURA DE \_ RECONHECIMENTO DO SISTEMA DE \_ \_ ARQUIVOS**](file-system-recognition-structure.md)
</dt> <dt>

[**RECONHECIMENTO DO SISTEMA DE ARQUIVOS DE CONSULTA FSCTL \_ \_ \_ \_**](/windows/win32/api/winioctl/ni-winioctl-fsctl_query_file_system_recognition)
</dt> </dl>

 

 
