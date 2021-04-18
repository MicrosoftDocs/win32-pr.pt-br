---
description: Você pode usar a mesma DLL em vinculação dinâmica e em tempo de carregamento e em tempo de execução.
ms.assetid: 0ffce2b1-ce50-4550-aa68-6628fdcac01a
title: Usando Run-Time vinculação dinâmica
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a4d6ca65c510433350b81a282d8bf7a3a3825ef1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105757829"
---
# <a name="using-run-time-dynamic-linking"></a><span data-ttu-id="0f30d-103">Usando Run-Time vinculação dinâmica</span><span class="sxs-lookup"><span data-stu-id="0f30d-103">Using Run-Time Dynamic Linking</span></span>

<span data-ttu-id="0f30d-104">Você pode usar a mesma DLL em vinculação dinâmica e em tempo de carregamento e em tempo de execução.</span><span class="sxs-lookup"><span data-stu-id="0f30d-104">You can use the same DLL in both load-time and run-time dynamic linking.</span></span> <span data-ttu-id="0f30d-105">O exemplo a seguir usa a função [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) para obter um identificador para a dll mycolocar (consulte [criando uma biblioteca simples de Dynamic-Link](creating-a-simple-dynamic-link-library.md)).</span><span class="sxs-lookup"><span data-stu-id="0f30d-105">The following example uses the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) function to get a handle to the Myputs DLL (see [Creating a Simple Dynamic-Link Library](creating-a-simple-dynamic-link-library.md)).</span></span> <span data-ttu-id="0f30d-106">Se **LoadLibrary** for executado com sucesso, o programa usará o identificador retornado na função [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) para obter o endereço da função mycoloque da dll.</span><span class="sxs-lookup"><span data-stu-id="0f30d-106">If **LoadLibrary** succeeds, the program uses the returned handle in the [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) function to get the address of the DLL's myPuts function.</span></span> <span data-ttu-id="0f30d-107">Depois de chamar a função DLL, o programa chama a função [**FreeLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-freelibrary) para descarregar a dll.</span><span class="sxs-lookup"><span data-stu-id="0f30d-107">After calling the DLL function, the program calls the [**FreeLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-freelibrary) function to unload the DLL.</span></span>

<span data-ttu-id="0f30d-108">Como o programa usa vinculação dinâmica em tempo de execução, não é necessário vincular o módulo a uma biblioteca de importação para a DLL.</span><span class="sxs-lookup"><span data-stu-id="0f30d-108">Because the program uses run-time dynamic linking, it is not necessary to link the module with an import library for the DLL.</span></span>

<span data-ttu-id="0f30d-109">Este exemplo ilustra uma diferença importante entre a vinculação dinâmica em tempo de execução e em tempo de carregamento.</span><span class="sxs-lookup"><span data-stu-id="0f30d-109">This example illustrates an important difference between run-time and load-time dynamic linking.</span></span> <span data-ttu-id="0f30d-110">Se a DLL não estiver disponível, o aplicativo que usa vinculação dinâmica de tempo de carregamento deverá ser encerrado.</span><span class="sxs-lookup"><span data-stu-id="0f30d-110">If the DLL is not available, the application using load-time dynamic linking must simply terminate.</span></span> <span data-ttu-id="0f30d-111">O exemplo de vinculação dinâmica em tempo de execução, no entanto, pode responder ao erro.</span><span class="sxs-lookup"><span data-stu-id="0f30d-111">The run-time dynamic linking example, however, can respond to the error.</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="0f30d-112">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="0f30d-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0f30d-113">Vinculação dinâmica em tempo de execução</span><span class="sxs-lookup"><span data-stu-id="0f30d-113">Run-Time Dynamic Linking</span></span>](run-time-dynamic-linking.md)
</dt> </dl>

 

 
