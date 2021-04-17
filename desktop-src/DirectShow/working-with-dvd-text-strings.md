---
description: Trabalhando com cadeias de caracteres de texto em DVD
ms.assetid: 6d415ebb-5cd0-4631-9404-f2ebabef2476
title: Trabalhando com cadeias de caracteres de texto em DVD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 31d04a786e46c795f028edbe2b955e71715aaefb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105754687"
---
# <a name="working-with-dvd-text-strings"></a><span data-ttu-id="5e451-103">Trabalhando com cadeias de caracteres de texto em DVD</span><span class="sxs-lookup"><span data-stu-id="5e451-103">Working with DVD Text Strings</span></span>

<span data-ttu-id="5e451-104">Alguns discos de DVD, especialmente discos do karaokê, podem conter uma lista de cadeias de caracteres de texto para complementar o conteúdo de vídeo ou áudio.</span><span class="sxs-lookup"><span data-stu-id="5e451-104">Some DVD discs, especially karaoke discs, might contain a list of text strings to supplement the video or audio content.</span></span> <span data-ttu-id="5e451-105">Essas cadeias de caracteres de texto contêm metadados sobre o conteúdo, como títulos de música, nomes de artistas, informações de gênero e assim por diante.</span><span class="sxs-lookup"><span data-stu-id="5e451-105">These text strings contain metadata about the content, such as song titles, artist names, genre information, and so on.</span></span> <span data-ttu-id="5e451-106">As cadeias de caracteres de texto podem estar presentes em mais de um idioma.</span><span class="sxs-lookup"><span data-stu-id="5e451-106">Text strings can be present in more than one language.</span></span> <span data-ttu-id="5e451-107">Essas cadeias de caracteres são opcionais e muitos discos não as têm.</span><span class="sxs-lookup"><span data-stu-id="5e451-107">These strings are optional, and many discs do not have them.</span></span>

<span data-ttu-id="5e451-108">Para recuperar cadeias de caracteres de texto de um DVD, use a interface [**IDvdInfo2**](/windows/desktop/api/Strmif/nn-strmif-idvdinfo2) , que é exposta pelo [navegador de DVD](dvd-navigator-filter.md).</span><span class="sxs-lookup"><span data-stu-id="5e451-108">To retrieve text strings from a DVD, use the [**IDvdInfo2**](/windows/desktop/api/Strmif/nn-strmif-idvdinfo2) interface, which is exposed by the [DVD Navigator](dvd-navigator-filter.md).</span></span> <span data-ttu-id="5e451-109">Na verdade, você não precisa criar um grafo de reprodução de DVD para recuperar as cadeias de caracteres de texto.</span><span class="sxs-lookup"><span data-stu-id="5e451-109">You do not actually need to build a DVD playback graph to retrieve the text strings.</span></span> <span data-ttu-id="5e451-110">Você pode simplesmente criar o navegador de DVD, definir o volume de DVD e, em seguida, chamar os métodos de cadeia de caracteres de texto relevantes:</span><span class="sxs-lookup"><span data-stu-id="5e451-110">You can simply create the DVD Navigator, set the DVD volume, and then call the relevant text-string methods:</span></span>



