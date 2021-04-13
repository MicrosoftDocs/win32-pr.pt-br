---
title: Como enumerar fontes
description: Esta visão geral mostrará como enumerar as fontes na coleção de fontes do sistema, por nome da família.
ms.assetid: c1ec7721-2a30-4de3-b986-932f098228a6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a9db05deb6b367f1392151ac8c12f2792d6e34f0
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104366301"
---
# <a name="how-to-enumerate-fonts"></a>Como enumerar fontes

Esta visão geral mostrará como enumerar as fontes na coleção de fontes do sistema, por nome da família.

Esta visão geral consiste nas seguintes partes:

-   [Etapa 1: obter a coleção de fontes do sistema.](#step-1-get-the-system-font-collection)
-   [Etapa 2: obter a contagem da família de fontes.](#step-2-get-the-font-family-count)
-   [Faça um loop for.](#make-a-for-loop)
    -   [Etapa 3: obter a família de fontes.](#step-3-get-the-font-family)
    -   [Etapa 4: obter os nomes de família.](#step-4-get-the-family-names)
    -   [Etapa 5: localizar o nome da localidade.](#step-5-find-the-locale-name)
    -   [Etapa 6: obter o comprimento do comprimento da cadeia de caracteres do nome da família e a cadeia de caracteres.](#step-6-get-the-length-of-the-family-name-string-length-and-the-string)
-   [Conclusão](#conclusion)
-   [Código de exemplo](#example-code)

## <a name="step-1-get-the-system-font-collection"></a>Etapa 1: obter a coleção de fontes do sistema.

Use o método [**GetSystemFontCollection**](/windows/win32/api/dwrite/nf-dwrite-idwritefactory-getsystemfontcollection) fornecido pela fábrica do DirectWrite para retornar um [**IDWriteFontCollection**](/windows/win32/api/dwrite/nn-dwrite-idwritefontcollection) com todas as fontes do sistema nele.


```C++
IDWriteFontCollection* pFontCollection = NULL;

// Get the system font collection.
if (SUCCEEDED(hr))
{
    hr = pDWriteFactory->GetSystemFontCollection(&pFontCollection);
}
```



## <a name="step-2-get-the-font-family-count"></a>Etapa 2: obter a contagem da família de fontes.

Em seguida, obtenha a contagem de famílias de fontes da coleção de fontes usando [**IDWriteFontCollection:: GetFontFamilyCount**](/windows/win32/api/dwrite/nf-dwrite-idwritefontcollection-getfontfamilycount). Usaremos isso para executar um loop sobre cada família de fontes na coleção.


```C++
UINT32 familyCount = 0;

// Get the number of font families in the collection.
if (SUCCEEDED(hr))
{
    familyCount = pFontCollection->GetFontFamilyCount();
}
```



## <a name="make-a-for-loop"></a>Faça um loop for.


```C++
for (UINT32 i = 0; i < familyCount; ++i)
```



Agora que você tem a coleção de fontes e a contagem de fontes, as etapas restantes executam um loop sobre cada família de fontes, recuperando o objeto [**IDWriteFontFamily**](/windows/win32/api/dwrite/nn-dwrite-idwritefontfamily) e consultando-o.

### <a name="step-3-get-the-font-family"></a>Etapa 3: obter a família de fontes.

Obtenha um objeto [**IDWriteFontFamily**](/windows/win32/api/dwrite/nn-dwrite-idwritefontfamily) usando [**IDWriteFontCollection:: GetFontFamily**](/windows/win32/api/dwrite/nf-dwrite-idwritefontcollection-getfontfamily) e passando-o índice atual, *i*.


```C++
IDWriteFontFamily* pFontFamily = NULL;

// Get the font family.
if (SUCCEEDED(hr))
{
    hr = pFontCollection->GetFontFamily(i, &pFontFamily);
}
```



### <a name="step-4-get-the-family-names"></a>Etapa 4: obter os nomes de família.

Obtenha os nomes da família de fontes usando [**IDWriteFontFamily:: Getfamilynames**](/windows/win32/api/dwrite/nf-dwrite-idwritefontfamily-getfamilynames). Este é um objeto [**IDWriteLocalizedStrings**](/windows/win32/api/dwrite/nn-dwrite-idwritelocalizedstrings) . Ele pode ter várias versões localizadas do nome da família para a família de fontes.


```C++
IDWriteLocalizedStrings* pFamilyNames = NULL;

// Get a list of localized strings for the family name.
if (SUCCEEDED(hr))
{
    hr = pFontFamily->GetFamilyNames(&pFamilyNames);
}
```



### <a name="step-5-find-the-locale-name"></a>Etapa 5: localizar o nome da localidade.

Obtenha o nome da fonte famliy na localidade que você deseja usando o método [**IDWriteLocalizedStrings:: FindLocaleName**](/windows/win32/api/dwrite/nf-dwrite-idwritelocalizedstrings-findlocalename) . Nesse caso, primeiro a localidade padrão é recuperada e solicitada. Se isso não funcionar, a localidade "en-US" será solicitada. Se nenhuma das localidades especificadas não for encontrada, este exemplo simplesmente retornará ao índice 0, a primeira localidade disponível.


```C++
UINT32 index = 0;
BOOL exists = false;

wchar_t localeName[LOCALE_NAME_MAX_LENGTH];

if (SUCCEEDED(hr))
{
    // Get the default locale for this user.
    int defaultLocaleSuccess = GetUserDefaultLocaleName(localeName, LOCALE_NAME_MAX_LENGTH);

    // If the default locale is returned, find that locale name, otherwise use "en-us".
    if (defaultLocaleSuccess)
    {
        hr = pFamilyNames->FindLocaleName(localeName, &index, &exists);
    }
    if (SUCCEEDED(hr) && !exists) // if the above find did not find a match, retry with US English
    {
        hr = pFamilyNames->FindLocaleName(L"en-us", &index, &exists);
    }
}

// If the specified locale doesn't exist, select the first on the list.
if (!exists)
    index = 0;
```



### <a name="step-6-get-the-length-of-the-family-name-string-length-and-the-string"></a>Etapa 6: obter o comprimento do comprimento da cadeia de caracteres do nome da família e a cadeia de caracteres.

Por fim, obtenha o tamanho da cadeia de caracteres do nome da família usando [**IDWriteLocalizedStrings:: GetStringLength**](/windows/win32/api/dwrite/nf-dwrite-idwritelocalizedstrings-getstringlength). Use esse comprimento para alocar uma cadeia de caracteres grande o suficiente para manter o nome e obter o nome da família de fontes usando [**IDWriteLocalizedStrings:: GetString**](/windows/win32/api/dwrite/nf-dwrite-idwritelocalizedstrings-getstring).


```C++
UINT32 length = 0;

// Get the string length.
if (SUCCEEDED(hr))
{
    hr = pFamilyNames->GetStringLength(index, &length);
}

// Allocate a string big enough to hold the name.
wchar_t* name = new (std::nothrow) wchar_t[length+1];
if (name == NULL)
{
    hr = E_OUTOFMEMORY;
}

// Get the family name.
if (SUCCEEDED(hr))
{
    hr = pFamilyNames->GetString(index, name, length+1);
}
```



## <a name="conclusion"></a>Conclusão

Depois de ter o nome da família ou os nomes na localidade, você pode listá-los para que o usuário escolha ou passá-lo para CreateTextFormat para começar a formatar o texto com a família de fontes especificada e assim por diante.

## <a name="example-code"></a>Código de exemplo

Para ver o código-fonte completo deste exemplo, consulte o [exemplo de enumeração de fontes](/samples/browse/?redirectedfrom=MSDN-samples).

 

 