---
title: Exemplo de redirecionamento do Registro no WOW64
description: O código de exemplo a seguir demonstra as exibições separadas do Registro fornecidas pelo redirecionador do Registro em 64 bits Windows.
ms.assetid: b3ca2a47-402d-4e91-88bc-ddda6c776468
keywords:
- exemplos de programação Windows 64 bits
- Exemplos de Windows de programação de 64 bits Windows programação
- Exemplos de Windows de programação de 64 Windows de 64 bits, redirecionamento de registro no WOW64
- exemplo de redirecionamento de registro de 64 bits Windows programação
- Guia de programação Windows de 64 bits Windows de 64 bits, exemplos Consulte exemplos de guia Windows programação de 64 bits
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 83428edb31e53bdd1c70825c7fa5a4d799a36536fa9c17f9ce1c4587ab096048
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119680218"
---
# <a name="example-of-registry-redirection-on-wow64"></a>Exemplo de redirecionamento do Registro no WOW64

O código de exemplo a seguir demonstra as exibições separadas do Registro fornecidas pelo redirecionador do Registro em 64 bits Windows. Ele também demonstra como os valores de chaves são definidos dependendo se uma chave é compartilhada ou redirecionada. Para obter mais informações, consulte [Chaves do Registro afetadas pelo WOW64.](shared-registry-keys.md)

Compile o código a seguir separadamente para 32 bits e 64 bits Windows. Execute cada arquivo executável resultante em uma Windows de 64 bits e compare a saída. A saída de exemplo para ambas as versões está listada abaixo do código-fonte.


