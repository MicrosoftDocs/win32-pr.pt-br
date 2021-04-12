---
description: O reconhecimento do sistema de arquivos é a capacidade de reconhecer a mídia de armazenamento que contém um layout de volume/sistema de arquivos válido que ainda não foi definido, mas a mídia é capaz de se identificar por meio da presença da estrutura de reconhecimento definida internamente pelo Windows.
ms.assetid: 23ed6de0-25ff-4841-91f6-94b487dee613
title: Obtendo informações de reconhecimento do sistema de arquivos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 18cafa9f1c7cf6cbbe11d434aff3db424a1cd0a0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104296507"
---
# <a name="obtaining-file-system-recognition-information"></a><span data-ttu-id="da7b6-103">Obtendo informações de reconhecimento do sistema de arquivos</span><span class="sxs-lookup"><span data-stu-id="da7b6-103">Obtaining File System Recognition Information</span></span>

<span data-ttu-id="da7b6-104">O [reconhecimento do sistema de arquivos](file-system-recognition.md) é a capacidade de reconhecer a mídia de armazenamento que contém um layout de volume/sistema de arquivos válido que ainda não foi definido, mas a mídia é capaz de se identificar por meio da presença da estrutura de reconhecimento definida internamente pelo Windows.</span><span class="sxs-lookup"><span data-stu-id="da7b6-104">[File system recognition](file-system-recognition.md) is the ability to recognize storage media that contain a valid file system/volume layout that has not been defined yet, but the media is able to identify itself through the presence of the recognition structure defined internally by Windows.</span></span>

<span data-ttu-id="da7b6-105">Como nenhum sistema de arquivos existente reconhecerá um novo layout de disco, o sistema de arquivos "bruto" montará o volume e fornecerá acesso direto ao nível de bloco.</span><span class="sxs-lookup"><span data-stu-id="da7b6-105">Because no existing file system will recognize a new disk layout, the "RAW" file system will mount the volume and provide direct block level access.</span></span> <span data-ttu-id="da7b6-106">O sistema de arquivos "bruto", incorporado em *NtosKrnl*, terá a capacidade de ler a estrutura de reconhecimento do sistema de arquivos e fornecer aos aplicativos acesso a tais estruturas por meio da solicitação de controle do sistema de arquivos [**fsctl consulta do \_ \_ sistema de arquivos \_ \_**](/windows/win32/api/winioctl/ni-winioctl-fsctl_query_file_system_recognition), mostrada no exemplo a seguir.</span><span class="sxs-lookup"><span data-stu-id="da7b6-106">The "RAW" file system, incorporated in *NtosKrnl*, will have the ability to read the file system recognition structure and provide applications access to such structures through the file system control request [**FSCTL\_QUERY\_FILE\_SYSTEM\_RECOGNITION**](/windows/win32/api/winioctl/ni-winioctl-fsctl_query_file_system_recognition), shown in the following example.</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="da7b6-107">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="da7b6-107">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="da7b6-108">Reconhecimento do sistema de arquivos</span><span class="sxs-lookup"><span data-stu-id="da7b6-108">File System Recognition</span></span>](file-system-recognition.md)
</dt> <dt>

[<span data-ttu-id="da7b6-109">**\_estrutura de \_ reconhecimento do sistema de arquivos \_**</span><span class="sxs-lookup"><span data-stu-id="da7b6-109">**FILE\_SYSTEM\_RECOGNITION\_STRUCTURE**</span></span>](file-system-recognition-structure.md)
</dt> <dt>

[<span data-ttu-id="da7b6-110">**\_reconhecimento do \_ sistema de arquivos de consulta fsctl \_ \_**</span><span class="sxs-lookup"><span data-stu-id="da7b6-110">**FSCTL\_QUERY\_FILE\_SYSTEM\_RECOGNITION**</span></span>](/windows/win32/api/winioctl/ni-winioctl-fsctl_query_file_system_recognition)
</dt> </dl>

 

 