| <span data-ttu-id="5e451-111">Método</span><span class="sxs-lookup"><span data-stu-id="5e451-111">Method</span></span>                                                                                  | <span data-ttu-id="5e451-112">Descrição</span><span class="sxs-lookup"><span data-stu-id="5e451-112">Description</span></span>                                                                                                                                                                                     |
|-----------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="5e451-113">**IDvdInfo2::GetDVDTextNumberOfLanguages**</span><span class="sxs-lookup"><span data-stu-id="5e451-113">**IDvdInfo2::GetDVDTextNumberOfLanguages**</span></span>](/windows/desktop/api/Strmif/nf-strmif-idvdinfo2-getdvdtextnumberoflanguages) | <span data-ttu-id="5e451-114">Obtém o número de idiomas para os quais há cadeias de caracteres de texto.</span><span class="sxs-lookup"><span data-stu-id="5e451-114">Gets the number of languages for which there are text strings.</span></span>                                                                                                                                  |
| [<span data-ttu-id="5e451-115">**IDvdInfo2::GetDVDTextLanguageInfo**</span><span class="sxs-lookup"><span data-stu-id="5e451-115">**IDvdInfo2::GetDVDTextLanguageInfo**</span></span>](/windows/desktop/api/Strmif/nf-strmif-idvdinfo2-getdvdtextlanguageinfo)           | <span data-ttu-id="5e451-116">Obtém informações sobre as cadeias de caracteres de texto para um idioma.</span><span class="sxs-lookup"><span data-stu-id="5e451-116">Gets information about the text strings for one language.</span></span>                                                                                                                                       |
| [<span data-ttu-id="5e451-117">**IDvdInfo2::GetDVDTextStringAsUnicode**</span><span class="sxs-lookup"><span data-stu-id="5e451-117">**IDvdInfo2::GetDVDTextStringAsUnicode**</span></span>](/windows/desktop/api/Strmif/nf-strmif-idvdinfo2-getdvdtextstringasunicode)     | <span data-ttu-id="5e451-118">Obtém uma cadeia de texto para um idioma especificado, por índice.</span><span class="sxs-lookup"><span data-stu-id="5e451-118">Gets a text string for a specified language, by index.</span></span>                                                                                                                                          |
| [<span data-ttu-id="5e451-119">**IDvdInfo2::GetDVDTextStringAsNative**</span><span class="sxs-lookup"><span data-stu-id="5e451-119">**IDvdInfo2::GetDVDTextStringAsNative**</span></span>](/windows/desktop/api/Strmif/nf-strmif-idvdinfo2-getdvdtextstringasnative)       | <span data-ttu-id="5e451-120">Obtém uma cadeia de caracteres de texto como uma matriz de bytes brutos.</span><span class="sxs-lookup"><span data-stu-id="5e451-120">Gets a text string as a raw byte array.</span></span> <span data-ttu-id="5e451-121">Use esse método se a cadeia de caracteres de texto usar uma codificação de caracteres sem suporte do [**GetDVDTextStringAsUnicode**](/windows/desktop/api/Strmif/nf-strmif-idvdinfo2-getdvdtextstringasunicode).</span><span class="sxs-lookup"><span data-stu-id="5e451-121">Use this method if the text string uses a character encoding not supported by [**GetDVDTextStringAsUnicode**](/windows/desktop/api/Strmif/nf-strmif-idvdinfo2-getdvdtextstringasunicode).</span></span> |



 

<span data-ttu-id="5e451-122">Este é o procedimento básico para obter cadeias de texto:</span><span class="sxs-lookup"><span data-stu-id="5e451-122">Here is the basic procedure for getting text strings:</span></span>

