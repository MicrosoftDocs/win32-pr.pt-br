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
# <a name="working-with-dvd-text-strings"></a>Trabalhando com cadeias de caracteres de texto em DVD

Alguns discos de DVD, especialmente discos do karaokê, podem conter uma lista de cadeias de caracteres de texto para complementar o conteúdo de vídeo ou áudio. Essas cadeias de caracteres de texto contêm metadados sobre o conteúdo, como títulos de música, nomes de artistas, informações de gênero e assim por diante. As cadeias de caracteres de texto podem estar presentes em mais de um idioma. Essas cadeias de caracteres são opcionais e muitos discos não as têm.

Para recuperar cadeias de caracteres de texto de um DVD, use a interface [**IDvdInfo2**](/windows/desktop/api/Strmif/nn-strmif-idvdinfo2) , que é exposta pelo [navegador de DVD](dvd-navigator-filter.md). Na verdade, você não precisa criar um grafo de reprodução de DVD para recuperar as cadeias de caracteres de texto. Você pode simplesmente criar o navegador de DVD, definir o volume de DVD e, em seguida, chamar os métodos de cadeia de caracteres de texto relevantes:



| Método                                                                                  | Descrição                                                                                                                                                                                     |
|-----------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IDvdInfo2::GetDVDTextNumberOfLanguages**](/windows/desktop/api/Strmif/nf-strmif-idvdinfo2-getdvdtextnumberoflanguages) | Obtém o número de idiomas para os quais há cadeias de caracteres de texto.                                                                                                                                  |
| [**IDvdInfo2::GetDVDTextLanguageInfo**](/windows/desktop/api/Strmif/nf-strmif-idvdinfo2-getdvdtextlanguageinfo)           | Obtém informações sobre as cadeias de caracteres de texto para um idioma.                                                                                                                                       |
| [**IDvdInfo2::GetDVDTextStringAsUnicode**](/windows/desktop/api/Strmif/nf-strmif-idvdinfo2-getdvdtextstringasunicode)     | Obtém uma cadeia de texto para um idioma especificado, por índice.                                                                                                                                          |
| [**IDvdInfo2::GetDVDTextStringAsNative**](/windows/desktop/api/Strmif/nf-strmif-idvdinfo2-getdvdtextstringasnative)       | Obtém uma cadeia de caracteres de texto como uma matriz de bytes brutos. Use esse método se a cadeia de caracteres de texto usar uma codificação de caracteres sem suporte do [**GetDVDTextStringAsUnicode**](/windows/desktop/api/Strmif/nf-strmif-idvdinfo2-getdvdtextstringasunicode). |



 

Este é o procedimento básico para obter cadeias de texto:

1.  Chame [**IDvdInfo2:: GetDVDTextNumberOfLanguages**](/windows/desktop/api/Strmif/nf-strmif-idvdinfo2-getdvdtextnumberoflanguages) para localizar o número total de idiomas nos quais as cadeias de caracteres de texto aparecem. Se o número for zero, significa que o DVD não tem nenhuma cadeia de caracteres de texto. (Talvez esse seja o caso mais comum, na verdade).
2.  Se o número de idiomas for pelo menos um, chame [**IDvdInfo2:: GetDVDTextLanguageInfo**](/windows/desktop/api/Strmif/nf-strmif-idvdinfo2-getdvdtextlanguageinfo) para obter informações sobre cada idioma. O idioma é especificado pelo índice. O método retorna o número total de cadeias de caracteres de texto nesse idioma, o **LCID**(identificador de localidade) para o idioma e a codificação de caracteres (Unicode ou outro). Cadeias de texto em DVD podem usar vários conjuntos de caracteres diferentes; Eles são listados na [**\_ Enumeração textcharset de DVD**](/windows/desktop/api/strmif/ne-strmif-dvd_textcharset).
3.  Para obter uma cadeia de texto, chame [**IDvdInfo2:: GetDVDTextStringAsUnicode**](/windows/desktop/api/Strmif/nf-strmif-idvdinfo2-getdvdtextstringasunicode) ou [**IDvdInfo2:: GetDVDTextStringAsNative**](/windows/desktop/api/Strmif/nf-strmif-idvdinfo2-getdvdtextstringasnative). O primeiro método retorna uma cadeia de caracteres largos, mas não dá suporte a todos os conjuntos de caracteres. O segundo método retorna uma matriz de bytes que contém os dados de texto brutos. Para ambos os métodos, você pode chamar o método com um ponteiro de buffer **nulo** para localizar o tamanho da cadeia de caracteres e o tipo de texto. Em seguida, aloque um buffer e chame o método novamente para obter a cadeia de caracteres.

