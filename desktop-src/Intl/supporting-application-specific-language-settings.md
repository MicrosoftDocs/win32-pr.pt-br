---
description: Seu aplicativo pode dar suporte a um conjunto diferente de idiomas de interface do usuário daqueles com suporte do sistema operacional de destino. Este tópico discute esse tipo de suporte, usando trechos de código de exemplos completos.
ms.assetid: cb9f2a5f-3bb8-4287-a542-c71d20b37194
title: suporte ao idioma do Application-Specific Configurações
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 96c934ea2f01c37eb2f9e846382447a50ccbedcd9b69fe20069216fa46521b02
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120130056"
---
# <a name="supporting-application-specific-language-settings"></a>suporte ao idioma do Application-Specific Configurações

Seu aplicativo pode dar suporte a um conjunto diferente de idiomas de interface do usuário daqueles com suporte do sistema operacional de destino. Este tópico discute esse tipo de suporte, usando trechos de código de exemplos completos.

## <a name="interpret-users-language-preference"></a>Interpretar a preferência de idioma do usuário

Seu aplicativo deve primeiro determinar qual idioma da interface do usuário será exibido, com base na preferência do usuário. O código pode ler as configurações de um arquivo de configuração ou de configurações do registro.

O exemplo a seguir define duas funções usadas para interpretar a preferência de idioma do usuário. A primeira função ilustra a leitura de uma lista delimitada de idiomas de um arquivo, representado no código como "langs.txt". Os delimitadores com suporte no exemplo são ",", ";"; "." e "". A segunda função converte a cadeia de caracteres lida do arquivo para um valor de cadeia de caracteres múltipla. Essa operação é necessária porque as funções de MUI usadas para definir idiomas aceitam apenas valores de várias cadeias de caracteres.


```C++
BOOL GetMyUserDefinedLanguages(WCHAR * langStr, DWORD langStrSize)
{
    BOOL rtnVal = FALSE;
    // Very simple implementation - assumes that first 'langStrSize' characters of the
    // L".\\langs.txt" file comprises a string of one or more languages.
    HANDLE langConfigFileHandle = CreateFileW(L".\\langs.txt", GENERIC_READ, 0,
                                    NULL, OPEN_EXISTING, FILE_ATTRIBUTE_NORMAL, NULL);
    if(langConfigFileHandle != INVALID_HANDLE_VALUE)
    {
        // Clear the input variables.
        DWORD bytesActuallyRead = 0;
        if(ReadFile(langConfigFileHandle, langStr, langStrSize*sizeof(WCHAR), &bytesActuallyRead, NULL)
           && bytesActuallyRead > 0)
        {
            rtnVal = TRUE;
            DWORD nullIndex = (bytesActuallyRead/sizeof(WCHAR) < langStrSize)
                              ? bytesActuallyRead/sizeof(WCHAR) : langStrSize;
            langStr[nullIndex] = L'\0';
        }
        CloseHandle(langConfigFileHandle);
    }
    return rtnVal;
}
BOOL ConvertMyLangStrToMultiLangStr(WCHAR * langStr, WCHAR * langMultiStr, DWORD langMultiStrSize)
{
    BOOL rtnVal = FALSE;
    size_t strLen = 0;
    rtnVal = SUCCEEDED(StringCchLengthW(langStr, USER_CONFIGURATION_STRING_BUFFER*2, &strLen));
    if(rtnVal && strLen > 0 && langMultiStr && langMultiStrSize > 0)
    {
        WCHAR * langMultiStrPtr = langMultiStr;
        WCHAR * last = langStr + (langStr[0] == 0xFEFF ? 1 : 0);
        WCHAR * context = last;
        WCHAR * next = wcstok_s(last,L",; :",&context);
        while(next && rtnVal)
        {
            // Make sure you validate the user input.
            if(SUCCEEDED(StringCchLengthW(last, LOCALE_NAME_MAX_LENGTH, &strLen))
               && IsValidLocaleName(next))
            {
                langMultiStrPtr[0] = L'\0';
                rtnVal &= SUCCEEDED(StringCchCatW(langMultiStrPtr,
                                    (langMultiStrSize - (langMultiStrPtr - langMultiStr)), next));
                langMultiStrPtr += strLen + 1;
            }
            next = wcstok_s(NULL, L",; :", &context);
            if(next)
                last = next;
        }
        // Make sure there is a double null term for the multi-string.
        if(rtnVal && (langMultiStrSize - (langMultiStrPtr - langMultiStr)))
        {
            langMultiStrPtr[0] = L'\0';
        }
        else // Fail and guard anyone whom might use the multi-string.
        {
            langMultiStr[0] = L'\0';
            langMultiStr[1] = L'\0';
        }
    }
    return rtnVal;
}
```



## <a name="set-the-application-language"></a>Definir o idioma do aplicativo

Depois de ler as informações de preferência de idioma, o código do aplicativo deve usar a configuração recuperada para definir o idioma do aplicativo. no Windows 7 e posterior, o aplicativo pode definir o idioma no nível do processo chamando a função [**SetProcessPreferredUILanguages**](/windows/desktop/api/Winnls/nf-winnls-setprocesspreferreduilanguages) .


```C++
DWORD langCount = 0;
// Using SetProcessPreferredUILanguages is recommended for new applications (esp. multi-threaded applications).
if(!SetProcessPreferredUILanguages(MUI_LANGUAGE_NAME, userLanguagesMultiString, &langCount) || langCount == 0)
{
    swprintf_s(displayBuffer, SUFFICIENTLY_LARGE_ERROR_BUFFER,
               L"FAILURE: Unable to set the user defined languages, last error = %d.", GetLastError());
    MessageBoxW(NULL, displayBuffer, L"HelloMUI ERROR!", MB_OK | MB_ICONERROR);
    return 1; // Exit.
}
```



no Windows Vista e posterior, o idioma do aplicativo é definido no nível do thread chamando a função [**SetThreadPreferredUILanguages**](/windows/desktop/api/Winnls/nf-winnls-setthreadpreferreduilanguages) .


```C++
DWORD langCount = 0;
// The following line of code is supported on Windows Vista and later.
if(!SetThreadPreferredUILanguages(MUI_LANGUAGE_NAME, userLanguagesMultiString, &langCount) || langCount == 0)
{
    swprintf_s(displayBuffer, SUFFICIENTLY_LARGE_ERROR_BUFFER,
               L"FAILURE: Unable to set the user defined languages, last error = %d.", GetLastError());
    MessageBoxW(NULL, displayBuffer, L"HelloMUI ERROR!", MB_OK | MB_ICONERROR);
    return 1; // Exit.
}
return 1;
```



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Definindo preferências de idioma do aplicativo](setting-application-language-preferences.md)
</dt> <dt>

[MUI: exemplo de Configurações de Application-Specific (Windows Vista)](mui-application-specific-settings-sample-vista.md)
</dt> <dt>

[MUI: exemplo de Configurações de Application-Specific (pré-Windows Vista)](mui-application-specific-settings-sample-pre-vista.md)
</dt> </dl>

 

 



