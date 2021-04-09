---
description: O exemplo a seguir define a hora da última gravação de um arquivo para a hora atual do sistema usando a função SetFileTime.
ms.assetid: b4a70c01-d5ce-47e8-9918-9c9176894240
title: Alterando a hora do arquivo para a hora atual
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1b3d4b6189514196c5f8a332c259da9f8f8d7417
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103922976"
---
# <a name="changing-a-file-time-to-the-current-time"></a>Alterando a hora do arquivo para a hora atual

O exemplo a seguir define a hora da última gravação de um arquivo para a hora atual do sistema usando a função [**SetFileTime**](/windows/desktop/api/FileAPI/nf-fileapi-setfiletime) .

O sistema de arquivos NTFS armazena valores de tempo no formato UTC, portanto, eles não são afetados por alterações no fuso horário ou no horário de verão. O sistema de arquivos FAT armazena valores de tempo com base na hora local do computador.

O arquivo deve ser aberto com a função [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) usando o \_ acesso a atributos de gravação de arquivo \_ .


```C++
#include <windows.h>

// SetFileToCurrentTime - sets last write time to current system time
// Return value - TRUE if successful, FALSE otherwise
// hFile  - must be a valid file handle

BOOL SetFileToCurrentTime(HANDLE hFile)
{
    FILETIME ft;
    SYSTEMTIME st;
    BOOL f;

    GetSystemTime(&st);              // Gets the current system time
    SystemTimeToFileTime(&st, &ft);  // Converts the current system time to file time format
    f = SetFileTime(hFile,           // Sets last-write time of the file 
        (LPFILETIME) NULL,           // to the converted current system time 
        (LPFILETIME) NULL, 
        &ft);    

    return f;
}
```



 

 