Cada cadeia de texto tem um código de identificador associado, que indica o significado da cadeia de texto. O identificador é retornado como um valor de [**DVD \_ textstringtype**](/windows/desktop/api/strmif/ne-strmif-dvd_textstringtype) . Há duas categorias de identificador: *identificadores de estrutura* e *identificadores de conteúdo*. Os identificadores de estrutura têm códigos numéricos no intervalo 0x00 – 0x02F. Os identificadores de conteúdo têm um intervalo de 0x30 e superior. (A **enumeração \_ textstringtype de DVD** define um subconjunto dos identificadores mais comuns, mas os métodos [**IDvdInfo2**](/windows/desktop/api/Strmif/nn-strmif-idvdinfo2) podem retornar qualquer código de identificador.) Um identificador de estrutura descreve uma parte lógica do DVD, como volume, título ou parte do título (PTT). Um identificador de conteúdo indica o significado de uma cadeia de texto específica, como título do filme, título da música ou gênero.

Os identificadores de estrutura não têm cadeias de caracteres de texto associadas. Quando um identificador de estrutura aparece nos dados de cadeia de caracteres de texto, ele sinaliza que as cadeias de texto a seguir se aplicam à parte lógica do DVD até o próximo identificador de estrutura. A posição dos identificadores de estrutura dentro dos dados de texto corresponde à hierarquia lógica do volume de DVD. Por exemplo, a primeira ocorrência do identificador de \_ título de struct \_ (0x02) do DVD representa o primeiro título do volume e a próxima ocorrência representa o segundo título.

A tabela a seguir mostra como as cadeias de caracteres de texto podem ser definidas para um DVD com dois títulos.



| Cadeia de caracteres de DVD \_        | Cadeia de caracteres de texto  | Description                                    |
|----------------------------|--------------|------------------------------------------------|
| \_ \_ Volume de struct de DVD (0x01) | ""           | Identificador de estrutura para todo o lado do disco. |
| \_Nome geral \_ do DVD (0x30)  | "Volume de DVD" | Nome do volume do DVD.                               |
| \_Título da estrutura \_ do DVD (0x02)  | ""           | Identificador de estrutura do primeiro título.      |
| \_Nome geral \_ do DVD (0x30)  | "Título 1"    | Nome do primeiro título.                       |
| \_Título da estrutura \_ do DVD (0x02)  | ""           | Identificador de estrutura para o segundo título.     |
| \_Nome geral \_ do DVD (0x30)  | "Título 2"    | Nome do segundo título.                      |



 

Os métodos [**GetDVDTextStringAsUnicode**](/windows/desktop/api/Strmif/nf-strmif-idvdinfo2-getdvdtextstringasunicode) e [**GetDVDTextStringAsNative**](/windows/desktop/api/Strmif/nf-strmif-idvdinfo2-getdvdtextstringasnative) tratam identificadores de estrutura e identificadores de conteúdo. A única diferença é que, para identificadores de estrutura, o buffer de texto associado está vazio. Cabe ao aplicativo manter o controle da relação entre as cadeias de caracteres de texto e as partes lógicas do DVD.

O exemplo a seguir mostra como obter cadeias de caracteres de texto de um DVD. Este exemplo ignora alguns detalhes que um aplicativo real exigiria. (Por exemplo, ele ignora identificadores de estrutura.) O exemplo destina-se apenas a mostrar a sequência correta de chamadas.


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



Para obter informações sobre cadeias de caracteres de texto em DVD, consulte o [site do fórum de DVD](https://go.microsoft.com/fwlink/?LinkId=8677).

O método **CDvdCore:: GetDvdText** no aplicativo DVDSample demonstra as etapas básicas de enumeração e exibição de cadeias de caracteres de texto em DVD.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Aplicativos de DVD](dvd-applications.md)
</dt> </dl>

 

 