1.  <span data-ttu-id="5e451-123">Chame [**IDvdInfo2:: GetDVDTextNumberOfLanguages**](/windows/desktop/api/Strmif/nf-strmif-idvdinfo2-getdvdtextnumberoflanguages) para localizar o número total de idiomas nos quais as cadeias de caracteres de texto aparecem.</span><span class="sxs-lookup"><span data-stu-id="5e451-123">Call [**IDvdInfo2::GetDVDTextNumberOfLanguages**](/windows/desktop/api/Strmif/nf-strmif-idvdinfo2-getdvdtextnumberoflanguages) to find the total number of languages in which the text strings appear.</span></span> <span data-ttu-id="5e451-124">Se o número for zero, significa que o DVD não tem nenhuma cadeia de caracteres de texto.</span><span class="sxs-lookup"><span data-stu-id="5e451-124">If the number is zero, it means the DVD does not have any text strings.</span></span> <span data-ttu-id="5e451-125">(Talvez esse seja o caso mais comum, na verdade).</span><span class="sxs-lookup"><span data-stu-id="5e451-125">(This is perhaps the most common case, in fact.)</span></span>
2.  <span data-ttu-id="5e451-126">Se o número de idiomas for pelo menos um, chame [**IDvdInfo2:: GetDVDTextLanguageInfo**](/windows/desktop/api/Strmif/nf-strmif-idvdinfo2-getdvdtextlanguageinfo) para obter informações sobre cada idioma.</span><span class="sxs-lookup"><span data-stu-id="5e451-126">If the number of languages is at least one, call [**IDvdInfo2::GetDVDTextLanguageInfo**](/windows/desktop/api/Strmif/nf-strmif-idvdinfo2-getdvdtextlanguageinfo) to get information about each language.</span></span> <span data-ttu-id="5e451-127">O idioma é especificado pelo índice.</span><span class="sxs-lookup"><span data-stu-id="5e451-127">The language is specified by index.</span></span> <span data-ttu-id="5e451-128">O método retorna o número total de cadeias de caracteres de texto nesse idioma, o **LCID**(identificador de localidade) para o idioma e a codificação de caracteres (Unicode ou outro).</span><span class="sxs-lookup"><span data-stu-id="5e451-128">The method returns the total number of text strings in that language, the locale identifier (**LCID**) for the language, and the character encoding (Unicode or other).</span></span> <span data-ttu-id="5e451-129">Cadeias de texto em DVD podem usar vários conjuntos de caracteres diferentes; Eles são listados na [**\_ Enumeração textcharset de DVD**](/windows/desktop/api/strmif/ne-strmif-dvd_textcharset).</span><span class="sxs-lookup"><span data-stu-id="5e451-129">DVD text strings can use several different character sets; these are listed in [**DVD\_TextCharSet Enumeration**](/windows/desktop/api/strmif/ne-strmif-dvd_textcharset).</span></span>
3.  <span data-ttu-id="5e451-130">Para obter uma cadeia de texto, chame [**IDvdInfo2:: GetDVDTextStringAsUnicode**](/windows/desktop/api/Strmif/nf-strmif-idvdinfo2-getdvdtextstringasunicode) ou [**IDvdInfo2:: GetDVDTextStringAsNative**](/windows/desktop/api/Strmif/nf-strmif-idvdinfo2-getdvdtextstringasnative).</span><span class="sxs-lookup"><span data-stu-id="5e451-130">To get a text string, call [**IDvdInfo2::GetDVDTextStringAsUnicode**](/windows/desktop/api/Strmif/nf-strmif-idvdinfo2-getdvdtextstringasunicode) or [**IDvdInfo2::GetDVDTextStringAsNative**](/windows/desktop/api/Strmif/nf-strmif-idvdinfo2-getdvdtextstringasnative).</span></span> <span data-ttu-id="5e451-131">O primeiro método retorna uma cadeia de caracteres largos, mas não dá suporte a todos os conjuntos de caracteres.</span><span class="sxs-lookup"><span data-stu-id="5e451-131">The first method returns a wide-character string, but does not support every character set.</span></span> <span data-ttu-id="5e451-132">O segundo método retorna uma matriz de bytes que contém os dados de texto brutos.</span><span class="sxs-lookup"><span data-stu-id="5e451-132">The second method returns a byte array containing the raw text data.</span></span> <span data-ttu-id="5e451-133">Para ambos os métodos, você pode chamar o método com um ponteiro de buffer **nulo** para localizar o tamanho da cadeia de caracteres e o tipo de texto.</span><span class="sxs-lookup"><span data-stu-id="5e451-133">For both methods, you can call the method with a **NULL** buffer pointer to find the size of the string and the text type.</span></span> <span data-ttu-id="5e451-134">Em seguida, aloque um buffer e chame o método novamente para obter a cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="5e451-134">Then allocate a buffer and call the method again to get the string.</span></span>

<span data-ttu-id="5e451-135">Cada cadeia de texto tem um código de identificador associado, que indica o significado da cadeia de texto.</span><span class="sxs-lookup"><span data-stu-id="5e451-135">Each text string has an associated identifier code, which indicates the meaning of the text string.</span></span> <span data-ttu-id="5e451-136">O identificador é retornado como um valor de [**DVD \_ textstringtype**](/windows/desktop/api/strmif/ne-strmif-dvd_textstringtype) .</span><span class="sxs-lookup"><span data-stu-id="5e451-136">The identifier is returned as a [**DVD\_TextStringType**](/windows/desktop/api/strmif/ne-strmif-dvd_textstringtype) value.</span></span> <span data-ttu-id="5e451-137">Há duas categorias de identificador: *identificadores de estrutura* e *identificadores de conteúdo*.</span><span class="sxs-lookup"><span data-stu-id="5e451-137">There are two categories of identifier: *structure identifiers* and *content identifiers*.</span></span> <span data-ttu-id="5e451-138">Os identificadores de estrutura têm códigos numéricos no intervalo 0x00 – 0x02F.</span><span class="sxs-lookup"><span data-stu-id="5e451-138">Structure identifiers have numeric codes in the range 0x00–0x02F.</span></span> <span data-ttu-id="5e451-139">Os identificadores de conteúdo têm um intervalo de 0x30 e superior.</span><span class="sxs-lookup"><span data-stu-id="5e451-139">Content identifiers have a range of 0x30 and higher.</span></span> <span data-ttu-id="5e451-140">(A **enumeração \_ textstringtype de DVD** define um subconjunto dos identificadores mais comuns, mas os métodos [**IDvdInfo2**](/windows/desktop/api/Strmif/nn-strmif-idvdinfo2) podem retornar qualquer código de identificador.) Um identificador de estrutura descreve uma parte lógica do DVD, como volume, título ou parte do título (PTT).</span><span class="sxs-lookup"><span data-stu-id="5e451-140">(The **DVD\_TextStringType** enumeration defines a subset of the most common identifiers, but the [**IDvdInfo2**](/windows/desktop/api/Strmif/nn-strmif-idvdinfo2) methods can return any identifier code.) A structure identifier describes a logical portion of the DVD, such as volume, title, or part of title (PTT).</span></span> <span data-ttu-id="5e451-141">Um identificador de conteúdo indica o significado de uma cadeia de texto específica, como título do filme, título da música ou gênero.</span><span class="sxs-lookup"><span data-stu-id="5e451-141">A content identifier indicates the meaning of a particular text string, such as movie title, song title, or genre.</span></span>

