---
description: O exemplo a seguir usa as funções RegQueryInfoKey, RegEnumKeyEx e RegEnumValue para enumerar as subchaves da chave especificada.
ms.assetid: 3730180a-52bc-4382-83ca-39f162273ba5
title: Enumerando subchaves do registro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 81aa61dbcbfe487298725de0ac17e1367639da93
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105756352"
---
# <a name="enumerating-registry-subkeys"></a><span data-ttu-id="c6ada-103">Enumerando subchaves do registro</span><span class="sxs-lookup"><span data-stu-id="c6ada-103">Enumerating Registry Subkeys</span></span>

<span data-ttu-id="c6ada-104">O exemplo a seguir usa as funções [**RegQueryInfoKey**](/windows/desktop/api/Winreg/nf-winreg-regqueryinfokeya), [**RegEnumKeyEx**](/windows/desktop/api/Winreg/nf-winreg-regenumkeyexa)e [**RegEnumValue**](/windows/desktop/api/Winreg/nf-winreg-regenumvaluea) para enumerar as subchaves da chave especificada.</span><span class="sxs-lookup"><span data-stu-id="c6ada-104">The following example uses the [**RegQueryInfoKey**](/windows/desktop/api/Winreg/nf-winreg-regqueryinfokeya), [**RegEnumKeyEx**](/windows/desktop/api/Winreg/nf-winreg-regenumkeyexa), and [**RegEnumValue**](/windows/desktop/api/Winreg/nf-winreg-regenumvaluea) functions to enumerate the subkeys of the specified key.</span></span> <span data-ttu-id="c6ada-105">O parâmetro hKey passado para cada função é um identificador para uma chave aberta.</span><span class="sxs-lookup"><span data-stu-id="c6ada-105">The hKey parameter passed to each function is a handle to an open key.</span></span> <span data-ttu-id="c6ada-106">Essa chave deve ser aberta antes da chamada de função e fechada posteriormente.</span><span class="sxs-lookup"><span data-stu-id="c6ada-106">This key must be opened before the function call and closed afterward.</span></span>


```C++
// QueryKey - Enumerates the subkeys of key and its associated values.
//     hKey - Key whose subkeys and values are to be enumerated.

#include <windows.h>
#include <stdio.h>
#include <tchar.h>

#define MAX_KEY_LENGTH 255
#define MAX_VALUE_NAME 16383
 
void QueryKey(HKEY hKey) 
{ 
    TCHAR    achKey[MAX_KEY_LENGTH];   // buffer for subkey name
    DWORD    cbName;                   // size of name string 
    TCHAR    achClass[MAX_PATH] = TEXT("");  // buffer for class name 
    DWORD    cchClassName = MAX_PATH;  // size of class string 
    DWORD    cSubKeys=0;               // number of subkeys 
    DWORD    cbMaxSubKey;              // longest subkey size 
    DWORD    cchMaxClass;              // longest class string 
    DWORD    cValues;              // number of values for key 
    DWORD    cchMaxValue;          // longest value name 
    DWORD    cbMaxValueData;       // longest value data 
    DWORD    cbSecurityDescriptor; // size of security descriptor 
    FILETIME ftLastWriteTime;      // last write time 
 
    DWORD i, retCode; 
 
    TCHAR  achValue[MAX_VALUE_NAME]; 
    DWORD cchValue = MAX_VALUE_NAME; 
 
    // Get the class name and the value count. 
    retCode = RegQueryInfoKey(
        hKey,                    // key handle 
        achClass,                // buffer for class name 
        &cchClassName,           // size of class string 
        NULL,                    // reserved 
        &cSubKeys,               // number of subkeys 
        &cbMaxSubKey,            // longest subkey size 
        &cchMaxClass,            // longest class string 
        &cValues,                // number of values for this key 
        &cchMaxValue,            // longest value name 
        &cbMaxValueData,         // longest value data 
        &cbSecurityDescriptor,   // security descriptor 
        &ftLastWriteTime);       // last write time 
 
    // Enumerate the subkeys, until RegEnumKeyEx fails.
    
    if (cSubKeys)
    {
        printf( "\nNumber of subkeys: %d\n", cSubKeys);

        for (i=0; i<cSubKeys; i++) 
        { 
            cbName = MAX_KEY_LENGTH;
            retCode = RegEnumKeyEx(hKey, i,
                     achKey, 
                     &cbName, 
                     NULL, 
                     NULL, 
                     NULL, 
                     &ftLastWriteTime); 
            if (retCode == ERROR_SUCCESS) 
            {
                _tprintf(TEXT("(%d) %s\n"), i+1, achKey);
            }
        }
    } 
 
    // Enumerate the key values. 

    if (cValues) 
    {
        printf( "\nNumber of values: %d\n", cValues);

        for (i=0, retCode=ERROR_SUCCESS; i<cValues; i++) 
        { 
            cchValue = MAX_VALUE_NAME; 
            achValue[0] = '\0'; 
            retCode = RegEnumValue(hKey, i, 
                achValue, 
                &cchValue, 
                NULL, 
                NULL,
                NULL,
                NULL);
 
            if (retCode == ERROR_SUCCESS ) 
            { 
                _tprintf(TEXT("(%d) %s\n"), i+1, achValue); 
            } 
        }
    }
}

int __cdecl _tmain()
{
   HKEY hTestKey;

   if( RegOpenKeyEx( HKEY_CURRENT_USER,
        TEXT("SOFTWARE\\Microsoft"),
        0,
        KEY_READ,
        &hTestKey) == ERROR_SUCCESS
      )
   {
      QueryKey(hTestKey);
   }
   
   RegCloseKey(hTestKey);
}
```



 

 



