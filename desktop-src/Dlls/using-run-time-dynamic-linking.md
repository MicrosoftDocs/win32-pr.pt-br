---
description: Você pode usar a mesma DLL em vinculação dinâmica e em tempo de carregamento e em tempo de execução.
ms.assetid: 0ffce2b1-ce50-4550-aa68-6628fdcac01a
title: Usando Run-Time vinculação dinâmica
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c8c13cc66a34f0fd5938fcdada027b30223ebff0abe6e9ce459d60f93a6546f2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119255976"
---
# <a name="using-run-time-dynamic-linking"></a>Usando Run-Time vinculação dinâmica

Você pode usar a mesma DLL em vinculação dinâmica e em tempo de carregamento e em tempo de execução. O exemplo a seguir usa a função [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) para obter um identificador para a dll mycolocar (consulte [criando uma biblioteca simples de Dynamic-Link](creating-a-simple-dynamic-link-library.md)). Se **LoadLibrary** for executado com sucesso, o programa usará o identificador retornado na função [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) para obter o endereço da função mycoloque da dll. Depois de chamar a função DLL, o programa chama a função [**FreeLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-freelibrary) para descarregar a dll.

Como o programa usa vinculação dinâmica em tempo de execução, não é necessário vincular o módulo a uma biblioteca de importação para a DLL.

Este exemplo ilustra uma diferença importante entre a vinculação dinâmica em tempo de execução e em tempo de carregamento. Se a DLL não estiver disponível, o aplicativo que usa vinculação dinâmica de tempo de carregamento deverá ser encerrado. O exemplo de vinculação dinâmica em tempo de execução, no entanto, pode responder ao erro.


```C++
// A simple program that uses LoadLibrary and 
// GetProcAddress to access myPuts from Myputs.dll. 
 
#include <windows.h> 
#include <stdio.h> 
 
typedef int (__cdecl *MYPROC)(LPWSTR); 
 
int main( void ) 
{ 
    HINSTANCE hinstLib; 
    MYPROC ProcAdd; 
    BOOL fFreeResult, fRunTimeLinkSuccess = FALSE; 
 
    // Get a handle to the DLL module.
 
    hinstLib = LoadLibrary(TEXT("MyPuts.dll")); 
 
    // If the handle is valid, try to get the function address.
 
    if (hinstLib != NULL) 
    { 
        ProcAdd = (MYPROC) GetProcAddress(hinstLib, "myPuts"); 
 
        // If the function address is valid, call the function.
 
        if (NULL != ProcAdd) 
        {
            fRunTimeLinkSuccess = TRUE;
            (ProcAdd) (L"Message sent to the DLL function\n"); 
        }
        // Free the DLL module.
 
        fFreeResult = FreeLibrary(hinstLib); 
    } 

    // If unable to call the DLL function, use an alternative.
    if (! fRunTimeLinkSuccess) 
        printf("Message printed from executable\n"); 

    return 0;

}
```



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Vinculação dinâmica em tempo de execução](run-time-dynamic-linking.md)
</dt> </dl>

 

 
