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
# <a name="how-to-enumerate-fonts"></a><span data-ttu-id="42726-103">Como enumerar fontes</span><span class="sxs-lookup"><span data-stu-id="42726-103">How to Enumerate Fonts</span></span>

<span data-ttu-id="42726-104">Esta visão geral mostrará como enumerar as fontes na coleção de fontes do sistema, por nome da família.</span><span class="sxs-lookup"><span data-stu-id="42726-104">This overview will show how to enumerate the fonts in the system font collection, by family name.</span></span>

<span data-ttu-id="42726-105">Esta visão geral consiste nas seguintes partes:</span><span class="sxs-lookup"><span data-stu-id="42726-105">This overview consists of the following parts:</span></span>

-   [<span data-ttu-id="42726-106">Etapa 1: obter a coleção de fontes do sistema.</span><span class="sxs-lookup"><span data-stu-id="42726-106">Step 1: Get the System Font Collection.</span></span>](#step-1-get-the-system-font-collection)
-   [<span data-ttu-id="42726-107">Etapa 2: obter a contagem da família de fontes.</span><span class="sxs-lookup"><span data-stu-id="42726-107">Step 2: Get the Font Family Count.</span></span>](#step-2-get-the-font-family-count)
-   [<span data-ttu-id="42726-108">Faça um loop for.</span><span class="sxs-lookup"><span data-stu-id="42726-108">Make a For Loop.</span></span>](#make-a-for-loop)
    -   [<span data-ttu-id="42726-109">Etapa 3: obter a família de fontes.</span><span class="sxs-lookup"><span data-stu-id="42726-109">Step 3: Get the Font Family.</span></span>](#step-3-get-the-font-family)
    -   [<span data-ttu-id="42726-110">Etapa 4: obter os nomes de família.</span><span class="sxs-lookup"><span data-stu-id="42726-110">Step 4: Get the Family Names.</span></span>](#step-4-get-the-family-names)
    -   [<span data-ttu-id="42726-111">Etapa 5: localizar o nome da localidade.</span><span class="sxs-lookup"><span data-stu-id="42726-111">Step 5: Find the Locale Name.</span></span>](#step-5-find-the-locale-name)
    -   [<span data-ttu-id="42726-112">Etapa 6: obter o comprimento do comprimento da cadeia de caracteres do nome da família e a cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="42726-112">Step 6: Get the Length of the Family Name String Length and the String.</span></span>](#step-6-get-the-length-of-the-family-name-string-length-and-the-string)
-   [<span data-ttu-id="42726-113">Conclusão</span><span class="sxs-lookup"><span data-stu-id="42726-113">Conclusion</span></span>](#conclusion)
-   [<span data-ttu-id="42726-114">Código de exemplo</span><span class="sxs-lookup"><span data-stu-id="42726-114">Example Code</span></span>](#example-code)

## <a name="step-1-get-the-system-font-collection"></a><span data-ttu-id="42726-115">Etapa 1: obter a coleção de fontes do sistema.</span><span class="sxs-lookup"><span data-stu-id="42726-115">Step 1: Get the System Font Collection.</span></span>

<span data-ttu-id="42726-116">Use o método [**GetSystemFontCollection**](/windows/win32/api/dwrite/nf-dwrite-idwritefactory-getsystemfontcollection) fornecido pela fábrica do DirectWrite para retornar um [**IDWriteFontCollection**](/windows/win32/api/dwrite/nn-dwrite-idwritefontcollection) com todas as fontes do sistema nele.</span><span class="sxs-lookup"><span data-stu-id="42726-116">Use the [**GetSystemFontCollection**](/windows/win32/api/dwrite/nf-dwrite-idwritefactory-getsystemfontcollection) method provided by the DirectWrite Factory to return an [**IDWriteFontCollection**](/windows/win32/api/dwrite/nn-dwrite-idwritefontcollection) with all of the system fonts in it.</span></span>


```C++
IDWriteFontCollection* pFontCollection = NULL;

// Get the system font collection.
if (SUCCEEDED(hr))
{
    hr = pDWriteFactory->GetSystemFontCollection(&pFontCollection);
}
```



## <a name="step-2-get-the-font-family-count"></a><span data-ttu-id="42726-117">Etapa 2: obter a contagem da família de fontes.</span><span class="sxs-lookup"><span data-stu-id="42726-117">Step 2: Get the Font Family Count.</span></span>

<span data-ttu-id="42726-118">Em seguida, obtenha a contagem de famílias de fontes da coleção de fontes usando [**IDWriteFontCollection:: GetFontFamilyCount**](/windows/win32/api/dwrite/nf-dwrite-idwritefontcollection-getfontfamilycount).</span><span class="sxs-lookup"><span data-stu-id="42726-118">Next, get the font family count from the font collection by using [**IDWriteFontCollection::GetFontFamilyCount**](/windows/win32/api/dwrite/nf-dwrite-idwritefontcollection-getfontfamilycount).</span></span> <span data-ttu-id="42726-119">Usaremos isso para executar um loop sobre cada família de fontes na coleção.</span><span class="sxs-lookup"><span data-stu-id="42726-119">We'll use this to loop over each font family in the collection.</span></span>


```C++
UINT32 familyCount = 0;

// Get the number of font families in the collection.
if (SUCCEEDED(hr))
{
    familyCount = pFontCollection->GetFontFamilyCount();
}
```



## <a name="make-a-for-loop"></a><span data-ttu-id="42726-120">Faça um loop for.</span><span class="sxs-lookup"><span data-stu-id="42726-120">Make a For Loop.</span></span>


```C++
for (UINT32 i = 0; i < familyCount; ++i)
```



<span data-ttu-id="42726-121">Agora que você tem a coleção de fontes e a contagem de fontes, as etapas restantes executam um loop sobre cada família de fontes, recuperando o objeto [**IDWriteFontFamily**](/windows/win32/api/dwrite/nn-dwrite-idwritefontfamily) e consultando-o.</span><span class="sxs-lookup"><span data-stu-id="42726-121">Now that you have the font collection and the font count, the remaining steps loop over each font family, retrieving the [**IDWriteFontFamily**](/windows/win32/api/dwrite/nn-dwrite-idwritefontfamily) object and querying it.</span></span>

### <a name="step-3-get-the-font-family"></a><span data-ttu-id="42726-122">Etapa 3: obter a família de fontes.</span><span class="sxs-lookup"><span data-stu-id="42726-122">Step 3: Get the Font Family.</span></span>

<span data-ttu-id="42726-123">Obtenha um objeto [**IDWriteFontFamily**](/windows/win32/api/dwrite/nn-dwrite-idwritefontfamily) usando [**IDWriteFontCollection:: GetFontFamily**](/windows/win32/api/dwrite/nf-dwrite-idwritefontcollection-getfontfamily) e passando-o índice atual, *i*.</span><span class="sxs-lookup"><span data-stu-id="42726-123">Get a [**IDWriteFontFamily**](/windows/win32/api/dwrite/nn-dwrite-idwritefontfamily) object by using [**IDWriteFontCollection::GetFontFamily**](/windows/win32/api/dwrite/nf-dwrite-idwritefontcollection-getfontfamily) and passing it the current index, *i*.</span></span>


```C++
IDWriteFontFamily* pFontFamily = NULL;

// Get the font family.
if (SUCCEEDED(hr))
{
    hr = pFontCollection->GetFontFamily(i, &pFontFamily);
}
```



### <a name="step-4-get-the-family-names"></a><span data-ttu-id="42726-124">Etapa 4: obter os nomes de família.</span><span class="sxs-lookup"><span data-stu-id="42726-124">Step 4: Get the Family Names.</span></span>

<span data-ttu-id="42726-125">Obtenha os nomes da família de fontes usando [**IDWriteFontFamily:: Getfamilynames**](/windows/win32/api/dwrite/nf-dwrite-idwritefontfamily-getfamilynames).</span><span class="sxs-lookup"><span data-stu-id="42726-125">Get the font family names by using the [**IDWriteFontFamily::GetFamilyNames**](/windows/win32/api/dwrite/nf-dwrite-idwritefontfamily-getfamilynames).</span></span> <span data-ttu-id="42726-126">Este é um objeto [**IDWriteLocalizedStrings**](/windows/win32/api/dwrite/nn-dwrite-idwritelocalizedstrings) .</span><span class="sxs-lookup"><span data-stu-id="42726-126">This is an [**IDWriteLocalizedStrings**](/windows/win32/api/dwrite/nn-dwrite-idwritelocalizedstrings) object.</span></span> <span data-ttu-id="42726-127">Ele pode ter várias versões localizadas do nome da família para a família de fontes.</span><span class="sxs-lookup"><span data-stu-id="42726-127">It can have multiple localized versions of the family name for the font family.</span></span>


```C++
IDWriteLocalizedStrings* pFamilyNames = NULL;

// Get a list of localized strings for the family name.
if (SUCCEEDED(hr))
{
    hr = pFontFamily->GetFamilyNames(&pFamilyNames);
}
```



### <a name="step-5-find-the-locale-name"></a><span data-ttu-id="42726-128">Etapa 5: localizar o nome da localidade.</span><span class="sxs-lookup"><span data-stu-id="42726-128">Step 5: Find the Locale Name.</span></span>

<span data-ttu-id="42726-129">Obtenha o nome da fonte famliy na localidade que você deseja usando o método [**IDWriteLocalizedStrings:: FindLocaleName**](/windows/win32/api/dwrite/nf-dwrite-idwritelocalizedstrings-findlocalename) .</span><span class="sxs-lookup"><span data-stu-id="42726-129">Get the font famliy name in the locale you want by using the [**IDWriteLocalizedStrings::FindLocaleName**](/windows/win32/api/dwrite/nf-dwrite-idwritelocalizedstrings-findlocalename) method.</span></span> <span data-ttu-id="42726-130">Nesse caso, primeiro a localidade padrão é recuperada e solicitada.</span><span class="sxs-lookup"><span data-stu-id="42726-130">In this case, first the default locale is retrieved and requested.</span></span> <span data-ttu-id="42726-131">Se isso não funcionar, a localidade "en-US" será solicitada.</span><span class="sxs-lookup"><span data-stu-id="42726-131">If that does not work, the "en-us" locale is requested.</span></span> <span data-ttu-id="42726-132">Se nenhuma das localidades especificadas não for encontrada, este exemplo simplesmente retornará ao índice 0, a primeira localidade disponível.</span><span class="sxs-lookup"><span data-stu-id="42726-132">If either of the specified locales are not found, this example simply falls back to index 0, the first available locale.</span></span>


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



### <a name="step-6-get-the-length-of-the-family-name-string-length-and-the-string"></a><span data-ttu-id="42726-133">Etapa 6: obter o comprimento do comprimento da cadeia de caracteres do nome da família e a cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="42726-133">Step 6: Get the Length of the Family Name String Length and the String.</span></span>

<span data-ttu-id="42726-134">Por fim, obtenha o tamanho da cadeia de caracteres do nome da família usando [**IDWriteLocalizedStrings:: GetStringLength**](/windows/win32/api/dwrite/nf-dwrite-idwritelocalizedstrings-getstringlength).</span><span class="sxs-lookup"><span data-stu-id="42726-134">Finally, get the length of the family name string by using [**IDWriteLocalizedStrings::GetStringLength**](/windows/win32/api/dwrite/nf-dwrite-idwritelocalizedstrings-getstringlength).</span></span> <span data-ttu-id="42726-135">Use esse comprimento para alocar uma cadeia de caracteres grande o suficiente para manter o nome e obter o nome da família de fontes usando [**IDWriteLocalizedStrings:: GetString**](/windows/win32/api/dwrite/nf-dwrite-idwritelocalizedstrings-getstring).</span><span class="sxs-lookup"><span data-stu-id="42726-135">Use this length to allocate a string large enough to hold the name and then get the font family name by using [**IDWriteLocalizedStrings::GetString**](/windows/win32/api/dwrite/nf-dwrite-idwritelocalizedstrings-getstring).</span></span>


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



## <a name="conclusion"></a><span data-ttu-id="42726-136">Conclusão</span><span class="sxs-lookup"><span data-stu-id="42726-136">Conclusion</span></span>

<span data-ttu-id="42726-137">Depois de ter o nome da família ou os nomes na localidade, você pode listá-los para que o usuário escolha ou passá-lo para CreateTextFormat para começar a formatar o texto com a família de fontes especificada e assim por diante.</span><span class="sxs-lookup"><span data-stu-id="42726-137">Once you have the family name or names in the locale, you can list them for the user to choose from, or pass it to CreateTextFormat to begin formatting text with the specified font family, and so on.</span></span>

## <a name="example-code"></a><span data-ttu-id="42726-138">Código de exemplo</span><span class="sxs-lookup"><span data-stu-id="42726-138">Example Code</span></span>

<span data-ttu-id="42726-139">Para ver o código-fonte completo deste exemplo, consulte o [exemplo de enumeração de fontes](/samples/browse/?redirectedfrom=MSDN-samples).</span><span class="sxs-lookup"><span data-stu-id="42726-139">To see the full source code for this example see the [Font Enumeration Sample](/samples/browse/?redirectedfrom=MSDN-samples).</span></span>

 

 