<span data-ttu-id="5e451-142">Os identificadores de estrutura não têm cadeias de caracteres de texto associadas.</span><span class="sxs-lookup"><span data-stu-id="5e451-142">Structure identifiers do not have associated text strings.</span></span> <span data-ttu-id="5e451-143">Quando um identificador de estrutura aparece nos dados de cadeia de caracteres de texto, ele sinaliza que as cadeias de texto a seguir se aplicam à parte lógica do DVD até o próximo identificador de estrutura.</span><span class="sxs-lookup"><span data-stu-id="5e451-143">When a structure identifier appears in the text-string data, it signals that the following text strings apply to that logical portion of the DVD, up until the next structure identifier.</span></span> <span data-ttu-id="5e451-144">A posição dos identificadores de estrutura dentro dos dados de texto corresponde à hierarquia lógica do volume de DVD.</span><span class="sxs-lookup"><span data-stu-id="5e451-144">The position of the structure identifiers within the text data corresponds to the logical hierarchy of the DVD volume.</span></span> <span data-ttu-id="5e451-145">Por exemplo, a primeira ocorrência do identificador de \_ título de struct \_ (0x02) do DVD representa o primeiro título do volume e a próxima ocorrência representa o segundo título.</span><span class="sxs-lookup"><span data-stu-id="5e451-145">For example, the first occurrence of the DVD\_Struct\_Title identifier (0x02) represents the first title in the volume, and the next occurrence represents the second title.</span></span>

<span data-ttu-id="5e451-146">A tabela a seguir mostra como as cadeias de caracteres de texto podem ser definidas para um DVD com dois títulos.</span><span class="sxs-lookup"><span data-stu-id="5e451-146">The following table shows how the text strings might be defined for a DVD with two titles.</span></span>