```C++
#include <windows.h>
#include <stdio.h>

#pragma comment(lib, "advapi32.lib")

// Define application constants.
#if defined(_WIN64)

#define VIEW_DATA L"Hello! 64-bit World"
#define ALT_VIEW_DATA L"Hello! 32-bit World"
#define CROSS_ACCESS KEY_WOW64_32KEY

#else

#define VIEW_DATA L"Hello! 32-bit World"
#define ALT_VIEW_DATA L"Hello! 64-bit World"
#define CROSS_ACCESS KEY_WOW64_64KEY

#endif

// Create a registry key and set its value.
// Return TRUE if the function succeeds, FALSE if it fails.
BOOL
    CreateRegistryKeyValue(
        HKEY hKeyParent,
        PWCHAR KeyName,
        REGSAM rsAccessMask,
        REGSAM rsSamViewFlag,
        PBYTE pValue,
        DWORD dwValueSize
        )
{
    DWORD dwDisposition;
    HKEY  hKey;
    DWORD dwRet;

    dwRet = 
        RegCreateKeyEx(
            hKeyParent,
            KeyName,
            0,
            NULL,
            REG_OPTION_NON_VOLATILE,
            rsAccessMask | rsSamViewFlag,
            NULL,
            &hKey,
            &dwDisposition);

    if (dwRet != ERROR_SUCCESS)
    {
        printf("Error opening or creating key.\n");
        return FALSE;
    }

    // Attempt to set the value of the key.
    // If the call fails, close the key and return.
    if (ERROR_SUCCESS !=
            RegSetValueEx(
                hKey,
                NULL,
                0,
                REG_SZ,
                pValue,
                dwValueSize))
    {
        printf("Could not set registry value.\n");
        RegCloseKey(hKey);
        return FALSE;
    }

    RegCloseKey(hKey);
    return TRUE;
}

// Access a registry key and print its value.
// Return TRUE if the function succeeds, FALSE if it fails.
BOOL
    AccessRegistryKeyValue(
        HKEY hKeyParent,
        PWCHAR KeyName,
        REGSAM rsAccessMask,
        REGSAM rsSamViewFlag
        )
{
    HKEY hKey;
    WCHAR Buffer[MAX_PATH];
    DWORD dwSize = sizeof(Buffer);
    DWORD dwType;
    DWORD dwRet;

    dwRet =
        RegOpenKeyEx(
            hKeyParent,
            KeyName,
            0,
            rsAccessMask | rsSamViewFlag,
            &hKey);

    if (dwRet != ERROR_SUCCESS)
    {
        printf("Error opening key!\n");
        return FALSE;
    }

    if (ERROR_SUCCESS !=
            RegQueryValueEx(
                hKey,
                NULL,
                0,
                &dwType,
                (PBYTE)Buffer,
                &dwSize))
    {
        printf("Could not read registry value.\n");
        RegCloseKey(hKey);
        return FALSE;
    }

    if (rsSamViewFlag != 0)
    {
        printf("Alternate view:   %S\n", Buffer);
    }
    else
    {
        printf("Default view:     %S\n", Buffer);
    }

    RegCloseKey(hKey);
    return TRUE;
}

int
main()
{
    BOOL Res;

    // Define the list of keys to work with.
    typedef struct {
        HKEY hkRoot;
        LPWSTR szRootName;
        LPWSTR szName;
    }KEYDATA;

    KEYDATA Keys[] =
    {
        { HKEY_LOCAL_MACHINE, L"HKLM", L"Software\\Hello World" },
        { HKEY_CLASSES_ROOT,  L"HKCR", L"Hello" },
        { HKEY_CLASSES_ROOT,  L"HKCR", L"CLSID\\{00000000-0000-0000-0000-ABCD00000000}" },
        { HKEY_CLASSES_ROOT,  L"HKCR", L"CLSID\\{00000000-0000-0000-0000-ABCD00000000}\\InprocServer32" },
        { HKEY_CLASSES_ROOT,  L"HKCR", L"CLSID\\{00000000-0000-0000-0000-ABCD00000000}\\LocalServer32" }
    };

    // Now create the keys.
    for (int i = 0; i < _countof(Keys); i++)
    {
        // Create the keys in the alternate view of the registry.
        Res = 
            CreateRegistryKeyValue(
                Keys[i].hkRoot,
                Keys[i].szName,
                KEY_READ | KEY_WRITE,
                CROSS_ACCESS,
                (PBYTE)ALT_VIEW_DATA,
                sizeof(ALT_VIEW_DATA));
        if (Res == FALSE)
        {
            printf("Could not create keys in alternate view of the registry.\n");
            return 1; 
       }

        // Create the keys in the default view of the registry.
        Res = 
            CreateRegistryKeyValue(
                Keys[i].hkRoot,
                Keys[i].szName,
                KEY_READ | KEY_WRITE,
                0,
                (PBYTE)VIEW_DATA,
                sizeof(VIEW_DATA));
        if (Res == FALSE)
        {
            printf("Could not create keys in default view of the registry.\n");
            return 1;
        }
    }

    // Access the registry and print key values.
    printf("Application string: %S\n", VIEW_DATA);

    for (int i = 0; i < _countof(Keys); i++)
    {
        printf("%S\\%S\n", Keys[i].szRootName, Keys[i].szName);
        Res = 
            AccessRegistryKeyValue(
                Keys[i].hkRoot,
                Keys[i].szName,
                KEY_READ, 
                0);
        if (Res == FALSE)
        {
            printf("Unable to access default view of registry.\n");
            return 1;
        }

        // Calls with CROSS_ACCESS explicitly access the alternate registry view.
        Res =
            AccessRegistryKeyValue(
                Keys[i].hkRoot,
                Keys[i].szName,
                KEY_READ,
                CROSS_ACCESS);
        if (Res == FALSE)
        {
            printf("Unable to access alternate view of registry.\n");
            return 1;
        }
    }
    return 0;
}
```



Quando a versão de 64 bits do exemplo é executado, ela produz a saída a seguir. Os valores das exibições padrão e alternativa do **HKCR \\ Hello** são os mesmos porque essa chave é compartilhada. Os valores das outras chaves diferem porque são redirecionados.

