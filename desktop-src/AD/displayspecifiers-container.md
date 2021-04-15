---
title: Contêiner DisplaySpecifiers
description: Os especificadores de exibição são armazenados, por localidade, no contêiner DisplaySpecifiers do contêiner de configuração. Como o contêiner de configuração é replicado em toda a floresta, os especificadores de exibição são propagados em todos os domínios em uma floresta.
ms.assetid: d7647c50-f95c-41ef-8d67-dc72542cae5a
ms.tgt_platform: multiple
keywords:
- Contêiner DisplaySpecifiers
- Contêineres, exibir especificadores
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 406258a6c9983581491420a49621e3d10df4601e
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/17/2020
ms.locfileid: "104453932"
---
# <a name="displayspecifiers-container"></a>Contêiner DisplaySpecifiers

Os especificadores de exibição são armazenados, por localidade, no contêiner DisplaySpecifiers do contêiner de configuração. Como o contêiner de configuração é replicado em toda a floresta, os especificadores de exibição são propagados em todos os domínios em uma floresta.

O contêiner de configuração armazena o contêiner DisplaySpecifiers, que armazena contêineres que correspondem a cada localidade. Esses contêineres de localidade são nomeados usando a representação hexadecimal do identificador de localidade. Por exemplo, o contêiner de localidade dos EUA/inglês é denominado 409, o contêiner da localidade alemão é denominado 407 e o contêiner da localidade japonesa é chamado de 411. Para obter mais informações e uma lista de possíveis identificadores de idioma, consulte [constantes e cadeias de caracteres de identificador de linguagem](/windows/desktop/Intl/language-identifier-constants-and-strings).

Cada contêiner de localidade armazena objetos da classe [**displaySpecifier**](/windows/desktop/ADSchema/c-displayspecifier) .

Para listar todos os especificadores de exibição para uma localidade, enumere todos os objetos [**displaySpecifier**](/windows/desktop/ADSchema/c-displayspecifier) no contêiner de localidade especificado dentro do contêiner DisplaySpecifiers.

O exemplo de código a seguir contém uma função que é associada ao contêiner de especificador de exibição para a localidade especificada:


```C++
/**********
This function returns a pointer to the display specifier container 
for the specified locale.

If locale is NULL, use default system locale and then return the 
locale in the locale parameter.
***********/
HRESULT BindToDisplaySpecifiersContainerByLocale(
    LCID *locale,
    IADs **ppDispSpecCont)
{
HRESULT hr = E_FAIL;
 
if ((!ppDispSpecCont)||(!locale))
    return E_POINTER;
 
// If no locale is specified, use the default system locale.
if (!(*locale))
{
    *locale = GetSystemDefaultLCID();
    if (!(*locale))
        return E_FAIL;
}
 
// Be sure that the locale is valid.
if (!IsValidLocale(*locale, LCID_SUPPORTED))
    return E_INVALIDARG;
 
LPOLESTR szPath = new OLECHAR[MAX_PATH*2];
IADs *pObj = NULL;
VARIANT var;
 
hr = ADsOpenObject(L"LDAP://rootDSE",
                     NULL,
                     NULL,
                     ADS_SECURE_AUTHENTICATION,
                     IID_IADs,
                     (void**)&pObj);
 
if (SUCCEEDED(hr))
{
    // Get the DN to the configuration container.
    hr = pObj->Get(CComBSTR("configurationNamingContext"), &var);
    if (SUCCEEDED(hr))
    {
        // Build the string to bind to the container for the
        // specified locale in the DisplaySpecifiers container.
        swprintf_s(
            szPath, 
            L"LDAP://cn=%x,cn=DisplaySpecifiers,%s", 
            *locale, 
            var.bstrVal);

        // Bind to the container.
        *ppDispSpecCont = NULL;
        hr = ADsOpenObject(szPath,
                     NULL,
                     NULL,
                     ADS_SECURE_AUTHENTICATION,
                     IID_IADs,
                     (void**)ppDispSpecCont);
 
        if(FAILED(hr))
        {
            if ((*ppDispSpecCont))
            {
                (*ppDispSpecCont)->Release();
                (*ppDispSpecCont) = NULL;
            }
        }
    }
}
 
// Cleanup.
VariantClear(&var);
if (pObj)
    pObj->Release();
 
return hr;
}
```



 

 