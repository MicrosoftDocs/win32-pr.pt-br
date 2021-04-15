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
# <a name="displayspecifiers-container"></a><span data-ttu-id="c7203-106">Contêiner DisplaySpecifiers</span><span class="sxs-lookup"><span data-stu-id="c7203-106">DisplaySpecifiers Container</span></span>

<span data-ttu-id="c7203-107">Os especificadores de exibição são armazenados, por localidade, no contêiner DisplaySpecifiers do contêiner de configuração.</span><span class="sxs-lookup"><span data-stu-id="c7203-107">Display specifiers are stored, by locale, in the DisplaySpecifiers container of the Configuration container.</span></span> <span data-ttu-id="c7203-108">Como o contêiner de configuração é replicado em toda a floresta, os especificadores de exibição são propagados em todos os domínios em uma floresta.</span><span class="sxs-lookup"><span data-stu-id="c7203-108">Because the Configuration container is replicated across the entire forest, display specifiers are propagated across all domains in a forest.</span></span>

<span data-ttu-id="c7203-109">O contêiner de configuração armazena o contêiner DisplaySpecifiers, que armazena contêineres que correspondem a cada localidade.</span><span class="sxs-lookup"><span data-stu-id="c7203-109">The Configuration container stores the DisplaySpecifiers container, which then stores containers that correspond to each locale.</span></span> <span data-ttu-id="c7203-110">Esses contêineres de localidade são nomeados usando a representação hexadecimal do identificador de localidade.</span><span class="sxs-lookup"><span data-stu-id="c7203-110">These locale containers are named using the hexadecimal representation of the locale identifier.</span></span> <span data-ttu-id="c7203-111">Por exemplo, o contêiner de localidade dos EUA/inglês é denominado 409, o contêiner da localidade alemão é denominado 407 e o contêiner da localidade japonesa é chamado de 411.</span><span class="sxs-lookup"><span data-stu-id="c7203-111">For example, the US/English locale container is named 409, the German locale's container is named 407, and the Japanese locale's container is named 411.</span></span> <span data-ttu-id="c7203-112">Para obter mais informações e uma lista de possíveis identificadores de idioma, consulte [constantes e cadeias de caracteres de identificador de linguagem](/windows/desktop/Intl/language-identifier-constants-and-strings).</span><span class="sxs-lookup"><span data-stu-id="c7203-112">For more information, and a list of possible language identifiers, see [Language Identifier Constants and Strings](/windows/desktop/Intl/language-identifier-constants-and-strings).</span></span>

<span data-ttu-id="c7203-113">Cada contêiner de localidade armazena objetos da classe [**displaySpecifier**](/windows/desktop/ADSchema/c-displayspecifier) .</span><span class="sxs-lookup"><span data-stu-id="c7203-113">Each locale container stores objects of the [**displaySpecifier**](/windows/desktop/ADSchema/c-displayspecifier) class.</span></span>

<span data-ttu-id="c7203-114">Para listar todos os especificadores de exibição para uma localidade, enumere todos os objetos [**displaySpecifier**](/windows/desktop/ADSchema/c-displayspecifier) no contêiner de localidade especificado dentro do contêiner DisplaySpecifiers.</span><span class="sxs-lookup"><span data-stu-id="c7203-114">To list all display specifiers for a locale, enumerate all the [**displaySpecifier**](/windows/desktop/ADSchema/c-displayspecifier) objects in the specified locale container within the DisplaySpecifiers container.</span></span>

<span data-ttu-id="c7203-115">O exemplo de código a seguir contém uma função que é associada ao contêiner de especificador de exibição para a localidade especificada:</span><span class="sxs-lookup"><span data-stu-id="c7203-115">The following code example contains a function that binds to the display specifier container for the specified locale:</span></span>


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



 

 