**Windows Server 2008, Windows Vista, Windows Server 2003 e Windows XP:** Quando este exemplo é executado nesses sistemas operacionais, as exibições padrão e alternativa da chave LocalServer32 têm o mesmo valor. Isso porque a chave LocalServer32 é redirecionada e refletida, o que faz com que seu valor seja sincronizado entre as exibições de 64 bits e 32 bits do Registro assim que o alçamento para a chave for fechado. A reflexão do Registro foi removida do Windows 7. Para obter mais informações, consulte [Reflexão do Registro.](registry-reflection.md)

``` syntax
Application string: Hello! 64-bit World
HKLM\Software\Hello World
Default view:     Hello! 64-bit World
Alternate view:   Hello! 32-bit World
HKCR\Hello
Default view:     Hello! 64-bit World
Alternate view:   Hello! 64-bit World
HKCR\CLSID\{00000000-0000-0000-0000-ABCD00000000}
Default view:     Hello! 64-bit World
Alternate view:   Hello! 32-bit World
HKCR\CLSID\{00000000-0000-0000-0000-ABCD00000000}\InprocServer32
Default view:     Hello! 64-bit World
Alternate view:   Hello! 32-bit World
HKCR\CLSID\{00000000-0000-0000-0000-ABCD00000000}\LocalServer32
Default view:     Hello! 64-bit World
Alternate view:   Hello! 32-bit World
```

Quando a versão de 32 bits do exemplo é executado, ela produz a saída a seguir. Para um aplicativo de 32 bits, a exibição de 64 bits do Registro é a exibição alternativa para que os valores sejam invertidos, exceto para HKCR Hello, que é uma chave \\ compartilhada.

``` syntax
Application string: Hello! 32-bit World
HKLM\Software\Hello World
Default view:     Hello! 32-bit World
Alternate view:   Hello! 64-bit World
HKCR\Hello
Default view:     Hello! 32-bit World
Alternate view:   Hello! 32-bit World
HKCR\CLSID\{00000000-0000-0000-0000-ABCD00000000}
Default view:     Hello! 32-bit World
Alternate view:   Hello! 64-bit World
HKCR\CLSID\{00000000-0000-0000-0000-ABCD00000000}\InprocServer32
Default view:     Hello! 32-bit World
Alternate view:   Hello! 64-bit World
HKCR\CLSID\{00000000-0000-0000-0000-ABCD00000000}\LocalServer32
Default view:     Hello! 32-bit World
Alternate view:   Hello! 64-bit World
```

Para examinar o efeito de executar este exemplo com regedit, inspecione os valores das chaves a seguir. Observe que os aplicativos devem evitar usar Wow6432Node em caminhos de registro codificados.

**HKLM \\ SOFTWARE \\ Olá, Mundo**  
**HKLM \\ SOFTWARE \\ Wow6432Node \\ Olá, Mundo**  
**\\CLSID do HKCR \\ {00000000-0000-0000-0000-ABCD0000000}**  
**CLSID do HKCR \\ \\ {00000000-0000-0000-0000-ABCD0000000} \\ InprocServer32**  
**\\CLSID do HKCR \\ {00000000-0000-0000-0000-ABCD0000000} \\ LocalServer32**  
**HKCR \\ Hello HKCR \\ Wow6432Node \\ CLSID \\ {00000000-0000-0000-0000-ABCD0000000}**  
**\\HKCR Wow6432Node \\ CLSID \\ {00000000-0000-0000-0000-ABCD0000000} \\ InprocServer32**  
**\\HKCR Wow6432Node \\ CLSID \\ {00000000-0000-0000-0000-ABCD0000000} \\ LocalServer32**  
**HKCR \\ Wow6432Node \\ Hello**  


## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Redirecionador de Registro](registry-redirector.md)
</dt> <dt>

[Reflexão do Registro](registry-reflection.md)
</dt> </dl>

 

 




