---
description: Uma interface do usuário personalizada pode ser inserida no pacote de Windows Installer.
ms.assetid: d037cd8d-9c88-4851-a9da-b2179f53cee6
title: Usando uma interface do usuário inserida
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f187e50461cfe88adc9c2cabbf8dd8b88ca97a5a
ms.sourcegitcommit: 7b8f6151ebe247536304866459b2973276271d4d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/06/2021
ms.locfileid: "104011983"
---
# <a name="using-an-embedded-ui"></a><span data-ttu-id="c3327-103">Usando uma interface do usuário inserida</span><span class="sxs-lookup"><span data-stu-id="c3327-103">Using an Embedded UI</span></span>

<span data-ttu-id="c3327-104">Uma interface do usuário personalizada pode ser inserida no pacote de Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="c3327-104">A custom user interface can be embedded within the Windows Installer package.</span></span>

<span data-ttu-id="c3327-105">O arquivo DLL que contém a interface do usuário personalizada e todos os arquivos de recursos usados pela interface do usuário personalizada devem ser listados na tabela [MsiEmbeddedUI](msiembeddedui-table.md) .</span><span class="sxs-lookup"><span data-stu-id="c3327-105">The DLL file containing the custom UI, and any resource files used by the custom UI, should be listed in the [MsiEmbeddedUI](msiembeddedui-table.md) table.</span></span> <span data-ttu-id="c3327-106">Por exemplo, essa tabela MsiEmbeddedUI contém uma linha para o arquivo DLL que contém a interface do usuário inserida e uma linha para um arquivo de bitmap usado pela interface do usuário.</span><span class="sxs-lookup"><span data-stu-id="c3327-106">For example, this MsiEmbeddedUI table contains a row for the DLL file containing the embedded UI and a row for a bitmap file used by the UI.</span></span>

| <span data-ttu-id="c3327-107">MsiEmbeddedUI</span><span class="sxs-lookup"><span data-stu-id="c3327-107">MsiEmbeddedUI</span></span> | <span data-ttu-id="c3327-108">FileName</span><span class="sxs-lookup"><span data-stu-id="c3327-108">FileName</span></span>    | <span data-ttu-id="c3327-109">Atributos</span><span class="sxs-lookup"><span data-stu-id="c3327-109">Attributes</span></span> | <span data-ttu-id="c3327-110">MessageFilter</span><span class="sxs-lookup"><span data-stu-id="c3327-110">MessageFilter</span></span> | <span data-ttu-id="c3327-111">Dados</span><span class="sxs-lookup"><span data-stu-id="c3327-111">Data</span></span>            |
|---------------|-------------|------------|---------------|-----------------|
| <span data-ttu-id="c3327-112">EmbeddedUI</span><span class="sxs-lookup"><span data-stu-id="c3327-112">EmbeddedUI</span></span>    | <span data-ttu-id="c3327-113">embedui.dll</span><span class="sxs-lookup"><span data-stu-id="c3327-113">embedui.dll</span></span> | <span data-ttu-id="c3327-114">3</span><span class="sxs-lookup"><span data-stu-id="c3327-114">3</span></span>          | <span data-ttu-id="c3327-115">201359327</span><span class="sxs-lookup"><span data-stu-id="c3327-115">201359327</span></span>     | <span data-ttu-id="c3327-116">\[Binary Data\]</span><span class="sxs-lookup"><span data-stu-id="c3327-116">\[Binary Data\]</span></span> |
| <span data-ttu-id="c3327-117">CustomBitmap</span><span class="sxs-lookup"><span data-stu-id="c3327-117">CustomBitmap</span></span>  | <span data-ttu-id="c3327-118">custom.bmp</span><span class="sxs-lookup"><span data-stu-id="c3327-118">custom.bmp</span></span>  | <span data-ttu-id="c3327-119">0</span><span class="sxs-lookup"><span data-stu-id="c3327-119">0</span></span>          |               | <span data-ttu-id="c3327-120">\[Binary Data\]</span><span class="sxs-lookup"><span data-stu-id="c3327-120">\[Binary Data\]</span></span> |



 

<span data-ttu-id="c3327-121">O DLL da interface do usuário personalizada, neste exemplo embedui.dll, deve exportar as funções *InitializeEmbeddedUI*, *EmbeddedUIHandler* e *ShutdownEmbeddedUI* definidas pelo usuário.</span><span class="sxs-lookup"><span data-stu-id="c3327-121">The custom UI DLL, in this example embedui.dll, should export the user-defined *InitializeEmbeddedUI*, *EmbeddedUIHandler*, and *ShutdownEmbeddedUI* functions.</span></span> <span data-ttu-id="c3327-122">O código de exemplo a seguir ilustra essas funções.</span><span class="sxs-lookup"><span data-stu-id="c3327-122">The following sample code illustrates these functions.</span></span>


