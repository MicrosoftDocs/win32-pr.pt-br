---
description: a função MsiGetPatchFileList e a propriedade PatchFiles do objeto instalador usam uma lista de patches Windows Installer (arquivos. msp) e retornam uma lista de arquivos que podem ser atualizados pelos patches.
ms.assetid: cc2eb506-c1fc-4125-b98c-12221b918e23
title: Listando os arquivos que podem ser atualizados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6ad76355c97d62d9c3f1282b5ebd66f54c5fef0f6f7359a41a35f2ebaee9a2fd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118945901"
---
# <a name="listing-the-files-that-can-be-updated"></a>Listando os arquivos que podem ser atualizados

a função [**MsiGetPatchFileList**](/windows/desktop/api/Msi/nf-msi-msigetpatchfilelista) e a propriedade [**PatchFiles**](installer-patchfiles.md) do [**objeto instalador**](installer-object.md) usam uma lista de patches Windows Installer (arquivos. msp) e retornam uma lista de arquivos que podem ser atualizados pelos patches. a função [**MsiGetPatchFileList**](/windows/desktop/api/Msi/nf-msi-msigetpatchfilelista) e a propriedade [**PatchFiles**](installer-patchfiles.md) estão disponíveis a partir do Windows Installer 4,0.

## <a name="listing-files-that-can-be-updated"></a>Listando arquivos que podem ser atualizados

o exemplo a seguir mostra como extrair as informações de aplicabilidade para uma lista de patches de Windows Installer (arquivos. msp) usando o [**MsiGetPatchFileList**](/windows/desktop/api/Msi/nf-msi-msigetpatchfilelista). A função **MsiGetPatchFileList** fornece o código do produto para o destino dos patches e uma lista de arquivos. msp delimitadas por ponto e vírgula. este exemplo requer Windows Installer 4,0 em execução no Windows Vista.


```C++
#include <windows.h>
#include <stdio.h>
#include <Shellapi.h>
#include <msi.h>
#include <Msiquery.h>
#pragma comment(lib, "msi.lib")
#pragma comment(lib, "shell32.lib")

void CloseMsiHandles(MSIHANDLE* phFileListRec, DWORD dwcFiles);

int __cdecl main()
{
    UINT uiRet = ERROR_SUCCESS;
    int argc;
    WCHAR** argv = CommandLineToArgvW(GetCommandLine(), &argc);
    
    MSIHANDLE *phFileListRec = NULL;
    DWORD dwcFiles = 0;
    WCHAR* szProductCode = argv[1];
    WCHAR* szPatchFileList = argv[2];
    if(ERROR_SUCCESS != (uiRet = MsiGetPatchFileList(szProductCode, szPatchFileList, &dwcFiles, &phFileListRec)))
    {
        printf("MsiGetPatchFileListW(%S, ...) Failed with:%d", szProductCode, uiRet);
        return uiRet;
    }
    
    DWORD cchBuf = 1;
    DWORD cchBufSize = 1;
    WCHAR* szBuf = new WCHAR[cchBufSize];
    if (!szBuf)
    {
        printf("Failed to allocate memory");
        CloseMsiHandles(phFileListRec, dwcFiles);
        return ERROR_OUTOFMEMORY;
    }
    memset(szBuf, 0, sizeof(WCHAR)*cchBufSize);
    
    for(unsigned int i = 0; i < dwcFiles; i++)
    {
        cchBuf = cchBufSize;
        while(ERROR_MORE_DATA == (uiRet = MsiRecordGetString(phFileListRec[i], 0, szBuf, &cchBuf)))
        {
            if (szBuf)
                delete[] szBuf;
            cchBufSize = ++cchBuf;
            szBuf = new WCHAR[cchBufSize];
            if (!szBuf)
            {
                printf("Failed to allocate memory");
                CloseMsiHandles(phFileListRec, dwcFiles);
                return ERROR_OUTOFMEMORY;
            }
        }
        
        if(uiRet != ERROR_SUCCESS)
        {
            printf("MsiRecordGetString(phFileListRec[%d] with %d", i, uiRet);
            CloseMsiHandles(phFileListRec, dwcFiles);
            if (szBuf)
                delete[] szBuf;
            return uiRet;
        }
        else
        {
            printf("File %d:%S\n", i, szBuf);
        }            
    }

    CloseMsiHandles(phFileListRec, dwcFiles);
    if (szBuf)
        delete[] szBuf;
    return 0;
}

void CloseMsiHandles(MSIHANDLE* phFileListRec, DWORD dwcFiles)
{
    if (!phFileListRec)
        return;
    
    for (unsigned int i = 0; i < dwcFiles; i++)
    {
        if (phFileListRec[i])
            MsiCloseHandle(phFileListRec[i]);
    }    
}
//
```



o exemplo a seguir mostra como extrair as informações de aplicabilidade para uma lista de patches de Windows Installer (arquivos. msp) usando a propriedade [**PatchFiles**](installer-patchfiles.md) do [**objeto do instalador**](installer-object.md). A propriedade **PatchFiles** fornece o código do produto para o destino dos patches e uma lista de arquivos. msp delimitadas por ponto e vírgula. este exemplo requer Windows Installer 4,0 em execução no Windows Vista.


```VB
Dim FileList
Dim installer : Set installer = Nothing
Dim argCount:argCount = Wscript.Arguments.Count

Set installer = Wscript.CreateObject("WindowsInstaller.Installer")

If (argCount > 0) Then
    sProdCode = Wscript.Arguments(0)
    sPatchPckgPath = Wscript.Arguments(1)
    Set FileList = installer.PatchFiles (sProdCode, sPatchPckgPath)
    For each File in FileList
           Wscript.Echo "Affected file: " & File
    Next
Else
    Usage
End If

Sub Usage
    Wscript.Echo "Windows Installer utility to list files updated by a patch for an installed product" &_
    vbNewLine & " 1st argument is the product code (GUID) of an installed product" &_
    vbNewLine & " 2nd argument is the list of patches" &_
    vbNewLine &_
    vbNewLine & "Copyright (C) Microsoft. All rights reserved."
    Wscript.Quit 1
End Sub
```



 

 