| <span data-ttu-id="5e451-147">Cadeia de caracteres de DVD \_</span><span class="sxs-lookup"><span data-stu-id="5e451-147">DVD\_TextStringType</span></span>        | <span data-ttu-id="5e451-148">Cadeia de caracteres de texto</span><span class="sxs-lookup"><span data-stu-id="5e451-148">Text string</span></span>  | <span data-ttu-id="5e451-149">Description</span><span class="sxs-lookup"><span data-stu-id="5e451-149">Description</span></span>                                    |
|----------------------------|--------------|------------------------------------------------|
| <span data-ttu-id="5e451-150">\_ \_ Volume de struct de DVD (0x01)</span><span class="sxs-lookup"><span data-stu-id="5e451-150">DVD\_Struct\_Volume (0x01)</span></span> | <span data-ttu-id="5e451-151">""</span><span class="sxs-lookup"><span data-stu-id="5e451-151">""</span></span>           | <span data-ttu-id="5e451-152">Identificador de estrutura para todo o lado do disco.</span><span class="sxs-lookup"><span data-stu-id="5e451-152">Structure identifier for the entire disc side.</span></span> |
| <span data-ttu-id="5e451-153">\_Nome geral \_ do DVD (0x30)</span><span class="sxs-lookup"><span data-stu-id="5e451-153">DVD\_General\_Name (0x30)</span></span>  | <span data-ttu-id="5e451-154">"Volume de DVD"</span><span class="sxs-lookup"><span data-stu-id="5e451-154">"DVD Volume"</span></span> | <span data-ttu-id="5e451-155">Nome do volume do DVD.</span><span class="sxs-lookup"><span data-stu-id="5e451-155">DVD volume name.</span></span>                               |
| <span data-ttu-id="5e451-156">\_Título da estrutura \_ do DVD (0x02)</span><span class="sxs-lookup"><span data-stu-id="5e451-156">DVD\_Struct\_Title (0x02)</span></span>  | <span data-ttu-id="5e451-157">""</span><span class="sxs-lookup"><span data-stu-id="5e451-157">""</span></span>           | <span data-ttu-id="5e451-158">Identificador de estrutura do primeiro título.</span><span class="sxs-lookup"><span data-stu-id="5e451-158">Structure identifier for the first title.</span></span>      |
| <span data-ttu-id="5e451-159">\_Nome geral \_ do DVD (0x30)</span><span class="sxs-lookup"><span data-stu-id="5e451-159">DVD\_General\_Name (0x30)</span></span>  | <span data-ttu-id="5e451-160">"Título 1"</span><span class="sxs-lookup"><span data-stu-id="5e451-160">"Title 1"</span></span>    | <span data-ttu-id="5e451-161">Nome do primeiro título.</span><span class="sxs-lookup"><span data-stu-id="5e451-161">Name of the first title.</span></span>                       |
| <span data-ttu-id="5e451-162">\_Título da estrutura \_ do DVD (0x02)</span><span class="sxs-lookup"><span data-stu-id="5e451-162">DVD\_Struct\_Title (0x02)</span></span>  | <span data-ttu-id="5e451-163">""</span><span class="sxs-lookup"><span data-stu-id="5e451-163">""</span></span>           | <span data-ttu-id="5e451-164">Identificador de estrutura para o segundo título.</span><span class="sxs-lookup"><span data-stu-id="5e451-164">Structure identifier for the second title.</span></span>     |
| <span data-ttu-id="5e451-165">\_Nome geral \_ do DVD (0x30)</span><span class="sxs-lookup"><span data-stu-id="5e451-165">DVD\_General\_Name (0x30)</span></span>  | <span data-ttu-id="5e451-166">"Título 2"</span><span class="sxs-lookup"><span data-stu-id="5e451-166">"Title 2"</span></span>    | <span data-ttu-id="5e451-167">Nome do segundo título.</span><span class="sxs-lookup"><span data-stu-id="5e451-167">Name of the second title.</span></span>                      |



 

<span data-ttu-id="5e451-168">Os métodos [**GetDVDTextStringAsUnicode**](/windows/desktop/api/Strmif/nf-strmif-idvdinfo2-getdvdtextstringasunicode) e [**GetDVDTextStringAsNative**](/windows/desktop/api/Strmif/nf-strmif-idvdinfo2-getdvdtextstringasnative) tratam identificadores de estrutura e identificadores de conteúdo.</span><span class="sxs-lookup"><span data-stu-id="5e451-168">The [**GetDVDTextStringAsUnicode**](/windows/desktop/api/Strmif/nf-strmif-idvdinfo2-getdvdtextstringasunicode) and [**GetDVDTextStringAsNative**](/windows/desktop/api/Strmif/nf-strmif-idvdinfo2-getdvdtextstringasnative) methods treat structure identifiers and content identifiers the same.</span></span> <span data-ttu-id="5e451-169">A única diferença é que, para identificadores de estrutura, o buffer de texto associado está vazio.</span><span class="sxs-lookup"><span data-stu-id="5e451-169">The only difference is that for structure identifiers, the associated text buffer is empty.</span></span> <span data-ttu-id="5e451-170">Cabe ao aplicativo manter o controle da relação entre as cadeias de caracteres de texto e as partes lógicas do DVD.</span><span class="sxs-lookup"><span data-stu-id="5e451-170">It is up to the application to keep track of the relationship between the text strings and the logical portions of the DVD.</span></span>

<span data-ttu-id="5e451-171">O exemplo a seguir mostra como obter cadeias de caracteres de texto de um DVD.</span><span class="sxs-lookup"><span data-stu-id="5e451-171">The following example shows how to get text strings from a DVD.</span></span> <span data-ttu-id="5e451-172">Este exemplo ignora alguns detalhes que um aplicativo real exigiria.</span><span class="sxs-lookup"><span data-stu-id="5e451-172">This example ignores some details that a real application would require.</span></span> <span data-ttu-id="5e451-173">(Por exemplo, ele ignora identificadores de estrutura.) O exemplo destina-se apenas a mostrar a sequência correta de chamadas.</span><span class="sxs-lookup"><span data-stu-id="5e451-173">(For example, it ignores structure identifiers.) The example is only meant to show the correct sequence of calls.</span></span>