```C++
#include <stdio.h>
#include <stdlib.h>
#include <windows.h>
#include <msi.h>
#include <msiquery.h>
#include <Aclapi.h>
#include <strsafe.h>
#pragma comment(lib, "msi.lib")

#define cchGUID 38

int __stdcall InitializeEmbeddedUI(MSIHANDLE hInstall, 
        LPCWSTR szResourcePath, LPDWORD pdwInternalUILevel)
{
    // The hInstall handle is only valid within this function and 
     // can be used to get or set properties. The handle 
    // does not need to be explicitly closed.

    WCHAR szProductCode[cchGUID+1];
    DWORD cchProductCode = ARRAYSIZE(szProductCode);
    UINT uiStat =  MsiGetProperty(hInstall, L"ProductCode",
             szProductCode, &cchProductCode);
    UNREFERENCED_PARAMETER(szResourcePath);

    if (ERROR_SUCCESS != uiStat)
    {
        // The installation should fail.
        return ERROR_INSTALL_FAILURE;
    }

    WCHAR* szReinstall = NULL;
    DWORD cchReinstall = 0;
    uiStat = MsiGetProperty(hInstall, TEXT("REINSTALL"),  
            szReinstall, &cchReinstall);
    if (ERROR_MORE_DATA == uiStat)
    {
        ++cchProductCode; // Add 1 for terminating null character.
        szReinstall = new WCHAR[cchReinstall];
        if (szReinstall)
        {
        uiStat = MsiGetProperty(hInstall, L"REINSTALL", 
                szReinstall, &cchReinstall);
        }
    }
    if (ERROR_SUCCESS != uiStat)
    {
        if (szReinstall != NULL) 
            delete [] szReinstall;
        // This installation should fail.
        return ERROR_INSTALL_FAILURE;
    }

    if (INSTALLSTATE_DEFAULT != MsiQueryProductState(szProductCode))
    {
        if (INSTALLUILEVEL_BASIC == *pdwInternalUILevel)
        {
            // Insert the custom UI used by basic installation here.
        }
        else
        {
            // Insert the custom UI used by full installation here.
        }
    }
    else if (szReinstall && szReinstall[0])
    {
        // Reinstall the UI sequence.
    }
    else
    {
        // This is a maintenance installation. Remove the UI sequence.

        MsiSetProperty(hInstall, TEXT("REMOVE"), TEXT("ALL"));
    }

    if (szProductCode)
        delete [] szReinstall;

    // Setting the internal UI level to none specifies that 
    // no authored UI should run.
    *pdwInternalUILevel = INSTALLUILEVEL_NONE;
    return 0;
}

DWORD __stdcall ShutdownEmbeddedUI()
{
    // ShutdownEmbeddedUI is optional. It can allow the embedded UI 
    // to perform any cleanup. After this call, the embedded UI   
    // should not receive any additional callbacks.
    return 0;
}


INT __stdcall EmbeddedUIHandler(UINT iMessageType, MSIHANDLE hRecord)
{
    // This function is similar to the MsiSetExternalUIRecord callback.
    INSTALLMESSAGE mt;
    UINT uiFlags;
    UNREFERENCED_PARAMETER(hRecord);

    mt = (INSTALLMESSAGE) (0xFF000000 & (UINT) iMessageType);
    uiFlags = 0x00FFFFFF & iMessageType;

    switch (mt)
    {
    case INSTALLMESSAGE_FATALEXIT:
        {
            return IDOK;
        }
    case INSTALLMESSAGE_ERROR:
        {
            return IDOK;
        }
    case INSTALLMESSAGE_WARNING:
        {
            return IDOK;
        }
    case INSTALLMESSAGE_FILESINUSE:
        {
            return IDOK;
        }
    case INSTALLMESSAGE_RESOLVESOURCE:
        {
            return IDOK;
        }
    case INSTALLMESSAGE_USER:
        {
            return IDOK;
        }
    case INSTALLMESSAGE_INFO:
        {
            return IDOK;
        }
    case INSTALLMESSAGE_OUTOFDISKSPACE:
        {
            return IDOK;
        }
    case INSTALLMESSAGE_ACTIONSTART:
        {
            return IDOK;
        }
    case INSTALLMESSAGE_ACTIONDATA:
        {
            return IDOK;
        }
    case INSTALLMESSAGE_PROGRESS:
        {
            return IDOK;
        }
    case INSTALLMESSAGE_SHOWDIALOG:
        {
            return IDOK;
        }
    case INSTALLMESSAGE_COMMONDATA:
        {
            return IDOK;
        }
    case INSTALLMESSAGE_INSTALLSTART:
        {
            // This message is sent when the Install begins.
            // Record contains the ProductName and ProductCode
            return IDOK;
        }
    case INSTALLMESSAGE_INSTALLEND:
        {
            // This message is sent when the Install ends.
            // Record contains the ProductName and ProductCode 
            // and return value of the installation.
            return IDOK;
        }

    default:
        {
            return 0;
        }
    }
}
```



 

 



