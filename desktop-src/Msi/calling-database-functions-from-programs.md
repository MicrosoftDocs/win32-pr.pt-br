---
description: Antes de chamar qualquer uma das seguintes funções de banco de dados de um programa, como uma ação personalizada ou um processo de automação, o instalador deve primeiro executar a ação CostInitialize, a ação de filecusto e a ação CostFinalize.
ms.assetid: b9795825-41fa-474b-a0c5-06770aa99bc1
title: Chamando funções de banco de dados de programas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1959e43b680d84e04de1f68483e8a1016bbeca0e867daebf10a317838d68c0ce
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119145699"
---
# <a name="calling-database-functions-from-programs"></a>Chamando funções de banco de dados de programas

Antes de chamar qualquer uma das seguintes [funções de banco de dados](database-functions.md) de um programa, como uma ação personalizada ou um processo de automação, o instalador deve primeiro executar a ação [CostInitialize](costinitialize-action.md), a [ação de filecusto](filecost-action.md)e a [ação CostFinalize](costfinalize-action.md).

veja a seguir uma lista de funções de banco de dados usadas no Windows Installer:

-   [**MsiGetComponentState**](/windows/desktop/api/Msiquery/nf-msiquery-msigetcomponentstatea)
-   [**MsiGetFeatureCost**](/windows/desktop/api/Msiquery/nf-msiquery-msigetfeaturecosta)
-   [**MsiGetFeatureState**](/windows/desktop/api/Msiquery/nf-msiquery-msigetfeaturestatea)
-   [**MsiGetFeatureValidStates**](/windows/desktop/api/Msiquery/nf-msiquery-msigetfeaturevalidstatesa)
-   [**MsiGetSourcePath**](/windows/desktop/api/Msiquery/nf-msiquery-msigetsourcepatha)
-   [**MsiGetTargetPath**](/windows/desktop/api/Msiquery/nf-msiquery-msigettargetpatha)
-   [**MsiSetComponentState**](/windows/desktop/api/Msiquery/nf-msiquery-msisetcomponentstatea)
-   [**MsiSetFeatureState**](/windows/desktop/api/Msiquery/nf-msiquery-msisetfeaturestatea)
-   [**MsiSetInstallLevel**](/windows/desktop/api/Msiquery/nf-msiquery-msisetinstalllevel)
-   [**MsiSetTargetPath**](/windows/desktop/api/Msiquery/nf-msiquery-msisettargetpatha)
-   [**MsiVerifyDiskSpace**](/windows/desktop/api/Msiquery/nf-msiquery-msiverifydiskspace)

Antes de chamar [**MsiSetFeatureAttributes**](/windows/desktop/api/Msiquery/nf-msiquery-msisetfeatureattributesa) de um programa, o instalador deve primeiro executar a ação CostInitialize. Em seguida, o instalador executa a ação CostFinalize após **MsiSetFeatureAttributes**.

O exemplo a seguir ilustra a ordem na qual as ações de função devem ser chamadas ao usar [**MsiGetTargetPath**](/windows/desktop/api/Msiquery/nf-msiquery-msigettargetpatha) em um programa.


```C++
#include <windows.h>
#include <Msiquery.h>
#include <tchar.h>
#pragma comment(lib, "msi.lib") 

int main()  
{ 

MSIHANDLE hInstall;
TCHAR *szBuf;
DWORD cch  = 0 ;
 
if(MsiOpenPackage(_T("PathToPackage...."), &hInstall) == ERROR_SUCCESS)
{
    if(MsiDoAction(hInstall, _T("CostInitialize"))==ERROR_SUCCESS  
        && MsiDoAction(hInstall, _T("FileCost"))==ERROR_SUCCESS  
        && MsiDoAction(hInstall, _T("CostFinalize"))==ERROR_SUCCESS)   
    { 
        if(MsiGetTargetPath(hInstall, _T("FolderName"), _T(""),&cch)==ERROR_MORE_DATA)
        { 
            cch++; // add 1 to include null terminator since MsiGetTargetPath does not include it on return 
            szBuf = (TCHAR *) malloc(cch*sizeof(TCHAR));
            if(szBuf)
            {
                if(MsiGetTargetPath(hInstall, _T("FolderName"), szBuf,&cch)==ERROR_SUCCESS)
                {
                    // Add code to use szBuf here
                }
                free(szBuf);
            }
        } 
    } 
    MsiCloseHandle(hInstall);
}

return 0;  
}
```



 

 