```C++
#define CHECK_HR(hr) if (FAILED(hr)) { goto done; }
#define SAFE_ARRAY_DELETE(x) { if (x != NULL) { delete [] x; x = NULL; } }

HRESULT GetDVDTextStrings()
{
    HRESULT hr = S_OK;
    ULONG cLangs = 0;       // Number of languages.
    ULONG cStrings = 0;     // Number of text strings.
    ULONG cchBuffer = 0;    // Buffer size.
    ULONG cchActual = 0;    // Actual string size.

    LCID lcid;              // Locale identifier.
    DVD_TextCharSet     characterSet;
    DVD_TextStringType  stringType;

    WCHAR *pszBuffer = NULL;

    CComPtr<IBaseFilter> pFilter;
    CComPtr<IDvdInfo2> pInfo;
    CComPtr<IDvdControl2> pControl;

    // Set up the DVD Navigator.
    CHECK_HR(hr = pFilter.CoCreateInstance(CLSID_DVDNavigator));
    CHECK_HR(hr = pFilter.QueryInterface(&pInfo));
    CHECK_HR(hr = pFilter.QueryInterface(&pControl));
    CHECK_HR(hr = pControl->SetDVDDirectory(NULL));

    // Find the number of text-string languages.
    CHECK_HR(hr = pInfo->GetDVDTextNumberOfLanguages(&cLangs));
    if (cLangs == 0)
    {
        return S_FALSE; // No text strings.
    }

    // Get information about the 0'th language.
    CHECK_HR(hr = pInfo->GetDVDTextLanguageInfo(
        0, &cStrings, &lcid, &characterSet));

    // First check if this character set is compatible with the 
    // GetDVDTextStringAsUnicode method.

    if (characterSet == DVD_CharSet_Unicode || 
        characterSet == DVD_CharSet_ISO646)
    {
        // Loop through all of the strings.
        for (ULONG i = 0; i < cStrings; i++)
        {
            // Get the i'th string for the 0'th language.

            // Find the required buffer size and the string type.
            CHECK_HR(hr = pInfo->GetDVDTextStringAsUnicode(
                0,            // Language index.
                i,            // String index.
                NULL,         // Pass NULL pointer to get the buffer size.
                0,            // Size of the buffer we are passing in.
                &cchBuffer,   // Receives the required buffer size.
                &stringType   // Receives the identifier code.
                ));

            // Skip structure identifiers (0x00 - 0x2F).
            if ((cchBuffer > 0) && (stringType >= 0x30))
            {
                // Allocate a buffer and get the text string.
                pszBuffer = new WCHAR[cchBuffer];
                if (pszBuffer == NULL)
                {
                    CHECK_HR(hr = E_OUTOFMEMORY);
                }

                CHECK_HR(hr = pInfo->GetDVDTextStringAsUnicode(
                    0, i, pszBuffer, cchBuffer, &cchActual, &stringType));

                // TODO: Display the text string.

                SAFE_ARRAY_DELETE(pszBuffer);
            }
        }
    }

done:
    SAFE_ARRAY_DELETE(pszBuffer);
    return hr;
}
```



<span data-ttu-id="5e451-174">Para obter informações sobre cadeias de caracteres de texto em DVD, consulte o [site do fórum de DVD](https://go.microsoft.com/fwlink/?LinkId=8677).</span><span class="sxs-lookup"><span data-stu-id="5e451-174">For information on DVD text strings, see the [DVD Forum's Web site](https://go.microsoft.com/fwlink/?LinkId=8677).</span></span>

<span data-ttu-id="5e451-175">O método **CDvdCore:: GetDvdText** no aplicativo DVDSample demonstra as etapas básicas de enumeração e exibição de cadeias de caracteres de texto em DVD.</span><span class="sxs-lookup"><span data-stu-id="5e451-175">The **CDvdCore::GetDvdText** method in the DVDSample application demonstrates the basic steps in enumerating and displaying DVD text strings.</span></span>

## <a name="related-topics"></a><span data-ttu-id="5e451-176">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="5e451-176">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5e451-177">Aplicativos de DVD</span><span class="sxs-lookup"><span data-stu-id="5e451-177">DVD Applications</span></span>](dvd-applications.md)
</dt> </dl>

 

 



